# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:11

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00046.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **7** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. EcuM_swc

- **UUID**: `c657ea19-5504-4e43-9d56-df7bf7ff9303`
- **包名称**: `EcuM_swc`
- **包含元素数量**: 0

### 3. DataTypes

- **UUID**: `a4868eb1-1115-4573-b08f-f0befb43ca41`
- **包名称**: `DataTypes`
- **包含元素数量**: 6

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **EcuM_StateType**
2. **EcuM_ModeType**
3. **EcuM_TimeType**
4. **EcuM_UserType**
5. **EcuM_ShutdownCauseType**
6. **EcuM_BootTargetType**

### 4. DataConstrs

- **UUID**: `a19bd430-acc1-4500-b9f6-f9905b8b6579`
- **包名称**: `DataConstrs`
- **包含元素数量**: 6

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **EcuM_StateType_Constr**
2. **EcuM_ModeType_Constr**
3. **EcuM_TimeType_Constr**
4. **EcuM_UserType_Constr**
5. **EcuM_ShutdownCauseType_Constr**
6. **EcuM_BootTargetType_Constr**

### 5. CompuMethods

- **UUID**: `79ef3912-b225-40e4-8a54-bd4caeae005b`
- **包名称**: `CompuMethods`
- **包含元素数量**: 4

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **EcuM_StateType**
2. **EcuM_ModeType**
3. **EcuM_ShutdownCauseType**
4. **EcuM_BootTargetType**

### 6. Interfaces

- **UUID**: `2656a495-f29d-4844-968d-d427e2beab56`
- **包名称**: `Interfaces`
- **包含元素数量**: 2

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **EcuM_ShutdownTarget**
2. **EcuM_BootTarget**

### 7. ComponentTypes

- **UUID**: `44fb63f3-9df2-4334-b204-abfd2eb66bb1`
- **包名称**: `ComponentTypes`
- **包含元素数量**: 2

#### 包含的元素

##### SERVICE-SW-COMPONENT-TYPE 类型元素

1. **EcuM**

##### SWC-IMPLEMENTATION 类型元素

1. **EcuMImplementation**
