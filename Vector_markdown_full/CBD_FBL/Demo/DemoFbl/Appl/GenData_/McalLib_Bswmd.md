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

此ARXML文件包含 **7** 个包：

### 1. AURIX2G_McalLib

- **包名称**: `AURIX2G_McalLib`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **McalLib**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 25

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Mcal_GetCpuWdgPassword**
2. **Mcal_SetCpuWdgPassword**
3. **Mcal_WriteCpuEndInitProtReg**
4. **Mcal_GetSafetyEndInitPassword**
5. **Mcal_SetSafetyEndInitPassword**
6. **Mcal_WriteSafetyEndInitProtReg**
7. **Mcal_WriteSafetyEndInitProtReg16**
8. **Mcal_WriteSafetyEndInitProtRegMask**
9. **Mcal_GetPeripheralEndInitPassword**
10. **Mcal_SetPeripheralEndInitPassword**
11. **Mcal_WritePeripEndInitProtReg**
12. **Mcal_GetCpuPhysicalId**
13. **Mcal_GetGlobalDsprAddress**
14. **Mcal_GetLocalDsprAddress**
15. **Mcal_GetGlobalPsprAddress**
16. **Mcal_GetLocalPsprAddress**
17. **Mcal_DelayTickResolution**
18. **Mcal_DelayResetTickCalibration**
19. **Mcal_DelayGetTick**
20. **Mcal_GetCpuIndex**
21. **McalLib_GetVersionInfo**
22. **Mcal_GetSpinlock**
23. **Mcal_ReleaseSpinlock**
24. **Mcal_SetBitAtomic**
25. **Mcal_GetBitAtomic**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **McalLib**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 1

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **unsigned_int**

### 6. BaseTypes

- **包名称**: `BaseTypes`
- **包含元素数量**: 1

#### 包含的元素

##### SW-BASE-TYPE 类型元素

1. **UnsignedInt**

### 7. DataConstrs_compu

- **包名称**: `DataConstrs_compu`
- **包含元素数量**: 1

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **unsignedInt_constr**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. McalLib

- **实现名称**: `McalLib`
- **编程语言**: C
- **软件版本**: 10.40.1
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
