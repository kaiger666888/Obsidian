# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:49:18

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

### 1. AUTOSAR_Port

- **包名称**: `AUTOSAR_Port`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Port**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Port_Init**
2. **Port_SetPinDirection**
3. **Port_RefreshPortDirection**
4. **Port_SetPinMode**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Port**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 9

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Port_PinDirectionType**
2. **Port_PinModeType**
3. **Port_PinType**
4. **Port_ConfigType**
5. **Port_n_ConfigType**
6. **Port_n_ControlType**
7. **Port_n_LVDSConfigType**
8. **Port_n_ModeType**
9. **Port_n_PinType**

### 6. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 1

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Port_PinDirectionType**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Port

- **实现名称**: `Port`
- **编程语言**: C
- **软件版本**: 10.40.1
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
