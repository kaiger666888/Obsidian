# SoAd

## 模块描述

The Socket Adaptor is an interface between an AUTOSAR communication service module using PDUs and a
socket based TCP/IP stack.
#Ethernet #SomeIpSd
#AUTOSAR

## 容器列表

### 1. SoAdBswModules

**描述**: Each container describes a specific BSW module that the SoAd shall interface to.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdIf
  长名称: ''
  描述: This parameter defines if the BSW module supports the Communication Interface APIs or not.
      Value true means that the APIs are supported. A module can have both Communication
      Interface APIs and Transport Protocol APIs (e.g. the PduR module).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdIfTriggerTransmit
  长名称: ''
  描述: This parameter defines if the BSW module supports the TriggerTransmit API or not. Value true
      means that the API is supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdIfTxConfirmation
  长名称: ''
  描述: This parameter defines if the BSW module supports the TxConfirmation API or not. Value true
      means that the API is supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SoAdLocalIpAddrAssigmentChg
  长名称: ''
  描述: This parameter defines if the BSW module supports the LocalIpAddrAssigmentChg API or not.
      Value true means that the API is supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SoAdSoConModeChg
  长名称: ''
  描述: This parameter defines if the BSW module supports the SoConModeChg API or not. Value true
      means that the API is supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SoAdTp
  长名称: ''
  描述: This parameter defines if the BSW module supports the TransportProtocol APIs or not. Value
      true means that the APIs are supported. A module can have both Communication Interface
      APIs and Transport Protocol APIs (e.g. the PduR module).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SoAdUseCallerInfix
  长名称: ''
  描述: This parameter defines if SoAd shall use (TRUE) the infix "SoAd" when calling an upper layer
      module function or not (FALSE). E.g. if SoAdUseCallerInfix is TRUE for the upper layer
      "ABC" then SoAd will call ABC_SoAdIfRxIndication() otherwise SoAd would call
      ABC_IfRxIndication().
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdUseTypeInfix
  长名称: ''
  描述: This parameter defines if SoAd shall use (TRUE) the API type infix "Tp" or "If" when calling
      an upper layer module function or not (FALSE). E.g. if SoAdUseTypeInfix is TRUE for the
      upper layer "ABC" then SoAd will call ABC_IfRxIndication(), otherwise SoAd would call
      ABC_RxIndication().
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SoAdShutdownFinishedCbk
  长名称: ''
  描述: This parameter enables a callback which is called if SoAd is in shutdown state after
      successful call to SoAd_Shutdown().
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: SoAdTpCopyTxDataWithConstPointer
  长名称: ''
  描述: This parameter specifies if the upper layer Ul_[SoAd][Tp]CopyTxData() function is implemented
      with constant pointer for parameter "info".
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SoAdTpCopyRxDataWithConstPointer
  长名称: ''
  描述: This parameter specifies if the upper layer Ul_[SoAd][Tp]CopyRxData() function is implemented
      with constant pointer for parameter "info".
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: SoAdTpStartOfReceptionWithConstPointer
  长名称: ''
  描述: This parameter specifies if the upper layer Ul_[SoAd][Tp]StartOfReception() function is
      implemented with constant pointer for parameter "info".
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. SoAdConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR SoAd module.
This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist
once per configuration set.

该容器没有参数。

### 3. SoAdPduRoute

**描述**: Describes the path of a PDU from an upper layer of the SoAd to the socket in the TCP/IP stack for
transmission.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdTxPduId
  长名称: PDU ID
  描述: This value specifies the Tx PDU ID of the PDU coming from the PDU Router.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SoAdTxUpperLayerType
  长名称: Upper Layer Type
  描述: This paramater defines the upper layer interface type (must be "IF" in case of multiple
      PduRoutes).
  默认值: IF
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdTxIfTriggerTransmit
  长名称: If Trigger Transmit
  描述: |
    This parameter defines if this PDU is transmitted via TriggerTransmit API.
    true: On transmission current value is retrieved via call to TriggerTransmit API of upper layer.
    false: Transmission is performed in context of transmit service.
    
    In context of nPduUdpTxBuffer this behavior can be used to optimize the nPduUdpTxBuffer and
    replace it by a request queue.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SoAdTxTpOptimized
  长名称: Tp Optimized
  描述: |
    This parameter defines if optimization for TP transmission shall be used for this PDU.
    true: SoAd handles transmission in context of SoAd_TpTransmit i.e. TpCopyTxData and
    TpTxConfirmation of upper layer may be called in context of SoAd_TpTransmit.
    false: SoAd stores transmission request in SoAd_TpTransmit and handles transmission in
    SoAd_MainFunction (accroding to AUTOSAR).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SoAdTxIfOptimized
  长名称: If Optimized
  描述: |
    This parameter defines if optimization for IF transmission shall be used for this PDU.
    true: SoAd handles the transmission in context of SoAd_IfTransmit. This means
    Ul_[SoAd][If]TxConfirmation and Ul_[SoAd][If]TriggerTransmit of upper layer may be called in
    context of SoAd_IfTransmit.
    false: SoAd stores and forwards transmission requests according to AUTOSAR
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SoAdTxIfTriggerTransmitForceSingleCall
  长名称: If Trigger Transmit Force Single Call
  描述: |
    This parameter defines if the Ul_[SoAd][If]TriggerTransmit API is forced to be called only once.
    In case of a PDU fan-out, SoAd calls Ul_[SoAd][If]TriggerTransmit for each SoAdSocketConnection,
    otherwise. If this parameter is enabled, a SoAdIfTriggerTransmitBuffer is used to store the PDU
    data retrieved by Ul_[SoAd][If]TriggerTransmit before initiating the PDU fan-out.
    true: SoAd calls Ul_[SoAd][If]TriggerTransmit only once.
    false: SoAd calls Ul_[SoAd][If]TriggerTransmit for each SoAdSocketConnection.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SoAdTxIfOptimisticTransmit
  长名称: If Optimistic Transmit
  描述: |
    This parameter defines if the return value of an IF transmission procedure shall be handled
    optimistic in case of transmission fan-out on more than one PduRouteDest.
    true: Transmission is handled as successful (SoAd_IfTransmit returns E_OK) in case transmission
    succeeded at least for one PduRouteDest of the PduRoute.
    false: Transmission is only handled as successful in case transmission succeeded for all
    PduRouteDest of the PduRoute (standard AUTOSAR behavior).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdTxPduCollectionSemantics
  长名称: ''
  描述: |
    This parameter defines if this PDU shall be collected using a queued or last-is-best semantics.
    This parameter is only relevant if the PDU collection feature is enabled.
    This parameter depends on SoAdTxIfTriggerTransmit.
    For SOAD_COLLECT_LAST_IS_BEST set SoAdTxIfTriggerTransmit to true.
    For SOAD_COLLECT_QUEUED set SoAdTxIfTriggerTransmit to false.
  默认值: SOAD_COLLECT_QUEUED
  最小值: ''
  最大值: ''
```

### 4. SoAdPduRouteDest

**描述**: Specifies the PDU route destination.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdTxPduHeaderId
  长名称: PDU Header ID
  描述: This value specifies the ID to be sent on the TCP/IP connection if the PDU header option is
      enabled.
  默认值: 0
  最小值: 0
  最大值: 4294967296
- 
  序号: 2
  名称: SoAdTxUdpTriggerMode
  长名称: UDP Trigger Mode
  描述: |
    This parameter defines whether a PDU triggers the transmission of the nPduUdpTxBuffer.
    NPduUdpTxBuffer can only be used for upper layers with "IF" API, i.e. this parameter shall only
    be set if all upper layers belonging to the related socket connection have SoAdTxUpperLayerType
    set to "IF".
    This parameter is only relevant for UDP connections.
    
    TRIGGER_ALWAYS: PDU transmission triggers transmission of nPduUdpTxBuffer
    TRIGGER_NEVER: PDU transmission is stored in nPduUdpTxBuffer and triggers nPduUdpTxBuffer
    transmission only if buffer size is not sufficient
    
    Note: nPduUdpTxBuffer is not required in case TRIGGER_ALWAYS is used on all related
    SoAdPduRouteDest.
  默认值: TRIGGER_ALWAYS
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdTxUdpTriggerTimeout
  长名称: UDP Trigger Timeout
  描述: |
    This value specifies the timeout in [s] the nPduUdpTxBuffer shall be transmitted at the latest
    after this PDU is put into the buffer. This optional parameter is only relevant if
    SoAdTxUdpTriggerMode is TRIGGER_NEVER.
    
    Note: In case the timeout is configured to a value smaller than the SoAdMainFunctionPeriod the
    timeout is set to one main funtion cycle.
  默认值: 2
  最小值: 0
  最大值: 65535
```

### 5. SoAdRoutingGroup

**描述**: Each container describes a specific routing group which can be enabled or disabled. A routing group
consists of PDUs. Routing of PDUs can either be forwarding of PDUs from the upper layer to a TCP or
UDP socket of the TCP/IP stack specified by a SoAdPduRoute or the other way around specified by a
SoAdSocketRoute.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdRoutingGroupId
  长名称: Routing Group ID
  描述: This value specifies a unique ID of Routing Group
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SoAdRoutingGroupIsEnabledAtInit
  长名称: Enable at Initialization
  描述: This parameter defines if this routing group is enabled (TRUE) after initializing the SoAd
      module (i.e. enabled in the SoAd_Init function) or not (FALSE).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdRoutingGroupTxTriggerable
  长名称: Enable Tx Triggerable
  描述: This parameter defines if the IF Tx-PDUs related to the PduRouteDest containers referenced by
      this routing group can be triggered via SoAd_IfRoutingGroupTransmit (TRUE) or not
      (FALSE).
  默认值: false
  最小值: ''
  最大值: ''
```

### 6. SoAdSocketConnectionGroup

**描述**: Specifies the configuration of a socket connection group, i.e. specifies the socket connections
belonging to the group and the parameters which are common for all socket connections of the group.
A socket connection specifies how data can be received and transmited via a TCP or UDP socket.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdPduHeaderEnable
  长名称: Enable PDU Header
  描述: |
    This parameter defines the usage of the PDU header (ID, length) on all socket connections of
    this group.
    TRUE: Add SoAd PDU header before PDU data.
    FALSE: No SoAd PDU header is used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdSocketAutomaticSoConSetup
  长名称: Enable Automatic Socket Connection Setup
  描述: This parameter defines if the setup of the socket connection shall be done automatically
      (TRUE) or manually (FALSE) via SoAd_OpenSoCon() and SoAd_CloseSoCon().
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdSocketFramePriority
  长名称: Ethernet Frame Priority
  描述: |
    This value specifies the priority of the Ethernet frame.
    If IEEE 802.1Q VLAN Tags are used, the specified priority will be used in the VLAN Tag PCP
    field. If this optional parameter is not available the default priority specified in the TcpIp
    module is used.
  默认值: 7
  最小值: 0
  最大值: 7
- 
  序号: 4
  名称: SoAdSocketIpAddrAssignmentChgNotification
  长名称: Enable IP Address Assignment Change Notification
  描述: This parameter defines if the local IP address assignment change notification callback
      function of the upper layer shall be called if the assignment of the local IP address
      used by this socket connection changes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SoAdSocketLocalPort
  长名称: Local Port
  描述: This value specifies the local UDP or TCP port used for this connection. If this parameter is
      set to 0 SoAd requests TcpIp to select an ephemeral port.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: SoAdSocketMsgAcceptanceFilterEnabled
  长名称: Enable Message Acceptance Filter
  描述: |
    This parameter defines if the message acceptance filter is enabled (TRUE) or not (FALSE).
    Note: if a wildcard is used in SoAdSocketRemoteAddress AND SoAdSocketUdpListenOnly is FALSE,
    this parameter must be TRUE.
    Note: if multiple SoAdSocketConnections are configured for one SoAdSocketConnectionGroup, this
    parameter must be TRUE.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SoAdSocketSoConModeChgNotification
  长名称: Enable Socket Connection Mode Change Notification
  描述: This parameter defines if the SoCon mode change notification callback function of the upper
      layer shall be called in case of SoCon mode change.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdSocketTpRxBufferMin
  长名称: Minimum TP Rx Buffer
  描述: |
    This value specifies the amount of data in bytes (PDU data for the upper layer and PDU Header if
    used) the SoAd shall at least be able to buffer for data reception via each socket connection of
    the socket connection group and using an upper layer with TP.
    Note: in case of a TCP socket where PduHeaderMode is used and an upper layer with IF-API, the
    required buffer size can be determined automatically.
  默认值: 512
  最小值: 0
  最大值: 65535
- 
  序号: 9
  名称: SoAdBestMatchWithSockRouteEnabled
  长名称: Enable Best Match Algorithm with SocketRoute validation
  描述: |
    This parameter defines if the best match algorithm for this socket connection group considers
    that a socket route is configured for a socket connection.
    This means: The best match algortihm will not choose a socket connection which has no receiver
    even if the remote address matches in case this parameter is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: SoAdBestMatchWithPduHeaderEnabled
  长名称: Enable Best Match Algorithm with PDU Header validation
  描述: |
    This parameter defines if the best match algorithm of this socket connection group considers the
    received PDU Header when choosing a socket connection. A received PDU is discarded if no socket
    route could be found containing the corresponding PDU Header ID in case this parameter is
    enabled.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SoAdSocketAutomaticSoConSetupKeepOnline
  长名称: Enable Automatic Socket Connection Setup Keep Online
  描述: |
    This parameter defines if the socket connection is kept online on transmission in case automatic
    socket connection setup is used together with a remote address containing wildcards.
    According to AUTOSAR, a socket connection can be opened on UDP reception or on TCP connection
    establishment. This applies if the configured remote address contains wildcards. After
    transmission of a PDU, the socket connection shall be closed.
    
    TRUE: The socket connection is not closed on PDU transmission.
    FALSE: The socket connection is closed on PDU transmission (standard AUTOSAR behavior).
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: SoAdMeasurementDataSomeIpSdType
  长名称: ''
  描述: |
    This parameter enables/disables the SOME/IP and SD measurement data counting invalid service IDs
    and method IDs inside the PDU header for all socket routes of the socket connection group. This
    is only possible if SoAdGetAndResetMeasurementDataSomeIpSd == TRUE.
    
    NONE: Counting of invalid IDs is not enabled for this socket connection group.
    SOME_IP: Invalid service and method IDs are counted into the SOME/IP counters.
    SOME_IP_SD: Invalid service and method IDs are counted into the SOME/IP SD counters.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: SoAdSocketDifferentiatedServicesField
  长名称: ''
  描述: |
    This value specifies the 6-bit Differentiated Service Field in the IP headers which may be used
    for classifying network traffic.
    
    This parameter is not yet supported and its value is not evaluated but the parameter exists for
    compatibility reasons.
  默认值: 0
  最小值: 0
  最大值: 63
- 
  序号: 14
  名称: SoAdSocketFlowLabel
  长名称: ''
  描述: |
    This value specifies the 20-bit Flow Label field in the IPv6 header which may be used by a
    source to label sequences of packets for which it requests special handling by the IPv6 routers,
    such as non-default quality of service.
    
    This parameter is not yet supported and its value is not evaluated but the parameter exists for
    compatibility reasons.
  默认值: 0
  最小值: 0
  最大值: 1048575
- 
  序号: 15
  名称: SoAdSocketPathMTUEnable
  长名称: ''
  描述: |
    This parameter defines if path MTU discovery shall be performed for this connection.
    
    This parameter is not yet supported and its value is not evaluated but the parameter exists for
    compatibility reasons.
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. SoAdSocketConnection

**描述**: Specifies the socket connection (Id and remote address information).
Note: Parameters which are common to all socket connections of a socket connection group are
specified directly on the group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketId
  长名称: Socket Connection ID
  描述: This value specifies the unique identifier of the socket connection.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SoAdSocketGetReceivedRemoteAddressEnabled
  长名称: ''
  描述: |
    This parameter defines the ability to store the remote IP address of the last received data on
    the corresponding Socket Connection.
    
    The remote IP address can be retrived by the upper layer by calling the SoAd_GetRcvRemoteAddr()
    API with the corresponding Socket Connection ID as function parameter.
    
    false:    Remote IP address of last received data on Socket Connection isn't stored
    true:     Remote IP address of last received data on Socket Connection is stored and can be
    retrieved by calling the SoAd_GetRcvRemoteAddr() API
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdTcpTxQueueSize
  长名称: ''
  描述: This parameter defines the size of a TxQueue to support parallel transmission requests on TCP
      and a streaming-based TxConfirmation.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: SoAdVerifyRxPduEnable
  长名称: ''
  描述: |
    This parameter enables the usage of the Rx PDU verification callback on this socket connection.
    The corresponding callback is configured by parameter SoAdVerifyRxPduCallback.
  默认值: false
  最小值: ''
  最大值: ''
```

### 8. SoAdSocketRemoteAddress

**描述**: Subcontainer of SoAdSocketConnection to specify the remote address (IP address and port) for a
socket connection.
If remote address contains wildcards socket connection cannot be opened (set to online). The remote
address has to be overwritten at runtime via API call, on UDP frame reception or via TCP connection
establishment.
If SoAdSocketRemoteAddress is not specified the remote address has to be set by the upper layer via
SoAd_SetRemoteAddr().

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketRemoteIpAddress
  长名称: Remote IP Address
  描述: |
    This parameter defines the IP address of remote node.
    To accept any remote IP address, leave this parameter empty. See message acceptance policy for
    more details.
    If this parameter is empty (wildcard) socket connection cannot be openned (set to online). The
    remote address has to be overwritten at runtime via API call, on UDP frame reception or via TCP
    connection establishment.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdSocketRemotePort
  长名称: Remote Port
  描述: |
    This value specifies the UDP or TCP port of remote node.
    To accept any remote port, set SoAdSocketRemotePort to 0. See message acceptance policy for more
    details.
    If this parameter is set to 0 socket connection cannot be openned (set to online). The remote
    address has to be overwritten at runtime via API call, on UDP frame reception or via TCP
    connection establishment.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SoAdSocketRemoteIpAddressNotSet
  长名称: Remote IP Address not set
  描述: |
    This parameter defines whether remote IP address is set (valid or wildcard) or not set.
    
    True: IP address not set,
    False: IP address set (valid/wildcard).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SoAdSocketRemotePortNotSet
  长名称: Remote Port not set
  描述: |
    This parameter defines whether remote port is set (valid or wildcard) or not set.
    
    True: port not set,
    False: port set (valid/wildcard).
  默认值: false
  最小值: ''
  最大值: ''
```

### 9. SoAdSocketTcp

**描述**: Specifies that TCP is used as transport protocol for the socket connection group and parameters only
related to TCP socket connections.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketTcpImmediateTpTxConfirmation
  长名称: Enable Immediate Tx Confirmation
  描述: This parameter defines when SoAd notifies the TP upper layer via transmit confirmation. If set
      to FALSE, SoAd notifies the TP upper layer via transmit confirmation after a Tcp Ack has
      been received. If set to TRUE, SoAd notifies the TP upper layer via transmit
      confirmation immediately after transmit has been accepted by TcpIp.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdSocketTcpInitiate
  长名称: Initiate TCP Connection
  描述: |
    This parameter defines the initiator for this TCP connection. It will not be defined for UDP
    sockets.
    TRUE: This TCP connection is initiated by this module.
    FALSE: This TCP connection is to be initiated in the listen mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdSocketTcpKeepAlive
  长名称: Enable Keep Alive
  描述: |
    This parameter defines if the keep-alive mechanism is used for this connection. It will not be
    defined for UDP sockets.
    TRUE:      This TCP connection will use the keep-alive mechanism.
    FALSE:     This TCP connection will not use the keep-alive mechanism.
    
    Note: This parameter must not be set to TRUE if TcpIpTcpKeepAliveEnabled is set to
    FALSE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SoAdSocketTcpKeepAliveInterval
  长名称: Keep Alive Interval
  描述: |
    This value specifies the interval in seconds between subsequent keepalive probes.
    
    Note: The configured value is forwarded to the TcpIp as integer value in seconds. If the value
    is configured with a higher accuracy, the additional digits are truncated.
  默认值: 1
  最小值: 0
  最大值: 4294967
- 
  序号: 5
  名称: SoAdSocketTcpKeepAliveProbesMax
  长名称: Maximum Keep Alive Probes
  描述: This value specifies the maximum number of times that TCP retransmits an individual data
      segment before aborting the connection.
  默认值: 1
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: SoAdSocketTcpKeepAliveTime
  长名称: Keep Alive Time
  描述: |
    This value specifies the time in seconds between the last data packet sent and the first
    keepalive probe.
    
    Note: The configured value is forwarded to the TcpIp as integer value in seconds. If the value
    is configured with a higher accuracy, the additional digits are truncated.
  默认值: 7200
  最小值: 0
  最大值: 4294967
- 
  序号: 7
  名称: SoAdSocketTcpNoDelay
  长名称: Disable TCP Congestion Control
  描述: |
    This parameter defines if the congestion control mechanism for this connection is used. It will
    not be defined for UDP sockets.
    TRUE: This TCP connection will NOT use congestion control.
    FALSE: This TCP connection will use congestion control.
    If the optional parameter is not enabled, the default behavior configured for TcpIp via the
    parameter TcpIpTcpNagleEnabled is applied.
    Note: This parameter must not be set to FALSE if TcpIpTcpNagleEnabled is set to FALSE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdSocketTcpTxQuota
  长名称: Transmission Quota
  描述: This parameter is not applicable and its value is not evaluated but the parameter exists for
      compatibility reasons.
  默认值: 4294967295
  最小值: 0
  最大值: 4294967295
- 
  序号: 9
  名称: SoAdSocketTcpTxBufferMin
  长名称: Minimum Tx Buffer
  描述: This value specifies a minimum transmission buffer size the TcpIp must be able to provide on
      each socket connection of this group. The value is forwarded to TcpIp on socket creation
      at runtime. If this optional parameter is not configured TcpIp will use a default value.
  默认值: 512
  最小值: 1
  最大值: 65535
- 
  序号: 10
  名称: SoAdSocketTcpMsl
  长名称: Maximum Segment Lifetime
  描述: |
    This value specifies a socket specific maximum segment lifetime (MSL). The configured value is
    used instead of TcpIpTcpMsl for the corresponding socket. The SoAd calls TcpIp_ChangeParameter
    to apply the MSL configuration at runtime.
    
    Note: The configured value is forwarded to the TcpIp as integer value in milliseconds. If the
    value is configured with a higher accuracy, the additional digits are truncated.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 11
  名称: SoAdSocketTcpAutoConnectTimeout
  长名称: ''
  描述: |
    This value specifies the time in seconds how long TCP connection attempts are repeated to reach
    SOAD_SOCON_ONLINE. This parameter is restricted to socket connection groups which are initiating
    a TCP connection and are under control of SoAd (SoAdSocketAutomaticSoConSetup and
    SoAdSocketTcpInitiate are enabled in SoAdSocketConnectionGroup).
    
    Note 1: A value of 0 means that the feature is disabled.
    Note 2: This parameter and the related functionality is introduced with ASR R21-11.
    
  默认值: 0
  最小值: 0
  最大值: 4294967
```

### 10. SoAdSocketUdp

**描述**: Specifies that UDP is used as transport protocol for the socket connection group and parameters only
related to UDP socket connections.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketUdpAliveSupervisionTimeout
  长名称: Alive Supervision Timeout
  描述: |
    This value specifies the time in [s] a UDP socket connection remains in the mode
    SOAD_SOCON_ONLINE after the latest reception of a frame from the remote peer specified by the
    remote address. If this optional parameter is not enabled UDP Alive Supervision is deactivated
    for the related socket connection group.
    
    Note: In case the timeout is configured to a value smaller than the SoAdMainFunctionPeriod the
    timeout is set to one main funtion cycle.
  默认值: 1
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SoAdSocketUdpListenOnly
  长名称: Enable Listen Only
  描述: This parameter defines if the socket connection group is only used for reception (TRUE) or
      used for both reception and transmission (FALSE).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdSocketUdpStrictHeaderLenCheckEnabled
  长名称: ''
  描述: This parameter defines if UDP messages shall be dropped (TRUE) if the length of all contained
      PDUs does not match the length of the whole message or not (FALSE). Shall only be set to
      TRUE if SoAdPduHeaderEnable is also set to TRUE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SoAdSocketUdpTriggerTimeout
  长名称: Timeout for Trigger Transmission
  描述: |
    This value specifies the timeout in [s] a nPduUdpTxBuffer is waiting for a PDU with TriggerMode
    = TRIGGER_ALWAYS, i.e. when the timeout expires the nPduUdpTxBuffer is transmitted. Timer is
    reset after each UDP transmission. This optional parameter is only relevant if a nPduUdpTxBuffer
    is used.
    
    Note: In case the timeout is configured to a value smaller than the SoAdMainFunctionPeriod the
    timeout is set to one main funtion cycle.
  默认值: 2
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: SoAdSocketnPduUdpTxBufferMin
  长名称: Socket nPdu Udp Tx Buffer Min
  描述: |
    This value specifies the amount of data in bytes (PDU data provided by the upper layer and PDU
    Header if used) the SoAd shall be able to buffer for data transmission via this socket
    connection in case the UDP message shall be buffered for transmission of multiple PDUs per UDP
    (nPduUdpTxBuffer).
    
    This parameter must not exist if no nPduUdpTxBuffer is used.
    Note: in case of a UDP socket and an upper layer with TP API or an upper layer with IF API with
    UDP transmit retry (for single PDUs) configured, the required buffer size can be determined
    automatically.
  默认值: 32
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: SoAdSocketUdpChecksumEnabled
  长名称: Enable Checksum
  描述: |
    This parameter specifies if UDP checksum calculation shall be enabled (TRUE) or disabled (FALSE)
    on the related socket. FALSE implies that the upper layer of the socket connection is either
    capable to handle malformed messages or applies a checksum mechanism itself.
    
    Note:
    This parameter is ignored when SoAdSocketUdpChecksumChangeEnabled is disabled.
    
    When the parameter is set to FALSE the following applies:
     Rx: Checksum of 0 is accepted and the frame is forwarded. Checksums unequal to 0 will be
    checked.
     Tx: Checksum is not calculated and the value is set to 0.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SoAdSocketUdpAddressResolutionRetryEnabled
  长名称: Enable Address Resolution Retry
  描述: |
    This parameter defines if a transmission request shall be stored in TcpIp module to retry
    transmission in case of missing address resolution (ARP/NDP).
    True: Retry enabled
    False: Retry disabled
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdSocketUdpImmediateIfTxConfirmation
  长名称: ''
  描述: |
    This parameter defines the ability to notify the IF upper layers via TX Confirmation in context
    of Ethernet driver's TX Confirmation.
    
    All upper layers using a Socket Connection of a Socket Connection Group configured for UDP
    communication with this feature enabled will be notified by the TX Confirmation in context of
    Ethernet driver's TX Confirmation.
    
    false:    Upper Layers are notified by the TX Confirmation called in next main function cycle of
    SoAd (Task-Context). The call is independent from the TX Confirmation by the lower layer of
    SoAd.
    true:    Upper Layers are notified by the TX Confirmation propagated through the Ethernet Stack
    starting by the Ethernet Driver (Task- or Interrupt-Context).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SoAdSocketUdpImmediateIfTxConfirmationListSize
  长名称: ''
  描述: |
    This value specifies the size of a list which is used in the TcpIp module to handle UDP
    transmissions with TxConfirmation.
    Please refer to TcpIp parameter "TcpIpUdpTxReqListSize" for more details.
    
    This parameter is used if "SoAdSocketUdpImmediateIfTxConfirmation" is enabled.
    
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 10
  名称: SoAdSocketnPduUdpTxQueueSize
  长名称: Socket n Pdu Udp Tx Queue Size
  描述: |
    This value specifies the size of a management queue for each socket connection. This queue is
    used to manage PDUs in the nPduUdpTxBuffer and PDU transmission requests for trigger transmit.
    Both transmission types are stored within one queue, so make sure that size is sufficient for
    all related SoAdPduRoutes.
    
    This parameter must not exist if no related SoAdPduRoute exisits with enabled
    SoAdTxIfTriggerTransmit.
  默认值: 2
  最小值: 1
  最大值: 255
- 
  序号: 11
  名称: SoAdSocketUdpAddressResolutionRetryQueueLimit
  长名称: ''
  描述: |
    This value specifies the limitation of maximum used UDP transmission retry queue elements for
    this socket.
    The value is forwarded to the TcpIp module on socket creation.
    Example: A transmission over a UDP socket fails in TcpIp module since address resolution (ARP)
    is not finished yet. This transmission is stored in the retry queue and the transmission request
    is assumed as successful. If the limitation is set to 1 TcpIp will reject further transmission
    requests until retry queue element is released.
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: SoAdSocketUdpChecksumChangeEnabled
  长名称: Enable Change of Checksum
  描述: |
    This parameter defines if UDP checksum calculation setting shall be changed (TRUE) or not
    (FALSE) on the related socket. If enabled, the SoAd calls TcpIp_ChangeParameter with the
    corresponding value of SoAdSocketUdpChecksumEnabled to apply the UDP checksum calculation
    configuration at runtime.
    
    Note:
    This parameter must be disabled when...
    ...UDP frames are used via IPv6. A checksum is mandatory in this case.
    ...vBsdAd TcpIp is used (SoAdVBsdAdUsed).
    
    Additionally, when UDP checksum offloading is done in hardware (EthCtrlEnableOffloadChecksumUDP)
    this parameter is usually expected to be disabled. If you enable it be aware that HW could
    overwrite checksums of '0' with a valid calculated checksum which can not be detected by SW.
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. SoAdSocketRoute

**描述**: Describes the path of a PDU from a socket in the TCP/IP stack to an upper layer of the SoAd after
reception in the TCP/IP Stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdRxPduHeaderId
  长名称: PDU Header ID
  描述: This value specifies the ID contained in the packet received on the TCP/IP connection if the
      PDU header option is enabled.
  默认值: 0
  最小值: 0
  最大值: 4294967296
```

### 12. SoAdSocketRouteDest

**描述**: Describes the upper layer destination PDU for a message received on a TcpIp socket.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdRxPduId
  长名称: PDU ID
  描述: This value specifies a unique identifier which is used for a receive cancellation request from
      an upper layer of the SoAd.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SoAdRxUpperLayerType
  长名称: Upper Layer Type
  描述: This parameter defines the upper layer interface type (must be "IF" in case of multiple
      RxPdus).
  默认值: IF
  最小值: ''
  最大值: ''
```

### 13. SoAdInstance

**描述**: This container contains the configuration of a locigal Instance.
An instance is a set of paramaters which applies to related data paths and corresponding
configuration elements. The instance is also used to be mapped to partitions to enable multicore
support.

该容器没有参数。

### 14. SoAdEventQueueOptimization

**描述**: This container provides optimization parameter for module internal event queues.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdEventQueueLimitTpRxSoCon
  长名称: ''
  描述: This parameter limits the number of handled TP receptions on socket connections per main
      function. If more TP receptions are active they will be handled in further main
      functions. This parameter can be used to minimize main function runtime but may lead to
      performance losses for TP receptions.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: SoAdEventQueueLimitStateSoCon
  长名称: ''
  描述: This parameter limits the number of handled socket connection events per main function (e.g.
      after remote address change). If more socket connection events have to be handled they
      will be handled in further main functions. This parameter can be used to minimize main
      function runtime but may lead to performance losses on socket connections state change
      (e.g. open/close).
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: SoAdEventQueueLimitIfUdpPduRoute
  长名称: ''
  描述: This parameter limits the number of handled IF TxConfirmations on PduRoutes per main function.
      If more TxConfirmations are pending they will be handled in further main functions. This
      parameter can be used to minimize main function runtime but may lead to performance
      losses for IF PduRoutes since TxConfirmation may be called delayed.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: SoAdEventQueueLimitIfTxRouteGrp
  长名称: ''
  描述: This parameter limits the number of handled IF Routing Group transmissions per main function.
      If more transmissions are pending they will be handled in further main functions. This
      parameter can be used to minimize main function runtime but may lead to performance
      losses for IF Routing Group transmissions.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 5
  名称: SoAdEventQueueLimitTpTxSoCon
  长名称: ''
  描述: This parameter limits the number of handled TP transmissions on socket connections per main
      function. If more transmissions are active they will be handled in further main
      functions. This parameter can be used to minimize main function runtime but may lead to
      performance losses for TP transmissions.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: SoAdEventQueueLimitSoConModeChg
  长名称: ''
  描述: This parameter limits the number of handled socket connections per main function for which the
      SoConModeChg callback is pending. If more socket connections have pending SoConModeChg
      callbacks they will be handled in further main functions. This parameter can be used to
      minimize main function runtime but may lead to delayed reporting of SoConModeChg.
  默认值: 1
  最小值: 1
  最大值: 65535
```

### 15. SoAdTimeoutListOptimization

**描述**: This container provides optimization parameter for module internal timeout lists.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdTimeoutListLimitNPduUdpTx
  长名称: ''
  描述: This parameter limits the number of parallel nPdu transmissions per main function. All further
      transmission requests are rejected if list is filled. This parameter can be used to
      minimize main function runtime and RAM.
  默认值: 1
  最小值: 1
  最大值: 65535
```

### 16. SoAdIpConfig

**描述**: This container provides IP related configuration parameter.

该容器没有参数。

### 17. SoAdIpFragmentationBuffer

**描述**: This container provides parameter to configure an IP fragmentation buffer.

An IP fragmentation buffer is used when a SoAdPduRoute configures SoAdTxIfTriggerTransmit to true
and no nPduUdpTxBuffer is used on a UDP socket. In this case a buffer is required since TcpIp copies
the PDU fragmented (multiple SoAd API calls) but TriggerTransmit API allows only one call.

The IP fragmentation buffers are shared by all socket connections of an instance. A transmission
request fails when no buffer is available at the moment.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdIpFragmentationBufferSize
  长名称: ''
  描述: This parameter defines the size of the IP fragmentation buffer.
  默认值: 3000
  最小值: 1
  最大值: 65535
```

### 18. SoAdIfTriggerTransmitConfig

**描述**: This container provides trigger transmit related configuration parameter.

该容器没有参数。

### 19. SoAdIfTriggerTransmitBuffer

**描述**: This container provides parameter to configure a trigger transmit buffer.
A trigger transmit buffer is used whenever PDU data has to be stored in SoAd before transmission is
possible and SoAdTxIfTriggerTransmit is enabled. This applies for example if
SoAdTxIfTriggerTransmitForceSingleCall is enabled for a PDU fan-out or for transmissions via TCP.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdIfTriggerTransmitBufferSize
  长名称: ''
  描述: This parameter defines the size of the trigger transmit buffer.
  默认值: 1500
  最小值: 1
  最大值: 65535
```

### 20. SoAdMetaDataConfig

**描述**: This container provides meta data related configuration parameter.

该容器没有参数。

### 21. SoAdIfMetaDataBuffer

**描述**: This container provides parameter to configure a meta data buffer.
A meta data buffer is used whenever it is requested to forward the socket connection on reception.
The mechanism appends the socket connection index as meta data to a received PDU. When meta data is
used for TCP and UDP on an instance, it is recommended to configure at least 2 meta data buffers.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdIfMetaDataBufferSize
  长名称: ''
  描述: This parameter defines the size of the IF meta data buffer.
  默认值: 1500
  最小值: 1
  最大值: 65535
```

### 22. SoAdGeneral

**描述**: This container contains all global configuration parameters of SoAd.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdDevErrorDetect
  长名称: Development Error Detection
  描述: Pre-processor switch for enabling development error detection support.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdIPv6AddressEnabled
  长名称: IPv6 Address Enabled
  描述: |
    Allows for increased memory allocation to store IPv6 addresses.
    TRUE: Enables support for IPv6 addresses
    FALSE: Only IPv4 addresses are supported
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdMainFunctionPeriod
  长名称: Main Function Period
  描述: Determines the frequency at which the SoAd_MainFunction() is called in [s].
  默认值: 0.005
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: SoAdRoutingGroupMax
  长名称: Routing Group Count
  描述: Specifies the maximum number of SoAd routing groups.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: SoAdSoConMax
  长名称: Socket Connection Count
  描述: Count of configured SoAd Socket Connections.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: SoAdVersionInfoApi
  长名称: Version Info API
  描述: |
    This parameter defines if the SoAd_GetVersionInfo() API is activated.
    TRUE: Enables the SoAd_GetVersionInfo() API.
    FALSE: SoAd_GetVersionInfo() API is not included.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SoAdUserConfigFile
  长名称: User Config File
  描述: |
    If a file path will be specified, the file is read and its contents are put at the end of the
    SoAd config file.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdShutdownFinishedWaitTime
  长名称: Shutdown Finished Wait Time
  描述: This parameter defines a timeout for the shutdown mechanism which is initiated by call to
      SoAd_Shutdown(). If this timeout expires SoAd will switch to state shutdown even if
      sockets are not yet closed completely.
  默认值: 2
  最小值: 0
  最大值: 4294967295
- 
  序号: 9
  名称: SoAdHeaderFileInclusion
  长名称: ''
  描述: |
    This parameter defines a list of include header files containing callback declarations (e.g. for
    TLS callback configuration).
    These header files are included in the SoAd_Lcfg.c file.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: SoAdHeaderFileInclusionExtended
  长名称: ''
  描述: |
    This parameter defines a list of include header files containing extended information which are
    needed in static SoAd source file.
    These header files are included in the SoAd_Cfg.h file.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SoAdTxDynamicLengthEnabled
  长名称: ''
  描述: |
    This parameter defines if data length can be modified or set during transmission process.
    In case of transmission via IfRoutingGroupTransmit API no PDU length is known until call to
    TriggerTransmit callback to retrieve data from upper layer. Therefore, an internal buffer is
    used to store the PDU first before transmit function of TcpIp module can be called. If this
    feature is enabled the mentioned buffer is not needed anymore since TcpIp module can handle
    setting length on transmission.
    In case of transmission via IfTriggerTransmit API length can differ between transmission request
    and TriggerTransmit callback. If this feature is not enabled such transmissions are aborted.
    In case of nPdu and if IfTriggerTransmit is enabled on the corresponding SoAdPduRoutes
    nPduUdpTxBuffer can be optimized and is replaced by a request queue if this feature is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: SoAdMainFunctionSplitEnabled
  长名称: ''
  描述: |
    This parameter specifies whether SoAd shall split up the SoAd_MainFunction into three functions:
    
    SoAd_MainFunctionRx
    SoAd_MainFunctionState
    SoAd_MainFunctionTx
    
    This allows optimizing the data reception and data transmission path for a specific use case.
    
    Note: All three MainFunctions must be called from the same task or at least from tasks that do
    not interrupt each other.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: SoAdSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: SoAdGetAndResetMeasurementDataApi
  长名称: ''
  描述: This parameter enables/disables the function SoAd_GetAndResetMeasurementData() to get/reset
      the measurement data.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: SoAdGetAndResetMeasurementDataSomeIpSd
  长名称: ''
  描述: |
    This parameter enables/disables the SOME/IP and SD measurement data counting invalid service IDs
    and method IDs inside the PDU header. The measurement is only active if
    SoAdMeasurementDataSomeIpSdType is configured to SOME_IP or SOME_IP_SD on the
    SoAdSocketConnectionGroup for which the measurement data shall be active.
    
    This parameter can only be set to TRUE when SoAdGetAndResetMeasurementDataApi is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: SoAdRxTcpBufferSegmentsMax
  长名称: ''
  描述: This parameter defines the maximum amount of supported TCP buffer segments on reception.
  默认值: 2
  最小值: 2
  最大值: 255
- 
  序号: 17
  名称: SoAdEnableSecurityEventReporting
  长名称: ''
  描述: This parameter enables/disables the reporting of security events to the IdsM.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: SoAdRuntimeErrorReport
  长名称: ''
  描述: |
    This parameter defines the usage of runtime error reporting.
    The parameter shall be true if runtime errors shall be reported.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: SoAdBmcUsageEnabled
  长名称: Bmc Usage Enabled
  描述: |
    This parameter defines if the Basic Software Multicore Library (Bmc) is used for atomical
    operations. If the usage is disabled, SoAd uses internal measures to ensure data consistency.
    
    Note: This parameter is only relevant in multi-partition usecase.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: SoAdSoConModeChgQueueSize
  长名称: ''
  描述: |
    This value specifies the amount of mode changes that is stored per socket connection to be
    reported in the SoConModeChg callback(s).
    In case the value is configured to 0, no queueing mechanism is used.
    The required queue size depends on the amount of contexts that may interrupt each other.
    Usually, a queue size of 2 should be sufficient.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 21
  名称: SoAdResetForForceReleaseEnabled
  长名称: ''
  描述: |
    This parameter defines the behavior of SoAd_ForceReleaseRemoteAddress.
    
    TRUE: ForceReleaseRemoteAddr leads to sending a TCP RST.
    FALSE: ForceReleaseRemoteAddr leads to sending a TCP FIN.
  默认值: true
  最小值: ''
  最大值: ''
```

### 23. SoAdAdditionalLocalIpAddrAssignmentChgCallback

**描述**: This container contains an addtional callback to notify an user about a local IP address assignment
change.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdAdditionalLocalIpAddrAssignmentChg
  长名称: ''
  描述: |
    This parameter defines an additional callback to notify any module about a local IP address
    assignment change on a socket connection (LocalIpAddrAssignmentChg). There are no restrictions
    reagrding name but function parameters have to match the specification.
    This additional callback may be required if notified component is no SoAd upper layer.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 24. SoAdAdditionalSoConModeChgCallback

**描述**: This container contains an addtional callback to notify an user about a socket connection state
change.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdAdditionalSoConModeChg
  长名称: ''
  描述: |
    This parameter defines an additional callback to notify any module about a socket connection
    mode change (SoConModeChg). There are no restrictions regarding name but function parameters
    have to match the specification.
    This additional callback may be required if notified component is no SoAd upper layer.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 25. SoAdShutdownFinishedCallback

**描述**: This container contains a callback to notify an user about finished shutdown.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdShutdownFinished
  长名称: ''
  描述: This parameter defines a callback to notify any module about a successful shutdown after call
      to SoAd_Shutdown().
  默认值: ''
  最小值: ''
  最大值: ''
```

### 26. SoAdVerifyRxPduCallback

**描述**: This container contains a callback to verify if a Rx PDU is allowed to be received.

The callback forwards local socket address, remote socket address, PDU Header ID and a configured
number of PDU data to an user. If callback fails SoAd drops the received PDU completely. Otherwise
SoAd forwards the received PDU.

Via SoAdVerifyRxPduEnable the feature can be enabled on each socket connection separately.

Hint: This feature is only available for TP-PDUs with PDU header option on TCP socket connections.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdVerifyRxPdu
  长名称: ''
  描述: This parameter defines the callback name for the Rx PDU verification.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdVerifyRxPduMaxDataLength
  长名称: ''
  描述: This parameter defines the number of received PDU data which are forwarded to the user for Rx
      PDU verification.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 27. SoAdGeneration

**描述**: Contains the generation configuration parameters of the module SoAd.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdOutOfBoundsWriteProtectionStrategy
  长名称: ''
  描述: |
    This parameter is used to configure a strategy to protect the code to write out of bounds.
    
    NONE: no protection strategy is generated in the data access.
    INDEX_SATURATION: arrays are blown up and the data access index is saturated by an appropriate
    mask. The advantage is the speed of the data access, but own data elements at other indexes of
    the same variable can be overridden.
    INDEX_CHECKING: the data access index is validated by a runtime check. The advantage is that
    values are never written to incorrect indexes of the data access.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdOutOfBoundsWriteSanitizer
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
  序号: 3
  名称: SoAdOutOfBoundsReadSanitizer
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
  序号: 4
  名称: SoAdReduceConstantData2Define
  长名称: Reduce Constant Data To a Define
  描述: |
    This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM
    arrays as constant define.
    
    FALSE: ROM arrays are generated as data even if all values are identical.
    TRUE: ROM arrays are generated as constant define if all values are identical.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SoAdBoolDataInArrayOfStructStrategy
  长名称: ''
  描述: |
    This parameter is used to tailor the usage of boolean data in structures in all CONFIG-CLASSES
    ROM data. The difference between BITFIELD and BITMASKING depends on your compiler options and
    memory mapping.
    
    BOOLEAN: the datatype of boolean data is native boolean.
    BITFIELD: the bitfield type is used and the compiler extracts the boolean data from structures.
    BITMASKING: generated masks are used to extract the boolean data from structures.
  默认值: BOOLEAN
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SoAdDeduplicateIndirectedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress 0:N relational ROM data in all
    CONFIG-CLASSES without increasing the runtime.
    
    FALSE: 0:N relational ROM data is not compressed.
    TRUE: 0:N relational ROM data is compressed without increasing the runtime.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SoAdDataDeduplicationStrategy
  长名称: ''
  描述: |
    This parameter is used to taylor the the deduplication of CONFIG-CLASS PRE-COMPILE  ROM data.
    
    NONE: The generated data is not deduplicated.
    DEDUPLICATE_CONST_DATA_WITHOUT_CAST: The data is deduplicated without using casts.
    DEDUPLICATE_CONST_DATA_WITH_CAST: The data is deduplicated using casts.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdReduceBoolDataByNegationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using the negation operator.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 0
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 9
  名称: SoAdReduceBoolDataByNumericalComparisonThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using numerical comparison with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 0
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 10
  名称: SoAdReduceBoolDataByNumericalRelationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using relational comparison with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 0
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 11
  名称: SoAdReduceBoolDataByNumericalOperandStrategy
  长名称: ''
  描述: |
    This parameter is used to taylor the CONFIG-CLASS PRE-COMPILE ROM bool data with number
    deduplication mechanisms. A comparison with 0 is very efficient, but a numerical comparison with
    a value not 0 can be used to increase the ROM data compression rate.
    
    NONE: ROM data deduplications are switched off.
    DEDUPLICATE_DATA_WITH_ZERO: ROM data deduplications can be applied with the value 0.
    DEDUPLICATE_DATA_WITH_ANY_VALUE: ROM data deduplications can be applied with any numerical
    value.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: SoAdReduceNumericalDataByOffsetThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS
    PRE-COMPILE ROM data by using a constant offset.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 0
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 13
  名称: SoAdReduceNumericalDataByArraySubtractionThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS
    PRE-COMPILE ROM data by using a subtraction with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 0
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 14
  名称: SoAdShortSymbols
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
  序号: 15
  名称: SoAdInterfacesForDeactivatedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate bsw data interfaces for
    deactivated data elements. This is an advantage for the BSW developer to reduce the time to
    market with a development environment using auto completition and to investigate potential
    interfaces.
    
    FALSE: data interfaces are not generated if the data elementis deactivated.
    TRUE: data interfaces are generated as e.g. empty macros.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: SoAdReferringKeysInComments
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

### 28. SoAdSocketApi

**描述**: This container contains configuration parameters describing socket API dependent parameter.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketApiPrefix
  长名称: ''
  描述: |
    This parameter defines the function name prefix for the socket API.
    
    Examples:
    With a prefix set to "TcpIp", SoAd calls the function "TcpIp_Bind" to bind a socket to a local
    IP address and port.
    With a prefix set to "vBsdAd", SoAd calls the function "vBsdAd_Close" to close a socket.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdVBsdAdUsed
  长名称: Use vBsdAd
  描述: |
    This parameter defines if vBsdAd component is used as lower layer.
    
    Note: When vBsdAd component is used instead of MICROSAR TcpIp the following features are not
    supported:
    - Enabling/disabling of UDP checksum (SoAdSocketUdpChecksumEnabled)
    - DHCP event callbacks (SoAdDhcpEvent)
    - TLS (SoAdSocketTcpTlsConnectionRef)
    - Immediate UDP IF Tx Confirmation (SoAdSocketUdpImmediateIfTxConfirmation)
    - UDP address resolution retry (SoAdSocketUdpAddressResolutionRetryEnabled)
    
  默认值: false
  最小值: ''
  最大值: ''
```

### 29. SoAdDhcpEventCallback

**描述**: This container contains a callback to notify user of a DHCP event.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdDhcpEvent
  长名称: ''
  描述: This parameter defines a callback to notify any module of a DHCP event.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 30. SoAdSecurityEventRefs

**描述**: Container for the references to IdsMEvent elements representing the security events that the SoAd
module shall report to the IdsM in case the corresponding security related event occurs (and if
SoAdEnableSecurityEventReporting is set to "true").

该容器没有参数。

