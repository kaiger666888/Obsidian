# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:22

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00046.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **67** 个包：

### 1. AUTOSAR_Platform

- **包名称**: `AUTOSAR_Platform`
- **包含元素数量**: 0

### 2. BaseTypes

- **包名称**: `BaseTypes`
- **包含元素数量**: 7

#### 包含的元素

##### SW-BASE-TYPE 类型元素

1. **boolean**
2. **dtRef_const_VOID**
3. **dtRef_VOID**
4. **sint8**
5. **uint16**
6. **uint32**
7. **uint8**

### 3. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 1

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **boolean_CompuMethod**

### 4. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 5

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **boolean_DataConstr**
2. **sint8_DataConstr**
3. **uint16_DataConstr**
4. **uint32_DataConstr**
5. **uint8_DataConstr**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 7

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **boolean**
2. **dtRef_const_VOID**
3. **dtRef_VOID**
4. **sint8**
5. **uint16**
6. **uint32**
7. **uint8**

### 6. MICROSAR_Static_ServicePortInterfaces

- **包名称**: `MICROSAR_Static_ServicePortInterfaces`
- **包含元素数量**: 0

### 7. ComM_swc

- **包名称**: `ComM_swc`
- **包含元素数量**: 1

#### 包含的元素

##### MODE-DECLARATION-GROUP 类型元素

1. **ComMMode**

### 8. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 2

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **ComM_InhibitionStatusType**
2. **ComM_ModeType**

### 9. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 1

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **ComM_ModeType**

### 10. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 2

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **ComM_InhibitionStatusType_Constr**
2. **ComM_ModeType_Constr**

### 11. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 5

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **ComM_ChannelLimitation**
2. **ComM_ChannelWakeUp**
3. **ComM_ECUModeLimitation**
4. **ComM_UserRequest**

##### MODE-SWITCH-INTERFACE 类型元素

1. **ComM_CurrentMode**

### 12. Csm_swc

- **包名称**: `Csm_swc`
- **包含元素数量**: 0

### 13. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 6

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Crypto_VerifyResultType**
2. **Csm_MacGenerateDataType_CsmPrimitivesMACGenerate**
3. **Csm_MacGenerateResultType_CsmPrimitivesMACGenerate**
4. **Csm_MacVerifyCompareType_CsmPrimitivesMACVerify**
5. **Csm_MacVerifyDataType_CsmPrimitivesMACVerify**
6. **Csm_ResultType**

### 14. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 2

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Crypto_VerifyResultType**
2. **Csm_ResultType**

### 15. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 2

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **Crypto_VerifyResultType_Constr**
2. **Csm_ResultType_Constr**

### 16. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 3

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **CallbackNotification**
2. **CsmMacGenerate_CsmPrimitivesMACGenerate**
3. **CsmMacVerify_CsmPrimitivesMACVerify**

### 17. Dcm_swc

- **包名称**: `Dcm_swc`
- **包含元素数量**: 3

#### 包含的元素

##### MODE-DECLARATION-GROUP 类型元素

1. **DcmControlDtcSetting**
2. **DcmDiagnosticSessionControl**
3. **DcmEcuReset**

### 18. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 10

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Dcm_ConfirmationStatusType**
2. **Dcm_Data2ByteType**
3. **Dcm_Data4ByteType**
4. **Dcm_Data650ByteType**
5. **Dcm_NegativeResponseCodeType**
6. **Dcm_OpStatusType**
7. **Dcm_ProtocolType**
8. **Dcm_RequestKindType**
9. **Dcm_SecLevelType**
10. **Dcm_SesCtrlType**

### 19. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 7

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Dcm_ConfirmationStatusType**
2. **Dcm_NegativeResponseCodeType**
3. **Dcm_OpStatusType**
4. **Dcm_ProtocolType**
5. **Dcm_RequestKindType**
6. **Dcm_SecLevelType**
7. **Dcm_SesCtrlType**

### 20. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 7

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **Dcm_ConfirmationStatusType_Constr**
2. **Dcm_NegativeResponseCodeType_Constr**
3. **Dcm_OpStatusType_Constr**
4. **Dcm_ProtocolType_Constr**
5. **Dcm_RequestKindType_Constr**
6. **Dcm_SecLevelType_Constr**
7. **Dcm_SesCtrlType_Constr**

### 21. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 7

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **DCMServices**
2. **SecurityAccess_Level_3**
3. **SecurityAccess_UnlockedL1**
4. **ServiceRequestNotification**

##### MODE-SWITCH-INTERFACE 类型元素

1. **DcmControlDtcSetting**
2. **DcmDiagnosticSessionControl**
3. **DcmEcuReset**

### 22. Dem_swc

- **包名称**: `Dem_swc`
- **包含元素数量**: 0

### 23. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 12

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Dem_DebounceResetStatusType**
2. **Dem_DebouncingStateType**
3. **Dem_DTCFormatType**
4. **Dem_DTCOriginType**
5. **Dem_EventIdType**
6. **Dem_EventStatusType**
7. **Dem_IndicatorStatusType**
8. **Dem_InitMonitorReasonType**
9. **Dem_MaxDataValueType**
10. **Dem_MonitorStatusType**
11. **Dem_OperationCycleStateType**
12. **Dem_UdsStatusByteType**

### 24. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 10

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Dem_DebounceResetStatusType**
2. **Dem_DebouncingStateType**
3. **Dem_DTCFormatType**
4. **Dem_DTCOriginType**
5. **Dem_EventStatusType**
6. **Dem_IndicatorStatusType**
7. **Dem_InitMonitorReasonType**
8. **Dem_MonitorStatusType**
9. **Dem_OperationCycleStateType**
10. **Dem_UdsStatusByteType**

### 25. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 11

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **Dem_DebounceResetStatusType_Constr**
2. **Dem_DebouncingStateType_Constr**
3. **Dem_DTCFormatType_Constr**
4. **Dem_DTCOriginType_Constr**
5. **Dem_EventIdType_Constr**
6. **Dem_EventStatusType_Constr**
7. **Dem_IndicatorStatusType_Constr**
8. **Dem_InitMonitorReasonType_Constr**
9. **Dem_MonitorStatusType_Constr**
10. **Dem_OperationCycleStateType_Constr**
11. **Dem_UdsStatusByteType_Constr**

### 26. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 10

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **CallbackInitMonitorForEvent**
2. **ClearDTC**
3. **DemServices**
4. **DiagnosticInfo**
5. **DiagnosticMonitor**
6. **EventAvailable**
7. **EvMemOverflowIndication**
8. **GeneralDiagnosticInfo**
9. **IndicatorStatus**
10. **OperationCycle**

### 27. Det_swc

- **包名称**: `Det_swc`
- **包含元素数量**: 0

### 28. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 2

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **DETService**
2. **DETServiceLegacy**

### 29. Dlt_swc

- **包名称**: `Dlt_swc`
- **包含元素数量**: 0

### 30. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 16

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Dlt_ApplicationIdInfoType**
2. **Dlt_ApplicationIDType**
3. **Dlt_AssignmentOperation**
4. **Dlt_ContextIdInfoType**
5. **Dlt_ContextIDType**
6. **Dlt_DataType**
7. **Dlt_GlobalStateType**
8. **Dlt_LogChannelNameType**
9. **Dlt_LogInfoPtrType**
10. **Dlt_LogInfoType**
11. **Dlt_MessageLogInfoType**
12. **Dlt_MessageLogLevelType**
13. **Dlt_MessageOptionsType**
14. **Dlt_MessageTraceInfoType**
15. **Dlt_MessageTraceType**
16. **Dlt_Uint8BufferType**

### 31. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 4

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Dlt_AssignmentOperation**
2. **Dlt_GlobalStateType**
3. **Dlt_MessageLogLevelType**
4. **Dlt_MessageTraceType**

### 32. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 6

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **argCount_Constr**
2. **Dlt_AssignmentOperation_Constr**
3. **Dlt_GlobalStateType_Constr**
4. **Dlt_MessageLogLevelType_Constr**
5. **Dlt_MessageOptionsType_Constr**
6. **Dlt_MessageTraceType_Constr**

### 33. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 6

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **DltControlService**
2. **DltInjection**
3. **DLTStateHandling**
4. **DltSwcMessageService**
5. **InjectionCallback**
6. **LogTraceSessionControl**

### 34. EcuM_swc

- **包名称**: `EcuM_swc`
- **包含元素数量**: 0

### 35. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 4

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **EcuM_BootTargetType**
2. **EcuM_ModeType**
3. **EcuM_ShutdownCauseType**
4. **EcuM_StateType**

### 36. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 4

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **EcuM_BootTargetType**
2. **EcuM_ModeType**
3. **EcuM_ShutdownCauseType**
4. **EcuM_StateType**

### 37. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 4

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **EcuM_BootTargetType_Constr**
2. **EcuM_ModeType_Constr**
3. **EcuM_ShutdownCauseType_Constr**
4. **EcuM_StateType_Constr**

### 38. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 2

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **EcuM_BootTarget**
2. **EcuM_ShutdownTarget**

### 39. FiM_swc

- **包名称**: `FiM_swc`
- **包含元素数量**: 0

### 40. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 1

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **FunctionInhibition**

### 41. IdsM_swc

- **包名称**: `IdsM_swc`
- **包含元素数量**: 0

### 42. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 1

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **IdsM_SWC_IdsMEventConfig_ContextDataType**

### 43. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 1

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **IdsMService_SWC_IdsMEventConfig**

### 44. J1939Rm_swc

- **包名称**: `J1939Rm_swc`
- **包含元素数量**: 0

### 45. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 4

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **J1939Rm_AckCode**
2. **J1939Rm_ExtIdInfoType**
3. **J1939Rm_ExtIdType**
4. **NetworkHandleType**

### 46. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 2

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **J1939Rm_AckCode**
2. **J1939Rm_ExtIdType**

### 47. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 3

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **J1939Rm_AckCode_Constr**
2. **J1939Rm_ExtIdType_Constr**
3. **NetworkHandleType_Constr**

### 48. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 6

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **AppAckIndication**
2. **AppCancelRequestTimeout**
3. **AppRequestIndication**
4. **AppRequestTimeoutIndication**
5. **AppSendAck**
6. **AppSendRequest**

### 49. KeyM_swc

- **包名称**: `KeyM_swc`
- **包含元素数量**: 0

### 50. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 3

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **KeyM_CertificateStatusType**
2. **KeyM_const_CryptoKeyDataType**
3. **KeyM_ResultType**

### 51. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 2

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **KeyM_CertificateStatusType**
2. **KeyM_ResultType**

### 52. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 2

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **KeyM_CertificateStatusType_Constr**
2. **KeyM_ResultType_Constr**

### 53. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 1

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **KeyMCertificateNotification**

### 54. SecOC_swc

- **包名称**: `SecOC_swc`
- **包含元素数量**: 0

### 55. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 2

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **SecOC_VerificationResultType**
2. **SecOC_VerificationStatusType**

### 56. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 1

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **SecOC_VerificationResultType**

### 57. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 3

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **freshnessValueID_Constr**
2. **SecOC_VerificationResultType_Constr**
3. **secOCDataId_Constr**

### 58. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 2

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **SecOC_VerifyStatusConfiguration**

##### SENDER-RECEIVER-INTERFACE 类型元素

1. **SecOC_VerificationStatusService**

### 59. WdgM_swc

- **包名称**: `WdgM_swc`
- **包含元素数量**: 0

### 60. DataTypes

- **包名称**: `DataTypes`
- **包含元素数量**: 5

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **WdgM_CheckpointIdType**
2. **WdgM_GlobalStatusType**
3. **WdgM_LocalStatusType**
4. **WdgM_ModeType**
5. **WdgM_SupervisedEntityIdType**

### 61. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 2

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **WdgM_GlobalStatusType**
2. **WdgM_LocalStatusType**

### 62. DataConstrs

- **包名称**: `DataConstrs`
- **包含元素数量**: 5

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **WdgM_CheckpointIdType_Constr**
2. **WdgM_GlobalStatusType_Constr**
3. **WdgM_LocalStatusType_Constr**
4. **WdgM_ModeType_Constr**
5. **WdgM_SupervisedEntityIdType_Constr**

### 63. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 3

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **WdgM_AliveSupervision**
2. **WdgM_General**
3. **WdgM_LocalStatus**

### 64. NvM_swc

- **包名称**: `NvM_swc`
- **包含元素数量**: 0

### 65. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 2

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **NvM_RequestResultType**
2. **NvM_ServiceIdType**

### 66. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 2

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **NvM_RequestResultType**
2. **NvM_ServiceIdType**

### 67. Interfaces

- **包名称**: `Interfaces`
- **包含元素数量**: 21

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **NvMAdministration**
2. **NvMNotifyInitBlock**
3. **NvMNotifyJobFinished**
4. **NvMService**
5. **NvMService_AC2**
6. **NvMService_AC2_Defs**
7. **NvMService_AC2_DS**
8. **NvMService_AC2_DS_Defs**
9. **NvMService_AC2_SRBS**
10. **NvMService_AC2_SRBS_Defs**
11. **NvMService_AC2_SRBS_DS**
12. **NvMService_AC2_SRBS_DS_Defs**
13. **NvMService_AC3**
14. **NvMService_AC3_Defs**
15. **NvMService_AC3_DS**
16. **NvMService_AC3_DS_Defs**
17. **NvMService_AC3_SRBS**
18. **NvMService_AC3_SRBS_Defs**
19. **NvMService_AC3_SRBS_DS**
20. **NvMService_AC3_SRBS_DS_Defs**
21. **NvMService_SRBS**
