# Arti - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:37

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Arti](#arti)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00050.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Arti

#### 基本信息

- **UUID**: `de72af36-1f32-451a-985a-e246cf71201d`
- **模块名称**: `Arti`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

The Arti Module serves as a superordinate container collecting all information and parameters concerning ARTI.

#### 版本历史

共有 **3** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: Created
- **发布日期**: 2022-05-17
- **发布者**: visrk, virleh, visdqk, twurm

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: Created
- **发布日期**: 2022-08-04
- **发布者**: virleh

**变更内容**:

##### 3. 版本 1.02.00

- **状态**: Created
- **发布日期**: 2023-06-20
- **发布者**: visdqk

**变更内容**:

#### 配置容器

本模块包含 **61** 个配置容器：

##### 1. ArtiGeneric

**容器属性**:

- **UUID**: `c1d923b9-44fd-423b-9938-5c6bfa19c58c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGeneric`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

The ArtiGeneric container contains definitions for generic objects, i.e. not belonging to a standard AUTOSAR module.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. ArtiGenericComponentClass

**容器属性**:

- **UUID**: `c8cb2e3f-c484-42ef-8e7e-02ec58751589`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClass`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The class definition describes the layout of the object (similar to a "class" definition in C++).

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiGenericComponentClassName

- **UUID**: `b6b5a50c-4bac-4f1f-9d2a-b8354462785a`
- **参数名**: `ArtiGenericComponentClassName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the class.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ArtiGenericComponentClassParameter

**容器属性**:

- **UUID**: `03bb04f4-42da-45c3-86b1-718376c050c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClassParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Parameter definition of a class.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. ArtiGenericComponentClassParameterName

- **UUID**: `d9e3cc1c-c466-4b67-b538-3921cd696a88`
- **参数名**: `ArtiGenericComponentClassParameterName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the parameter.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. ArtiGenericComponentClassParameterTypeMapRef

- **UUID**: `047d595b-81a5-4c71-8440-66a6bbb14e08`
- **引用名**: `ArtiGenericComponentClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiParameterTypeMap`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a parameter type to interpret the parameter value.

####### 2. ArtiGenericComponentClassParameter

**容器属性**:

- **UUID**: `03bb04f4-42da-45c3-86b1-718376c050c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClassParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Parameter definition of a class.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiGenericComponentClassParameterName

- **UUID**: `d9e3cc1c-c466-4b67-b538-3921cd696a88`
- **参数名**: `ArtiGenericComponentClassParameterName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the parameter.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiGenericComponentClassParameterTypeMapRef

- **UUID**: `047d595b-81a5-4c71-8440-66a6bbb14e08`
- **引用名**: `ArtiGenericComponentClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiParameterTypeMap`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a parameter type to interpret the parameter value.

####### 3. ArtiGenericComponentInstance

**容器属性**:

- **UUID**: `275a3a87-c25f-40b7-b528-104f026fb7de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The instance definition describes a specific instantiated object.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiGenericComponentInstanceName

- **UUID**: `71115732-465d-4e19-8f76-cd502c232dff`
- **参数名**: `ArtiGenericComponentInstanceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the instance.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiGenericComponentInstanceClassRef

- **UUID**: `f2e294bf-c1b0-40a4-9bcb-7481fa7cba87`
- **引用名**: `ArtiGenericComponentInstanceClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a ArtGenericClass of which this object is instantiated.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ArtiGenericComponentInstanceParameter

**容器属性**:

- **UUID**: `28088b04-d46b-4220-93c2-f557615b05ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstanceParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Parameter definition of an instance.

########## 引用关系

此容器包含 **4** 个引用：

########### REFERENCE 类型引用

############ 1. ArtiGenericComponentInstanceParameterClassParameterRef

- **UUID**: `482d4c50-03fa-4563-9df9-ec7910e9f818`
- **引用名**: `ArtiGenericComponentInstanceParameterClassParameterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiGenericComponentClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass/ArtiGenericComponentClassParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClassParameter that defines this parameter.

############ 2. ArtiGenericComponentInstanceParameterConstantRef

- **UUID**: `958b803e-aaaf-42c7-be7c-f3778076117e`
- **引用名**: `ArtiGenericComponentInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiConstant`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiConstant that represents the value of this parameter.

############ 3. ArtiGenericComponentInstanceParameterExpressionRef

- **UUID**: `140a5413-5d94-4c22-a4f3-bfe5a68476a3`
- **引用名**: `ArtiGenericComponentInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiExpression`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiExpression that evaluates the value of this parameter.

############ 4. ArtiGenericComponentInstanceParameterHookRef

- **UUID**: `66051a76-1b6a-4c6b-a24a-1f2ffadbd7b9`
- **引用名**: `ArtiGenericComponentInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiHook`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a hook that records this parameter.

####### 4. ArtiGenericComponentInstanceParameter

**容器属性**:

- **UUID**: `28088b04-d46b-4220-93c2-f557615b05ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstanceParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Parameter definition of an instance.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiGenericComponentInstanceParameterClassParameterRef

- **UUID**: `482d4c50-03fa-4563-9df9-ec7910e9f818`
- **引用名**: `ArtiGenericComponentInstanceParameterClassParameterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiGenericComponentClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass/ArtiGenericComponentClassParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClassParameter that defines this parameter.

########## 2. ArtiGenericComponentInstanceParameterConstantRef

- **UUID**: `958b803e-aaaf-42c7-be7c-f3778076117e`
- **引用名**: `ArtiGenericComponentInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiConstant`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiConstant that represents the value of this parameter.

########## 3. ArtiGenericComponentInstanceParameterExpressionRef

- **UUID**: `140a5413-5d94-4c22-a4f3-bfe5a68476a3`
- **引用名**: `ArtiGenericComponentInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiExpression`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiExpression that evaluates the value of this parameter.

########## 4. ArtiGenericComponentInstanceParameterHookRef

- **UUID**: `66051a76-1b6a-4c6b-a24a-1f2ffadbd7b9`
- **引用名**: `ArtiGenericComponentInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiHook`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a hook that records this parameter.

##### 2. ArtiGenericComponentClass

**容器属性**:

- **UUID**: `c8cb2e3f-c484-42ef-8e7e-02ec58751589`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClass`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The class definition describes the layout of the object (similar to a "class" definition in C++).

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiGenericComponentClassName

- **UUID**: `b6b5a50c-4bac-4f1f-9d2a-b8354462785a`
- **参数名**: `ArtiGenericComponentClassName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the class.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ArtiGenericComponentClassParameter

**容器属性**:

- **UUID**: `03bb04f4-42da-45c3-86b1-718376c050c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClassParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Parameter definition of a class.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiGenericComponentClassParameterName

- **UUID**: `d9e3cc1c-c466-4b67-b538-3921cd696a88`
- **参数名**: `ArtiGenericComponentClassParameterName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the parameter.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiGenericComponentClassParameterTypeMapRef

- **UUID**: `047d595b-81a5-4c71-8440-66a6bbb14e08`
- **引用名**: `ArtiGenericComponentClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiParameterTypeMap`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a parameter type to interpret the parameter value.

##### 3. ArtiGenericComponentClassParameter

**容器属性**:

- **UUID**: `03bb04f4-42da-45c3-86b1-718376c050c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentClassParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Parameter definition of a class.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiGenericComponentClassParameterName

- **UUID**: `d9e3cc1c-c466-4b67-b538-3921cd696a88`
- **参数名**: `ArtiGenericComponentClassParameterName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the parameter.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiGenericComponentClassParameterTypeMapRef

- **UUID**: `047d595b-81a5-4c71-8440-66a6bbb14e08`
- **引用名**: `ArtiGenericComponentClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiParameterTypeMap`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a parameter type to interpret the parameter value.

##### 4. ArtiGenericComponentInstance

**容器属性**:

- **UUID**: `275a3a87-c25f-40b7-b528-104f026fb7de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The instance definition describes a specific instantiated object.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiGenericComponentInstanceName

- **UUID**: `71115732-465d-4e19-8f76-cd502c232dff`
- **参数名**: `ArtiGenericComponentInstanceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the instance.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiGenericComponentInstanceClassRef

- **UUID**: `f2e294bf-c1b0-40a4-9bcb-7481fa7cba87`
- **引用名**: `ArtiGenericComponentInstanceClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a ArtGenericClass of which this object is instantiated.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ArtiGenericComponentInstanceParameter

**容器属性**:

- **UUID**: `28088b04-d46b-4220-93c2-f557615b05ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstanceParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Parameter definition of an instance.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiGenericComponentInstanceParameterClassParameterRef

- **UUID**: `482d4c50-03fa-4563-9df9-ec7910e9f818`
- **引用名**: `ArtiGenericComponentInstanceParameterClassParameterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiGenericComponentClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass/ArtiGenericComponentClassParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClassParameter that defines this parameter.

########## 2. ArtiGenericComponentInstanceParameterConstantRef

- **UUID**: `958b803e-aaaf-42c7-be7c-f3778076117e`
- **引用名**: `ArtiGenericComponentInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiConstant`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiConstant that represents the value of this parameter.

########## 3. ArtiGenericComponentInstanceParameterExpressionRef

- **UUID**: `140a5413-5d94-4c22-a4f3-bfe5a68476a3`
- **引用名**: `ArtiGenericComponentInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiExpression`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiExpression that evaluates the value of this parameter.

########## 4. ArtiGenericComponentInstanceParameterHookRef

- **UUID**: `66051a76-1b6a-4c6b-a24a-1f2ffadbd7b9`
- **引用名**: `ArtiGenericComponentInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiHook`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a hook that records this parameter.

##### 5. ArtiGenericComponentInstanceParameter

**容器属性**:

- **UUID**: `28088b04-d46b-4220-93c2-f557615b05ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGenericComponentInstanceParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Parameter definition of an instance.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiGenericComponentInstanceParameterClassParameterRef

- **UUID**: `482d4c50-03fa-4563-9df9-ec7910e9f818`
- **引用名**: `ArtiGenericComponentInstanceParameterClassParameterRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiGenericComponentClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass/ArtiGenericComponentClassParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClassParameter that defines this parameter.

######## 2. ArtiGenericComponentInstanceParameterConstantRef

- **UUID**: `958b803e-aaaf-42c7-be7c-f3778076117e`
- **引用名**: `ArtiGenericComponentInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiConstant`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiConstant that represents the value of this parameter.

######## 3. ArtiGenericComponentInstanceParameterExpressionRef

- **UUID**: `140a5413-5d94-4c22-a4f3-bfe5a68476a3`
- **引用名**: `ArtiGenericComponentInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiExpression`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiExpression that evaluates the value of this parameter.

######## 4. ArtiGenericComponentInstanceParameterHookRef

- **UUID**: `66051a76-1b6a-4c6b-a24a-1f2ffadbd7b9`
- **引用名**: `ArtiGenericComponentInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiHook`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a hook that records this parameter.

##### 6. ArtiHardware

**容器属性**:

- **UUID**: `18f08ccc-98c1-45f1-ad26-ab3947a54faf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHardware`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

The ArtiHardware container contains ARTI extensions to the EcucHardware module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. ArtiHardwareCoreClass

**容器属性**:

- **UUID**: `2042cdd1-e975-4a98-a1ef-e3e1966b2b05`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHardwareCoreClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "Core" object, extending the EcucCoreDefinition.

######## 引用关系

此容器包含 **6** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiHardwareCoreClassCurrentApplicationRef

- **UUID**: `e825755c-8b91-4dc7-8d81-16e9e831c1b4`
- **引用名**: `ArtiHardwareCoreClassCurrentApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentApplicationInstance parameter.

########## 2. ArtiHardwareCoreClassCurrentIsrRef

- **UUID**: `7353ffc4-fae9-4d4b-9b1a-2ea26c3dbee6`
- **引用名**: `ArtiHardwareCoreClassCurrentIsrRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentIsrInstance parameter.

########## 3. ArtiHardwareCoreClassCurrentTaskRef

- **UUID**: `258e1f25-5785-4c48-865d-cbdff93ce94a`
- **引用名**: `ArtiHardwareCoreClassCurrentTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentTaskInstance parameter.

########## 4. ArtiHardwareCoreClassGenericComponentRef

- **UUID**: `a0d6035d-fd38-4e8c-8c2a-b2aea1264b85`
- **引用名**: `ArtiHardwareCoreClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the core description.

########## 5. ArtiHardwareCoreClassLastErrorRef

- **UUID**: `2df35fc0-9d06-4726-8934-381648f24593`
- **引用名**: `ArtiHardwareCoreClassLastErrorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiLastErrorInstance parameter.

########## 6. ArtiHardwareCoreClassRunningTaskPriorityRef

- **UUID**: `39835450-74eb-4597-a1f4-d85436fe50e5`
- **引用名**: `ArtiHardwareCoreClassRunningTaskPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiHwCoreInstanceRunningTaskPriority parameter. This attribute specifies how to evaluate the current priority of the task referred by RUNNINGTASK. The current priority can be different from the static task priority as a result of priority ceiling protocol. This attribute differs from ArtiCurrentTask->ArtiOsTaskClassPriority as here is a single variable while in multiple tasks there is a single variable per task.

####### 2. ArtiHardwareCoreInstance

**容器属性**:

- **UUID**: `00e8dd3d-7dcf-4349-9f76-94e4c688b851`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHardwareCoreInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Description: Represents an instance of an ARTI "Core" object, extending the EcucCoreDefinition. When using ARTI for debugging or hardware based tracing, this is mandatory (i.e. multiplicity 1..*), else optional.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. ArtiHardwareCoreInstanceCoreId

- **UUID**: `71a61f85-31d8-4fc7-b429-fc0a647b0cd8`
- **参数名**: `ArtiHardwareCoreInstanceCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter represents the "CoreID" as given by the OS, returned by GetCoreID().

######## 引用关系

此容器包含 **8** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiHardwareCoreInstanceCurrentApplicationRef

- **UUID**: `43f62ba1-78d7-48a8-8a5b-fcb09ea3b491`
- **引用名**: `ArtiHardwareCoreInstanceCurrentApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current application" that is running on this core.

########## 2. ArtiHardwareCoreInstanceCurrentIsrRef

- **UUID**: `854e0039-4e31-4528-bded-287233d820d5`
- **引用名**: `ArtiHardwareCoreInstanceCurrentIsrRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current ISR" that is running on this core.

########## 3. ArtiHardwareCoreInstanceCurrentTaskRef

- **UUID**: `e72c1f28-85c5-476b-97bb-1d134744666a`
- **引用名**: `ArtiHardwareCoreInstanceCurrentTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current task" that is running on this core.

########## 4. ArtiHardwareCoreInstanceEcucCoreRef

- **UUID**: `113e1fd2-2d89-40e9-bc93-396e44f19985`
- **引用名**: `ArtiHardwareCoreInstanceEcucCoreRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucCoreDefinition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucHardware/EcucCoreDefinition`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the EcucCoreDefinition of this core.

########## 5. ArtiHardwareCoreInstanceGenericComponentRef

- **UUID**: `5eddf14c-0fb3-4e55-a80f-8b21166d5aa6`
- **引用名**: `ArtiHardwareCoreInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends a core.

########## 6. ArtiHardwareCoreInstanceLastErrorRef

- **UUID**: `fa4b6183-e102-4a23-a049-66aa6bb967e9`
- **引用名**: `ArtiHardwareCoreInstanceLastErrorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "last error" that happened on this core.

########## 7. ArtiHardwareCoreInstanceRunningTaskPriorityRef

- **UUID**: `d5f512bd-1408-48bf-94a1-5ed61adf1236`
- **引用名**: `ArtiHardwareCoreInstanceRunningTaskPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "running task priority" that is on this core.

########## 8. ArtiHardwareCoreInstanceValidRef

- **UUID**: `30a418e7-3795-4e0e-82db-b144133f789b`
- **引用名**: `ArtiHardwareCoreInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiHwCoreInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 7. ArtiHardwareCoreClass

**容器属性**:

- **UUID**: `2042cdd1-e975-4a98-a1ef-e3e1966b2b05`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHardwareCoreClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "Core" object, extending the EcucCoreDefinition.

###### 引用关系

此容器包含 **6** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiHardwareCoreClassCurrentApplicationRef

- **UUID**: `e825755c-8b91-4dc7-8d81-16e9e831c1b4`
- **引用名**: `ArtiHardwareCoreClassCurrentApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentApplicationInstance parameter.

######## 2. ArtiHardwareCoreClassCurrentIsrRef

- **UUID**: `7353ffc4-fae9-4d4b-9b1a-2ea26c3dbee6`
- **引用名**: `ArtiHardwareCoreClassCurrentIsrRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentIsrInstance parameter.

######## 3. ArtiHardwareCoreClassCurrentTaskRef

- **UUID**: `258e1f25-5785-4c48-865d-cbdff93ce94a`
- **引用名**: `ArtiHardwareCoreClassCurrentTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentTaskInstance parameter.

######## 4. ArtiHardwareCoreClassGenericComponentRef

- **UUID**: `a0d6035d-fd38-4e8c-8c2a-b2aea1264b85`
- **引用名**: `ArtiHardwareCoreClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the core description.

######## 5. ArtiHardwareCoreClassLastErrorRef

- **UUID**: `2df35fc0-9d06-4726-8934-381648f24593`
- **引用名**: `ArtiHardwareCoreClassLastErrorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiLastErrorInstance parameter.

######## 6. ArtiHardwareCoreClassRunningTaskPriorityRef

- **UUID**: `39835450-74eb-4597-a1f4-d85436fe50e5`
- **引用名**: `ArtiHardwareCoreClassRunningTaskPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiHwCoreInstanceRunningTaskPriority parameter. This attribute specifies how to evaluate the current priority of the task referred by RUNNINGTASK. The current priority can be different from the static task priority as a result of priority ceiling protocol. This attribute differs from ArtiCurrentTask->ArtiOsTaskClassPriority as here is a single variable while in multiple tasks there is a single variable per task.

##### 8. ArtiHardwareCoreInstance

**容器属性**:

- **UUID**: `00e8dd3d-7dcf-4349-9f76-94e4c688b851`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHardwareCoreInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Description: Represents an instance of an ARTI "Core" object, extending the EcucCoreDefinition. When using ARTI for debugging or hardware based tracing, this is mandatory (i.e. multiplicity 1..*), else optional.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. ArtiHardwareCoreInstanceCoreId

- **UUID**: `71a61f85-31d8-4fc7-b429-fc0a647b0cd8`
- **参数名**: `ArtiHardwareCoreInstanceCoreId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter represents the "CoreID" as given by the OS, returned by GetCoreID().

###### 引用关系

此容器包含 **8** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiHardwareCoreInstanceCurrentApplicationRef

- **UUID**: `43f62ba1-78d7-48a8-8a5b-fcb09ea3b491`
- **引用名**: `ArtiHardwareCoreInstanceCurrentApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current application" that is running on this core.

######## 2. ArtiHardwareCoreInstanceCurrentIsrRef

- **UUID**: `854e0039-4e31-4528-bded-287233d820d5`
- **引用名**: `ArtiHardwareCoreInstanceCurrentIsrRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current ISR" that is running on this core.

######## 3. ArtiHardwareCoreInstanceCurrentTaskRef

- **UUID**: `e72c1f28-85c5-476b-97bb-1d134744666a`
- **引用名**: `ArtiHardwareCoreInstanceCurrentTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current task" that is running on this core.

######## 4. ArtiHardwareCoreInstanceEcucCoreRef

- **UUID**: `113e1fd2-2d89-40e9-bc93-396e44f19985`
- **引用名**: `ArtiHardwareCoreInstanceEcucCoreRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucCoreDefinition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucHardware/EcucCoreDefinition`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the EcucCoreDefinition of this core.

######## 5. ArtiHardwareCoreInstanceGenericComponentRef

- **UUID**: `5eddf14c-0fb3-4e55-a80f-8b21166d5aa6`
- **引用名**: `ArtiHardwareCoreInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends a core.

######## 6. ArtiHardwareCoreInstanceLastErrorRef

- **UUID**: `fa4b6183-e102-4a23-a049-66aa6bb967e9`
- **引用名**: `ArtiHardwareCoreInstanceLastErrorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "last error" that happened on this core.

######## 7. ArtiHardwareCoreInstanceRunningTaskPriorityRef

- **UUID**: `d5f512bd-1408-48bf-94a1-5ed61adf1236`
- **引用名**: `ArtiHardwareCoreInstanceRunningTaskPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "running task priority" that is on this core.

######## 8. ArtiHardwareCoreInstanceValidRef

- **UUID**: `30a418e7-3795-4e0e-82db-b144133f789b`
- **引用名**: `ArtiHardwareCoreInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiHwCoreInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 9. ArtiOs

**容器属性**:

- **UUID**: `3ae6a247-e751-4ea6-b390-7c3f680b4b71`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOs`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

The ArtiOs container contains ARTI extensions to the EcucDefs/Os module.

###### 配置容器

本模块包含 **16** 个配置容器：

####### 1. ArtiOsAlarmClass

**容器属性**:

- **UUID**: `b5f782ab-efc6-4648-8b85-156f4949836e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsAlarmClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ArtiOsAlarm object.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsAlarmClassGenericComponentClassRef

- **UUID**: `a8e92da9-932a-4f32-b9b0-19829803f38c`
- **引用名**: `ArtiOsAlarmClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsAlarmClass.

########## 2. ArtiOsAlarmClassStateRef

- **UUID**: `51627aa2-5d77-4936-b4c0-8f7a31ee50c9`
- **引用名**: `ArtiOsAlarmClassStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsAlarmStateRef in ArtiOsAlarmInstances. This attribute specifies if an alarm is "RUNNING" or "STOPPED". The refered ArtiObjectClassParameter does include the mapping from integer to human readable "RUNNING" or "STOPPED".

####### 2. ArtiOsAlarmInstance

**容器属性**:

- **UUID**: `14e3d025-67ab-41b2-82f4-e5db983eac9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsAlarmInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an ArtiOsAlarm object, extending the EcuC OsTaskAlarm.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. ArtiOsAlarmInstanceAction

- **UUID**: `6c8a9e36-91a5-4e5d-827d-cbb671a64b39`
- **参数名**: `ArtiOsAlarmInstanceAction`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute provides a string with a description of the action when the alarm expires, e.g. "ActivateTask TaskA".

########## 2. ArtiOsAlarmInstanceCounter

- **UUID**: `fb6682af-490b-4a63-834a-a8aa6d48fee9`
- **参数名**: `ArtiOsAlarmInstanceCounter`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute provides a string containing the name of the counter used by this alarm.

######## 引用关系

此容器包含 **6** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsAlarmInstanceAlarmTimeRef

- **UUID**: `d045dd9d-5d12-4d2c-8557-5574a6660c0f`
- **引用名**: `ArtiOsAlarmInstanceAlarmTimeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This attribute specifies how to evaluate the time until the alarm expires next. The time should be represented in seconds.

########## 2. ArtiOsAlarmInstanceCycleTimeRef

- **UUID**: `890b3b18-b4cf-4129-b381-3ccfc8c78b7c`
- **引用名**: `ArtiOsAlarmInstanceCycleTimeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This attribute specifies how to evaluate the cycle time for cyclic alarms. The value of "cycle time" is 0 for non-cyclic alarms. The time should be represendet in seconds.

########## 3. ArtiOsAlarmInstanceEcuCRef

- **UUID**: `442280d1-fb7d-4efa-b302-80d88167143a`
- **引用名**: `ArtiOsAlarmInstanceEcuCRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an EcuC OsAlarm that is beeing extended.

########## 4. ArtiOsAlarmInstanceGenericComponentInstanceRef

- **UUID**: `6dd649b0-ed9b-44b3-839a-dd67c49e9fa6`
- **引用名**: `ArtiOsAlarmInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsAlarmInstance.

########## 5. ArtiOsAlarmInstanceStateRef

- **UUID**: `17afaf04-3812-499a-8d43-a34f934de357`
- **引用名**: `ArtiOsAlarmInstanceStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "state" of this alarm. The result then is mapped with the typemap of the ArtiOsAlarmStateRef of the ArtiOsAlarmClass.

########## 6. ArtiOsAlarmInstanceValidRef

- **UUID**: `0380140b-861f-4055-92f1-cb873bd26048`
- **引用名**: `ArtiOsAlarmInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this alarm. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 3. ArtiOsClass

**容器属性**:

- **UUID**: `2b22415b-e184-40c9-b360-1b25d75e7f80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "Os" object, extending the EcuC OsOS.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsClassAppModeRef

- **UUID**: `7b71f020-64f3-43e3-b67c-bfc22785b7a9`
- **引用名**: `ArtiOsClassAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiOsAppModeInstance parameter.

########## 2. ArtiOsClassGenericComponentRef

- **UUID**: `f0541cba-aad8-45ed-b9a6-1bd2eef85e75`
- **引用名**: `ArtiOsClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the OS description.

########## 3. ArtiOsClassServiceTraceRef

- **UUID**: `f58b9974-5e2f-4de7-91ef-dd7691264836`
- **引用名**: `ArtiOsClassServiceTraceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiOsInstanceServiceTrace parameter. This attribute indicates the entry or exit of a service routine and the ID of this service routine. The value of this attribute must be evaluated from one single memory location.

####### 4. ArtiOsContextClass

**容器属性**:

- **UUID**: `2d823e70-a607-471d-b19d-afa8576d4a32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsContextClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "OsContext" object.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsContextClassGenericComponentClassRef

- **UUID**: `59be4ef5-2db8-4db1-b3c5-d850b35c3f1e`
- **引用名**: `ArtiOsContextClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsContextClass.

####### 5. ArtiOsContextInstance

**容器属性**:

- **UUID**: `80a8f9bf-5e07-44ab-8880-28a52d8bdc19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsContextInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an "ArtiContext" object.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsContextInstanceAddressRef

- **UUID**: `54f89187-852e-4f80-812f-e48fbe43fa0d`
- **引用名**: `ArtiOsContextInstanceAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "address" of this context.

########## 2. ArtiOsContextInstanceGenericComponentInstanceRef

- **UUID**: `23938db4-bbf3-4ae5-ad95-296f79b16d6c`
- **引用名**: `ArtiOsContextInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsContext.

########## 3. ArtiOsContextInstanceSizeRef

- **UUID**: `96769bcd-c46a-42db-8f24-f5768700bdc1`
- **引用名**: `ArtiOsContextInstanceSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "size" of this context.

########## 4. ArtiOsContextInstanceValidRef

- **UUID**: `146ac2d4-0f2c-4409-b86e-fbb23be29098`
- **引用名**: `ArtiOsContextInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this context. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 6. ArtiOsInstance

**容器属性**:

- **UUID**: `75d6a881-c5de-420e-a93d-d4ef2a42ff18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsInstance`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Represents an instance of an ARTI "Os" object, extending the EcuC OsOS.

######## 引用关系

此容器包含 **6** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsInstanceAppModeRef

- **UUID**: `1894f4dc-432b-46fb-8903-5014d3edd198`
- **引用名**: `ArtiOsInstanceAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "application mode" of this OS.

########## 2. ArtiOsInstanceEcucRef

- **UUID**: `53e05590-8021-4f0d-a655-927626abc426`
- **引用名**: `ArtiOsInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsOS`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsOS`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the EcucDefs/Os/OsOS of this OS.

########## 3. ArtiOsInstanceGenericComponentRef

- **UUID**: `60cc8e10-9d54-4c91-92b3-07027ff814fc`
- **引用名**: `ArtiOsInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OS.

########## 4. ArtiOsInstanceHookRef

- **UUID**: `8705d640-c9f4-4a82-9d39-d82b145e2c92`
- **引用名**: `ArtiOsInstanceHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiHook`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiHook`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a hook defined in the OS.

########## 5. ArtiOsInstanceServiceTraceRef

- **UUID**: `f2e1ea30-9167-4c2a-a1be-a2f87c5621b8`
- **引用名**: `ArtiOsInstanceServiceTraceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a hook defined in the OS.

########## 6. ArtiOsInstanceValidRef

- **UUID**: `a8d33bbc-d8c7-4d38-92d2-41f12e6fc8db`
- **引用名**: `ArtiOsInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 7. ArtiOsIsrClass

**容器属性**:

- **UUID**: `5792a9bd-8d2e-486b-ac25-f3e19060ecb6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsIsrClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "OsIsr" object, extending the EcuC OsIsr.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsIsrClassGenericComponentRef

- **UUID**: `565fecdb-50d0-4bed-9761-d1135472bd6c`
- **引用名**: `ArtiOsIsrClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an optional ArtiGenericComponentClass that extends the OsIsr with additional parameters.

####### 8. ArtiOsIsrInstance

**容器属性**:

- **UUID**: `45355954-0eee-49a5-afca-de458d29aecd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsIsrInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an ARTI "OsIsr" object, extending the EcuC OsIsr.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. ArtiOsIsrInstanceId

- **UUID**: `d182da57-0d5c-4135-aa38-dca157fd3775`
- **参数名**: `ArtiOsIsrInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter represents the "ISRID" as given by the OS, returned by GetISRID().

######### ENUMERATION 类型参数

########## 1. ArtiOsIsrInstanceCategory

- **UUID**: `fa58b723-f5ff-418f-8083-fb9b14b50db7`
- **参数名**: `ArtiOsIsrInstanceCategory`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CATEGORY_1` (来源: AUTOSAR_ECUC)
  - `CATEGORY_2` (来源: AUTOSAR_ECUC)
- **描述**: Specifies category of this ISR. If omitted the instance is related to a CATEGORY_2.

######### FUNCTION-NAME 类型参数

########## 1. ArtiOsIsrInstanceFunction

- **UUID**: `ee3a5aee-44e7-4b01-b0cb-a8076f9d0313`
- **参数名**: `ArtiOsIsrInstanceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter represents the C function name of the ISR routine.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsIsrInstanceEcucRef

- **UUID**: `c90951f2-ce27-409f-8543-d9b4acafbaae`
- **引用名**: `ArtiOsIsrInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsIsr`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsIsr`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the EcucDefs/Os/OsIsr of this ISR.

########## 2. ArtiOsIsrInstanceGenericComponentRef

- **UUID**: `35aa9890-6625-40e9-83aa-c09b65ff836d`
- **引用名**: `ArtiOsIsrInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an optional ArtiGenericComponentInstance that extends this OsIsr with additional parameters.

########## 3. ArtiOsIsrInstanceValidRef

- **UUID**: `495cf147-f919-49c8-a4e0-1b29ac8849e6`
- **引用名**: `ArtiOsIsrInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsIsrInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 9. ArtiOsMessageContainerClass

**容器属性**:

- **UUID**: `18da79e4-9d0e-4db0-a45e-96c280e05b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsMessageContainerClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "OsMessageContainer" object. The "OsMessageContainer" object represents an existing combination of OSEK messages.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsMessageContainerClassGenericComponentClassRef

- **UUID**: `1f502f6a-d94f-48cb-9a60-1512b1392f4f`
- **引用名**: `ArtiOsMessageContainerClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsMessageContainerClass.

####### 10. ArtiOsMessageContainerInstance

**容器属性**:

- **UUID**: `1f39e839-4b8b-4c61-8e6c-f303016fadd8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsMessageContainerInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an "ArtiMessageContainer" object.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. ArtiOsMessageContainerInstanceMsgName

- **UUID**: `e19dc328-c6c2-4c59-9137-ce89a3b5484c`
- **参数名**: `ArtiOsMessageContainerInstanceMsgName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute provides the name of the message as defined in OIL file.

########## 2. ArtiOsMessageContainerInstanceMsgType

- **UUID**: `e2bc4ba5-4cf9-493d-be5b-9d91b623d4ec`
- **参数名**: `ArtiOsMessageContainerInstanceMsgType`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute provides the type of the message.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsMessageContainerInstanceFirstElementRef

- **UUID**: `e42ef9a9-874a-4a78-b895-371173fb266b`
- **引用名**: `ArtiOsMessageContainerInstanceFirstElementRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "firstelement" of this "ArtiOsMessageContainer". This attribute provides the formula for evaluation of address of first valid message. This message will be received next. If no message is in the queue the value is zero.

########## 2. ArtiOsMessageContainerInstanceGenericComponentInstanceRef

- **UUID**: `e9427339-1727-4bb7-b2ea-889105fed005`
- **引用名**: `ArtiOsMessageContainerInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsMessageContainerInstance.

########## 3. ArtiOsMessageContainerInstanceQueueCountRef

- **UUID**: `e68efeea-7a3e-4de4-a52c-b1fe7ce0b9ac`
- **引用名**: `ArtiOsMessageContainerInstanceQueueCountRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "queuecount" of this "ArtiOsMessageContainer". This attribute provides the number of valid messages in the queue and "1" for unqueued messages.

########## 4. ArtiOsMessageContainerInstanceQueueSizeRef

- **UUID**: `fcde820f-aba6-4aeb-b61b-6fef5238b301`
- **引用名**: `ArtiOsMessageContainerInstanceQueueSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "queuesize" of this "ArtiOsMessageContainer". This attribute provides the size of the queue for queued messages and "1" for unqueued messages.

########## 5. ArtiOsMessageContainerInstanceValidRef

- **UUID**: `806093e3-29ba-4955-a746-7f6c4efe71f8`
- **引用名**: `ArtiOsMessageContainerInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsMessageContainerInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 11. ArtiOsResourceClass

**容器属性**:

- **UUID**: `f21de7e4-e46d-4a4e-be22-b5d574d1a245`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsResourceClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ArtiOsResource object. The ArtiOsResource object represents an OSEK resource.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsResourceClassGenericComponentClassRef

- **UUID**: `bee8f7b7-3d5d-4e1c-98b3-be62f0c1bfae`
- **引用名**: `ArtiOsResourceClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsResourceClass.

########## 2. ArtiOsResourceClassLockerRef

- **UUID**: `29c43115-ed0f-4293-9d02-5db49b984332`
- **引用名**: `ArtiOsResourceClassLockerRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsResourceLockerRef in ArtiOsResourceInstances. This attribute indicates the locking ArtiOsTaskInstance or ArtiOsIsrInstance.

########## 3. ArtiOsResourceClassStateRef

- **UUID**: `d2ac2895-ebca-449d-922d-6de8c235f4b7`
- **引用名**: `ArtiOsResourceClassStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsResourceStateRef in ArtiOsResourceInstances. This attribute represents the state of a resource ("LOCKED"/"UNLOCKED"). The ArtiObjectClassParameter does include the mapping from integer to human readable "LOCKED" or "UNLOCKED".

####### 12. ArtiOsResourceInstance

**容器属性**:

- **UUID**: `75c3064b-2a7e-482f-bbbb-a463cf355f03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsResourceInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an ArtiOsResource object.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiOsResourceInstancePriority

- **UUID**: `266c180a-c0c6-4686-a2af-74f79cdf7639`
- **参数名**: `ArtiOsResourceInstancePriority`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute has two components that state: that the RESOURCE is used by TASKs only or by TASKs and ISRs, and the priority that will be used when locking the RESOURCE.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsResourceInstanceEcuCRef

- **UUID**: `865d490d-5277-430c-ad97-3652eba99d83`
- **引用名**: `ArtiOsResourceInstanceEcuCRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an EcuC OsResource that is beeing extended.

########## 2. ArtiOsResourceInstanceGenericComponentInstanceRef

- **UUID**: `9cd554f4-3282-4e33-9a13-b806f04de97e`
- **引用名**: `ArtiOsResourceInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsResourceInstance.

########## 3. ArtiOsResourceInstanceLockerRef

- **UUID**: `1c5221b4-e4cd-411c-b185-064faa2f8e35`
- **引用名**: `ArtiOsResourceInstanceLockerRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "locker" of this ArtiOsResource.

########## 4. ArtiOsResourceInstanceStateRef

- **UUID**: `0c6d91b9-09f6-47d8-a91c-77547a94b278`
- **引用名**: `ArtiOsResourceInstanceStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "state" of this ArtiOsResource.

########## 5. ArtiOsResourceInstanceValidRef

- **UUID**: `78a293fc-77df-4da3-a493-0377aef33ce7`
- **引用名**: `ArtiOsResourceInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsResourceInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 13. ArtiOsStackClass

**容器属性**:

- **UUID**: `362e5858-b128-4875-9a0c-d52805b881ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsStackClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ArtiOsStack object. The ArtiOsStack object defines the memory area of any stack in the system.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsStackClassGenericComponentClassRef

- **UUID**: `f8e55f56-4a8a-4475-a31e-8c0e179884e4`
- **引用名**: `ArtiOsStackClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsStackClass.

####### 14. ArtiOsStackInstance

**容器属性**:

- **UUID**: `c243161f-cb41-44e7-91a3-d0b2d66feec0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsStackInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an ArtiOsStack object.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiOsStackInstanceDirection

- **UUID**: `1ac82a0e-f709-442d-b2e9-70566932d987`
- **参数名**: `ArtiOsStackInstanceDirection`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute specifies the direction of stack growth and may have either "UP" or "DOWN" as its value. UP means growing from lower to higher addresses. DOWN means growing from higher addresses to lower addresses.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsStackInstanceBaseAddressRef

- **UUID**: `9ca238b8-2f28-4027-a56a-841a59eb0977`
- **引用名**: `ArtiOsStackInstanceBaseAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "baseaddress" of this ArtiOsStack. This attribute specifies the lowest address of stack memory area, regardless of the stack direction.

########## 2. ArtiOsStackInstanceFillPatternRef

- **UUID**: `d8bddf2d-51be-4838-bac3-fcad16830e2b`
- **引用名**: `ArtiOsStackInstanceFillPatternRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "fillpattern" of this ArtiOsStack. If the operating system fills the stack during initialisation, this attribute specifies with which pattern the stack area is initialised. This allows the debugger to evaluate the maximum stack usage. For "stackdirection" "DOWN" the pattern starts at "baseaddress". For "stackdirection" "UP" the pattern starts at "baseaddress" + "size". If no pattern is used, this attribute must be omitted.

########## 3. ArtiOsStackInstanceGenericComponentInstanceRef

- **UUID**: `eaa700b4-3edd-45c7-a641-e2aaa8d40b47`
- **引用名**: `ArtiOsStackInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsStackInstance.

########## 4. ArtiOsStackInstanceSizeRef

- **UUID**: `0a3e9ed9-8a07-4012-99a3-9c17b5f3368b`
- **引用名**: `ArtiOsStackInstanceSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "size" of this ArtiOsStack. This attribute represents the size (in bytes) of the memory area allocated for stack.

########## 5. ArtiOsStackInstanceValidRef

- **UUID**: `0d750424-f610-4f46-8e8c-25b3cf42d50c`
- **引用名**: `ArtiOsStackInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsStackInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

####### 15. ArtiOsTaskClass

**容器属性**:

- **UUID**: `0c36f049-272a-4dca-a9da-601525f017d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsTaskClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "OsTask" object, extending the EcuC OsTask.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsTaskClassClassGenericComponentRef

- **UUID**: `0d713ec7-d99c-49f6-9553-4e68dd1c3c6b`
- **引用名**: `ArtiOsTaskClassClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the OsTask.

########## 2. ArtiOsTaskClassContextRef

- **UUID**: `a3eaf2a0-db1d-4aae-91ce-a858af062dfd`
- **引用名**: `ArtiOsTaskClassContextRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: ArtiOsTaskContextRef in ArtiOsTaskInstances. This attribute contains a reference to the context object that the task is currently using.

########## 3. ArtiOsTaskClassCurrentTaskStateRef

- **UUID**: `b8429894-3f45-41a7-8dcb-29451c58de4c`
- **引用名**: `ArtiOsTaskClassCurrentTaskStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentTaskStateInstance parameter including the task state mapping.

########## 4. ArtiOsTaskClassPriorityRef

- **UUID**: `4dd2db8b-2002-4280-bf58-a5bc39827dd5`
- **引用名**: `ArtiOsTaskClassPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsTaskPriorityRef in ArtiOsTaskInstances. This attribute represents the current priority of the TASK object. The current priority can be different from the static task priority as a result of priority ceiling protocol. The priority displayed is the priority as defined in the OsTask.

########## 5. ArtiOsTaskClassStackRef

- **UUID**: `2bc48f8d-0c30-489a-a4b4-38428ade7308`
- **引用名**: `ArtiOsTaskClassStackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsTaskStackRef in ArtiOsTaskInstances. This attribute contains a reference to the stack object that the task is currently using.

####### 16. ArtiOsTaskInstance

**容器属性**:

- **UUID**: `86223bb3-c182-4a6d-9186-a9f733bac0d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsTaskInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an ARTI "OsTask" object, extending the EcuC OsTask.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. ArtiOsTaskInstanceId

- **UUID**: `c51f0dc6-be2b-435f-9502-57fa80a7c82c`
- **参数名**: `ArtiOsTaskInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter represents the "TaskID" as given by the OSEK OS, returned by GetTaskID().

######### FUNCTION-NAME 类型参数

########## 1. ArtiOsTaskInstanceFunction

- **UUID**: `f9d0e68d-5a96-4836-b9d0-9f5848b86ba4`
- **参数名**: `ArtiOsTaskInstanceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter represents the C function name of the task body.

######## 引用关系

此容器包含 **8** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiOsTaskInstanceContextRef

- **UUID**: `81d6a1ad-f676-4bfd-9c9c-8b385b4f94cf`
- **引用名**: `ArtiOsTaskInstanceContextRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the ArtiOsContext of this ArtiOsTask.

########## 2. ArtiOsTaskInstanceCurrentActivationsRef

- **UUID**: `67f80508-105f-4df8-a94b-5d638212e419`
- **引用名**: `ArtiOsTaskInstanceCurrentActivationsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current activations" of this task. This attribute specifies the number of current activations for the task.

########## 3. ArtiOsTaskInstanceCurrentTaskStateRef

- **UUID**: `8813a8c9-1f71-494f-a612-7a90f9cd2340`
- **引用名**: `ArtiOsTaskInstanceCurrentTaskStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current state" of this task.

########## 4. ArtiOsTaskInstanceEcucRef

- **UUID**: `cd8c34be-65e8-43e2-b67b-0b0bf0f3057e`
- **引用名**: `ArtiOsTaskInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OsTask.

########## 5. ArtiOsTaskInstanceGenericComponentRef

- **UUID**: `738951ca-3cc0-4a91-b077-90d66828ef03`
- **引用名**: `ArtiOsTaskInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OsTask.

########## 6. ArtiOsTaskInstancePriorityRef

- **UUID**: `8a8bcbc3-a939-4d46-8c30-03c26d38d5bd`
- **引用名**: `ArtiOsTaskInstancePriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "task priority" of this task.

########## 7. ArtiOsTaskInstanceStackRef

- **UUID**: `34c87203-331f-4aae-84a2-ab38177462ce`
- **引用名**: `ArtiOsTaskInstanceStackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the ArtiOsStack of this ArtiOsTask.

########## 8. ArtiOsTaskInstanceValidRef

- **UUID**: `b51ece07-dd02-44e6-990d-eacc3fba9610`
- **引用名**: `ArtiOsTaskInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsTaskInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 10. ArtiOsAlarmClass

**容器属性**:

- **UUID**: `b5f782ab-efc6-4648-8b85-156f4949836e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsAlarmClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ArtiOsAlarm object.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsAlarmClassGenericComponentClassRef

- **UUID**: `a8e92da9-932a-4f32-b9b0-19829803f38c`
- **引用名**: `ArtiOsAlarmClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsAlarmClass.

######## 2. ArtiOsAlarmClassStateRef

- **UUID**: `51627aa2-5d77-4936-b4c0-8f7a31ee50c9`
- **引用名**: `ArtiOsAlarmClassStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsAlarmStateRef in ArtiOsAlarmInstances. This attribute specifies if an alarm is "RUNNING" or "STOPPED". The refered ArtiObjectClassParameter does include the mapping from integer to human readable "RUNNING" or "STOPPED".

##### 11. ArtiOsAlarmInstance

**容器属性**:

- **UUID**: `14e3d025-67ab-41b2-82f4-e5db983eac9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsAlarmInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an ArtiOsAlarm object, extending the EcuC OsTaskAlarm.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. ArtiOsAlarmInstanceAction

- **UUID**: `6c8a9e36-91a5-4e5d-827d-cbb671a64b39`
- **参数名**: `ArtiOsAlarmInstanceAction`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute provides a string with a description of the action when the alarm expires, e.g. "ActivateTask TaskA".

######## 2. ArtiOsAlarmInstanceCounter

- **UUID**: `fb6682af-490b-4a63-834a-a8aa6d48fee9`
- **参数名**: `ArtiOsAlarmInstanceCounter`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute provides a string containing the name of the counter used by this alarm.

###### 引用关系

此容器包含 **6** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsAlarmInstanceAlarmTimeRef

- **UUID**: `d045dd9d-5d12-4d2c-8557-5574a6660c0f`
- **引用名**: `ArtiOsAlarmInstanceAlarmTimeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This attribute specifies how to evaluate the time until the alarm expires next. The time should be represented in seconds.

######## 2. ArtiOsAlarmInstanceCycleTimeRef

- **UUID**: `890b3b18-b4cf-4129-b381-3ccfc8c78b7c`
- **引用名**: `ArtiOsAlarmInstanceCycleTimeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This attribute specifies how to evaluate the cycle time for cyclic alarms. The value of "cycle time" is 0 for non-cyclic alarms. The time should be represendet in seconds.

######## 3. ArtiOsAlarmInstanceEcuCRef

- **UUID**: `442280d1-fb7d-4efa-b302-80d88167143a`
- **引用名**: `ArtiOsAlarmInstanceEcuCRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an EcuC OsAlarm that is beeing extended.

######## 4. ArtiOsAlarmInstanceGenericComponentInstanceRef

- **UUID**: `6dd649b0-ed9b-44b3-839a-dd67c49e9fa6`
- **引用名**: `ArtiOsAlarmInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsAlarmInstance.

######## 5. ArtiOsAlarmInstanceStateRef

- **UUID**: `17afaf04-3812-499a-8d43-a34f934de357`
- **引用名**: `ArtiOsAlarmInstanceStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "state" of this alarm. The result then is mapped with the typemap of the ArtiOsAlarmStateRef of the ArtiOsAlarmClass.

######## 6. ArtiOsAlarmInstanceValidRef

- **UUID**: `0380140b-861f-4055-92f1-cb873bd26048`
- **引用名**: `ArtiOsAlarmInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this alarm. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 12. ArtiOsClass

**容器属性**:

- **UUID**: `2b22415b-e184-40c9-b360-1b25d75e7f80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "Os" object, extending the EcuC OsOS.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsClassAppModeRef

- **UUID**: `7b71f020-64f3-43e3-b67c-bfc22785b7a9`
- **引用名**: `ArtiOsClassAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiOsAppModeInstance parameter.

######## 2. ArtiOsClassGenericComponentRef

- **UUID**: `f0541cba-aad8-45ed-b9a6-1bd2eef85e75`
- **引用名**: `ArtiOsClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the OS description.

######## 3. ArtiOsClassServiceTraceRef

- **UUID**: `f58b9974-5e2f-4de7-91ef-dd7691264836`
- **引用名**: `ArtiOsClassServiceTraceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiOsInstanceServiceTrace parameter. This attribute indicates the entry or exit of a service routine and the ID of this service routine. The value of this attribute must be evaluated from one single memory location.

##### 13. ArtiOsContextClass

**容器属性**:

- **UUID**: `2d823e70-a607-471d-b19d-afa8576d4a32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsContextClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "OsContext" object.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsContextClassGenericComponentClassRef

- **UUID**: `59be4ef5-2db8-4db1-b3c5-d850b35c3f1e`
- **引用名**: `ArtiOsContextClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsContextClass.

##### 14. ArtiOsContextInstance

**容器属性**:

- **UUID**: `80a8f9bf-5e07-44ab-8880-28a52d8bdc19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsContextInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an "ArtiContext" object.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsContextInstanceAddressRef

- **UUID**: `54f89187-852e-4f80-812f-e48fbe43fa0d`
- **引用名**: `ArtiOsContextInstanceAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "address" of this context.

######## 2. ArtiOsContextInstanceGenericComponentInstanceRef

- **UUID**: `23938db4-bbf3-4ae5-ad95-296f79b16d6c`
- **引用名**: `ArtiOsContextInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsContext.

######## 3. ArtiOsContextInstanceSizeRef

- **UUID**: `96769bcd-c46a-42db-8f24-f5768700bdc1`
- **引用名**: `ArtiOsContextInstanceSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "size" of this context.

######## 4. ArtiOsContextInstanceValidRef

- **UUID**: `146ac2d4-0f2c-4409-b86e-fbb23be29098`
- **引用名**: `ArtiOsContextInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this context. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 15. ArtiOsInstance

**容器属性**:

- **UUID**: `75d6a881-c5de-420e-a93d-d4ef2a42ff18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsInstance`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Represents an instance of an ARTI "Os" object, extending the EcuC OsOS.

###### 引用关系

此容器包含 **6** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsInstanceAppModeRef

- **UUID**: `1894f4dc-432b-46fb-8903-5014d3edd198`
- **引用名**: `ArtiOsInstanceAppModeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "application mode" of this OS.

######## 2. ArtiOsInstanceEcucRef

- **UUID**: `53e05590-8021-4f0d-a655-927626abc426`
- **引用名**: `ArtiOsInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsOS`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsOS`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the EcucDefs/Os/OsOS of this OS.

######## 3. ArtiOsInstanceGenericComponentRef

- **UUID**: `60cc8e10-9d54-4c91-92b3-07027ff814fc`
- **引用名**: `ArtiOsInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OS.

######## 4. ArtiOsInstanceHookRef

- **UUID**: `8705d640-c9f4-4a82-9d39-d82b145e2c92`
- **引用名**: `ArtiOsInstanceHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiHook`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiHook`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a hook defined in the OS.

######## 5. ArtiOsInstanceServiceTraceRef

- **UUID**: `f2e1ea30-9167-4c2a-a1be-a2f87c5621b8`
- **引用名**: `ArtiOsInstanceServiceTraceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a hook defined in the OS.

######## 6. ArtiOsInstanceValidRef

- **UUID**: `a8d33bbc-d8c7-4d38-92d2-41f12e6fc8db`
- **引用名**: `ArtiOsInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 16. ArtiOsIsrClass

**容器属性**:

- **UUID**: `5792a9bd-8d2e-486b-ac25-f3e19060ecb6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsIsrClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "OsIsr" object, extending the EcuC OsIsr.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsIsrClassGenericComponentRef

- **UUID**: `565fecdb-50d0-4bed-9761-d1135472bd6c`
- **引用名**: `ArtiOsIsrClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an optional ArtiGenericComponentClass that extends the OsIsr with additional parameters.

##### 17. ArtiOsIsrInstance

**容器属性**:

- **UUID**: `45355954-0eee-49a5-afca-de458d29aecd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsIsrInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an ARTI "OsIsr" object, extending the EcuC OsIsr.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. ArtiOsIsrInstanceId

- **UUID**: `d182da57-0d5c-4135-aa38-dca157fd3775`
- **参数名**: `ArtiOsIsrInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter represents the "ISRID" as given by the OS, returned by GetISRID().

####### ENUMERATION 类型参数

######## 1. ArtiOsIsrInstanceCategory

- **UUID**: `fa58b723-f5ff-418f-8083-fb9b14b50db7`
- **参数名**: `ArtiOsIsrInstanceCategory`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CATEGORY_1` (来源: AUTOSAR_ECUC)
  - `CATEGORY_2` (来源: AUTOSAR_ECUC)
- **描述**: Specifies category of this ISR. If omitted the instance is related to a CATEGORY_2.

####### FUNCTION-NAME 类型参数

######## 1. ArtiOsIsrInstanceFunction

- **UUID**: `ee3a5aee-44e7-4b01-b0cb-a8076f9d0313`
- **参数名**: `ArtiOsIsrInstanceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter represents the C function name of the ISR routine.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsIsrInstanceEcucRef

- **UUID**: `c90951f2-ce27-409f-8543-d9b4acafbaae`
- **引用名**: `ArtiOsIsrInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsIsr`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsIsr`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the EcucDefs/Os/OsIsr of this ISR.

######## 2. ArtiOsIsrInstanceGenericComponentRef

- **UUID**: `35aa9890-6625-40e9-83aa-c09b65ff836d`
- **引用名**: `ArtiOsIsrInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an optional ArtiGenericComponentInstance that extends this OsIsr with additional parameters.

######## 3. ArtiOsIsrInstanceValidRef

- **UUID**: `495cf147-f919-49c8-a4e0-1b29ac8849e6`
- **引用名**: `ArtiOsIsrInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsIsrInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 18. ArtiOsMessageContainerClass

**容器属性**:

- **UUID**: `18da79e4-9d0e-4db0-a45e-96c280e05b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsMessageContainerClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "OsMessageContainer" object. The "OsMessageContainer" object represents an existing combination of OSEK messages.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsMessageContainerClassGenericComponentClassRef

- **UUID**: `1f502f6a-d94f-48cb-9a60-1512b1392f4f`
- **引用名**: `ArtiOsMessageContainerClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsMessageContainerClass.

##### 19. ArtiOsMessageContainerInstance

**容器属性**:

- **UUID**: `1f39e839-4b8b-4c61-8e6c-f303016fadd8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsMessageContainerInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an "ArtiMessageContainer" object.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. ArtiOsMessageContainerInstanceMsgName

- **UUID**: `e19dc328-c6c2-4c59-9137-ce89a3b5484c`
- **参数名**: `ArtiOsMessageContainerInstanceMsgName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute provides the name of the message as defined in OIL file.

######## 2. ArtiOsMessageContainerInstanceMsgType

- **UUID**: `e2bc4ba5-4cf9-493d-be5b-9d91b623d4ec`
- **参数名**: `ArtiOsMessageContainerInstanceMsgType`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute provides the type of the message.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsMessageContainerInstanceFirstElementRef

- **UUID**: `e42ef9a9-874a-4a78-b895-371173fb266b`
- **引用名**: `ArtiOsMessageContainerInstanceFirstElementRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "firstelement" of this "ArtiOsMessageContainer". This attribute provides the formula for evaluation of address of first valid message. This message will be received next. If no message is in the queue the value is zero.

######## 2. ArtiOsMessageContainerInstanceGenericComponentInstanceRef

- **UUID**: `e9427339-1727-4bb7-b2ea-889105fed005`
- **引用名**: `ArtiOsMessageContainerInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsMessageContainerInstance.

######## 3. ArtiOsMessageContainerInstanceQueueCountRef

- **UUID**: `e68efeea-7a3e-4de4-a52c-b1fe7ce0b9ac`
- **引用名**: `ArtiOsMessageContainerInstanceQueueCountRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "queuecount" of this "ArtiOsMessageContainer". This attribute provides the number of valid messages in the queue and "1" for unqueued messages.

######## 4. ArtiOsMessageContainerInstanceQueueSizeRef

- **UUID**: `fcde820f-aba6-4aeb-b61b-6fef5238b301`
- **引用名**: `ArtiOsMessageContainerInstanceQueueSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "queuesize" of this "ArtiOsMessageContainer". This attribute provides the size of the queue for queued messages and "1" for unqueued messages.

######## 5. ArtiOsMessageContainerInstanceValidRef

- **UUID**: `806093e3-29ba-4955-a746-7f6c4efe71f8`
- **引用名**: `ArtiOsMessageContainerInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsMessageContainerInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 20. ArtiOsResourceClass

**容器属性**:

- **UUID**: `f21de7e4-e46d-4a4e-be22-b5d574d1a245`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsResourceClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ArtiOsResource object. The ArtiOsResource object represents an OSEK resource.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsResourceClassGenericComponentClassRef

- **UUID**: `bee8f7b7-3d5d-4e1c-98b3-be62f0c1bfae`
- **引用名**: `ArtiOsResourceClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsResourceClass.

######## 2. ArtiOsResourceClassLockerRef

- **UUID**: `29c43115-ed0f-4293-9d02-5db49b984332`
- **引用名**: `ArtiOsResourceClassLockerRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsResourceLockerRef in ArtiOsResourceInstances. This attribute indicates the locking ArtiOsTaskInstance or ArtiOsIsrInstance.

######## 3. ArtiOsResourceClassStateRef

- **UUID**: `d2ac2895-ebca-449d-922d-6de8c235f4b7`
- **引用名**: `ArtiOsResourceClassStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsResourceStateRef in ArtiOsResourceInstances. This attribute represents the state of a resource ("LOCKED"/"UNLOCKED"). The ArtiObjectClassParameter does include the mapping from integer to human readable "LOCKED" or "UNLOCKED".

##### 21. ArtiOsResourceInstance

**容器属性**:

- **UUID**: `75c3064b-2a7e-482f-bbbb-a463cf355f03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsResourceInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an ArtiOsResource object.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiOsResourceInstancePriority

- **UUID**: `266c180a-c0c6-4686-a2af-74f79cdf7639`
- **参数名**: `ArtiOsResourceInstancePriority`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute has two components that state: that the RESOURCE is used by TASKs only or by TASKs and ISRs, and the priority that will be used when locking the RESOURCE.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsResourceInstanceEcuCRef

- **UUID**: `865d490d-5277-430c-ad97-3652eba99d83`
- **引用名**: `ArtiOsResourceInstanceEcuCRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an EcuC OsResource that is beeing extended.

######## 2. ArtiOsResourceInstanceGenericComponentInstanceRef

- **UUID**: `9cd554f4-3282-4e33-9a13-b806f04de97e`
- **引用名**: `ArtiOsResourceInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsResourceInstance.

######## 3. ArtiOsResourceInstanceLockerRef

- **UUID**: `1c5221b4-e4cd-411c-b185-064faa2f8e35`
- **引用名**: `ArtiOsResourceInstanceLockerRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "locker" of this ArtiOsResource.

######## 4. ArtiOsResourceInstanceStateRef

- **UUID**: `0c6d91b9-09f6-47d8-a91c-77547a94b278`
- **引用名**: `ArtiOsResourceInstanceStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "state" of this ArtiOsResource.

######## 5. ArtiOsResourceInstanceValidRef

- **UUID**: `78a293fc-77df-4da3-a493-0377aef33ce7`
- **引用名**: `ArtiOsResourceInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsResourceInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 22. ArtiOsStackClass

**容器属性**:

- **UUID**: `362e5858-b128-4875-9a0c-d52805b881ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsStackClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ArtiOsStack object. The ArtiOsStack object defines the memory area of any stack in the system.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsStackClassGenericComponentClassRef

- **UUID**: `f8e55f56-4a8a-4475-a31e-8c0e179884e4`
- **引用名**: `ArtiOsStackClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiOsStackClass.

##### 23. ArtiOsStackInstance

**容器属性**:

- **UUID**: `c243161f-cb41-44e7-91a3-d0b2d66feec0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsStackInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an ArtiOsStack object.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiOsStackInstanceDirection

- **UUID**: `1ac82a0e-f709-442d-b2e9-70566932d987`
- **参数名**: `ArtiOsStackInstanceDirection`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This attribute specifies the direction of stack growth and may have either "UP" or "DOWN" as its value. UP means growing from lower to higher addresses. DOWN means growing from higher addresses to lower addresses.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsStackInstanceBaseAddressRef

- **UUID**: `9ca238b8-2f28-4027-a56a-841a59eb0977`
- **引用名**: `ArtiOsStackInstanceBaseAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "baseaddress" of this ArtiOsStack. This attribute specifies the lowest address of stack memory area, regardless of the stack direction.

######## 2. ArtiOsStackInstanceFillPatternRef

- **UUID**: `d8bddf2d-51be-4838-bac3-fcad16830e2b`
- **引用名**: `ArtiOsStackInstanceFillPatternRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "fillpattern" of this ArtiOsStack. If the operating system fills the stack during initialisation, this attribute specifies with which pattern the stack area is initialised. This allows the debugger to evaluate the maximum stack usage. For "stackdirection" "DOWN" the pattern starts at "baseaddress". For "stackdirection" "UP" the pattern starts at "baseaddress" + "size". If no pattern is used, this attribute must be omitted.

######## 3. ArtiOsStackInstanceGenericComponentInstanceRef

- **UUID**: `eaa700b4-3edd-45c7-a641-e2aaa8d40b47`
- **引用名**: `ArtiOsStackInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiOsStackInstance.

######## 4. ArtiOsStackInstanceSizeRef

- **UUID**: `0a3e9ed9-8a07-4012-99a3-9c17b5f3368b`
- **引用名**: `ArtiOsStackInstanceSizeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "size" of this ArtiOsStack. This attribute represents the size (in bytes) of the memory area allocated for stack.

######## 5. ArtiOsStackInstanceValidRef

- **UUID**: `0d750424-f610-4f46-8e8c-25b3cf42d50c`
- **引用名**: `ArtiOsStackInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsStackInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 24. ArtiOsTaskClass

**容器属性**:

- **UUID**: `0c36f049-272a-4dca-a9da-601525f017d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsTaskClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ARTI "OsTask" object, extending the EcuC OsTask.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsTaskClassClassGenericComponentRef

- **UUID**: `0d713ec7-d99c-49f6-9553-4e68dd1c3c6b`
- **引用名**: `ArtiOsTaskClassClassGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the OsTask.

######## 2. ArtiOsTaskClassContextRef

- **UUID**: `a3eaf2a0-db1d-4aae-91ce-a858af062dfd`
- **引用名**: `ArtiOsTaskClassContextRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: ArtiOsTaskContextRef in ArtiOsTaskInstances. This attribute contains a reference to the context object that the task is currently using.

######## 3. ArtiOsTaskClassCurrentTaskStateRef

- **UUID**: `b8429894-3f45-41a7-8dcb-29451c58de4c`
- **引用名**: `ArtiOsTaskClassCurrentTaskStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that defines the ArtiCurrentTaskStateInstance parameter including the task state mapping.

######## 4. ArtiOsTaskClassPriorityRef

- **UUID**: `4dd2db8b-2002-4280-bf58-a5bc39827dd5`
- **引用名**: `ArtiOsTaskClassPriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsTaskPriorityRef in ArtiOsTaskInstances. This attribute represents the current priority of the TASK object. The current priority can be different from the static task priority as a result of priority ceiling protocol. The priority displayed is the priority as defined in the OsTask.

######## 5. ArtiOsTaskClassStackRef

- **UUID**: `2bc48f8d-0c30-489a-a4b4-38428ade7308`
- **引用名**: `ArtiOsTaskClassStackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiOsTaskStackRef in ArtiOsTaskInstances. This attribute contains a reference to the stack object that the task is currently using.

##### 25. ArtiOsTaskInstance

**容器属性**:

- **UUID**: `86223bb3-c182-4a6d-9186-a9f733bac0d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiOsTaskInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Represents an instance of an ARTI "OsTask" object, extending the EcuC OsTask.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. ArtiOsTaskInstanceId

- **UUID**: `c51f0dc6-be2b-435f-9502-57fa80a7c82c`
- **参数名**: `ArtiOsTaskInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter represents the "TaskID" as given by the OSEK OS, returned by GetTaskID().

####### FUNCTION-NAME 类型参数

######## 1. ArtiOsTaskInstanceFunction

- **UUID**: `f9d0e68d-5a96-4836-b9d0-9f5848b86ba4`
- **参数名**: `ArtiOsTaskInstanceFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter represents the C function name of the task body.

###### 引用关系

此容器包含 **8** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiOsTaskInstanceContextRef

- **UUID**: `81d6a1ad-f676-4bfd-9c9c-8b385b4f94cf`
- **引用名**: `ArtiOsTaskInstanceContextRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the ArtiOsContext of this ArtiOsTask.

######## 2. ArtiOsTaskInstanceCurrentActivationsRef

- **UUID**: `67f80508-105f-4df8-a94b-5d638212e419`
- **引用名**: `ArtiOsTaskInstanceCurrentActivationsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current activations" of this task. This attribute specifies the number of current activations for the task.

######## 3. ArtiOsTaskInstanceCurrentTaskStateRef

- **UUID**: `8813a8c9-1f71-494f-a612-7a90f9cd2340`
- **引用名**: `ArtiOsTaskInstanceCurrentTaskStateRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "current state" of this task.

######## 4. ArtiOsTaskInstanceEcucRef

- **UUID**: `cd8c34be-65e8-43e2-b67b-0b0bf0f3057e`
- **引用名**: `ArtiOsTaskInstanceEcucRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OsTask.

######## 5. ArtiOsTaskInstanceGenericComponentRef

- **UUID**: `738951ca-3cc0-4a91-b077-90d66828ef03`
- **引用名**: `ArtiOsTaskInstanceGenericComponentRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the OsTask.

######## 6. ArtiOsTaskInstancePriorityRef

- **UUID**: `8a8bcbc3-a939-4d46-8c30-03c26d38d5bd`
- **引用名**: `ArtiOsTaskInstancePriorityRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "task priority" of this task.

######## 7. ArtiOsTaskInstanceStackRef

- **UUID**: `34c87203-331f-4aae-84a2-ab38177462ce`
- **引用名**: `ArtiOsTaskInstanceStackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the ArtiOsStack of this ArtiOsTask.

######## 8. ArtiOsTaskInstanceValidRef

- **UUID**: `b51ece07-dd02-44e6-990d-eacc3fba9610`
- **引用名**: `ArtiOsTaskInstanceValidRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiObjectInstanceParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectInstanceParameter`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectInstanceParameter that contains the evaluation for the "validity" of this ArtiOsTaskInstance. Every object declaration may contain a VALID attribute telling the debugger whether the object's attributes are currently valid. It may have an integer type of any size. Its possible values are 0 (invalid) and non zero (object is valid).

##### 26. ArtiRte

**容器属性**:

- **UUID**: `118dee09-46c1-4e0d-b7fe-39e0d6878104`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRte`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

The ArtiRte Container contains all parameters for ARTI that are filled by the generators RTE.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiRteHookRef

- **UUID**: `ca569315-6806-4b00-9fed-9ecaaa62ec7a`
- **引用名**: `ArtiRteHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ArtiHook`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiHook`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an arti hook which is called by the RTE.

###### 配置容器

本模块包含 **20** 个配置容器：

####### 1. ArtiRteRunnableClass

**容器属性**:

- **UUID**: `3a282322-e000-446d-a44b-b4647b64c03b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteRunnableClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ArtiRteRunnable object.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiRteRunnableClassGenericComponentClassRef

- **UUID**: `9b74b214-47c0-4073-9cb2-61d6116db78a`
- **引用名**: `ArtiRteRunnableClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiRteRunnableClass.

########## 2. ArtiRteRunnableIdRef

- **UUID**: `b6baf292-af43-4258-99b8-6ef495e37c05`
- **引用名**: `ArtiRteRunnableIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiRteRunnableIdRef in ArtiRteRunnableEntityInstances. This attribute specifies the idOf(reName) mapping.

####### 2. ArtiRteRunnableInstance

**容器属性**:

- **UUID**: `b137973a-b4ea-4157-91b7-f5bc45806c4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteRunnableInstance`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Represents an instance of an ArtiRteRunnable object, extending the BswM RunnableEntity.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiRteRunnableInstanceSymbol

- **UUID**: `a466a2d3-eae1-4452-a967-4020c43eb72d`
- **参数名**: `ArtiRteRunnableInstanceSymbol`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the symbol / function name that implements the runnable.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiRteRunnableInstanceGenericComponentInstanceRef

- **UUID**: `1ea4bd6f-06b2-4a3a-9fcd-34e3b33daf5f`
- **引用名**: `ArtiRteRunnableInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiRteRunnableInstance.

######### FOREIGN-REFERENCE 类型引用

########## 1. ArtiRteRunnableInstanceBswRef

- **UUID**: `f8c91e6e-7901-40bf-8701-ed80411909dc`
- **引用名**: `ArtiRteRunnableInstanceBswRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: RUNNABLE-ENTITY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an Rte Runnable that is beeing extended.

####### 3. ArtiRteSchedulableClass

**容器属性**:

- **UUID**: `4955e62e-a786-46c5-93b0-45ab77b73510`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteSchedulableClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ArtiRteSchedulable object.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiRteSchedulableClassGenericComponentClassRef

- **UUID**: `1aac1781-1e9a-44fb-a7f1-493763ce2d3a`
- **引用名**: `ArtiRteSchedulableClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiRteSchedulableClass.

########## 2. ArtiRteSchedulableIdRef

- **UUID**: `214837c1-aecc-4599-b40d-d2a6ae885686`
- **引用名**: `ArtiRteSchedulableIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiRteSchmEntityIdRef in ArtiRteSchedulableInstances. This attribute specifies the idOf(entityName) mapping.

####### 4. ArtiRteSchedulableInstance

**容器属性**:

- **UUID**: `ece9579c-1543-4d21-b160-1ffed4bfbe3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteSchedulableInstance`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Represents an instance of an ArtiRteSchedulable object, extending the Rte Schedulable Entity.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiRteSchedulableInstanceSymbol

- **UUID**: `f0521884-c9dc-47b0-9128-ba7f08a0f5cd`
- **参数名**: `ArtiRteSchedulableInstanceSymbol`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the symbol / function name that implements the schedulable.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiRteSchedulableInstanceGenericComponentInstanceRef

- **UUID**: `37730e71-adb9-4bbb-a52e-3a9d4d94b7f7`
- **引用名**: `ArtiRteSchedulableInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiRteSchedulableInstance.

######### FOREIGN-REFERENCE 类型引用

########## 1. ArtiRteSchedulableInstanceBswRef

- **UUID**: `61ffda40-b905-4f85-a045-b775c9e3440e`
- **引用名**: `ArtiRteSchedulableInstanceBswRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-SCHEDULABLE-ENITIY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an Rte Schedulable that is beeing extended.

####### 5. ArtiRteVfbTraceHooks

**容器属性**:

- **UUID**: `a8fd9920-af1e-43cd-9926-0f78ea34dd52`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteVfbTraceHooks`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container defines the parent container to which all trace hook containers are added.

######## 配置容器

本模块包含 **15** 个配置容器：

######### 1. RteVfbTraceHook

**容器属性**:

- **UUID**: `819aff16-a8d0-4d22-b1be-3fe8a862546a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHook`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents a specific VFB Trace hook. Its ShortName equals the hook function's C symbol.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. RteVfbTraceHookType

- **UUID**: `3b3e8388-89af-45cb-aa5c-053e80a4cd43`
- **参数名**: `RteVfbTraceHookType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BSW_SCHEDULABLE_ENTITY_INVOCATION` (来源: AUTOSAR_ECUC)
  - `BSW_SCHEDULABLE_ENTITY_TERMINATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_CALLBACK` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_GROUP_INVALIDATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_INVALIDATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_RECEPTION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `OS_RECEIVED_EVENT` (来源: AUTOSAR_ECUC)
  - `OS_SET_EVENT` (来源: AUTOSAR_ECUC)
  - `OS_TASK_ACTIVATION` (来源: AUTOSAR_ECUC)
  - `OS_TASK_DISPATCH` (来源: AUTOSAR_ECUC)
  - `OS_TASK_TERMINATION` (来源: AUTOSAR_ECUC)
  - `OS_WAIT_EVENT` (来源: AUTOSAR_ECUC)
  - `RPT_RECEPTION` (来源: AUTOSAR_ECUC)
  - `RPT_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `RTE_API_RETURN` (来源: AUTOSAR_ECUC)
  - `RTE_API_START` (来源: AUTOSAR_ECUC)
  - `RUNNABLE_ENTITY_INVOCATION` (来源: AUTOSAR_ECUC)
  - `RUNNABLE_ENTITY_TERMINATION` (来源: AUTOSAR_ECUC)
  - `SCHM_API_RETURN` (来源: AUTOSAR_ECUC)
  - `SCHM_API_START` (来源: AUTOSAR_ECUC)
- **描述**: This specifies the type of the hook.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookEntryRef

- **UUID**: `26b7d8d1-39da-40cf-8194-7fdfd2d87cae`
- **引用名**: `RteVfbTraceHookEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswModuleEntry of this VFB Trace hook in the BSWMD of the generated RTE

########## 配置容器

本模块包含 **14** 个配置容器：

########### 1. RteVfbTraceHookAccessPoint

**容器属性**:

- **UUID**: `b8b0c337-438a-4561-b757-37f2a14ee9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookAccessPoint`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook the ShortName of this container is the Access Point name part of the VFB Trace hook (<ap> in SWS_Rte).

############ 引用关系

此容器包含 **1** 个引用：

############# FOREIGN-REFERENCE 类型引用

############## 1. RteVfbTraceHookAccessPointElementRef

- **UUID**: `1bd1a5fb-b3a2-4d3e-b6d3-1123d4c7b6d1`
- **引用名**: `RteVfbTraceHookAccessPointElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the Access Point was derived. Number and type of the referenced objects depend on the API.

########### 2. RteVfbTraceHookApi

**容器属性**:

- **UUID**: `daf86f41-1ece-433f-abad-c0ab6c957b34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookApi`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or RTE API Trace hook the ShortName of this container is the API name part of the VFB Trace hook (<api> in SWS_Rte).

########### 3. RteVfbTraceHookBswSchedulerNamePrefix

**容器属性**:

- **UUID**: `9ec33780-e7e8-4105-9be8-a010022f82b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookBswSchedulerNamePrefix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the BSW Scheduler Name Prefix name part of the VFB Trace hook (<bsnp> in SWS_Rte).

############ 引用关系

此容器包含 **1** 个引用：

############# FOREIGN-REFERENCE 类型引用

############## 1. RteVfbTraceHookBswImplementationRef

- **UUID**: `f69fee6d-7696-4559-b37c-16a057f1979b`
- **引用名**: `RteVfbTraceHookBswImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-IMPLEMENTATION
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswImplementation from which the BSW Scheduler Name Prefix was derived

########### 4. RteVfbTraceHookComHookEvent

**容器属性**:

- **UUID**: `ecf0f0fd-f216-4175-b2f4-76048da60ceb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComHookEvent`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM hook event part of the VFB Trace hook (<Event> in SWS_Rte).

########### 5. RteVfbTraceHookComponentTypeSymbol

**容器属性**:

- **UUID**: `c5292f94-70a2-45ec-824f-3b19bf9dcf30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComponentTypeSymbol`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook, Runnable Entity Trace hook or RPT Trace hook the ShortName of this container is the component type symbol name part of the VFB Trace hook (<cts> in SWS_Rte).

############ 引用关系

此容器包含 **1** 个引用：

############# FOREIGN-REFERENCE 类型引用

############## 1. RteVfbTraceHookSwComponentTypeRef

- **UUID**: `1275eddf-2775-4703-a204-30f8dc2e6ab3`
- **引用名**: `RteVfbTraceHookSwComponentTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SW-COMPONENT-TYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the SwComponentType from which the component type symbol was derived

########### 6. RteVfbTraceHookExecutableEntityName

**容器属性**:

- **UUID**: `3ace6444-52fd-4866-8af3-fcd52f04936b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookExecutableEntityName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a Runnable Entity Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the Executable Entity name part of the VFB Trace hook (<reName> or <entityName> in SWS_Rte).

############ 引用关系

此容器包含 **1** 个引用：

############# FOREIGN-REFERENCE 类型引用

############## 1. RteVfbTraceHookExecutableEntityRef

- **UUID**: `e66c5b76-45ab-4529-8e9d-a3212e6be18f`
- **引用名**: `RteVfbTraceHookExecutableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: EXECUTABLE-ENTITY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the Executable Entity from which the Runnable Entity or BSW Schedulable Entity name was derived

########### 7. RteVfbTraceHookName

**容器属性**:

- **UUID**: `bc536993-54bf-4a65-a30e-12ae16a321d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook the ShortName of this container is the "Name provided by the API" name part of the VFB Trace hook (<name> in SWS_Rte).

############ 引用关系

此容器包含 **1** 个引用：

############# FOREIGN-REFERENCE 类型引用

############## 1. RteVfbTraceHookNameElementRef

- **UUID**: `3088ee3a-e773-4553-85d5-145411bf877b`
- **引用名**: `RteVfbTraceHookNameElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "Name provided by the API" was derived. Number and type of the referenced objects depend on the API.

########### 8. RteVfbTraceHookOsApplication

**容器属性**:

- **UUID**: `fb985108-7ed2-41af-8161-b53d93c42b96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookOsApplication`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the application name part of the VFB Trace hook (<application> in SWS_Rte).

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. RteVfbTraceHookOsApplicationRef

- **UUID**: `acbf0a2c-968b-4397-91d3-4a22286c0344`
- **引用名**: `RteVfbTraceHookOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsApplication from which the application name was derived

########### 9. RteVfbTraceHookSignal

**容器属性**:

- **UUID**: `bb599798-9fe2-47cf-86ef-f750e7a17c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignal`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal name part of the VFB Trace hook (<signalName> in SWS_Rte).

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. RteVfbTraceHookSignalRef

- **UUID**: `ab810aff-ec5d-408e-9e10-90d8874fec14`
- **引用名**: `RteVfbTraceHookSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignal from which the signal name was derived

########### 10. RteVfbTraceHookSignalGroup

**容器属性**:

- **UUID**: `e29f3e25-bdf6-482f-b2ef-2f1875e74b63`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignalGroup`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal group name part of the VFB Trace hook (<signalGroupName> in SWS_Rte).

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. RteVfbTraceHookSignalGroupRef

- **UUID**: `3fd0ac7b-eece-42da-a1ce-b3ce863a0b39`
- **引用名**: `RteVfbTraceHookSignalGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignalGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignalGroup from which the signal group name was derived

########### 11. RteVfbTraceHookTask

**容器属性**:

- **UUID**: `6d17d5ff-f556-4afb-99fe-2476c301f5e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookTask`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the task name part of the VFB Trace hook (<task> in SWS_Rte).

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. RteVfbTraceHookTaskRef

- **UUID**: `ae32a6a1-fbbb-49eb-8c43-fd60d9d50746`
- **引用名**: `RteVfbTraceHookTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsTask from which the task name was derived

########### 12. RteVfbTraceHookVariable

**容器属性**:

- **UUID**: `0d9bfa5e-93ff-4fc0-870c-28c2729b1324`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVariable`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RPT Trace hook the ShortName of this container is the "identifying name of the RP global buffer" name part of the VFB Trace hook (<var> in SWS_Rte).

############ 引用关系

此容器包含 **1** 个引用：

############# FOREIGN-REFERENCE 类型引用

############## 1. RteVfbTraceHookVariableElementRef

- **UUID**: `b2b73c20-8800-43ad-a0e8-5b2313e5ee4b`
- **引用名**: `RteVfbTraceHookVariableElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "identifying name of the RP global buffer" was derived. Number and type of the referenced objects depend on the API.

########### 13. RteVfbTraceHookVendorApiInfix

**容器属性**:

- **UUID**: `4640d6c7-281d-4035-bea4-7d87cd105f44`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorApiInfix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorApiInfix name part of the VFB Trace hook (<ai> in SWS_Rte).

########### 14. RteVfbTraceHookVendorId

**容器属性**:

- **UUID**: `c86d6ef5-a80d-4d6e-a77d-d85a42a00c75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorId`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorId name part of the VFB Trace hook (<vi> in SWS_Rte).

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. RteVfbTraceHookVendorIdIntegerValue

- **UUID**: `fae3fbc4-1f14-4d50-8c86-5eb8da66a211`
- **参数名**: `RteVfbTraceHookVendorIdIntegerValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The VendorId as Integer parameter.

This parameter is an extension to ECUC_Rte_09188.
It is required to work around an AUTOSAR inconsistency: 
  - AUTOSAR defines the VendorId as Integer value
  - AUTOSAR defines that shortnames shall not begin with an Integer.
Therefore, it is impossible to pass the VendorId as shortname of the container.

######### 2. RteVfbTraceHookAccessPoint

**容器属性**:

- **UUID**: `b8b0c337-438a-4561-b757-37f2a14ee9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookAccessPoint`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook the ShortName of this container is the Access Point name part of the VFB Trace hook (<ap> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookAccessPointElementRef

- **UUID**: `1bd1a5fb-b3a2-4d3e-b6d3-1123d4c7b6d1`
- **引用名**: `RteVfbTraceHookAccessPointElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the Access Point was derived. Number and type of the referenced objects depend on the API.

######### 3. RteVfbTraceHookApi

**容器属性**:

- **UUID**: `daf86f41-1ece-433f-abad-c0ab6c957b34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookApi`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or RTE API Trace hook the ShortName of this container is the API name part of the VFB Trace hook (<api> in SWS_Rte).

######### 4. RteVfbTraceHookBswSchedulerNamePrefix

**容器属性**:

- **UUID**: `9ec33780-e7e8-4105-9be8-a010022f82b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookBswSchedulerNamePrefix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the BSW Scheduler Name Prefix name part of the VFB Trace hook (<bsnp> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookBswImplementationRef

- **UUID**: `f69fee6d-7696-4559-b37c-16a057f1979b`
- **引用名**: `RteVfbTraceHookBswImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-IMPLEMENTATION
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswImplementation from which the BSW Scheduler Name Prefix was derived

######### 5. RteVfbTraceHookComHookEvent

**容器属性**:

- **UUID**: `ecf0f0fd-f216-4175-b2f4-76048da60ceb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComHookEvent`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM hook event part of the VFB Trace hook (<Event> in SWS_Rte).

######### 6. RteVfbTraceHookComponentTypeSymbol

**容器属性**:

- **UUID**: `c5292f94-70a2-45ec-824f-3b19bf9dcf30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComponentTypeSymbol`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook, Runnable Entity Trace hook or RPT Trace hook the ShortName of this container is the component type symbol name part of the VFB Trace hook (<cts> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookSwComponentTypeRef

- **UUID**: `1275eddf-2775-4703-a204-30f8dc2e6ab3`
- **引用名**: `RteVfbTraceHookSwComponentTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SW-COMPONENT-TYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the SwComponentType from which the component type symbol was derived

######### 7. RteVfbTraceHookExecutableEntityName

**容器属性**:

- **UUID**: `3ace6444-52fd-4866-8af3-fcd52f04936b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookExecutableEntityName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a Runnable Entity Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the Executable Entity name part of the VFB Trace hook (<reName> or <entityName> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookExecutableEntityRef

- **UUID**: `e66c5b76-45ab-4529-8e9d-a3212e6be18f`
- **引用名**: `RteVfbTraceHookExecutableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: EXECUTABLE-ENTITY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the Executable Entity from which the Runnable Entity or BSW Schedulable Entity name was derived

######### 8. RteVfbTraceHookName

**容器属性**:

- **UUID**: `bc536993-54bf-4a65-a30e-12ae16a321d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook the ShortName of this container is the "Name provided by the API" name part of the VFB Trace hook (<name> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookNameElementRef

- **UUID**: `3088ee3a-e773-4553-85d5-145411bf877b`
- **引用名**: `RteVfbTraceHookNameElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "Name provided by the API" was derived. Number and type of the referenced objects depend on the API.

######### 9. RteVfbTraceHookOsApplication

**容器属性**:

- **UUID**: `fb985108-7ed2-41af-8161-b53d93c42b96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookOsApplication`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the application name part of the VFB Trace hook (<application> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookOsApplicationRef

- **UUID**: `acbf0a2c-968b-4397-91d3-4a22286c0344`
- **引用名**: `RteVfbTraceHookOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsApplication from which the application name was derived

######### 10. RteVfbTraceHookSignal

**容器属性**:

- **UUID**: `bb599798-9fe2-47cf-86ef-f750e7a17c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignal`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal name part of the VFB Trace hook (<signalName> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookSignalRef

- **UUID**: `ab810aff-ec5d-408e-9e10-90d8874fec14`
- **引用名**: `RteVfbTraceHookSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignal from which the signal name was derived

######### 11. RteVfbTraceHookSignalGroup

**容器属性**:

- **UUID**: `e29f3e25-bdf6-482f-b2ef-2f1875e74b63`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignalGroup`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal group name part of the VFB Trace hook (<signalGroupName> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookSignalGroupRef

- **UUID**: `3fd0ac7b-eece-42da-a1ce-b3ce863a0b39`
- **引用名**: `RteVfbTraceHookSignalGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignalGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignalGroup from which the signal group name was derived

######### 12. RteVfbTraceHookTask

**容器属性**:

- **UUID**: `6d17d5ff-f556-4afb-99fe-2476c301f5e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookTask`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the task name part of the VFB Trace hook (<task> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookTaskRef

- **UUID**: `ae32a6a1-fbbb-49eb-8c43-fd60d9d50746`
- **引用名**: `RteVfbTraceHookTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsTask from which the task name was derived

######### 13. RteVfbTraceHookVariable

**容器属性**:

- **UUID**: `0d9bfa5e-93ff-4fc0-870c-28c2729b1324`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVariable`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RPT Trace hook the ShortName of this container is the "identifying name of the RP global buffer" name part of the VFB Trace hook (<var> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookVariableElementRef

- **UUID**: `b2b73c20-8800-43ad-a0e8-5b2313e5ee4b`
- **引用名**: `RteVfbTraceHookVariableElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "identifying name of the RP global buffer" was derived. Number and type of the referenced objects depend on the API.

######### 14. RteVfbTraceHookVendorApiInfix

**容器属性**:

- **UUID**: `4640d6c7-281d-4035-bea4-7d87cd105f44`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorApiInfix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorApiInfix name part of the VFB Trace hook (<ai> in SWS_Rte).

######### 15. RteVfbTraceHookVendorId

**容器属性**:

- **UUID**: `c86d6ef5-a80d-4d6e-a77d-d85a42a00c75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorId`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorId name part of the VFB Trace hook (<vi> in SWS_Rte).

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. RteVfbTraceHookVendorIdIntegerValue

- **UUID**: `fae3fbc4-1f14-4d50-8c86-5eb8da66a211`
- **参数名**: `RteVfbTraceHookVendorIdIntegerValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The VendorId as Integer parameter.

This parameter is an extension to ECUC_Rte_09188.
It is required to work around an AUTOSAR inconsistency: 
  - AUTOSAR defines the VendorId as Integer value
  - AUTOSAR defines that shortnames shall not begin with an Integer.
Therefore, it is impossible to pass the VendorId as shortname of the container.

####### 6. RteVfbTraceHook

**容器属性**:

- **UUID**: `819aff16-a8d0-4d22-b1be-3fe8a862546a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHook`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents a specific VFB Trace hook. Its ShortName equals the hook function's C symbol.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. RteVfbTraceHookType

- **UUID**: `3b3e8388-89af-45cb-aa5c-053e80a4cd43`
- **参数名**: `RteVfbTraceHookType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BSW_SCHEDULABLE_ENTITY_INVOCATION` (来源: AUTOSAR_ECUC)
  - `BSW_SCHEDULABLE_ENTITY_TERMINATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_CALLBACK` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_GROUP_INVALIDATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_INVALIDATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_RECEPTION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `OS_RECEIVED_EVENT` (来源: AUTOSAR_ECUC)
  - `OS_SET_EVENT` (来源: AUTOSAR_ECUC)
  - `OS_TASK_ACTIVATION` (来源: AUTOSAR_ECUC)
  - `OS_TASK_DISPATCH` (来源: AUTOSAR_ECUC)
  - `OS_TASK_TERMINATION` (来源: AUTOSAR_ECUC)
  - `OS_WAIT_EVENT` (来源: AUTOSAR_ECUC)
  - `RPT_RECEPTION` (来源: AUTOSAR_ECUC)
  - `RPT_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `RTE_API_RETURN` (来源: AUTOSAR_ECUC)
  - `RTE_API_START` (来源: AUTOSAR_ECUC)
  - `RUNNABLE_ENTITY_INVOCATION` (来源: AUTOSAR_ECUC)
  - `RUNNABLE_ENTITY_TERMINATION` (来源: AUTOSAR_ECUC)
  - `SCHM_API_RETURN` (来源: AUTOSAR_ECUC)
  - `SCHM_API_START` (来源: AUTOSAR_ECUC)
- **描述**: This specifies the type of the hook.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookEntryRef

- **UUID**: `26b7d8d1-39da-40cf-8194-7fdfd2d87cae`
- **引用名**: `RteVfbTraceHookEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswModuleEntry of this VFB Trace hook in the BSWMD of the generated RTE

######## 配置容器

本模块包含 **14** 个配置容器：

######### 1. RteVfbTraceHookAccessPoint

**容器属性**:

- **UUID**: `b8b0c337-438a-4561-b757-37f2a14ee9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookAccessPoint`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook the ShortName of this container is the Access Point name part of the VFB Trace hook (<ap> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookAccessPointElementRef

- **UUID**: `1bd1a5fb-b3a2-4d3e-b6d3-1123d4c7b6d1`
- **引用名**: `RteVfbTraceHookAccessPointElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the Access Point was derived. Number and type of the referenced objects depend on the API.

######### 2. RteVfbTraceHookApi

**容器属性**:

- **UUID**: `daf86f41-1ece-433f-abad-c0ab6c957b34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookApi`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or RTE API Trace hook the ShortName of this container is the API name part of the VFB Trace hook (<api> in SWS_Rte).

######### 3. RteVfbTraceHookBswSchedulerNamePrefix

**容器属性**:

- **UUID**: `9ec33780-e7e8-4105-9be8-a010022f82b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookBswSchedulerNamePrefix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the BSW Scheduler Name Prefix name part of the VFB Trace hook (<bsnp> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookBswImplementationRef

- **UUID**: `f69fee6d-7696-4559-b37c-16a057f1979b`
- **引用名**: `RteVfbTraceHookBswImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-IMPLEMENTATION
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswImplementation from which the BSW Scheduler Name Prefix was derived

######### 4. RteVfbTraceHookComHookEvent

**容器属性**:

- **UUID**: `ecf0f0fd-f216-4175-b2f4-76048da60ceb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComHookEvent`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM hook event part of the VFB Trace hook (<Event> in SWS_Rte).

######### 5. RteVfbTraceHookComponentTypeSymbol

**容器属性**:

- **UUID**: `c5292f94-70a2-45ec-824f-3b19bf9dcf30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComponentTypeSymbol`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook, Runnable Entity Trace hook or RPT Trace hook the ShortName of this container is the component type symbol name part of the VFB Trace hook (<cts> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookSwComponentTypeRef

- **UUID**: `1275eddf-2775-4703-a204-30f8dc2e6ab3`
- **引用名**: `RteVfbTraceHookSwComponentTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SW-COMPONENT-TYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the SwComponentType from which the component type symbol was derived

######### 6. RteVfbTraceHookExecutableEntityName

**容器属性**:

- **UUID**: `3ace6444-52fd-4866-8af3-fcd52f04936b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookExecutableEntityName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a Runnable Entity Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the Executable Entity name part of the VFB Trace hook (<reName> or <entityName> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookExecutableEntityRef

- **UUID**: `e66c5b76-45ab-4529-8e9d-a3212e6be18f`
- **引用名**: `RteVfbTraceHookExecutableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: EXECUTABLE-ENTITY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the Executable Entity from which the Runnable Entity or BSW Schedulable Entity name was derived

######### 7. RteVfbTraceHookName

**容器属性**:

- **UUID**: `bc536993-54bf-4a65-a30e-12ae16a321d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook the ShortName of this container is the "Name provided by the API" name part of the VFB Trace hook (<name> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookNameElementRef

- **UUID**: `3088ee3a-e773-4553-85d5-145411bf877b`
- **引用名**: `RteVfbTraceHookNameElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "Name provided by the API" was derived. Number and type of the referenced objects depend on the API.

######### 8. RteVfbTraceHookOsApplication

**容器属性**:

- **UUID**: `fb985108-7ed2-41af-8161-b53d93c42b96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookOsApplication`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the application name part of the VFB Trace hook (<application> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookOsApplicationRef

- **UUID**: `acbf0a2c-968b-4397-91d3-4a22286c0344`
- **引用名**: `RteVfbTraceHookOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsApplication from which the application name was derived

######### 9. RteVfbTraceHookSignal

**容器属性**:

- **UUID**: `bb599798-9fe2-47cf-86ef-f750e7a17c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignal`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal name part of the VFB Trace hook (<signalName> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookSignalRef

- **UUID**: `ab810aff-ec5d-408e-9e10-90d8874fec14`
- **引用名**: `RteVfbTraceHookSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignal from which the signal name was derived

######### 10. RteVfbTraceHookSignalGroup

**容器属性**:

- **UUID**: `e29f3e25-bdf6-482f-b2ef-2f1875e74b63`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignalGroup`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal group name part of the VFB Trace hook (<signalGroupName> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookSignalGroupRef

- **UUID**: `3fd0ac7b-eece-42da-a1ce-b3ce863a0b39`
- **引用名**: `RteVfbTraceHookSignalGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignalGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignalGroup from which the signal group name was derived

######### 11. RteVfbTraceHookTask

**容器属性**:

- **UUID**: `6d17d5ff-f556-4afb-99fe-2476c301f5e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookTask`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the task name part of the VFB Trace hook (<task> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookTaskRef

- **UUID**: `ae32a6a1-fbbb-49eb-8c43-fd60d9d50746`
- **引用名**: `RteVfbTraceHookTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsTask from which the task name was derived

######### 12. RteVfbTraceHookVariable

**容器属性**:

- **UUID**: `0d9bfa5e-93ff-4fc0-870c-28c2729b1324`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVariable`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RPT Trace hook the ShortName of this container is the "identifying name of the RP global buffer" name part of the VFB Trace hook (<var> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookVariableElementRef

- **UUID**: `b2b73c20-8800-43ad-a0e8-5b2313e5ee4b`
- **引用名**: `RteVfbTraceHookVariableElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "identifying name of the RP global buffer" was derived. Number and type of the referenced objects depend on the API.

######### 13. RteVfbTraceHookVendorApiInfix

**容器属性**:

- **UUID**: `4640d6c7-281d-4035-bea4-7d87cd105f44`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorApiInfix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorApiInfix name part of the VFB Trace hook (<ai> in SWS_Rte).

######### 14. RteVfbTraceHookVendorId

**容器属性**:

- **UUID**: `c86d6ef5-a80d-4d6e-a77d-d85a42a00c75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorId`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorId name part of the VFB Trace hook (<vi> in SWS_Rte).

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. RteVfbTraceHookVendorIdIntegerValue

- **UUID**: `fae3fbc4-1f14-4d50-8c86-5eb8da66a211`
- **参数名**: `RteVfbTraceHookVendorIdIntegerValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The VendorId as Integer parameter.

This parameter is an extension to ECUC_Rte_09188.
It is required to work around an AUTOSAR inconsistency: 
  - AUTOSAR defines the VendorId as Integer value
  - AUTOSAR defines that shortnames shall not begin with an Integer.
Therefore, it is impossible to pass the VendorId as shortname of the container.

####### 7. RteVfbTraceHookAccessPoint

**容器属性**:

- **UUID**: `b8b0c337-438a-4561-b757-37f2a14ee9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookAccessPoint`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook the ShortName of this container is the Access Point name part of the VFB Trace hook (<ap> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookAccessPointElementRef

- **UUID**: `1bd1a5fb-b3a2-4d3e-b6d3-1123d4c7b6d1`
- **引用名**: `RteVfbTraceHookAccessPointElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the Access Point was derived. Number and type of the referenced objects depend on the API.

####### 8. RteVfbTraceHookApi

**容器属性**:

- **UUID**: `daf86f41-1ece-433f-abad-c0ab6c957b34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookApi`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or RTE API Trace hook the ShortName of this container is the API name part of the VFB Trace hook (<api> in SWS_Rte).

####### 9. RteVfbTraceHookBswSchedulerNamePrefix

**容器属性**:

- **UUID**: `9ec33780-e7e8-4105-9be8-a010022f82b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookBswSchedulerNamePrefix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the BSW Scheduler Name Prefix name part of the VFB Trace hook (<bsnp> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookBswImplementationRef

- **UUID**: `f69fee6d-7696-4559-b37c-16a057f1979b`
- **引用名**: `RteVfbTraceHookBswImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-IMPLEMENTATION
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswImplementation from which the BSW Scheduler Name Prefix was derived

####### 10. RteVfbTraceHookComHookEvent

**容器属性**:

- **UUID**: `ecf0f0fd-f216-4175-b2f4-76048da60ceb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComHookEvent`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM hook event part of the VFB Trace hook (<Event> in SWS_Rte).

####### 11. RteVfbTraceHookComponentTypeSymbol

**容器属性**:

- **UUID**: `c5292f94-70a2-45ec-824f-3b19bf9dcf30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComponentTypeSymbol`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook, Runnable Entity Trace hook or RPT Trace hook the ShortName of this container is the component type symbol name part of the VFB Trace hook (<cts> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookSwComponentTypeRef

- **UUID**: `1275eddf-2775-4703-a204-30f8dc2e6ab3`
- **引用名**: `RteVfbTraceHookSwComponentTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SW-COMPONENT-TYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the SwComponentType from which the component type symbol was derived

####### 12. RteVfbTraceHookExecutableEntityName

**容器属性**:

- **UUID**: `3ace6444-52fd-4866-8af3-fcd52f04936b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookExecutableEntityName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a Runnable Entity Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the Executable Entity name part of the VFB Trace hook (<reName> or <entityName> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookExecutableEntityRef

- **UUID**: `e66c5b76-45ab-4529-8e9d-a3212e6be18f`
- **引用名**: `RteVfbTraceHookExecutableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: EXECUTABLE-ENTITY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the Executable Entity from which the Runnable Entity or BSW Schedulable Entity name was derived

####### 13. RteVfbTraceHookName

**容器属性**:

- **UUID**: `bc536993-54bf-4a65-a30e-12ae16a321d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook the ShortName of this container is the "Name provided by the API" name part of the VFB Trace hook (<name> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookNameElementRef

- **UUID**: `3088ee3a-e773-4553-85d5-145411bf877b`
- **引用名**: `RteVfbTraceHookNameElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "Name provided by the API" was derived. Number and type of the referenced objects depend on the API.

####### 14. RteVfbTraceHookOsApplication

**容器属性**:

- **UUID**: `fb985108-7ed2-41af-8161-b53d93c42b96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookOsApplication`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the application name part of the VFB Trace hook (<application> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookOsApplicationRef

- **UUID**: `acbf0a2c-968b-4397-91d3-4a22286c0344`
- **引用名**: `RteVfbTraceHookOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsApplication from which the application name was derived

####### 15. RteVfbTraceHookSignal

**容器属性**:

- **UUID**: `bb599798-9fe2-47cf-86ef-f750e7a17c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignal`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal name part of the VFB Trace hook (<signalName> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookSignalRef

- **UUID**: `ab810aff-ec5d-408e-9e10-90d8874fec14`
- **引用名**: `RteVfbTraceHookSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignal from which the signal name was derived

####### 16. RteVfbTraceHookSignalGroup

**容器属性**:

- **UUID**: `e29f3e25-bdf6-482f-b2ef-2f1875e74b63`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignalGroup`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal group name part of the VFB Trace hook (<signalGroupName> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookSignalGroupRef

- **UUID**: `3fd0ac7b-eece-42da-a1ce-b3ce863a0b39`
- **引用名**: `RteVfbTraceHookSignalGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignalGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignalGroup from which the signal group name was derived

####### 17. RteVfbTraceHookTask

**容器属性**:

- **UUID**: `6d17d5ff-f556-4afb-99fe-2476c301f5e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookTask`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the task name part of the VFB Trace hook (<task> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookTaskRef

- **UUID**: `ae32a6a1-fbbb-49eb-8c43-fd60d9d50746`
- **引用名**: `RteVfbTraceHookTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsTask from which the task name was derived

####### 18. RteVfbTraceHookVariable

**容器属性**:

- **UUID**: `0d9bfa5e-93ff-4fc0-870c-28c2729b1324`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVariable`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RPT Trace hook the ShortName of this container is the "identifying name of the RP global buffer" name part of the VFB Trace hook (<var> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookVariableElementRef

- **UUID**: `b2b73c20-8800-43ad-a0e8-5b2313e5ee4b`
- **引用名**: `RteVfbTraceHookVariableElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "identifying name of the RP global buffer" was derived. Number and type of the referenced objects depend on the API.

####### 19. RteVfbTraceHookVendorApiInfix

**容器属性**:

- **UUID**: `4640d6c7-281d-4035-bea4-7d87cd105f44`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorApiInfix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorApiInfix name part of the VFB Trace hook (<ai> in SWS_Rte).

####### 20. RteVfbTraceHookVendorId

**容器属性**:

- **UUID**: `c86d6ef5-a80d-4d6e-a77d-d85a42a00c75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorId`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorId name part of the VFB Trace hook (<vi> in SWS_Rte).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. RteVfbTraceHookVendorIdIntegerValue

- **UUID**: `fae3fbc4-1f14-4d50-8c86-5eb8da66a211`
- **参数名**: `RteVfbTraceHookVendorIdIntegerValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The VendorId as Integer parameter.

This parameter is an extension to ECUC_Rte_09188.
It is required to work around an AUTOSAR inconsistency: 
  - AUTOSAR defines the VendorId as Integer value
  - AUTOSAR defines that shortnames shall not begin with an Integer.
Therefore, it is impossible to pass the VendorId as shortname of the container.

##### 27. ArtiRteRunnableClass

**容器属性**:

- **UUID**: `3a282322-e000-446d-a44b-b4647b64c03b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteRunnableClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ArtiRteRunnable object.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiRteRunnableClassGenericComponentClassRef

- **UUID**: `9b74b214-47c0-4073-9cb2-61d6116db78a`
- **引用名**: `ArtiRteRunnableClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiRteRunnableClass.

######## 2. ArtiRteRunnableIdRef

- **UUID**: `b6baf292-af43-4258-99b8-6ef495e37c05`
- **引用名**: `ArtiRteRunnableIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiRteRunnableIdRef in ArtiRteRunnableEntityInstances. This attribute specifies the idOf(reName) mapping.

##### 28. ArtiRteRunnableInstance

**容器属性**:

- **UUID**: `b137973a-b4ea-4157-91b7-f5bc45806c4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteRunnableInstance`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Represents an instance of an ArtiRteRunnable object, extending the BswM RunnableEntity.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiRteRunnableInstanceSymbol

- **UUID**: `a466a2d3-eae1-4452-a967-4020c43eb72d`
- **参数名**: `ArtiRteRunnableInstanceSymbol`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the symbol / function name that implements the runnable.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiRteRunnableInstanceGenericComponentInstanceRef

- **UUID**: `1ea4bd6f-06b2-4a3a-9fcd-34e3b33daf5f`
- **引用名**: `ArtiRteRunnableInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiRteRunnableInstance.

####### FOREIGN-REFERENCE 类型引用

######## 1. ArtiRteRunnableInstanceBswRef

- **UUID**: `f8c91e6e-7901-40bf-8701-ed80411909dc`
- **引用名**: `ArtiRteRunnableInstanceBswRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: RUNNABLE-ENTITY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an Rte Runnable that is beeing extended.

##### 29. ArtiRteSchedulableClass

**容器属性**:

- **UUID**: `4955e62e-a786-46c5-93b0-45ab77b73510`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteSchedulableClass`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Contains the layout of an ArtiRteSchedulable object.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiRteSchedulableClassGenericComponentClassRef

- **UUID**: `1aac1781-1e9a-44fb-a7f1-493763ce2d3a`
- **引用名**: `ArtiRteSchedulableClassGenericComponentClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentClass`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentClass`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentClass that extends the ArtiRteSchedulableClass.

######## 2. ArtiRteSchedulableIdRef

- **UUID**: `214837c1-aecc-4599-b40d-d2a6ae885686`
- **引用名**: `ArtiRteSchedulableIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ArtiObjectClassParameter`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiObjectClassParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the ArtiObjectClassParameter that declares the attribute ArtiRteSchmEntityIdRef in ArtiRteSchedulableInstances. This attribute specifies the idOf(entityName) mapping.

##### 30. ArtiRteSchedulableInstance

**容器属性**:

- **UUID**: `ece9579c-1543-4d21-b160-1ffed4bfbe3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteSchedulableInstance`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Represents an instance of an ArtiRteSchedulable object, extending the Rte Schedulable Entity.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiRteSchedulableInstanceSymbol

- **UUID**: `f0521884-c9dc-47b0-9128-ba7f08a0f5cd`
- **参数名**: `ArtiRteSchedulableInstanceSymbol`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the symbol / function name that implements the schedulable.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiRteSchedulableInstanceGenericComponentInstanceRef

- **UUID**: `37730e71-adb9-4bbb-a52e-3a9d4d94b7f7`
- **引用名**: `ArtiRteSchedulableInstanceGenericComponentInstanceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiGenericComponentInstance`
- **完整路径**: `/MICROSAR/Arti/ArtiGeneric/ArtiGenericComponentInstance`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an ArtiGenericComponentInstance that extends the ArtiRteSchedulableInstance.

####### FOREIGN-REFERENCE 类型引用

######## 1. ArtiRteSchedulableInstanceBswRef

- **UUID**: `61ffda40-b905-4f85-a045-b775c9e3440e`
- **引用名**: `ArtiRteSchedulableInstanceBswRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-SCHEDULABLE-ENITIY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an Rte Schedulable that is beeing extended.

##### 31. ArtiRteVfbTraceHooks

**容器属性**:

- **UUID**: `a8fd9920-af1e-43cd-9926-0f78ea34dd52`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiRteVfbTraceHooks`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container defines the parent container to which all trace hook containers are added.

###### 配置容器

本模块包含 **15** 个配置容器：

####### 1. RteVfbTraceHook

**容器属性**:

- **UUID**: `819aff16-a8d0-4d22-b1be-3fe8a862546a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHook`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents a specific VFB Trace hook. Its ShortName equals the hook function's C symbol.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. RteVfbTraceHookType

- **UUID**: `3b3e8388-89af-45cb-aa5c-053e80a4cd43`
- **参数名**: `RteVfbTraceHookType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BSW_SCHEDULABLE_ENTITY_INVOCATION` (来源: AUTOSAR_ECUC)
  - `BSW_SCHEDULABLE_ENTITY_TERMINATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_CALLBACK` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_GROUP_INVALIDATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_INVALIDATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_RECEPTION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `OS_RECEIVED_EVENT` (来源: AUTOSAR_ECUC)
  - `OS_SET_EVENT` (来源: AUTOSAR_ECUC)
  - `OS_TASK_ACTIVATION` (来源: AUTOSAR_ECUC)
  - `OS_TASK_DISPATCH` (来源: AUTOSAR_ECUC)
  - `OS_TASK_TERMINATION` (来源: AUTOSAR_ECUC)
  - `OS_WAIT_EVENT` (来源: AUTOSAR_ECUC)
  - `RPT_RECEPTION` (来源: AUTOSAR_ECUC)
  - `RPT_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `RTE_API_RETURN` (来源: AUTOSAR_ECUC)
  - `RTE_API_START` (来源: AUTOSAR_ECUC)
  - `RUNNABLE_ENTITY_INVOCATION` (来源: AUTOSAR_ECUC)
  - `RUNNABLE_ENTITY_TERMINATION` (来源: AUTOSAR_ECUC)
  - `SCHM_API_RETURN` (来源: AUTOSAR_ECUC)
  - `SCHM_API_START` (来源: AUTOSAR_ECUC)
- **描述**: This specifies the type of the hook.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookEntryRef

- **UUID**: `26b7d8d1-39da-40cf-8194-7fdfd2d87cae`
- **引用名**: `RteVfbTraceHookEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswModuleEntry of this VFB Trace hook in the BSWMD of the generated RTE

######## 配置容器

本模块包含 **14** 个配置容器：

######### 1. RteVfbTraceHookAccessPoint

**容器属性**:

- **UUID**: `b8b0c337-438a-4561-b757-37f2a14ee9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookAccessPoint`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook the ShortName of this container is the Access Point name part of the VFB Trace hook (<ap> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookAccessPointElementRef

- **UUID**: `1bd1a5fb-b3a2-4d3e-b6d3-1123d4c7b6d1`
- **引用名**: `RteVfbTraceHookAccessPointElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the Access Point was derived. Number and type of the referenced objects depend on the API.

######### 2. RteVfbTraceHookApi

**容器属性**:

- **UUID**: `daf86f41-1ece-433f-abad-c0ab6c957b34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookApi`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or RTE API Trace hook the ShortName of this container is the API name part of the VFB Trace hook (<api> in SWS_Rte).

######### 3. RteVfbTraceHookBswSchedulerNamePrefix

**容器属性**:

- **UUID**: `9ec33780-e7e8-4105-9be8-a010022f82b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookBswSchedulerNamePrefix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the BSW Scheduler Name Prefix name part of the VFB Trace hook (<bsnp> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookBswImplementationRef

- **UUID**: `f69fee6d-7696-4559-b37c-16a057f1979b`
- **引用名**: `RteVfbTraceHookBswImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-IMPLEMENTATION
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswImplementation from which the BSW Scheduler Name Prefix was derived

######### 4. RteVfbTraceHookComHookEvent

**容器属性**:

- **UUID**: `ecf0f0fd-f216-4175-b2f4-76048da60ceb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComHookEvent`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM hook event part of the VFB Trace hook (<Event> in SWS_Rte).

######### 5. RteVfbTraceHookComponentTypeSymbol

**容器属性**:

- **UUID**: `c5292f94-70a2-45ec-824f-3b19bf9dcf30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComponentTypeSymbol`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook, Runnable Entity Trace hook or RPT Trace hook the ShortName of this container is the component type symbol name part of the VFB Trace hook (<cts> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookSwComponentTypeRef

- **UUID**: `1275eddf-2775-4703-a204-30f8dc2e6ab3`
- **引用名**: `RteVfbTraceHookSwComponentTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SW-COMPONENT-TYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the SwComponentType from which the component type symbol was derived

######### 6. RteVfbTraceHookExecutableEntityName

**容器属性**:

- **UUID**: `3ace6444-52fd-4866-8af3-fcd52f04936b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookExecutableEntityName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a Runnable Entity Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the Executable Entity name part of the VFB Trace hook (<reName> or <entityName> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookExecutableEntityRef

- **UUID**: `e66c5b76-45ab-4529-8e9d-a3212e6be18f`
- **引用名**: `RteVfbTraceHookExecutableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: EXECUTABLE-ENTITY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the Executable Entity from which the Runnable Entity or BSW Schedulable Entity name was derived

######### 7. RteVfbTraceHookName

**容器属性**:

- **UUID**: `bc536993-54bf-4a65-a30e-12ae16a321d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook the ShortName of this container is the "Name provided by the API" name part of the VFB Trace hook (<name> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookNameElementRef

- **UUID**: `3088ee3a-e773-4553-85d5-145411bf877b`
- **引用名**: `RteVfbTraceHookNameElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "Name provided by the API" was derived. Number and type of the referenced objects depend on the API.

######### 8. RteVfbTraceHookOsApplication

**容器属性**:

- **UUID**: `fb985108-7ed2-41af-8161-b53d93c42b96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookOsApplication`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the application name part of the VFB Trace hook (<application> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookOsApplicationRef

- **UUID**: `acbf0a2c-968b-4397-91d3-4a22286c0344`
- **引用名**: `RteVfbTraceHookOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsApplication from which the application name was derived

######### 9. RteVfbTraceHookSignal

**容器属性**:

- **UUID**: `bb599798-9fe2-47cf-86ef-f750e7a17c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignal`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal name part of the VFB Trace hook (<signalName> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookSignalRef

- **UUID**: `ab810aff-ec5d-408e-9e10-90d8874fec14`
- **引用名**: `RteVfbTraceHookSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignal from which the signal name was derived

######### 10. RteVfbTraceHookSignalGroup

**容器属性**:

- **UUID**: `e29f3e25-bdf6-482f-b2ef-2f1875e74b63`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignalGroup`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal group name part of the VFB Trace hook (<signalGroupName> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookSignalGroupRef

- **UUID**: `3fd0ac7b-eece-42da-a1ce-b3ce863a0b39`
- **引用名**: `RteVfbTraceHookSignalGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignalGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignalGroup from which the signal group name was derived

######### 11. RteVfbTraceHookTask

**容器属性**:

- **UUID**: `6d17d5ff-f556-4afb-99fe-2476c301f5e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookTask`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the task name part of the VFB Trace hook (<task> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. RteVfbTraceHookTaskRef

- **UUID**: `ae32a6a1-fbbb-49eb-8c43-fd60d9d50746`
- **引用名**: `RteVfbTraceHookTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsTask from which the task name was derived

######### 12. RteVfbTraceHookVariable

**容器属性**:

- **UUID**: `0d9bfa5e-93ff-4fc0-870c-28c2729b1324`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVariable`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RPT Trace hook the ShortName of this container is the "identifying name of the RP global buffer" name part of the VFB Trace hook (<var> in SWS_Rte).

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. RteVfbTraceHookVariableElementRef

- **UUID**: `b2b73c20-8800-43ad-a0e8-5b2313e5ee4b`
- **引用名**: `RteVfbTraceHookVariableElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "identifying name of the RP global buffer" was derived. Number and type of the referenced objects depend on the API.

######### 13. RteVfbTraceHookVendorApiInfix

**容器属性**:

- **UUID**: `4640d6c7-281d-4035-bea4-7d87cd105f44`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorApiInfix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorApiInfix name part of the VFB Trace hook (<ai> in SWS_Rte).

######### 14. RteVfbTraceHookVendorId

**容器属性**:

- **UUID**: `c86d6ef5-a80d-4d6e-a77d-d85a42a00c75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorId`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorId name part of the VFB Trace hook (<vi> in SWS_Rte).

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. RteVfbTraceHookVendorIdIntegerValue

- **UUID**: `fae3fbc4-1f14-4d50-8c86-5eb8da66a211`
- **参数名**: `RteVfbTraceHookVendorIdIntegerValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The VendorId as Integer parameter.

This parameter is an extension to ECUC_Rte_09188.
It is required to work around an AUTOSAR inconsistency: 
  - AUTOSAR defines the VendorId as Integer value
  - AUTOSAR defines that shortnames shall not begin with an Integer.
Therefore, it is impossible to pass the VendorId as shortname of the container.

####### 2. RteVfbTraceHookAccessPoint

**容器属性**:

- **UUID**: `b8b0c337-438a-4561-b757-37f2a14ee9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookAccessPoint`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook the ShortName of this container is the Access Point name part of the VFB Trace hook (<ap> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookAccessPointElementRef

- **UUID**: `1bd1a5fb-b3a2-4d3e-b6d3-1123d4c7b6d1`
- **引用名**: `RteVfbTraceHookAccessPointElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the Access Point was derived. Number and type of the referenced objects depend on the API.

####### 3. RteVfbTraceHookApi

**容器属性**:

- **UUID**: `daf86f41-1ece-433f-abad-c0ab6c957b34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookApi`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or RTE API Trace hook the ShortName of this container is the API name part of the VFB Trace hook (<api> in SWS_Rte).

####### 4. RteVfbTraceHookBswSchedulerNamePrefix

**容器属性**:

- **UUID**: `9ec33780-e7e8-4105-9be8-a010022f82b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookBswSchedulerNamePrefix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the BSW Scheduler Name Prefix name part of the VFB Trace hook (<bsnp> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookBswImplementationRef

- **UUID**: `f69fee6d-7696-4559-b37c-16a057f1979b`
- **引用名**: `RteVfbTraceHookBswImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-IMPLEMENTATION
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswImplementation from which the BSW Scheduler Name Prefix was derived

####### 5. RteVfbTraceHookComHookEvent

**容器属性**:

- **UUID**: `ecf0f0fd-f216-4175-b2f4-76048da60ceb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComHookEvent`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM hook event part of the VFB Trace hook (<Event> in SWS_Rte).

####### 6. RteVfbTraceHookComponentTypeSymbol

**容器属性**:

- **UUID**: `c5292f94-70a2-45ec-824f-3b19bf9dcf30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComponentTypeSymbol`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook, Runnable Entity Trace hook or RPT Trace hook the ShortName of this container is the component type symbol name part of the VFB Trace hook (<cts> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookSwComponentTypeRef

- **UUID**: `1275eddf-2775-4703-a204-30f8dc2e6ab3`
- **引用名**: `RteVfbTraceHookSwComponentTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SW-COMPONENT-TYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the SwComponentType from which the component type symbol was derived

####### 7. RteVfbTraceHookExecutableEntityName

**容器属性**:

- **UUID**: `3ace6444-52fd-4866-8af3-fcd52f04936b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookExecutableEntityName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a Runnable Entity Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the Executable Entity name part of the VFB Trace hook (<reName> or <entityName> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookExecutableEntityRef

- **UUID**: `e66c5b76-45ab-4529-8e9d-a3212e6be18f`
- **引用名**: `RteVfbTraceHookExecutableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: EXECUTABLE-ENTITY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the Executable Entity from which the Runnable Entity or BSW Schedulable Entity name was derived

####### 8. RteVfbTraceHookName

**容器属性**:

- **UUID**: `bc536993-54bf-4a65-a30e-12ae16a321d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook the ShortName of this container is the "Name provided by the API" name part of the VFB Trace hook (<name> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookNameElementRef

- **UUID**: `3088ee3a-e773-4553-85d5-145411bf877b`
- **引用名**: `RteVfbTraceHookNameElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "Name provided by the API" was derived. Number and type of the referenced objects depend on the API.

####### 9. RteVfbTraceHookOsApplication

**容器属性**:

- **UUID**: `fb985108-7ed2-41af-8161-b53d93c42b96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookOsApplication`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the application name part of the VFB Trace hook (<application> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookOsApplicationRef

- **UUID**: `acbf0a2c-968b-4397-91d3-4a22286c0344`
- **引用名**: `RteVfbTraceHookOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsApplication from which the application name was derived

####### 10. RteVfbTraceHookSignal

**容器属性**:

- **UUID**: `bb599798-9fe2-47cf-86ef-f750e7a17c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignal`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal name part of the VFB Trace hook (<signalName> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookSignalRef

- **UUID**: `ab810aff-ec5d-408e-9e10-90d8874fec14`
- **引用名**: `RteVfbTraceHookSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignal from which the signal name was derived

####### 11. RteVfbTraceHookSignalGroup

**容器属性**:

- **UUID**: `e29f3e25-bdf6-482f-b2ef-2f1875e74b63`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignalGroup`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal group name part of the VFB Trace hook (<signalGroupName> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookSignalGroupRef

- **UUID**: `3fd0ac7b-eece-42da-a1ce-b3ce863a0b39`
- **引用名**: `RteVfbTraceHookSignalGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignalGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignalGroup from which the signal group name was derived

####### 12. RteVfbTraceHookTask

**容器属性**:

- **UUID**: `6d17d5ff-f556-4afb-99fe-2476c301f5e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookTask`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the task name part of the VFB Trace hook (<task> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookTaskRef

- **UUID**: `ae32a6a1-fbbb-49eb-8c43-fd60d9d50746`
- **引用名**: `RteVfbTraceHookTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsTask from which the task name was derived

####### 13. RteVfbTraceHookVariable

**容器属性**:

- **UUID**: `0d9bfa5e-93ff-4fc0-870c-28c2729b1324`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVariable`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RPT Trace hook the ShortName of this container is the "identifying name of the RP global buffer" name part of the VFB Trace hook (<var> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookVariableElementRef

- **UUID**: `b2b73c20-8800-43ad-a0e8-5b2313e5ee4b`
- **引用名**: `RteVfbTraceHookVariableElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "identifying name of the RP global buffer" was derived. Number and type of the referenced objects depend on the API.

####### 14. RteVfbTraceHookVendorApiInfix

**容器属性**:

- **UUID**: `4640d6c7-281d-4035-bea4-7d87cd105f44`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorApiInfix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorApiInfix name part of the VFB Trace hook (<ai> in SWS_Rte).

####### 15. RteVfbTraceHookVendorId

**容器属性**:

- **UUID**: `c86d6ef5-a80d-4d6e-a77d-d85a42a00c75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorId`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorId name part of the VFB Trace hook (<vi> in SWS_Rte).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. RteVfbTraceHookVendorIdIntegerValue

- **UUID**: `fae3fbc4-1f14-4d50-8c86-5eb8da66a211`
- **参数名**: `RteVfbTraceHookVendorIdIntegerValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The VendorId as Integer parameter.

This parameter is an extension to ECUC_Rte_09188.
It is required to work around an AUTOSAR inconsistency: 
  - AUTOSAR defines the VendorId as Integer value
  - AUTOSAR defines that shortnames shall not begin with an Integer.
Therefore, it is impossible to pass the VendorId as shortname of the container.

##### 32. RteVfbTraceHook

**容器属性**:

- **UUID**: `819aff16-a8d0-4d22-b1be-3fe8a862546a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHook`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents a specific VFB Trace hook. Its ShortName equals the hook function's C symbol.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. RteVfbTraceHookType

- **UUID**: `3b3e8388-89af-45cb-aa5c-053e80a4cd43`
- **参数名**: `RteVfbTraceHookType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BSW_SCHEDULABLE_ENTITY_INVOCATION` (来源: AUTOSAR_ECUC)
  - `BSW_SCHEDULABLE_ENTITY_TERMINATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_CALLBACK` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_GROUP_INVALIDATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_INVALIDATION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_RECEPTION` (来源: AUTOSAR_ECUC)
  - `COM_SIGNAL_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `OS_RECEIVED_EVENT` (来源: AUTOSAR_ECUC)
  - `OS_SET_EVENT` (来源: AUTOSAR_ECUC)
  - `OS_TASK_ACTIVATION` (来源: AUTOSAR_ECUC)
  - `OS_TASK_DISPATCH` (来源: AUTOSAR_ECUC)
  - `OS_TASK_TERMINATION` (来源: AUTOSAR_ECUC)
  - `OS_WAIT_EVENT` (来源: AUTOSAR_ECUC)
  - `RPT_RECEPTION` (来源: AUTOSAR_ECUC)
  - `RPT_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `RTE_API_RETURN` (来源: AUTOSAR_ECUC)
  - `RTE_API_START` (来源: AUTOSAR_ECUC)
  - `RUNNABLE_ENTITY_INVOCATION` (来源: AUTOSAR_ECUC)
  - `RUNNABLE_ENTITY_TERMINATION` (来源: AUTOSAR_ECUC)
  - `SCHM_API_RETURN` (来源: AUTOSAR_ECUC)
  - `SCHM_API_START` (来源: AUTOSAR_ECUC)
- **描述**: This specifies the type of the hook.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteVfbTraceHookEntryRef

- **UUID**: `26b7d8d1-39da-40cf-8194-7fdfd2d87cae`
- **引用名**: `RteVfbTraceHookEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswModuleEntry of this VFB Trace hook in the BSWMD of the generated RTE

###### 配置容器

本模块包含 **14** 个配置容器：

####### 1. RteVfbTraceHookAccessPoint

**容器属性**:

- **UUID**: `b8b0c337-438a-4561-b757-37f2a14ee9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookAccessPoint`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook the ShortName of this container is the Access Point name part of the VFB Trace hook (<ap> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookAccessPointElementRef

- **UUID**: `1bd1a5fb-b3a2-4d3e-b6d3-1123d4c7b6d1`
- **引用名**: `RteVfbTraceHookAccessPointElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the Access Point was derived. Number and type of the referenced objects depend on the API.

####### 2. RteVfbTraceHookApi

**容器属性**:

- **UUID**: `daf86f41-1ece-433f-abad-c0ab6c957b34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookApi`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or RTE API Trace hook the ShortName of this container is the API name part of the VFB Trace hook (<api> in SWS_Rte).

####### 3. RteVfbTraceHookBswSchedulerNamePrefix

**容器属性**:

- **UUID**: `9ec33780-e7e8-4105-9be8-a010022f82b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookBswSchedulerNamePrefix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the BSW Scheduler Name Prefix name part of the VFB Trace hook (<bsnp> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookBswImplementationRef

- **UUID**: `f69fee6d-7696-4559-b37c-16a057f1979b`
- **引用名**: `RteVfbTraceHookBswImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-IMPLEMENTATION
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswImplementation from which the BSW Scheduler Name Prefix was derived

####### 4. RteVfbTraceHookComHookEvent

**容器属性**:

- **UUID**: `ecf0f0fd-f216-4175-b2f4-76048da60ceb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComHookEvent`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM hook event part of the VFB Trace hook (<Event> in SWS_Rte).

####### 5. RteVfbTraceHookComponentTypeSymbol

**容器属性**:

- **UUID**: `c5292f94-70a2-45ec-824f-3b19bf9dcf30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComponentTypeSymbol`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook, Runnable Entity Trace hook or RPT Trace hook the ShortName of this container is the component type symbol name part of the VFB Trace hook (<cts> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookSwComponentTypeRef

- **UUID**: `1275eddf-2775-4703-a204-30f8dc2e6ab3`
- **引用名**: `RteVfbTraceHookSwComponentTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SW-COMPONENT-TYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the SwComponentType from which the component type symbol was derived

####### 6. RteVfbTraceHookExecutableEntityName

**容器属性**:

- **UUID**: `3ace6444-52fd-4866-8af3-fcd52f04936b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookExecutableEntityName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a Runnable Entity Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the Executable Entity name part of the VFB Trace hook (<reName> or <entityName> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookExecutableEntityRef

- **UUID**: `e66c5b76-45ab-4529-8e9d-a3212e6be18f`
- **引用名**: `RteVfbTraceHookExecutableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: EXECUTABLE-ENTITY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the Executable Entity from which the Runnable Entity or BSW Schedulable Entity name was derived

####### 7. RteVfbTraceHookName

**容器属性**:

- **UUID**: `bc536993-54bf-4a65-a30e-12ae16a321d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook the ShortName of this container is the "Name provided by the API" name part of the VFB Trace hook (<name> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookNameElementRef

- **UUID**: `3088ee3a-e773-4553-85d5-145411bf877b`
- **引用名**: `RteVfbTraceHookNameElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "Name provided by the API" was derived. Number and type of the referenced objects depend on the API.

####### 8. RteVfbTraceHookOsApplication

**容器属性**:

- **UUID**: `fb985108-7ed2-41af-8161-b53d93c42b96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookOsApplication`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the application name part of the VFB Trace hook (<application> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookOsApplicationRef

- **UUID**: `acbf0a2c-968b-4397-91d3-4a22286c0344`
- **引用名**: `RteVfbTraceHookOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsApplication from which the application name was derived

####### 9. RteVfbTraceHookSignal

**容器属性**:

- **UUID**: `bb599798-9fe2-47cf-86ef-f750e7a17c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignal`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal name part of the VFB Trace hook (<signalName> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookSignalRef

- **UUID**: `ab810aff-ec5d-408e-9e10-90d8874fec14`
- **引用名**: `RteVfbTraceHookSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignal from which the signal name was derived

####### 10. RteVfbTraceHookSignalGroup

**容器属性**:

- **UUID**: `e29f3e25-bdf6-482f-b2ef-2f1875e74b63`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignalGroup`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal group name part of the VFB Trace hook (<signalGroupName> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookSignalGroupRef

- **UUID**: `3fd0ac7b-eece-42da-a1ce-b3ce863a0b39`
- **引用名**: `RteVfbTraceHookSignalGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignalGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignalGroup from which the signal group name was derived

####### 11. RteVfbTraceHookTask

**容器属性**:

- **UUID**: `6d17d5ff-f556-4afb-99fe-2476c301f5e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookTask`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the task name part of the VFB Trace hook (<task> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. RteVfbTraceHookTaskRef

- **UUID**: `ae32a6a1-fbbb-49eb-8c43-fd60d9d50746`
- **引用名**: `RteVfbTraceHookTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsTask from which the task name was derived

####### 12. RteVfbTraceHookVariable

**容器属性**:

- **UUID**: `0d9bfa5e-93ff-4fc0-870c-28c2729b1324`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVariable`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RPT Trace hook the ShortName of this container is the "identifying name of the RP global buffer" name part of the VFB Trace hook (<var> in SWS_Rte).

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. RteVfbTraceHookVariableElementRef

- **UUID**: `b2b73c20-8800-43ad-a0e8-5b2313e5ee4b`
- **引用名**: `RteVfbTraceHookVariableElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "identifying name of the RP global buffer" was derived. Number and type of the referenced objects depend on the API.

####### 13. RteVfbTraceHookVendorApiInfix

**容器属性**:

- **UUID**: `4640d6c7-281d-4035-bea4-7d87cd105f44`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorApiInfix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorApiInfix name part of the VFB Trace hook (<ai> in SWS_Rte).

####### 14. RteVfbTraceHookVendorId

**容器属性**:

- **UUID**: `c86d6ef5-a80d-4d6e-a77d-d85a42a00c75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorId`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorId name part of the VFB Trace hook (<vi> in SWS_Rte).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. RteVfbTraceHookVendorIdIntegerValue

- **UUID**: `fae3fbc4-1f14-4d50-8c86-5eb8da66a211`
- **参数名**: `RteVfbTraceHookVendorIdIntegerValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The VendorId as Integer parameter.

This parameter is an extension to ECUC_Rte_09188.
It is required to work around an AUTOSAR inconsistency: 
  - AUTOSAR defines the VendorId as Integer value
  - AUTOSAR defines that shortnames shall not begin with an Integer.
Therefore, it is impossible to pass the VendorId as shortname of the container.

##### 33. RteVfbTraceHookAccessPoint

**容器属性**:

- **UUID**: `b8b0c337-438a-4561-b757-37f2a14ee9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookAccessPoint`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook the ShortName of this container is the Access Point name part of the VFB Trace hook (<ap> in SWS_Rte).

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteVfbTraceHookAccessPointElementRef

- **UUID**: `1bd1a5fb-b3a2-4d3e-b6d3-1123d4c7b6d1`
- **引用名**: `RteVfbTraceHookAccessPointElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the Access Point was derived. Number and type of the referenced objects depend on the API.

##### 34. RteVfbTraceHookApi

**容器属性**:

- **UUID**: `daf86f41-1ece-433f-abad-c0ab6c957b34`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookApi`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or RTE API Trace hook the ShortName of this container is the API name part of the VFB Trace hook (<api> in SWS_Rte).

##### 35. RteVfbTraceHookBswSchedulerNamePrefix

**容器属性**:

- **UUID**: `9ec33780-e7e8-4105-9be8-a010022f82b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookBswSchedulerNamePrefix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the BSW Scheduler Name Prefix name part of the VFB Trace hook (<bsnp> in SWS_Rte).

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteVfbTraceHookBswImplementationRef

- **UUID**: `f69fee6d-7696-4559-b37c-16a057f1979b`
- **引用名**: `RteVfbTraceHookBswImplementationRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-IMPLEMENTATION
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswImplementation from which the BSW Scheduler Name Prefix was derived

##### 36. RteVfbTraceHookComHookEvent

**容器属性**:

- **UUID**: `ecf0f0fd-f216-4175-b2f4-76048da60ceb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComHookEvent`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM hook event part of the VFB Trace hook (<Event> in SWS_Rte).

##### 37. RteVfbTraceHookComponentTypeSymbol

**容器属性**:

- **UUID**: `c5292f94-70a2-45ec-824f-3b19bf9dcf30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookComponentTypeSymbol`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RTE API Trace hook, Runnable Entity Trace hook or RPT Trace hook the ShortName of this container is the component type symbol name part of the VFB Trace hook (<cts> in SWS_Rte).

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteVfbTraceHookSwComponentTypeRef

- **UUID**: `1275eddf-2775-4703-a204-30f8dc2e6ab3`
- **引用名**: `RteVfbTraceHookSwComponentTypeRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: SW-COMPONENT-TYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the SwComponentType from which the component type symbol was derived

##### 38. RteVfbTraceHookExecutableEntityName

**容器属性**:

- **UUID**: `3ace6444-52fd-4866-8af3-fcd52f04936b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookExecutableEntityName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a Runnable Entity Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the Executable Entity name part of the VFB Trace hook (<reName> or <entityName> in SWS_Rte).

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteVfbTraceHookExecutableEntityRef

- **UUID**: `e66c5b76-45ab-4529-8e9d-a3212e6be18f`
- **引用名**: `RteVfbTraceHookExecutableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: EXECUTABLE-ENTITY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the Executable Entity from which the Runnable Entity or BSW Schedulable Entity name was derived

##### 39. RteVfbTraceHookName

**容器属性**:

- **UUID**: `bc536993-54bf-4a65-a30e-12ae16a321d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookName`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook the ShortName of this container is the "Name provided by the API" name part of the VFB Trace hook (<name> in SWS_Rte).

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteVfbTraceHookNameElementRef

- **UUID**: `3088ee3a-e773-4553-85d5-145411bf877b`
- **引用名**: `RteVfbTraceHookNameElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "Name provided by the API" was derived. Number and type of the referenced objects depend on the API.

##### 40. RteVfbTraceHookOsApplication

**容器属性**:

- **UUID**: `fb985108-7ed2-41af-8161-b53d93c42b96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookOsApplication`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the application name part of the VFB Trace hook (<application> in SWS_Rte).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. RteVfbTraceHookOsApplicationRef

- **UUID**: `acbf0a2c-968b-4397-91d3-4a22286c0344`
- **引用名**: `RteVfbTraceHookOsApplicationRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsApplication`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsApplication`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsApplication from which the application name was derived

##### 41. RteVfbTraceHookSignal

**容器属性**:

- **UUID**: `bb599798-9fe2-47cf-86ef-f750e7a17c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignal`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal name part of the VFB Trace hook (<signalName> in SWS_Rte).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. RteVfbTraceHookSignalRef

- **UUID**: `ab810aff-ec5d-408e-9e10-90d8874fec14`
- **引用名**: `RteVfbTraceHookSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignal from which the signal name was derived

##### 42. RteVfbTraceHookSignalGroup

**容器属性**:

- **UUID**: `e29f3e25-bdf6-482f-b2ef-2f1875e74b63`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookSignalGroup`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a COM Trace hook the ShortName of this container is the COM signal group name part of the VFB Trace hook (<signalGroupName> in SWS_Rte).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. RteVfbTraceHookSignalGroupRef

- **UUID**: `3fd0ac7b-eece-42da-a1ce-b3ce863a0b39`
- **引用名**: `RteVfbTraceHookSignalGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignalGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ComSignalGroup from which the signal group name was derived

##### 43. RteVfbTraceHookTask

**容器属性**:

- **UUID**: `6d17d5ff-f556-4afb-99fe-2476c301f5e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookTask`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an OS Trace hook the ShortName of this container is the task name part of the VFB Trace hook (<task> in SWS_Rte).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. RteVfbTraceHookTaskRef

- **UUID**: `ae32a6a1-fbbb-49eb-8c43-fd60d9d50746`
- **引用名**: `RteVfbTraceHookTaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsTask`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsTask`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the OsTask from which the task name was derived

##### 44. RteVfbTraceHookVariable

**容器属性**:

- **UUID**: `0d9bfa5e-93ff-4fc0-870c-28c2729b1324`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVariable`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of an RPT Trace hook the ShortName of this container is the "identifying name of the RP global buffer" name part of the VFB Trace hook (<var> in SWS_Rte).

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. RteVfbTraceHookVariableElementRef

- **UUID**: `b2b73c20-8800-43ad-a0e8-5b2313e5ee4b`
- **引用名**: `RteVfbTraceHookVariableElementRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..infinite]
- **目标类型**: IDENTIFIABLE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the elements from which the "identifying name of the RP global buffer" was derived. Number and type of the referenced objects depend on the API.

##### 45. RteVfbTraceHookVendorApiInfix

**容器属性**:

- **UUID**: `4640d6c7-281d-4035-bea4-7d87cd105f44`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorApiInfix`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorApiInfix name part of the VFB Trace hook (<ai> in SWS_Rte).

##### 46. RteVfbTraceHookVendorId

**容器属性**:

- **UUID**: `c86d6ef5-a80d-4d6e-a77d-d85a42a00c75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RteVfbTraceHookVendorId`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

In case of a BSW Scheduler API Trace hook or BSW Schedulable Entities Trace hook the ShortName of this container is the optional VendorId name part of the VFB Trace hook (<vi> in SWS_Rte).

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. RteVfbTraceHookVendorIdIntegerValue

- **UUID**: `fae3fbc4-1f14-4d50-8c86-5eb8da66a211`
- **参数名**: `RteVfbTraceHookVendorIdIntegerValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The VendorId as Integer parameter.

This parameter is an extension to ECUC_Rte_09188.
It is required to work around an AUTOSAR inconsistency: 
  - AUTOSAR defines the VendorId as Integer value
  - AUTOSAR defines that shortnames shall not begin with an Integer.
Therefore, it is impossible to pass the VendorId as shortname of the container.

##### 47. ArtiValues

**容器属性**:

- **UUID**: `e758f32b-6795-44cc-8e83-ef6067b48453`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiValues`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The ArtiValues container collects all parameter values for ARTI that are filled by the generators (OS, RTE, ...)

###### 配置容器

本模块包含 **9** 个配置容器：

####### 1. ArtiConstant

**容器属性**:

- **UUID**: `e0d27118-64b4-49a1-b2c1-3f7337372bd7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiConstant`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container holds a constant value.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiConstantString

- **UUID**: `b5853b91-631e-4383-85e8-73ae825eaac9`
- **参数名**: `ArtiConstantString`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the constant value for a specific parameter.

####### 2. ArtiExpression

**容器属性**:

- **UUID**: `9eb0f29f-73c6-4c40-9995-60fdaf326bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiExpression`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container holds a C like expression that a debugger can evaluate. This is similar to what is already done in ORTI.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. ArtiExpressionString

- **UUID**: `a129fbf3-4f27-4886-8b0f-116cda8b2fdd`
- **参数名**: `ArtiExpressionString`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This string represents a C like expression that a debugger can evaluate.

####### 3. ArtiHook

**容器属性**:

- **UUID**: `3c09698b-e0ae-4f43-bb2f-6267695a97be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHook`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents an ARTI hook that is present in the module.

######## 参数配置

此容器包含 **5** 个参数：

######### BOOLEAN 类型参数

########## 1. ArtiHookOnlyDeclarationNeeded

- **UUID**: `04e12dc6-9205-4f10-a4b2-9b75bd072680`
- **参数名**: `ArtiHookOnlyDeclarationNeeded`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter should be set to true in case the calling component never calls the hook with the configured parameter values but needs the respective identifiers declared. If this parameter is set to false ARTI expects that the hook is called with the configured parameter values.

######### STRING 类型参数

########## 1. ArtiHookClass

- **UUID**: `a06f3e3d-24de-483d-b10e-99973eaa2b06`
- **参数名**: `ArtiHookClass`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the (schedule) class of macros. Classes can be one of the predefined classes or user defined.

########## 2. ArtiHookContext

- **UUID**: `ed356af6-a374-4a5d-a4a1-e70fdf10cc11`
- **参数名**: `ArtiHookContext`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the execution context. One of NOSUSP, SPRVSR, or USER.

########## 3. ArtiHookEventName

- **UUID**: `19398e7c-e716-4bf5-a971-4d9e78c3b44d`
- **参数名**: `ArtiHookEventName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The name of the event as defined for a particular class, or an arbitrary name for generic classes.

########## 4. ArtiHookInstance

- **UUID**: `13d1b951-b6ce-4b1a-a484-e65b16d2d3d5`
- **参数名**: `ArtiHookInstance`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of an instance of the (schedule) class.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiHookEventParameterTypeRef

- **UUID**: `2fc3d721-14a9-42a2-a7d7-ba3ac5a831f8`
- **引用名**: `ArtiHookEventParameterTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiParameterTypeMap`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a parameter type to interpret the hook event number.

########## 2. ArtiHookInstanceParameterTypeRef

- **UUID**: `9b426d8d-bfe0-488e-974e-2f2a052f7d70`
- **引用名**: `ArtiHookInstanceParameterTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiParameterTypeMap`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a parameter type to interpret the hook instance number.

######### FOREIGN-REFERENCE 类型引用

########## 1. ArtiHookEntryRef

- **UUID**: `c3cd46e8-a113-48b6-989b-adf3b7b9614c`
- **引用名**: `ArtiHookEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-MODULE-ENTRY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswModuleEntry that describes the parameters of this hook.

####### 4. ArtiObjectClassParameter

**容器属性**:

- **UUID**: `0af7d89a-8f29-4583-bd0b-088de5fa8930`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiObjectClassParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents a parameter of an Arti object class definition.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiObjectClassParameterTypeMapRef

- **UUID**: `b4b334c9-349f-4d13-b565-ff6197b2918e`
- **引用名**: `ArtiObjectClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiParameterTypeMap`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a parameter type to interpret the instance parameter value.

####### 5. ArtiObjectInstanceParameter

**容器属性**:

- **UUID**: `5cfddb8e-5775-456b-ab50-a6964656f9b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiObjectInstanceParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents a parameter of an Arti object instance.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiObjectInstanceParameterConstantRef

- **UUID**: `75a8ccbc-ad49-44b5-b2ff-ae3f9793e615`
- **引用名**: `ArtiObjectInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiConstant`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a constant representing the value of this parameter.

########## 2. ArtiObjectInstanceParameterExpressionRef

- **UUID**: `e0f22282-51b0-409e-ac1c-8f016b2e8e9f`
- **引用名**: `ArtiObjectInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiExpression`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an expression that evaluates the value of this parameter.

########## 3. ArtiObjectInstanceParameterHookRef

- **UUID**: `4143fac1-8957-43d6-bfb1-31f99d2262c9`
- **引用名**: `ArtiObjectInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiHook`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a hook that records this parameter.

####### 6. ArtiParameterTypeMap

**容器属性**:

- **UUID**: `216e9896-3138-475f-a962-005b0fd5b179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMap`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

A map of key/value pairs to map a parameter value to a display string and/or an Arti or EcuC object.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ArtiParameterTypeMapPair

**容器属性**:

- **UUID**: `461a3082-a94e-4bca-abc0-88e4d3d40a9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMapPair`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

A key/value pair to map a parameter value to a display string and/or an Arti or EcuC object.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. ArtiParameterTypeMapPairInput

- **UUID**: `e9c19d64-82a1-4430-b3f2-04e20e200043`
- **参数名**: `ArtiParameterTypeMapPairInput`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The numerical value given by a parameter to translate.

########### STRING 类型参数

############ 1. ArtiParameterTypeMapPairOutput

- **UUID**: `0036af0b-9260-4096-94d3-1afab19b868a`
- **参数名**: `ArtiParameterTypeMapPairOutput`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The string to display for the Input value.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. ArtiParameterTypeMapPairInputExpressionRef

- **UUID**: `86381dbf-a0f8-4d1a-bd8b-42f93db39cc3`
- **引用名**: `ArtiParameterTypeMapPairInputExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiExpression`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an expression that evaluates to a numerical value to translate.

########### CHOICE-REFERENCE 类型引用

############ 1. ArtiParameterTypeMapPairOutputRef

- **UUID**: `6e23f6db-93ef-4b9a-901c-1f17ccb362f2`
- **引用名**: `ArtiParameterTypeMapPairOutputRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Arti/ArtiOs/ArtiOsContextInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsIsrInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsStackInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsTaskInstance`
  - `/MICROSAR/Arti/ArtiValues/ArtiStates/ArtiStatesTaskState`
  - `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **描述**: Choice Reference to ArtiOsTaskInstance, ArtiOsIsrInstance, ArtiStatesTaskState, OsAppMode, ArtiOsContextInstance, or ArtiOsStackInstance.

####### 7. ArtiParameterTypeMapPair

**容器属性**:

- **UUID**: `461a3082-a94e-4bca-abc0-88e4d3d40a9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMapPair`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

A key/value pair to map a parameter value to a display string and/or an Arti or EcuC object.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. ArtiParameterTypeMapPairInput

- **UUID**: `e9c19d64-82a1-4430-b3f2-04e20e200043`
- **参数名**: `ArtiParameterTypeMapPairInput`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The numerical value given by a parameter to translate.

######### STRING 类型参数

########## 1. ArtiParameterTypeMapPairOutput

- **UUID**: `0036af0b-9260-4096-94d3-1afab19b868a`
- **参数名**: `ArtiParameterTypeMapPairOutput`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The string to display for the Input value.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiParameterTypeMapPairInputExpressionRef

- **UUID**: `86381dbf-a0f8-4d1a-bd8b-42f93db39cc3`
- **引用名**: `ArtiParameterTypeMapPairInputExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiExpression`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an expression that evaluates to a numerical value to translate.

######### CHOICE-REFERENCE 类型引用

########## 1. ArtiParameterTypeMapPairOutputRef

- **UUID**: `6e23f6db-93ef-4b9a-901c-1f17ccb362f2`
- **引用名**: `ArtiParameterTypeMapPairOutputRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Arti/ArtiOs/ArtiOsContextInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsIsrInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsStackInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsTaskInstance`
  - `/MICROSAR/Arti/ArtiValues/ArtiStates/ArtiStatesTaskState`
  - `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **描述**: Choice Reference to ArtiOsTaskInstance, ArtiOsIsrInstance, ArtiStatesTaskState, OsAppMode, ArtiOsContextInstance, or ArtiOsStackInstance.

####### 8. ArtiStates

**容器属性**:

- **UUID**: `846ef0af-80f6-4206-b332-b905baf624dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStates`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains all states of tasks, isrs... that the EcuC uses.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. ArtiStatesTaskEnhanced

- **UUID**: `26993265-e43d-458b-9982-f565befd32b6`
- **参数名**: `ArtiStatesTaskEnhanced`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Set to true, if the OS provides an "enhanced" state model with "READY" split to "Activated", "Preempted", "Released".

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ArtiStatesTaskState

**容器属性**:

- **UUID**: `c7b53bce-68f8-4aaf-9bf9-f64b815a0090`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStatesTaskState`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Each state used by the OS has to be listed as ArtiStatesTaskState Parameter with a choice of the states.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. ArtiStatesTaskStateEnum

- **UUID**: `c9da8e04-91df-486c-812d-3b239b3d932a`
- **参数名**: `ArtiStatesTaskStateEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
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

- **UUID**: `c7b53bce-68f8-4aaf-9bf9-f64b815a0090`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStatesTaskState`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Each state used by the OS has to be listed as ArtiStatesTaskState Parameter with a choice of the states.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. ArtiStatesTaskStateEnum

- **UUID**: `c9da8e04-91df-486c-812d-3b239b3d932a`
- **参数名**: `ArtiStatesTaskStateEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ArtiTaskStateActivated` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStatePreempted` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReady` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReleased` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateRunning` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateSuspended` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateWaiting` (来源: AUTOSAR_ECUC)
- **描述**: ArtiStatesTaskState choice of the states.

##### 48. ArtiConstant

**容器属性**:

- **UUID**: `e0d27118-64b4-49a1-b2c1-3f7337372bd7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiConstant`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container holds a constant value.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiConstantString

- **UUID**: `b5853b91-631e-4383-85e8-73ae825eaac9`
- **参数名**: `ArtiConstantString`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the constant value for a specific parameter.

##### 49. ArtiExpression

**容器属性**:

- **UUID**: `9eb0f29f-73c6-4c40-9995-60fdaf326bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiExpression`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container holds a C like expression that a debugger can evaluate. This is similar to what is already done in ORTI.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. ArtiExpressionString

- **UUID**: `a129fbf3-4f27-4886-8b0f-116cda8b2fdd`
- **参数名**: `ArtiExpressionString`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This string represents a C like expression that a debugger can evaluate.

##### 50. ArtiHook

**容器属性**:

- **UUID**: `3c09698b-e0ae-4f43-bb2f-6267695a97be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHook`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents an ARTI hook that is present in the module.

###### 参数配置

此容器包含 **5** 个参数：

####### BOOLEAN 类型参数

######## 1. ArtiHookOnlyDeclarationNeeded

- **UUID**: `04e12dc6-9205-4f10-a4b2-9b75bd072680`
- **参数名**: `ArtiHookOnlyDeclarationNeeded`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter should be set to true in case the calling component never calls the hook with the configured parameter values but needs the respective identifiers declared. If this parameter is set to false ARTI expects that the hook is called with the configured parameter values.

####### STRING 类型参数

######## 1. ArtiHookClass

- **UUID**: `a06f3e3d-24de-483d-b10e-99973eaa2b06`
- **参数名**: `ArtiHookClass`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the (schedule) class of macros. Classes can be one of the predefined classes or user defined.

######## 2. ArtiHookContext

- **UUID**: `ed356af6-a374-4a5d-a4a1-e70fdf10cc11`
- **参数名**: `ArtiHookContext`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the execution context. One of NOSUSP, SPRVSR, or USER.

######## 3. ArtiHookEventName

- **UUID**: `19398e7c-e716-4bf5-a971-4d9e78c3b44d`
- **参数名**: `ArtiHookEventName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The name of the event as defined for a particular class, or an arbitrary name for generic classes.

######## 4. ArtiHookInstance

- **UUID**: `13d1b951-b6ce-4b1a-a484-e65b16d2d3d5`
- **参数名**: `ArtiHookInstance`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of an instance of the (schedule) class.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiHookEventParameterTypeRef

- **UUID**: `2fc3d721-14a9-42a2-a7d7-ba3ac5a831f8`
- **引用名**: `ArtiHookEventParameterTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiParameterTypeMap`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a parameter type to interpret the hook event number.

######## 2. ArtiHookInstanceParameterTypeRef

- **UUID**: `9b426d8d-bfe0-488e-974e-2f2a052f7d70`
- **引用名**: `ArtiHookInstanceParameterTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiParameterTypeMap`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a parameter type to interpret the hook instance number.

####### FOREIGN-REFERENCE 类型引用

######## 1. ArtiHookEntryRef

- **UUID**: `c3cd46e8-a113-48b6-989b-adf3b7b9614c`
- **引用名**: `ArtiHookEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-MODULE-ENTRY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswModuleEntry that describes the parameters of this hook.

##### 51. ArtiObjectClassParameter

**容器属性**:

- **UUID**: `0af7d89a-8f29-4583-bd0b-088de5fa8930`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiObjectClassParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents a parameter of an Arti object class definition.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiObjectClassParameterTypeMapRef

- **UUID**: `b4b334c9-349f-4d13-b565-ff6197b2918e`
- **引用名**: `ArtiObjectClassParameterTypeMapRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiParameterTypeMap`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiParameterTypeMap`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a parameter type to interpret the instance parameter value.

##### 52. ArtiObjectInstanceParameter

**容器属性**:

- **UUID**: `5cfddb8e-5775-456b-ab50-a6964656f9b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiObjectInstanceParameter`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents a parameter of an Arti object instance.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiObjectInstanceParameterConstantRef

- **UUID**: `75a8ccbc-ad49-44b5-b2ff-ae3f9793e615`
- **引用名**: `ArtiObjectInstanceParameterConstantRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiConstant`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiConstant`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a constant representing the value of this parameter.

######## 2. ArtiObjectInstanceParameterExpressionRef

- **UUID**: `e0f22282-51b0-409e-ac1c-8f016b2e8e9f`
- **引用名**: `ArtiObjectInstanceParameterExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiExpression`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an expression that evaluates the value of this parameter.

######## 3. ArtiObjectInstanceParameterHookRef

- **UUID**: `4143fac1-8957-43d6-bfb1-31f99d2262c9`
- **引用名**: `ArtiObjectInstanceParameterHookRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiHook`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiHook`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to a hook that records this parameter.

##### 53. ArtiParameterTypeMap

**容器属性**:

- **UUID**: `216e9896-3138-475f-a962-005b0fd5b179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMap`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

A map of key/value pairs to map a parameter value to a display string and/or an Arti or EcuC object.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ArtiParameterTypeMapPair

**容器属性**:

- **UUID**: `461a3082-a94e-4bca-abc0-88e4d3d40a9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMapPair`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

A key/value pair to map a parameter value to a display string and/or an Arti or EcuC object.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. ArtiParameterTypeMapPairInput

- **UUID**: `e9c19d64-82a1-4430-b3f2-04e20e200043`
- **参数名**: `ArtiParameterTypeMapPairInput`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The numerical value given by a parameter to translate.

######### STRING 类型参数

########## 1. ArtiParameterTypeMapPairOutput

- **UUID**: `0036af0b-9260-4096-94d3-1afab19b868a`
- **参数名**: `ArtiParameterTypeMapPairOutput`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The string to display for the Input value.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ArtiParameterTypeMapPairInputExpressionRef

- **UUID**: `86381dbf-a0f8-4d1a-bd8b-42f93db39cc3`
- **引用名**: `ArtiParameterTypeMapPairInputExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiExpression`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an expression that evaluates to a numerical value to translate.

######### CHOICE-REFERENCE 类型引用

########## 1. ArtiParameterTypeMapPairOutputRef

- **UUID**: `6e23f6db-93ef-4b9a-901c-1f17ccb362f2`
- **引用名**: `ArtiParameterTypeMapPairOutputRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Arti/ArtiOs/ArtiOsContextInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsIsrInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsStackInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsTaskInstance`
  - `/MICROSAR/Arti/ArtiValues/ArtiStates/ArtiStatesTaskState`
  - `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **描述**: Choice Reference to ArtiOsTaskInstance, ArtiOsIsrInstance, ArtiStatesTaskState, OsAppMode, ArtiOsContextInstance, or ArtiOsStackInstance.

##### 54. ArtiParameterTypeMapPair

**容器属性**:

- **UUID**: `461a3082-a94e-4bca-abc0-88e4d3d40a9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiParameterTypeMapPair`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

A key/value pair to map a parameter value to a display string and/or an Arti or EcuC object.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. ArtiParameterTypeMapPairInput

- **UUID**: `e9c19d64-82a1-4430-b3f2-04e20e200043`
- **参数名**: `ArtiParameterTypeMapPairInput`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The numerical value given by a parameter to translate.

####### STRING 类型参数

######## 1. ArtiParameterTypeMapPairOutput

- **UUID**: `0036af0b-9260-4096-94d3-1afab19b868a`
- **参数名**: `ArtiParameterTypeMapPairOutput`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: The string to display for the Input value.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ArtiParameterTypeMapPairInputExpressionRef

- **UUID**: `86381dbf-a0f8-4d1a-bd8b-42f93db39cc3`
- **引用名**: `ArtiParameterTypeMapPairInputExpressionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ArtiExpression`
- **完整路径**: `/MICROSAR/Arti/ArtiValues/ArtiExpression`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to an expression that evaluates to a numerical value to translate.

####### CHOICE-REFERENCE 类型引用

######## 1. ArtiParameterTypeMapPairOutputRef

- **UUID**: `6e23f6db-93ef-4b9a-901c-1f17ccb362f2`
- **引用名**: `ArtiParameterTypeMapPairOutputRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Arti/ArtiOs/ArtiOsContextInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsIsrInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsStackInstance`
  - `/MICROSAR/Arti/ArtiOs/ArtiOsTaskInstance`
  - `/MICROSAR/Arti/ArtiValues/ArtiStates/ArtiStatesTaskState`
  - `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **描述**: Choice Reference to ArtiOsTaskInstance, ArtiOsIsrInstance, ArtiStatesTaskState, OsAppMode, ArtiOsContextInstance, or ArtiOsStackInstance.

##### 55. ArtiStates

**容器属性**:

- **UUID**: `846ef0af-80f6-4206-b332-b905baf624dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStates`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container contains all states of tasks, isrs... that the EcuC uses.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. ArtiStatesTaskEnhanced

- **UUID**: `26993265-e43d-458b-9982-f565befd32b6`
- **参数名**: `ArtiStatesTaskEnhanced`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Set to true, if the OS provides an "enhanced" state model with "READY" split to "Activated", "Preempted", "Released".

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ArtiStatesTaskState

**容器属性**:

- **UUID**: `c7b53bce-68f8-4aaf-9bf9-f64b815a0090`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStatesTaskState`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Each state used by the OS has to be listed as ArtiStatesTaskState Parameter with a choice of the states.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. ArtiStatesTaskStateEnum

- **UUID**: `c9da8e04-91df-486c-812d-3b239b3d932a`
- **参数名**: `ArtiStatesTaskStateEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ArtiTaskStateActivated` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStatePreempted` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReady` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReleased` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateRunning` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateSuspended` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateWaiting` (来源: AUTOSAR_ECUC)
- **描述**: ArtiStatesTaskState choice of the states.

##### 56. ArtiStatesTaskState

**容器属性**:

- **UUID**: `c7b53bce-68f8-4aaf-9bf9-f64b815a0090`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiStatesTaskState`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Each state used by the OS has to be listed as ArtiStatesTaskState Parameter with a choice of the states.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. ArtiStatesTaskStateEnum

- **UUID**: `c9da8e04-91df-486c-812d-3b239b3d932a`
- **参数名**: `ArtiStatesTaskStateEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ArtiTaskStateActivated` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStatePreempted` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReady` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateReleased` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateRunning` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateSuspended` (来源: AUTOSAR_ECUC)
  - `ArtiTaskStateWaiting` (来源: AUTOSAR_ECUC)
- **描述**: ArtiStatesTaskState choice of the states.

##### 57. ArtiGeneral

**容器属性**:

- **UUID**: `d823413b-2415-4e58-bc6d-27f429a24286`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

General configuration parameters of ARTI.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. ArtiDevErrorDetect

- **UUID**: `ba5b39db-65de-4a7b-8b13-d2e5f0af772e`
- **参数名**: `ArtiDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.

true: Development error detection is enabled.
false: Development error detection is disabled.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

######## 2. ArtiSafeBswChecks

- **UUID**: `11a2f98d-8bc3-4ab6-89ca-980efe2253a9`
- **参数名**: `ArtiSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Selects whether safety checks are used. These checks improve robustness as e.g. invalid parameter values are detected before a function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######## 3. ArtiEnableVfbTraceClient

- **UUID**: `aa4d16c1-6eba-43bf-8792-a83507e698ca`
- **参数名**: `ArtiEnableVfbTraceClient`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Selects whether the Arti Vfb Trace Client is enabled or disabled.
When the client is enabled, the Arti module will generate the configured Rte Vfb Trace Hooks and register Arti as a Vfb Trace Client in the RTE.

####### STRING 类型参数

######## 1. ArtiMacroAccessIncludeHeader

- **UUID**: `b0d2e7e5-a3f6-497a-9282-47a9f4a3f8be`
- **参数名**: `ArtiMacroAccessIncludeHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of the header file containing the definition of the macro ARTI_WRITE_TRACE_HOOK_VAR(variableName, variableValue).
This macro is called for all ArtiHookTraceVariable with an ArtiHookTraceVariableAccessType of "Macro".

Note:
Insert the complete filename including the extension (e.g. MyHeader.h).

##### 58. ArtiHookTraceVariable

**容器属性**:

- **UUID**: `9df04a86-2c47-404a-8b7d-fc3cbfa7d6a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHookTraceVariable`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Holds the configuration of a hook trace variable. These variables provide information on hook parameters to an external debugging or tracing tool.

Note:
The prefix "Arti_" is added to the name of the hook trace variable in all generated files.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. ArtiHookTraceVariableAccessType

- **UUID**: `1b745b64-d492-48f4-99c7-2d6998fda2d3`
- **参数名**: `ArtiHookTraceVariableAccessType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Direct` (来源: Vector Informatik)
  - `Macro` (来源: Vector Informatik)
- **描述**: Specifies in which way the trace variable is accessed.

Direct:
The trace variable will be accessed directly.

Macro:
The trace variable will be accessed using the ARTI_WRITE_TRACE_HOOK_VAR macro.
This allows the implementation of further steps like signaling an event or writing the value directly into a register.
Note: In this case the header that defines the macro must be specified in /MICROSAR/Arti/ArtiGeneral/ArtiMacroAccessIncludeHeader.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. ArtiHookTraceVariableCondition

**容器属性**:

- **UUID**: `2a863cb2-3d5b-408c-bd8a-d5e54594dbc2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHookTraceVariableCondition`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container holds the different conditions of the trace variable. Hooks with matching parameter values will use this variable for writing their information.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. ArtiHookConditionStringValue

- **UUID**: `d4b87af4-1767-46bd-91d1-0999f74fd4ee`
- **参数名**: `ArtiHookConditionStringValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the string value corresponding to the configuration in:
/MICROSAR/Arti/ArtiHookTraceVariable/ArtiHookTraceVariableCondition/ArtiHookConditionPart.
The string value is compared against the respective hook parameter value. The hook trace variable will only be written in case of equality.

######### ENUMERATION 类型参数

########## 1. ArtiHookConditionPart

- **UUID**: `0bd834d3-1661-4d16-9921-d2dc041cb2b1`
- **参数名**: `ArtiHookConditionPart`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HookClass` (来源: Vector Informatik)
  - `HookContext` (来源: Vector Informatik)
  - `HookEventName` (来源: Vector Informatik)
  - `HookInstance` (来源: Vector Informatik)
- **描述**: This parameter is used to configure which hook parameter shall be taken as a condition.
The hook trace variable will be written, if the respective hook parameters match the values configured at: /MICROSAR/Arti/ArtiHookTraceVariable/ArtiHookTraceVariableCondition/ArtiHookConditionStringValue.

####### 2. ArtiHookTraceVariableIndex

**容器属性**:

- **UUID**: `b6a90181-08f0-435d-829f-62a8ea72ca85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHookTraceVariableIndex`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This sub-container shall be added to the hook trace variable configuration in case it shall be an array variable.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. ArtiHookIndexPart

- **UUID**: `62492f0e-42e3-45f2-834c-9a384cdb961e`
- **参数名**: `ArtiHookIndexPart`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `HookInstanceParameter`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HookInstanceParameter` (来源: Vector Informatik)
- **描述**: Specifies the hook parameter that will be used as the array index. Currently, only HookInstanceParameter is supported.
Mind that ARTI needs to know the value range. Therefore, the respective ArtiHookInstanceParameterTypeRef needs to be configured.

####### 3. ArtiHookTraceVariablePart

**容器属性**:

- **UUID**: `60ffe205-0b1d-4af3-a615-2f932e17d480`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHookTraceVariablePart`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container configures a part of a hook trace variable. The parameters in this container configure which hook parameters shall be stored at which start bit and with which size.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. ArtiHookStartBit

- **UUID**: `b5a03f01-639d-4f76-b5d6-5df117c24818`
- **参数名**: `ArtiHookStartBit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the bit of the trace variable that the part starts at where 0 is considered to be the least significant bit.

Note: ArtiHookStartBit + ArtiHookBitCount has to be smaller than or equal to 32

########## 2. ArtiHookBitCount

- **UUID**: `866cb6a8-b021-4e45-bffa-1a4f72e431e2`
- **参数名**: `ArtiHookBitCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the number of bits that the part uses in the trace variable.

Note: ArtiHookStartBit + ArtiHookBitCount has to be smaller than or equal to 32

######### ENUMERATION 类型参数

########## 1. ArtiHookPartPart

- **UUID**: `4b2bd90b-9685-4046-a10a-ef3d05f9fa42`
- **参数名**: `ArtiHookPartPart`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HookClass` (来源: Vector Informatik)
  - `HookContext` (来源: Vector Informatik)
  - `HookEventName` (来源: Vector Informatik)
  - `HookInstance` (来源: Vector Informatik)
  - `HookEventParameter` (来源: Vector Informatik)
  - `HookInstanceParameter` (来源: Vector Informatik)
  - `One` (来源: Vector Informatik)
  - `Zero` (来源: Vector Informatik)
- **描述**: Specifies the content that is stored in the part:

HookContext:
Stores an ID corresponding to the Context of the Hook.

HookClass:
Stores an ID corresponding to the Class of the Hook.

HookEventName:
Stores an ID corresponding to the EventName of the Hook.

HookInstance:
Stores an ID corresponding to the Instance of the Hook.

HookEventParameter:
Stores the event parameter of the Hook.

HookInstanceParameter:
Stores the instance parameter of the Hook.

One:
Stores one bits.

Zero:
Stores zero bits.

##### 59. ArtiHookTraceVariableCondition

**容器属性**:

- **UUID**: `2a863cb2-3d5b-408c-bd8a-d5e54594dbc2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHookTraceVariableCondition`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container holds the different conditions of the trace variable. Hooks with matching parameter values will use this variable for writing their information.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. ArtiHookConditionStringValue

- **UUID**: `d4b87af4-1767-46bd-91d1-0999f74fd4ee`
- **参数名**: `ArtiHookConditionStringValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the string value corresponding to the configuration in:
/MICROSAR/Arti/ArtiHookTraceVariable/ArtiHookTraceVariableCondition/ArtiHookConditionPart.
The string value is compared against the respective hook parameter value. The hook trace variable will only be written in case of equality.

####### ENUMERATION 类型参数

######## 1. ArtiHookConditionPart

- **UUID**: `0bd834d3-1661-4d16-9921-d2dc041cb2b1`
- **参数名**: `ArtiHookConditionPart`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HookClass` (来源: Vector Informatik)
  - `HookContext` (来源: Vector Informatik)
  - `HookEventName` (来源: Vector Informatik)
  - `HookInstance` (来源: Vector Informatik)
- **描述**: This parameter is used to configure which hook parameter shall be taken as a condition.
The hook trace variable will be written, if the respective hook parameters match the values configured at: /MICROSAR/Arti/ArtiHookTraceVariable/ArtiHookTraceVariableCondition/ArtiHookConditionStringValue.

##### 60. ArtiHookTraceVariableIndex

**容器属性**:

- **UUID**: `b6a90181-08f0-435d-829f-62a8ea72ca85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHookTraceVariableIndex`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This sub-container shall be added to the hook trace variable configuration in case it shall be an array variable.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. ArtiHookIndexPart

- **UUID**: `62492f0e-42e3-45f2-834c-9a384cdb961e`
- **参数名**: `ArtiHookIndexPart`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `HookInstanceParameter`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HookInstanceParameter` (来源: Vector Informatik)
- **描述**: Specifies the hook parameter that will be used as the array index. Currently, only HookInstanceParameter is supported.
Mind that ARTI needs to know the value range. Therefore, the respective ArtiHookInstanceParameterTypeRef needs to be configured.

##### 61. ArtiHookTraceVariablePart

**容器属性**:

- **UUID**: `60ffe205-0b1d-4af3-a615-2f932e17d480`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ArtiHookTraceVariablePart`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container configures a part of a hook trace variable. The parameters in this container configure which hook parameters shall be stored at which start bit and with which size.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. ArtiHookStartBit

- **UUID**: `b5a03f01-639d-4f76-b5d6-5df117c24818`
- **参数名**: `ArtiHookStartBit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the bit of the trace variable that the part starts at where 0 is considered to be the least significant bit.

Note: ArtiHookStartBit + ArtiHookBitCount has to be smaller than or equal to 32

######## 2. ArtiHookBitCount

- **UUID**: `866cb6a8-b021-4e45-bffa-1a4f72e431e2`
- **参数名**: `ArtiHookBitCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the number of bits that the part uses in the trace variable.

Note: ArtiHookStartBit + ArtiHookBitCount has to be smaller than or equal to 32

####### ENUMERATION 类型参数

######## 1. ArtiHookPartPart

- **UUID**: `4b2bd90b-9685-4046-a10a-ef3d05f9fa42`
- **参数名**: `ArtiHookPartPart`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `HookClass` (来源: Vector Informatik)
  - `HookContext` (来源: Vector Informatik)
  - `HookEventName` (来源: Vector Informatik)
  - `HookInstance` (来源: Vector Informatik)
  - `HookEventParameter` (来源: Vector Informatik)
  - `HookInstanceParameter` (来源: Vector Informatik)
  - `One` (来源: Vector Informatik)
  - `Zero` (来源: Vector Informatik)
- **描述**: Specifies the content that is stored in the part:

HookContext:
Stores an ID corresponding to the Context of the Hook.

HookClass:
Stores an ID corresponding to the Class of the Hook.

HookEventName:
Stores an ID corresponding to the EventName of the Hook.

HookInstance:
Stores an ID corresponding to the Instance of the Hook.

HookEventParameter:
Stores the event parameter of the Hook.

HookInstanceParameter:
Stores the instance parameter of the Hook.

One:
Stores one bits.

Zero:
Stores zero bits.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 2

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Arti**

##### BSW-IMPLEMENTATION 类型元素

1. **Arti_Impl**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Arti_Impl

- **UUID**: `5e87954a-b9fd-41fd-9015-d89cdcbd3f4a`
- **实现名称**: `Arti_Impl`
- **编程语言**: C
- **软件版本**: 1.02.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.06.00
