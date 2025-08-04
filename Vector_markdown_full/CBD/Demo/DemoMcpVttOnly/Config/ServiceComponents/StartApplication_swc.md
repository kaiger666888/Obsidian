# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:11

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00046.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **7** 个包：

### 1. StartApplication

- **UUID**: `cd7fb1b1-16c7-40b4-b10b-49c8cc0a0849`
- **包名称**: `StartApplication`
- **包含元素数量**: 0

### 2. StartApplication_swc

- **UUID**: `8c8bab3f-6207-4e26-8ebe-012e9bf273f1`
- **包名称**: `StartApplication_swc`
- **包含元素数量**: 0

### 3. DataTypes

- **UUID**: `d49e8b37-abf4-4a85-8fd7-369d3ee32dc5`
- **包名称**: `DataTypes`
- **包含元素数量**: 15

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **IdtUint8Array_508**
2. **DtEthernetCommunicationDataElementType**
3. **IdtEthernetCommunicationInfo**
4. **EnumMEM_BlockStateType**
5. **EnumNM_ApplStateType**
6. **ComM_ModeType**
7. **NvM_ServiceIdType**
8. **NvM_RequestResultType**
9. **Dem_EventStatusType**
10. **Dem_OperationCycleStateType**
11. **Dcm_Data2ByteType**
12. **Dcm_NegativeResponseCodeType**
13. **DataArray_Type_2**
14. **WdgM_CheckpointIdType**
15. **EnumActiveComponentType**

### 4. DataConstrs

- **UUID**: `3bee520b-a1bd-489c-ae7d-d09cd54c091d`
- **包名称**: `DataConstrs`
- **包含元素数量**: 9

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **EnumMEM_BlockStateType_Constr**
2. **EnumNM_ApplStateType_Constr**
3. **ComM_ModeType_Constr**
4. **NvM_ServiceIdType_Constr**
5. **NvM_RequestResultType_Constr**
6. **Dem_EventStatusType_Constr**
7. **Dem_OperationCycleStateType_Constr**
8. **Dcm_NegativeResponseCodeType_Constr**
9. **EnumActiveComponentType_Constr**

### 5. CompuMethods

- **UUID**: `9d9b78a9-ba93-46aa-a438-28f42166bcf5`
- **包名称**: `CompuMethods`
- **包含元素数量**: 9

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **EnumMEM_BlockStateType**
2. **EnumNM_ApplStateType**
3. **EnumActiveComponentType**
4. **ComM_ModeType**
5. **NvM_ServiceIdType**
6. **NvM_RequestResultType**
7. **Dem_EventStatusType**
8. **Dem_OperationCycleStateType**
9. **Dcm_NegativeResponseCodeType**

### 6. Interfaces

- **UUID**: `bca973e1-2443-42af-9e18-089bf64c3e89`
- **包名称**: `Interfaces`
- **包含元素数量**: 20

#### 包含的元素

##### SENDER-RECEIVER-INTERFACE 类型元素

1. **PiGeneric**
2. **PiEthernetCommunication**
3. **Pisig_MyECU_to_LinSlaveX_A_5401d589_Tx**
4. **Pisig_MyECU_to_CanNode1_B_d718add7_Tx**
5. **Pisig_LinSlaveX_to_MyECU_A_7f2584dc_Rx**
6. **Pisig_MyECU_to_CanNode1_A_4e11fc6d_Tx**
7. **Pisig_CanNode1_to_MyECUboth_B_b620be75_Rx**
8. **Pisig_CanNode1_to_MyECUboth_A_2f29efcf_Rx**

##### CLIENT-SERVER-INTERFACE 类型元素

1. **PiUR_CN_MyECU_CanCluster_039555d1**
2. **PiUR_CN_MyECU_LinClusterX_b6c35bc1**
3. **PiUR_CN_MyECU_EthernetCluster_4610953d**
4. **PiPS_StartApplication_NvMBlock1**
5. **PiNvM_RpNotifyJobEnd_StartApplication_NvMBlock1**
6. **PiPS_StartApplication_NvMBlock2**
7. **PiNvM_RpNotifyJobEnd_StartApplication_NvMBlock2**
8. **PiDiagnosticMonitor_DEM_EVENT_StartApplication**
9. **PiDemOpCycle_PowerCycle**
10. **PiDcmDataService_DID_StartApplication**
11. **PiDemDataService_DemDataElementClass_StartApplication**
12. **PiAliveWdgMSupervisedEntity_StartApplication_WdgMCheckpoint_StartApplication**

### 7. ComponentTypes

- **UUID**: `52da3911-0994-45c4-bc61-d2f39e076836`
- **包名称**: `ComponentTypes`
- **包含元素数量**: 4

#### 包含的元素

##### APPLICATION-SW-COMPONENT-TYPE 类型元素

1. **StartApplication**

##### SWC-IMPLEMENTATION 类型元素

1. **StartApplicationImplementation**
2. **StartApplicationEthImplementation**

##### COMPLEX-DEVICE-DRIVER-SW-COMPONENT-TYPE 类型元素

1. **StartApplicationEth**
