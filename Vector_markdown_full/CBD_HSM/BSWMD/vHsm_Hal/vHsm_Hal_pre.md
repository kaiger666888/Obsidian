# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:59

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)
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
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **vHsm_Rec**

### 2. vHsm_Hal

- **UUID**: `b4b8e5dd-7621-44f5-b0d0-70346b08094c`
- **包名称**: `vHsm_Hal`
- **包含元素数量**: 2

#### 包含的元素

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Crypto_Pre**
2. **Crypto_Rec**

## ⚙️ 配置信息

此ARXML文件包含 **3** 个配置：

### 1. vHsm_Rec

- **UUID**: `8a2de420-fb36-4f78-b131-cbefede83416`
- **配置名称**: `vHsm_Rec`
- **定义引用**: `/MICROSAR/vHsm`

### 2. Crypto_Pre

- **UUID**: `c7df8df1-bd13-4b7f-a1b5-a075c9896285`
- **配置名称**: `Crypto_Pre`
- **定义引用**: `/MICROSAR/vHsm_Hal/Crypto`

### 3. Crypto_Rec

- **UUID**: `f16665ad-5bab-47f2-9dbb-0fb7e21f7ff3`
- **配置名称**: `Crypto_Rec`
- **定义引用**: `/MICROSAR/vHsm_Hal/Crypto`
