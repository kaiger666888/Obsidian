# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:49:21

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

### 1. AUTOSAR_Spi

- **包名称**: `AUTOSAR_Spi`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Spi**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 16

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Spi_Init**
2. **Spi_DeInit**
3. **Spi_AsyncTransmit**
4. **Spi_SetupEB**
5. **Spi_GetStatus**
6. **Spi_GetJobResult**
7. **Spi_GetSequenceResult**
8. **Spi_SyncTransmit**
9. **Spi_GetHWUnitStatus**
10. **Spi_SetAsyncMode**
11. **Spi_ControlLoopBack**
12. **Spi_IsrQspiPT2**
13. **Spi_IsrQspiError**
14. **Spi_QspiDmaCallout**
15. **Spi_QspiDmaErrCallout**
16. **Spi_MainFunction_Handling**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Spi**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 21

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Spi_AsyncModeType**
2. **Spi_JobEndNotification**
3. **Spi_JobResultType**
4. **Spi_SeqEndNotification**
5. **Spi_SeqResultType**
6. **Spi_StatusType**
7. **Spi_DataBufferType**
8. **Spi_NumberOfDataType**
9. **Spi_ChannelType**
10. **Spi_JobType**
11. **Spi_SequenceType**
12. **Spi_HWUnitType**
13. **Spi_LoopBackType**
14. **Spi_QSPIHwMapConfigType**
15. **Spi_ChannelConfigType**
16. **Spi_ConfigType**
17. **Spi_CoreChannelOffsetType**
18. **Spi_CoreConfigType**
19. **Spi_JobConfigType**
20. **Spi_QspiHwConfigType**
21. **Spi_SequenceConfigType**

### 6. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 5

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Spi_AsyncModeType**
2. **Spi_LoopBackType**
3. **Spi_JobResultType**
4. **Spi_SeqResultType**
5. **Spi_StatusType**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Spi

- **实现名称**: `Spi`
- **编程语言**: C
- **软件版本**: 10.40.2
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
