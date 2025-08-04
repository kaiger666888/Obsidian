# VariantsDemo - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:27

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [VariantsDemo](#variantsdemo)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. VariantsDemo

#### 基本信息

- **模块名称**: `VariantsDemo`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-POST-BUILD

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. SelectableContainer

**容器属性**:

- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SelectableContainer`
- **多重性**: [0..1]

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. Variable

- **参数名**: `Variable`
- **数据类型**: INTEGER
- **多重性**: [0..1]

##### 2. Container

**容器属性**:

- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Container`
- **多重性**: [0..1]

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. SelectableBoolean

- **参数名**: `SelectableBoolean`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`

##### 3. LoadableContainer

**容器属性**:

- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LoadableContainer`
- **多重性**: [0..1]

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. Integer

- **参数名**: `Integer`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `3`

##### 4. Container2

**容器属性**:

- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Container2`
- **多重性**: [0..1]

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. LoadableString

- **参数名**: `LoadableString`
- **数据类型**: STRING
- **多重性**: [0..1]

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. EB

- **包名称**: `EB`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **VariantsDemo**
