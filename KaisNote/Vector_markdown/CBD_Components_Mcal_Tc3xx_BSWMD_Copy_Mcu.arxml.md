# Mcu

## 模块描述

Configuration of the Mcu (Microcontroller Unit) module.

## 容器列表

### 1. McuGeneralConfiguration

**描述**: This container contains the configuration (parameters) of the MCU driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuMultiCoreErrorDetect
  长名称: ''
  描述: Switches the Multicore Error detection and notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuGetRamStateApi
  长名称: ''
  描述: Pre-processor switch to enable/disable the API Mcu_GetRamState. This Api is not supported,
      therefore this parameter is always false.                               TRUE : The
      function Mcu_GetRamState() is enabled.                               FALSE: The function
      Mcu_GetRamState() is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: McuInitClock
  长名称: ''
  描述: If this parameter is set to FALSE, the clock initialization has to be disabled from the MCU
      driver. This concept applies when there are some write once clock registers and a
      bootloader is present. If this parameter is set to TRUE, the MCU driver is responsible
      of the clock initialization.                               TRUE : Mcu_InitClock API is
      available.                               FALSE: Mcu_InitClock API is not available.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: McuNoPll
  长名称: ''
  描述: This parameter is set True, if the H/W does not have a PLL or the PLL circuitry is enabled
      after the power on without S/W intervention. In this case MCU_DistributePllClock API is
      disabled and  MCU_GetPllStatus returns MCU_PLL_STATUS_UNDEFINED. Otherwise, this
      parameters has to be set False                               TRUE : Mcu is not
      responsible for PLL related setup.                               FALSE: Mcu is
      responsible to setup PLLs.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: McuPerformResetApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the use of the function Mcu_PerformReset()
      TRUE : The function Mcu_PerformReset() is available                               FALSE:
      The function Mcu_PerformReset() not is available
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: McuVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information.
      TRUE : Mcu_GetVersionInfo() API is enabled                               FALSE:
      Mcu_GetVersionInfo() API is disabled
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: McuClearColdResetStatusApi
  长名称: ''
  描述: Pre-processor switch to enable/disable the API Mcu_ClearColdResetStatus.
      TRUE : Enables Mcu_ClearColdResetStatus API.                               FALSE:
      Disables Mcu_ClearColdResetStatus API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: McuGpt12SleepModeEnabled
  长名称: ''
  描述: |
    This parameter specifies if GPT12 peripheral goes into sleep mode when complete system is put
    into sleep mode.
                                 TRUE : Enables sleep mode for GPT12 peripheral
                                 FALSE: Disables sleep mode for GPT12 peripheral.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: McuGtmSleepModeEnabled
  长名称: ''
  描述: |
    This parameter specifies if GTM peripheral goes into sleep mode when complete system is put into
    sleep mode.
                                 TRUE : Enables sleep mode for GTM peripheral
                                 FALSE: Disables sleep mode for GTM peripheral.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: McuCcu60SleepModeEnabled
  长名称: ''
  描述: |
    This parameter specifies if CCU60 peripheral goes into sleep mode when complete system is put
    into sleep mode.
                                 TRUE : Enables sleep mode for CCU60 peripheral
                                 FALSE: Disables sleep mode for CCU60 peripheral.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: McuCcu61SleepModeEnabled
  长名称: ''
  描述: |
    This parameter specifies if CCU61 peripheral goes into sleep mode when complete system is put
    into sleep mode.
                                 TRUE : Enables sleep mode for CCU61 peripheral
                                 FALSE: Disables sleep mode for CCU61 peripheral.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: McuIfxLpmApi
  长名称: ''
  描述: |
    This parameter Enables/Disables availability of low power mode APIs defined by IFX namely
    Mcu_GetCpuIdleModeInitiator,
                                 Mcu_GetCpuState, Mcu_GetWakeupCause and Mcu_ClearWakeupCause..
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: McuIfxTrapApi
  长名称: ''
  描述: |
    This parameter Enables/Disables availability of trap related APIs defined by IFX namely
    Mcu_GetTrapCause,
                                 Mcu_SetTrapRequest and Mcu_ClearTrapRequest..
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: McuIfxCpuCcuconApi
  长名称: ''
  描述: This parameter Enables/Disables availability of Cpu Ccucon register update API defined by IFX
      namely Mcu_UpdateCpuCcuconReg.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: McuIfxDeInitApi
  长名称: ''
  描述: This parameter Enables/Disables availability of Mcu Deinitialization API - Mcu_DeInit.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: McuClockSourceFailureNotification
  长名称: ''
  描述: |
    This parameter availibility of Clock failure related DEMs notification function.
                                 ENABLED Clock failure related DEMs are reported
                                 DISABLED Clock failure related DEMs are not reported
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: McuSafetyEnable
  长名称: ''
  描述: Enables/Disables safety checks and features of MCU driver
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: McuInitCheckApi
  长名称: ''
  描述: Enables/Disables availability of Mcu_InitCheck API. Currently this parameter is disabled since
      Mcu_InitCheck API is not supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: McuOscAmpRegulationEnable
  长名称: ''
  描述: |
    Enables/Disables oscillator amplitude regulation
                               True: Oscillator amplitude regulation is Enabled.
                               False: Oscillator amplitude regulation is Disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: McuOscCapacitance0Enable
  长名称: ''
  描述: |
    Enables/Disables oscillator load capacitance0
                               True: Oscillator load capacitance0 is Enabled.
                               False: Oscillator load capacitance0 is Disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: McuOscCapacitance1Enable
  长名称: ''
  描述: |
    Enables/Disables oscillator load capacitance1
                               True: Oscillator load capacitance1 is Enabled.
                               False: Oscillator load capacitance1 is Disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: McuOscCapacitance2Enable
  长名称: ''
  描述: |
    Enables/Disables oscillator load capacitance2
                               True: Oscillator load capacitance2 is Enabled.
                               False: Oscillator load capacitance2 is Disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: McuOscCapacitance3Enable
  长名称: ''
  描述: |
    Enables/Disables oscillator load capacitance3
                               True: Oscillator load capacitance3 is Enabled.
                               False: Oscillator load capacitance3 is Disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: McuMainOscillatorFrequency
  长名称: ''
  描述: This parameter defines External crystal frequency value in MHz
  默认值: 20
  最小值: 4
  最大值: 40
- 
  序号: 26
  名称: McuSysClkFrequency
  长名称: ''
  描述: This parameter defines Sysclk frequency value in MHz
  默认值: 20
  最小值: 16
  最大值: 40
- 
  序号: 27
  名称: McuSystemModeCpuCore
  长名称: ''
  描述: This parameter defines core responsible to trigger system modes (sleep / standby). 
  默认值: CPU_SYSTEM_CORE0_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: McuIdleModeCpuCore
  长名称: ''
  描述: This parameter defines core responsible to trigger idle mode. 
  默认值: INDIVIDUAL_IDLE_CORES_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: McuStandbyEntryMode
  长名称: ''
  描述: |
    This parameter will define standby mode entry criteria.
                             STANDBY_ENTRY_REQ_SLEEP_SEL0: Entry to standby domain is through
    PMSWCR1.STBYEV.
                             STANDBY_ENTRY_ESR_SEL4: Entry to standby mode domain is through
    ESR1/NMI assertion.
  默认值: STANDBY_ENTRY_REQ_SLEEP_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: McuOscillatorMode
  长名称: ''
  描述: |
    This parameter selects ocillator mode.
                             EXT_CRYSTAL_CERAMIC_RES_MODE_SEL0: External Crystal or Ceramic
    resonator mode is selected.
                             EXT_INPUT_CLOCK_MODE_SEL2: External input clock source mode is
    selected.
                             OSC_DISABLED_MODE_SEL3: Oscillator is disabled.
  默认值: EXT_CRYSTAL_CERAMIC_RES_MODE_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: McuInitDeInitApiMode
  长名称: ''
  描述: This parameter selects the operating modes for MCU initialization, de-initialization APIs
  默认值: MCU_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 32
  名称: McuRuntimeApiMode
  长名称: ''
  描述: This parameter selects the operating modes for MCU runtime APIs
  默认值: MCU_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
```

### 2. McuModuleConfiguration

**描述**: This container contains the configuration (parameters) of the MCU driver

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuClockSrcFailureNotification
  长名称: ''
  描述: Enables/Disables clock failure notification. In case this feature is not supported by HW the
      setting should be disabled.This parameter doesn't have any influence on the generated
      code file
  默认值: DISABLED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuNumberOfMcuModes
  长名称: ''
  描述: This parameter shall represent the number of Modes available for the MCU. This parameter is
      disabled and is included here for completeness.
      calculation Formula = Number of configured McuModeSettingConf.
      Press the Calculate button beside the parameter to automatically update the field. This
      parameter doesn't have any influence on the generated
      code file
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 3
  名称: McuRamSectors
  长名称: ''
  描述: This parameter shall represent the number of RAM sectors configured for initialization for the
      MCU. This parameter is disabled and is included here for completeness.
      calculation Formula = Number of configured McuRamSectorSettingConf.
      Press the Calculate button beside the parameter to automatically update the field. This
      parameter doesn't have any influence on the generated
      code file
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: McuResetSetting
  长名称: ''
  描述: This parameter relates to the MCU specific reset configuration. This applies to the function
      Mcu_PerformReset, which performs a microcontroller reset using the hardware feature of
      the microcontroller. This parameter is disabled and is included here for completeness.
  默认值: 1
  最小值: 1
  最大值: 255
```

### 3. McuResetSettingConf

**描述**: This container contains the configuration (parameters) of the reset settings

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuESR0ResetConf
  长名称: ''
  描述: |
    This parameter defines the response of ESR0 reset request.
                                 MCU_ESR0_NO_RESET_SEL0 : No reset request is triggered.
                                 MCU_ESR0_SYSTEM_RESET_SEL1 : System reset is triggered.
                                 MCU_ESR0_APPLICATION_RESET_SEL2: Application reset request is
    triggered.
  默认值: MCU_ESR0_NO_RESET_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuESR1ResetConf
  长名称: ''
  描述: |
    This parameter defines the response of ESR1 reset request.
                                 MCU_ESR1_NO_RESET_SEL0  : No reset request is triggered.
                                 MCU_ESR1_SYSTEM_RESET_SEL1 : System reset request is triggered.
                                 MCU_ESR1_APPLICATION_RESET_SEL2: Application reset request is
    triggered.
  默认值: MCU_ESR1_NO_RESET_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuSWResetConf
  长名称: ''
  描述: |
    This parameter defines the response of SW reset request.
                                 MCU_SW_NO_RESET_SEL0 : No reset request is triggered.
                                 MCU_SW_SYSTEM_RESET_SEL1 : System reset request is triggered.
                                 MCU_SW_APPLICATION_RESET_SEL2: Application reset request is
    triggered.
  默认值: MCU_SW_NO_RESET_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: McuSMUResetConf
  长名称: ''
  描述: |
    This parameter defines the response of SMU reset request.
                                 MCU_SMU_NO_RESET_SEL0 : No reset request is triggered.
                                 MCU_SMU_SYSTEM_RESET_SEL1 : System reset request is triggered.
                                 MCU_SMU_APPLICATION_RESET_SEL2: Application reset request is
    triggered.
  默认值: MCU_SMU_NO_RESET_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: McuSTM0ResetConf
  长名称: ''
  描述: |
    This parameter defines the response of STM0 reset request.
                                 MCU_STM0_NO_RESET_SEL0 : No reset request is triggered.
                                 MCU_STM0_SYSTEM_RESET_SEL1 : System reset request is triggered.
                                 MCU_STM0_APPLICATION_RESET_SEL2: Application reset request is
    triggered.
  默认值: MCU_STM0_NO_RESET_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: McuSTM1ResetConf
  长名称: ''
  描述: |
    This parameter defines the response of STM1 reset request.
                                 MCU_STM1_NO_RESET_SEL0 : No reset request is triggered.
                                 MCU_STM1_SYSTEM_RESET_SEL1 : System reset request is triggered.
                                 MCU_STM1_APPLICATION_RESET_SEL2: Application reset request is
    triggered.
                                 The parameter will be disabled if STM1 timer doesn't exist on the
    HW.
  默认值: MCU_STM1_NO_RESET_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: McuSTM2ResetConf
  长名称: ''
  描述: |
    This parameter defines the response of STM2 reset request.
                                 MCU_STM2_NO_RESET_SEL0 : No reset request is triggered.
                                 MCU_STM2_SYSTEM_RESET_SEL1 : System reset request is triggered.
                                 MCU_STM2_APPLICATION_RESET_SEL2: Application reset request is
    triggered.
                                 The parameter will be disabled if STM2 timer doesn't exist on the
    HW.
  默认值: MCU_STM2_NO_RESET_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: McuSTM3ResetConf
  长名称: ''
  描述: |
    This parameter defines the response of STM3 reset request.
                                 MCU_STM3_NO_RESET_SEL0 : No reset request is triggered.
                                 MCU_STM3_SYSTEM_RESET_SEL1 : System reset request is triggered.
                                 MCU_STM3_APPLICATION_RESET_SEL2: Application reset request is
    triggered.
                                 The parameter will be disabled if STM3 timer doesn't exist on the
    HW.
  默认值: MCU_STM3_NO_RESET_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: McuSTM4ResetConf
  长名称: ''
  描述: |
    This parameter defines the response of STM4 reset request.
                                 MCU_STM4_NO_RESET_SEL0 : No reset request is triggered.
                                 MCU_STM4_SYSTEM_RESET_SEL1 : System reset request is triggered.
                                 MCU_STM4_APPLICATION_RESET_SEL2: Application reset request is
    triggered.
                                 The parameter will be disabled if STM4 timer doesn't exist on the
    HW.
  默认值: MCU_STM4_NO_RESET_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: McuSTM5ResetConf
  长名称: ''
  描述: |
    This parameter defines the response of STM5 reset request.
                                 MCU_STM5_NO_RESET_SEL0 : No reset request is triggered.
                                 MCU_STM5_SYSTEM_RESET_SEL1 : System reset request is triggered.
                                 MCU_STM5_APPLICATION_RESET_SEL2: Application reset request is
    triggered.
                                 The parameter will be disabled if STM5 timer doesn't exist on the
    HW.
  默认值: MCU_STM5_NO_RESET_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: McuSTM0ResetOnApplResetEnable
  长名称: ''
  描述: |
    This parameter specifies enabling of STM0 timer reset on occurance of application reset.
                               TRUE : STM0 timer is reset on application reset request.
                               FALSE: STM0 timer is not reset on application reset request.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: McuSTM1ResetOnApplResetEnable
  长名称: ''
  描述: |
    This parameter specifies enabling of STM1 timer reset on occurance of application reset.
                               TRUE : STM1 timer is reset on application reset request.
                               FALSE: STM1 timer is not reset on application reset request.
                               The parameter will be disabled if STM2 timer doesn't exist on the HW.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: McuSTM2ResetOnApplResetEnable
  长名称: ''
  描述: |
    This parameter specifies enabling of STM2 timer reset on occurance of application reset.
                               TRUE : STM2 timer is reset on application reset request.
                               FALSE: STM2 timer is not reset on application reset request.
                               The parameter will be disabled if STM2 timer doesn't exist on the HW.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: McuSTM3ResetOnApplResetEnable
  长名称: ''
  描述: |
    This parameter specifies enabling of STM3 timer reset on occurance of application reset.
                               TRUE : STM3 timer is reset on application reset request.
                               FALSE: STM3 timer is not reset on application reset request.
                               The parameter will be disabled if STM3 timer doesn't exist on the HW.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: McuSTM4ResetOnApplResetEnable
  长名称: ''
  描述: |
    This parameter specifies enabling of STM4 timer reset on occurance of application reset.
                               TRUE : STM4 timer is reset on application reset request.
                               FALSE: STM4 timer is not reset on application reset request.
                               The parameter will be disabled if STM4 timer doesn't exist on the HW.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: McuSTM5ResetOnApplResetEnable
  长名称: ''
  描述: |
    This parameter specifies enabling of STM5 timer reset on occurance of application reset.
                               TRUE : STM5 timer is reset on application reset request.
                               FALSE: STM5 timer is not reset on application reset request.
                               The parameter will be disabled if STM5 timer doesn't exist on the HW.
  默认值: true
  最小值: ''
  最大值: ''
```

### 4. McuTrapSettingConf

**描述**: This container defines the configuration (parameters) of the trap settings

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuCPU0ESR0TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR0 trap can be generated by CPU0.
                               TRUE : ESR0 trap request can be generated.
                               FALSE: ESR0 trap request can not be generated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuCPU1ESR0TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR0 trap can be generated by CPU1.
                               TRUE : ESR0 trap request can be generated.
                               FALSE: ESR0 trap request can not be generated.
                               The parameter will be disabled if CPU1 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuCPU2ESR0TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR0 trap can be generated by CPU2.
                               TRUE : ESR0 trap request can be generated.
                               FALSE: ESR0 trap request can not be generated.
                               The parameter will be disabled if CPU2 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: McuCPU3ESR0TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR0 trap can be generated by CPU3.
                               TRUE : ESR0 trap request can be generated.
                               FALSE: ESR0 trap request can not be generated.
                               The parameter will be disabled if CPU3 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: McuCPU4ESR0TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR0 trap can be generated by CPU4.
                               TRUE : ESR0 trap request can be generated.
                               FALSE: ESR0 trap request can not be generated.
                               The parameter will be disabled if CPU4 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: McuCPU5ESR0TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR0 trap can be generated by CPU5.
                               TRUE : ESR0 trap request can be generated.
                               FALSE: ESR0 trap request can not be generated.
                               The parameter will be disabled if CPU5 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: McuCPU0ESR1TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR1 trap can be generated by CPU0.
                               TRUE : ESR1 trap request can be generated.
                               FALSE: ESR1 trap request can not be generated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: McuCPU1ESR1TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR1 trap can be generated by CPU1.
                               TRUE : ESR1 trap request can be generated.
                               FALSE: ESR1 trap request can not be generated.
                               The parameter will be disabled if CPU1 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: McuCPU2ESR1TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR1 trap can be generated by CPU2.
                               TRUE : ESR1 trap request can be generated.
                               FALSE: ESR1 trap request can not be generated.
                               The parameter will be disabled if CPU2 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: McuCPU3ESR1TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR1 trap can be generated by CPU3.
                               TRUE : ESR1 trap request can be generated.
                               FALSE: ESR1 trap request can not be generated.
                               The parameter will be disabled if CPU3 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: McuCPU4ESR1TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR1 trap can be generated by CPU4.
                               TRUE : ESR1 trap request can be generated.
                               FALSE: ESR1 trap request can not be generated.
                               The parameter will be disabled if CPU4 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: McuCPU5ESR1TrapEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR1 trap can be generated by CPU5.
                               TRUE : ESR1 trap request can be generated.
                               FALSE: ESR1 trap request can not be generated.
                               The parameter will be disabled if CPU5 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: McuCPU0Trap2Enable
  长名称: ''
  描述: |
    This parameter specifies if Trap2 trap can be generated by CPU0.
                               TRUE : Trap2 trap request can be generated.
                               FALSE: Trap2 trap request can not be generated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: McuCPU1Trap2Enable
  长名称: ''
  描述: |
    This parameter specifies if Trap2 trap can be generated by CPU1.
                               TRUE : Trap2 trap request can be generated.
                               FALSE: Trap2 trap request can not be generated.
                               The parameter will be disabled if CPU1 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: McuCPU2Trap2Enable
  长名称: ''
  描述: |
    This parameter specifies if Trap2 trap can be generated by CPU2.
                               TRUE : Trap2 trap request can be generated.
                               FALSE: Trap2 trap request can not be generated.
                               The parameter will be disabled if CPU2 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: McuCPU3Trap2Enable
  长名称: ''
  描述: |
    This parameter specifies if Trap2 trap can be generated by CPU3.
                               TRUE : Trap2 trap request can be generated.
                               FALSE: Trap2 trap request can not be generated.
                               The parameter will be disabled if CPU3 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: McuCPU4Trap2Enable
  长名称: ''
  描述: |
    This parameter specifies if Trap2 trap can be generated by CPU4.
                               TRUE : Trap2 trap request can be generated.
                               FALSE: Trap2 trap request can not be generated.
                               The parameter will be disabled if CPU4 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: McuCPU5Trap2Enable
  长名称: ''
  描述: |
    This parameter specifies if Trap2 trap can be generated by CPU5.
                               TRUE : Trap2 trap request can be generated.
                               FALSE: Trap2 trap request can not be generated.
                               The parameter will be disabled if CPU5 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: McuCPU0SMUTrapEnable
  长名称: ''
  描述: |
    This parameter specifies if SMU trap can be generated by CPU0.
                               TRUE : SMU trap request can be generated.
                               FALSE: SMU trap request can not be generated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: McuCPU1SMUTrapEnable
  长名称: ''
  描述: |
    This parameter specifies if SMU trap can be generated by CPU1.
                               TRUE : SMU trap request can be generated.
                               FALSE: SMU trap request can not be generated.
                               The parameter will be disabled if CPU1 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: McuCPU2SMUTrapEnable
  长名称: ''
  描述: |
    This parameter specifies if SMU trap can be generated by CPU2.
                               TRUE : SMU trap request can be generated.
                               FALSE: SMU trap request can not be generated.
                               The parameter will be disabled if CPU2 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: McuCPU3SMUTrapEnable
  长名称: ''
  描述: |
    This parameter specifies if SMU trap can be generated by CPU3.
                               TRUE : SMU trap request can be generated.
                               FALSE: SMU trap request can not be generated.
                               The parameter will be disabled if CPU3 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: McuCPU4SMUTrapEnable
  长名称: ''
  描述: |
    This parameter specifies if SMU trap can be generated by CPU4.
                               TRUE : SMU trap request can be generated.
                               FALSE: SMU trap request can not be generated.
                               The parameter will be disabled if CPU4 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: McuCPU5SMUTrapEnable
  长名称: ''
  描述: |
    This parameter specifies if SMU trap can be generated by CPU5.
                               TRUE : SMU trap request can be generated.
                               FALSE: SMU trap request can not be generated.
                               The parameter will be disabled if CPU5 doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
```

### 5. McuEruGlobalConf

**描述**: This container contains the configuration (parameters) for Global ERU settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuEruInputFilterRegVal
  长名称: ''
  描述: This configuration parameter enables/disables the glitch filter and also the Glitch filter
      pre-divider and filters depth. (Register EIFILT). In case 0 is passed for bitfields
      which are reserved according to the TS, the value will be masked out.
  默认值: 0
  最小值: 0
  最大值: 4278321151
```

### 6. McuClockSettingConfig

**描述**: This container defines the configuration (parameters) for the MCU Clock settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuClockSettingId
  长名称: ''
  描述: The Id of this McuClockSettingConfig to be used as argument for the API call Mcu_InitClock.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 7. McuClockReferencePointConfig

**描述**: This container has sub-container for the configuration of Mcu Clock tree.

该容器没有参数。

### 8. McuSystemPllSettingConfig

**描述**: This container contains the configuration (parameters) for the System clock settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuPllInputSrcSelection
  长名称: ''
  描述: |
    This parameter will define PLL input source.
                                       BACKUP_CLOCK_SRC_SELECT_SEL0: Backup clock selected for
    oscillator watchdog clock source.
                                       OSC_CLOCK_SRC_SELECT_SEL1: Oscillator clock selected for
    oscillator watchdog clock source.
                                       SYSCLK_SRC_SELECT_SEL2: SYSCLK pin is selected as an input
    source for the system and peripheral PLLs
  默认值: OSC_CLOCK_SRC_SELECT_SEL1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuSystemPllPDivider
  长名称: ''
  描述: The parameter defines P divider value for System PLL.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 3
  名称: McuSystemPllNDivider
  长名称: ''
  描述: The parameter defines N divider value for System PLL.
  默认值: 29
  最小值: 0
  最大值: 127
- 
  序号: 4
  名称: McuSystemPllK2Divider
  长名称: ''
  描述: The parameter defines K2 divider value for System PLL.
  默认值: 1
  最小值: 0
  最大值: 7
- 
  序号: 5
  名称: McuSysPllK2DivStepUpChangeDelay
  长名称: ''
  描述: McuSysPllK2DivStepUpChangeDelay : This paramter configures the delay in micro-seconds for
      ramping up/down K2 div increment to reach configured system PLL frequency
  默认值: 10
  最小值: 5
  最大值: 100
- 
  序号: 6
  名称: McuSysPllK2DivStepDownChangeDelay
  长名称: ''
  描述: McuSysPllK2DivStepDownChangeDelay : This paramter configures the delay in micro-seconds for
      ramping up/down K2 div decrement to reach configured system PLL frequency
  默认值: 10
  最小值: 5
  最大值: 100
- 
  序号: 7
  名称: McuFmPllEnable
  长名称: ''
  描述: |
    This parameter specifies if Frequency Modulation for system PLL is enabled.
                                       TRUE : Frequency modulation for system PLL is enabled.
                                       FALSE: Frequency modulation for system PLL is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: McuFMPllModAmp
  长名称: ''
  描述: McuFMPllModAmp : It is the value for Modulation Amplitude for system PLL Frequency
      modulation.For any desired Modulation Amplitude, the corresponding bitfield MODCFG[9:0]
      of SCU_PLLCON2 can be calculated considering oscillator frequency
      McuMainOscillatorFrequency, McuPllPDivider and McuPllNDivider, according to this
      equation:MODCFG[9:0] = (64 * McuFMPllModAmp/100 *
      McuMainOscillatorFrequency/McuPllPDivider * McuPllNDivider/3.6) ; units: McuFMPllModAmp
      [%] , McuMainOscillatorFrequency [MHz].
  默认值: 1.25
  最小值: 0.0
  最大值: 2.0
- 
  序号: 9
  名称: McuClockReferencePointFrequency0
  长名称: ''
  描述: |
    This is the System PLL frequency for the specific instance of the McuClockReferencePointConfig
    container. The unit is Hz.
                                           Its value is calculated based on Oscillator frequency and
    P, N and K2 divider configuration
                                           Calculation Formula: Fpll =( (Fosc * (McuNDivider + 1)) /
    ((McuK2Divider+1)*(McuPDivider+1)))
                                           The McuClockReferencePointFrequency for NORMAL_MODE
    should be in range:
                                           20 - 300 MHz
                                           If McuClockDistributionInpClockSel is selected as
    BACKUP_INPUT_CLOCK_SRC_SELECT, then manually configure this clock to
                                           Fback = 100MHz.
  默认值: 3.0E8
  最小值: 2.0E7
  最大值: 3.0E8
```

### 9. McuPeripheralPllSettingConfig

**描述**: This container contains the configuration (parameters) for the Peripheral clock settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuPeripheralPllPDivider
  长名称: ''
  描述: The parameter defines P divider value for peripheral PLL.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: McuPeripheralPllNDivider
  长名称: ''
  描述: The parameter defines N divider value for peripheral PLL.
  默认值: 31
  最小值: 0
  最大值: 127
- 
  序号: 3
  名称: McuPeripheralPllK2Divider
  长名称: ''
  描述: The parameter defines K2 divider value for peripheral PLL.
  默认值: 1
  最小值: 0
  最大值: 7
- 
  序号: 4
  名称: McuPerPllK2DivStepUpChangeDelay
  长名称: ''
  描述: McuPerPllK2DivStepChangeDelay : This paramter configures the delay in micro-seconds for
      ramping up/down K2 div to reach configured peripheral PLL frequency
  默认值: 10
  最小值: 5
  最大值: 100
- 
  序号: 5
  名称: McuPerPllK2DivStepDownChangeDelay
  长名称: ''
  描述: McuPerPllK2DivStepChangeDelay : This paramter configures the delay in micro-seconds for
      ramping up/down K2 div to reach configured peripheral PLL frequency
  默认值: 10
  最小值: 5
  最大值: 100
- 
  序号: 6
  名称: McuPeripheralPllK3Divider
  长名称: ''
  描述: The parameter defines K3 divider value for peripheral PLL.
  默认值: 1
  最小值: 0
  最大值: 7
- 
  序号: 7
  名称: McuPerPllK3DivStepUpChangeDelay
  长名称: ''
  描述: McuPerPllK3DivStepChangeDelay : This paramter configures the delay in micro-seconds for
      ramping up/down K3 div to reach configured peripheral PLL frequency
  默认值: 10
  最小值: 5
  最大值: 100
- 
  序号: 8
  名称: McuPerPllK3DivStepDownChangeDelay
  长名称: ''
  描述: McuPerPllK3DivStepChangeDelay : This paramter configures the delay in micro-seconds for
      ramping up/down K3 div to reach configured peripheral PLL frequency
  默认值: 10
  最小值: 5
  最大值: 100
- 
  序号: 9
  名称: McuFreqSource1ClockDivSelect
  长名称: ''
  描述: |
    This parameter defines the peripheral clock divider selection.
                                       DIV_FACTOR_2_NOT_BYPASSED_SEL0: Divider factor of two is not
    bypassed. (Fpll1/2 = Fsource1 ).
                                       DIV_FACTOR_2_BYPASSED_SEL1: Divider factor of two is
    bypassed. (Fpll1 = Fsource1).
  默认值: DIV_FACTOR_2_NOT_BYPASSED_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: McuPll2DivSelect
  长名称: ''
  描述: |
    This parameter will define peripheral clock divider selection.
                                       MCU_K3_DIV_FACTOR_NOT_BYPASSED_SEL0: Divider factor for K3 is
    not bypassed.
                                       MCU_K3_DIV_FACTOR_BYPASSED_SEL1: Divider factor for K3 is
    bypassed.
  默认值: MCU_K3_DIV_FACTOR_NOT_BYPASSED_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: McuClockReferencePointFrequency1
  长名称: ''
  描述: |
    This is the peripheral PLL frequency for the specific instance of the
    McuClockReferencePointConfig container. It shall be given in Hz.
                                           Its value is given by Fpll =( (Fosc * (McuNDivider + 1))
    / ((McuK2Divider+1)*(McuPDivider+1))).
                                           McuClockReferencePointFrequency1 = Fpll if
    McuFreqSource1ClockDivSelect = DIV_FACTOR_2_BYPASSED_SEL1
                                           McuClockReferencePointFrequency1 = Fpll / 2 if
    McuFreqSource1ClockDivSelect = DIV_FACTOR_2_NOT_BYPASSED_SEL0
                                           The McuClockReferencePointFrequency for NORMAL_MODE
    should be in range:
                                           20 - 320 MHz
                                           If McuClockDistributionInpClockSel is selected as
    BACKUP_INPUT_CLOCK_SRC_SELECT, then manually configure the clock to 100 MHz.
  默认值: 1.6E8
  最小值: 2.0E7
  最大值: 3.2E8
- 
  序号: 12
  名称: McuClockReferencePointFrequency2
  长名称: ''
  描述: |
    This is the peripheral PLL frequency for the specific instance of the
    McuClockReferencePointConfig container. It shall be given in Hz.
                                           Its value is given by Fpll =( (Fosc * (McuNDivider + 1))
    / (1.6 * (McuK3Divider+1)*(McuPDivider+1))) if McuPll2DivSelect =
    MCU_K3_DIV_FACTOR_NOT_BYPASSED_SEL0 or
                                           Fpll =( (Fosc * (McuNDivider + 1)) / (1 *
    (McuK3Divider+1)*(McuPDivider+1))) if McuPll2DivSelect = MCU_K3_DIV_FACTOR_BYPASSED_SEL1
                                           The McuClockReferencePointFrequency for NORMAL_MODE
    should be in range:
                                           20 - 200 MHz
                                           If McuClockDistributionInpClockSel is selected as
    BACKUP_INPUT_CLOCK_SRC_SELECT, then manually configure this clock to
                                           Fback = 100MHz.
  默认值: 2.0E8
  最小值: 2.0E7
  最大值: 2.0E8
```

### 10. McuPllDistributionSettingConfig

**描述**: This container contains the configuration (parameters) for PLL Distribution and frequencies to
various HW modules within clock tree.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuClockDistributionInpClockSel
  长名称: ''
  描述: |
    This parameter defines clock source selection for clock distribution unit.
                                       BACKUP_INPUT_CLOCK_SRC_SELECT_SEL0: Backup clock is selected
    as an input to the clock distribution unit.
                                       PLL_INPUT_CLOCK_SRC_SELECT_SEL1: PLLx(x=0, 1, 2) is selected
    as an input clock to the clock distribution unit.
  默认值: PLL_INPUT_CLOCK_SRC_SELECT_SEL1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuLowPowerDivValue
  长名称: ''
  描述: |
    This parameter defines whether low power divider feature is enabled or disabled.
                                       LOW_POWER_DIVIDER_DISABLE_SEL0: Low power mode is disabled.
                                       LOW_POWER_DIVIDE_BY_30_SEL1: Low power mode clock divider is
    set to 30.
                                       LOW_POWER_DIVIDE_BY_60_SEL2: Low power mode clock divider is
    set to 60.
                                       LOW_POWER_DIVIDE_BY_120_SEL3: Low power mode clock divider is
    set to 120.
                                       LOW_POWER_DIVIDE_BY_240_SEL4: Low power mode clock divider is
    set to 240.
  默认值: LOW_POWER_DIVIDER_DISABLE_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuSRIFrequency
  长名称: ''
  描述: |
    This parameter defines the SRI frequency. SRI should always be in proportionate to
                                          McuClockReferencePointFrequency0. The unit is Hz.
  默认值: 300000000.0
  最小值: 1.0
  最大值: 3.0E8
- 
  序号: 4
  名称: McuCPU0Frequency
  长名称: ''
  描述: |
    This parameter defines the CPU0 frequency. The unit is Hz.
                                          McuCPU0Frequency configuration requires adherence to the
    following formula.
                                          McuCPU0Frequency = McuSRIFrequency * (64 - CPU0DIV) / 64.
  默认值: 300000000
  最小值: 1.0
  最大值: 3.0E8
- 
  序号: 5
  名称: McuCPU1Frequency
  长名称: ''
  描述: |
    This parameter defines the CPU1 frequency. The unit is Hz.
                                          McuCPU1Frequency configuration requires adherence to the
    following formula.
                                          McuCPU1Frequency = McuSRIFrequency * (64 - CPU1DIV) / 64.
                                          The parameter will be disabled if CPU1 doesn't exist on
    the HW.
  默认值: 3.0E8
  最小值: 1.0
  最大值: 3.0E8
- 
  序号: 6
  名称: McuCPU2Frequency
  长名称: ''
  描述: |
    This parameter defines the CPU2 frequency. The unit is Hz.
                                          McuCPU2Frequency configuration requires adherence to the
    following formula.
                                          McuCPU2Frequency = McuSRIFrequency * (64 - CPU2DIV) / 64.
                                          The parameter will be disabled if CPU2 doesn't exist on
    the HW.
  默认值: 3.0E8
  最小值: 1.0
  最大值: 3.0E8
- 
  序号: 7
  名称: McuCPU3Frequency
  长名称: ''
  描述: |
    This parameter defines the CPU3 frequency. The unit is Hz.
                                          McuCPU3Frequency configuration requires adherence to the
    following formula.
                                          McuCPU3Frequency = McuSRIFrequency * (64 - CPU3DIV) / 64.
                                          The parameter will be disabled if CPU3 doesn't exist on
    the HW.
  默认值: 3.0E8
  最小值: 1.0
  最大值: 3.0E8
- 
  序号: 8
  名称: McuCPU4Frequency
  长名称: ''
  描述: |
    This parameter defines the CPU4 frequency. The unit is Hz.
                                          McuCPU4Frequency configuration requires adherence to the
    following formula.
                                          McuCPU4Frequency = McuSRIFrequency * (64 - CPU4DIV) / 64.
                                          The parameter will be disabled if CPU4 doesn't exist on
    the HW.
  默认值: 3.0E8
  最小值: 1.0
  最大值: 3.0E8
- 
  序号: 9
  名称: McuCPU5Frequency
  长名称: ''
  描述: |
    This parameter defines the CPU5 frequency. The unit is Hz.
                                          McuCPU5Frequency configuration requires adherence to the
    following formula.
                                          McuCPU5Frequency = McuSRIFrequency * (64 - CPU5DIV) / 64.
                                          The parameter will be disabled if CPU5 doesn't exist on
    the HW.
  默认值: 3.0E8
  最小值: 1.0
  最大值: 3.0E8
- 
  序号: 10
  名称: McuSPBFrequency
  长名称: ''
  描述: |
    This parameter defines the SPB frequency. SPB should always be in proportionate to
                                          McuClockReferencePointFrequency0. The unit is Hz.
  默认值: 100000000.0
  最小值: 1.0
  最大值: 1.0E8
- 
  序号: 11
  名称: McuFSIFrequency
  长名称: ''
  描述: |
    This parameter specifies the intended target FSI frequency. The unit is Hz.
                                          FSI can be same as SRI.
                                          If FSI is intended to be half of SRI then SRIDIV must be
    either 1 or 2.
                                          If FSI is intended to be one third of SRI then SRIDIV must
    be either 1 or 2
                                          default : 100MHz (Max FSI clock value wrt fSRI @ 300Mhz.)
  默认值: 100000000
  最小值: 2.0E7
  最大值: 1.0E8
- 
  序号: 12
  名称: McuFSI2Frequency
  长名称: ''
  描述: |
    This parameter specifies the intended target FSI2 frequency. The unit is Hz.
                                          FSI2 can be same as SRI.
                                          If FSI2 is intended to be half of SRI then SRIDIV must be
    either 1 or 2.
                                          If FSI2 is intended to be one third of SRI then SRIDIV
    must be either 1 or 2
                                          default : 300MHz (Max FSI clock value wrt fSRI @ 300Mhz.)
  默认值: 3.0E8
  最小值: 1.0
  最大值: 3.0E8
- 
  序号: 13
  名称: McuReferenceFrequency1
  长名称: ''
  描述: |
    This parameter specifies the intended reference frequency 1 for MCDS.
                                          McuReferenceFrequency1 = McuClockReferencePointFrequency0
    / 24. The unit is Hz.
  默认值: 1.25E7
  最小值: 0.0
  最大值: 1.0E8
- 
  序号: 14
  名称: McuReferenceFrequency2
  长名称: ''
  描述: |
    This parameter specifies the intended reference frequency 2 for MCDS.
                                          McuReferenceFrequency2 = McuClockReferencePointFrequency1
    / 24. The unit is Hz.
  默认值: 6666667.0
  最小值: 0.0
  最大值: 1.0E8
- 
  序号: 15
  名称: McuBBBFrequency
  长名称: ''
  描述: This parameter specifies Back Bone Bus frequency. BBB frequency output can be stopped by
      configuring 0 to this configuration parameter. The unit is Hz.
  默认值: 150000000.0
  最小值: 0.0
  最大值: 1.5E8
- 
  序号: 16
  名称: McuErayClkEnable
  长名称: ''
  描述: |
    This parameter specifies if frequencies provided for ERAY module, fERAY is enabled or not
                                       TRUE : fERAY is enabled.
                                       FALSE: fERAY is disabled.
                                       The parameter will be disabled if FlexRay IP doesn't exist on
    the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: McuErayFrequency
  长名称: ''
  描述: |
    This parameter specifies Eray frequency.
                                    Resultant Eray frequency is always peripheral PLL frequency
    (McuClockReferencePointFrequency1) divided by fixed divider 2. Eray frequency has to be disabled
    when distribution source is selected as Back Up Frequency. The unit is Hz.
  默认值: 8.0E7
  最小值: 0.0
  最大值: 8.0E7
- 
  序号: 18
  名称: McuGTMFrequency
  长名称: ''
  描述: |
    This parameter specifies GTM peripheral frequency. The unit is Hz.
                                          If GTM peripheral frequency to be disabled, value 0 has to
    be configured to this configuration parameter.
                                          GTM frequency, if enabled, is derived by dividing the
    FSourceGTM frequency by one of the following factors. 1, 2, 3, 4, 5, 6, 8, 10, 12, 15.
                                          FSourceGTM is derived by following formula.
                                          if GTMDIV = 1 ; then FSourceGTM = McuSPBFrequency * 2,
                                          otherwise FSourceGTM = McuClockReferencePointFrequency0
                                          Hence, GTM has to be configured either equal to =
    McuSPBFrequency * 2 or fraction of McuClockReferencePointFrequency0. (Valid fraction values are
    2, 3, 4, 5, 6, 8, 10, 12 and 15.)
                                          The parameter will be disabled if GTM IP doesn't exist on
    the HW.
  默认值: 2.0E8
  最小值: 0.0
  最大值: 2.0E8
- 
  序号: 19
  名称: McuSTMFrequency
  长名称: ''
  描述: |
    This parameter specifies STM peripheral frequency. The unit is Hz.
                                          If STM peripheral frequency to be disabled, value 0 has to
    be configured to this configuration parameter.
                                          STM frequency, if enabled, has to be divisible by
    McuClockReferencePointFrequency0 with one of the following dividers. 1, 2, 3, 4, 5, 6, 8, 10, 12
    and 15. STM frequency can be slower or faster or equal to SPB frequency.
  默认值: 100000000.0
  最小值: 0.0
  最大值: 1.0E8
- 
  序号: 20
  名称: McuMscClockSourceSelection
  长名称: ''
  描述: |
    This parameter will define the input clock source for MSC peripheral.
                                       MSC_CLOCK_SOURCE_DISABLED_SEL0: MSC peripheral frequency is
    disabled.
                                       MSC_CLOCK_SOURCE_SOURCE1_SEL1:
    McuClockReferencePointFrequency1 is used as input clock source for MSC dividers.
                                       MSC_CLOCK_SOURCE_SOURCE2_SEL2:
    McuClockReferencePointFrequency2 is used as input clock source for MSC dividers.
  默认值: MSC_CLOCK_SOURCE_DISABLED_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: McuMscFrequency
  长名称: ''
  描述: |
    This parameter specifies MSC peripheral frequency. The unit is Hz.
                                       This parameter is applicable only if
    McuMscClockSourceSelection is not MSC_CLOCK_SOURCE_DISABLED.
                                       Target frequency to be configured should be perfectly
    divisible by one of the following dividers 1, 2, 3, 4, 5, 6, 8, 10, 12 and 15.
  默认值: 2.0E8
  最小值: 0.0
  最大值: 2.0E8
- 
  序号: 22
  名称: McuMCanClockSourceSelection
  长名称: ''
  描述: |
    This parameter will define the input clock source for MCAN peripheral.
                                       MCAN_CLOCK_SOURCE_DISABLED_SEL0: MCAN peripheral frequency is
    disabled.
                                       MCAN_CLOCK_SOURCE_MCANI_SEL1: fMCANI frequency is used as
    input clock source for MCAN peripheral.
                                       MCAN_CLOCK_SOURCE_OSC_SEL2: Main oscillator frequency is used
    as input clock source for MCAN peripheral.
  默认值: MCAN_CLOCK_SOURCE_DISABLED_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: McuMCanFrequency
  长名称: ''
  描述: |
    This parameter specifies MSC peripheral frequency. The unit is Hz.
                                          This parameter is applicable only if
    McuMCANClockSourceSelection is not MCAN_CLOCK_SOURCE_DISABLED_SEL0.
                                          Target frequency to be configured should be perfectly
    divisible by one of the following dividers 1, 2, 3, 4, 5, 6, 8, 10, 12 and 15
  默认值: 80000000.0
  最小值: 0.0
  最大值: 8.0E7
- 
  序号: 24
  名称: McuAscLinFastFrequency
  长名称: ''
  描述: |
    This parameter specifies ASCLIN peripheral frequency. The unit is Hz.
                                       If ASCLIN peripheral frequency for fast mode to be disabled,
    value 0 has to be configured to this configuration parameter.
                                       If not disabled, intended target frequency to be configured
    should be McuClockReferencePointFrequency2 perfectly divisible by one of the following dividers
    1, 2, 3, 4, 5, 6, 8, 10, 12 and 15
  默认值: 200000000.0
  最小值: 0.0
  最大值: 2.0E8
- 
  序号: 25
  名称: McuAscLinSlowClockSourceSelection
  长名称: ''
  描述: |
    This parameter specifies the input clock source for ASCLIN peripheral slow frequency.
                                       ASCLINS_CLOCK_SOURCE_DISABLED_SEL0: AscLin clock source is
    disabled.
                                       ASCLINS_CLOCK_SOURCE_ASCLINSI_SEL1: McuAscLinSlowFrequency is
    used as input clock source for ASCLIN dividers.
                                       ASCLINS_CLOCK_SOURCE_OSC0_SEL2: McuMainOscillatorFrequency is
    used as input clock source for ASCLIN dividers.
  默认值: ASCLINS_CLOCK_SOURCE_DISABLED_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: McuAscLinSlowFrequency
  长名称: ''
  描述: |
    This parameter specifies ASCLIN peripheral slow frequency. The unit is Hz.
                                          If ASCLIN peripheral frequency for fast mode to be
    disabled, value 0 has to be configured to this configuration parameter.
                                          If not disabled, intended target frequency to be
    configured should be McuClockReferencePointFrequency1 perfectly divisible by one of the
    following dividers 1, 2, 3, 4, 5, 6, 8, 10, 12 and 15
  默认值: 80000000.0
  最小值: 0.0
  最大值: 2.0E8
- 
  序号: 27
  名称: McuQspiClockSourceSelection
  长名称: ''
  描述: |
    This parameter will define the input clock source for QSPI peripheral.
                                       QSPI_CLOCK_SOURCE_DISABLED_SEL0: AscLin clock source is
    disabled.
                                       QSPI_CLOCK_SOURCE_SOURCE1_SEL1:
    McuClockReferencePointFrequency1 is used as input clock source for QSPI dividers.
                                       QSPI_CLOCK_SOURCE_SOURCE2_SEL2:
    McuClockReferencePointFrequency2 is used as input clock source for QSPI dividers.
  默认值: QSPI_CLOCK_SOURCE_DISABLED_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: McuQspiFrequency
  长名称: ''
  描述: |
    This parameter specifies QSPI peripheral frequency. The unit is Hz.
                                          Target frequency to be configured should be perfectly
    divisible by one of the following dividers 1, 2, 3, 4, 5, 6, 8, 10, 12 and 15
  默认值: 200000000.0
  最小值: 0.0
  最大值: 2.0E8
- 
  序号: 29
  名称: McuAdcFrequency
  长名称: ''
  描述: |
    This parameter specifies ADC peripheral frequency. The unit is Hz.
                                          This clock frequency is always equal to
    McuClockReferencePointFrequency1.
  默认值: 1.6E8
  最小值: 2.0E7
  最大值: 1.6E8
- 
  序号: 30
  名称: McuConvCtrlPhaseSynchConf
  长名称: ''
  描述: |
    This parameter defines the phase shift frequency divider for converter control block.
                                       This parameter is included here as this is a common across
    ADC and DSADC module.
                                       PHASE_SYNCH_CONST_ACTIVE_SEL0: Constant phase signal is
    active.
                                       PHASE_SYNCH_PER_FREQ_BY_2_SEL1: Phase synchronization is
    generated at fPER by 2.
                                       PHASE_SYNCH_PER_FREQ_BY_3_SEL2: Phase synchronization is
    generated at fPER by 3.
                                       PHASE_SYNCH_PER_FREQ_BY_4_SEL3: Phase synchronization is
    generated at fPER  by 4.
                                       PHASE_SYNCH_PER_FREQ_BY_5_SEL4: Phase synchronization is
    generated at fPER  by 5.
                                       PHASE_SYNCH_PER_FREQ_BY_6_SEL5: Phase synchronization is
    generated at fPER by 6.
                                       PHASE_SYNCH_PER_FREQ_BY_7_SEL6: Phase synchronization is
    generated at fPER by 7.
                                       PHASE_SYNCH_PER_FREQ_BY_8_SEL7: Phase synchronization is
    generated at fPER by 8.
                                       PHASE_SYNCH_PER_FREQ_BY_9_SEL8: Phase synchronization is
    generated at fPER by 9.
                                       PHASE_SYNCH_PER_FREQ_BY_10_SEL9: Phase synchronization is
    generated at fPER by 10.
                                       PHASE_SYNCH_PER_FREQ_BY_11_SEL10: Phase synchronization is
    generated at fPER by 11.
                                       PHASE_SYNCH_PER_FREQ_BY_12_SEL11: Phase synchronization is
    generated at fPER by 12.
                                       PHASE_SYNCH_PER_FREQ_BY_13_SEL12: Phase synchronization is
    generated at fPER by 13.
                                       PHASE_SYNCH_PER_FREQ_BY_14_SEL13: Phase synchronization is
    generated at fPER by 14.
                                       PHASE_SYNCH_PER_FREQ_BY_15_SEL14: Phase synchronization is
    generated at fPER by 15.
                                       PHASE_SYNCH_PER_FREQ_BY_16_SEL15: Phase synchronization is
    generated at fPER by 16.
  默认值: PHASE_SYNCH_CONST_ACTIVE_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: McuI2CFrequency
  长名称: ''
  描述: This parameter specifies I2C peripheral frequency. The unit is Hz. McuI2CFrequency has to be
      divisible by McuClockReferencePointFrequency2 with the divider values specified in HW TS
      specification.
  默认值: 6.6666667E7
  最小值: 0.0
  最大值: 1.0E8
- 
  序号: 32
  名称: McuEbuClkEnable
  长名称: ''
  描述: |
    This parameter specifies if frequencies provided for EBU module, fEBU is enabled or not
                                       TRUE : fEBU is enabled.
                                       FALSE: fEBU is disabled.
                                       The parameter will be disabled if EBU interface doesn't exist
    on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 33
  名称: McuEbuFrequency
  长名称: ''
  描述: |
    This parameter specifies EBU peripheral frequency. The unit is Hz.
                                          This clock frequency is always same as
    McuClockReferencePointFrequency1.
  默认值: 1.6E8
  最小值: 2.0E7
  最大值: 1.6E8
- 
  序号: 34
  名称: McuHsctFrequency
  长名称: ''
  描述: |
    This parameter specifies HSCT frequency. The unit is Hz.
                                          This clock frequency is always same Peripheral DCO
    frequency / 2.
  默认值: 1.0E7
  最小值: 0.0
  最大值: 4.0E8
- 
  序号: 35
  名称: McuHspdmClkEnable
  长名称: ''
  描述: |
    This parameter specifies if frequencies provided for HSPDM module, fHSPDM160 and fHSPDM320 are
    enabled or not
                                       TRUE : fHSPDM160 and fHSPDM320 are enabled.
                                       FALSE: fHSPDM160 and fHSPDM320 are disabled.
                                       The parameter will be disabled if High Speed Pulse Density
    Modulator IP doesn't exist on the HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 36
  名称: McuHspdm160Frequency
  长名称: ''
  描述: |
    This parameter specifies HSPDM160 peripheral frequency. The unit is Hz.
                                          This clock frequency is always equal to
    McuClockReferencePointFrequency1.
  默认值: 1.6E8
  最小值: 2.0E7
  最大值: 1.6E8
- 
  序号: 37
  名称: McuHspdm320Frequency
  长名称: ''
  描述: |
    This parameter specifies HSPDM320 peripheral frequency. The unit is Hz.
                                          This clock frequency is always equal to fPLL1 or
    fBACKUP(based on McuClockDistributionInpClockSel).
  默认值: 3.2E8
  最小值: 2.0E7
  最大值: 3.2E8
- 
  序号: 38
  名称: McuAdasFrequency
  长名称: ''
  描述: |
    This parameter Specifies the ADAS peripheral frequency in Hz.The ratio between ADAS frequency
    and McuClockReferencePointFrequency0 should be within the range as specified in the target
    specification.
                                    In order to facilitate the clearing of SRAM support hardware
    registers, this frequency is also configurable for non-ADAS devices. However, the default value
    for such devices is kept to 0, which disables the ADAS clock.
  默认值: 0.0
  最小值: 0.0
  最大值: 3.0E8
- 
  序号: 39
  名称: McuGEthFrequency
  长名称: ''
  描述: This parameter specifies Gigabit Ethernet peripheral frequency. McuGEthFrequency has to be
      divisible by McuClockReferencePointFrequency0 with the divider values specified in HW TS
      specification.  The unit is Hz.
  默认值: 1.5E8
  最小值: 0.0
  最大值: 1.5E8
- 
  序号: 40
  名称: McuMcanHFrequency
  长名称: ''
  描述: This parameter specifies MCANH peripheral frequency. McuMcanHFrequency has to be divisible by
      McuClockReferencePointFrequency0 with the divider values specified in HW TS
      specification. The unit is Hz.
  默认值: 100000000
  最小值: 0.0
  最大值: 1.0E8
```

### 11. McuExternalClockOutputConfig

**描述**: This container defines the configuration (parameters) for External clock out of the MCU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuExtClock0Enable
  长名称: ''
  描述: |
    This parameter specifies if external clock output 0 is enabled/disabled.
                                       TRUE : EXTCLK0 signal is available on external pad.
                                       FALSE: EXTCLK0 signal is not available on external pad.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuExtClockOutSel0
  长名称: ''
  描述: |
    This parameter will define clock source for external clock output 0.
                                       This parameter is included here as this is a common across
    ADC and DSADC module.
                                       FOUT_EXT_CLOCK0_SEL0: FOUT clock is selected.
                                       PLL0_EXT_CLOCK0_SEL1: PLL0 clock is selected.
                                       PLL1_EXT_CLOCK0_SEL2: PLL1 clock is selected.
                                       OSC0_EXT_CLOCK0_SEL3: OSC0 clock is selected.
                                       BACKUP_EXT_CLOCK0_SEL4: BACKUP clock is selected.
                                       PLL2_EXT_CLOCK0_SEL5: PLL2 clock is selected.
                                       BBB_EXT_CLOCK0_SEL6: BBB clock is selected.
                                       SRI_EXT_CLOCK0_SEL8: SRI clock is selected.
                                       SPB_EXT_CLOCK0_SEL9: SPB clock is selected.
                                       FSI_EXT_CLOCK0_SEL10: FSI clock is selected.
                                       STM_EXT_CLOCK0_SEL11: STM clock is selected.
                                       GTM_EXT_CLOCK0_SEL12: GTM clock is selected.
                                       TCK_EXT_CLOCK0_SEL13: TCK clock is selected.
                                       FSI2_EXT_CLOCK0_SEL14: FSI2 clock is selected.
                                       ERAY_MT0_EXT_CLOCK0_SEL15: ERAY_MT0 clock is selected.
                                       Note: ALT mode for corresponding port pin must be configured
    in port driver to observe the output at a port pin.
  默认值: FOUT_EXT_CLOCK0_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuExtClock1Enable
  长名称: ''
  描述: |
    This parameter specifies if external clock output 1 is enabled/disabled.
                                       TRUE : EXTCLK1 signal is available on external pad.
                                       FALSE: EXTCLK1 signal is not available on external pad.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: McuExtClock1Inverted
  长名称: ''
  描述: |
    This parameter specifies if external clock output 1 would be inverted or not.
                                       TRUE : output signal is inverted of the actual signal for
    external clock source1.
                                       FALSE: output signal is not inverted of the actual signal for
    external clock .
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: McuExtClockOutSel1
  长名称: ''
  描述: |
    This parameter will define clock source for external clock output 1.
                                       This parameter is included here as this is a common across
    ADC and DSADC module.
                                       FOUT_EXT_CLOCK1_SEL0: FOUT clock is selected.
                                       PLL0_EXT_CLOCK1_SEL1: PLL0 clock is selected.
                                       PLL1_EXT_CLOCK1_SEL2: PLL1 clock is selected.
                                       EBU_EXT_CLOCK1_SEL3:  EBU clock is selected.
                                       BACKUP_EXT_CLOCK1_SEL4: BACKUP clock is selected.
                                       MCAN_EXT_CLOCK1_SEL5: MCAN clock is selected.
                                       ADC_EXT_CLOCK1_SEL6:  ADC clock is selected.
                                       QSPI_EXT_CLOCK1_SEL7: QSPI clock is selected.
                                       SRI_EXT_CLOCK1_SEL8:  SRI clock is selected.
                                       SPB_EXT_CLOCK1_SEL9:  SPB clock is selected.
                                       I2C_EXT_CLOCK1_SEL10: I2C clock is selected.
                                       MSC_EXT_CLOCK1_SEL11: MSC clock is selected.
                                       ERAY_EXT_CLOCK1_SEL12: ERAY  clock is selected.
                                       ASCLINF_EXT_CLOCK1_SEL13: ASCLINF clock is selected.
                                       ASCLINS_EXT_CLOCK1_SEL14: ASCLINS clock is selected.
                                       OSCFL_EXT_CLOCK1_SEL15: OSCFL clock is selected.
                                       Note: ALT mode for corresponding port pin must be configured
    in port driver to observe the output at a port pin.
  默认值: FOUT_EXT_CLOCK1_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: McuFoutClockDiv
  长名称: ''
  描述: This parameter specifies reload value of the divider that generates fOUT out of
      fSPB (fOUT = fSPB/(McuExtClock1Div)). The divider itself is cleared each time bit EN1 is
      cleared. The value entered by user is decremented by 1 and programmed into EXTCON.DIV1
  默认值: 1
  最小值: 1
  最大值: 256
```

### 12. McuClockMonitorConfig

**描述**: This container defines the configuration for clock monitoring MCU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuPll0ClockMonEnable
  长名称: ''
  描述: |
    This parameter specifies if PLL0 monitoring is enabled/disabled.
                                       TRUE : PLL0 monitoring is Enabled.
                                       FALSE: PLL0 monitoring is Disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuPll1ClockMonEnable
  长名称: ''
  描述: |
    This parameter specifies if PLL1 monitoring is enabled/disabled.
                                       TRUE : PLL1 monitoring is Enabled.
                                       FALSE: PLL1 monitoring is Disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuPll2ClockMonEnable
  长名称: ''
  描述: |
    This parameter specifies if PLL2 monitoring is enabled/disabled.
                                       TRUE : PLL2 monitoring is Enabled.
                                       FALSE: PLL2 monitoring is Disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: McuSpbClockMonEnable
  长名称: ''
  描述: |
    This parameter specifies if SPB clock monitoring is enabled/disabled.
                                       TRUE : SPB clock monitoring is Enabled.
                                       FALSE: SPB clock monitoring is Disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: McuBackupClockMonEnable
  长名称: ''
  描述: |
    This parameter specifies if Backup clock monitoring is enabled/disabled.
                                       TRUE : Backup clock monitoring is Enabled.
                                       FALSE: Backup clock monitoring is Disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: McuBackupClockRangeMonEnable
  长名称: ''
  描述: |
    This parameter specifies if Backup clock range monitoring is enabled/disabled.
                                       TRUE : Backup clock range monitoring is Enabled.
                                       FALSE: Backup clock range monitoring is Disabled.
  默认值: false
  最小值: ''
  最大值: ''
```

### 13. McuClockReferencePoint

**描述**: This container defines a reference point in the Mcu Clock tree. It defines the frequencies which
then can be used by other modules as an input value. Lower multiplicity is 1, as even in the
simplest case (only one frequency is used), there is one frequency to be defined.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuClockRefSelection
  长名称: ''
  描述: This parameter selects the source of clock reference, based on which
      McuClockReferencePointFrequency is populated with frequency. If user selected
      MCU_USER_DEFINED_FREQUENCY, the value has to be entered by the user in parameter
      McuClockReferencePointFrequency.
  默认值: MCU_USER_DEFINED_FREQUENCY
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuClockReferencePointFrequency
  长名称: ''
  描述: This is the frequency for the specific instance of the McuClockReferencePoint container. It
      shall be given in Hz.
  默认值: 0.0
  最小值: 0.0
  最大值: 3.2E8
```

### 14. McuDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId symbolic name. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 15. McuModeSettingConf

**描述**: This container contains the configuration (parameters) for the Mode setting of the MCU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuMode
  长名称: ''
  描述: |
    The parameter represents the MCU Mode settings.
                                   0 : IDLE mode is selected.
                                   1 : SLEEP mode is selected.
                                   2: STANDBY mode is selected.
  默认值: 0
  最小值: 0
  最大值: 2
- 
  序号: 2
  名称: McuEvrcLPMOnSleepReqEnable
  长名称: ''
  描述: |
    This parameter enables EVRC low power mode in sleep mode.
                                 TRUE:  Entering into Low power mode for EVRC on sleep mode request
    is enabled.
                                 FALSE: Entering into Low power mode for EVRC on sleep mode request
    is disabled.
  默认值: false
  最小值: ''
  最大值: ''
```

### 16. McuStdbyModeSettingConf

**描述**: This container contains the configuration (parameters) for the MCU Standby Mode setting.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuStdbyModePortTriStateEnable
  长名称: ''
  描述: |
    This parameter specifies if pads is in tristate while in standby mode.
                                   TRUE: Tristate is enabled for port pins while in standby mode.
                                   FALSE: Tristate is disabled for port pins while in standby mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuStdbyModeESR0TriStateEnable
  长名称: ''
  描述: |
    This parameter specifies if ESR0 is in tristate while in standby mode.
                                   TRUE: Tristate is enabled for ESR0 while in standby mode.
                                   FALSE: Tristate is disabled for ESR0 while in standby mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuStdbyModeWakeupFromPORST
  长名称: ''
  描述: |
    This parameter specifies wakeup configramtion from PORST.
                                   TRUE: Wakeup from standby mode via PORST is enabled.
                                   FALSE: Wakeup from standby mode via PORST is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: McuStdbyModePORSTFilterEnable
  长名称: ''
  描述: |
    This parameter specifies if PORST digital filter is enabled or disabled.
                                   TRUE: PORST digital filter is enabled.
                                   FALSE: PORST digital filter is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: McuStdbyModeWakeupFromEVR
  长名称: ''
  描述: |
    This parameter specifies if wakeup from standby mode is enabled via EVR.
                                   TRUE: Wakeup from standby mode via EVR is enabled.
                                   FALSE: Wakeup from standby mode via EVR is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: McuStdbyModeWakeupFromSCR
  长名称: ''
  描述: |
    This parameter specifies if wakeup from standby mode via standby controller is enabled.
                                   TRUE: Wakeup from standby mode via standby controller is enabled.
                                   FALSE: Wakeup from standby mode via standby controller is
    disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: McuStdbyModeClkSelection
  长名称: ''
  描述: |
    The parameter specifies the active oscillator clock during standby mode operation.
                                       This parameter is kept disabled as Standby controller is not
    in scope of the Mcu driver and responsibility lies on user to configure it.
                                     SCR_CLOCK_SEL0 : Selecting this option configures
    PMSWCR4.SCRCLKSEL to 0. 100 MHz clock is enabled or disabled based on request from SCR in
    standby mode.
                                     SCR_CLOCK_SEL1 : Selecting this option configures
    PMSWCR4.SCRCLKSEL to 1. 100 MHz clock is always available.
  默认值: SCR_CLOCK_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: McuStdbyModeBlankingFilterDelay
  长名称: ''
  描述: |
    The parameter specifies the delay for blanking filter.
                                     DELAY_0_MS_SEL0 : No delay.
                                     DELAY_2_5_MS_SEL1 : selected delay is 2.5 ms.
                                     DELAY_5_MS_SEL2   : selected delay is 5 ms.
                                     DELAY_10_MS_SEL3  : selected delay is 10 ms.
                                     DELAY_20_MS_SEL4  : selected delay is 20 ms.
                                     DELAY_40_MS_SEL5  : selected delay is 40 ms.
                                     DELAY_80_MS_SEL6  : selected delay is 80 ms.
                                     DELAY_160_MS_SEL7 : selected delay is 160 ms.
                                     DELAY_320_MS_SEL8 : selected delay is 320 ms.
                                     DELAY_640_MS_SEL9 : selected delay is 640 ms.
                                     DELAY_1280_MS_SEL10 : selected delay is 1280 ms.
                                     DELAY_2560_MS_SEL11 : selected delay is 2560 ms.
                                     DELAY_5120_MS_SEL12 : selected delay is 5120 ms.
                                     DELAY_10240_MS_SEL13 : selected delay is 10240 ms.
                                     This can be set only when McuStdbyModeWakeupFromEVR = true.
  默认值: DELAY_0_MS_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: McuStdbyModeRamEnable
  长名称: ''
  描述: |
    This parameter enables dLMU0/dLMU1 powered up in sleep mode.
                                   MCU_STANDBYRAM_DISABLED_SEL0 : Standby ram is disabled.
                                   MCU_STANDBYRAM_CPU0_BLK0_SEL1 : standby ram is enabled as dLMU0
                                   MCU_STANDBYRAM_CPU0_BLK0_BLK1_SEL2 : standby ram is enabled as
    dLMU0 BLK0 and BLK1.
                                   MCU_STANDBYRAM_CPU1_BLK0_BLK1_SEL4 : standby ram is enabled as
    dLMU1 BLK0 and BLK1.
                                   MCU_STANDBYRAM_CPU0_CPU1_BLK0_BLK1_SEL7 : standby ram is enabled
    as dLMU0 and dLMU1.
                                   Only BLK0 addresses (start of dLMU0/1) are supported right in
    respective selections.
  默认值: MCU_STANDBYRAM_DISABLED_SEL0
  最小值: ''
  最大值: ''
```

### 17. McuStdbyModeESR0Conf

**描述**: This container defines the configuration (parameters) for ESR0 in standby mode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuStdbyModeESR0WakeupEnable
  长名称: ''
  描述: |
    This parameter specifies if wakeup from standby mode is enabled via ESR0.
                                     TRUE: Wakeup from standby mode through ESR0 is enabled.
                                     FALSE: Wakeup from standby mode through ESR0 is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuStdbyModeESR0FltEnable
  长名称: ''
  描述: |
    This parameter specifies if digital filter is enabled for ESR0 to wakeup from standby mode.
                                     TRUE : Digital filter is enabled for ESR0 wakeup from standby
    mode.
                                     FALSE: Digital filter is disabled for ESR0 wakeup from standby
    mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuStdbyModeESR0EdgeDetection
  长名称: ''
  描述: |
    The parameter specifies if trigger is generated on rising edge detection, falling edge detection
    or both.
                                       ESR0_TRIG_RISING_EDGE_SEL1: A trigger is generated on rising
    edge detection.
                                       ESR0_TRIG_FALLING_EDGE_SEL2: A trigger is generated on
    falling edge detection.
                                       ESR0_TRIG_RISING_FALLING_EDGE_SEL3: A trigger is generated on
    both rising edge detection and falling edge detection.
  默认值: ESR0_TRIG_RISING_EDGE_SEL1
  最小值: ''
  最大值: ''
```

### 18. McuStdbyModeESR1Conf

**描述**: This container contains the configuration (parameters) for the ESR1 configuration in Mcu standby
mode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuStdbyModeESR1WakeupEnable
  长名称: ''
  描述: |
    This parameter specifies if wakeup from standby mode is enabled via ESR1.
                                       TRUE: Wakeup from standby mode through ESR1 is enabled.
                                       FALSE: Wakeup from standby mode through ESR1 is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuStdbyModeESR1FltEnable
  长名称: ''
  描述: |
    This parameter specifies if digital filter is enabled for ESR1 to wakeup from standby mode.
                                       TRUE: Digital filter is enabled for ESR1 wakeup from standby
    mode.
                                       FALSE: Digital filter is disabled for ESR1 wakeup from
    standby mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuStdbyModeESR1EdgeDetection
  长名称: ''
  描述: |
    The parameter specifies if trigger is generated on rising edge detection, falling edge detection
    or both.
                                       ESR1_TRIG_RISING_EDGE_SEL1: A trigger is generated on rising
    edge detection.
                                       ESR1_TRIG_FALLING_EDGE_SEL2: A trigger is generated on
    falling edge detection.
                                       ESR1_TRIG_RISING_FALLING_EDGE_SEL3: A trigger is generated on
    both rising edge detection and falling edge detection.
  默认值: ESR1_TRIG_RISING_EDGE_SEL1
  最小值: ''
  最大值: ''
```

### 19. McuStdbyModePinAConf

**描述**: This container contains the configuration (parameters) for  standby PinA mode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuStdbyModePinAWakeupEnable
  长名称: ''
  描述: |
    This parameter specifies if wakeup from standby mode is enabled via PINA.
                                     TRUE: Wakeup from standby mode through PINA is enabled.
                                     FALSE: Wakeup from standby mode through PINA is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuStdbyModePinAFltEnable
  长名称: ''
  描述: |
    This parameter specifies if digital filter is enabled for PINA to wakeup from standby mode.
                                     TRUE: Digital filter is enabled for PINA wakeup from standby
    mode.
                                     FALSE: Digital filter is disabled for PINA wakeup from standby
    mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuStdbyModePinAEdgeDetection
  长名称: ''
  描述: |
    The parameter specifies if trigger is generated on rising edge detection, falling edge detection
    or both.
                                        PINA_TRIG_RISING_EDGE_SEL1: A trigger is generated on rising
    edge detection.
                                        PINA_TRIG_FALLING_EDGE_SEL2: A trigger is generated on
    falling edge detection.
                                        PINA_TRIG_RISING_FALLING_EDGE_SEL3: A trigger is generated
    on both rising edge detection and falling edge detection.
  默认值: PINA_TRIG_RISING_EDGE_SEL1
  最小值: ''
  最大值: ''
```

### 20. McuStdbyModePinBConf

**描述**: This container contains the configuration (parameters) for PinB MCU standby mode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuStdbyModePinBWakeupEnable
  长名称: ''
  描述: |
    This parameter specifies if wakeup from standby mode is enabled via PINB.
                                     TRUE : Wakeup from standby mode through PINB is enabled.
                                     FALSE: Wakeup from standby mode through PINB is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuStdbyModePinBFltEnable
  长名称: ''
  描述: |
    This parameter specifies if digital filter is enabled for PINB to wakeup from standby mode.
                                     TRUE: Digital filter is enabled for PINB wakeup from standby
    mode.
                                     FALSE: Digital filter is disabled for PINB wakeup from standby
    mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuStdbyModePinBEdgeDetection
  长名称: ''
  描述: |
    The parameter specifies if trigger is generated on rising edge detection, falling edge detection
    or both.
                                       PINB_TRIG_RISING_EDGE_SEL1: A trigger is generated on rising
    edge detection.
                                       PINB_TRIG_FALLING_EDGE_SEL2: A trigger is generated on
    falling edge detection.
                                       PINB_TRIG_RISING_FALLING_EDGE_SEL3: A trigger is generated on
    both rising edge detection and falling edge detection.
  默认值: PINB_TRIG_RISING_EDGE_SEL1
  最小值: ''
  最大值: ''
```

### 21. McuStdbyModeWakeupTimerConf

**描述**: This container contains the configuration (parameters) for Standby wakeup from timer.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuStdbyModeWakeupTimerEnable
  长名称: ''
  描述: |
    This parameter specifies specifies if wake up from low power mode is supported through wake up
    timer.
                                       TRUE: Wakeup from low power modes with wake up timer is
    enabled.
                                       FALSE: Wakeup from low power modes with wake up timer is
    disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuStdbyModeWakeupTimerValue
  长名称: ''
  描述: This parameter specifies the wakeup timer reload value
  默认值: 16777215
  最小值: 0
  最大值: 16777215
- 
  序号: 3
  名称: McuStdbyModeWakeupTimerClkDiv
  长名称: ''
  描述: |
    The parameter specifies the wakeup timer clock source selection.
                                       WUT_70KHZ_NO_DIV_CLK_SEL0: wake up timer runs on 70 KHz
    frequency .
                                       WUT_70KHZ_DIV_CLK_SEL1: wake up timer runs on 70 KHz
    frequency divided by 1024 divider value.
  默认值: WUT_70KHZ_NO_DIV_CLK_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: McuStdbyModeWakeupTimerMode
  长名称: ''
  描述: |
    The parameter specifies the wakeup timer clock source selection.
                                       WUT_AUTO_RELOAD_MODE_SEL0: selected counter starts running
    from McuStdbyModeWakeupTimerValue downwards direction. On counter underflow, the wakeup counter
    value is reloaded with McuStdbyModeWakeupTimerValue again
                                       WUT_AUTO_STOP_MODE_SEL1: counter starts running from
    McuStdbyModeWakeupTimerValue downwards direction. On counter underflow, wakeup timer stops
    running.
  默认值: WUT_AUTO_RELOAD_MODE_SEL0
  最小值: ''
  最大值: ''
```

### 22. McuStdbyModeVddVextConf

**描述**: This container contains the configuration (parameters) for the standby mode setting for VDD and VEXT
supply.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuStdbyModeEntryOnVEXTRampDown
  长名称: ''
  描述: |
    This parameter specifies if the standby entry on VEXT supply ramp down is enabled or not
                                   TRUE: standby mode entry on VEXT supply ramp-down is enabled.
                                   FALSE: standby mode entry on VEXT supply ramp-down is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuStdbyModeEntryOnVDDRampDown
  长名称: ''
  描述: |
    This parameter specifies if the standby entry on VDD supply ramp down is enabled or not
                                   TRUE: standby mode entry on VDD supply ramp-down is enabled.
                                   FALSE: standby mode entry on VDD supply ramp-down is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuStdbyModeVextUVThres
  长名称: ''
  描述: This parameter specifies the secondary under voltage threshold value of VEXT.(This parameter
      shall be configurable when McuStdbyModeEntryOnVEXTRampDown is enabled)
  默认值: 117
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: McuStdbyModeVextUMMonMode
  长名称: ''
  描述: |
    The parameter specifies the VEXT under voltage monitoring mode.(This parameter shall be
    configurable when   McuStdbyModeEntryOnVEXTRampDown is enabled)
                                       VEXT_UV_MON_MODE_SEL0: Under voltage monitoring is inactive.
                                       VEXT_UV_MON_MODE_SEL1: An under-voltage event is triggered
    when the threshold is crossed in a lower to higher voltage transition. Greater than or equal
    compare is used.
                                       VEXT_UV_MON_MODE_SEL2: An under-voltage event is triggered
    when the threshold is crossed in a higher to lower    voltage transition. Less than or equal
    compare is used.
                                       VEXT_UV_MON_MODE_SEL3: An under-voltage event is triggered
    when the threshold is crossed in either direction. Less than or equal compare is used.
  默认值: VEXT_UV_MON_MODE_SEL2
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: McuStdbyModeVddUVThres
  长名称: ''
  描述: This parameter specifies the secondary under voltage threshold value of VDD. (This parameter
      shall be configurable when McuStdbyModeEntryOnVDDRampDown is enabled)
  默认值: 184
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: McuStdbyModeVddUMMonMode
  长名称: ''
  描述: |
    The parameter specifies the VDD under voltage monitoring mode. (This parameter shall be
    configurable when McuStdbyModeEntryOnVDDRampDown is enabled)
                                       VDD_UV_MON_MODE_SEL0: Under voltage monitoring is inactive.
                                       VDD_UV_MON_MODE_SEL1: An under-voltage event is triggered
    when the threshold is crossed in a lower to higher voltage transition. Greater than or equal
    compare is used.
                                       VDD_UV_MON_MODE_SEL2: An under-voltage event is triggered
    when the threshold is crossed in a higher to lower voltage transition. Less than or equal
    compare is used.
                                       VDD_UV_MON_MODE_SEL3: An under-voltage event is triggered
    when the threshold is crossed in either direction. Less than or equal compare is used.
  默认值: VDD_UV_MON_MODE_SEL2
  最小值: ''
  最大值: ''
```

### 23. McuRamSectorSettingConf

**描述**: This container contains the configuration (parameters) for the RAM Sector setting.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuRamSectorSettingId
  长名称: ''
  描述: The Id of this McuRamSectorSettingConf to be used as argument for the API call
      Mcu_InitRamSection.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: McuRamDefaultValue
  长名称: ''
  描述: This parameter shall represent the Data pre-setting to be initialized
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: McuRamSectionBaseAddress
  长名称: ''
  描述: This parameter shall represent the MCU RAM section base address
  默认值: 1879048192
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: McuRamSectionSize
  长名称: ''
  描述: This parameter represents the MCU RAM Section size in bytes.
  默认值: 8
  最小值: 0
  最大值: 4294967295
```

### 24. McuGpt12PrescalerConf

**描述**: This container contains the prescalar configuration (parameters) for GPT12 Timer.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Gpt1BlockPrescalerSel
  长名称: ''
  描述: |
    The parameter specifies the divider for the clock of GPT1 Block.
                                GPT1_BLOCK_NOT_USED : GPT1 Timer Block is not used.
                                GPT1_PRESCALING_FACTOR_4 : GPT1 Timer Block is clocked at FGPT BY 4.
                                GPT1_PRESCALING_FACTOR_8 : GPT1 Timer Block is clocked at FGPT BY 8.
                                GPT1_PRESCALING_FACTOR_16 : GPT1 Timer Block is clocked at FGPT BY
    16.
                                GPT1_PRESCALING_FACTOR_32 : GPT1 Timer Block is clocked at FGPT BY
    32.
  默认值: GPT1_BLOCK_NOT_USED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Gpt2BlockPrescalerSel
  长名称: ''
  描述: |
    The parameter specifies the divider for the clock of GPT2 Block.
                                GPT2_BLOCK_NOT_USED : GPT2 Block is not used.
                                GPT2_PRESCALING_FACTOR_2 : GPT2 Timer Block is clocked at FGPT BY 2.
                                GPT2_PRESCALING_FACTOR_4 : GPT2 Timer Block is clocked at FGPT BY 4.
                                GPT2_PRESCALING_FACTOR_8 : GPT2 Timer Block is clocked at FGPT BY 8.
                                GPT2_PRESCALING_FACTOR_16 : GPT2 Timer Block is clocked at FGPT BY
    16.
  默认值: GPT2_BLOCK_NOT_USED
  最小值: ''
  最大值: ''
```

### 25. GtmGlobalConfiguration

**描述**: This container contains the configuration (parameters) for Global GTM settings.

该容器没有参数。

### 26. McuGtmClockManagementConf

**描述**: This container contains the configuration (parameters) for GTM Clock configurations.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmCmuGlobalClockNumerator
  长名称: ''
  描述: This parameter specifies the GTM global numerator value for configurable clock and fixed clock
  默认值: 1
  最小值: 1
  最大值: 16777215
- 
  序号: 2
  名称: GtmCmuGlobalClockDenominator
  长名称: ''
  描述: This parameter specifies the GTM global denominator value for configurable clock and fixed
      clock
  默认值: 1
  最小值: 1
  最大值: 16777215
```

### 27. GtmFixedClockSetting

**描述**: This container contains the configuration (parameters) for GTM Fixed Clock settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmCmuFixedClockEnable
  长名称: ''
  描述: |
    This parameter specifies enable of fixed clock.
                                       TRUE: CMU fixed clock is enabled
                                       FALSE: CMU fixed clock is disabled
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GtmCmuFixedClockSel
  长名称: ''
  描述: |
    The parameter specifies the divider for the fixed clock.
                                       CMU_GLOBAL_CLOCK_SEL0  : Global clock divider is selected.
                                       CMU_CLOCK0_SEL1 :  clock0 divider is selected.
                                       CMU_CLOCK1_SEL2 :  clock1 divider is selected.
                                       CMU_CLOCK2_SEL3 :  clock2 divider is selected.
                                       CMU_CLOCK3_SEL4 :  clock3 divider is selected.
                                       CMU_CLOCK4_SEL5 :  clock4 divider is selected.
                                       CMU_CLOCK5_SEL6 :  clock5 divider is selected.
                                       CMU_CLOCK6_SEL7 :  clock6 divider is selected.
                                       CMU_CLOCK7_SEL8 :  clock7 divider is selected.
  默认值: CMU_GLOBAL_CLOCK_SEL0
  最小值: ''
  最大值: ''
```

### 28. GtmConfigClockSetting

**描述**: This container contains the configuration (parameters) for GTM configuration clock settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmCmuConfigClock0Enable
  长名称: ''
  描述: |
    This parameter specifies enable of configurable Clock0.
                                       TRUE: CMU configurable Clock0 enabled
                                       FALSE: CMU configurable Clock0 is disabled
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GtmCmuConfigClock0Div
  长名称: ''
  描述: This parameter specifies the configurable Clock0 divider value
  默认值: 0
  最小值: 0
  最大值: 16777215
- 
  序号: 3
  名称: GtmCmuConfigClock1Enable
  长名称: ''
  描述: |
    This parameter specifies enable of configurable Clock1.
                                       TRUE : CMU configurable Clock1 enabled
                                       FALSE: CMU configurable Clock1 is disabled
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: GtmCmuConfigClock1Div
  长名称: ''
  描述: This parameter specifies the configurable Clock1 divider value
  默认值: 0
  最小值: 0
  最大值: 16777215
- 
  序号: 5
  名称: GtmCmuConfigClock2Enable
  长名称: ''
  描述: |
    This parameter specifies enable of configurable Clock2.
                                       TRUE: CMU configurable Clock2 enabled.
                                       FALSE: CMU configurable Clock2 is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: GtmCmuConfigClock2Div
  长名称: ''
  描述: This parameter specifies the configurable Clock2 divider value
  默认值: 0
  最小值: 0
  最大值: 16777215
- 
  序号: 7
  名称: GtmCmuConfigClock3Enable
  长名称: ''
  描述: |
    This parameter specifies enable of configurable Clock3.
                                       TRUE: CMU configurable Clock3 enabled.
                                       FALSE: CMU configurable Clock3 is disabled
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: GtmCmuConfigClock3Div
  长名称: ''
  描述: This parameter specifies the configurable Clock3 divider value
  默认值: 0
  最小值: 0
  最大值: 16777215
- 
  序号: 9
  名称: GtmCmuConfigClock4Enable
  长名称: ''
  描述: |
    This parameter specifies enable of configurable Clock4.
                                       TRUE: CMU configurable Clock4 enabled.
                                       FALSE: CMU configurable Clock4 is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: GtmCmuConfigClock4Div
  长名称: ''
  描述: This parameter specifies the configurable Clock4 divider value
  默认值: 0
  最小值: 0
  最大值: 16777215
- 
  序号: 11
  名称: GtmCmuConfigClock5Enable
  长名称: ''
  描述: |
    This parameter specifies enable of configurable Clock5.
                                       TRUE: CMU configurable Clock5 enabled.
                                       FALSE: CMU configurable Clock5 is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: GtmCmuConfigClock5Div
  长名称: ''
  描述: This parameter specifies the configurable Clock5 divider value
  默认值: 0
  最小值: 0
  最大值: 16777215
- 
  序号: 13
  名称: GtmCmuConfigClock6Enable
  长名称: ''
  描述: |
    This parameter specifies enable of configurable Clock6.
                                       TRUE: CMU configurable Clock6 enabled.
                                       FALSE: CMU configurable Clock6 is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: GtmCmuConfigClock6Div
  长名称: ''
  描述: This parameter specifies the configurable Clock6 divider value
  默认值: 0
  最小值: 0
  最大值: 16777215
- 
  序号: 15
  名称: GtmCmuConfigClock7Enable
  长名称: ''
  描述: |
    This parameter specifies enable of configurable Clock7.
                                       TRUE: CMU configurable Clock7 enabled.
                                       FALSE: CMU configurable Clock7 is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: GtmCmuConfigClock7Div
  长名称: ''
  描述: This parameter specifies the configurable Clock7 divider value
  默认值: 0
  最小值: 0
  最大值: 16777215
```

### 29. GtmExtClockSetting

**描述**: This container contains the configuration (parameters) for GTM external clock settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmCmuExtClock0Enable
  长名称: ''
  描述: |
    This parameter specifies if External Clock0 is enabled or not.
                                      TRUE : CMU External Clock0 is enabled.
                                      FALSE: CMU External Clock0 is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GtmCmuExtClock0Numerator
  长名称: ''
  描述: This parameter specifies the numerator value for external Clock0
  默认值: 1
  最小值: 1
  最大值: 16777215
- 
  序号: 3
  名称: GtmCmuExtClock0Denominator
  长名称: ''
  描述: This parameter specifies the denominator value for external Clock0
  默认值: 1
  最小值: 1
  最大值: 16777215
- 
  序号: 4
  名称: GtmCmuExtClock1Enable
  长名称: ''
  描述: |
    This parameter specifies if External Clock1 is enabled or not.
                                      TRUE : CMU External Clock1 is enabled.
                                      FALSE: CMU External Clock1 is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: GtmCmuExtClock1Numerator
  长名称: ''
  描述: This parameter specifies the numerator value for external Clock1
  默认值: 1
  最小值: 1
  最大值: 16777215
- 
  序号: 6
  名称: GtmCmuExtClock1Denominator
  长名称: ''
  描述: This parameter specifies the denominator value for external Clock1
  默认值: 1
  最小值: 1
  最大值: 16777215
- 
  序号: 7
  名称: GtmCmuExtClock2Enable
  长名称: ''
  描述: |
    This parameter specifies if External Clock2 is enabled or not.
                                      TRUE : CMU External Clock2 is enabled.
                                      FALSE: CMU External Clock2 is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: GtmCmuExtClock2Numerator
  长名称: ''
  描述: This parameter specifies the numerator value for external Clock2
  默认值: 1
  最小值: 1
  最大值: 16777215
- 
  序号: 9
  名称: GtmCmuExtClock2Denominator
  长名称: ''
  描述: This parameter specifies the denominator value for external Clock2
  默认值: 1
  最小值: 1
  最大值: 16777215
```

### 30. GtmClusterConf

**描述**: This container contains the configuration (parameters) for GTM Cluster settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmCmuClusterInputClockDividerEnable
  长名称: ''
  描述: |
    This configuration parameter enables/disables the dividing of fGTM to CMU for cluster-x.
                                       CLS_CLK_CFG_DISABLED_SEL0: Cluster x is disabled
                                       CLS_CLK_CFG_ENABLED_WITHOUT_DIV_SEL1: Cluster x is enabled
    without clock divider.
                                       CLS_CLK_CFG_ENABLED_WITH_DIV_SEL2: Cluster x is enabled with
    clock divider.
                                       The configuration value CLS0_CLK_DIV defines the primary
    input clock period for CMU.
                                       If CLS0_CLK_DIV is configured to a value 0b10 (i.e. clock
    divider 2), the
                                       maximum CMU clock frequency for all other cluster c=1..n is
    also limited
                                       to configured CMU clock frequency of cluster 0.
                                       NOTE: For the Clusters greater than 4, (only 100MHz capable),
    the allowed settings for the CLS_CLK_DIV are
                                       00 and 10 (clock divider 2).
  默认值: CLS_CLK_CFG_ENABLED_WITH_DIV_SEL2
  最小值: ''
  最大值: ''
```

### 31. GtmClusterConfClockSetting

**描述**: This container contains the configuration (parameters) for GTM cluster clock settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmClusterConfClock0Src
  长名称: ''
  描述: |
    The parameter specifies specifies the input clock source for current GTM cluster sub peripheral
    using configurable Clock0.
                                         CMU_CONF_CLOCK0_SEL0: Configurable clock-x is used for
    clock.
                                         CMU_CONF_CLOCK8_SEL1: Configurable clock8 is used for
    clock.
                                         EXT_CAPTURE_SEL2: External capture source is used for
    clock.
  默认值: CMU_CONF_CLOCK0_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GtmClusterConfClock1Src
  长名称: ''
  描述: |
    The parameter specifies specifies the input clock source for current GTM
                                         cluster sub peripheral using configurable Clock1.
                                         CMU_CONF_CLOCK1_SEL0: Configurable clock1 is used for
    clock.
                                         CMU_CONF_CLOCK8_SEL1: Configurable clock8 is used for
    clock.
                                         EXT_CAPTURE_SEL2: External capture source is used for
    clock.
  默认值: CMU_CONF_CLOCK1_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GtmClusterConfClock2Src
  长名称: ''
  描述: |
    The parameter specifies specifies the input clock source for current GTM
                                         cluster sub peripheral using configurable Clock2.
                                         CMU_CONF_CLOCK2_SEL0: Configurable clock1 is used for
    clock.
                                         CMU_CONF_CLOCK8_SEL1: Configurable clock8 is used for
    clock.
                                         EXT_CAPTURE_SEL2: External capture source is used for
    clock.
  默认值: CMU_CONF_CLOCK2_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: GtmClusterConfClock3Src
  长名称: ''
  描述: |
    The parameter specifies specifies the input clock source for current
                                      GTM cluster sub peripheral using configurable Clock3.
                                         CMU_CONF_CLOCK3_SEL0: Configurable clock3 is used for
    clock.
                                         CMU_CONF_CLOCK8_SEL1: Configurable clock8 is used for
    clock.
                                         EXT_CAPTURE_SEL2: External capture source is used for
    clock.
  默认值: CMU_CONF_CLOCK3_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: GtmClusterConfClock4Src
  长名称: ''
  描述: |
    The parameter specifies specifies the input clock source for current
                                      GTM cluster sub peripheral using configurable Clock4.
                                         CMU_CONF_CLOCK4_SEL0: Configurable clock4 is used for
    clock.
                                         CMU_CONF_CLOCK8_SEL1: Configurable clock8 is used for
    clock.
                                         EXT_CAPTURE_SEL2: External capture source is used for
    clock.
  默认值: CMU_CONF_CLOCK4_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: GtmClusterConfClock5Src
  长名称: ''
  描述: |
    The parameter specifies specifies the input clock source for current
                                      GTM cluster sub peripheral using configurable Clock4.
                                         CMU_CONF_CLOCK5_SEL0: Configurable clock5 is used for
    clock.
                                         CMU_CONF_CLOCK8_SEL1: Configurable clock8 is used for
    clock.
                                         EXT_CAPTURE_SEL2: External capture source is used for
    clock.
  默认值: CMU_CONF_CLOCK5_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: GtmClusterConfClock6Src
  长名称: ''
  描述: |
    The parameter specifies specifies the input clock source for current
                                      GTM cluster sub peripheral using configurable Clock6.
                                         CMU_CONF_CLOCK6_SEL0: Configurable clock6 is used for
    clock.
                                         CMU_CONF_CLOCK8_SEL1: Configurable clock8 is used for
    clock.
                                         EXT_CAPTURE_SEL2: External capture source is used for
    clock.
  默认值: CMU_CONF_CLOCK6_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: GtmClusterConfClock7Src
  长名称: ''
  描述: |
    The parameter specifies specifies the input clock source for current
                                      GTM cluster sub peripheral using configurable Clock7.
                                         CMU_CONF_CLOCK7_SEL0: Configurable clock7 is used for
    clock.
                                         CMU_CONF_CLOCK8_SEL1: Configurable clock8 is used for
    clock.
                                         EXT_CAPTURE_SEL2: External capture source is used for
    clock.
  默认值: CMU_CONF_CLOCK7_SEL0
  最小值: ''
  最大值: ''
```

### 32. GtmClusterFixedClockSetting

**描述**: This container contains the configuration (parameters) for GTM cluster fixed clock settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmClusterFixedClockSrc
  长名称: ''
  描述: |
    The parameter specifies specifies the input clock source for current
                                         GTM cluster sub peripheral using fixe Clock.
                                         CMU_FIXED_CLOCK0_SEL0: Fixed clock0 is used for clock.
                                         CMU_CONF_CLOCK8_SEL1: Configurable clock8 is used for
    clock.
                                         EXT_CAPTURE_SEL2: External capture source is used for
    clock.
  默认值: CMU_FIXED_CLOCK0_SEL0
  最小值: ''
  最大值: ''
```

### 33. GtmTbuChannelConf

**描述**: This container contains the configuration (parameters) for GTM TBU channel settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmTbuChannelEnable
  长名称: ''
  描述: |
    This parameter specifies enable TBU channel.
                                         TRUE: Channel is enabled
                                         FALSE: Channel is disabled
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GtmTbuChClockSourceSelection
  长名称: ''
  描述: |
    This parameter will defines configurable clock source selection for the corresponding TBU
    channel.
                                       CMU_CLOCK0_SEL0 : Clock0 is selected as source.
                                       CMU_CLOCK1_SEL1 : Clock1 is selected as source.
                                       CMU_CLOCK2_SEL2 : Clock2 is selected as source.
                                       CMU_CLOCK3_SEL3 : Clock3 is selected as source.
                                       CMU_CLOCK4_SEL4 : Clock4 is selected as source.
                                       CMU_CLOCK5_SEL5 : Clock5 is selected as source.
                                       CMU_CLOCK6_SEL6 : Clock6 is selected as source.
                                       CMU_CLOCK7_SEL7 : Clock7 is selected as source.
  默认值: CMU_CLOCK0_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GtmTbuChResolutionSel
  长名称: ''
  描述: |
    This parameter defines the resolution of time base values given by TBU_CH0_BASE.
                                       TBU_CH_LOWER_COUNT_BITS_SEL0 : 0 __ 23 bits of TBU_CH0_BASE
    is considered.
                                       TBU_CH_UPPER_COUNT_BITS_SEL1 : 3 __ 26 bits of TBU_CH0_BASE
    is considered.
  默认值: TBU_CH_LOWER_COUNT_BITS_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: GtmTbuChMode
  长名称: ''
  描述: |
    This parameter defines TBU channle run mode.
                                       FREE_RUNNING_COUNTER_SEL0 : TBU channel is in free running
    counter mode.
                                       FORWARD_BACKWARD_SEL1     : TBU channel is in forward
    backward counter mode. (default for TBU channel 3)
  默认值: FREE_RUNNING_COUNTER_SEL0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: GtmTbuChModuloCntrSel
  长名称: ''
  描述: |
    This parameter defines TBU channle run mode.
                                       TBU_CH1_SEL0 : TBU_CH1 values used.
                                       TBU_CH2_SEL1 : TBU_CH2 values used.
  默认值: TBU_CH1_SEL0
  最小值: ''
  最大值: ''
```

### 34. GtmTomGlobalConf

**描述**: This container contains the configuration (parameters) for GTM TOM unit global settings.

该容器没有参数。

### 35. GtmTomGroupConf

**描述**: This container contains the configuration (parameters) for GTM TOM group settings.

该容器没有参数。

### 36. GtmTomActionTimeBaseUnitConf

**描述**: This container contains the configuration (parameters) for GTM TOM group time base settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmTomActionTimeBaseSelection
  长名称: ''
  描述: |
    This parameter specifies time base selected to compare with value configured in
    GtmTomActionTimeBaseValue.
                                             TOM_ACT_TB_TBU_TS0 : TBU_TS0 is used as reference time
    base for TOM group.
                                             TOM_ACT_TB_TBU_TS1 : TBU_TS1 is used as reference time
    base for TOM group.
                                             TOM_ACT_TB_TBU_TS2 : TBU_TS2 is used as reference time
    base for TOM group.
  默认值: TOM_ACT_TB_TBU_TS0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GtmTomActionTimeBaseValue
  长名称: ''
  描述: This parameter specifies the time base value for TOM group channel level trigger
  默认值: 1
  最小值: 1
  最大值: 16777215
```

### 37. GtmTomChannelConf

**描述**: This container contains the configuration (parameters) for GTM TOM channel settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmTomChResetCn0OnTriggerEnable
  长名称: ''
  描述: |
    This parameter specifies enables/disables Tom channel counter Cn0 value is reset on global
    trigger from any of the trigger sources.
                                         TRUE: Resetting of Tom channel Cn0 on global trigger from
    any trigger source is enabled.
                                         FALSE: Resetting of Tom channel Cn0 on global trigger from
    any trigger source is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GtmTomChInternalTriggerEnable
  长名称: ''
  描述: |
    This parameter specifies enables/disables internal trigger from channel 0 of the corresponding
    group channel number.
                                         TRUE: Enable internal trigger from channel 0 or 8 (based on
    the TGC a channel belong to).
                                         FALSE: Disable internal trigger from channel 0 or 8 (based
    on the TGC a channel belong to)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GtmTimerPortPinSelect
  长名称: ''
  描述: This parameter decides the output port and pin for the GTM timer.
  默认值: NONE
  最小值: ''
  最大值: ''
```

### 38. GtmAtomGlobalConf

**描述**: This container contains the configuration (parameters) for GTM ATOM unit global settings.

该容器没有参数。

### 39. GtmAtomGroupConf

**描述**: This container contains the configuration (parameters) for GTM ATOM group settings.

该容器没有参数。

### 40. GtmAtomActionTimeBaseUnitConf

**描述**: This container contains the configuration (parameters) for GTM ATOM group time base settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmAtomActionTimeBaseSelection
  长名称: ''
  描述: |
    This parameter specifies time base selected to compare with value configured in
    GtmAtomActionTimeBaseValue.
                                           ATOM_ACT_TB_TBU_TS0 : TBU_TS0 is used as reference time
    base for ATOM group.
                                           ATOM_ACT_TB_TBU_TS1 : TBU_TS1 is used as reference time
    base for ATOM group.
                                           ATOM_ACT_TB_TBU_TS2 : TBU_TS2 is used as reference time
    base for ATOM group.
  默认值: ATOM_ACT_TB_TBU_TS0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GtmAtomActionTimeBaseValue
  长名称: ''
  描述: This parameter specifies the time base value for ATOM group channel level trigger
  默认值: 1
  最小值: 1
  最大值: 16777215
```

### 41. GtmAtomChannelConf

**描述**: This container contains the configuration (parameters) for GTM ATOM channel common settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmAtomChResetCn0OnTriggerEnable
  长名称: ''
  描述: |
    This parameter specifies enables/disables Atom channel counter Cn0 value is reset on global
    trigger from any of the trigger sources.
                                            TRUE: Resetting of Atom channel Cn0 on global trigger
    from any trigger source is enabled.
                                            FALSE: Resetting of Atom channel Cn0 on global trigger
    from any trigger source is disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GtmAtomChInternalTriggerEnable
  长名称: ''
  描述: |
    This parameter specifies enables/disables internal trigger from channel 0 of the corresponding
    group channel number.
                                            TRUE: Enable internal trigger from channel 0 or 8 (based
    on the AGC a channel belong to).
                                            FALSE: Disable internal trigger from channel 0 or 8
    (based on the AGC a channel belong to)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GtmTimerPortPinSelect
  长名称: ''
  描述: This parameter decides the output port and pin for the GTM timer.
  默认值: NONE
  最小值: ''
  最大值: ''
```

### 42. GtmTimGlobalConf

**描述**: This container holds the configuration parameters for the TIM global parameters.

该容器没有参数。

### 43. GtmTimChannelConf

**描述**: This container holds the configuration parameters for TIM channel- level parameters required to be
configured globally.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmTimInpPortPinSel
  长名称: ''
  描述: This parameter to configure the input port pin connection for TIM channels.
  默认值: SEL0_NONE
  最小值: ''
  最大值: ''
```

### 44. GtmTriggerForAdc

**描述**: This Specifies the TOM/ATOM channels that can be used as ADC Triggers

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmAdcTrigger0Select
  长名称: ''
  描述: This parameter defines the GTM timer (TOM/ATOM) channel controlling the adc_trig0 signal.
      TRIG_'VAL'_NO_TRIGGER indicating that this trigger line is electrically disconnected
      from possible trigger sources. TRIG_'VAL' - 'VAL' is the value programmed into the
      register. TOMx/ATOMx is the module containing Channel which generates the trigger.
  默认值: TRIG_0_NO_TRIGGER
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GtmAdcTrigger1Select
  长名称: ''
  描述: This parameter defines the GTM timer (TOM/ATOM) channel controlling the adc_trig1 signal.
      TRIG_'VAL'_NO_TRIGGER indicating that this trigger line is electrically disconnected
      from possible trigger sources. TRIG_'VAL' - 'VAL' is the value programmed into the
      register. TOMx/ATOMx is the module containing Channel which generates the trigger.
  默认值: TRIG_0_NO_TRIGGER
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GtmAdcTrigger2Select
  长名称: ''
  描述: This parameter defines the GTM timer (TOM/ATOM) channel controlling the adc_trig2 signal.
      TRIG_'VAL'_NO_TRIGGER indicating that this trigger line is electrically disconnected
      from possible trigger sources. TRIG_'VAL' - 'VAL' is the value programmed into the
      register. TOMx/ATOMx is the module containing Channel which generates the trigger.
  默认值: TRIG_0_NO_TRIGGER
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: GtmAdcTrigger3Select
  长名称: ''
  描述: This parameter defines the GTM timer (TOM/ATOM) channel controlling the adc_trig3 signal.
      TRIG_'VAL'_NO_TRIGGER indicating that this trigger line is electrically disconnected
      from possible trigger sources. TRIG_'VAL' - 'VAL' is the value programmed into the
      register. TOMx/ATOMx is the module containing Channel which generates the trigger.
  默认值: TRIG_0_NO_TRIGGER
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: GtmAdcTrigger4Select
  长名称: ''
  描述: This parameter defines the GTM timer (TOM/ATOM) channel controlling the adc_trig4 signal.
      TRIG_'VAL'_NO_TRIGGER indicating that this trigger line is electrically disconnected
      from possible trigger sources. TRIG_'VAL' - 'VAL' is the value programmed into the
      register. TOMx/ATOMx is the module containing Channel which generates the trigger.
  默认值: TRIG_0_NO_TRIGGER
  最小值: ''
  最大值: ''
```

### 45. GtmTriggerForDsadc

**描述**: This Specifies the TOM/ATOM channels that can be used as DSADC Triggers

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmDsadcTrigger0Select
  长名称: ''
  描述: This parameter defines the GTM timer (TOM/ATOM) channel controlling the adc_trig0 signal.
      TRIG_'VAL'_NO_TRIGGER indicating that this trigger line is electrically disconnected
      from possible trigger sources. TRIG_'VAL' - 'VAL' is the value programmed into the
      register. TOMx/ATOMx is the module containing Channel which generates the trigger.
  默认值: TRIG_0_NO_TRIGGER
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GtmDsadcTrigger1Select
  长名称: ''
  描述: This parameter defines the GTM timer (TOM/ATOM) channel controlling the adc_trig1 signal.
      TRIG_'VAL'_NO_TRIGGER indicating that this trigger line is electrically disconnected
      from possible trigger sources. TRIG_'VAL' - 'VAL' is the value programmed into the
      register. TOMx/ATOMx is the module containing Channel which generates the trigger.
  默认值: TRIG_0_NO_TRIGGER
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GtmDsadcTrigger2Select
  长名称: ''
  描述: This parameter defines the GTM timer (TOM/ATOM) channel controlling the adc_trig2 signal.
      TRIG_'VAL'_NO_TRIGGER indicating that this trigger line is electrically disconnected
      from possible trigger sources. TRIG_'VAL' - 'VAL' is the value programmed into the
      register. TOMx/ATOMx is the module containing Channel which generates the trigger.
  默认值: TRIG_0_NO_TRIGGER
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: GtmDsadcTrigger3Select
  长名称: ''
  描述: This parameter defines the GTM timer (TOM/ATOM) channel controlling the adc_trig3 signal.
      TRIG_'VAL'_NO_TRIGGER indicating that this trigger line is electrically disconnected
      from possible trigger sources. TRIG_'VAL' - 'VAL' is the value programmed into the
      register. TOMx/ATOMx is the module containing Channel which generates the trigger.
  默认值: TRIG_0_NO_TRIGGER
  最小值: ''
  最大值: ''
```

### 46. McuHardwareResourceAllocationConf

**描述**: Mcu Hardware resource allocation configuration

该容器没有参数。

### 47. McuGtmAllocationConf

**描述**: Mcu GTM unit resource allocation configuration

该容器没有参数。

### 48. McuGtmTimAllocationConf

**描述**: This container contains the TIM Configuration for GTM

该容器没有参数。

### 49. McuGtmTimChannelAllocationConf

**描述**: This container contains the TIM Channel Configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuGtmTimChannelAllocationConf
  长名称: ''
  描述: |
    This decides as to if this Channel is used for ICU or will it not be used.
                                         GTM_TIM_CHANNEL_NOT_USED: Specifies that this Channel is
    not configured by any module (unused).
                                         GTM_TIM_CHANNEL_USED_BY_ICU: Specifies that this Channel is
    configured by ICU module.
  默认值: GTM_TIM_CHANNEL_NOT_USED
  最小值: ''
  最大值: ''
```

### 50. McuGtmTomAllocationConf

**描述**: This container contains the TOM Configuration for GTM

该容器没有参数。

### 51. McuGtmTomChannelAllocationConf

**描述**: This container contains the TOM Channel Configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuGtmTomChannelAllocationConf
  长名称: ''
  描述: |
    This decides as to if this Channel is used or will it not be used.
                                         GTM_TOM_CHANNEL_NOT_USED: Specifies that this Channel is
    not configured by any module (unused).
                                         GTM_TOM_CHANNEL_USED_BY_ADC: Specifies that this Channel is
    configured by ADC module.
                                         GTM_TOM_CHANNEL_USED_BY_WDG: Specifies that this Channel is
    configured by WDG module.
                                         GTM_TOM_CHANNEL_USED_BY_PWM: Specifies that this Channel is
    configured by PWM module.
                                         GTM_TOM_CHANNEL_USED_BY_GPT: Specifies that this Channel is
    configured by GPT module.
                                         GTM_TOM_CHANNEL_USED_BY_OCU: Specifies that this Channel is
    configured by OCU module.
  默认值: GTM_TOM_CHANNEL_NOT_USED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuTomChannelEventHandledByDsadc
  长名称: ''
  描述: This parameter specifies which callback will be invoked when an event occurs
      TRUE : The callback of DSADC is invoked on an event.
      FALSE: The callback of the module which has configured the channel is invoked on an
      event.
  默认值: false
  最小值: ''
  最大值: ''
```

### 52. McuGtmAtomAllocationConf

**描述**: This container contains the ATOM Configuration for GTM

该容器没有参数。

### 53. McuGtmAtomChannelAllocationConf

**描述**: This container contains the ATOM Channel Configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuGtmAtomChannelAllocationConf
  长名称: ''
  描述: |
    This decides as to if this Channel is used or will it not be used.
                                         GTM_ATOM_CHANNEL_NOT_USED: Specifies that this Channel is
    not configured by any module (unused).
                                         GTM_ATOM_CHANNEL_USED_BY_ADC: Specifies that this Channel
    is configured by ADC module.
                                         GTM_ATOM_CHANNEL_USED_BY_GPT: Specifies that this Channel
    is configured by GPT module.
                                         GTM_ATOM_CHANNEL_USED_BY_OCU: Specifies that this Channel
    is configured by OCU module.
                                         GTM_ATOM_CHANNEL_USED_BY_PWM: Specifies that this Channel
    is configured by PWM module.
                                         GTM_ATOM_CHANNEL_USED_BY_WDG: Specifies that this Channel
    is configured by WDG module.
  默认值: GTM_ATOM_CHANNEL_NOT_USED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuAtomChannelEventHandledByDsadc
  长名称: ''
  描述: This parameter specifies which callback will be invoked when an event occurs
      TRUE : The callback of DSADC is invoked on an event.
      FALSE: The callback of the module which has configured the channel is invoked on an
      event.
  默认值: false
  最小值: ''
  最大值: ''
```

### 54. McuAscLinAllocationConf

**描述**: This container contains the AscLin Configuration

该容器没有参数。

### 55. McuAscLinChannelAllocationConf

**描述**: This container defines the AscLin Channel Configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuAscLinChannelAllocationConf
  长名称: ''
  描述: |
    This decides the usage of ASCLIN channel. This parameter is currently disabled, as none of the
    drivers are using ASCLIN channels.
                                 ASCLIN_CH_NOT_USED: Specifies that this Channel is not configured
    by any module (unused).
                                 ASCLIN_CH_USED_BY_LIN_DRIVER: Specifies that this Channel is
    configured by LIN module.
                                 ASCLIN_CH_USED_BY_UART_DRIVER: Specifies that this Channel is
    configured by UART module.
  默认值: ASCLIN_CH_NOT_USED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuAscLinKernelId
  长名称: ''
  描述: Specifies the Kernel Id for the respective Asclin channel.
  默认值: ASCLIN0
  最小值: ''
  最大值: ''
```

### 56. McuCcu6ModuleAllocationConf

**描述**: This container contains the Ccu6 Configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuCcu6ModuleAllocationConf
  长名称: ''
  描述: |
    This decides the usage of CCU6 module.
                                 CCU6_MODULE_NOT_USED: Specifies that this Channel is not configured
    by any module (unused).
                                 CCU6_MODULE_USED_BY_ADC_DRIVER: Specifies that this Module is
    configured by ADC module.
                                 CCU6_MODULE_USED_BY_ICU_DRIVER: Specifies that this Module is
    configured by ICU module.
                                 CCU6_MODULE_USED_BY_PWM_DRIVER: Specifies that this Module is
    configured by PWM module.
  默认值: CCU6_MODULE_NOT_USED
  最小值: ''
  最大值: ''
```

### 57. McuGpt12ModuleAllocationConf

**描述**: This container contains the GPT12 allocation configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuGpt12TimerAllocation
  长名称: ''
  描述: This denotes the timer in GPT1 or GPT2 block
  默认值: GPT_TIMER_2
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuGpt12ModuleAllocationConf
  长名称: ''
  描述: |
    This decides the usage of the timer of GPT1/GPT2 Timer block.
                                    GPT_TIMER_NOT_USED: Specifies that this timer is not configured
    by any module (unused).
                                    GPT_TIMER_USED_BY_ICU_DRIVER: Specifies that this timer is
    configured by ICU module.
                                    GPT_TIMER_USED_BY_GPT_DRIVER: Specifies that this timer is
    configured by GPT module.
  默认值: GPT_TIMER_NOT_USED
  最小值: ''
  最大值: ''
```

### 58. McuEruAllocationConf

**描述**: This container contains the ERU module configurations

该容器没有参数。

### 59. McuEruChannelInputLineConf

**描述**: This container contains the ERU input line Configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuEruChannelInputLineConf
  长名称: ''
  描述: |
    This decides usage of ERU input channel.
                                     ERU_CHANNEL_INP_NOT_USED: Specifies that this Channel is not
    configured by any module (unused).
                                     ERU_CHANNEL_INP_USED_BY_ADC_DRIVER: Specifies that this Channel
    is configured by ADC module.
                                     ERU_CHANNEL_INP_USED_BY_ICU_DRIVER: Specifies that this Channel
    is configured by ICU module.
                                     ERU_CHANNEL_INP_USED_BY_DSADC_DRIVER: Specifies that this
    Channel is configured by DSADC module.
  默认值: ERU_CHANNEL_INP_NOT_USED
  最小值: ''
  最大值: ''
```

### 60. McuEruChannelOutputUnitConf

**描述**: This container contains the ERU output line Configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuEruChannelOutputUnitConf
  长名称: ''
  描述: |
    This decides the usage of ERU output channel.
                                     ERU_CHANNEL_OUT_NOT_USED: Specifies that this Channel is not
    configured by any module (unused).
                                     ERU_CHANNEL_OUT_USED_BY_ADC_DRIVER: Specifies that this Channel
    is configured by ADC module.
                                     ERU_CHANNEL_OUT_USED_BY_ICU_DRIVER: Specifies that this Channel
    is configured by ICU module.
                                     ERU_CHANNEL_OUT_USED_BY_DSADC_DRIVER: Specifies that this
    Channel is configured by DSADC module.
  默认值: ERU_CHANNEL_OUT_NOT_USED
  最小值: ''
  最大值: ''
```

### 61. McuStmAllocationConf

**描述**: Mcu STM resource allocation configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuStmCmp0RegAllocationConf
  长名称: ''
  描述: |
    The STM timer compare register 0 usage.
                                  STM_CMP0_NOT_USED: STM timer compare register 0 not used.
                                  STM_CMP0_USED_BY_WDG: STM timer compare register 0 used by WDG.
                                  STM_CMP0_USED_BY_STM: STM timer compare register 0 used by STM.
  默认值: STM_CMP0_NOT_USED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuStmCmp1RegAllocationConf
  长名称: ''
  描述: |
    The STM timer compare register 1 usage.
                                  STM_CMP1_NOT_USED: STM timer compare register 1 not used.
                                  STM_CMP1_USED_BY_WDG: STM timer compare register 1 used by WDG.
                                  STM_CMP1_USED_BY_STM: STM timer compare register 1 used by STM.
  默认值: STM_CMP1_NOT_USED
  最小值: ''
  最大值: ''
```

### 62. McuDemEventParameterRefsConf

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId symbolic name. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 63. CommonPublishedInformation

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
  默认值: 20
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: SwMinorVersion
  长名称: ''
  描述: Minor version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: SwPatchVersion
  长名称: ''
  描述: Patch level version number of the vendor specific implementation of the module. The numbering
      is vendor specific.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: ModuleId
  长名称: ''
  描述: Module ID of this module from Module List
  默认值: 101
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
  描述: AURIX2G derivative used for the implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

### 64. McuPublishedInformation

**描述**: Container holding all MCU specific published information parameters

该容器没有参数。

### 65. McuResetReasonConf

**描述**: This container contains the configuration for the different type of reset reason that can be
retrieved from Mcu_GetResetReason Api.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuResetReason
  长名称: ''
  描述: The parameter represents the different type of reset that the controller supports. This
      parameter is referenced by the parameter EcuMResetReason in the ECU State manager
      module.
  默认值: 0
  最小值: 0
  最大值: 255
```

