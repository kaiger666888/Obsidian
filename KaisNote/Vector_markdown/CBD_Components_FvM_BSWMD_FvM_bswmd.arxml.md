# FvM

## 模块描述

The software component Freshness Value Manager provides freshness values to the Secure Onboard
Communication module. The freshness values are used to counter replay-attacks.
#Security
#Vector

## 容器列表

### 1. FvMGeneral

**描述**: Freshness Value Manager Time Based General Attributes Container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FvMDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling development error detection support.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FvMVersionInfoApi
  长名称: ''
  描述: If true the SecOC_GetVersionInfo API is available.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FvMCheckTxTimeBaseStatusCallout
  长名称: ''
  描述: |
    This callout gives the application the opportunity to evaluate the StbM_TimeBaseStatus.
    Returns E_OK -> FvM will use the time stamp.
    Retruns E_NOT_OK -> FvM will not provide a freshness value to the SecOC.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FvMCheckRxTimeBaseStatusCallout
  长名称: ''
  描述: |
    This callout gives the application the opportunity to evaluate the StbM_TimeBaseStatus.
    Returns E_OK -> FvM will use the time stamp.
    Retruns E_NOT_OK -> FvM will not provide a freshness value to the SecOC.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FvMSafeBswChecks
  长名称: ''
  描述: |
    Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
    are checked before function is executed.
    This attribute has to be enabled for safety projects where this component is mapped to an ASIL
    partition.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. FvMGeneration

**描述**: Contains the generation configuration parameters of the module FvM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FvMOutOfBoundsWriteProtectionStrategy
  长名称: ''
  描述: |
    This parameter is used to configure a strategy to protect the code to write out of bounds.
    
    NONE: no protection strategy is generated in the data access.
    INDEX_SATURATION: arrays are blown up and the data access index is saturated by an appropriate
    mask. The advantage is the speed of the data access, but own data elements at other indexes of
    the same variable can be overridden.
    INDEX_CHECKING: the data access index is validated by a runtime check. The advantage is that
    values are never written to incorrect indexes of the data access.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FvMOutOfBoundsWriteSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds write problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FvMOutOfBoundsReadSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds read problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FvMShortSymbols
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate shortened symbol names.
    
    FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant
    names.
    TRUE: symbol names are generated based on the MIP and a CRC32.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FvMInterfacesForDeactivatedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate bsw data interfaces for
    deactivated data elements. This is an advantage for the BSW developer to reduce the time to
    market with a development environment using auto completition and to investigate potential
    interfaces.
    
    FALSE: data interfaces are not generated if the data elementis deactivated.
    TRUE: data interfaces are generated as e.g. emty macros.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FvMReferringKeysInComments
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate referring keys in comments. This
    is an advantage for the developer to investigate indirections, but this feature reduces the
    overall readability of the generated data.
    
    FALSE: referring keys are not generated in comments.
    TRUE: referring keys are generated in comments.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. FvMTimeBasedOption

**描述**: Container to configure a timebase option.
The parameters SecOCFreshnessValueLength, SecOCFreshnessValueTxLength and
SecOCAuthenticationVerifyAttempts of the related SecOC(Rx|Tx)PduProcessing are used by the FvM for
this option.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FvMTimeBasedOptionId
  长名称: ''
  描述: Time Based Option Id. To use this option with a SecOC(Rx|Tx)PduProcessing the
      SecOCFreshnessValueId must match this Id.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: FvMNanosecondsBitSize
  长名称: Truncated Nanoseconds Bit Size
  描述: Number of nanoseconds bits that are transmitted on the bus (TFV) and are used as nanoseconds
      part of the freshness value (FV). The number of nanoseconds bits is always the same for
      the truncated freshness value and the freshness value.
  默认值: 30
  最小值: 0
  最大值: 30
- 
  序号: 3
  名称: FvMSecondsBitSize
  长名称: ''
  描述: Number of seconds bits that are used as seconds part of the freshness value (FV).
  默认值: 32
  最小值: 0
  最大值: 32
- 
  序号: 4
  名称: FvMTruncatedSecondsBitSize
  长名称: ''
  描述: Number of seconds bits that are transmitted on the bus (TFV).
  默认值: 32
  最小值: 0
  最大值: 32
- 
  序号: 5
  名称: FvMRxAcceptanceWindow
  长名称: ''
  描述: |
    A tolerant time window shall be defined as RX Acceptance Window.
    
    The RX Acceptance Window shall be determined based on the worst-case message latency (i.e.
    procecssing and transmission time) and synchronized Local Time difference. The acceptance window
    shall be large enough for legitimate fresh messages to be accepted correctly by the receiver,
    while it shall be small enough to detect replayed messages. Depending on the use case
    requirement of Acceptance Window size, tuning may be required to find out the best and minimum
    Acceptance Window.
  默认值: 1000000000
  最小值: 0
  最大值: 4294967295
```

