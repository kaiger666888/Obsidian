# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:52:29

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3_STRICT_COMPACT.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **7** 个包：

### 1. DemoApplication

- **包名称**: `DemoApplication`
- **包含元素数量**: 0

### 2. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 1

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **ComM_ModeType**

### 3. ConstantSpecifications

- **包名称**: `ConstantSpecifications`
- **包含元素数量**: 2

#### 包含的元素

##### CONSTANT-SPECIFICATION 类型元素

1. **CONST_0c0f918b8f394b8586f853bd5**
2. **CONST_951406b330e947ed9394eb477**

### 4. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 1

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **ComM_ModeTypeValues**

### 5. PortInterfaces

- **包名称**: `PortInterfaces`
- **包含元素数量**: 7

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **If_CounterModify**
2. **If_DiscreteValueOutput**
3. **DETService**
4. **NvMService**
5. **ComM_UserRequest**

##### SENDER-RECEIVER-INTERFACE 类型元素

1. **If_Counter**
2. **If_Internal**

### 6. SwComponentTypes

- **包名称**: `SwComponentTypes`
- **包含元素数量**: 4

#### 包含的元素

##### APPLICATION-SW-COMPONENT-TYPE 类型元素

1. **SWC_CyclicCounter**
2. **SWC_ModifyEcho**

##### ECU-ABSTRACTION-SW-COMPONENT-TYPE 类型元素

1. **SWC_IoHwAbs**

##### COMPOSITION-SW-COMPONENT-TYPE 类型元素

1. **TopLevelComposition**

### 7. SwcImplementations

- **包名称**: `SwcImplementations`
- **包含元素数量**: 3

#### 包含的元素

##### SWC-IMPLEMENTATION 类型元素

1. **Impl_SWC_CyclicCounter**
2. **Impl_SWC_ModifyEcho**
3. **Impl_SWC_IoHwAbs**
