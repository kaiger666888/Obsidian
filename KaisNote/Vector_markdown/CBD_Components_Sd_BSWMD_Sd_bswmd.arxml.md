# Sd

## 模块描述

The Service Discovery module (Sd) implements the SOME/IP-SD protocol to offer and detect available
services within a vehicle network in order to establish a service-oriented communication between
different network nodes.The Sd module configures the SoAd for the IP data path; Service state
changes  are requested from/reported to the BswM module.
#Ethernet #SomeIpSd #SoAd #BswM
#Autosar

## 容器列表

### 1. SdConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR Service
Discovery module.

该容器没有参数。

### 2. SdInstance

**描述**: This container represents an instance of the SD; i.e. the SD configuration for a certain link.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdInstanceHostname
  长名称: ''
  描述: Configuration parameter to specify the Hostname.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SdMaxNrDestAddr
  长名称: Maximal Number of Destination Addresses
  描述: This Parameter specifies the size of the address storage array saving the addresses of
      communication partners.
  默认值: 16
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: SdInOutQueueSize
  长名称: Size of the Input/Output Queue
  描述: |
    This parameter specifies the maximal amount of Entries which can pend in order to be processed.
    (Specifies the Rx as well as the Tx Entries).
    
    Note: Only (Stop)Subscribe SdEntries are stored in the Rx Queue,
    while the TxQueue is used for all SdEntry Types.
  默认值: 96
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: SdSubscribeEventgroupRetryDelay
  长名称: ''
  描述: Time in seconds when a subscription to an event group shall be retriggered, if no
      SubscribeEventGroupAck or SubscribeEventGroupNack was received.
  默认值: 0.01
  最小值: 0.001
  最大值: 50
- 
  序号: 5
  名称: SdSubscribeEventgroupRetryMax
  长名称: ''
  描述: Maximum count of retry a subscription, if a subscription to an event group is not acknowledged
      by SubscribeEventGroupAck or SubscribeEventGroupNack. 0x0=no retry, 0xFF=retry forever
      (as long as the event group is requested)
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: SdInQueueProcessLimit
  长名称: Input Queue Process Limit
  描述: |
    Specifies the maximum number of Rx Queue Entries which shall be processed during one
    MainFunction cycle. If value is set to zero the number of Entries to be processed during one
    cycle is not restricted.
    
    Note: Only (Stop)Subscribe SdEntries are stored in the Rx Queue.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: SdInstanceLocalAdressCheckLength
  长名称: Local Adress Check Length
  描述: Specifies how many leading bits of a remote addresses shall be compared to the local address
      in order to determine, if the remote address is part of the same subnet and can
      therefore be used. This shall support IPv4 (0..32) and IPv6 (0..128). A value of "0"
      means that the address is not checked at all. If this item is not present, the security
      checks use the configured netmask instead.
  默认值: ''
  最小值: 0
  最大值: 128
```

### 3. SdClientService

**描述**: This container specifies all parameters used by Client services.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdClientServiceAutoRequire
  长名称: ''
  描述: If existing and set to true, this Service will be set to "required" on start.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SdClientServiceHandleId
  长名称: ''
  描述: The HandleId by which the BswM can identify this Client Service Instance.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SdClientServiceId
  长名称: ''
  描述: Id to identify the service. This is unique for the service interface.
  默认值: 0
  最小值: 0
  最大值: 65534
- 
  序号: 4
  名称: SdClientServiceInstanceId
  长名称: ''
  描述: Configuration parameter to specify Instance Id of the service as used in SD entries.
  默认值: 1
  最小值: 0
  最大值: 65534
- 
  序号: 5
  名称: SdClientServiceMajorVersion
  长名称: ''
  描述: Major version number of the Service as used in the SD entries.
  默认值: 1
  最小值: 0
  最大值: 254
- 
  序号: 6
  名称: SdClientServiceMinorVersion
  长名称: ''
  描述: Minor version number of the Service as used in the SD Service Entries.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: SdVersionDrivenFindBehavior
  长名称: ''
  描述: Defined the possible acceptance kinds for required service instances.
  默认值: EXACT_OR_ANY_MINOR_VERSION
  最小值: ''
  最大值: ''
```

### 4. SdClientCapabilityRecord

**描述**: Sd uses capability records to store arbitrary name/value pairs conveying additional information
about the named service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdClientServiceCapabilityRecordKey
  长名称: ''
  描述: Defines a CapabilityRecord key.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SdClientServiceCapabilityRecordValue
  长名称: ''
  描述: Defines the corresponding CapabilityRecord value.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. SdConsumedEventGroup

**描述**: A Service may have event groups which can be consumed. A service consumer has to subscribe to the
corresponding event-group. After the subscription the event consumer takes the role of a server and
the event provider that of a client.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdConsumedEventGroupAutoRequire
  长名称: ''
  描述: If existing and set to true, this EventGroup will be set to "required" on start.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SdConsumedEventGroupHandleId
  长名称: ''
  描述: The HandleId by which the BswM can identify this EventGroup.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SdConsumedEventGroupId
  长名称: ''
  描述: |
    The Eventgroup Id of this eventGroup as a unique identifier of the eventgroup in this service.
    This identifier is used for EventGroup entries as well.
    Please note, that the Eventgroup ID 0x0000 is reserved.
  默认值: 0
  最小值: 0
  最大值: 65534
```

### 6. SdConsumedMethods

**描述**: Container element for representing the data path for accessing the server methods.

该容器没有参数。

### 7. SdClientTimer

**描述**: This container specifies all timers used by the Service Discovery module for Client Services.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdClientTimerInitialFindDelayMax
  长名称: ''
  描述: Max value in [s] to delay randomly the transmission of a find message. This parameter is
      mandatory for ClientService.
  默认值: 0.5
  最小值: 0
  最大值: 4294967
- 
  序号: 2
  名称: SdClientTimerInitialFindDelayMin
  长名称: ''
  描述: Min value in [s] to delay randomly the transmission of a find message. This parameter is
      mandatory for ClientService.
  默认值: 0.1
  最小值: 0
  最大值: 4294967
- 
  序号: 3
  名称: SdClientTimerInitialFindRepetitionsBaseDelay
  长名称: ''
  描述: The base delay in [s] for find repetitions. Successive finds have an exponential back off
      delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory
      for ClientService.
  默认值: 1
  最小值: 0
  最大值: 4294967
- 
  序号: 4
  名称: SdClientTimerInitialFindRepetitionsMax
  长名称: ''
  描述: Configuration for the maximum number of find repetitions. This parameter is mandatory for
      ClientService.
  默认值: 4
  最小值: 0
  最大值: 10
- 
  序号: 5
  名称: SdClientTimerRequestResponseMaxDelay
  长名称: ''
  描述: Maximum allowable response delay to entries received by multicast in seconds. This parameter
      is mandatory for ConsumedEventGroups.
  默认值: 0.1
  最小值: 0
  最大值: 4294967
- 
  序号: 6
  名称: SdClientTimerRequestResponseMinDelay
  长名称: ''
  描述: Minimum allowable response delay to the find message in seconds. This parameter is mandatory
      for ConsumedEventGroups.
  默认值: 0.01
  最小值: 0
  最大值: 4294967
- 
  序号: 7
  名称: SdClientTimerTTL
  长名称: ''
  描述: Time to live for find and subscribe messages.
  默认值: 5
  最小值: 1
  最大值: 16777215
```

### 8. SdInstanceDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 9. SdInstanceMulticastRxPdu

**描述**: This container specifies the received PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdRxPduId
  长名称: ''
  描述: ID of the PDU that will be received via the API Sd_SoAdIfRxIndication().
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 10. SdInstanceTxPdu

**描述**: This container specifies the transmitted PDU.

该容器没有参数。

### 11. SdInstanceUnicastRxPdu

**描述**: This container specifies the received PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdRxPduId
  长名称: ''
  描述: ID of the PDU that will be received via the API Sd_SoAdIfRxIndication().
  默认值: 1
  最小值: 0
  最大值: 65535
```

### 12. SdServerService

**描述**: This container specifies all parameters used by Server services.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdServerServiceAutoAvailable
  长名称: ''
  描述: If existing and set to true, this Service will be set to "Available" on start.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SdServerServiceHandleId
  长名称: ''
  描述: The HandleId by which the BswM can identify this Server Service Instance.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SdServerServiceId
  长名称: ''
  描述: Id to identify the service. This is unique for the service interface.
  默认值: 0
  最小值: 0
  最大值: 65534
- 
  序号: 4
  名称: SdServerServiceInstanceId
  长名称: ''
  描述: Configuration parameter to specify Instance Id of the Service implemented by the Server
      Service.
  默认值: 1
  最小值: 0
  最大值: 65534
- 
  序号: 5
  名称: SdServerServiceMajorVersion
  长名称: ''
  描述: Major version number of the Service as used in SD Entries.
  默认值: 1
  最小值: 0
  最大值: 254
- 
  序号: 6
  名称: SdServerServiceMinorVersion
  长名称: ''
  描述: Minor version number of the Service as used e.g. in Offer Service entries.
  默认值: 0
  最小值: 0
  最大值: 4294967294
```

### 13. SdEventHandler

**描述**: Container Element for representing an EventGroup as part of the Service Instance.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdEventHandlerEventGroupId
  长名称: ''
  描述: |
    The EventGroup Id of this EventGroup as a unique identifier of the EventGroup in this service.
    This identifier is used for EventGroup entries as well.
    Please note, that the Eventgroup ID 0x0000 is reserved.
  默认值: 0
  最小值: 0
  最大值: 65534
- 
  序号: 2
  名称: SdEventHandlerHandleId
  长名称: ''
  描述: The HandleId by which the BswM can identify this EventGroup.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SdEventHandlerMulticastThreshold
  长名称: ''
  描述: |
    Specifies the number of subscribed clients with different endpoint
    information (see SWS_SD_00754) that triggers the Server to change
    the transmission of events via the Eventhandler Multicast connection.
    
    If configured to 0 only Consumed Evengroup unicast connections and
    Consumed Eventgroup multicast connections will be used.
    
    If configured to 1 the first client and all further subscribed clients will be
    served via the Eventhandler Multicast connection as configured in
    SdMulticastEventSoConRef.
    
    If configured to n up to n-1 clients with different endpoint information
    will be served via Consumed Evengroup unicast connections and
    Consumed Eventgroup multicast connections. As soon as the number
    of subscribed clients with different endpoint information reaches n,
    then all subscribed clients are served via the Eventhandler Multicast
    connection as configured in SdMulticastEventSoConRef.
    
    This does not influence the handling of initial events.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: SdEventHandlerMaxRemoteClients
  长名称: ''
  描述: The maximum number of remote clients for this SdEventHandler. Can be used to reduce the RAM
      footprint if the same SoConGroup is used for multiple SdEventHandlers and the maximum
      number of clients for an individual EventHandler is known during configuration time. If
      set to zero, the number of maximum clients is calculated according to the number of
      SocketConnections in the referenced SoConGroups of the EventHandler.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 14. SdEventHandlerMulticast

**描述**: The subcontainer including the Routing Group for Activation of Events sent over Multicast.

该容器没有参数。

### 15. SdEventHandlerTcp

**描述**: The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent
over TCP.

该容器没有参数。

### 16. SdEventHandlerUdp

**描述**: The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent
over UDP.

该容器没有参数。

### 17. SdProvidedMethods

**描述**: Container element for representing the needed elements of the data path for the methods provided by
the service.

该容器没有参数。

### 18. SdServerCapabilityRecord

**描述**: Sd uses capability records to store arbitrary name/value pairs conveying additional information
about the named service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdServerCapabilityRecordKey
  长名称: ''
  描述: Defines a CapabilityRecord key.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SdServerCapabilityRecordValue
  长名称: ''
  描述: Defines the corresponding CapabilityRecord value.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 19. SdServerTimer

**描述**: This container specifies all timers used by the Service Discovery module for Server Services.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdServerTimerInitialOfferDelayMax
  长名称: ''
  描述: Max value in [s] to delay randomly the first offer. This parameter is mandatory for
      ServerService.
  默认值: 0.5
  最小值: 0
  最大值: 4294967
- 
  序号: 2
  名称: SdServerTimerInitialOfferDelayMin
  长名称: ''
  描述: Min value in [s] to delay randomly the first offer. This parameter is mandatory for
      ServerService.
  默认值: 0.1
  最小值: 0
  最大值: 4294967
- 
  序号: 3
  名称: SdServerTimerInitialOfferRepetitionBaseDelay
  长名称: ''
  描述: The base delay in [s] for offer repetitions. Successive offers have an exponential back off
      delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory
      for ServerService.
  默认值: 0.1
  最小值: 0
  最大值: 4294967
- 
  序号: 4
  名称: SdServerTimerInitialOfferRepetitionsMax
  长名称: ''
  描述: Configure the maximum amount of offer repetition. This parameter is mandatory for
      ServerService.
  默认值: 5
  最小值: 0
  最大值: 10
- 
  序号: 5
  名称: SdServerTimerOfferCyclicDelay
  长名称: ''
  描述: Interval between cyclic offers in the main phase. This parameter is mandatory for
      ServerService.
  默认值: 2
  最小值: 0
  最大值: 4294967
- 
  序号: 6
  名称: SdServerTimerRequestResponseMaxDelay
  长名称: ''
  描述: Maximum allowable response delay to entries received by multicast in seconds.
  默认值: 0.1
  最小值: 0
  最大值: 4294967
- 
  序号: 7
  名称: SdServerTimerRequestResponseMinDelay
  长名称: ''
  描述: Minimum allowable response delay to entries received by multicast in seconds.
  默认值: 0.01
  最小值: 0
  最大值: 4294967
- 
  序号: 8
  名称: SdServerTimerTTL
  长名称: ''
  描述: Time to live for offer service.
  默认值: 5
  最小值: 1
  最大值: 16777215
```

### 20. SdCapabilityRecordMatchCallout

**描述**: Callout that is invoked by the Sd implementation  to determine whether the configuration options
contained in the entries of a received SD message match the capability record elements configured in
SdServerCapabilityRecord or SdClientCapabilityRecord.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdCapabilityRecordMatchCalloutName
  长名称: ''
  描述: Function name (i.e., C-identifier) of the SdCapabilityRecordMatchCallout.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 21. SdServiceGroup

**描述**: Contains the configuration parameters of the AUTOSAR SD module's
SdServiceGroupS.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdServiceGroupHandleId
  长名称: ''
  描述: |
    The numerical value used as the ID of this SdServiceGroup. The
    SdServiceHandleId is required by the API calls to start and stop
    SdServiceGroupS.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 22. SdGeneral

**描述**: This container lists the general configuration parameters for the Service Discovery module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdDevErrorDetect
  长名称: ''
  描述: |
    Switches the development error detection and notification on or off.
    - true: detection and notification is enabled.
    - false: detection and notification is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SdMainFunctionCycleTime
  长名称: ''
  描述: This parameter defines the cycle time in seconds of the periodic calling of Sd main function.
  默认值: 0.005
  最小值: 0.0001
  最大值: 1
- 
  序号: 3
  名称: SdVersionInfoApi
  长名称: ''
  描述: Enables and disables the version info API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SdMaxNrOptionsPerMsg
  长名称: ''
  描述: This parameter specifies the amount of attached options, which can be handled per incomming
      message.
  默认值: 10
  最小值: 1
  最大值: 65534
- 
  序号: 5
  名称: SdRandomNumberFunctionIncludeFile
  长名称: ''
  描述: This parameter defines the header file holding the declaration of the random number generation
      function defined in 'SdRandomNumberFunction'.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SdRandomNumberFunction
  长名称: ''
  描述: This parameter defines the function called for the random number generation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SdUserConfigFile
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
  序号: 8
  名称: SdTxBufferSize
  长名称: ''
  描述: Buffer size in bytes which can be used for message transmission.
  默认值: 1464
  最小值: 48
  最大值: 65535
- 
  序号: 9
  名称: SdSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: SdSetRemAddrOfClientRxMulticastSoCon
  长名称: ''
  描述: |
    This parameter specifies whether the remote address of consumed eventgroup multicast socket
    connection(s) shall be configured to the unicast remote address of the remote server.
    If the remote address is set (value == TRUE), the socket connection can only receive events from
    this remote server. If the address is not set (value == FALSE) and remains at WILDCARD, this
    socket connection is able to receive events from multiple remote servers.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SdSubscribeEventgroupRetryEnable
  长名称: ''
  描述: Switch to enable or disable the retry functionality to subscribe to Eventgroups of
      ServerServices with TTL set to 0xFFFFFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: SdGetAndResetMeasurementDataApi
  长名称: ''
  描述: This parameter enables/disables the function Sd_GetAndResetMeasurementData() to get/reset
      measurement data with the number of invalid SdMessages and received
      SubscribeEventgroupNack entries.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: SdRuntimeMeasurementSupport
  长名称: ''
  描述: |
    If enabled runtime measurement points are added to the BSW module code and are added to the
    module configuration of MICROSAR Rtm. The available measurement points can be seen and
    configured in the Rtm module configuration.
    Runtime measurement should be disabled in production code.
    
    Only available if the Rtm module is part of the project.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: SdRuntimeErrorReport
  长名称: ''
  描述: |
    Switches the runtime error notification on or off.
    - true: notification is enabled.
    - false: notification is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: SdFastSubscriptionRecoveryAfterReboot
  长名称: ''
  描述: |
    This setting changes the behavior when the reboot of a remote SD instance is detected
    with a SD message which contains SubscribeEventgroup entries:
    
    Disabled: Local SD implementation aborts all connections to rebooted remote SD endpoint,
    even if connections have been initiated after the reboot. The client has not enough time to
    reconnect,
    so the local SD will send SubscribeNack(s) (behavior before version 16.00.00).
    
    Enabled: Local SD implementation does not abort connections which have been initiated
    after the reboot and  sends SubscribeAck(s) right away.
    
    Rationale: A detected reboot shall lead to expiration of the state of the remote SD instance
    before the reboot.
    If the remote SD instance sends Subscriptions with the first SD Message after its reboot
    however,
    connections have been initiated after the reboot as a reaction to Offers and it is not necessary
    to abort them.
    Furthermore, if feature is disabled and the connection is aborted due to the detected reboot,
    re-initiating the connection
    will not work if ephemeral ports are used, even if a delay would have been introduced to allow
    some time for the client to re-initiate the connection,
    since the TCP endpoint of the subscribe will not match to the port of the new connection
    anymore.
    This feature has been introduced to migitate this.
  默认值: false
  最小值: ''
  最大值: ''
```

### 23. SdGeneration

**描述**: Contains the generation configuration parameters of the module Sd.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdOutOfBoundsWriteProtectionStrategy
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
  名称: SdOutOfBoundsWriteSanitizer
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
  名称: SdOutOfBoundsReadSanitizer
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
  名称: SdReduceConstantData2Define
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
  名称: SdBoolDataInArrayOfStructStrategy
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
  名称: SdDeduplicateIndirectedData
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
  名称: SdDataDeduplicationStrategy
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
  名称: SdReduceBoolDataByNegationThreshold
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
  名称: SdReduceBoolDataByNumericalComparisonThreshold
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
  名称: SdReduceBoolDataByNumericalRelationThreshold
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
  名称: SdReduceBoolDataByNumericalOperandStrategy
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
  名称: SdReduceNumericalDataByOffsetThreshold
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
  名称: SdReduceNumericalDataByArraySubtractionThreshold
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
  名称: SdShortSymbols
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
  名称: SdInterfacesForDeactivatedData
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
  序号: 16
  名称: SdReferringKeysInComments
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

