# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:49:16

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00047.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **6** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. Csm_swc

- **UUID**: `c4384820-81aa-46fc-bd3e-bcf4e63f5c62`
- **包名称**: `Csm_swc`
- **包含元素数量**: 0

### 3. DataTypes

- **UUID**: `5e04e0fe-6589-4e20-8138-0d4209df7223`
- **包名称**: `DataTypes`
- **包含元素数量**: 11

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Csm_VerifyResultType**
2. **Csm_ConfigIdType**
3. **Crypto_OperationModeType**
4. **Crypto_VerifyResultType**
5. **Csm_DataPtr**
6. **Csm_const_DataPtr**
7. **Csm_LengthPtr**
8. **Csm_VerifyResultPtr**
9. **Crypto_ResultType**
10. **Csm_KeyElementEnumType**
11. **Csm_ResultType**

### 4. DataConstrs

- **UUID**: `2f969abc-0847-4b32-b046-257a5deb5e18`
- **包名称**: `DataConstrs`
- **包含元素数量**: 7

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **Csm_VerifyResultType_Constr**
2. **Csm_ConfigIdType_Constr**
3. **Crypto_OperationModeType_Constr**
4. **Crypto_VerifyResultType_Constr**
5. **Crypto_ResultType_Constr**
6. **Csm_KeyElementEnumType_Constr**
7. **Csm_ResultType_Constr**

### 5. CompuMethods

- **UUID**: `3e67a849-4df4-4d2b-9372-2e08ebbe2392`
- **包名称**: `CompuMethods`
- **包含元素数量**: 6

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Csm_VerifyResultType**
2. **Crypto_OperationModeType**
3. **Crypto_VerifyResultType**
4. **Csm_KeyElementEnumType**
5. **Csm_ResultType**
6. **Crypto_ResultType**

### 6. ComponentTypes

- **UUID**: `0633bf1b-f608-464a-81a1-837573935244`
- **包名称**: `ComponentTypes`
- **包含元素数量**: 2

#### 包含的元素

##### SERVICE-SW-COMPONENT-TYPE 类型元素

1. **Csm**

##### SWC-IMPLEMENTATION 类型元素

1. **CsmImplementation**
