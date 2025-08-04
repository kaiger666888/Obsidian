# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:11

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **6** 个包：

### 1. AURIX2G_Iom

- **包名称**: `AURIX2G_Iom`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Iom**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 21

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Iom_Init**
2. **Iom_DeInit**
3. **Iom_ResetKernel**
4. **Iom_GetResetStatus**
5. **Iom_ClrResetStatus**
6. **Iom_ClrFpcEdgeStatus**
7. **Iom_GetFpcEdgeStatus**
8. **Iom_SetFpcCompare**
9. **Iom_GetFpcCompare**
10. **Iom_SetLamConfig**
11. **Iom_GetLamConfig**
12. **Iom_SetLamThreshold**
13. **Iom_GetLamThreshold**
14. **Iom_GetLamEntWinCount**
15. **Iom_SetEcmGlobalEveSel**
16. **Iom_GetEcmGlobalEveSel**
17. **Iom_SetEcmThresVal**
18. **Iom_GetEcmThresVal**
19. **Iom_GetEcmEveTrigHis**
20. **Iom_ClrEcmStatusHistory**
21. **Iom_GetVersionInfo**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Iom**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 14

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Iom_EventHistory**
2. **Iom_RstStatusType**
3. **Iom_FpcStatusType**
4. **Iom_Ecm_ThresType**
5. **Iom_Fpc_CompareType**
6. **Iom_Ecm_EveHisType**
7. **Iom_Lam_ConfigType**
8. **Iom_Lam_ThresType**
9. **Iom_Lam_CountType**
10. **Iom_Ecm_EveSelType**
11. **Iom_FpcConfigType**
12. **Iom_LamConfigType**
13. **Iom_EcmConfigType**
14. **Iom_ConfigType**

### 6. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 1

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Iom_EventHistory**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Iom

- **实现名称**: `Iom`
- **编程语言**: C
- **软件版本**: 10.40.0
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
