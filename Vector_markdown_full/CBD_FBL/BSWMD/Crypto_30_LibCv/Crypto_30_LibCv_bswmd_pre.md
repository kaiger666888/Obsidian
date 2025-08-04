# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:00

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. Crypto_30_LibCv

- **UUID**: `b4b8e5dd-7621-44f5-b0d0-70346b08094c`
- **包名称**: `Crypto_30_LibCv`
- **包含元素数量**: 3

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Crypto_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Crypto_Rec**
2. **Crypto_Pre**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Crypto_Impl

- **UUID**: `1a1491f6-7cc9-49cb-a255-e18167548a83`
- **实现名称**: `Crypto_Impl`
- **编程语言**: C
- **软件版本**: 8.05.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Crypto_Rec

- **UUID**: `b1820846-3feb-4ece-982d-dc4980cca7b1`
- **配置名称**: `Crypto_Rec`
- **定义引用**: `/MICROSAR/Crypto_30_LibCv/Crypto`

### 2. Crypto_Pre

- **UUID**: `c83de28b-6024-4c92-a86b-93ce6e6d7f7c`
- **配置名称**: `Crypto_Pre`
- **定义引用**: `/MICROSAR/Crypto_30_LibCv/Crypto`
