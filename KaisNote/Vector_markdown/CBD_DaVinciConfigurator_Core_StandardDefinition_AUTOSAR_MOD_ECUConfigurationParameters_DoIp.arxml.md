# DoIP

## 模块描述

Configuration of the DoIP (Diagnostic over IP) module.

## 容器列表

### 1. DoIPConfigSet

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR DoIP module.
This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist
once per configuration set.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPEid
  长名称: ''
  描述: Configured EID (Entity ID of) for vehicle identification/vehicle announcement. Only necessary
      if DoIPUseMacAddressForIdentification is set to FALSE.
  默认值: ''
  最小值: 1
  最大值: 281474976710656
- 
  序号: 2
  名称: DoIPGid
  长名称: ''
  描述: Configured GID (Group ID of) for vehicle identification/vehicle announcement.
  默认值: ''
  最小值: 1
  最大值: 281474976710656
- 
  序号: 3
  名称: DoIPLogicalAddress
  长名称: ''
  描述: Describes the logical address of the DoIP entity, i.e. the SA that will route diagnostic
      requests to the Dcm of the DoIP entity.
  默认值: ''
  最小值: 1
  最大值: 65535
```

### 2. DoIPInterface

**描述**: This container defines a logical IP interface and collects properties to configure this interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPAliveCheckResponseTimeout
  长名称: ''
  描述: Timeout  in [s] for waiting for a response to an Alive Check request before the connection is
      considered to be disconnected. Represents parameter T_TCP_AliveCheck of ISO
      13400-2:2012.
  默认值: ''
  最小值: 0
  最大值: INF
- 
  序号: 2
  名称: DoIPGeneralInactivityTime
  长名称: ''
  描述: Timeout in [s] for maximum inactivity of a TCP socket connection before the DoIP module will
      close the according socket connection. Represents parameter T_TCP_General_Inactivity of
      ISO 13400-2:2012
  默认值: ''
  最小值: 0
  最大值: INF
- 
  序号: 3
  名称: DoIPInitialInactivityTime
  长名称: ''
  描述: Timeout in [s] used for initial inactivity of a connected TCP socket connection directly after
      socket connection. Represents parameter T_TCP_Initial_Inactivity of ISO 13400-2:2012
  默认值: ''
  最小值: 0
  最大值: INF
- 
  序号: 4
  名称: DoIPInitialVehicleAnnouncementTime
  长名称: ''
  描述: Time to wait in [s] for sending first vehicle anouncement message after IP address assignment.
      Represents parameter A_DoIP_Announce_Wait of ISO 13400-2:2012
  默认值: ''
  最小值: 0
  最大值: INF
- 
  序号: 5
  名称: DoIPInterfaceActLineCtrl
  长名称: ''
  描述: This attribute defines whether the network interface
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DoIPInterfaceAnnouncementStart
  长名称: ''
  描述: This attribute defines, when vehicle announcement is started on a DoIPInterface
  默认值: DOIP_AUTOMATIC_ANNOUNCE
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DoIPInterfaceId
  长名称: ''
  描述: This parameter is an identifier of the DoIPInterface. The value of this parameter will be
      assigned to the symbolic name derived from the container short name.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: DoIPMaxTesterConnections
  长名称: ''
  描述: Maximum amount of tester connections that shall be maintained at one time before alive check
      is performed.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 9
  名称: DoIPUseMacAddressForIdentification
  长名称: ''
  描述: Provided the information if a configured EID at vehicle identification response/vehicle
      announment is used or the MAC address.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DoIPUseVehicleIdentificationSyncStatus
  长名称: ''
  描述: Defines if the optional VIN/GID synchronization status is used additionally in the vehicle
      identification/announcement.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DoIPVehicleAnnouncementCount
  长名称: ''
  描述: Number of vehicle announcement messages on IP address assignment. Represents parameter
      A_DoIP_Announce_Num of ISO 13400-2:2012.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 12
  名称: DoIPVehicleAnnouncementInterval
  长名称: ''
  描述: Time to wait in [s] for sending subsequent vehicle anouncement messages. Represents parameter
      A_DoIP_Announce_Interval of ISO 13400-2:2012
  默认值: ''
  最小值: 0
  最大值: INF
```

### 3. DoIPChannel

**描述**: Configuration of one DoIPChannel.

该容器没有参数。

### 4. DoIPPduRRxPdu

**描述**: This container contains the Rx Pdus to connect with the Rx Pdus of the PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPPduRRxPduId
  长名称: ''
  描述: The DoIPPduRRxPduId is required by the API call DoIP_TpCancelReceive.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 5. DoIPPduRTxPdu

**描述**: This container contains the Tx Pdus to connect with the Tx Pdus of the PduR.  If the parameter is
not configured the channel is for functional addressing.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPPduRTxPduId
  长名称: ''
  描述: The DoIPPduRTxPduId is required by DoIP_TpTransmit or DoIP_IfTransmit and
      DoIP_TpCancelTransmit.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DoIPPduType
  长名称: ''
  描述: API Type to use for communication with PduR. DOIP_IFPDU for UUDT messages, DOIP_TPPDU for all
      other diagnostic messages.
  默认值: DOIP_TPPDU
  最小值: ''
  最大值: ''
```

### 6. DoIPConnections

**描述**: Container contains all lower layer connection specific information, i.e. the single Pdu References
and Handle IDs to the SoAd.

该容器没有参数。

### 7. DoIPTargetAddress

**描述**: This container describes a possible TargetAddress that is supported by DoIP.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPTargetAddressValue
  长名称: ''
  描述: Valid Target Address of a DoIP target address.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 8. DoIPTcpConnection

**描述**: This container describes a TCP connection to the lower layer SoAd module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPRequestAddressAssignment
  长名称: ''
  描述: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment()
      for the TcpIpLocalAddr related to this DoIpConnection.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DoIPTcpConnectionSecurityRequired
  长名称: ''
  描述: Indicates if the associated TCP socket uses a secure connection (e.g. TLS)
  默认值: false
  最小值: ''
  最大值: ''
```

### 9. DoIPSoAdTcpRxPdu

**描述**: This container describes a Rx PDU received via SoAd over TCP

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPSoAdTcpRxPduId
  长名称: ''
  描述: The DoIPSoAdTcpRxPduId is required by the API call DoIP_SoAdTpRxIndication to receive I-PDUs
      from the SoAd.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 10. DoIPSoAdTcpTxPdu

**描述**: This container describes a Tx PDU sent via SoAd over TCP

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPSoAdTcpTxPduId
  长名称: ''
  描述: The DoIPSoAdTcpTxPduId is required by the API call DoIP_SoAdTpTxConfirmation that is called by
      the SoAd to confirm that the IPdu has been transmitted successfully.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 11. DoIPUdpConnection

**描述**: This Container describes a Udp connection to the lower layer SoAd module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPRequestAddressAssignment
  长名称: ''
  描述: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment()
      for the TcpIpLocalAddr related to this DoIpConnection.
  默认值: true
  最小值: ''
  最大值: ''
```

### 12. DoIPSoAdUdpRxPdu

**描述**: This container describes a Rx PDU received via SoAd over UDP.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPSoAdUdpRxPduId
  长名称: ''
  描述: The DoIPSoAdUdpRxPduId is required by the API call DoIP_SoAdIfRxIndication to receive I-PDUs
      from the SoAd.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 13. DoIPSoAdUdpTxPdu

**描述**: This container describes a Tx PDU sent via SoAd over UDP.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPSoAdUdpTxPduId
  长名称: ''
  描述: The DoIPSoAdUdpTxPduId is required by the API call DoIP_SoAdIfTxConfirmation that is called by
      the SoAd to confirm that the IPdu has been transmitted successfully.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 14. DoIPUdpVehicleAnnouncementConnection

**描述**: This container describes the UDP multicast connections to the lower layer SoAd module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPRequestAddressAssignment
  长名称: ''
  描述: The DoIP module shall request IP address assignment by calling SoAd_RequestIpAddrAssignment()
      for the TcpIpLocalAddr related to this DoIpConnection.
  默认值: true
  最小值: ''
  最大值: ''
```

### 15. DoIPSoAdUdpVehicleAnnouncementTxPdu

**描述**: This container describes the vehicle announcement TxPdu sent via the SoAd.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPSoAdUdpVehicleAnnouncementTxPduId
  长名称: ''
  描述: The DoIPSoAdUdpVehicleAnnouncementTxPduId is required by the API call
      DoIP_SoAdIfTxConfirmation() that is called by the SoAd to confirm that the IPdu has been
      transmitted successfully.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 16. DoIPFurtherActionByteCallback

**描述**: This container describes the Callbackfunction to get the Further Action byte. This container shall
always be present. If the DoIPFurtherActionByteDirect parameter is not present, the DoIP module will
use an RPort of ServiceInterface CallbackGetFurtherActionByte with the name
"CBGetFurtherActionByte_<shortname of enclosing DoIPInterface container>".

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPFurtherActionByteDirect
  长名称: ''
  描述: Direct C Callback function to get the OEM specific Further Action Byte for the DoIP vehicle
      identification response/vehicle announcement. If the DoIPFurtherActionByteDirect
      parameter is present, the DoIP module will not use an RPort of ServiceInterface
      "CBGetFurtherActionByte" but will call the configured function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 17. DoIPRoutingActivation

**描述**: This container describes the routing activation possibilities by representing for each container a
possible routing activation request message to the DoIP entity and the according references to the
activated diagnostic messages.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPRoutingActivationNumber
  长名称: ''
  描述: Identifies the Routing activation Number which is received for a DoIP routing activation
      request message.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DoIPRoutingActivationSecurityRequired
  长名称: ''
  描述: Indicates if a routing activation requires a secure TCP connection
  默认值: false
  最小值: ''
  最大值: ''
```

### 18. DoIPRoutingActivationAuthenticationCallback

**描述**: Container describes the Callbackfunction to call on a Routing Activation Request for Authentication.
If this container is configured but the DoIPRoutingActivationAuthenticationFunc parameter is not
present, the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation
with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the
DoIPRoutingActiviation container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPRoutingActivationAuthenticationFunc
  长名称: ''
  描述: Direct C Callback function to trigger the authentication function for routing activation. If
      the DoIPRoutingActivationAuthenticationFunc parameter is present, the DoIP module will
      not use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the
      configured function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DoIPRoutingActivationAuthenticationReqLength
  长名称: ''
  描述: Describes the amount of bytes used to handle to the authentication function on routing
      activation. If 0 is configured as length the parameter AuthenticationReqData will not be
      handled to the API.
  默认值: ''
  最小值: 0
  最大值: 4
- 
  序号: 3
  名称: DoIPRoutingActivationAuthenticationResLength
  长名称: ''
  描述: Describes the amount of bytes used to read by the authentication function on routing
      activation. If 0 is configured as length the parameter AuthenticationResData will not be
      fetched via the API.
  默认值: ''
  最小值: 0
  最大值: 4
```

### 19. DoIPRoutingActivationConfirmationCallback

**描述**: Container describes the Callbackfunction to call on a Routing Activation Request for Confirmation.
If this container is configured but the DoIPRoutingActivationConfirmationFunc parameter is not
present the DoIP module will use an RPort of ServiceInterface <RoutingActivation>_RoutingActivation
with the name "CB<RoutingActivation>RoutingActivation". <RoutingActivation> is the ShortName of the
DoIPRoutingActiviation container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPRoutingActivationConfirmationFunc
  长名称: ''
  描述: Direct C Callback function to trigger the confirmation function for routing activation. If the
      DoIPRoutingActivationConfirmationFunc parameter is present the DoIP module will not use
      an RPort of ServiceInterface <RoutingActivation>_RoutingActivation but call the
      configured function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DoIPRoutingActivationConfirmationReqLength
  长名称: ''
  描述: Describes the amount of bytes used to handle to the confirmation function on routing
      activation. If 0 is configured as length the parameter ConfirmedReqData will not be
      handled to the API.
  默认值: ''
  最小值: 0
  最大值: 4
- 
  序号: 3
  名称: DoIPRoutingActivationConfirmationResLength
  长名称: ''
  描述: Describes the amount of bytes used to read by the confirmation function on routing activation.
      If 0 is configured as length the parameter ConfirmedResData will not be fetched via the
      API.
  默认值: ''
  最小值: 0
  最大值: 4
```

### 20. DoIPTester

**描述**: This container describes the properties of the possible connectable Tester for the DoIP entity.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPNumByteDiagAckNack
  长名称: ''
  描述: Specifies the number of original Diagnostic request bytes the DoIP entity responses on a NACK
      of a diagnostic response message to the Tester.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: DoIPTesterSA
  长名称: ''
  描述: Source Address of the Tester sent via routing activation or diagnostic message.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 21. DoIPGeneral

**描述**: This container specifies the general configuration parameters of the DoIP module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPAliveCheckResponseTimeout
  长名称: ''
  描述: Timeout  in [s] for waiting for a response to an Alive Check request before the connection is
      considered to be disconnected. Represents parameter T_TCP_AliveCheck of ISO
      13400-2:2012.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: DoIPDevelopmentErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling development error detection support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DoIPDhcpOptionVinUse
  长名称: ''
  描述: If DoIPDhcpOptionVinUse is set to true the DoIP module will add the VIN to the Dhcp host name
      if no valid Dhcp host name is already set.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DoIPEntityStatusMaxByteFieldUse
  长名称: ''
  描述: This parameter is used to distinguish the optional support of the Max data size element of a
      diagnostic entity status response.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DoIPGIDInvalidityPattern
  长名称: ''
  描述: Specifies the Byte pattern that is used for response messages if no valid GID could be
      retrieved.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: DoIPGeneralInactivityTime
  长名称: ''
  描述: Timeout in [s] for maximum inactivity of a TCP socket connection before the DoIP module will
      close the according socket connection. Represents parameter T_TCP_General_Inactivity of
      ISO 13400-2:2012
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 7
  名称: DoIPHeaderFileInclusion
  长名称: ''
  描述: Name of the header file(s) to be included by the DoIP module containing the used C-callback
      declarations.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DoIPInitialInactivityTime
  长名称: ''
  描述: Timeout in [s] used for initial inactivity of a connected TCP socket connection directly after
      socket connection. Represents parameter T_TCP_Initial_Inactivity of ISO 13400-2:2012
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 9
  名称: DoIPInitialVehicleAnnouncementTime
  长名称: ''
  描述: Time to wait in [s] for sending first vehicle anouncement message after IP address assignment.
      Represents parameter A_DoIP_Announce_Wait of ISO 13400-2:2012
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 10
  名称: DoIPMainFunctionPeriod
  长名称: ''
  描述: Determines the frequency at which the DoIP_MainFunction() is called in [s].
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 11
  名称: DoIPMaxRequestBytes
  长名称: ''
  描述: Specifies the maximum allowed bytes of a DoIP message request without the DoIP header.
  默认值: ''
  最小值: 1
  最大值: 18446744073709551615
- 
  序号: 12
  名称: DoIPMaxTesterConnections
  长名称: ''
  描述: Maximum ammount of tester connections that shall be maintained at one time before alive check
      is performed.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 13
  名称: DoIPNodeType
  长名称: ''
  描述: Describes the Type of the DoIP node.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: DoIPUseEIDasGID
  长名称: ''
  描述: Specifies if the DoIP entity shall use its EID if it is the Master for vehicle identification
      gid on the vehicle identification/vehicle announcement.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: DoIPUseMacAddressForIdentification
  长名称: ''
  描述: Provided the information if a configured EID at vehicle identification response/vehicle
      announment is used or the MAC address.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: DoIPUseVehicleIdentificationSyncStatus
  长名称: ''
  描述: Defines if the optional VIN/GID synchronization status is used additionally in the vehicle
      identification/announcement.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: DoIPVehicleAnnouncementInterval
  长名称: ''
  描述: Time to wait in [s] for sending subsequent vehicle anouncement messages. Represents parameter
      A_DoIP_Announce_Interval of ISO 13400-2:2012
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 18
  名称: DoIPVehicleAnnouncementRepetition
  长名称: ''
  描述: Amount of repetitions of the vehicle announcement message on IP address assignment. Represents
      parameter A_DoIP_Annunce_Num of ISO 13400-2:2012
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 19
  名称: DoIPVersionInfoApi
  长名称: ''
  描述: Activates the DoIP_GetVersionInfo() API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: DoIPVinGidMaster
  长名称: ''
  描述: Specifies if the DoIP entity is the Vehicle identification Master for the GID (Group ID).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: DoIPVinInvalidityPattern
  长名称: ''
  描述: Specifies the Byte pattern that is used for response messages if no valid VIN could be
      retrieved.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 22. DoIPGetGid

**描述**: This container describes the Callbackfunction to get the GID.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPGetGID
  长名称: ''
  描述: Direct C Callback function to get the GID of the DoIP entity. If the DoIPGetGID parameter is
      present, the DoIP module will not use an RPort of ServiceInterface CallbackGetGID but
      call the configured function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 23. DoIPPowerModeCallback

**描述**: This container describes the Callbackfunction to get the Power Mode. This container shall always be
present.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPPowerMode
  长名称: ''
  描述: Direct C Callback function to get the Power Mode of the DoIP entity. If the DoIPPowerMode
      parameter is present, the DoIP module will not use an RPort of ServiceInterface
      CallbackGetPowerMode but will call the configured function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 24. DoIPTriggerGidSynchronization

**描述**: This container describes the Callbackfunction to trigger the GID synchronisation.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPTriggerGIDSynchronzation
  长名称: ''
  描述: Direct C Callback function to trigger the synchronization of the GID. If the
      DoIPTriggerGIDSynchronzation parameter is present, the DoIP module will not use an RPort
      of ServiceInterface CallbackTriggerGIDSynchronization but call the configured function.
  默认值: ''
  最小值: ''
  最大值: ''
```

