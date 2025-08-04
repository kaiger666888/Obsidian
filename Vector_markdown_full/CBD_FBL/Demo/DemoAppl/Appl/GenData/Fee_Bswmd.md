# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:49:00

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
- **包含元素数量**: 19

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Fee_Init**
2. **Fee_Read**
3. **Fee_Write**
4. **Fee_Cancel**
5. **Fee_GetStatus**
6. **Fee_GetJobResult**
7. **Fee_InvalidateBlock**
8. **Fee_EraseImmediateBlock**
9. **Fee_JobEndNotification**
10. **Fee_JobErrorNotification**
11. **Fee_17_EnableGcStart**
12. **Fee_17_DisableGcStart**
13. **Fee_MainFunction**
14. **Fee_17_IllegalStateNotification**
15. **Fee_17_JobEraseErrorNotification**
16. **Fee_17_JobProgErrorNotification**
17. **Fee_17_EraseQuasiStaticData**
18. **Fee_17_GetQuasiStaticBlockInfo**
19. **Fee_17_GetQuasiStaticJobResult**

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
- **软件版本**: 10.40.2
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
