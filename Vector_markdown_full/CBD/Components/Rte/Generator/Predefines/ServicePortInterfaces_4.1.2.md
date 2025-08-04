# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:50

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-1-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **9** 个包：

### 1. MICROSAR_SWCS_DEV

- **包名称**: `MICROSAR_SWCS_DEV`
- **包含元素数量**: 0

### 2. NvM_swc

- **包名称**: `NvM_swc`
- **包含元素数量**: 0

### 3. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 6

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Boolean**
2. **dtRef_const_VOID**
3. **dtRef_VOID**
4. **NvM_RequestResultType**
5. **NvM_ServiceIdType**
6. **UInt8**

### 4. BaseTypes

- **包名称**: `BaseTypes`
- **包含元素数量**: 6

#### 包含的元素

##### SW-BASE-TYPE 类型元素

1. **Boolean**
2. **dtRef_const_VOID**
3. **dtRef_VOID**
4. **NvM_RequestResultType**
5. **NvM_ServiceIdType**
6. **UInt8**

### 5. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 2

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **NvM_RequestResultType**
2. **NvM_ServiceIdType**

### 6. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 1

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **UInt8_Constr**

### 7. Predefined_DEV

- **包名称**: `Predefined_DEV`
- **包含元素数量**: 0

### 8. DataConstraints

- **包名称**: `DataConstraints`
- **包含元素数量**: 1

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **Dem_UdsStatusByteType**

### 9. ServicePortInterfaces

- **包名称**: `ServicePortInterfaces`
- **包含元素数量**: 21

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **NvMAdministration**
2. **NvMNotifyInitBlock**
3. **NvMNotifyJobFinished**
4. **NvMService**
5. **NvMService_AC2**
6. **NvMService_AC2_Defs**
7. **NvMService_AC2_DS**
8. **NvMService_AC2_DS_Defs**
9. **NvMService_AC2_SRBS**
10. **NvMService_AC2_SRBS_Defs**
11. **NvMService_AC2_SRBS_DS**
12. **NvMService_AC2_SRBS_DS_Defs**
13. **NvMService_AC3**
14. **NvMService_AC3_Defs**
15. **NvMService_AC3_DS**
16. **NvMService_AC3_DS_Defs**
17. **NvMService_AC3_SRBS**
18. **NvMService_AC3_SRBS_Defs**
19. **NvMService_AC3_SRBS_DS**
20. **NvMService_AC3_SRBS_DS_Defs**
21. **NvMService_SRBS**
