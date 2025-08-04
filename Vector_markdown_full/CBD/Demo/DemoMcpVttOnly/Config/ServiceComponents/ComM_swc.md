# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:09

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

### 2. ComM_swc

- **UUID**: `4770fc44-e047-403d-8057-0c3e5e73fee6`
- **包名称**: `ComM_swc`
- **包含元素数量**: 2

#### 包含的元素

##### MODE-DECLARATION-GROUP 类型元素

1. **ComMMode**

##### DATA-TYPE-MAPPING-SET 类型元素

1. **ComMMode_DataTypeMappingSet**

### 3. DataTypes

- **UUID**: `bba2b52c-de75-4f02-ab04-eb1d9ccd0a53`
- **包名称**: `DataTypes`
- **包含元素数量**: 4

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **ComM_ModeType**
2. **ComM_InhibitionStatusType**
3. **ComM_UserHandleType**
4. **NetworkHandleType**

### 4. DataConstrs

- **UUID**: `7ef98a6d-5028-4d92-9a0b-7546d470bbe9`
- **包名称**: `DataConstrs`
- **包含元素数量**: 4

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **ComM_ModeType_Constr**
2. **ComM_InhibitionStatusType_Constr**
3. **ComM_UserHandleType_Constr**
4. **NetworkHandleType_Constr**

### 5. CompuMethods

- **UUID**: `d4838d0e-fe4e-4adf-a150-a18c90d4ecc5`
- **包名称**: `CompuMethods`
- **包含元素数量**: 1

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **ComM_ModeType**

### 6. Interfaces

- **UUID**: `d7a80c05-cc98-4a36-9a63-0eca6e7faa2c`
- **包名称**: `Interfaces`
- **包含元素数量**: 5

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **ComM_UserRequest**
2. **ComM_ECUModeLimitation**
3. **ComM_ChannelWakeUp**
4. **ComM_ChannelLimitation**

##### MODE-SWITCH-INTERFACE 类型元素

1. **ComM_CurrentMode**

### 7. ComponentTypes

- **UUID**: `a7a252e9-4a4e-466b-8a1d-fe71e0dbab81`
- **包名称**: `ComponentTypes`
- **包含元素数量**: 2

#### 包含的元素

##### SERVICE-SW-COMPONENT-TYPE 类型元素

1. **ComM**

##### SWC-IMPLEMENTATION 类型元素

1. **ComMImplementation**
