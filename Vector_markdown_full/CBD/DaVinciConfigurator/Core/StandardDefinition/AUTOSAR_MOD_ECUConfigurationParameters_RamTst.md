# RamTst - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:31

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [RamTst](#ramtst)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. RamTst

#### 基本信息

- **UUID**: `ECUC:c41e9d3e-2da8-4985-a0ad-283ad8661088`
- **模块名称**: `RamTst`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the RamTst module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. RamTstCommon

**容器属性**:

- **UUID**: `ECUC:8e3b9850-bbd7-415a-a5bb-e6e4962cc5da`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstCommon`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds a list of all available functions in the RamTst module.  Each function is turned ON or OFF before compiling so that only the desired functions and test algorithms are in the compiled code.

###### 参数配置

此容器包含 **16** 个参数：

####### BOOLEAN 类型参数

######## 1. RamTstAllowApi

- **UUID**: `ECUC:16d97fa1-5ab2-41a9-af8c-3cda57200b97`
- **参数名**: `RamTstAllowApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function "RamTst_Allow".

######## 2. RamTstChangeNumOfTestedCellsApi

- **UUID**: `ECUC:67b4eef0-edc6-4494-9520-88892daafa0c`
- **参数名**: `RamTstChangeNumOfTestedCellsApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function "RamTst_ChangeNumberOfTestedCells".

######## 3. RamTstDevErrorDetect

- **UUID**: `ECUC:93c7f35b-d732-421e-b9fb-4b1dcb8d2b14`
- **参数名**: `RamTstDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the development error tracer (DET)

######## 4. RamTstGetAlgParamsApi

- **UUID**: `ECUC:121a2fc3-d8e6-487c-aec7-2de919158616`
- **参数名**: `RamTstGetAlgParamsApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function "RamTst_GetAlgParams".

######## 5. RamTstGetExecutionStatusApi

- **UUID**: `ECUC:ce59a5d7-75da-4e29-ae79-682dbf67224e`
- **参数名**: `RamTstGetExecutionStatusApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function

######## 6. RamTstGetNumberOfTestedCellsApi

- **UUID**: `ECUC:2c64f7c8-4708-445b-b554-59cf1ed50d00`
- **参数名**: `RamTstGetNumberOfTestedCellsApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function "RamTst_GetNumberOfTestedCells".

######## 7. RamTstGetTestAlgorithmApi

- **UUID**: `ECUC:22e5162a-cb96-4587-ae82-d484e700063b`
- **参数名**: `RamTstGetTestAlgorithmApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function

######## 8. RamTstGetTestResultApi

- **UUID**: `ECUC:1cf74528-d6b7-427e-bdef-5e5bc20a272d`
- **参数名**: `RamTstGetTestResultApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function

######## 9. RamTstGetTestResultPerBlockApi

- **UUID**: `ECUC:d498d99f-687c-4c3e-aee3-7dcb64361ceb`
- **参数名**: `RamTstGetTestResultPerBlockApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function

######## 10. RamTstGetVersionInfoApi

- **UUID**: `ECUC:2b74d931-78c0-46ec-9f62-34fa7cbdec9c`
- **参数名**: `RamTstGetVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function

######## 11. RamTstResumeApi

- **UUID**: `ECUC:53eb56f0-9d37-4896-a0a2-f8ed5386f467`
- **参数名**: `RamTstResumeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function "RamTst_Resume".

######## 12. RamTstRunFullTestApi

- **UUID**: `ECUC:7ac6372f-f153-4355-82cc-681d17b7f103`
- **参数名**: `RamTstRunFullTestApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function

######## 13. RamTstRunPartialTestApi

- **UUID**: `ECUC:d16c5d80-6a90-45d6-85b1-e625962a5345`
- **参数名**: `RamTstRunPartialTestApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function

######## 14. RamTstSelectAlgParamsApi

- **UUID**: `ECUC:bf32a854-b733-4de2-b7bc-4b4828533715`
- **参数名**: `RamTstSelectAlgParamsApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function "RamTst_SelectAlgParams".

######## 15. RamTstStopApi

- **UUID**: `ECUC:e8ffd34d-8e36-4485-b40c-985cff41cc2d`
- **参数名**: `RamTstStopApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function

######## 16. RamTstSuspendApi

- **UUID**: `ECUC:7a003020-da8b-4bc7-8833-d53d520c82be`
- **参数名**: `RamTstSuspendApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to disable / enable the function "RamTst_Suspend".

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. RamTstAlgorithms

**容器属性**:

- **UUID**: `ECUC:62eb25f3-28ac-452e-a2fa-0f92357c16a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstAlgorithms`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds all of the available test algorithms for the specific microcontroller.  Each test algorithm is selected ON or OFF before compiling so that only the desired test algorithms are in the compiled code.

######## 参数配置

此容器包含 **6** 个参数：

######### BOOLEAN 类型参数

########## 1. RamTstAbrahamTestSelected

- **UUID**: `ECUC:03482ab8-281d-4bfb-ae2d-fd63631d8108`
- **参数名**: `RamTstAbrahamTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the Abraham Test ON or OFF

########## 2. RamTstCheckerboardTestSelected

- **UUID**: `ECUC:0f5c4e78-46da-40cf-a1c7-11bce1d9263f`
- **参数名**: `RamTstCheckerboardTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the Checkerboard Test ON or OFF

########## 3. RamTstGalpatTestSelected

- **UUID**: `ECUC:090daeed-f256-425a-8e8f-be78873010f1`
- **参数名**: `RamTstGalpatTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the Galpat Test ON or OFF

########## 4. RamTstMarchTestSelected

- **UUID**: `ECUC:3582c79a-0327-4966-8752-343657127d47`
- **参数名**: `RamTstMarchTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the March Test ON or OFF

########## 5. RamTstTranspGalpatTestSelected

- **UUID**: `ECUC:94098234-bf83-41a3-84e4-f233699940b5`
- **参数名**: `RamTstTranspGalpatTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the Transparent Galpat Test ON or OFF

########## 6. RamTstWalkPathTestSelected

- **UUID**: `ECUC:f58faded-f154-4097-bfab-f56397d80138`
- **参数名**: `RamTstWalkPathTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the Walking Path Test ON or OFF

####### 2. RamTstConfigParams

**容器属性**:

- **UUID**: `ECUC:f21793ef-75e0-4393-b885-e5580bc5e76f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstConfigParams`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters which are set at pre-compile or link time.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. RamTstDefaultAlgParamsId

- **UUID**: `ECUC:06024431-c473-4eca-9fc7-cb09b2c469a0`
- **参数名**: `RamTstDefaultAlgParamsId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier for the default "RamTstAlgParams" valid after the "RamTst_Init(..)" function. It is the initial value for a RAM variable which could be changed by the function "RamTst_SelectAlgParams".

########## 2. RamTstMinNumberOfTestedCells

- **UUID**: `ECUC:b5bda6a2-ef40-4cbd-b1b2-0798c4470c9b`
- **参数名**: `RamTstMinNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum number of tested cells for one cyle of a background test, as defined by implementer.

########## 3. RamTstNumberOfAlgParamSets

- **UUID**: `ECUC:657cca5b-020d-4d2f-8f3c-72fb031dc992`
- **参数名**: `RamTstNumberOfAlgParamSets`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of configured parameter sets for the available test algorithms.

######### FUNCTION-NAME 类型参数

########## 1. RamTstTestCompletedNotification

- **UUID**: `ECUC:c1358c78-a1a1-4f16-a6da-7ab1912eca98`
- **参数名**: `RamTstTestCompletedNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This function will be called from abackground test after finishing the RAM test without an error.

########## 2. RamTstTestErrorNotification

- **UUID**: `ECUC:a1575dfa-04a7-496c-bb71-d5dbf722f0cc`
- **参数名**: `RamTstTestErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This function will be called from a background test if an error occurs during the RAM test.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. RamTstAlgParams

**容器属性**:

- **UUID**: `ECUC:72143fb4-1c83-44dc-8753-282521328089`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstAlgParams`
- **多重性**: [1..255]
- **多配置容器**: false

**容器描述**:

This container holds parameters for configuring an algorithm.  For each algorithm selected in the RamTst_Algorithms container there can be one or more RamTstAlgParams containers. The multiplicity of the included container RamTstBlockParams depends on the number of separate blocks of RAM which are defined for the particular test configuration.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. RamTstAlgParamsId

- **UUID**: `ECUC:ee97557e-a517-4dc6-a63d-e47756d5572f`
- **参数名**: `RamTstAlgParamsId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier by which this RamTstAlgParams set can be selected.

############ 2. RamTstExtNumberOfTestedCells

- **UUID**: `ECUC:733eb7c6-c2b1-4d00-9a53-564d38e9565f`
- **参数名**: `RamTstExtNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the absolute maximum value for the number of cells that NUMBER_OF_TESTED_CELLS and MAX_NUMBER_OF_TESTED_CELLS can be.

############ 3. RamTstMaxNumberOfTestedCells

- **UUID**: `ECUC:ed2796ab-085b-470c-b351-095568a161f2`
- **参数名**: `RamTstMaxNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the maximum value for the number of cells that can be tested in one cycle of a background test.

############ 4. RamTstNumberOfBlocks

- **UUID**: `ECUC:2e0f071e-2902-4850-a181-728a84d916b6`
- **参数名**: `RamTstNumberOfBlocks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of RAM blocks configured using the container

############ 5. RamTstNumberOfTestedCells

- **UUID**: `ECUC:8ba7b460-0266-4e5f-816d-0d5aa100dfa7`
- **参数名**: `RamTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the initial value for a RAM variable, which can be changed by the function "RamTst_ChangeNumberOfTestedCells"

########### ENUMERATION 类型参数

############ 1. RamTstAlgorithm

- **UUID**: `ECUC:c7ffb64f-2076-45ab-83c3-8c16a01d9a62`
- **参数名**: `RamTstAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTST_ABRAHAM_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_CHECKERBOARD_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_GALPAT_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_MARCH_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_TRANSP_GALPAT_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_WALK_PATH_TEST` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the algorithm for which this RamTstAlgParams set is defined. Note that the same algorithm can be used in more than one RamTstAlgParams.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. RamTstBlockParams

**容器属性**:

- **UUID**: `ECUC:365453a2-a957-4210-899c-637b8bb698fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstBlockParams`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container holds the description for one block of RAM.  For each RAM block to be tested by a given algorithm, there is one container which describes the block.  Multiple instances of this container are included in each container RamTst_AlgParams.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. RamTstBlockId

- **UUID**: `ECUC:870cc0a7-22ab-4ec1-a6c3-bbdd1f48186a`
- **参数名**: `RamTstBlockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RAM block

############## 2. RamTstEndAddress

- **UUID**: `ECUC:db9b3de1-6fa0-4124-9b4c-54348cf8a124`
- **参数名**: `RamTstEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End Address of the RAM block.

############## 3. RamTstFillPattern

- **UUID**: `ECUC:9cb6843f-a344-4e37-b442-d28f2b57f222`
- **参数名**: `RamTstFillPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pattern to be filled into each memory cell after destructive test of this block.

############## 4. RamTstStartAddress

- **UUID**: `ECUC:3cf53207-3a55-4307-b184-899a4d9e6060`
- **参数名**: `RamTstStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the RAM block.

############# ENUMERATION 类型参数

############## 1. RamTstTestPolicy

- **UUID**: `ECUC:1ba15d70-cca5-4af0-8497-2f540a258f38`
- **参数名**: `RamTstTestPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTEST_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
  - `RAMTEST_NON_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Policy regading destruction or non-destruction of memory content.

######### 2. RamTstBlockParams

**容器属性**:

- **UUID**: `ECUC:365453a2-a957-4210-899c-637b8bb698fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstBlockParams`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container holds the description for one block of RAM.  For each RAM block to be tested by a given algorithm, there is one container which describes the block.  Multiple instances of this container are included in each container RamTst_AlgParams.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. RamTstBlockId

- **UUID**: `ECUC:870cc0a7-22ab-4ec1-a6c3-bbdd1f48186a`
- **参数名**: `RamTstBlockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RAM block

############ 2. RamTstEndAddress

- **UUID**: `ECUC:db9b3de1-6fa0-4124-9b4c-54348cf8a124`
- **参数名**: `RamTstEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End Address of the RAM block.

############ 3. RamTstFillPattern

- **UUID**: `ECUC:9cb6843f-a344-4e37-b442-d28f2b57f222`
- **参数名**: `RamTstFillPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pattern to be filled into each memory cell after destructive test of this block.

############ 4. RamTstStartAddress

- **UUID**: `ECUC:3cf53207-3a55-4307-b184-899a4d9e6060`
- **参数名**: `RamTstStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the RAM block.

########### ENUMERATION 类型参数

############ 1. RamTstTestPolicy

- **UUID**: `ECUC:1ba15d70-cca5-4af0-8497-2f540a258f38`
- **参数名**: `RamTstTestPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTEST_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
  - `RAMTEST_NON_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Policy regading destruction or non-destruction of memory content.

####### 3. RamTstAlgParams

**容器属性**:

- **UUID**: `ECUC:72143fb4-1c83-44dc-8753-282521328089`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstAlgParams`
- **多重性**: [1..255]
- **多配置容器**: false

**容器描述**:

This container holds parameters for configuring an algorithm.  For each algorithm selected in the RamTst_Algorithms container there can be one or more RamTstAlgParams containers. The multiplicity of the included container RamTstBlockParams depends on the number of separate blocks of RAM which are defined for the particular test configuration.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. RamTstAlgParamsId

- **UUID**: `ECUC:ee97557e-a517-4dc6-a63d-e47756d5572f`
- **参数名**: `RamTstAlgParamsId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier by which this RamTstAlgParams set can be selected.

########## 2. RamTstExtNumberOfTestedCells

- **UUID**: `ECUC:733eb7c6-c2b1-4d00-9a53-564d38e9565f`
- **参数名**: `RamTstExtNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the absolute maximum value for the number of cells that NUMBER_OF_TESTED_CELLS and MAX_NUMBER_OF_TESTED_CELLS can be.

########## 3. RamTstMaxNumberOfTestedCells

- **UUID**: `ECUC:ed2796ab-085b-470c-b351-095568a161f2`
- **参数名**: `RamTstMaxNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the maximum value for the number of cells that can be tested in one cycle of a background test.

########## 4. RamTstNumberOfBlocks

- **UUID**: `ECUC:2e0f071e-2902-4850-a181-728a84d916b6`
- **参数名**: `RamTstNumberOfBlocks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of RAM blocks configured using the container

########## 5. RamTstNumberOfTestedCells

- **UUID**: `ECUC:8ba7b460-0266-4e5f-816d-0d5aa100dfa7`
- **参数名**: `RamTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the initial value for a RAM variable, which can be changed by the function "RamTst_ChangeNumberOfTestedCells"

######### ENUMERATION 类型参数

########## 1. RamTstAlgorithm

- **UUID**: `ECUC:c7ffb64f-2076-45ab-83c3-8c16a01d9a62`
- **参数名**: `RamTstAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTST_ABRAHAM_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_CHECKERBOARD_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_GALPAT_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_MARCH_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_TRANSP_GALPAT_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_WALK_PATH_TEST` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the algorithm for which this RamTstAlgParams set is defined. Note that the same algorithm can be used in more than one RamTstAlgParams.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. RamTstBlockParams

**容器属性**:

- **UUID**: `ECUC:365453a2-a957-4210-899c-637b8bb698fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstBlockParams`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container holds the description for one block of RAM.  For each RAM block to be tested by a given algorithm, there is one container which describes the block.  Multiple instances of this container are included in each container RamTst_AlgParams.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. RamTstBlockId

- **UUID**: `ECUC:870cc0a7-22ab-4ec1-a6c3-bbdd1f48186a`
- **参数名**: `RamTstBlockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RAM block

############ 2. RamTstEndAddress

- **UUID**: `ECUC:db9b3de1-6fa0-4124-9b4c-54348cf8a124`
- **参数名**: `RamTstEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End Address of the RAM block.

############ 3. RamTstFillPattern

- **UUID**: `ECUC:9cb6843f-a344-4e37-b442-d28f2b57f222`
- **参数名**: `RamTstFillPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pattern to be filled into each memory cell after destructive test of this block.

############ 4. RamTstStartAddress

- **UUID**: `ECUC:3cf53207-3a55-4307-b184-899a4d9e6060`
- **参数名**: `RamTstStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the RAM block.

########### ENUMERATION 类型参数

############ 1. RamTstTestPolicy

- **UUID**: `ECUC:1ba15d70-cca5-4af0-8497-2f540a258f38`
- **参数名**: `RamTstTestPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTEST_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
  - `RAMTEST_NON_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Policy regading destruction or non-destruction of memory content.

####### 4. RamTstBlockParams

**容器属性**:

- **UUID**: `ECUC:365453a2-a957-4210-899c-637b8bb698fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstBlockParams`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container holds the description for one block of RAM.  For each RAM block to be tested by a given algorithm, there is one container which describes the block.  Multiple instances of this container are included in each container RamTst_AlgParams.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. RamTstBlockId

- **UUID**: `ECUC:870cc0a7-22ab-4ec1-a6c3-bbdd1f48186a`
- **参数名**: `RamTstBlockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RAM block

########## 2. RamTstEndAddress

- **UUID**: `ECUC:db9b3de1-6fa0-4124-9b4c-54348cf8a124`
- **参数名**: `RamTstEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End Address of the RAM block.

########## 3. RamTstFillPattern

- **UUID**: `ECUC:9cb6843f-a344-4e37-b442-d28f2b57f222`
- **参数名**: `RamTstFillPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pattern to be filled into each memory cell after destructive test of this block.

########## 4. RamTstStartAddress

- **UUID**: `ECUC:3cf53207-3a55-4307-b184-899a4d9e6060`
- **参数名**: `RamTstStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the RAM block.

######### ENUMERATION 类型参数

########## 1. RamTstTestPolicy

- **UUID**: `ECUC:1ba15d70-cca5-4af0-8497-2f540a258f38`
- **参数名**: `RamTstTestPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTEST_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
  - `RAMTEST_NON_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Policy regading destruction or non-destruction of memory content.

##### 2. RamTstAlgorithms

**容器属性**:

- **UUID**: `ECUC:62eb25f3-28ac-452e-a2fa-0f92357c16a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstAlgorithms`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds all of the available test algorithms for the specific microcontroller.  Each test algorithm is selected ON or OFF before compiling so that only the desired test algorithms are in the compiled code.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. RamTstAbrahamTestSelected

- **UUID**: `ECUC:03482ab8-281d-4bfb-ae2d-fd63631d8108`
- **参数名**: `RamTstAbrahamTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the Abraham Test ON or OFF

######## 2. RamTstCheckerboardTestSelected

- **UUID**: `ECUC:0f5c4e78-46da-40cf-a1c7-11bce1d9263f`
- **参数名**: `RamTstCheckerboardTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the Checkerboard Test ON or OFF

######## 3. RamTstGalpatTestSelected

- **UUID**: `ECUC:090daeed-f256-425a-8e8f-be78873010f1`
- **参数名**: `RamTstGalpatTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the Galpat Test ON or OFF

######## 4. RamTstMarchTestSelected

- **UUID**: `ECUC:3582c79a-0327-4966-8752-343657127d47`
- **参数名**: `RamTstMarchTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the March Test ON or OFF

######## 5. RamTstTranspGalpatTestSelected

- **UUID**: `ECUC:94098234-bf83-41a3-84e4-f233699940b5`
- **参数名**: `RamTstTranspGalpatTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the Transparent Galpat Test ON or OFF

######## 6. RamTstWalkPathTestSelected

- **UUID**: `ECUC:f58faded-f154-4097-bfab-f56397d80138`
- **参数名**: `RamTstWalkPathTestSelected`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to select the Walking Path Test ON or OFF

##### 3. RamTstConfigParams

**容器属性**:

- **UUID**: `ECUC:f21793ef-75e0-4393-b885-e5580bc5e76f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstConfigParams`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters which are set at pre-compile or link time.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. RamTstDefaultAlgParamsId

- **UUID**: `ECUC:06024431-c473-4eca-9fc7-cb09b2c469a0`
- **参数名**: `RamTstDefaultAlgParamsId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier for the default "RamTstAlgParams" valid after the "RamTst_Init(..)" function. It is the initial value for a RAM variable which could be changed by the function "RamTst_SelectAlgParams".

######## 2. RamTstMinNumberOfTestedCells

- **UUID**: `ECUC:b5bda6a2-ef40-4cbd-b1b2-0798c4470c9b`
- **参数名**: `RamTstMinNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum number of tested cells for one cyle of a background test, as defined by implementer.

######## 3. RamTstNumberOfAlgParamSets

- **UUID**: `ECUC:657cca5b-020d-4d2f-8f3c-72fb031dc992`
- **参数名**: `RamTstNumberOfAlgParamSets`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of configured parameter sets for the available test algorithms.

####### FUNCTION-NAME 类型参数

######## 1. RamTstTestCompletedNotification

- **UUID**: `ECUC:c1358c78-a1a1-4f16-a6da-7ab1912eca98`
- **参数名**: `RamTstTestCompletedNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This function will be called from abackground test after finishing the RAM test without an error.

######## 2. RamTstTestErrorNotification

- **UUID**: `ECUC:a1575dfa-04a7-496c-bb71-d5dbf722f0cc`
- **参数名**: `RamTstTestErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This function will be called from a background test if an error occurs during the RAM test.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. RamTstAlgParams

**容器属性**:

- **UUID**: `ECUC:72143fb4-1c83-44dc-8753-282521328089`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstAlgParams`
- **多重性**: [1..255]
- **多配置容器**: false

**容器描述**:

This container holds parameters for configuring an algorithm.  For each algorithm selected in the RamTst_Algorithms container there can be one or more RamTstAlgParams containers. The multiplicity of the included container RamTstBlockParams depends on the number of separate blocks of RAM which are defined for the particular test configuration.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. RamTstAlgParamsId

- **UUID**: `ECUC:ee97557e-a517-4dc6-a63d-e47756d5572f`
- **参数名**: `RamTstAlgParamsId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier by which this RamTstAlgParams set can be selected.

########## 2. RamTstExtNumberOfTestedCells

- **UUID**: `ECUC:733eb7c6-c2b1-4d00-9a53-564d38e9565f`
- **参数名**: `RamTstExtNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the absolute maximum value for the number of cells that NUMBER_OF_TESTED_CELLS and MAX_NUMBER_OF_TESTED_CELLS can be.

########## 3. RamTstMaxNumberOfTestedCells

- **UUID**: `ECUC:ed2796ab-085b-470c-b351-095568a161f2`
- **参数名**: `RamTstMaxNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the maximum value for the number of cells that can be tested in one cycle of a background test.

########## 4. RamTstNumberOfBlocks

- **UUID**: `ECUC:2e0f071e-2902-4850-a181-728a84d916b6`
- **参数名**: `RamTstNumberOfBlocks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of RAM blocks configured using the container

########## 5. RamTstNumberOfTestedCells

- **UUID**: `ECUC:8ba7b460-0266-4e5f-816d-0d5aa100dfa7`
- **参数名**: `RamTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the initial value for a RAM variable, which can be changed by the function "RamTst_ChangeNumberOfTestedCells"

######### ENUMERATION 类型参数

########## 1. RamTstAlgorithm

- **UUID**: `ECUC:c7ffb64f-2076-45ab-83c3-8c16a01d9a62`
- **参数名**: `RamTstAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTST_ABRAHAM_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_CHECKERBOARD_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_GALPAT_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_MARCH_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_TRANSP_GALPAT_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_WALK_PATH_TEST` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the algorithm for which this RamTstAlgParams set is defined. Note that the same algorithm can be used in more than one RamTstAlgParams.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. RamTstBlockParams

**容器属性**:

- **UUID**: `ECUC:365453a2-a957-4210-899c-637b8bb698fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstBlockParams`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container holds the description for one block of RAM.  For each RAM block to be tested by a given algorithm, there is one container which describes the block.  Multiple instances of this container are included in each container RamTst_AlgParams.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. RamTstBlockId

- **UUID**: `ECUC:870cc0a7-22ab-4ec1-a6c3-bbdd1f48186a`
- **参数名**: `RamTstBlockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RAM block

############ 2. RamTstEndAddress

- **UUID**: `ECUC:db9b3de1-6fa0-4124-9b4c-54348cf8a124`
- **参数名**: `RamTstEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End Address of the RAM block.

############ 3. RamTstFillPattern

- **UUID**: `ECUC:9cb6843f-a344-4e37-b442-d28f2b57f222`
- **参数名**: `RamTstFillPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pattern to be filled into each memory cell after destructive test of this block.

############ 4. RamTstStartAddress

- **UUID**: `ECUC:3cf53207-3a55-4307-b184-899a4d9e6060`
- **参数名**: `RamTstStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the RAM block.

########### ENUMERATION 类型参数

############ 1. RamTstTestPolicy

- **UUID**: `ECUC:1ba15d70-cca5-4af0-8497-2f540a258f38`
- **参数名**: `RamTstTestPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTEST_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
  - `RAMTEST_NON_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Policy regading destruction or non-destruction of memory content.

####### 2. RamTstBlockParams

**容器属性**:

- **UUID**: `ECUC:365453a2-a957-4210-899c-637b8bb698fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstBlockParams`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container holds the description for one block of RAM.  For each RAM block to be tested by a given algorithm, there is one container which describes the block.  Multiple instances of this container are included in each container RamTst_AlgParams.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. RamTstBlockId

- **UUID**: `ECUC:870cc0a7-22ab-4ec1-a6c3-bbdd1f48186a`
- **参数名**: `RamTstBlockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RAM block

########## 2. RamTstEndAddress

- **UUID**: `ECUC:db9b3de1-6fa0-4124-9b4c-54348cf8a124`
- **参数名**: `RamTstEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End Address of the RAM block.

########## 3. RamTstFillPattern

- **UUID**: `ECUC:9cb6843f-a344-4e37-b442-d28f2b57f222`
- **参数名**: `RamTstFillPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pattern to be filled into each memory cell after destructive test of this block.

########## 4. RamTstStartAddress

- **UUID**: `ECUC:3cf53207-3a55-4307-b184-899a4d9e6060`
- **参数名**: `RamTstStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the RAM block.

######### ENUMERATION 类型参数

########## 1. RamTstTestPolicy

- **UUID**: `ECUC:1ba15d70-cca5-4af0-8497-2f540a258f38`
- **参数名**: `RamTstTestPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTEST_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
  - `RAMTEST_NON_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Policy regading destruction or non-destruction of memory content.

##### 4. RamTstAlgParams

**容器属性**:

- **UUID**: `ECUC:72143fb4-1c83-44dc-8753-282521328089`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstAlgParams`
- **多重性**: [1..255]
- **多配置容器**: false

**容器描述**:

This container holds parameters for configuring an algorithm.  For each algorithm selected in the RamTst_Algorithms container there can be one or more RamTstAlgParams containers. The multiplicity of the included container RamTstBlockParams depends on the number of separate blocks of RAM which are defined for the particular test configuration.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. RamTstAlgParamsId

- **UUID**: `ECUC:ee97557e-a517-4dc6-a63d-e47756d5572f`
- **参数名**: `RamTstAlgParamsId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the identifier by which this RamTstAlgParams set can be selected.

######## 2. RamTstExtNumberOfTestedCells

- **UUID**: `ECUC:733eb7c6-c2b1-4d00-9a53-564d38e9565f`
- **参数名**: `RamTstExtNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the absolute maximum value for the number of cells that NUMBER_OF_TESTED_CELLS and MAX_NUMBER_OF_TESTED_CELLS can be.

######## 3. RamTstMaxNumberOfTestedCells

- **UUID**: `ECUC:ed2796ab-085b-470c-b351-095568a161f2`
- **参数名**: `RamTstMaxNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the maximum value for the number of cells that can be tested in one cycle of a background test.

######## 4. RamTstNumberOfBlocks

- **UUID**: `ECUC:2e0f071e-2902-4850-a181-728a84d916b6`
- **参数名**: `RamTstNumberOfBlocks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of RAM blocks configured using the container

######## 5. RamTstNumberOfTestedCells

- **UUID**: `ECUC:8ba7b460-0266-4e5f-816d-0d5aa100dfa7`
- **参数名**: `RamTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the initial value for a RAM variable, which can be changed by the function "RamTst_ChangeNumberOfTestedCells"

####### ENUMERATION 类型参数

######## 1. RamTstAlgorithm

- **UUID**: `ECUC:c7ffb64f-2076-45ab-83c3-8c16a01d9a62`
- **参数名**: `RamTstAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTST_ABRAHAM_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_CHECKERBOARD_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_GALPAT_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_MARCH_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_TRANSP_GALPAT_TEST` (来源: AUTOSAR_ECUC)
  - `RAMTST_WALK_PATH_TEST` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the algorithm for which this RamTstAlgParams set is defined. Note that the same algorithm can be used in more than one RamTstAlgParams.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. RamTstBlockParams

**容器属性**:

- **UUID**: `ECUC:365453a2-a957-4210-899c-637b8bb698fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstBlockParams`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container holds the description for one block of RAM.  For each RAM block to be tested by a given algorithm, there is one container which describes the block.  Multiple instances of this container are included in each container RamTst_AlgParams.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. RamTstBlockId

- **UUID**: `ECUC:870cc0a7-22ab-4ec1-a6c3-bbdd1f48186a`
- **参数名**: `RamTstBlockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RAM block

########## 2. RamTstEndAddress

- **UUID**: `ECUC:db9b3de1-6fa0-4124-9b4c-54348cf8a124`
- **参数名**: `RamTstEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End Address of the RAM block.

########## 3. RamTstFillPattern

- **UUID**: `ECUC:9cb6843f-a344-4e37-b442-d28f2b57f222`
- **参数名**: `RamTstFillPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pattern to be filled into each memory cell after destructive test of this block.

########## 4. RamTstStartAddress

- **UUID**: `ECUC:3cf53207-3a55-4307-b184-899a4d9e6060`
- **参数名**: `RamTstStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the RAM block.

######### ENUMERATION 类型参数

########## 1. RamTstTestPolicy

- **UUID**: `ECUC:1ba15d70-cca5-4af0-8497-2f540a258f38`
- **参数名**: `RamTstTestPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTEST_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
  - `RAMTEST_NON_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Policy regading destruction or non-destruction of memory content.

##### 5. RamTstBlockParams

**容器属性**:

- **UUID**: `ECUC:365453a2-a957-4210-899c-637b8bb698fe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstBlockParams`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container holds the description for one block of RAM.  For each RAM block to be tested by a given algorithm, there is one container which describes the block.  Multiple instances of this container are included in each container RamTst_AlgParams.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. RamTstBlockId

- **UUID**: `ECUC:870cc0a7-22ab-4ec1-a6c3-bbdd1f48186a`
- **参数名**: `RamTstBlockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the RAM block

######## 2. RamTstEndAddress

- **UUID**: `ECUC:db9b3de1-6fa0-4124-9b4c-54348cf8a124`
- **参数名**: `RamTstEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End Address of the RAM block.

######## 3. RamTstFillPattern

- **UUID**: `ECUC:9cb6843f-a344-4e37-b442-d28f2b57f222`
- **参数名**: `RamTstFillPattern`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pattern to be filled into each memory cell after destructive test of this block.

######## 4. RamTstStartAddress

- **UUID**: `ECUC:3cf53207-3a55-4307-b184-899a4d9e6060`
- **参数名**: `RamTstStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the RAM block.

####### ENUMERATION 类型参数

######## 1. RamTstTestPolicy

- **UUID**: `ECUC:1ba15d70-cca5-4af0-8497-2f540a258f38`
- **参数名**: `RamTstTestPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAMTEST_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
  - `RAMTEST_NON_DESTRUCTIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Policy regading destruction or non-destruction of memory content.

##### 6. RamTstDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:837481e5-843f-49a5-bef6-fbe366860373`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. RAMTST_E_RAM_FAILURE

- **UUID**: `ECUC:b688e59f-c065-4c8d-92f7-1dd4a961f00b`
- **引用名**: `RAMTST_E_RAM_FAILURE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "RAM failure" has occurred.

##### 7. RamTstPublishedInformation

**容器属性**:

- **UUID**: `ECUC:ada3cd50-4795-4481-84dd-e5f0575be6c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RamTstPublishedInformation`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container holding all RamTst specific published information parameter.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. RamTstCellSize

- **UUID**: `ECUC:79ad475e-d255-4fb7-a3d8-4ae49f9106ef`
- **参数名**: `RamTstCellSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-LINK-TIME
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Size of RAM cells (in bits) which can be tested individually by the given implementation.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AUTOSAR

- **UUID**: `ECUC:AUTOSAR`
- **包名称**: `AUTOSAR`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **RamTst**
