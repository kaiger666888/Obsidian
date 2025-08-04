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
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdIfTriggerTransmit
  长名称: ''
  描述: Specifies if the BSW module supports the TriggerTransmit API or not. Value true means that the
      API is supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdIfTxConfirmation
  长名称: ''
  描述: Specifies if the BSW module supports the TxConfirmation API or not. Value true means that the
      API is supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SoAdLocalIpAddrAssigmentChg
  长名称: ''
  描述: Specifies if the BSW module supports the LocalIpAddrAssigmentChg API or not. Value true means
      that the API is supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SoAdSoConModeChg
  长名称: ''
  描述: Specifies if the BSW module supports the SoConModeChg API or not. Value true means that the
      API is supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SoAdTp
  长名称: ''
  描述: Specifies if the BSW module supports the TransportProtocol APIs or not. Value true means that
      the APIs are supported. A module can have both Communication Interface APIs and
      Transport Protocol APIs (e.g. the PduR module).
  默认值: ''
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
```

### 2. SoAdConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR SoAd module.
This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist
once per configuration set.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdConfigurationId
  长名称: ''
  描述: Identification of the SoAd configuration.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 3. SoAdPduRoute

**描述**: Describes the path of a PDU from an upper layer of the SoAd to the socket in the TCP/IP stack for
transmission.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdTxPduId
  长名称: ''
  描述: Tx PDU ID of the PDU coming from the PDU Router.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SoAdTxUpperLayerType
  长名称: ''
  描述: Specifies the upper layer interface type (must be "IF" in case of multiple PduRoutes).
  默认值: ''
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
  长名称: ''
  描述: ID to be sent on the TCP/IP connection if the PDU header option is enabled.
  默认值: ''
  最小值: 0
  最大值: 4294967296
- 
  序号: 2
  名称: SoAdTxUdpTriggerMode
  长名称: ''
  描述: Specifies whether a PDU triggers the transmission of the nPduUdpTxBuffer.
  默认值: ''
  最小值: ''
  最大值: ''
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
  长名称: ''
  描述: Unique ID of Routing Group
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SoAdRoutingGroupIsEnabledAtInit
  长名称: ''
  描述: If set to true this routing group will be enabled after initializing the SoAd module (i.e.
      enabled in the SoAd_Init function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdRoutingGroupTxTriggerable
  长名称: ''
  描述: Specifies if the If-TxPDUs related to the PduRouteDest containers
  默认值: ''
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
  长名称: ''
  描述: Enables the transmission of the PDU header (ID, length) on this socket connection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdResourceManagementEnable
  长名称: ''
  描述: Enables the resource management option for this socket.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdSocketAutomaticSoConSetup
  长名称: ''
  描述: Specifies if the setup of the socket connection shall be done automatically (TRUE) or manually
      (FALSE) via SoAd_OpenSoCon() and SoAd_CloseSoCon().
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SoAdSocketFramePriority
  长名称: ''
  描述: Specifies the priority of the Ethernet frame.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 5
  名称: SoAdSocketIpAddrAssignmentChgNotification
  长名称: ''
  描述: Specifies if the local IP address assignment change notification callback function of the
      upper layer shall be called if the assignment of the local IP address used by this
      socket connection changes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SoAdSocketLocalPort
  长名称: ''
  描述: Local UDP or TCP port used for this connection.If this parameter set to 0 SoAd requests TcpIp
      to select an ephemeral port.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: SoAdSocketMsgAcceptanceFilterEnabled
  长名称: ''
  描述: Specifies if the message acceptance filter is enabled (TRUE) or not (FALSE).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SoAdSocketSoConModeChgNotification
  长名称: ''
  描述: Specifies if the SoCon mode change notification callback function of the upper layer shall be
      called in case of SoCon mode change.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SoAdSocketTpRxBufferMin
  长名称: ''
  描述: Specifies the amout of data in bytes (PDU data for the upper layer and PDU Header if used) the
      SoAd shall at least be able to buffer for data reception via each socket connection of
      the socket connection group and using an upper layer with TP.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 7. SoAdSocketConnection

**描述**: Specifies the socket connection (Id and remote address information).

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketId
  长名称: ''
  描述: Socket connection identifier used as SoConId in the interaction with upper layers.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 8. SoAdSocketRemoteAddress

**描述**: Subcontainer of SoAdSocketConnection to specify the remote address (IP address and port) for a
socket connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketRemoteIpAddress
  长名称: ''
  描述: IP address of remote node.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdSocketRemotePort
  长名称: ''
  描述: Remote UDP or TCP port used for this connection.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 9. SoAdSocketTcp

**描述**: Specifies that TCP is used as transport protocol for the socket connection group and parameters only
related to TCP socket connections.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketTcpImmediateTpTxConfirmation
  长名称: ''
  描述: If set to FALSE, SoAd notifies the TP upper layer via transmit confirmation after a Tcp Ack
      has been received. If set to TRUE, SoAd notifies the TP upper layer via transmit
      confirmation immediately after transmit has been accepted by TcpIp.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdSocketTcpInitiate
  长名称: ''
  描述: Specifies the initiator for this TCP connection. It will not be defined for UDP sockets.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdSocketTcpNoDelay
  长名称: ''
  描述: Specifies not to use the congestion control mechanism for this connection. It will not be
      defined for UDP sockets.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SoAdSocketTcpTxQuota
  长名称: ''
  描述: Specifies the maximum amout of bytes (PDU data provided by the upper layer and PDU Header if
      used) the SoAd may queue for transmission via TCP at the TcpIp module for each socket
      connection of this socket connection group.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 10. SoAdSocketUdp

**描述**: Specifies that UDP is used as transport protocol for the socket connection group and parameters only
related to UDP socket connections.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdSocketUdpListenOnly
  长名称: ''
  描述: Specifies if the socket connection group is only used for reception (TRUE) or used for both
      reception and transmission (FALSE).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdSocketUdpRetryEnabled
  长名称: ''
  描述: Specifies if an UdpTxBuffer shall be used (TRUE) to retry an UDP transmission in case of
      TCPIP_E_ARP_CACHE_MISS or not (FALSE).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdSocketUdpTriggerTimeout
  长名称: ''
  描述: Specifies the timeout in [s] a nPduUdpTxBuffer is waiting for a PDU with TriggerMode =
      TRIGGER_ALWAYS, i.e. when the timeout expires the nPduUdpTxBuffer is transmitted. Timer
      is reset after each UDP transmission. This optional parameter is only relevant if a
      nPduUdpTxBuffer is used.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 4
  名称: SoAdSocketnPduUdpTxBufferMin
  长名称: ''
  描述: Specifies the amout of data in bytes (PDU data provided by the upper layer and PDU Header if
      used) the SoAd shall be able to buffer for data transmission via this socket connection
      in case the UDP message shall be buffered for transmission of multiple PDUs per UDP.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 11. SoAdSocketRoute

**描述**: Describes the path of a PDU from a socket in the TCP/IP stack to an upper layer of the SoAd after
reception in the TCP/IP Stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdRxPduHeaderId
  长名称: ''
  描述: ID contained in the packet received on the TCP/IP connection if the PDU header option is
      enabled.
  默认值: ''
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
  长名称: ''
  描述: This unique identifier is used for a receive cancellation request from an upper layer of the
      SoAd.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SoAdRxUpperLayerType
  长名称: ''
  描述: Specifies the upper layer interface type (must be "IF" in case of multiple RxPdus).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 13. SoAdGeneral

**描述**: This container contains all global configuration parameters of SoAd.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SoAdDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling development error detection support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SoAdIPv6AddressEnabled
  长名称: ''
  描述: Allows for increased memory allocation to store IPv6 addresses.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SoAdMainFunctionPeriod
  长名称: ''
  描述: Determines the frequency at which the SoAd_MainFunction() is called in [s].
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 4
  名称: SoAdRoutingGroupMax
  长名称: ''
  描述: Specifies the maximum number of SoAd routing groups. Furthermore it defines the platform type
      used for RoutingGroupIdType. If SoAdRoutingGroupMax is not greater than 256, an uint8 is
      used,
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: SoAdSoConMax
  长名称: ''
  描述: Specifies the maximum number of SoAd socket connections.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: SoAdVersionInfoApi
  长名称: ''
  描述: Activates the SoAd_GetVersionInfo() API.
  默认值: ''
  最小值: ''
  最大值: ''
```

