# Det - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:13

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Det](#det)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-3-0.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Det

#### 基本信息

- **UUID**: `ECUC:6acf214a-da9c-4b50-85cd-59b92e6636e6`
- **模块名称**: `Det`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Det configuration includes the functions to be called at notification. On one

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.3.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. DetConfigSet

**容器属性**:

- **UUID**: `ECUC:5dd819cd-a8a0-4190-8c6a-8e1a29607869`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetConfigSet`
- **多重性**: [0..1]

**容器描述**:

Configuration set container for Det.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DetModule

**容器属性**:

- **UUID**: `ECUC:0b7d9c3e-7690-4cef-b6b1-394862e748f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModule`
- **多重性**: [0..infinite]

**容器描述**:

This container describes a non BSW module that is using the Det via Service Interface.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DetModuleId

- **UUID**: `ECUC:90426035-5ea7-46d9-a899-026b1b5cb19c`
- **参数名**: `DetModuleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [4096..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the error reporting component. When reporting errors to the DET, a symbolic name derived from the moduleID has to be used to identify the reporter.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DetModuleInstance

**容器属性**:

- **UUID**: `ECUC:8e0d687f-fd94-48cd-b975-d661274fb333`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModuleInstance`
- **多重性**: [1..infinite]

**容器描述**:

Describes the Instance used for the according Service Port.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DetInstanceId

- **UUID**: `ECUC:86c27104-85da-43ea-a8be-427590bfc8c3`
- **参数名**: `DetInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the InstanceId used for the according Service Port.

####### 2. DetModuleInstance

**容器属性**:

- **UUID**: `ECUC:8e0d687f-fd94-48cd-b975-d661274fb333`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModuleInstance`
- **多重性**: [1..infinite]

**容器描述**:

Describes the Instance used for the according Service Port.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DetInstanceId

- **UUID**: `ECUC:86c27104-85da-43ea-a8be-427590bfc8c3`
- **参数名**: `DetInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the InstanceId used for the according Service Port.

##### 2. DetModule

**容器属性**:

- **UUID**: `ECUC:0b7d9c3e-7690-4cef-b6b1-394862e748f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModule`
- **多重性**: [0..infinite]

**容器描述**:

This container describes a non BSW module that is using the Det via Service Interface.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DetModuleId

- **UUID**: `ECUC:90426035-5ea7-46d9-a899-026b1b5cb19c`
- **参数名**: `DetModuleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [4096..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the error reporting component. When reporting errors to the DET, a symbolic name derived from the moduleID has to be used to identify the reporter.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DetModuleInstance

**容器属性**:

- **UUID**: `ECUC:8e0d687f-fd94-48cd-b975-d661274fb333`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModuleInstance`
- **多重性**: [1..infinite]

**容器描述**:

Describes the Instance used for the according Service Port.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DetInstanceId

- **UUID**: `ECUC:86c27104-85da-43ea-a8be-427590bfc8c3`
- **参数名**: `DetInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the InstanceId used for the according Service Port.

##### 3. DetModuleInstance

**容器属性**:

- **UUID**: `ECUC:8e0d687f-fd94-48cd-b975-d661274fb333`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModuleInstance`
- **多重性**: [1..infinite]

**容器描述**:

Describes the Instance used for the according Service Port.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DetInstanceId

- **UUID**: `ECUC:86c27104-85da-43ea-a8be-427590bfc8c3`
- **参数名**: `DetInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Describes the InstanceId used for the according Service Port.

##### 4. DetGeneral

**容器属性**:

- **UUID**: `ECUC:b7be2bf7-601e-4026-ac3e-a373d11757e9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetGeneral`
- **多重性**: [1..1]

**容器描述**:

Generic configuration parameters of the Det module.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. DetForwardToDlt

- **UUID**: `ECUC:b2357d09-e516-4d39-9ffc-ea9d879036cd`
- **参数名**: `DetForwardToDlt`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Only if the parameter is present and set to true, the Det requires the Dlt interface and forwards it's call to the function Dlt_DetForwardErrorTrace. In this case the optional interface to Dlt_Det is required.

######## 2. DetVersionInfoApi

- **UUID**: `ECUC:e159322f-adc7-4d76-a86c-f70943ef81d7`
- **参数名**: `DetVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

####### FUNCTION-NAME 类型参数

######## 1. DetReportRuntimeErrorCallout

- **UUID**: `ECUC:2d406ad5-163f-459f-8ad8-75e7b6ec4234`
- **参数名**: `DetReportRuntimeErrorCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This parameter defines the existence and the names of callout functions for the corresponding runtime error handler.

######## 2. DetReportTransientFaultCallout

- **UUID**: `ECUC:ca0af0d8-ebf1-42e4-85b2-fccf8c24acf2`
- **参数名**: `DetReportTransientFaultCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This parameter defines the existence and the names of callout functions for the corresponding transient fault handler.

##### 5. DetNotification

**容器属性**:

- **UUID**: `ECUC:1f580088-5563-4447-93e8-216411efb4c8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetNotification`
- **多重性**: [0..1]

**容器描述**:

Configuration of the notification functions.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DetErrorHook

- **UUID**: `ECUC:d84b34e6-1a69-4388-9f95-60c7bc06a711`
- **参数名**: `DetErrorHook`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Optional list of functions to be called by the Default Error Tracer in context of each call of Det_ReportError.

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

1. **Det**
