# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:22

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
- **包含元素数量**: 81

#### 包含的元素

##### BSW-MODULE-ENTRY 类型元素

1. **Bfx_SetBit_u8u8**
2. **Bfx_SetBit_u16u8**
3. **Bfx_SetBit_u32u8**
4. **Bfx_SetBit_u64u8**
5. **Bfx_ClrBit_u8u8**
6. **Bfx_ClrBit_u16u8**
7. **Bfx_ClrBit_u32u8**
8. **Bfx_ClrBit_u64u8**
9. **Bfx_GetBit_u8u8_u8**
10. **Bfx_GetBit_u16u8_u8**
11. **Bfx_GetBit_u32u8_u8**
12. **Bfx_GetBit_u64u8_u8**
13. **Bfx_SetBits_u8u8u8u8**
14. **Bfx_SetBits_u16u8u8u8**
15. **Bfx_SetBits_u32u8u8u8**
16. **Bfx_SetBits_u64u8u8u8**
17. **Bfx_GetBits_u8u8u8_u8**
18. **Bfx_GetBits_u16u8u8_u16**
19. **Bfx_GetBits_u32u8u8_u32**
20. **Bfx_GetBits_u64u8u8_u64**
21. **Bfx_SetBitMask_u8u8**
22. **Bfx_SetBitMask_u16u16**
23. **Bfx_SetBitMask_u32u32**
24. **Bfx_SetBitMask_u64u64**
25. **Bfx_ClrBitMask_u8u8**
26. **Bfx_ClrBitMask_u16u16**
27. **Bfx_ClrBitMask_u32u32**
28. **Bfx_ClrBitMask_u64u64**
29. **Bfx_TstBitMask_u8u8_u8**
30. **Bfx_TstBitMask_u16u16_u8**
31. **Bfx_TstBitMask_u32u32_u8**
32. **Bfx_TstBitMask_u64u64_u8**
33. **Bfx_TstBitLnMask_u8u8_u8**
34. **Bfx_TstBitLnMask_u16u16_u8**
35. **Bfx_TstBitLnMask_u32u32_u8**
36. **Bfx_TstBitLnMask_u64u64_u8**
37. **Bfx_TstParityEven_u8_u8**
38. **Bfx_TstParityEven_u16_u8**
39. **Bfx_TstParityEven_u32_u8**
40. **Bfx_TstParityEven_u64_u8**
41. **Bfx_ToggleBits_u8**
42. **Bfx_ToggleBits_u16**
43. **Bfx_ToggleBits_u32**
44. **Bfx_ToggleBits_u64**
45. **Bfx_ToggleBitMask_u8u8**
46. **Bfx_ToggleBitMask_u16u16**
47. **Bfx_ToggleBitMask_u32u32**
48. **Bfx_ToggleBitMask_u64u64**
49. **Bfx_ShiftBitRt_u8u8**
50. **Bfx_ShiftBitRt_u16u8**
51. **Bfx_ShiftBitRt_u32u8**
52. **Bfx_ShiftBitRt_u64u8**
53. **Bfx_ShiftBitLt_u8u8**
54. **Bfx_ShiftBitLt_u16u8**
55. **Bfx_ShiftBitLt_u32u8**
56. **Bfx_ShiftBitLt_u64u8**
57. **Bfx_RotBitRt_u8u8**
58. **Bfx_RotBitRt_u16u8**
59. **Bfx_RotBitRt_u32u8**
60. **Bfx_RotBitRt_u64u8**
61. **Bfx_RotBitLt_u8u8**
62. **Bfx_RotBitLt_u16u8**
63. **Bfx_RotBitLt_u32u8**
64. **Bfx_RotBitLt_u64u8**
65. **Bfx_CopyBit_u8u8u8u8**
66. **Bfx_CopyBit_u16u8u16u8**
67. **Bfx_CopyBit_u32u8u32u8**
68. **Bfx_CopyBit_u64u8u64u8**
69. **Bfx_PutBits_u8u8u8u8**
70. **Bfx_PutBits_u16u8u8u16**
71. **Bfx_PutBits_u32u8u8u32**
72. **Bfx_PutBits_u64u8u8u64**
73. **Bfx_PutBitsMask_u8u8u8**
74. **Bfx_PutBitsMask_u16u16u16**
75. **Bfx_PutBitsMask_u32u32u32**
76. **Bfx_PutBitsMask_u64u64u64**
77. **Bfx_PutBit_u8u8u8**
78. **Bfx_PutBit_u16u8u8**
79. **Bfx_PutBit_u32u8u8**
80. **Bfx_PutBit_u64u8u8**
81. **Bfx_GetVersionInfo**

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
- **软件版本**: 20.0.1
- **供应商ID**: 17
- **AUTOSAR版本**: 4.2.2
