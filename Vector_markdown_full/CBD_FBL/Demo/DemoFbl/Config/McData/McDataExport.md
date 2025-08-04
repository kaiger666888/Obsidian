# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:49:44

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **18** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **ComM_Impl**
2. **DoIPInt_Impl**
3. **PduR_Impl**
4. **SoAd_Impl**

### 2. ComM_ib_bswmd

- **UUID**: `ad6a82b9-d715-420f-80a7-43c74f95392a`
- **包名称**: `ComM_ib_bswmd`
- **包含元素数量**: 0

### 3. BswModuleDescriptions

- **UUID**: `5c89617e-7230-4bd1-80c2-9c7654c6fd97`
- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 2

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **ComM**

##### BSW-MODULE-ENTRY 类型元素

1. **ComM_MainFunction_0**

### 4. XcpEvents

- **UUID**: `fa0cdb9c-cc4d-4474-b303-c6740d1d7c4c`
- **包名称**: `XcpEvents`
- **包含元素数量**: 0

### 5. DoIPInt_ib_bswmd

- **UUID**: `ed7f159c-1ebe-47a4-8a50-7df830f0fbc1`
- **包名称**: `DoIPInt_ib_bswmd`
- **包含元素数量**: 0

### 6. BswModuleDescriptions

- **UUID**: `b65bd732-9c7b-4247-85f9-53906b5fd852`
- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 2

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **DoIPInt**

##### BSW-MODULE-ENTRY 类型元素

1. **DoIPInt_MainFunction**

### 7. XcpEvents

- **UUID**: `ec820385-59ac-4aaa-9612-290b90b1c208`
- **包名称**: `XcpEvents`
- **包含元素数量**: 0

### 8. FblCw_ib_bswmd

- **UUID**: `8112fd4f-5903-43af-83f8-43cd16162e81`
- **包名称**: `FblCw_ib_bswmd`
- **包含元素数量**: 0

### 9. XcpEvents

- **UUID**: `42eeabaf-f4cc-4578-bd9d-32e8c4f9e26c`
- **包名称**: `XcpEvents`
- **包含元素数量**: 0

### 10. PduR_ib_bswmd

- **UUID**: `48e7ecf2-286b-4b4c-a30a-ae248f1cfa9e`
- **包名称**: `PduR_ib_bswmd`
- **包含元素数量**: 0

### 11. BswModuleDescriptions

- **UUID**: `153c1d92-fed0-4d13-b498-db5b75df636f`
- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **PduR**

### 12. XcpEvents

- **UUID**: `236e8733-18e0-4470-b2f5-af54797a54bc`
- **包名称**: `XcpEvents`
- **包含元素数量**: 0

### 13. SoAd_ib_bswmd

- **UUID**: `111eceb3-a994-4db9-be60-88affbf6daac`
- **包名称**: `SoAd_ib_bswmd`
- **包含元素数量**: 0

### 14. BswModuleDescriptions

- **UUID**: `caa5d63f-d34a-49f7-9247-82c1453851f6`
- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 2

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **SoAd**

##### BSW-MODULE-ENTRY 类型元素

1. **SoAd_MainFunction**

### 15. XcpEvents

- **UUID**: `42a7efad-6bd9-449a-8242-592cee9a7551`
- **包名称**: `XcpEvents`
- **包含元素数量**: 0

### 16. MICROSARFBL

- **UUID**: `2e83f445-6582-4070-922e-cd2fec8bf60a`
- **包名称**: `MICROSARFBL`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Dcm_Impl**

### 17. Dcm_ib_bswmd

- **UUID**: `3b5a19e4-1ac8-49b9-8f04-b5abe37da636`
- **包名称**: `Dcm_ib_bswmd`
- **包含元素数量**: 0

### 18. BswModuleDescriptions

- **UUID**: `fa8e9d34-c79a-4110-a803-0170339d2340`
- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Dcm**

## ⚡ 实现信息

此ARXML文件包含 **5** 个实现：

### 1. ComM_Impl

- **UUID**: `b484d690-bf7b-4b49-8cc0-23ce231b62c3`
- **实现名称**: `ComM_Impl`
- **编程语言**: C
- **软件版本**: 13.00.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

### 2. DoIPInt_Impl

- **UUID**: `494ff045-db42-43ac-9c29-43bf56637310`
- **实现名称**: `DoIPInt_Impl`
- **编程语言**: C
- **软件版本**: 2.00.02
- **供应商ID**: 30
- **AUTOSAR版本**: 4.02.02
- **代码生成器**: DaVinci Configurator

### 3. PduR_Impl

- **UUID**: `4a156671-5151-4f19-a8b4-579effc27f33`
- **实现名称**: `PduR_Impl`
- **编程语言**: C
- **软件版本**: 15.04.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.01.02
- **代码生成器**: DaVinci Configurator

### 4. SoAd_Impl

- **UUID**: `e2b22e5d-7458-491d-9936-688488e6f364`
- **实现名称**: `SoAd_Impl`
- **编程语言**: C
- **软件版本**: 16.05.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.02.02
- **代码生成器**: DaVinci Configurator

### 5. Dcm_Impl

- **UUID**: `c2d49cc4-56d4-45bc-b9e1-498ac0f93e78`
- **实现名称**: `Dcm_Impl`
- **编程语言**: C
- **软件版本**: 8.03.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator
