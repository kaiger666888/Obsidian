# EthTrcv

## 模块描述

Configuration of the EthTrcv (Ethernet Transceiver driver) module.

## 容器列表

### 1. EthTrcvGeneral

**描述**: General configuration of Ethernet Transceiver Driver module.


#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTrcvGetBaudRateApi
  长名称: Get Baud Rate API
  描述: |
    This parameter defines if the EthTrcv_GetBaudRate() API is enabled to get the current
    transceiver baud rate.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthTrcvGetDuplexModeApi
  长名称: Get Duplex Mode API
  描述: |
    This parameter defines if the EthTrcv_GetDuplexMode() API is enabled to get the current
    transceiver duplex mode.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTrcvGetLinkStateApi
  长名称: Get Transceiver Link State API
  描述: |
    This parameter defines if the EthTrcv_GetLinkState() API is enbled to get the current
    transceiver link state.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthTrcvGetTransceiverModeApi
  长名称: Get Transceiver Mode API
  描述: This parameter defines if the EthTrcv_GetTransceiverMode() API is enabled to get the current
      transceiver mode.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthTrcvMaxTrcvsSupported
  长名称: Max Trcvs Supported
  描述: |
    This value specifies the maximum number of transceiver configurations per transceiver driver.
    
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 6
  名称: EthTrcvSetTransceiverModeApi
  长名称: Set Transceiver Mode API
  描述: |
    This parameter defines if the EthTrcv_SetTransceiverMode() API is enabled to set the transceiver
    mode.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EthTrcvStartAutoNegotiationApi
  长名称: Start Auto Negotiaion API
  描述: |
    This parameter defines if the EthTrcv_StartAutoNegotiation() is enabled to start the transceiver
    auto negotiation.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EthTrcvVersionInfoApi
  长名称: Version Info API
  描述: |
    This parameter enables/disables the function EthTrcv_GetVersionInfo() to get major, minor and
    patch version information.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EthTrcvUserConfigFile
  长名称: User Config File
  描述: |
    Reference to an external text file that will be included during generation to EthTrcv_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthTrcvVersionInfoApiMacro
  长名称: Version Info API Macro
  描述: |
    Parameter not used.
    This parameter defines if EthTrcv_GetVersionInfo() is implemented as a macro.
    Restrictions: 'EthTrcvVersionInfoApiMacro' is only relevant, if 'EthTrcvVersionInfoApi' is set
    to 'true'.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EthTrcvIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: EthTrcvRuntimeMeasurementSupport
  长名称: ''
  描述: |
    If enabled runtime measurement points are added to the BSW module code and are added to the
    module configuration of MICROSAR RTM. The available measurement points can be seen and
    configured in the RTM module configuration. Availability of the MICROSAR RTM module is a
    prerequisite to make use of the runtime measurement functionality.
    Runtime measurement should be disabled in production code as measurement points may inflict
    additional runtime.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: EthTrcvGetTransceiverWakeupModeApi
  长名称: Get Transceiver Wakeup Mode API
  描述: |
    This parameter defines if the EthTrcv_GetTransceiverWakeupMode() API is enabled to get the
    current transceiver wakeup mode.
    
    The API can only be used if EthTrcvWakeUpSupport is not configured to
    ETHTRCV_WAKEUP_NOT_SUPPORTED.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: EthTrcvWakeUpSupport
  长名称: Wakeup Support
  描述: |
    This parameter specifies the kinde of wakeup support the transceiver provides.
    
    ETHTRCV_WAKEUP_BY_INTERRUPT:
    Wakeup is realised through a interrupt triggered by Icu.
    
    ETHTRCV_WAKEUP_BY_POLLING:
    Wakeup is realised trough polling of EthTrcv_CheckWakeup() through EcuM.
    
    ETHTRCV_WAKEUO_NOT_SUPPORTED:
    Wakeup capability is either not supported by hardware/driver or is disabled.
  默认值: ETHTRCV_WAKEUP_NOT_SUPPORTED
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: EthTrcvMainFunctionPeriod
  长名称: ''
  描述: This value specifies the period the EthTrcv_MainFunction is called.
  默认值: 0.02
  最小值: 0.001
  最大值: 1
- 
  序号: 16
  名称: EthTrcvDevErrorDetect
  长名称: ''
  描述: Enables / Disables development error detection.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: EthTrcvSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: EthTrcvCableDiagLoopCount
  长名称: ''
  描述: The cable diagnostic result can only be obtained after some waiting time. This parameter
      specifies the loop cycles the software performs until a timeout occurs.
  默认值: 10000
  最小值: 0
  最大值: 4294967296
- 
  序号: 19
  名称: EthTrcvHwAccessLoopCount
  长名称: ''
  描述: On some platforms there is a additional waiting time required before the hardware access is
      possible. This waiting is implemented as busy waiting. The loop count can be configured
      using this parameter.
  默认值: 0
  最小值: 0
  最大值: 4294967296
- 
  序号: 20
  名称: EthTrcvMainFunctionLinkHandlingPeriod
  长名称: Link Handling Main Function Period
  描述: This value specifies the period the function for link handling is called.
  默认值: 0.001
  最小值: 0.001
  最大值: 0.02
- 
  序号: 21
  名称: EthTrcvPreTrcvInitUserCallout
  长名称: Pre-Transceiver-Initialization User Callout
  描述: |
    This parameter defines the function to be called before the driver initializes a Ethernet
    transceiver.
    
    The function that is provided here has to have following signature:
    void <User>_PreTrcvInitCallout(uint8 EthTrcvIdx);
    
    NULL_PTR as value disables the functionality.
    
    With the passed EthTrcvIdx, representing the Symbolic Name Value of the respective Ethernet
    Transceiver, one can distinguish between the initialization context that is currently executed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: EthTrcvPostTrcvInitUserCallout
  长名称: Post-Transceiver-Initialization User Callout
  描述: |
    This parameter defines the function to be called after the driver has initialized a Ethernet
    transceiver.
    
    The function that is provided here has to have following signature:
    void <User>_PostTrcvInitCallout(uint8 EthTrcvIdx);
    
    NULL_PTR as value disables the functionality.
    
    With the passed EthTrcvIdx, representing the Symbolic Name Value of the respective Ethernet
    Transceiver, one can distinguish between the initialization context that is currently executed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: EthTrcvCalloutIncludeFiles
  长名称: ''
  描述: This parameter defines include files for the declaration of callouts, i.e. Pre- and
      Post-TransceiverInit-Callout, WakeUpCallout, WakeUpInspectionCallout,...
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: EthTrcvHwAccessMonitorPeriod
  长名称: Hardware Access Monitor Period
  描述: This is the cyclical period time the hardware access monitor checks the accessibility of the
      hardware.
  默认值: 0.001
  最小值: 0.001
  最大值: 1
- 
  序号: 25
  名称: EthTrcvHwAccessMonitorFailureUserCallout
  长名称: Hardware Access Monitor Failure User Callout
  描述: This parameter defines a user callout which is called in case a hardware access failure is
      detected by the hardware access monitor.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: EthTrcvWakeUpReasonPeriod
  长名称: Wake Up Reason Period
  描述: This is the cyclical period time the wake up reason check is performed, if
      EthTrcvWakeUpSupport is configured to POLLING.
  默认值: 0.001
  最小值: 0.001
  最大值: 1
- 
  序号: 27
  名称: EthTrcvHwAccessMonitorFailureDebounceValue
  长名称: Hardware Access Monitor Failure Debounce Value
  描述: This parameter defines the hardware access failure debounce counter value limit. Once the
      limit is reached, the error reaction is triggered after a hardware access failure was
      detected by the hardware access monitor. If the limit is not reached and the condition
      of the hardware access remains in the failed state, the counter is incremented. The
      minimum value for the limit is 0 which means no debouncing, The maximum value is 255.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 28
  名称: EthTrcvPreTrcvReadAccessCallout
  长名称: Pre-Transceiver Read Access Callout
  描述: |
    This parameter defines an optional user callout which is called directly before a transceiver
    read access.
    
    The function that is provided here has to have following signature:
    void <User>_PreTrcvReadAccessCallout(uint8 EthTrcvIdx);
    
    NULL_PTR as value disables the functionality.
    
    With the passed EthTrcvIdx, representing the Symbolic Name Value of the respective Ethernet
    Transceiver.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: EthTrcvPreTrcvWriteAccessCallout
  长名称: Pre-Transceiver Write Access Callout
  描述: |
    This parameter defines an optional user callout which is called directly before a transceiver
    write access.
    
    The function that is provided here has to have following signature:
    void <User>_PreTrcvWriteAccessCallout(uint8 EthTrcvIdx);
    
    NULL_PTR as value disables the functionality.
    
    With the passed EthTrcvIdx, representing the Symbolic Name Value of the respective Ethernet
    Transceiver.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: EthTrcvHwAccessMonitorRecoveryDebounceValue
  长名称: Hardware Access Monitor Recovery Debounce Value
  描述: This parameter defines the hardware access recovery debounce counter value limit. Once the
      limit is reached, the reaction is triggered after a hardware access recovery was
      detected by the hardware access monitor. If the limit is not reached and the condition
      of the hardware access remains in the unfailed state, the counter is incremented. The
      minimum value for the limit is 0 which means no debouncing, The maximum value is 255.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 2. EthTrcvConfigSet

**描述**: This conainter includes multiple configuration set containers.


该容器没有参数。

### 3. EthTrcvConfig

**描述**: This container includes the configuration of the individual transceiver.


#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTrcvIdx
  长名称: Transceiver Index
  描述: |
    This value specifies the instance ID of the configured transceiver.
    
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: EthTrcvSpeed
  长名称: ''
  描述: |
    This parameter specifies the speed of the Ethernet transceiver link in MBit/s.
    
    RESTRICTION: If Auto Negotiation is enabled this is the maximum speed advertised for
    Auto-Negotiation
    
  默认值: TRCV_SPEED_100
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTrcvWakeUpCallout
  长名称: ''
  描述: |
    This parameter specifies a callout function that is called during EthTrcv_SetTransceiverMode()
    for transceiver activation if a wakeup event has occured.
    
    The callout can be used for e.g. initiating a remote wakeup of related ECUs by setting a
    activation line connected to them.
    The function must be declared as followed:
    void &lt;EthTrcvWakeUpCallout&gt;(uint8 TrcvIdx)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthTrcvWakeupInspectionType
  长名称: Wakeup Inspection Type
  描述: |
    This parameter specifies the method used for inspection of wakeup events.
    
    ETHTRCV_ICU_CHANNEL:
    Uses the Icu_GetInputState() API for the related Icu channel to verify if a wakeup event occured
    and the corresponding AUTOSAR wakeup reason must be set.
    
    ETHTRCV_TRCV_REGISTERS:
    If hardware supports waking up by the transceiver itself the driver checks its registers if a
    wakeup event occured and the corresponding AUTOSAR wakeup reason must be set.
    
    ETHTRCV_USER_CODE:
    The user must provide integration code by itself for wakeup event inspection. This code must be
    embedded within the function EthTrcv_WakeupInspection generated into EthTrcv_Lcfg.c. For a more
    detailed information please refere to the Technical Reference of the driver.
  默认值: ETHTRCV_ICU_CHANNEL
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthTrcvConnNeg
  长名称: Connection Negotiation
  描述: This parameter specifies the connection negotiation of the Ethernet transceiver link. 
  默认值: ETHTRCV_CONN_NEG_MASTER
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthTrcvPhySignalQualityMeanValueLength
  长名称: ''
  描述: This parameter specifies how many consecutive data points of the phy's signal quality are used
      for the calculated mean value.
  默认值: 100
  最小值: 1
  最大值: 1000
- 
  序号: 7
  名称: EthTrcvSoftResetOnInit
  长名称: ''
  描述: This parameter speficies if a soft reset during transceiver initialization re-initializes all
      transceiver registers. In case the user sets some transceiver registers during runtime
      and wants to restore the default settings when transceiver is re-initialized, this
      option must be enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EthTrcvSoftResetWaitCycles
  长名称: ''
  描述: This value specifies the wait time until a soft reset is performed. After soft reset the
      driver polls the transceiver register and checks that the reset is performed or not.
      This is the maximum wait time.
  默认值: 120
  最小值: 1
  最大值: 65535
- 
  序号: 9
  名称: EthTrcvAutoNegotiationEnabled
  长名称: ''
  描述: Specifies if Auto-Negotiation is enabled (TRUE) or disabled (FALSE) for determination of the
      Ethernet transceiver speed.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthTrcvWakeUpInspectionCallout
  长名称: Wake Up Inspection Callout
  描述: |
    This parameter specifies a callout function that is called if the Wakeup Inspection Type is set
    to "ETHTRCV_USER_CODE".
    
    The callout can be used to realize a user-defined wake-up inspection and reporting.
    
    The function must be declared as follows:
    void &lt;EthTrcvWakeUpInspectionCallout&gt;(uint8 TrcvIdx)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EthTrcvDerivative
  长名称: Derivative
  描述: |
    This parameter specifies the used transceiver derivative.
    
    Available transceiver derivatives:
    - 88Q2112
    - 88Q2110
  默认值: TRCV_88Q2112
  最小值: ''
  最大值: ''
```

### 4. EthTrcvDemEventParameterRefs

**描述**: This container includes the references to DemEventParameter elements which shall be invoked using
the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from
the referenced DemEventParameter's DemEventId value.


该容器没有参数。

### 5. EthTrcvMiiInterface

**描述**: This container includes the MII interface configuration between an Ethernet Controller and the
Ethernet Transceiver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTrcvMiiIdx
  长名称: Transceiver MII Index
  描述: This value specifies the transceiver index used for MII (Media Independent Interface) access
      of the transceiver. A transceiver is usually  associated with a constant MII address,
      that can be selected via strapping pins on the hardware. The adress is used to identify
      the transceiver during communication.
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: EthTrcvMiiSelection
  长名称: ''
  描述: This parameter specifies the type of transceiver/controller interface. For the 88Q2112
      transceiver driver this selection is not possible because the setting is performed by
      strapping: Either RGMII or SGMII is possible.
  默认值: ETHTRCV_STRAPPING_CONFIG_ONLY
  最小值: ''
  最大值: ''
```

### 6. EthTrcvSwitchInterface

**描述**: This container includes the Switch interface configuration between an Ethernet Switch and an
Ethernet Transceiver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTrcvMiiSelection
  长名称: ''
  描述: This parameter specifies the type of transceiver/controller interface.  In case the configured
      element is an intenal PHY choose INTERNAL PHY, in case it is an external PHY managed by
      a switch the interface must be selected. For the 88Q2112 transceiver driver this
      selection is not possible since vendor specific registers are used. Extended register
      acces can be used instead.
  默认值: ETHTRCV_MII_MODE
  最小值: ''
  最大值: ''
```

### 7. EthTrcvWakeupMap

**描述**: Container for the mapping of wake up reasons to wake up sources. At least one container is needed if
EthTrcvWakeUpSupport is not ETHTRCV_WAKEUP_NOT_SUPPORTED.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTrcvWakeupReason
  长名称: Trcv Wakeup Reason
  描述: |
    This parameter specifies the corresponding wakeup reason mapped to the wakeup source of the
    EcuM.
    
    ETHTRCV_WUR_BUS:
    Reason for the wakeup is a event on the Ethernet network.
    
    ETHTRCV_WUR_GENERAL:
    Reason for the wakeup is a general event.
    
    ETHTRCV_WUR_INTERNAL:
    Reason for the wakeup is a internal transceiver event.
    
    ETHTRCV_WUR_PIN:
    Reason for the wakeup is a event on the related Icu channel.
    
    ETHTRCV_WUR_POWER_ON:
    Reason for the wakeup is the power on of the ECU.
    
    ETHTRCV_WUR_RESET:
    Reason for the wakeup is the reset of the ECU.
    
    ETHTRCV_WUR_SYSERR:
    Reason for the wakeup is a system error.
  默认值: ETHTRCV_WUR_BUS
  最小值: ''
  最大值: ''
```

