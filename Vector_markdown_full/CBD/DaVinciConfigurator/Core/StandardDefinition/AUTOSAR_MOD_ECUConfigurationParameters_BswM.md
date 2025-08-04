# BswM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:06

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [BswM](#bswm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. BswM

#### 基本信息

- **UUID**: `ECUC:98c4844c-a16a-4b8b-9928-d9846dcb2d25`
- **模块名称**: `BswM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the BswM (Basic SW Mode Manager) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **58** 个配置容器：

##### 1. BswMConfig

**容器属性**:

- **UUID**: `ECUC:80f40234-216b-48cd-a96c-4eeab986d79c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMConfig`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR BswM module. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 配置容器

本模块包含 **55** 个配置容器：

####### 1. BswMArbitration

**容器属性**:

- **UUID**: `ECUC:1bb152a0-b36c-460c-bada-c3347399266e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMArbitration`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container includes all configuration sub-containers and parameters related to the mode arbitration functionality of the BswM.

######## 配置容器

本模块包含 **30** 个配置容器：

######### 1. BswMLogicalExpression

**容器属性**:

- **UUID**: `ECUC:24badaf3-6672-43f0-b3b0-3343c67796e6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLogicalExpression`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the logical expressions that can be used for the mode arbitration. The logical expressions are built of a set of arguments and a logical operator.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMLogicalOperator

- **UUID**: `ECUC:71652a7c-9360-42b3-9432-2cd58bfe7949`
- **参数名**: `BswMLogicalOperator`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_AND` (来源: AUTOSAR_ECUC)
  - `BSWM_NAND` (来源: AUTOSAR_ECUC)
  - `BSWM_OR` (来源: AUTOSAR_ECUC)
  - `BSWM_XOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the logical operator to be used in the logical expression. If the expression only consists of a single condition this parameter shall not be used.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. BswMArgumentRef

- **UUID**: `ECUC:509833cd-a9df-4ffb-ba49-a4fea4761bf3`
- **引用名**: `BswMArgumentRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMLogicalExpression`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMModeCondition`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a choice reference either to a mode condition or a sub-expression.

######### 2. BswMModeCondition

**容器属性**:

- **UUID**: `ECUC:55038f0f-7e6c-49bf-a155-df75c068efe5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeCondition`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the BswM mode conditions that can be used either by itself to form a rule or as a part of a logical expression.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMConditionType

- **UUID**: `ECUC:4f137728-854d-4d76-aa9c-311449567f09`
- **参数名**: `BswMConditionType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_EQUALS` (来源: AUTOSAR_ECUC)
  - `BSWM_EQUALS_NOT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies what kind of comparison that is made for the evaluation of the mode condition.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. BswMConditionMode

- **UUID**: `ECUC:6a6a7ef5-77b2-4220-b440-3c7ad95e6237`
- **引用名**: `BswMConditionMode`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMModeRequestPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMModeRequestPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references the mode request port that is used for the condition.

########## 配置容器

本模块包含 **3** 个配置容器：

########### 1. BswMBswMode

**容器属性**:

- **UUID**: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the value and type of a mode in the BSW.

############ 参数配置

此容器包含 **1** 个参数：

############# STRING 类型参数

############## 1. BswMBswRequestedMode

- **UUID**: `ECUC:04a0b0ee-322c-48dc-a12d-2287e87e2e44`
- **参数名**: `BswMBswRequestedMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the symbolic name (as a string) of a certain mode/state that can be requested/indicated by the BSW modules.

########### 2. BswMModeDeclaration

**容器属性**:

- **UUID**: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeDeclaration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

############ 引用关系

此容器包含 **1** 个引用：

############# FOREIGN-REFERENCE 类型引用

############## 1. BswMModeValueRef

- **UUID**: `ECUC:16d03c04-047d-4b09-b573-5986fdeff4ed`
- **引用名**: `BswMModeValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the mode requests corresponding to this condition.

########### 3. BswMConditionValue

**容器属性**:

- **UUID**: `ECUC:6dfef60d-1d6f-4b42-a4ae-f32d9a3df94f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMConditionValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswMode**
  - UUID: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
  - 描述: This container defines the value and type of a mode in the BSW.
- **BswMModeDeclaration**
  - UUID: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
  - 描述: When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

**容器描述**:

This container holds the parameters and references necessary to identify the mode type and the value that the mode request is compared to.

######### 3. BswMBswMode

**容器属性**:

- **UUID**: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the value and type of a mode in the BSW.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMBswRequestedMode

- **UUID**: `ECUC:04a0b0ee-322c-48dc-a12d-2287e87e2e44`
- **参数名**: `BswMBswRequestedMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the symbolic name (as a string) of a certain mode/state that can be requested/indicated by the BSW modules.

######### 4. BswMModeDeclaration

**容器属性**:

- **UUID**: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeDeclaration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMModeValueRef

- **UUID**: `ECUC:16d03c04-047d-4b09-b573-5986fdeff4ed`
- **引用名**: `BswMModeValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the mode requests corresponding to this condition.

######### 5. BswMModeRequestPort

**容器属性**:

- **UUID**: `ECUC:46239dbf-b616-4d8e-be72-4e2f06f0c7df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeRequestPort`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container defines a mode request interface that is used to requests or indicate modes from/to the BswM. These interfaces are implemented as ports or as ordinary C-functions based upon if the request is made by an SW-C or a BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMRequestProcessing

- **UUID**: `ECUC:a853591d-e671-4863-aa10-0082efe4dda1`
- **参数名**: `BswMRequestProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_DEFERRED` (来源: AUTOSAR_ECUC)
  - `BSWM_IMMEDIATE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the processing of the mode arbitration shall be done immediately when a mode request is received or if it shall be deferred to the processing of the main function of BswM.

########## 配置容器

本模块包含 **23** 个配置容器：

########### 1. BswMBswModeInitValue

**容器属性**:

- **UUID**: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.

############ 参数配置

此容器包含 **1** 个参数：

############# STRING 类型参数

############## 1. BswMBswModeInitValueMode

- **UUID**: `ECUC:ce82e9c7-09eb-4a12-8e46-aaa2333a3fb7`
- **参数名**: `BswMBswModeInitValueMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the initial mode value that is used by BswM for the corresponding mode request after initialization.

########### 2. BswMSwcModeInitValue

**容器属性**:

- **UUID**: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

############ 引用关系

此容器包含 **1** 个引用：

############# FOREIGN-REFERENCE 类型引用

############## 1. BswMSwcModeInitValueRef

- **UUID**: `ECUC:087f03c1-56f6-4fdf-bba4-1050c4d08f8a`
- **引用名**: `BswMSwcModeInitValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the initialization of mode requests.

########### 3. BswMBswModeNotification

**容器属性**:

- **UUID**: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a Bsw Module.

############ 引用关系

此容器包含 **1** 个引用：

############# FOREIGN-REFERENCE 类型引用

############## 1. BswMBswModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:d1c204e5-6c8a-45e9-a191-7cc780db6f12`
- **引用名**: `BswMBswModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration Group Prototype.

########### 4. BswMCanSMIndication

**容器属性**:

- **UUID**: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMCanSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the CAN State Manager.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMCanSMChannelRef

- **UUID**: `ECUC:45faeefb-4d0e-4a75-bac3-3fe76ff15822`
- **引用名**: `BswMCanSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the CAN channel handle that the mode request corresponds to.

########### 5. BswMComMIndication

**容器属性**:

- **UUID**: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current communication mode of a channel in the Communication Manager.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMComMChannelRef

- **UUID**: `ECUC:4ad44a4c-b49e-4bff-99ef-aa813a13ee6e`
- **引用名**: `BswMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager channel handle that the indication corresponds to.

########### 6. BswMComMPncRequest

**容器属性**:

- **UUID**: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMPncRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMComMPncRef

- **UUID**: `ECUC:7b2f53bf-0115-4dc2-bd73-2ad6a4eac383`
- **引用名**: `BswMComMPncRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager PNC handle of the Partial Network Cluster that the request corresponds to.

########### 7. BswMDcmApplicationUpdatedIndication

**容器属性**:

- **UUID**: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmApplicationUpdatedIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.

########### 8. BswMDcmComModeRequest

**容器属性**:

- **UUID**: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmComModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is the Diagnostic Communication Manager.

############ 参数配置

此容器包含 **1** 个参数：

############# STRING 类型参数

############## 1. BswMDcmComMNetwork

- **UUID**: `ECUC:2bd12696-b9c4-49a7-bec0-b38cf1de1d05`
- **参数名**: `BswMDcmComMNetwork`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the network the request relates to.

########### 9. BswMEcuMIndication

**容器属性**:

- **UUID**: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.

########### 10. BswMEcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMWakeupSource`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current state of an ECU State Manager wakeup source.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMEcuMWakeupSrcRef

- **UUID**: `ECUC:c11bd4c1-5ed5-4ed5-8d1d-4d1370aeef89`
- **引用名**: `BswMEcuMWakeupSrcRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ECU State Manager Wakeup Source that the indication corresponds to.

########### 11. BswMEthSMIndication

**容器属性**:

- **UUID**: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEthSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the Ethernet State Manager.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMEthSMChannelRef

- **UUID**: `ECUC:1276bcab-5dc0-4704-b50b-7b714bdcbf4a`
- **引用名**: `BswMEthSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Ethernet channel handle that the mode request corresponds to.

########### 12. BswMFrSMIndication

**容器属性**:

- **UUID**: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMFrSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the FlexRay State Manager.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMFrSMChannelRef

- **UUID**: `ECUC:58be722e-6d43-4ed1-b1f0-441da75ea1cc`
- **引用名**: `BswMFrSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the  FlexRay Cluster handle that the mode request corresponds to.

########### 13. BswMGenericRequest

**容器属性**:

- **UUID**: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMGenericRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. BswMModeRequesterId

- **UUID**: `ECUC:418ab994-a918-4944-ad81-e4720ddd8b56`
- **参数名**: `BswMModeRequesterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameters identifies the different users of the generic mode request interface.

############## 2. BswMRequestedModeMax

- **UUID**: `ECUC:5a53cdcf-97de-4ac2-9526-ecc1e037bad0`
- **参数名**: `BswMRequestedModeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper limit for the modes requested by this mode requester.

########### 14. BswMLinSMIndication

**容器属性**:

- **UUID**: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the LIN State Manager.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMLinSMChannelRef

- **UUID**: `ECUC:806494fe-5721-4700-9aff-afb9b96842f4`
- **引用名**: `BswMLinSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN channel handle that the mode request corresponds to.

########### 15. BswMLinScheduleIndication

**容器属性**:

- **UUID**: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMLinScheduleRef

- **UUID**: `ECUC:a377f06e-9872-4bba-9040-e413f8949261`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Schedule Table handle that the mode request corresponds to.

########### 16. BswMLinTpModeRequest

**容器属性**:

- **UUID**: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinTpModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMLinTpChannelRef

- **UUID**: `ECUC:2d8c4b55-134e-4e91-8aa2-8990b56a74c3`
- **引用名**: `BswMLinTpChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Interface Channel that the mode

########### 17. BswMNvMJobModeIndication

**容器属性**:

- **UUID**: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMJobModeIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:

############ 参数配置

此容器包含 **1** 个参数：

############# ENUMERATION 类型参数

############## 1. BswMNvmService

- **UUID**: `ECUC:ac4b5a2a-a386-4bb4-b7b8-58a5baaefe2c`
- **参数名**: `BswMNvmService`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NvmReadAll` (来源: AUTOSAR_ECUC)
  - `NvmWriteAll` (来源: AUTOSAR_ECUC)
- **描述**: Identifies the Nvm job which is related to the mode request.

########### 18. BswMNvMRequest

**容器属性**:

- **UUID**: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMNvMBlockRef

- **UUID**: `ECUC:63b81990-3e16-437b-84f5-08451acf7709`
- **引用名**: `BswMNvMBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the NvM Block Descriptor that the request corresponds to.

########### 19. BswMSwcModeNotification

**容器属性**:

- **UUID**: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a mode switch notification associated with a RTE switch interface.

############ 引用关系

此容器包含 **1** 个引用：

############# FOREIGN-REFERENCE 类型引用

############## 1. BswMSwcModeNotificationModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:5aa3f84f-623b-4f8a-846d-b0f2f8506bd5`
- **引用名**: `BswMSwcModeNotificationModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype.

########### 20. BswMSwcModeRequest

**容器属性**:

- **UUID**: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a SW Component.

############ 引用关系

此容器包含 **1** 个引用：

############# FOREIGN-REFERENCE 类型引用

############## 1. BswMSwcModeRequestModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:106e96eb-0779-4153-b2f9-b05730aa991a`
- **引用名**: `BswMSwcModeRequestModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype. As the mode request is SR-Communication the BswM shall provide a SR-Interface which corresponds to the ModeDeclarationGroupPrototype.

########### 21. BswMWdgMRequestPartitionReset

**容器属性**:

- **UUID**: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMWdgMRequestPartitionReset`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a Partition Reset request from from the WdgM. This port

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. BswMWdgMRequestPartitionResetRef

- **UUID**: `ECUC:6770d76c-a522-43c4-961f-26d1d6e61afa`
- **引用名**: `BswMWdgMRequestPartitionResetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the partition that shall be reset.

########### 22. BswMModeInitValue

**容器属性**:

- **UUID**: `ECUC:a780195c-9698-494b-810e-d6f1b56cef30`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeInitValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswModeInitValue**
  - UUID: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
  - 描述: This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.
- **BswMSwcModeInitValue**
  - UUID: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
  - 描述: This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

**容器描述**:

This container defines the initial mode value that is used by BswM for the corresponding mode request after initialization. This container is optional and shall only be used for Mode Requests that do not already have an initial value.

########### 23. BswMModeRequestSource

**容器属性**:

- **UUID**: `ECUC:dd5d5587-bfd1-4960-a654-bcbc222aca93`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeRequestSource`
- **多重性**: [1..1]

**容器选择**:

- **BswMBswModeNotification**
  - UUID: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
  - 描述: The source of the mode request is a Bsw Module.
- **BswMCanSMIndication**
  - UUID: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
  - 描述: This is an indication of the current state of the CAN State Manager.
- **BswMComMIndication**
  - UUID: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
  - 描述: This is an indication of the current communication mode of a channel in the Communication Manager.
- **BswMComMPncRequest**
  - UUID: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
  - 描述: This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.
- **BswMDcmApplicationUpdatedIndication**
  - UUID: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
  - 描述: This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMDcmComModeRequest**
  - UUID: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
  - 描述: The source of the mode request is the Diagnostic Communication Manager.
- **BswMEcuMIndication**
  - UUID: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
  - 描述: This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMEcuMWakeupSource**
  - UUID: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
  - 描述: This is a notification of the current state of an ECU State Manager wakeup source.
- **BswMEthSMIndication**
  - UUID: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
  - 描述: This is an indication of the current state of the Ethernet State Manager.
- **BswMFrSMIndication**
  - UUID: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
  - 描述: This is an indication of the current state of the FlexRay State Manager.
- **BswMGenericRequest**
  - UUID: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
  - 描述: This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).
- **BswMLinSMIndication**
  - UUID: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
  - 描述: This is an indication of the current state of the LIN State Manager.
- **BswMLinScheduleIndication**
  - UUID: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
  - 描述: This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.
- **BswMLinTpModeRequest**
  - UUID: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
  - 描述: This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.
- **BswMNvMJobModeIndication**
  - UUID: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
  - 描述: Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:
- **BswMNvMRequest**
  - UUID: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
  - 描述: Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:
- **BswMSwcModeNotification**
  - UUID: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
  - 描述: This is a mode switch notification associated with a RTE switch interface.
- **BswMSwcModeRequest**
  - UUID: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
  - 描述: The source of the mode request is a SW Component.
- **BswMWdgMRequestPartitionReset**
  - UUID: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
  - 描述: This is a Partition Reset request from from the WdgM. This port

**容器描述**:

This choice container specifies the source of the mode request or state/mode indication. The requester of a mode can be both SW-C:s and other BSW Modules, such as the bus specific State Managers.

######### 6. BswMBswModeInitValue

**容器属性**:

- **UUID**: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMBswModeInitValueMode

- **UUID**: `ECUC:ce82e9c7-09eb-4a12-8e46-aaa2333a3fb7`
- **参数名**: `BswMBswModeInitValueMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the initial mode value that is used by BswM for the corresponding mode request after initialization.

######### 7. BswMSwcModeInitValue

**容器属性**:

- **UUID**: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwcModeInitValueRef

- **UUID**: `ECUC:087f03c1-56f6-4fdf-bba4-1050c4d08f8a`
- **引用名**: `BswMSwcModeInitValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the initialization of mode requests.

######### 8. BswMBswModeNotification

**容器属性**:

- **UUID**: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a Bsw Module.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMBswModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:d1c204e5-6c8a-45e9-a191-7cc780db6f12`
- **引用名**: `BswMBswModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration Group Prototype.

######### 9. BswMCanSMIndication

**容器属性**:

- **UUID**: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMCanSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the CAN State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMCanSMChannelRef

- **UUID**: `ECUC:45faeefb-4d0e-4a75-bac3-3fe76ff15822`
- **引用名**: `BswMCanSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the CAN channel handle that the mode request corresponds to.

######### 10. BswMComMIndication

**容器属性**:

- **UUID**: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current communication mode of a channel in the Communication Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMChannelRef

- **UUID**: `ECUC:4ad44a4c-b49e-4bff-99ef-aa813a13ee6e`
- **引用名**: `BswMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager channel handle that the indication corresponds to.

######### 11. BswMComMPncRequest

**容器属性**:

- **UUID**: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMPncRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMPncRef

- **UUID**: `ECUC:7b2f53bf-0115-4dc2-bd73-2ad6a4eac383`
- **引用名**: `BswMComMPncRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager PNC handle of the Partial Network Cluster that the request corresponds to.

######### 12. BswMDcmApplicationUpdatedIndication

**容器属性**:

- **UUID**: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmApplicationUpdatedIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.

######### 13. BswMDcmComModeRequest

**容器属性**:

- **UUID**: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmComModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is the Diagnostic Communication Manager.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMDcmComMNetwork

- **UUID**: `ECUC:2bd12696-b9c4-49a7-bec0-b38cf1de1d05`
- **参数名**: `BswMDcmComMNetwork`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the network the request relates to.

######### 14. BswMEcuMIndication

**容器属性**:

- **UUID**: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.

######### 15. BswMEcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMWakeupSource`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current state of an ECU State Manager wakeup source.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEcuMWakeupSrcRef

- **UUID**: `ECUC:c11bd4c1-5ed5-4ed5-8d1d-4d1370aeef89`
- **引用名**: `BswMEcuMWakeupSrcRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ECU State Manager Wakeup Source that the indication corresponds to.

######### 16. BswMEthSMIndication

**容器属性**:

- **UUID**: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEthSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the Ethernet State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEthSMChannelRef

- **UUID**: `ECUC:1276bcab-5dc0-4704-b50b-7b714bdcbf4a`
- **引用名**: `BswMEthSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Ethernet channel handle that the mode request corresponds to.

######### 17. BswMFrSMIndication

**容器属性**:

- **UUID**: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMFrSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the FlexRay State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMFrSMChannelRef

- **UUID**: `ECUC:58be722e-6d43-4ed1-b1f0-441da75ea1cc`
- **引用名**: `BswMFrSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the  FlexRay Cluster handle that the mode request corresponds to.

######### 18. BswMGenericRequest

**容器属性**:

- **UUID**: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMGenericRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. BswMModeRequesterId

- **UUID**: `ECUC:418ab994-a918-4944-ad81-e4720ddd8b56`
- **参数名**: `BswMModeRequesterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameters identifies the different users of the generic mode request interface.

############ 2. BswMRequestedModeMax

- **UUID**: `ECUC:5a53cdcf-97de-4ac2-9526-ecc1e037bad0`
- **参数名**: `BswMRequestedModeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper limit for the modes requested by this mode requester.

######### 19. BswMLinSMIndication

**容器属性**:

- **UUID**: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the LIN State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinSMChannelRef

- **UUID**: `ECUC:806494fe-5721-4700-9aff-afb9b96842f4`
- **引用名**: `BswMLinSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN channel handle that the mode request corresponds to.

######### 20. BswMLinScheduleIndication

**容器属性**:

- **UUID**: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinScheduleRef

- **UUID**: `ECUC:a377f06e-9872-4bba-9040-e413f8949261`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Schedule Table handle that the mode request corresponds to.

######### 21. BswMLinTpModeRequest

**容器属性**:

- **UUID**: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinTpModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinTpChannelRef

- **UUID**: `ECUC:2d8c4b55-134e-4e91-8aa2-8990b56a74c3`
- **引用名**: `BswMLinTpChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Interface Channel that the mode

######### 22. BswMNvMJobModeIndication

**容器属性**:

- **UUID**: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMJobModeIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMNvmService

- **UUID**: `ECUC:ac4b5a2a-a386-4bb4-b7b8-58a5baaefe2c`
- **参数名**: `BswMNvmService`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NvmReadAll` (来源: AUTOSAR_ECUC)
  - `NvmWriteAll` (来源: AUTOSAR_ECUC)
- **描述**: Identifies the Nvm job which is related to the mode request.

######### 23. BswMNvMRequest

**容器属性**:

- **UUID**: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMNvMBlockRef

- **UUID**: `ECUC:63b81990-3e16-437b-84f5-08451acf7709`
- **引用名**: `BswMNvMBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the NvM Block Descriptor that the request corresponds to.

######### 24. BswMSwcModeNotification

**容器属性**:

- **UUID**: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a mode switch notification associated with a RTE switch interface.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwcModeNotificationModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:5aa3f84f-623b-4f8a-846d-b0f2f8506bd5`
- **引用名**: `BswMSwcModeNotificationModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype.

######### 25. BswMSwcModeRequest

**容器属性**:

- **UUID**: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a SW Component.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwcModeRequestModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:106e96eb-0779-4153-b2f9-b05730aa991a`
- **引用名**: `BswMSwcModeRequestModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype. As the mode request is SR-Communication the BswM shall provide a SR-Interface which corresponds to the ModeDeclarationGroupPrototype.

######### 26. BswMWdgMRequestPartitionReset

**容器属性**:

- **UUID**: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMWdgMRequestPartitionReset`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a Partition Reset request from from the WdgM. This port

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. BswMWdgMRequestPartitionResetRef

- **UUID**: `ECUC:6770d76c-a522-43c4-961f-26d1d6e61afa`
- **引用名**: `BswMWdgMRequestPartitionResetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the partition that shall be reset.

######### 27. BswMRule

**容器属性**:

- **UUID**: `ECUC:9711550f-8c6a-4c9d-a1bd-b6d3828a9ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRule`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container describes a BswM arbitration rule. The rule either consists of a simple mode condition or a more complex logical expression. This container also references the action lists that shall be invoked when the rule is evaluated to True or False.

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMNestedExecutionOnly

- **UUID**: `ECUC:75ab5231-5ebb-4aec-a088-bc956ba35023`
- **参数名**: `BswMNestedExecutionOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines for its related Rule if the Rule is an Independent rule or a Subordinate rule;

########### ENUMERATION 类型参数

############ 1. BswMRuleInitState

- **UUID**: `ECUC:42592c03-2e60-4cb0-8357-5a711cba0547`
- **参数名**: `BswMRuleInitState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FALSE` (来源: AUTOSAR_ECUC)
  - `BSWM_TRUE` (来源: AUTOSAR_ECUC)
  - `BSWM_UNDEFINED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a part of the reset/initialization behavior of BswM.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. BswMRuleExpressionRef

- **UUID**: `ECUC:f734f4cd-0746-4a1b-85b4-2791ac9d910e`
- **引用名**: `BswMRuleExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMLogicalExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMLogicalExpression`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This choice reference either references the mode condition or the logical expression that is evaluated for each rule.

############ 2. BswMRuleFalseActionList

- **UUID**: `ECUC:cd76267f-738a-4738-ac2c-7b7d38b31ffa`
- **引用名**: `BswMRuleFalseActionList`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `BswMActionList`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the action list that shall be executed when the rule is evaluated to False

############ 3. BswMRuleTrueActionList

- **UUID**: `ECUC:309d8777-fea3-4ded-a73e-980296f093aa`
- **引用名**: `BswMRuleTrueActionList`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `BswMActionList`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the action list that shall be executed when the rule is evaluated to True

######### 28. BswMConditionValue

**容器属性**:

- **UUID**: `ECUC:6dfef60d-1d6f-4b42-a4ae-f32d9a3df94f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMConditionValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswMode**
  - UUID: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
  - 描述: This container defines the value and type of a mode in the BSW.
- **BswMModeDeclaration**
  - UUID: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
  - 描述: When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

**容器描述**:

This container holds the parameters and references necessary to identify the mode type and the value that the mode request is compared to.

######### 29. BswMModeInitValue

**容器属性**:

- **UUID**: `ECUC:a780195c-9698-494b-810e-d6f1b56cef30`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeInitValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswModeInitValue**
  - UUID: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
  - 描述: This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.
- **BswMSwcModeInitValue**
  - UUID: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
  - 描述: This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

**容器描述**:

This container defines the initial mode value that is used by BswM for the corresponding mode request after initialization. This container is optional and shall only be used for Mode Requests that do not already have an initial value.

######### 30. BswMModeRequestSource

**容器属性**:

- **UUID**: `ECUC:dd5d5587-bfd1-4960-a654-bcbc222aca93`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeRequestSource`
- **多重性**: [1..1]

**容器选择**:

- **BswMBswModeNotification**
  - UUID: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
  - 描述: The source of the mode request is a Bsw Module.
- **BswMCanSMIndication**
  - UUID: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
  - 描述: This is an indication of the current state of the CAN State Manager.
- **BswMComMIndication**
  - UUID: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
  - 描述: This is an indication of the current communication mode of a channel in the Communication Manager.
- **BswMComMPncRequest**
  - UUID: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
  - 描述: This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.
- **BswMDcmApplicationUpdatedIndication**
  - UUID: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
  - 描述: This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMDcmComModeRequest**
  - UUID: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
  - 描述: The source of the mode request is the Diagnostic Communication Manager.
- **BswMEcuMIndication**
  - UUID: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
  - 描述: This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMEcuMWakeupSource**
  - UUID: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
  - 描述: This is a notification of the current state of an ECU State Manager wakeup source.
- **BswMEthSMIndication**
  - UUID: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
  - 描述: This is an indication of the current state of the Ethernet State Manager.
- **BswMFrSMIndication**
  - UUID: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
  - 描述: This is an indication of the current state of the FlexRay State Manager.
- **BswMGenericRequest**
  - UUID: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
  - 描述: This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).
- **BswMLinSMIndication**
  - UUID: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
  - 描述: This is an indication of the current state of the LIN State Manager.
- **BswMLinScheduleIndication**
  - UUID: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
  - 描述: This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.
- **BswMLinTpModeRequest**
  - UUID: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
  - 描述: This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.
- **BswMNvMJobModeIndication**
  - UUID: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
  - 描述: Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:
- **BswMNvMRequest**
  - UUID: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
  - 描述: Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:
- **BswMSwcModeNotification**
  - UUID: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
  - 描述: This is a mode switch notification associated with a RTE switch interface.
- **BswMSwcModeRequest**
  - UUID: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
  - 描述: The source of the mode request is a SW Component.
- **BswMWdgMRequestPartitionReset**
  - UUID: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
  - 描述: This is a Partition Reset request from from the WdgM. This port

**容器描述**:

This choice container specifies the source of the mode request or state/mode indication. The requester of a mode can be both SW-C:s and other BSW Modules, such as the bus specific State Managers.

####### 2. BswMLogicalExpression

**容器属性**:

- **UUID**: `ECUC:24badaf3-6672-43f0-b3b0-3343c67796e6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLogicalExpression`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the logical expressions that can be used for the mode arbitration. The logical expressions are built of a set of arguments and a logical operator.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMLogicalOperator

- **UUID**: `ECUC:71652a7c-9360-42b3-9432-2cd58bfe7949`
- **参数名**: `BswMLogicalOperator`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_AND` (来源: AUTOSAR_ECUC)
  - `BSWM_NAND` (来源: AUTOSAR_ECUC)
  - `BSWM_OR` (来源: AUTOSAR_ECUC)
  - `BSWM_XOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the logical operator to be used in the logical expression. If the expression only consists of a single condition this parameter shall not be used.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. BswMArgumentRef

- **UUID**: `ECUC:509833cd-a9df-4ffb-ba49-a4fea4761bf3`
- **引用名**: `BswMArgumentRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMLogicalExpression`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMModeCondition`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a choice reference either to a mode condition or a sub-expression.

####### 3. BswMModeCondition

**容器属性**:

- **UUID**: `ECUC:55038f0f-7e6c-49bf-a155-df75c068efe5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeCondition`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the BswM mode conditions that can be used either by itself to form a rule or as a part of a logical expression.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMConditionType

- **UUID**: `ECUC:4f137728-854d-4d76-aa9c-311449567f09`
- **参数名**: `BswMConditionType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_EQUALS` (来源: AUTOSAR_ECUC)
  - `BSWM_EQUALS_NOT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies what kind of comparison that is made for the evaluation of the mode condition.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. BswMConditionMode

- **UUID**: `ECUC:6a6a7ef5-77b2-4220-b440-3c7ad95e6237`
- **引用名**: `BswMConditionMode`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMModeRequestPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMModeRequestPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references the mode request port that is used for the condition.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. BswMBswMode

**容器属性**:

- **UUID**: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the value and type of a mode in the BSW.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMBswRequestedMode

- **UUID**: `ECUC:04a0b0ee-322c-48dc-a12d-2287e87e2e44`
- **参数名**: `BswMBswRequestedMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the symbolic name (as a string) of a certain mode/state that can be requested/indicated by the BSW modules.

######### 2. BswMModeDeclaration

**容器属性**:

- **UUID**: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeDeclaration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMModeValueRef

- **UUID**: `ECUC:16d03c04-047d-4b09-b573-5986fdeff4ed`
- **引用名**: `BswMModeValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the mode requests corresponding to this condition.

######### 3. BswMConditionValue

**容器属性**:

- **UUID**: `ECUC:6dfef60d-1d6f-4b42-a4ae-f32d9a3df94f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMConditionValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswMode**
  - UUID: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
  - 描述: This container defines the value and type of a mode in the BSW.
- **BswMModeDeclaration**
  - UUID: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
  - 描述: When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

**容器描述**:

This container holds the parameters and references necessary to identify the mode type and the value that the mode request is compared to.

####### 4. BswMBswMode

**容器属性**:

- **UUID**: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the value and type of a mode in the BSW.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMBswRequestedMode

- **UUID**: `ECUC:04a0b0ee-322c-48dc-a12d-2287e87e2e44`
- **参数名**: `BswMBswRequestedMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the symbolic name (as a string) of a certain mode/state that can be requested/indicated by the BSW modules.

####### 5. BswMModeDeclaration

**容器属性**:

- **UUID**: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeDeclaration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMModeValueRef

- **UUID**: `ECUC:16d03c04-047d-4b09-b573-5986fdeff4ed`
- **引用名**: `BswMModeValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the mode requests corresponding to this condition.

####### 6. BswMModeRequestPort

**容器属性**:

- **UUID**: `ECUC:46239dbf-b616-4d8e-be72-4e2f06f0c7df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeRequestPort`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container defines a mode request interface that is used to requests or indicate modes from/to the BswM. These interfaces are implemented as ports or as ordinary C-functions based upon if the request is made by an SW-C or a BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMRequestProcessing

- **UUID**: `ECUC:a853591d-e671-4863-aa10-0082efe4dda1`
- **参数名**: `BswMRequestProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_DEFERRED` (来源: AUTOSAR_ECUC)
  - `BSWM_IMMEDIATE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the processing of the mode arbitration shall be done immediately when a mode request is received or if it shall be deferred to the processing of the main function of BswM.

######## 配置容器

本模块包含 **23** 个配置容器：

######### 1. BswMBswModeInitValue

**容器属性**:

- **UUID**: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMBswModeInitValueMode

- **UUID**: `ECUC:ce82e9c7-09eb-4a12-8e46-aaa2333a3fb7`
- **参数名**: `BswMBswModeInitValueMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the initial mode value that is used by BswM for the corresponding mode request after initialization.

######### 2. BswMSwcModeInitValue

**容器属性**:

- **UUID**: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwcModeInitValueRef

- **UUID**: `ECUC:087f03c1-56f6-4fdf-bba4-1050c4d08f8a`
- **引用名**: `BswMSwcModeInitValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the initialization of mode requests.

######### 3. BswMBswModeNotification

**容器属性**:

- **UUID**: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a Bsw Module.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMBswModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:d1c204e5-6c8a-45e9-a191-7cc780db6f12`
- **引用名**: `BswMBswModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration Group Prototype.

######### 4. BswMCanSMIndication

**容器属性**:

- **UUID**: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMCanSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the CAN State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMCanSMChannelRef

- **UUID**: `ECUC:45faeefb-4d0e-4a75-bac3-3fe76ff15822`
- **引用名**: `BswMCanSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the CAN channel handle that the mode request corresponds to.

######### 5. BswMComMIndication

**容器属性**:

- **UUID**: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current communication mode of a channel in the Communication Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMChannelRef

- **UUID**: `ECUC:4ad44a4c-b49e-4bff-99ef-aa813a13ee6e`
- **引用名**: `BswMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager channel handle that the indication corresponds to.

######### 6. BswMComMPncRequest

**容器属性**:

- **UUID**: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMPncRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMPncRef

- **UUID**: `ECUC:7b2f53bf-0115-4dc2-bd73-2ad6a4eac383`
- **引用名**: `BswMComMPncRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager PNC handle of the Partial Network Cluster that the request corresponds to.

######### 7. BswMDcmApplicationUpdatedIndication

**容器属性**:

- **UUID**: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmApplicationUpdatedIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.

######### 8. BswMDcmComModeRequest

**容器属性**:

- **UUID**: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmComModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is the Diagnostic Communication Manager.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMDcmComMNetwork

- **UUID**: `ECUC:2bd12696-b9c4-49a7-bec0-b38cf1de1d05`
- **参数名**: `BswMDcmComMNetwork`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the network the request relates to.

######### 9. BswMEcuMIndication

**容器属性**:

- **UUID**: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.

######### 10. BswMEcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMWakeupSource`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current state of an ECU State Manager wakeup source.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEcuMWakeupSrcRef

- **UUID**: `ECUC:c11bd4c1-5ed5-4ed5-8d1d-4d1370aeef89`
- **引用名**: `BswMEcuMWakeupSrcRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ECU State Manager Wakeup Source that the indication corresponds to.

######### 11. BswMEthSMIndication

**容器属性**:

- **UUID**: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEthSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the Ethernet State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEthSMChannelRef

- **UUID**: `ECUC:1276bcab-5dc0-4704-b50b-7b714bdcbf4a`
- **引用名**: `BswMEthSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Ethernet channel handle that the mode request corresponds to.

######### 12. BswMFrSMIndication

**容器属性**:

- **UUID**: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMFrSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the FlexRay State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMFrSMChannelRef

- **UUID**: `ECUC:58be722e-6d43-4ed1-b1f0-441da75ea1cc`
- **引用名**: `BswMFrSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the  FlexRay Cluster handle that the mode request corresponds to.

######### 13. BswMGenericRequest

**容器属性**:

- **UUID**: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMGenericRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. BswMModeRequesterId

- **UUID**: `ECUC:418ab994-a918-4944-ad81-e4720ddd8b56`
- **参数名**: `BswMModeRequesterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameters identifies the different users of the generic mode request interface.

############ 2. BswMRequestedModeMax

- **UUID**: `ECUC:5a53cdcf-97de-4ac2-9526-ecc1e037bad0`
- **参数名**: `BswMRequestedModeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper limit for the modes requested by this mode requester.

######### 14. BswMLinSMIndication

**容器属性**:

- **UUID**: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the LIN State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinSMChannelRef

- **UUID**: `ECUC:806494fe-5721-4700-9aff-afb9b96842f4`
- **引用名**: `BswMLinSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN channel handle that the mode request corresponds to.

######### 15. BswMLinScheduleIndication

**容器属性**:

- **UUID**: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinScheduleRef

- **UUID**: `ECUC:a377f06e-9872-4bba-9040-e413f8949261`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Schedule Table handle that the mode request corresponds to.

######### 16. BswMLinTpModeRequest

**容器属性**:

- **UUID**: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinTpModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinTpChannelRef

- **UUID**: `ECUC:2d8c4b55-134e-4e91-8aa2-8990b56a74c3`
- **引用名**: `BswMLinTpChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Interface Channel that the mode

######### 17. BswMNvMJobModeIndication

**容器属性**:

- **UUID**: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMJobModeIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMNvmService

- **UUID**: `ECUC:ac4b5a2a-a386-4bb4-b7b8-58a5baaefe2c`
- **参数名**: `BswMNvmService`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NvmReadAll` (来源: AUTOSAR_ECUC)
  - `NvmWriteAll` (来源: AUTOSAR_ECUC)
- **描述**: Identifies the Nvm job which is related to the mode request.

######### 18. BswMNvMRequest

**容器属性**:

- **UUID**: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMNvMBlockRef

- **UUID**: `ECUC:63b81990-3e16-437b-84f5-08451acf7709`
- **引用名**: `BswMNvMBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the NvM Block Descriptor that the request corresponds to.

######### 19. BswMSwcModeNotification

**容器属性**:

- **UUID**: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a mode switch notification associated with a RTE switch interface.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwcModeNotificationModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:5aa3f84f-623b-4f8a-846d-b0f2f8506bd5`
- **引用名**: `BswMSwcModeNotificationModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype.

######### 20. BswMSwcModeRequest

**容器属性**:

- **UUID**: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a SW Component.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwcModeRequestModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:106e96eb-0779-4153-b2f9-b05730aa991a`
- **引用名**: `BswMSwcModeRequestModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype. As the mode request is SR-Communication the BswM shall provide a SR-Interface which corresponds to the ModeDeclarationGroupPrototype.

######### 21. BswMWdgMRequestPartitionReset

**容器属性**:

- **UUID**: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMWdgMRequestPartitionReset`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a Partition Reset request from from the WdgM. This port

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. BswMWdgMRequestPartitionResetRef

- **UUID**: `ECUC:6770d76c-a522-43c4-961f-26d1d6e61afa`
- **引用名**: `BswMWdgMRequestPartitionResetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the partition that shall be reset.

######### 22. BswMModeInitValue

**容器属性**:

- **UUID**: `ECUC:a780195c-9698-494b-810e-d6f1b56cef30`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeInitValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswModeInitValue**
  - UUID: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
  - 描述: This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.
- **BswMSwcModeInitValue**
  - UUID: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
  - 描述: This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

**容器描述**:

This container defines the initial mode value that is used by BswM for the corresponding mode request after initialization. This container is optional and shall only be used for Mode Requests that do not already have an initial value.

######### 23. BswMModeRequestSource

**容器属性**:

- **UUID**: `ECUC:dd5d5587-bfd1-4960-a654-bcbc222aca93`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeRequestSource`
- **多重性**: [1..1]

**容器选择**:

- **BswMBswModeNotification**
  - UUID: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
  - 描述: The source of the mode request is a Bsw Module.
- **BswMCanSMIndication**
  - UUID: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
  - 描述: This is an indication of the current state of the CAN State Manager.
- **BswMComMIndication**
  - UUID: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
  - 描述: This is an indication of the current communication mode of a channel in the Communication Manager.
- **BswMComMPncRequest**
  - UUID: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
  - 描述: This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.
- **BswMDcmApplicationUpdatedIndication**
  - UUID: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
  - 描述: This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMDcmComModeRequest**
  - UUID: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
  - 描述: The source of the mode request is the Diagnostic Communication Manager.
- **BswMEcuMIndication**
  - UUID: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
  - 描述: This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMEcuMWakeupSource**
  - UUID: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
  - 描述: This is a notification of the current state of an ECU State Manager wakeup source.
- **BswMEthSMIndication**
  - UUID: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
  - 描述: This is an indication of the current state of the Ethernet State Manager.
- **BswMFrSMIndication**
  - UUID: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
  - 描述: This is an indication of the current state of the FlexRay State Manager.
- **BswMGenericRequest**
  - UUID: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
  - 描述: This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).
- **BswMLinSMIndication**
  - UUID: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
  - 描述: This is an indication of the current state of the LIN State Manager.
- **BswMLinScheduleIndication**
  - UUID: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
  - 描述: This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.
- **BswMLinTpModeRequest**
  - UUID: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
  - 描述: This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.
- **BswMNvMJobModeIndication**
  - UUID: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
  - 描述: Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:
- **BswMNvMRequest**
  - UUID: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
  - 描述: Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:
- **BswMSwcModeNotification**
  - UUID: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
  - 描述: This is a mode switch notification associated with a RTE switch interface.
- **BswMSwcModeRequest**
  - UUID: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
  - 描述: The source of the mode request is a SW Component.
- **BswMWdgMRequestPartitionReset**
  - UUID: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
  - 描述: This is a Partition Reset request from from the WdgM. This port

**容器描述**:

This choice container specifies the source of the mode request or state/mode indication. The requester of a mode can be both SW-C:s and other BSW Modules, such as the bus specific State Managers.

####### 7. BswMBswModeInitValue

**容器属性**:

- **UUID**: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMBswModeInitValueMode

- **UUID**: `ECUC:ce82e9c7-09eb-4a12-8e46-aaa2333a3fb7`
- **参数名**: `BswMBswModeInitValueMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the initial mode value that is used by BswM for the corresponding mode request after initialization.

####### 8. BswMSwcModeInitValue

**容器属性**:

- **UUID**: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwcModeInitValueRef

- **UUID**: `ECUC:087f03c1-56f6-4fdf-bba4-1050c4d08f8a`
- **引用名**: `BswMSwcModeInitValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the initialization of mode requests.

####### 9. BswMBswModeNotification

**容器属性**:

- **UUID**: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a Bsw Module.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMBswModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:d1c204e5-6c8a-45e9-a191-7cc780db6f12`
- **引用名**: `BswMBswModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration Group Prototype.

####### 10. BswMCanSMIndication

**容器属性**:

- **UUID**: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMCanSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the CAN State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMCanSMChannelRef

- **UUID**: `ECUC:45faeefb-4d0e-4a75-bac3-3fe76ff15822`
- **引用名**: `BswMCanSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the CAN channel handle that the mode request corresponds to.

####### 11. BswMComMIndication

**容器属性**:

- **UUID**: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current communication mode of a channel in the Communication Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMChannelRef

- **UUID**: `ECUC:4ad44a4c-b49e-4bff-99ef-aa813a13ee6e`
- **引用名**: `BswMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager channel handle that the indication corresponds to.

####### 12. BswMComMPncRequest

**容器属性**:

- **UUID**: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMPncRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMPncRef

- **UUID**: `ECUC:7b2f53bf-0115-4dc2-bd73-2ad6a4eac383`
- **引用名**: `BswMComMPncRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager PNC handle of the Partial Network Cluster that the request corresponds to.

####### 13. BswMDcmApplicationUpdatedIndication

**容器属性**:

- **UUID**: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmApplicationUpdatedIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.

####### 14. BswMDcmComModeRequest

**容器属性**:

- **UUID**: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmComModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is the Diagnostic Communication Manager.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMDcmComMNetwork

- **UUID**: `ECUC:2bd12696-b9c4-49a7-bec0-b38cf1de1d05`
- **参数名**: `BswMDcmComMNetwork`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the network the request relates to.

####### 15. BswMEcuMIndication

**容器属性**:

- **UUID**: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.

####### 16. BswMEcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMWakeupSource`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current state of an ECU State Manager wakeup source.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEcuMWakeupSrcRef

- **UUID**: `ECUC:c11bd4c1-5ed5-4ed5-8d1d-4d1370aeef89`
- **引用名**: `BswMEcuMWakeupSrcRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ECU State Manager Wakeup Source that the indication corresponds to.

####### 17. BswMEthSMIndication

**容器属性**:

- **UUID**: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEthSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the Ethernet State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEthSMChannelRef

- **UUID**: `ECUC:1276bcab-5dc0-4704-b50b-7b714bdcbf4a`
- **引用名**: `BswMEthSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Ethernet channel handle that the mode request corresponds to.

####### 18. BswMFrSMIndication

**容器属性**:

- **UUID**: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMFrSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the FlexRay State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMFrSMChannelRef

- **UUID**: `ECUC:58be722e-6d43-4ed1-b1f0-441da75ea1cc`
- **引用名**: `BswMFrSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the  FlexRay Cluster handle that the mode request corresponds to.

####### 19. BswMGenericRequest

**容器属性**:

- **UUID**: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMGenericRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. BswMModeRequesterId

- **UUID**: `ECUC:418ab994-a918-4944-ad81-e4720ddd8b56`
- **参数名**: `BswMModeRequesterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameters identifies the different users of the generic mode request interface.

########## 2. BswMRequestedModeMax

- **UUID**: `ECUC:5a53cdcf-97de-4ac2-9526-ecc1e037bad0`
- **参数名**: `BswMRequestedModeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper limit for the modes requested by this mode requester.

####### 20. BswMLinSMIndication

**容器属性**:

- **UUID**: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the LIN State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinSMChannelRef

- **UUID**: `ECUC:806494fe-5721-4700-9aff-afb9b96842f4`
- **引用名**: `BswMLinSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN channel handle that the mode request corresponds to.

####### 21. BswMLinScheduleIndication

**容器属性**:

- **UUID**: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinScheduleRef

- **UUID**: `ECUC:a377f06e-9872-4bba-9040-e413f8949261`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Schedule Table handle that the mode request corresponds to.

####### 22. BswMLinTpModeRequest

**容器属性**:

- **UUID**: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinTpModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinTpChannelRef

- **UUID**: `ECUC:2d8c4b55-134e-4e91-8aa2-8990b56a74c3`
- **引用名**: `BswMLinTpChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Interface Channel that the mode

####### 23. BswMNvMJobModeIndication

**容器属性**:

- **UUID**: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMJobModeIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMNvmService

- **UUID**: `ECUC:ac4b5a2a-a386-4bb4-b7b8-58a5baaefe2c`
- **参数名**: `BswMNvmService`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NvmReadAll` (来源: AUTOSAR_ECUC)
  - `NvmWriteAll` (来源: AUTOSAR_ECUC)
- **描述**: Identifies the Nvm job which is related to the mode request.

####### 24. BswMNvMRequest

**容器属性**:

- **UUID**: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMNvMBlockRef

- **UUID**: `ECUC:63b81990-3e16-437b-84f5-08451acf7709`
- **引用名**: `BswMNvMBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the NvM Block Descriptor that the request corresponds to.

####### 25. BswMSwcModeNotification

**容器属性**:

- **UUID**: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a mode switch notification associated with a RTE switch interface.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwcModeNotificationModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:5aa3f84f-623b-4f8a-846d-b0f2f8506bd5`
- **引用名**: `BswMSwcModeNotificationModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype.

####### 26. BswMSwcModeRequest

**容器属性**:

- **UUID**: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a SW Component.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwcModeRequestModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:106e96eb-0779-4153-b2f9-b05730aa991a`
- **引用名**: `BswMSwcModeRequestModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype. As the mode request is SR-Communication the BswM shall provide a SR-Interface which corresponds to the ModeDeclarationGroupPrototype.

####### 27. BswMWdgMRequestPartitionReset

**容器属性**:

- **UUID**: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMWdgMRequestPartitionReset`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a Partition Reset request from from the WdgM. This port

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. BswMWdgMRequestPartitionResetRef

- **UUID**: `ECUC:6770d76c-a522-43c4-961f-26d1d6e61afa`
- **引用名**: `BswMWdgMRequestPartitionResetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the partition that shall be reset.

####### 28. BswMRule

**容器属性**:

- **UUID**: `ECUC:9711550f-8c6a-4c9d-a1bd-b6d3828a9ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRule`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container describes a BswM arbitration rule. The rule either consists of a simple mode condition or a more complex logical expression. This container also references the action lists that shall be invoked when the rule is evaluated to True or False.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMNestedExecutionOnly

- **UUID**: `ECUC:75ab5231-5ebb-4aec-a088-bc956ba35023`
- **参数名**: `BswMNestedExecutionOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines for its related Rule if the Rule is an Independent rule or a Subordinate rule;

######### ENUMERATION 类型参数

########## 1. BswMRuleInitState

- **UUID**: `ECUC:42592c03-2e60-4cb0-8357-5a711cba0547`
- **参数名**: `BswMRuleInitState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FALSE` (来源: AUTOSAR_ECUC)
  - `BSWM_TRUE` (来源: AUTOSAR_ECUC)
  - `BSWM_UNDEFINED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a part of the reset/initialization behavior of BswM.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. BswMRuleExpressionRef

- **UUID**: `ECUC:f734f4cd-0746-4a1b-85b4-2791ac9d910e`
- **引用名**: `BswMRuleExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMLogicalExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMLogicalExpression`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This choice reference either references the mode condition or the logical expression that is evaluated for each rule.

########## 2. BswMRuleFalseActionList

- **UUID**: `ECUC:cd76267f-738a-4738-ac2c-7b7d38b31ffa`
- **引用名**: `BswMRuleFalseActionList`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `BswMActionList`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the action list that shall be executed when the rule is evaluated to False

########## 3. BswMRuleTrueActionList

- **UUID**: `ECUC:309d8777-fea3-4ded-a73e-980296f093aa`
- **引用名**: `BswMRuleTrueActionList`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `BswMActionList`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the action list that shall be executed when the rule is evaluated to True

####### 29. BswMDataTypeMappingSets

**容器属性**:

- **UUID**: `ECUC:fd679d55-8201-4daf-8762-a432eb79cb8c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDataTypeMappingSets`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Collection of references to DataTypeMappingSet.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMDataTypeMappingSetRef

- **UUID**: `ECUC:f0b7d567-bfdf-47c7-8459-32f20d811612`
- **引用名**: `BswMDataTypeMappingSetRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: DATA-TYPE-MAPPING-SET
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DataTypeMappingSet.

####### 30. BswMModeControl

**容器属性**:

- **UUID**: `ECUC:0f9b55d8-de62-4333-96a5-061519c7ffc1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeControl`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container includes all configuration sub-containers and parameters related to the mode control functionality of the BswM.

######## 配置容器

本模块包含 **22** 个配置容器：

######### 1. BswMAction

**容器属性**:

- **UUID**: `ECUC:add00e45-e97c-4d9a-8208-befcbfbfd3e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMAction`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each container of this type defines an action. These actions can be part of one or several action lists.

########## 配置容器

本模块包含 **18** 个配置容器：

########### 1. BswMComMAllowCom

**容器属性**:

- **UUID**: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMAllowCom`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.

############ 参数配置

此容器包含 **1** 个参数：

############# BOOLEAN 类型参数

############## 1. BswMComAllowed

- **UUID**: `ECUC:a75f55aa-9e34-48e5-9c33-8e121ac7f7d8`
- **参数名**: `BswMComAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter BswMComMAllowChannelRef refers to a channel which will allow or block communication using the function ComM_CommunicationAllowed().

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMComMAllowChannelRef

- **UUID**: `ECUC:cfa3f8ee-4192-4364-a046-f5ef39f8626f`
- **引用名**: `BswMComMAllowChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM Channel for which communication shall be allowed or blocked.

########### 2. BswMComMModeLimitation

**容器属性**:

- **UUID**: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeLimitation`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.

############ 参数配置

此容器包含 **1** 个参数：

############# BOOLEAN 类型参数

############## 1. BswMComMLimitMode

- **UUID**: `ECUC:a90697cd-02ca-46c7-b4d9-3561ac126656`
- **参数名**: `BswMComMLimitMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function ComM_LimitChannelToNoComMode() takes in this boolean parameter to limit the channel's com mode to no-com mode.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMComMLimitChannelRef

- **UUID**: `ECUC:dfb83a13-105c-4ad9-b65d-8465bcad8ddd`
- **引用名**: `BswMComMLimitChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM channel for which the communication mode should be limited.

########### 3. BswMComMModeSwitch

**容器属性**:

- **UUID**: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.

############ 参数配置

此容器包含 **1** 个参数：

############# ENUMERATION 类型参数

############## 1. BswMComMRequestedMode

- **UUID**: `ECUC:a8479736-a047-4a2e-a9de-9de9d1fe5e26`
- **参数名**: `BswMComMRequestedMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FULL_COM` (来源: AUTOSAR_ECUC)
  - `BSWM_NO_COM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the requested communication mode.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMComMUserRef

- **UUID**: `ECUC:38ab9166-a9b6-4666-8064-b0fe9192d7af`
- **引用名**: `BswMComMUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM User that is associated to the Communication channel for which the communication mode should be requested.

########### 4. BswMDeadlineMonitoringControl

**容器属性**:

- **UUID**: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDeadlineMonitoringControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMDisabledDMPduGroupRef

- **UUID**: `ECUC:858f665d-7fc6-49e4-a22a-b512c6e0b69b`
- **引用名**: `BswMDisabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be disabled.

############## 2. BswMEnabledDMPduGroupRef

- **UUID**: `ECUC:489675a3-4dfa-43b5-8f8e-48609a142a1d`
- **引用名**: `BswMEnabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be enabled.

########### 5. BswMEcuMGoDown

**容器属性**:

- **UUID**: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMGoDown`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the UserId which shall be forwarded to the GoDown request.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMEcuMUserIdRef

- **UUID**: `ECUC:5bf3393d-903b-435c-822a-e8df76b79337`
- **引用名**: `BswMEcuMUserIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a EcuM UserId.

########### 6. BswMEcuMSelectShutdownTarget

**容器属性**:

- **UUID**: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMSelectShutdownTarget`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the shutdown target.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMEcuMShutdownTargetRef

- **UUID**: `ECUC:46e261aa-240e-40c3-8b60-5242f58edfb2`
- **引用名**: `BswMEcuMShutdownTargetRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a shutdown target.

########### 7. BswMLinScheduleSwitch

**容器属性**:

- **UUID**: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMLinScheduleRef

- **UUID**: `ECUC:32b27d57-fa6d-4f23-a0c7-f872b0d789a0`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN schedule table that the LIN SM shall change to.

########### 8. BswMNMControl

**容器属性**:

- **UUID**: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNMControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.

############ 参数配置

此容器包含 **1** 个参数：

############# ENUMERATION 类型参数

############## 1. BswMNMAction

- **UUID**: `ECUC:b0783d19-a6d0-4699-ac8c-a4049b4d461e`
- **参数名**: `BswMNMAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_NM_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_NM_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the communication of the corresponding NM channel should be enabled or disabled.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMComMNetworkHandleRef

- **UUID**: `ECUC:71f03668-a386-4d49-b226-dd2c739ebc06`
- **引用名**: `BswMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

########### 9. BswMPduGroupSwitch

**容器属性**:

- **UUID**: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduGroupSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.

############ 参数配置

此容器包含 **1** 个参数：

############# BOOLEAN 类型参数

############## 1. BswMPduGroupSwitchReinit

- **UUID**: `ECUC:b6fb3fbb-cb5c-4d7a-9560-c5bc39a5da54`
- **参数名**: `BswMPduGroupSwitchReinit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the values for the parameters like periodical timer, minimum delay timer etc is retainer or reinitialized during a PDU Group Switch.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMDisabledPduGroupRef

- **UUID**: `ECUC:d63a77a6-da9d-467a-9c2f-6879f96a8b50`
- **引用名**: `BswMDisabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be disabled.

############## 2. BswMEnabledPduGroupRef

- **UUID**: `ECUC:754e70f9-ccd0-4a90-8e06-58d065bb4184`
- **引用名**: `BswMEnabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be enabled.

########### 10. BswMPduRouterControl

**容器属性**:

- **UUID**: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduRouterControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.

############ 参数配置

此容器包含 **1** 个参数：

############# ENUMERATION 类型参数

############## 1. BswPduRouterAction

- **UUID**: `ECUC:7a7d7b39-fdff-4f16-9aa1-9ea5d6b3f02f`
- **参数名**: `BswPduRouterAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_PDUR_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_PDUR_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the routing of the corresponding PDU should be enabled or disabled.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMPduRoutingPathGroupRef

- **UUID**: `ECUC:edbfb25c-322b-4d20-93f0-b1e32d0f50f5`
- **引用名**: `BswMPduRoutingPathGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `PduRRoutingPathGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRRoutingPathGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the PDU Routing Path Group for which the routing in the PDU Router should be enabled or disabled.

########### 11. BswMRteSwitch

**容器属性**:

- **UUID**: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRteSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. BswMRteSwitchPortRef

- **UUID**: `ECUC:4642d375-9c6d-4db5-84c5-fb8e6d59972c`
- **引用名**: `BswMRteSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

############# FOREIGN-REFERENCE 类型引用

############## 1. BswMSwitchedMode

- **UUID**: `ECUC:3d6f5054-ebed-40f3-9abc-b366bc6a8017`
- **引用名**: `BswMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

########### 12. BswMSchMSwitch

**容器属性**:

- **UUID**: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSchMSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. BswMSchMSwitchPortRef

- **UUID**: `ECUC:e18f3107-9272-4ace-95ac-cfce6556be97`
- **引用名**: `BswMSchMSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

############# FOREIGN-REFERENCE 类型引用

############## 1. BswMSchMSwitchedMode

- **UUID**: `ECUC:8223503b-58a4-4608-9fe1-4317c3c27858`
- **引用名**: `BswMSchMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

########### 13. BswMSwitchIPduMode

**容器属性**:

- **UUID**: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchIPduMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.

############ 参数配置

此容器包含 **1** 个参数：

############# BOOLEAN 类型参数

############## 1. BswMSwitchIPduModeValue

- **UUID**: `ECUC:75026229-698c-4fbc-a905-6652e28355d6`
- **参数名**: `BswMSwitchIPduModeValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines which transmission mode shall be selected during this call.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMSwitchIPduModeRef

- **UUID**: `ECUC:2629fedf-9668-4d93-af1e-99e2346f915f`
- **引用名**: `BswMSwitchIPduModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU for which the transmission mode shall be set.

########### 14. BswMTriggerIPduSend

**容器属性**:

- **UUID**: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerIPduSend`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMTriggeredIPduRef

- **UUID**: `ECUC:bf813042-367e-403f-849e-eb3d8b1c950f`
- **引用名**: `BswMTriggeredIPduRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU that should be triggered for transmission.

########### 15. BswMTriggerSlaveRTEStop

**容器属性**:

- **UUID**: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerSlaveRTEStop`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. BswMCoreId

- **UUID**: `ECUC:8fd528a4-a7eb-8b28-53f8-45f371b4c7ea`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

########### 16. BswMTriggerStartUpPhase2

**容器属性**:

- **UUID**: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerStartUpPhase2`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. BswMCoreId

- **UUID**: `ECUC:d2865d98-439b-83c9-38dc-4f3a8ce7f3ae`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

########### 17. BswMUserCallout

**容器属性**:

- **UUID**: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMUserCallout`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all details needed for a user defined function call.

############ 参数配置

此容器包含 **1** 个参数：

############# STRING 类型参数

############## 1. BswMUserCalloutFunction

- **UUID**: `ECUC:40b9feb6-e998-4e06-a351-81f431b4850e`
- **参数名**: `BswMUserCalloutFunction`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the complete function call including all parameters. The parameters are specified during configuration time, and cannot be changed during run time. Any return values passed by the callout will be ignored.

########### 18. BswMAvailableActions

**容器属性**:

- **UUID**: `ECUC:cc9ad948-01ce-4ed4-a898-41fcd6ede588`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMAvailableActions`
- **多重性**: [1..1]

**容器选择**:

- **BswMComMAllowCom**
  - UUID: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
  - 描述: This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.
- **BswMComMModeLimitation**
  - UUID: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
  - 描述: This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.
- **BswMComMModeSwitch**
  - UUID: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
  - 描述: This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.
- **BswMDeadlineMonitoringControl**
  - UUID: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
  - 描述: This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.
- **BswMEcuMGoDown**
  - UUID: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
  - 描述: This container defines the UserId which shall be forwarded to the GoDown request.
- **BswMEcuMSelectShutdownTarget**
  - UUID: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
  - 描述: This container defines the shutdown target.
- **BswMLinScheduleSwitch**
  - UUID: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
  - 描述: This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.
- **BswMNMControl**
  - UUID: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
  - 描述: This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.
- **BswMPduGroupSwitch**
  - UUID: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
  - 描述: This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.
- **BswMPduRouterControl**
  - UUID: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
  - 描述: This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.
- **BswMRteSwitch**
  - UUID: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.
- **BswMSchMSwitch**
  - UUID: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.
- **BswMSwitchIPduMode**
  - UUID: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
  - 描述: This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.
- **BswMTriggerIPduSend**
  - UUID: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
  - 描述: This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.
- **BswMTriggerSlaveRTEStop**
  - UUID: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
  - 描述: This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.
- **BswMTriggerStartUpPhase2**
  - UUID: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
  - 描述: This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.
- **BswMUserCallout**
  - UUID: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
  - 描述: This container includes all details needed for a user defined function call.

**容器描述**:

Choice container including the available actions to be used in the action lists.

######### 2. BswMComMAllowCom

**容器属性**:

- **UUID**: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMAllowCom`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMComAllowed

- **UUID**: `ECUC:a75f55aa-9e34-48e5-9c33-8e121ac7f7d8`
- **参数名**: `BswMComAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter BswMComMAllowChannelRef refers to a channel which will allow or block communication using the function ComM_CommunicationAllowed().

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMAllowChannelRef

- **UUID**: `ECUC:cfa3f8ee-4192-4364-a046-f5ef39f8626f`
- **引用名**: `BswMComMAllowChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM Channel for which communication shall be allowed or blocked.

######### 3. BswMComMModeLimitation

**容器属性**:

- **UUID**: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeLimitation`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMComMLimitMode

- **UUID**: `ECUC:a90697cd-02ca-46c7-b4d9-3561ac126656`
- **参数名**: `BswMComMLimitMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function ComM_LimitChannelToNoComMode() takes in this boolean parameter to limit the channel's com mode to no-com mode.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMLimitChannelRef

- **UUID**: `ECUC:dfb83a13-105c-4ad9-b65d-8465bcad8ddd`
- **引用名**: `BswMComMLimitChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM channel for which the communication mode should be limited.

######### 4. BswMComMModeSwitch

**容器属性**:

- **UUID**: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMComMRequestedMode

- **UUID**: `ECUC:a8479736-a047-4a2e-a9de-9de9d1fe5e26`
- **参数名**: `BswMComMRequestedMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FULL_COM` (来源: AUTOSAR_ECUC)
  - `BSWM_NO_COM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the requested communication mode.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMUserRef

- **UUID**: `ECUC:38ab9166-a9b6-4666-8064-b0fe9192d7af`
- **引用名**: `BswMComMUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM User that is associated to the Communication channel for which the communication mode should be requested.

######### 5. BswMDeadlineMonitoringControl

**容器属性**:

- **UUID**: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDeadlineMonitoringControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMDisabledDMPduGroupRef

- **UUID**: `ECUC:858f665d-7fc6-49e4-a22a-b512c6e0b69b`
- **引用名**: `BswMDisabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be disabled.

############ 2. BswMEnabledDMPduGroupRef

- **UUID**: `ECUC:489675a3-4dfa-43b5-8f8e-48609a142a1d`
- **引用名**: `BswMEnabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be enabled.

######### 6. BswMEcuMGoDown

**容器属性**:

- **UUID**: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMGoDown`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the UserId which shall be forwarded to the GoDown request.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEcuMUserIdRef

- **UUID**: `ECUC:5bf3393d-903b-435c-822a-e8df76b79337`
- **引用名**: `BswMEcuMUserIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a EcuM UserId.

######### 7. BswMEcuMSelectShutdownTarget

**容器属性**:

- **UUID**: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMSelectShutdownTarget`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the shutdown target.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEcuMShutdownTargetRef

- **UUID**: `ECUC:46e261aa-240e-40c3-8b60-5242f58edfb2`
- **引用名**: `BswMEcuMShutdownTargetRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a shutdown target.

######### 8. BswMLinScheduleSwitch

**容器属性**:

- **UUID**: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinScheduleRef

- **UUID**: `ECUC:32b27d57-fa6d-4f23-a0c7-f872b0d789a0`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN schedule table that the LIN SM shall change to.

######### 9. BswMNMControl

**容器属性**:

- **UUID**: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNMControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMNMAction

- **UUID**: `ECUC:b0783d19-a6d0-4699-ac8c-a4049b4d461e`
- **参数名**: `BswMNMAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_NM_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_NM_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the communication of the corresponding NM channel should be enabled or disabled.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMNetworkHandleRef

- **UUID**: `ECUC:71f03668-a386-4d49-b226-dd2c739ebc06`
- **引用名**: `BswMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

######### 10. BswMPduGroupSwitch

**容器属性**:

- **UUID**: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduGroupSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMPduGroupSwitchReinit

- **UUID**: `ECUC:b6fb3fbb-cb5c-4d7a-9560-c5bc39a5da54`
- **参数名**: `BswMPduGroupSwitchReinit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the values for the parameters like periodical timer, minimum delay timer etc is retainer or reinitialized during a PDU Group Switch.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMDisabledPduGroupRef

- **UUID**: `ECUC:d63a77a6-da9d-467a-9c2f-6879f96a8b50`
- **引用名**: `BswMDisabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be disabled.

############ 2. BswMEnabledPduGroupRef

- **UUID**: `ECUC:754e70f9-ccd0-4a90-8e06-58d065bb4184`
- **引用名**: `BswMEnabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be enabled.

######### 11. BswMPduRouterControl

**容器属性**:

- **UUID**: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduRouterControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswPduRouterAction

- **UUID**: `ECUC:7a7d7b39-fdff-4f16-9aa1-9ea5d6b3f02f`
- **参数名**: `BswPduRouterAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_PDUR_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_PDUR_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the routing of the corresponding PDU should be enabled or disabled.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMPduRoutingPathGroupRef

- **UUID**: `ECUC:edbfb25c-322b-4d20-93f0-b1e32d0f50f5`
- **引用名**: `BswMPduRoutingPathGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `PduRRoutingPathGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRRoutingPathGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the PDU Routing Path Group for which the routing in the PDU Router should be enabled or disabled.

######### 12. BswMRteSwitch

**容器属性**:

- **UUID**: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRteSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. BswMRteSwitchPortRef

- **UUID**: `ECUC:4642d375-9c6d-4db5-84c5-fb8e6d59972c`
- **引用名**: `BswMRteSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwitchedMode

- **UUID**: `ECUC:3d6f5054-ebed-40f3-9abc-b366bc6a8017`
- **引用名**: `BswMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

######### 13. BswMSchMSwitch

**容器属性**:

- **UUID**: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSchMSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. BswMSchMSwitchPortRef

- **UUID**: `ECUC:e18f3107-9272-4ace-95ac-cfce6556be97`
- **引用名**: `BswMSchMSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSchMSwitchedMode

- **UUID**: `ECUC:8223503b-58a4-4608-9fe1-4317c3c27858`
- **引用名**: `BswMSchMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

######### 14. BswMSwitchIPduMode

**容器属性**:

- **UUID**: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchIPduMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMSwitchIPduModeValue

- **UUID**: `ECUC:75026229-698c-4fbc-a905-6652e28355d6`
- **参数名**: `BswMSwitchIPduModeValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines which transmission mode shall be selected during this call.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMSwitchIPduModeRef

- **UUID**: `ECUC:2629fedf-9668-4d93-af1e-99e2346f915f`
- **引用名**: `BswMSwitchIPduModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU for which the transmission mode shall be set.

######### 15. BswMTriggerIPduSend

**容器属性**:

- **UUID**: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerIPduSend`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMTriggeredIPduRef

- **UUID**: `ECUC:bf813042-367e-403f-849e-eb3d8b1c950f`
- **引用名**: `BswMTriggeredIPduRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU that should be triggered for transmission.

######### 16. BswMTriggerSlaveRTEStop

**容器属性**:

- **UUID**: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerSlaveRTEStop`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. BswMCoreId

- **UUID**: `ECUC:8fd528a4-a7eb-8b28-53f8-45f371b4c7ea`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

######### 17. BswMTriggerStartUpPhase2

**容器属性**:

- **UUID**: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerStartUpPhase2`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. BswMCoreId

- **UUID**: `ECUC:d2865d98-439b-83c9-38dc-4f3a8ce7f3ae`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

######### 18. BswMUserCallout

**容器属性**:

- **UUID**: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMUserCallout`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all details needed for a user defined function call.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMUserCalloutFunction

- **UUID**: `ECUC:40b9feb6-e998-4e06-a351-81f431b4850e`
- **参数名**: `BswMUserCalloutFunction`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the complete function call including all parameters. The parameters are specified during configuration time, and cannot be changed during run time. Any return values passed by the callout will be ignored.

######### 19. BswMActionList

**容器属性**:

- **UUID**: `ECUC:407b970e-46be-4d6b-b8ad-157663aa5d94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionList`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container defines an action list that is invoked based on the BswM Rules. An action list contains a list of numbered action items to be processed. An action list can also include other action lists.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMActionListExecution

- **UUID**: `ECUC:e6f03759-bac9-40cb-816c-4432a6d70644`
- **参数名**: `BswMActionListExecution`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_CONDITION` (来源: AUTOSAR_ECUC)
  - `BSWM_TRIGGER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter controls if the corresponding action list shall be executed every time the rule is evaluated or only when the result of the evaluation changes.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. BswMActionListItem

**容器属性**:

- **UUID**: `ECUC:57ce84a2-0f20-4dd5-85a3-4fd44d75b91a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionListItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines an item in an action list.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. BswMActionListItemIndex

- **UUID**: `ECUC:d2944d1c-b5c4-4d6b-bc4c-ae6c1a89e946`
- **参数名**: `BswMActionListItemIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the index of the action in the action list. It is used define in which order the actions shall be performed.

############# BOOLEAN 类型参数

############## 1. BswMAbortOnFail

- **UUID**: `ECUC:79c629de-d4aa-49d9-b686-9a6bd7347aec`
- **参数名**: `BswMAbortOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the execution of the action list shall be aborted if this specific action returns E_NOT_OK. Note that this is only applicable for actions that have E_NOT_OK as a possible return value.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. BswMReportFailToDemRef

- **UUID**: `ECUC:5b95c4bb-7e3b-4788-bb34-eaf73a792725`
- **引用名**: `BswMReportFailToDemRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the reference is given, the DEM event shall be reported failed if this specific action returns E_NOT_OK; it shall be reported passed if this specific action returns E_OK.

############# CHOICE-REFERENCE 类型引用

############## 1. BswMActionListItemRef

- **UUID**: `ECUC:756c431f-9e65-40e8-b3a3-47599991abcb`
- **引用名**: `BswMActionListItemRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMAction`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMRule`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action item can either be an atomic action or a reference to another action list or rule.

######### 20. BswMActionListItem

**容器属性**:

- **UUID**: `ECUC:57ce84a2-0f20-4dd5-85a3-4fd44d75b91a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionListItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines an item in an action list.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. BswMActionListItemIndex

- **UUID**: `ECUC:d2944d1c-b5c4-4d6b-bc4c-ae6c1a89e946`
- **参数名**: `BswMActionListItemIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the index of the action in the action list. It is used define in which order the actions shall be performed.

########### BOOLEAN 类型参数

############ 1. BswMAbortOnFail

- **UUID**: `ECUC:79c629de-d4aa-49d9-b686-9a6bd7347aec`
- **参数名**: `BswMAbortOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the execution of the action list shall be aborted if this specific action returns E_NOT_OK. Note that this is only applicable for actions that have E_NOT_OK as a possible return value.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMReportFailToDemRef

- **UUID**: `ECUC:5b95c4bb-7e3b-4788-bb34-eaf73a792725`
- **引用名**: `BswMReportFailToDemRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the reference is given, the DEM event shall be reported failed if this specific action returns E_NOT_OK; it shall be reported passed if this specific action returns E_OK.

########### CHOICE-REFERENCE 类型引用

############ 1. BswMActionListItemRef

- **UUID**: `ECUC:756c431f-9e65-40e8-b3a3-47599991abcb`
- **引用名**: `BswMActionListItemRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMAction`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMRule`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action item can either be an atomic action or a reference to another action list or rule.

######### 21. BswMSwitchPort

**容器属性**:

- **UUID**: `ECUC:f962bf44-5314-4e9c-894b-e8cf24f38351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchPort`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies PPorts and/or providedModeDeclarationGroups, which the BswM has to create in its SWCD resp. BSWMD.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMModeSwitchInterfaceRef

- **UUID**: `ECUC:868ddf33-9a9f-4e55-9dcb-598cd2bed53a`
- **引用名**: `BswMModeSwitchInterfaceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-SWITCH-INTERFACE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ModeSwitchInterface of this BswMModeSwitchPort.

######### 22. BswMAvailableActions

**容器属性**:

- **UUID**: `ECUC:cc9ad948-01ce-4ed4-a898-41fcd6ede588`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMAvailableActions`
- **多重性**: [1..1]

**容器选择**:

- **BswMComMAllowCom**
  - UUID: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
  - 描述: This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.
- **BswMComMModeLimitation**
  - UUID: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
  - 描述: This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.
- **BswMComMModeSwitch**
  - UUID: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
  - 描述: This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.
- **BswMDeadlineMonitoringControl**
  - UUID: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
  - 描述: This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.
- **BswMEcuMGoDown**
  - UUID: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
  - 描述: This container defines the UserId which shall be forwarded to the GoDown request.
- **BswMEcuMSelectShutdownTarget**
  - UUID: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
  - 描述: This container defines the shutdown target.
- **BswMLinScheduleSwitch**
  - UUID: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
  - 描述: This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.
- **BswMNMControl**
  - UUID: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
  - 描述: This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.
- **BswMPduGroupSwitch**
  - UUID: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
  - 描述: This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.
- **BswMPduRouterControl**
  - UUID: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
  - 描述: This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.
- **BswMRteSwitch**
  - UUID: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.
- **BswMSchMSwitch**
  - UUID: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.
- **BswMSwitchIPduMode**
  - UUID: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
  - 描述: This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.
- **BswMTriggerIPduSend**
  - UUID: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
  - 描述: This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.
- **BswMTriggerSlaveRTEStop**
  - UUID: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
  - 描述: This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.
- **BswMTriggerStartUpPhase2**
  - UUID: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
  - 描述: This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.
- **BswMUserCallout**
  - UUID: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
  - 描述: This container includes all details needed for a user defined function call.

**容器描述**:

Choice container including the available actions to be used in the action lists.

####### 31. BswMAction

**容器属性**:

- **UUID**: `ECUC:add00e45-e97c-4d9a-8208-befcbfbfd3e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMAction`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each container of this type defines an action. These actions can be part of one or several action lists.

######## 配置容器

本模块包含 **18** 个配置容器：

######### 1. BswMComMAllowCom

**容器属性**:

- **UUID**: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMAllowCom`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMComAllowed

- **UUID**: `ECUC:a75f55aa-9e34-48e5-9c33-8e121ac7f7d8`
- **参数名**: `BswMComAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter BswMComMAllowChannelRef refers to a channel which will allow or block communication using the function ComM_CommunicationAllowed().

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMAllowChannelRef

- **UUID**: `ECUC:cfa3f8ee-4192-4364-a046-f5ef39f8626f`
- **引用名**: `BswMComMAllowChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM Channel for which communication shall be allowed or blocked.

######### 2. BswMComMModeLimitation

**容器属性**:

- **UUID**: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeLimitation`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMComMLimitMode

- **UUID**: `ECUC:a90697cd-02ca-46c7-b4d9-3561ac126656`
- **参数名**: `BswMComMLimitMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function ComM_LimitChannelToNoComMode() takes in this boolean parameter to limit the channel's com mode to no-com mode.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMLimitChannelRef

- **UUID**: `ECUC:dfb83a13-105c-4ad9-b65d-8465bcad8ddd`
- **引用名**: `BswMComMLimitChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM channel for which the communication mode should be limited.

######### 3. BswMComMModeSwitch

**容器属性**:

- **UUID**: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMComMRequestedMode

- **UUID**: `ECUC:a8479736-a047-4a2e-a9de-9de9d1fe5e26`
- **参数名**: `BswMComMRequestedMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FULL_COM` (来源: AUTOSAR_ECUC)
  - `BSWM_NO_COM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the requested communication mode.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMUserRef

- **UUID**: `ECUC:38ab9166-a9b6-4666-8064-b0fe9192d7af`
- **引用名**: `BswMComMUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM User that is associated to the Communication channel for which the communication mode should be requested.

######### 4. BswMDeadlineMonitoringControl

**容器属性**:

- **UUID**: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDeadlineMonitoringControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMDisabledDMPduGroupRef

- **UUID**: `ECUC:858f665d-7fc6-49e4-a22a-b512c6e0b69b`
- **引用名**: `BswMDisabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be disabled.

############ 2. BswMEnabledDMPduGroupRef

- **UUID**: `ECUC:489675a3-4dfa-43b5-8f8e-48609a142a1d`
- **引用名**: `BswMEnabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be enabled.

######### 5. BswMEcuMGoDown

**容器属性**:

- **UUID**: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMGoDown`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the UserId which shall be forwarded to the GoDown request.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEcuMUserIdRef

- **UUID**: `ECUC:5bf3393d-903b-435c-822a-e8df76b79337`
- **引用名**: `BswMEcuMUserIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a EcuM UserId.

######### 6. BswMEcuMSelectShutdownTarget

**容器属性**:

- **UUID**: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMSelectShutdownTarget`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the shutdown target.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEcuMShutdownTargetRef

- **UUID**: `ECUC:46e261aa-240e-40c3-8b60-5242f58edfb2`
- **引用名**: `BswMEcuMShutdownTargetRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a shutdown target.

######### 7. BswMLinScheduleSwitch

**容器属性**:

- **UUID**: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinScheduleRef

- **UUID**: `ECUC:32b27d57-fa6d-4f23-a0c7-f872b0d789a0`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN schedule table that the LIN SM shall change to.

######### 8. BswMNMControl

**容器属性**:

- **UUID**: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNMControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMNMAction

- **UUID**: `ECUC:b0783d19-a6d0-4699-ac8c-a4049b4d461e`
- **参数名**: `BswMNMAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_NM_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_NM_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the communication of the corresponding NM channel should be enabled or disabled.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMNetworkHandleRef

- **UUID**: `ECUC:71f03668-a386-4d49-b226-dd2c739ebc06`
- **引用名**: `BswMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

######### 9. BswMPduGroupSwitch

**容器属性**:

- **UUID**: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduGroupSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMPduGroupSwitchReinit

- **UUID**: `ECUC:b6fb3fbb-cb5c-4d7a-9560-c5bc39a5da54`
- **参数名**: `BswMPduGroupSwitchReinit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the values for the parameters like periodical timer, minimum delay timer etc is retainer or reinitialized during a PDU Group Switch.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMDisabledPduGroupRef

- **UUID**: `ECUC:d63a77a6-da9d-467a-9c2f-6879f96a8b50`
- **引用名**: `BswMDisabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be disabled.

############ 2. BswMEnabledPduGroupRef

- **UUID**: `ECUC:754e70f9-ccd0-4a90-8e06-58d065bb4184`
- **引用名**: `BswMEnabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be enabled.

######### 10. BswMPduRouterControl

**容器属性**:

- **UUID**: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduRouterControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswPduRouterAction

- **UUID**: `ECUC:7a7d7b39-fdff-4f16-9aa1-9ea5d6b3f02f`
- **参数名**: `BswPduRouterAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_PDUR_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_PDUR_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the routing of the corresponding PDU should be enabled or disabled.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMPduRoutingPathGroupRef

- **UUID**: `ECUC:edbfb25c-322b-4d20-93f0-b1e32d0f50f5`
- **引用名**: `BswMPduRoutingPathGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `PduRRoutingPathGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRRoutingPathGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the PDU Routing Path Group for which the routing in the PDU Router should be enabled or disabled.

######### 11. BswMRteSwitch

**容器属性**:

- **UUID**: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRteSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. BswMRteSwitchPortRef

- **UUID**: `ECUC:4642d375-9c6d-4db5-84c5-fb8e6d59972c`
- **引用名**: `BswMRteSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwitchedMode

- **UUID**: `ECUC:3d6f5054-ebed-40f3-9abc-b366bc6a8017`
- **引用名**: `BswMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

######### 12. BswMSchMSwitch

**容器属性**:

- **UUID**: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSchMSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. BswMSchMSwitchPortRef

- **UUID**: `ECUC:e18f3107-9272-4ace-95ac-cfce6556be97`
- **引用名**: `BswMSchMSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSchMSwitchedMode

- **UUID**: `ECUC:8223503b-58a4-4608-9fe1-4317c3c27858`
- **引用名**: `BswMSchMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

######### 13. BswMSwitchIPduMode

**容器属性**:

- **UUID**: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchIPduMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMSwitchIPduModeValue

- **UUID**: `ECUC:75026229-698c-4fbc-a905-6652e28355d6`
- **参数名**: `BswMSwitchIPduModeValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines which transmission mode shall be selected during this call.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMSwitchIPduModeRef

- **UUID**: `ECUC:2629fedf-9668-4d93-af1e-99e2346f915f`
- **引用名**: `BswMSwitchIPduModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU for which the transmission mode shall be set.

######### 14. BswMTriggerIPduSend

**容器属性**:

- **UUID**: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerIPduSend`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMTriggeredIPduRef

- **UUID**: `ECUC:bf813042-367e-403f-849e-eb3d8b1c950f`
- **引用名**: `BswMTriggeredIPduRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU that should be triggered for transmission.

######### 15. BswMTriggerSlaveRTEStop

**容器属性**:

- **UUID**: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerSlaveRTEStop`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. BswMCoreId

- **UUID**: `ECUC:8fd528a4-a7eb-8b28-53f8-45f371b4c7ea`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

######### 16. BswMTriggerStartUpPhase2

**容器属性**:

- **UUID**: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerStartUpPhase2`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. BswMCoreId

- **UUID**: `ECUC:d2865d98-439b-83c9-38dc-4f3a8ce7f3ae`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

######### 17. BswMUserCallout

**容器属性**:

- **UUID**: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMUserCallout`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all details needed for a user defined function call.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMUserCalloutFunction

- **UUID**: `ECUC:40b9feb6-e998-4e06-a351-81f431b4850e`
- **参数名**: `BswMUserCalloutFunction`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the complete function call including all parameters. The parameters are specified during configuration time, and cannot be changed during run time. Any return values passed by the callout will be ignored.

######### 18. BswMAvailableActions

**容器属性**:

- **UUID**: `ECUC:cc9ad948-01ce-4ed4-a898-41fcd6ede588`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMAvailableActions`
- **多重性**: [1..1]

**容器选择**:

- **BswMComMAllowCom**
  - UUID: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
  - 描述: This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.
- **BswMComMModeLimitation**
  - UUID: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
  - 描述: This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.
- **BswMComMModeSwitch**
  - UUID: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
  - 描述: This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.
- **BswMDeadlineMonitoringControl**
  - UUID: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
  - 描述: This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.
- **BswMEcuMGoDown**
  - UUID: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
  - 描述: This container defines the UserId which shall be forwarded to the GoDown request.
- **BswMEcuMSelectShutdownTarget**
  - UUID: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
  - 描述: This container defines the shutdown target.
- **BswMLinScheduleSwitch**
  - UUID: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
  - 描述: This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.
- **BswMNMControl**
  - UUID: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
  - 描述: This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.
- **BswMPduGroupSwitch**
  - UUID: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
  - 描述: This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.
- **BswMPduRouterControl**
  - UUID: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
  - 描述: This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.
- **BswMRteSwitch**
  - UUID: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.
- **BswMSchMSwitch**
  - UUID: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.
- **BswMSwitchIPduMode**
  - UUID: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
  - 描述: This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.
- **BswMTriggerIPduSend**
  - UUID: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
  - 描述: This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.
- **BswMTriggerSlaveRTEStop**
  - UUID: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
  - 描述: This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.
- **BswMTriggerStartUpPhase2**
  - UUID: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
  - 描述: This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.
- **BswMUserCallout**
  - UUID: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
  - 描述: This container includes all details needed for a user defined function call.

**容器描述**:

Choice container including the available actions to be used in the action lists.

####### 32. BswMComMAllowCom

**容器属性**:

- **UUID**: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMAllowCom`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMComAllowed

- **UUID**: `ECUC:a75f55aa-9e34-48e5-9c33-8e121ac7f7d8`
- **参数名**: `BswMComAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter BswMComMAllowChannelRef refers to a channel which will allow or block communication using the function ComM_CommunicationAllowed().

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMAllowChannelRef

- **UUID**: `ECUC:cfa3f8ee-4192-4364-a046-f5ef39f8626f`
- **引用名**: `BswMComMAllowChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM Channel for which communication shall be allowed or blocked.

####### 33. BswMComMModeLimitation

**容器属性**:

- **UUID**: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeLimitation`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMComMLimitMode

- **UUID**: `ECUC:a90697cd-02ca-46c7-b4d9-3561ac126656`
- **参数名**: `BswMComMLimitMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function ComM_LimitChannelToNoComMode() takes in this boolean parameter to limit the channel's com mode to no-com mode.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMLimitChannelRef

- **UUID**: `ECUC:dfb83a13-105c-4ad9-b65d-8465bcad8ddd`
- **引用名**: `BswMComMLimitChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM channel for which the communication mode should be limited.

####### 34. BswMComMModeSwitch

**容器属性**:

- **UUID**: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMComMRequestedMode

- **UUID**: `ECUC:a8479736-a047-4a2e-a9de-9de9d1fe5e26`
- **参数名**: `BswMComMRequestedMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FULL_COM` (来源: AUTOSAR_ECUC)
  - `BSWM_NO_COM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the requested communication mode.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMUserRef

- **UUID**: `ECUC:38ab9166-a9b6-4666-8064-b0fe9192d7af`
- **引用名**: `BswMComMUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM User that is associated to the Communication channel for which the communication mode should be requested.

####### 35. BswMDeadlineMonitoringControl

**容器属性**:

- **UUID**: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDeadlineMonitoringControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMDisabledDMPduGroupRef

- **UUID**: `ECUC:858f665d-7fc6-49e4-a22a-b512c6e0b69b`
- **引用名**: `BswMDisabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be disabled.

########## 2. BswMEnabledDMPduGroupRef

- **UUID**: `ECUC:489675a3-4dfa-43b5-8f8e-48609a142a1d`
- **引用名**: `BswMEnabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be enabled.

####### 36. BswMEcuMGoDown

**容器属性**:

- **UUID**: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMGoDown`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the UserId which shall be forwarded to the GoDown request.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEcuMUserIdRef

- **UUID**: `ECUC:5bf3393d-903b-435c-822a-e8df76b79337`
- **引用名**: `BswMEcuMUserIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a EcuM UserId.

####### 37. BswMEcuMSelectShutdownTarget

**容器属性**:

- **UUID**: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMSelectShutdownTarget`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the shutdown target.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEcuMShutdownTargetRef

- **UUID**: `ECUC:46e261aa-240e-40c3-8b60-5242f58edfb2`
- **引用名**: `BswMEcuMShutdownTargetRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a shutdown target.

####### 38. BswMLinScheduleSwitch

**容器属性**:

- **UUID**: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinScheduleRef

- **UUID**: `ECUC:32b27d57-fa6d-4f23-a0c7-f872b0d789a0`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN schedule table that the LIN SM shall change to.

####### 39. BswMNMControl

**容器属性**:

- **UUID**: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNMControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMNMAction

- **UUID**: `ECUC:b0783d19-a6d0-4699-ac8c-a4049b4d461e`
- **参数名**: `BswMNMAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_NM_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_NM_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the communication of the corresponding NM channel should be enabled or disabled.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMNetworkHandleRef

- **UUID**: `ECUC:71f03668-a386-4d49-b226-dd2c739ebc06`
- **引用名**: `BswMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

####### 40. BswMPduGroupSwitch

**容器属性**:

- **UUID**: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduGroupSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMPduGroupSwitchReinit

- **UUID**: `ECUC:b6fb3fbb-cb5c-4d7a-9560-c5bc39a5da54`
- **参数名**: `BswMPduGroupSwitchReinit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the values for the parameters like periodical timer, minimum delay timer etc is retainer or reinitialized during a PDU Group Switch.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMDisabledPduGroupRef

- **UUID**: `ECUC:d63a77a6-da9d-467a-9c2f-6879f96a8b50`
- **引用名**: `BswMDisabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be disabled.

########## 2. BswMEnabledPduGroupRef

- **UUID**: `ECUC:754e70f9-ccd0-4a90-8e06-58d065bb4184`
- **引用名**: `BswMEnabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be enabled.

####### 41. BswMPduRouterControl

**容器属性**:

- **UUID**: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduRouterControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswPduRouterAction

- **UUID**: `ECUC:7a7d7b39-fdff-4f16-9aa1-9ea5d6b3f02f`
- **参数名**: `BswPduRouterAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_PDUR_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_PDUR_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the routing of the corresponding PDU should be enabled or disabled.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMPduRoutingPathGroupRef

- **UUID**: `ECUC:edbfb25c-322b-4d20-93f0-b1e32d0f50f5`
- **引用名**: `BswMPduRoutingPathGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `PduRRoutingPathGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRRoutingPathGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the PDU Routing Path Group for which the routing in the PDU Router should be enabled or disabled.

####### 42. BswMRteSwitch

**容器属性**:

- **UUID**: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRteSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. BswMRteSwitchPortRef

- **UUID**: `ECUC:4642d375-9c6d-4db5-84c5-fb8e6d59972c`
- **引用名**: `BswMRteSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwitchedMode

- **UUID**: `ECUC:3d6f5054-ebed-40f3-9abc-b366bc6a8017`
- **引用名**: `BswMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

####### 43. BswMSchMSwitch

**容器属性**:

- **UUID**: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSchMSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. BswMSchMSwitchPortRef

- **UUID**: `ECUC:e18f3107-9272-4ace-95ac-cfce6556be97`
- **引用名**: `BswMSchMSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSchMSwitchedMode

- **UUID**: `ECUC:8223503b-58a4-4608-9fe1-4317c3c27858`
- **引用名**: `BswMSchMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

####### 44. BswMSwitchIPduMode

**容器属性**:

- **UUID**: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchIPduMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMSwitchIPduModeValue

- **UUID**: `ECUC:75026229-698c-4fbc-a905-6652e28355d6`
- **参数名**: `BswMSwitchIPduModeValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines which transmission mode shall be selected during this call.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMSwitchIPduModeRef

- **UUID**: `ECUC:2629fedf-9668-4d93-af1e-99e2346f915f`
- **引用名**: `BswMSwitchIPduModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU for which the transmission mode shall be set.

####### 45. BswMTriggerIPduSend

**容器属性**:

- **UUID**: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerIPduSend`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMTriggeredIPduRef

- **UUID**: `ECUC:bf813042-367e-403f-849e-eb3d8b1c950f`
- **引用名**: `BswMTriggeredIPduRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU that should be triggered for transmission.

####### 46. BswMTriggerSlaveRTEStop

**容器属性**:

- **UUID**: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerSlaveRTEStop`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. BswMCoreId

- **UUID**: `ECUC:8fd528a4-a7eb-8b28-53f8-45f371b4c7ea`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

####### 47. BswMTriggerStartUpPhase2

**容器属性**:

- **UUID**: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerStartUpPhase2`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. BswMCoreId

- **UUID**: `ECUC:d2865d98-439b-83c9-38dc-4f3a8ce7f3ae`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

####### 48. BswMUserCallout

**容器属性**:

- **UUID**: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMUserCallout`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all details needed for a user defined function call.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMUserCalloutFunction

- **UUID**: `ECUC:40b9feb6-e998-4e06-a351-81f431b4850e`
- **参数名**: `BswMUserCalloutFunction`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the complete function call including all parameters. The parameters are specified during configuration time, and cannot be changed during run time. Any return values passed by the callout will be ignored.

####### 49. BswMActionList

**容器属性**:

- **UUID**: `ECUC:407b970e-46be-4d6b-b8ad-157663aa5d94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionList`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container defines an action list that is invoked based on the BswM Rules. An action list contains a list of numbered action items to be processed. An action list can also include other action lists.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMActionListExecution

- **UUID**: `ECUC:e6f03759-bac9-40cb-816c-4432a6d70644`
- **参数名**: `BswMActionListExecution`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_CONDITION` (来源: AUTOSAR_ECUC)
  - `BSWM_TRIGGER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter controls if the corresponding action list shall be executed every time the rule is evaluated or only when the result of the evaluation changes.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. BswMActionListItem

**容器属性**:

- **UUID**: `ECUC:57ce84a2-0f20-4dd5-85a3-4fd44d75b91a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionListItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines an item in an action list.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. BswMActionListItemIndex

- **UUID**: `ECUC:d2944d1c-b5c4-4d6b-bc4c-ae6c1a89e946`
- **参数名**: `BswMActionListItemIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the index of the action in the action list. It is used define in which order the actions shall be performed.

########### BOOLEAN 类型参数

############ 1. BswMAbortOnFail

- **UUID**: `ECUC:79c629de-d4aa-49d9-b686-9a6bd7347aec`
- **参数名**: `BswMAbortOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the execution of the action list shall be aborted if this specific action returns E_NOT_OK. Note that this is only applicable for actions that have E_NOT_OK as a possible return value.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMReportFailToDemRef

- **UUID**: `ECUC:5b95c4bb-7e3b-4788-bb34-eaf73a792725`
- **引用名**: `BswMReportFailToDemRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the reference is given, the DEM event shall be reported failed if this specific action returns E_NOT_OK; it shall be reported passed if this specific action returns E_OK.

########### CHOICE-REFERENCE 类型引用

############ 1. BswMActionListItemRef

- **UUID**: `ECUC:756c431f-9e65-40e8-b3a3-47599991abcb`
- **引用名**: `BswMActionListItemRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMAction`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMRule`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action item can either be an atomic action or a reference to another action list or rule.

####### 50. BswMActionListItem

**容器属性**:

- **UUID**: `ECUC:57ce84a2-0f20-4dd5-85a3-4fd44d75b91a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionListItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines an item in an action list.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. BswMActionListItemIndex

- **UUID**: `ECUC:d2944d1c-b5c4-4d6b-bc4c-ae6c1a89e946`
- **参数名**: `BswMActionListItemIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the index of the action in the action list. It is used define in which order the actions shall be performed.

######### BOOLEAN 类型参数

########## 1. BswMAbortOnFail

- **UUID**: `ECUC:79c629de-d4aa-49d9-b686-9a6bd7347aec`
- **参数名**: `BswMAbortOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the execution of the action list shall be aborted if this specific action returns E_NOT_OK. Note that this is only applicable for actions that have E_NOT_OK as a possible return value.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMReportFailToDemRef

- **UUID**: `ECUC:5b95c4bb-7e3b-4788-bb34-eaf73a792725`
- **引用名**: `BswMReportFailToDemRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the reference is given, the DEM event shall be reported failed if this specific action returns E_NOT_OK; it shall be reported passed if this specific action returns E_OK.

######### CHOICE-REFERENCE 类型引用

########## 1. BswMActionListItemRef

- **UUID**: `ECUC:756c431f-9e65-40e8-b3a3-47599991abcb`
- **引用名**: `BswMActionListItemRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMAction`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMRule`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action item can either be an atomic action or a reference to another action list or rule.

####### 51. BswMSwitchPort

**容器属性**:

- **UUID**: `ECUC:f962bf44-5314-4e9c-894b-e8cf24f38351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchPort`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies PPorts and/or providedModeDeclarationGroups, which the BswM has to create in its SWCD resp. BSWMD.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMModeSwitchInterfaceRef

- **UUID**: `ECUC:868ddf33-9a9f-4e55-9dcb-598cd2bed53a`
- **引用名**: `BswMModeSwitchInterfaceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-SWITCH-INTERFACE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ModeSwitchInterface of this BswMModeSwitchPort.

####### 52. BswMConditionValue

**容器属性**:

- **UUID**: `ECUC:6dfef60d-1d6f-4b42-a4ae-f32d9a3df94f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMConditionValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswMode**
  - UUID: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
  - 描述: This container defines the value and type of a mode in the BSW.
- **BswMModeDeclaration**
  - UUID: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
  - 描述: When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

**容器描述**:

This container holds the parameters and references necessary to identify the mode type and the value that the mode request is compared to.

####### 53. BswMModeInitValue

**容器属性**:

- **UUID**: `ECUC:a780195c-9698-494b-810e-d6f1b56cef30`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeInitValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswModeInitValue**
  - UUID: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
  - 描述: This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.
- **BswMSwcModeInitValue**
  - UUID: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
  - 描述: This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

**容器描述**:

This container defines the initial mode value that is used by BswM for the corresponding mode request after initialization. This container is optional and shall only be used for Mode Requests that do not already have an initial value.

####### 54. BswMModeRequestSource

**容器属性**:

- **UUID**: `ECUC:dd5d5587-bfd1-4960-a654-bcbc222aca93`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeRequestSource`
- **多重性**: [1..1]

**容器选择**:

- **BswMBswModeNotification**
  - UUID: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
  - 描述: The source of the mode request is a Bsw Module.
- **BswMCanSMIndication**
  - UUID: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
  - 描述: This is an indication of the current state of the CAN State Manager.
- **BswMComMIndication**
  - UUID: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
  - 描述: This is an indication of the current communication mode of a channel in the Communication Manager.
- **BswMComMPncRequest**
  - UUID: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
  - 描述: This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.
- **BswMDcmApplicationUpdatedIndication**
  - UUID: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
  - 描述: This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMDcmComModeRequest**
  - UUID: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
  - 描述: The source of the mode request is the Diagnostic Communication Manager.
- **BswMEcuMIndication**
  - UUID: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
  - 描述: This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMEcuMWakeupSource**
  - UUID: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
  - 描述: This is a notification of the current state of an ECU State Manager wakeup source.
- **BswMEthSMIndication**
  - UUID: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
  - 描述: This is an indication of the current state of the Ethernet State Manager.
- **BswMFrSMIndication**
  - UUID: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
  - 描述: This is an indication of the current state of the FlexRay State Manager.
- **BswMGenericRequest**
  - UUID: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
  - 描述: This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).
- **BswMLinSMIndication**
  - UUID: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
  - 描述: This is an indication of the current state of the LIN State Manager.
- **BswMLinScheduleIndication**
  - UUID: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
  - 描述: This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.
- **BswMLinTpModeRequest**
  - UUID: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
  - 描述: This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.
- **BswMNvMJobModeIndication**
  - UUID: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
  - 描述: Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:
- **BswMNvMRequest**
  - UUID: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
  - 描述: Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:
- **BswMSwcModeNotification**
  - UUID: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
  - 描述: This is a mode switch notification associated with a RTE switch interface.
- **BswMSwcModeRequest**
  - UUID: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
  - 描述: The source of the mode request is a SW Component.
- **BswMWdgMRequestPartitionReset**
  - UUID: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
  - 描述: This is a Partition Reset request from from the WdgM. This port

**容器描述**:

This choice container specifies the source of the mode request or state/mode indication. The requester of a mode can be both SW-C:s and other BSW Modules, such as the bus specific State Managers.

####### 55. BswMAvailableActions

**容器属性**:

- **UUID**: `ECUC:cc9ad948-01ce-4ed4-a898-41fcd6ede588`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMAvailableActions`
- **多重性**: [1..1]

**容器选择**:

- **BswMComMAllowCom**
  - UUID: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
  - 描述: This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.
- **BswMComMModeLimitation**
  - UUID: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
  - 描述: This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.
- **BswMComMModeSwitch**
  - UUID: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
  - 描述: This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.
- **BswMDeadlineMonitoringControl**
  - UUID: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
  - 描述: This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.
- **BswMEcuMGoDown**
  - UUID: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
  - 描述: This container defines the UserId which shall be forwarded to the GoDown request.
- **BswMEcuMSelectShutdownTarget**
  - UUID: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
  - 描述: This container defines the shutdown target.
- **BswMLinScheduleSwitch**
  - UUID: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
  - 描述: This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.
- **BswMNMControl**
  - UUID: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
  - 描述: This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.
- **BswMPduGroupSwitch**
  - UUID: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
  - 描述: This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.
- **BswMPduRouterControl**
  - UUID: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
  - 描述: This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.
- **BswMRteSwitch**
  - UUID: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.
- **BswMSchMSwitch**
  - UUID: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.
- **BswMSwitchIPduMode**
  - UUID: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
  - 描述: This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.
- **BswMTriggerIPduSend**
  - UUID: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
  - 描述: This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.
- **BswMTriggerSlaveRTEStop**
  - UUID: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
  - 描述: This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.
- **BswMTriggerStartUpPhase2**
  - UUID: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
  - 描述: This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.
- **BswMUserCallout**
  - UUID: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
  - 描述: This container includes all details needed for a user defined function call.

**容器描述**:

Choice container including the available actions to be used in the action lists.

##### 2. BswMArbitration

**容器属性**:

- **UUID**: `ECUC:1bb152a0-b36c-460c-bada-c3347399266e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMArbitration`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container includes all configuration sub-containers and parameters related to the mode arbitration functionality of the BswM.

###### 配置容器

本模块包含 **30** 个配置容器：

####### 1. BswMLogicalExpression

**容器属性**:

- **UUID**: `ECUC:24badaf3-6672-43f0-b3b0-3343c67796e6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLogicalExpression`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the logical expressions that can be used for the mode arbitration. The logical expressions are built of a set of arguments and a logical operator.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMLogicalOperator

- **UUID**: `ECUC:71652a7c-9360-42b3-9432-2cd58bfe7949`
- **参数名**: `BswMLogicalOperator`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_AND` (来源: AUTOSAR_ECUC)
  - `BSWM_NAND` (来源: AUTOSAR_ECUC)
  - `BSWM_OR` (来源: AUTOSAR_ECUC)
  - `BSWM_XOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the logical operator to be used in the logical expression. If the expression only consists of a single condition this parameter shall not be used.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. BswMArgumentRef

- **UUID**: `ECUC:509833cd-a9df-4ffb-ba49-a4fea4761bf3`
- **引用名**: `BswMArgumentRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMLogicalExpression`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMModeCondition`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a choice reference either to a mode condition or a sub-expression.

####### 2. BswMModeCondition

**容器属性**:

- **UUID**: `ECUC:55038f0f-7e6c-49bf-a155-df75c068efe5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeCondition`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the BswM mode conditions that can be used either by itself to form a rule or as a part of a logical expression.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMConditionType

- **UUID**: `ECUC:4f137728-854d-4d76-aa9c-311449567f09`
- **参数名**: `BswMConditionType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_EQUALS` (来源: AUTOSAR_ECUC)
  - `BSWM_EQUALS_NOT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies what kind of comparison that is made for the evaluation of the mode condition.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. BswMConditionMode

- **UUID**: `ECUC:6a6a7ef5-77b2-4220-b440-3c7ad95e6237`
- **引用名**: `BswMConditionMode`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMModeRequestPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMModeRequestPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references the mode request port that is used for the condition.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. BswMBswMode

**容器属性**:

- **UUID**: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the value and type of a mode in the BSW.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMBswRequestedMode

- **UUID**: `ECUC:04a0b0ee-322c-48dc-a12d-2287e87e2e44`
- **参数名**: `BswMBswRequestedMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the symbolic name (as a string) of a certain mode/state that can be requested/indicated by the BSW modules.

######### 2. BswMModeDeclaration

**容器属性**:

- **UUID**: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeDeclaration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMModeValueRef

- **UUID**: `ECUC:16d03c04-047d-4b09-b573-5986fdeff4ed`
- **引用名**: `BswMModeValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the mode requests corresponding to this condition.

######### 3. BswMConditionValue

**容器属性**:

- **UUID**: `ECUC:6dfef60d-1d6f-4b42-a4ae-f32d9a3df94f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMConditionValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswMode**
  - UUID: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
  - 描述: This container defines the value and type of a mode in the BSW.
- **BswMModeDeclaration**
  - UUID: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
  - 描述: When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

**容器描述**:

This container holds the parameters and references necessary to identify the mode type and the value that the mode request is compared to.

####### 3. BswMBswMode

**容器属性**:

- **UUID**: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the value and type of a mode in the BSW.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMBswRequestedMode

- **UUID**: `ECUC:04a0b0ee-322c-48dc-a12d-2287e87e2e44`
- **参数名**: `BswMBswRequestedMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the symbolic name (as a string) of a certain mode/state that can be requested/indicated by the BSW modules.

####### 4. BswMModeDeclaration

**容器属性**:

- **UUID**: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeDeclaration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMModeValueRef

- **UUID**: `ECUC:16d03c04-047d-4b09-b573-5986fdeff4ed`
- **引用名**: `BswMModeValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the mode requests corresponding to this condition.

####### 5. BswMModeRequestPort

**容器属性**:

- **UUID**: `ECUC:46239dbf-b616-4d8e-be72-4e2f06f0c7df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeRequestPort`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container defines a mode request interface that is used to requests or indicate modes from/to the BswM. These interfaces are implemented as ports or as ordinary C-functions based upon if the request is made by an SW-C or a BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMRequestProcessing

- **UUID**: `ECUC:a853591d-e671-4863-aa10-0082efe4dda1`
- **参数名**: `BswMRequestProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_DEFERRED` (来源: AUTOSAR_ECUC)
  - `BSWM_IMMEDIATE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the processing of the mode arbitration shall be done immediately when a mode request is received or if it shall be deferred to the processing of the main function of BswM.

######## 配置容器

本模块包含 **23** 个配置容器：

######### 1. BswMBswModeInitValue

**容器属性**:

- **UUID**: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMBswModeInitValueMode

- **UUID**: `ECUC:ce82e9c7-09eb-4a12-8e46-aaa2333a3fb7`
- **参数名**: `BswMBswModeInitValueMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the initial mode value that is used by BswM for the corresponding mode request after initialization.

######### 2. BswMSwcModeInitValue

**容器属性**:

- **UUID**: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwcModeInitValueRef

- **UUID**: `ECUC:087f03c1-56f6-4fdf-bba4-1050c4d08f8a`
- **引用名**: `BswMSwcModeInitValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the initialization of mode requests.

######### 3. BswMBswModeNotification

**容器属性**:

- **UUID**: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a Bsw Module.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMBswModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:d1c204e5-6c8a-45e9-a191-7cc780db6f12`
- **引用名**: `BswMBswModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration Group Prototype.

######### 4. BswMCanSMIndication

**容器属性**:

- **UUID**: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMCanSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the CAN State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMCanSMChannelRef

- **UUID**: `ECUC:45faeefb-4d0e-4a75-bac3-3fe76ff15822`
- **引用名**: `BswMCanSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the CAN channel handle that the mode request corresponds to.

######### 5. BswMComMIndication

**容器属性**:

- **UUID**: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current communication mode of a channel in the Communication Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMChannelRef

- **UUID**: `ECUC:4ad44a4c-b49e-4bff-99ef-aa813a13ee6e`
- **引用名**: `BswMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager channel handle that the indication corresponds to.

######### 6. BswMComMPncRequest

**容器属性**:

- **UUID**: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMPncRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMPncRef

- **UUID**: `ECUC:7b2f53bf-0115-4dc2-bd73-2ad6a4eac383`
- **引用名**: `BswMComMPncRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager PNC handle of the Partial Network Cluster that the request corresponds to.

######### 7. BswMDcmApplicationUpdatedIndication

**容器属性**:

- **UUID**: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmApplicationUpdatedIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.

######### 8. BswMDcmComModeRequest

**容器属性**:

- **UUID**: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmComModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is the Diagnostic Communication Manager.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMDcmComMNetwork

- **UUID**: `ECUC:2bd12696-b9c4-49a7-bec0-b38cf1de1d05`
- **参数名**: `BswMDcmComMNetwork`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the network the request relates to.

######### 9. BswMEcuMIndication

**容器属性**:

- **UUID**: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.

######### 10. BswMEcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMWakeupSource`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current state of an ECU State Manager wakeup source.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEcuMWakeupSrcRef

- **UUID**: `ECUC:c11bd4c1-5ed5-4ed5-8d1d-4d1370aeef89`
- **引用名**: `BswMEcuMWakeupSrcRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ECU State Manager Wakeup Source that the indication corresponds to.

######### 11. BswMEthSMIndication

**容器属性**:

- **UUID**: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEthSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the Ethernet State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEthSMChannelRef

- **UUID**: `ECUC:1276bcab-5dc0-4704-b50b-7b714bdcbf4a`
- **引用名**: `BswMEthSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Ethernet channel handle that the mode request corresponds to.

######### 12. BswMFrSMIndication

**容器属性**:

- **UUID**: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMFrSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the FlexRay State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMFrSMChannelRef

- **UUID**: `ECUC:58be722e-6d43-4ed1-b1f0-441da75ea1cc`
- **引用名**: `BswMFrSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the  FlexRay Cluster handle that the mode request corresponds to.

######### 13. BswMGenericRequest

**容器属性**:

- **UUID**: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMGenericRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. BswMModeRequesterId

- **UUID**: `ECUC:418ab994-a918-4944-ad81-e4720ddd8b56`
- **参数名**: `BswMModeRequesterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameters identifies the different users of the generic mode request interface.

############ 2. BswMRequestedModeMax

- **UUID**: `ECUC:5a53cdcf-97de-4ac2-9526-ecc1e037bad0`
- **参数名**: `BswMRequestedModeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper limit for the modes requested by this mode requester.

######### 14. BswMLinSMIndication

**容器属性**:

- **UUID**: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the LIN State Manager.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinSMChannelRef

- **UUID**: `ECUC:806494fe-5721-4700-9aff-afb9b96842f4`
- **引用名**: `BswMLinSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN channel handle that the mode request corresponds to.

######### 15. BswMLinScheduleIndication

**容器属性**:

- **UUID**: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinScheduleRef

- **UUID**: `ECUC:a377f06e-9872-4bba-9040-e413f8949261`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Schedule Table handle that the mode request corresponds to.

######### 16. BswMLinTpModeRequest

**容器属性**:

- **UUID**: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinTpModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinTpChannelRef

- **UUID**: `ECUC:2d8c4b55-134e-4e91-8aa2-8990b56a74c3`
- **引用名**: `BswMLinTpChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Interface Channel that the mode

######### 17. BswMNvMJobModeIndication

**容器属性**:

- **UUID**: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMJobModeIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMNvmService

- **UUID**: `ECUC:ac4b5a2a-a386-4bb4-b7b8-58a5baaefe2c`
- **参数名**: `BswMNvmService`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NvmReadAll` (来源: AUTOSAR_ECUC)
  - `NvmWriteAll` (来源: AUTOSAR_ECUC)
- **描述**: Identifies the Nvm job which is related to the mode request.

######### 18. BswMNvMRequest

**容器属性**:

- **UUID**: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMNvMBlockRef

- **UUID**: `ECUC:63b81990-3e16-437b-84f5-08451acf7709`
- **引用名**: `BswMNvMBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the NvM Block Descriptor that the request corresponds to.

######### 19. BswMSwcModeNotification

**容器属性**:

- **UUID**: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a mode switch notification associated with a RTE switch interface.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwcModeNotificationModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:5aa3f84f-623b-4f8a-846d-b0f2f8506bd5`
- **引用名**: `BswMSwcModeNotificationModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype.

######### 20. BswMSwcModeRequest

**容器属性**:

- **UUID**: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a SW Component.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwcModeRequestModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:106e96eb-0779-4153-b2f9-b05730aa991a`
- **引用名**: `BswMSwcModeRequestModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype. As the mode request is SR-Communication the BswM shall provide a SR-Interface which corresponds to the ModeDeclarationGroupPrototype.

######### 21. BswMWdgMRequestPartitionReset

**容器属性**:

- **UUID**: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMWdgMRequestPartitionReset`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a Partition Reset request from from the WdgM. This port

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. BswMWdgMRequestPartitionResetRef

- **UUID**: `ECUC:6770d76c-a522-43c4-961f-26d1d6e61afa`
- **引用名**: `BswMWdgMRequestPartitionResetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the partition that shall be reset.

######### 22. BswMModeInitValue

**容器属性**:

- **UUID**: `ECUC:a780195c-9698-494b-810e-d6f1b56cef30`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeInitValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswModeInitValue**
  - UUID: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
  - 描述: This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.
- **BswMSwcModeInitValue**
  - UUID: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
  - 描述: This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

**容器描述**:

This container defines the initial mode value that is used by BswM for the corresponding mode request after initialization. This container is optional and shall only be used for Mode Requests that do not already have an initial value.

######### 23. BswMModeRequestSource

**容器属性**:

- **UUID**: `ECUC:dd5d5587-bfd1-4960-a654-bcbc222aca93`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeRequestSource`
- **多重性**: [1..1]

**容器选择**:

- **BswMBswModeNotification**
  - UUID: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
  - 描述: The source of the mode request is a Bsw Module.
- **BswMCanSMIndication**
  - UUID: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
  - 描述: This is an indication of the current state of the CAN State Manager.
- **BswMComMIndication**
  - UUID: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
  - 描述: This is an indication of the current communication mode of a channel in the Communication Manager.
- **BswMComMPncRequest**
  - UUID: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
  - 描述: This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.
- **BswMDcmApplicationUpdatedIndication**
  - UUID: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
  - 描述: This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMDcmComModeRequest**
  - UUID: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
  - 描述: The source of the mode request is the Diagnostic Communication Manager.
- **BswMEcuMIndication**
  - UUID: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
  - 描述: This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMEcuMWakeupSource**
  - UUID: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
  - 描述: This is a notification of the current state of an ECU State Manager wakeup source.
- **BswMEthSMIndication**
  - UUID: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
  - 描述: This is an indication of the current state of the Ethernet State Manager.
- **BswMFrSMIndication**
  - UUID: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
  - 描述: This is an indication of the current state of the FlexRay State Manager.
- **BswMGenericRequest**
  - UUID: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
  - 描述: This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).
- **BswMLinSMIndication**
  - UUID: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
  - 描述: This is an indication of the current state of the LIN State Manager.
- **BswMLinScheduleIndication**
  - UUID: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
  - 描述: This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.
- **BswMLinTpModeRequest**
  - UUID: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
  - 描述: This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.
- **BswMNvMJobModeIndication**
  - UUID: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
  - 描述: Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:
- **BswMNvMRequest**
  - UUID: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
  - 描述: Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:
- **BswMSwcModeNotification**
  - UUID: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
  - 描述: This is a mode switch notification associated with a RTE switch interface.
- **BswMSwcModeRequest**
  - UUID: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
  - 描述: The source of the mode request is a SW Component.
- **BswMWdgMRequestPartitionReset**
  - UUID: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
  - 描述: This is a Partition Reset request from from the WdgM. This port

**容器描述**:

This choice container specifies the source of the mode request or state/mode indication. The requester of a mode can be both SW-C:s and other BSW Modules, such as the bus specific State Managers.

####### 6. BswMBswModeInitValue

**容器属性**:

- **UUID**: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMBswModeInitValueMode

- **UUID**: `ECUC:ce82e9c7-09eb-4a12-8e46-aaa2333a3fb7`
- **参数名**: `BswMBswModeInitValueMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the initial mode value that is used by BswM for the corresponding mode request after initialization.

####### 7. BswMSwcModeInitValue

**容器属性**:

- **UUID**: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwcModeInitValueRef

- **UUID**: `ECUC:087f03c1-56f6-4fdf-bba4-1050c4d08f8a`
- **引用名**: `BswMSwcModeInitValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the initialization of mode requests.

####### 8. BswMBswModeNotification

**容器属性**:

- **UUID**: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a Bsw Module.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMBswModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:d1c204e5-6c8a-45e9-a191-7cc780db6f12`
- **引用名**: `BswMBswModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration Group Prototype.

####### 9. BswMCanSMIndication

**容器属性**:

- **UUID**: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMCanSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the CAN State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMCanSMChannelRef

- **UUID**: `ECUC:45faeefb-4d0e-4a75-bac3-3fe76ff15822`
- **引用名**: `BswMCanSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the CAN channel handle that the mode request corresponds to.

####### 10. BswMComMIndication

**容器属性**:

- **UUID**: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current communication mode of a channel in the Communication Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMChannelRef

- **UUID**: `ECUC:4ad44a4c-b49e-4bff-99ef-aa813a13ee6e`
- **引用名**: `BswMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager channel handle that the indication corresponds to.

####### 11. BswMComMPncRequest

**容器属性**:

- **UUID**: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMPncRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMPncRef

- **UUID**: `ECUC:7b2f53bf-0115-4dc2-bd73-2ad6a4eac383`
- **引用名**: `BswMComMPncRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager PNC handle of the Partial Network Cluster that the request corresponds to.

####### 12. BswMDcmApplicationUpdatedIndication

**容器属性**:

- **UUID**: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmApplicationUpdatedIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.

####### 13. BswMDcmComModeRequest

**容器属性**:

- **UUID**: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmComModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is the Diagnostic Communication Manager.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMDcmComMNetwork

- **UUID**: `ECUC:2bd12696-b9c4-49a7-bec0-b38cf1de1d05`
- **参数名**: `BswMDcmComMNetwork`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the network the request relates to.

####### 14. BswMEcuMIndication

**容器属性**:

- **UUID**: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.

####### 15. BswMEcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMWakeupSource`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current state of an ECU State Manager wakeup source.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEcuMWakeupSrcRef

- **UUID**: `ECUC:c11bd4c1-5ed5-4ed5-8d1d-4d1370aeef89`
- **引用名**: `BswMEcuMWakeupSrcRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ECU State Manager Wakeup Source that the indication corresponds to.

####### 16. BswMEthSMIndication

**容器属性**:

- **UUID**: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEthSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the Ethernet State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEthSMChannelRef

- **UUID**: `ECUC:1276bcab-5dc0-4704-b50b-7b714bdcbf4a`
- **引用名**: `BswMEthSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Ethernet channel handle that the mode request corresponds to.

####### 17. BswMFrSMIndication

**容器属性**:

- **UUID**: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMFrSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the FlexRay State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMFrSMChannelRef

- **UUID**: `ECUC:58be722e-6d43-4ed1-b1f0-441da75ea1cc`
- **引用名**: `BswMFrSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the  FlexRay Cluster handle that the mode request corresponds to.

####### 18. BswMGenericRequest

**容器属性**:

- **UUID**: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMGenericRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. BswMModeRequesterId

- **UUID**: `ECUC:418ab994-a918-4944-ad81-e4720ddd8b56`
- **参数名**: `BswMModeRequesterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameters identifies the different users of the generic mode request interface.

########## 2. BswMRequestedModeMax

- **UUID**: `ECUC:5a53cdcf-97de-4ac2-9526-ecc1e037bad0`
- **参数名**: `BswMRequestedModeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper limit for the modes requested by this mode requester.

####### 19. BswMLinSMIndication

**容器属性**:

- **UUID**: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the LIN State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinSMChannelRef

- **UUID**: `ECUC:806494fe-5721-4700-9aff-afb9b96842f4`
- **引用名**: `BswMLinSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN channel handle that the mode request corresponds to.

####### 20. BswMLinScheduleIndication

**容器属性**:

- **UUID**: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinScheduleRef

- **UUID**: `ECUC:a377f06e-9872-4bba-9040-e413f8949261`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Schedule Table handle that the mode request corresponds to.

####### 21. BswMLinTpModeRequest

**容器属性**:

- **UUID**: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinTpModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinTpChannelRef

- **UUID**: `ECUC:2d8c4b55-134e-4e91-8aa2-8990b56a74c3`
- **引用名**: `BswMLinTpChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Interface Channel that the mode

####### 22. BswMNvMJobModeIndication

**容器属性**:

- **UUID**: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMJobModeIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMNvmService

- **UUID**: `ECUC:ac4b5a2a-a386-4bb4-b7b8-58a5baaefe2c`
- **参数名**: `BswMNvmService`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NvmReadAll` (来源: AUTOSAR_ECUC)
  - `NvmWriteAll` (来源: AUTOSAR_ECUC)
- **描述**: Identifies the Nvm job which is related to the mode request.

####### 23. BswMNvMRequest

**容器属性**:

- **UUID**: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMNvMBlockRef

- **UUID**: `ECUC:63b81990-3e16-437b-84f5-08451acf7709`
- **引用名**: `BswMNvMBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the NvM Block Descriptor that the request corresponds to.

####### 24. BswMSwcModeNotification

**容器属性**:

- **UUID**: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a mode switch notification associated with a RTE switch interface.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwcModeNotificationModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:5aa3f84f-623b-4f8a-846d-b0f2f8506bd5`
- **引用名**: `BswMSwcModeNotificationModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype.

####### 25. BswMSwcModeRequest

**容器属性**:

- **UUID**: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a SW Component.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwcModeRequestModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:106e96eb-0779-4153-b2f9-b05730aa991a`
- **引用名**: `BswMSwcModeRequestModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype. As the mode request is SR-Communication the BswM shall provide a SR-Interface which corresponds to the ModeDeclarationGroupPrototype.

####### 26. BswMWdgMRequestPartitionReset

**容器属性**:

- **UUID**: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMWdgMRequestPartitionReset`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a Partition Reset request from from the WdgM. This port

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. BswMWdgMRequestPartitionResetRef

- **UUID**: `ECUC:6770d76c-a522-43c4-961f-26d1d6e61afa`
- **引用名**: `BswMWdgMRequestPartitionResetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the partition that shall be reset.

####### 27. BswMRule

**容器属性**:

- **UUID**: `ECUC:9711550f-8c6a-4c9d-a1bd-b6d3828a9ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRule`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container describes a BswM arbitration rule. The rule either consists of a simple mode condition or a more complex logical expression. This container also references the action lists that shall be invoked when the rule is evaluated to True or False.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMNestedExecutionOnly

- **UUID**: `ECUC:75ab5231-5ebb-4aec-a088-bc956ba35023`
- **参数名**: `BswMNestedExecutionOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines for its related Rule if the Rule is an Independent rule or a Subordinate rule;

######### ENUMERATION 类型参数

########## 1. BswMRuleInitState

- **UUID**: `ECUC:42592c03-2e60-4cb0-8357-5a711cba0547`
- **参数名**: `BswMRuleInitState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FALSE` (来源: AUTOSAR_ECUC)
  - `BSWM_TRUE` (来源: AUTOSAR_ECUC)
  - `BSWM_UNDEFINED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a part of the reset/initialization behavior of BswM.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. BswMRuleExpressionRef

- **UUID**: `ECUC:f734f4cd-0746-4a1b-85b4-2791ac9d910e`
- **引用名**: `BswMRuleExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMLogicalExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMLogicalExpression`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This choice reference either references the mode condition or the logical expression that is evaluated for each rule.

########## 2. BswMRuleFalseActionList

- **UUID**: `ECUC:cd76267f-738a-4738-ac2c-7b7d38b31ffa`
- **引用名**: `BswMRuleFalseActionList`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `BswMActionList`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the action list that shall be executed when the rule is evaluated to False

########## 3. BswMRuleTrueActionList

- **UUID**: `ECUC:309d8777-fea3-4ded-a73e-980296f093aa`
- **引用名**: `BswMRuleTrueActionList`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `BswMActionList`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the action list that shall be executed when the rule is evaluated to True

####### 28. BswMConditionValue

**容器属性**:

- **UUID**: `ECUC:6dfef60d-1d6f-4b42-a4ae-f32d9a3df94f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMConditionValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswMode**
  - UUID: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
  - 描述: This container defines the value and type of a mode in the BSW.
- **BswMModeDeclaration**
  - UUID: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
  - 描述: When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

**容器描述**:

This container holds the parameters and references necessary to identify the mode type and the value that the mode request is compared to.

####### 29. BswMModeInitValue

**容器属性**:

- **UUID**: `ECUC:a780195c-9698-494b-810e-d6f1b56cef30`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeInitValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswModeInitValue**
  - UUID: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
  - 描述: This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.
- **BswMSwcModeInitValue**
  - UUID: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
  - 描述: This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

**容器描述**:

This container defines the initial mode value that is used by BswM for the corresponding mode request after initialization. This container is optional and shall only be used for Mode Requests that do not already have an initial value.

####### 30. BswMModeRequestSource

**容器属性**:

- **UUID**: `ECUC:dd5d5587-bfd1-4960-a654-bcbc222aca93`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeRequestSource`
- **多重性**: [1..1]

**容器选择**:

- **BswMBswModeNotification**
  - UUID: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
  - 描述: The source of the mode request is a Bsw Module.
- **BswMCanSMIndication**
  - UUID: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
  - 描述: This is an indication of the current state of the CAN State Manager.
- **BswMComMIndication**
  - UUID: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
  - 描述: This is an indication of the current communication mode of a channel in the Communication Manager.
- **BswMComMPncRequest**
  - UUID: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
  - 描述: This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.
- **BswMDcmApplicationUpdatedIndication**
  - UUID: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
  - 描述: This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMDcmComModeRequest**
  - UUID: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
  - 描述: The source of the mode request is the Diagnostic Communication Manager.
- **BswMEcuMIndication**
  - UUID: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
  - 描述: This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMEcuMWakeupSource**
  - UUID: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
  - 描述: This is a notification of the current state of an ECU State Manager wakeup source.
- **BswMEthSMIndication**
  - UUID: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
  - 描述: This is an indication of the current state of the Ethernet State Manager.
- **BswMFrSMIndication**
  - UUID: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
  - 描述: This is an indication of the current state of the FlexRay State Manager.
- **BswMGenericRequest**
  - UUID: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
  - 描述: This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).
- **BswMLinSMIndication**
  - UUID: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
  - 描述: This is an indication of the current state of the LIN State Manager.
- **BswMLinScheduleIndication**
  - UUID: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
  - 描述: This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.
- **BswMLinTpModeRequest**
  - UUID: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
  - 描述: This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.
- **BswMNvMJobModeIndication**
  - UUID: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
  - 描述: Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:
- **BswMNvMRequest**
  - UUID: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
  - 描述: Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:
- **BswMSwcModeNotification**
  - UUID: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
  - 描述: This is a mode switch notification associated with a RTE switch interface.
- **BswMSwcModeRequest**
  - UUID: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
  - 描述: The source of the mode request is a SW Component.
- **BswMWdgMRequestPartitionReset**
  - UUID: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
  - 描述: This is a Partition Reset request from from the WdgM. This port

**容器描述**:

This choice container specifies the source of the mode request or state/mode indication. The requester of a mode can be both SW-C:s and other BSW Modules, such as the bus specific State Managers.

##### 3. BswMLogicalExpression

**容器属性**:

- **UUID**: `ECUC:24badaf3-6672-43f0-b3b0-3343c67796e6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLogicalExpression`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the logical expressions that can be used for the mode arbitration. The logical expressions are built of a set of arguments and a logical operator.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. BswMLogicalOperator

- **UUID**: `ECUC:71652a7c-9360-42b3-9432-2cd58bfe7949`
- **参数名**: `BswMLogicalOperator`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_AND` (来源: AUTOSAR_ECUC)
  - `BSWM_NAND` (来源: AUTOSAR_ECUC)
  - `BSWM_OR` (来源: AUTOSAR_ECUC)
  - `BSWM_XOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the logical operator to be used in the logical expression. If the expression only consists of a single condition this parameter shall not be used.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. BswMArgumentRef

- **UUID**: `ECUC:509833cd-a9df-4ffb-ba49-a4fea4761bf3`
- **引用名**: `BswMArgumentRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMLogicalExpression`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMModeCondition`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a choice reference either to a mode condition or a sub-expression.

##### 4. BswMModeCondition

**容器属性**:

- **UUID**: `ECUC:55038f0f-7e6c-49bf-a155-df75c068efe5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeCondition`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container describes the BswM mode conditions that can be used either by itself to form a rule or as a part of a logical expression.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. BswMConditionType

- **UUID**: `ECUC:4f137728-854d-4d76-aa9c-311449567f09`
- **参数名**: `BswMConditionType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_EQUALS` (来源: AUTOSAR_ECUC)
  - `BSWM_EQUALS_NOT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies what kind of comparison that is made for the evaluation of the mode condition.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. BswMConditionMode

- **UUID**: `ECUC:6a6a7ef5-77b2-4220-b440-3c7ad95e6237`
- **引用名**: `BswMConditionMode`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMModeRequestPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMModeRequestPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references the mode request port that is used for the condition.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. BswMBswMode

**容器属性**:

- **UUID**: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the value and type of a mode in the BSW.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMBswRequestedMode

- **UUID**: `ECUC:04a0b0ee-322c-48dc-a12d-2287e87e2e44`
- **参数名**: `BswMBswRequestedMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the symbolic name (as a string) of a certain mode/state that can be requested/indicated by the BSW modules.

####### 2. BswMModeDeclaration

**容器属性**:

- **UUID**: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeDeclaration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMModeValueRef

- **UUID**: `ECUC:16d03c04-047d-4b09-b573-5986fdeff4ed`
- **引用名**: `BswMModeValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the mode requests corresponding to this condition.

####### 3. BswMConditionValue

**容器属性**:

- **UUID**: `ECUC:6dfef60d-1d6f-4b42-a4ae-f32d9a3df94f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMConditionValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswMode**
  - UUID: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
  - 描述: This container defines the value and type of a mode in the BSW.
- **BswMModeDeclaration**
  - UUID: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
  - 描述: When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

**容器描述**:

This container holds the parameters and references necessary to identify the mode type and the value that the mode request is compared to.

##### 5. BswMBswMode

**容器属性**:

- **UUID**: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the value and type of a mode in the BSW.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. BswMBswRequestedMode

- **UUID**: `ECUC:04a0b0ee-322c-48dc-a12d-2287e87e2e44`
- **参数名**: `BswMBswRequestedMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the symbolic name (as a string) of a certain mode/state that can be requested/indicated by the BSW modules.

##### 6. BswMModeDeclaration

**容器属性**:

- **UUID**: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeDeclaration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. BswMModeValueRef

- **UUID**: `ECUC:16d03c04-047d-4b09-b573-5986fdeff4ed`
- **引用名**: `BswMModeValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the mode requests corresponding to this condition.

##### 7. BswMModeRequestPort

**容器属性**:

- **UUID**: `ECUC:46239dbf-b616-4d8e-be72-4e2f06f0c7df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeRequestPort`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container defines a mode request interface that is used to requests or indicate modes from/to the BswM. These interfaces are implemented as ports or as ordinary C-functions based upon if the request is made by an SW-C or a BSW module.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. BswMRequestProcessing

- **UUID**: `ECUC:a853591d-e671-4863-aa10-0082efe4dda1`
- **参数名**: `BswMRequestProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_DEFERRED` (来源: AUTOSAR_ECUC)
  - `BSWM_IMMEDIATE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the processing of the mode arbitration shall be done immediately when a mode request is received or if it shall be deferred to the processing of the main function of BswM.

###### 配置容器

本模块包含 **23** 个配置容器：

####### 1. BswMBswModeInitValue

**容器属性**:

- **UUID**: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMBswModeInitValueMode

- **UUID**: `ECUC:ce82e9c7-09eb-4a12-8e46-aaa2333a3fb7`
- **参数名**: `BswMBswModeInitValueMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the initial mode value that is used by BswM for the corresponding mode request after initialization.

####### 2. BswMSwcModeInitValue

**容器属性**:

- **UUID**: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwcModeInitValueRef

- **UUID**: `ECUC:087f03c1-56f6-4fdf-bba4-1050c4d08f8a`
- **引用名**: `BswMSwcModeInitValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the initialization of mode requests.

####### 3. BswMBswModeNotification

**容器属性**:

- **UUID**: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a Bsw Module.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMBswModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:d1c204e5-6c8a-45e9-a191-7cc780db6f12`
- **引用名**: `BswMBswModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration Group Prototype.

####### 4. BswMCanSMIndication

**容器属性**:

- **UUID**: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMCanSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the CAN State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMCanSMChannelRef

- **UUID**: `ECUC:45faeefb-4d0e-4a75-bac3-3fe76ff15822`
- **引用名**: `BswMCanSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the CAN channel handle that the mode request corresponds to.

####### 5. BswMComMIndication

**容器属性**:

- **UUID**: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current communication mode of a channel in the Communication Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMChannelRef

- **UUID**: `ECUC:4ad44a4c-b49e-4bff-99ef-aa813a13ee6e`
- **引用名**: `BswMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager channel handle that the indication corresponds to.

####### 6. BswMComMPncRequest

**容器属性**:

- **UUID**: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMPncRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMPncRef

- **UUID**: `ECUC:7b2f53bf-0115-4dc2-bd73-2ad6a4eac383`
- **引用名**: `BswMComMPncRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager PNC handle of the Partial Network Cluster that the request corresponds to.

####### 7. BswMDcmApplicationUpdatedIndication

**容器属性**:

- **UUID**: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmApplicationUpdatedIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.

####### 8. BswMDcmComModeRequest

**容器属性**:

- **UUID**: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmComModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is the Diagnostic Communication Manager.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMDcmComMNetwork

- **UUID**: `ECUC:2bd12696-b9c4-49a7-bec0-b38cf1de1d05`
- **参数名**: `BswMDcmComMNetwork`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the network the request relates to.

####### 9. BswMEcuMIndication

**容器属性**:

- **UUID**: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.

####### 10. BswMEcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMWakeupSource`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current state of an ECU State Manager wakeup source.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEcuMWakeupSrcRef

- **UUID**: `ECUC:c11bd4c1-5ed5-4ed5-8d1d-4d1370aeef89`
- **引用名**: `BswMEcuMWakeupSrcRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ECU State Manager Wakeup Source that the indication corresponds to.

####### 11. BswMEthSMIndication

**容器属性**:

- **UUID**: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEthSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the Ethernet State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEthSMChannelRef

- **UUID**: `ECUC:1276bcab-5dc0-4704-b50b-7b714bdcbf4a`
- **引用名**: `BswMEthSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Ethernet channel handle that the mode request corresponds to.

####### 12. BswMFrSMIndication

**容器属性**:

- **UUID**: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMFrSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the FlexRay State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMFrSMChannelRef

- **UUID**: `ECUC:58be722e-6d43-4ed1-b1f0-441da75ea1cc`
- **引用名**: `BswMFrSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the  FlexRay Cluster handle that the mode request corresponds to.

####### 13. BswMGenericRequest

**容器属性**:

- **UUID**: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMGenericRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. BswMModeRequesterId

- **UUID**: `ECUC:418ab994-a918-4944-ad81-e4720ddd8b56`
- **参数名**: `BswMModeRequesterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameters identifies the different users of the generic mode request interface.

########## 2. BswMRequestedModeMax

- **UUID**: `ECUC:5a53cdcf-97de-4ac2-9526-ecc1e037bad0`
- **参数名**: `BswMRequestedModeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper limit for the modes requested by this mode requester.

####### 14. BswMLinSMIndication

**容器属性**:

- **UUID**: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the LIN State Manager.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinSMChannelRef

- **UUID**: `ECUC:806494fe-5721-4700-9aff-afb9b96842f4`
- **引用名**: `BswMLinSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN channel handle that the mode request corresponds to.

####### 15. BswMLinScheduleIndication

**容器属性**:

- **UUID**: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinScheduleRef

- **UUID**: `ECUC:a377f06e-9872-4bba-9040-e413f8949261`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Schedule Table handle that the mode request corresponds to.

####### 16. BswMLinTpModeRequest

**容器属性**:

- **UUID**: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinTpModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinTpChannelRef

- **UUID**: `ECUC:2d8c4b55-134e-4e91-8aa2-8990b56a74c3`
- **引用名**: `BswMLinTpChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Interface Channel that the mode

####### 17. BswMNvMJobModeIndication

**容器属性**:

- **UUID**: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMJobModeIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMNvmService

- **UUID**: `ECUC:ac4b5a2a-a386-4bb4-b7b8-58a5baaefe2c`
- **参数名**: `BswMNvmService`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NvmReadAll` (来源: AUTOSAR_ECUC)
  - `NvmWriteAll` (来源: AUTOSAR_ECUC)
- **描述**: Identifies the Nvm job which is related to the mode request.

####### 18. BswMNvMRequest

**容器属性**:

- **UUID**: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMNvMBlockRef

- **UUID**: `ECUC:63b81990-3e16-437b-84f5-08451acf7709`
- **引用名**: `BswMNvMBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the NvM Block Descriptor that the request corresponds to.

####### 19. BswMSwcModeNotification

**容器属性**:

- **UUID**: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a mode switch notification associated with a RTE switch interface.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwcModeNotificationModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:5aa3f84f-623b-4f8a-846d-b0f2f8506bd5`
- **引用名**: `BswMSwcModeNotificationModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype.

####### 20. BswMSwcModeRequest

**容器属性**:

- **UUID**: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a SW Component.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwcModeRequestModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:106e96eb-0779-4153-b2f9-b05730aa991a`
- **引用名**: `BswMSwcModeRequestModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype. As the mode request is SR-Communication the BswM shall provide a SR-Interface which corresponds to the ModeDeclarationGroupPrototype.

####### 21. BswMWdgMRequestPartitionReset

**容器属性**:

- **UUID**: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMWdgMRequestPartitionReset`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a Partition Reset request from from the WdgM. This port

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. BswMWdgMRequestPartitionResetRef

- **UUID**: `ECUC:6770d76c-a522-43c4-961f-26d1d6e61afa`
- **引用名**: `BswMWdgMRequestPartitionResetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the partition that shall be reset.

####### 22. BswMModeInitValue

**容器属性**:

- **UUID**: `ECUC:a780195c-9698-494b-810e-d6f1b56cef30`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeInitValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswModeInitValue**
  - UUID: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
  - 描述: This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.
- **BswMSwcModeInitValue**
  - UUID: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
  - 描述: This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

**容器描述**:

This container defines the initial mode value that is used by BswM for the corresponding mode request after initialization. This container is optional and shall only be used for Mode Requests that do not already have an initial value.

####### 23. BswMModeRequestSource

**容器属性**:

- **UUID**: `ECUC:dd5d5587-bfd1-4960-a654-bcbc222aca93`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeRequestSource`
- **多重性**: [1..1]

**容器选择**:

- **BswMBswModeNotification**
  - UUID: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
  - 描述: The source of the mode request is a Bsw Module.
- **BswMCanSMIndication**
  - UUID: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
  - 描述: This is an indication of the current state of the CAN State Manager.
- **BswMComMIndication**
  - UUID: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
  - 描述: This is an indication of the current communication mode of a channel in the Communication Manager.
- **BswMComMPncRequest**
  - UUID: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
  - 描述: This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.
- **BswMDcmApplicationUpdatedIndication**
  - UUID: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
  - 描述: This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMDcmComModeRequest**
  - UUID: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
  - 描述: The source of the mode request is the Diagnostic Communication Manager.
- **BswMEcuMIndication**
  - UUID: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
  - 描述: This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMEcuMWakeupSource**
  - UUID: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
  - 描述: This is a notification of the current state of an ECU State Manager wakeup source.
- **BswMEthSMIndication**
  - UUID: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
  - 描述: This is an indication of the current state of the Ethernet State Manager.
- **BswMFrSMIndication**
  - UUID: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
  - 描述: This is an indication of the current state of the FlexRay State Manager.
- **BswMGenericRequest**
  - UUID: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
  - 描述: This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).
- **BswMLinSMIndication**
  - UUID: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
  - 描述: This is an indication of the current state of the LIN State Manager.
- **BswMLinScheduleIndication**
  - UUID: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
  - 描述: This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.
- **BswMLinTpModeRequest**
  - UUID: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
  - 描述: This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.
- **BswMNvMJobModeIndication**
  - UUID: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
  - 描述: Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:
- **BswMNvMRequest**
  - UUID: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
  - 描述: Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:
- **BswMSwcModeNotification**
  - UUID: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
  - 描述: This is a mode switch notification associated with a RTE switch interface.
- **BswMSwcModeRequest**
  - UUID: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
  - 描述: The source of the mode request is a SW Component.
- **BswMWdgMRequestPartitionReset**
  - UUID: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
  - 描述: This is a Partition Reset request from from the WdgM. This port

**容器描述**:

This choice container specifies the source of the mode request or state/mode indication. The requester of a mode can be both SW-C:s and other BSW Modules, such as the bus specific State Managers.

##### 8. BswMBswModeInitValue

**容器属性**:

- **UUID**: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. BswMBswModeInitValueMode

- **UUID**: `ECUC:ce82e9c7-09eb-4a12-8e46-aaa2333a3fb7`
- **参数名**: `BswMBswModeInitValueMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the initial mode value that is used by BswM for the corresponding mode request after initialization.

##### 9. BswMSwcModeInitValue

**容器属性**:

- **UUID**: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeInitValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. BswMSwcModeInitValueRef

- **UUID**: `ECUC:087f03c1-56f6-4fdf-bba4-1050c4d08f8a`
- **引用名**: `BswMSwcModeInitValueRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration used for the initialization of mode requests.

##### 10. BswMBswModeNotification

**容器属性**:

- **UUID**: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMBswModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a Bsw Module.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. BswMBswModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:d1c204e5-6c8a-45e9-a191-7cc780db6f12`
- **引用名**: `BswMBswModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the Mode Declaration Group Prototype.

##### 11. BswMCanSMIndication

**容器属性**:

- **UUID**: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMCanSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the CAN State Manager.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMCanSMChannelRef

- **UUID**: `ECUC:45faeefb-4d0e-4a75-bac3-3fe76ff15822`
- **引用名**: `BswMCanSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the CAN channel handle that the mode request corresponds to.

##### 12. BswMComMIndication

**容器属性**:

- **UUID**: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current communication mode of a channel in the Communication Manager.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMComMChannelRef

- **UUID**: `ECUC:4ad44a4c-b49e-4bff-99ef-aa813a13ee6e`
- **引用名**: `BswMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager channel handle that the indication corresponds to.

##### 13. BswMComMPncRequest

**容器属性**:

- **UUID**: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMPncRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMComMPncRef

- **UUID**: `ECUC:7b2f53bf-0115-4dc2-bd73-2ad6a4eac383`
- **引用名**: `BswMComMPncRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Communication Manager PNC handle of the Partial Network Cluster that the request corresponds to.

##### 14. BswMDcmApplicationUpdatedIndication

**容器属性**:

- **UUID**: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmApplicationUpdatedIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.

##### 15. BswMDcmComModeRequest

**容器属性**:

- **UUID**: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDcmComModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is the Diagnostic Communication Manager.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. BswMDcmComMNetwork

- **UUID**: `ECUC:2bd12696-b9c4-49a7-bec0-b38cf1de1d05`
- **参数名**: `BswMDcmComMNetwork`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the network the request relates to.

##### 16. BswMEcuMIndication

**容器属性**:

- **UUID**: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.

##### 17. BswMEcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMWakeupSource`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a notification of the current state of an ECU State Manager wakeup source.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMEcuMWakeupSrcRef

- **UUID**: `ECUC:c11bd4c1-5ed5-4ed5-8d1d-4d1370aeef89`
- **引用名**: `BswMEcuMWakeupSrcRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ECU State Manager Wakeup Source that the indication corresponds to.

##### 18. BswMEthSMIndication

**容器属性**:

- **UUID**: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEthSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the Ethernet State Manager.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMEthSMChannelRef

- **UUID**: `ECUC:1276bcab-5dc0-4704-b50b-7b714bdcbf4a`
- **引用名**: `BswMEthSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the Ethernet channel handle that the mode request corresponds to.

##### 19. BswMFrSMIndication

**容器属性**:

- **UUID**: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMFrSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the FlexRay State Manager.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMFrSMChannelRef

- **UUID**: `ECUC:58be722e-6d43-4ed1-b1f0-441da75ea1cc`
- **引用名**: `BswMFrSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the  FlexRay Cluster handle that the mode request corresponds to.

##### 20. BswMGenericRequest

**容器属性**:

- **UUID**: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMGenericRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. BswMModeRequesterId

- **UUID**: `ECUC:418ab994-a918-4944-ad81-e4720ddd8b56`
- **参数名**: `BswMModeRequesterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameters identifies the different users of the generic mode request interface.

######## 2. BswMRequestedModeMax

- **UUID**: `ECUC:5a53cdcf-97de-4ac2-9526-ecc1e037bad0`
- **参数名**: `BswMRequestedModeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper limit for the modes requested by this mode requester.

##### 21. BswMLinSMIndication

**容器属性**:

- **UUID**: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinSMIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the current state of the LIN State Manager.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMLinSMChannelRef

- **UUID**: `ECUC:806494fe-5721-4700-9aff-afb9b96842f4`
- **引用名**: `BswMLinSMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN channel handle that the mode request corresponds to.

##### 22. BswMLinScheduleIndication

**容器属性**:

- **UUID**: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMLinScheduleRef

- **UUID**: `ECUC:a377f06e-9872-4bba-9040-e413f8949261`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Schedule Table handle that the mode request corresponds to.

##### 23. BswMLinTpModeRequest

**容器属性**:

- **UUID**: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinTpModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMLinTpChannelRef

- **UUID**: `ECUC:2d8c4b55-134e-4e91-8aa2-8990b56a74c3`
- **引用名**: `BswMLinTpChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN Interface Channel that the mode

##### 24. BswMNvMJobModeIndication

**容器属性**:

- **UUID**: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMJobModeIndication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. BswMNvmService

- **UUID**: `ECUC:ac4b5a2a-a386-4bb4-b7b8-58a5baaefe2c`
- **参数名**: `BswMNvmService`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NvmReadAll` (来源: AUTOSAR_ECUC)
  - `NvmWriteAll` (来源: AUTOSAR_ECUC)
- **描述**: Identifies the Nvm job which is related to the mode request.

##### 25. BswMNvMRequest

**容器属性**:

- **UUID**: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNvMRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMNvMBlockRef

- **UUID**: `ECUC:63b81990-3e16-437b-84f5-08451acf7709`
- **引用名**: `BswMNvMBlockRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the NvM Block Descriptor that the request corresponds to.

##### 26. BswMSwcModeNotification

**容器属性**:

- **UUID**: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeNotification`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a mode switch notification associated with a RTE switch interface.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. BswMSwcModeNotificationModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:5aa3f84f-623b-4f8a-846d-b0f2f8506bd5`
- **引用名**: `BswMSwcModeNotificationModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype.

##### 27. BswMSwcModeRequest

**容器属性**:

- **UUID**: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwcModeRequest`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The source of the mode request is a SW Component.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. BswMSwcModeRequestModeDeclarationGroupPrototypeRef

- **UUID**: `ECUC:106e96eb-0779-4153-b2f9-b05730aa991a`
- **引用名**: `BswMSwcModeRequestModeDeclarationGroupPrototypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION-GROUP-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a foreign reference to the ModeDeclarationGroupPrototype. As the mode request is SR-Communication the BswM shall provide a SR-Interface which corresponds to the ModeDeclarationGroupPrototype.

##### 28. BswMWdgMRequestPartitionReset

**容器属性**:

- **UUID**: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMWdgMRequestPartitionReset`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This is a Partition Reset request from from the WdgM. This port

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. BswMWdgMRequestPartitionResetRef

- **UUID**: `ECUC:6770d76c-a522-43c4-961f-26d1d6e61afa`
- **引用名**: `BswMWdgMRequestPartitionResetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the partition that shall be reset.

##### 29. BswMRule

**容器属性**:

- **UUID**: `ECUC:9711550f-8c6a-4c9d-a1bd-b6d3828a9ce5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRule`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container describes a BswM arbitration rule. The rule either consists of a simple mode condition or a more complex logical expression. This container also references the action lists that shall be invoked when the rule is evaluated to True or False.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. BswMNestedExecutionOnly

- **UUID**: `ECUC:75ab5231-5ebb-4aec-a088-bc956ba35023`
- **参数名**: `BswMNestedExecutionOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines for its related Rule if the Rule is an Independent rule or a Subordinate rule;

####### ENUMERATION 类型参数

######## 1. BswMRuleInitState

- **UUID**: `ECUC:42592c03-2e60-4cb0-8357-5a711cba0547`
- **参数名**: `BswMRuleInitState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FALSE` (来源: AUTOSAR_ECUC)
  - `BSWM_TRUE` (来源: AUTOSAR_ECUC)
  - `BSWM_UNDEFINED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a part of the reset/initialization behavior of BswM.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. BswMRuleExpressionRef

- **UUID**: `ECUC:f734f4cd-0746-4a1b-85b4-2791ac9d910e`
- **引用名**: `BswMRuleExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMLogicalExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMLogicalExpression`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This choice reference either references the mode condition or the logical expression that is evaluated for each rule.

######## 2. BswMRuleFalseActionList

- **UUID**: `ECUC:cd76267f-738a-4738-ac2c-7b7d38b31ffa`
- **引用名**: `BswMRuleFalseActionList`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `BswMActionList`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the action list that shall be executed when the rule is evaluated to False

######## 3. BswMRuleTrueActionList

- **UUID**: `ECUC:309d8777-fea3-4ded-a73e-980296f093aa`
- **引用名**: `BswMRuleTrueActionList`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `BswMActionList`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the action list that shall be executed when the rule is evaluated to True

##### 30. BswMDataTypeMappingSets

**容器属性**:

- **UUID**: `ECUC:fd679d55-8201-4daf-8762-a432eb79cb8c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDataTypeMappingSets`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Collection of references to DataTypeMappingSet.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. BswMDataTypeMappingSetRef

- **UUID**: `ECUC:f0b7d567-bfdf-47c7-8459-32f20d811612`
- **引用名**: `BswMDataTypeMappingSetRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..infinite]
- **目标类型**: DATA-TYPE-MAPPING-SET
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DataTypeMappingSet.

##### 31. BswMModeControl

**容器属性**:

- **UUID**: `ECUC:0f9b55d8-de62-4333-96a5-061519c7ffc1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMModeControl`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container includes all configuration sub-containers and parameters related to the mode control functionality of the BswM.

###### 配置容器

本模块包含 **22** 个配置容器：

####### 1. BswMAction

**容器属性**:

- **UUID**: `ECUC:add00e45-e97c-4d9a-8208-befcbfbfd3e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMAction`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each container of this type defines an action. These actions can be part of one or several action lists.

######## 配置容器

本模块包含 **18** 个配置容器：

######### 1. BswMComMAllowCom

**容器属性**:

- **UUID**: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMAllowCom`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMComAllowed

- **UUID**: `ECUC:a75f55aa-9e34-48e5-9c33-8e121ac7f7d8`
- **参数名**: `BswMComAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter BswMComMAllowChannelRef refers to a channel which will allow or block communication using the function ComM_CommunicationAllowed().

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMAllowChannelRef

- **UUID**: `ECUC:cfa3f8ee-4192-4364-a046-f5ef39f8626f`
- **引用名**: `BswMComMAllowChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM Channel for which communication shall be allowed or blocked.

######### 2. BswMComMModeLimitation

**容器属性**:

- **UUID**: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeLimitation`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMComMLimitMode

- **UUID**: `ECUC:a90697cd-02ca-46c7-b4d9-3561ac126656`
- **参数名**: `BswMComMLimitMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function ComM_LimitChannelToNoComMode() takes in this boolean parameter to limit the channel's com mode to no-com mode.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMLimitChannelRef

- **UUID**: `ECUC:dfb83a13-105c-4ad9-b65d-8465bcad8ddd`
- **引用名**: `BswMComMLimitChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM channel for which the communication mode should be limited.

######### 3. BswMComMModeSwitch

**容器属性**:

- **UUID**: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMComMRequestedMode

- **UUID**: `ECUC:a8479736-a047-4a2e-a9de-9de9d1fe5e26`
- **参数名**: `BswMComMRequestedMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FULL_COM` (来源: AUTOSAR_ECUC)
  - `BSWM_NO_COM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the requested communication mode.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMUserRef

- **UUID**: `ECUC:38ab9166-a9b6-4666-8064-b0fe9192d7af`
- **引用名**: `BswMComMUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM User that is associated to the Communication channel for which the communication mode should be requested.

######### 4. BswMDeadlineMonitoringControl

**容器属性**:

- **UUID**: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDeadlineMonitoringControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMDisabledDMPduGroupRef

- **UUID**: `ECUC:858f665d-7fc6-49e4-a22a-b512c6e0b69b`
- **引用名**: `BswMDisabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be disabled.

############ 2. BswMEnabledDMPduGroupRef

- **UUID**: `ECUC:489675a3-4dfa-43b5-8f8e-48609a142a1d`
- **引用名**: `BswMEnabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be enabled.

######### 5. BswMEcuMGoDown

**容器属性**:

- **UUID**: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMGoDown`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the UserId which shall be forwarded to the GoDown request.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEcuMUserIdRef

- **UUID**: `ECUC:5bf3393d-903b-435c-822a-e8df76b79337`
- **引用名**: `BswMEcuMUserIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a EcuM UserId.

######### 6. BswMEcuMSelectShutdownTarget

**容器属性**:

- **UUID**: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMSelectShutdownTarget`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the shutdown target.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMEcuMShutdownTargetRef

- **UUID**: `ECUC:46e261aa-240e-40c3-8b60-5242f58edfb2`
- **引用名**: `BswMEcuMShutdownTargetRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a shutdown target.

######### 7. BswMLinScheduleSwitch

**容器属性**:

- **UUID**: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMLinScheduleRef

- **UUID**: `ECUC:32b27d57-fa6d-4f23-a0c7-f872b0d789a0`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN schedule table that the LIN SM shall change to.

######### 8. BswMNMControl

**容器属性**:

- **UUID**: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNMControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswMNMAction

- **UUID**: `ECUC:b0783d19-a6d0-4699-ac8c-a4049b4d461e`
- **参数名**: `BswMNMAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_NM_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_NM_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the communication of the corresponding NM channel should be enabled or disabled.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMComMNetworkHandleRef

- **UUID**: `ECUC:71f03668-a386-4d49-b226-dd2c739ebc06`
- **引用名**: `BswMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

######### 9. BswMPduGroupSwitch

**容器属性**:

- **UUID**: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduGroupSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMPduGroupSwitchReinit

- **UUID**: `ECUC:b6fb3fbb-cb5c-4d7a-9560-c5bc39a5da54`
- **参数名**: `BswMPduGroupSwitchReinit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the values for the parameters like periodical timer, minimum delay timer etc is retainer or reinitialized during a PDU Group Switch.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMDisabledPduGroupRef

- **UUID**: `ECUC:d63a77a6-da9d-467a-9c2f-6879f96a8b50`
- **引用名**: `BswMDisabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be disabled.

############ 2. BswMEnabledPduGroupRef

- **UUID**: `ECUC:754e70f9-ccd0-4a90-8e06-58d065bb4184`
- **引用名**: `BswMEnabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be enabled.

######### 10. BswMPduRouterControl

**容器属性**:

- **UUID**: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduRouterControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. BswPduRouterAction

- **UUID**: `ECUC:7a7d7b39-fdff-4f16-9aa1-9ea5d6b3f02f`
- **参数名**: `BswPduRouterAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_PDUR_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_PDUR_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the routing of the corresponding PDU should be enabled or disabled.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMPduRoutingPathGroupRef

- **UUID**: `ECUC:edbfb25c-322b-4d20-93f0-b1e32d0f50f5`
- **引用名**: `BswMPduRoutingPathGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `PduRRoutingPathGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRRoutingPathGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the PDU Routing Path Group for which the routing in the PDU Router should be enabled or disabled.

######### 11. BswMRteSwitch

**容器属性**:

- **UUID**: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRteSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. BswMRteSwitchPortRef

- **UUID**: `ECUC:4642d375-9c6d-4db5-84c5-fb8e6d59972c`
- **引用名**: `BswMRteSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSwitchedMode

- **UUID**: `ECUC:3d6f5054-ebed-40f3-9abc-b366bc6a8017`
- **引用名**: `BswMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

######### 12. BswMSchMSwitch

**容器属性**:

- **UUID**: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSchMSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. BswMSchMSwitchPortRef

- **UUID**: `ECUC:e18f3107-9272-4ace-95ac-cfce6556be97`
- **引用名**: `BswMSchMSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

########### FOREIGN-REFERENCE 类型引用

############ 1. BswMSchMSwitchedMode

- **UUID**: `ECUC:8223503b-58a4-4608-9fe1-4317c3c27858`
- **引用名**: `BswMSchMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

######### 13. BswMSwitchIPduMode

**容器属性**:

- **UUID**: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchIPduMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. BswMSwitchIPduModeValue

- **UUID**: `ECUC:75026229-698c-4fbc-a905-6652e28355d6`
- **参数名**: `BswMSwitchIPduModeValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines which transmission mode shall be selected during this call.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMSwitchIPduModeRef

- **UUID**: `ECUC:2629fedf-9668-4d93-af1e-99e2346f915f`
- **引用名**: `BswMSwitchIPduModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU for which the transmission mode shall be set.

######### 14. BswMTriggerIPduSend

**容器属性**:

- **UUID**: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerIPduSend`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMTriggeredIPduRef

- **UUID**: `ECUC:bf813042-367e-403f-849e-eb3d8b1c950f`
- **引用名**: `BswMTriggeredIPduRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU that should be triggered for transmission.

######### 15. BswMTriggerSlaveRTEStop

**容器属性**:

- **UUID**: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerSlaveRTEStop`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. BswMCoreId

- **UUID**: `ECUC:8fd528a4-a7eb-8b28-53f8-45f371b4c7ea`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

######### 16. BswMTriggerStartUpPhase2

**容器属性**:

- **UUID**: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerStartUpPhase2`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. BswMCoreId

- **UUID**: `ECUC:d2865d98-439b-83c9-38dc-4f3a8ce7f3ae`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

######### 17. BswMUserCallout

**容器属性**:

- **UUID**: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMUserCallout`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all details needed for a user defined function call.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. BswMUserCalloutFunction

- **UUID**: `ECUC:40b9feb6-e998-4e06-a351-81f431b4850e`
- **参数名**: `BswMUserCalloutFunction`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the complete function call including all parameters. The parameters are specified during configuration time, and cannot be changed during run time. Any return values passed by the callout will be ignored.

######### 18. BswMAvailableActions

**容器属性**:

- **UUID**: `ECUC:cc9ad948-01ce-4ed4-a898-41fcd6ede588`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMAvailableActions`
- **多重性**: [1..1]

**容器选择**:

- **BswMComMAllowCom**
  - UUID: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
  - 描述: This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.
- **BswMComMModeLimitation**
  - UUID: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
  - 描述: This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.
- **BswMComMModeSwitch**
  - UUID: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
  - 描述: This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.
- **BswMDeadlineMonitoringControl**
  - UUID: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
  - 描述: This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.
- **BswMEcuMGoDown**
  - UUID: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
  - 描述: This container defines the UserId which shall be forwarded to the GoDown request.
- **BswMEcuMSelectShutdownTarget**
  - UUID: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
  - 描述: This container defines the shutdown target.
- **BswMLinScheduleSwitch**
  - UUID: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
  - 描述: This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.
- **BswMNMControl**
  - UUID: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
  - 描述: This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.
- **BswMPduGroupSwitch**
  - UUID: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
  - 描述: This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.
- **BswMPduRouterControl**
  - UUID: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
  - 描述: This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.
- **BswMRteSwitch**
  - UUID: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.
- **BswMSchMSwitch**
  - UUID: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.
- **BswMSwitchIPduMode**
  - UUID: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
  - 描述: This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.
- **BswMTriggerIPduSend**
  - UUID: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
  - 描述: This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.
- **BswMTriggerSlaveRTEStop**
  - UUID: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
  - 描述: This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.
- **BswMTriggerStartUpPhase2**
  - UUID: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
  - 描述: This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.
- **BswMUserCallout**
  - UUID: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
  - 描述: This container includes all details needed for a user defined function call.

**容器描述**:

Choice container including the available actions to be used in the action lists.

####### 2. BswMComMAllowCom

**容器属性**:

- **UUID**: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMAllowCom`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMComAllowed

- **UUID**: `ECUC:a75f55aa-9e34-48e5-9c33-8e121ac7f7d8`
- **参数名**: `BswMComAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter BswMComMAllowChannelRef refers to a channel which will allow or block communication using the function ComM_CommunicationAllowed().

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMAllowChannelRef

- **UUID**: `ECUC:cfa3f8ee-4192-4364-a046-f5ef39f8626f`
- **引用名**: `BswMComMAllowChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM Channel for which communication shall be allowed or blocked.

####### 3. BswMComMModeLimitation

**容器属性**:

- **UUID**: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeLimitation`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMComMLimitMode

- **UUID**: `ECUC:a90697cd-02ca-46c7-b4d9-3561ac126656`
- **参数名**: `BswMComMLimitMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function ComM_LimitChannelToNoComMode() takes in this boolean parameter to limit the channel's com mode to no-com mode.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMLimitChannelRef

- **UUID**: `ECUC:dfb83a13-105c-4ad9-b65d-8465bcad8ddd`
- **引用名**: `BswMComMLimitChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM channel for which the communication mode should be limited.

####### 4. BswMComMModeSwitch

**容器属性**:

- **UUID**: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMComMRequestedMode

- **UUID**: `ECUC:a8479736-a047-4a2e-a9de-9de9d1fe5e26`
- **参数名**: `BswMComMRequestedMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FULL_COM` (来源: AUTOSAR_ECUC)
  - `BSWM_NO_COM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the requested communication mode.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMUserRef

- **UUID**: `ECUC:38ab9166-a9b6-4666-8064-b0fe9192d7af`
- **引用名**: `BswMComMUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM User that is associated to the Communication channel for which the communication mode should be requested.

####### 5. BswMDeadlineMonitoringControl

**容器属性**:

- **UUID**: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDeadlineMonitoringControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMDisabledDMPduGroupRef

- **UUID**: `ECUC:858f665d-7fc6-49e4-a22a-b512c6e0b69b`
- **引用名**: `BswMDisabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be disabled.

########## 2. BswMEnabledDMPduGroupRef

- **UUID**: `ECUC:489675a3-4dfa-43b5-8f8e-48609a142a1d`
- **引用名**: `BswMEnabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be enabled.

####### 6. BswMEcuMGoDown

**容器属性**:

- **UUID**: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMGoDown`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the UserId which shall be forwarded to the GoDown request.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEcuMUserIdRef

- **UUID**: `ECUC:5bf3393d-903b-435c-822a-e8df76b79337`
- **引用名**: `BswMEcuMUserIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a EcuM UserId.

####### 7. BswMEcuMSelectShutdownTarget

**容器属性**:

- **UUID**: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMSelectShutdownTarget`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the shutdown target.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEcuMShutdownTargetRef

- **UUID**: `ECUC:46e261aa-240e-40c3-8b60-5242f58edfb2`
- **引用名**: `BswMEcuMShutdownTargetRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a shutdown target.

####### 8. BswMLinScheduleSwitch

**容器属性**:

- **UUID**: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinScheduleRef

- **UUID**: `ECUC:32b27d57-fa6d-4f23-a0c7-f872b0d789a0`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN schedule table that the LIN SM shall change to.

####### 9. BswMNMControl

**容器属性**:

- **UUID**: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNMControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMNMAction

- **UUID**: `ECUC:b0783d19-a6d0-4699-ac8c-a4049b4d461e`
- **参数名**: `BswMNMAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_NM_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_NM_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the communication of the corresponding NM channel should be enabled or disabled.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMNetworkHandleRef

- **UUID**: `ECUC:71f03668-a386-4d49-b226-dd2c739ebc06`
- **引用名**: `BswMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

####### 10. BswMPduGroupSwitch

**容器属性**:

- **UUID**: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduGroupSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMPduGroupSwitchReinit

- **UUID**: `ECUC:b6fb3fbb-cb5c-4d7a-9560-c5bc39a5da54`
- **参数名**: `BswMPduGroupSwitchReinit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the values for the parameters like periodical timer, minimum delay timer etc is retainer or reinitialized during a PDU Group Switch.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMDisabledPduGroupRef

- **UUID**: `ECUC:d63a77a6-da9d-467a-9c2f-6879f96a8b50`
- **引用名**: `BswMDisabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be disabled.

########## 2. BswMEnabledPduGroupRef

- **UUID**: `ECUC:754e70f9-ccd0-4a90-8e06-58d065bb4184`
- **引用名**: `BswMEnabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be enabled.

####### 11. BswMPduRouterControl

**容器属性**:

- **UUID**: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduRouterControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswPduRouterAction

- **UUID**: `ECUC:7a7d7b39-fdff-4f16-9aa1-9ea5d6b3f02f`
- **参数名**: `BswPduRouterAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_PDUR_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_PDUR_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the routing of the corresponding PDU should be enabled or disabled.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMPduRoutingPathGroupRef

- **UUID**: `ECUC:edbfb25c-322b-4d20-93f0-b1e32d0f50f5`
- **引用名**: `BswMPduRoutingPathGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `PduRRoutingPathGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRRoutingPathGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the PDU Routing Path Group for which the routing in the PDU Router should be enabled or disabled.

####### 12. BswMRteSwitch

**容器属性**:

- **UUID**: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRteSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. BswMRteSwitchPortRef

- **UUID**: `ECUC:4642d375-9c6d-4db5-84c5-fb8e6d59972c`
- **引用名**: `BswMRteSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwitchedMode

- **UUID**: `ECUC:3d6f5054-ebed-40f3-9abc-b366bc6a8017`
- **引用名**: `BswMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

####### 13. BswMSchMSwitch

**容器属性**:

- **UUID**: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSchMSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. BswMSchMSwitchPortRef

- **UUID**: `ECUC:e18f3107-9272-4ace-95ac-cfce6556be97`
- **引用名**: `BswMSchMSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSchMSwitchedMode

- **UUID**: `ECUC:8223503b-58a4-4608-9fe1-4317c3c27858`
- **引用名**: `BswMSchMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

####### 14. BswMSwitchIPduMode

**容器属性**:

- **UUID**: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchIPduMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMSwitchIPduModeValue

- **UUID**: `ECUC:75026229-698c-4fbc-a905-6652e28355d6`
- **参数名**: `BswMSwitchIPduModeValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines which transmission mode shall be selected during this call.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMSwitchIPduModeRef

- **UUID**: `ECUC:2629fedf-9668-4d93-af1e-99e2346f915f`
- **引用名**: `BswMSwitchIPduModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU for which the transmission mode shall be set.

####### 15. BswMTriggerIPduSend

**容器属性**:

- **UUID**: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerIPduSend`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMTriggeredIPduRef

- **UUID**: `ECUC:bf813042-367e-403f-849e-eb3d8b1c950f`
- **引用名**: `BswMTriggeredIPduRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU that should be triggered for transmission.

####### 16. BswMTriggerSlaveRTEStop

**容器属性**:

- **UUID**: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerSlaveRTEStop`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. BswMCoreId

- **UUID**: `ECUC:8fd528a4-a7eb-8b28-53f8-45f371b4c7ea`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

####### 17. BswMTriggerStartUpPhase2

**容器属性**:

- **UUID**: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerStartUpPhase2`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. BswMCoreId

- **UUID**: `ECUC:d2865d98-439b-83c9-38dc-4f3a8ce7f3ae`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

####### 18. BswMUserCallout

**容器属性**:

- **UUID**: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMUserCallout`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all details needed for a user defined function call.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMUserCalloutFunction

- **UUID**: `ECUC:40b9feb6-e998-4e06-a351-81f431b4850e`
- **参数名**: `BswMUserCalloutFunction`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the complete function call including all parameters. The parameters are specified during configuration time, and cannot be changed during run time. Any return values passed by the callout will be ignored.

####### 19. BswMActionList

**容器属性**:

- **UUID**: `ECUC:407b970e-46be-4d6b-b8ad-157663aa5d94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionList`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container defines an action list that is invoked based on the BswM Rules. An action list contains a list of numbered action items to be processed. An action list can also include other action lists.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMActionListExecution

- **UUID**: `ECUC:e6f03759-bac9-40cb-816c-4432a6d70644`
- **参数名**: `BswMActionListExecution`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_CONDITION` (来源: AUTOSAR_ECUC)
  - `BSWM_TRIGGER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter controls if the corresponding action list shall be executed every time the rule is evaluated or only when the result of the evaluation changes.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. BswMActionListItem

**容器属性**:

- **UUID**: `ECUC:57ce84a2-0f20-4dd5-85a3-4fd44d75b91a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionListItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines an item in an action list.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. BswMActionListItemIndex

- **UUID**: `ECUC:d2944d1c-b5c4-4d6b-bc4c-ae6c1a89e946`
- **参数名**: `BswMActionListItemIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the index of the action in the action list. It is used define in which order the actions shall be performed.

########### BOOLEAN 类型参数

############ 1. BswMAbortOnFail

- **UUID**: `ECUC:79c629de-d4aa-49d9-b686-9a6bd7347aec`
- **参数名**: `BswMAbortOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the execution of the action list shall be aborted if this specific action returns E_NOT_OK. Note that this is only applicable for actions that have E_NOT_OK as a possible return value.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. BswMReportFailToDemRef

- **UUID**: `ECUC:5b95c4bb-7e3b-4788-bb34-eaf73a792725`
- **引用名**: `BswMReportFailToDemRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the reference is given, the DEM event shall be reported failed if this specific action returns E_NOT_OK; it shall be reported passed if this specific action returns E_OK.

########### CHOICE-REFERENCE 类型引用

############ 1. BswMActionListItemRef

- **UUID**: `ECUC:756c431f-9e65-40e8-b3a3-47599991abcb`
- **引用名**: `BswMActionListItemRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMAction`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMRule`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action item can either be an atomic action or a reference to another action list or rule.

####### 20. BswMActionListItem

**容器属性**:

- **UUID**: `ECUC:57ce84a2-0f20-4dd5-85a3-4fd44d75b91a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionListItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines an item in an action list.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. BswMActionListItemIndex

- **UUID**: `ECUC:d2944d1c-b5c4-4d6b-bc4c-ae6c1a89e946`
- **参数名**: `BswMActionListItemIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the index of the action in the action list. It is used define in which order the actions shall be performed.

######### BOOLEAN 类型参数

########## 1. BswMAbortOnFail

- **UUID**: `ECUC:79c629de-d4aa-49d9-b686-9a6bd7347aec`
- **参数名**: `BswMAbortOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the execution of the action list shall be aborted if this specific action returns E_NOT_OK. Note that this is only applicable for actions that have E_NOT_OK as a possible return value.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMReportFailToDemRef

- **UUID**: `ECUC:5b95c4bb-7e3b-4788-bb34-eaf73a792725`
- **引用名**: `BswMReportFailToDemRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the reference is given, the DEM event shall be reported failed if this specific action returns E_NOT_OK; it shall be reported passed if this specific action returns E_OK.

######### CHOICE-REFERENCE 类型引用

########## 1. BswMActionListItemRef

- **UUID**: `ECUC:756c431f-9e65-40e8-b3a3-47599991abcb`
- **引用名**: `BswMActionListItemRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMAction`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMRule`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action item can either be an atomic action or a reference to another action list or rule.

####### 21. BswMSwitchPort

**容器属性**:

- **UUID**: `ECUC:f962bf44-5314-4e9c-894b-e8cf24f38351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchPort`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies PPorts and/or providedModeDeclarationGroups, which the BswM has to create in its SWCD resp. BSWMD.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMModeSwitchInterfaceRef

- **UUID**: `ECUC:868ddf33-9a9f-4e55-9dcb-598cd2bed53a`
- **引用名**: `BswMModeSwitchInterfaceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-SWITCH-INTERFACE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ModeSwitchInterface of this BswMModeSwitchPort.

####### 22. BswMAvailableActions

**容器属性**:

- **UUID**: `ECUC:cc9ad948-01ce-4ed4-a898-41fcd6ede588`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMAvailableActions`
- **多重性**: [1..1]

**容器选择**:

- **BswMComMAllowCom**
  - UUID: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
  - 描述: This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.
- **BswMComMModeLimitation**
  - UUID: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
  - 描述: This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.
- **BswMComMModeSwitch**
  - UUID: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
  - 描述: This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.
- **BswMDeadlineMonitoringControl**
  - UUID: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
  - 描述: This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.
- **BswMEcuMGoDown**
  - UUID: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
  - 描述: This container defines the UserId which shall be forwarded to the GoDown request.
- **BswMEcuMSelectShutdownTarget**
  - UUID: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
  - 描述: This container defines the shutdown target.
- **BswMLinScheduleSwitch**
  - UUID: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
  - 描述: This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.
- **BswMNMControl**
  - UUID: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
  - 描述: This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.
- **BswMPduGroupSwitch**
  - UUID: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
  - 描述: This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.
- **BswMPduRouterControl**
  - UUID: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
  - 描述: This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.
- **BswMRteSwitch**
  - UUID: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.
- **BswMSchMSwitch**
  - UUID: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.
- **BswMSwitchIPduMode**
  - UUID: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
  - 描述: This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.
- **BswMTriggerIPduSend**
  - UUID: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
  - 描述: This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.
- **BswMTriggerSlaveRTEStop**
  - UUID: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
  - 描述: This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.
- **BswMTriggerStartUpPhase2**
  - UUID: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
  - 描述: This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.
- **BswMUserCallout**
  - UUID: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
  - 描述: This container includes all details needed for a user defined function call.

**容器描述**:

Choice container including the available actions to be used in the action lists.

##### 32. BswMAction

**容器属性**:

- **UUID**: `ECUC:add00e45-e97c-4d9a-8208-befcbfbfd3e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMAction`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each container of this type defines an action. These actions can be part of one or several action lists.

###### 配置容器

本模块包含 **18** 个配置容器：

####### 1. BswMComMAllowCom

**容器属性**:

- **UUID**: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMAllowCom`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMComAllowed

- **UUID**: `ECUC:a75f55aa-9e34-48e5-9c33-8e121ac7f7d8`
- **参数名**: `BswMComAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter BswMComMAllowChannelRef refers to a channel which will allow or block communication using the function ComM_CommunicationAllowed().

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMAllowChannelRef

- **UUID**: `ECUC:cfa3f8ee-4192-4364-a046-f5ef39f8626f`
- **引用名**: `BswMComMAllowChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM Channel for which communication shall be allowed or blocked.

####### 2. BswMComMModeLimitation

**容器属性**:

- **UUID**: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeLimitation`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMComMLimitMode

- **UUID**: `ECUC:a90697cd-02ca-46c7-b4d9-3561ac126656`
- **参数名**: `BswMComMLimitMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function ComM_LimitChannelToNoComMode() takes in this boolean parameter to limit the channel's com mode to no-com mode.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMLimitChannelRef

- **UUID**: `ECUC:dfb83a13-105c-4ad9-b65d-8465bcad8ddd`
- **引用名**: `BswMComMLimitChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM channel for which the communication mode should be limited.

####### 3. BswMComMModeSwitch

**容器属性**:

- **UUID**: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMComMRequestedMode

- **UUID**: `ECUC:a8479736-a047-4a2e-a9de-9de9d1fe5e26`
- **参数名**: `BswMComMRequestedMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FULL_COM` (来源: AUTOSAR_ECUC)
  - `BSWM_NO_COM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the requested communication mode.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMUserRef

- **UUID**: `ECUC:38ab9166-a9b6-4666-8064-b0fe9192d7af`
- **引用名**: `BswMComMUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM User that is associated to the Communication channel for which the communication mode should be requested.

####### 4. BswMDeadlineMonitoringControl

**容器属性**:

- **UUID**: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDeadlineMonitoringControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMDisabledDMPduGroupRef

- **UUID**: `ECUC:858f665d-7fc6-49e4-a22a-b512c6e0b69b`
- **引用名**: `BswMDisabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be disabled.

########## 2. BswMEnabledDMPduGroupRef

- **UUID**: `ECUC:489675a3-4dfa-43b5-8f8e-48609a142a1d`
- **引用名**: `BswMEnabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be enabled.

####### 5. BswMEcuMGoDown

**容器属性**:

- **UUID**: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMGoDown`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the UserId which shall be forwarded to the GoDown request.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEcuMUserIdRef

- **UUID**: `ECUC:5bf3393d-903b-435c-822a-e8df76b79337`
- **引用名**: `BswMEcuMUserIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a EcuM UserId.

####### 6. BswMEcuMSelectShutdownTarget

**容器属性**:

- **UUID**: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMSelectShutdownTarget`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the shutdown target.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMEcuMShutdownTargetRef

- **UUID**: `ECUC:46e261aa-240e-40c3-8b60-5242f58edfb2`
- **引用名**: `BswMEcuMShutdownTargetRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a shutdown target.

####### 7. BswMLinScheduleSwitch

**容器属性**:

- **UUID**: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMLinScheduleRef

- **UUID**: `ECUC:32b27d57-fa6d-4f23-a0c7-f872b0d789a0`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN schedule table that the LIN SM shall change to.

####### 8. BswMNMControl

**容器属性**:

- **UUID**: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNMControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswMNMAction

- **UUID**: `ECUC:b0783d19-a6d0-4699-ac8c-a4049b4d461e`
- **参数名**: `BswMNMAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_NM_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_NM_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the communication of the corresponding NM channel should be enabled or disabled.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMComMNetworkHandleRef

- **UUID**: `ECUC:71f03668-a386-4d49-b226-dd2c739ebc06`
- **引用名**: `BswMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

####### 9. BswMPduGroupSwitch

**容器属性**:

- **UUID**: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduGroupSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMPduGroupSwitchReinit

- **UUID**: `ECUC:b6fb3fbb-cb5c-4d7a-9560-c5bc39a5da54`
- **参数名**: `BswMPduGroupSwitchReinit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the values for the parameters like periodical timer, minimum delay timer etc is retainer or reinitialized during a PDU Group Switch.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMDisabledPduGroupRef

- **UUID**: `ECUC:d63a77a6-da9d-467a-9c2f-6879f96a8b50`
- **引用名**: `BswMDisabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be disabled.

########## 2. BswMEnabledPduGroupRef

- **UUID**: `ECUC:754e70f9-ccd0-4a90-8e06-58d065bb4184`
- **引用名**: `BswMEnabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be enabled.

####### 10. BswMPduRouterControl

**容器属性**:

- **UUID**: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduRouterControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. BswPduRouterAction

- **UUID**: `ECUC:7a7d7b39-fdff-4f16-9aa1-9ea5d6b3f02f`
- **参数名**: `BswPduRouterAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_PDUR_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_PDUR_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the routing of the corresponding PDU should be enabled or disabled.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMPduRoutingPathGroupRef

- **UUID**: `ECUC:edbfb25c-322b-4d20-93f0-b1e32d0f50f5`
- **引用名**: `BswMPduRoutingPathGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `PduRRoutingPathGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRRoutingPathGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the PDU Routing Path Group for which the routing in the PDU Router should be enabled or disabled.

####### 11. BswMRteSwitch

**容器属性**:

- **UUID**: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRteSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. BswMRteSwitchPortRef

- **UUID**: `ECUC:4642d375-9c6d-4db5-84c5-fb8e6d59972c`
- **引用名**: `BswMRteSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSwitchedMode

- **UUID**: `ECUC:3d6f5054-ebed-40f3-9abc-b366bc6a8017`
- **引用名**: `BswMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

####### 12. BswMSchMSwitch

**容器属性**:

- **UUID**: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSchMSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. BswMSchMSwitchPortRef

- **UUID**: `ECUC:e18f3107-9272-4ace-95ac-cfce6556be97`
- **引用名**: `BswMSchMSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

######### FOREIGN-REFERENCE 类型引用

########## 1. BswMSchMSwitchedMode

- **UUID**: `ECUC:8223503b-58a4-4608-9fe1-4317c3c27858`
- **引用名**: `BswMSchMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

####### 13. BswMSwitchIPduMode

**容器属性**:

- **UUID**: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchIPduMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. BswMSwitchIPduModeValue

- **UUID**: `ECUC:75026229-698c-4fbc-a905-6652e28355d6`
- **参数名**: `BswMSwitchIPduModeValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines which transmission mode shall be selected during this call.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMSwitchIPduModeRef

- **UUID**: `ECUC:2629fedf-9668-4d93-af1e-99e2346f915f`
- **引用名**: `BswMSwitchIPduModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU for which the transmission mode shall be set.

####### 14. BswMTriggerIPduSend

**容器属性**:

- **UUID**: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerIPduSend`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMTriggeredIPduRef

- **UUID**: `ECUC:bf813042-367e-403f-849e-eb3d8b1c950f`
- **引用名**: `BswMTriggeredIPduRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU that should be triggered for transmission.

####### 15. BswMTriggerSlaveRTEStop

**容器属性**:

- **UUID**: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerSlaveRTEStop`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. BswMCoreId

- **UUID**: `ECUC:8fd528a4-a7eb-8b28-53f8-45f371b4c7ea`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

####### 16. BswMTriggerStartUpPhase2

**容器属性**:

- **UUID**: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerStartUpPhase2`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. BswMCoreId

- **UUID**: `ECUC:d2865d98-439b-83c9-38dc-4f3a8ce7f3ae`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

####### 17. BswMUserCallout

**容器属性**:

- **UUID**: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMUserCallout`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all details needed for a user defined function call.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMUserCalloutFunction

- **UUID**: `ECUC:40b9feb6-e998-4e06-a351-81f431b4850e`
- **参数名**: `BswMUserCalloutFunction`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the complete function call including all parameters. The parameters are specified during configuration time, and cannot be changed during run time. Any return values passed by the callout will be ignored.

####### 18. BswMAvailableActions

**容器属性**:

- **UUID**: `ECUC:cc9ad948-01ce-4ed4-a898-41fcd6ede588`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMAvailableActions`
- **多重性**: [1..1]

**容器选择**:

- **BswMComMAllowCom**
  - UUID: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
  - 描述: This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.
- **BswMComMModeLimitation**
  - UUID: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
  - 描述: This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.
- **BswMComMModeSwitch**
  - UUID: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
  - 描述: This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.
- **BswMDeadlineMonitoringControl**
  - UUID: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
  - 描述: This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.
- **BswMEcuMGoDown**
  - UUID: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
  - 描述: This container defines the UserId which shall be forwarded to the GoDown request.
- **BswMEcuMSelectShutdownTarget**
  - UUID: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
  - 描述: This container defines the shutdown target.
- **BswMLinScheduleSwitch**
  - UUID: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
  - 描述: This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.
- **BswMNMControl**
  - UUID: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
  - 描述: This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.
- **BswMPduGroupSwitch**
  - UUID: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
  - 描述: This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.
- **BswMPduRouterControl**
  - UUID: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
  - 描述: This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.
- **BswMRteSwitch**
  - UUID: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.
- **BswMSchMSwitch**
  - UUID: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.
- **BswMSwitchIPduMode**
  - UUID: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
  - 描述: This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.
- **BswMTriggerIPduSend**
  - UUID: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
  - 描述: This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.
- **BswMTriggerSlaveRTEStop**
  - UUID: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
  - 描述: This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.
- **BswMTriggerStartUpPhase2**
  - UUID: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
  - 描述: This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.
- **BswMUserCallout**
  - UUID: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
  - 描述: This container includes all details needed for a user defined function call.

**容器描述**:

Choice container including the available actions to be used in the action lists.

##### 33. BswMComMAllowCom

**容器属性**:

- **UUID**: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMAllowCom`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. BswMComAllowed

- **UUID**: `ECUC:a75f55aa-9e34-48e5-9c33-8e121ac7f7d8`
- **参数名**: `BswMComAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter BswMComMAllowChannelRef refers to a channel which will allow or block communication using the function ComM_CommunicationAllowed().

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMComMAllowChannelRef

- **UUID**: `ECUC:cfa3f8ee-4192-4364-a046-f5ef39f8626f`
- **引用名**: `BswMComMAllowChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM Channel for which communication shall be allowed or blocked.

##### 34. BswMComMModeLimitation

**容器属性**:

- **UUID**: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeLimitation`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. BswMComMLimitMode

- **UUID**: `ECUC:a90697cd-02ca-46c7-b4d9-3561ac126656`
- **参数名**: `BswMComMLimitMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The function ComM_LimitChannelToNoComMode() takes in this boolean parameter to limit the channel's com mode to no-com mode.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMComMLimitChannelRef

- **UUID**: `ECUC:dfb83a13-105c-4ad9-b65d-8465bcad8ddd`
- **引用名**: `BswMComMLimitChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM channel for which the communication mode should be limited.

##### 35. BswMComMModeSwitch

**容器属性**:

- **UUID**: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMComMModeSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. BswMComMRequestedMode

- **UUID**: `ECUC:a8479736-a047-4a2e-a9de-9de9d1fe5e26`
- **参数名**: `BswMComMRequestedMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_FULL_COM` (来源: AUTOSAR_ECUC)
  - `BSWM_NO_COM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the requested communication mode.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMComMUserRef

- **UUID**: `ECUC:38ab9166-a9b6-4666-8064-b0fe9192d7af`
- **引用名**: `BswMComMUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the ComM User that is associated to the Communication channel for which the communication mode should be requested.

##### 36. BswMDeadlineMonitoringControl

**容器属性**:

- **UUID**: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMDeadlineMonitoringControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMDisabledDMPduGroupRef

- **UUID**: `ECUC:858f665d-7fc6-49e4-a22a-b512c6e0b69b`
- **引用名**: `BswMDisabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be disabled.

######## 2. BswMEnabledDMPduGroupRef

- **UUID**: `ECUC:489675a3-4dfa-43b5-8f8e-48609a142a1d`
- **引用名**: `BswMEnabledDMPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group for which the Deadline Monitoring should be enabled.

##### 37. BswMEcuMGoDown

**容器属性**:

- **UUID**: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMGoDown`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the UserId which shall be forwarded to the GoDown request.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMEcuMUserIdRef

- **UUID**: `ECUC:5bf3393d-903b-435c-822a-e8df76b79337`
- **引用名**: `BswMEcuMUserIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a EcuM UserId.

##### 38. BswMEcuMSelectShutdownTarget

**容器属性**:

- **UUID**: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMEcuMSelectShutdownTarget`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the shutdown target.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMEcuMShutdownTargetRef

- **UUID**: `ECUC:46e261aa-240e-40c3-8b60-5242f58edfb2`
- **引用名**: `BswMEcuMShutdownTargetRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a shutdown target.

##### 39. BswMLinScheduleSwitch

**容器属性**:

- **UUID**: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMLinScheduleSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMLinScheduleRef

- **UUID**: `ECUC:32b27d57-fa6d-4f23-a0c7-f872b0d789a0`
- **引用名**: `BswMLinScheduleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinSMSchedule`
- **完整路径**: `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet/LinSMChannel/LinSMSchedule`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the LIN schedule table that the LIN SM shall change to.

##### 40. BswMNMControl

**容器属性**:

- **UUID**: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMNMControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. BswMNMAction

- **UUID**: `ECUC:b0783d19-a6d0-4699-ac8c-a4049b4d461e`
- **参数名**: `BswMNMAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_NM_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_NM_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the communication of the corresponding NM channel should be enabled or disabled.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMComMNetworkHandleRef

- **UUID**: `ECUC:71f03668-a386-4d49-b226-dd2c739ebc06`
- **引用名**: `BswMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

##### 41. BswMPduGroupSwitch

**容器属性**:

- **UUID**: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduGroupSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. BswMPduGroupSwitchReinit

- **UUID**: `ECUC:b6fb3fbb-cb5c-4d7a-9560-c5bc39a5da54`
- **参数名**: `BswMPduGroupSwitchReinit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the values for the parameters like periodical timer, minimum delay timer etc is retainer or reinitialized during a PDU Group Switch.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMDisabledPduGroupRef

- **UUID**: `ECUC:d63a77a6-da9d-467a-9c2f-6879f96a8b50`
- **引用名**: `BswMDisabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be disabled.

######## 2. BswMEnabledPduGroupRef

- **UUID**: `ECUC:754e70f9-ccd0-4a90-8e06-58d065bb4184`
- **引用名**: `BswMEnabledPduGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to a PDU Group that should be enabled.

##### 42. BswMPduRouterControl

**容器属性**:

- **UUID**: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMPduRouterControl`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. BswPduRouterAction

- **UUID**: `ECUC:7a7d7b39-fdff-4f16-9aa1-9ea5d6b3f02f`
- **参数名**: `BswPduRouterAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_PDUR_DISABLE` (来源: AUTOSAR_ECUC)
  - `BSWM_PDUR_ENABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if the routing of the corresponding PDU should be enabled or disabled.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMPduRoutingPathGroupRef

- **UUID**: `ECUC:edbfb25c-322b-4d20-93f0-b1e32d0f50f5`
- **引用名**: `BswMPduRoutingPathGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `PduRRoutingPathGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRRoutingPathGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the PDU Routing Path Group for which the routing in the PDU Router should be enabled or disabled.

##### 43. BswMRteSwitch

**容器属性**:

- **UUID**: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMRteSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. BswMRteSwitchPortRef

- **UUID**: `ECUC:4642d375-9c6d-4db5-84c5-fb8e6d59972c`
- **引用名**: `BswMRteSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

####### FOREIGN-REFERENCE 类型引用

######## 1. BswMSwitchedMode

- **UUID**: `ECUC:3d6f5054-ebed-40f3-9abc-b366bc6a8017`
- **引用名**: `BswMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

##### 44. BswMSchMSwitch

**容器属性**:

- **UUID**: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSchMSwitch`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. BswMSchMSwitchPortRef

- **UUID**: `ECUC:e18f3107-9272-4ace-95ac-cfce6556be97`
- **引用名**: `BswMSchMSwitchPortRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `BswMSwitchPort`
- **完整路径**: `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMSwitchPort`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to the BswMSwitchPort.

####### FOREIGN-REFERENCE 类型引用

######## 1. BswMSchMSwitchedMode

- **UUID**: `ECUC:8223503b-58a4-4608-9fe1-4317c3c27858`
- **引用名**: `BswMSchMSwitchedMode`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-DECLARATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the integer value that corresponds to a certain mode in a Mode Declaration Group.

##### 45. BswMSwitchIPduMode

**容器属性**:

- **UUID**: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchIPduMode`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. BswMSwitchIPduModeValue

- **UUID**: `ECUC:75026229-698c-4fbc-a905-6652e28355d6`
- **参数名**: `BswMSwitchIPduModeValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines which transmission mode shall be selected during this call.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMSwitchIPduModeRef

- **UUID**: `ECUC:2629fedf-9668-4d93-af1e-99e2346f915f`
- **引用名**: `BswMSwitchIPduModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU for which the transmission mode shall be set.

##### 46. BswMTriggerIPduSend

**容器属性**:

- **UUID**: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerIPduSend`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMTriggeredIPduRef

- **UUID**: `ECUC:bf813042-367e-403f-849e-eb3d8b1c950f`
- **引用名**: `BswMTriggeredIPduRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to an I-PDU that should be triggered for transmission.

##### 47. BswMTriggerSlaveRTEStop

**容器属性**:

- **UUID**: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerSlaveRTEStop`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. BswMCoreId

- **UUID**: `ECUC:8fd528a4-a7eb-8b28-53f8-45f371b4c7ea`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

##### 48. BswMTriggerStartUpPhase2

**容器属性**:

- **UUID**: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMTriggerStartUpPhase2`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. BswMCoreId

- **UUID**: `ECUC:d2865d98-439b-83c9-38dc-4f3a8ce7f3ae`
- **参数名**: `BswMCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the identifier of the slave core that is used as input parameter for the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this parameter shall be synchronized with the OsApplicationCoreAssignment parameter.

##### 49. BswMUserCallout

**容器属性**:

- **UUID**: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMUserCallout`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container includes all details needed for a user defined function call.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. BswMUserCalloutFunction

- **UUID**: `ECUC:40b9feb6-e998-4e06-a351-81f431b4850e`
- **参数名**: `BswMUserCalloutFunction`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the complete function call including all parameters. The parameters are specified during configuration time, and cannot be changed during run time. Any return values passed by the callout will be ignored.

##### 50. BswMActionList

**容器属性**:

- **UUID**: `ECUC:407b970e-46be-4d6b-b8ad-157663aa5d94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionList`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each instance of this container defines an action list that is invoked based on the BswM Rules. An action list contains a list of numbered action items to be processed. An action list can also include other action lists.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. BswMActionListExecution

- **UUID**: `ECUC:e6f03759-bac9-40cb-816c-4432a6d70644`
- **参数名**: `BswMActionListExecution`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BSWM_CONDITION` (来源: AUTOSAR_ECUC)
  - `BSWM_TRIGGER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter controls if the corresponding action list shall be executed every time the rule is evaluated or only when the result of the evaluation changes.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. BswMActionListItem

**容器属性**:

- **UUID**: `ECUC:57ce84a2-0f20-4dd5-85a3-4fd44d75b91a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionListItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines an item in an action list.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. BswMActionListItemIndex

- **UUID**: `ECUC:d2944d1c-b5c4-4d6b-bc4c-ae6c1a89e946`
- **参数名**: `BswMActionListItemIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the index of the action in the action list. It is used define in which order the actions shall be performed.

######### BOOLEAN 类型参数

########## 1. BswMAbortOnFail

- **UUID**: `ECUC:79c629de-d4aa-49d9-b686-9a6bd7347aec`
- **参数名**: `BswMAbortOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the execution of the action list shall be aborted if this specific action returns E_NOT_OK. Note that this is only applicable for actions that have E_NOT_OK as a possible return value.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. BswMReportFailToDemRef

- **UUID**: `ECUC:5b95c4bb-7e3b-4788-bb34-eaf73a792725`
- **引用名**: `BswMReportFailToDemRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the reference is given, the DEM event shall be reported failed if this specific action returns E_NOT_OK; it shall be reported passed if this specific action returns E_OK.

######### CHOICE-REFERENCE 类型引用

########## 1. BswMActionListItemRef

- **UUID**: `ECUC:756c431f-9e65-40e8-b3a3-47599991abcb`
- **引用名**: `BswMActionListItemRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMAction`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMRule`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action item can either be an atomic action or a reference to another action list or rule.

##### 51. BswMActionListItem

**容器属性**:

- **UUID**: `ECUC:57ce84a2-0f20-4dd5-85a3-4fd44d75b91a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMActionListItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines an item in an action list.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. BswMActionListItemIndex

- **UUID**: `ECUC:d2944d1c-b5c4-4d6b-bc4c-ae6c1a89e946`
- **参数名**: `BswMActionListItemIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the index of the action in the action list. It is used define in which order the actions shall be performed.

####### BOOLEAN 类型参数

######## 1. BswMAbortOnFail

- **UUID**: `ECUC:79c629de-d4aa-49d9-b686-9a6bd7347aec`
- **参数名**: `BswMAbortOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the execution of the action list shall be aborted if this specific action returns E_NOT_OK. Note that this is only applicable for actions that have E_NOT_OK as a possible return value.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. BswMReportFailToDemRef

- **UUID**: `ECUC:5b95c4bb-7e3b-4788-bb34-eaf73a792725`
- **引用名**: `BswMReportFailToDemRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the reference is given, the DEM event shall be reported failed if this specific action returns E_NOT_OK; it shall be reported passed if this specific action returns E_OK.

####### CHOICE-REFERENCE 类型引用

######## 1. BswMActionListItemRef

- **UUID**: `ECUC:756c431f-9e65-40e8-b3a3-47599991abcb`
- **引用名**: `BswMActionListItemRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMAction`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMModeControl/BswMActionList`
  - `/AUTOSAR/EcucDefs/BswM/BswMConfig/BswMArbitration/BswMRule`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action item can either be an atomic action or a reference to another action list or rule.

##### 52. BswMSwitchPort

**容器属性**:

- **UUID**: `ECUC:f962bf44-5314-4e9c-894b-e8cf24f38351`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMSwitchPort`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies PPorts and/or providedModeDeclarationGroups, which the BswM has to create in its SWCD resp. BSWMD.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. BswMModeSwitchInterfaceRef

- **UUID**: `ECUC:868ddf33-9a9f-4e55-9dcb-598cd2bed53a`
- **引用名**: `BswMModeSwitchInterfaceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: MODE-SWITCH-INTERFACE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ModeSwitchInterface of this BswMModeSwitchPort.

##### 53. BswMGeneral

**容器属性**:

- **UUID**: `ECUC:fa61d6da-9eb0-40f5-91ad-14a6c6302f8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

General configuration parameters of the Basic SW Mode Manager.

###### 参数配置

此容器包含 **15** 个参数：

####### BOOLEAN 类型参数

######## 1. BswMCanSMEnabled

- **UUID**: `ECUC:20b09b71-af6c-4742-bc19-d7be46ef2c56`
- **参数名**: `BswMCanSMEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable CanSM module related BswM API:

######## 2. BswMComMEnabled

- **UUID**: `ECUC:5cf2bda7-4d17-4ce1-82ce-f766c3b72a24`
- **参数名**: `BswMComMEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable ComM module related BswM API:

######## 3. BswMDcmEnabled

- **UUID**: `ECUC:541b52fa-ca18-4b78-80ce-d3465511157e`
- **参数名**: `BswMDcmEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable Dcm module related BswM API:

######## 4. BswMDevErrorDetect

- **UUID**: `ECUC:d8e85281-44c8-4346-9f78-2dc8123999ce`
- **参数名**: `BswMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 5. BswMEcuMEnabled

- **UUID**: `ECUC:4b8a67a5-6cb4-410f-a920-88f95b9b6135`
- **参数名**: `BswMEcuMEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable EcuM module related BswM API:

######## 6. BswMEthSMEnabled

- **UUID**: `ECUC:9c14cece-710b-491c-881c-3f26036d5934`
- **参数名**: `BswMEthSMEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable EthSM module related BswM API:

######## 7. BswMFrSMEnabled

- **UUID**: `ECUC:470ff123-9312-48f9-9437-fa492139535d`
- **参数名**: `BswMFrSMEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable FrSM module related BswM API:

######## 8. BswMGenericRequestEnabled

- **UUID**: `ECUC:9a887940-d041-456c-8f7b-1275123155f8`
- **参数名**: `BswMGenericRequestEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable Generic Request related BswM API:

######## 9. BswMLinSMEnabled

- **UUID**: `ECUC:bfacb96c-1654-4a15-8bf0-ab9450e57349`
- **参数名**: `BswMLinSMEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable LinSM module related BswM API:

######## 10. BswMLinTPEnabled

- **UUID**: `ECUC:2e5c6fe7-5142-49a1-aab3-f8f6d46572bb`
- **参数名**: `BswMLinTPEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable LinTP module related BswM API:

######## 11. BswMNvMEnabled

- **UUID**: `ECUC:036412df-b35c-43c0-b986-10d000024996`
- **参数名**: `BswMNvMEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable NvM module related BswM API:

######## 12. BswMSchMEnabled

- **UUID**: `ECUC:cc68af98-14aa-460e-a4cd-b26655bf0148`
- **参数名**: `BswMSchMEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable SchM module related BswM API:

######## 13. BswMVersionInfoApi

- **UUID**: `ECUC:dd2c4266-ade2-43ac-a7a3-adba2f1ca684`
- **参数名**: `BswMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the possibility to read the version information with the service BswM_GetVersionInfo().

######## 14. BswMWdgMEnabled

- **UUID**: `ECUC:393d1df2-c7d9-4d1b-9b1f-37b58840b592`
- **参数名**: `BswMWdgMEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: enable/disable WdgM module related BswM API:

####### FLOAT 类型参数

######## 1. BswMMainFunctionPeriod

- **UUID**: `ECUC:abcfbdc1-fe8b-436d-91b9-4ddc763395c4`
- **参数名**: `BswMMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The cycle time of the periodic main function of BswM. Defined in seconds .

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. BswMUserIncludeFiles

**容器属性**:

- **UUID**: `ECUC:b1c3db6a-2121-452d-aaa1-51f63963bb03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMUserIncludeFiles`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Collection of header file names which shall be included by the BswM.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. BswMUserIncludeFile

- **UUID**: `ECUC:2bfbd962-d945-4d4a-84c5-3fe3a3e06004`
- **参数名**: `BswMUserIncludeFile`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Header file name which shall be included by the BswM.

##### 54. BswMUserIncludeFiles

**容器属性**:

- **UUID**: `ECUC:b1c3db6a-2121-452d-aaa1-51f63963bb03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `BswMUserIncludeFiles`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Collection of header file names which shall be included by the BswM.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. BswMUserIncludeFile

- **UUID**: `ECUC:2bfbd962-d945-4d4a-84c5-3fe3a3e06004`
- **参数名**: `BswMUserIncludeFile`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Header file name which shall be included by the BswM.

##### 55. BswMConditionValue

**容器属性**:

- **UUID**: `ECUC:6dfef60d-1d6f-4b42-a4ae-f32d9a3df94f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMConditionValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswMode**
  - UUID: `ECUC:a9aa03c3-81c2-4949-b63a-a84a134a3291`
  - 描述: This container defines the value and type of a mode in the BSW.
- **BswMModeDeclaration**
  - UUID: `ECUC:2ed5817c-df9e-47bd-a384-c5c818caf935`
  - 描述: When the mode corresponds to a mode request or mode indication interface the mode is defined by a mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign reference to the corresponding Mode Declaration is used.

**容器描述**:

This container holds the parameters and references necessary to identify the mode type and the value that the mode request is compared to.

##### 56. BswMModeInitValue

**容器属性**:

- **UUID**: `ECUC:a780195c-9698-494b-810e-d6f1b56cef30`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeInitValue`
- **多重性**: [0..1]

**容器选择**:

- **BswMBswModeInitValue**
  - UUID: `ECUC:6b72e37c-506c-4dee-91b5-84f3dfabcf3b`
  - 描述: This is the choice for a initial mode value used for the initialization of mode requests in case the request is made by a BSW module.
- **BswMSwcModeInitValue**
  - UUID: `ECUC:9100ba60-b7ab-4c63-9121-f9c057463ebf`
  - 描述: This is the choice for a foreign reference to the Mode Declaration used for the initialization of mode requests in case the request is made by a SW-C.

**容器描述**:

This container defines the initial mode value that is used by BswM for the corresponding mode request after initialization. This container is optional and shall only be used for Mode Requests that do not already have an initial value.

##### 57. BswMModeRequestSource

**容器属性**:

- **UUID**: `ECUC:dd5d5587-bfd1-4960-a654-bcbc222aca93`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMModeRequestSource`
- **多重性**: [1..1]

**容器选择**:

- **BswMBswModeNotification**
  - UUID: `ECUC:a9fda01e-f3ad-46c3-affd-8a4e594a80e0`
  - 描述: The source of the mode request is a Bsw Module.
- **BswMCanSMIndication**
  - UUID: `ECUC:60c83276-d2ab-4077-9e33-d59f361ac518`
  - 描述: This is an indication of the current state of the CAN State Manager.
- **BswMComMIndication**
  - UUID: `ECUC:873fd64c-17e3-44f6-84a5-b045a48b8dc0`
  - 描述: This is an indication of the current communication mode of a channel in the Communication Manager.
- **BswMComMPncRequest**
  - UUID: `ECUC:48cb0816-8ced-4ad5-a493-2a63540eae85`
  - 描述: This is a request of the current communication mode of a Partial Network Cluster in the Communication Manager.
- **BswMDcmApplicationUpdatedIndication**
  - UUID: `ECUC:ccb455cd-746c-48e3-a406-201cc4294c40`
  - 描述: This is a request to update application data from the DCM. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMDcmComModeRequest**
  - UUID: `ECUC:f00a68aa-b64e-4d58-b694-f815644860a2`
  - 描述: The source of the mode request is the Diagnostic Communication Manager.
- **BswMEcuMIndication**
  - UUID: `ECUC:90275834-804e-460b-9d2b-0a066e5130ef`
  - 描述: This is a notification of the current operation mode of the ECU State Manager. This container does not contain any parameters since there are no further configuration needed for this type of request.
- **BswMEcuMWakeupSource**
  - UUID: `ECUC:fedcd4b6-8179-4135-b1eb-0d4ed3702d3a`
  - 描述: This is a notification of the current state of an ECU State Manager wakeup source.
- **BswMEthSMIndication**
  - UUID: `ECUC:c7a1a655-ad99-4506-8f61-328c655fc837`
  - 描述: This is an indication of the current state of the Ethernet State Manager.
- **BswMFrSMIndication**
  - UUID: `ECUC:bacadd7e-ce13-40d0-bd5e-2a656b772fbd`
  - 描述: This is an indication of the current state of the FlexRay State Manager.
- **BswMGenericRequest**
  - UUID: `ECUC:92e6a2bd-21cc-446c-abf1-172371d7a891`
  - 描述: This mode request originates from a requester that is not among the list of standardized mode requesters (i.e. the different resource managers).
- **BswMLinSMIndication**
  - UUID: `ECUC:17fe2db3-4d90-462a-9e6b-d1ba8d923419`
  - 描述: This is an indication of the current state of the LIN State Manager.
- **BswMLinScheduleIndication**
  - UUID: `ECUC:b605a404-6163-4591-8c3c-0832afb197ce`
  - 描述: This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.
- **BswMLinTpModeRequest**
  - UUID: `ECUC:34b88433-6423-4a7c-9d50-73e217a7730a`
  - 描述: This is a LinTp mode request from the LinIf. This port corresponds to a call of the BswM_LinTp_RequestMode API.
- **BswMNvMJobModeIndication**
  - UUID: `ECUC:2452616b-0819-4fa3-9a20-28c9fd64b6fe`
  - 描述: Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g. 0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:
- **BswMNvMRequest**
  - UUID: `ECUC:7e2e5f6f-6b37-4408-8b4b-fb66169315d4`
  - 描述: Via this Mode Request Source the NvM indicates the current status of the specified block. Possible Values are:
- **BswMSwcModeNotification**
  - UUID: `ECUC:2f25796e-4212-4187-a4fd-5cae123930de`
  - 描述: This is a mode switch notification associated with a RTE switch interface.
- **BswMSwcModeRequest**
  - UUID: `ECUC:cec88478-df6b-44b1-9036-edb5f3e101eb`
  - 描述: The source of the mode request is a SW Component.
- **BswMWdgMRequestPartitionReset**
  - UUID: `ECUC:77b44dcd-e54f-4030-bdbc-ecdd6e569ce4`
  - 描述: This is a Partition Reset request from from the WdgM. This port

**容器描述**:

This choice container specifies the source of the mode request or state/mode indication. The requester of a mode can be both SW-C:s and other BSW Modules, such as the bus specific State Managers.

##### 58. BswMAvailableActions

**容器属性**:

- **UUID**: `ECUC:cc9ad948-01ce-4ed4-a898-41fcd6ede588`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `BswMAvailableActions`
- **多重性**: [1..1]

**容器选择**:

- **BswMComMAllowCom**
  - UUID: `ECUC:0ce4c9d3-b52a-4bf4-8268-aebdfac80f52`
  - 描述: This container includes all parameters for the action to allow or to block communication for a ComM Channel. ComM_CommunicationAllowed  is called when this action is configured.
- **BswMComMModeLimitation**
  - UUID: `ECUC:93ede02b-24af-4c08-a0ef-1e3a636fbbcc`
  - 描述: This container includes all parameters related to a limitation of communication mode for a ComM Channel. ComM_LimitChannelToNoComMode is called when this action is configured.
- **BswMComMModeSwitch**
  - UUID: `ECUC:5c07eb69-9db2-4f5c-8e08-36329bcf4dc9`
  - 描述: This container includes all parameters related to a switch of communication mode for a ComM User. ComM_RequestComMode is called when this action is configured.
- **BswMDeadlineMonitoringControl**
  - UUID: `ECUC:22778ab5-dd84-4876-b8f8-3baced96702a`
  - 描述: This container includes all parameters related to enabling and disabling of deadline monitoring for one or several PDUs in COM.
- **BswMEcuMGoDown**
  - UUID: `ECUC:88eb34f2-e877-4fd8-8ecb-b5f8ee97123d`
  - 描述: This container defines the UserId which shall be forwarded to the GoDown request.
- **BswMEcuMSelectShutdownTarget**
  - UUID: `ECUC:20f34f5e-3ff3-4e97-8120-ed86c17c2351`
  - 描述: This container defines the shutdown target.
- **BswMLinScheduleSwitch**
  - UUID: `ECUC:23b5f4bd-fb88-4b60-b666-96efbced6dcc`
  - 描述: This container includes all parameters related to a switch of LIN schedule table. LinSM_ScheduleRequest is called when this action is configured.
- **BswMNMControl**
  - UUID: `ECUC:d44540a9-aa53-4e68-a8b5-ea3a59dcff78`
  - 描述: This container includes all parameters related to enabling and disabling of Network Management communication. Disabling of NM communication can be requested by DCM.
- **BswMPduGroupSwitch**
  - UUID: `ECUC:b7e1d5b8-cc18-4508-bbbf-9257454d5c80`
  - 描述: This container includes references to the PDU groups that shall be enabled and disabled. Com_IpduGroupControl is called when this action is configured.
- **BswMPduRouterControl**
  - UUID: `ECUC:40e0c9d2-b19e-4c8a-b501-1aac72a34ff5`
  - 描述: This container includes all parameters related to enabling and disabling of routing of Routing Path Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is configured.
- **BswMRteSwitch**
  - UUID: `ECUC:3d4d94e4-a15a-4442-88ce-2c30ccbffbee`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. RTE_Switch is called when this action is configured.
- **BswMSchMSwitch**
  - UUID: `ECUC:07525aab-f7a7-4e5b-a6b0-762131ec234d`
  - 描述: This container defines a mode switch indication that the BswM provides to the SW-C that need to be notified about the mode switch. SchM_Switch is called when this action is configured.
- **BswMSwitchIPduMode**
  - UUID: `ECUC:239dfa77-aac8-4c83-a5e7-1be8c85669a5`
  - 描述: This container includes all parameters related to the selection of the transmission mode an I-PDU to be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.
- **BswMTriggerIPduSend**
  - UUID: `ECUC:5e313869-250f-44b6-964e-4dbda0dc8af8`
  - 描述: This container includes all parameters related to the triggering of an I-PDU to be sent by COM. Com_TriggerIPDUSend is called when this action is configured.
- **BswMTriggerSlaveRTEStop**
  - UUID: `ECUC:c187c207-dff7-477d-b46f-1e0518c19801`
  - 描述: This container includes all parameters needed to stop the RTE on a slave core. This choice shall only be chosen if multicore is used.
- **BswMTriggerStartUpPhase2**
  - UUID: `ECUC:0438f6fb-7ba7-401e-9953-274c33f4c3c5`
  - 描述: This container includes all parameters needed to start phase two on a slave core. This choice shall only be chosen if multicore is used.
- **BswMUserCallout**
  - UUID: `ECUC:1c998532-6f53-42ea-9dad-4825df61605a`
  - 描述: This container includes all details needed for a user defined function call.

**容器描述**:

Choice container including the available actions to be used in the action lists.

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

1. **BswM**
