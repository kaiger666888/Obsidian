# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:12

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

### 2. WdgM_swc

- **UUID**: `8ccdb8e0-39eb-4a39-a4de-8d087c8312f1`
- **包名称**: `WdgM_swc`
- **包含元素数量**: 0

### 3. DataTypes

- **UUID**: `0b3304ee-258d-44b9-bec8-166d009f6c5d`
- **包名称**: `DataTypes`
- **包含元素数量**: 6

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **WdgM_SupervisedEntityIdType**
2. **WdgM_CheckpointIdType**
3. **WdgM_ModeType**
4. **WdgM_ViolationType**
5. **WdgM_LocalStatusType**
6. **WdgM_GlobalStatusType**

### 4. DataConstrs

- **UUID**: `c2c97c14-7c7a-4475-8225-7a1f294344c3`
- **包名称**: `DataConstrs`
- **包含元素数量**: 6

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **WdgM_SupervisedEntityIdType_Constr**
2. **WdgM_CheckpointIdType_Constr**
3. **WdgM_ModeType_Constr**
4. **WdgM_ViolationType_Constr**
5. **WdgM_LocalStatusType_Constr**
6. **WdgM_GlobalStatusType_Constr**

### 5. CompuMethods

- **UUID**: `ceec3613-91f4-4288-af2d-198ce7302b3a`
- **包名称**: `CompuMethods`
- **包含元素数量**: 2

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **WdgM_LocalStatusType**
2. **WdgM_GlobalStatusType**

### 6. Interfaces

- **UUID**: `10bdc4f2-a98b-489d-90d9-c1f1536f9dcd`
- **包名称**: `Interfaces`
- **包含元素数量**: 5

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **WdgM_AliveSupervision**
2. **WdgM_LocalStatus**
3. **WdgM_General**
4. **WdgM_LocalStatusCallback**
5. **WdgM_GlobalStatusCallback**

### 7. ComponentTypes

- **UUID**: `e34fb010-b3e9-4ee2-bb85-7633b59ee2f8`
- **包名称**: `ComponentTypes`
- **包含元素数量**: 2

#### 包含的元素

##### SERVICE-SW-COMPONENT-TYPE 类型元素

1. **WdgM**

##### SWC-IMPLEMENTATION 类型元素

1. **WdgMImplementation**
