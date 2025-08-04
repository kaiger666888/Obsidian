# vBRS

## 模块描述

Configuration of the Basic Runtime System.

## 容器列表

### 1. vBRSGeneral

**描述**: General configuration parameters of the vBRS.


#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSEnableSupportLEDs
  长名称: Toggle LED-Pin
  描述: |
    Use the functionality of a blinking live-LED for the used EvalBoard
    Sets the following generated parameters:
    BRS_ENABLE_SUPPORT_LEDS in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vBRSEnableSafeContextSupport
  长名称: Enable OS SafeContext (SC3) support
  描述: |
    Enable support of SafeContext OS (used for OS partitioning UseCase).
    Sets the following generated parameters:
    BRS_ENABLE_SAFECTXSUPPORT in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vBRSEnableMultiCoreSupport
  长名称: Enable OS MultiCore support
  描述: |
    Enable support of MultiCore OS.
    Sets the following generated parameters:
    BRS_ENABLE_OS_MULTICORESUPPORT in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vBRSUserConfigFile
  长名称: User Config Header File
  描述: If a file name is entered here, it will be included in vBrsCfg.h.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vBRSEnableSupportToggleWdPin
  长名称: Toggle WD-Pin
  描述: |
    Use the functionality of a blinking live-LED for the used EvalBoard
    Sets the following generated parameters:
    BRS_ENABLE_SUPPORT_TOGGLE_WD_PIN in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vBRSEnableSupportToggleCustomPin
  长名称: Toggle Custom-Pin
  描述: |
    Use the functionality of a blinking live-LED for the used EvalBoard
    Sets the following generated parameters:
    BRS_ENABLE_SUPPORT_TOGGLE_CUSTOM_PIN in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vBRSEnableEcuMStubGeneration
  长名称: Generation of EcuM Stub
  描述: If no real EcuM is part of the configuration this functionality generates an EcuM.c/h stub
      that calls the Init-functions of the Asr modules as specified in the EcuC configuration.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vBRSDisableSetupSupport
  长名称: ''
  描述: Activate this, if you don't want the BRS to guide you through the default MSR stack
      configuration (e.g. AutosolvingActions for mandatory tasks).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vBRSEnableSchmStubGeneration
  长名称: Generation of SchM Stub
  描述: Activate this, if the SchM stubs containing the defines for EXCLUSIVE AREAs should be
      generated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: vBRSEnableSchmStubSupportDrvCanAN
  长名称: Generation of SchM Stub - support DrvCan AN
  描述: |
    Prevents the SchM stub from generation of the following exclusive areas:
    CAN Driver (CAN_EXCLUSIVE_AREA_6)
    CAN Interface (CANIF_EXCLUSIVE_AREA_0)
    CANSM (CANSM_ EXCLUSIVE_AREA_1, CANSM_ EXCLUSIVE_AREA_4)
    COMM (COMM_ EXCLUSIVE_AREA_1)
    As described within CanDriver ApplicationNote AN-ISC-8-1149
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: vBRSFblSupport
  长名称: FBL Support Configuration
  描述: |
    Configure the support for FlashBootLoader projects.
    Sets the following generated parameters:
    BRS_ENABLE_FBL in vBrsCfg.h, additional to one of the following:
    BRS_FBL_NO_ECUMINIT, BRS_FBL_WITH_ECUMINIT
  默认值: Disabled
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: vBRSEnableHSMSupport
  长名称: Enable HSM Core support
  描述: |
    Enable support of HSM Core UseCase.
    Sets the following generated parameters:
    BRS_ENABLE_HSM_SUPPORT in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. vBRSHwConfig

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSOscClock
  长名称: Clock Config: Oscillator Clock Frequency
  描述: |
    Frequency of the board specific external oscillator.
    
    Sets the following generated parameters:
    BRS_OSC_CLK  in vBrsCfg.h
    MAIN_OSC_CLK in Makefile.config.generated
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: vBRSTimebaseClock
  长名称: Clock Config: Timebase (PLL) clock frequency
  描述: |
    Frequency, used for PLL calculation (normally used as CPU core clock).
    
    Sets the following generated parameters:
    BRS_TIMEBASE_CLOCK in vBrsCfg.h
    TIMEBASE_CLOCK in Makefile.config.generated
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 3
  名称: vBRSPeriphClock
  长名称: Clock Config: Peripheral (Timer) Clock Frequency
  描述: |
    Frequency of the controller peripherals, at least for the default timer, used by the OS.
    This frequency value is used to calculate the proper value of the TicksPerBase value inside the
    OS configuration.
    If the frequencies for communication peripherals differ from this peripheral clock, they could
    be configured within the depending communictaion channel configuration (e.g.
    vBRSHwConfig/vBRSDriverHandlingCAN/vBRSDriverHandlingCAN_Clock).
    
    Sets the following generated parameters:
    BRS_PERIPH_CLOCK in vBrsCfg.h
    PERIPH_CLOCK in Makefile.config.generated
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 4
  名称: vBRSEnablePortHandling
  长名称: BrsHw: Enable Port Handling
  描述: |
    Enable the handling of Ports configuration inside BrsHw.
    
    Sets the following generated parameter:
    BRS_ENABLE_PORT in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vBRSEnableWatchdogHandling
  长名称: BrsHw: Enable Watchdog Handling
  描述: |
    Enable the handling of Watchdog configuration inside BrsHw.
    
    Sets the following generated parameter:
    BRS_ENABLE_WATCHDOG in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vBRSEnablePLLClocksHandling
  长名称: BrsHw: Enable PLL&Clocks Handling
  描述: |
    Enable the handling of PLL and Clocks configuration inside BrsHw.
    
    Sets the following generated parameter:
    BRS_ENABLE_PLLCLOCKS in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vBRSCompilerInstructionSet
  长名称: Makesupport: Compiler Instruction Set
  描述: |
    Select the platform dependent Instruction Set for compile/link of the project.
    Note: not all platforms are supporting different instruction sets.
    
    Generated as the following:
    Makefile.config.generated: INSTRUCTION_SET = xxx
    vBrsCfg.h: BRS_INSTRUCTION_SET_xxx
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vBRSCompilerEnableFPU
  长名称: Makesupport: Enable FPU support
  描述: |
    Enable FPU usage on the controller. This has effect on the compiler/linker options.
    Note: not all platforms are supporting enabling/disabling of FPU usage.
    
    Generated as the following:
    Makefile.config.generated: FPU_USED = 1/0
    vBrsCfg.h: BRS_FPU_USED
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vBRSPeriphClockDescription
  长名称: Clock Config: Peripheral (Timer) Clock Description
  描述: Platform/family specific preconfig parameter with description of the recommended
      platform/family clock values and for usage of the peripheral clock (connection to OS
      timer).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: vBRSMakefileUserCode
  长名称: Makesupport: UserCode
  描述: Define here additional UserCode, to be generated into Makefile.config.generated
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: vBRSPreferPLLWatchdogInit
  长名称: BrsHw: Prefer PLL and Watchdog Init
  描述: |
    Prefer the initialization of PLL and Watchdog, previous to memory initialization.
    This will cause the depending init calls, previous to init stage One, inside the callout
    BrsMain_MemoryInit_StageOne_Hook() of BrsMain_Callout_Stubs.c.
    
    Sets the following generated parameter:
    BRS_ENABLE_PREFER_PLL_WATCHDOG_INIT in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. vBRSDriverHandlingCAN

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSEnableDriverHandlingCAN
  长名称: Enable handling of CAN driver
  描述: |
    This switch enables the handling of driver specific settings of
    - PLL and clock settings
    - Port Pin settings
    - On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or
    BrsHw_EnableHwAccess()
    
    To handle this inside the BrsHw Sourcecode, the define
    BRS_ENABLE_CAN_SUPPORT
    is genrated.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vBRSDriverHandlingCAN_channel0
  长名称: Handling of channel 00
  描述: |
    Enable the configuration of communication channel 0.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_0 in vBrsCfg.h
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vBRSDriverHandlingCAN_channel1
  长名称: Handling of channel 01
  描述: |
    Enable the configuration of communication channel 1.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_1 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vBRSDriverHandlingCAN_channel2
  长名称: Handling of channel 02
  描述: |
    Enable the configuration of communication channel 2.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_2 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vBRSDriverHandlingCAN_channel3
  长名称: Handling of channel 03
  描述: |
    Enable the configuration of communication channel 3.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_3 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vBRSDriverHandlingCAN_channel4
  长名称: Handling of channel 04
  描述: |
    Enable the configuration of communication channel 4.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_4 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vBRSDriverHandlingCAN_channel5
  长名称: Handling of channel 05
  描述: |
    Enable the configuration of communication channel 5.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_5 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vBRSDriverHandlingCAN_channel6
  长名称: Handling of channel 06
  描述: |
    Enable the configuration of communication channel 6.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_6 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vBRSDriverHandlingCAN_channel7
  长名称: Handling of channel 07
  描述: |
    Enable the configuration of communication channel 7.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_7 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: vBRSDriverHandlingCAN_channel8
  长名称: Handling of channel 08
  描述: |
    Enable the configuration of communication channel 8.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_8 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: vBRSDriverHandlingCAN_channel9
  长名称: Handling of channel 09
  描述: |
    Enable the configuration of communication channel 9.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_9 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: vBRSDriverHandlingCAN_PeripheralClock
  长名称: Frequency is similar with timer peripheral clock
  描述: |
    If enabled, the clock defined in
    vBRSHwConfig/vBRSPeriphClock
    will also be used for the peripheral clock, used by the CAN driver.
    
    If the clock, provided to the driver cell, is different, disable this parameter and configure
    the valid frequency within the paramter
    vBRSDriverHandlingCAN_Clock or
    vBRSDriverHandlingCAN_ClockRef (if Mcu is used)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: vBRSDriverHandlingCAN_Clock
  长名称: Frequency of peripheral clock
  描述: |
    Frequency, used for PLL calculation of CAN driver peripheral clock.
    Sets the following generated parameters:
    BRS_CAN_CLOCK in vBrsCfg.h
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 14
  名称: vBRSDriverHandlingCAN_channel10
  长名称: Handling of channel 10
  描述: |
    Enable the configuration of communication channel 10.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_10 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: vBRSDriverHandlingCAN_channel11
  长名称: Handling of channel 11
  描述: |
    Enable the configuration of communication channel 11.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_11 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: vBRSDriverHandlingCAN_channel12
  长名称: Handling of channel 12
  描述: |
    Enable the configuration of communication channel 12.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_12 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: vBRSDriverHandlingCAN_channel13
  长名称: Handling of channel 13
  描述: |
    Enable the configuration of communication channel 13.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_13 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: vBRSDriverHandlingCAN_channel14
  长名称: Handling of channel 14
  描述: |
    Enable the configuration of communication channel 14.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_14 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: vBRSDriverHandlingCAN_channel15
  长名称: Handling of channel 15
  描述: |
    Enable the configuration of communication channel 15.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_15 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: vBRSDriverHandlingCAN_channel16
  长名称: Handling of channel 16
  描述: |
    Enable the configuration of communication channel 16.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_16 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: vBRSDriverHandlingCAN_channel17
  长名称: Handling of channel 17
  描述: |
    Enable the configuration of communication channel 17.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_17 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: vBRSDriverHandlingCAN_channel18
  长名称: Handling of channel 18
  描述: |
    Enable the configuration of communication channel 18.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_18 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: vBRSDriverHandlingCAN_channel19
  长名称: Handling of channel 19
  描述: |
    Enable the configuration of communication channel 19.
    Sets the following generated parameter:
    BRS_ENABLE_CAN_CHANNEL_19 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
```

### 4. vBRSDriverHandlingLIN

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSEnableDriverHandlingLIN
  长名称: Enable handling of LIN driver
  描述: |
    This switch enables the handling of driver specific settings of
    - PLL and clock settings
    - Port Pin settings
    - On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or
    BrsHw_EnableHwAccess()
    
    To handle this inside the BrsHw Sourcecode, the define
    BRS_ENABLE_LIN_SUPPORT
    is genrated.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vBRSDriverHandlingLIN_channel0
  长名称: Handling of channel 00
  描述: |
    Enable the configuration of communication channel 0.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_0 in vBrsCfg.h
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vBRSDriverHandlingLIN_channel1
  长名称: Handling of channel 01
  描述: |
    Enable the configuration of communication channel 1.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_1 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vBRSDriverHandlingLIN_channel2
  长名称: Handling of channel 02
  描述: |
    Enable the configuration of communication channel 2.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_2 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vBRSDriverHandlingLIN_channel3
  长名称: Handling of channel 03
  描述: |
    Enable the configuration of communication channel 3.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_3 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vBRSDriverHandlingLIN_channel4
  长名称: Handling of channel 04
  描述: |
    Enable the configuration of communication channel 4.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_4 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vBRSDriverHandlingLIN_channel5
  长名称: Handling of channel 05
  描述: |
    Enable the configuration of communication channel 5.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_5 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vBRSDriverHandlingLIN_channel6
  长名称: Handling of channel 06
  描述: |
    Enable the configuration of communication channel 6.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_6 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vBRSDriverHandlingLIN_channel7
  长名称: Handling of channel 07
  描述: |
    Enable the configuration of communication channel 7.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_7 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: vBRSDriverHandlingLIN_channel8
  长名称: Handling of channel 08
  描述: |
    Enable the configuration of communication channel 8.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_8 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: vBRSDriverHandlingLIN_channel9
  长名称: Handling of channel 09
  描述: |
    Enable the configuration of communication channel 9.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_9 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: vBRSDriverHandlingLIN_Clock
  长名称: Frequency of peripheral clock
  描述: |
    Frequency, used for PLL calculation of LIN driver peripheral clock.
    Sets the following generated parameters:
    BRS_LIN_CLOCK in vBrsCfg.h
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 13
  名称: vBRSDriverHandlingLIN_PeripheralClock
  长名称: Frequency is similar with timer peripheral clock
  描述: |
    If enabled, the clock defined in
    vBRSHwConfig/vBRSPeriphClock
    will also be used for the peripheral clock, used by the LIN driver.
    
    If the clock, provided to the driver cell, is different, disable this parameter and configure
    the valid frequency within the paramter
    vBRSDriverHandlingLIN_Clock or
    vBRSDriverHandlingLIN_ClockRef (if Mcu is used)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: vBRSDriverHandlingLIN_channel10
  长名称: Handling of channel 10
  描述: |
    Enable the configuration of communication channel 10.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_10 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: vBRSDriverHandlingLIN_channel11
  长名称: Handling of channel 11
  描述: |
    Enable the configuration of communication channel 11.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_11 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: vBRSDriverHandlingLIN_channel12
  长名称: Handling of channel 12
  描述: |
    Enable the configuration of communication channel 12.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_12 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: vBRSDriverHandlingLIN_channel13
  长名称: Handling of channel 13
  描述: |
    Enable the configuration of communication channel 13.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_13 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: vBRSDriverHandlingLIN_channel14
  长名称: Handling of channel 14
  描述: |
    Enable the configuration of communication channel 14.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_14 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: vBRSDriverHandlingLIN_channel15
  长名称: Handling of channel 15
  描述: |
    Enable the configuration of communication channel 15.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_15 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: vBRSDriverHandlingLIN_channel16
  长名称: Handling of channel 16
  描述: |
    Enable the configuration of communication channel 16.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_16 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: vBRSDriverHandlingLIN_channel17
  长名称: Handling of channel 17
  描述: |
    Enable the configuration of communication channel 10.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_10 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: vBRSDriverHandlingLIN_channel18
  长名称: Handling of channel 18
  描述: |
    Enable the configuration of communication channel 18.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_18 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: vBRSDriverHandlingLIN_channel19
  长名称: Handling of channel 19
  描述: |
    Enable the configuration of communication channel 19.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_19 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: vBRSDriverHandlingLIN_channel20
  长名称: Handling of channel 20
  描述: |
    Enable the configuration of communication channel 20.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_20 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: vBRSDriverHandlingLIN_channel21
  长名称: Handling of channel 21
  描述: |
    Enable the configuration of communication channel 21.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_21 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: vBRSDriverHandlingLIN_channel22
  长名称: Handling of channel 22
  描述: |
    Enable the configuration of communication channel 22.
    Sets the following generated parameter:
    BRS_ENABLE_LIN_CHANNEL_22 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
```

### 5. vBRSDriverHandlingFlexray

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSEnableDriverHandlingFlexray
  长名称: Enable handling of FlexRay driver
  描述: |
    This switch enables the handling of driver specific settings of
    - PLL and clock settings
    - Port Pin settings
    - On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or
    BrsHw_EnableHwAccess()
    
    To handle this inside the BrsHw Sourcecode, the define
    BRS_ENABLE_FLEXRAY_SUPPORT
    is genrated.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vBRSDriverHandlingFlexray_channel0A
  长名称: Handling of channel 0A
  描述: |
    Enable the configuration of communication channel 0A.
    Sets the following generated parameter:
    BRS_ENABLE_FLEXRAY_CHANNEL_0A in vBrsCfg.h
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vBRSDriverHandlingFlexray_channel0B
  长名称: Handling of channel 0B
  描述: |
    Enable the configuration of communication channel 0B.
    Sets the following generated parameter:
    BRS_ENABLE_FLEXRAY_CHANNEL_0B in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vBRSDriverHandlingFlexray_channel1A
  长名称: Handling of channel 1A
  描述: |
    Enable the configuration of communication channel 1A.
    Sets the following generated parameter:
    BRS_ENABLE_FLEXRAY_CHANNEL_1A in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vBRSDriverHandlingFlexray_channel1B
  长名称: Handling of channel 1B
  描述: |
    Enable the configuration of communication channel 1B.
    Sets the following generated parameter:
    BRS_ENABLE_FLEXRAY_CHANNEL_1B in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vBRSDriverHandlingFlexray_PeripheralClock
  长名称: Frequency is similar with timer peripheral clock
  描述: |
    If enabled, the clock defined in
    vBRSHwConfig/vBRSPeriphClock
    will also be used for the peripheral clock, used by the FlexRay driver.
    
    If the clock, provided to the driver cell, is different, disable this parameter and configure
    the valid frequency within the paramter
    vBRSDriverHandlingFlexray_Clock or
    vBRSDriverHandlingFlexray_ClockRef (if Mcu is used)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vBRSDriverHandlingFlexray_Clock
  长名称: Frequency of peripheral clock
  描述: |
    Frequency, used for PLL calculation of FlexRay driver peripheral clock.
    Sets the following generated parameters:
    BRS_FLEXRAY_CLOCK in vBrsCfg.h
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

### 6. vBRSDriverHandlingEthernet

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSEnableDriverHandlingEthernet
  长名称: Enable handling of EtherNet driver
  描述: |
    This switch enables the handling of driver specific settings of
    - PLL and clock settings
    - Port Pin settings
    - On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or
    BrsHw_EnableHwAccess()
    
    To handle this inside the BrsHw Sourcecode, the define
    BRS_ENABLE_ETHERNET_SUPPORT
    is genrated.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vBRSDriverHandlingEthernet_PeripheralClock
  长名称: Frequency is similar with timer peripheral clock
  描述: |
    If enabled, the clock defined in
    vBRSHwConfig/vBRSPeriphClock
    will also be used for the peripheral clock, used by the EtherNet driver.
    
    If the clock, provided to the driver cell, is different, disable this parameter and configure
    the valid frequency within the paramter
    vBRSDriverHandlingEthernet_Clock or
    vBRSDriverHandlingEthernet_ClockRef (if Mcu is used)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vBRSDriverHandlingEthernet_Clock
  长名称: Frequency of peripheral clock
  描述: |
    Frequency, used for PLL calculation of EtherNet driver peripheral clock.
    Sets the following generated parameters:
    BRS_ETHERNET_CLOCK in vBrsCfg.h
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

### 7. vBRSEvalBoardInfo

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSEvalBoardDescription
  长名称: Evaluation Board Description
  描述: General description of the supported evaluation board.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vBRSEvalBoard
  长名称: Evaluation Board Define
  描述: |
    Define, used in SourceCode, for this specific Evaluation Board.
    Most times, this is used for board specific pin settings.
    Sets the following generated parameters:
    BRS_EVA_BOARD_x in vBrsCfg.h
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vBRSEvalBoardOscClock
  长名称: Evaluation Board Oscillator Clock Frequency
  描述: |
    Defines the frequency of the oscillator clock, equipped on the specific evaluation board.
    This valus will be verified through the vBRS generator to fit with the configured value of
    vBRSOscClock.
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

### 8. vBRSDriverHandlingHyperbus

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSEnableDriverHandlingHyperbus
  长名称: Enable handling of Hyperbus driver
  描述: |
    This switch enables the handling of driver specific settings of
    - PLL and clock settings
    - Port Pin settings
    - On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or
    BrsHw_EnableHwAccess()
    
    To handle this inside the BrsHw Sourcecode, the define
    BRS_ENABLE_HYPERBUS_SUPPORT
    is genrated.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vBRSDriverHandlingHyperbus_channel0
  长名称: Handling of channel 00
  描述: |
    Enable the configuration of communication channel 0.
    Sets the following generated parameter:
    BRS_ENABLE_HYPERBUS_CHANNEL_0 in vBrsCfg.h
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vBRSDriverHandlingHyperbus_channel1
  长名称: Handling of channel 01
  描述: |
    Enable the configuration of communication channel 1.
    Sets the following generated parameter:
    BRS_ENABLE_HYPERBUS_CHANNEL_1 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vBRSDriverHandlingHyperbus_PeripheralClock
  长名称: Frequency is similar with timer peripheral clock
  描述: |
    If enabled, the clock defined in
    vBRSHwConfig/vBRSPeriphClock
    will also be used for the peripheral clock, used by the Hyperbus driver.
    
    If the clock, provided to the driver cell, is different, disable this parameter and configure
    the valid frequency within the paramter
    vBRSDriverHandlingHyperbus_Clock or
    vBRSDriverHandlingHyperbus_ClockRef (if Mcu is used)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vBRSDriverHandlingHyperbus_Clock
  长名称: Frequency of peripheral clock
  描述: |
    Frequency, used for PLL calculation of Hyperbus driver peripheral clock.
    Sets the following generated parameters:
    BRS_HYPERBUS_CLOCK in vBrsCfg.h
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

### 9. vBRSDriverHandlingI2C

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSEnableDriverHandlingI2C
  长名称: Enable handling of I2C driver
  描述: |
    This switch enables the handling of driver specific settings of
    - PLL and clock settings
    - Port Pin settings
    - On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or
    BrsHw_EnableHwAccess()
    
    To handle this inside the BrsHw Sourcecode, the define
    BRS_ENABLE_I2C_SUPPORT
    is genrated.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vBRSDriverHandlingI2C_channel0
  长名称: Handling of channel 00
  描述: |
    Enable the configuration of communication channel 0.
    Sets the following generated parameter:
    BRS_ENABLE_I2C_CHANNEL_0 in vBrsCfg.h
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vBRSDriverHandlingI2C_channel1
  长名称: Handling of channel 01
  描述: |
    Enable the configuration of communication channel 1.
    Sets the following generated parameter:
    BRS_ENABLE_I2C_CHANNEL_1 in vBrsCfg.h
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vBRSDriverHandlingI2C_PeripheralClock
  长名称: Frequency is similar with timer peripheral clock
  描述: |
    If enabled, the clock defined in
    vBRSHwConfig/vBRSPeriphClock
    will also be used for the peripheral clock, used by the I2C driver.
    
    If the clock, provided to the driver cell, is different, disable this parameter and configure
    the valid frequency within the paramter
    vBRSDriverHandlingI2C_Clock or
    vBRSDriverHandlingI2C_ClockRef (if Mcu is used)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vBRSDriverHandlingI2C_Clock
  长名称: Frequency of peripheral clock
  描述: |
    Frequency, used for PLL calculation of I2C driver peripheral clock.
    Sets the following generated parameters:
    BRS_I2C_CLOCK in vBrsCfg.h
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

### 10. vBRSTestsuiteSupport

**描述**: Support for Vector internal Testsuites

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSEnableTestsuiteSupport
  长名称: ''
  描述: |
    Enable support of the Generic TestSuite connectioin.
    Via the define BRS_ENABLE_TESTSUITE_SUPPORT, the Generic TestSuite concept headerfile
    BrsTestsuite.h will be included and the Generic Testsuite init function BrsTestsuiteInit() will
    be called within BrsMain.c
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vBRSTccSupport
  长名称: ''
  描述: vBRS Tcc Support
  默认值: None
  最小值: ''
  最大值: ''
```

### 11. vBRSTcc

该容器没有参数。

### 12. vBRSComIfUpperLayerRxPdu

**描述**: This container specifies Rx PDU that is received by the BRS through communication stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSComIfHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 13. vBRSComIfUpperLayerTxPdu

**描述**: This container specifies Tx PDU that is transmitted by the CDD through communication stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSComIfHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 14. vBRSMemoryInit

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBRSInitPatternBlocks
  长名称: Init pattern for Zero Init Blocks
  描述: |
    Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_PreMainStartup().
    This value is for the blocks, configured with "Zero Init Policy" = ALWAYS within the vLinkGen
    configuration.
    The pattern has to be 32-bit aligned.
    Default value is 0x0.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vBRSInitPatternHardResetBlocks
  长名称: Init pattern for Hard Reset Zero Init Blocks
  描述: |
    Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_PreMainStartup().
    This value is for the blocks, configured with "Zero Init Policy" = HARD_RESET within the
    vLinkGen configuration.
    The pattern has to be 32-bit aligned.
    Default value is 0x0.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vBRSInitPatternAreas
  长名称: Init pattern for Zero Init Areas
  描述: |
    Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_PreMainStartup().
    This value is for the areas, configured with "Zero Init Policy" = ALWAYS within the vLinkGen
    configuration.
    The pattern has to be 32-bit aligned.
    Default value is 0x0.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vBRSInitPatternHardResetAreas
  长名称: Init pattern for Hard Reset Zero Init Areas
  描述: |
    Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_PreMainStartup().
    This value is for the areas, configured with "Zero Init Policy" = HARD_RESET within the vLinkGen
    configuration.
    The pattern has to be 32-bit aligned.
    Default value is 0x0.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

