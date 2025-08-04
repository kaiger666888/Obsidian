# SoAd

## 模块描述

Configuration of the SoAd (Socket Adaptor) module.

## 容器列表

### 1. SoAdBswModules

**描述**: Each container describes a specific BSW module that the SoAd shall interface to.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdIf
  长名称: ''
  描述: Specifies if the BSW module supports the Communication Interface APIs or not. Value true means
      that the APIs are supported. A module can have both Communication Interface APIs and
      Transport Protocol APIs (e.g. the PduR module).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdIfTriggerTransmit
  长名称: ''
  描述: Specifies if the BSW module supports the TriggerTransmit API or not. Value true means that the
      API is supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdIfTxConfirmation
  长名称: ''
  描述: Specifies if the BSW module supports the TxConfirmation API or not. Value true means that the
      API is supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SoAdLocalIpAddrAssigmentChg
  长名称: ''
  描述: Specifies if the BSW module supports the LocalIpAddrAssigmentChg API or not. Value true means
      that the API is supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SoAdSoConModeChg
  长名称: ''
  描述: Specifies if the BSW module supports the SoConModeChg API or not. Value true means that the
      API is supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SoAdTp
  长名称: ''
  描述: Specifies if the BSW module supports the TransportProtocol APIs or not. Value true means that
      the APIs are supported. A module can have both Communication Interface APIs and
      Transport Protocol APIs (e.g. the PduR module).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SoAdUseCallerInfix
  长名称: ''
  描述: Specifies if SoAd shall use (TRUE) the infix "SoAd" when calling an upper layer module
      function or not (FALSE). E.g. if SoAdUseCallerInfix is TRUE for the upper layer "ABC"
      then SoAd will call ABC_SoAdIfRxIndication() otherwise SoAd would call
      ABC_IfRxIndication().
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdUseTypeInfix
  长名称: ''
  描述: Specifies if SoAd shall use (TRUE) the API type infix "Tp" or "If" when calling an upper layer
      module function or not (FALSE). E.g. if SoAdUseTypeInfix is TRUE for the upper layer
      "ABC" then SoAd will call ABC_IfRxIndication(), otherwise SoAd would call
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
  描述: Tx PDU ID of the PDU coming from the PDU Router.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SoAdTxUpperLayerType
  长名称: Upper Layer Type
  描述: Specifies the upper layer interface type (must be "IF" in case of multiple PduRoutes).
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
  长名称: ''
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
```

### 4. SoAdPduRouteDest

**描述**: Specifies the PDU route destination.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdTxPduHeaderId
  长名称: PDU Header ID
  描述: ID to be sent on the TCP/IP connection if the PDU header option is enabled.
  默认值: 0
  最小值: 0
  最大值: 4294967296
- 
  序号: 2
  名称: SoAdTxUdpTriggerMode
  长名称: UDP Trigger Mode
  描述: |
    Specifies whether a PDU triggers the transmission of the nPduUdpTxBuffer. NPduUdpTxBuffer can
    only be used for upper layers with "IF" API, i.e. this parameter shall only be set if all upper
    layers belonging to the related socket connection have SoAdTxUpperLayerType set to "IF".
    This parameter is only relevant for UDP connections.
    
    TRIGGER_ALWAYS: PDU transmission triggers transmission of nPduUdpTxBuffer
    TRIGGER_NEVER: PDU transmission is stored in nPduUdpTxBuffer and triggers nPduUdpTxBuffer
    transmission only if buffer size is not sufficient
  默认值: TRIGGER_NEVER
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdTxUdpTriggerTimeout
  长名称: UDP Trigger Timeout
  描述: Specifies the timeout in [s] the nPduUdpTxBuffer shall be transmitted at the latest after this
      PDU is put into the buffer. This optional parameter is only relevant if
      SoAdTxUdpTriggerMode is TRIGGER_NEVER.
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
  描述: Unique ID of Routing Group
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SoAdRoutingGroupIsEnabledAtInit
  长名称: Enable at Initialization
  描述: If set to true this routing group will be enabled after initializing the SoAd module (i.e.
      enabled in the SoAd_Init function).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdRoutingGroupTxTriggerable
  长名称: Enable Tx Triggerable
  描述: Specifies if the If-TxPDUs related to the PduRouteDest containers
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
  描述: Enables the transmission of the PDU header (ID, length) on this socket connection.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdResourceManagementEnable
  长名称: Enable Resource Management
  描述: Enables the resource management option for this socket.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdSocketAutomaticSoConSetup
  长名称: Enable Automatic Socket Connection Setup
  描述: Specifies if the setup of the socket connection shall be done automatically (TRUE) or manually
      (FALSE) via SoAd_OpenSoCon() and SoAd_CloseSoCon().
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SoAdSocketFramePriority
  长名称: Ethernet Frame Priority
  描述: Specifies the priority of the Ethernet frame.
  默认值: 7
  最小值: 0
  最大值: 7
- 
  序号: 5
  名称: SoAdSocketIpAddrAssignmentChgNotification
  长名称: Enable IP Address Assignment Change Notification
  描述: Specifies if the local IP address assignment change notification callback function of the
      upper layer shall be called if the assignment of the local IP address used by this
      socket connection changes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SoAdSocketLocalPort
  长名称: Local Port
  描述: Local UDP or TCP port used for this connection.If this parameter set to 0 SoAd requests TcpIp
      to select an ephemeral port.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: SoAdSocketMsgAcceptanceFilterEnabled
  长名称: Enable Message Acceptance Filter
  描述: Specifies if the message acceptance filter is enabled (TRUE) or not (FALSE).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdSocketSoConModeChgNotification
  长名称: Enable Socket Connection Mode Change Notification
  描述: Specifies if the SoCon mode change notification callback function of the upper layer shall be
      called in case of SoCon mode change.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SoAdSocketTpRxBufferMin
  长名称: Minimum TP Rx Buffer
  描述: Specifies the amout of data in bytes (PDU data for the upper layer and PDU Header if used) the
      SoAd shall at least be able to buffer for data reception via each socket connection of
      the socket connection group and using an upper layer with TP.
  默认值: 512
  最小值: 0
  最大值: 65535
- 
  序号: 10
  名称: SoAdBestMatchWithSockRouteEnabled
  长名称: Enable Best Match Algorithm with SocketRoute validation
  描述: |
    If this feature is enabled the best match algorithm for this socket connection group considers
    that a socket route is configured for a socket connection.
    This means: The best match algortihm will not choose a socket connection which has no receiver
    even if the remote address matches.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SoAdBestMatchWithPduHeaderEnabled
  长名称: Enable Best Match Algorithm with PDU Header validation
  描述: |
    If this feature is enabled the best match algorithm of this socket connection group considers
    the received PDU Header when choosing a socket connection. A received PDU is discarded if no
    socket route could be found containing the corresponding PDU Header ID.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
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
```

### 7. SoAdSocketConnection

**描述**: Specifies the socket connection (Id and remote address information).

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketId
  长名称: Socket Connection ID
  描述: The Socket ID is used as a reference to a particular connection when transferring data to and
      from the PDU Router.
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
If remote address contains wildcards socket connection cannot be openned (set to online). The remote
address has to be overwritten at runtime via API call, on UDP frame reception or via TCP connection
establishment.

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
    This parameter defines the UDP or TCP port of remote node.
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

### 9. SoAdTcpTlsConfig

**描述**: This container contains the TLS configuration for a socket connection. TLS is supported on TCP
client sockets only (SoAdSocketTcp/TcpInitiate = TRUE).
If this container does not exist TLS is disabled on this socket connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdTcpTlsTxBufferSize
  长名称: ''
  描述: This parameter defines the transmission buffer size for Tls. The value of this parameter is
      forwarded to TcpIp and Tls on socket creation at runtime.
  默认值: 512
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: SoAdTcpTlsRxBufferSize
  长名称: ''
  描述: This parameter defines the reception buffer size for Tls. The value of this parameter is
      forwarded to TcpIp and Tls on socket creation at runtime.
  默认值: 512
  最小值: 1
  最大值: 4294967295
```

### 10. SoAdSocketTcp

**描述**: Specifies that TCP is used as transport protocol for the socket connection group and parameters only
related to TCP socket connections.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketTcpImmediateTpTxConfirmation
  长名称: Enable Immediate Tx Confirmation
  描述: If set to FALSE, SoAd notifies the TP upper layer via transmit confirmation after a Tcp Ack
      has been received. If set to TRUE, SoAd notifies the TP upper layer via transmit
      confirmation immediately after transmit has been accepted by TcpIp.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdSocketTcpInitiate
  长名称: Initiate TCP Connection
  描述: Specifies the initiator for this TCP connection. It will not be defined for UDP sockets.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdSocketTcpKeepAlive
  长名称: Enable Keep Alive
  描述: |
    Specifies to use the keep-alive mechanism for this connection. It will not be
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
  描述: Specifies the interval in seconds between subsequent keepalive probes.
  默认值: 1
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: SoAdSocketTcpKeepAliveProbesMax
  长名称: Maximum Keep Alive Probes
  描述: |
    Maximum number of times that TCP retransmits an individual data
    segment before aborting the connection.
  默认值: 1
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: SoAdSocketTcpKeepAliveTime
  长名称: Keep Alive Time
  描述: |
    Specifies the time in seconds between the last data packet sent and the
    first keepalive probe.
  默认值: 7200
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: SoAdSocketTcpNoDelay
  长名称: Disable TCP Congestion Control
  描述: Specifies not to use the congestion control mechanism for this connection. It will not be
      defined for UDP sockets.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdSocketTcpTxQuota
  长名称: Transmission Quota
  描述: |
    Specifies the maximum amout of bytes (PDU data provided by the upper layer and PDU Header if
    used) the SoAd may queue for transmission via TCP at the TcpIp module for each socket connection
    of this socket connection group.
    
    (not used)
  默认值: 4294967295
  最小值: 0
  最大值: 4294967295
- 
  序号: 9
  名称: SoAdSocketTcpTxBufferMin
  长名称: Minimum Tx Buffer
  描述: This parameter defines a minimum transmission buffer size the TcpIp must be able to provide on
      each socket connection of this group. The value is forwarded to TcpIp on socket creation
      at runtime. If this optional parameter is not configured TcpIp will use a default value.
  默认值: 512
  最小值: 1
  最大值: 65535
```

### 11. SoAdSocketUdp

**描述**: Specifies that UDP is used as transport protocol for the socket connection group and parameters only
related to UDP socket connections.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketUdpAliveSupervisionTimeout
  长名称: Alive Supervision Timeout
  描述: Specifies the time in [s] a UDP socket connection remains in the mode SOAD_SOCON_ONLINE after
      the latest reception of a frame from the remote peer specified by the remote address. If
      this optional parameter is not enabled UDP Alive Supervision is deactivated for the
      related socket connection group.
  默认值: 1
  最小值: 0
  最大值: 320
- 
  序号: 2
  名称: SoAdSocketUdpListenOnly
  长名称: Enable Listen Only
  描述: Specifies if the socket connection group is only used for reception (TRUE) or used for both
      reception and transmission (FALSE).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdSocketUdpStrictHeaderLenCheckEnabled
  长名称: ''
  描述: Specifies if UDP messages shall be dropped (TRUE) if the length of all contained PDUs does not
      match the length of the whole message or not (FALSE). Shall only be set to TRUE if
      SoAdPduHeaderEnable is also set to TRUE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SoAdSocketUdpTriggerTimeout
  长名称: Timeout for Trigger Transmission
  描述: Specifies the timeout in [s] a nPduUdpTxBuffer is waiting for a PDU with TriggerMode =
      TRIGGER_ALWAYS, i.e. when the timeout expires the nPduUdpTxBuffer is transmitted. Timer
      is reset after each UDP transmission. This optional parameter is only relevant if a
      nPduUdpTxBuffer is used.
  默认值: 2
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: SoAdSocketnPduUdpTxBufferMin
  长名称: Socket n Pdu Udp Tx Buffer Min
  描述: |
    Specifies the amout of data in bytes (PDU data provided by the upper layer and PDU Header if
    used) the SoAd shall be able to buffer for data transmission via this socket connection in case
    the UDP message shall be buffered for transmission of multiple PDUs per UDP (nPduUdpTxBuffer).
    
    This parameter must not exist if no nPduUdpTxBuffer is used.
  默认值: 32
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: SoAdSocketUdpAddressResolutionRetryEnabled
  长名称: Enable Address Resolution Retry
  描述: |
    Specifies if a transmission request shall be stored in TcpIp module to retry transmission in
    case of missing address resolution (ARP/NDP).
    True: Retry enabled
    False: Retry disabled
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
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
  序号: 8
  名称: SoAdSocketUdpImmediateIfTxConfirmationListSize
  长名称: ''
  描述: |
    This parameter specifies the size of a list which is used in the TcpIp module to handle UDP
    transmissions with TxConfirmation.
    Please refer to TcpIp parameter "TcpIpUdpTxReqListSize" for more details.
    
    This parameter is used if "SoAdSocketUdpImmediateIfTxConfirmation" is enabled.
    
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 9
  名称: SoAdSocketnPduUdpTxQueueSize
  长名称: Socket n Pdu Udp Tx Queue Size
  描述: |
    This parameter defines the size of a management queue for each socket connection. This queue is
    used to manage PDUs in the nPduUdpTxBuffer and PDU transmission requests for trigger transmit.
    Both transmission types are stored within one queue, so make sure that size is sufficient for
    all related SoAdPduRoutes.
    
    This parameter must not exist if no related SoAdPduRoute exisits with enabled
    SoAdTxIfTriggerTransmit.
  默认值: 2
  最小值: 1
  最大值: 255
- 
  序号: 10
  名称: SoAdSocketUdpAddressResolutionRetryQueueLimit
  长名称: ''
  描述: |
    This parameter sets the limitation of maximum used UDP transmission retry queue elements for
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
  序号: 11
  名称: SoAdSocketUdpBroadcastReceptionEnabled
  长名称: ''
  描述: |
    This parameter defines if the reception of broadcasts (IPv4 limited and directed broadcast) and
    multicasts (IPv6 all nodes and all routers multicast) is enabled.
    The parameter must exist if SoAdSocketApiType is LINUX or QNX and if SoAdSocketLocalAddressRef
    references a unicast address.
    Otherwise, this parameter must not exist.
    True: Broadcasts and multicasts shall be received.
    False: Broadcasts and multicasts shall not be received.
  默认值: true
  最小值: ''
  最大值: ''
```

### 12. SoAdSocketRoute

**描述**: Describes the path of a PDU from a socket in the TCP/IP stack to an upper layer of the SoAd after
reception in the TCP/IP Stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdRxPduHeaderId
  长名称: PDU Header ID
  描述: ID contained in the packet received on the TCP/IP connection if the PDU header option is
      enabled.
  默认值: 0
  最小值: 0
  最大值: 4294967296
```

### 13. SoAdSocketRouteDest

**描述**: Describes the upper layer destination PDU for a message received on a TcpIp socket.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdRxPduId
  长名称: PDU ID
  描述: This unique identifier is used for a receive cancellation request from an upper layer of the
      SoAd.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SoAdRxUpperLayerType
  长名称: Upper Layer Type
  描述: Specifies the upper layer interface type (must be "IF" in case of multiple RxPdus).
  默认值: IF
  最小值: ''
  最大值: ''
```

### 14. SoAdIpConfig

**描述**: This container provides IP related configuration parameter.

该容器没有参数。

### 15. SoAdIpFragmentationBuffer

**描述**: This container provides parameter to configure an IP fragmentation buffer.

An IP fragmentation buffer is used when a SoAdPduRoute configures SoAdTxIfTriggerTransmit to true
and no nPduUdpTxBuffer is used on a UDP socket. In this case a buffer is required since TcpIp copies
the PDU fragmented (multiple SoAd API calls) but TriggerTransmit API allows only one call.

The IP fragmentation buffers are shared by all socket connections. A transmission request fails when
no buffer is available at the moment.

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

### 16. SoAdIfTriggerTransmitConfig

**描述**: This container provides trigger transmit related configuration parameter.

该容器没有参数。

### 17. SoAdIfTriggerTransmitBuffer

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

### 18. SoAdGeneral

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
  描述: Allows for increased memory allocation to store IPv6 addresses.
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
  描述: Specifies the maximum number of SoAd routing groups. Furthermore it defines the platform type
      used for RoutingGroupIdType. If SoAdRoutingGroupMax is not greater than 256, an uint8 is
      used,
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
  描述: Activates the SoAd_GetVersionInfo() API.
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
  描述: This parameter defines a timout for the shutdown mechanism which is initiated by call to
      SoAd_Shutdown(). If this timeout expires SoAd will switch to state shutdown even if
      sockets are not yet closed completely.
  默认值: 2
  最小值: 0
  最大值: 65535
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
    needed in static SoAd source file (e.g. linux/if_oacket.h).
    These header files are included in the SoAd_Cfg.h file.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SoAdTcpTlsEnabled
  长名称: ''
  描述: This parameter defines if TLS communication shall be enabled for SoAd.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: SoAdTxDynamicLengthEnabled
  长名称: ''
  描述: |
    This parameter defines if data length can be modified or set during transmission process.
    In case of transmission via IfRoutingGroupTrannsmit API no PDU length is known until call to
    TriggerTransmit callback to retrieve data from upper layer. Therefore an internal buffer is used
    to store the PDU first before transmit function of TcpIp module can be called. If this feature
    is enabled the mentioned buffer is not needed anymore since TcpIp module can handle setting
    length on transmission.
    In case of transmission via IfTriggerTransmit API length can differ between transmission request
    and TriggerTransmit callback. If this feature is not enabled such transmissions are aborted.
    In case of nPdu and if IfTriggerTransmit is enabled on the corresponding SoAdPduRoutes
    nPduUdpTxBuffer can be optimized and is replaced by a request queue if this feature is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
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
  序号: 14
  名称: SoAdSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: SoAdMetaDataRxBufferSize
  长名称: ''
  描述: This parameter defines the size of a buffer used to forward PDUs using meta data. The size of
      this buffer has to be 2 bytes larger than the maximum length of all PDUs using meta
      data. Ths last 2 bytes are used to store the meta data.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 16
  名称: SoAdGetAndResetMeasurementDataApi
  长名称: ''
  描述: This parameter enables/disables the function SoAd_GetAndResetMeasurementData() to get/reset
      the measurement data.
  默认值: false
  最小值: ''
  最大值: ''
```

### 19. SoAdTcpTlsCallback

**描述**: This container contains a callback which is called if a Tls socket was created.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdTcpTlsSocketCreatedNotification
  长名称: ''
  描述: This parameter defines a callback which is called if a TLS socket was created. The callback
      can be used to set additional parameters for TLS communication (e.g. set client
      certificate).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 20. SoAdAdditionalLocalIpAddrAssignmentChgCallback

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

### 21. SoAdAdditionalSoConModeChgCallback

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
    mode change (SoConModeChg). There are no restrictions reagrding name but function parameters
    have to match the specification.
    This additional callback may be required if notified component is no SoAd upper layer.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 22. SoAdShutdownFinishedCallback

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

### 23. SoAdEventQueueOptimization

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
  名称: SoAdEventQueueLimitTcpTxSoCon
  长名称: ''
  描述: This parameter limits the number of handled TCP transmissions in case of BSD on socket
      connections per main function. If more transmissions are active they will be handled in
      further main functions. This parameter can be used to minimize main function runtime but
      may lead to performance losses for TCP transmissions in case of BSD.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 4
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
  序号: 5
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
  序号: 6
  名称: SoAdEventQueueLimitSocketIdx
  长名称: ''
  描述: This parameter limits the number of handled events on sockets (e.g. TCP socket state changes,
      reception of data) per main function in case of BSD. If more events are pending they
      will be handled in further main functions. This parameter can be used to minimize main
      function runtime but may lead to performance losses for socket handling.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 7
  名称: SoAdEventQueueLimitLocalAddr
  长名称: ''
  描述: This parameter limits the number of handled events on local addresses (e.g. IP address
      assignment) per main function in case of BSD. If more events are pending they will be
      handled in further main functions. This parameter can be used to minimize main function
      runtime but may lead to performance losses for local address handling (e.g. slow IP
      address assignment).
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 8
  名称: SoAdEventQueueLimitTpTxSoCon
  长名称: ''
  描述: This parameter limits the number of handled TP transmissions on socket connections per main
      function. If more transmissions are active they will be handled in further main
      functions. This parameter can be used to minimize main function runtime but may lead to
      performance losses for TP transmissions.
  默认值: 1
  最小值: 1
  最大值: 65535
```

### 24. SoAdTimeoutListOptimization

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

### 25. SoAdVerifyRxPduCallback

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

### 26. SoAdGeneration

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
  名称: SoAdReduceDataByStreaming
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to pack generated CONFIG-CLASS PRE-COMPILE
    ROM data into a data type dependent stream.
    
    FALSE: generated const data is not packed into a data type dependent stream.
    TRUE: generated const data is packed into a data type dependent stream.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
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
  序号: 16
  名称: SoAdInterfacesForDeactivatedData
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
  序号: 17
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

### 27. SoAdSocketApi

**描述**: This container contains configuration parameters describing socket API dependent parameter.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketApiType
  长名称: ''
  描述: |
    This parameter defines the socket API.
    AUTOSAR: AUTOSAR compatible API.
    LINUX: Linux compatible API (used in Linux operating system).
    QNX: QNX compatible API (used in QNX operating system).
    INTEGRITY: INTEGRITY compatible API (used in INTEGRITY operating system).
  默认值: AUTOSAR
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdSocketTxBufferSize
  长名称: ''
  描述: |
    This parameter defines the size of a global buffer which is used to store data to be
    transmitted. This buffer is used for UDP and TCP transmissions. It is recommended to set this
    value to the maximum transmission unit on SoAd level (MTU without IP and UDP/TCP header).
    
    This parameter is only relevant if a socket API is used which is based on polling (e.g. Linux).
  默认值: 1452
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: SoAdSocketTxBufferNum
  长名称: ''
  描述: |
    This parameter defines the number of global buffer which are used to store data to be
    transmitted. In case transmission to socket API fails for TCP, SoAd performs a retry for the
    buffer until the data could be sent or the socket is closed.
    
    This parameter is only relevant if a socket API is used which is based on polling (e.g. Linux).
  默认值: 1
  最小值: 1
  最大值: 254
- 
  序号: 4
  名称: SoAdSocketTxBufferMaxNumPerSocket
  长名称: ''
  描述: |
    This parameter defines the maximum number of socket transmission buffer which can be assigned to
    a single socket at the same time. The transmission request fails for all subsequent transmission
    requests.
    
    This parameter is only relevant if a socket API is used which is based on polling (e.g. Linux).
  默认值: 1
  最小值: 1
  最大值: 254
- 
  序号: 5
  名称: SoAdSocketRxBufferSize
  长名称: ''
  描述: |
    This parameter defines the size of a global buffer which is used to store received data.This
    buffer is used for UDP only. It is recommended to set this value to the maximum reception unit
    on SoAd level (MTU without IP and UDP/TCP header).
    
    This parameter is only relevant if a socket API is used which is based on polling (e.g. Linux).
  默认值: 1452
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: SoAdSocketLingerTimeoutEnabled
  长名称: ''
  描述: |
    Indicates whether the SoAd sets linger time to 0 (SO_LINGER) via setsockopt(). This option can
    be used to close TCP connections immediately.
    true: option is set on socket creation
    false: option is not set on socket creation
    
    This parameter is only relevant if a socket API is used which is related to the BSD API (e.g.
    Linux).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SoAdSocketReportErrorFunction
  长名称: ''
  描述: |
    This parameter defines a callback which is called in case any call to socket API returns an
    unexpected error.
    
    This parameter is only relevant if a socket API is used which is related to the BSD API (e.g.
    Linux).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdLocalIpAddrCheckInterval
  长名称: ''
  描述: |
    This parameter defines the interval used to check if a local IP address is available.
    This interval can be used to optimze calls to the socket API to prevent timing issues.
    If parameter is 0 the check is perfomed in each main function cycle.
  默认值: 0.1
  最小值: 0
  最大值: 65535
```

### 28. SoAdDhcpEventCallback

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

