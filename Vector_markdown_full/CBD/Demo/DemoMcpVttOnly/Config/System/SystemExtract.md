# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:13

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00046.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **24** 个包：

### 1. Communication

- **UUID**: `0a9b246c9e373afb9330a953844b3b6e`
- **包名称**: `Communication`
- **包含元素数量**: 0

### 2. DataTransformation

- **UUID**: `bd41cf36a4a136fc81592f3b1c3660df`
- **包名称**: `DataTransformation`
- **包含元素数量**: 1

#### 包含的元素

##### DATA-TRANSFORMATION-SET 类型元素

1. **TransformerConfiguration**

### 3. Diagnostics

- **UUID**: `ef78db009409358f81d701061368e950`
- **包名称**: `Diagnostics`
- **包含元素数量**: 2

#### 包含的元素

##### DIAGNOSTIC-CONNECTION 类型元素

1. **DC_0EF8115B_MyECU**
2. **DC_E001_MyECU**

### 4. Frames

- **UUID**: `644b31cca3f63b8aa8f86bf533b94a9a`
- **包名称**: `Frames`
- **包含元素数量**: 13

#### 包含的元素

##### CAN-FRAME 类型元素

1. **frm_CanNode1_to_MyECUboth**
2. **frm_DiagRequest_All_Tp**
3. **frm_DiagRequest_MyECU_Tp**
4. **frm_DiagResponse_MyECU_Tp**
5. **frm_MyECU2nd_to_MyECU**
6. **frm_MyECU_to_CanNode1**
7. **frm_MyECU_to_MyECU2nd**
8. **frm_nm_Appl**
9. **frm_nm_MyECU**

##### LIN-UNCONDITIONAL-FRAME 类型元素

1. **frm_LinSlaveX_to_MyECU**
2. **frm_MasterReq_Tp**
3. **frm_MyECU_to_LinSlaveX**
4. **frm_SlaveResp_Tp**

### 5. NetworkManagement

- **UUID**: `d97be474d70931dca0bc034ced0b9322`
- **包名称**: `NetworkManagement`
- **包含元素数量**: 1

#### 包含的元素

##### NM-CONFIG 类型元素

1. **NmConfig**

### 6. PDUs

- **UUID**: `8ea7d5f648373dcb81a5df496ef28b08`
- **包名称**: `PDUs`
- **包含元素数量**: 38

#### 包含的元素

##### DCM-I-PDU 类型元素

1. **pdu_DiagRequest_All**
2. **pdu_DiagRequest_MyECU**
3. **pdu_DiagResponse_MyECU**
4. **pdu_DoIpRequest_All**
5. **pdu_DoIpRequest_MyECU**
6. **pdu_DoIpResponse_MyECU**
7. **pdu_MasterReq_LinSlaveX**
8. **pdu_SlaveResp_LinSlaveX**

##### GENERAL-PURPOSE-PDU 类型元素

1. **DoIPRequest_TCP01**
2. **DoIPRequest_TCP02**
3. **DoIPRequest_UDP**
4. **DoIPResponse_TCP01**
5. **DoIPResponse_TCP02**
6. **DoIPResponse_UDP**
7. **DoIPResponse_UDP_BC**
8. **SD_Ctrl_Rx_Multicast**
9. **SD_Ctrl_Rx_MyECU**
10. **SD_Ctrl_Tx_MyECU**

##### I-SIGNAL-I-PDU-GROUP 类型元素

1. **MyECU_CanCluster_Rx**
2. **MyECU_CanCluster_Tx**
3. **MyECU_LinClusterX_Rx**
4. **MyECU_LinClusterX_Tx**

##### I-SIGNAL-I-PDU 类型元素

1. **pdu_CanNode1_to_MyECUboth**
2. **pdu_EthNode1_to_MyECU_call**
3. **pdu_EthNode1_to_MyECU_return**
4. **pdu_LinSlaveX_to_MyECU**
5. **pdu_MyECU2nd_to_MyECU**
6. **pdu_MyECU_to_CanNode1**
7. **pdu_MyECU_to_EventGroup**
8. **pdu_MyECU_to_LinSlaveX**
9. **pdu_MyECU_to_MyECU2nd**

##### N-PDU 类型元素

1. **pdu_DiagRequest_All_Tp**
2. **pdu_DiagRequest_MyECU_Tp**
3. **pdu_DiagResponse_MyECU_Tp**
4. **pdu_MasterReq_Tp**
5. **pdu_SlaveResp_Tp**

##### NM-PDU 类型元素

1. **pdu_nm_Appl**
2. **pdu_nm_MyECU**

### 7. Signals

- **UUID**: `8d148d7186933bf681808a1b3ce3d0b3`
- **包名称**: `Signals`
- **包含元素数量**: 21

#### 包含的元素

##### I-SIGNAL 类型元素

1. **sig_CanNode1_to_MyECUboth_A**
2. **sig_CanNode1_to_MyECUboth_B**
3. **sig_EthNode1_to_MyECU_call**
4. **sig_EthNode1_to_MyECU_return**
5. **sig_LinSlaveX_to_MyECU_A**
6. **sig_LinSlaveX_to_MyECU_B**
7. **sig_LinSlaveX_to_MyECU_C**
8. **sig_LinSlaveX_to_MyECU_RsErr**
9. **sig_MyECU2nd_to_MyECU_A**
10. **sig_MyECU2nd_to_MyECU_B**
11. **sig_MyECU_to_CanNode1_A**
12. **sig_MyECU_to_CanNode1_B**
13. **sig_MyECU_to_EventGroup**
14. **sig_MyECU_to_LinSlaveX_A**
15. **sig_MyECU_to_LinSlaveX_B**
16. **sig_MyECU_to_MyECU2nd_A**
17. **sig_MyECU_to_MyECU2nd_B**
18. **sig_nm_Appl_A**
19. **sig_nm_Appl_B**
20. **sig_nm_MyECU_A**
21. **sig_nm_MyECU_B**

### 8. SystemSignals

- **UUID**: `c804a5701d0931fc916944b1da5613ca`
- **包名称**: `SystemSignals`
- **包含元素数量**: 31

#### 包含的元素

##### SYSTEM-SIGNAL 类型元素

1. **sys_CanNode1_to_MyECUboth_A**
2. **sys_CanNode1_to_MyECUboth_B**
3. **sys_CanNode2_to_MyECU_A**
4. **sys_CanNode2_to_MyECU_B**
5. **sys_EthNode1_to_MyECU_call**
6. **sys_EthNode1_to_MyECU_return**
7. **sys_LinSlaveX_to_MyECU_A**
8. **sys_LinSlaveX_to_MyECU_B**
9. **sys_LinSlaveX_to_MyECU_C**
10. **sys_LinSlaveX_to_MyECU_RsErr**
11. **sys_LinSlaveY_to_MyECU_A**
12. **sys_LinSlaveY_to_MyECU_B**
13. **sys_LinSlaveY_to_MyECU_C**
14. **sys_LinSlaveY_to_MyECU_RsErr**
15. **sys_MyECU2nd_to_MyECU_A**
16. **sys_MyECU2nd_to_MyECU_B**
17. **sys_MyECU_to_CanNode1_A**
18. **sys_MyECU_to_CanNode1_B**
19. **sys_MyECU_to_CanNode2_A**
20. **sys_MyECU_to_CanNode2_B**
21. **sys_MyECU_to_EventGroup**
22. **sys_MyECU_to_LinSlaveX_A**
23. **sys_MyECU_to_LinSlaveX_B**
24. **sys_MyECU_to_LinSlaveY_A**
25. **sys_MyECU_to_LinSlaveY_B**
26. **sys_MyECU_to_MyECU2nd_A**
27. **sys_MyECU_to_MyECU2nd_B**
28. **sys_nm_Appl_A**
29. **sys_nm_Appl_B**
30. **sys_nm_MyECU_A**
31. **sys_nm_MyECU_B**

### 9. TransportProtocol

- **UUID**: `f5fa874a19563e6293112070b1b1de08`
- **包名称**: `TransportProtocol`
- **包含元素数量**: 3

#### 包含的元素

##### CAN-TP-CONFIG 类型元素

1. **TP_CanCluster**

##### DO-IP-TP-CONFIG 类型元素

1. **TP_EthernetCluster**

##### LIN-TP-CONFIG 类型元素

1. **TP_LinClusterX**

### 10. Constants

- **UUID**: `39361e6423b83087acdf88a806d830a3`
- **包名称**: `Constants`
- **包含元素数量**: 1

#### 包含的元素

##### CONSTANT-SPECIFICATION 类型元素

1. **InitValueSW_RS_0**

### 11. DataTypeMappingSets

- **UUID**: `3a9d9d5ba064311caf68b24ed18841b5`
- **包名称**: `DataTypeMappingSets`
- **包含元素数量**: 1

#### 包含的元素

##### DATA-TYPE-MAPPING-SET 类型元素

1. **DataTypeMappings**

### 12. DataTypes

- **UUID**: `f771792e92c533f297a1b6eb53ac2ad9`
- **包名称**: `DataTypes`
- **包含元素数量**: 0

### 13. ApplicationDataTypes

- **UUID**: `601e6d60b0f93899bf506b2d633dd39d`
- **包名称**: `ApplicationDataTypes`
- **包含元素数量**: 2

#### 包含的元素

##### APPLICATION-PRIMITIVE-DATA-TYPE 类型元素

1. **ApplicationValueType**

##### APPLICATION-RECORD-DATA-TYPE 类型元素

1. **ApplicationRecordType**

### 14. BaseTypes

- **UUID**: `52bf5f499fbc3c2687e8f61a9e45cd41`
- **包名称**: `BaseTypes`
- **包含元素数量**: 3

#### 包含的元素

##### SW-BASE-TYPE 类型元素

1. **boolean**
2. **uint32**
3. **uint8**

### 15. CompuMethods

- **UUID**: `d0c477af727330c9bba069b6d9b3d249`
- **包名称**: `CompuMethods`
- **包含元素数量**: 1

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Identical**

### 16. ImplementationDataTypes

- **UUID**: `f98090829fe83006adf84d1317881500`
- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 2

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **ImplementationRecord**
2. **uint8**

### 17. SoAdRoutingGroups

- **UUID**: `c3352b5079433f49b50406f9c84cc5a3`
- **包名称**: `SoAdRoutingGroups`
- **包含元素数量**: 2

#### 包含的元素

##### SO-AD-ROUTING-GROUP 类型元素

1. **SoAdRG_EventGroup**
2. **SoAdRG_Method**

### 18. SoftwareTypes

- **UUID**: `a6d3ea9731e031668c161933c19cb8d6`
- **包名称**: `SoftwareTypes`
- **包含元素数量**: 0

### 19. ComponentTypes

- **UUID**: `5a099a20b9943503bdbfb2d67e1094a4`
- **包名称**: `ComponentTypes`
- **包含元素数量**: 2

#### 包含的元素

##### APPLICATION-SW-COMPONENT-TYPE 类型元素

1. **ApplicationSWComponentType**

##### COMPOSITION-SW-COMPONENT-TYPE 类型元素

1. **MyECUEcuComp**

### 20. Interfaces

- **UUID**: `343af3c2383e360e8acf537589d92d54`
- **包名称**: `Interfaces`
- **包含元素数量**: 2

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **ServiceInterface**

##### SENDER-RECEIVER-INTERFACE 类型元素

1. **MyECU_to_EventGroupInterface**

### 21. System

- **UUID**: `9a0722db13d534ebbe5fe34b8e780bdb`
- **包名称**: `System`
- **包含元素数量**: 1

#### 包含的元素

##### SYSTEM 类型元素

1. **System**

### 22. Topology

- **UUID**: `e02953f3dc2732e4a64a0d10e1f81c98`
- **包名称**: `Topology`
- **包含元素数量**: 0

### 23. Clusters

- **UUID**: `d3b99285c5933f55ac710621851679ed`
- **包名称**: `Clusters`
- **包含元素数量**: 3

#### 包含的元素

##### CAN-CLUSTER 类型元素

1. **CanCluster**

##### ETHERNET-CLUSTER 类型元素

1. **EthernetCluster**

##### LIN-CLUSTER 类型元素

1. **LinClusterX**

### 24. HardwareComponents

- **UUID**: `0127c66a2ab03563b55cad94c58faad0`
- **包名称**: `HardwareComponents`
- **包含元素数量**: 1

#### 包含的元素

##### ECU-INSTANCE 类型元素

1. **MyECU**
