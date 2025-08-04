# Det - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:48

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Det](#det)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00048.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Det

#### 基本信息

- **UUID**: `59256d6c-5eb7-4e5f-b2e2-456df76fd7ec`
- **模块名称**: `Det`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Default Error Tracer. DET is the central error handler in the AUTOSAR architecture. All other basic software modules can report development errors, runtime errors and transient faults to the DET.
#AUTOSAR #ServiceComponent

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.05.00

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. DetConfigSet

**容器属性**:

- **UUID**: `e82010a5-eb64-495c-b2ca-a4cc826540ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetConfigSet`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configuration set container for Det.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DetModule

**容器属性**:

- **UUID**: `3e2ca637-3696-4204-a983-2192d1f12e86`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModule`
- **多重性**: [0..65535]
- **需要索引**: false

**容器描述**:

This container describes a non BSW module that is using the Det via Service Interface.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DetModuleId

- **UUID**: `d6b5d502-73f5-4f39-8632-928c63dfc327`
- **参数名**: `DetModuleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4096`
- **取值范围**: [4096..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: Unique identifier of the error reporting component. When reporting errors to the DET, a symbolic name derived from the moduleID has to be used to identify the reporter.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DetModuleInstance

**容器属性**:

- **UUID**: `b0f3376b-5777-401c-aa78-0a10f4ef1a10`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModuleInstance`
- **多重性**: [0..255]
- **需要索引**: false

**容器描述**:

Describes the Instance used for the according Service Port. It shall be used to differentiate software component instances when multiple instantiation is used.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DetInstanceId

- **UUID**: `df03b8b6-7a13-42c1-b972-753c5c73b65b`
- **参数名**: `DetInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter describes the InstanceId used for the according Service Port. It shall be used to differentiate software component instances when multiple instantiation is used. Else it shall be set to 0.

####### 2. DetModuleInstance

**容器属性**:

- **UUID**: `b0f3376b-5777-401c-aa78-0a10f4ef1a10`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModuleInstance`
- **多重性**: [0..255]
- **需要索引**: false

**容器描述**:

Describes the Instance used for the according Service Port. It shall be used to differentiate software component instances when multiple instantiation is used.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DetInstanceId

- **UUID**: `df03b8b6-7a13-42c1-b972-753c5c73b65b`
- **参数名**: `DetInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter describes the InstanceId used for the according Service Port. It shall be used to differentiate software component instances when multiple instantiation is used. Else it shall be set to 0.

##### 2. DetModule

**容器属性**:

- **UUID**: `3e2ca637-3696-4204-a983-2192d1f12e86`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModule`
- **多重性**: [0..65535]
- **需要索引**: false

**容器描述**:

This container describes a non BSW module that is using the Det via Service Interface.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DetModuleId

- **UUID**: `d6b5d502-73f5-4f39-8632-928c63dfc327`
- **参数名**: `DetModuleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4096`
- **取值范围**: [4096..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: Unique identifier of the error reporting component. When reporting errors to the DET, a symbolic name derived from the moduleID has to be used to identify the reporter.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DetModuleInstance

**容器属性**:

- **UUID**: `b0f3376b-5777-401c-aa78-0a10f4ef1a10`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModuleInstance`
- **多重性**: [0..255]
- **需要索引**: false

**容器描述**:

Describes the Instance used for the according Service Port. It shall be used to differentiate software component instances when multiple instantiation is used.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DetInstanceId

- **UUID**: `df03b8b6-7a13-42c1-b972-753c5c73b65b`
- **参数名**: `DetInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter describes the InstanceId used for the according Service Port. It shall be used to differentiate software component instances when multiple instantiation is used. Else it shall be set to 0.

##### 3. DetModuleInstance

**容器属性**:

- **UUID**: `b0f3376b-5777-401c-aa78-0a10f4ef1a10`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetModuleInstance`
- **多重性**: [0..255]
- **需要索引**: false

**容器描述**:

Describes the Instance used for the according Service Port. It shall be used to differentiate software component instances when multiple instantiation is used.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DetInstanceId

- **UUID**: `df03b8b6-7a13-42c1-b972-753c5c73b65b`
- **参数名**: `DetInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter describes the InstanceId used for the according Service Port. It shall be used to differentiate software component instances when multiple instantiation is used. Else it shall be set to 0.

##### 4. DetGeneral

**容器属性**:

- **UUID**: `f8499476-3b46-4cc0-a170-8135f40a6041`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Generic configuration parameters of the Det module.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. DetGlobalFilterSize

- **UUID**: `962458c9-4e89-42db-9e0a-7848ed3c8a8d`
- **参数名**: `DetGlobalFilterSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter configures the number of global filters which can be used to discard irrelevant errors. The filters are typically configured at runtime using a debugger. Please refer to the technical reference about details.
This setting is only relevant if extended debug support (DetExtDebugSupport) is enabled.

######## 2. DetBreakFilterSize

- **UUID**: `af340689-c359-45f1-b6d0-aebcb4b2af1c`
- **参数名**: `DetBreakFilterSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter configures the number of break handler filters which can be used to exit the DET without entering the endless loop. The filters are typically configured at runtime using a debugger. Please refer to the technical reference about details.
This setting is only relevant if extended debug support (DetExtDebugSupport) is enabled.

######## 3. DetLogBufferSize

- **UUID**: `05f44335-179d-40a1-a6f2-a523de239cd3`
- **参数名**: `DetLogBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter configures the size of the log buffer which can be used to log errors reported to the DET. The log buffer is typically accessed at runtime using a debugger. Please refer to the technical reference about details.
This setting is only relevant if extended debug support (DetExtDebugSupport) is enabled.

######## 4. DetReportErrorRecursionLimit

- **UUID**: `18914a90-611e-4d5f-84b5-813dc913582e`
- **参数名**: `DetReportErrorRecursionLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter configures the number of allowed recursions for calling Det_ReportError. Refer to the technical reference for details. To disable recursion detection set this value to 0.

######## 5. DetReportRuntimeErrorRecursionLimit

- **UUID**: `d375cb95-97e8-4da4-bf0d-3a7efbef1eac`
- **参数名**: `DetReportRuntimeErrorRecursionLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter configures the number of allowed recursions for calling Det_ReportRuntimeError. Refer to the technical reference for details. To disable recursion detection set this value to 0.

######## 6. DetReportTransientFaultRecursionLimit

- **UUID**: `dbc9ed68-ecbf-4203-9547-03e4cbdfc2f9`
- **参数名**: `DetReportTransientFaultRecursionLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter configures the number of allowed recursions for calling Det_ReportTransientFault. Refer to the technical reference for details. To disable recursion detection set this value to 0.

######## 7. DetDltFilterSize

- **UUID**: `e0a982d8-33aa-4fc9-8303-3582c388dcfd`
- **参数名**: `DetDltFilterSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter configures the number of Dlt filters which can be used to suppress reporting of irrelevant errors to the Dlt module. The filters are typically configured at runtime using a debugger. Please refer to the technical reference about details.
This setting is only relevant if extended debug support (DetExtDebugSupport) is enabled and if Dlt forwarding (DetForwardToDlt) is enabled.

####### BOOLEAN 类型参数

######## 1. DetForwardToDlt

- **UUID**: `91a8e24c-9b87-4464-b290-d8eeb27b8b4d`
- **参数名**: `DetForwardToDlt`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter controls the fowarding of DET errors to the DLT module. If the parameter is present and set to true, the DET forwards all errors to the function Dlt_DetForwardErrorTrace before other DET functionality is performed.

######## 2. DetVersionInfoApi

- **UUID**: `bcbdfeb4-38b3-4c8c-b943-8ca25b4c1c26`
- **参数名**: `DetVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter if set to true enables the function Det_GetVersionInfo() to get major, minor and patch version information.
true: Version info API enabled.
false: Version info API disabled.

######## 3. DetEnableDet

- **UUID**: `3d5c0c78-e0bf-40bb-b673-529288e14a0b`
- **参数名**: `DetEnableDet`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter if set to true enables reporting of development error. It can be used to disable the DET completely.

######## 4. DetExtDebugSupport

- **UUID**: `45dfe56a-1154-44bf-818e-0b51e75492a9`
- **参数名**: `DetExtDebugSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter if set the true enables the extended debug support feature which provides additional functionality to the DET such as filtering, logging and flexible break handling. Please refer to the technical reference for details.

####### STRING 类型参数

######## 1. DetUserConfigFile

- **UUID**: `519fd349-37ca-4ec1-91b3-20c683f18982`
- **参数名**: `DetUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

##### 5. DetNotification

**容器属性**:

- **UUID**: `b6e7f526-3caa-4e13-9690-1b8703e304c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DetNotification`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configuration of the notification functions.

###### 参数配置

此容器包含 **3** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DetErrorHook

- **UUID**: `37447d40-0c1d-41e3-a4de-065fecac3f6e`
- **参数名**: `DetErrorHook`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Optional list of functions to be called by the Default Error Tracer in context of each call of Det_ReportError.
The type of these functions shall be identical the type of Det_ReportError itself: Std_ReturnType (*f)(uint16, uint8, uint8, uint8).

######## 2. DetReportRuntimeErrorCallout

- **UUID**: `b59016bc-4335-4c14-8472-68a85a4656e0`
- **参数名**: `DetReportRuntimeErrorCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the existence and the names of callout functions for the corresponding runtime error handler. 
The type of these functions shall be identical the type of Det_ReportRuntimeError itself: Std_ReturnType (*f)(uint16, uint8, uint8, uint8)

######## 3. DetReportTransientFaultCallout

- **UUID**: `3a13b4c7-569e-4c8a-9ca1-7abfbd8e74eb`
- **参数名**: `DetReportTransientFaultCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the existence and the names of callout functions for the corresponding transient fault handler.
The type of these functions shall be identical the type of Det_ReportTransientFault itself: Std_ReturnType (*f)(uint16, uint8, uint8, uint8)

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Det**

##### BSW-IMPLEMENTATION 类型元素

1. **Det_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Det_Pre**
2. **Det_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Det_Impl

- **UUID**: `a3c2bcfc-41be-48b7-bb7a-dae0ce607f12`
- **实现名称**: `Det_Impl`
- **编程语言**: C
- **软件版本**: 14.00.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.05.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Det_Pre

- **UUID**: `164b51b1-d1c1-47bd-b6ca-304ff7d60cd7`
- **配置名称**: `Det_Pre`
- **定义引用**: `/MICROSAR/Det`

### 2. Det_Rec

- **UUID**: `3d3b64c6-d8dd-4e71-8998-f7fce83d5bff`
- **配置名称**: `Det_Rec`
- **定义引用**: `/MICROSAR/Det`
