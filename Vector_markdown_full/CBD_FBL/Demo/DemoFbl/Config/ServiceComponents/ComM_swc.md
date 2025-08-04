# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:49:44

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00047.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **7** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. ComM_swc

- **UUID**: `b6dd5ab2-7f39-41f1-b572-f5331a06c5de`
- **包名称**: `ComM_swc`
- **包含元素数量**: 2

#### 包含的元素

##### MODE-DECLARATION-GROUP 类型元素

1. **ComMMode**

##### DATA-TYPE-MAPPING-SET 类型元素

1. **ComMMode_DataTypeMappingSet**

### 3. DataTypes

- **UUID**: `7ca95bcf-fe46-4f2d-a1bf-9a4d662bddea`
- **包名称**: `DataTypes`
- **包含元素数量**: 4

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **ComM_ModeType**
2. **ComM_InhibitionStatusType**
3. **ComM_UserHandleType**
4. **NetworkHandleType**

### 4. DataConstrs

- **UUID**: `b9f08952-5f32-46cc-b099-7189c7a06704`
- **包名称**: `DataConstrs`
- **包含元素数量**: 4

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **ComM_ModeType_Constr**
2. **ComM_InhibitionStatusType_Constr**
3. **ComM_UserHandleType_Constr**
4. **NetworkHandleType_Constr**

### 5. CompuMethods

- **UUID**: `83ac880b-0ae3-4aa0-a867-e1825d3b1840`
- **包名称**: `CompuMethods`
- **包含元素数量**: 1

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **ComM_ModeType**

### 6. Interfaces

- **UUID**: `389145b8-596c-4f20-8722-16c6d911d056`
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

- **UUID**: `24c03a24-477f-4ded-b414-dc25cf966f7e`
- **包名称**: `ComponentTypes`
- **包含元素数量**: 2

#### 包含的元素

##### SERVICE-SW-COMPONENT-TYPE 类型元素

1. **ComM**

##### SWC-IMPLEMENTATION 类型元素

1. **ComMImplementation**
