# EthSM

## 模块描述

Ethernet State Manager (EthSM). The EthSM realizes a software layer between the Communication
Manager (ComM) and the Ethernet Interface (EthIf). The EthSM handles start-up and shutdown of the
communication of an Ethernet network.
#Ethernet #State #StateManager #ModeManagement #Startup #Shutdown #Wakeup
#AUTOSAR

## 容器列表

### 1. EthSMGeneral

**描述**: General configuration parameters of the EthSM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSMDevErrorDetect
  长名称: ''
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    
    True: Development error detection is enabled.
    False: Development error detection is disabeld.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthSMMainFunctionPeriod
  长名称: Main Function Period
  描述: This value specifies the period that the Main Function of the EthSM has to be triggered with.
  默认值: 0.02
  最小值: 0.005
  最大值: 1
- 
  序号: 3
  名称: EthSMVersionInfoApi
  长名称: Enable Version Info API
  描述: This parameter enables/disables the function EthSM_GetVersionInfo() to get major, minor and
      patch version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthSMUserConfigFile
  长名称: User Config File
  描述: |
    Reference to an external file that will be included during generation to EthSM_Cfg.h.
    
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with greate care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthSMEnableEthIfApiTimeout
  长名称: Enable EthIf API Timeout
  描述: |
    This parameter defines if a error handling for possibly unsuccessful calls to the EthIf APIs is
    actived.
    
    false:
    The error handling is disabled and the EthSM will call EthIf APIs endlessly every main function
    cycle until they return successfully.
    
    true:
    The error handling is enabled and the EthSM will call the EthIf APIs with a time gap specified
    by 'EthSMConfirmationTimeout' and as often as specified by 'EthSMMaxNumRetry'. (Both
    configurable Ethernet network-specific)
    
    Error handling of unsuccessful calls will be as followed:
    
    DET:
    (only enabled if 'EthSMDevErrorDetect' is enabled)
    EthSM will report the error ETHSM_E_ETHIF_TIMEOUT to DET by calling Det_ReportError.
    
    DEM:
    (only enabled if Ethernet network-specific DEM event 'ETHSM_E_TIMEOUT' is configured)
    EthSM will report the error with the specific DEM event ID by calling Dem_ReportErrorStatus.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthSMSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. EthSMGeneration

**描述**: Contains parameters which have influence on the generation of the module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSMOutOfBoundsWriteSanitizer
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
  序号: 2
  名称: EthSMOutOfBoundsReadSanitizer
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
  序号: 3
  名称: EthSMShortSymbols
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate shortened symbol names.
    
    FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant
    names.
    TRUE: symbol names are generated based on the MIP and a CRC32.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. EthSMNetwork

**描述**: This container contains the Ethernet network-specific parameters of each Ethernet network.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSMConfirmationTimeout
  长名称: EthIf API Confirmation Timeout
  描述: |
    This value specifes the time gap between the retries of the calls to EthIf:
    -EthIf_ControllerInit
    -EthIf_TransceiverInit
    -EthIf_SetControllerMode
    -EthIf_SetTransceiverMode
    
    For further information of EthIf API timeout handling please refere to the description of
    'EthSMEnableEthIfApiTimeout'.
  默认值: 0.1
  最小值: 0.001
  最大值: 10
- 
  序号: 2
  名称: EthSMMaxNumRetry
  长名称: Max Number of EthIf API Retries
  描述: |
    This value specifies the maximum number of retries for EthIf API calls.
    
    One try to call the EthIf API successfully is done without taking the specified value into
    account.
    
    For further information of EthIf API timeout handling please refere to the description of
    'EthSMEnableEthIfApiTimeout'.
  默认值: 0
  最小值: 0
  最大值: 10
- 
  序号: 3
  名称: EthSMStackType
  长名称: Stack Type
  描述: |
    Parameter defines the communication stack using this Ethernet network.
    
    TcpIp:
    
    The Ethernet network is used by a TcpIp communication stack. The two-stage communication request
    for this network specified by AUTOSAR will be used.
    The EthIf APIs are used to change activate/deactivate the Ethernet controller and transceiver
    and the TcpIp API is used to change the TcpIp mode.
    Also the EthSM relies on the indications of the transceiver link and the TcpIp mode for state
    handling.
    
    Avb:
    
    The Ethernet network is used by a Avb communication stack. The two-stage communication request
    for this network specified by AUTOSAR will be tailored into a one-stage request.
    The EthIf APIs are used to change activate/deactivate the Ethernet controller and transceiver.
    The TcpIp APIs aren't used anymore.
    Also the EthSM only relies on the indications of the transceiver link for state handling.
    
  默认值: TcpIp
  最小值: ''
  最大值: ''
```

### 4. EthSMDemEventParameterRefs

**描述**: This container includes the references to DemEventParameter elements which shall be invoked using
the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from
the referenced DemEventParameter's DemEventId value.

该容器没有参数。

