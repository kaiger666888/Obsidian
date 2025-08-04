# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:10

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **6** 个包：

### 1. AURIX2G_Hssl

- **包名称**: `AURIX2G_Hssl`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Hssl**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 27

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Hssl_SetMode**
2. **Hssl_DmaCallout**
3. **Hssl_DmaErrCallout**
4. **Hssl_SelectSlave**
5. **Hssl_ActivateSlave**
6. **Hssl_DeactivateSlave**
7. **Hssl_IsrCOK**
8. **Hssl_IsrError**
9. **Hssl_IsrTrg**
10. **Hssl_IsrEXI**
11. **Hssl_IsrRDI**
12. **Hssl_Init**
13. **Hssl_Reset**
14. **Hssl_InitChannel**
15. **Hssl_Write**
16. **Hssl_WriteAck**
17. **Hssl_Read**
18. **Hssl_ReadRply**
19. **Hssl_Id**
20. **Hssl_Trigger**
21. **Hssl_StartStream**
22. **Hssl_StopStream**
23. **Hssl_MultiWrite**
24. **Hssl_MultiRead**
25. **Hssl_GetGlobalError**
26. **Hssl_GetChannelError**
27. **Hssl_GetVersionInfo**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Hssl**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 8

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Hssl_ConfigType**
2. **Hssl_UserNotify**
3. **Hssl_InstanceID**
4. **Hssl_SlaveStatusType**
5. **Hssl_ChannelErrorType**
6. **Hssl_ChannelType**
7. **Hssl_DataTemplateType**
8. **Hssl_ReadDataTemplateType**

### 6. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 4

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Hssl_InstanceID**
2. **Hssl_SlaveStatusType**
3. **Hssl_ChannelErrorType**
4. **Hssl_EventType**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Hssl

- **实现名称**: `Hssl`
- **编程语言**: C
- **软件版本**: 10.40.1
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
