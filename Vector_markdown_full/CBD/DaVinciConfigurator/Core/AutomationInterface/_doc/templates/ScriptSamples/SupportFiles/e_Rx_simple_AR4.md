# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:04

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **18** 个包：

### 1. ComponentType

- **包名称**: `ComponentType`
- **包含元素数量**: 2

#### 包含的元素

##### APPLICATION-SW-COMPONENT-TYPE 类型元素

1. **CT_App**

##### SWC-IMPLEMENTATION 类型元素

1. **CT_App_Implementation**

### 2. Constant

- **包名称**: `Constant`
- **包含元素数量**: 1

#### 包含的元素

##### CONSTANT-SPECIFICATION 类型元素

1. **cInit**

### 3. DataType

- **包名称**: `DataType`
- **包含元素数量**: 1

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Signal_Bool**

### 4. DaVinci

- **包名称**: `DaVinci`
- **包含元素数量**: 0

### 5. ABC_ClusterCANCluster

- **包名称**: `ABC_ClusterCANCluster`
- **包含元素数量**: 1

#### 包含的元素

##### CAN-CLUSTER 类型元素

1. **CANCluster**

### 6. ABC_Frame

- **包名称**: `ABC_Frame`
- **包含元素数量**: 1

#### 包含的元素

##### CAN-FRAME 类型元素

1. **Msg_Bool**

### 7. ABC_ISignal

- **包名称**: `ABC_ISignal`
- **包含元素数量**: 1

#### 包含的元素

##### I-SIGNAL 类型元素

1. **Signal_Bool_Msg_Bool**

### 8. ABC_PDU

- **包名称**: `ABC_PDU`
- **包含元素数量**: 1

#### 包含的元素

##### I-SIGNAL-I-PDU 类型元素

1. **Msg_Bool**

### 9. ABC_ECU

- **包名称**: `ABC_ECU`
- **包含元素数量**: 1

#### 包含的元素

##### ECU-INSTANCE 类型元素

1. **e_Rx_simple**

### 10. ABC_PDUGroup

- **包名称**: `ABC_PDUGroup`
- **包含元素数量**: 2

#### 包含的元素

##### PDUR-I-PDU-GROUP 类型元素

1. **e_Rx_simple_CANCluster_Rx**
2. **e_Rx_simple_CANCluster_Tx**

### 11. ECUComposition

- **包名称**: `ECUComposition`
- **包含元素数量**: 1

#### 包含的元素

##### COMPOSITION-SW-COMPONENT-TYPE 类型元素

1. **EcuSwComposition**

### 12. ECUCompositionType

- **包名称**: `ECUCompositionType`
- **包含元素数量**: 1

#### 包含的元素

##### COMPOSITION-SW-COMPONENT-TYPE 类型元素

1. **EcuSwComposition**

### 13. PortInterface

- **包名称**: `PortInterface`
- **包含元素数量**: 1

#### 包含的元素

##### SENDER-RECEIVER-INTERFACE 类型元素

1. **Signal_Bool**

### 14. Signal

- **包名称**: `Signal`
- **包含元素数量**: 1

#### 包含的元素

##### SYSTEM-SIGNAL 类型元素

1. **Signal_Bool**

### 15. VehicleProject

- **包名称**: `VehicleProject`
- **包含元素数量**: 1

#### 包含的元素

##### SYSTEM 类型元素

1. **e_Rx_simple**

### 16. AR4_TemporaryElements

- **包名称**: `AR4_TemporaryElements`
- **包含元素数量**: 0

### 17. DataConstrain

- **包名称**: `DataConstrain`
- **包含元素数量**: 1

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **Signal_Bool_DataConstrain**

### 18. BaseType

- **包名称**: `BaseType`
- **包含元素数量**: 1

#### 包含的元素

##### SW-BASE-TYPE 类型元素

1. **Signal_Bool**
