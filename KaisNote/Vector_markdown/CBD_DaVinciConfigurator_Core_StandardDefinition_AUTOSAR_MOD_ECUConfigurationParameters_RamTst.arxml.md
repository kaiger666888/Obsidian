# RamTst

## 模块描述

Configuration of the RamTst module.

## 容器列表

### 1. RamTstCommon

**描述**: This container holds a list of all available functions in the RamTst module.  Each function is
turned ON or OFF before compiling so that only the desired functions and test algorithms are in the
compiled code.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RamTstAllowApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function "RamTst_Allow".
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: RamTstChangeNumOfTestedCellsApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function "RamTst_ChangeNumberOfTestedCells".
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: RamTstDevErrorDetect
  长名称: ''
  描述: Preprocessor switch to select the development error tracer (DET)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: RamTstGetAlgParamsApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function "RamTst_GetAlgParams".
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: RamTstGetExecutionStatusApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: RamTstGetNumberOfTestedCellsApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function "RamTst_GetNumberOfTestedCells".
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: RamTstGetTestAlgorithmApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: RamTstGetTestResultApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: RamTstGetTestResultPerBlockApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: RamTstGetVersionInfoApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: RamTstResumeApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function "RamTst_Resume".
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: RamTstRunFullTestApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: RamTstRunPartialTestApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: RamTstSelectAlgParamsApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function "RamTst_SelectAlgParams".
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: RamTstStopApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: RamTstSuspendApi
  长名称: ''
  描述: Preprocessor switch to disable / enable the function "RamTst_Suspend".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. RamTstAlgorithms

**描述**: This container holds all of the available test algorithms for the specific microcontroller.  Each
test algorithm is selected ON or OFF before compiling so that only the desired test algorithms are
in the compiled code.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RamTstAbrahamTestSelected
  长名称: ''
  描述: Preprocessor switch to select the Abraham Test ON or OFF
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: RamTstCheckerboardTestSelected
  长名称: ''
  描述: Preprocessor switch to select the Checkerboard Test ON or OFF
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: RamTstGalpatTestSelected
  长名称: ''
  描述: Preprocessor switch to select the Galpat Test ON or OFF
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: RamTstMarchTestSelected
  长名称: ''
  描述: Preprocessor switch to select the March Test ON or OFF
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: RamTstTranspGalpatTestSelected
  长名称: ''
  描述: Preprocessor switch to select the Transparent Galpat Test ON or OFF
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: RamTstWalkPathTestSelected
  长名称: ''
  描述: Preprocessor switch to select the Walking Path Test ON or OFF
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. RamTstConfigParams

**描述**: This container specifies configuration parameters which are set at pre-compile or link time.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RamTstDefaultAlgParamsId
  长名称: ''
  描述: This is the identifier for the default "RamTstAlgParams" valid after the "RamTst_Init(..)"
      function. It is the initial value for a RAM variable which could be changed by the
      function "RamTst_SelectAlgParams".
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: RamTstMinNumberOfTestedCells
  长名称: ''
  描述: Minimum number of tested cells for one cyle of a background test, as defined by implementer.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: RamTstNumberOfAlgParamSets
  长名称: ''
  描述: Number of configured parameter sets for the available test algorithms.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 4
  名称: RamTstTestCompletedNotification
  长名称: ''
  描述: This function will be called from abackground test after finishing the RAM test without an
      error.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: RamTstTestErrorNotification
  长名称: ''
  描述: This function will be called from a background test if an error occurs during the RAM test.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. RamTstAlgParams

**描述**: This container holds parameters for configuring an algorithm.  For each algorithm selected in the
RamTst_Algorithms container there can be one or more RamTstAlgParams containers. The multiplicity of
the included container RamTstBlockParams depends on the number of separate blocks of RAM which are
defined for the particular test configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RamTstAlgParamsId
  长名称: ''
  描述: This is the identifier by which this RamTstAlgParams set can be selected.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: RamTstAlgorithm
  长名称: ''
  描述: This is the algorithm for which this RamTstAlgParams set is defined. Note that the same
      algorithm can be used in more than one RamTstAlgParams.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: RamTstExtNumberOfTestedCells
  长名称: ''
  描述: This is the absolute maximum value for the number of cells that NUMBER_OF_TESTED_CELLS and
      MAX_NUMBER_OF_TESTED_CELLS can be.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 4
  名称: RamTstMaxNumberOfTestedCells
  长名称: ''
  描述: This is the maximum value for the number of cells that can be tested in one cycle of a
      background test.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 5
  名称: RamTstNumberOfBlocks
  长名称: ''
  描述: Number of RAM blocks configured using the container
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: RamTstNumberOfTestedCells
  长名称: ''
  描述: This is the initial value for a RAM variable, which can be changed by the function
      "RamTst_ChangeNumberOfTestedCells"
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 5. RamTstBlockParams

**描述**: This container holds the description for one block of RAM.  For each RAM block to be tested by a
given algorithm, there is one container which describes the block.  Multiple instances of this
container are included in each container RamTst_AlgParams.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RamTstBlockId
  长名称: ''
  描述: ID of the RAM block
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: RamTstEndAddress
  长名称: ''
  描述: End Address of the RAM block.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: RamTstFillPattern
  长名称: ''
  描述: Pattern to be filled into each memory cell after destructive test of this block.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: RamTstStartAddress
  长名称: ''
  描述: Start Address of the RAM block.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: RamTstTestPolicy
  长名称: ''
  描述: Policy regading destruction or non-destruction of memory content.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. RamTstDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value.

该容器没有参数。

### 7. RamTstPublishedInformation

**描述**: Container holding all RamTst specific published information parameter.

#### 参数列表

```yaml
- 
  序号: 1
  名称: RamTstCellSize
  长名称: ''
  描述: Size of RAM cells (in bits) which can be tested individually by the given implementation.
  默认值: ''
  最小值: 1
  最大值: 64
```

