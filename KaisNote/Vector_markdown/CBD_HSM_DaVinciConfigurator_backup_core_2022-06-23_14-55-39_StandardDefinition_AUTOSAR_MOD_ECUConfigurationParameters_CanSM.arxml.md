# CanSM

## 模块描述

Configuration of the CanSM module

## 容器列表

### 1. CanSMConfiguration

**描述**: This container contains the global parameters of the CanSM and sub containers, which are for the CAN
network specific configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanSMModeRequestRepetitionMax
  长名称: ''
  描述: Specifies the maximal amount of mode request repetitions without a respective mode indication
      from the CanIf module until the CanSM module reports a development error to the DET and
      tries to go back to no communication.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: CanSMModeRequestRepetitionTime
  长名称: ''
  描述: Specifies in which time duration the CanSM module shall repeat mode change requests by using
      the API of the CanIf module.
  默认值: ''
  最小值: 0
  最大值: 65.535
```

### 2. CanSMManagerNetwork

**描述**: This container contains the CAN network specific parameters of each CAN network

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanSMBorCounterL1ToL2
  长名称: ''
  描述: This threshold defines the count of bus-offs until the bus-off recovery switches from level 1
      (short recovery time) to level 2 (long recovery time).
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: CanSMBorTimeL1
  长名称: ''
  描述: This time parameter defines in seconds the duration of the bus-off recovery time in level 1
      (short recovery time).
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 3
  名称: CanSMBorTimeL2
  长名称: ''
  描述: This time parameter defines in seconds the duration of the bus-off recovery time in level 2
      (long recovery time).
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 4
  名称: CanSMBorTimeTxEnsured
  长名称: ''
  描述: This parameter defines in seconds the duration of the bus-off event check. This check
      assesses, if the recovery has been successful after the recovery reenables the transmit
      path. If a new bus-off occurs during this time period, the CanSM assesses this bus-off
      as sequential bus-off without successful recovery. Because a bus-off only can be
      detected, when PDUs are transmitted, the time has to be great enough to ensure that PDUs
      are transmitted again (e. g. time period of the fastest cyclic transmitted PDU of the
      COM module / ComTxModeTimePeriodFactor).
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 5
  名称: CanSMBorTxConfirmationPolling
  长名称: ''
  描述: This parameter shall configure, if the CanSM polls the CanIf_GetTxConfirmationState API to
      decide the bus-off state to be recovered instead of using the CanSMBorTimeTxEnsured
      parameter for this decision.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. CanSMController

**描述**: This container contains the controller IDs assigned to a CAN network.

该容器没有参数。

### 4. CanSMDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 5. CanSMGeneral

**描述**: Container for general pre-compile parameters of the CanSM module

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanSMDevErrorDetect
  长名称: ''
  描述: Enables and disables the development error detection and notification mechanism.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanSMMainFunctionTimePeriod
  长名称: ''
  描述: This parameter defines the cycle time of the function CanSM_MainFunction in seconds
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 3
  名称: CanSMVersionInfoApi
  长名称: ''
  描述: Activate/Deactivate the version information API (CanSM_GetVersionInfo).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CanSmChangeBaudrateApi
  长名称: ''
  描述: The support of the Can_ChangeBaudrate API is optional.
  默认值: false
  最小值: ''
  最大值: ''
```

