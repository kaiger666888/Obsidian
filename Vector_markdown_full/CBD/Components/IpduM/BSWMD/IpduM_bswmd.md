# IpduM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:02

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [IpduM](#ipdum)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. IpduM

#### 基本信息

- **UUID**: `f746bf70-c327-48ee-8d0c-ce3acd22eec1`
- **模块名称**: `IpduM`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-POST-BUILD-LOADABLE
  - VARIANT-POST-BUILD-SELECTABLE

#### 模块描述

The I-PDU Multiplexer realizes two distinct functionalities:
(1) PDU multiplexing. One PDU on the bus can have different, static data layouts, defined by a selector value. The multiplexed PDU usually is of similar size for all layouts.
(2) Container handling. Multiple PDUs are combined in one container in static or dynamic order, transmitted as one large PDU, and then unpacked into separate PDUs at the receiver again. The containers are usually much larger than the individual PDUs.

#### 版本历史

共有 **79** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2011-11-30
- **发布者**: visms

**变更内容**:

##### 2. 版本 1.00.01

- **状态**: released
- **发布日期**: 2012-03-28
- **发布者**: visms

**变更内容**:

##### 3. 版本 1.00.02

- **状态**: released
- **发布日期**: 2012-04-11
- **发布者**: visms

**变更内容**:

##### 4. 版本 2.00.00

- **状态**: released
- **发布日期**: 2011-11-09
- **发布者**: visms

**变更内容**:

##### 5. 版本 2.00.01

- **状态**: released
- **发布日期**: 2012-09-25
- **发布者**: visbms

**变更内容**:

##### 6. 版本 2.00.02

- **状态**: released
- **发布日期**: 2012-11-06
- **发布者**: visms

**变更内容**:

##### 7. 版本 2.01.00

- **状态**: released
- **发布日期**: 2012-11-26
- **发布者**: visbms

**变更内容**:

##### 8. 版本 2.02.00

- **状态**: released
- **发布日期**: 2013-02-14
- **发布者**: visms

**变更内容**:

##### 9. 版本 2.03.00

- **状态**: released
- **发布日期**: 2013-07-09
- **发布者**: visms

**变更内容**:

##### 10. 版本 2.03.00

- **状态**: released
- **发布日期**: 2013-07-09
- **发布者**: visms

**变更内容**:

##### 11. 版本 2.03.00

- **状态**: released
- **发布日期**: 2013-07-09
- **发布者**: visms

**变更内容**:

##### 12. 版本 2.03.00

- **状态**: released
- **发布日期**: 2013-07-11
- **发布者**: visms

**变更内容**:

##### 13. 版本 2.03.00

- **状态**: released
- **发布日期**: 2013-10-21
- **发布者**: visbms

**变更内容**:

##### 14. 版本 2.03.01

- **状态**: released
- **发布日期**: 2013-12-18
- **发布者**: visbms

**变更内容**:

##### 15. 版本 2.03.02

- **状态**: released
- **发布日期**: 2014-05-07
- **发布者**: visbms

**变更内容**:

##### 16. 版本 2.03.03

- **状态**: released
- **发布日期**: 2014-05-09
- **发布者**: visbms

**变更内容**:

##### 17. 版本 3.00.00

- **状态**: released
- **发布日期**: 2014-05-14
- **发布者**: visms

**变更内容**:

##### 18. 版本 4.00.00

- **状态**: released
- **发布日期**: 2014-06-30
- **发布者**: visbms

**变更内容**:

##### 19. 版本 4.00.00

- **状态**: released
- **发布日期**: 2014-08-13
- **发布者**: visbms

**变更内容**:

##### 20. 版本 5.00.00

- **状态**: released
- **发布日期**: 2014-11-17
- **发布者**: visbms

**变更内容**:

##### 21. 版本 5.01.00

- **状态**: released
- **发布日期**: 2015-02-20
- **发布者**: visbms

**变更内容**:

##### 22. 版本 5.01.01

- **状态**: released
- **发布日期**: 2015-04-29
- **发布者**: visbms

**变更内容**:

##### 23. 版本 5.01.02

- **状态**: released
- **发布日期**: 2015-04-29
- **发布者**: visbms

**变更内容**:

##### 24. 版本 5.01.03

- **状态**: released
- **发布日期**: 2015-05-07
- **发布者**: visbms

**变更内容**:

##### 25. 版本 5.01.04

- **状态**: released
- **发布日期**: 2015-05-28
- **发布者**: visbms

**变更内容**:

##### 26. 版本 5.01.05

- **状态**: released
- **发布日期**: 2015-06-29
- **发布者**: visbms

**变更内容**:

##### 27. 版本 6.00.00

- **状态**: released
- **发布日期**: 2015-11-05
- **发布者**: visbms

**变更内容**:

##### 28. 版本 6.01.00

- **状态**: released
- **发布日期**: 2016-02-19
- **发布者**: visms

**变更内容**:

##### 29. 版本 6.01.01

- **状态**: released
- **发布日期**: 2016-02-19
- **发布者**: visbms

**变更内容**:

##### 30. 版本 6.01.02

- **状态**: released
- **发布日期**: 2016-04-28
- **发布者**: visbms

**变更内容**:

##### 31. 版本 6.01.03

- **状态**: released
- **发布日期**: 2016-05-09
- **发布者**: visbms

**变更内容**:

##### 32. 版本 6.01.04

- **状态**: released
- **发布日期**: 2016-06-15
- **发布者**: visbms

**变更内容**:

##### 33. 版本 6.02.00

- **状态**: released
- **发布日期**: 2016-06-21
- **发布者**: visbms

**变更内容**:

##### 34. 版本 6.04.00

- **状态**: released
- **发布日期**: 2016-11-08
- **发布者**: visbms

**变更内容**:

##### 35. 版本 6.04.01

- **状态**: released
- **发布日期**: 2016-12-02
- **发布者**: visbms

**变更内容**:

##### 36. 版本 6.05.00

- **状态**: released
- **发布日期**: 2017-01-11
- **发布者**: visms

**变更内容**:

##### 37. 版本 6.05.00

- **状态**: released
- **发布日期**: 2017-01-11
- **发布者**: visms

**变更内容**:

##### 38. 版本 6.05.01

- **状态**: released
- **发布日期**: 2017-05-17
- **发布者**: visms

**变更内容**:

##### 39. 版本 6.05.02

- **状态**: released
- **发布日期**: 2017-06-22
- **发布者**: visms

**变更内容**:

##### 40. 版本 6.06.00

- **状态**: released
- **发布日期**: 2017-07-20
- **发布者**: visms

**变更内容**:

##### 41. 版本 6.06.01

- **状态**: released
- **发布日期**: 2017-08-28
- **发布者**: visms

**变更内容**:

##### 42. 版本 6.06.02

- **状态**: released
- **发布日期**: 2017-09-18
- **发布者**: visms

**变更内容**:

##### 43. 版本 6.06.03

- **状态**: released
- **发布日期**: 2017-09-22
- **发布者**: visms

**变更内容**:

##### 44. 版本 6.06.04

- **状态**: released
- **发布日期**: 2017-09-22
- **发布者**: visms

**变更内容**:

##### 45. 版本 6.06.05

- **状态**: released
- **发布日期**: 2017-09-22
- **发布者**: visms

**变更内容**:

##### 46. 版本 6.07.00

- **状态**: released
- **发布日期**: 2017-12-19
- **发布者**: visms

**变更内容**:

##### 47. 版本 6.07.01

- **状态**: released
- **发布日期**: 2017-12-19
- **发布者**: visms

**变更内容**:

##### 48. 版本 6.08.00

- **状态**: released
- **发布日期**: 2018-02-16
- **发布者**: visms

**变更内容**:

##### 49. 版本 6.08.01

- **状态**: released
- **发布日期**: 2018-02-16
- **发布者**: visms

**变更内容**:

##### 50. 版本 7.00.00

- **状态**: released
- **发布日期**: 2018-03-14
- **发布者**: visms

**变更内容**:

##### 51. 版本 7.01.00

- **状态**: released
- **发布日期**: 2018-05-24
- **发布者**: visbms

**变更内容**:

##### 52. 版本 7.01.01

- **状态**: released
- **发布日期**: 2018-06-13
- **发布者**: visms

**变更内容**:

##### 53. 版本 7.01.02

- **状态**: released
- **发布日期**: 2018-10-24
- **发布者**: visbms

**变更内容**:

##### 54. 版本 7.01.03

- **状态**: released
- **发布日期**: 2018-11-21
- **发布者**: visbms

**变更内容**:

##### 55. 版本 7.02.00

- **状态**: released
- **发布日期**: 2018-12-18
- **发布者**: visbms

**变更内容**:

##### 56. 版本 7.02.01

- **状态**: released
- **发布日期**: 2019-01-08
- **发布者**: visbms

**变更内容**:

##### 57. 版本 7.03.00

- **状态**: released
- **发布日期**: 2019-03-14
- **发布者**: visbms

**变更内容**:

##### 58. 版本 7.04.00

- **状态**: released
- **发布日期**: 2019-04-01
- **发布者**: visbms

**变更内容**:

##### 59. 版本 7.04.01

- **状态**: released
- **发布日期**: 2019-04-05
- **发布者**: visbms

**变更内容**:

##### 60. 版本 7.04.02

- **状态**: released
- **发布日期**: 2019-04-17
- **发布者**: vismij

**变更内容**:

##### 61. 版本 8.00.00

- **状态**: released
- **发布日期**: 2019-05-24
- **发布者**: visbms

**变更内容**:

##### 62. 版本 8.00.01

- **状态**: released
- **发布日期**: 2019-11-21
- **发布者**: visbms

**变更内容**:

##### 63. 版本 9.00.00

- **状态**: released
- **发布日期**: 2020-01-21
- **发布者**: visssg

**变更内容**:

##### 64. 版本 9.01.00

- **状态**: released
- **发布日期**: 2020-06-18T14:14:45+02:00
- **发布者**: vismij

**变更内容**:

##### 65. 版本 9.01.01

- **状态**: released
- **发布日期**: 2020-11-13T09:55:00+01:00
- **发布者**: visbms

**变更内容**:

##### 66. 版本 10.00.00

- **状态**: released
- **发布日期**: 2020-11-24T09:55:00+01:00
- **发布者**: visbms

**变更内容**:

##### 67. 版本 10.00.01

- **状态**: released
- **发布日期**: 2021-02-02T09:55:00+01:00
- **发布者**: visbms

**变更内容**:

##### 68. 版本 10.00.02

- **状态**: released
- **发布日期**: 2021-02-16T09:55:00+01:00
- **发布者**: visbms

**变更内容**:

##### 69. 版本 11.00.00

- **状态**: released
- **发布日期**: 2021-03-25T09:55:00+01:00
- **发布者**: visbms

**变更内容**:

##### 70. 版本 

- **状态**: released
- **发布日期**: 2021-06-07T10:44:03+02:00
- **发布者**: visfrm

**变更内容**:

##### 71. 版本 11.01.00

- **状态**: released
- **发布日期**: 2021-06-11T13:56:27+02:00
- **发布者**: visfrm

**变更内容**:

##### 72. 版本 11.02.00

- **发布日期**: 2021-08-10T10:28:21+02:00
- **发布者**: visssg

**变更内容**:

##### 73. 版本 11.02.01

- **发布日期**: 2022-06-07T10:28:21+02:00
- **发布者**: visbms

**变更内容**:

##### 74. 版本 12.00.00

- **发布日期**: 2023-02-09T10:28:21+02:00
- **发布者**: visbms

**变更内容**:

##### 75. 版本 13.00.00

- **发布日期**: 2023-03-15T14:03:41+01:00
- **发布者**: visfrm

**变更内容**:

##### 76. 版本 

- **发布日期**: 2023-04-11T11:12:56+02:00
- **发布者**: visfrm

**变更内容**:

##### 77. 版本 13.01.00

- **发布日期**: 2024-01-11T11:22:00+01:00
- **发布者**: visbms

**变更内容**:

##### 78. 版本 13.02.00

- **发布日期**: 2024-03-18T11:33:49+01:00
- **发布者**: visms

**变更内容**:

##### 79. 版本 13.02.00

- **发布日期**: 2024-03-18T11:51:31+01:00
- **发布者**: visms

**变更内容**:

#### 配置容器

本模块包含 **22** 个配置容器：

##### 1. IpduMGeneral

**容器属性**:

- **UUID**: `b7b08915-9aba-4d18-8ec7-5e3fff574922`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Global configuration parameters of the IpduM.

###### 参数配置

此容器包含 **10** 个参数：

####### BOOLEAN 类型参数

######## 1. IpduMContainedTxPduPriorityHandling

- **UUID**: `ECUC:44ab461e-2693-4749-a288-b37a2a6aeab2`
- **参数名**: `IpduMContainedTxPduPriorityHandling`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter enables/disables handling of priority for IpduMContainedTxPdu's with IpduMContainedTxPduCollectionSemantics IPDUM_LAST_IS_BEST.

######## 2. IpduMDevErrorDetect

- **UUID**: `5eb0d57b-c2b7-47e6-b765-c3c478094c01`
- **参数名**: `IpduMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.
true: Development Error Detection is enabled.
false: Development Error Detection is disabled.

######## 3. IpduMStaticPartExists

- **UUID**: `66383b60-c486-46e9-b088-5c3e9fa95605`
- **参数名**: `IpduMStaticPartExists`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Allow optimizations in the case the IpduM will never be used with a static part.
Note that this is a pre-compile option. If it is de-activated, it will not be possible to configure static parts after compilation.
True: A static part may exist.
False: A static part will never exist.

######## 4. IpduMVersionInfoApi

- **UUID**: `52a9ad55-863e-433e-a05e-8e000b2b83c5`
- **参数名**: `IpduMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter enables/disables the function IpduM_GetVersionInfo() to get major, minor and patch version information.
True: version information activated.
False: version information de-activated.

######## 5. IpduMSafeBswChecks

- **UUID**: `994a3451-578d-46a0-bd39-6ac517918497`
- **参数名**: `IpduMSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed.
This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

####### FLOAT 类型参数

######## 1. IpduMConfigurationTimeBase

- **UUID**: `df0be8d5-866d-4508-9e97-ae59e38515eb`
- **参数名**: `IpduMConfigurationTimeBase`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The cycle time with which IpduM_MainFunction is invoked.
Note: This parameter is not used by the generator.

######## 2. IpduMRxTimeBase

- **UUID**: `33646c19-3cbf-475f-a548-aba1fbd475ff`
- **参数名**: `IpduMRxTimeBase`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0..3600]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The period between successive calls to IpduM_MainFunctionRx. This parameter is used by the IpduM generator to transform the values of the reception related timing configuration parameters of the IpduM module to internal implementation specific counter or tick values.

######## 3. IpduMTxTimeBase

- **UUID**: `b8d8b727-5681-432d-8356-b6ec2bcb84c5`
- **参数名**: `IpduMTxTimeBase`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0..3600]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The period between successive calls to IpduM_MainFunctionTx. This parameter is used by the IpduM generator to transform the values of the transmission related timing configuration parameters of the IpduM module to internal implementation specific counter or tick values.

####### STRING 类型参数

######## 1. IpduMUserConfigFile

- **UUID**: `24dc172c-1fc8-49b2-afaa-3aecdf8cf5dd`
- **参数名**: `IpduMUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

####### ENUMERATION 类型参数

######## 1. IpduMHeaderByteOrder

- **UUID**: `ECUC:afc9ce05-da15-49c3-869b-8caf4cc3a1e9`
- **参数名**: `IpduMHeaderByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IPDUM_BIG_ENDIAN`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_BIG_ENDIAN` (来源: Vector Informatik)
  - `IPDUM_LITTLE_ENDIAN` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the ByteOrder of the headers inside a Container I-PDU.

##### 2. IpduMGeneration

**容器属性**:

- **UUID**: `eac15d19-a0a8-4820-ab4c-748c2f386533`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the generation configuration parameters of the module IpduM.

###### 参数配置

此容器包含 **17** 个参数：

####### INTEGER 类型参数

######## 1. IpduMReduceBoolDataByNegationThreshold

- **UUID**: `2a3caf05-c0bc-47d5-bd0f-9331c292406a`
- **参数名**: `IpduMReduceBoolDataByNegationThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using the negation operator.
0: The optimization is not performed.
>0: This is the threshold to activate the data optimization.

Code: the code size is increased due to the usage of the negation operator in the data access.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: the runtime is increased due to the usage of the negation operator in the data access.

######## 2. IpduMReduceBoolDataByNumericalComparisonThreshold

- **UUID**: `4e3de8be-b216-4a60-997a-c05a7e99a3af`
- **参数名**: `IpduMReduceBoolDataByNumericalComparisonThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using comparison with other ROM data.
0: The optimization is not performed.
>0: This is the threshold to activate the data optimization.

Code: the code size is increased due to the usage of the operation in the data access.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: the runtime is increased due to the usage of the operation in the data access.

######## 3. IpduMReduceBoolDataByNumericalRelationThreshold

- **UUID**: `6059122e-ed64-47fa-8991-dfaaaee995b4`
- **参数名**: `IpduMReduceBoolDataByNumericalRelationThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using relational comparison with other ROM data.
0: The optimization is not performed.
>0: This is the threshold to activate the data optimization.

Code: the code size is increased due to the usage of the operation in the data access.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: the runtime is increased due to the usage of the operation in the data access.

######## 4. IpduMReduceNumericalDataByOffsetThreshold

- **UUID**: `fb518410-21d4-423f-9ad2-ed4c64241832`
- **参数名**: `IpduMReduceNumericalDataByOffsetThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS PRE-COMPILE ROM data by using a constant offset.
0: The optimization is not performed.
>0: This is the threshold to activate the data optimization.

Code: the code size is increased due to the usage of the constant offset operation in the data access.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: the runtime is increased due to the usage of the constant offset operation in the data access.

######## 5. IpduMReduceNumericalDataByArraySubtractionThreshold

- **UUID**: `9f34d5f1-e1ae-4a46-848f-27a48b2792bc`
- **参数名**: `IpduMReduceNumericalDataByArraySubtractionThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS PRE-COMPILE ROM data by using a subtraction with other ROM data.
0: The optimization is not performed.
>0: This is the threshold to activate the data optimization.

Code: the code size is increased due to the usage of the operation in the data access.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: the runtime is increased due to the usage of the operation in the data access.

####### BOOLEAN 类型参数

######## 1. IpduMOutOfBoundsWriteSanitizer

- **UUID**: `d679fa7e-4541-401c-9c37-13d4ff69b1ed`
- **参数名**: `IpduMOutOfBoundsWriteSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.
This debugging feature must not be used in production code!

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 2. IpduMOutOfBoundsReadSanitizer

- **UUID**: `9cf56b23-a733-42a8-ba69-fa23ca4e94c0`
- **参数名**: `IpduMOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.
This debugging feature must not be used in production code!

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 3. IpduMReduceConstantData2Define

- **UUID**: `d99ec2ea-c147-4827-b3da-8c63a9baa77a`
- **参数名**: `IpduMReduceConstantData2Define`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM arrays as constant define.

FALSE: ROM arrays are generated as data even if all values are identical.
TRUE: ROM arrays are generated as constant define if all values are identical.

######## 4. IpduMDeduplicateIndirectedData

- **UUID**: `7ea4b841-1114-4cd1-a685-454e80d92a7a`
- **参数名**: `IpduMDeduplicateIndirectedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to compress 0:N relational ROM data in all CONFIG-CLASSES without increasing the runtime.
This option can be used in lib builds and in postbuild configurations.

TRUE: 0:N relational ROM data is compressed without decreasing the runtime.
Code: no change expected.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: no change expected.

FALSE: 0:N relational ROM data is not compressed.

######## 5. IpduMReduceDataByStreaming

- **UUID**: `e651508f-980c-4768-8c9d-10c94733c2fa`
- **参数名**: `IpduMReduceDataByStreaming`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to pack generated CONFIG-CLASS PRE-COMPILE ROM data into a data type dependent stream.

TRUE: generated const data is packed into a data type dependent stream.
Code: no change expected.
RAM: no change expected.
ROM: configuration dependent smaller than with FALSE.
Runtime: no change expected.

FALSE: generated const data is not packed into a data type dependent stream.

######## 6. IpduMShortSymbols

- **UUID**: `ee978e19-f9c5-4ac0-bd6e-6ba68042793c`
- **参数名**: `IpduMShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

######## 7. IpduMInterfacesForDeactivatedData

- **UUID**: `712405e8-cdf5-45d1-ae37-841361ecb491`
- **参数名**: `IpduMInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

######## 8. IpduMReferringKeysInComments

- **UUID**: `a2d73f39-cfc9-4c9c-ae25-e99421fb36ca`
- **参数名**: `IpduMReferringKeysInComments`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate referring keys in comments. This is an advantage for the developer to investigate indirections, but this feature reduces the overall readability of the generated data.

FALSE: referring keys are not generated in comments.
TRUE: referring keys are generated in comments.

####### ENUMERATION 类型参数

######## 1. IpduMOutOfBoundsWriteProtectionStrategy

- **UUID**: `709f0688-a83c-4a3d-aadd-29d5e061a454`
- **参数名**: `IpduMOutOfBoundsWriteProtectionStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `INDEX_SATURATION` (来源: Vector Informatik)
  - `INDEX_CHECKING` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter is used to configure a strategy to protect the code to write out of bounds.

NONE: no protection strategy is generated in the data access.
INDEX_SATURATION: arrays are blown up and the data access index is saturated by an appropriate mask. The advantage is the speed of the data access, but own data elements at other indexes of the same variable can be overridden. This debugging feature must not be used in production code!
INDEX_CHECKING: the data access index is validated by a runtime check. The advantage is that values are never written to incorrect indexes of the data access. This debugging feature must not be used in production code!

######## 2. IpduMBoolDataInArrayOfStructStrategy

- **UUID**: `50e44902-5374-4ec1-b8c6-8bdf0845300d`
- **参数名**: `IpduMBoolDataInArrayOfStructStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `BITMASKING`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BOOLEAN`
  - `BITFIELD`
  - `BITMASKING`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter is used to tailor the usage of boolean data in structures in all CONFIG-CLASSES. The difference between BITFIELD and BITMASKING depends on your compiler options and memory mapping.

BOOLEAN: The datatype of boolean data is native boolean.
Code: the code size is small.
RAM: no change expected.
ROM: the ROM size is large.
Runtime: the runtime is fast.

BITFIELD: The bitfield type is used and the compiler extracts the boolean data from structures.
Code: the code size is larger than using BOOLEAN.
RAM: no change expected.
ROM: the ROM size is smaller than using BOOLEAN.
Runtime: the runtime is larger than using BOOLEAN.

BITMASKING: Generated Masks are used to extract the boolean data from structures.
Code: the code size is larger than using BOOLEAN.
RAM: no change expected.
ROM: the ROM size is smaller than using BOOLEAN.
Runtime: the runtime is larger than using BOOLEAN.

######## 3. IpduMDataDeduplicationStrategy

- **UUID**: `15a37771-4df1-48d1-a82f-df2a5de332d1`
- **参数名**: `IpduMDataDeduplicationStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WITH_CAST`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE`
  - `WITHOUT_CAST`
  - `WITH_CAST`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter is used to deduplicate CONFIG-CLASS PRE-COMPILE  ROM data.

NONE: The generated data is not deduplicated.

WITHOUT_CAST: The data is deduplicated without using casts.
Code: no change expected.
RAM: no change expected.
ROM: the ROM size can be minimized.
Runtime: no change expected.

WITH_CAST: The data is deduplicated using casts.
Code: no change expected.
RAM: no change expected.
ROM: the ROM size can be minimized more than in DEDUPLICATE_CONST_DATA_WITHOUT_CAST.
Runtime: no change expected.

######## 4. IpduMReduceBoolDataByNumericalOperandStrategy

- **UUID**: `a1b9355f-508e-43fc-9e69-b21ef94dee6f`
- **参数名**: `IpduMReduceBoolDataByNumericalOperandStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WITH_ANY_VALUE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE`
  - `WITH_ZERO`
  - `WITH_ANY_VALUE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter is used to taylor the CONFIG-CLASS PRE-COMPILE ROM data deduplication mechaisms. A comparison with 0 is very efficient, but a numerical comparison with a value not 0 can be used to increase the ROM data compression rate.

NONE: ROM data deduplications are switched off.
Code: the code size is small.
RAM: no change expected.
ROM: the ROM size is large.
Runtime: the runtime is fast.

WITH_ZERO: ROM data deduplications can be applied with the value 0.
Code: the code size is larger than using NONE
RAM: no change expected.
ROM: the ROM size is smaller than using NONE.
Runtime: the runtime is larger than using NONE.

WITH_ANY_VALUE: ROM data deduplications can be applied with any numerical value.
Code: the code size is larger than using NONE
RAM: no change expected.
ROM: the ROM size is smaller than using DEDUPLICATE_DATA_WITH_ZERO.
Runtime: the runtime is larger than using NONE.

##### 3. IpduMConfig

**容器属性**:

- **UUID**: `73a36c2b-a62a-43d7-86f3-bca4158cd990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMConfig`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the sub containers of the IpduM module. The IpduMTxPathway subcontainer includes information about transmitted multiplex I-PDUs. The IpduMRxPathway includes information about received multiplex I-PDUs.

###### 配置容器

本模块包含 **18** 个配置容器：

####### 1. IpduMContainedRxPdu

**容器属性**:

- **UUID**: `ECUC:23135174-a437-419a-9d97-d0c8a6da224d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMContainedRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration of a received contained Pdu.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMContainedPduHeaderId

- **UUID**: `ECUC:b2c8d44a-66f0-8b8e-46f4-c8c1d0191412`
- **参数名**: `IpduMContainedPduHeaderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Header Id which is part of the ContainerPdu when this ContainedPdu is inside.

########## 2. IpduMContainedPduOffset

- **UUID**: `ECUC:9d46e30a-1d3f-8303-3509-8be80c94c764`
- **参数名**: `IpduMContainedPduOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Static offset (in bytes) of the ContainedPdu.

########## 3. IpduMPduUpdateBitPosition

- **UUID**: `ECUC:845ed947-d78d-8d78-4d57-b62f10b3777c`
- **参数名**: `IpduMPduUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies where the PDU's Update-Bit is stored in the Container PDU (bit location of PDU's Update-Bit in the Container PDU).

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMContainedRxInContainerPduRef

- **UUID**: `ECUC:30e6206f-666f-4d8f-a66b-883ce64951f7`
- **引用名**: `IpduMContainedRxInContainerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `IpduMContainerRxPdu`
- **完整路径**: `/MICROSAR/IpduM/IpduMConfig/IpduMContainerRxPdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to a container Pdu this contained Pdu may be transported in.

########## 2. IpduMContainedRxPduRef

- **UUID**: `ECUC:2c109a6f-b369-4e64-8aab-d16df021b5eb`
- **引用名**: `IpduMContainedRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Pdu which represents this ContainedPdu and is used for reception indication.

####### 2. IpduMContainedTxPdu

**容器属性**:

- **UUID**: `ECUC:791848d7-cbc2-4736-823a-c714e80fa697`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMContainedTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration of a sender ContainedPdu.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. IpduMContainedPduHeaderId

- **UUID**: `ECUC:08cdcbad-8e7b-912a-2b97-bf0e114e985c`
- **参数名**: `IpduMContainedPduHeaderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Header Id which is part of the ContainerPdu when this ContainedPdu is inside.

########## 2. IpduMContainedPduOffset

- **UUID**: `ECUC:f34bda6d-44ca-889f-19ac-82344dca4bae`
- **参数名**: `IpduMContainedPduOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Static offset (in bytes) of the ContainedPdu.

########## 3. IpduMContainedTxPduHandleId

- **UUID**: `ECUC:30a9f077-e171-4238-96c7-b2abdefe20cf`
- **参数名**: `IpduMContainedTxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Handle Id of the ContainedPdu.

########## 4. IpduMContainedTxPduPriority

- **UUID**: `ECUC:ceed8f53-b9f8-48f4-a35a-5c53db1580e1`
- **参数名**: `IpduMContainedTxPduPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines a priority of a ContainedTxPdu. 255 represents the lowest priority and 0 represent the highest priority.

########## 5. IpduMPduUpdateBitPosition

- **UUID**: `ECUC:da63d0aa-ff18-9314-31fa-ac7b51e8fbc6`
- **参数名**: `IpduMPduUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies where the PDU's Update-Bit is stored in the Container PDU (bit location of PDU's Update-Bit in the Container PDU).

######### BOOLEAN 类型参数

########## 1. IpduMContainedTxPduConfirmation

- **UUID**: `ECUC:ea74c379-a393-4df0-bd9c-2405c7d70434`
- **参数名**: `IpduMContainedTxPduConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This Parameter determines whether for this contained I-PDU a TxConfirmation shall be provided. If set to TRUE a TxConfirmation is issued. It is not used when an I-PDU is requested using the trigger transmit API.

######### FLOAT 类型参数

########## 1. IpduMContainedTxPduSendTimeout

- **UUID**: `ECUC:e6fac165-cc62-4ab5-94e1-2cec0609f5f3`
- **参数名**: `IpduMContainedTxPduSendTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines a ContainedPdu specific sender timeout which can reduce the ContainerPdu timer when this ContainedPdu is put inside the ContainerPdu.

If this parameter is omitted, the linked Container-PDU must have a SendTimeout configured.

The value 0 does not have special semantics here, 0 is a normal, valid value.

######### ENUMERATION 类型参数

########## 1. IpduMContainedTxPduCollectionSemantics

- **UUID**: `ECUC:241b7e86-021b-48ba-b29a-79b59768422a`
- **参数名**: `IpduMContainedTxPduCollectionSemantics`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_COLLECT_LAST_IS_BEST` (来源: Vector Informatik)
  - `IPDUM_COLLECT_QUEUED` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines whether this IpduMContainedTxPdu shall be collected using a last-is-best or queued semantics.

########## 2. IpduMContainedTxPduTrigger

- **UUID**: `ECUC:1fc45d53-28ef-48a4-8195-4922ec1935ea`
- **参数名**: `IpduMContainedTxPduTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_TRIGGER_ALWAYS` (来源: Vector Informatik)
  - `IPDUM_TRIGGER_NEVER` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines whether this Pdu triggers the sending of the ContainerPdu.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMContainedTxInContainerPduRef

- **UUID**: `ECUC:0a15c013-c0d4-417d-9674-76207d08a72a`
- **引用名**: `IpduMContainedTxInContainerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IpduMContainerTxPdu`
- **完整路径**: `/MICROSAR/IpduM/IpduMConfig/IpduMContainerTxPdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the container Pdu which this contained Pdu shall be collected in.

########## 2. IpduMContainedTxPduRef

- **UUID**: `ECUC:1b2057ec-907f-4bc7-9f34-25a9eef84053`
- **引用名**: `IpduMContainedTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Pdu which represents this ContainedPdu and is used for transmission.

####### 3. IpduMContainerRxPdu

**容器属性**:

- **UUID**: `ECUC:5d925ddf-12e3-4599-b270-042c31e381bb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMContainerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration of a receiver ContainerPdu which may collect several ContainedPdus.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. IpduMContainerQueueSize

- **UUID**: `ECUC:0bd46c1b-1938-859e-52eb-9f58b74213ec`
- **参数名**: `IpduMContainerQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines a local queue for handling of each ContainerPdu.

########## 2. IpduMContainerRxHandleId

- **UUID**: `ECUC:aa0c884d-6267-4829-9396-98b8fd5a1cad`
- **参数名**: `IpduMContainerRxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Handle Id used by the PduR for RxIndication.

######### ENUMERATION 类型参数

########## 1. IpduMContainerHeaderSize

- **UUID**: `ECUC:f6085257-2137-889a-5714-432746509801`
- **参数名**: `IpduMContainerHeaderSize`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_HEADERTYPE_LONG` (来源: Vector Informatik)
  - `IPDUM_HEADERTYPE_SHORT` (来源: Vector Informatik)
  - `IPDUM_HEADERTYPE_NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the layout of the header information (header id and length).

########## 2. IpduMContainerPduProcessing

- **UUID**: `ECUC:54dd7b87-c70e-4292-8fb0-d2248a0b7e19`
- **参数名**: `IpduMContainerPduProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IPDUM_PROCESSING_IMMEDIATE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_PROCESSING_DEFERRED` (来源: Vector Informatik)
  - `IPDUM_PROCESSING_IMMEDIATE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines whether the handling of this ContainerPdu shall be done in the context of the caller (IMMEDIATE) or in the next IpduM main function (DEFERRED).

########## 3. IpduMContainerRxAcceptContainedPdu

- **UUID**: `ECUC:722a835c-4867-4f34-94e1-4936cec8948f`
- **参数名**: `IpduMContainerRxAcceptContainedPdu`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_ACCEPT_ALL` (来源: Vector Informatik)
  - `IPDUM_ACCEPT_CONFIGURED` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines for the received IpduMRxContainerPdu whether the list of referencing IpduMRxContainedPdus (via the reference IpduMRxContainedPduContainerRef) is a closed set.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMContainerRxPduRef

- **UUID**: `ECUC:f2caa5c2-e8b8-4fc2-b142-005df5ec6c44`
- **引用名**: `IpduMContainerRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Pdu which represents the container and is used for reception.

####### 4. IpduMContainerTxPdu

**容器属性**:

- **UUID**: `ECUC:05166e13-676a-4d11-857b-c0a25b5bf15a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMContainerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration of a transmitted container Pdu.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. IpduMContainerQueueSize

- **UUID**: `ECUC:b3587c4f-6dbf-8d16-25f7-5bcee0ba838b`
- **参数名**: `IpduMContainerQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines a local queue for handling of each ContainerPdu.

The actual queue length in the implementation is incremented by 1 as a performance optimization. So the current instance is within the queue and does not need additional copy instructions. The maximum value was lowered to 254 to enable this performance optimization.

########## 2. IpduMContainerTxHandleId

- **UUID**: `ECUC:efa3fff6-909e-44c5-8511-bf9555ed9dcf`
- **参数名**: `IpduMContainerTxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Handle Id used by the PduR for TxConfirmation and for TriggerTransmit of the ContainerPdu.

########## 3. IpduMContainerTxSizeThreshold

- **UUID**: `ECUC:a06d30c7-b0ce-4b1b-9cb1-9cb21b510de7`
- **参数名**: `IpduMContainerTxSizeThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the size threshold in bytes which, when exceeded, triggers the sending of the ContainerPdu although the maxium Pdu size (PduLength parameter of Pdu object)  has not been reached yet.

########## 4. IpduMUnusedAreasDefault

- **UUID**: `ECUC:27348714-d1c3-4091-98be-692839840e20`
- **参数名**: `IpduMUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: IpduM fills not updated areas of the Container PDU with this byte-pattern.

######### BOOLEAN 类型参数

########## 1. IpduMContainerTxFirstContainedPduTrigger

- **UUID**: `ECUC:2ed7ba6a-3bcf-4daa-9296-e4b8f3bbbf75`
- **参数名**: `IpduMContainerTxFirstContainedPduTrigger`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines if the transmission of this IpduMContainerTxPdu shall be requested right after the first IpduMContainedTxPdu was put into it.

######### FLOAT 类型参数

########## 1. IpduMContainerTxConfirmationTimeout

- **UUID**: `ECUC:fcf4eda4-4f81-4ee9-abe0-503bb347e758`
- **参数名**: `IpduMContainerTxConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This timeout (in seconds) defines the timeout period for monitoring the reception of the TxConfirmation. It is not used when an I-PDU is requested using the trigger transmit API.

########## 2. IpduMContainerTxSendTimeout

- **UUID**: `ECUC:9a4008f5-85c6-424a-9d51-5e7833214912`
- **参数名**: `IpduMContainerTxSendTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: When this timeout expires the ContainerPdu is triggered for sending. The respective timer is started when the first Pdu is put into the ContainerPdu.

######### ENUMERATION 类型参数

########## 1. IpduMContainerHeaderSize

- **UUID**: `ECUC:9d8c628b-75be-9012-2a1f-ff9d6fc907a0`
- **参数名**: `IpduMContainerHeaderSize`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_HEADERTYPE_LONG` (来源: Vector Informatik)
  - `IPDUM_HEADERTYPE_SHORT` (来源: Vector Informatik)
  - `IPDUM_HEADERTYPE_NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the layout of the header information (header id and length).

########## 2. IpduMContainerTxTriggerMode

- **UUID**: `ECUC:fe00aca6-2aa1-47c5-ac1b-c708b0a2da1c`
- **参数名**: `IpduMContainerTxTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_DIRECT` (来源: Vector Informatik)
  - `IPDUM_TRIGGERTRANSMIT` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines whether this ContainerPdu is fetched via trigger transmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMContainerTxPduRef

- **UUID**: `ECUC:c60e1385-2617-4809-8f06-3165454aef0e`
- **引用名**: `IpduMContainerTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Pdu which represents the container and is used for transmission.

####### 5. IpduMRxPathway

**容器属性**:

- **UUID**: `d6a59454-e00d-42aa-8fce-ea57183abb6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxPathway`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines one lower layer I-PDU that is received from the network and resolved to multiple upper layer I-PDUs depending on the selector field value.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. IpduMRxIndication

**容器属性**:

- **UUID**: `957fe70d-c081-4872-ad43-4a455c13083c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxIndication`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Contains the configuration for incoming calls to the IpduM_RxIndication API.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMRxHandleId

- **UUID**: `1ad54562-ca2c-4776-abc6-2b8415640ec4`
- **参数名**: `IpduMRxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the I-PDU ID of the incoming I-PDU. If an incoming RxIndication's I-PDU ID matches this value then it is unpacked according to the specification in this container.

########### ENUMERATION 类型参数

############ 1. IpduMByteOrder

- **UUID**: `efb8ed48-6a62-420b-af4b-bff7033d0774`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BIG_ENDIAN`
  - `LITTLE_ENDIAN`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.
This is necessary because the positions are defined differently (LSB for little endian and MSB for big endian) based on endianness.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMRxIndicationPduRef

- **UUID**: `77d9f123-af11-402b-b55a-26458f1fa264`
- **引用名**: `IpduMRxIndicationPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the lower layer I-PDU that is processed and demultiplexed by the IpduM.

########## 配置容器

本模块包含 **5** 个配置容器：

########### 1. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `77f52ec5-ee20-4382-8e0b-579fcb753441`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. If an incoming received I-PDU's selector field matches the IpduMRxSelectorValue of any of the dynamic parts, the new outgoing I-PDU for the dynamic part is de-multiplexed according to the corresponding dynamic IpduMSegment specification and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IpduMRxSelectorValue

- **UUID**: `4db5e83b-090c-4651-a3c5-f5ffee79a524`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the dynamic part that is transmitted within the received multiplexed I-PDU.
If the selector field value of the received multiplex I-PDU matches this value. It will be de-multiplexed according to the configuration in the parent IpduMRxDynamicPart container.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. IpduMOutgoingDynamicPduRef

- **UUID**: `e7dc82d2-b76c-4e55-85a4-49ff27353685`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that is notified by the IpduM depending on the selector field value.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

################ 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

########### 2. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############## 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

########### 3. IpduMRxStaticPart

**容器属性**:

- **UUID**: `7d20171e-1213-4dd1-ab59-073d5581fd57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of incoming lower layer I-PDU. If a static part is defined any reception of the lower layer I-PDU will cause the notification of the upper layer I-PDU representing the static part. This is independent from the selector field value.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. IpduMOutgoingStaticPduRef

- **UUID**: `1947f98a-d4f0-41e6-8105-ba5a80bbe23b`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that notified by the IPDUM as static I-PDU part of each multiplexed I-PDU.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

################ 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 4. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############## 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 5. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `cc327dfc-37dd-4288-a5b1-7ce3f1070eb9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the location and the length of the selector field that is used to identify the dynamic part of each multiplexed I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSelectorFieldLength

- **UUID**: `a2926cdc-e3a9-4144-9971-7764d637299b`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

############## 2. IpduMSelectorFieldPosition

- **UUID**: `eabf5332-45e6-4867-8e32-1283c0ff11ee`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.
Bits are numbered ascending, bytes depending on the endianness defined in IpduMByteOrder.

######### 2. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `77f52ec5-ee20-4382-8e0b-579fcb753441`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. If an incoming received I-PDU's selector field matches the IpduMRxSelectorValue of any of the dynamic parts, the new outgoing I-PDU for the dynamic part is de-multiplexed according to the corresponding dynamic IpduMSegment specification and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IpduMRxSelectorValue

- **UUID**: `4db5e83b-090c-4651-a3c5-f5ffee79a524`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the dynamic part that is transmitted within the received multiplexed I-PDU.
If the selector field value of the received multiplex I-PDU matches this value. It will be de-multiplexed according to the configuration in the parent IpduMRxDynamicPart container.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingDynamicPduRef

- **UUID**: `e7dc82d2-b76c-4e55-85a4-49ff27353685`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that is notified by the IpduM depending on the selector field value.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############## 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

######### 3. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

######### 4. IpduMRxStaticPart

**容器属性**:

- **UUID**: `7d20171e-1213-4dd1-ab59-073d5581fd57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of incoming lower layer I-PDU. If a static part is defined any reception of the lower layer I-PDU will cause the notification of the upper layer I-PDU representing the static part. This is independent from the selector field value.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingStaticPduRef

- **UUID**: `1947f98a-d4f0-41e6-8105-ba5a80bbe23b`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that notified by the IPDUM as static I-PDU part of each multiplexed I-PDU.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############## 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 6. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `cc327dfc-37dd-4288-a5b1-7ce3f1070eb9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the location and the length of the selector field that is used to identify the dynamic part of each multiplexed I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `a2926cdc-e3a9-4144-9971-7764d637299b`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

############ 2. IpduMSelectorFieldPosition

- **UUID**: `eabf5332-45e6-4867-8e32-1283c0ff11ee`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.
Bits are numbered ascending, bytes depending on the endianness defined in IpduMByteOrder.

####### 6. IpduMRxIndication

**容器属性**:

- **UUID**: `957fe70d-c081-4872-ad43-4a455c13083c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxIndication`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Contains the configuration for incoming calls to the IpduM_RxIndication API.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMRxHandleId

- **UUID**: `1ad54562-ca2c-4776-abc6-2b8415640ec4`
- **参数名**: `IpduMRxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the I-PDU ID of the incoming I-PDU. If an incoming RxIndication's I-PDU ID matches this value then it is unpacked according to the specification in this container.

######### ENUMERATION 类型参数

########## 1. IpduMByteOrder

- **UUID**: `efb8ed48-6a62-420b-af4b-bff7033d0774`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BIG_ENDIAN`
  - `LITTLE_ENDIAN`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.
This is necessary because the positions are defined differently (LSB for little endian and MSB for big endian) based on endianness.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMRxIndicationPduRef

- **UUID**: `77d9f123-af11-402b-b55a-26458f1fa264`
- **引用名**: `IpduMRxIndicationPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the lower layer I-PDU that is processed and demultiplexed by the IpduM.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `77f52ec5-ee20-4382-8e0b-579fcb753441`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. If an incoming received I-PDU's selector field matches the IpduMRxSelectorValue of any of the dynamic parts, the new outgoing I-PDU for the dynamic part is de-multiplexed according to the corresponding dynamic IpduMSegment specification and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IpduMRxSelectorValue

- **UUID**: `4db5e83b-090c-4651-a3c5-f5ffee79a524`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the dynamic part that is transmitted within the received multiplexed I-PDU.
If the selector field value of the received multiplex I-PDU matches this value. It will be de-multiplexed according to the configuration in the parent IpduMRxDynamicPart container.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingDynamicPduRef

- **UUID**: `e7dc82d2-b76c-4e55-85a4-49ff27353685`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that is notified by the IpduM depending on the selector field value.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############## 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

######### 2. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

######### 3. IpduMRxStaticPart

**容器属性**:

- **UUID**: `7d20171e-1213-4dd1-ab59-073d5581fd57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of incoming lower layer I-PDU. If a static part is defined any reception of the lower layer I-PDU will cause the notification of the upper layer I-PDU representing the static part. This is independent from the selector field value.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingStaticPduRef

- **UUID**: `1947f98a-d4f0-41e6-8105-ba5a80bbe23b`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that notified by the IPDUM as static I-PDU part of each multiplexed I-PDU.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############## 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 4. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `cc327dfc-37dd-4288-a5b1-7ce3f1070eb9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the location and the length of the selector field that is used to identify the dynamic part of each multiplexed I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `a2926cdc-e3a9-4144-9971-7764d637299b`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

############ 2. IpduMSelectorFieldPosition

- **UUID**: `eabf5332-45e6-4867-8e32-1283c0ff11ee`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.
Bits are numbered ascending, bytes depending on the endianness defined in IpduMByteOrder.

####### 7. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `77f52ec5-ee20-4382-8e0b-579fcb753441`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. If an incoming received I-PDU's selector field matches the IpduMRxSelectorValue of any of the dynamic parts, the new outgoing I-PDU for the dynamic part is de-multiplexed according to the corresponding dynamic IpduMSegment specification and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IpduMRxSelectorValue

- **UUID**: `4db5e83b-090c-4651-a3c5-f5ffee79a524`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the dynamic part that is transmitted within the received multiplexed I-PDU.
If the selector field value of the received multiplex I-PDU matches this value. It will be de-multiplexed according to the configuration in the parent IpduMRxDynamicPart container.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingDynamicPduRef

- **UUID**: `e7dc82d2-b76c-4e55-85a4-49ff27353685`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that is notified by the IpduM depending on the selector field value.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

####### 8. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

########## 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

####### 9. IpduMRxStaticPart

**容器属性**:

- **UUID**: `7d20171e-1213-4dd1-ab59-073d5581fd57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of incoming lower layer I-PDU. If a static part is defined any reception of the lower layer I-PDU will cause the notification of the upper layer I-PDU representing the static part. This is independent from the selector field value.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingStaticPduRef

- **UUID**: `1947f98a-d4f0-41e6-8105-ba5a80bbe23b`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that notified by the IPDUM as static I-PDU part of each multiplexed I-PDU.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 10. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

########## 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 11. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `cc327dfc-37dd-4288-a5b1-7ce3f1070eb9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the location and the length of the selector field that is used to identify the dynamic part of each multiplexed I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `a2926cdc-e3a9-4144-9971-7764d637299b`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

########## 2. IpduMSelectorFieldPosition

- **UUID**: `eabf5332-45e6-4867-8e32-1283c0ff11ee`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.
Bits are numbered ascending, bytes depending on the endianness defined in IpduMByteOrder.

####### 12. IpduMTxPathway

**容器属性**:

- **UUID**: `a860e300-7600-4a8d-80d7-a017f5f9f612`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxPathway`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines one lower layer I-PDU that is assembled from multiple upper layer I-PDUs depending on the selector field value.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. IpduMTxRequest

**容器属性**:

- **UUID**: `a0fa246f-5b36-4e22-82b4-998ad2ef96d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxRequest`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This is used to specify the configuration for Transmit requests.

There will one instance of this container for each I-PDU that can be requested for transmission (the outgoing I-PDUs) by the IpduM.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. IpduMIPduUnusedAreasDefault

- **UUID**: `74d2a1f2-f593-40e4-9905-c1e0a48730cc`
- **参数名**: `IpduMIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IPDUM  module fills unused areas of a transmitted multiplexed I-PDU with this bit-pattern.
If this attribute is undefined unused areas are not initialized any may have an arbitrary value

############ 2. IpduMTxConfirmationPduId

- **UUID**: `b82c12be-4a9b-450c-a4e7-bbdc15cf44d3`
- **参数名**: `IpduMTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The handle Id used by the lower layer to identify this IPDUM I-PDU during TriggerTransmit and TxConfirmation calls.

########### FLOAT 类型参数

############ 1. IpduMTxConfirmationTimeout

- **UUID**: `cf596dbd-7ba4-4d59-b537-e344bb587d81`
- **参数名**: `IpduMTxConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the timeout time for monitoring the TxConfirmation call from the lower layer (i.e. the transmission of the corresponding multiplex I-PDU occured).
Parameter is not used for lower layer I-PDU that use the TriggerTransmit API.

########### ENUMERATION 类型参数

############ 1. IpduMByteOrder

- **UUID**: `09e480a4-cdc7-46df-826d-dba06b30152d`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

############ 2. IpduMTxTriggerMode

- **UUID**: `06a7e279-fb78-4380-9334-910d5b3ec857`
- **参数名**: `IpduMTxTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DYNAMIC_PART_TRIGGER`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DYNAMIC_PART_TRIGGER`
  - `NONE`
  - `STATIC_OR_DYNAMIC_PART_TRIGGER`
  - `STATIC_PART_TRIGGER`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the upper layer transmission event that causes the transmission of the multiplexed I-PDU through the lower layer.
	NONE: do not trigger transmission on upper layer transmission events
	STATIC_PART_TRIGGER: trigger transmission if the static part I-PDU is transmitted to IpduM
	DYNAMIC_PART_TRIGGER: trigger transmission if the dynamic part I-PDU is transmitted to IpduM
	STATIC_OR_DYNAMIC_PART_TRIGGER: trigger transmission if the static or dynamic part I-PDU is transmitted to IpduM

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMInitialDynamicPart

- **UUID**: `04957cef-24c7-4006-9391-5bba02bb5300`
- **引用名**: `IpduMInitialDynamicPart`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IpduMTxDynamicPart`
- **完整路径**: `/AUTOSAR/EcucDefs/IpduM/IpduMConfig/IpduMTxPathway/IpduMTxRequest/IpduMTxDynamicPart`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the dynamic part that shall be used to initialize this multiplexed TX-I-PDU. This part is used as the dynamic part in case of a static part first being triggered for transmission after ECU initialization, i.e. no last transmitted dynamic part is available yet.

############ 2. IpduMOutgoingPduRef

- **UUID**: `baaca0dd-c423-48ec-8e0a-222b0f11806b`
- **引用名**: `IpduMOutgoingPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to I-Pdu representation in the ECU Configuration Description exchange file.
When the outgoing I-PDU is sent this is the I-PDU ID to give it. It is the IPDUM  I-PDU ID of the assembled I-PDU.

########## 配置容器

本模块包含 **5** 个配置容器：

########### 1. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `1ce1c9d6-379f-42ef-95da-d37d013bf4f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSelectorFieldLength

- **UUID**: `3d638d53-14fd-41b0-901e-9aea97b70f4f`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

############## 2. IpduMSelectorFieldPosition

- **UUID**: `6ffe9e06-37e6-42e5-a39b-cc184e3ab6c6`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

########### 2. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `0b5e3db8-89b1-43ee-8fec-97b4e27bddeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honored. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. IpduMTxDynamicHandleId

- **UUID**: `b0c7d66e-9580-41d9-89e1-dc738290c4b1`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. When the handle of an incoming Tx Request matches this, the TxDynamicPart is multiplexed according to the corresponding IpduMSegments.

############# BOOLEAN 类型参数

############## 1. IpduMJitUpdate

- **UUID**: `37c53dab-5b16-46aa-80cd-eeac23b053db`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for this dynamic part I-PDU is used, i.e. the dynamic part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

############## 2. IpduMTxDynamicConfirmation

- **UUID**: `7505eec3-7047-4a0f-9e8a-891430382ce5`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. IpduMTxDynamicPduRef

- **UUID**: `2ffc37d5-0efa-48b1-8bea-51dd8ae1a018`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

################ 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 3. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 4. IpduMTxStaticPart

**容器属性**:

- **UUID**: `519af9ba-66eb-4fa9-9b9d-36dcfcf9df26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of outgoing multiplexed lower layer I-PDU. If a static part is defined any transmission of the lower layer I-PDU will include I-PDU data provided by the static part. This is independent from the selector field value that shall be transmitted.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. IpduMTxStaticHandleId

- **UUID**: `0caaa019-2eb4-473a-9638-1f2f5f178fa6`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. If the handle of an incoming Tx Request matches this, the TxStaticPart is multiplexed according to the corresponding IpduMSegments and the send mode is honored.

############# BOOLEAN 类型参数

############## 1. IpduMJitUpdate

- **UUID**: `88d3dfb6-7143-4e5c-ad6e-dd355b4a5c26`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for the static part I-PDU is used, i.e. the static part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

############## 2. IpduMTxStaticConfirmation

- **UUID**: `01638e05-a1fc-4540-84fa-30e80a576521`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. IpduMTxStaticPduRef

- **UUID**: `d7ee9102-2b9f-4f80-b1f4-dafd3add511e`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the multiplexed Pdu's (static part, if exists) representation in the ECU Configuration Description exchange file to be transmitted.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

################ 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 5. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 2. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `1ce1c9d6-379f-42ef-95da-d37d013bf4f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `3d638d53-14fd-41b0-901e-9aea97b70f4f`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

############ 2. IpduMSelectorFieldPosition

- **UUID**: `6ffe9e06-37e6-42e5-a39b-cc184e3ab6c6`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

######### 3. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `0b5e3db8-89b1-43ee-8fec-97b4e27bddeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honored. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxDynamicHandleId

- **UUID**: `b0c7d66e-9580-41d9-89e1-dc738290c4b1`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. When the handle of an incoming Tx Request matches this, the TxDynamicPart is multiplexed according to the corresponding IpduMSegments.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `37c53dab-5b16-46aa-80cd-eeac23b053db`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for this dynamic part I-PDU is used, i.e. the dynamic part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

############ 2. IpduMTxDynamicConfirmation

- **UUID**: `7505eec3-7047-4a0f-9e8a-891430382ce5`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxDynamicPduRef

- **UUID**: `2ffc37d5-0efa-48b1-8bea-51dd8ae1a018`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 4. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMTxStaticPart

**容器属性**:

- **UUID**: `519af9ba-66eb-4fa9-9b9d-36dcfcf9df26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of outgoing multiplexed lower layer I-PDU. If a static part is defined any transmission of the lower layer I-PDU will include I-PDU data provided by the static part. This is independent from the selector field value that shall be transmitted.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxStaticHandleId

- **UUID**: `0caaa019-2eb4-473a-9638-1f2f5f178fa6`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. If the handle of an incoming Tx Request matches this, the TxStaticPart is multiplexed according to the corresponding IpduMSegments and the send mode is honored.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `88d3dfb6-7143-4e5c-ad6e-dd355b4a5c26`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for the static part I-PDU is used, i.e. the static part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

############ 2. IpduMTxStaticConfirmation

- **UUID**: `01638e05-a1fc-4540-84fa-30e80a576521`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxStaticPduRef

- **UUID**: `d7ee9102-2b9f-4f80-b1f4-dafd3add511e`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the multiplexed Pdu's (static part, if exists) representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 6. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 13. IpduMTxRequest

**容器属性**:

- **UUID**: `a0fa246f-5b36-4e22-82b4-998ad2ef96d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxRequest`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This is used to specify the configuration for Transmit requests.

There will one instance of this container for each I-PDU that can be requested for transmission (the outgoing I-PDUs) by the IpduM.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. IpduMIPduUnusedAreasDefault

- **UUID**: `74d2a1f2-f593-40e4-9905-c1e0a48730cc`
- **参数名**: `IpduMIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IPDUM  module fills unused areas of a transmitted multiplexed I-PDU with this bit-pattern.
If this attribute is undefined unused areas are not initialized any may have an arbitrary value

########## 2. IpduMTxConfirmationPduId

- **UUID**: `b82c12be-4a9b-450c-a4e7-bbdc15cf44d3`
- **参数名**: `IpduMTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The handle Id used by the lower layer to identify this IPDUM I-PDU during TriggerTransmit and TxConfirmation calls.

######### FLOAT 类型参数

########## 1. IpduMTxConfirmationTimeout

- **UUID**: `cf596dbd-7ba4-4d59-b537-e344bb587d81`
- **参数名**: `IpduMTxConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the timeout time for monitoring the TxConfirmation call from the lower layer (i.e. the transmission of the corresponding multiplex I-PDU occured).
Parameter is not used for lower layer I-PDU that use the TriggerTransmit API.

######### ENUMERATION 类型参数

########## 1. IpduMByteOrder

- **UUID**: `09e480a4-cdc7-46df-826d-dba06b30152d`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

########## 2. IpduMTxTriggerMode

- **UUID**: `06a7e279-fb78-4380-9334-910d5b3ec857`
- **参数名**: `IpduMTxTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DYNAMIC_PART_TRIGGER`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DYNAMIC_PART_TRIGGER`
  - `NONE`
  - `STATIC_OR_DYNAMIC_PART_TRIGGER`
  - `STATIC_PART_TRIGGER`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the upper layer transmission event that causes the transmission of the multiplexed I-PDU through the lower layer.
	NONE: do not trigger transmission on upper layer transmission events
	STATIC_PART_TRIGGER: trigger transmission if the static part I-PDU is transmitted to IpduM
	DYNAMIC_PART_TRIGGER: trigger transmission if the dynamic part I-PDU is transmitted to IpduM
	STATIC_OR_DYNAMIC_PART_TRIGGER: trigger transmission if the static or dynamic part I-PDU is transmitted to IpduM

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMInitialDynamicPart

- **UUID**: `04957cef-24c7-4006-9391-5bba02bb5300`
- **引用名**: `IpduMInitialDynamicPart`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IpduMTxDynamicPart`
- **完整路径**: `/AUTOSAR/EcucDefs/IpduM/IpduMConfig/IpduMTxPathway/IpduMTxRequest/IpduMTxDynamicPart`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the dynamic part that shall be used to initialize this multiplexed TX-I-PDU. This part is used as the dynamic part in case of a static part first being triggered for transmission after ECU initialization, i.e. no last transmitted dynamic part is available yet.

########## 2. IpduMOutgoingPduRef

- **UUID**: `baaca0dd-c423-48ec-8e0a-222b0f11806b`
- **引用名**: `IpduMOutgoingPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to I-Pdu representation in the ECU Configuration Description exchange file.
When the outgoing I-PDU is sent this is the I-PDU ID to give it. It is the IPDUM  I-PDU ID of the assembled I-PDU.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `1ce1c9d6-379f-42ef-95da-d37d013bf4f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `3d638d53-14fd-41b0-901e-9aea97b70f4f`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

############ 2. IpduMSelectorFieldPosition

- **UUID**: `6ffe9e06-37e6-42e5-a39b-cc184e3ab6c6`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

######### 2. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `0b5e3db8-89b1-43ee-8fec-97b4e27bddeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honored. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxDynamicHandleId

- **UUID**: `b0c7d66e-9580-41d9-89e1-dc738290c4b1`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. When the handle of an incoming Tx Request matches this, the TxDynamicPart is multiplexed according to the corresponding IpduMSegments.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `37c53dab-5b16-46aa-80cd-eeac23b053db`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for this dynamic part I-PDU is used, i.e. the dynamic part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

############ 2. IpduMTxDynamicConfirmation

- **UUID**: `7505eec3-7047-4a0f-9e8a-891430382ce5`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxDynamicPduRef

- **UUID**: `2ffc37d5-0efa-48b1-8bea-51dd8ae1a018`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 3. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 4. IpduMTxStaticPart

**容器属性**:

- **UUID**: `519af9ba-66eb-4fa9-9b9d-36dcfcf9df26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of outgoing multiplexed lower layer I-PDU. If a static part is defined any transmission of the lower layer I-PDU will include I-PDU data provided by the static part. This is independent from the selector field value that shall be transmitted.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxStaticHandleId

- **UUID**: `0caaa019-2eb4-473a-9638-1f2f5f178fa6`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. If the handle of an incoming Tx Request matches this, the TxStaticPart is multiplexed according to the corresponding IpduMSegments and the send mode is honored.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `88d3dfb6-7143-4e5c-ad6e-dd355b4a5c26`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for the static part I-PDU is used, i.e. the static part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

############ 2. IpduMTxStaticConfirmation

- **UUID**: `01638e05-a1fc-4540-84fa-30e80a576521`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxStaticPduRef

- **UUID**: `d7ee9102-2b9f-4f80-b1f4-dafd3add511e`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the multiplexed Pdu's (static part, if exists) representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 14. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `1ce1c9d6-379f-42ef-95da-d37d013bf4f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `3d638d53-14fd-41b0-901e-9aea97b70f4f`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

########## 2. IpduMSelectorFieldPosition

- **UUID**: `6ffe9e06-37e6-42e5-a39b-cc184e3ab6c6`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

####### 15. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `0b5e3db8-89b1-43ee-8fec-97b4e27bddeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honored. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxDynamicHandleId

- **UUID**: `b0c7d66e-9580-41d9-89e1-dc738290c4b1`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. When the handle of an incoming Tx Request matches this, the TxDynamicPart is multiplexed according to the corresponding IpduMSegments.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `37c53dab-5b16-46aa-80cd-eeac23b053db`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for this dynamic part I-PDU is used, i.e. the dynamic part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

########## 2. IpduMTxDynamicConfirmation

- **UUID**: `7505eec3-7047-4a0f-9e8a-891430382ce5`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxDynamicPduRef

- **UUID**: `2ffc37d5-0efa-48b1-8bea-51dd8ae1a018`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 16. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 17. IpduMTxStaticPart

**容器属性**:

- **UUID**: `519af9ba-66eb-4fa9-9b9d-36dcfcf9df26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of outgoing multiplexed lower layer I-PDU. If a static part is defined any transmission of the lower layer I-PDU will include I-PDU data provided by the static part. This is independent from the selector field value that shall be transmitted.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxStaticHandleId

- **UUID**: `0caaa019-2eb4-473a-9638-1f2f5f178fa6`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. If the handle of an incoming Tx Request matches this, the TxStaticPart is multiplexed according to the corresponding IpduMSegments and the send mode is honored.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `88d3dfb6-7143-4e5c-ad6e-dd355b4a5c26`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for the static part I-PDU is used, i.e. the static part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

########## 2. IpduMTxStaticConfirmation

- **UUID**: `01638e05-a1fc-4540-84fa-30e80a576521`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxStaticPduRef

- **UUID**: `d7ee9102-2b9f-4f80-b1f4-dafd3add511e`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the multiplexed Pdu's (static part, if exists) representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 18. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 4. IpduMContainedRxPdu

**容器属性**:

- **UUID**: `ECUC:23135174-a437-419a-9d97-d0c8a6da224d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMContainedRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration of a received contained Pdu.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. IpduMContainedPduHeaderId

- **UUID**: `ECUC:b2c8d44a-66f0-8b8e-46f4-c8c1d0191412`
- **参数名**: `IpduMContainedPduHeaderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Header Id which is part of the ContainerPdu when this ContainedPdu is inside.

######## 2. IpduMContainedPduOffset

- **UUID**: `ECUC:9d46e30a-1d3f-8303-3509-8be80c94c764`
- **参数名**: `IpduMContainedPduOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Static offset (in bytes) of the ContainedPdu.

######## 3. IpduMPduUpdateBitPosition

- **UUID**: `ECUC:845ed947-d78d-8d78-4d57-b62f10b3777c`
- **参数名**: `IpduMPduUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies where the PDU's Update-Bit is stored in the Container PDU (bit location of PDU's Update-Bit in the Container PDU).

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMContainedRxInContainerPduRef

- **UUID**: `ECUC:30e6206f-666f-4d8f-a66b-883ce64951f7`
- **引用名**: `IpduMContainedRxInContainerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `IpduMContainerRxPdu`
- **完整路径**: `/MICROSAR/IpduM/IpduMConfig/IpduMContainerRxPdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Optional reference to a container Pdu this contained Pdu may be transported in.

######## 2. IpduMContainedRxPduRef

- **UUID**: `ECUC:2c109a6f-b369-4e64-8aab-d16df021b5eb`
- **引用名**: `IpduMContainedRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Pdu which represents this ContainedPdu and is used for reception indication.

##### 5. IpduMContainedTxPdu

**容器属性**:

- **UUID**: `ECUC:791848d7-cbc2-4736-823a-c714e80fa697`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMContainedTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration of a sender ContainedPdu.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. IpduMContainedPduHeaderId

- **UUID**: `ECUC:08cdcbad-8e7b-912a-2b97-bf0e114e985c`
- **参数名**: `IpduMContainedPduHeaderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Header Id which is part of the ContainerPdu when this ContainedPdu is inside.

######## 2. IpduMContainedPduOffset

- **UUID**: `ECUC:f34bda6d-44ca-889f-19ac-82344dca4bae`
- **参数名**: `IpduMContainedPduOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Static offset (in bytes) of the ContainedPdu.

######## 3. IpduMContainedTxPduHandleId

- **UUID**: `ECUC:30a9f077-e171-4238-96c7-b2abdefe20cf`
- **参数名**: `IpduMContainedTxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Handle Id of the ContainedPdu.

######## 4. IpduMContainedTxPduPriority

- **UUID**: `ECUC:ceed8f53-b9f8-48f4-a35a-5c53db1580e1`
- **参数名**: `IpduMContainedTxPduPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines a priority of a ContainedTxPdu. 255 represents the lowest priority and 0 represent the highest priority.

######## 5. IpduMPduUpdateBitPosition

- **UUID**: `ECUC:da63d0aa-ff18-9314-31fa-ac7b51e8fbc6`
- **参数名**: `IpduMPduUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies where the PDU's Update-Bit is stored in the Container PDU (bit location of PDU's Update-Bit in the Container PDU).

####### BOOLEAN 类型参数

######## 1. IpduMContainedTxPduConfirmation

- **UUID**: `ECUC:ea74c379-a393-4df0-bd9c-2405c7d70434`
- **参数名**: `IpduMContainedTxPduConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This Parameter determines whether for this contained I-PDU a TxConfirmation shall be provided. If set to TRUE a TxConfirmation is issued. It is not used when an I-PDU is requested using the trigger transmit API.

####### FLOAT 类型参数

######## 1. IpduMContainedTxPduSendTimeout

- **UUID**: `ECUC:e6fac165-cc62-4ab5-94e1-2cec0609f5f3`
- **参数名**: `IpduMContainedTxPduSendTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines a ContainedPdu specific sender timeout which can reduce the ContainerPdu timer when this ContainedPdu is put inside the ContainerPdu.

If this parameter is omitted, the linked Container-PDU must have a SendTimeout configured.

The value 0 does not have special semantics here, 0 is a normal, valid value.

####### ENUMERATION 类型参数

######## 1. IpduMContainedTxPduCollectionSemantics

- **UUID**: `ECUC:241b7e86-021b-48ba-b29a-79b59768422a`
- **参数名**: `IpduMContainedTxPduCollectionSemantics`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_COLLECT_LAST_IS_BEST` (来源: Vector Informatik)
  - `IPDUM_COLLECT_QUEUED` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines whether this IpduMContainedTxPdu shall be collected using a last-is-best or queued semantics.

######## 2. IpduMContainedTxPduTrigger

- **UUID**: `ECUC:1fc45d53-28ef-48a4-8195-4922ec1935ea`
- **参数名**: `IpduMContainedTxPduTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_TRIGGER_ALWAYS` (来源: Vector Informatik)
  - `IPDUM_TRIGGER_NEVER` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines whether this Pdu triggers the sending of the ContainerPdu.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMContainedTxInContainerPduRef

- **UUID**: `ECUC:0a15c013-c0d4-417d-9674-76207d08a72a`
- **引用名**: `IpduMContainedTxInContainerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IpduMContainerTxPdu`
- **完整路径**: `/MICROSAR/IpduM/IpduMConfig/IpduMContainerTxPdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the container Pdu which this contained Pdu shall be collected in.

######## 2. IpduMContainedTxPduRef

- **UUID**: `ECUC:1b2057ec-907f-4bc7-9f34-25a9eef84053`
- **引用名**: `IpduMContainedTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Pdu which represents this ContainedPdu and is used for transmission.

##### 6. IpduMContainerRxPdu

**容器属性**:

- **UUID**: `ECUC:5d925ddf-12e3-4599-b270-042c31e381bb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMContainerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration of a receiver ContainerPdu which may collect several ContainedPdus.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. IpduMContainerQueueSize

- **UUID**: `ECUC:0bd46c1b-1938-859e-52eb-9f58b74213ec`
- **参数名**: `IpduMContainerQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines a local queue for handling of each ContainerPdu.

######## 2. IpduMContainerRxHandleId

- **UUID**: `ECUC:aa0c884d-6267-4829-9396-98b8fd5a1cad`
- **参数名**: `IpduMContainerRxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Handle Id used by the PduR for RxIndication.

####### ENUMERATION 类型参数

######## 1. IpduMContainerHeaderSize

- **UUID**: `ECUC:f6085257-2137-889a-5714-432746509801`
- **参数名**: `IpduMContainerHeaderSize`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_HEADERTYPE_LONG` (来源: Vector Informatik)
  - `IPDUM_HEADERTYPE_SHORT` (来源: Vector Informatik)
  - `IPDUM_HEADERTYPE_NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the layout of the header information (header id and length).

######## 2. IpduMContainerPduProcessing

- **UUID**: `ECUC:54dd7b87-c70e-4292-8fb0-d2248a0b7e19`
- **参数名**: `IpduMContainerPduProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `IPDUM_PROCESSING_IMMEDIATE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_PROCESSING_DEFERRED` (来源: Vector Informatik)
  - `IPDUM_PROCESSING_IMMEDIATE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines whether the handling of this ContainerPdu shall be done in the context of the caller (IMMEDIATE) or in the next IpduM main function (DEFERRED).

######## 3. IpduMContainerRxAcceptContainedPdu

- **UUID**: `ECUC:722a835c-4867-4f34-94e1-4936cec8948f`
- **参数名**: `IpduMContainerRxAcceptContainedPdu`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_ACCEPT_ALL` (来源: Vector Informatik)
  - `IPDUM_ACCEPT_CONFIGURED` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines for the received IpduMRxContainerPdu whether the list of referencing IpduMRxContainedPdus (via the reference IpduMRxContainedPduContainerRef) is a closed set.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMContainerRxPduRef

- **UUID**: `ECUC:f2caa5c2-e8b8-4fc2-b142-005df5ec6c44`
- **引用名**: `IpduMContainerRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Pdu which represents the container and is used for reception.

##### 7. IpduMContainerTxPdu

**容器属性**:

- **UUID**: `ECUC:05166e13-676a-4d11-857b-c0a25b5bf15a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMContainerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration of a transmitted container Pdu.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. IpduMContainerQueueSize

- **UUID**: `ECUC:b3587c4f-6dbf-8d16-25f7-5bcee0ba838b`
- **参数名**: `IpduMContainerQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines a local queue for handling of each ContainerPdu.

The actual queue length in the implementation is incremented by 1 as a performance optimization. So the current instance is within the queue and does not need additional copy instructions. The maximum value was lowered to 254 to enable this performance optimization.

######## 2. IpduMContainerTxHandleId

- **UUID**: `ECUC:efa3fff6-909e-44c5-8511-bf9555ed9dcf`
- **参数名**: `IpduMContainerTxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Handle Id used by the PduR for TxConfirmation and for TriggerTransmit of the ContainerPdu.

######## 3. IpduMContainerTxSizeThreshold

- **UUID**: `ECUC:a06d30c7-b0ce-4b1b-9cb1-9cb21b510de7`
- **参数名**: `IpduMContainerTxSizeThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the size threshold in bytes which, when exceeded, triggers the sending of the ContainerPdu although the maxium Pdu size (PduLength parameter of Pdu object)  has not been reached yet.

######## 4. IpduMUnusedAreasDefault

- **UUID**: `ECUC:27348714-d1c3-4091-98be-692839840e20`
- **参数名**: `IpduMUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: IpduM fills not updated areas of the Container PDU with this byte-pattern.

####### BOOLEAN 类型参数

######## 1. IpduMContainerTxFirstContainedPduTrigger

- **UUID**: `ECUC:2ed7ba6a-3bcf-4daa-9296-e4b8f3bbbf75`
- **参数名**: `IpduMContainerTxFirstContainedPduTrigger`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines if the transmission of this IpduMContainerTxPdu shall be requested right after the first IpduMContainedTxPdu was put into it.

####### FLOAT 类型参数

######## 1. IpduMContainerTxConfirmationTimeout

- **UUID**: `ECUC:fcf4eda4-4f81-4ee9-abe0-503bb347e758`
- **参数名**: `IpduMContainerTxConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This timeout (in seconds) defines the timeout period for monitoring the reception of the TxConfirmation. It is not used when an I-PDU is requested using the trigger transmit API.

######## 2. IpduMContainerTxSendTimeout

- **UUID**: `ECUC:9a4008f5-85c6-424a-9d51-5e7833214912`
- **参数名**: `IpduMContainerTxSendTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: When this timeout expires the ContainerPdu is triggered for sending. The respective timer is started when the first Pdu is put into the ContainerPdu.

####### ENUMERATION 类型参数

######## 1. IpduMContainerHeaderSize

- **UUID**: `ECUC:9d8c628b-75be-9012-2a1f-ff9d6fc907a0`
- **参数名**: `IpduMContainerHeaderSize`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_HEADERTYPE_LONG` (来源: Vector Informatik)
  - `IPDUM_HEADERTYPE_SHORT` (来源: Vector Informatik)
  - `IPDUM_HEADERTYPE_NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the layout of the header information (header id and length).

######## 2. IpduMContainerTxTriggerMode

- **UUID**: `ECUC:fe00aca6-2aa1-47c5-ac1b-c708b0a2da1c`
- **参数名**: `IpduMContainerTxTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IPDUM_DIRECT` (来源: Vector Informatik)
  - `IPDUM_TRIGGERTRANSMIT` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines whether this ContainerPdu is fetched via trigger transmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMContainerTxPduRef

- **UUID**: `ECUC:c60e1385-2617-4809-8f06-3165454aef0e`
- **引用名**: `IpduMContainerTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Pdu which represents the container and is used for transmission.

##### 8. IpduMRxPathway

**容器属性**:

- **UUID**: `d6a59454-e00d-42aa-8fce-ea57183abb6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxPathway`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines one lower layer I-PDU that is received from the network and resolved to multiple upper layer I-PDUs depending on the selector field value.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. IpduMRxIndication

**容器属性**:

- **UUID**: `957fe70d-c081-4872-ad43-4a455c13083c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxIndication`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Contains the configuration for incoming calls to the IpduM_RxIndication API.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMRxHandleId

- **UUID**: `1ad54562-ca2c-4776-abc6-2b8415640ec4`
- **参数名**: `IpduMRxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the I-PDU ID of the incoming I-PDU. If an incoming RxIndication's I-PDU ID matches this value then it is unpacked according to the specification in this container.

######### ENUMERATION 类型参数

########## 1. IpduMByteOrder

- **UUID**: `efb8ed48-6a62-420b-af4b-bff7033d0774`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BIG_ENDIAN`
  - `LITTLE_ENDIAN`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.
This is necessary because the positions are defined differently (LSB for little endian and MSB for big endian) based on endianness.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMRxIndicationPduRef

- **UUID**: `77d9f123-af11-402b-b55a-26458f1fa264`
- **引用名**: `IpduMRxIndicationPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the lower layer I-PDU that is processed and demultiplexed by the IpduM.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `77f52ec5-ee20-4382-8e0b-579fcb753441`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. If an incoming received I-PDU's selector field matches the IpduMRxSelectorValue of any of the dynamic parts, the new outgoing I-PDU for the dynamic part is de-multiplexed according to the corresponding dynamic IpduMSegment specification and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IpduMRxSelectorValue

- **UUID**: `4db5e83b-090c-4651-a3c5-f5ffee79a524`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the dynamic part that is transmitted within the received multiplexed I-PDU.
If the selector field value of the received multiplex I-PDU matches this value. It will be de-multiplexed according to the configuration in the parent IpduMRxDynamicPart container.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingDynamicPduRef

- **UUID**: `e7dc82d2-b76c-4e55-85a4-49ff27353685`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that is notified by the IpduM depending on the selector field value.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############## 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

######### 2. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

######### 3. IpduMRxStaticPart

**容器属性**:

- **UUID**: `7d20171e-1213-4dd1-ab59-073d5581fd57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of incoming lower layer I-PDU. If a static part is defined any reception of the lower layer I-PDU will cause the notification of the upper layer I-PDU representing the static part. This is independent from the selector field value.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingStaticPduRef

- **UUID**: `1947f98a-d4f0-41e6-8105-ba5a80bbe23b`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that notified by the IPDUM as static I-PDU part of each multiplexed I-PDU.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############## 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 4. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `cc327dfc-37dd-4288-a5b1-7ce3f1070eb9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the location and the length of the selector field that is used to identify the dynamic part of each multiplexed I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `a2926cdc-e3a9-4144-9971-7764d637299b`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

############ 2. IpduMSelectorFieldPosition

- **UUID**: `eabf5332-45e6-4867-8e32-1283c0ff11ee`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.
Bits are numbered ascending, bytes depending on the endianness defined in IpduMByteOrder.

####### 2. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `77f52ec5-ee20-4382-8e0b-579fcb753441`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. If an incoming received I-PDU's selector field matches the IpduMRxSelectorValue of any of the dynamic parts, the new outgoing I-PDU for the dynamic part is de-multiplexed according to the corresponding dynamic IpduMSegment specification and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IpduMRxSelectorValue

- **UUID**: `4db5e83b-090c-4651-a3c5-f5ffee79a524`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the dynamic part that is transmitted within the received multiplexed I-PDU.
If the selector field value of the received multiplex I-PDU matches this value. It will be de-multiplexed according to the configuration in the parent IpduMRxDynamicPart container.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingDynamicPduRef

- **UUID**: `e7dc82d2-b76c-4e55-85a4-49ff27353685`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that is notified by the IpduM depending on the selector field value.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

####### 3. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

########## 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

####### 4. IpduMRxStaticPart

**容器属性**:

- **UUID**: `7d20171e-1213-4dd1-ab59-073d5581fd57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of incoming lower layer I-PDU. If a static part is defined any reception of the lower layer I-PDU will cause the notification of the upper layer I-PDU representing the static part. This is independent from the selector field value.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingStaticPduRef

- **UUID**: `1947f98a-d4f0-41e6-8105-ba5a80bbe23b`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that notified by the IPDUM as static I-PDU part of each multiplexed I-PDU.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 5. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

########## 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 6. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `cc327dfc-37dd-4288-a5b1-7ce3f1070eb9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the location and the length of the selector field that is used to identify the dynamic part of each multiplexed I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `a2926cdc-e3a9-4144-9971-7764d637299b`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

########## 2. IpduMSelectorFieldPosition

- **UUID**: `eabf5332-45e6-4867-8e32-1283c0ff11ee`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.
Bits are numbered ascending, bytes depending on the endianness defined in IpduMByteOrder.

##### 9. IpduMRxIndication

**容器属性**:

- **UUID**: `957fe70d-c081-4872-ad43-4a455c13083c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxIndication`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Contains the configuration for incoming calls to the IpduM_RxIndication API.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMRxHandleId

- **UUID**: `1ad54562-ca2c-4776-abc6-2b8415640ec4`
- **参数名**: `IpduMRxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the I-PDU ID of the incoming I-PDU. If an incoming RxIndication's I-PDU ID matches this value then it is unpacked according to the specification in this container.

####### ENUMERATION 类型参数

######## 1. IpduMByteOrder

- **UUID**: `efb8ed48-6a62-420b-af4b-bff7033d0774`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BIG_ENDIAN`
  - `LITTLE_ENDIAN`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.
This is necessary because the positions are defined differently (LSB for little endian and MSB for big endian) based on endianness.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMRxIndicationPduRef

- **UUID**: `77d9f123-af11-402b-b55a-26458f1fa264`
- **引用名**: `IpduMRxIndicationPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the lower layer I-PDU that is processed and demultiplexed by the IpduM.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `77f52ec5-ee20-4382-8e0b-579fcb753441`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. If an incoming received I-PDU's selector field matches the IpduMRxSelectorValue of any of the dynamic parts, the new outgoing I-PDU for the dynamic part is de-multiplexed according to the corresponding dynamic IpduMSegment specification and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IpduMRxSelectorValue

- **UUID**: `4db5e83b-090c-4651-a3c5-f5ffee79a524`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the dynamic part that is transmitted within the received multiplexed I-PDU.
If the selector field value of the received multiplex I-PDU matches this value. It will be de-multiplexed according to the configuration in the parent IpduMRxDynamicPart container.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingDynamicPduRef

- **UUID**: `e7dc82d2-b76c-4e55-85a4-49ff27353685`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that is notified by the IpduM depending on the selector field value.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

####### 2. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

########## 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

####### 3. IpduMRxStaticPart

**容器属性**:

- **UUID**: `7d20171e-1213-4dd1-ab59-073d5581fd57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of incoming lower layer I-PDU. If a static part is defined any reception of the lower layer I-PDU will cause the notification of the upper layer I-PDU representing the static part. This is independent from the selector field value.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingStaticPduRef

- **UUID**: `1947f98a-d4f0-41e6-8105-ba5a80bbe23b`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that notified by the IPDUM as static I-PDU part of each multiplexed I-PDU.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

############ 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 4. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

########## 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 5. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `cc327dfc-37dd-4288-a5b1-7ce3f1070eb9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the location and the length of the selector field that is used to identify the dynamic part of each multiplexed I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `a2926cdc-e3a9-4144-9971-7764d637299b`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

########## 2. IpduMSelectorFieldPosition

- **UUID**: `eabf5332-45e6-4867-8e32-1283c0ff11ee`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.
Bits are numbered ascending, bytes depending on the endianness defined in IpduMByteOrder.

##### 10. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `77f52ec5-ee20-4382-8e0b-579fcb753441`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. If an incoming received I-PDU's selector field matches the IpduMRxSelectorValue of any of the dynamic parts, the new outgoing I-PDU for the dynamic part is de-multiplexed according to the corresponding dynamic IpduMSegment specification and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IpduMRxSelectorValue

- **UUID**: `4db5e83b-090c-4651-a3c5-f5ffee79a524`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the dynamic part that is transmitted within the received multiplexed I-PDU.
If the selector field value of the received multiplex I-PDU matches this value. It will be de-multiplexed according to the configuration in the parent IpduMRxDynamicPart container.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMOutgoingDynamicPduRef

- **UUID**: `e7dc82d2-b76c-4e55-85a4-49ff27353685`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that is notified by the IpduM depending on the selector field value.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

########## 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

##### 11. IpduMSegment

**容器属性**:

- **UUID**: `fc8af20c-163a-41fa-a600-262487336526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied to the same location within the upper layer I-PDU.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSegmentLength

- **UUID**: `f3c5a6eb-203b-4532-bceb-aa570976cf70`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

######## 2. IpduMSegmentPosition

- **UUID**: `7e2e37e4-08ab-456c-9894-e4fd86c38c05`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.
Bits within a byte are always numbered in ascending order. Bytes are ordered based on IpduMByteOrder.

##### 12. IpduMRxStaticPart

**容器属性**:

- **UUID**: `7d20171e-1213-4dd1-ab59-073d5581fd57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of incoming lower layer I-PDU. If a static part is defined any reception of the lower layer I-PDU will cause the notification of the upper layer I-PDU representing the static part. This is independent from the selector field value.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMOutgoingStaticPduRef

- **UUID**: `1947f98a-d4f0-41e6-8105-ba5a80bbe23b`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the upper layer I-PDU that notified by the IPDUM as static I-PDU part of each multiplexed I-PDU.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

########## 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 13. IpduMSegment

**容器属性**:

- **UUID**: `f2e5ca55-f827-483c-b969-ac00168fa588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSegmentLength

- **UUID**: `0fef652a-3d4f-464a-8990-fc008bf1f2af`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment [bit].

######## 2. IpduMSegmentPosition

- **UUID**: `ca7a5f6a-cd62-4627-9faa-abba29965e5a`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 14. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `cc327dfc-37dd-4288-a5b1-7ce3f1070eb9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Defines the location and the length of the selector field that is used to identify the dynamic part of each multiplexed I-PDU.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSelectorFieldLength

- **UUID**: `a2926cdc-e3a9-4144-9971-7764d637299b`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

######## 2. IpduMSelectorFieldPosition

- **UUID**: `eabf5332-45e6-4867-8e32-1283c0ff11ee`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.
Bits are numbered ascending, bytes depending on the endianness defined in IpduMByteOrder.

##### 15. IpduMTxPathway

**容器属性**:

- **UUID**: `a860e300-7600-4a8d-80d7-a017f5f9f612`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxPathway`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines one lower layer I-PDU that is assembled from multiple upper layer I-PDUs depending on the selector field value.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. IpduMTxRequest

**容器属性**:

- **UUID**: `a0fa246f-5b36-4e22-82b4-998ad2ef96d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxRequest`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This is used to specify the configuration for Transmit requests.

There will one instance of this container for each I-PDU that can be requested for transmission (the outgoing I-PDUs) by the IpduM.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. IpduMIPduUnusedAreasDefault

- **UUID**: `74d2a1f2-f593-40e4-9905-c1e0a48730cc`
- **参数名**: `IpduMIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IPDUM  module fills unused areas of a transmitted multiplexed I-PDU with this bit-pattern.
If this attribute is undefined unused areas are not initialized any may have an arbitrary value

########## 2. IpduMTxConfirmationPduId

- **UUID**: `b82c12be-4a9b-450c-a4e7-bbdc15cf44d3`
- **参数名**: `IpduMTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The handle Id used by the lower layer to identify this IPDUM I-PDU during TriggerTransmit and TxConfirmation calls.

######### FLOAT 类型参数

########## 1. IpduMTxConfirmationTimeout

- **UUID**: `cf596dbd-7ba4-4d59-b537-e344bb587d81`
- **参数名**: `IpduMTxConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the timeout time for monitoring the TxConfirmation call from the lower layer (i.e. the transmission of the corresponding multiplex I-PDU occured).
Parameter is not used for lower layer I-PDU that use the TriggerTransmit API.

######### ENUMERATION 类型参数

########## 1. IpduMByteOrder

- **UUID**: `09e480a4-cdc7-46df-826d-dba06b30152d`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

########## 2. IpduMTxTriggerMode

- **UUID**: `06a7e279-fb78-4380-9334-910d5b3ec857`
- **参数名**: `IpduMTxTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DYNAMIC_PART_TRIGGER`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DYNAMIC_PART_TRIGGER`
  - `NONE`
  - `STATIC_OR_DYNAMIC_PART_TRIGGER`
  - `STATIC_PART_TRIGGER`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the upper layer transmission event that causes the transmission of the multiplexed I-PDU through the lower layer.
	NONE: do not trigger transmission on upper layer transmission events
	STATIC_PART_TRIGGER: trigger transmission if the static part I-PDU is transmitted to IpduM
	DYNAMIC_PART_TRIGGER: trigger transmission if the dynamic part I-PDU is transmitted to IpduM
	STATIC_OR_DYNAMIC_PART_TRIGGER: trigger transmission if the static or dynamic part I-PDU is transmitted to IpduM

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMInitialDynamicPart

- **UUID**: `04957cef-24c7-4006-9391-5bba02bb5300`
- **引用名**: `IpduMInitialDynamicPart`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IpduMTxDynamicPart`
- **完整路径**: `/AUTOSAR/EcucDefs/IpduM/IpduMConfig/IpduMTxPathway/IpduMTxRequest/IpduMTxDynamicPart`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the dynamic part that shall be used to initialize this multiplexed TX-I-PDU. This part is used as the dynamic part in case of a static part first being triggered for transmission after ECU initialization, i.e. no last transmitted dynamic part is available yet.

########## 2. IpduMOutgoingPduRef

- **UUID**: `baaca0dd-c423-48ec-8e0a-222b0f11806b`
- **引用名**: `IpduMOutgoingPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to I-Pdu representation in the ECU Configuration Description exchange file.
When the outgoing I-PDU is sent this is the I-PDU ID to give it. It is the IPDUM  I-PDU ID of the assembled I-PDU.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `1ce1c9d6-379f-42ef-95da-d37d013bf4f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `3d638d53-14fd-41b0-901e-9aea97b70f4f`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

############ 2. IpduMSelectorFieldPosition

- **UUID**: `6ffe9e06-37e6-42e5-a39b-cc184e3ab6c6`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

######### 2. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `0b5e3db8-89b1-43ee-8fec-97b4e27bddeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honored. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxDynamicHandleId

- **UUID**: `b0c7d66e-9580-41d9-89e1-dc738290c4b1`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. When the handle of an incoming Tx Request matches this, the TxDynamicPart is multiplexed according to the corresponding IpduMSegments.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `37c53dab-5b16-46aa-80cd-eeac23b053db`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for this dynamic part I-PDU is used, i.e. the dynamic part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

############ 2. IpduMTxDynamicConfirmation

- **UUID**: `7505eec3-7047-4a0f-9e8a-891430382ce5`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxDynamicPduRef

- **UUID**: `2ffc37d5-0efa-48b1-8bea-51dd8ae1a018`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 3. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 4. IpduMTxStaticPart

**容器属性**:

- **UUID**: `519af9ba-66eb-4fa9-9b9d-36dcfcf9df26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of outgoing multiplexed lower layer I-PDU. If a static part is defined any transmission of the lower layer I-PDU will include I-PDU data provided by the static part. This is independent from the selector field value that shall be transmitted.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxStaticHandleId

- **UUID**: `0caaa019-2eb4-473a-9638-1f2f5f178fa6`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. If the handle of an incoming Tx Request matches this, the TxStaticPart is multiplexed according to the corresponding IpduMSegments and the send mode is honored.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `88d3dfb6-7143-4e5c-ad6e-dd355b4a5c26`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for the static part I-PDU is used, i.e. the static part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

############ 2. IpduMTxStaticConfirmation

- **UUID**: `01638e05-a1fc-4540-84fa-30e80a576521`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxStaticPduRef

- **UUID**: `d7ee9102-2b9f-4f80-b1f4-dafd3add511e`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the multiplexed Pdu's (static part, if exists) representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 2. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `1ce1c9d6-379f-42ef-95da-d37d013bf4f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `3d638d53-14fd-41b0-901e-9aea97b70f4f`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

########## 2. IpduMSelectorFieldPosition

- **UUID**: `6ffe9e06-37e6-42e5-a39b-cc184e3ab6c6`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

####### 3. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `0b5e3db8-89b1-43ee-8fec-97b4e27bddeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honored. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxDynamicHandleId

- **UUID**: `b0c7d66e-9580-41d9-89e1-dc738290c4b1`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. When the handle of an incoming Tx Request matches this, the TxDynamicPart is multiplexed according to the corresponding IpduMSegments.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `37c53dab-5b16-46aa-80cd-eeac23b053db`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for this dynamic part I-PDU is used, i.e. the dynamic part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

########## 2. IpduMTxDynamicConfirmation

- **UUID**: `7505eec3-7047-4a0f-9e8a-891430382ce5`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxDynamicPduRef

- **UUID**: `2ffc37d5-0efa-48b1-8bea-51dd8ae1a018`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 4. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 5. IpduMTxStaticPart

**容器属性**:

- **UUID**: `519af9ba-66eb-4fa9-9b9d-36dcfcf9df26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of outgoing multiplexed lower layer I-PDU. If a static part is defined any transmission of the lower layer I-PDU will include I-PDU data provided by the static part. This is independent from the selector field value that shall be transmitted.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxStaticHandleId

- **UUID**: `0caaa019-2eb4-473a-9638-1f2f5f178fa6`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. If the handle of an incoming Tx Request matches this, the TxStaticPart is multiplexed according to the corresponding IpduMSegments and the send mode is honored.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `88d3dfb6-7143-4e5c-ad6e-dd355b4a5c26`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for the static part I-PDU is used, i.e. the static part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

########## 2. IpduMTxStaticConfirmation

- **UUID**: `01638e05-a1fc-4540-84fa-30e80a576521`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxStaticPduRef

- **UUID**: `d7ee9102-2b9f-4f80-b1f4-dafd3add511e`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the multiplexed Pdu's (static part, if exists) representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 6. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 16. IpduMTxRequest

**容器属性**:

- **UUID**: `a0fa246f-5b36-4e22-82b4-998ad2ef96d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxRequest`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This is used to specify the configuration for Transmit requests.

There will one instance of this container for each I-PDU that can be requested for transmission (the outgoing I-PDUs) by the IpduM.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. IpduMIPduUnusedAreasDefault

- **UUID**: `74d2a1f2-f593-40e4-9905-c1e0a48730cc`
- **参数名**: `IpduMIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IPDUM  module fills unused areas of a transmitted multiplexed I-PDU with this bit-pattern.
If this attribute is undefined unused areas are not initialized any may have an arbitrary value

######## 2. IpduMTxConfirmationPduId

- **UUID**: `b82c12be-4a9b-450c-a4e7-bbdc15cf44d3`
- **参数名**: `IpduMTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The handle Id used by the lower layer to identify this IPDUM I-PDU during TriggerTransmit and TxConfirmation calls.

####### FLOAT 类型参数

######## 1. IpduMTxConfirmationTimeout

- **UUID**: `cf596dbd-7ba4-4d59-b537-e344bb587d81`
- **参数名**: `IpduMTxConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the timeout time for monitoring the TxConfirmation call from the lower layer (i.e. the transmission of the corresponding multiplex I-PDU occured).
Parameter is not used for lower layer I-PDU that use the TriggerTransmit API.

####### ENUMERATION 类型参数

######## 1. IpduMByteOrder

- **UUID**: `09e480a4-cdc7-46df-826d-dba06b30152d`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

######## 2. IpduMTxTriggerMode

- **UUID**: `06a7e279-fb78-4380-9334-910d5b3ec857`
- **参数名**: `IpduMTxTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DYNAMIC_PART_TRIGGER`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DYNAMIC_PART_TRIGGER`
  - `NONE`
  - `STATIC_OR_DYNAMIC_PART_TRIGGER`
  - `STATIC_PART_TRIGGER`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the upper layer transmission event that causes the transmission of the multiplexed I-PDU through the lower layer.
	NONE: do not trigger transmission on upper layer transmission events
	STATIC_PART_TRIGGER: trigger transmission if the static part I-PDU is transmitted to IpduM
	DYNAMIC_PART_TRIGGER: trigger transmission if the dynamic part I-PDU is transmitted to IpduM
	STATIC_OR_DYNAMIC_PART_TRIGGER: trigger transmission if the static or dynamic part I-PDU is transmitted to IpduM

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMInitialDynamicPart

- **UUID**: `04957cef-24c7-4006-9391-5bba02bb5300`
- **引用名**: `IpduMInitialDynamicPart`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IpduMTxDynamicPart`
- **完整路径**: `/AUTOSAR/EcucDefs/IpduM/IpduMConfig/IpduMTxPathway/IpduMTxRequest/IpduMTxDynamicPart`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the dynamic part that shall be used to initialize this multiplexed TX-I-PDU. This part is used as the dynamic part in case of a static part first being triggered for transmission after ECU initialization, i.e. no last transmitted dynamic part is available yet.

######## 2. IpduMOutgoingPduRef

- **UUID**: `baaca0dd-c423-48ec-8e0a-222b0f11806b`
- **引用名**: `IpduMOutgoingPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to I-Pdu representation in the ECU Configuration Description exchange file.
When the outgoing I-PDU is sent this is the I-PDU ID to give it. It is the IPDUM  I-PDU ID of the assembled I-PDU.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `1ce1c9d6-379f-42ef-95da-d37d013bf4f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `3d638d53-14fd-41b0-901e-9aea97b70f4f`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

########## 2. IpduMSelectorFieldPosition

- **UUID**: `6ffe9e06-37e6-42e5-a39b-cc184e3ab6c6`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

####### 2. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `0b5e3db8-89b1-43ee-8fec-97b4e27bddeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honored. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxDynamicHandleId

- **UUID**: `b0c7d66e-9580-41d9-89e1-dc738290c4b1`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. When the handle of an incoming Tx Request matches this, the TxDynamicPart is multiplexed according to the corresponding IpduMSegments.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `37c53dab-5b16-46aa-80cd-eeac23b053db`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for this dynamic part I-PDU is used, i.e. the dynamic part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

########## 2. IpduMTxDynamicConfirmation

- **UUID**: `7505eec3-7047-4a0f-9e8a-891430382ce5`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxDynamicPduRef

- **UUID**: `2ffc37d5-0efa-48b1-8bea-51dd8ae1a018`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 3. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 4. IpduMTxStaticPart

**容器属性**:

- **UUID**: `519af9ba-66eb-4fa9-9b9d-36dcfcf9df26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of outgoing multiplexed lower layer I-PDU. If a static part is defined any transmission of the lower layer I-PDU will include I-PDU data provided by the static part. This is independent from the selector field value that shall be transmitted.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxStaticHandleId

- **UUID**: `0caaa019-2eb4-473a-9638-1f2f5f178fa6`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. If the handle of an incoming Tx Request matches this, the TxStaticPart is multiplexed according to the corresponding IpduMSegments and the send mode is honored.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `88d3dfb6-7143-4e5c-ad6e-dd355b4a5c26`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for the static part I-PDU is used, i.e. the static part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

########## 2. IpduMTxStaticConfirmation

- **UUID**: `01638e05-a1fc-4540-84fa-30e80a576521`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxStaticPduRef

- **UUID**: `d7ee9102-2b9f-4f80-b1f4-dafd3add511e`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the multiplexed Pdu's (static part, if exists) representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 5. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 17. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `1ce1c9d6-379f-42ef-95da-d37d013bf4f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSelectorFieldLength

- **UUID**: `3d638d53-14fd-41b0-901e-9aea97b70f4f`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field [bit].

######## 2. IpduMSelectorFieldPosition

- **UUID**: `6ffe9e06-37e6-42e5-a39b-cc184e3ab6c6`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

##### 18. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `0b5e3db8-89b1-43ee-8fec-97b4e27bddeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honored. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. IpduMTxDynamicHandleId

- **UUID**: `b0c7d66e-9580-41d9-89e1-dc738290c4b1`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. When the handle of an incoming Tx Request matches this, the TxDynamicPart is multiplexed according to the corresponding IpduMSegments.

####### BOOLEAN 类型参数

######## 1. IpduMJitUpdate

- **UUID**: `37c53dab-5b16-46aa-80cd-eeac23b053db`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for this dynamic part I-PDU is used, i.e. the dynamic part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

######## 2. IpduMTxDynamicConfirmation

- **UUID**: `7505eec3-7047-4a0f-9e8a-891430382ce5`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMTxDynamicPduRef

- **UUID**: `2ffc37d5-0efa-48b1-8bea-51dd8ae1a018`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 19. IpduMSegment

**容器属性**:

- **UUID**: `475d7506-be7b-4756-ab72-36e0f80c58b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSegmentLength

- **UUID**: `44985646-cbb6-42c2-91d4-b990037a1d7b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

######## 2. IpduMSegmentPosition

- **UUID**: `ac0ab759-68f0-4dd3-b20a-aac90be2bf47`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 20. IpduMTxStaticPart

**容器属性**:

- **UUID**: `519af9ba-66eb-4fa9-9b9d-36dcfcf9df26`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional static part of outgoing multiplexed lower layer I-PDU. If a static part is defined any transmission of the lower layer I-PDU will include I-PDU data provided by the static part. This is independent from the selector field value that shall be transmitted.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. IpduMTxStaticHandleId

- **UUID**: `0caaa019-2eb4-473a-9638-1f2f5f178fa6`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This is the handle id of a requested transmit. If the handle of an incoming Tx Request matches this, the TxStaticPart is multiplexed according to the corresponding IpduMSegments and the send mode is honored.

####### BOOLEAN 类型参数

######## 1. IpduMJitUpdate

- **UUID**: `88d3dfb6-7143-4e5c-ad6e-dd355b4a5c26`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be cleared correctly.

If configured to false, the data currently present in the IpduM's buffer for the static part I-PDU is used, i.e. the static part that was transmitted last. This way, transmissions may be on the bus faster, depending on configuration.

Jit update can be activated independently from the lower layer.

######## 2. IpduMTxStaticConfirmation

- **UUID**: `01638e05-a1fc-4540-84fa-30e80a576521`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission of the multiplexed I-PDU by the lower layer.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMTxStaticPduRef

- **UUID**: `d7ee9102-2b9f-4f80-b1f4-dafd3add511e`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the multiplexed Pdu's (static part, if exists) representation in the ECU Configuration Description exchange file to be transmitted.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 21. IpduMSegment

**容器属性**:

- **UUID**: `77aa02d9-aebf-424b-80b6-69eb3411b919`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Defines the location and the length of a segment that is used to describe the composition of a multiplexed I-PDU for one selector field value. The data area that is covered by the configured segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied to the same location within the upper layer I-PDU.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSegmentLength

- **UUID**: `94284215-42f5-4a7b-ad85-c5ebec6d69d7`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

######## 2. IpduMSegmentPosition

- **UUID**: `779ca2ac-9c79-49a0-a26a-26a6cd31d90f`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 22. IpduMPublishedInformation

**容器属性**:

- **UUID**: `825c8a94-339f-4d5b-961c-e9595984708a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMPublishedInformation`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Additional published parameters not covered by CommonPublishedInformation container. Note that these parameters do not have any configuration class setting, since they are published information.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. IpduMRxDirectComInvocation

- **UUID**: `3dd55b63-078f-47d7-8918-2de6f72538b3`
- **参数名**: `IpduMRxDirectComInvocation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD-LOADABLE
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD-SELECTABLE
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: If set to TRUE the methods Com_RxIndication and Com_TriggerTransmit are invocated directly without using the PduR as intermediate module. This is required by the AUTOSAR requirement IPDUM140.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **IpduM_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **IpduM**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **IpduM_Pre**
2. **IpduM_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. IpduM_Impl

- **UUID**: `36014e0b-182e-4a59-bacf-15c80eacece9`
- **实现名称**: `IpduM_Impl`
- **编程语言**: C
- **软件版本**: 13.02.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.01
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. IpduM_Pre

- **UUID**: `6b85cb88-157c-434d-9f6a-e40a4a56e4d5`
- **配置名称**: `IpduM_Pre`
- **定义引用**: `/MICROSAR/IpduM`

### 2. IpduM_Rec

- **UUID**: `9385f182-d7d4-43b1-b49a-7fa08fbc4ef1`
- **配置名称**: `IpduM_Rec`
- **定义引用**: `/MICROSAR/IpduM`
