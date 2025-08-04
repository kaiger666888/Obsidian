# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:52:02

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

### 1. AUTOSAR_Fee

- **包名称**: `AUTOSAR_Fee`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Fee**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 20

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Fee_Init**
2. **Fee_SetMode**
3. **Fee_Read**
4. **Fee_Write**
5. **Fee_Cancel**
6. **Fee_GetStatus**
7. **Fee_GetJobResult**
8. **Fee_InvalidateBlock**
9. **Fee_EraseImmediateBlock**
10. **Fee_JobEndNotification**
11. **Fee_JobErrorNotification**
12. **Fee_17_EnableGcStart**
13. **Fee_17_DisableGcStart**
14. **Fee_MainFunction**
15. **Fee_17_IllegalStateNotification**
16. **Fee_17_JobEraseErrorNotification**
17. **Fee_17_JobProgErrorNotification**
18. **Fee_17_EraseQuasiStaticData**
19. **Fee_17_GetQuasiStaticBlockInfo**
20. **Fee_17_GetQuasiStaticJobResult**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Fee**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 16

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Fee_BlockType**
2. **Fee_NotifFunctionPtrType**
3. **Fee_PageType**
4. **Fee_QsBlock_StateType**
5. **Fee_CacheStatusType**
6. **Fee_CacheType**
7. **Fee_ConfigType**
8. **Fee_GcBlkInfoType**
9. **Fee_GCConfigType**
10. **Fee_LastWrittenBlkInfoType**
11. **Fee_PendReqBufType**
12. **Fee_QuasiStaticBlockInfoType**
13. **Fee_SectorInfoType**
14. **Fee_SectorStatusType**
15. **Fee_StateDataType**
16. **Fee_StatusFlagsType**

### 6. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 1

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Fee_QsBlock_StateType**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Fee

- **实现名称**: `Fee`
- **编程语言**: C
- **软件版本**: 2.0.0
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
