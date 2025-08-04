# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:10

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

### 2. Dcm_swc

- **UUID**: `e2c0c399-fb36-490a-98f3-361ec19ad353`
- **包名称**: `Dcm_swc`
- **包含元素数量**: 5

#### 包含的元素

##### MODE-DECLARATION-GROUP 类型元素

1. **DcmControlDtcSetting**
2. **DcmEcuReset**
3. **DcmDiagnosticSessionControl**
4. **DcmCommunicationControl**

##### DATA-TYPE-MAPPING-SET 类型元素

1. **DcmMappingSet**

### 3. DataTypes

- **UUID**: `10f6f4f7-1003-4c90-9287-f86e9c712ba7`
- **包名称**: `DataTypes`
- **包含元素数量**: 70

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Dcm_ConfirmationStatusType**
2. **Dcm_OpStatusType**
3. **Dcm_NegativeResponseCodeType**
4. **Dcm_ProtocolType**
5. **Dcm_RequestKindType**
6. **Dcm_SecLevelType**
7. **Dcm_SesCtrlType**
8. **Dcm_ControlDtcSettingType**
9. **Dcm_EcuResetType**
10. **Dcm_DiagnosticSessionControlType**
11. **Dcm_CommunicationModeType**
12. **Dcm_Data4ByteType**
13. **Dcm_Data2ByteType**
14. **Dcm_StartDataIn_SampleRoutineControl_In_Option0PrimitiveType**
15. **Dcm_StartDataIn_SampleRoutineControl_In_Option0Type**
16. **Dcm_StartDataOut_SampleRoutineControl_Out_InitStatePrimitiveType**
17. **Dcm_StartDataOut_SampleRoutineControl_Out_InitStateType**
18. **Dcm_StopDataOut_SampleRoutineControl_Out_StopStatePrimitiveType**
19. **Dcm_StopDataOut_SampleRoutineControl_Out_StopStateType**
20. **Dcm_RequestDataOut_SampleRoutineControl_Out_ResultPrimitiveType**
21. **Dcm_RequestDataOut_SampleRoutineControl_Out_ResultType**
22. **Dcm_StartDataIn_SampleRoutineControl_StartOnly_In_Option1ArrayType**
23. **Dcm_StartDataIn_SampleRoutineControl_StartOnly_In_Option1Type**
24. **Dcm_RequestDataOut_SampleRoutineControl_StartOnly_Out_ResultPrimitiveType**
25. **Dcm_RequestDataOut_SampleRoutineControl_StartOnly_Out_ResultType**
26. **Dcm_Data17ByteType**
27. **Dcm_Data15ByteType**
28. **Dcm_Data13ByteType**
29. **Dcm_Data6ByteType**
30. **Dcm_DataElement_DevelopmentData_TransportLayerVersion_PrimitiveType**
31. **Dcm_DataElement_DevelopmentData_TransportLayerVersionType**
32. **Dcm_DataElement_DevelopmentData_CanDriverVersion_PrimitiveType**
33. **Dcm_DataElement_DevelopmentData_CanDriverVersionType**
34. **Dcm_DataElement_DevelopmentData_DiagnosticModuleVersion_PrimitiveType**
35. **Dcm_DataElement_DevelopmentData_DiagnosticModuleVersionType**
36. **Dcm_DataElement_DevelopmentData_NmVersion_PrimitiveType**
37. **Dcm_DataElement_DevelopmentData_NmVersionType**
38. **Dcm_DataElement_DevelopmentData_OperatingSystemVersion_PrimitiveType**
39. **Dcm_DataElement_DevelopmentData_OperatingSystemVersionType**
40. **Dcm_DataElement_Boot_Software_NumberOfModules_PrimitiveType**
41. **Dcm_DataElement_Boot_Software_NumberOfModulesType**
42. **Dcm_DataElement_Boot_Software_Boot_Software_Identification_PrimitiveType**
43. **Dcm_DataElement_Boot_Software_Boot_Software_IdentificationType**
44. **Dcm_DataElement_DID_0x001A_DID_Uint16_Array_ArrayType**
45. **Dcm_DataElement_DID_0x001A_DID_Uint16_ArrayType**
46. **Dcm_DataElement_DID_0x001B_DID_Sint8_Array_ArrayType**
47. **Dcm_DataElement_DID_0x001B_DID_Sint8_ArrayType**
48. **Dcm_DataElement_DID_0xF412_DID_Data_PrimitiveType**
49. **Dcm_DataElement_DID_0xF412_DID_DataType**
50. **Dcm_DataElement_DID_0xF413_DID_Data_PrimitiveType**
51. **Dcm_DataElement_DID_0xF413_DID_DataType**
52. **Dcm_DataElement_DID_0xF410_DID_Data_PrimitiveType**
53. **Dcm_DataElement_DID_0xF410_DID_DataType**
54. **Dcm_DataElement_SerialNumber_SerialNumber_PrimitiveType**
55. **Dcm_DataElement_SerialNumber_SerialNumberType**
56. **Dcm_DataElement_Example_ReadWriteData_GlobalTime_PrimitiveType**
57. **Dcm_DataElement_Example_ReadWriteData_GlobalTimeType**
58. **Dcm_DataElement_DID_0x0019_DID_Sint16_Array_ArrayType**
59. **Dcm_DataElement_DID_0x0019_DID_Sint16_ArrayType**
60. **Dcm_DataElement_DID_0x0017_DID_Sint32_Array_ArrayType**
61. **Dcm_DataElement_DID_0x0017_DID_Sint32_ArrayType**
62. **Dcm_DataElement_DID_0x0018_DID_Uint32_Array_ArrayType**
63. **Dcm_DataElement_DID_0x0018_DID_Uint32_ArrayType**
64. **Dcm_DataElement_SampleIoControl_DID_Data_PrimitiveType**
65. **Dcm_DataElement_SampleIoControl_DID_DataType**
66. **Dcm_DataElement_Example_WriteOnlyDID_DID_DataObject_PrimitiveType**
67. **Dcm_DataElement_Example_WriteOnlyDID_DID_DataObjectType**
68. **Dcm_DataElement_DataDiagnosticIdentifier_DID_DataDiagnosticIdentifier_PrimitiveType**
69. **Dcm_DataElement_DataDiagnosticIdentifier_DID_DataDiagnosticIdentifierType**
70. **Dcm_RequestDataArrayType**

### 4. DataConstrs

- **UUID**: `035fa1ac-29a2-454e-bcc1-e6079135061d`
- **包名称**: `DataConstrs`
- **包含元素数量**: 11

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **Dcm_ConfirmationStatusType_Constr**
2. **Dcm_OpStatusType_Constr**
3. **Dcm_NegativeResponseCodeType_Constr**
4. **Dcm_ProtocolType_Constr**
5. **Dcm_RequestKindType_Constr**
6. **Dcm_SecLevelType_Constr**
7. **Dcm_SesCtrlType_Constr**
8. **Dcm_ControlDtcSettingType_Constr**
9. **Dcm_EcuResetType_Constr**
10. **Dcm_DiagnosticSessionControlType_Constr**
11. **Dcm_CommunicationModeType_Constr**

### 5. CompuMethods

- **UUID**: `8439773d-da64-453b-9864-1b71de59a4a1`
- **包名称**: `CompuMethods`
- **包含元素数量**: 11

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Dcm_ConfirmationStatusType**
2. **Dcm_OpStatusType**
3. **Dcm_NegativeResponseCodeType**
4. **Dcm_ProtocolType**
5. **Dcm_RequestKindType**
6. **Dcm_SecLevelType**
7. **Dcm_SesCtrlType**
8. **Dcm_ControlDtcSettingType**
9. **Dcm_EcuResetType**
10. **Dcm_DiagnosticSessionControlType**
11. **Dcm_CommunicationModeType**

### 6. Interfaces

- **UUID**: `01371434-ec97-4ff8-8064-dc1c6a698d17`
- **包名称**: `Interfaces`
- **包含元素数量**: 36

#### 包含的元素

##### MODE-SWITCH-INTERFACE 类型元素

1. **DcmControlDtcSetting**
2. **DcmEcuReset**
3. **DcmDiagnosticSessionControl**
4. **DcmCommunicationControl_ComMConf_ComMChannel_CN_MyECU_CanCluster_eb1193db**
5. **DcmCommunicationControl_ComMConf_ComMChannel_CN_MyECU_EthernetCluster_74fadd9e**

##### CLIENT-SERVER-INTERFACE 类型元素

1. **DCMServices**
2. **SecurityAccess_UnlockedL1**
3. **SecurityAccess_Level_3**
4. **RoutineServices_SampleRoutineControl**
5. **RoutineServices_SampleRoutineControl_StartOnly**
6. **DataServices_DevelopmentData_TransportLayerVersion**
7. **DataServices_DevelopmentData_CanDriverVersion**
8. **DataServices_DevelopmentData_DiagnosticModuleVersion**
9. **DataServices_DevelopmentData_NmVersion**
10. **DataServices_DevelopmentData_OperatingSystemVersion**
11. **DataServices_Boot_Software_NumberOfModules**
12. **DataServices_Boot_Software_Boot_Software_Identification**
13. **DataServices_DID_0x001A_DID_Uint16_Array**
14. **DataServices_DID_0x001B_DID_Sint8_Array**
15. **DataServices_Vehicle_Identification_VIN**
16. **DataServices_Hardware_Version_Hardware_Version_Number**
17. **DataServices_DID_0xF412_DID_Data**
18. **DataServices_DID_0xF413_DID_Data**
19. **DataServices_DID_0xF410_DID_Data**
20. **DataServices_EcuIdentification_Part_Number**
21. **DataServices_SerialNumber_SerialNumber**
22. **DataServices_Example_ReadWriteData_GlobalTime**
23. **DataServices_DID_0x0019_DID_Sint16_Array**
24. **DataServices_DID_0x0017_DID_Sint32_Array**
25. **DataServices_DID_0x0018_DID_Uint32_Array**
26. **DataServices_SampleIoControl_DID_Data**
27. **DataServices_Spare_Part_Number_Spare_Part_Number**
28. **DataServices_Example_ReadOnlyDID_DID_Data_GlobalTime**
29. **DataServices_Example_WriteOnlyDID_DID_DataObject**
30. **DataServices_DataDiagnosticIdentifier_DID_DataDiagnosticIdentifier**
31. **DataServices_Data_DID_StartApplication**

### 7. ComponentTypes

- **UUID**: `7896792f-f9f3-4b33-ba24-e9569ef49b87`
- **包名称**: `ComponentTypes`
- **包含元素数量**: 2

#### 包含的元素

##### SERVICE-SW-COMPONENT-TYPE 类型元素

1. **Dcm**

##### SWC-IMPLEMENTATION 类型元素

1. **DcmImplementation**
