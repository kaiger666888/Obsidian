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

### 1. AURIX2G_Dma

- **包名称**: `AURIX2G_Dma`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Dma**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 19

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Dma_Init**
2. **Dma_IsInitDone**
3. **Dma_ChInit**
4. **Dma_ChUpdate**
5. **Dma_ChEnableHardwareTrigger**
6. **Dma_ChDisableHardwareTrigger**
7. **Dma_ChStartTransfer**
8. **Dma_ChStopTransfer**
9. **Dma_ChStatusClear**
10. **Dma_ChInterruptEnable**
11. **Dma_ChInterruptDisable**
12. **Dma_GetEvents**
13. **Dma_MEStatusClear**
14. **Dma_ChInterruptHandler**
15. **Dma_MEInterruptDispatcher**
16. **Dma_GetCrcValue**
17. **Dma_GetCurrentTimeStamp**
18. **Dma_IsChannelInitDone**
19. **Dma_InitCheck**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Dma**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 12

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Dma_ChannelNotificationFnPtrType**
2. **Dma_EventsType**
3. **Dma_ConfigUpdateType**
4. **Dma_CrcType**
5. **Dma_MoveEngineErrorNotificationPtrType**
6. **Dma_MoveEngineListType**
7. **Dma_ChannelMapType**
8. **Dma_CoreSpecificChConfigType**
9. **Dma_TransactionCtrlSetType**
10. **Dma_ChConfigType**
11. **Dma_ResourcePartitionConfigType**
12. **Dma_ConfigType**

### 6. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 3

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Dma_EventsType**
2. **Dma_CrcType**
3. **Dma_MoveEngineListType**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Dma

- **实现名称**: `Dma`
- **编程语言**: C
- **软件版本**: 10.40.1
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
