# Arti - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:05

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Arti](#arti)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00049.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Arti

#### 基本信息

- **UUID**: `ECUC:d0758586-0443-404b-a4e3-dd824bb49b41`
- **模块名称**: `Arti`
- **多重性**: [0..1]

#### 模块描述

The Arti Module serves as a superordinate container collecting all information and parameters concerning ARTI.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.6.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **40** 个配置容器：

##### 1. ArtiGeneric

**容器属性**:

- **UUID**: `ECUC:0e95db36-c2ca-478f-97d2-668bf818bfea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGeneric`
- **多重性**: [0..1]

**容器描述**:

The ArtiGeneric container contains definitions for generic objects, i.e. not belonging to a standard AUTOSAR module.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. ArtiGenericComponentClass

**容器属性**:

- **UUID**: `ECUC:dc8b1c52-b839-4702-bb8c-c00e6dacf867`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClass`
- **多重性**: [0..infinite]

**容器描述**:

The class definition describes the layout of the object (similar to a "class" definition in C).

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiGenericComponentClassName

- **UUID**: `ECUC:79e31615-719b-4b28-925b-201e1179e7cc`
- **参数名**: `ArtiGenericComponentClassName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the class.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ArtiGenericComponentClassParameter

**容器属性**:

- **UUID**: `ECUC:b1ca1916-0013-4c35-bc71-2e3e03cabf31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClassParameter`
- **多重性**: [0..infinite]

**容器描述**:

Parameter definition of a class.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. ArtiGenericComponentClassParameterName

- **UUID**: `ECUC:9f2ea270-7b99-4b12-a771-536d771488eb`
- **参数名**: `ArtiGenericComponentClassParameterName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the parameter.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. ArtiGenericComponentClassParameterTypeMapRef

- **UUID**: `ECUC:8de6e175-ddaa-4330-a4bf-3e422898c906`
- **引用名**: `ArtiGenericComponentClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiParameterTypeMap`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a parameter type to interpret the parameter value.

####### 2. ArtiGenericComponentClassParameter

**容器属性**:

- **UUID**: `ECUC:b1ca1916-0013-4c35-bc71-2e3e03cabf31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClassParameter`
- **多重性**: [0..infinite]

**容器描述**:

Parameter definition of a class.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiGenericComponentClassParameterName

- **UUID**: `ECUC:9f2ea270-7b99-4b12-a771-536d771488eb`
- **参数名**: `ArtiGenericComponentClassParameterName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the parameter.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiGenericComponentClassParameterTypeMapRef

- **UUID**: `ECUC:8de6e175-ddaa-4330-a4bf-3e422898c906`
- **引用名**: `ArtiGenericComponentClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiParameterTypeMap`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a parameter type to interpret the parameter value.

####### 3. ArtiGenericComponentInstance

**容器属性**:

- **UUID**: `ECUC:1171181e-f661-40f0-bd48-7e753290dfd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstance`
- **多重性**: [0..infinite]

**容器描述**:

The instance definition describes a specific instantiated object.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiGenericComponentInstanceName

- **UUID**: `ECUC:1d57675e-c642-4cb1-9f57-388c4a670cb9`
- **参数名**: `ArtiGenericComponentInstanceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the instance.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiGenericComponentInstanceClassRef

- **UUID**: `ECUC:98317161-8c38-4440-92c8-a681ac313c7e`
- **引用名**: `ArtiGenericComponentInstanceClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a ArtGenericClass of which this object is instantiated.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ArtiGenericComponentInstanceParameter

**容器属性**:

- **UUID**: `ECUC:0ce680cf-6a46-4224-be85-cebc9da404b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstanceParameter`
- **多重性**: [0..infinite]

**容器描述**:

Parameter definition of an instance.

########## 引用关系

此容器包含 **4** 个引用：

########### REFERENCE 类型引用

############ 1. ArtiGenericComponentInstanceParameterClassParameterRef

- **UUID**: `ECUC:973f8d67-63a5-4b7e-b77a-a490839e21a5`
- **引用名**: `ArtiGenericComponentInstanceParameterClassParameterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiGenericComponentClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass/ArtiGenericComponentClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClassParameter that defines this parameter.

############ 2. ArtiGenericComponentInstanceParameterConstantRef

- **UUID**: `ECUC:4b5042b3-46b6-47bf-945d-e9a998784f0f`
- **引用名**: `ArtiGenericComponentInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiConstant`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiConstant that represents the value of this parameter.

############ 3. ArtiGenericComponentInstanceParameterExpressionRef

- **UUID**: `ECUC:d8811807-ab16-4bdd-b707-9827a8f7cc5c`
- **引用名**: `ArtiGenericComponentInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiExpression`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiExpression that evaluates the value of this parameter.

############ 4. ArtiGenericComponentInstanceParameterHookRef

- **UUID**: `ECUC:4cb52969-651d-43b2-be80-86c040ecc70b`
- **引用名**: `ArtiGenericComponentInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiHook`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a hook that records this parameter.

####### 4. ArtiGenericComponentInstanceParameter

**容器属性**:

- **UUID**: `ECUC:0ce680cf-6a46-4224-be85-cebc9da404b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstanceParameter`
- **多重性**: [0..infinite]

**容器描述**:

Parameter definition of an instance.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiGenericComponentInstanceParameterClassParameterRef

- **UUID**: `ECUC:973f8d67-63a5-4b7e-b77a-a490839e21a5`
- **引用名**: `ArtiGenericComponentInstanceParameterClassParameterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiGenericComponentClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass/ArtiGenericComponentClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClassParameter that defines this parameter.

########## 2. ArtiGenericComponentInstanceParameterConstantRef

- **UUID**: `ECUC:4b5042b3-46b6-47bf-945d-e9a998784f0f`
- **引用名**: `ArtiGenericComponentInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiConstant`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiConstant that represents the value of this parameter.

########## 3. ArtiGenericComponentInstanceParameterExpressionRef

- **UUID**: `ECUC:d8811807-ab16-4bdd-b707-9827a8f7cc5c`
- **引用名**: `ArtiGenericComponentInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiExpression`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiExpression that evaluates the value of this parameter.

########## 4. ArtiGenericComponentInstanceParameterHookRef

- **UUID**: `ECUC:4cb52969-651d-43b2-be80-86c040ecc70b`
- **引用名**: `ArtiGenericComponentInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiHook`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a hook that records this parameter.

##### 2. ArtiGenericComponentClass

**容器属性**:

- **UUID**: `ECUC:dc8b1c52-b839-4702-bb8c-c00e6dacf867`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClass`
- **多重性**: [0..infinite]

**容器描述**:

The class definition describes the layout of the object (similar to a "class" definition in C).

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiGenericComponentClassName

- **UUID**: `ECUC:79e31615-719b-4b28-925b-201e1179e7cc`
- **参数名**: `ArtiGenericComponentClassName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the class.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ArtiGenericComponentClassParameter

**容器属性**:

- **UUID**: `ECUC:b1ca1916-0013-4c35-bc71-2e3e03cabf31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClassParameter`
- **多重性**: [0..infinite]

**容器描述**:

Parameter definition of a class.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiGenericComponentClassParameterName

- **UUID**: `ECUC:9f2ea270-7b99-4b12-a771-536d771488eb`
- **参数名**: `ArtiGenericComponentClassParameterName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the parameter.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiGenericComponentClassParameterTypeMapRef

- **UUID**: `ECUC:8de6e175-ddaa-4330-a4bf-3e422898c906`
- **引用名**: `ArtiGenericComponentClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiParameterTypeMap`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a parameter type to interpret the parameter value.

##### 3. ArtiGenericComponentClassParameter

**容器属性**:

- **UUID**: `ECUC:b1ca1916-0013-4c35-bc71-2e3e03cabf31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClassParameter`
- **多重性**: [0..infinite]

**容器描述**:

Parameter definition of a class.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiGenericComponentClassParameterName

- **UUID**: `ECUC:9f2ea270-7b99-4b12-a771-536d771488eb`
- **参数名**: `ArtiGenericComponentClassParameterName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the parameter.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiGenericComponentClassParameterTypeMapRef

- **UUID**: `ECUC:8de6e175-ddaa-4330-a4bf-3e422898c906`
- **引用名**: `ArtiGenericComponentClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiParameterTypeMap`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a parameter type to interpret the parameter value.

##### 4. ArtiGenericComponentInstance

**容器属性**:

- **UUID**: `ECUC:1171181e-f661-40f0-bd48-7e753290dfd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstance`
- **多重性**: [0..infinite]

**容器描述**:

The instance definition describes a specific instantiated object.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiGenericComponentInstanceName

- **UUID**: `ECUC:1d57675e-c642-4cb1-9f57-388c4a670cb9`
- **参数名**: `ArtiGenericComponentInstanceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the instance.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiGenericComponentInstanceClassRef

- **UUID**: `ECUC:98317161-8c38-4440-92c8-a681ac313c7e`
- **引用名**: `ArtiGenericComponentInstanceClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a ArtGenericClass of which this object is instantiated.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ArtiGenericComponentInstanceParameter

**容器属性**:

- **UUID**: `ECUC:0ce680cf-6a46-4224-be85-cebc9da404b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstanceParameter`
- **多重性**: [0..infinite]

**容器描述**:

Parameter definition of an instance.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiGenericComponentInstanceParameterClassParameterRef

- **UUID**: `ECUC:973f8d67-63a5-4b7e-b77a-a490839e21a5`
- **引用名**: `ArtiGenericComponentInstanceParameterClassParameterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiGenericComponentClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass/ArtiGenericComponentClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClassParameter that defines this parameter.

########## 2. ArtiGenericComponentInstanceParameterConstantRef

- **UUID**: `ECUC:4b5042b3-46b6-47bf-945d-e9a998784f0f`
- **引用名**: `ArtiGenericComponentInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiConstant`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiConstant that represents the value of this parameter.

########## 3. ArtiGenericComponentInstanceParameterExpressionRef

- **UUID**: `ECUC:d8811807-ab16-4bdd-b707-9827a8f7cc5c`
- **引用名**: `ArtiGenericComponentInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiExpression`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiExpression that evaluates the value of this parameter.

########## 4. ArtiGenericComponentInstanceParameterHookRef

- **UUID**: `ECUC:4cb52969-651d-43b2-be80-86c040ecc70b`
- **引用名**: `ArtiGenericComponentInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiHook`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a hook that records this parameter.

##### 5. ArtiGenericComponentInstanceParameter

**容器属性**:

- **UUID**: `ECUC:0ce680cf-6a46-4224-be85-cebc9da404b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstanceParameter`
- **多重性**: [0..infinite]

**容器描述**:

Parameter definition of an instance.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiGenericComponentInstanceParameterClassParameterRef

- **UUID**: `ECUC:973f8d67-63a5-4b7e-b77a-a490839e21a5`
- **引用名**: `ArtiGenericComponentInstanceParameterClassParameterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiGenericComponentClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass/ArtiGenericComponentClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClassParameter that defines this parameter.

######## 2. ArtiGenericComponentInstanceParameterConstantRef

- **UUID**: `ECUC:4b5042b3-46b6-47bf-945d-e9a998784f0f`
- **引用名**: `ArtiGenericComponentInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiConstant`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiConstant that represents the value of this parameter.

######## 3. ArtiGenericComponentInstanceParameterExpressionRef

- **UUID**: `ECUC:d8811807-ab16-4bdd-b707-9827a8f7cc5c`
- **引用名**: `ArtiGenericComponentInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiExpression`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiExpression that evaluates the value of this parameter.

######## 4. ArtiGenericComponentInstanceParameterHookRef

- **UUID**: `ECUC:4cb52969-651d-43b2-be80-86c040ecc70b`
- **引用名**: `ArtiGenericComponentInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiHook`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a hook that records this parameter.

##### 6. ArtiHardware

**容器属性**:

- **UUID**: `ECUC:8ae17e9e-0047-4b41-af33-78e6292cdfe9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHardware`
- **多重性**: [0..1]

**容器描述**:

The ArtiHardware container contains ARTI extensions to the EcucHardware module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. ArtiHardwareCoreClass

**容器属性**:

- **UUID**: `ECUC:2857607a-8c82-4f33-bb04-8ab37a2d358b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHardwareCoreClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "Core" object, extending the EcucCoreDefinition.

######## 引用关系

此容器包含 **6** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiHardwareCoreClassCurrentApplicationRef

- **UUID**: `ECUC:36f89e39-a933-428e-b126-c64841317313`
- **引用名**: `ArtiHardwareCoreClassCurrentApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentApplicationInstance parameter.

########## 2. ArtiHardwareCoreClassCurrentIsrRef

- **UUID**: `ECUC:c9e3fffc-8e0f-4227-8cf4-387375fac5fb`
- **引用名**: `ArtiHardwareCoreClassCurrentIsrRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentIsrInstance parameter.

########## 3. ArtiHardwareCoreClassCurrentTaskRef

- **UUID**: `ECUC:708bb30c-2a67-4c71-903c-d9c6bf6ff762`
- **引用名**: `ArtiHardwareCoreClassCurrentTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentTaskInstance parameter.

########## 4. ArtiHardwareCoreClassGenericComponentRef

- **UUID**: `ECUC:0a888e86-605f-46ab-ac9c-42d475ed602f`
- **引用名**: `ArtiHardwareCoreClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the core description.

########## 5. ArtiHardwareCoreClassLastErrorRef

- **UUID**: `ECUC:1b65f6e9-3208-4cf1-acb8-bbffeb3991b2`
- **引用名**: `ArtiHardwareCoreClassLastErrorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiLastErrorInstance parameter.

########## 6. ArtiHardwareCoreClassRunningTaskPriorityRef

- **UUID**: `ECUC:ef3bb939-b4c6-48cb-9c09-cb9116346610`
- **引用名**: `ArtiHardwareCoreClassRunningTaskPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiHwCoreInstanceRunningTaskPriority parameter. This attribute specifies how to evaluate the current priority of the task referred by RUNNINGTASK. The current priority can be different from the static task priority as a result of priority ceiling protocol. This attribute differs from ArtiCurrentTask->ArtiOsTaskClassPriority as here is a single variable while in multiple tasks there is a single variable per task.

####### 2. ArtiHardwareCoreInstance

**容器属性**:

- **UUID**: `ECUC:18bd11ce-a56f-4567-9063-0de14da10d07`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHardwareCoreInstance`
- **多重性**: [0..infinite]

**容器描述**:

Description: Represents an instance of an ARTI "Core" object, extending the EcucCoreDefinition. When using ARTI for debugging or hardware based tracing, this is mandatory (i.e. multiplicity 1..*), else optional.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. ArtiHardwareCoreInstanceCoreId

- **UUID**: `ECUC:eabec4d1-dc65-423a-ae3a-84f9039de478`
- **参数名**: `ArtiHardwareCoreInstanceCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter represents the "CoreID" as given by the OS, returned by GetCoreID().

######## 引用关系

此容器包含 **8** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiHardwareCoreInstanceCurrentApplicationRef

- **UUID**: `ECUC:9a7fdd04-1dcf-4728-97f5-28418182e5a2`
- **引用名**: `ArtiHardwareCoreInstanceCurrentApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current application" that is running on this core.

########## 2. ArtiHardwareCoreInstanceCurrentIsrRef

- **UUID**: `ECUC:6e865b4a-079b-4903-baec-5661a918a7b2`
- **引用名**: `ArtiHardwareCoreInstanceCurrentIsrRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current ISR" that is running on this core.

########## 3. ArtiHardwareCoreInstanceCurrentTaskRef

- **UUID**: `ECUC:59402b5a-a0bd-4cb0-8aea-00334d1c529f`
- **引用名**: `ArtiHardwareCoreInstanceCurrentTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current task" that is running on this core.

########## 4. ArtiHardwareCoreInstanceEcucCoreRef

- **UUID**: `ECUC:47b50d4e-d888-4937-bab8-115f1d9387e5`
- **引用名**: `ArtiHardwareCoreInstanceEcucCoreRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucCoreDefinition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucHardware/EcucCoreDefinition`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the EcucCoreDefinition of this core.

########## 5. ArtiHardwareCoreInstanceGenericComponentRef

- **UUID**: `ECUC:b6f98c07-f72e-42d1-ac19-2b8d85c07970`
- **引用名**: `ArtiHardwareCoreInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends a core.

########## 6. ArtiHardwareCoreInstanceLastErrorRef

- **UUID**: `ECUC:4286f213-38f7-475a-9d2c-4188a8ac75ba`
- **引用名**: `ArtiHardwareCoreInstanceLastErrorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "last error" that happened on this core.

########## 7. ArtiHardwareCoreInstanceRunningTaskPriorityRef

- **UUID**: `ECUC:b093adb2-8da2-444f-b97a-c9ad6f37f246`
- **引用名**: `ArtiHardwareCoreInstanceRunningTaskPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "running task priority" that is on this core.

########## 8. ArtiHardwareCoreInstanceValidRef

- **UUID**: `ECUC:b0132d13-b0f7-413d-bf4f-ddac77a553c0`
- **引用名**: `ArtiHardwareCoreInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiHwCoreInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 7. ArtiHardwareCoreClass

**容器属性**:

- **UUID**: `ECUC:2857607a-8c82-4f33-bb04-8ab37a2d358b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHardwareCoreClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "Core" object, extending the EcucCoreDefinition.

###### 引用关系

此容器包含 **6** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiHardwareCoreClassCurrentApplicationRef

- **UUID**: `ECUC:36f89e39-a933-428e-b126-c64841317313`
- **引用名**: `ArtiHardwareCoreClassCurrentApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentApplicationInstance parameter.

######## 2. ArtiHardwareCoreClassCurrentIsrRef

- **UUID**: `ECUC:c9e3fffc-8e0f-4227-8cf4-387375fac5fb`
- **引用名**: `ArtiHardwareCoreClassCurrentIsrRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentIsrInstance parameter.

######## 3. ArtiHardwareCoreClassCurrentTaskRef

- **UUID**: `ECUC:708bb30c-2a67-4c71-903c-d9c6bf6ff762`
- **引用名**: `ArtiHardwareCoreClassCurrentTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentTaskInstance parameter.

######## 4. ArtiHardwareCoreClassGenericComponentRef

- **UUID**: `ECUC:0a888e86-605f-46ab-ac9c-42d475ed602f`
- **引用名**: `ArtiHardwareCoreClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the core description.

######## 5. ArtiHardwareCoreClassLastErrorRef

- **UUID**: `ECUC:1b65f6e9-3208-4cf1-acb8-bbffeb3991b2`
- **引用名**: `ArtiHardwareCoreClassLastErrorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiLastErrorInstance parameter.

######## 6. ArtiHardwareCoreClassRunningTaskPriorityRef

- **UUID**: `ECUC:ef3bb939-b4c6-48cb-9c09-cb9116346610`
- **引用名**: `ArtiHardwareCoreClassRunningTaskPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiHwCoreInstanceRunningTaskPriority parameter. This attribute specifies how to evaluate the current priority of the task referred by RUNNINGTASK. The current priority can be different from the static task priority as a result of priority ceiling protocol. This attribute differs from ArtiCurrentTask->ArtiOsTaskClassPriority as here is a single variable while in multiple tasks there is a single variable per task.

##### 8. ArtiHardwareCoreInstance

**容器属性**:

- **UUID**: `ECUC:18bd11ce-a56f-4567-9063-0de14da10d07`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHardwareCoreInstance`
- **多重性**: [0..infinite]

**容器描述**:

Description: Represents an instance of an ARTI "Core" object, extending the EcucCoreDefinition. When using ARTI for debugging or hardware based tracing, this is mandatory (i.e. multiplicity 1..*), else optional.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. ArtiHardwareCoreInstanceCoreId

- **UUID**: `ECUC:eabec4d1-dc65-423a-ae3a-84f9039de478`
- **参数名**: `ArtiHardwareCoreInstanceCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter represents the "CoreID" as given by the OS, returned by GetCoreID().

###### 引用关系

此容器包含 **8** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiHardwareCoreInstanceCurrentApplicationRef

- **UUID**: `ECUC:9a7fdd04-1dcf-4728-97f5-28418182e5a2`
- **引用名**: `ArtiHardwareCoreInstanceCurrentApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current application" that is running on this core.

######## 2. ArtiHardwareCoreInstanceCurrentIsrRef

- **UUID**: `ECUC:6e865b4a-079b-4903-baec-5661a918a7b2`
- **引用名**: `ArtiHardwareCoreInstanceCurrentIsrRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current ISR" that is running on this core.

######## 3. ArtiHardwareCoreInstanceCurrentTaskRef

- **UUID**: `ECUC:59402b5a-a0bd-4cb0-8aea-00334d1c529f`
- **引用名**: `ArtiHardwareCoreInstanceCurrentTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current task" that is running on this core.

######## 4. ArtiHardwareCoreInstanceEcucCoreRef

- **UUID**: `ECUC:47b50d4e-d888-4937-bab8-115f1d9387e5`
- **引用名**: `ArtiHardwareCoreInstanceEcucCoreRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucCoreDefinition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucHardware/EcucCoreDefinition`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the EcucCoreDefinition of this core.

######## 5. ArtiHardwareCoreInstanceGenericComponentRef

- **UUID**: `ECUC:b6f98c07-f72e-42d1-ac19-2b8d85c07970`
- **引用名**: `ArtiHardwareCoreInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends a core.

######## 6. ArtiHardwareCoreInstanceLastErrorRef

- **UUID**: `ECUC:4286f213-38f7-475a-9d2c-4188a8ac75ba`
- **引用名**: `ArtiHardwareCoreInstanceLastErrorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "last error" that happened on this core.

######## 7. ArtiHardwareCoreInstanceRunningTaskPriorityRef

- **UUID**: `ECUC:b093adb2-8da2-444f-b97a-c9ad6f37f246`
- **引用名**: `ArtiHardwareCoreInstanceRunningTaskPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "running task priority" that is on this core.

######## 8. ArtiHardwareCoreInstanceValidRef

- **UUID**: `ECUC:b0132d13-b0f7-413d-bf4f-ddac77a553c0`
- **引用名**: `ArtiHardwareCoreInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiHwCoreInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 9. ArtiOs

**容器属性**:

- **UUID**: `ECUC:87148dee-7bd7-42cd-85b5-2211305f3490`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOs`
- **多重性**: [0..1]

**容器描述**:

The ArtiOs container contains ARTI extensions to the EcucDefs/Os module.

###### 配置容器

本模块包含 **16** 个配置容器：

####### 1. ArtiOsAlarmClass

**容器属性**:

- **UUID**: `ECUC:f6c8f934-40a8-495d-93c5-6d24cc11b848`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsAlarmClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ArtiOsAlarm object.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsAlarmClassGenericComponentClassRef

- **UUID**: `ECUC:2b159123-ec19-44d2-ab6a-cbfd521680c6`
- **引用名**: `ArtiOsAlarmClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsAlarmClass.

########## 2. ArtiOsAlarmClassStateRef

- **UUID**: `ECUC:7e2abcc9-b755-4a65-aeee-f0d5a13a6f40`
- **引用名**: `ArtiOsAlarmClassStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsAlarmStateRef in ArtiOsAlarmInstances. This attribute specifies if an alarm is "RUNNING" or "STOPPED". The refered ArtiObjectClassParameter does include the mapping from integer to human readable "RUNNING" or "STOPPED".

####### 2. ArtiOsAlarmInstance

**容器属性**:

- **UUID**: `ECUC:13b6673b-5924-488d-9efc-98f04702dbe8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsAlarmInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an ArtiOsAlarm object, extending the EcuC OsTaskAlarm.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. ArtiOsAlarmInstanceAction

- **UUID**: `ECUC:d8e08489-bab7-4efb-8629-c14919cb3f01`
- **参数名**: `ArtiOsAlarmInstanceAction`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute provides a string with a description of the action when the alarm expires, e.g. "ActivateTask TaskA".

########## 2. ArtiOsAlarmInstanceCounter

- **UUID**: `ECUC:756503f2-4eb8-461f-a079-355e4bb43368`
- **参数名**: `ArtiOsAlarmInstanceCounter`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute provides a string containing the name of the counter used by this alarm.

######## 引用关系

此容器包含 **6** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsAlarmInstanceAlarmTimeRef

- **UUID**: `ECUC:b4d33c37-865c-4c49-bf2c-dab6df3c1a6e`
- **引用名**: `ArtiOsAlarmInstanceAlarmTimeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute specifies how to evaluate the time until the alarm expires next. The time should be represented in seconds.

########## 2. ArtiOsAlarmInstanceCycleTimeRef

- **UUID**: `ECUC:35a98a28-b083-4c79-8201-8eafd004f9d6`
- **引用名**: `ArtiOsAlarmInstanceCycleTimeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute specifies how to evaluate the cycle time for cyclic alarms. The value of "cycle time" is 0 for non-cyclic alarms. The time should be represendet in seconds.

########## 3. ArtiOsAlarmInstanceEcuCRef

- **UUID**: `ECUC:aecb39a2-9cfe-4dac-bfaa-68d826543841`
- **引用名**: `ArtiOsAlarmInstanceEcuCRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an EcuC OsAlarm that is beeing extended.

########## 4. ArtiOsAlarmInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:f94ec3f7-dff7-4d78-b797-6453c58e0dc2`
- **引用名**: `ArtiOsAlarmInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsAlarmInstance.

########## 5. ArtiOsAlarmInstanceStateRef

- **UUID**: `ECUC:77eb375d-d579-4cc9-95d6-1e64b20b12f1`
- **引用名**: `ArtiOsAlarmInstanceStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "state" of this alarm. The result then is mapped with the typemap of the ArtiOsAlarmStateRef of the ArtiOsAlarmClass.

########## 6. ArtiOsAlarmInstanceValidRef

- **UUID**: `ECUC:42da2230-8e6d-4e3c-941e-d72effca8e94`
- **引用名**: `ArtiOsAlarmInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this alarm. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 3. ArtiOsClass

**容器属性**:

- **UUID**: `ECUC:407dd9b4-0454-4bbe-ba9f-030c9f6fe697`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "Os" object, extending the EcuC OsOS.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsClassAppModeRef

- **UUID**: `ECUC:2543c018-e93d-4d83-aab8-7060068d1d7e`
- **引用名**: `ArtiOsClassAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiOsAppModeInstance parameter.

########## 2. ArtiOsClassGenericComponentRef

- **UUID**: `ECUC:ca3a7994-71fa-421e-8d5b-31256ed3fbf1`
- **引用名**: `ArtiOsClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the OS description.

########## 3. ArtiOsClassServiceTraceRef

- **UUID**: `ECUC:d3c5dce4-6661-423d-8541-760e8bde9e2f`
- **引用名**: `ArtiOsClassServiceTraceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiOsInstanceServiceTrace parameter. This attribute indicates the entry or exit of a service routine and the ID of this service routine. The value of this attribute must be evaluated from one single memory location.

####### 4. ArtiOsContextClass

**容器属性**:

- **UUID**: `ECUC:c370f4c9-6f6e-462a-bddb-624db0aa9a96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsContextClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "OsContext" object.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsContextClassGenericComponentClassRef

- **UUID**: `ECUC:d5d77649-562c-43ef-82f9-dfbc705cd081`
- **引用名**: `ArtiOsContextClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsContextClass.

####### 5. ArtiOsContextInstance

**容器属性**:

- **UUID**: `ECUC:73757e1e-6f5f-40e6-a447-edaf12ca137b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsContextInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an "ArtiContext" object.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsContextInstanceAddressRef

- **UUID**: `ECUC:d498eb59-23b7-480c-a18a-6ed6bebbba53`
- **引用名**: `ArtiOsContextInstanceAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "address" of this context.

########## 2. ArtiOsContextInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:7c03b1d4-5acd-49ed-b6fc-7330ececd934`
- **引用名**: `ArtiOsContextInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsContext.

########## 3. ArtiOsContextInstanceSizeRef

- **UUID**: `ECUC:7b80e64e-c91b-473c-b0e1-84b7f39e9856`
- **引用名**: `ArtiOsContextInstanceSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "size" of this context.

########## 4. ArtiOsContextInstanceValidRef

- **UUID**: `ECUC:f7f426f2-9b3f-4ea7-b0de-fc742bf533ab`
- **引用名**: `ArtiOsContextInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this context. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 6. ArtiOsInstance

**容器属性**:

- **UUID**: `ECUC:696083fb-4846-4ead-8267-2b601f9fb8bb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsInstance`
- **多重性**: [0..1]

**容器描述**:

Represents an instance of an ARTI "Os" object, extending the EcuC OsOS.

######## 引用关系

此容器包含 **6** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsInstanceAppModeRef

- **UUID**: `ECUC:27d75b37-1075-4ec5-98d1-0cf7f925d12e`
- **引用名**: `ArtiOsInstanceAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "application mode" of this OS.

########## 2. ArtiOsInstanceEcucRef

- **UUID**: `ECUC:4ccdcb25-b09f-4f50-ab64-22122367b124`
- **引用名**: `ArtiOsInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsOS`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsOS`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the EcucDefs/Os/OsOS of this OS.

########## 3. ArtiOsInstanceGenericComponentRef

- **UUID**: `ECUC:837582c4-d78d-4071-ba04-14148708b906`
- **引用名**: `ArtiOsInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OS.

########## 4. ArtiOsInstanceHookRef

- **UUID**: `ECUC:9f2b7d96-7a32-4cc3-8306-b087284e5c02`
- **引用名**: `ArtiOsInstanceHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiHook`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiHook`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a hook defined in the OS.

########## 5. ArtiOsInstanceServiceTraceRef

- **UUID**: `ECUC:ceddfdcc-f46a-4e85-bcc9-4c7dea5e2d53`
- **引用名**: `ArtiOsInstanceServiceTraceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a hook defined in the OS.

########## 6. ArtiOsInstanceValidRef

- **UUID**: `ECUC:a4d1f2b2-15c2-4efa-87a7-644b1d225bcb`
- **引用名**: `ArtiOsInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 7. ArtiOsIsrClass

**容器属性**:

- **UUID**: `ECUC:335c0140-9ebc-400a-a7b3-c6cdb56169f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsIsrClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "OsIsr" object, extending the EcuC OsIsr.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsIsrClassGenericComponentRef

- **UUID**: `ECUC:2fca94bd-d5ab-41f2-84ed-b2e2ebde6663`
- **引用名**: `ArtiOsIsrClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an optional ArtiGenericComponentClass that extends the OsIsr with additional parameters.

####### 8. ArtiOsIsrInstance

**容器属性**:

- **UUID**: `ECUC:b057462e-ba05-482e-b4d1-bb784a65325c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsIsrInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an ARTI "OsIsr" object, extending the EcuC OsIsr.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. ArtiOsIsrInstanceId

- **UUID**: `ECUC:e319855a-e1db-4299-82f8-80a0376604d4`
- **参数名**: `ArtiOsIsrInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter represents the "ISRID" as given by the OS, returned by GetISRID().

######### ENUMERATION 类型参数

########## 1. ArtiOsIsrInstanceCategory

- **UUID**: `ECUC:a6bc034f-8b89-4c91-aeb3-77294bb27f90`
- **参数名**: `ArtiOsIsrInstanceCategory`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CATEGORY_1` (来源: AUTOSAR_ECUC)
  - `CATEGORY_2` (来源: AUTOSAR_ECUC)
- **描述**: Specifies category of this ISR. If omitted the instance is related to a CATEGORY_2.

######### FUNCTION-NAME 类型参数

########## 1. ArtiOsIsrInstanceFunction

- **UUID**: `ECUC:b51c4f2f-7d97-43c6-b814-fbabc9b947e2`
- **参数名**: `ArtiOsIsrInstanceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This parameter represents the C function name of the ISR routine.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsIsrInstanceEcucRef

- **UUID**: `ECUC:a7cb30fd-600e-4211-82f2-76d752327527`
- **引用名**: `ArtiOsIsrInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsIsr`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsIsr`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the EcucDefs/Os/OsIsr of this ISR.

########## 2. ArtiOsIsrInstanceGenericComponentRef

- **UUID**: `ECUC:56825c6b-8d9e-4555-aa9e-69ba2106696d`
- **引用名**: `ArtiOsIsrInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an optional ArtiGenericComponentInstance that extends this OsIsr with additional parameters.

########## 3. ArtiOsIsrInstanceValidRef

- **UUID**: `ECUC:8811e977-25ce-48fb-812c-81c156cc4938`
- **引用名**: `ArtiOsIsrInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsIsrInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 9. ArtiOsMessageContainerClass

**容器属性**:

- **UUID**: `ECUC:4d3166b2-d2e4-4e7e-ae58-cd1384c1a2f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsMessageContainerClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "OsMessageContainer" object. The "OsMessageContainer" object represents an existing combination of OSEK messages.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsMessageContainerClassGenericComponentClassRef

- **UUID**: `ECUC:6fe9fd84-c9ee-4faf-acf0-343acd36dff4`
- **引用名**: `ArtiOsMessageContainerClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsMessageContainerClass.

####### 10. ArtiOsMessageContainerInstance

**容器属性**:

- **UUID**: `ECUC:f81ef7a5-b044-488d-b5a7-38d66d610d0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsMessageContainerInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an "ArtiMessageContainer" object.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. ArtiOsMessageContainerInstanceMsgName

- **UUID**: `ECUC:ef06dd09-9147-4da1-858b-d3c0afa53b97`
- **参数名**: `ArtiOsMessageContainerInstanceMsgName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute provides the name of the message as defined in OIL file.

########## 2. ArtiOsMessageContainerInstanceMsgType

- **UUID**: `ECUC:13ba9a9c-0504-42ab-bba0-f5bc39dd5394`
- **参数名**: `ArtiOsMessageContainerInstanceMsgType`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute provides the type of the message.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsMessageContainerInstanceFirstElementRef

- **UUID**: `ECUC:d02ae1ba-6675-4847-aa7a-4193bd0005df`
- **引用名**: `ArtiOsMessageContainerInstanceFirstElementRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "firstelement" of this "ArtiOsMessageContainer". This attribute provides the formula for evaluation of address of first valid message. This message will be received next. If no message is in the queue the value is zero.

########## 2. ArtiOsMessageContainerInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:eb32ba22-fa53-45fe-99c9-8b393d8e8cfb`
- **引用名**: `ArtiOsMessageContainerInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsMessageContainerInstance.

########## 3. ArtiOsMessageContainerInstanceQueueCountRef

- **UUID**: `ECUC:ac8e14b2-abd7-4bf9-8d75-89fe5589c91f`
- **引用名**: `ArtiOsMessageContainerInstanceQueueCountRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "queuecount" of this "ArtiOsMessageContainer". This attribute provides the number of valid messages in the queue and "1" for unqueued messages.

########## 4. ArtiOsMessageContainerInstanceQueueSizeRef

- **UUID**: `ECUC:bc49b697-3299-4765-8593-1ff592d5b695`
- **引用名**: `ArtiOsMessageContainerInstanceQueueSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "queuesize" of this "ArtiOsMessageContainer". This attribute provides the size of the queue for queued messages and "1" for unqueued messages.

########## 5. ArtiOsMessageContainerInstanceValidRef

- **UUID**: `ECUC:40b080ea-4be2-42a1-bfad-758b5f8ca676`
- **引用名**: `ArtiOsMessageContainerInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsMessageContainerInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 11. ArtiOsResourceClass

**容器属性**:

- **UUID**: `ECUC:20fdf1bf-55b0-40cd-9f86-a3f7e7212764`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsResourceClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ArtiOsResource object. The ArtiOsResource object represents an OSEK resource.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsResourceClassGenericComponentClassRef

- **UUID**: `ECUC:0e22238d-1295-43ee-9c9b-04147679330b`
- **引用名**: `ArtiOsResourceClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsResourceClass.

########## 2. ArtiOsResourceClassLockerRef

- **UUID**: `ECUC:a3ac7330-3cb9-47c6-b083-076103ab5762`
- **引用名**: `ArtiOsResourceClassLockerRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsResourceLockerRef in ArtiOsResourceInstances. This attribute indicates the locking ArtiOsTaskInstance or ArtiOsIsrInstance.

########## 3. ArtiOsResourceClassStateRef

- **UUID**: `ECUC:3a587256-3d4e-42dd-bdfd-6424edb739ce`
- **引用名**: `ArtiOsResourceClassStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsResourceStateRef in ArtiOsResourceInstances. This attribute represents the state of a resource ("LOCKED"/"UNLOCKED"). The ArtiObjectClassParameter does include the mapping from integer to human readable "LOCKED" or "UNLOCKED".

####### 12. ArtiOsResourceInstance

**容器属性**:

- **UUID**: `ECUC:335f2f7b-6bad-48f1-9923-1e77382b22f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsResourceInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an ArtiOsResource object.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiOsResourceInstancePriority

- **UUID**: `ECUC:9701fe64-1afd-4731-9d9a-5a76d7fd3812`
- **参数名**: `ArtiOsResourceInstancePriority`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute has two components that state: that the RESOURCE is used by TASKs only or by TASKs and ISRs, and the priority that will be used when locking the RESOURCE.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsResourceInstanceEcuCRef

- **UUID**: `ECUC:9870f0b8-92d8-465b-aff0-cbc3a736869b`
- **引用名**: `ArtiOsResourceInstanceEcuCRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an EcuC OsResource that is beeing extended.

########## 2. ArtiOsResourceInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:87a06716-22dd-4533-88a1-6ec4c15fe2fd`
- **引用名**: `ArtiOsResourceInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsResourceInstance.

########## 3. ArtiOsResourceInstanceLockerRef

- **UUID**: `ECUC:cd0c3100-679d-4814-ad76-cbcfa7e4d017`
- **引用名**: `ArtiOsResourceInstanceLockerRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "locker" of this ArtiOsResource.

########## 4. ArtiOsResourceInstanceStateRef

- **UUID**: `ECUC:a1bc17e6-735b-4885-acf3-3579cade827f`
- **引用名**: `ArtiOsResourceInstanceStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "state" of this ArtiOsResource.

########## 5. ArtiOsResourceInstanceValidRef

- **UUID**: `ECUC:69611519-6ebc-4a39-b6dd-f7ee915e568c`
- **引用名**: `ArtiOsResourceInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsResourceInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 13. ArtiOsStackClass

**容器属性**:

- **UUID**: `ECUC:d8126031-adca-4867-95d6-ba1adc5e86e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsStackClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ArtiOsStack object. The ArtiOsStack object defines the memory area of any stack in the system.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsStackClassGenericComponentClassRef

- **UUID**: `ECUC:8afcf99d-3900-488c-9d99-8d88885087a8`
- **引用名**: `ArtiOsStackClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsStackClass.

####### 14. ArtiOsStackInstance

**容器属性**:

- **UUID**: `ECUC:e719b4a1-b433-42d3-afe1-cf8273400432`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsStackInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an ArtiOsStack object.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiOsStackInstanceDirection

- **UUID**: `ECUC:8f64367d-6ec9-4d11-b1e4-a795bc5851fb`
- **参数名**: `ArtiOsStackInstanceDirection`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute specifies the direction of stack growth and may have either "UP" or "DOWN" as its value. UP means growing from lower to higher addresses. DOWN means growing from higher addresses to lower addresses.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsStackInstanceBaseAddressRef

- **UUID**: `ECUC:a8347439-fc5b-41db-bea9-b002016671e1`
- **引用名**: `ArtiOsStackInstanceBaseAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "baseaddress" of this ArtiOsStack. This attribute specifies the lowest address of stack memory area, regardless of the stack direction.

########## 2. ArtiOsStackInstanceFillPatternRef

- **UUID**: `ECUC:107bd51c-e8e4-49d7-ac81-ec768c92bbd8`
- **引用名**: `ArtiOsStackInstanceFillPatternRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "fillpattern" of this ArtiOsStack. If the operating system fills the stack during initialisation, this attribute specifies with which pattern the stack area is initialised. This allows the debugger to evaluate the maximum stack usage. For "stackdirection" "DOWN" the pattern starts at "baseaddress". For "stackdirection" "UP" the pattern starts at "baseaddress" + "size". If no pattern is used, this attribute must be omitted.

########## 3. ArtiOsStackInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:5a50e6bd-a0a8-49fc-8dad-89d8a95df83e`
- **引用名**: `ArtiOsStackInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsStackInstance.

########## 4. ArtiOsStackInstanceSizeRef

- **UUID**: `ECUC:16d3d24f-27c0-4d4e-8c8d-0937ca8809bd`
- **引用名**: `ArtiOsStackInstanceSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "size" of this ArtiOsStack. This attribute represents the size (in bytes) of the memory area allocated for stack.

########## 5. ArtiOsStackInstanceValidRef

- **UUID**: `ECUC:7e5eca33-79b5-4276-a09d-69ddbae8ce97`
- **引用名**: `ArtiOsStackInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsStackInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 15. ArtiOsTaskClass

**容器属性**:

- **UUID**: `ECUC:f4b3af52-d152-4341-a493-a38ae7d0a345`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsTaskClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "OsTask" object, extending the EcuC OsTask.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsTaskClassClassGenericComponentRef

- **UUID**: `ECUC:2f77be33-f281-452e-b63e-154d05e6fd72`
- **引用名**: `ArtiOsTaskClassClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the OsTask.

########## 2. ArtiOsTaskClassContextRef

- **UUID**: `ECUC:e907b038-bf11-420a-b91c-d059c913b741`
- **引用名**: `ArtiOsTaskClassContextRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: ArtiOsTaskContextRef in ArtiOsTaskInstances. This attribute contains a reference to the context object that the task is currently using.

########## 3. ArtiOsTaskClassCurrentTaskStateRef

- **UUID**: `ECUC:5799e97c-37d7-48ac-b75f-6d2f10212ead`
- **引用名**: `ArtiOsTaskClassCurrentTaskStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentTaskStateInstance parameter including the task state mapping.

########## 4. ArtiOsTaskClassPriorityRef

- **UUID**: `ECUC:3299a988-d752-41a8-8311-f39944d56ddb`
- **引用名**: `ArtiOsTaskClassPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsTaskPriorityRef in ArtiOsTaskInstances. This attribute represents the current priority of the TASK object. The current priority can be different from the static task priority as a result of priority ceiling protocol. The priority displayed is the priority as defined in the OsTask.

########## 5. ArtiOsTaskClassStackRef

- **UUID**: `ECUC:6c5b8e8d-143b-4d35-baaa-b2cce0139255`
- **引用名**: `ArtiOsTaskClassStackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsTaskStackRef in ArtiOsTaskInstances. This attribute contains a reference to the stack object that the task is currently using.

####### 16. ArtiOsTaskInstance

**容器属性**:

- **UUID**: `ECUC:485b0f61-3e65-4100-a507-b9e4a4c9cf25`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsTaskInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an ARTI "OsTask" object, extending the EcuC OsTask.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. ArtiOsTaskInstanceId

- **UUID**: `ECUC:9aa6d0d2-d65d-4dd9-9195-e423e1563d51`
- **参数名**: `ArtiOsTaskInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter represents the "TaskID" as given by the OSEK OS, returned by GetTaskID().

######### FUNCTION-NAME 类型参数

########## 1. ArtiOsTaskInstanceFunction

- **UUID**: `ECUC:23ae0f71-e011-4f9f-8f4d-86775ad81ef6`
- **参数名**: `ArtiOsTaskInstanceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This parameter represents the C function name of the task body.

######## 引用关系

此容器包含 **8** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsTaskInstanceContextRef

- **UUID**: `ECUC:50cebf51-c4ce-4d34-af35-236de78ee234`
- **引用名**: `ArtiOsTaskInstanceContextRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the ArtiOsContext of this ArtiOsTask.

########## 2. ArtiOsTaskInstanceCurrentActivationsRef

- **UUID**: `ECUC:3c32c481-c95b-460c-8a77-e43104ddf350`
- **引用名**: `ArtiOsTaskInstanceCurrentActivationsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current activations" of this task. This attribute specifies the number of current activations for the task.

########## 3. ArtiOsTaskInstanceCurrentTaskStateRef

- **UUID**: `ECUC:7141bb20-c512-4d20-b0c7-5df85a7f98fc`
- **引用名**: `ArtiOsTaskInstanceCurrentTaskStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current state" of this task.

########## 4. ArtiOsTaskInstanceEcucRef

- **UUID**: `ECUC:129f6697-aa8d-4ec0-a897-43cef1b128d0`
- **引用名**: `ArtiOsTaskInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OsTask.

########## 5. ArtiOsTaskInstanceGenericComponentRef

- **UUID**: `ECUC:badacb9d-24ec-4359-aa35-1099e50424ca`
- **引用名**: `ArtiOsTaskInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OsTask.

########## 6. ArtiOsTaskInstancePriorityRef

- **UUID**: `ECUC:b69c941d-9937-4b77-9bcb-11476eec7d70`
- **引用名**: `ArtiOsTaskInstancePriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "task priority" of this task.

########## 7. ArtiOsTaskInstanceStackRef

- **UUID**: `ECUC:0e5fbf19-1ecd-43b3-b363-2ef518815341`
- **引用名**: `ArtiOsTaskInstanceStackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the ArtiOsStack of this ArtiOsTask.

########## 8. ArtiOsTaskInstanceValidRef

- **UUID**: `ECUC:7fe49fd9-9de1-4d40-bf9a-10f20e334e71`
- **引用名**: `ArtiOsTaskInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsTaskInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 10. ArtiOsAlarmClass

**容器属性**:

- **UUID**: `ECUC:f6c8f934-40a8-495d-93c5-6d24cc11b848`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsAlarmClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ArtiOsAlarm object.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsAlarmClassGenericComponentClassRef

- **UUID**: `ECUC:2b159123-ec19-44d2-ab6a-cbfd521680c6`
- **引用名**: `ArtiOsAlarmClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsAlarmClass.

######## 2. ArtiOsAlarmClassStateRef

- **UUID**: `ECUC:7e2abcc9-b755-4a65-aeee-f0d5a13a6f40`
- **引用名**: `ArtiOsAlarmClassStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsAlarmStateRef in ArtiOsAlarmInstances. This attribute specifies if an alarm is "RUNNING" or "STOPPED". The refered ArtiObjectClassParameter does include the mapping from integer to human readable "RUNNING" or "STOPPED".

##### 11. ArtiOsAlarmInstance

**容器属性**:

- **UUID**: `ECUC:13b6673b-5924-488d-9efc-98f04702dbe8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsAlarmInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an ArtiOsAlarm object, extending the EcuC OsTaskAlarm.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. ArtiOsAlarmInstanceAction

- **UUID**: `ECUC:d8e08489-bab7-4efb-8629-c14919cb3f01`
- **参数名**: `ArtiOsAlarmInstanceAction`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute provides a string with a description of the action when the alarm expires, e.g. "ActivateTask TaskA".

######## 2. ArtiOsAlarmInstanceCounter

- **UUID**: `ECUC:756503f2-4eb8-461f-a079-355e4bb43368`
- **参数名**: `ArtiOsAlarmInstanceCounter`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute provides a string containing the name of the counter used by this alarm.

###### 引用关系

此容器包含 **6** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsAlarmInstanceAlarmTimeRef

- **UUID**: `ECUC:b4d33c37-865c-4c49-bf2c-dab6df3c1a6e`
- **引用名**: `ArtiOsAlarmInstanceAlarmTimeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute specifies how to evaluate the time until the alarm expires next. The time should be represented in seconds.

######## 2. ArtiOsAlarmInstanceCycleTimeRef

- **UUID**: `ECUC:35a98a28-b083-4c79-8201-8eafd004f9d6`
- **引用名**: `ArtiOsAlarmInstanceCycleTimeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: This attribute specifies how to evaluate the cycle time for cyclic alarms. The value of "cycle time" is 0 for non-cyclic alarms. The time should be represendet in seconds.

######## 3. ArtiOsAlarmInstanceEcuCRef

- **UUID**: `ECUC:aecb39a2-9cfe-4dac-bfaa-68d826543841`
- **引用名**: `ArtiOsAlarmInstanceEcuCRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an EcuC OsAlarm that is beeing extended.

######## 4. ArtiOsAlarmInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:f94ec3f7-dff7-4d78-b797-6453c58e0dc2`
- **引用名**: `ArtiOsAlarmInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsAlarmInstance.

######## 5. ArtiOsAlarmInstanceStateRef

- **UUID**: `ECUC:77eb375d-d579-4cc9-95d6-1e64b20b12f1`
- **引用名**: `ArtiOsAlarmInstanceStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "state" of this alarm. The result then is mapped with the typemap of the ArtiOsAlarmStateRef of the ArtiOsAlarmClass.

######## 6. ArtiOsAlarmInstanceValidRef

- **UUID**: `ECUC:42da2230-8e6d-4e3c-941e-d72effca8e94`
- **引用名**: `ArtiOsAlarmInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this alarm. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 12. ArtiOsClass

**容器属性**:

- **UUID**: `ECUC:407dd9b4-0454-4bbe-ba9f-030c9f6fe697`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "Os" object, extending the EcuC OsOS.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsClassAppModeRef

- **UUID**: `ECUC:2543c018-e93d-4d83-aab8-7060068d1d7e`
- **引用名**: `ArtiOsClassAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiOsAppModeInstance parameter.

######## 2. ArtiOsClassGenericComponentRef

- **UUID**: `ECUC:ca3a7994-71fa-421e-8d5b-31256ed3fbf1`
- **引用名**: `ArtiOsClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the OS description.

######## 3. ArtiOsClassServiceTraceRef

- **UUID**: `ECUC:d3c5dce4-6661-423d-8541-760e8bde9e2f`
- **引用名**: `ArtiOsClassServiceTraceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiOsInstanceServiceTrace parameter. This attribute indicates the entry or exit of a service routine and the ID of this service routine. The value of this attribute must be evaluated from one single memory location.

##### 13. ArtiOsContextClass

**容器属性**:

- **UUID**: `ECUC:c370f4c9-6f6e-462a-bddb-624db0aa9a96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsContextClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "OsContext" object.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsContextClassGenericComponentClassRef

- **UUID**: `ECUC:d5d77649-562c-43ef-82f9-dfbc705cd081`
- **引用名**: `ArtiOsContextClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsContextClass.

##### 14. ArtiOsContextInstance

**容器属性**:

- **UUID**: `ECUC:73757e1e-6f5f-40e6-a447-edaf12ca137b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsContextInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an "ArtiContext" object.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsContextInstanceAddressRef

- **UUID**: `ECUC:d498eb59-23b7-480c-a18a-6ed6bebbba53`
- **引用名**: `ArtiOsContextInstanceAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "address" of this context.

######## 2. ArtiOsContextInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:7c03b1d4-5acd-49ed-b6fc-7330ececd934`
- **引用名**: `ArtiOsContextInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsContext.

######## 3. ArtiOsContextInstanceSizeRef

- **UUID**: `ECUC:7b80e64e-c91b-473c-b0e1-84b7f39e9856`
- **引用名**: `ArtiOsContextInstanceSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "size" of this context.

######## 4. ArtiOsContextInstanceValidRef

- **UUID**: `ECUC:f7f426f2-9b3f-4ea7-b0de-fc742bf533ab`
- **引用名**: `ArtiOsContextInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this context. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 15. ArtiOsInstance

**容器属性**:

- **UUID**: `ECUC:696083fb-4846-4ead-8267-2b601f9fb8bb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsInstance`
- **多重性**: [0..1]

**容器描述**:

Represents an instance of an ARTI "Os" object, extending the EcuC OsOS.

###### 引用关系

此容器包含 **6** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsInstanceAppModeRef

- **UUID**: `ECUC:27d75b37-1075-4ec5-98d1-0cf7f925d12e`
- **引用名**: `ArtiOsInstanceAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "application mode" of this OS.

######## 2. ArtiOsInstanceEcucRef

- **UUID**: `ECUC:4ccdcb25-b09f-4f50-ab64-22122367b124`
- **引用名**: `ArtiOsInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsOS`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsOS`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the EcucDefs/Os/OsOS of this OS.

######## 3. ArtiOsInstanceGenericComponentRef

- **UUID**: `ECUC:837582c4-d78d-4071-ba04-14148708b906`
- **引用名**: `ArtiOsInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OS.

######## 4. ArtiOsInstanceHookRef

- **UUID**: `ECUC:9f2b7d96-7a32-4cc3-8306-b087284e5c02`
- **引用名**: `ArtiOsInstanceHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiHook`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiHook`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a hook defined in the OS.

######## 5. ArtiOsInstanceServiceTraceRef

- **UUID**: `ECUC:ceddfdcc-f46a-4e85-bcc9-4c7dea5e2d53`
- **引用名**: `ArtiOsInstanceServiceTraceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a hook defined in the OS.

######## 6. ArtiOsInstanceValidRef

- **UUID**: `ECUC:a4d1f2b2-15c2-4efa-87a7-644b1d225bcb`
- **引用名**: `ArtiOsInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 16. ArtiOsIsrClass

**容器属性**:

- **UUID**: `ECUC:335c0140-9ebc-400a-a7b3-c6cdb56169f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsIsrClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "OsIsr" object, extending the EcuC OsIsr.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsIsrClassGenericComponentRef

- **UUID**: `ECUC:2fca94bd-d5ab-41f2-84ed-b2e2ebde6663`
- **引用名**: `ArtiOsIsrClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an optional ArtiGenericComponentClass that extends the OsIsr with additional parameters.

##### 17. ArtiOsIsrInstance

**容器属性**:

- **UUID**: `ECUC:b057462e-ba05-482e-b4d1-bb784a65325c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsIsrInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an ARTI "OsIsr" object, extending the EcuC OsIsr.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. ArtiOsIsrInstanceId

- **UUID**: `ECUC:e319855a-e1db-4299-82f8-80a0376604d4`
- **参数名**: `ArtiOsIsrInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter represents the "ISRID" as given by the OS, returned by GetISRID().

####### ENUMERATION 类型参数

######## 1. ArtiOsIsrInstanceCategory

- **UUID**: `ECUC:a6bc034f-8b89-4c91-aeb3-77294bb27f90`
- **参数名**: `ArtiOsIsrInstanceCategory`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CATEGORY_1` (来源: AUTOSAR_ECUC)
  - `CATEGORY_2` (来源: AUTOSAR_ECUC)
- **描述**: Specifies category of this ISR. If omitted the instance is related to a CATEGORY_2.

####### FUNCTION-NAME 类型参数

######## 1. ArtiOsIsrInstanceFunction

- **UUID**: `ECUC:b51c4f2f-7d97-43c6-b814-fbabc9b947e2`
- **参数名**: `ArtiOsIsrInstanceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This parameter represents the C function name of the ISR routine.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsIsrInstanceEcucRef

- **UUID**: `ECUC:a7cb30fd-600e-4211-82f2-76d752327527`
- **引用名**: `ArtiOsIsrInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsIsr`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsIsr`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the EcucDefs/Os/OsIsr of this ISR.

######## 2. ArtiOsIsrInstanceGenericComponentRef

- **UUID**: `ECUC:56825c6b-8d9e-4555-aa9e-69ba2106696d`
- **引用名**: `ArtiOsIsrInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an optional ArtiGenericComponentInstance that extends this OsIsr with additional parameters.

######## 3. ArtiOsIsrInstanceValidRef

- **UUID**: `ECUC:8811e977-25ce-48fb-812c-81c156cc4938`
- **引用名**: `ArtiOsIsrInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsIsrInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 18. ArtiOsMessageContainerClass

**容器属性**:

- **UUID**: `ECUC:4d3166b2-d2e4-4e7e-ae58-cd1384c1a2f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsMessageContainerClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "OsMessageContainer" object. The "OsMessageContainer" object represents an existing combination of OSEK messages.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsMessageContainerClassGenericComponentClassRef

- **UUID**: `ECUC:6fe9fd84-c9ee-4faf-acf0-343acd36dff4`
- **引用名**: `ArtiOsMessageContainerClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsMessageContainerClass.

##### 19. ArtiOsMessageContainerInstance

**容器属性**:

- **UUID**: `ECUC:f81ef7a5-b044-488d-b5a7-38d66d610d0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsMessageContainerInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an "ArtiMessageContainer" object.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. ArtiOsMessageContainerInstanceMsgName

- **UUID**: `ECUC:ef06dd09-9147-4da1-858b-d3c0afa53b97`
- **参数名**: `ArtiOsMessageContainerInstanceMsgName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute provides the name of the message as defined in OIL file.

######## 2. ArtiOsMessageContainerInstanceMsgType

- **UUID**: `ECUC:13ba9a9c-0504-42ab-bba0-f5bc39dd5394`
- **参数名**: `ArtiOsMessageContainerInstanceMsgType`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute provides the type of the message.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsMessageContainerInstanceFirstElementRef

- **UUID**: `ECUC:d02ae1ba-6675-4847-aa7a-4193bd0005df`
- **引用名**: `ArtiOsMessageContainerInstanceFirstElementRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "firstelement" of this "ArtiOsMessageContainer". This attribute provides the formula for evaluation of address of first valid message. This message will be received next. If no message is in the queue the value is zero.

######## 2. ArtiOsMessageContainerInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:eb32ba22-fa53-45fe-99c9-8b393d8e8cfb`
- **引用名**: `ArtiOsMessageContainerInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsMessageContainerInstance.

######## 3. ArtiOsMessageContainerInstanceQueueCountRef

- **UUID**: `ECUC:ac8e14b2-abd7-4bf9-8d75-89fe5589c91f`
- **引用名**: `ArtiOsMessageContainerInstanceQueueCountRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "queuecount" of this "ArtiOsMessageContainer". This attribute provides the number of valid messages in the queue and "1" for unqueued messages.

######## 4. ArtiOsMessageContainerInstanceQueueSizeRef

- **UUID**: `ECUC:bc49b697-3299-4765-8593-1ff592d5b695`
- **引用名**: `ArtiOsMessageContainerInstanceQueueSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "queuesize" of this "ArtiOsMessageContainer". This attribute provides the size of the queue for queued messages and "1" for unqueued messages.

######## 5. ArtiOsMessageContainerInstanceValidRef

- **UUID**: `ECUC:40b080ea-4be2-42a1-bfad-758b5f8ca676`
- **引用名**: `ArtiOsMessageContainerInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsMessageContainerInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 20. ArtiOsResourceClass

**容器属性**:

- **UUID**: `ECUC:20fdf1bf-55b0-40cd-9f86-a3f7e7212764`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsResourceClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ArtiOsResource object. The ArtiOsResource object represents an OSEK resource.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsResourceClassGenericComponentClassRef

- **UUID**: `ECUC:0e22238d-1295-43ee-9c9b-04147679330b`
- **引用名**: `ArtiOsResourceClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsResourceClass.

######## 2. ArtiOsResourceClassLockerRef

- **UUID**: `ECUC:a3ac7330-3cb9-47c6-b083-076103ab5762`
- **引用名**: `ArtiOsResourceClassLockerRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsResourceLockerRef in ArtiOsResourceInstances. This attribute indicates the locking ArtiOsTaskInstance or ArtiOsIsrInstance.

######## 3. ArtiOsResourceClassStateRef

- **UUID**: `ECUC:3a587256-3d4e-42dd-bdfd-6424edb739ce`
- **引用名**: `ArtiOsResourceClassStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsResourceStateRef in ArtiOsResourceInstances. This attribute represents the state of a resource ("LOCKED"/"UNLOCKED"). The ArtiObjectClassParameter does include the mapping from integer to human readable "LOCKED" or "UNLOCKED".

##### 21. ArtiOsResourceInstance

**容器属性**:

- **UUID**: `ECUC:335f2f7b-6bad-48f1-9923-1e77382b22f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsResourceInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an ArtiOsResource object.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiOsResourceInstancePriority

- **UUID**: `ECUC:9701fe64-1afd-4731-9d9a-5a76d7fd3812`
- **参数名**: `ArtiOsResourceInstancePriority`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute has two components that state: that the RESOURCE is used by TASKs only or by TASKs and ISRs, and the priority that will be used when locking the RESOURCE.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsResourceInstanceEcuCRef

- **UUID**: `ECUC:9870f0b8-92d8-465b-aff0-cbc3a736869b`
- **引用名**: `ArtiOsResourceInstanceEcuCRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an EcuC OsResource that is beeing extended.

######## 2. ArtiOsResourceInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:87a06716-22dd-4533-88a1-6ec4c15fe2fd`
- **引用名**: `ArtiOsResourceInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsResourceInstance.

######## 3. ArtiOsResourceInstanceLockerRef

- **UUID**: `ECUC:cd0c3100-679d-4814-ad76-cbcfa7e4d017`
- **引用名**: `ArtiOsResourceInstanceLockerRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "locker" of this ArtiOsResource.

######## 4. ArtiOsResourceInstanceStateRef

- **UUID**: `ECUC:a1bc17e6-735b-4885-acf3-3579cade827f`
- **引用名**: `ArtiOsResourceInstanceStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "state" of this ArtiOsResource.

######## 5. ArtiOsResourceInstanceValidRef

- **UUID**: `ECUC:69611519-6ebc-4a39-b6dd-f7ee915e568c`
- **引用名**: `ArtiOsResourceInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsResourceInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 22. ArtiOsStackClass

**容器属性**:

- **UUID**: `ECUC:d8126031-adca-4867-95d6-ba1adc5e86e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsStackClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ArtiOsStack object. The ArtiOsStack object defines the memory area of any stack in the system.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsStackClassGenericComponentClassRef

- **UUID**: `ECUC:8afcf99d-3900-488c-9d99-8d88885087a8`
- **引用名**: `ArtiOsStackClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsStackClass.

##### 23. ArtiOsStackInstance

**容器属性**:

- **UUID**: `ECUC:e719b4a1-b433-42d3-afe1-cf8273400432`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsStackInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an ArtiOsStack object.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiOsStackInstanceDirection

- **UUID**: `ECUC:8f64367d-6ec9-4d11-b1e4-a795bc5851fb`
- **参数名**: `ArtiOsStackInstanceDirection`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This attribute specifies the direction of stack growth and may have either "UP" or "DOWN" as its value. UP means growing from lower to higher addresses. DOWN means growing from higher addresses to lower addresses.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsStackInstanceBaseAddressRef

- **UUID**: `ECUC:a8347439-fc5b-41db-bea9-b002016671e1`
- **引用名**: `ArtiOsStackInstanceBaseAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "baseaddress" of this ArtiOsStack. This attribute specifies the lowest address of stack memory area, regardless of the stack direction.

######## 2. ArtiOsStackInstanceFillPatternRef

- **UUID**: `ECUC:107bd51c-e8e4-49d7-ac81-ec768c92bbd8`
- **引用名**: `ArtiOsStackInstanceFillPatternRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "fillpattern" of this ArtiOsStack. If the operating system fills the stack during initialisation, this attribute specifies with which pattern the stack area is initialised. This allows the debugger to evaluate the maximum stack usage. For "stackdirection" "DOWN" the pattern starts at "baseaddress". For "stackdirection" "UP" the pattern starts at "baseaddress" + "size". If no pattern is used, this attribute must be omitted.

######## 3. ArtiOsStackInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:5a50e6bd-a0a8-49fc-8dad-89d8a95df83e`
- **引用名**: `ArtiOsStackInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsStackInstance.

######## 4. ArtiOsStackInstanceSizeRef

- **UUID**: `ECUC:16d3d24f-27c0-4d4e-8c8d-0937ca8809bd`
- **引用名**: `ArtiOsStackInstanceSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "size" of this ArtiOsStack. This attribute represents the size (in bytes) of the memory area allocated for stack.

######## 5. ArtiOsStackInstanceValidRef

- **UUID**: `ECUC:7e5eca33-79b5-4276-a09d-69ddbae8ce97`
- **引用名**: `ArtiOsStackInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsStackInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 24. ArtiOsTaskClass

**容器属性**:

- **UUID**: `ECUC:f4b3af52-d152-4341-a493-a38ae7d0a345`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsTaskClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ARTI "OsTask" object, extending the EcuC OsTask.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsTaskClassClassGenericComponentRef

- **UUID**: `ECUC:2f77be33-f281-452e-b63e-154d05e6fd72`
- **引用名**: `ArtiOsTaskClassClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the OsTask.

######## 2. ArtiOsTaskClassContextRef

- **UUID**: `ECUC:e907b038-bf11-420a-b91c-d059c913b741`
- **引用名**: `ArtiOsTaskClassContextRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: ArtiOsTaskContextRef in ArtiOsTaskInstances. This attribute contains a reference to the context object that the task is currently using.

######## 3. ArtiOsTaskClassCurrentTaskStateRef

- **UUID**: `ECUC:5799e97c-37d7-48ac-b75f-6d2f10212ead`
- **引用名**: `ArtiOsTaskClassCurrentTaskStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentTaskStateInstance parameter including the task state mapping.

######## 4. ArtiOsTaskClassPriorityRef

- **UUID**: `ECUC:3299a988-d752-41a8-8311-f39944d56ddb`
- **引用名**: `ArtiOsTaskClassPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsTaskPriorityRef in ArtiOsTaskInstances. This attribute represents the current priority of the TASK object. The current priority can be different from the static task priority as a result of priority ceiling protocol. The priority displayed is the priority as defined in the OsTask.

######## 5. ArtiOsTaskClassStackRef

- **UUID**: `ECUC:6c5b8e8d-143b-4d35-baaa-b2cce0139255`
- **引用名**: `ArtiOsTaskClassStackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsTaskStackRef in ArtiOsTaskInstances. This attribute contains a reference to the stack object that the task is currently using.

##### 25. ArtiOsTaskInstance

**容器属性**:

- **UUID**: `ECUC:485b0f61-3e65-4100-a507-b9e4a4c9cf25`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsTaskInstance`
- **多重性**: [0..infinite]

**容器描述**:

Represents an instance of an ARTI "OsTask" object, extending the EcuC OsTask.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. ArtiOsTaskInstanceId

- **UUID**: `ECUC:9aa6d0d2-d65d-4dd9-9195-e423e1563d51`
- **参数名**: `ArtiOsTaskInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter represents the "TaskID" as given by the OSEK OS, returned by GetTaskID().

####### FUNCTION-NAME 类型参数

######## 1. ArtiOsTaskInstanceFunction

- **UUID**: `ECUC:23ae0f71-e011-4f9f-8f4d-86775ad81ef6`
- **参数名**: `ArtiOsTaskInstanceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This parameter represents the C function name of the task body.

###### 引用关系

此容器包含 **8** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsTaskInstanceContextRef

- **UUID**: `ECUC:50cebf51-c4ce-4d34-af35-236de78ee234`
- **引用名**: `ArtiOsTaskInstanceContextRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the ArtiOsContext of this ArtiOsTask.

######## 2. ArtiOsTaskInstanceCurrentActivationsRef

- **UUID**: `ECUC:3c32c481-c95b-460c-8a77-e43104ddf350`
- **引用名**: `ArtiOsTaskInstanceCurrentActivationsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current activations" of this task. This attribute specifies the number of current activations for the task.

######## 3. ArtiOsTaskInstanceCurrentTaskStateRef

- **UUID**: `ECUC:7141bb20-c512-4d20-b0c7-5df85a7f98fc`
- **引用名**: `ArtiOsTaskInstanceCurrentTaskStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current state" of this task.

######## 4. ArtiOsTaskInstanceEcucRef

- **UUID**: `ECUC:129f6697-aa8d-4ec0-a897-43cef1b128d0`
- **引用名**: `ArtiOsTaskInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OsTask.

######## 5. ArtiOsTaskInstanceGenericComponentRef

- **UUID**: `ECUC:badacb9d-24ec-4359-aa35-1099e50424ca`
- **引用名**: `ArtiOsTaskInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OsTask.

######## 6. ArtiOsTaskInstancePriorityRef

- **UUID**: `ECUC:b69c941d-9937-4b77-9bcb-11476eec7d70`
- **引用名**: `ArtiOsTaskInstancePriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "task priority" of this task.

######## 7. ArtiOsTaskInstanceStackRef

- **UUID**: `ECUC:0e5fbf19-1ecd-43b3-b363-2ef518815341`
- **引用名**: `ArtiOsTaskInstanceStackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the ArtiOsStack of this ArtiOsTask.

######## 8. ArtiOsTaskInstanceValidRef

- **UUID**: `ECUC:7fe49fd9-9de1-4d40-bf9a-10f20e334e71`
- **引用名**: `ArtiOsTaskInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsTaskInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 26. ArtiRte

**容器属性**:

- **UUID**: `ECUC:46efdcc8-4930-43da-bee1-cd957abebf33`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRte`
- **多重性**: [0..1]

**容器描述**:

The ArtiRte Container contains all parameters for ARTI that are filled by the generators RTE.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiRteHookRef

- **UUID**: `ECUC:c78c2157-32e4-46c1-abcf-cd848657aa15`
- **引用名**: `ArtiRteHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiHook`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiHook`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an arti hook which is called by the RTE.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. ArtiRteRunnableClass

**容器属性**:

- **UUID**: `ECUC:0a3434b9-48dc-4401-a0bc-b8293b8edbdd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteRunnableClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ArtiRteRunnable object.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiRteRunnableClassGenericComponentClassRef

- **UUID**: `ECUC:ece2ff41-0954-457e-b67b-c9322f6a044f`
- **引用名**: `ArtiRteRunnableClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiRteRunnableClass.

########## 2. ArtiRteRunnableIdRef

- **UUID**: `ECUC:0dea5fbb-c2d4-41f0-88fc-39ecbc5acc1b`
- **引用名**: `ArtiRteRunnableIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiRteRunnableIdRef in ArtiRteRunnableEntityInstances. This attribute specifies the idOf(reName) mapping.

####### 2. ArtiRteRunnableInstance

**容器属性**:

- **UUID**: `ECUC:bfbd97db-1e8f-46bd-be04-dcf5c5b37d6c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteRunnableInstance`
- **多重性**: [0..1]

**容器描述**:

Represents an instance of an ArtiRteRunnable object, extending the BswM RunnableEntity.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiRteRunnableInstanceSymbol

- **UUID**: `ECUC:02f89655-649b-4366-86e1-23662b53210c`
- **参数名**: `ArtiRteRunnableInstanceSymbol`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Specifies the symbol / function name that implements the runnable.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiRteRunnableInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:66eff002-6121-4a11-aaa6-a575dc82f37e`
- **引用名**: `ArtiRteRunnableInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiRteRunnableInstance.

######### FOREIGN-REFERENCE 类型引用

########## 1. ArtiRteRunnableInstanceBswRef

- **UUID**: `ECUC:d90e068d-0f9e-46eb-b1ab-8eac60e5bc55`
- **引用名**: `ArtiRteRunnableInstanceBswRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: RUNNABLE-ENTITY
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an Rte Runnable that is beeing extended.

####### 3. ArtiRteSchedulableClass

**容器属性**:

- **UUID**: `ECUC:ea200fed-5ef4-48a7-953b-ba2359f9217c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteSchedulableClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ArtiRteSchedulable object.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiRteSchedulableClassGenericComponentClassRef

- **UUID**: `ECUC:bd6d4955-4116-4194-bb66-831a6ef371d8`
- **引用名**: `ArtiRteSchedulableClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiRteSchedulableClass.

########## 2. ArtiRteSchedulableIdRef

- **UUID**: `ECUC:e1f9c8ec-8066-4c11-b51f-41c3dbea2f9d`
- **引用名**: `ArtiRteSchedulableIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiRteSchmEntityIdRef in ArtiRteSchedulableInstances. This attribute specifies the idOf(entityName) mapping.

####### 4. ArtiRteSchedulableInstance

**容器属性**:

- **UUID**: `ECUC:17e891ee-aadb-4f70-9599-fd1c0cd41da5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteSchedulableInstance`
- **多重性**: [0..1]

**容器描述**:

Represents an instance of an ArtiRteSchedulable object, extending the Rte Schedulable Entity.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiRteSchedulableInstanceSymbol

- **UUID**: `ECUC:6661ae2c-5a54-47b6-ad13-58eb4db1330e`
- **参数名**: `ArtiRteSchedulableInstanceSymbol`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Specifies the symbol / function name that implements the schedulable.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiRteSchedulableInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:157afd43-fcbb-44a8-9b64-7da8ae411fd7`
- **引用名**: `ArtiRteSchedulableInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiRteSchedulableInstance.

######### FOREIGN-REFERENCE 类型引用

########## 1. ArtiRteSchedulableInstanceBswRef

- **UUID**: `ECUC:91e56d6f-d29b-4e0b-8ccf-3904c0baa9c7`
- **引用名**: `ArtiRteSchedulableInstanceBswRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-SCHEDULABLE-ENITIY
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an Rte Schedulable that is beeing extended.

##### 27. ArtiRteRunnableClass

**容器属性**:

- **UUID**: `ECUC:0a3434b9-48dc-4401-a0bc-b8293b8edbdd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteRunnableClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ArtiRteRunnable object.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiRteRunnableClassGenericComponentClassRef

- **UUID**: `ECUC:ece2ff41-0954-457e-b67b-c9322f6a044f`
- **引用名**: `ArtiRteRunnableClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiRteRunnableClass.

######## 2. ArtiRteRunnableIdRef

- **UUID**: `ECUC:0dea5fbb-c2d4-41f0-88fc-39ecbc5acc1b`
- **引用名**: `ArtiRteRunnableIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiRteRunnableIdRef in ArtiRteRunnableEntityInstances. This attribute specifies the idOf(reName) mapping.

##### 28. ArtiRteRunnableInstance

**容器属性**:

- **UUID**: `ECUC:bfbd97db-1e8f-46bd-be04-dcf5c5b37d6c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteRunnableInstance`
- **多重性**: [0..1]

**容器描述**:

Represents an instance of an ArtiRteRunnable object, extending the BswM RunnableEntity.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiRteRunnableInstanceSymbol

- **UUID**: `ECUC:02f89655-649b-4366-86e1-23662b53210c`
- **参数名**: `ArtiRteRunnableInstanceSymbol`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Specifies the symbol / function name that implements the runnable.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiRteRunnableInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:66eff002-6121-4a11-aaa6-a575dc82f37e`
- **引用名**: `ArtiRteRunnableInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiRteRunnableInstance.

####### FOREIGN-REFERENCE 类型引用

######## 1. ArtiRteRunnableInstanceBswRef

- **UUID**: `ECUC:d90e068d-0f9e-46eb-b1ab-8eac60e5bc55`
- **引用名**: `ArtiRteRunnableInstanceBswRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: RUNNABLE-ENTITY
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an Rte Runnable that is beeing extended.

##### 29. ArtiRteSchedulableClass

**容器属性**:

- **UUID**: `ECUC:ea200fed-5ef4-48a7-953b-ba2359f9217c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteSchedulableClass`
- **多重性**: [0..1]

**容器描述**:

Contains the layout of an ArtiRteSchedulable object.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiRteSchedulableClassGenericComponentClassRef

- **UUID**: `ECUC:bd6d4955-4116-4194-bb66-831a6ef371d8`
- **引用名**: `ArtiRteSchedulableClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiRteSchedulableClass.

######## 2. ArtiRteSchedulableIdRef

- **UUID**: `ECUC:e1f9c8ec-8066-4c11-b51f-41c3dbea2f9d`
- **引用名**: `ArtiRteSchedulableIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiObjectClassParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiRteSchmEntityIdRef in ArtiRteSchedulableInstances. This attribute specifies the idOf(entityName) mapping.

##### 30. ArtiRteSchedulableInstance

**容器属性**:

- **UUID**: `ECUC:17e891ee-aadb-4f70-9599-fd1c0cd41da5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteSchedulableInstance`
- **多重性**: [0..1]

**容器描述**:

Represents an instance of an ArtiRteSchedulable object, extending the Rte Schedulable Entity.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiRteSchedulableInstanceSymbol

- **UUID**: `ECUC:6661ae2c-5a54-47b6-ad13-58eb4db1330e`
- **参数名**: `ArtiRteSchedulableInstanceSymbol`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Specifies the symbol / function name that implements the schedulable.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiRteSchedulableInstanceGenericComponentInstanceRef

- **UUID**: `ECUC:157afd43-fcbb-44a8-9b64-7da8ae411fd7`
- **引用名**: `ArtiRteSchedulableInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiRteSchedulableInstance.

####### FOREIGN-REFERENCE 类型引用

######## 1. ArtiRteSchedulableInstanceBswRef

- **UUID**: `ECUC:91e56d6f-d29b-4e0b-8ccf-3904c0baa9c7`
- **引用名**: `ArtiRteSchedulableInstanceBswRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-SCHEDULABLE-ENITIY
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an Rte Schedulable that is beeing extended.

##### 31. ArtiValues

**容器属性**:

- **UUID**: `ECUC:23abaaea-04ea-4349-8305-0ad31e31794e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiValues`
- **多重性**: [0..infinite]

**容器描述**:

The ArtiValues container collects all parameter values for ARTI that are filled by the generators (OS, RTE, ...)

###### 配置容器

本模块包含 **9** 个配置容器：

####### 1. ArtiConstant

**容器属性**:

- **UUID**: `ECUC:c161abde-e451-46ea-8dba-d7db465845ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiConstant`
- **多重性**: [0..infinite]

**容器描述**:

This container holds a constant value.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiConstantString

- **UUID**: `ECUC:0a007e52-6426-4b2d-80fb-3e05379d598f`
- **参数名**: `ArtiConstantString`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This is the constant value for a specific parameter.

####### 2. ArtiExpression

**容器属性**:

- **UUID**: `ECUC:cc7289be-08d8-4286-91af-79259f674241`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiExpression`
- **多重性**: [0..infinite]

**容器描述**:

This container holds a C like expression that a debugger can evaluate. This is similar to what is already done in ORTI.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiExpressionString

- **UUID**: `ECUC:dfcfe0ed-0e16-4049-969b-78a5d40b4491`
- **参数名**: `ArtiExpressionString`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This string represents a C like expression that a debugger can evaluate.

####### 3. ArtiHook

**容器属性**:

- **UUID**: `ECUC:81392ce4-93b8-4934-b9fe-7f01dcc2da72`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHook`
- **多重性**: [0..infinite]

**容器描述**:

This container represents an ARTI hook that is present in the module.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. ArtiHookClass

- **UUID**: `ECUC:00a1fa88-924d-4a55-8215-5a48f98ba9c1`
- **参数名**: `ArtiHookClass`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the (schedule) class of macros. Classes can be one of the predefined classes or user defined.

########## 2. ArtiHookContext

- **UUID**: `ECUC:7a8eb1a0-da8c-4914-8cc9-a560b8a6643a`
- **参数名**: `ArtiHookContext`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the execution context. One of NOSUSP, SPRVSR, or USER.

########## 3. ArtiHookEventName

- **UUID**: `ECUC:ec285046-62b2-4145-ae17-79253c2fe836`
- **参数名**: `ArtiHookEventName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: The name of the event as defined for a particular class, or an arbitrary name for generic classes.

########## 4. ArtiHookInstance

- **UUID**: `ECUC:cb5240f2-7b27-42ab-b327-42a3902e03fb`
- **参数名**: `ArtiHookInstance`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of an instance of the (schedule) class.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiHookEventParameterTypeRef

- **UUID**: `ECUC:d22b8331-8951-49cb-96a3-3bbc2560d20e`
- **引用名**: `ArtiHookEventParameterTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiParameterTypeMap`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a parameter type to interpret the hook event number.

########## 2. ArtiHookInstanceParameterTypeRef

- **UUID**: `ECUC:4df421d6-b105-4baf-9768-ee004ef81c6e`
- **引用名**: `ArtiHookInstanceParameterTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiParameterTypeMap`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a parameter type to interpret the hook instance number.

####### 4. ArtiObjectClassParameter

**容器属性**:

- **UUID**: `ECUC:1c08a76b-96f1-4c04-abf7-5415edcb7bbb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiObjectClassParameter`
- **多重性**: [0..infinite]

**容器描述**:

This container represents a parameter of an Arti object class definition.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiObjectClassParameterTypeMapRef

- **UUID**: `ECUC:c715d81a-354a-4048-8aef-a286b8082e74`
- **引用名**: `ArtiObjectClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiParameterTypeMap`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a parameter type to interpret the instance parameter value.

####### 5. ArtiObjectInstanceParameter

**容器属性**:

- **UUID**: `ECUC:6575b287-9552-4ee7-8014-9d0b93ba9acb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiObjectInstanceParameter`
- **多重性**: [0..infinite]

**容器描述**:

This container represents a parameter of an Arti object instance.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiObjectInstanceParameterConstantRef

- **UUID**: `ECUC:47fc42b3-bf66-4fe3-9ff5-bec32cc927a5`
- **引用名**: `ArtiObjectInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiConstant`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a constant representing the value of this parameter.

########## 2. ArtiObjectInstanceParameterExpressionRef

- **UUID**: `ECUC:b19c6494-e2d8-427d-872d-ef02f4cc11b3`
- **引用名**: `ArtiObjectInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiExpression`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an expression that evaluates the value of this parameter.

########## 3. ArtiObjectInstanceParameterHookRef

- **UUID**: `ECUC:dbbd7880-78a6-4814-9702-0c1f420f4333`
- **引用名**: `ArtiObjectInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiHook`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a hook that records this parameter.

####### 6. ArtiParameterTypeMap

**容器属性**:

- **UUID**: `ECUC:522ccfe6-c7f4-400d-8817-54f1041e9fad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMap`
- **多重性**: [0..infinite]

**容器描述**:

A map of key/value pairs to map a parameter value to a display string and/or an Arti or EcuC object.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ArtiParameterTypeMapPair

**容器属性**:

- **UUID**: `ECUC:b141b4df-cead-4a92-aac5-ec2ecf7ec3f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMapPair`
- **多重性**: [1..infinite]

**容器描述**:

A key/value pair to map a parameter value to a display string and/or an Arti or EcuC object.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. ArtiParameterTypeMapPairInput

- **UUID**: `ECUC:83031463-4053-4dbb-bfaf-237015e31ced`
- **参数名**: `ArtiParameterTypeMapPairInput`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The numerical value given by a parameter to translate.

########### STRING 类型参数

############ 1. ArtiParameterTypeMapPairOutput

- **UUID**: `ECUC:0bc154c3-6242-45b2-beee-247d35a47561`
- **参数名**: `ArtiParameterTypeMapPairOutput`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: The string to display for the Input value.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. ArtiParameterTypeMapPairInputExpressionRef

- **UUID**: `ECUC:21ef4ed0-1c9f-4534-bc7c-f3ab3266efe1`
- **引用名**: `ArtiParameterTypeMapPairInputExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiExpression`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an expression that evaluates to a numerical value to translate.

########### CHOICE-REFERENCE 类型引用

############ 1. ArtiParameterTypeMapPairOutputRef

- **UUID**: `ECUC:17fa6f71-ca96-4719-b1e6-d19ab7d61747`
- **引用名**: `ArtiParameterTypeMapPairOutputRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsContextInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsIsrInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsStackInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsTaskInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiStates/ArtiStatesTaskState`
  - `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **描述**: Choice Reference to ArtiOsTaskInstance, ArtiOsIsrInstance, ArtiStatesTaskState, OsAppMode, ArtiOsContextInstance, or ArtiOsStackInstance.

####### 7. ArtiParameterTypeMapPair

**容器属性**:

- **UUID**: `ECUC:b141b4df-cead-4a92-aac5-ec2ecf7ec3f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMapPair`
- **多重性**: [1..infinite]

**容器描述**:

A key/value pair to map a parameter value to a display string and/or an Arti or EcuC object.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. ArtiParameterTypeMapPairInput

- **UUID**: `ECUC:83031463-4053-4dbb-bfaf-237015e31ced`
- **参数名**: `ArtiParameterTypeMapPairInput`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The numerical value given by a parameter to translate.

######### STRING 类型参数

########## 1. ArtiParameterTypeMapPairOutput

- **UUID**: `ECUC:0bc154c3-6242-45b2-beee-247d35a47561`
- **参数名**: `ArtiParameterTypeMapPairOutput`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: The string to display for the Input value.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiParameterTypeMapPairInputExpressionRef

- **UUID**: `ECUC:21ef4ed0-1c9f-4534-bc7c-f3ab3266efe1`
- **引用名**: `ArtiParameterTypeMapPairInputExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiExpression`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an expression that evaluates to a numerical value to translate.

######### CHOICE-REFERENCE 类型引用

########## 1. ArtiParameterTypeMapPairOutputRef

- **UUID**: `ECUC:17fa6f71-ca96-4719-b1e6-d19ab7d61747`
- **引用名**: `ArtiParameterTypeMapPairOutputRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsContextInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsIsrInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsStackInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsTaskInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiStates/ArtiStatesTaskState`
  - `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **描述**: Choice Reference to ArtiOsTaskInstance, ArtiOsIsrInstance, ArtiStatesTaskState, OsAppMode, ArtiOsContextInstance, or ArtiOsStackInstance.

####### 8. ArtiStates

**容器属性**:

- **UUID**: `ECUC:f09e1b11-b3d0-4428-b514-97a06ade8299`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStates`
- **多重性**: [0..infinite]

**容器描述**:

This container contains all states of tasks, isrs... that the EcuC uses.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ArtiStatesTaskState

**容器属性**:

- **UUID**: `ECUC:e8303f32-586e-4a57-8910-c6c969a7f363`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStatesTaskState`
- **多重性**: [0..infinite]

**容器描述**:

Each state used by the OS has to be listed as ArtiStatesTaskState Parameter with a choice of the states.

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. ArtiStatesTaskStateEnhanced

- **UUID**: `ECUC:3c4e4984-fd12-46b1-92e6-d2fa56d11758`
- **参数名**: `ArtiStatesTaskStateEnhanced`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Set to true, if the OS provides an "enhanced" state model with "READY" split to "Activated", "Preempted", "Released".

########### ENUMERATION 类型参数

############ 1. ArtiStatesTaskStateEnum

- **UUID**: `ECUC:2f811309-d4f6-4fc7-b12e-03e43ac7e547`
- **参数名**: `ArtiStatesTaskStateEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ArtiTaskStateActivated` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStatePreempted` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReady` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReleased` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateRunning` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateSuspended` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateWaiting` (来源: AUTOSAR_ECUC)
- **描述**: ArtiStatesTaskState choice of the states.

####### 9. ArtiStatesTaskState

**容器属性**:

- **UUID**: `ECUC:e8303f32-586e-4a57-8910-c6c969a7f363`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStatesTaskState`
- **多重性**: [0..infinite]

**容器描述**:

Each state used by the OS has to be listed as ArtiStatesTaskState Parameter with a choice of the states.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. ArtiStatesTaskStateEnhanced

- **UUID**: `ECUC:3c4e4984-fd12-46b1-92e6-d2fa56d11758`
- **参数名**: `ArtiStatesTaskStateEnhanced`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Set to true, if the OS provides an "enhanced" state model with "READY" split to "Activated", "Preempted", "Released".

######### ENUMERATION 类型参数

########## 1. ArtiStatesTaskStateEnum

- **UUID**: `ECUC:2f811309-d4f6-4fc7-b12e-03e43ac7e547`
- **参数名**: `ArtiStatesTaskStateEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ArtiTaskStateActivated` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStatePreempted` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReady` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReleased` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateRunning` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateSuspended` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateWaiting` (来源: AUTOSAR_ECUC)
- **描述**: ArtiStatesTaskState choice of the states.

##### 32. ArtiConstant

**容器属性**:

- **UUID**: `ECUC:c161abde-e451-46ea-8dba-d7db465845ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiConstant`
- **多重性**: [0..infinite]

**容器描述**:

This container holds a constant value.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiConstantString

- **UUID**: `ECUC:0a007e52-6426-4b2d-80fb-3e05379d598f`
- **参数名**: `ArtiConstantString`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This is the constant value for a specific parameter.

##### 33. ArtiExpression

**容器属性**:

- **UUID**: `ECUC:cc7289be-08d8-4286-91af-79259f674241`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiExpression`
- **多重性**: [0..infinite]

**容器描述**:

This container holds a C like expression that a debugger can evaluate. This is similar to what is already done in ORTI.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiExpressionString

- **UUID**: `ECUC:dfcfe0ed-0e16-4049-969b-78a5d40b4491`
- **参数名**: `ArtiExpressionString`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This string represents a C like expression that a debugger can evaluate.

##### 34. ArtiHook

**容器属性**:

- **UUID**: `ECUC:81392ce4-93b8-4934-b9fe-7f01dcc2da72`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHook`
- **多重性**: [0..infinite]

**容器描述**:

This container represents an ARTI hook that is present in the module.

###### 参数配置

此容器包含 **4** 个参数：

####### STRING 类型参数

######## 1. ArtiHookClass

- **UUID**: `ECUC:00a1fa88-924d-4a55-8215-5a48f98ba9c1`
- **参数名**: `ArtiHookClass`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the (schedule) class of macros. Classes can be one of the predefined classes or user defined.

######## 2. ArtiHookContext

- **UUID**: `ECUC:7a8eb1a0-da8c-4914-8cc9-a560b8a6643a`
- **参数名**: `ArtiHookContext`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of the execution context. One of NOSUSP, SPRVSR, or USER.

######## 3. ArtiHookEventName

- **UUID**: `ECUC:ec285046-62b2-4145-ae17-79253c2fe836`
- **参数名**: `ArtiHookEventName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: The name of the event as defined for a particular class, or an arbitrary name for generic classes.

######## 4. ArtiHookInstance

- **UUID**: `ECUC:cb5240f2-7b27-42ab-b327-42a3902e03fb`
- **参数名**: `ArtiHookInstance`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Name of an instance of the (schedule) class.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiHookEventParameterTypeRef

- **UUID**: `ECUC:d22b8331-8951-49cb-96a3-3bbc2560d20e`
- **引用名**: `ArtiHookEventParameterTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiParameterTypeMap`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a parameter type to interpret the hook event number.

######## 2. ArtiHookInstanceParameterTypeRef

- **UUID**: `ECUC:4df421d6-b105-4baf-9768-ee004ef81c6e`
- **引用名**: `ArtiHookInstanceParameterTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiParameterTypeMap`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a parameter type to interpret the hook instance number.

##### 35. ArtiObjectClassParameter

**容器属性**:

- **UUID**: `ECUC:1c08a76b-96f1-4c04-abf7-5415edcb7bbb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiObjectClassParameter`
- **多重性**: [0..infinite]

**容器描述**:

This container represents a parameter of an Arti object class definition.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiObjectClassParameterTypeMapRef

- **UUID**: `ECUC:c715d81a-354a-4048-8aef-a286b8082e74`
- **引用名**: `ArtiObjectClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiParameterTypeMap`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a parameter type to interpret the instance parameter value.

##### 36. ArtiObjectInstanceParameter

**容器属性**:

- **UUID**: `ECUC:6575b287-9552-4ee7-8014-9d0b93ba9acb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiObjectInstanceParameter`
- **多重性**: [0..infinite]

**容器描述**:

This container represents a parameter of an Arti object instance.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiObjectInstanceParameterConstantRef

- **UUID**: `ECUC:47fc42b3-bf66-4fe3-9ff5-bec32cc927a5`
- **引用名**: `ArtiObjectInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiConstant`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a constant representing the value of this parameter.

######## 2. ArtiObjectInstanceParameterExpressionRef

- **UUID**: `ECUC:b19c6494-e2d8-427d-872d-ef02f4cc11b3`
- **引用名**: `ArtiObjectInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiExpression`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an expression that evaluates the value of this parameter.

######## 3. ArtiObjectInstanceParameterHookRef

- **UUID**: `ECUC:dbbd7880-78a6-4814-9702-0c1f420f4333`
- **引用名**: `ArtiObjectInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiHook`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to a hook that records this parameter.

##### 37. ArtiParameterTypeMap

**容器属性**:

- **UUID**: `ECUC:522ccfe6-c7f4-400d-8817-54f1041e9fad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMap`
- **多重性**: [0..infinite]

**容器描述**:

A map of key/value pairs to map a parameter value to a display string and/or an Arti or EcuC object.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ArtiParameterTypeMapPair

**容器属性**:

- **UUID**: `ECUC:b141b4df-cead-4a92-aac5-ec2ecf7ec3f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMapPair`
- **多重性**: [1..infinite]

**容器描述**:

A key/value pair to map a parameter value to a display string and/or an Arti or EcuC object.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. ArtiParameterTypeMapPairInput

- **UUID**: `ECUC:83031463-4053-4dbb-bfaf-237015e31ced`
- **参数名**: `ArtiParameterTypeMapPairInput`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The numerical value given by a parameter to translate.

######### STRING 类型参数

########## 1. ArtiParameterTypeMapPairOutput

- **UUID**: `ECUC:0bc154c3-6242-45b2-beee-247d35a47561`
- **参数名**: `ArtiParameterTypeMapPairOutput`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: The string to display for the Input value.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiParameterTypeMapPairInputExpressionRef

- **UUID**: `ECUC:21ef4ed0-1c9f-4534-bc7c-f3ab3266efe1`
- **引用名**: `ArtiParameterTypeMapPairInputExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiExpression`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an expression that evaluates to a numerical value to translate.

######### CHOICE-REFERENCE 类型引用

########## 1. ArtiParameterTypeMapPairOutputRef

- **UUID**: `ECUC:17fa6f71-ca96-4719-b1e6-d19ab7d61747`
- **引用名**: `ArtiParameterTypeMapPairOutputRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsContextInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsIsrInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsStackInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsTaskInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiStates/ArtiStatesTaskState`
  - `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **描述**: Choice Reference to ArtiOsTaskInstance, ArtiOsIsrInstance, ArtiStatesTaskState, OsAppMode, ArtiOsContextInstance, or ArtiOsStackInstance.

##### 38. ArtiParameterTypeMapPair

**容器属性**:

- **UUID**: `ECUC:b141b4df-cead-4a92-aac5-ec2ecf7ec3f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMapPair`
- **多重性**: [1..infinite]

**容器描述**:

A key/value pair to map a parameter value to a display string and/or an Arti or EcuC object.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. ArtiParameterTypeMapPairInput

- **UUID**: `ECUC:83031463-4053-4dbb-bfaf-237015e31ced`
- **参数名**: `ArtiParameterTypeMapPairInput`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The numerical value given by a parameter to translate.

####### STRING 类型参数

######## 1. ArtiParameterTypeMapPairOutput

- **UUID**: `ECUC:0bc154c3-6242-45b2-beee-247d35a47561`
- **参数名**: `ArtiParameterTypeMapPairOutput`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: The string to display for the Input value.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiParameterTypeMapPairInputExpressionRef

- **UUID**: `ECUC:21ef4ed0-1c9f-4534-bc7c-f3ab3266efe1`
- **引用名**: `ArtiParameterTypeMapPairInputExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiExpression`
- **来源**: AUTOSAR_ECUC
- **描述**: Refers to an expression that evaluates to a numerical value to translate.

####### CHOICE-REFERENCE 类型引用

######## 1. ArtiParameterTypeMapPairOutputRef

- **UUID**: `ECUC:17fa6f71-ca96-4719-b1e6-d19ab7d61747`
- **引用名**: `ArtiParameterTypeMapPairOutputRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsContextInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsIsrInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsStackInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiOs/ArtiOsTaskInstance`
  - `/AUTOSAR/EcucDefs/Arti/ArtiValues/ArtiStates/ArtiStatesTaskState`
  - `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **描述**: Choice Reference to ArtiOsTaskInstance, ArtiOsIsrInstance, ArtiStatesTaskState, OsAppMode, ArtiOsContextInstance, or ArtiOsStackInstance.

##### 39. ArtiStates

**容器属性**:

- **UUID**: `ECUC:f09e1b11-b3d0-4428-b514-97a06ade8299`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStates`
- **多重性**: [0..infinite]

**容器描述**:

This container contains all states of tasks, isrs... that the EcuC uses.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ArtiStatesTaskState

**容器属性**:

- **UUID**: `ECUC:e8303f32-586e-4a57-8910-c6c969a7f363`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStatesTaskState`
- **多重性**: [0..infinite]

**容器描述**:

Each state used by the OS has to be listed as ArtiStatesTaskState Parameter with a choice of the states.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. ArtiStatesTaskStateEnhanced

- **UUID**: `ECUC:3c4e4984-fd12-46b1-92e6-d2fa56d11758`
- **参数名**: `ArtiStatesTaskStateEnhanced`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Set to true, if the OS provides an "enhanced" state model with "READY" split to "Activated", "Preempted", "Released".

######### ENUMERATION 类型参数

########## 1. ArtiStatesTaskStateEnum

- **UUID**: `ECUC:2f811309-d4f6-4fc7-b12e-03e43ac7e547`
- **参数名**: `ArtiStatesTaskStateEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ArtiTaskStateActivated` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStatePreempted` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReady` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReleased` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateRunning` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateSuspended` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateWaiting` (来源: AUTOSAR_ECUC)
- **描述**: ArtiStatesTaskState choice of the states.

##### 40. ArtiStatesTaskState

**容器属性**:

- **UUID**: `ECUC:e8303f32-586e-4a57-8910-c6c969a7f363`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStatesTaskState`
- **多重性**: [0..infinite]

**容器描述**:

Each state used by the OS has to be listed as ArtiStatesTaskState Parameter with a choice of the states.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. ArtiStatesTaskStateEnhanced

- **UUID**: `ECUC:3c4e4984-fd12-46b1-92e6-d2fa56d11758`
- **参数名**: `ArtiStatesTaskStateEnhanced`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Set to true, if the OS provides an "enhanced" state model with "READY" split to "Activated", "Preempted", "Released".

####### ENUMERATION 类型参数

######## 1. ArtiStatesTaskStateEnum

- **UUID**: `ECUC:2f811309-d4f6-4fc7-b12e-03e43ac7e547`
- **参数名**: `ArtiStatesTaskStateEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ArtiTaskStateActivated` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStatePreempted` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReady` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReleased` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateRunning` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateSuspended` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateWaiting` (来源: AUTOSAR_ECUC)
- **描述**: ArtiStatesTaskState choice of the states.

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

1. **Arti**
