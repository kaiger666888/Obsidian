# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:49:17

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

### 1. AUTOSAR_Dio

- **包名称**: `AUTOSAR_Dio`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Dio**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 6

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Dio_ReadChannel**
2. **Dio_WriteChannel**
3. **Dio_ReadPort**
4. **Dio_WritePort**
5. **Dio_ReadChannelGroup**
6. **Dio_WriteChannelGroup**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Dio**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 5

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Dio_ChannelGroupType**
2. **Dio_ChannelType**
3. **Dio_LevelType**
4. **Dio_PortType**
5. **Dio_PortLevelType**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Dio

- **实现名称**: `Dio`
- **编程语言**: C
- **软件版本**: 10.40.0
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
