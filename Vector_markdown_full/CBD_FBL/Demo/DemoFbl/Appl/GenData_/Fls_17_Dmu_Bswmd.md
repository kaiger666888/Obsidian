# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:49:20

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **5** 个包：

### 1. AUTOSAR_Fls_17_Dmu

- **包名称**: `AUTOSAR_Fls_17_Dmu`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Fls**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 15

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Fls_Init**
2. **Fls_InitCheck**
3. **Fls_Erase**
4. **Fls_Write**
5. **Fls_IsHardeningRequired**
6. **Fls_MainFunction**
7. **Fls_Read**
8. **Fls_ReadWordsSync**
9. **Fls_CompareWordsSync**
10. **Fls_VerifyErase**
11. **Fls_VerifySectorErase**
12. **Fls_GetNotifCaller**
13. **Fls_CancelNonEraseJobs**
14. **Fls_GetOperStatus**
15. **Fls_ControlTimeoutDet**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Fls**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 7

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Fls_17_Dmu_ConfigType**
2. **Fls_17_Dmu_StateType**
3. **Fls_17_Dmu_LengthType**
4. **Fls_17_Dmu_Job_Type**
5. **Fls_17_Dmu_AddressType**
6. **Fls_17_Dmu_NotifFunctionPtrType**
7. **Fls_17_Dmu_JobStartType**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Fls

- **实现名称**: `Fls`
- **编程语言**: C
- **软件版本**: 10.40.1
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
