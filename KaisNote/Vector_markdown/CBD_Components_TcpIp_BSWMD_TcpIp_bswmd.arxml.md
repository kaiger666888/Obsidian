# TcpIp

## 模块描述

The Transmission Control Protocol/Internet Protocol (TCP/IP) module provides access to socket based
communication interfaces which can be used to communicate via UDP (User Datagram Protocol) and TCP
(Transmission Control Protocol) in IPv4/IPv6 networks.
#Ethernet  #SmartCharging #SomeIpSd #Diag
#AUTOSAR

## 容器列表

### 1. TcpIpConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR TcpIp module.

该容器没有参数。

### 2. TcpIpCtrl

**描述**: Specifies the EthIf controller used for IP communication and TcpIp errors that shall be reported to
DEM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIpFramePrioDefault
  长名称: IP Frame Prio Default
  描述: Specifies the default value for the frame priority used by all sockets.
  默认值: 0
  最小值: 0
  最大值: 7
```

### 3. TcpIpCtrlDemEventParameterRefs

**描述**: This container is a subcontainer of TcpIpCtrl and specifies the references to DemEventParameter
elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding
TcpIp error occurs for communication on the EthIf Controller. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 4. TcpIpIpV4Ctrl

**描述**: Specifies an Internet Protocol version 4 (IPv4) instance.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIpTypeOfServiceDefault
  长名称: IP Type Of Service Default
  描述: This value specifies the default for the "Type of Service" field of the IPv4 header in
      outgoing packets on this IP controller.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: TcpIpIpCtrlIdx
  长名称: IPv4 Controller Index
  描述: IPv4 controller index (calculated automatically)
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: TcpIpIpDefaultTtl
  长名称: Default Time To Live
  描述: |
    This value specifies the default for the "Time to Live" field of the IPv4 header in outgoing
    packets on this IP controller.
    
    "The current recommended default time to live (TTL) for the Internet
    Protocol (IP) is 64 [RFC791], [RFC1122]."
    (see http://www.iana.org/assignments/ip-parameters/ip-parameters.xhtml#ip-parameters-2)
  默认值: 64
  最小值: 0
  最大值: 255
```

### 5. TcpIpIpV6Ctrl

**描述**: Specifies an Internet Protocol version 6 (IPv6) instance.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIpV6DefaultHopLimit
  长名称: Default Hop Limit
  描述: This value specifies the default Hop Limit for outgoing IPv6 packets. If "Allow Hop Limit
      Reconfiguration" is checked, the value may be reconfigured based on received Router
      Advertisements according to [RFC4861 6.3.4. Processing Received Router Advertisements].
  默认值: 64
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: TcpIpIpV6DefaultTrafficClass
  长名称: Default Traffic Class
  描述: |
    This value specifies the default 'Traffic Class' set in the IPv6 header of outgoing packets of
    this controller.
    This value may be changed to a socket specific value during runtime.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: TcpIpIpV6DefaultFlowLabel
  长名称: Default Flow Label
  描述: |
    This value specifies the default 'FlowLabel' set in the IPv6 header of outgoing packets of this
    controller.
    This value may be changed to a socket specific value during runtime.
  默认值: 0
  最小值: 0
  最大值: 1048575
- 
  序号: 4
  名称: TcpIpIpV6CtrlIdx
  长名称: Controller Index
  描述: IPv6 controller index (calculated automatically)
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: TcpIpDiscardUnknownExtHdr
  长名称: Discard packets with unknown ext. header
  描述: |
    This parameter specified the behaviour for received packets with IPv6 extension header(s) that
    can not be processed.
    FALSE: The extension header will be skipped and the packet processed.
    TRUE: The packet will be discarded.
  默认值: false
  最小值: ''
  最大值: ''
```

### 6. TcpIpIpV6MtuConfig

**描述**: This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIpV6DefaultMtuSize
  长名称: Default Mtu Size
  描述: Maximum Transmission Unit (MTU) of the link.
  默认值: 1500
  最小值: 1280
  最大值: 65535
- 
  序号: 2
  名称: TcpIpIpV6PathMtuEnabled
  长名称: Path Mtu Enabled
  描述: If enabled the IPv6 processes incoming ICMPv6 "Packet Too Big" messages and stores a MTU value
      for each destination address.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpIpV6PathMtuTimeout
  长名称: Path Mtu Timeout
  描述: If this value is >0 the IPv6 will reset the MTU value stored for each destination after n
      seconds.
  默认值: 600
  最小值: 0
  最大值: 86400
```

### 7. TcpIpDhcpServerConfig

**描述**: Specifies the configuration parameters of the DHCP Server sub-module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpDhcpDefaultRouter
  长名称: Default Router
  描述: IP address of default router (gateway).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpDhcpNetmask
  长名称: Netmask
  描述: Network mask of IPv4 address or address prefix of IPv6 address in CIDR Notation, i.e. decimal
      value between 0 and 32 (IPv4) or 0 and 128 (IPv6) that describes the number of
      significant bits defining the network number or prefix of an IP address.
  默认值: 24
  最小值: 0
  最大值: 128
- 
  序号: 3
  名称: TcpIpDhcpOfferValidTime
  长名称: Offer Valid Time
  描述: ''
  默认值: 5
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: TcpIpDhcpLeaseTimeMax
  长名称: Lease Time Max
  描述: |
    This value specifies the maximum lease time. If a client requests a longer lease time the server
    will use this maximum value instead.
    If this parameter does not exists the maximum lease time is infinite.
  默认值: 60
  最小值: 1
  最大值: 4294967295
- 
  序号: 5
  名称: TcpIpDhcpLeaseTimeMin
  长名称: Lease Time Min
  描述: This value specifies the minimum lease time. If a client requests a shorter lease time the
      server will use this minimum value instead.
  默认值: 60
  最小值: 1
  最大值: 4294967295
- 
  序号: 6
  名称: TcpIpDhcpLeaseTimeDefault
  长名称: Lease Time Default
  描述: |
    This value specifies the default lease time that is used if a client does not has requested a
    specific lease time.
    If this parameter does not exist the maximum lease time will be used as default.
  默认值: 4294967295
  最小值: 1
  最大值: 4294967295
- 
  序号: 7
  名称: TcpIpDhcpMaxClientIdLen
  长名称: Max ClientId Len
  描述: |
    This value specifies the maxumin length of a DHCP client identifier.
    A client identifier may be either the value of the 'chaddr' filed in the DHCP message header or
    the content of the client identifier option [RFC2132 9.14. Client-identifier]. A client
    identifer may be up to 255 bytes long but usually the client MAC address is used as client
    identifer. This value should be at least set to 7 in order to store the type (1 byte) and the
    address value (6 bytes).
  默认值: 7
  最小值: 6
  最大值: 255
- 
  序号: 8
  名称: TcpIpDhcpHostname
  长名称: Hostname
  描述: This parameter defines the value of the DHCP server name that will be sent in the 'sname'
      field of outgoing DHCPOFFER, DHCPACK and DHCPNAK messages.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. TcpIpDhcpAddressAssignment

**描述**: Defines a Ethernet Switch port based IP address assignment.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpDhcpAddressLowerBound
  长名称: Address Lower Bound
  描述: The lower bound IP address which shall be assigned.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpDhcpAddressUpperBound
  长名称: Address Upper Bound
  描述: The upper bound IP address which shall be assigned.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. TcpIpIpConfig

**描述**: Specifies the configuration parameters of the IP (Internet Protocol) sub-module

该容器没有参数。

### 10. TcpIpIpV4Config

**描述**: Specifies the configuration parameters of the IPv4 (Internet Protocol version 4) sub-module.

该容器没有参数。

### 11. TcpIpArpConfig

**描述**: Specifies the configuration parameters of the ARP (Address Resolution Protocol) sub-module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpArpNumGratuitousARPonStartup
  长名称: Num Gratuitous ARP On Startup
  描述: Specifies the number of gratuitous ARP replies which shall be sent on assignment of a new IP
      address.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: TcpIpArpPacketQueueEnabled
  长名称: Packet Queue Enabled
  描述: Enables (TRUE) or disables (FALSE) support of the ARP Packet Queue according to IETF RFC 1122,
      section 2.3.2.2.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpArpTableEntryTimeout
  长名称: Table Entry Timeout
  描述: |
    Timeout in seconds after which an unused ARP entry is removed.
    
    A value of 0 means that en entry will never be removed from the ARP table due to a timeout.
    
    If an entry in the ARP cache is used and has not been updated for the specified time, the ARP
    will revalidate the ARP entry by sending one or more ARP requests for the corresponding IP
    address. If the remote host does not send an ARP reply within the period specified by
    TcpIpArpRetryTime, the entry will be removed from the ARP table.
    
    If the ARP cache is full and TcpIpArpDiscardedEntryHandling is set to FALSE, an entry may be
    replaced by a new ARP entry based on a least recently used strategy before the timeout has
    expired.
  默认值: 30
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: TcpIpArpTableSizeMax
  长名称: Table Size Max
  描述: Maximum number of entries in the ARP table.
  默认值: 10
  最小值: 1
  最大值: 65535
- 
  序号: 5
  名称: TcpIpArpRetryTime
  长名称: Retry Timeout
  描述: |
    This value specifies the maximum time for an ARP resolution.
    If no answer has been received before this time has expired, ARP resolution is canceled.
  默认值: 5
  最小值: 0.001
  最大值: 65535
- 
  序号: 6
  名称: TcpIpArpRetryInterval
  长名称: Retry Interval
  描述: This value specifies the ARP retry interval.
  默认值: 2
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: TcpIpArpRequestTimeout
  长名称: ''
  描述: |
    Specifies a timeout in seconds for the validity of ARP requests. After the transmission of an
    ARP request the TcpIp shall skip the transmission of any further ARP requests to the same
    destination within a duration of TcpIpArpRequestTimeout seconds. (IETF RFC 1122, section
    2.3.2.1) The value of this parameter shall be an integral multiple of TcpIpMainFunctionPeriod or
    0. If this Parameter set to 0 this feature is disabled and no delay between ARP requests is
    enforced.
    
    Specifies Timeout for outgoing ARP request, triggered by upperlayer.
    TcpIp will send only one ARP request during ArpRequestTimeout period,even if multiple Tx of ARP
    request is triggered by upperlayer.
    
    i.e. One ARP request transmission(Triggered by upperlayer) per one ArpRequestTimeout period.
    
    
  默认值: 1
  最小值: 0
  最大值: 65535
```

### 12. TcpIpAutoIpConfig

**描述**: Specifies the configuration parameters of the Auto-IP (automatic private IP addressing) sub-module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpAutoIpInitTimeout
  长名称: Init Timeout
  描述: The time Auto-IP waits at startup, before beginning with ARP probing. This delay is used to
      give DHCP time to acquire a lease in case a DHCP server is present.
  默认值: 1
  最小值: 0
  最大值: 65.535
- 
  序号: 2
  名称: TcpIpAutoIpProbeNum
  长名称: Probe Number
  描述: This value specifies the number of probe packets (RFC standard: 3)
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 3
  名称: TcpIpAutoIpProbeMin
  长名称: Probe Min Delay
  描述: This value specifies the minimum interval between probe messages (RFC standard: 1s)
  默认值: 0.4
  最小值: 0
  最大值: 65.535
- 
  序号: 4
  名称: TcpIpAutoIpProbeMax
  长名称: Probe Max Delay
  描述: This value specifies the maximum delay between probe messages (RFC standard: 2s)
  默认值: 0.6
  最小值: 0
  最大值: 65.535
- 
  序号: 5
  名称: TcpIpAutoIpAnnounceWait
  长名称: Announce Wait
  描述: This value specifies the delay before the first announcement message (RFC standard: 2s)
  默认值: 0.5
  最小值: 0
  最大值: 65.535
- 
  序号: 6
  名称: TcpIpAutoIpAnnounceNum
  长名称: Announce Number
  描述: This value specifies the number of announcement packets (RFC standard: 2)
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 7
  名称: TcpIpAutoIpAnnounceInterval
  长名称: Announce Interval
  描述: This value specifies the interval between announcement packets (RFC standard: 2s)
  默认值: 0.4
  最小值: 0
  最大值: 65.535
- 
  序号: 8
  名称: TcpIpAutoIpMaxConflicts
  长名称: Max Number Of Conflicts
  描述: |
    This value specifies the maximum number of conflicts before rate limiting (RFC standard: 10)
    
    If the specified number of conflicts has been reached new address configurations attempts are
    rate limited by "Rate Limit Interval".
  默认值: 10
  最小值: 1
  最大值: 255
- 
  序号: 9
  名称: TcpIpAutoIpRateLimitInterval
  长名称: Rate Limit Interval
  描述: |
    This value specifies the delay between successive address configuration attempts when rate
    limiting is active (RFC standard: 60s)
    
    see "Max Number Of Conflicts"
  默认值: 5
  最小值: 0
  最大值: 65.535
- 
  序号: 10
  名称: TcpIpAutoIpDefendInterval
  长名称: Defend Interval
  描述: This value specifies the minimum interval between defensive ARPs (RFC standard: 10s)
  默认值: 5
  最小值: 0
  最大值: 65.535
- 
  序号: 11
  名称: TcpIpAutoIpProbeWaitMax
  长名称: Probe Wait Max
  描述: This value specifies the maximum initial random delay before the first probe message is sent.
      (RFC standard: 1s)
  默认值: 7
  最小值: 0
  最大值: 65.535
- 
  序号: 12
  名称: TcpIpAutoIpAddrCandidateCalloutFunction
  长名称: IP Address Candidate Callout Function
  描述: |
    This parameter specifies the name of a callout function that shall be called if an address
    candidate for link-local address assignment is required.
    
    Note: The callout should only return valid values from the range 169.254.1.0 to 169.254.254.255
    (inclusive) according to [IETF RFC3927 2.1. Link-Local Address Selection].
    
    If no callout is configured or the callout does not return an address candidate, the TcpIp will
    select a random address according to [IETF RFC3927].
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: TcpIpAutoIpAddrCandidateCalloutHeaderFile
  长名称: IP Address Candidate Callout Function Header File
  描述: This parameter specifies the name of the header file containing the declaration for the
      function specified in TcpIpAutoIpAddrCandidateCalloutFunction.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 13. TcpIpDhcpConfig

**描述**: Specifies the configuration parameters of the DHCPv4.
The SocketOwner is informed via the TcpIpSocketOwnerDhcpEventName callback about the reception and
transmission of options.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpDhcpV4InitWaitMin
  长名称: Init Wait Min
  描述: |
    Minimum initial delay for DISCOVER (RFC standard: 1s)
    
    RESTRICTIONS: 'DhcpV4InitWaitMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.
  默认值: 0.1
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: TcpIpDhcpV4InitWaitMax
  长名称: Init Wait Max
  描述: |
    Maximum initial delay for DISCOVER (RFC standard: 10s)
    
    RESTRICTIONS: 'DhcpV4InitWaitMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.
  默认值: 0.8
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: TcpIpDhcpV4DiscoverMaxNum
  长名称: Discover Max Num
  描述: |
    Maximum number of DISCOVER messages
    
    RESTRICTIONS: 'DhcpV4DiscoverMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.
  默认值: 5
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: TcpIpDhcpV4DiscoverIntervalMin
  长名称: Discover Interval Min
  描述: |
    Minimum DISCOVER interval
    
    RESTRICTIONS: 'DhcpV4DiscoverIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to
    'true'.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: TcpIpDhcpV4DiscoverIntervalMax
  长名称: Discover Interval Max
  描述: |
    Maximum DISCOVER interval
    
    RESTRICTIONS: 'DhcpV4DiscoverIntervalMax' is only available, if 'TcpIpEnableDhcpV4' is set to
    'true'.
  默认值: 30
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: TcpIpDhcpV4RequestMaxNum
  长名称: Request Max Num
  描述: |
    Maximum number of REQUEST messages
    
    RESTRICTIONS: 'DhcpV4RequestMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.
  默认值: 6
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: TcpIpDhcpV4RequestInterval
  长名称: Request Interval
  描述: |
    REQUEST interval
    
    RESTRICTIONS: 'DhcpV4RequestInterval' is only available, if 'TcpIpEnableDhcpV4' is set to
    'true'.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: TcpIpDhcpV4RenewIntervalMin
  长名称: Renew Interval Min
  描述: |
    Minimum Renew interval
    
    RESTRICTIONS: 'DhcpV4RenewIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to
    'true'.
  默认值: 5
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: TcpIpDhcpV4RebindIntervalMin
  长名称: Rebind Interval Min
  描述: |
    Minimum Rebind interval
    
    RESTRICTIONS: 'DhcpV4RebindIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to
    'true'.
  默认值: 5
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: TcpIpDhcpV4HostNameLenMax
  长名称: Host Name Length Max
  描述: |
    Maximum support Host name length
    
    RESTRICTIONS: 'DhcpV4HostNameLenMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.
  默认值: 30
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: TcpIpDhcpV4RestartOnFail
  长名称: Restart On Failure
  描述: |
    Restart the DHCP address assignment process if a used address lease times out and no lease
    update could be obtained. After the lease expires either the DHCP process is restarted or the
    process will be stopped completely (no new address assignment).
    
    RESTRICTIONS: 'TcpIpDhcpV4RestartOnFail' is only available, if 'TcpIpEnableDhcpV4' is set to
    'true'.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: TcpIpDhcpV4RequestedAddrCalloutFunction
  长名称: Requested IP Address Callout Function
  描述: |
    This parameter specifies the name of a callout function that shall be called if an address
    candidate for DHCP address assignment is required. The returned IP address will be included via
    the 'Requested IP Address' option in the DHCPDISCOVER message.
    
    If no callout is configured or the callout does not return an address candidate, the 'Requested
    IP Address' is not contained in the DHCPDISCOVER message.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: TcpIpDhcpV4RequestedAddrCalloutHeaderFile
  长名称: Requested IP Address Callout Function Header File
  描述: This parameter specifies the name of the header file containing the declaration for the
      function specified in TcpIpDhcpV4RequestedAddrCalloutFunction.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 14. TcpIpDhcpUserOption

**描述**: Configures DHCP user options which shall be transmitted/received by the DHCP client.

RESTRICTION: User options are only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpDhcpUserOptionCode
  长名称: ''
  描述: Code of user option.
  默认值: ''
  最小值: 1
  最大值: 254
- 
  序号: 2
  名称: TcpIpDhcpUserOptionLength
  长名称: ''
  描述: Maximum support length of configured user option.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 3
  名称: TcpIpDhcpUserOptionDirection
  长名称: ''
  描述: |
    Direction of configured user option.
    Options with direction TX can be read and written via the AUTOSAR APIs
    TcpIp_DhcpReadOption/TcpIp_DhcpWriteOption.
    Options with direction RX or RX_REQUESTED can only be read or cleared (DataLength == 0).
    If the direction is set to RX_REQUESTED, the DHCP client will request the option via the
    Parameter Request List (option code 55).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 15. TcpIpIcmpConfig

**描述**: Specifies the configuration parameters of the ICMP (Internet Control Message Protocol) sub-module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIcmpTtl
  长名称: Time-To-Live (TTL)
  描述: Default Time-to-live value of outgoing ICMP packets.
  默认值: 64
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: TcpIpIcmpEchoReplyMaxLen
  长名称: Echo Reply Max Buffer Len
  描述: |
    This value specifies the maximum payload length of an Echo Reply.
    If an Echo Request contains more data the payload of the response will be truncated.
  默认值: 32
  最小值: 1
  最大值: 32767
- 
  序号: 3
  名称: TcpIpIcmpDestinationUnreachableEnabled
  长名称: ''
  描述: |
    This parameter defines whether the ICMPv4 shall send ICMP Destination Unreachable messages
    according to IETF RFC 792.
    
    If enabled, the ICMPv4 responds with a Destination Unreachable Message if a unicast packet with
    one of the following properties is received.
    - The upper layer protocol is unknown.
    - The UDP destination port is not open.
  默认值: false
  最小值: ''
  最大值: ''
```

### 16. TcpIpIcmpMsgHandler

**描述**: This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for
the ICMP message handler.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIcmpMsgHandlerHeaderFileName
  长名称: Msg Handler Header File Name
  描述: This parameter specifies the name of the header file containing the definition of the ICMP
      message handler function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpIcmpMsgHandlerName
  长名称: Msg Handler Name
  描述: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 17. TcpIpIpFragmentationConfig

**描述**: Specifies the configuration parameters of IPv4 packet fragmentation/reassembly.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIpFragmentationRxEnabled
  长名称: Enable Packet Reassembly
  描述: Enables (TRUE) or disables (FALSE) support for reassembling of incoming datagrams that are
      fragmented according to IETF RFC 815 (IP Datagram Reassembly Algorithms).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpIpNumFragments
  长名称: Maximum Number of Fragments
  描述: |
    This value specifies the maximum number of IP fragments per datagram.
    This value depends on the maximum TX datagram size and the Maximum Transmission Unit (MTU) of
    the ethernet link.
    
    Note: For reassembly (RX) there is no explicit limit to the number of fragments.
    Instead the number of fragments during reassembly is indirectly limited by the reassembly buffer
    size.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: TcpIpIpNumReassDgrams
  长名称: Number of Reassembly Buffers
  描述: |
    This value specifies the maximum number of fragmented IP datagrams that can be reassembled in
    parallel.
    
    Note: This parameter defines the number of reassembly buffers.
  默认值: 3
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: TcpIpIpReassTimeout
  长名称: Reassembly Timeout
  描述: This value specifies the timeout after which an incomplete datagram gets discarded.
  默认值: 60
  最小值: 0
  最大值: 65.535
- 
  序号: 5
  名称: TcpIpIpMaxReassDgramSize
  长名称: Reassembly Buffer Size
  描述: This value specifies the maximum size of IP datagrams that can be reassembled. One or more
      reassembly buffers of this size will be created.
  默认值: 1500
  最小值: 4
  最大值: 65535
- 
  序号: 6
  名称: TcpIpIpReassInOrderEnabled
  长名称: Optimize for In-Order Reassembly
  描述: |
    This parameter defines whether all fragments of an IP datagram are expected to arrive in order.
    If enabled, reassembly of an IP datagram is aborted if a fragment arrives out of order so the
    buffer is available for reassembly of other datagrams immediately.
    This is an optimization for local networks where all fragments of a fragmented IP datagram
    should arrive in order.
    
    This option should be turned of if fragments may arrive out of order.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpIpMaxTxDgramSize
  长名称: Maximum TX Datagram Size
  描述: |
    This value specifies the maximum size of outgoing IP datagrams (including all headers). If a
    datagram does not fit into the ethernet MTU it will be split up into multiple IP fragments.
    
    Note: No additional buffer is required for transmission of fragmented IP datagrams but there
    must be sufficient ethernet TX buffers to hold all fragments.
  默认值: 1500
  最小值: 64
  最大值: 65535
```

### 18. TcpIpStaticArpTable

**描述**: This container includes one or more static ARP table entries.
It may be referenced by multiple IpV4CtrlConfig containers if they shall use the same static ARP
table.
The static ARP table is stored into the ROM and cannot be overwritten during runtime.
IP instances using this static ARP table will never send ARP requests for the configured addresses.

该容器没有参数。

### 19. TcpIpStaticArpEntry

**描述**: This container includes a static IP address to physical address mapping.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpStaticArpEntryIpAddr
  长名称: IPv4 Address
  描述: This parameter defines the IP address that shall be statically mapped to the physical address
      defined in IpV4StaticArpEntryPhysAddr
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpStaticArpEntryPhysAddr
  长名称: Physical Address
  描述: This parameter defines the physical address that shall be used for outgoing packets to the IP
      address specified in IpV4StaticArpEntryIpAddr
  默认值: ''
  最小值: ''
  最大值: ''
```

### 20. TcpIpIpV6Config

**描述**: Specifies the configuration parameters of the IPv6 (Internet Protocol version 6) sub-module.

该容器没有参数。

### 21. TcpIpDhcpV6Config

**描述**: Specifies the configuration parameters of the DHCPv6.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpDhcpV6CnfDelayMax
  长名称: Cnf Delay Max
  描述: Maximum delay before sending the first Confirm message. If this value is bigger than the
      previous minimum delay value a random delay will be chosen from the interval.
  默认值: 1
  最小值: 0
  最大值: 100
- 
  序号: 2
  名称: TcpIpDhcpV6CnfDelayMin
  长名称: Cnf Delay Min
  描述: Minimum delay before the first Confirm message will be sent.
  默认值: 0
  最小值: 0
  最大值: 100
- 
  序号: 3
  名称: TcpIpDhcpV6InfDelayMax
  长名称: Inf Delay Max
  描述: Maximum delay before sending the first Information Request message. If this value is bigger
      than the previous minimum delay value a random delay will be chosen from the interval.
  默认值: 1
  最小值: 0
  最大值: 100
- 
  序号: 4
  名称: TcpIpDhcpV6InfDelayMin
  长名称: Inf Delay Min
  描述: Minimum delay before the first Information Request message will be sent.
  默认值: 0
  最小值: 0
  最大值: 100
- 
  序号: 5
  名称: TcpIpDhcpV6SolDelayMax
  长名称: Sol Delay Max
  描述: Maximum delay before sending the first Solicit message. If this value is bigger than the
      previous minimum delay value a random delay will be chosen from the interval.
  默认值: 1
  最小值: 0
  最大值: 100
- 
  序号: 6
  名称: TcpIpDhcpV6SolDelayMin
  长名称: Sol Delay Min
  描述: Minimum delay before the first Solicit message will be sent.
  默认值: 0
  最小值: 0
  最大值: 100
- 
  序号: 7
  名称: TcpIpDhcpV6ClientIdTime
  长名称: Client DUID Time
  描述: |
    Time value used to build the DHCP Unique Identifier (DUID) of the client.
    
    The Identifier of the client will be built from this time value and the link-layer address of
    this node.
    
    "The time value is the time that the DUID is generated represented in seconds since midnight
    (UTC), January 1, 2000, modulo 2^32."
    
    [RFC3315 9.2. DUID Based on Link-layer Address Plus Time [DUID-LLT]]
  默认值: 0
  最小值: 0
  最大值: 100
- 
  序号: 8
  名称: TcpIpDhcpV6RandomizeTimeouts
  长名称: Randomize Timeouts
  描述: |
    Use randomization factor for computing retransmission timeouts.
    
    "Each of the computations of a new RT include a randomization factor (RAND), which is a random
    number chosen with a uniform distribution between -0.1 and +0.1. The randomization factor is
    included to minimize synchronization of messages transmitted by DHCP clients."
    
    [RFC3315 14. Reliability of Client Initiated Message Exchanges]
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: TcpIpDhcpV6TxMsgBufferLen
  长名称: Tx Message Buffer Size
  描述: Size of the buffer for outgoing DHCPv6 messages. The size of a DHCPv6 message depends on the
      number and length of options included in it.
  默认值: 128
  最小值: 64
  最大值: 1280
- 
  序号: 10
  名称: TcpIpDhcpV6UseFirstValidAdv
  长名称: Use first valid advertisment
  描述: |
    If enabled the Dhcp will not wait for other advertise messages if a valid one has been received
    but the preference is less than 255.
    
    "A client MUST collect Advertise messages for the first RT seconds, unless it receives an
    Advertise message with a preference value of 255"
    
    [RFC3315 17.1.2. Transmission of Solicit Messages]
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: TcpIpDhcpV6Rfc3646DomainListOptEnabled
  长名称: Enable Domain List Option
  描述: |
    If enabled the DhcpV6 will notify the Dns of dns search lists contained in DOMAIN_LIST options
    of received DHCPv6 Reply messages.
    
    [RFC3646 4. Domain Search List option]
    
    Requires Dns Component.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: TcpIpDhcpV6Rfc3646DnsServersOptEnabled
  长名称: Enable DNS Server Option
  描述: |
    If enabled the DhcpV6 will notify the Dns of dns server addresses contained in DNS_SERVERS
    options of received DHCPv6 Reply messages.
    
    [RFC3646 3. DNS Recursive Name Server option]
    
    Requires Dns Component.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: TcpIpDhcpV6FqdnLenMax
  长名称: Fully Qualified Domain Name Length Max
  描述: |
    Maximum support Fully Qualified Domain Name (Host name) length
    
    RESTRICTIONS: 'TcpIpDhcpV6FqdnLenMax' is only available, if 'TcpIpEnableDhcpV6' is set to
    'true'.
  默认值: 30
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: TcpIpDhcpV6RestartOnFail
  长名称: Restart On Failure
  描述: |
    Restart the DHCP address assignment process if a used address lease times out and no lease
    update could be obtained. After the lease expires either the DHCP process is restarted or the
    process will be stopped completely (no new address assignment).
    
    RESTRICTIONS: 'TcpIpDhcpV6RestartOnFail' is only available, if 'TcpIpEnableDhcpV6' is set to
    'true'.
  默认值: false
  最小值: ''
  最大值: ''
```

### 22. TcpIpDhcpV6UserOption

**描述**: Configures DHCP user options which shall be transmitted/received by the DHCP client.

RESTRICTION: User options are only available, if 'TcpIpEnableDhcpV6' is set to 'true'.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpDhcpV6UserOptionCode
  长名称: ''
  描述: Code of user option.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: TcpIpDhcpV6UserOptionLength
  长名称: ''
  描述: Maximum support length of configured user option.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: TcpIpDhcpV6UserOptionDirection
  长名称: ''
  描述: |
    Direction of configured user option.
    Options with direction TX can be read and written via the AUTOSAR APIs
    TcpIp_DhcpV6ReadOption/TcpIp_DhcpV6WriteOption.
    Options with direction RX or RX_REQUESTED can only be read or cleared (DataLength == 0).
    If the direction is set to RX_REQUESTED, the DHCP client will request the option via the Option
    Request Option (OPTION_ORO 6).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 23. TcpIpIcmpV6Config

**描述**: Specifies the configuration parameters of the ICMPv6 (Internet Control Message Protocol for IPv6)
sub-module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIcmpV6EchoDataBufferSize
  长名称: Echo Data Buffer Size
  描述: Configure the maximum amount of arbitrary data that will be sent back to the sender of an echo
      request. If the arbitrary data of an incoming echo request is bigger than configured
      here, the response payload will be truncated.
  默认值: 64
  最小值: 0
  最大值: 1452
- 
  序号: 2
  名称: TcpIpIcmpV6EchoReplyEnabled
  长名称: Echo Reply Enabled
  描述: If enabled, the stack will respond to incoming ICMPv6 Echo Requests (Pings).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpIcmpV6HopLimit
  长名称: Hop Limit
  描述: Default Hop-Limit value of outgoing ICMPv6 packets.
  默认值: 64
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: TcpIpIcmpV6MsgDestinationUnreachableEnabled
  长名称: Msg Destination Unreachable Enabled
  描述: Dis/Enables transmission of Destination Unreachable Messages
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: TcpIpIcmpV6MsgParameterProblemEnabled
  长名称: Msg Parameter Problem Enabled
  描述: If enabled an ICMPv6 parameter problem message will be sent if a received packet has been
      dropped due to unknown options or headers that are found in the packet.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: TcpIpIcmpV6EchoRequestApiEnabled
  长名称: Enable Echo Request API
  描述: |
    This parameter defines whether the API function IpV6_Icmp_TxEchoRequest() is available. This
    function can be used to send outgoing Echo Requests (Pings) to other Hosts.
    
    Note: This function is for debugging purposes only. Incoming Echo Replies are currently not
    handled by the ICMPv6.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpIcmpV6ErrorMessagesEnabled
  长名称: Send ICMP Error Messages
  描述: |
    This parameter defines whether ICMPv6 Error Messages will be sent as specified in [RFC4443].
    
    [RFC4443 3.2. Packet Too Big Message]
    [RFC4443 3.3. Time Exceeded Message]
    [RFC4443 3.4. Parameter Problem Message]
    
    If disabled, no ICMPv6 Error Messages will be sent
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: TcpIpIcmpV6TxMessageBufferSize
  长名称: Tx Message Buffer Size
  描述: |
    This value specifies the maximum size of outgoing ICMPv6 messages.
    This value should be 1280 if IpV6EnableIcmpErrMsgs is enabled.
    If the value is smaller the Original Packet payload in ICMPv6 Error messages will be truncated.
  默认值: 1280
  最小值: 48
  最大值: 1280
```

### 24. TcpIpIcmpV6MsgHandler

**描述**: This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for
the ICMPv6 message handler.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIcmpV6MsgHandlerHeaderFileName
  长名称: Msg Handler Header File Name
  描述: This parameter specifies the name of the header file containing the definition of the ICMPv6
      message handler function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpIcmpV6MsgHandlerName
  长名称: Msg Handler Name
  描述: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpIcmpV6MaxPayloadLenChgHandlerName
  长名称: Maximum Payload Length Change Callback Function
  描述: |
    This parameter defines a function that will be called when the maximum payload length, that fits
    into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.
    
    see [RFC1981 Path MTU Discovery for IP version 6]
    
    Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr,
    uint16 Mtu)
    
    For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should
    be configured here in order to avoid that TCP transmits packets that need to be fragmented by
    the IP layer.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpIcmpV6IndAddrListReceivedHandlerName
  长名称: Inverse ND Address List Received Callback Function
  描述: |
    This parameter defines a function that will be called when an Inverse Neighbor Discovery
    Solicitation or Advertisement with an Address List Option [RFC3122] is received.
    
    Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType)
    RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);
  默认值: ''
  最小值: ''
  最大值: ''
```

### 25. TcpIpIpV6FragmentationConfig

**描述**: Specifies the configuration parameters of IPv6 packet fragmentation/reassembly.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIpV6ReassemblyBufferCount
  长名称: Rx Reassembly Buffer Count
  描述: Number of buffers that can be used for fragment reassembly. In case of a reassembly error or
      if not all fragments are received in time this buffer will be blocked until the
      specified "Fragment Reassembly Timeout" has been exceeded.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: TcpIpIpV6ReassemblyBufferSize
  长名称: Rx Reassembly Buffer Size
  描述: |
    [RFC2460 5. Packet Size Issues]
    Specifies the maximum size in bytes of a received IPv6 packet that is fragmented.
  默认值: 1500
  最小值: 1500
  最大值: 65535
- 
  序号: 3
  名称: TcpIpIpV6ReassemblySegmentCount
  长名称: Rx Reassembly Out of Order Segment Count
  描述: Specifies the maximum number of consecutive data segments that can be managed in each
      reassembly buffer. If all fragments are received in order, only one segment will be
      needed.
  默认值: 5
  最小值: 1
  最大值: 255
- 
  序号: 4
  名称: TcpIpIpV6ReassemblyTimeout
  长名称: Rx Reassembly Timeout
  描述: |
    [RFC2460 4.5 Fragment Header]
    If this timeout expires all received fragments of an IPv6 packet will be discarded.
    The timeout starts when the first fragment is received.
  默认值: 60
  最小值: 0.001
  最大值: 100
- 
  序号: 5
  名称: TcpIpIpV6TxFragmentBufferCount
  长名称: Tx Fragment Buffer Count
  描述: These buffers will be used if the IPv6 receives packets from the upper layer that do not fit
      into the MTU and thus must be fragmented.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: TcpIpIpV6TxFragmentBufferSize
  长名称: Tx Fragment Buffer Size
  描述: |
    Size of each IPv6 Tx fragmentation buffer in bytes.
    Specifies the maximum size of a Tx IPv6 packet that could be fragmented.
  默认值: 1500
  最小值: 1500
  最大值: 65535
```

### 26. TcpIpNdpConfig

**描述**: Specifies the configuration parameters of the Neighbor Discovery Protocol for IPv6

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpNdpRfc6106DnsslOptEnabled
  长名称: Enable DNS Search List Option
  描述: |
    This parameter defines whether the IPv6 will notify the DNS of domain names of DNS suffixes
    contained in DNSSL options of received Router Advertisements.
    
    [RFC6106 5.2. DNS Search List Option]
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpNdpRfc6106RdnssOptEnabled
  长名称: Enable Recursive DNS Server Option
  描述: |
    This parameter defines whether the IPv6 will notify the DNS of dns server adresses contained in
    RDNS options of received Router Advertisements.
    
    [RFC6106 5.1. Recursive DNS Server Option]
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpNdpV6DropRedirect
  长名称: Drop Redirect message
  描述: This parameter defines if received NDPv6 redirect messages should be droped
  默认值: false
  最小值: ''
  最大值: ''
```

### 27. TcpIpNdpArNudConfig

**描述**: Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability
Detection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpNdpDefaultReachableTime
  长名称: Default Reachable Time
  描述: Configuration of the ReachableTime specified in [RFC4861 6.3.2. Host Variables].
  默认值: 30
  最小值: 0
  最大值: 120
- 
  序号: 2
  名称: TcpIpNdpDefaultRetransTimer
  长名称: Default Retrans Timer
  描述: Configures the default value for the RetransTimer variable specified in [RFC4861 6.3.2. Host
      Variables].
  默认值: 1
  最小值: 0
  最大值: 60
- 
  序号: 3
  名称: TcpIpNdpDelayFirstProbeTime
  长名称: Delay First Probe Time
  描述: Delay before sending the first NUD probe.
  默认值: 5
  最小值: 0
  最大值: 60
- 
  序号: 4
  名称: TcpIpNdpMaxNeighborCacheSize
  长名称: Max Neighbor Cache Size
  描述: Maximum number of entries in the neighbor cache.
  默认值: 5
  最小值: 1
  最大值: 254
- 
  序号: 5
  名称: TcpIpNdpMaxRandomFactor
  长名称: Max Random Factor
  描述: Maximum random factor used for randomization
  默认值: 15
  最小值: 0
  最大值: 100
- 
  序号: 6
  名称: TcpIpNdpMinRandomFactor
  长名称: Min Random Factor
  描述: Minimum random factor used for randomization
  默认值: 5
  最小值: 0
  最大值: 100
- 
  序号: 7
  名称: TcpIpNdpNeighborUnreachabilityDetectionEnabled
  长名称: Neighbor Unreachability Detection Enabled
  描述: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache.
      This feature is a basic feature of NDP and should be turned on.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: TcpIpNdpNumMulticastSolicitations
  长名称: Num Multicast Solicitations
  描述: Maximum number of multicast solicitations that will be sent when performing address
      resolution.
  默认值: 3
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: TcpIpNdpNumUnicastSolicitations
  长名称: Num Unicast Solicitations
  描述: Maximum number of unicast solicitations that will be sent when performig Neighbor
      Unreachability Detection.
  默认值: 3
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: TcpIpNdpPacketQueueEnabled
  长名称: Packet Queue Enabled
  描述: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861,
      section 7.2.2.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: TcpIpNdpRandomReachableTimeEnabled
  长名称: Random Reachable Time Enabled
  描述: If enabled the value of ReachableTime will be multiplied with a random value between
      MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from
      transmitting at exactly the same time
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: TcpIpNdpInverseNaEnabled
  长名称: Inverse Advertisements Enabled
  描述: |
    This parameter defines whether Inverse Neighbor Advertisements are processed or silently
    discarded.
    This also enables the API IpV6_Ndp_SendInverseSolicitation().
    
    Use "User Callback Configuration" to configure a callback function that handles received Address
    Lists.
    
    If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor
    Advertisements will be silently ignored.
    
    [RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: TcpIpNdpInverseNsEnabled
  长名称: Inverse Solicitations Enabled
  描述: |
    This parameter defines whether Inverse Neighbor Advertisements are sent in response to received
    Inverse Neighbor Solicitations.
    
    Use "User Callback Configuration" to configure a callback function that handles received Address
    Lists.
    
    If disabled received Inverse Neighbor Solicitations will be silently ignored.
    
    [RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: TcpIpNdpNeighborCacheUpdateByInverseNaEnabled
  长名称: Inverse Advertisement Neighbor Cache Updates Enabled
  描述: |
    This parameter defines whether the Neighbor Cache will be updated with information from received
    Inverse Neighbor Advertisements.
    
    [RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]
  默认值: true
  最小值: ''
  最大值: ''
```

### 28. TcpIpNdpPrefixRouterDiscoveryConfig

**描述**: Specifies the configuration parameters for NDP Prefix and Router Discovery.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpNdpDefaultRouterListSize
  长名称: Default Router List Size
  描述: Maximum number of default router entries.
  默认值: 2
  最小值: 2
  最大值: 254
- 
  序号: 2
  名称: TcpIpNdpDestinationCacheSize
  长名称: Destination Cache Size
  描述: Maximum number of entries in the destination cache.
  默认值: 5
  最小值: 1
  最大值: 254
- 
  序号: 3
  名称: TcpIpNdpDynamicHopLimitEnabled
  长名称: Dynamic Hop Limit Enabled
  描述: If enabled the default hop limit may be reconfigured based on received Router Advertisements.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpNdpDynamicMtuEnabled
  长名称: Dynamic MTU Enabled
  描述: Allow dynamic reconfiguration of link MTU via Router Advertisements.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: TcpIpNdpDynamicReachableTimeEnabled
  长名称: Dynamic Reachable Time Enabled
  描述: If enabled the default Reachable Time value may be reconfigured based on received Router
      Advertisements.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: TcpIpNdpDynamicRetransTimeEnabled
  长名称: Dynamic Retrans Time Enabled
  描述: If enabled the default Retransmit Timer value may be reconfigured based on received Router
      Advertisements.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpNdpMaxRtrSolicitationDelay
  长名称: Max Rtr Solicitation Delay
  描述: Maximum delay before the first Router Solicitation will be sent after interface
      initialization.
  默认值: 1
  最小值: 0.001
  最大值: 60
- 
  序号: 8
  名称: TcpIpNdpMaxRtrSolicitations
  长名称: Max Rtr Solicitations
  描述: Maximum number of Router Solicitations that will be sent before the first Router Advertisement
      has been received.
  默认值: 3
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: TcpIpNdpPrefixListSize
  长名称: Prefix List Size
  描述: Maximum number of entries in the on-link prefix list.
  默认值: 5
  最小值: 1
  最大值: 254
- 
  序号: 10
  名称: TcpIpNdpRndRtrSolicitationDelayEnabled
  长名称: Rnd Rtr Solicitation Delay Enabled
  描述: If enabled the first router solicitation will be delayed randomly from
      [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent
      after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: TcpIpNdpRtrSolicitationInterval
  长名称: Rtr Solicitation Interval
  描述: Interval between consecutive Router Solicitations.
  默认值: 4
  最小值: 0.001
  最大值: 60
- 
  序号: 12
  名称: TcpIpNdpOnLinkPrefix
  长名称: On Link Prefix
  描述: |
    This parameter defines one or more IPv6 address prefixes that shall always be considered as
    on-link.
    This means, link layer address resolution will be performed for all addresses starting with this
    prefix instead of forwading packets to the defautl router.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: TcpIpNdpDropRouterAdvertisement
  长名称: Drop Router Advertisement
  描述: This parameter defines if received router advertisement should be droped
  默认值: false
  最小值: ''
  最大值: ''
```

### 29. TcpIpNdpSlaacConfig

**描述**: Specifies the configuration parameters for StateLess Address AutoConfiguration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpNdpSlaacDadNumberOfTransmissions
  长名称: DAD Number Of Transmissions
  描述: Number of Neighbor Solicitations that have to be unanswered in order to set an
      autoconfigurated address to PREFERRED (usable) state.
  默认值: 1
  最小值: 0
  最大值: 254
- 
  序号: 2
  名称: TcpIpNdpSlaacDadRetransmissionDelay
  长名称: DAD Retransmission Delay
  描述: |
    Sets the maximum value for the address configuration delay.
    
    (This parameter is currently not used and does not affect the functionality of the module.)
  默认值: 1
  最小值: 0
  最大值: 10
- 
  序号: 3
  名称: TcpIpNdpSlaacDelayEnabled
  长名称: Slaac Delay Enabled
  描述: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random
      value from [0...MAX_DAD_DELAY].
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpNdpSlaacOptimisticDadEnabled
  长名称: Optimistic DAD Enabled
  描述: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: TcpIpNdpSlaacMinLifetime
  长名称: Minimum Address Lifetime
  描述: |
    This value specifies the minimum valid Lifetime for addresses configured via Stateless Address
    Autoconfiguration.
    
    [RFC4862 5.5.3. e]
    
    RFC Default: 7200sec (2hrs)
  默认值: 7200
  最小值: 10
  最大值: 120000
- 
  序号: 6
  名称: TcpIpNdpSlaacMaxDelay
  长名称: Max address configuration delay
  描述: |
    This value specifies the maximum value for the address configuration delay.
    
    According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the
    same as MAX_RTR_SOLICITATION_DELAY.
    
    RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds
  默认值: 1
  最小值: 0
  最大值: 65.535
```

### 30. TcpIpIpV6MldConfig

**描述**: This container includes configuration parameters for the Multicast Listener Discovery Version 2
(MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpMldV1QuerierPresentTimeout
  长名称: Older Version Querier Present Timeout
  描述: |
    This value specifies the value of the "Older Version Querier Present Timeout" Variable.
    
    See [RFC3810 9.12. Older Version Querier Present Timeout]
    
    "This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query
    Response Interval])."
  默认值: 5000
  最小值: 1
  最大值: 600000
- 
  序号: 2
  名称: TcpIpMldIfStatePoolSize
  长名称: If State Pool Size
  描述: This value specifies the maximum number of multicast addresses the IPv6 instance can listen
      to.
  默认值: 8
  最小值: 1
  最大值: 254
- 
  序号: 3
  名称: TcpIpMldSrcAddrPoolSize
  长名称: Src Addr Pool Size
  描述: |
    This value specifies the maximum number of source addresses that can be stored for all
    socket-based multicast memberships.
    
    If multicast packets shall only be received if they have been sent from specific source
    addresses each of these addresses requires an entry in this pool.
  默认值: 32
  最小值: 0
  最大值: 254
- 
  序号: 4
  名称: TcpIpMldSocketMembershipPoolSize
  长名称: Socket Membership Pool Size
  描述: |
    This value specifies the maximum number of multicast memberships that can be managed via the
    IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address
    can apper at most once for each socket.
    
    Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast
    groups)
    Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address
    group)
  默认值: 8
  最小值: 1
  最大值: 254
- 
  序号: 5
  名称: TcpIpMldIfStateSrcAddrPoolSize
  长名称: If State Src Addr Pool Size
  描述: |
    This value specifies the total number of all source addresses for all multicast addresses.
    
    This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast
    packets from the same source addresses.
  默认值: 16
  最小值: 1
  最大值: 254
- 
  序号: 6
  名称: TcpIpMldRobustness
  长名称: Robustness
  描述: |
    This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1.
    Robustness Variable].
    
    "MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable
    MUST NOT be zero, and SHOULD NOT be one. Default value: 2."
  默认值: 2
  最小值: 1
  最大值: 255
- 
  序号: 7
  名称: TcpIpMldMaxReportMsgSize
  长名称: Max Report Msg Size
  描述: |
    This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40
    bytes) and the Hop-by-Hop header (8 bytes).
    This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)
  默认值: 1280
  最小值: 76
  最大值: 1500
- 
  序号: 8
  名称: TcpIpMldMinUnsolicitedReportInt
  长名称: Min Unsolicited Report Int
  描述: |
    This value specifies the lower bound for the randomized Unsolicited Report Interval.
    
    If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.
    
    RFC Default: 0
    
    See: IpV6MldMaxUnsolicitedReportInt
  默认值: 0
  最小值: 0
  最大值: 100000
- 
  序号: 9
  名称: TcpIpMldMaxUnsolicitedReportInt
  长名称: Max Unsolicited Report Int
  描述: |
    This value specifies the upper bound for the randomized Unsolicited Report Interval.
    
    "The Unsolicited Report Interval is the time between repetitions of a node's initial report of
    interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]
    
    RFC Default: 1 second.
    
    "To cover the possibility of the State Change Report being missed by one or more multicast
    routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission
    Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])."
    [RFC3810 6.1. Action on Change of Per-Interface State]
  默认值: 1000
  最小值: 0
  最大值: 100000
```

### 31. TcpIpIpV6PrivExtConfig

**描述**: This container includes configuration parameters for the Privacy Extensions for Stateless Address
Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpPrivExtTempValidLifetime
  长名称: Lifetime of temp. Address
  描述: |
    This value specifies the maximum time a temporary address is valid.
    
    RFC Default: 604800s (1 week)
    [RFC4941 5. Defined Constants]
    
    [RFC4941 3.3. Generating Temporary Addresses / 1.]
  默认值: 604800
  最小值: 0
  最大值: 4294967
- 
  序号: 2
  名称: TcpIpPrivExtTempPreferredLifetime
  长名称: Time temp. Address is preferred
  描述: |
    This value specifies the maximum time a temporary address is preferred.
    
    RFC Default: 86400s (1 day)
    [RFC4941 5. Defined Constants]
    
    [RFC4941 3.3. Generating Temporary Addresses / 1.]
  默认值: 86400
  最小值: 0
  最大值: 4294967
- 
  序号: 3
  名称: TcpIpPrivExtRegenAdvance
  长名称: Time in advance for temp. Address Regeneration
  描述: |
    A new temporary addresses is generated RegenAdvance time units before its predecessor gets
    deprecated.
    
    RFC Default: 5s
    [RFC4941 5. Defined Constants]
    
    "To ensure that a preferred temporary address is always available, a new temporary address
    SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient
    time to avoid race conditions in the case where generating a new temporary address is not
    instantaneous, such as when duplicate address detection must be run. The node SHOULD start the
    address regeneration process REGEN_ADVANCE time units before a temporary address would actually
    be deprecated."
    [RFC4941 3.4. Expiration of Temporary Addresses]
  默认值: 5
  最小值: 0
  最大值: 100
- 
  序号: 4
  名称: TcpIpPrivExtMaxDesyncFactor
  长名称: DeSync-Factor upper bound
  描述: |
    This value specifies the upper bound for the random value DESYNC_FACTOR.
    
    RFC Default: 600s (10 minutes)
    [RFC4941 5. Defined Constants]
    
    "The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients
    don't synchronize with each other and generate new addresses at exactly thesame time."
    [RFC4941 3.5. Regeneration of Randomized Interface Identifiers]
  默认值: 600
  最小值: 0
  最大值: 10000
- 
  序号: 5
  名称: TcpIpPrivExtTempIdGenRetries
  长名称: Interface UID generation retries
  描述: |
    This parameter defines the number of times the node shall retry to generate an unique interface
    identifier for a temporary address.
    
    If an unique identifier could not be generated after the specified number of retries, there will
    be no temporary address available.
    
    RFC Default: 3
    [RFC4941 5. Defined Constants]
    [RFC4941 3.3. Generating Temporary Addresses / 7.]
  默认值: 3
  最小值: 0
  最大值: 10
- 
  序号: 6
  名称: TcpIpPrivExtMaxTempAddrs
  长名称: Temp. Address count
  描述: |
    This value specifies the maximum number of temporary addresses that can be configured at the
    same time.
    
    This should be at least 2 times the number of golbal prefixes advertised by routers.
  默认值: 4
  最小值: 1
  最大值: 254
- 
  序号: 7
  名称: TcpIpPrivExtUseOnLinkPrefixes
  长名称: Use On Link Prefixes
  描述: This parameter defines whether the IPv6 will generate temporary addresses for prefixes marked
      as on-link in received Router Advertisements. Normally temporary addresses are only
      created for prefixes that are not marked as on-link.
  默认值: false
  最小值: ''
  最大值: ''
```

### 32. TcpIpLocalAddr

**描述**: Specifies the local IP (Internet Protocol) addresses used for IP communication.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpAddrId
  长名称: Addr ID
  描述: IP address table identifier assigned by TCP/IP stack.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: TcpIpAddressType
  长名称: ''
  描述: Address type.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpDomainType
  长名称: ''
  描述: Address family.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpIpAddrReceiveAllNotConfiguredMulticasts
  长名称: IP Addr Receive All Not Configured Multicasts
  描述: |
    This configuration is only useable for IPv4 adresses:
    This parameter defines whether an address of type TCPIP_IPV4_BROADCAST shall also be used to
    receive multicasts that have not been configured individually by addresses of type
    TCPIP_MULTICAST.
    
    Note: If this parameter is set, the IPv4 will configure the EthIf to accept all multicast
    packets on the corresponsing controller.
    
    This parameter is only valid for a TCPIP_IPV4_BROADCAST address.
  默认值: false
  最小值: ''
  最大值: ''
```

### 33. TcpIpAddrAssignment

**描述**: This container is a subcontainer of TcpIpLocalAddr and specifies the assignment policy for the IP
address.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpAssignmentLifetime
  长名称: ''
  描述: |
    Defines the lifetime of a dynamically fetched IP address.
    
    TCPIP_FORGET: After IP address has been assigned just use it for this link-up time. (default)
    TCPIP_STORE: After IP address has been assigned store the address persistently into NvM.
    
    If this parameter exists and "AssignmentMethod" is set to TCPIP_STATIC, the address can be
    assigned/changed during runtime via the TcpIp_RequestIpAddrAssignment() API.
  默认值: TCPIP_FORGET
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpAssignmentMethod
  长名称: ''
  描述: Method of address assignment
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpAssignmentPriority
  长名称: ''
  描述: Priority of assignment (1 is highest). If a new address from an assignment method with a
      higher priority is available, it overwrites the IP address previously assigned by an
      assignment method with a lower priority.
  默认值: 1
  最小值: 1
  最大值: 3
- 
  序号: 4
  名称: TcpIpAssignmentTrigger
  长名称: ''
  描述: |
    AUTOMATIC: The address assignment method is triggerred automatically after the pysical link is
    established. A statically configured IP address (see TcpIpStaticIpAddressConfig) will be
    assigned immediately but may be changed during runtime by calling
    TcpIp_RequestIpAddrAssignment()
    
    MANUAL: The address assignment method is triggered manually by the user by calling
    TcpIp_RequestIpAddrAssignment().
  默认值: TCPIP_AUTOMATIC
  最小值: ''
  最大值: ''
```

### 34. TcpIpStaticIpAddressConfig

**描述**: This container is a subcontainer of TcpIpLocalAddr and specifies a static IP address including
directly related parameters.

If this container is not present and the "Assignment Method" of this address is TCPIP_STATIC the
address will be unassigned after startup and can be assigned/changed via the
TcpIp_RequestIpAddrAssignment() API.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpDefaultRouter
  长名称: ''
  描述: IP address of default router (gateway)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpNetmask
  长名称: ''
  描述: Network mask of IPv4 address or address prefix of IPv6 address in CIDR Notation, i.e. decimal
      value between 0 and 32 (IPv4) or 64 (IPv6) that describes the number of significant bits
      defining the network number or prefix of an IP address.
  默认值: ''
  最小值: 1
  最大值: 128
- 
  序号: 3
  名称: TcpIpStaticIpAddress
  长名称: ''
  描述: Static IP Address.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpIpV6AddrPrefixIsOnLink
  长名称: ''
  描述: |
    This parameter defines whether the prefix of this static IPv6 address shall be considered as "on
    link" by the IPv6. This means the IPv6 will perform link layer address resolution for addresses
    with this prefix.
    Usually the IPv6 will only do link layer address resolution for link local addresses using the
    prefix fe80::/10 or for addresses with prefixes that have been marked to be on link by received
    router advertisements.
  默认值: false
  最小值: ''
  最大值: ''
```

### 35. TcpIpNvmBlock

**描述**: Configuration of optional usage of Nvm in case the TcpIp module requires non volatile memory in the
Ecu to store information (e.g. IP Address received via DHCP and shall be stored).

该容器没有参数。

### 36. TcpIpPhysAddrConfig

**描述**: Specifies the physical address configuration.

该容器没有参数。

### 37. TcpIpPhysAddrChgHandler

**描述**: This container is a subcontainer of TcpIpPhysAddrConfig and configures the optional callback
function to notify a physical address change.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpPhysAddrChgHandlerHeaderFileName
  长名称: Header File Name
  描述: This parameter specifies the name of the header file containing the definition of the physical
      address change handler function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpPhysAddrChgHandlerName
  长名称: Handler Name
  描述: This parameter defines the name of the physical address change function <Up>_PhysAddrTableChg.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 38. TcpIpPhysAddrChgDiscardedHandler

**描述**: This container is a subcontainer of TcpIpPhysAddrConfig and configures the optional callback
function to notify the discarding of a physical address entry.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpPhysAddrChgDiscardedHandlerHeaderFileName
  长名称: Header File Name
  描述: This parameter specifies the name of the header file containing the definition of the physical
      address entry discarded handler function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpPhysAddrChgDiscardedHandlerName
  长名称: ''
  描述: This parameter defines the name of the IP address entry discarded/updated/overwritten function
      <UL>_PhysAddrTableChgDiscarded.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 39. TcpIpSocketOwnerConfig

**描述**: Specifies the upper layer modules of TcpIp using the socket API.

该容器没有参数。

### 40. TcpIpSocketOwner

**描述**: This container is a subcontainer of TcpIpSocketOwnerConfig and specifies an upper layer of TcpIp
that uses the socket API.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpSocketOwnerCopyTxDataName
  长名称: CopyTxData Name
  描述: |
    This parameter defines the name of the <Up_CopyTxData> function of the TcpIpSocketOwner module.
    The function name is only configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpSocketOwnerHeaderFileName
  长名称: Header File Name
  描述: This parameter specifies the name of the header file containing the definition of the
      TcpIpSocketOwner module functions. The header file is only configurable if
      TcpIpSocketOwnerUpperLayerType is set to CDD.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpSocketOwnerLocalIpAddrAssignmentChgName
  长名称: Local IP Addr Assignment Chg Name
  描述: This parameter defines the name of the <Up_LocalIpAddrAssignmentChg> function of the
      TcpIpSocketOwner module. The function name is only configurable if
      TcpIpSocketOwnerUpperLayerType is set to CDD.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpSocketOwnerRxIndicationName
  长名称: RX Indication Name
  描述: |
    This parameter defines the name of the <Up_RxIndication> function of the TcpIpSocketOwner
    module.
    The function name is only configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: TcpIpSocketOwnerTcpAcceptedName
  长名称: TCP Accepted Name
  描述: |
    This parameter defines the name of the <Up_TcpAccepted> function of the TcpIpSocketOwner module.
    The function name is only configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: TcpIpSocketOwnerTcpConnectedName
  长名称: TCP Connected Name
  描述: |
    This parameter defines the name of the <Up_TcpConnected> function of the TcpIpSocketOwner
    module.
    The function name is only configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpSocketOwnerTxConfirmationName
  长名称: TX Confirmation Name
  描述: |
    This parameter defines the name of the <Up_TxConfirmation> function of the TcpIpSocketOwner
    module.
    The function name is only configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: TcpIpSocketOwnerUpperLayerType
  长名称: Upper Layer Type
  描述: This parameter specifies the type of the upper layer module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: TcpIpSocketOwnerId
  长名称: Socket User Index
  描述: |
    This value specifies the ID of the socket user.
    (auto calculated)
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 10
  名称: TcpIpSocketOwnerTcpIpEventName
  长名称: TcpIp Event Name
  描述: |
    This parameter defines the name of the <Up_TcpIpEvent> function of the TcpIpSocketOwner module.
    The function name is only configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: TcpIpSocketOwnerTcpListenSocketMax
  长名称: TCP Listen Socket Max
  描述: This value specifies the number of TCP listen sockets this socket owner will use
      simultaneously
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: TcpIpSocketOwnerCopyTxDataDynamicLengthEnabled
  长名称: CopyTxData Dynamic Length Enabled
  描述: This parameter specifies that the 'BufLength' parameter of CopyTxData is an IN/OUT parameter
      that allows the user to provide less data than specified in the Trasmit call. If
      CopyTxData decreases the parameter value, the TcpIp will not call CopyTxData again and
      send only the data that has been provided so far.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: TcpIpSocketOwnerTlsValidationResultName
  长名称: Tls Validation Result Name
  描述: |
    This parameter specifies the name of the function to indicate the TLS validation result for a
    server certificate chain.
    The function is only used for TCP sockets where TLS is enabled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: TcpIpSocketOwnerDhcpEventName
  长名称: DHCP Event Name
  描述: |
    This parameter defines the name of the <Up_DhcpEvent> function of the TcpIpSocketOwner module.
    Via this callout the upper layer will be informed about received and transmitted DHCP options.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: TcpIpSocketOwnerTlsCertRequestName
  长名称: Tls Certificate Request Name
  描述: |
    This parameter specifies the name of the function to provide the Socket Owner the elements of
    the certificate reqeust message and to provide the TLS the certificates that should be used.
    The function is only used for TCP sockets where TLS is enabled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: TcpIpSocketOwnerTlsChangeableCipherName
  长名称: Tls Changeable Cipher Name
  描述: |
    This parameter specifies the name of the function to provide the Socket Owner the changable
    lists of cipher suites and signature algorithms.
    The function is only used for TCP sockets where TLS is enabled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: TcpIpSocketOwnerTlsKeyUpdateName
  长名称: Tls Key Update Name
  描述: |
    This parameter specifies the name of the function to provide the Socket Owner the info about a
    key update in the current TLS connection.
    The function is only used for TCP sockets where TLS and secret access
    (TcpIpTlsSupportSecretAccess) is enabled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: TcpIpSocketOwnerTlsSessionTicketUpdateName
  长名称: ''
  描述: This parameter specifies the name of a callout function that informs an user about the current
      available session tickets in a TLS 1.3 connection.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 41. TcpIpTcpConfig

**描述**: Specifies the configuration parameters of the TCP (Transmission Control Protocol) sub-module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpTcpCongestionAvoidanceEnabled
  长名称: Congestion Avoidance Enabled
  描述: Enables (TRUE) or disables (FALSE) support of TCP congestion avoidance algorithm according to
      IETF RFC 5681.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpTcpFastRecoveryEnabled
  长名称: Fast Recovery Enabled
  描述: Enables (TRUE) or disables (FALSE) support of TCP Fast Recovery according to IETF RFC 5681.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpTcpFastRetransmitEnabled
  长名称: Fast Retransmit Enabled
  描述: Enables (TRUE) or disables (FALSE) support of TCP Fast Retransmission according to IETF RFC
      5681.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpTcpFinWait2Timeout
  长名称: FIN Wait 2 Timeout
  描述: |
    Timeout to receive a FIN from the remote node (after this node has initiated connection
    termination), i.e. maximum time waiting in FINWAIT-2 for a connection termination request from
    the remote TCP.
    
    Value of Timeout must be atleast 1 MSL.
    
    Default value is 120s
  默认值: 120
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: TcpIpTcpKeepAliveEnabled
  长名称: Keep Alive Enabled
  描述: |
    Enables (TRUE) or disables (FALSE) TCP Keep Alive Probes according to IETF RFC 1122 chapter
    4.2.3.6
    
    Note: This parameter only enables general support of the Keep Alive Mechanism.
    Keep Alive must be enabled explicitly for each socket during runtime. (see
    SoAdSocketTcpKeepAlive* parameters)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: TcpIpTcpKeepAliveInterval
  长名称: Keep Alive Interval
  描述: |
    Specifies the default interval between subsequent Keep Alive Probes.
    If TcpIpTcpKeepAliveProbesMax is set to 0, this parameter has no effect by default but may have
    an effect if the number of Keep Alive Probes is changed during runtime.
  默认值: 0
  最小值: 0
  最大值: 4294967
- 
  序号: 7
  名称: TcpIpTcpKeepAliveProbesMax
  长名称: Keep Alive Probes Max
  描述: Default number of times that a TCP Keep Alive Probe is retransmitted before the connection is
      closed.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: TcpIpTcpKeepAliveTime
  长名称: Keep Alive Time
  描述: Specifies the time between the last data packet sent (simple ACKs are not considered data) and
      the first Keep Alive Probe. Note: Setting this configuration parameter to a value
      smaller or equal to the value of TcpIpMainFunctionPeriod results in the transmission of
      Keep Alive Probes within every MainFunction cycle.
  默认值: 7200
  最小值: 0
  最大值: 4294967
- 
  序号: 9
  名称: TcpIpTcpMaxRtx
  长名称: Max Rtx
  描述: Maximum number of times that a TCP segment is retransmitted before the TCP connection is
      closed. This parameter is only valid if TcpIpTcpRetransmissionTimeout is configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: TcpIpTcpMsl
  长名称: Maximum Segment Lifetime (MSL)
  描述: Maximum segment lifetime.
  默认值: 120
  最小值: 0
  最大值: 31536000
- 
  序号: 11
  名称: TcpIpTcpNagleEnabled
  长名称: Nagle Enabled
  描述: Enables (TRUE) or disables (FALSE) support of Nagle's algorithm according to IETF RFC 896. If
      enabled the Nagle's algorithm is activated per default for all TCP sockets, but can be
      deactivated via TcpIp_ChangeParameter() API.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: TcpIpTcpReceiveWindowMax
  长名称: Receive Window Max
  描述: |
    Default value of maximum receive window in bytes.
    
    (This parameter is currently not used and does not affect the functionality of the module.)
  默认值: 512
  最小值: 0
  最大值: 65535
- 
  序号: 13
  名称: TcpIpTcpRetransmissionTimeout
  长名称: Retransmission Timeout
  描述: Timeout before an unacknowledged TCP segment is sent again.
  默认值: 1
  最小值: 0.001
  最大值: 31536000
- 
  序号: 14
  名称: TcpIpTcpSlowStartEnabled
  长名称: Slow Start Enabled
  描述: Enables (TRUE) or disables (FALSE) support of TCP slow start algorithm according to IETF RFC
      5681.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: TcpIpTcpSynMaxRtx
  长名称: SYN Max Rtx
  描述: |
    Maximum number of times that a TCP SYN is retransmitted.
    
    (This parameter is currently not used and does not affect the functionality of the module.)
  默认值: 255
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: TcpIpTcpSynReceivedTimeout
  长名称: SYN Received Timeout
  描述: |
    Timeout to complete a remotely initiated TCP connection establishment, i.e. maximum time waiting
    in SYN-RECEIVED for a confirming connection request acknowledgment after having both received
    and sent a connection request.
    
    (This parameter is currently not used and does not affect the functionality of the module.)
  默认值: 0
  最小值: 0
  最大值: 31536000
- 
  序号: 17
  名称: TcpIpTcpTtl
  长名称: Time-To-Live (TTL)
  描述: |
    Default Time-to-live value of outgoing TCP packets.
    (This parameter is not used and has no influence on the processing of the module. The default
    TTL can be set for each TcpIpCtrl (IPv4: TcpIpIpDefaultTtl, IPv6: TcpIpIpV6DefaultHopLimit) and
    can be changed during runtime via TcpIp_ChangeParameter() API for each socket.)
  默认值: 64
  最小值: 0
  最大值: 255
- 
  序号: 18
  名称: TcpIpTcpEnableDiagReadAckSeqNum
  长名称: Enable Diag Read Ack Seq Num
  描述: |
    Enable reading of current TCP sequence number and acknowledgement number for a specified socket.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: TcpIpTcpSackOptionSupport
  长名称: Enable Selective Acknowledgement Support
  描述: |
    This parameter defines if the TCP option 'selective acknowlagement' is enabled.
    [RFC 2018]
    
    RESTRICTIONS: 'TcpSackOptionSupport' is only available, if 'TcpOutOfOrderRxSupport' is set to
    'true'.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: TcpIpTcpMaxNumOooSegsPerSocket
  长名称: Max Num Out Of Order Segments per Socket
  描述: |
    This value specifes the maximum number of out of order control elements that can be allocated
    for one TCP socket during runtime.
    
    RESTRICTIONS: 'TcpAvgNumOooSegsPerSocket' is only available, if 'TcpOutOfOrderRxSupport' is set
    to 'true'.
  默认值: 5
  最小值: 1
  最大值: 65535
- 
  序号: 21
  名称: TcpIpTcpAvgNumOooSegsPerSocket
  长名称: Avg Num Out Of Order Segments per Socket
  描述: |
    This value specifes the number of out of order control elements per TCP socket.
    
    The elements are grouped into a pool shared by all TCP sockets.
    A TCP socket is allowed to allocate as much elements as specified by
    'TcpIpTcpMaxNumOooSegsPerSocket'.
    
    RESTRICTIONS: 'TcpAvgNumOooSegsPerSocket' is only available, if 'TcpOutOfOrderRxSupport' is set
    to 'true'.
  默认值: 5
  最小值: 1
  最大值: 254
- 
  序号: 22
  名称: TcpIpTcpUserTimeoutDef
  长名称: User Timeout Def
  描述: |
    This value specifies the default value for User Timeout.
    (default: 20s)
    (time transmitted data may stay un-acknowlaged)
    
    RESTRICTION: Value of 'TcpUserTimeoutDef' has to be in the range defined by 'TcpUserTimeoutMin'
    and 'TcpUserTimeoutMax'.
  默认值: 20
  最小值: 0
  最大值: 10000
- 
  序号: 23
  名称: TcpIpTcpUserTimeoutMax
  长名称: User Timeout Max
  描述: |
    This value specifes the maximum value for User Timeout.
    (default: 300s)
    
    RESTRICTION: Value of 'TcpUserTimeoutMax' has to be greater than 'TcpUserTimeoutMin' and greater
    than or equal to 'TcpUserTimeoutDef'.
  默认值: 300
  最小值: 0
  最大值: 10000
- 
  序号: 24
  名称: TcpIpTcpUserTimeoutMin
  长名称: User Timeout Min
  描述: |
    This value specifies the minimum value for User Timeout.
    (default: 5s)
    RFC 1122 defines it to 100 seconds (3 minutes for SYN segments).
    
    RESTRICTION: Value of 'TcpUserTimeoutMin' has to be smaller than 'TcpUserTimeoutMax' and smaller
    than or equal to 'TcpUserTimeoutDef'.
  默认值: 5
  最小值: 0
  最大值: 5000
- 
  序号: 25
  名称: TcpIpTcpUserTimeoutOptionSupport
  长名称: User Timeout Option Support
  描述: This parameter defines if the User Timeout Option of TCP is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: TcpIpTcpTimeStampOptionSupport
  长名称: Time Stamp Option
  描述: This parameter defines if the Timestamp Option of TCP is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: TcpIpTcpNagleTimeout
  长名称: Nagle Timeout
  描述: |
    This value specifies the timeout for Nagle algorithm, The timeout defines the time after which a
    small TCP segment is sent even though a previous segment is not yet acked.
    Setting the timeout value to '0' turns the timeout function off and TCP will wait forever to
    send a small segment if previously sent data is still not acked by the peer. This setting may
    cause a huge delay if the peer uses 'delayed acknowledgement'.
    
    Note:
    Value must be a multiple of Main Function Period
    
    RESTRICTIONS: 'TcpNagleTimeoutMsec' is only available, if 'TcpEnableNagle' is enabled.
  默认值: 0
  最小值: 0
  最大值: 0.255
- 
  序号: 28
  名称: TcpIpTcpTxResetQueueSize
  长名称: Tx Reset Queue Size
  描述: |
    This value specifies the amount of entries reserved for the Tx Reset Queue.
    
    Note:
    The Reset Queue is shared by all TCP Sockets.
  默认值: 8
  最小值: 0
  最大值: 127
- 
  序号: 29
  名称: TcpIpTcpTxRetryQueueSize
  长名称: Average Tx Retry Queue Size
  描述: |
    This value specifies the average amount of entries allocated for the Tx Retry Queue of one TCP
    Socket.
    
    Note:
    The Retry Queues are grouped in a pool shared by all TCP Sockets. Therefore a Socket may have
    less entries available as specified.
  默认值: 10
  最小值: 0
  最大值: 127
- 
  序号: 30
  名称: TcpIpTcpOutOfOrderRxSupport
  长名称: Out Of Order Rx Support
  描述: This parameter defines if the reception of out of order TCP segments is supported.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: TcpIpTcpRetransmissionTimeoutMax
  长名称: Retransmission Timeout Max
  描述: |
    Maximum Timeout before an unacknowledged TCP segment is sent again.
    This value is an upper limit for the exponential backoff of the retransmission timer and the
    computation according to [RFC 6298 Computing TCP's Retransmission Timer] if the Timestamp Option
    defined in [RFC1323] is enabled.
    
  默认值: 60
  最小值: 1
  最大值: 300
- 
  序号: 32
  名称: TcpIpTcpNoRstInvSocket
  长名称: No RST on Invalid Socket
  描述: This parameter specifies whether the TCP module shall suppress the transmission of a RST (RFC
      793 p.64) when the ECU receives a message on a port without a open socket.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 33
  名称: TcpIpTcpPortMin
  长名称: Tcp Dynamic Port Min
  描述: If the API TcpIp_Bind() is called on a TCP socket without specified port, the local TCP port
      is chosen as the next free port in the range between TcpIpTcpPortMin and
      TcpIpTcpPortMax.
  默认值: 49152
  最小值: 1
  最大值: 65535
- 
  序号: 34
  名称: TcpIpTcpPortMax
  长名称: Tcp Dynamic Port Max
  描述: If the API TcpIp_Bind() is called on a TCP socket without specified port, the local TCP port
      is chosen as the next free port in the range between TcpIpTcpPortMin and
      TcpIpTcpPortMax.
  默认值: 65535
  最小值: 1
  最大值: 65535
```

### 42. TcpIpTcpSocketBuffer

**描述**: This container includes the rx and tx buffer configuration of a TCP socket.
The number of available socket handles will be the sum of all TCP rx and tx buffer configurations
and the number of all TCP listen sockets.

Note: rx and tx buffers are not bound to a specific socket handle.
The buffers are shared between all users and must be allocated to a socket during runtime via the
TcpIp_ChangeParameter() API.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpTcpSocketRxBufferSize
  长名称: Socket Rx Buffer Size
  描述: |
    This value specifies the size of a RX buffer segment that can be allocated to a TCP socket
    handle via the TcpIp_ChangeParameter() API during runtime.
    
    Note: A buffer segment is shared between all TCP sockets but can only be used for one socket at
    a time. If multiple sockets with the same buffer size shall be used simultaneously, multiple
    buffer segments of the same size have to be configured.
  默认值: 512
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: TcpIpTcpSocketTxBufferSize
  长名称: Socket Tx Buffer Size
  描述: |
    This value specifies the size of a TX buffer segment that can be allocated to a TCP socket
    handle via the TcpIp_ChangeParameter() API during runtime.
    
    Note: A buffer segment is shared between all TCP sockets but can only be used for one socket at
    a time. If multiple sockets with the same buffer size shall be used simultaneously, multiple
    buffer segments of the same size have to be configured.
  默认值: 512
  最小值: 1
  最大值: 65535
```

### 43. TcpIpUdpConfig

**描述**: Specifies the configuration parameters of the UDP (User Datagram Protocol) sub-module

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpUdpTtl
  长名称: TTL
  描述: |
    Default Time-to-live value of outgoing UDP packets.
    (This parameter is not used and has no influence on the processing of the module. The default
    TTL can be set for each TcpIpCtrl (IPv4: TcpIpIpDefaultTtl, IPv6: TcpIpIpV6DefaultHopLimit) and
    can be changed during runtime via TcpIp_ChangeParameter() API for each socket.)
  默认值: 64
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: TcpIpUdpTxRetryQueueSize
  长名称: Tx Retry Queue Size
  描述: |
    Total number of UDP Tx Retry Queue elements, the number has to be smaller as or equal to the
    number of EthTxBufTotal.
    This value specifies the number of UDP transmit messages that can be stored in case there is no
    valid resolution of the remote physical address (using ARP or NDP) available.
    A configured value requires an enabled ARP/NDP packet queue.
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 3
  名称: TcpIpUdpPortMin
  长名称: Udp Dynamic Port Min
  描述: If the API TcpIp_Bind() is called on a UDP socket without specified port, the local UDP port
      is chosen as the next free port in the range between TcpIpUdpPortMin and
      TcpIpUdpPortMax.
  默认值: 49152
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: TcpIpUdpPortMax
  长名称: Udp Dynamic Port Max
  描述: If the API TcpIp_Bind() is called on a UDP socket without specified port, the local UDP port
      is chosen as the next free port in the range between TcpIpUdpPortMin and
      TcpIpUdpPortMax.
  默认值: 65535
  最小值: 1
  最大值: 65535
```

### 44. TcpIpUdpTxReqList

**描述**: This container includes configuration parameters of a UDP TX request list that can be attached to a
UDP socket handle via TcpIp_ChangeParameter() during runtime.

A UDP socket only needs a TX request list if a TxConfirmation is required by the upper layer.

Note: A UDP tx request list is shared between all UDP sockets but can only be used for one socket at
a time. If multiple sockets with the same request list size shall be used simultaneously, multiple
request lists of the same size have to be configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpUdpTxReqListSize
  长名称: Tx Req List Size
  描述: This value specifies the maximum number of entries in the UDP TX request list.
  默认值: 1
  最小值: 1
  最大值: 255
```

### 45. TcpIpDuplicateAddressDetectionConfig

**描述**: This container is a subcontainer of TcpIpConfig and configures the DAD callout function.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpDuplicateAddressDetectionHeaderFileName
  长名称: Header File Name
  描述: This parameter specifies the name of the header file containing the definition of the
      duplicate address detection handler function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpDuplicateAddressDetectionCalloutName
  长名称: Handler Name
  描述: This parameter defines the name of the duplicate address detection function
      <Up_DADAddressConflict>.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 46. TcpIpIpSecConfigSet

**描述**: Specifies the IPsec configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpRemoteDeviceNum
  长名称: ''
  描述: Amount of remote clients which will negotiate a Security Association (SA).
  默认值: ''
  最小值: 1
  最大值: ''
- 
  序号: 2
  名称: TcpIpIpSecSpdCalloutFunction
  长名称: IPsec Security Policy Database Callout Function
  描述: This parameter specifies the name of a callout function that shall be called for each Rx/Tx
      messag, after the IPsec has processed all corresponding SPD entries and has determined
      the policy. The callout function allows it to override the applied policy.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpIpSecCalloutHeaderFile
  长名称: IPsec Callout Function Header File
  描述: This parameter specifies the name of the header file containing the definition for the
      functions specified in TcpIpIpSecSpdCalloutFunction and
      TcpIpIpSecAuditEventCalloutFunction.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpIpSecAuditEventCalloutFunction
  长名称: IPsec Auditable Event Callout Function
  描述: |
    This parameter specifies the name of a callout function that will be called for each auditable
    event.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: TcpIpIpSecSaEntryTxActivationTimeout
  长名称: IPsec SA Entry TX Activation Timeout
  描述: |
    The maximum time interval after which an SA entry pair created by vIKE as responder is activated
    for transmission. (For reception, the SA entry is directly activated.)
    If an IPsec packet is received on the SA entry before this timeout expires, then the SA entry is
    also activated for transmission as soon as the packet is processed.
    If this parameter is set to 0, all SA entries are enabled for transmission as soon as they are
    created by vIKE.
  默认值: 2
  最小值: 0
  最大值: 4294967
```

### 47. TcpIpSpdEntry

**描述**: Entry of the Security Policy Database (SPD).

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIpSecPolicy
  长名称: ''
  描述: Policy for usage of IPsec.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpIpSecPriority
  长名称: ''
  描述: Priority of the SPD entry. The processing of entries is based on priority, starting with the
      highest priority "0". The first matching SPD entry defines the policy.
  默认值: 0
  最小值: 0
  最大值: ''
- 
  序号: 3
  名称: TcpIpIpSecHeaderType
  长名称: ''
  描述: Header type speifying the IPsec secutiry mechanism.
  默认值: TCPIP_IPSEC_HDR_AH
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpLocalPortRangeStart
  长名称: ''
  描述: Start value of the local port range.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 5
  名称: TcpIpLocalPortRangeEnd
  长名称: ''
  描述: End value of the local port range.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: TcpIpLocalIpAddrStart
  长名称: ''
  描述: Start value of the local IP address range.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpLocalIpAddrEnd
  长名称: ''
  描述: End value of the remote IP address range.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: TcpIpRemIpAddrStart
  长名称: ''
  描述: Start value of the remote IP address range.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: TcpIpRemIpAddrEnd
  长名称: ''
  描述: End value of the remote IP address range.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: TcpIpRemPortRangeStart
  长名称: ''
  描述: Start value of the remote port range.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 11
  名称: TcpIpRemPortRangeEnd
  长名称: ''
  描述: End value of the remote port range.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 12
  名称: TcpIpProtocol
  长名称: ''
  描述: |
    Relevant IP protocol.
    Note: As specified in IETF Rfc 4301 section 6, ICMP error messages will always be BYPASSed. The
    policy for TCPIP_PROTOCOL_ICMP only applies to ICMP non-error messages. (Echo reply/response).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 48. TcpIpIntegrityAlgorithm

**描述**: Container for configuration of supported integrity algorithm transforms. This container is used to
configure supported
algorithms for AH.
The transform algorithm must be configured in the Crypto module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpIntegrityTransformIdentifier
  长名称: ''
  描述: Integrity algorithm transform identifier. Parameter values are defined as per IETF RFC 7296
      3.3.2
  默认值: TCPIP_IPSEC_TRANSFORM_AUTH_HMAC_SHA2_256_128
  最小值: ''
  最大值: ''
```

### 49. TcpIpIntegrityTransformJobPair

**描述**: Container for storing the CSM integrity transform job references for performing authentication.
Valid for ESP and AH.
Atleast one Integrity transform job pair needs to be configured for each Integrity Algorithm.

该容器没有参数。

### 50. TcpIpEncryptionAlgorithm

**描述**: Container for configuration of supported encryption algorithm transforms. This container is used to
configure supported
algorithms for ESP.
The transform algorithm must be configured in the Crypto module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpEncryptionTransformIdentifier
  长名称: ''
  描述: Encryption algorithm transform identifier. Parameter values are defined as per IETF RFC 7296
      3.3.2
  默认值: TCPIP_IPSEC_TRANSFORM_ENCR_DES
  最小值: ''
  最大值: ''
```

### 51. TcpIpEncryptionTransformJobPair

**描述**: Container for storing the CSM encryption transform job references for performing encryption. Only
valid for ESP.
Atleast one Integrity encryption job pair needs to be configured for each Integrity encrypytion
algorithm.

该容器没有参数。

### 52. TcpIpTlsConfig

**描述**: Specifies the configuration parameters of the TLS (Transport Layer Security) sub module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpTlsMaxConnections
  长名称: ''
  描述: Defines the max. number of TLS connections that can be opened at the same time.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: TcpIpTlsMaxServerInstances
  长名称: ''
  描述: This parameter specifies the maximum number of server instances of a TLS Connection.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: TcpIpTlsUserErrorCalloutFunction
  长名称: Tls User Error Callout Function
  描述: This parameter specifies the name of a callout function that informs an user about occured
      user errors within a TLS connection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpTlsSupportMasterSecretAccess
  长名称: Support Master Secret Access
  描述: |
    Enabling this feature grants access to the TLS master secret via an API.
    
    Warning: This feature has to be disabled for any productive code due to security reasons!
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: TcpIpTlsUserErrorHeaderFile
  长名称: ''
  描述: This parameter specifies the name of the header file containing the definition for the
      functions specified in TcpIp_TlsUserErrorCalloutFunction.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: TcpIpTlsClearBufferAfterHandshake
  长名称: ''
  描述: |
    When set, the TLS RX and TX buffer will be cleared after the succesfull established TLS
    connection (TLS handshake).
    Dependent on the configured TLS buffer sizes, this could affect the perfomance of the TLS
    handshake.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpTlsSupportErrorIndicationCallout
  长名称: ''
  描述: |
    If set to TRUE TLS error indication callout is enabled.The callout contains information about
    the raised error indication and will be triggered directly when the error occurs (e.g. during
    TLS handshake).
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: TcpIpTlsMaxNumDistinguishedNames
  长名称: Tls Max Num Distinguished Names in Certificate Request Message
  描述: The maximum number of distinguished names the client can handle in a received certificate
      request message.
  默认值: 10
  最小值: 1
  最大值: 65535
- 
  序号: 9
  名称: TcpIpTlsMaxNumCertificates
  长名称: ''
  描述: The maximum number of client certificates we support for one certificate chain that should be
      sent.
  默认值: 5
  最小值: 1
  最大值: 65535
- 
  序号: 10
  名称: TcpIpTlsSecretsViaNssFrame
  长名称: ''
  描述: |
    Enabling this feature let the ECU send Handshake- and Trafficsecrets of TLS 1.3 or the
    Mastersecret of TLS 1.2 via a NSS Frame over UDP.
    
    Warning: This feature has to be disabled for any productive code due to security reasons!
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: TcpIpTlsNssFramePortAssignment
  长名称: ''
  描述: |
    Specifies the port that is used for the NSS Key Log Frame in TLS 1.3 and TLS 1.2.
    The configured port specifies the source and destination port.
  默认值: 54321
  最小值: 1
  最大值: 65535
- 
  序号: 12
  名称: TcpIpTlsSupportSecretAccess
  长名称: Support Secret Access
  描述: |
    Enabling this feature grants access to the TLS master secret via an API in TLS 1.2 and to the
    TLS Client/Server- Handshake/Traffic secrets in TLS 1.3.
    
    Warning: This feature has to be disabled for any productive code due to security reasons!
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: TcpIpTlsUseKeyUpdateCallout
  长名称: ''
  描述: |
    Defines if the user is informed about a key update during a TLS connection.
    
    Configure the function name via TcpIpSocketOwnerTlsKeyUpdateName.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: TcpIpTlsMaxPskIdentityLength
  长名称: Tls Session Resumption Max Psk Identity Length
  描述: This parameter specifies the maximum receivable length for the PSK identity (in the RFC8446
      chapter 4.6.1 it is named ticket) in a TLS 1.3 NewSessionTicket.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 15
  名称: TcpIpTlsRejectEarlyDataExtensionInTicket
  长名称: Tls Session Resumption Reject Early Data Extension In Ticket
  描述: If enabled a NewSessionTicket with included early_data extension is rejected / ignored. If
      disabled the extension will just be ignored and the NewSessionTicket (if otherwise
      valid) stored.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: TcpIpTlsMinTicketLifetime
  长名称: Tls Session Resumption Min Ticket Lifetime
  描述: This parameter specifies the minimum lifetime for a session ticket.
  默认值: 20
  最小值: 1
  最大值: 65535
- 
  序号: 17
  名称: TcpIpTlsMaxTicketLifetime
  长名称: Tls Session Resumption Max Ticket Lifetime
  描述: This parameter specifies the maximum lifetime for a session ticket from the time of ticket
      issuance.
  默认值: 86400
  最小值: 1
  最大值: 4294967295
- 
  序号: 18
  名称: TcpIpTlsMaxAcceptanceTicketTime
  长名称: Tls Session Resumption Max Acceptance Ticket Time
  描述: This parameter specifies the maximum acceptance time for a session ticket. The acceptance time
      takes into account the time starting from the handshake of the resumption base
      connection till a ticket is used + the lifetime of that ticket. If the acceptance time
      is larger than the configured maximum acceptance time, the lifetime of the ticket is
      decreased so that the maximum is fullfilled (if possible). If the resumption base
      connection is established longer than the maximum acceptance time, all received tickets
      will be rejected / ignored.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 19
  名称: TcpIpTlsMinRemainingTicketLifetime
  长名称: Tls Session Resumption Min Remaining Ticket Lifetime
  描述: This parameter specifies the minimum remaining lifetime for a session ticket to still be
      processed. Before the ClientHello of the resumed connection is build and its
      calculations are done, it is checked that the corresponding session ticket has enough
      lifetime left.
  默认值: 5
  最小值: 1
  最大值: 65535
- 
  序号: 20
  名称: TcpIpTlsMaxNumSigAlgsInCertReqMsg
  长名称: Tls Max Num Signature Algorithms in Certificate Request Message
  描述: |
    The maximum number of signature algorithms the client can handle in a received certificate
    request message.
    
    TLS 1.2: Limits entries in 'supported_signature_algorithms'
    TLS 1.3: Limits entries in extensions 'signature_algorithms' and 'signature_algorithms_cert'
  默认值: 10
  最小值: 1
  最大值: 65535
```

### 53. TcpIpTlsCiphersuites

**描述**: This container provides the information about supported ciphersuites used by TLS.

该容器没有参数。

### 54. TcpIpTlsCertificateIdentity

**描述**: This container provides information about the certificates used for ciphersuites.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpTlsServerNameIdentification
  长名称: ''
  描述: Defines a server identification name. If present, the name will be added as an extension with
      the "TLS client hello" handshake message. The TLS server will check for the name to
      identify the server certificate.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 55. TcpIpTlsCiphersuiteDefinition

**描述**: This container provides the static information of a ciphersuite used by TLS.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpTlsCiphersuiteId
  长名称: ''
  描述: ID that represents the ciphersuite according to IETF, e.g. RFC4492, Sect. 6, RFC8446, Appendix
      B.4 or RFC5246, Appendix A.5.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: TcpIpTlsCiphersuiteName
  长名称: ''
  描述: Provides a verbal name for the ciphersuite. The name should be the one defined in the
      respective RFC, e.g. TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256 (TLS 1.2) or
      TLS_AES_128_GCM_SHA256 (TLS 1.3)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpTlsCiphersuitePriority
  长名称: ''
  描述: Defines the priority of the cipher. The higher the number the lower the priority.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: TcpIpTlsUseAEADCipher
  长名称: ''
  描述: Specifies if the ciphersuite supports AEAD for data en-/decryption.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: TcpIpTlsUsePresharedKeys
  长名称: ''
  描述: Defines if this ciphersuite uses pre-shared keys. If so, additional configuration or callbacks
      will be used for pre-shared key negotiation.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: TcpIpTlsUseSecurityExtensionForceEncryptThenMac
  长名称: ''
  描述: Defines if the security extension according to IETF RFC 7366 shall be supported. This is
      useful for ciphersuites using CBC mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpTlsVersion
  长名称: ''
  描述: Declares the TLS version that this ciphersuite shall be used for.
  默认值: TLS_VERSION_V12
  最小值: ''
  最大值: ''
```

### 56. TcpIpTlsCiphersuiteWorker

**描述**: This container provides the jobs and keys necessary for TLS data transmission and reception.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpTlsCipherAEADCipherKeyLength
  长名称: ''
  描述: Defines the key length for en- / decryption with authentication data (AEAD).
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: TcpIpTlsCipherEncryptKeyLength
  长名称: ''
  描述: Defines the key length used for en- or decryption. The key length is valid for (symmetric)
      encryption and decryption.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: TcpIpTlsCipherMacKeyLength
  长名称: ''
  描述: Specifies the length of the MAC key
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: TcpIpTlsCiphersuiteWorkerPriority
  长名称: ''
  描述: Global priority of the cipersuite worker. A new TLS connection will use the highest priority
      ciphersuite worker which is referenced by the connection and not yet occupied. (The
      highest priority is "1".)
  默认值: 1
  最小值: 1
  最大值: 65535
```

### 57. TcpIpTlsHandshake

**描述**: This container provides information that is needed to process a handshake. It contains the
appropriate references to jobs and keys of the CSM to perform the key exchange cryptographic for the
ciphersuite and involved certificates.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpTlsCsmPRFSupportType
  长名称: Tls Csm Prf Support Type
  描述: Specifies how the CSM job supports the PRF operation.
  默认值: TLS_PRF_CSM_NO_SUPPORT
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpTlsHsSupportedEllipticCurve
  长名称: ''
  描述: This parameter describes the supported Curve which is used for this handshake. The definition
      is based on the standard RFC8422 "5.1.1.  Supported Elliptic Curves Extension".
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpTlsHsSignatureAlgorithm
  长名称: ''
  描述: |
    This parameter described the signature algorithm pair that must be used with this handshake. The
    definition is based on the standard RFC8422 "5.1.3.  The signature_algorithms Extension and
    EdDSA"
     (for Elliptic Curves) and RFC5246 "7.4.1.4.1.  Signature Algorithms".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 58. TcpIpTls13Config

**描述**: This container provides information that is needed to process a TLS 1.3 handshake. It contains the
appropriate references to jobs and keys of the CSM to perform the key calculation.

该容器没有参数。

### 59. TcpIpTlsPskIdentity

**描述**: This container is used in two ways. For TLS 1.2 it provides information about static definition of
pre-shared keys and is used during the handshake to negotiate pre-shared keys between a client and a
server. In TLS 1.3 for each configured container a NewSessionTicket can be processed and saved if
the configured hash algorithm in the container matches the hash algorithm of the handshake's
ciphersuite. Then a connection can be resumed with the stored NewSessionTicket. When the resumed
connection is closed the container can be used for the next NewSessionTicket.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpTlsPresharedKeyIdentity
  长名称: ''
  描述: This item provides the key identification. The TLS client selects the pre-shared key based on
      the identification hint provided by the server and returns the key identification name
      back to the server.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpTlsPresharedKeyIdentityHint
  长名称: ''
  描述: Provides the identity hint for a pre-shared key. This information is transmitted by the TLS
      Server to provide its identification to the TLS client.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpTlsPskGetClientKeyIdentityFunc
  长名称: ''
  描述: Defines the function name for the Up_TlsClientGetPskIdentity() callback.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpTlsPskGetKeyIdentityHintFunc
  长名称: ''
  描述: Defines the function name for the Up_TlsServerGetPskIdentityHint() callback.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: TcpIpTlsPskGetServerKeyIdentityFunc
  长名称: ''
  描述: Defines the function name for the Up_TlsServerGetPskIdentity () callback.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: TcpIpTlsPskVersion
  长名称: ''
  描述: Defines the TLS version that this PSK identity shall be used for.
  默认值: TLS_VERSION_V12
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpTls13PskHashAlgorithm
  长名称: ''
  描述: This parameter defines the hash algorithm for which this PSK identity can be used in TLS 1.3.
      The referenced CSM jobs in this identity must be configured for this algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 60. TcpIpTlsConnection

**描述**: This container defines the properties of a TLS connection

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpTlsConnectionGetTimeFunc
  长名称: ''
  描述: Defines the function name for the Up_TlsGetCurrentTimeStamp() callback.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpTlsConnectionId
  长名称: ''
  描述: Identifier of the connection. The set of configured identifiers shall be consecutive and
      gapless.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: TcpIpTlsConnectionType
  长名称: ''
  描述: Specifies if the TLS connection is a server or a client.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpTlsMaxFragmentLength
  长名称: ''
  描述: |
    Specifies the max length in bytes of a TLS fragment that is sent as a block.
    
    Note: This parameter is automatically set to the available TLS RxBuffer size. If the TLS Record
    Size Limit Extension (RFC8449) is enabled, this parameter is offered to the peer during the TLS
    handshake.
  默认值: 16384
  最小值: 1
  最大值: 16384
- 
  序号: 5
  名称: TcpIpTlsPortAssignment
  长名称: ''
  描述: |
    Specifies the port address that is used for TLS communication.
    For TLS server connections, the configured port specifies the local port of the connection.
    For TLS client connections, the configured port specifies the remote port of the connection.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: TcpIpTlsUseClientAuthenticationRequest
  长名称: ''
  描述: Defines if client authentication shall be applied for this TLS connection.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpTlsUseSecurityExtensionRecordSizeLimit
  长名称: ''
  描述: |
    Defines if the security extension for max_fragment_length shall be supported as defined in IETF
    RFC 8449, chapter 4.1.
    
    Note:
    Endpoints SHOULD advertise the "record_size_limit" extension, even if they have no need to limit
    the size of records. For clients, this allows servers to advertise a limit at their discretion.
    For servers, this allows clients to know that their limit will be respected.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: TcpIpTlsUserErrorBufferEntries
  长名称: ''
  描述: Number of maximum stored user entries wihtin the user error buffer
  默认值: 10
  最小值: 1
  最大值: 100
- 
  序号: 9
  名称: TcpIpTlsUseExtensionTrustedCaIndication
  长名称: ''
  描述: |
    Defines if the extension for trusted CA indication shall be supported as defined in IETF RFC
    6066 chapter 6
    
    All root certificates (KeyMCertificateGroupIssuerRef) must be configured with an corresponding
    CSM hash job (KeyMCertCsmHashJobRef).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: TcpIpTlsUseExtensionCertificateStatusRequest
  长名称: ''
  描述: |
    Defines if the extension for certificate status requests shall be supported as defined in IETF
    RFC 6066 chapter 8.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: TcpIpTlsIncludeRootCertificate
  长名称: ''
  描述: |
    Include the root certificate into the certificate message (part of the TLS handshake) if a root
    certificate is configured and availbale.
    For TLS server connections, this parameter must be configured equally for all connections
    belonging to the same group of server connections.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: TcpIpTlsUseChangeableCipherCallback
  长名称: ''
  描述: Defines if the user can change the order of the cipher suites and/or signature algorimthms
      during runtime for this TLS connection.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: TcpIpTlsUseMiddleboxCompatibilityMode
  长名称: ''
  描述: Defines if in the connection the middlebox compatibility mode as defined in IETF RFC 8466
      appendix D.4 is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: TcpIpTlsMaxSizeDistinguishedNames
  长名称: ''
  描述: The maximum size (in bytes) of one distinguished name (BER encoded) sent in the
      certificate_authorities extension for TLS 1.3. The extension then contains one
      destingished name per referenced root certificate for this connection.
  默认值: 500
  最小值: 1
  最大值: 16384
- 
  序号: 15
  名称: TcpIpTlsResumptionBaseConnectionId
  长名称: ''
  描述: Id of the resumption base connection where the TLS 1.3 handshake with certificates was
      performed and from which this connection can be resumed.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 61. TcpIpTlsBufferConfig

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpTlsHsRxBufferSize
  长名称: Tls Handshake Rx Buffer Size
  描述: Required TLS handshake RX buffer size.
  默认值: 2500
  最小值: 0
  最大值: 4294967294
- 
  序号: 2
  名称: TcpIpTlsHsTxBufferSize
  长名称: Tls Handshake Tx Buffer Size
  描述: Required TLS handshake TX buffer size.
  默认值: 2500
  最小值: 0
  最大值: 4294967294
- 
  序号: 3
  名称: TcpIpTlsAdRxBufferSize
  长名称: Tls Application Data Rx Buffer Size
  描述: Required TLS application data (plaintext) RX buffer size.
  默认值: 1500
  最小值: 0
  最大值: 4294967294
- 
  序号: 4
  名称: TcpIpTlsAdTxBufferSize
  长名称: Tls Application Data Tx Buffer Size
  描述: Required TLS application data (plaintext) TX buffer size.
  默认值: 1500
  最小值: 0
  最大值: 4294967294
```

### 62. TcpIpTlsConnectionGroup

**描述**: This optional container is used to collect all TlsConnections that belong to a TlsConnectionGroup.
The intention of a TLS connection group is to share resources among TLS connections collected in a
group, because only one connection of a group can be used at a time.

该容器没有参数。

### 63. TcpIpGeneral

**描述**: This container is a subcontainer of TcpIp and specifies the general configuration parameters of the
TCP/IP stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpBufferMemory
  长名称: ''
  描述: Memory size in bytes reserved for TCP/IP buffers.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: TcpIpDevErrorDetect
  长名称: ''
  描述: If true then TCP/IP will enable the error-reporting to the Development Error Tracer (DET).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpDhcpServerEnabled
  长名称: DHCP Server Enabled
  描述: Enables (TRUE) or disables (FALSE) the DHCPv4 (Dynamic Host Configuration Protocol) Server.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpMainFunctionPeriod
  长名称: MainFunction Period
  描述: Period of TcpIp_MainFunction.
  默认值: 0.005
  最小值: 0.001
  最大值: 1000
- 
  序号: 5
  名称: TcpIpResetIpAssignmentApi
  长名称: Reset IP Assignment Api
  描述: |
    Enables/disables the API TcpIp_ResetIpAssignment of a DHCP-client.
    
    (This parameter is currently not used and does not affect the functionality of the module.)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: TcpIpScalabilityClass
  长名称: ''
  描述: In order to customize the TcpIp Stack to the specific needs of the user it can be scaled
      according to the scalability classes.
  默认值: SC1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpTcpEnabled
  长名称: TCP Enabled
  描述: Enables (TRUE) or disabled (FALSE) support of TCP (Transmission Control Protocol).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: TcpIpTcpSocketMax
  长名称: TCP Socket Max
  描述: Maximum number of TCP sockets
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 9
  名称: TcpIpUdpEnabled
  长名称: UDP Enabled
  描述: Enables (TRUE) or disabled (FALSE) support of UDP (User Datagram Protocol)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: TcpIpUdpSocketMax
  长名称: UDP Socket Max
  描述: Maximum number of UDP sockets.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 11
  名称: TcpIpVersionInfoApi
  长名称: ''
  描述: If true the TcpIp_GetVersionInfo API is available.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: TcpIpUserConfigFile
  长名称: User Config File
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
  序号: 13
  名称: TcpIpRandNoFct
  长名称: Random Number Function
  描述: This parameter defines the function called for the random number generation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: TcpIpRandNoFctIncludeFile
  长名称: Random Function Include File
  描述: This parameter defines the header file holding the declaration of the random number generation
      function defined in 'TcpIpRandNoFct'.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: TcpIpDiagExtensionsEnabled
  长名称: ''
  描述: |
    Enable diagnostic read access to several parameters. For some parameters read access has to be
    enabled separately.
    
    Read features can be located at TcpIp_General or at the different sub-components.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: TcpIpLowerLayerName
  长名称: Lower Layer Name
  描述: |
    This parameter defines the name of TcpIp's lower layer.
    According to AUTOSAR this is the EthIf module.
    This parameter should only be changed if there is a special CDD between EthIf and the TcpIp
    module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: TcpIpMainFunctionSplitEnabled
  长名称: MainFunction Splitting Enabled
  描述: |
    This parameter specifies whether the TcpIp_MainFunction shall be split-up into three functions.
    This allows optimizing the reception and transmission path of upper layer data for a specific
    use case.
    
    TcpIp_MainFunctionRx - Handles reception of data and forwards it to upper-layer.
    TcpIp_MainFunctionState - Handles module state changes and transmits data of internal protocols
    (e.g DHCP and ARP/NDP messages).
    TcpIp_MainFunctionTx - Handles transmission requests of upper-layer and transmits data.
    
    Note: All TcpIp MainFunctions must be called from the same task or at least from tasks that do
    not interrupt each other.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: TcpIpSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: TcpIpGetDhcpStatusApi
  长名称: ''
  描述: |
    Enables/disables the APIs TcpIp_DhcpV4_GetStatus (in case IPv4 is enabled) and
    TcpIp_DhcpV6_GetStatus (in case IPv6 is enabled) of a DHCP-client.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: TcpIpIpSecEnabled
  长名称: IPsec Enabled
  描述: Enables (TRUE) or disables (FALSE) support of IPsec (Internet Protocol Security).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: TcpIpGetAndResetMeasurementDataApi
  长名称: ''
  描述: Enables / Disables the Get and Reset Measurement Data API
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: TcpIpAsrTlsEnabled
  长名称: ''
  描述: Enables support for AUTOSAR TLS functionality.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: TcpIpMultiCoreSupportEnabled
  长名称: ''
  描述: |
    Enable support for MultiCore operation of TcpIp
    Default value FALSE
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: TcpIpCsmAccessIndirectionPrefix
  长名称: ''
  描述: |
    This parameter allows the user to configure TcpIp to use a different CSM stack. All CSM APIs are
    expected to be defined
    in the format <CSM prefix value>_Function.
    Special characters are not allowed.
    
    By default the prefix "Csm" shall be used.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: TcpIpAdditionalIncludeFiles
  长名称: ''
  描述: This parameter defines additional needed header files.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: TcpIpEnableSecurityEventReporting
  长名称: ''
  描述: Switches the reporting of security events to the IdsM:
  默认值: false
  最小值: ''
  最大值: ''
```

### 64. TcpIpIpV4General

**描述**: This container is a subcontainer of TcpIp and specifies the general configuration parameters of the
TCP/IP stack for IPv4

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpArpEnabled
  长名称: ARP Enabled
  描述: Enables (TRUE) or disables (FALSE) support of ARP (Address Resolution Protocol).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpAutoIpEnabled
  长名称: AutoIp Enabled
  描述: Enables (TRUE) or disables (FALSE) the Auto-IP (automatic private IP addressing) sub-module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpDhcpClientEnabled
  长名称: DHCP Client Enabled
  描述: Enables (TRUE) or disables (FALSE) the DHCP (Dynamic Host Configuration Protocol) Client.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpIcmpEnabled
  长名称: ICMP Enabled
  描述: Enables (TRUE) or disabled (FALSE) support of ICMP (Internet Control Message Protocol).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: TcpIpIpV4Enabled
  长名称: IPv4 Enabled
  描述: Enables (TRUE) or disables (FALSE) support of IPv4 (Internet Protocol version 4).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: TcpIpLocalAddrIpv4EntriesMax
  长名称: Local Addr IPv4 Entries Max
  描述: Maximum number of LocalAddr table entries for IPv4.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: TcpIpPathMtuDiscoveryEnabled
  长名称: Path MTU Discovery Enabled
  描述: |
    Enables (TRUE) or disables (FALSE) the discovery of the maximum transmission unit on a path
    according to IETF RfC 1191.
    
    (This parameter is currently not used and does not affect the functionality of the module.)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: TcpIpIpV4EthIfUpdatePhysAddrFilterApiEnabled
  长名称: IPv4 EthIf Update Phys Addr Filter Api Enabled
  描述: |
    This parameter defines whether the IPv4 will call EthIf_SetPhysAddrFilter() in order to
    configure the ethernet group address Rx filter.
    
    If the controller is in promiscuous mode or statically configured to accept all neccessary
    multicasts, this parameter can be disabled in order to avoid superfluous calls to the EthIf API.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: TcpIpArpDiscardedEntryHandling
  长名称: ''
  描述: |
    Enables (TRUE): In case the table is full, new entries are discarded and this fact is indicated
    by the callback function configured in TcpIpPhysAddrChgDiscardedEntryHandlerName with the IP of
    the discarded entry.
    Disables (FALSE): In case the table is full, the new entry overwrites the oldest entry and this
    fact is indicated by the callback function configured in
    TcpIpPhysAddrChgDiscardedEntryHandlerName with the IP of the old entry.
  默认值: false
  最小值: ''
  最大值: ''
```

### 65. TcpIpIpV6General

**描述**: This container is a subcontainer of TcpIp and specifies the general configuration parameters of the
TCP/IP stack for IPv6.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpDhcpV6ClientEnabled
  长名称: DHCPv6 Client Enabled
  描述: Enables (TRUE) or disables (FALSE) the DHCPv6 (Dynamic Host Configuration Protocol for IPv6)
      Client.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TcpIpIpV6Enabled
  长名称: IPv6 Enabled
  描述: Enables (TRUE) or disables (FALSE) support of IPv6 (Internet Protocol version 6).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TcpIpIpV6PathMtuDiscoveryEnabled
  长名称: IPv6 Path Mtu Discovery Enabled
  描述: Enables (TRUE) or disables (FALSE) Path MTU Discovery support for IPv6 according to IETF RFC
      1981.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TcpIpLocalAddrIpv6EntriesMax
  长名称: Local Addr IPv6 Entries Max
  描述: Maximum number of LocalAddr table entries for IPv6.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: TcpIpNdpAddressResolutionUnrechabilityDetectionEnabled
  长名称: NDP Address Resolution Unrechability Detection Enabled
  描述: Enables (TRUE) or disables (FALSE) support of Address Resoultion and Neighbor Unreachability
      Detetion via NDP.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: TcpIpNdpPrefixAndRouterDiscoveryEnabled
  长名称: NDP Prefix And Router Discovery Enabled
  描述: Enables (TRUE) or disables (FALSE) support of Prefix and Router Discovery via NDP.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpIpV6EthIfUpdatePhysAddrFilterApiEnabled
  长名称: IPv6 EthIf Update Phys Addr Filter Api Enabled
  描述: |
    This parameter defines whether the IPv6 will call EthIf_SetPhysAddrFilter() in order to
    configure the ethernet group address Rx filter.
    
    Since the IPv6 Neighbor Discovery Protocol uses ethernet link-layer multicasts, the controller
    must be configured to accept received ethernet multicast IPv6 packets.
    
    If the controller is in promiscuous mode or statically configured to accept all neccessary
    multicasts, this parameter can be disabled in order to avoid superfluous calls to the EthIf API.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: TcpIpIpV6SetTrafficClassAndFlowLabelApiEnabled
  长名称: IPv6 Set Traffic Class And Flow Label Api Enabled
  描述: |
    This parameter defines whether the IPv6 provides the IpV6_SetTrafficClass() and
    IpV6_SetFlowLabel() APIs to change the Traffic Class octet of the IPv6 header for outgoing
    packets.
    
    If enabled the value can be set on a per-socket basis during runtime.
    The default values for the Traffic Class and the Flow Label for all outgoing packets are
    controller specific and are configured by the IpV6DefaultTrafficClass and IpV6DefaultFlowLabel
    parameters.
    
    [RFC2460 3. IPv6 Header Format]
    [RFC2460 7. Traffic Classes]
    
    see also [RFC2474 3. Differentiated Services Field Definition]
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: TcpIpIpV6ExtendedDestAddrValidationEnabled
  长名称: IPv6 Extended Dest Addr Validation Enabled
  描述: |
    This parameter defines whether the IPv6 will check the destination address every time
    IpV6_ProvideTxBuffer() is called.
    If disabled the user should call IpV6_IsValidDestinationAddr() before IpV6_ProvideTxBuffer() is
    called the first time with a specific destination address.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: TcpIpIpV6CacheLookupOptimizationEnabled
  长名称: IPv6 Cache Lookup Optimization Enabled
  描述: |
    This parameter defines whether lookups in internal IPv6 data structures shall be optimized.
    
    If enabled the last lookup result is stored and reused for the next lookup.
    Disabling this feature will save some bytes in RAM and ROM but reduce performance.
  默认值: true
  最小值: ''
  最大值: ''
```

### 66. TcpIpGeneration

**描述**: Contains the generation configuration parameters of the module TcpIp. Please refer to the parameter
description and to the TechnicalReference_CommonAsr_ComStackLib which is part of the delivery for
more information. Please note that there are customizations which are only valid for a specific
quality level (e.g. during the development phase).

#### 参数列表

```yaml
- 
  序号: 1
  名称: TcpIpOutOfBoundsWriteProtectionStrategy
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
  名称: TcpIpOutOfBoundsWriteSanitizer
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
  名称: TcpIpOutOfBoundsReadSanitizer
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
  名称: TcpIpReduceConstantData2Define
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
  名称: TcpIpBoolDataInArrayOfStructStrategy
  长名称: ''
  描述: |
    This parameter is used to tailor the usage of boolean data in structures in all CONFIG-CLASSES
    ROM data. The difference between BITFIELD and BITMASKING depends on your compiler options and
    memory mapping.
    
    BOOLEAN: the datatype of boolean data is native boolean.
    BITFIELD: the bitfield type is used and the compiler extracts the boolean data from structures.
    BITMASKING: generated masks are used to extract the boolean data from structures.
  默认值: BITMASKING
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: TcpIpDeduplicateIndirectedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress 0:N relational ROM data in all
    CONFIG-CLASSES without increasing the runtime.
    
    FALSE: 0:N relational ROM data is not compressed.
    TRUE: 0:N relational ROM data is compressed without increasing the runtime.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: TcpIpDataDeduplicationStrategy
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
  名称: TcpIpReduceBoolDataByNegationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using the negation operator.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 9
  名称: TcpIpReduceBoolDataByNumericalComparisonThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using numerical comparison with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 10
  名称: TcpIpReduceBoolDataByNumericalRelationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using relational comparison with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 11
  名称: TcpIpReduceBoolDataByNumericalOperandStrategy
  长名称: ''
  描述: |
    This parameter is used to taylor the CONFIG-CLASS PRE-COMPILE ROM bool data with number
    deduplication mechanisms. A comparison with 0 is very efficient, but a numerical comparison with
    a value not 0 can be used to increase the ROM data compression rate.
    
    NONE: ROM data deduplications are switched off.
    DEDUPLICATE_DATA_WITH_ZERO: ROM data deduplications can be applied with the value 0.
    DEDUPLICATE_DATA_WITH_ANY_VALUE: ROM data deduplications can be applied with any numerical
    value.
  默认值: DEDUPLICATE_DATA_WITH_ANY_VALUE
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: TcpIpReduceNumericalDataByOffsetThreshold
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
  名称: TcpIpReduceNumericalDataByArraySubtractionThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS
    PRE-COMPILE ROM data by using a subtraction with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 14
  名称: TcpIpReduceDataByStreaming
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
  名称: TcpIpShortSymbols
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
  名称: TcpIpInterfacesForDeactivatedData
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
  名称: TcpIpReferringKeysInComments
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

### 67. TcpIpSecurityEventRefs

**描述**: Container for the references to IdsMEvent elements representing the security events that the TcpIp
module shall report to the IdsM in case the coresponding security related event occurs (and if
TcpIpEnableSecurityEventReporting is set to "true"). The standardized security events in this
container can be extended by vendor-specific security events.

该容器没有参数。

