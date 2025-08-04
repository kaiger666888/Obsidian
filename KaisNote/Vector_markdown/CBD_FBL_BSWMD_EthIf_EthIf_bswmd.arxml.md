# EthIf

## 模块描述

Configuration of the EthIf (Ethernet Interface) module.

## 容器列表

### 1. EthIfConfigSet

**描述**: This container includes containers and parameters that may be part of a multiple configuration set.

该容器没有参数。

### 2. EthIfFrameOwnerConfig

**描述**: These containers include the configuration of Ethernet frame owners. Each frame owner registers for
a certain Ethertype to receive and transmit Ethernet frames with the respective Ethertype. Each
frame owner must implement an RxIndication and TxConfirmation function that need to be configured in
the EthIfRxIndicationConfig and EthIfTxConfirmationConfig containers.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfFrameType
  长名称: Frame Type
  描述: This value selects the Ethernet frame type the frame owner wants to register for.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: EthIfOwner
  长名称: Owner Index
  描述: This value selects the owner of an Ethernet frame type. The owner is a zero based index into
      the callback function configuration 'EthIfRxIndicationConfig'. I.e. an Ethernet frame of
      type IPv4 (0x800) at index 0 will call the first callback function configured in
      'EthIfRxIndicationConfig'. The EthIfOwner is calculated automatically and is not
      relevant for the user since it is not used in any external APIs.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 3. EthIfRxIndicationConfig

**描述**: These containers include the configuration of receive callback functions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfRxIndicationFunction
  长名称: Rx Indication
  描述: |
    This parameter defines the name of a receive indication callback function.
    
    The prototype of the function is as specified as followed:
    void <User>_RxIndication(uint8 EthIfCtrlIdx, Eth_FrameType FrameType, boolean IsBroadcast, uint8
    *PhysAddrPtr, uint8 *DataPtr, uint16 LenByte);
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. EthIfTrcvLinkStateChgConfig

**描述**: These containers include the link state change callback function. In case the transceiver link of
ther underlaying hardware changes all transceiver link state change callback functions are called by
the EthIf to inform the observers about a link state change.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfTrcvLinkStateChgFunction
  长名称: Transceiver Link State Change Indication
  描述: |
    This parameter defines the name of a link state change indication function. This function is
    called in case the transceiver link state of the underlaying hardware changes.
    
    The prototype of the function is as specified as followed:
    void <User>_TrcvLinkStateChg(uint8 EthIfCtrlIdx, EthTrcv_LinkStateType TrcvLinkState);
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. EthIfTxConfirmationConfig

**描述**: These containers include the configuration of transmit indication callback functions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfTxConfirmationFunction
  长名称: Tx Confirmation
  描述: |
    This parameter defines the name of a transmit indication callback function.
    
    The prototype of the function is as specified as followed:
    void <User>_TxConfirmation(uint8 EthIfCtrlIdx, uint8 BufferIdx);
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. EthIfController

**描述**: These containers include the configuration of virtual controllers. A virtual controller either
directly references a physical controller or points to a VLAN that is mapped onto a physical
controller. An EthIfController is used by the upper layers to send and receive frames of a certain
VLAN or frames that aren't VLAN-tagged.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfCtrlIdx
  长名称: ''
  描述: This parameter provides a zero-based consecutive index of the Ethernet Communication
      Controllers. Upper layer BSW modules and the EthIf itself use this index to identify an
      Ethernet Interface Controller.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: EthIfEnableVLAN
  长名称: ''
  描述: This parameter defines if the virtual controller is mapped to a VLAN.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthIfVlanId
  长名称: ''
  描述: |
    This value specifies a 12 bit VLAN identifier according to IEEE 802.1Q. Only values between
    0x000 and 0xffe are valid. All other values are reserved or invalid.
    When VID equals 0x000, the transmitted frames does not belong to any VLAN. The VLAN tag of the
    transmitted frames only specifies the priority. The receive behavior of a VLAN with VID=0x000 is
    the same to the behavior of a physical controller. All frames without any VLAN tag or with
    VID=0x000 are received.
  默认值: 0
  最小值: 0
  最大值: 4095
- 
  序号: 4
  名称: EthIfCtrlMtu
  长名称: ''
  描述: |
    This value specifies the maximum transmission unit (MTU) of the EthIfController in bytes. The
    MTU defines the maximum frame size that can be transmitted on the network.
    Note: In case a VLAN tag is used for the EthIfCtrl, the MTU is 4 bytes smaller than the maximum
    buffer size configured within the Eth module.
  默认值: 1500
  最小值: 46
  最大值: 9000
- 
  序号: 5
  名称: EthIfEnableLaxLinkAggregation
  长名称: Enable Lax Link Aggregation
  描述: |
    This parameter defines if Lax Link Aggregation for this EthIf Controller is enabled/disabled.
    
    Unaivailable/Disabled:
    The link for this EthIf Controller is aggregated by retrieving the link information of all
    switch ports configured in the referenced Switch Port Group. Only if all of the ports have
    established a link the EthIf Controller issues also a link to its upper layers.
    
    Enabled:
    The link for the EthIf Controller is aggregated by retrieving the link of all switch ports
    configured in the reference Switch Port Group. However the EthIf Controller now issues a link to
    its upper layers when at least two ports have a link established.
    
    Restriction:
    This parameter is only available if a Switch Port Group is mapped to the EthIf Controller.
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. EthIfBufFilterConfig

**描述**: This container includes buffer filter rules. A buffer filter rules defines if a reception buffers
must be explicitly unlocked by upper layers or not. Explicitly unlocking reception buffers may be
necessary to implement zero-copy concepts. By default unlocking of the reception buffers is
implicitly done right after the receive indication callback method.

该容器没有参数。

### 8. EthIfVlanFilterConfig

**描述**: These containers include buffer filter rules depending on the VLAN ID of an Ethernet frame.
As far as a filter rule for a specific VLAN ID exists, the buffer must be explicitly unlocked when
the VLAN ID of the Ethernet frame matches.

该容器没有参数。

### 9. EthIfEthTypeFilterConfig

**描述**: These containers include buffer filter rules depending on the Ethertype of an Ethernet frame.
As far as a filter rule for a specific Ethertype AND VLAN exists, the buffer must be explicitly
unlocked when the Ethertype of the Ethernet frame matches.

该容器没有参数。

### 10. EthIfSwitch

**描述**: This container is used to globally index all hardware switches that are used by the Ethernet
Interface. The index may be used by upper layers like the DHCP server component as a unique
identifier when calling a Ethernet Interface API. Besides the global index a reference to a hardware
switch configuration container resides in this container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfSwitchIndex
  长名称: EthIf Ethernet Switch Index
  描述: This value specifies a globally unique index for each hardware Ethernet Switch that is used by
      the Ethernet Interface. The index is zero-based and incremented by one for each hardware
      switch.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 11. EthIfWakeupMap

**描述**: This container includes the mapping of EcuM wakeup sources to corresponding hardware drivers for
wakeup check.

该容器没有参数。

### 12. EthIfTrafficMirroring

**描述**: This container includes the general configuration elements and sub containers of the traffic
mirroring feature.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfMaxParallelTxTrafficFrames
  长名称: Max Parallel Tx Traffic Frames
  描述: This value defines how many parallel Tx traffic frames can be handled by traffic mirroring.
  默认值: 2
  最小值: 1
  最大值: 65535
```

### 13. EthIfMirroringMap

**描述**: This container contains the configuration elements for one mirroring map.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfKeepOrgSrcMac
  长名称: Keep original Source MAC
  描述: |
    This parameter defines if the original Source MAC of the frame mirrored is keept or substituted
    on the destination interface.
    
    True:
    Source MAC address of frame to be mirrored is kept for frame mirrored on the Ethernet Controller
    referenced by "EthIfDestEthCtrlRef".
    
    False:
    Source MAC address of frame to be mirrored is replaced by the source MAC address of the Ethernet
    Controller referenced by "EthIfDestEthCtrlRef".
  默认值: true
  最小值: ''
  最大值: ''
```

### 14. EthIfTrafficGateway

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfSrcMacBlackListEntry
  长名称: Black List Source MAC address
  描述: |
    This parameter defines an entry for the source MAC address list of the traffic gateway.
    
    Ethernet frames containing the MAC address as source address will be ignored for traffic
    gateway.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 15. EthIfTrafficGatewayRoute

**描述**: This container containes two Ethernet Interface Controller references which reference the
controllers involved in the gateway route.

该容器没有参数。

### 16. EthIfSwitchPortGroup

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfSwitchPortGroupSemantics
  长名称: Port Group Semantic
  描述: |
    This parameter defines the semantics of the port group.
    
    Not existing:
    Port group is handled by BswM
    - mode control with EthIf_SwitchPortGroupRequestMode()
    - link indication to BswM_EthIf_PortGroupLinkStateChg()
    
    Existing:
    Port group is handled by EthIf dependent on the selected semantic
    
    ETHIF_SWITCH_PORT_GROUP_CONTROL:
    EthIf requests mode changes for the ports in the port group and uses the link state to define a
    link for the EthIf controller using the port group.
    
    ETHIF_SWITCH_PORT_GROUP_LINK_INFO:
    EthIf doesn't request mode changes for the ports but only uses the link state to define a link
    for the EthIf controller using the port group.
  默认值: ETHIF_SWITCH_PORT_GROUP_CONTROL
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthIfSwitchPortGroupIdx
  长名称: Switch Port Group Idx
  描述: This parameter defines the value of the symbolic name representing this switch port group.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 17. EthIfGeneral

**描述**: General configuration parameters of the EthIf

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfDevErrorDetect
  长名称: Dev Error Detect
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    true:   Development error detection is enabled.
    false:  Development error detection is disabled.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthIfEnableRxInterrupt
  长名称: Enable Rx Interrupt
  描述: |
    This parameter defines if the interrupt mode is used by Ethernet interface to receive data. In
    interrupt mode the reception of a frame is immediately indicated to the upper modules within an
    interrupt context. If interrupt mode is disabled, the EthIf polls the uderlaying hardware to
    receive the data.
    
    RESTRICTIONS: 'EthIfEnableRxInterrupt' needs to be set corresponding to Ethernet Drivers
    'EthEnableRxInterrupt'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthIfEnableTxInterrupt
  长名称: Enable Tx Interrupt
  描述: |
    This parameter defines if the interrupt mode is used by Ethernet interface to send data. In
    interrupt mode the transmission confirmation is triggered within the interrupt context
    immediately after frame transmission. If interrupt mode is disabled, the transmission
    confirmation is triggered when the EthIf polls the Eth module within its EthIf_MainFunctionTx
    function. The MainFunction is scheduled by the RTE.
    
    RESTRICTIONS: 'EthIfEnableTxInterrupt' needs to be set corresponding to Ethernet Drivers
    'EthEnableTxInterrupt'
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthIfMaxTrcvsTotal
  长名称: Max Trcvs Total
  描述: This value specifies the the maximum number of transceivers. This value is not relevant to the
      user since it is only used for internal DET checks.
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 5
  名称: EthIfMaxTxBufsTotal
  长名称: Max Tx Bufs Total
  描述: This value specifies the maximum number of transmit buffers.
  默认值: 10
  最小值: 1
  最大值: 255
- 
  序号: 6
  名称: EthIfTrcvLinkStateChgMainReload
  长名称: Trcv Link State Chg Main Reload
  描述: |
    This value specifies the period of the link state change check triggered in
    EthIf_MainFunctionTx() if EthIf_MainFunctionState() isn't used.
    
    Example:
    If this value is configured to 5, link state change checkis trigger every (5 *
    EthIf_MainFunctionPeriod) milliseconds.
    
    So the minimal latency to detect a link state change is equal to this timespan, the maximum
    latency is (  (2 * (EthIfTrcvLinkStatChgMainReload * EthIf_MainFunctionPeriod) ) - 1)
  默认值: 5
  最小值: 1
  最大值: 255
- 
  序号: 7
  名称: EthIfVersionInfoApi
  长名称: Version Info API
  描述: |
    This parameter enables/disables the function EthIf_GetVersionInfo() to get major, minor and
    patch version information.
    This parameter enables/disables the function EthIf_GetVersionInfo() to get major, minor and
    patch version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EthIfVersionInfoApiMacro
  长名称: Version Info API Macro
  描述: |
    This parameter defines if EthIf_GetVersionInfo() is implemented as a macro.
    
    RESTRICTIONS: 'EthIfVersionInfoApiMacro' is only relevant, if 'EthIfVersionInfoApi' is set to
    'true'.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EthIfUserConfigFile
  长名称: User Config File
  描述: |
    Reference to an external text file that will be included during generation to EthIf_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthIfEnableMainFunctionState
  长名称: Enable Main Function State
  描述: This parameter defines if a separate main function for transceiver link state supervision is
      used. Instead of polling the link within the EthIf_MainFunctionTx function (as specified
      in Autosar), the link is polled with the function EthIf_MainFunctionState. This function
      is called by the RTE scheduler directly. Instead of checking that the
      EthIfLinkStateChgMainReload counter in each period of the EthIf_MainFunctionTx state
      reaches zero, the scheduler already calls the EthIf_MainFunctionState with the proper
      period.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EthIfMainFunctionPeriod
  长名称: ''
  描述: This value specifies the the cycle time at which the EthIf_MainFunctionCyclic() is called.
  默认值: 0.005
  最小值: 0
  最大值: 32.767
- 
  序号: 12
  名称: EthIfMainFunctionRxTimeout
  长名称: ''
  描述: In polling mode (EthIfEnableRxInterrupt = false) the EthIf_MainFunctionRx polls the
      underlaying hardware for new received frames. This value specifies the timeout after the
      EthIf stops to receive frames. The current implementation does not support a timeout
      because it has no suitable time base for the supervision.
  默认值: 0.005
  最小值: 0
  最大值: 32.767
- 
  序号: 13
  名称: EthIfPublicCddHeaderFile
  长名称: ''
  描述: These parameters defines header files for callback functions which shall be included in case
      of CDDs.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: EthIfRxIndicationIterations
  长名称: Max Frames per Eth Controller
  描述: |
    This parameter defines the maximum number of Ethernet frames received during a
    EthIf_MainFunctionRx on one Ethernet controller, when EthIf is configured to polling mode
    (EthIfEnableRxInterrupt == FALSE).
    
    In case not all frames can be processed by EthIf, the reception queues of the underlaying
    hardware could get filled till next main function cycle and the hardware may drop frames.
  默认值: 5
  最小值: 0
  最大值: 65535
- 
  序号: 15
  名称: EthIfUpdatePhysAddrFilter
  长名称: ''
  描述: This parameter defines if the optional API EthIf_UpdatePhysAddrFilter is enabled. The API is
      used to enable and disable the frame reception filter for multicast addresses. If the
      filter for a certain multicast address is enabled, all frames are received that are
      destined for that address.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: EthIfEnableZeroCopyExtensions
  长名称: Enable Zero-Copy Extensions
  描述: |
    This parameter defines if buffer filtering and usage of external buffers is enabled.
    Depending on the buffer filter, reception buffers must be explicitly unlocked by upper layers or
    not. Explicitly unlocking reception buffers may be necessary to implement zero-copy concepts.
    However, default behavior is unlocking the reception buffer is implicitly done by the Eth
    component right after the receive indication callback method.
    For transmission the upper layer may use own buffers that must not be provided by the Eth
    component. Analogical to buffer filtering, external transmission buffers may be necessary to
    implement zero-copy concepts.
    
    RESTRICTIONS: 'EthIfEnableZeroCopyExtensions' needs to be set corresponding to Ethernet Drivers
    'EthEnableZeroCopyExtensions'
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: EthIfMaxExtTxBufsTotal
  长名称: Max External Tx Bufs Total
  描述: |
    This value specifies the maximum number of external transmission buffers.
    
    RESTRICTIONS: 'EthIfEnableZeroCopyExtensions' needs to be enabled for external transmission
    buffers.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 18
  名称: EthIfGlobalTimeSupport
  长名称: Global Time Support
  描述: |
    This parameter defines if the global time support is enabled/disabled.
    
    The global time support allows the retrieve time stamping information related to an Ethernet
    frame either from an local Ethernet controller or from an Ethernet switch.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: EthIfEnableHeaderAccessApi
  长名称: Enable Header Access API
  描述: |
    This parameter defines if APIs are provided to allow access to the Ethernet frame header.
    Usually the Ethernet header is cut off during reception or is assembled during transmission by
    the Ethernet driver. To read the header information during reception or to overwrite the header
    that is assembled by the driver during transmission, further APIs are provided.
    
    RESTRICTIONS: 'EthIfEnableHeaderAccessApi' needs to be set corresponding to Ethernet Drivers
    'EthEnableHeaderAccessApi'
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: EthIfGetTransceiverWakeupModeApi
  长名称: ''
  描述: This parameter defines if the EthIf_GetTransceiverWakeupMode() API is available.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: EthIfWakeupSupport
  长名称: ''
  描述: This parameter defines if the wakeup functionallity is supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: EthIfSwitchManagementSupport
  长名称: Switch Management Support
  描述: This parameter defines if switch frame management is supported
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: EthIfSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: EthIfEnableSignalQualityApi
  长名称: Enable Signal Quality Api
  描述: |
    This parameter defines if the APIs
    EthIf_GetTrcvSignalQuality
    EthIf_ClearTrcvSignalQuality
    EthIf_GetSwitchPortSignalQuality
    EthIf_ClearSwitchPortSignalQuality
    are available.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: EthIfSignalQualityCheckPeriod
  长名称: ''
  描述: Specifies the period in units of seconds in which the signal quality it polled in the context
      of EthIf_MainfunctionState. The value shall be an integral multiple of
      EthIfMainFunctionStatePeriod. If this parameter is defined, the EthIf_MainFunctionState
      shall be generated and parameter EthIfEnableSignalQualityApi shall be set to TRUE.
  默认值: 0.25
  最小值: 0
  最大值: 32.767
- 
  序号: 26
  名称: EthIfGetAndResetMeasurementDataApi
  长名称: ''
  描述: This parameter defines if the EthIf_GetAndResetMeasurementData() API is available.
  默认值: false
  最小值: ''
  最大值: ''
```

