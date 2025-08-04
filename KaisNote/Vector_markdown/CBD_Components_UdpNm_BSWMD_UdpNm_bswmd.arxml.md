# UdpNm

## 模块描述

Ethernet Network Management (Udp). The UdpNm is a hardware independent protocol that can only be
used on ETH. Its main purpose is to coordinate the transition between normal operation and bus-sleep
mode of the network. #ModeManagement #NetworkManagement #Shutdown

## 容器列表

### 1. UdpNmGlobalConfig

**描述**: Global configuration parameters of the UdpNm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmBusSynchronizationEnabled
  长名称: ''
  描述: |
    This parameter defines if the bus synchronization support is enabled. This feature is required
    for gateway nodes only.
    
    This option allows the transmission of an asynchronous NM message at any time within Network
    Mode. This may be required for the synchronized shutdown of networks. Therefore this option is
    usually only enabled in gateways.
    
    
    RESTRICTIONS: This parameter is derived from NmBusSynchronizationEnabled. This parameter is only
    relevant if UdpNmPassiveModeEnabled == false.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: UdpNmComControlEnabled
  长名称: ''
  描述: |
    This parameter defines if the Communication Control support is enabled.
    If this option is enabled two additional APIs are available that can either enable or disable
    the transmission of Network Management messages in the Normal Operation state. While the
    transmission is disabled the network cannot be released.
    
    RESTRICTIONS: Derived from NmComControlEnabled.
    If this global parameter is enabled, at least one channel configuration must have this parameter
    enabled. If this parameter is disabled, all channel configurations must have this parameter
    disabled.
    /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmChannelConfig/UdpNmComControlEnabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: UdpNmComUserDataSupport
  长名称: ''
  描述: This parameter defines if the user data handling by a PDU handled within an upper layer is
      supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: UdpNmCoordinatorSyncSupport
  长名称: ''
  描述: This parameter defines if the coordinator synchronization support is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: UdpNmDevErrorDetect
  长名称: ''
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    true:   Development error detection is enabled.
    false:  Development error detection is disabled.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
    If it is enabled development errors are reported to the Development Error Tracer (Det).
    The following development errors are reported:
    - service call without intialization of network management
    - service call with invalid channel handle
    - service call with invalid PDU ID
    - reception of an NM PDU in Bus Sleep Mode
    - network timeout (i.e. the network management timoeut timer has timed out in Repeat Message
    State or Normal Operation State)
    - null pointer has been passed as argument
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: UdpNmImmediateRestartEnabled
  长名称: ''
  描述: |
    This parameter defines if the asynchronous transmission of an NM PDU upon bus-communication
    request in Prepare-Bus-Sleep mode is enabled.
    Enabling this option may lead to a burst of NM messages if all nodes get a bus-communication
    request approximately at the same time.
    
    RESTRICTIONS: This parameter is only relevant if UdpNmPassiveModeEnabled is False
    If this global parameter is enabled, at least one channel configuration must have this parameter
    enabled. If this parameter is disabled, all channel configurations must have this parameter
    disabled.
    /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmChannelConfig/UdpNmImmediateRestartEnabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: UdpNmNodeDetectionEnabled
  长名称: ''
  描述: |
    This parameter defines if the node detection feature is enabled.
    If a Tester is present in the network, 'UdpNmNodeDetectionEnabled' offers the opportunity to
    detect all present network nodes.
    
    
    RESTRICTIONS: Derived from NmNodeDetectionEnabled.
    This parameter is only relevant if UdpNmPassiveModeEnabled is false.
    This parameter is only valid if UdpNmPduNidPosition is not UDPNM_PDU_OFF for at least one
    channel.
    
    If this global parameter is enabled, at least one channel configuration must have this parameter
    enabled. If this parameter is disabled, all channel configurations must have this parameter
    disabled.
    /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmChannelConfig/UdpNmNodeDetectionEnabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: UdpNmNodeIdEnabled
  长名称: ''
  描述: |
    This parameter specifies if the Node ID is enabled.
    
    Parameters value is derived from configuration parameter NmNodeIdEnabled.
    
    RESTRICTIONS:If this global parameter is enabled, at least one channel configuration must have
    this parameter enabled. If this parameter is disabled, all channel configurations must have this
    parameter disabled.
    /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmChannelConfig/UdpNmNodeIdEnabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: UdpNmNumberOfChannels
  长名称: ''
  描述: not used
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 10
  名称: UdpNmPassiveModeEnabled
  长名称: ''
  描述: |
    This parameter defines if the Passive Mode is supported.
    If this option is set, the node is not able to send NM messages. This option can be used for
    nodes that do not require to keep the bus awake.
    
    RESTRICTIONS: Needs to have the same value as 'NmPassiveModeEnabled' for all UdpNm channels.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: UdpNmPduRxIndicationEnabled
  长名称: ''
  描述: |
    This parameter defines if the PDU Rx Indication is called.
    If this option is enabled a callback function for every received PDU will be triggered.
    
    
    RESTRICTIONS: Derived from 'NmPduRxIndicationEnabled'.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: UdpNmPnEiraCalcEnabled
  长名称: ''
  描述: |
    Specifies if UdpNm calculates the PN request information for internal and external requests.
    (EIRA)
    
    true: PN request are calculated
    false: PN request are not calculated
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: UdpNmPnResetTime
  长名称: ''
  描述: Specifies the runtime of the reset timer in seconds. This reset time is valid for the reset of
      PN requests in the EIRA and in the ERA. The value shall be the same for every channel.
      Thus it is a global config parameter.
  默认值: 1
  最小值: 0.001
  最大值: 65.535
- 
  序号: 14
  名称: UdpNmRemoteSleepIndEnabled
  长名称: ''
  描述: |
    This parameter defines if the remote sleep indication support is enabled. This feature is
    required for gateway nodes only.
    'UdpNmRemoteSleepIndEnabled' is used in gateways to detect when the synchronized shutdown of
    networks has to be carried out.
    It comprises Remote Sleep Indication, Remote Sleep Cancelation and checking of the Remote Sleep
    Indication State.
    
    Remote Sleep Indication is notified when your network node is the only one in the whole network
    that requests bus-communication for 'UdpNmRemoteSleepIndTime'.
    Remote Sleep Cancelation is notified if any other network node requires the communication bus
    while Remote Sleep Indication takes place in your network node.
    
    
    RESTRICTIONS: Derived from NmRemoteSleepIndEnabled.
    This parameter is only relevant if UdpNmPassiveModeEnabled is false.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: UdpNmRepeatMsgIndEnabled
  长名称: ''
  描述: |
    This parameter defines if the notification that a RepeatMessageRequest bit has been received is
    enabled.
    
    This option enables a callback to the NM Interface whenever a state change due to a repeat
    message request or a repeat message bit occurs.
    
    
    
    RESTRICTIONS: If (UdpNmNodeDetectionEnabled == false) then (UdpNmRepeatMsgIndEnabled = false).
    Derived from 'NmRepeatMsgIndEnabled'.
    
    If this global parameter is enabled, at least one channel configuration must have this parameter
    enabled. If this parameter is disabled, all channel configurations must have this parameter
    disabled.
    /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmChannelConfig/UdpNmRepeatMsgIndEnabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: UdpNmStateChangeIndEnabled
  长名称: ''
  描述: |
    This parameter defines if the UdpNm state change notification is enabled.
    This option allows to track every change in the NM state machine by the means of a callback
    function triggered on every state change.
    
    
    
    RESTRICTIONS: Derived from 'NmStateChangeIndEnabled'.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: UdpNmUserDataEnabled
  长名称: ''
  描述: |
    This parameter defines if the user data support is enabled.
    This option provides read and write access to the user data. Location of user data in the NM
    message depends on the message configuration.
    
    
    
    RESTRICTIONS: Derived from 'NmUserDataEnabled'.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: UdpNmVersionInfoApi
  长名称: ''
  描述: This parameter enables/disables the function UdpNm_GetVersionInfo() to get major, minor and
      patch version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: UdpNmUserConfigFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation to UdpNm_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: UdpNmRuntimeMeasurementSupport
  长名称: ''
  描述: |
    This parameter defines if runtime measurement points are added to the BSW module code and to the
    module configuration of MICROSAR RTM. The available measurement points can be seen and
    configured in the RTM module configuration. Availability of the MICROSAR RTM module is a
    prerequisite to make use of the runtime measurement functionality.
    Runtime measurement should be disabled in production code as measurement points may inflict
    additional runtime.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: UdpNmSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: UdpNmRuntimeErrorReport
  长名称: ''
  描述: Selects if runtime errors are reported.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: UdpNmCoordinatorEnabled
  长名称: ''
  描述: not used
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: UdpNmCoordinatorId
  长名称: ''
  描述: not used
  默认值: 0
  最小值: 0
  最大值: 3
- 
  序号: 25
  名称: UdpNmPnShutdownMessageRetransmissionDuration
  长名称: ''
  描述: Specifies the duration in msec of retransmission phase of a PN shutdown message. A
      retransmission shall be performed per affected NM channel, as long as the PN shutdown
      message could not be successfully sent and the retransmission timer is running. The
      value shall be a multiple integral of UdpNmMainFunctionPeriod.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 26
  名称: UdpNmPnSyncShutdownErrorReactionEnabled
  长名称: ''
  描述: Pre-processor switch for enabling reaction, if a top-level PNC coordinator received a PN
      shutdown message on a NM-channel which refer to a ComM channel that is actively
      coordinated by a PNC gateway.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: UdpNmPnShutdownMessageTimeoutTime
  长名称: ''
  描述: |
    This message timeout time is only relevant if the feature UdpNmSynchronizedPncShutdownEnabled is
    enabled.
    
    This parameter specifies the timeout time that is waited for a TxConfirmation of the transmitted
    PNSR message until a retry is performed.
    
    Note: This time must be smaller than the UdpNmPnShutdownMessageRetransmissionDuration.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
```

### 2. UdpNmChannelConfig

**描述**: This container includes the channel specific configuration parameter of the UdpNm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmMainFunctionPeriod
  长名称: ''
  描述: This value specifies the period for the calls of UdpNm_MainFunction for this channel.
  默认值: 0.01
  最小值: 0.001
  最大值: 0.255
- 
  序号: 2
  名称: UdpNmMsgCycleOffset
  长名称: ''
  描述: |
    This value specifies the offset in the periodic transmission node. It determines the start delay
    of the transmission.
    Whenever the transmission of network management messages is started, the transmission start is
    delayed by this value.
    
    RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False)
  默认值: 0
  最小值: 0
  最大值: 65.535
- 
  序号: 3
  名称: UdpNmMsgCycleTime
  长名称: ''
  描述: |
    This value specifies the period of a NM PDU. It determines the periodic rate and is the basis
    for transmit scheduling.
    
    RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False)
  默认值: 0.1
  最小值: 0.001
  最大值: 65.535
- 
  序号: 4
  名称: UdpNmMsgTimeoutTime
  长名称: ''
  描述: |
    This value specifies the transmission timeout of NM PDUs. If there is no transmission
    confirmation by the SoAd within this timeout, the UdpNm module shall give an error notification.
    
    RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False). It should
    be a multiple of UdpNmMainFunctionPeriod and smaller than UdpNmMsgCycleTime.
  默认值: 0.06
  最小值: 0.001
  最大值: 65.535
- 
  序号: 5
  名称: UdpNmNodeId
  长名称: ''
  描述: |
    This value specifies the node identifier of local node.
    
    The 'NodeId' is transmitted within the network management message if UdpNmPduNidPosition !=
    UDPNM_PDU_OFF)
    
    The node identifier is used for the detection of present nodes and can be read by the
    application at any time.
    
    Note: This value is transmitted within the NM message.
    
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: UdpNmPduCbvPosition
  长名称: ''
  描述: |
    This value specifies the position of the control bit vector within the NM PDU.
    The value of the parameter represents the location of the control bit vector in the NM PDU
    (UDPNM_PDU_BYTE_0 means byte 0, UDPNM_PDU_BYTE_1 means byte 1, UDPNM_PDU_OFF means that the
    Control Bit Vector is not part of the NM PDU).
    
    RESTRICTIONS: If (UdpNmPduCbvPosition != UDPNM_PDU_OFF) then (UdpNmPduCbvPosition !=
    UdpNmPduNidPosition) and (UdpNmPduLength >= UdpNmPduCbvPosition).
    If (UdpNmPduNidPosition == UDPNM_PDU_OFF) then (UdpNmPduCbvPosition != UDPNM_PDU_BYTE_1).
    
  默认值: UDPNM_PDU_OFF
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: UdpNmPduLength
  长名称: ''
  描述: |
    This value specifies the length of the NM PDU.
    
    The value is auto-calculated dependent on 'UdpNmPduCbvPosition', 'UdpNmPduNidPosition' and
    'UdpNmUserDataLength'.
    
    According to AUTOSAR RfC 70333 the PDU Length shall not be restricted to 8 Byte anymore like
    specified in AUTOSAR SWS (last released version 4.2.2). Therefore it is possible to use PDUs
    larger than 8 Byte.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: UdpNmPduNidPosition
  长名称: ''
  描述: |
    This value specifies the position of the source node identifier within the NM PDU.
    The value of the parameter represents the location of the source node identifier in the NM PDU
    (UDPNM_PDU_BYTE_0 means byte 0, UDPNM_PDU_BYTE_1 means byte 1, UDPNM_PDU_OFF means that the
    source node identifier is not part of the NM PDU).
    
    RESTRICTIONS: If (UdpNmPduNidPosition != UDPNM_PDU_OFF) then (UdpNmPduNidPosition !=
    UdpNmPduCbvPosition) and (UdpNmPduLength >= UdpNmPduNidPosition).
    If (UdpNmPduCbvPosition == UDPNM_PDU_OFF) then (UdpNmPduNidPosition != UDPNM_PDU_BYTE_1).
  默认值: UDPNM_PDU_OFF
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: UdpNmPnEnabled
  长名称: ''
  描述: |
    Enables or disables support of partial networking.
    
    false: Partial networking is not supported
    true: Partial networking supported
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: UdpNmPnEraCalcEnabled
  长名称: ''
  描述: |
    Specifies if UdpNm calculates the PN request information for external requests. (ERA)
    
    false: PN request information for external requests is not calculated.
    true: PN request information for external requests is calculated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: UdpNmPnHandleMultipleNetworkRequests
  长名称: ''
  描述: |
    This parameter defines whether UdpNm_NetworkRequest calls have an effect in Network Mode. If
    disabled UdpNm_NetworkRequest is ignored in Network Mode. If enabled UdpNm_NetworkRequest
    triggers a change from Network Mode to Repeat Message.
    
    RESTRICTIONS: This parameter is only relevant if (UdpNmPnEnabled == True)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: UdpNmRemoteSleepIndTime
  长名称: ''
  描述: |
    This value specifies the timeout for Remote Sleep Indication.
    
    Remote Sleep Indication is notified when the network node of the own ECU is the only one in the
    whole network that requests bus communication for this timing value.
    
    Typically it should be equal to: n * UdpNmMsgCycleTime, where n denotes the number of
    NM-Messages that are normally sent before Remote Sleep Indication is detected.
    The value of n decremented by one determines the amount of lost NM-Messages that can be
    tolerated by the Remote Sleep Indication procedure.
    
    RESTRICTIONS: This parameter is only relevant if (UdpNmRemoteSleepIndEnabled == True)
    If (UdpNmRemoteSleepIndEnabled == True) then (UdpNmRemoteSleepIndTime > 0)
  默认值: 0.5
  最小值: 0.001
  最大值: 65.535
- 
  序号: 13
  名称: UdpNmRepeatMessageTime
  长名称: ''
  描述: |
    This value specifies the timeout for Repeat Message State.
    It defines how long the NM shall stay in the Repeat Message State. Within Repeat Message State
    the NM messages are always transmitted cyclically.
    
    Typically it should be equal to: n * UdpNmMsgCycleTime, where n denotes the number of
    NM-Messages that are normally sent in the Repeat Message State.
    The value of n decremented by one determines the amount of lost NM-Messages that can be
    tolerated by the node detection procedure.
    The value 0 denotes that no Repeat Message State is configured. It means that Repeat Message
    State is transient what implicates that it is left immediately after entrance and in result, no
    start-up stability is guaranteed and no node detection procedure is possible.
    
    If UdpNmPassiveModeEnabled == True, then a value of UdpNmRepeatMessageTime = 0 is forced.
  默认值: 0.4
  最小值: 0
  最大值: 65.535
- 
  序号: 14
  名称: UdpNmTimeoutTime
  长名称: ''
  描述: |
    This value specifies the Network Timeout for the reception and transmission of network
    management messages.
    If in Network Mode (Repeat Message State, Normal Operation State or Ready Sleep State) your
    network node does not require the communication bus anymore and no more NM messages are received
    within this time 'Prepare Bus-Sleep' is entered.
    
    It shall be equal for all nodes in the cluster. It shall be greater than 'UdpNmMsgCycleTime'.
    Typically it should be equal to n * UdpNmMsgCycleTime, where n denotes the number of NM-Message
    cycle times in the Ready Sleep State before transition into the Bus-Sleep Mode is initiated. The
    value of n decremented by one determines the amount of lost NM-Messages that can be tolerated by
    the coordination algorithm.
  默认值: 1
  最小值: 0.002
  最大值: 65.535
- 
  序号: 15
  名称: UdpNmUserDataLength
  长名称: ''
  描述: |
    This value specifies the length of the user data contained in the NM PDU.
    
    According to AUTOSAR RfC 70333 the PDU Length shall not be restricted to 8 Byte anymore like
    specified in AUTOSAR SWS (last released version 4.2.2). Therefore the User Data Length is
    extended in line with the extension of the PDU Length.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 16
  名称: UdpNmWaitBusSleepTime
  长名称: ''
  描述: |
    This value specifies the timeout for bus calm down phase (Prepare Bus-Sleep Mode).
    The bus calm down period is a safety zone between bus-communication of application messages and
    shutdown of the communication bus.
    
    It shall be equal for all nodes in the cluster. It shall be long enough to make all Tx-buffers
    empty.
  默认值: 0.75
  最小值: 0.001
  最大值: 4294967.295
- 
  序号: 17
  名称: UdpNmImmediateNmTransmissions
  长名称: ''
  描述: This value specifies the number of immediate NM PDUs which shall be transmitted. If the value
      is zero no immediate NM PDUs are transmitted. The cycle time of immediate NM PDUs is
      defined by UdpNmImmediateNmCycleTime.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 18
  名称: UdpNmImmediateNmCycleTime
  长名称: ''
  描述: This value specifies the immediate NM PDU cycle time which is used for
      'UdpNmImmediateNmTransmissions' NM PDU transmissions. This parameter is only valid if
      'UdpNmImmediateNmTransmissions' is greater than one.
  默认值: 0.1
  最小值: 0.001
  最大值: 65.535
- 
  序号: 19
  名称: UdpNmAllNmMessagesKeepAwake
  长名称: ''
  描述: |
    Specifies if UdpNm drops irrelevant NM PDUs.
    
    false: Only NM PDUs with a PNI bit = true and containing a PN request for this ECU triggers the
    standard RX indication handling
    true: Every NM PDU triggers the standard RX indication handling
    
    RESTRICTIONS: This parameter is only relevant if UdpNmPnEnabled == True
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: UdpNmCarWakeUpBitPosition
  长名称: ''
  描述: |
    This parameter specifies the Bit position of the Car Wake-Up Bit within the NM-PDU.
    
    Note that this parameter has to be set to a value between 0 and 7.
    
    RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpRxEnabled == True)
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 21
  名称: UdpNmCarWakeUpBytePosition
  长名称: ''
  描述: |
    This parameter specifies the Byte position of the Car Wake-Up Bit within the NM-PDU.
    
    Note that this parameter has to be set to a valid byte position within the user data of the NM
    PDU.
    If this setting is set to '0', the first byte of the NM PDU (not necessarily the first user data
    byte) is referred.
    
    RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpRxEnabled == True)
  默认值: 2
  最小值: 0
  最大值: 65535
- 
  序号: 22
  名称: UdpNmCarWakeUpFilterEnabled
  长名称: ''
  描述: |
    This parameter defines if Car Wake-Up filtering is supported. Then only the Car Wake-Up bit
    within the NM message with source node identifier 'UdpNmCarWakeUpFilterNodeId' is considered as
    Car Wake-Up request.
    
    false: Car Wake-up filtering is not supported
    true: Car Wake-up filtering is supported
    
    RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpRxEnabled == True)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: UdpNmCarWakeUpFilterNodeId
  长名称: ''
  描述: |
    This value specifies the source node identifier for Car Wake-Up filtering. If Car Wake-Up
    filtering is supported, only the Car Wake-Up bit within the NM message with source node
    identifier 'UdpNmCarWakeUpFilterNodeId' is considered as Car Wake-Up request.
    
    Note that this parameter has to be set to a value between 0x00 and 0xFF.
    
    RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpFilterEnabled == True)
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 24
  名称: UdpNmCarWakeUpRxEnabled
  长名称: ''
  描述: |
    This parameter defines if support of Car Wake-Up bit evaluation in received NM PDUs is enabled.
    
    false: Car Wake-up is not supported
    true: Car Wake-up is supported
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: UdpNmActiveWakeupBitEnabled
  长名称: ''
  描述: This parameter defines if the active wakeup bit is set in the CBV for this channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: UdpNmNodeIdEnabled
  长名称: ''
  描述: |
    This parameter enables the source node identifier on the selected channel.
    This option provides read access to the local node identifier and to the node identifier
    received in the last NM message.
    
    RESTRICTIONS: If this parameter is enabled, the global parameter
    /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeIdEnabled must be enabled.
    If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeIdEnabled is disabled, this parameter must be
    disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: UdpNmNodeDetectionEnabled
  长名称: ''
  描述: |
    This parameter defines if the node detection feature is enabled per channel.
    If a Tester is present in the network 'UdpNmNodeDetectionEnabled' offers the opportunity to
    detect all present network nodes.
    
    
    RESTRICTIONS: This parameter is only relevant if 'UdpNmPassiveModeEnabled' is false.
    The feature can only be used on a channel if UdpNmPduNidPosition is not equal to UDPNM_PDU_OFF.
    If this parameter is enabled, the global parameter
    /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeDetectionEnabled must be enabled.
    If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeDetectionEnabled is disabled, this parameter must
    be disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: UdpNmComControlEnabled
  长名称: ''
  描述: |
    This parameter defines if the Communication Control support is enabled per channel.
    If this option is enabled two additional APIs are available that can either enable or disable
    the transmission of Network Management messages in the Normal Operation state. While the
    transmission is disabled the network cannot be released.
    
    RESTRICTIONS: If this parameter is enabled, the global parameter
    /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmComControlEnabled must be enabled.
    If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmComControlEnabled is disabled, this parameter must be
    disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: UdpNmImmediateRestartEnabled
  长名称: ''
  描述: |
    This parameter defines if the asynchronous transmission of an NM PDU upon bus-communication
    request in Prepare-Bus-Sleep mode is enabled per channel.
    Enabling this option may lead to a burst of NM messages if all Nodes get a bus-communication
    request approximately at the same time.
    
    RESTRICTIONS: This parameter is only relevant if 'UdpNmPassiveModeEnabled' is False
    If this parameter is enabled, the global parameter
    /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmImmediateRestartEnabled must be enabled.
    If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmImmediateRestartEnabled is disabled, this parameter
    must be disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: UdpNmRepeatMsgIndEnabled
  长名称: ''
  描述: |
    This parameter defines if the notification that a RepeatMessageRequest bit has been received is
    enabled per channel.
    
    This option enables a callback to the NM Interface whenever a state change due to a repeat
    message request or a repeat message bit occurs.
    
    
    RESTRICTIONS: If (UdpNmNodeDetectionEnabled == false) then (UdpNmRepeatMsgIndEnabled = false).
    If this parameter is enabled, the global parameter
    /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmRepeatMsgIndEnabled must be enabled.
    If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmRepeatMsgIndEnabled is disabled, this parameter must
    be disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: UdpNmRetryFirstMessageRequest
  长名称: ''
  描述: |
    This pararmeter specifies if first message request in UdpNm is repeated until accepted by the
    SoAd.
    
    RESTRICTION:
    UdpNmRetryFirstMessageRequest = false if UdpNmPassiveModeEnabled == true
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 32
  名称: UdpNmCriBitAlwaysEnabled
  长名称: ''
  描述: |
    When this feature is enabled, the CRI bit in the CBV byte is always enabled. Regardless of the
    configured Partial Network setting.
    
    Note: The CRI bit is responsible to display if the current message contains PN info bytes and is
    usually only set if Partial Network is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 33
  名称: UdpNmSynchronizedPncShutdownEnabled
  长名称: ''
  描述: |
    Specifies if UdpNm handle PN shutdown messages to support a synchronized PNC shutdown across a
    PN topology. This is only used for ECUs in the role of a top-level PNC coordinator or
    intermediate PNC coordinator. Thus, the PNC gateway functionality is enabled and therefore ERA
    calculation is used.
    
    FALSE: synchronized PNC shutdown is disabled
    TRUE: synchronized PNC shutdown is enabled
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. UdpNmRxPdu

**描述**: This container includes the configuration of Rx PDU properties that are used for the UdpNm Channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmRxPduId
  长名称: ''
  描述: ID of the RxPdu that will be used by a RxIndication of the lower layer.
  默认值: 0
  最小值: 0
  最大值: 4294967296
```

### 4. UdpNmTxPdu

**描述**: This container includes the configuration of Tx PDU properties that are used for the UdpNm Channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmTxConfirmationPduId
  长名称: ''
  描述: |
    Id of the TxPdu that will be used by a TxConfirmation from the lower layer.
    
    RESTRICTIONS: This parameter is only relevant if UdpNmPassiveModeEnabled = False.
  默认值: 0
  最小值: 0
  最大值: 4294967296
```

### 5. UdpNmUserDataTxPdu

**描述**: This optional container is used to configure the UserNm PDU. This container is only available if
UdpNmComUserDataSupport is enabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmTxUserDataPduId
  长名称: ''
  描述: |
    This parameter defines the Handle ID of the NM User Data I-PDU.
    
    RESTRICTIONS: This parameter is only relevant if UdpNmComUserDataSupport = True.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: UdpNmAllowTriggeredMsgTransmission
  长名称: ''
  描述: |
    This parameter defines if changes written to the User Data Pdu triggers an immediate
    transmission of the NM message.
    
    RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False)
    
  默认值: false
  最小值: ''
  最大值: ''
```

### 6. UdpNmPnInfo

**描述**: This container includes the PN information configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmPnInfoLength
  长名称: ''
  描述: |
    Specifies the length of the PN request information in the NM message.
    
    Note that this parameter has to be set to a value less or equal to user data length.
    
    RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.
    This parameter cannot be edited directly in DaVinci Configurator. To change its value, add or
    remove UdpNmPnFilterMaskByte containers.
  默认值: 0
  最小值: 0
  最大值: 63
- 
  序号: 2
  名称: UdpNmPnInfoOffset
  长名称: ''
  描述: |
    Specifies the offset of the PN request information in the NM message.
    
    Note that this parameter has to be set to a valid byte position within the user data of the NM
    PDU.
    
    RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.
  默认值: 1
  最小值: 1
  最大值: 63
```

### 7. UdpNmPnFilterMaskByte

**描述**: This container includes the PN filter mask configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmPnFilterMaskByteIndex
  长名称: ''
  描述: |
    Specifies the offset of the PN request information in the NM message.
    
    RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.
  默认值: 0
  最小值: 0
  最大值: 62
- 
  序号: 2
  名称: UdpNmPnFilterMaskByteValue
  长名称: ''
  描述: |
    This value specifies the filter mask byte.
    This parameter defines the value of the mask byte which is used for the filter algorithm for
    relevant NM messages.
    
    RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 8. UdpNmGeneration

**描述**: Contains the generation configuration parameters of the module UdpNm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmOutOfBoundsWriteSanitizer
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
  名称: UdpNmOutOfBoundsReadSanitizer
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
  名称: UdpNmInterfacesForDeactivatedData
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
```

### 9. UdpNmDemEventParameterRefs

**描述**: not used

该容器没有参数。

