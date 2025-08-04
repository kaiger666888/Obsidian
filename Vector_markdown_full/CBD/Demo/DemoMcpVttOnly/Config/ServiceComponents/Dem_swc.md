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

### 2. Dem_swc

- **UUID**: `f0672d94-503f-4a90-89ca-aaf7be620fde`
- **包名称**: `Dem_swc`
- **包含元素数量**: 0

### 3. DataTypes

- **UUID**: `edf295b0-d555-4a47-a5fd-6296c91ff67d`
- **包名称**: `DataTypes`
- **包含元素数量**: 27

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Dem_EventIdType**
2. **Dem_RatioIdType**
3. **Dem_DTCStatusMaskType**
4. **Dem_OperationCycleIdType**
5. **Dem_DTCGroupType**
6. **Dem_MaxDataValueType**
7. **Dem_EventStatusType**
8. **Dem_InitMonitorReasonType**
9. **Dem_OperationCycleStateType**
10. **Dem_IndicatorStatusType**
11. **Dem_DTCKindType**
12. **Dem_IumprDenomCondIdType**
13. **Dem_IumprDenomCondStatusType**
14. **Dem_DebounceResetStatusType**
15. **Dem_IumprReadinessGroupType**
16. **Dem_DTRControlType**
17. **Dem_DebouncingStateType**
18. **Dem_DTCSeverityType**
19. **Dem_UdsStatusByteType**
20. **Dem_MonitorStatusType**
21. **DataPrimitiveType_uint16**
22. **DataArrayType_uint8_6**
23. **DataArrayType_uint8_2**
24. **Dem_DTCOriginType**
25. **Dem_DTCFormatType**
26. **Dem_BufferLengthType**
27. **Dcm_NegativeResponseCodeType**

### 4. DataConstrs

- **UUID**: `7a430e40-af48-4ac6-a7d1-b1166cb32a6f`
- **包名称**: `DataConstrs`
- **包含元素数量**: 23

#### 包含的元素

##### DATA-CONSTR 类型元素

1. **Dem_EventIdType_Constr**
2. **Dem_RatioIdType_Constr**
3. **Dem_DTCStatusMaskType_Constr**
4. **Dem_OperationCycleIdType_Constr**
5. **Dem_DTCGroupType_Constr**
6. **Dem_EventStatusType_Constr**
7. **Dem_InitMonitorReasonType_Constr**
8. **Dem_OperationCycleStateType_Constr**
9. **Dem_IndicatorStatusType_Constr**
10. **Dem_DTCKindType_Constr**
11. **Dem_IumprDenomCondIdType_Constr**
12. **Dem_IumprDenomCondStatusType_Constr**
13. **Dem_DebounceResetStatusType_Constr**
14. **Dem_IumprReadinessGroupType_Constr**
15. **Dem_DTRControlType_Constr**
16. **Dem_DebouncingStateType_Constr**
17. **Dem_DTCSeverityType_Constr**
18. **Dem_UdsStatusByteType_Constr**
19. **Dem_MonitorStatusType_Constr**
20. **Dem_DTCOriginType_Constr**
21. **Dem_DTCFormatType_Constr**
22. **Dem_BufferLengthType_Constr**
23. **Dcm_NegativeResponseCodeType_Constr**

### 5. CompuMethods

- **UUID**: `cb1e34db-dddc-4465-aa23-ccec664a2db5`
- **包名称**: `CompuMethods`
- **包含元素数量**: 16

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Dem_EventStatusType**
2. **Dem_InitMonitorReasonType**
3. **Dem_DTCOriginType**
4. **Dem_DTCFormatType**
5. **Dem_OperationCycleStateType**
6. **Dem_IndicatorStatusType**
7. **Dem_DTCKindType**
8. **Dem_IumprDenomCondIdType**
9. **Dem_IumprDenomCondStatusType**
10. **Dem_DebounceResetStatusType**
11. **Dem_IumprReadinessGroupType**
12. **Dem_DTRControlType**
13. **Dem_DebouncingStateType**
14. **Dem_DTCSeverityType**
15. **Dem_UdsStatusByteType**
16. **Dem_MonitorStatusType**

### 6. Interfaces

- **UUID**: `6d72957d-6593-470f-87d2-cd30a64c196c`
- **包名称**: `Interfaces`
- **包含元素数量**: 13

#### 包含的元素

##### CLIENT-SERVER-INTERFACE 类型元素

1. **DemServices**
2. **CallbackInitMonitorForEvent**
3. **ClearDTC**
4. **IndicatorStatus**
5. **EvMemOverflowIndication**
6. **GeneralDiagnosticInfo**
7. **OperationCycle**
8. **CSDataServices_PID_0x12_DID_Data**
9. **CSDataServices_DID_0x1_DID_Data_GlobalTime**
10. **CSDataServices_PID_0x13_DID_Data**
11. **CSDataServices_DemDataElementClass_StartApplication**
12. **DiagnosticInfo**
13. **DiagnosticMonitor**

### 7. ComponentTypes

- **UUID**: `d67d9d69-ebeb-4962-ae3f-4058bad931c7`
- **包名称**: `ComponentTypes`
- **包含元素数量**: 4

#### 包含的元素

##### SERVICE-SW-COMPONENT-TYPE 类型元素

1. **DemMaster_SystemApplication_OsCore0**
2. **DemSatellite_SystemApplication_OsCore0**

##### SWC-IMPLEMENTATION 类型元素

1. **DemMaster_SystemApplication_OsCore0Implementation**
2. **DemSatellite_SystemApplication_OsCore0Implementation**
