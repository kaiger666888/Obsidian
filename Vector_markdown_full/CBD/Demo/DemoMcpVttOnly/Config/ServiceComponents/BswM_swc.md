# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:09

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00046.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **7** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. BswM_swc

- **UUID**: `391366f4-bdcb-41e3-9d36-dc0d1fba0df5`
- **包名称**: `BswM_swc`
- **包含元素数量**: 4

#### 包含的元素

##### MODE-DECLARATION-GROUP 类型元素

1. **ESH_RunRequest**
2. **SDC_SdEventHandlerState**
3. **SDC_SdServerServiceRequest**

##### DATA-TYPE-MAPPING-SET 类型元素

1. **BswMMappingSet**

### 3. DataTypes

- **UUID**: `4de5bced-0416-4318-9d49-363f0ae0b138`
- **包名称**: `DataTypes`
- **包含元素数量**: 3

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **BswM_ESH_RunRequest**
2. **BswM_SDC_SdEventHandlerState**
3. **BswM_SDC_SdServerServiceRequest**

### 4. DataConstrs

- **UUID**: `7eaacd57-204c-43b9-bd03-bdb584de9e82`
- **包名称**: `DataConstrs`
- **包含元素数量**: 3

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **BswM_ESH_RunRequest_Constr**
2. **BswM_SDC_SdEventHandlerState_Constr**
3. **BswM_SDC_SdServerServiceRequest_Constr**

### 5. CompuMethods

- **UUID**: `8071f092-64af-4701-9826-21f07d70e02a`
- **包名称**: `CompuMethods`
- **包含元素数量**: 3

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **BswM_ESH_RunRequest**
2. **BswM_SDC_SdEventHandlerState**
3. **BswM_SDC_SdServerServiceRequest**

### 6. Interfaces

- **UUID**: `a4cffe88-5f18-4412-8810-8c90947f8daa`
- **包名称**: `Interfaces`
- **包含元素数量**: 6

#### 包含的元素

##### MODE-SWITCH-INTERFACE 类型元素

1. **BswM_MSI_ESH_RunRequest**
2. **BswM_MSI_SDC_SdEventHandlerState**
3. **BswM_MSI_SDC_SdServerServiceRequest**

##### SENDER-RECEIVER-INTERFACE 类型元素

1. **BswM_SRI_BswM_MSI_ESH_RunRequest_BswM_MDGP_ESH_RunRequest**
2. **BswM_SRI_BswM_MSI_SDC_SdEventHandlerState_BswM_MDGP_SDC_SdEventHandlerState**
3. **BswM_SRI_BswM_MSI_SDC_SdServerServiceRequest_BswM_MDGP_SDC_SdServerServiceRequest**

### 7. ComponentTypes

- **UUID**: `930b3dbc-99a7-4f34-9eaf-f60f2f382feb`
- **包名称**: `ComponentTypes`
- **包含元素数量**: 2

#### 包含的元素

##### SERVICE-SW-COMPONENT-TYPE 类型元素

1. **BswM**

##### SWC-IMPLEMENTATION 类型元素

1. **BswMImplementation**
