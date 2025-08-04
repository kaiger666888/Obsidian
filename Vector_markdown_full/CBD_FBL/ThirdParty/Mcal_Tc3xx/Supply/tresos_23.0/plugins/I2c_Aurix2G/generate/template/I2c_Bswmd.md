# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:33

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

### 1. AURIX2G_I2c

- **包名称**: `AURIX2G_I2c`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **I2c**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 12

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **I2c_Init**
2. **I2c_DeInit**
3. **I2c_SyncWrite**
4. **I2c_AsyncWrite**
5. **I2c_SyncRead**
6. **I2c_AsyncRead**
7. **I2c_GetStatus**
8. **I2c_CancelOperation**
9. **I2c_GetVersionInfo**
10. **I2c_IsrI2cDtr**
11. **I2c_IsrI2cProtocol**
12. **I2c_IsrI2cError**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **I2c**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 11

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **I2c_ChannelType**
2. **I2c_SizeType**
3. **I2c_DataType**
4. **I2c_SlaveAddrType**
5. **I2c_ChannelStatusType**
6. **I2c_AddressingModeType**
7. **I2c_ConfigType**
8. **I2c_ChannelConfigType**
9. **I2c_NotifType**
10. **I2c_ErrorType**
11. **I2c_NotifFunctionPtrType**

### 6. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 3

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **I2c_ErrorType**
2. **I2c_ChannelStatusType**
3. **I2c_AddressingModeType**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. I2c

- **实现名称**: `I2c`
- **编程语言**: C
- **软件版本**: 10.40.0
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
