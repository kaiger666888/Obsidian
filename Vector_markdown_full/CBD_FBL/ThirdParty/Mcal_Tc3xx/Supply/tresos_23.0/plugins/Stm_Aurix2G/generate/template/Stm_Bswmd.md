# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:37

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

### 1. AURIX2G_Stm

- **包名称**: `AURIX2G_Stm`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Stm**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 9

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Stm_EnableModule**
2. **Stm_EnableAlarm**
3. **Stm_DisableAlarm**
4. **Stm_SetCompareMatchControl**
5. **Stm_ReadTimerValue**
6. **Stm_ReadTotalTimerValue**
7. **Stm_SleepModeHandle**
8. **Stm_GetVersionInfo**
9. **Stm_Isr**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Stm**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 2

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Stm_CallbackFnPtrType**
2. **Stm_TotalTimerCaptureType**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Stm

- **实现名称**: `Stm`
- **编程语言**: C
- **软件版本**: 10.30.0
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
