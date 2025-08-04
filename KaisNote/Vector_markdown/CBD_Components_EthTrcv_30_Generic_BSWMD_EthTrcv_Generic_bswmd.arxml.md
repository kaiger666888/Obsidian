# EthTrcv

## 模块描述

Configuration of the EthTrcv (Ethernet Transceiver driver) module.

## 容器列表

### 1. EthTrcvGeneral

**描述**: General configuration of Ethernet Transceiver Driver module

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTrcvDevErrorDetect
  长名称: ''
  描述: Enables / Disables development error detection.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthTrcvGetBaudRateApi
  长名称: ''
  描述: Enables / Disables EthTrcv_GetBaudRate API
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTrcvGetDuplexModeApi
  长名称: ''
  描述: Enables / Disables EthTrcv_GetDuplexMode API
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthTrcvGetLinkStateApi
  长名称: ''
  描述: Enables / Disables EthTrcv_GetLinkState API
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthTrcvGetTransceiverModeApi
  长名称: ''
  描述: Enables / Disables EthTrcv_GetTransceiverMode API
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthTrcvMaxTrcvsSupported
  长名称: ''
  描述: This value limits the maximum number of transceiver configurations per transceiver driver
  默认值: 1
  最小值: 0
  最大值: 1
- 
  序号: 7
  名称: EthTrcvSetTransceiverModeApi
  长名称: ''
  描述: Enables / Disables EthTrcv_SetTransceiverMode API
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EthTrcvStartAutoNegotiationApi
  长名称: ''
  描述: Enables / Disables EthTrcv_StartAutoNegotiation API
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EthTrcvVersionInfoApi
  长名称: ''
  描述: Enables / Disables version info API
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthTrcvUserConfigFile
  长名称: ''
  描述: If a file path will be specified, the file is read and its contents are put at the end of the
      EthTrcv config file.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EthTrcvVersionInfoApiMacro
  长名称: ''
  描述: |
    If 'EthTrcvVersionInfoApiMacro' is enabled, macro will be used to get major, minor and patch
    version information.
    
    RESTRICTIONS: 'EthTrcvVersionInfoApiMacro' is only available, if 'EthTrcvVersionInfoApi' is set
    to 'true'
    
    (Vector spcific: not used)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: EthTrcvIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
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
  序号: 14
  名称: EthTrcvGetTransceiverWakeupModeApi
  长名称: Get Transceiver Wakeup Mode API
  描述: |
    This parameter defines if the EthTrcv_GetTransceiverWakeupMode() API is enabled to get the
    current transceiver wakeup mode.
    
    The API can only be used if EthTrcvWakeUpSupport is not configured to
    ETHTRCV_WAKEUP_NOT_SUPPORTED.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
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
  序号: 16
  名称: EthTrcvMainFunctionPeriod
  长名称: ''
  描述: This value specifies the period the EthTrcv_MainFunction is called.
  默认值: 0.02
  最小值: 0.001
  最大值: 1
- 
  序号: 17
  名称: EthTrcvWakeUpCalloutIncludeFiles
  长名称: ''
  描述: This parameter defines include files for the declaration of wakeup callouts.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: EthTrcvHwAccessLoopCount
  长名称: ''
  描述: On some platforms there is a additional waiting time required before the hardware access is
      possible. This waiting is implemented as busy waiting. The loop count can be configured
      using this parameter.
  默认值: 0
  最小值: 0
  最大值: 4294967296
- 
  序号: 19
  名称: EthTrcvSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: EthTrcvCableDiagLoopCount
  长名称: ''
  描述: The cable diagnostic result can only be obtained after some waiting time. This parameter
      specifies the loop cycles the software performs until a timeout occurs.
  默认值: 10000
  最小值: 0
  最大值: 4294967296
- 
  序号: 21
  名称: EthTrcvMacSecApi
  长名称: MACsec API
  描述: Enables / Disables the MACsec API
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: EthTrcvMainFunctionMacSecPeriod
  长名称: ''
  描述: This value specifies the period after which  the EthTrcv_MainFunctionMacSec is called.
  默认值: 0.02
  最小值: 0.001
  最大值: 1
```

### 2. EthTrcvConfigSet

**描述**: All underlying parameters may be part of a multiple configuration set.

该容器没有参数。

### 3. EthTrcvConfig

**描述**: Configuration of the individual transceiver

#### 参数列表

```yaml
- 
  序号: 1
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
  序号: 2
  名称: EthTrcvAutoNegotiationEnabled
  长名称: ''
  描述: This parameter specifies if Auto Negotiation is enabled or disabled for determination of the
      Ethernet Transceiver speed.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTrcvIdx
  长名称: Transceiver Index
  描述: This value specifies the instance ID of the configured transceiver.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
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
  序号: 5
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
  序号: 6
  名称: EthTrcvConnNeg
  长名称: Connection Negotiation
  描述: This parameter specifies the connection negotiation of the Ethernet transceiver link
      (Master/Slave or Auto Negotiation).
  默认值: ETHTRCV_CONN_NEG_MANUAL
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EthTrcvPhySignalQualityMeanValueLength
  长名称: ''
  描述: This parameter specifies how many consecutive data points of the phy's signal quality are used
      for the calculated mean value.
  默认值: 100
  最小值: 1
  最大值: 1000
- 
  序号: 8
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
  序号: 9
  名称: EthTrcvSoftResetWaitCycles
  长名称: ''
  描述: This value specifies the wait time until a soft reset is performed. After soft reset the
      driver polls the transceiver register and checks that the reset is performed or not.
      This is the maximum wait time.
  默认值: 120
  最小值: 1
  最大值: 65535
```

### 4. EthTrcvDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

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
  描述: This parameter specifies the type of transceiver/controller interface. The interface is either
      (G)MII, Light-MII or R(G)MII. In case of R(G)MII the refclock signal can be generated by
      the transceiver or applied externally. Choose R(G)MII_XTAL for transceiver clock
      generation and R(G)MII for an external clock. The interface must be selected according
      to your electric circuit design.
  默认值: MII
  最小值: ''
  最大值: ''
```

### 6. EthTrcvSwitchInterface

**描述**: This container includes the Switch interface configuration between an Ethernet Switch and an
Ethernet Transceiver.

该容器没有参数。

### 7. EthTrcvSpiInterface

该容器没有参数。

### 8. EthTrcvWakeupMap

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

### 9. EthTrcvGenericDriver

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTrcvGenericDriverName
  长名称: Driver Name
  描述: |
    This value specifies the identifier used for the API infixing of the drivers AUTOSAR API.
    
    Example:
    The EthTrcv_Init() API will be generated as EthTrcv_<Vendor ID>_<Driver Name>_Init().
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthTrcvGenericDriverVendorId
  长名称: Vendor ID
  描述: |
    This value specifies the Vendor ID used for the API infixing of the drivers AUTOSAR API.
    
    Example:
    The EthTrcv_Init() API will be generated as EthTrcv_<Vendor ID>_<Driver Name>_Init().
  默认值: 30
  最小值: 0
  最大值: 65535
```

