# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:49:01

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

### 1. AUTOSAR_Mcu

- **包名称**: `AUTOSAR_Mcu`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Mcu**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 65

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Mcu_Init**
2. **Mcu_InitClock**
3. **Mcu_InitRamSection**
4. **Mcu_SetMode**
5. **Mcu_DistributePllClock**
6. **Mcu_GetPllStatus**
7. **Mcu_GetResetRawValue**
8. **Mcu_GetResetReason**
9. **Mcu_17_Gtm_TomChannelInit**
10. **Mcu_17_Gtm_TomChannelShadowTransfer**
11. **Mcu_17_Gtm_TomChannelDeInit**
12. **Mcu_17_Gtm_TomChannelDisable**
13. **Mcu_17_Gtm_TomChannelEnable**
14. **Mcu_17_Gtm_IsTomChannelEnabled**
15. **Mcu_17_Gtm_IsAtomChannelEnabled**
16. **Mcu_17_Gtm_IsTimChannelEnabled**
17. **Mcu_17_Gtm_AtomChannelInit**
18. **Mcu_17_Gtm_AtomChannelShadowTransfer**
19. **Mcu_17_Gtm_AtomChannelDeInit**
20. **Mcu_17_Gtm_AtomChannelEnable**
21. **Mcu_17_Gtm_AtomChannelDisable**
22. **Mcu_17_Gtm_TimChannelInit**
23. **Mcu_17_Gtm_TimChannelDeInit**
24. **Mcu_17_Gtm_TimChannelEnable**
25. **Mcu_17_Gtm_TimChannelDisable**
26. **Mcu_17_Gtm_TimChannelIsr**
27. **Mcu_17_Gtm_TomChannelIsr**
28. **Mcu_17_Gtm_AtomChannelIsr**
29. **Mcu_17_Gtm_ConnectPortPinToTim**
30. **Mcu_17_Gtm_ConnectTimerOutToPortPin**
31. **Mcu_17_Gtm_TomChInitCheck**
32. **Mcu_17_Gtm_AtomChInitCheck**
33. **Mcu_17_Gtm_TimChInitCheck**
34. **Mcu_17_Gtm_AtomChEndisCtrlUpdate**
35. **Mcu_17_Gtm_AtomChEndisStatUpdate**
36. **Mcu_17_Gtm_TomChEndisStatUpdate**
37. **Mcu_17_Gtm_TomChEndisCtrlUpdate**
38. **Mcu_17_Gtm_AtomChOutEnStatUpdate**
39. **Mcu_17_Gtm_TomChOutEnStatUpdate**
40. **Mcu_17_Gtm_TomChOutEnCtrlUpdate**
41. **Mcu_17_Gtm_TomChUpdateEnDis**
42. **Mcu_17_Gtm_AtomChUpdateEnDis**
43. **Mcu_17_Gtm_AtomChOutEnCtrlUpdate**
44. **Mcu_17_Gtm_AtomTriggerRequest**
45. **Mcu_17_Gtm_TomTriggerRequest**
46. **Mcu_17_Ccu6_TimerInit**
47. **Mcu_17_Ccu6_TimerDeInit**
48. **Mcu_17_Ccu6_TimerStart**
49. **Mcu_17_Ccu6_TimerStop**
50. **Mcu_17_Ccu6_TimerShadowTransfer**
51. **Mcu_17_Ccu6_TimerIntEnDis**
52. **Mcu_17_Ccu6_ChannelIsr**
53. **Mcu_17_Gpt12_TimerInit**
54. **Mcu_17_Gpt12_TimerDeInit**
55. **Mcu_17_Gpt12_TimerStart**
56. **Mcu_17_Gpt12_TimerStop**
57. **Mcu_17_Gpt12_TimerClockInit**
58. **Mcu_17_Gpt12_ChannelIsr**
59. **Mcu_17_Ccu6_TimerInitCheck**
60. **Mcu_17_Gpt12_TimerInitCheck**
61. **Mcu_17_Stm_ComparatorIntDisable**
62. **Mcu_17_Stm_SetupComparator**
63. **Mcu_17_Stm_CheckComparator**
64. **Mcu_17_Eru_GatingIsr**
65. **Mcu_17_Stm_CompareMatchIsr**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 2

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Mcu**
2. **Mcu_17_TimerIp**

### 5. ImplementationDataTypes

- **包名称**: `ImplementationDataTypes`
- **包含元素数量**: 49

#### 包含的元素

##### IMPLEMENTATION-DATA-TYPE 类型元素

1. **Mcu_17_Ccu6_TimerChIntType**
2. **Mcu_17_Eru_SrcIdentifierType**
3. **Mcu_17_Gpt12_ClkPrescalarType**
4. **Mcu_17_Gpt12_TimerBlockType**
5. **Mcu_17_Gtm_MappedPortTimerOutType**
6. **Mcu_17_Gtm_TimerEnableType**
7. **Mcu_17_Gtm_TimerEnTriggerType**
8. **Mcu_17_Gtm_TimerOutputEnableType**
9. **Mcu_17_Gtm_TimerOutputEnTriggerType**
10. **Mcu_17_Gtm_TimerUpdateEnableType**
11. **Mcu_17_Stm_StmCmpIdentifierType**
12. **Mcu_17_Stm_StmIdentifierType**
13. **Mcu_17_Stm_TimerConfigType**
14. **Mcu_PllStatusType**
15. **Mcu_ClockType**
16. **Mcu_ResetType**
17. **Mcu_RawResetType**
18. **Mcu_RamSectionType**
19. **Mcu_ModeType**
20. **Mcu_17_Gtm_TimChConfigType**
21. **Mcu_17_Gtm_TimerChIdentifierType**
22. **Mcu_17_Gtm_TimerOutType**
23. **Mcu_17_Gtm_TomAtomChConfigType**
24. **Mcu_17_Gtm_TimerStatusType**
25. **Mcu_17_Ccu6_ComparatorType**
26. **Mcu_17_Ccu6_KernelIdentifierType**
27. **Mcu_17_Ccu6_TimerChIdentifierType**
28. **Mcu_17_Ccu6_TimerConfigType**
29. **Mcu_17_Gpt12_TimerChIdentifierType**
30. **Mcu_17_Gpt12_TimerConfigType**
31. **Mcu_ClockConfigType**
32. **Mcu_ConfigType**
33. **Mcu_ExternalClockConfigType**
34. **Mcu_GtmAdcTrigType**
35. **Mcu_GtmAtomConfigType**
36. **Mcu_GtmClockSettingType**
37. **Mcu_GtmClusterConfigType**
38. **Mcu_GtmConfigType**
39. **Mcu_GtmExtClkType**
40. **Mcu_GtmTomConfigType**
41. **Mcu_LowPowerModeType**
42. **Mcu_ModeEvrcCtrlType**
43. **Mcu_PeripheralPllConfigType**
44. **Mcu_PllDistributionConfigType**
45. **Mcu_RamBaseAdrType**
46. **Mcu_RamConfigType**
47. **Mcu_RamPrstDatType**
48. **Mcu_RamSizeType**
49. **Mcu_SystemPllConfigType**

### 6. CompuMethods

- **包名称**: `CompuMethods`
- **包含元素数量**: 8

#### 包含的元素

##### COMPU-METHOD 类型元素

1. **Mcu_17_Gtm_MappedPortTimerOutType**
2. **Mcu_17_Gtm_TimerEnTriggerType**
3. **Mcu_17_Gtm_TimerOutputEnableType**
4. **Mcu_17_Gtm_TimerOutputEnTriggerType**
5. **Mcu_PllStatusType**
6. **Mcu_ResetType**
7. **Mcu_17_Gtm_TimerOutType**
8. **Mcu_17_Gtm_TimerStatusType**

## ⚡ 实现信息

此ARXML文件包含 **2** 个实现：

### 1. Mcu

- **实现名称**: `Mcu`
- **编程语言**: C
- **软件版本**: 10.40.2
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2

### 2. Mcu_17_TimerIp

- **实现名称**: `Mcu_17_TimerIp`
- **编程语言**: C
- **软件版本**: 4.0.0
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
