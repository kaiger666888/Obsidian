# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:06

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **4** 个包：

### 1. AUTOSAR_Bfx

- **包名称**: `AUTOSAR_Bfx`
- **包含元素数量**: 0

### 2. BswModuleDescriptions

- **包名称**: `BswModuleDescriptions`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-MODULE-DESCRIPTION 类型元素

1. **Bfx**

### 3. BswModuleEntrys

- **包名称**: `BswModuleEntrys`
- **包含元素数量**: 61

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Bfx_SetBit_u8u8**
2. **Bfx_SetBit_u16u8**
3. **Bfx_SetBit_u32u8**
4. **Bfx_ClrBit_u8u8**
5. **Bfx_ClrBit_u16u8**
6. **Bfx_ClrBit_u32u8**
7. **Bfx_GetBit_u8u8_u8**
8. **Bfx_GetBit_u16u8_u8**
9. **Bfx_GetBit_u32u8_u8**
10. **Bfx_SetBits_u8u8u8u8**
11. **Bfx_SetBits_u16u8u8u8**
12. **Bfx_SetBits_u32u8u8u8**
13. **Bfx_GetBits_u8u8u8_u8**
14. **Bfx_GetBits_u16u8u8_u16**
15. **Bfx_GetBits_u32u8u8_u32**
16. **Bfx_SetBitMask_u8u8**
17. **Bfx_SetBitMask_u16u16**
18. **Bfx_SetBitMask_u32u32**
19. **Bfx_ClrBitMask_u8u8**
20. **Bfx_ClrBitMask_u16u16**
21. **Bfx_ClrBitMask_u32u32**
22. **Bfx_TstBitMask_u8u8_u8**
23. **Bfx_TstBitMask_u16u16_u8**
24. **Bfx_TstBitMask_u32u32_u8**
25. **Bfx_TstBitLnMask_u8u8_u8**
26. **Bfx_TstBitLnMask_u16u16_u8**
27. **Bfx_TstBitLnMask_u32u32_u8**
28. **Bfx_TstParityEven_u8_u8**
29. **Bfx_TstParityEven_u16_u8**
30. **Bfx_TstParityEven_u32_u8**
31. **Bfx_ToggleBits_u8**
32. **Bfx_ToggleBits_u16**
33. **Bfx_ToggleBits_u32**
34. **Bfx_ToggleBitMask_u8u8**
35. **Bfx_ToggleBitMask_u16u16**
36. **Bfx_ToggleBitMask_u32u32**
37. **Bfx_ShiftBitRt_u8u8**
38. **Bfx_ShiftBitRt_u16u8**
39. **Bfx_ShiftBitRt_u32u8**
40. **Bfx_ShiftBitLt_u8u8**
41. **Bfx_ShiftBitLt_u16u8**
42. **Bfx_ShiftBitLt_u32u8**
43. **Bfx_RotBitRt_u8u8**
44. **Bfx_RotBitRt_u16u8**
45. **Bfx_RotBitRt_u32u8**
46. **Bfx_RotBitLt_u8u8**
47. **Bfx_RotBitLt_u16u8**
48. **Bfx_RotBitLt_u32u8**
49. **Bfx_CopyBit_u8u8u8u8**
50. **Bfx_CopyBit_u16u8u16u8**
51. **Bfx_CopyBit_u32u8u32u8**
52. **Bfx_PutBits_u8u8u8u8**
53. **Bfx_PutBits_u16u8u8u16**
54. **Bfx_PutBits_u32u8u8u32**
55. **Bfx_PutBitsMask_u8u8u8**
56. **Bfx_PutBitsMask_u16u16u16**
57. **Bfx_PutBitsMask_u32u32u32**
58. **Bfx_PutBit_u8u8u8**
59. **Bfx_PutBit_u16u8u8**
60. **Bfx_PutBit_u32u8u8**
61. **Bfx_GetVersionInfo**

### 4. Implementations

- **包名称**: `Implementations`
- **包含元素数量**: 1

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Bfx**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Bfx

- **实现名称**: `Bfx`
- **编程语言**: C
- **软件版本**: 10.40.0
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
