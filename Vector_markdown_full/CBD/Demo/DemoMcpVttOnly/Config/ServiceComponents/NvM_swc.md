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

### 2. NvM_swc

- **UUID**: `8f4cf2dc-6c89-4eee-8f27-d09263afafb1`
- **包名称**: `NvM_swc`
- **包含元素数量**: 0

### 3. DataTypes

- **UUID**: `f86ea1ef-ca85-4559-bcad-d32dcf132ab9`
- **包名称**: `DataTypes`
- **包含元素数量**: 3

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **NvM_RequestResultType**
2. **NvM_BlockIdType**
3. **NvM_ServiceIdType**

### 4. DataConstrs

- **UUID**: `b8dca4f9-0208-4ece-b6b1-c7920d54390a`
- **包名称**: `DataConstrs`
- **包含元素数量**: 3

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **NvM_RequestResultType_Constr**
2. **NvM_BlockIdType_Constr**
3. **NvM_ServiceIdType_Constr**

### 5. CompuMethods

- **UUID**: `22634c9b-dcae-422c-be08-2ed8d92c88ec`
- **包名称**: `CompuMethods`
- **包含元素数量**: 2

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **NvM_RequestResultType**
2. **NvM_ServiceIdType**

### 6. Interfaces

- **UUID**: `1855c925-ba07-4cc0-bb58-9d147a00bd72`
- **包名称**: `Interfaces`
- **包含元素数量**: 3

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **NvMAdministration**
2. **NvMService_AC3_SRBS**
3. **NvMNotifyJobFinished**

### 7. ComponentTypes

- **UUID**: `fb8c1454-58d7-447b-aa35-1124442b51c3`
- **包名称**: `ComponentTypes`
- **包含元素数量**: 2

#### 包含的元素

##### SERVICE-SW-COMPONENT-TYPE 类型元素

1. **NvM**

##### SWC-IMPLEMENTATION 类型元素

1. **NvMImplementation**
