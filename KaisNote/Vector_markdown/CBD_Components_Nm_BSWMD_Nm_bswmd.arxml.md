# Nm

## 模块描述

Network Management Interface (NmIf). The NmIf acts as an adaption layer between AUTOSAR BSW module
ComM and the AUTOSAR BSW bus-specific network management modules (e.g. CanNm). The NmIf also
provides a coordination algorithm to perform a synchronous shutdown handling of several connected
networks and/or multiple BusNms on one channel.
#Interface #forwarding #NetworkManagement #ModeManagement #Shutdown #NM #BusSleep
#AUTOSAR

## 容器列表

### 1. NmChannelConfig

**描述**: This container represents the configuration of one Network Management channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmActiveCoordinator
  长名称: ''
  描述: |
    This parameter indicates whether a NM Coordinator is an active gateway (NmActiveCoordinator =
    TRUE) or a passive.
    
    An active coordinator is the node on the channel that is the last one that withdraws its network
    request. That means that it waits until all other nodes have indicated readiness to sleep and it
    waits for all other channels in the coordinator cluster for being ready to sleep until it
    indicates readiness to sleep itself.
    
    A passive coordinator is a node on the channel that is not the last one that withdraws its
    network request. Instead, the request is withdrawn when all channels in the coordinator cluster
    are ready to sleep and the own node is ready to sleep on the channel.
    
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE. This
    parameter is only valid if 'NmCoordClusterIndex' is defined. This parameter needs to be set to
    true if 'NmCoordinatorSyncSupport' is OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: NmChannelId
  长名称: ''
  描述: |
    Handle ID of the NM channel. The value shall be the same as the ComMChannelId of the ComMChannel
    referenced by NmComMChannelRef. The value of this parameter is calculated automatically at
    validation time.
    
    Implementation Type: NetworkHandleType
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: NmChannelSleepMaster
  长名称: ''
  描述: |
    This parameter shall be set to indicate if the readiness to sleep of this network can be
    absolutely decided by the local node only and that no other nodes can oppose that decision.
    I.e. if this parameter is set to TRUE, the NM coordinator considers that the bus is ready to
    sleep at all times and shall not evaluate the remote sleep indication status. If this parameter
    is set to FALSE, the NM Coordinator evaluates the remote sleep indication status to decide
    whether the bus is ready to sleep or not.
    
    If a Generic BusNm is used that is not able to determine the 'Remote Sleep' State and/or all
    other nodes are always ready to sleep, consider setting this value to true and also consider
    setting the NmGenericBusNmChannelSleepMaster switch to TRUE.
    The setting for an AUTOSAR Standard BusNm is considered as
    - TRUE for J1939Nm
    - FALSE for all other BusNms (CanNm, FrNm, LinNm, UdpNm)
    
    This parameter must not be set to TRUE if other nodes need to keep this node awake althrough the
    own node is ready to sleep.
    
    This parameter needs to be turned ON, if NmGenericBusNmChannelSleepMaster is TRUE for at least
    one Generic BusNm on this channel.
    
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE. This
    parameter is only valid if 'NmCoordClusterIndex' is defined.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: NmCoordClusterIndex
  长名称: ''
  描述: |
    This parameter specifies to which coordination cluster a bus belongs. If this parameter is
    undefined for a channel, the corresponding bus does not belong to an NM coordination cluster.
    
    An NM coordination cluster is a group of networks/busses/channels that shall be shut down
    synchronously. Each NM coordination cluster requires at least two channels that need to be shut
    down synchronously.
    
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: NmPassiveModeEnabled
  长名称: ''
  描述: |
    If set to TRUE the passive mode of the network is enabled. Passive nodes are not able to send NM
    PDUs and therefore cannot keep the network awake. Passive nodes can however be woken up by the
    network by receiving the NM PDUs of other ECUs.
    If set to FALSE, the ECU will be able to keep the network awake by transmitting own NM PDUs.
    
    Restrictions: This parameter is not allowed to be defined in NmChannelConfig, if it is defined
    in NmGlobalFeatures.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: NmShutdownDelayTimer
  长名称: ''
  描述: |
    Parameter not used as the value is determined automatically by the code generator.
    
    The Shutdown Delay Timer is started by the NM Coordinator on an actively coordinated channel
    when readiness for sleep is recognized on all channels in an NM coordination cluster. When the
    timer is elapsed, the Network Request is withdrawn on the BusNm.
  默认值: 0
  最小值: 0
  最大值: 65.535
- 
  序号: 7
  名称: NmStateReportEnabled
  长名称: ''
  描述: |
    If this feature is enabled the Nm module will write state transition information into the Com
    Signal provided by 'NmStateReportSignalRef'. Most likely, the signal is inside the NM User Data
    TX PDU of the BusNm.
    
    false: No NM State is written into the Com Signal.
    true: The NM State is written into the Com Signal.
    
    If enabled, the referenced signal will contain the last state transition of the BusNm. This can
    be one of the following values:
    NM_RM_BSM (1): The last state transition has been from Bus Sleep to Repeat Message
    NM_RM_PBSM (2): The last state transition has been from Prepare Bus Sleep to Repeat Message
    NM_NO_RM (4) : The last state transition has been from Repeat Message to Normal Operation
    NM_NO_RS (8): The last state transition has been from Ready Sleep to Normal Operation
    NM_RM_RS (16): The last state transition has been from Ready Sleep to Repeat Message
    NM_RM_NO (32): The last state transition has been from Normal Operation to Repeat Message
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: NmSynchronizingNetwork
  长名称: ''
  描述: |
    If this parameter is true the network is a synchronizing network for the NM coordination cluster
    which it belongs to. A synchronizing network is a network where the NM message is usually sent
    in a static time pattern and an NM message cannot be sent asynchronously due to the restrictions
    of the underlying bus type (e.g. FrNm) or due to the restrictions of the NM algorithm (e.g. OSEK
    NM).
    If enabled, the network is expected to call Nm_SynchronizationPoint() at regular intervals.
    Otherwise, the NM coordinator does not wait for Nm_SynchronizationPoint() calls.
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE. This
    parameter is only valid if 'NmCoordClusterIndex' is defined. This parameter can only be set to
    TRUE if all channels in the NM Coordination Cluster are actively coordinated, i.e.
    'NmActiveCoordinator' is TRUE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: NmGlobalCoordinatorTimeAllNmOsekInNormal
  长名称: ''
  描述: |
    This parameter defines the maximum shutdown time of a connected and coordinated NM-Cluster if
    all channels equipped with NmOsek are in the NMNormal state, i,e. not in NMLimpHome.
    This time indicates to the NM coordinator how long it takes to shut down all NM coordinated
    channels on all ECUs in the vehicle networks. This is not a hard upper limit, since there may be
    slight time differences due to NM algorithms, call cycles of functions, etc.
    
    For minimum values, refer to the description of NmGlobalCoordinatorTime in the NmGlobalFeatures
    container.
    The only exception for NmOsek channels is that instead of NmGenericBusNmShutdownTime, the result
    of (NmGenericBusNmShutdownTime - (NmOsekErrorWaitBusSleepTime - NmOsekWaitBusSleepTime)) is used
    as BusNm shutdown time.
    
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE and
    NmOsekWaitBusSleepExtensions is TRUE.
    This parameter shall only be defined if and only if the parameter is relevant AND
    NmSynchronizingNetwork is turned ON.
    Note: this parameter is automatically calculated.
  默认值: 0
  最小值: 0
  最大值: 65.535
```

### 2. NmGenericBusNmConfig

**描述**: Choose this container if the underlying BusNm is a Complex Device Driver with a Generic BusNm
Interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmGenericBusNmPrefix
  长名称: ''
  描述: |
    This parameter defines the short name of the lower layer Nm used as <BusNm> prefix. The name is
    used to determine the function names of the APIs provided by the Generic BusNm that are called
    by Nm.
    This string will used for the module prefix in front of the "_" character in the API call name.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: NmGenericBusNmShutdownTime
  长名称: ''
  描述: |
    This parameter defines the time the generic BusNm needs to shut down the channel.
    
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE. This
    parameter is only valid if 'NmCoordClusterIndex' is defined.
  默认值: 0
  最小值: 0
  最大值: 65.535
- 
  序号: 3
  名称: NmGenericBusNmChannelSleepMaster
  长名称: ''
  描述: |
    This parameter shall be set to indicate if the readiness to sleep of the NM algorithm for this
    Generic BusNm can be absolutely decided by the local node only and that no other nodes can
    oppose that decision.
    I.e. if this parameter is set to TRUE, the NM coordinator considers that the BusNm is ready to
    sleep at all times and shall not evaluate the remote sleep indication status. If this parameter
    is set to FALSE, the NM Coordinator evaluates the remote sleep indication status to decide
    whether the BusNm is ready to sleep or not.
    
    Set this parameter to TRUE if this GenericBusNm does not provide the 'Remote Sleep' status (i.e.
    it cannot determine whether the other nodes are ready to sleep) and/or if the own node can
    completely decide on its own that the other nodes are ready to sleep.
    This parameter must not be set to TRUE if other nodes need to keep this node awake althrough the
    own node is ready to sleep.
    
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE and
    'NmChannelSleepMaster' is TRUE. This parameter is only valid if 'NmCoordClusterIndex' is
    defined.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: NmGenericBusNmPduRxIndication
  长名称: ''
  描述: |
    Function called to notify the reception of a NmPdu.
    This function can be used to distinguish between each BusNm on the same channel by using
    different identifiers for each BusNm.
    It is not necessary to configure the function if there is only one BusNm on the channel. The
    NmPduReceiveIndCallback can be used as an alternative for this purpose.
    Function prototype:
    FUNC(void, <MODULE_NAME>_CODE)<FunctionName>(CONST(NetworkHandleType, AUTOMATIC)
    nmNetworkHandle, P2CONST(PduInfoType, AUTOMATIC, AUTOMATIC) pduInfo)
    
    This function can be implemented by the Application, but it can also be used by BswM as a mode
    request port.
    
    Example:
    In a setup with two channels, one of them equipped with one Generic BusNm, the other one
    equipped with another Generic BusNm, there is no distinction required between the BusNms,
    because the Network Handle parameter is different for each channel.
    Therefore it suffices to use NmPduRxIndicationEnabled with NmPduReceiveIndCallback. However,
    this type of notification cannot be realized in BswM.
    If a mode request port in BswM is required, define this parameter to a function name that BswM
    shall implement and configure.
    
    Another example:
    In a setup with one channel equipped with CanNm and NmOsek on the same channel, a distinction of
    which BusNm has received a NM PDU cannot be made by the NmPduReceiveIndCallback, since the
    provided Network Handle is the same.
    Therefore, for a distinction, define this parameter to a certain value for NmOsek and the
    NmStandardBusNmPduRxIndication for the CanNm to a certain value.
    
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. NmStandardBusNmConfig

**描述**: Choose this container if the underlying BusNm is an AUTOSAR standard BusNm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmStandardBusType
  长名称: ''
  描述: |
    Identifies the bus type for standard AUTOSAR <BusNm>s and is used to determine which APIs are to
    be called by the Nm module.
    
    NOTE: The BusNm for Ethernet is UdpNm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: NmStandardBusNmPduRxIndication
  长名称: ''
  描述: |
    Function called to notify the reception of a NmPdu.
    This function can be used to distinguish between each BusNm on the same channel by using
    different identifiers for each BusNm.
    It is not necessary to configure the function if there is only one BusNm on the channel. The
    NmPduReceiveIndCallback can be used as an alternative for this purpose.
    Function prototype:
    FUNC(void, <MODULE_NAME>_CODE)<FunctionName>(CONST(NetworkHandleType, AUTOMATIC)
    nmNetworkHandle, P2CONST(PduInfoType, AUTOMATIC, AUTOMATIC) pduInfo)
    
    This function can be implemented by the Application, but it can also be used by BswM as a mode
    request port.
    
    Example:
    In a setup with two channels, one of them equipped with CanNm, the other one equipped with FrNm,
    there is no distinction required between the BusNms, because the Network Handle parameter is
    different for each channel.
    Therefore it suffices to use NmPduRxIndicationEnabled with NmPduReceiveIndCallback. However,
    this type of notification cannot be realized in BswM.
    If a mode request port in BswM is required, define this parameter to a function name that BswM
    shall implement and configure.
    
    Another example:
    In a setup with one channel equipped with CanNm and NmOsek on the same channel, a distinction of
    which BusNm has received a NM PDU cannot be made by the NmPduReceiveIndCallback, since the
    provided Network Handle is the same.
    Therefore, for a distinction, define this parameter to a certain value for CanNm and the
    NmGenericBusNmPduRxIndication for the NmOsek to a certain value.
    
    RESTRICTIONS: This parameter cannot be defined if NmStandardBusType equals to NM_BUSNM_J1939NM
    or equals to NM_BUSNM_LINNM.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. NmGlobalConfig

**描述**: General configuration parameters of the NM module.

该容器没有参数。

### 5. NmGlobalConstants

**描述**: This container contains module constants related to the NM functionality.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmNumberOfChannels
  长名称: ''
  描述: |
    Defines the number of logical Nm channels the ECU shall handle.
    Parameter not used as the value is determined through the number of NmChannelConfig containers
    by the code generator.
  默认值: 1
  最小值: 1
  最大值: 255
```

### 6. NmGlobalFeatures

**描述**: This container contains module features related to the NM functionality.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmBusSynchronizationEnabled
  长名称: ''
  描述: |
    If enabled, the bus synchronization support of the <BusNm>s is turned ON. This parameter needs
    to be enabled if the NM Coordinator is used on this ECU.
    Bus Synchronization permits an asynchronous message transmission for BusNms that support this
    feature (e.g. CanNm, UdpNm). This feature is required for the NM Coordinator to send the last NM
    message on the Bus that is responsible for restarting the Timeout Timer in the BusNm.
    
    Restrictions: This parameter is only valid if it has the same value as
    'NmCoordinatorSupportEnabled'.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: NmCarWakeUpCallback
  长名称: ''
  描述: |
    Callback function that is called if the BusNm has detected the Car Wake-up Bit being set to 1 in
    the NM message (indicated by a function call of Nm_CarWakeUpIndication()).
    
    Restrictions: Only relevant if 'NmCarWakeUpRxEnabled' is TRUE
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: NmCarWakeUpRxEnabled
  长名称: ''
  描述: |
    Enables or disables Car Wake-Up detection.
    If this option is enabled the Nm reports a detected Car Wake-Up in a received NM message to an
    upper layer (e.g. Complex Device Driver/Application) by calling the function given in
    'NmCarWakeUpCallback'.
    
    false: Car Wake-up is not supported.
    true: Car Wake-up is supported.
    
    It is completely application-specific how to react on this event. This can for instance be used
    for wake-up forwardings, so that all ComM users assigned to communication channels have to
    request FULL COMMUNICATION if this event occurs.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: NmComControlEnabled
  长名称: ''
  描述: |
    If this option is enabled an additional API (CanNm_DisableCommunication(),
    CanNm_EnableCommunication()) is available that allows to enable and disable the transmission of
    NM PDUs at run-time while the NM is in the Normal Operation State. While the transmission is
    disabled the network cannot be released which implies that the network cannot be shut down.
    
    Enable this feature in order to support ISO 14229 Communication Control Service $28.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: NmComUserDataSupport
  长名称: ''
  描述: |
    If enabled NM user data that is transmitted inside the NM PDU is determined through the contents
    of the COM I-PDU configured as NM User Data TX PDU inside the BusNm. The User Data of NM TX
    messages are handled as standard COM Signals and can be set by the application. The API
    Nm_SetUserData is not available.
    If disabled NM user data that is transmitted inside the NM PDU can be set by the API
    Nm_SetUserData.
    
    The NM user data in received NM PDUs is not handled by this feature and can be determined via
    Nm_GetUserData() and/or Nm_GetPduData().
    
    Restrictions: This parameter is only relevant if at least one channel is not passive or the
    CONFIG-VARIANT is not VARIANT-PRE-COMPILE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: NmCoordinatorSupportEnabled
  长名称: ''
  描述: |
    If enabled the NM module allows the coordinated shutdown for all synchronized channels of the
    node. All synchronized channels are kept awake until the readiness to sleep is reached on all
    coordinated channels in one NM Coordination Cluster. Supported Network Managements are CANNM,
    FRNM, LINNM, UDPNM and Generic BusNms. J1939NM is not supported.
    If disabled and a coordinated shutdown is required, the ComM users can be used inside the
    application.
    If wake-up coordination is required, the 'Synchronous Wake-up' feature in ComM can be used and
    the coordination of different channels can be implemented by the application using ComM users.
    
    Restrictions: This parameter is only relevant if at least one channel is not passive or the
    CONFIG-VARIANT is not VARIANT-PRE-COMPILE. If 'NmCoordinatorSupportEnabled' is set to TRUE, then
    'NmRemoteSleepIndEnabled' and 'NmBusSynchronizationEnabled' have to be TRUE.
    
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: NmGlobalCoordinatorTime
  长名称: ''
  描述: |
    This parameter defines the maximum shutdown time of a connected and coordinated NM-Cluster.
    This time indicates to the NM coordinator how long it takes to shut down all NM coordinated
    channels on all ECUs in the vehicle networks. This is not a hard upper limit, since there may be
    slight time differences due to NM algorithms, call cycles of functions, etc.
    The minimum value of this parameter is given as the maximum of:
    CanNmWaitBusSleepTime + CanNmTimeoutTime for all coordinated CAN NM channels
    ((FrNmReadySleepCnt + 1) * FrNmRepetitionCycle * FrCycleTime for all coordinated FR NM channels
    0 for all coordinated LIN NM channels
    UdpNmWaitBusSleepTime + UdpNmTimeoutTime for all coordinated UDP NM channels
    NmGenericBusNmShutdownTime for all coordinated channels with a Generic BusNmIf this parameter is
    not defined, the minimum value as given above is calculated and used for code generation.
    
    Note: This includes connections to coordinators across multiple networks.
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.
  默认值: 0
  最小值: 0
  最大值: 4294967.295
- 
  序号: 8
  名称: NmNodeDetectionEnabled
  长名称: ''
  描述: |
    If this feature is enabled on all nodes of a network other ECUs or a tester have the opportunity
    to detect all present active network nodes of a network.
    The node that transmit an NM PDU with the 'Repeat Message Bit' set to 1, initiates the node
    detection. This can be realized by a Nm_RepeatMessageRequest() function call. This node and all
    nodes that receive this message return back to the 'Repeat Message' state so that their NM PDUs
    can be seen on the bus.
    The function Nm_GetNodeIdentifier() returns the Node Identifier of the most recently received NM
    PDU. This function may be called in the context of Nm_PduRxIndication() and its configured
    callback function in 'NmPduReceiveIndCallback'.
    Thus the algorithm for node detection can be realized by the application or by a Complex Device
    Driver.
    Restrictions: This parameter is only relevant if at least one channel is not passive or the
    CONFIG-VARIANT is not VARIANT-PRE-COMPILE. If 'NmNodeDetectionEnabled' is set to TRUE, then
    'NmNodeIdEnabled' has to be TRUE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: NmNodeIdEnabled
  长名称: ''
  描述: |
    This option provides read access to the local node identifier and to the node identifier
    received in the last NM message. Also, the own node identifier is transmitted in the NM PDU.
    The following APIs are provided if the option is enabled:
    - Nm_GetPduData() to receive the whole data bytes of the most recently received NM PDU.
    - Nm_GetNodeIdentifier() to receive the Node Identifier byte of the most recently received NM
    PDU
    - Nm_GetLocalNodeIdentifier() to receive the Node Identifier byte of own NM TX PDU
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: NmPduRxIndicationEnabled
  长名称: ''
  描述: |
    If enabled a callback function for every received NM PDU will be triggered.
    The name of the callback function is configurable by the parameter 'NmPduReceiveIndCallback'.
    The function provided by this parameter can be implemented in the Application or in a Complex
    Device Driver.
    The function Nm_GetPduData() may be used to access the data bytes (payload) of the received NM
    PDU. In order to use this function, the settings 'NmNodeIdEnabled' and/or 'NmUserDataEnabled'
    must be turned ON.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: NmRemoteSleepIndEnabled
  长名称: ''
  描述: |
    Enable this feature in gateways (e.g. if NM coordinator is used) to allow the remote sleep
    detection. 'Remote Sleep' is a state of the network where all other nodes have indicated their
    readiness to sleep (e.g. in AUTOSAR Standard BusNms due to the absence of the NM PDU/negative
    votes).
    This switch needs to be enabled if the synchronized shutdown of networks has to be carried out.
    It comprises Remote Sleep Indication, Remote Sleep Cancellation and checking of the Remote Sleep
    Indication State.
    If the feature is enabled, the following behavior is activated: Remote Sleep Indication is
    notified to the Nm module when your network node is the only one in the whole network that
    requests bus-communication for 'Remote Sleep Indication Time'.
    Remote Sleep Cancellation is notified if any other network node requires the communication bus
    while Remote Sleep Indication takes place in your network node.
    The Remote Sleep Status can be determined via the API Nm_CheckRemoteSleepIndication().
    Optionally, an upper layer (e.g. Complex Device Driver, Application) can be notified by callback
    function calls about a Remote Sleep Indication and a remote Sleep Cancellation using the
    functions configured in 'NmRemoteSleepIndCallback' and 'NmRemoteSleepCancelCallback'.
    If disabled, the above mentioned notifications do not happen and the API
    Nm_CheckRemoteSleepIndication is not available.
    This feature is required for NM Coordinator nodes.
    
    
    
    Restrictions: This parameter is only relevant if at least one channel is not passive or the
    CONFIG-VARIANT is not VARIANT-PRE-COMPILE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: NmRepeatMsgIndEnabled
  长名称: ''
  描述: |
    If enabled the ECU can request the transmission of NM messages from other nodes in order to
    detect which nodes are present in the network. To request this functionality the API
    Nm_RepeatMessageRequest() has to be called. Activated nodes can then be detected by the
    Application/by a Complex Device Driver through the API Nm_GetNodeIdentifier() that is enabled by
    'NmNodeIdEnabled'. This API determines the Node Identifier of the most recently received NM PDU.
    
    Restrictions: If 'NmRepeatMsgIndEnabled' is set to TRUE, then 'NmNodeDetectionEnabled' has to be
    TRUE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: NmStateChangeIndEnabled
  长名称: ''
  描述: If enabled every change in the NM state machine in the BusNm is reported as a function call to
      Nm_StateChangeNotification(). This state change indication can be forwarded to an upper
      layer (e.g. Complex Device Driver, Application) using the function configured in
      'NmStateChangeIndCallback'.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: NmUserDataEnabled
  长名称: ''
  描述: |
    Enables read and write access to the user data of NM PDUs. The location of user data in the NM
    message depends on the message configuration.
    If enabled, the NM user data can be read from the most recently received NM PDU through the
    APIs:
    - Nm_GetUserData(): determines a pointer to the first user data byte.
    - Nm_GetPduData(): determines a pointer to the first byte of the NM PDU.
    If 'NmComUserDataSupport' is not enabled, the NM User Data Bytes can also be changed through the
    API:
    - Nm_SetUserData().
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: NmMacroLayerEnabled
  长名称: ''
  描述: |
    If enabled, this option can be used to minimize the NM resource consumption ROM, RAM and runtime
    in case 'NmCoordinatorSupportEnabled' is FALSE and in case only one type of BusNm is used.
    If disabled all NM options and features are available.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: NmStateChangeIndCallback
  长名称: ''
  描述: Define the callback function that shall be invoked in case of NM state changes. The function
      is only called if 'NmStateChangeIndEnabled' has been enabled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: NmRemoteSleepIndCallback
  长名称: ''
  描述: |
    Define the remote sleep indication callback. The function is only called if
    'NmRemoteSleepIndEnabled' has been enabled. If no function name is defined, no API call will be
    made.
    The indication will be called when the own node has detected that all other nodes are ready to
    sleep.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: NmRemoteSleepCancelCallback
  长名称: ''
  描述: |
    Define the remote sleep cancellation indication callback. The function is only called if
    'NmRemoteSleepIndEnabled' has been enabled. If no function name is defined, no API call will be
    made.
    The cancellation indication will be called when the own node has detected that it is not the
    only node that is ready to sleep.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: NmPduReceiveIndCallback
  长名称: ''
  描述: If 'NmPduRxIndicationEnabled' is enabled, the configured callback function will be invoked to
      notify an upper layer (e.g. Complex Device Driver, Application) about the reception of
      an NM PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: NmRepeatMessageIndCallback
  长名称: ''
  描述: If 'NmRepeatMsgIndEnabled' is enabled, the configured callback function will be invoked to
      notify an upper layer (e.g. Complex Device Driver, Application) upon the state
      transition to Repeat Message due to a Repeat Message Request issued by any node. The
      repeat message state will be entered and executed by the NM module independently of the
      configured callback function. Note that entering Repeat Message will not always be
      notified, only if it has been entered because of a Repeat Message Request. If an upper
      layer shall always be notified about a state transition, for instance to Repeat Message,
      it is recommended to use the 'NmStateChangeIndEnabled' setting in combination with a
      configured callback function in the parameter 'NmStateChangeIndCallback'.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: NmTxTimeoutErrorCallback
  长名称: ''
  描述: |
    If a function name is configured the configured callback function will be invoked if the
    transmission of a NM PDU has failed due to a TX timeout. The notification may be used by an
    upper layer (e.g. Complex Device Driver) for error reporting.
    
    Restrictions: This parameter is only relevant if at least one channel is not passive or
    CONFIG-VARIANT is not VARIANT-PRE-COMPILE.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: NmCallbacksPrototypeHeader
  长名称: ''
  描述: |
    If any of the configurable callback functions in the Nm is used the name of the header file
    providing the callback prototypes has to be defined here.
    A header file is required for the following callback APIs: State Change Notification, Remote
    Sleep Indication, Remote Sleep Cancellation, Pdu Receive Indication, Repeat Message Indication,
    Tx Timeout Error Notification and/or Car Wakeup Indication.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: NmCoordinatorSyncSupport
  长名称: ''
  描述: |
    Enables/disables the coordinator synchronization support.
    If enabled, there can be active and passive coordinators. To allow synchronization between
    multiple coordinators, the NM PDU also contains a 'Sleep Ready' bit. For the difference of an
    active and a passive coordinator, see also the description of the 'NmActiveCoordinator'
    parameter.
    If disabled, only active coordinators can be used and the 'Sleep Ready' bit in the NM PDU is not
    available.
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: NmSynchronizationTimeoutTime
  长名称: ''
  描述: |
    This parameter defines the maximum waiting time for a synchronization point. After this time, NM
    coordinator will continue the shutdown even if no synchronization point has appeared. If the
    time is set to 0, the NM module will not force any shutdown without a synchronization point.
    A 'synchronization point' in this context is a notification that the BusNm has reached a state
    where usually the NM message is being sent or another NM algorithm-specific event has occurred
    that is relevant for the shutdown timing. See also the description of the parameter
    'NmSynchronizingNetwork'.
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE and at
    least one channel is a synchronizing network.
  默认值: 0
  最小值: 0
  最大值: 65.535
- 
  序号: 25
  名称: NmRuntimeMeasurementSupport
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
  序号: 26
  名称: NmPassiveModeEnabled
  长名称: ''
  描述: |
    If set to TRUE the passive mode of all networks is enabled. Passive nodes are not able to send
    NM PDUs and therefore cannot keep the network awake. Passive nodes can however be woken up by
    the network by receiving the NM PDUs of other ECUs.
    If set to FALSE, the ECU will be able to keep the network awake by transmitting own NM PDUs. The
    functions Nm_NetworkRequest() and Nm_NetworkRelease() will be available.
    If set to TRUE, the ECU will not be able to keep all networks awake by transmitting own NM PDUs.
    The functions Nm_NetworkRequest() and Nm_NetworkRelease() will not be available.
    If this parameter is not defined, the NmPassiveModeEnabled switch needs to be defined in each
    NmChannelConfig. This way, Passive Mode can be set individually for each network.
    
    Restrictions: This parameter is only valid if 'NmPassiveModeEnabled' is not defined in every
    NmChannelConfig.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: NmCoordinatorRequestChannelsInBusSleep
  长名称: ''
  描述: |
    Enables/disables the support to request channels that are in Bus Sleep Mode.
    If enabled, channels that belong to a coordination cluster are also requested
    (BusNm_NetworkRequest() call) if they are in Bus Sleep Mode if there is any reason to abort the
    coordinated shutdown.
    If disabled, only those channels are requested that are not in Bus Sleep mode if there is any
    reason to abort the coordinated shutdown.
    
    This behavior can be used to have an alternative to 'Synchronous Wake-up' at ComM that requests
    only the channels that belong to a coordination cluster.
    
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: NmBusNmSpecificPduRxIndicationEnabled
  长名称: ''
  描述: |
    Enables/disables the generation of a BusNm specific callback that shall be called by the BusNm
    upon reception of the RxNmPdu.
    
    The BusNm shall call this function instead of Nm_PduRxIndication to have a distinction between
    the BusNm if there are multiple BusNm on one channel.
    However, Nm_PduRxIndication() can also be called instead of the specific BusNm Pdu RxIndication.
    
    BusNm shall not call both functions.
    
    RESTRICTIONS:
    The functions are generated only for CAN channels.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: NmCoordinatorPassiveStartUpForwarding
  长名称: ''
  描述: |
    Enables/disables the direct call of BusNm_PassiveStartUp when calling Nm_PassiveStartUp.
    
    If enabled, the algorithm of the coordinator has a special handling in which the call of
    Nm_PassiveStartUp leads always to a BusNm_PassiveStartUp. Shortly after, the coordinator
    algorithm will call BusNm_NetworkRequest
    
    Use this switch if the active wake up bit is used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: NmSynchronizedPncShutdownEnabled
  长名称: ''
  描述: |
    Enables or disables support of synchronized PNC shutdown.
    
    FALSE: synchronized PNC shutdown is disabled. This is the default setting.
    
    TRUE: synchronized PNC shutdown is enabled.
    
    Dependencies:
    This feature can only be enabled for ECUs in the role of a Top-Level-PNC-Coordinator (TLPC) or
    an intermediate PNC coordinator. It cannot be enabled for subordinated (or leaf) nodes.
    This feature can only be enabled if NmCoordinatorSupportEnabled is deactivated.
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. NmGlobalProperties

**描述**: This container contains module properties related to the NM functionality.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmCycletimeMainFunction
  长名称: ''
  描述: |
    The period between successive calls to the NM Main Function (Nm_MainFunction()).
    
    Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.
  默认值: 0.01
  最小值: 0.001
  最大值: 0.255
- 
  序号: 2
  名称: NmDevErrorDetect
  长名称: ''
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
  序号: 3
  名称: NmVersionInfoApi
  长名称: ''
  描述: This parameter enables/disables the function Nm_GetVersionInfo() to get major, minor and patch
      version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: NmUserConfigFile
  长名称: ''
  描述: |
    Reference to an external user configuration file that will be included during generation.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: NmSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
```

### 8. NmGeneration

**描述**: Contains the generation configuration parameters of the module Nm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmOutOfBoundsWriteSanitizer
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
  名称: NmOutOfBoundsReadSanitizer
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
  名称: NmShortSymbols
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
  序号: 4
  名称: NmInterfacesForDeactivatedData
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
  序号: 5
  名称: NmReferringKeysInComments
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

