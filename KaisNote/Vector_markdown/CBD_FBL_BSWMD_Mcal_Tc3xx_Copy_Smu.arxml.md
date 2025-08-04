# Smu

## 模块描述

Configuration of the Smu (Safety Management Unit) module.

## 容器列表

### 1. SmuConfigSet

**描述**: This is the base container that contains the post-build configuration parameters

该容器没有参数。

### 2. SmuCoreConfig

**描述**: This is the base container that contains the post-build configuration parameters for SmuCore

该容器没有参数。

### 3. SmuCoreRecoveryTimer

**描述**: SmuCore Recovery Timer configuration (parameters).

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmuCoreEnableRT0
  长名称: ''
  描述: Defines the Enabling or Disabling of SmuCore Recovery Timer 0.
  默认值: SMU_RT_DISABLE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmuCoreEnableRT1
  长名称: ''
  描述: Defines the Enabling or Disabling of SmuCore Recovery Timer 1.
  默认值: SMU_RT_DISABLE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SmuCoreRTDuration
  长名称: ''
  描述: Defines the SmuCore Recovery Timer maximum duration.
  默认值: 16383
  最小值: 1
  最大值: 16777215
```

### 4. SmuCoreRT0Alarm

**描述**: Alarms for Recovery Timer 0.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmuCoreRT0AlarmGroupId
  长名称: ''
  描述: Defines the alarm group that can use the recovery timer 0.
  默认值: SMU_ALARM_GROUP0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmuCoreRT0AlarmId
  长名称: ''
  描述: Defines the alarm identifier of the selected group that can use the recovery timer 0.
  默认值: 0
  最小值: 0
  最大值: 31
```

### 5. SmuCoreRT1Alarm

**描述**: Alarms for the Recovery Timer 1.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmuCoreRT1AlarmGroupId
  长名称: ''
  描述: Defines the alarm group that can use the recovery timer 1.
  默认值: SMU_ALARM_GROUP0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmuCoreRT1AlarmId
  长名称: ''
  描述: Defines the alarm identifier of the selected group that can use the recovery timer 1.
  默认值: 0
  最小值: 0
  最大值: 31
```

### 6. SmuCoreAlarmGlobalConfig

**描述**: SmuCore Alarm Global Configuration .

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmuCoreInterruptSet0
  长名称: ''
  描述: Defines the output value of the interrupt request vector when the alarm configuration flag
      selects the interrupt configuration set 0.
  默认值: SMU_SELECT_INT_NONE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmuCoreInterruptSet1
  长名称: ''
  描述: Defines the output value of the interrupt request vector when the alarm configuration flag
      selects the interrupt configuration set 1
  默认值: SMU_SELECT_INT_NONE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SmuCoreInterruptSet2
  长名称: ''
  描述: Defines the output value of the interrupt request vector when the alarm configuration flag
      selects the interrupt configuration set 2
  默认值: SMU_SELECT_INT_NONE
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SmuCoreCpu0ResetRequest
  长名称: ''
  描述: This parameter defines the Cpu reset request to CPU.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SmuCoreCpu1ResetRequest
  长名称: ''
  描述: This parameter defines the Cpu reset request to CPU.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SmuCoreCpu2ResetRequest
  长名称: ''
  描述: This parameter defines the Cpu reset request to CPU.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SmuCoreCpu3ResetRequest
  长名称: ''
  描述: This parameter defines the Cpu reset request to CPU.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SmuCoreCpu4ResetRequest
  长名称: ''
  描述: This parameter defines the Cpu reset request to CPU.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SmuCoreCpu5ResetRequest
  长名称: ''
  描述: This parameter defines the Cpu reset request to CPU.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: SmuCoreIGCS0ActivatePES
  长名称: ''
  描述: Defines the control of the Port Emergency Stop (PES) feature when IGCS0 configured alarm is
      active. When an internal action is triggered, the hardware triggers automatically the
      PES on enabling
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SmuCoreIGCS1ActivatePES
  长名称: ''
  描述: Defines the control of the Port Emergency Stop (PES) feature when IGCS1 configured alarm is
      active. When an internal action is triggered, the hardware triggers automatically the
      PES on enabling
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: SmuCoreIGCS2ActivatePES
  长名称: ''
  描述: Defines the control of the Port Emergency Stop (PES) feature when IGCS2 configured alarm is
      active. When an internal action is triggered, the hardware triggers automatically the
      PES on enabling
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: SmuCoreNMIActivatePES
  长名称: ''
  描述: Defines the control of the Port Emergency Stop (PES) feature when NMI configured alarm is
      active. When an internal action is triggered, the hardware triggers automatically the
      PES on enabling
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: SmuCoreCpuResetActivatePES
  长名称: ''
  描述: Defines the control of the Port Emergency Stop (PES) feature when CPU RESET configured alarm
      is active. When an internal action is triggered, the hardware triggers automatically the
      PES on enabling
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: SmuCoreEnableFaultToRunState
  长名称: ''
  描述: Defines the control of Fault State to Fault Free (Run) State transition. The state transition
      is possible only when this parameter is defined with SMU_EFRST_ENABLE
  默认值: SMU_EFRST_DISABLE
  最小值: ''
  最大值: ''
```

### 7. SmuCoreFSPHandling

**描述**: SmuCore driver FSP configuration (parameters) .

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmuCoreFSPPrescaler1
  长名称: ''
  描述: Defines the dividing factor to apply to the reference clock FEVR_OSC. The divided clock is
      used as reference to generate the timing of the FSP fault state
  默认值: SMU_REF_CLK_FRQ_DIV_2
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmuCoreFSPPrescaler2
  长名称: ''
  描述: Defines the dividing factor to apply to the reference clock FEVR_OSC in order to generate the
      timing of the fault free state for the dynamic dual rail and time switching modes of the
      fault signaling protocol
  默认值: SMU_REF_CLK_FRQ_DIV_512
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SmuCoreFSPSignalingMode
  长名称: ''
  描述: Defines the type of signal output for FSP on an alarm event
  默认值: SMU_FSP_BISTABLE_PROTOCOL
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SmuCorePESOnFSP
  长名称: ''
  描述: Defines the PES to automatically request when an alarm event configured to start the FSP is
      detected
  默认值: SMU_FSP_PES_DISABLE
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SmuCoreFSPFaultStateDuration
  长名称: ''
  描述: This parameter enables the maximum fault state duration of FSP signal. The value is written in
      TFSP_HIGH bits of SMU_FSP register. It shall be specified as a number of fSMU_FS ticks.
  默认值: 1
  最小值: 0
  最大值: 1023
```

### 8. SmuCoreAlarmGroup

**描述**: Container for SmuCore Alarm Group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmuCoreAlmGrpId
  长名称: ''
  描述: Group Id of the SMU alarm group. This value will be assigned to the symbolic name derived of
      the AlarmGroup container short name.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 9. SmuCoreAlarmBehavior

**描述**: Container for SMU Alarm Behavior.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmuCoreAlmBehaviourId
  长名称: ''
  描述: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the
      AlarmBehaviour container short name.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SmuCoreAlarmIntBeh
  长名称: ''
  描述: Defines the internal behavior of an alarm event
  默认值: SMU_NA_INT_ACTION
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SmuCoreAlarmFSP
  长名称: ''
  描述: Defines the Fault Signaling of an alarm event
  默认值: SMU_ALARM_FSP_DISABLED
  最小值: ''
  最大值: ''
```

### 10. SmuStdbyConfig

**描述**: This is the base container that contains the post-build configuration parameters for SmuStdby

该容器没有参数。

### 11. SmuStdbyAlarmGlobalConfig

**描述**: SmuStdby Alarm Global Configuration .

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmuStdbyEnableFSP0
  长名称: ''
  描述: Defines the error pin 33.8 to be used for FSP
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmuStdbyEnableFSP1
  长名称: ''
  描述: Defines the error pin 33.10 to be used for FSP
  默认值: false
  最小值: ''
  最大值: ''
```

### 12. SmuStdbyAlarmGroup

**描述**: Container for SmuStdby Alarm Group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmuStdbyAlmGrpId
  长名称: ''
  描述: Group Id of the SMU alarm group. This value will be assigned to the symbolic name derived of
      the AlarmGroup container short name.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 13. SmuStdbyAlarmBehavior

**描述**: Container for SmuStdby Alarm Behavior.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmuStdbyAlmBehaviourId
  长名称: ''
  描述: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the
      AlarmBehaviour container short name.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SmuStdbyAlarmFSP
  长名称: ''
  描述: Defines the Fault Signaling of an alarm event
  默认值: SMU_ALARM_FSP_DISABLED
  最小值: ''
  最大值: ''
```

### 14. SmuGeneral

**描述**: SMU Module related generic configurations.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmuStdbyEnable
  长名称: ''
  描述: This parameter switches the SmuStdby on/off
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmuDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SmuSafetyEnable
  长名称: ''
  描述: Switches the safety Error Checking ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SmuInitCheckApi
  长名称: ''
  描述: Switches the Smu_InitCheck detection and notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SmuRuntimeApiMode
  长名称: ''
  描述: Defines the output value of the Runtime API mode
  默认值: SMU_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SmuInitDeInitApiMode
  长名称: ''
  描述: Defines the output value of the Init API mode
  默认值: SMU_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SmuVersionInfoApi
  长名称: ''
  描述: Adds / removes the service Smu_GetVersionInfo() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SmuCoreFSP0OutputEnable
  长名称: ''
  描述: This parameter sets FSP[0] state to output if TRUE
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SmuCoreFSP1OutputEnable
  长名称: ''
  描述: This parameter sets FSP[1] state to output if TRUE
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: SmuCoreFSP0PortEnable
  长名称: ''
  描述: This parameter sets FSP[0] PORT enable TRUE
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SmuCoreFSP1PortEnable
  长名称: ''
  描述: This parameter sets FSP[1] PORT enable TRUE
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: SmuCoreGlitchFilterSCU
  长名称: ''
  描述: This parameter sets glitch filter for SCU enabled
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: SmuCoreGlitchFilterSTS
  长名称: ''
  描述: This parameter sets glitch filter for SMU_STS enabled
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: SmuAGStatusTimeout
  长名称: ''
  描述: timeout value for SMU AGStatus
  默认值: 4096
  最小值: 4096
  最大值: 65535
```

### 15. CommonPublishedInformation

**描述**: Common container, aggregated by all modules. It contains published information about vendor and
versions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArMajorVersion
  长名称: ''
  描述: Major version number of AUTOSAR specification on which the appropriate implementation is based
      on.
  默认值: 4
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: ArMinorVersion
  长名称: ''
  描述: Minor version number of AUTOSAR specification on which the appropriate implementation is based
      on.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: ArPatchVersion
  长名称: ''
  描述: Patch level version number of AUTOSAR specification on which the appropriate implementation is
      based on.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: SwMajorVersion
  长名称: ''
  描述: Major version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 10
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: SwMinorVersion
  长名称: ''
  描述: Minor version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 40
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: SwPatchVersion
  长名称: ''
  描述: Patch level version number of the vendor specific implementation of the module. The numbering
      is vendor specific.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: ModuleId
  长名称: ''
  描述: Module ID of this module from Module List
  默认值: 255
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: VendorId
  长名称: ''
  描述: Vendor ID of the dedicated implementation of this module according to the AUTOSAR vendor list
  默认值: 17
  最小值: 0
  最大值: 65535
- 
  序号: 9
  名称: Release
  长名称: ''
  描述: Aurix derivative used for the implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

### 16. SmuDemEventParameterRefsConf

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId symbolic name. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

