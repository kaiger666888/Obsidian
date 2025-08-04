# Sd

## 模块描述

Configuration of the Service Discovery module.

## 容器列表

### 1. SdConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR Service
Discovery module. This container is a MultipleConfigurationContainer, i.e. this container and its
sub-containers exist once per configuration set.

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
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SdClientServiceId
  长名称: ''
  描述: Id to identify the service. This is unique for the service interface.
  默认值: ''
  最小值: 0
  最大值: 65534
- 
  序号: 4
  名称: SdClientServiceInstanceId
  长名称: ''
  描述: Configuration parameter to specify Instance Id of the service as used in SD entries.
  默认值: ''
  最小值: 0
  最大值: 65534
- 
  序号: 5
  名称: SdClientServiceMajorVersion
  长名称: ''
  描述: Major version number of the Service as used in the SD entries.
  默认值: ''
  最小值: 0
  最大值: 254
- 
  序号: 6
  名称: SdClientServiceMinorVersion
  长名称: ''
  描述: Minor version number of the Service as used in the SD Service Entries.
  默认值: ''
  最小值: 0
  最大值: 4294967295
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
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SdConsumedEventGroupId
  长名称: ''
  描述: The Eventgroup Id of this eventGroup as a unique identifier of the eventgroup in this service.
      This identifier is used for EventGroup entries as well.
  默认值: ''
  最小值: 0
  最大值: 65534
```

### 6. SdClientCapabilityRecord

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

### 7. SdConsumedMethods

**描述**: Container element for representing the data path for accessing the server methods.

该容器没有参数。

### 8. SdClientTimer

**描述**: This container specifies all timers used by the Service Discovery module for Client Services.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdClientTimerInitialFindDelayMax
  长名称: ''
  描述: Max value in [s] to delay randomly the transmission of a find message. This parameter is
      mandatory for ClientService.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: SdClientTimerInitialFindDelayMin
  长名称: ''
  描述: Min value in [s] to delay randomly the transmission of a find message. This parameter is
      mandatory for ClientService.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: SdClientTimerInitialFindRepetitionsBaseDelay
  长名称: ''
  描述: The base delay in [s] for find repetitions. Successive finds have an exponential back off
      delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory
      for ClientService.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 4
  名称: SdClientTimerInitialFindRepetitionsMax
  长名称: ''
  描述: Configuration for the maximum number of find repetitions. This parameter is mandatory for
      ClientService.
  默认值: ''
  最小值: 0
  最大值: 10
- 
  序号: 5
  名称: SdClientTimerRequestResponseMaxDelay
  长名称: ''
  描述: Maximum allowable response delay to entries received by multicast in seconds. This parameter
      is mandatory for ConsumedEventGroups.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 6
  名称: SdClientTimerRequestResponseMinDelay
  长名称: ''
  描述: Minimum allowable response delay to the find message in seconds. This parameter is mandatory
      for ConsumedEventGroups.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 7
  名称: SdClientTimerTTL
  长名称: ''
  描述: Time to live for find and subscribe messages.
  默认值: ''
  最小值: 1
  最大值: 16777215
```

### 9. SdInstanceMulticastRxPdu

**描述**: This container specifies the received PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdRxPduId
  长名称: ''
  描述: ID of the PDU that will be received via the API Sd_SoAdIfRxIndication().
  默认值: ''
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
  默认值: ''
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
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SdServerServiceId
  长名称: ''
  描述: Id to identify the service. This is unique for the service interface.
  默认值: ''
  最小值: 0
  最大值: 65534
- 
  序号: 4
  名称: SdServerServiceInstanceId
  长名称: ''
  描述: Configuration parameter to specify Instance Id of the Service implemented by the Server
      Service.
  默认值: ''
  最小值: 0
  最大值: 65534
- 
  序号: 5
  名称: SdServerServiceMajorVersion
  长名称: ''
  描述: Major version number of the Service as used in SD Entries.
  默认值: ''
  最小值: 0
  最大值: 254
- 
  序号: 6
  名称: SdServerServiceMinorVersion
  长名称: ''
  描述: Minor version number of the Service as used e.g. in Offer Service entries.
  默认值: ''
  最小值: 0
  最大值: 4294967294
```

### 13. SdEventHandler

**描述**: Container Element for representing an EventGroup as part of the Service Instance.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdEventHandlerAutoAvailable
  长名称: ''
  描述: If existing and set to true, this EventGroup will be set to "available" on start.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SdEventHandlerEventGroupId
  长名称: ''
  描述: The EventGroup Id of this EventGroup as a unique identifier of the EventGroup in this service.
      This identifier is used for EventGroup entries as well.
  默认值: ''
  最小值: 0
  最大值: 65534
- 
  序号: 3
  名称: SdEventHandlerHandleId
  长名称: ''
  描述: The HandleId by which the BswM can identify this EventGroup.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: SdEventHandlerMulticastThreshold
  长名称: ''
  描述: Specifies the number of subscribed clients that trigger the Server to change the transmission
      of events to Multicast.
  默认值: ''
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

### 17. SdServerCapabilityRecord

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

### 18. SdProvidedMethods

**描述**: Container element for representing the needed elements of the data path for the methods provided by
the service.

该容器没有参数。

### 19. SdServerCapabilityRecord

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

### 20. SdServerTimer

**描述**: This container specifies all timers used by the Service Discovery module for Server Services.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SdServerTimerInitialOfferDelayMax
  长名称: ''
  描述: Max value in [s] to delay randomly the first offer. This parameter is mandatory for
      ServerService.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: SdServerTimerInitialOfferDelayMin
  长名称: ''
  描述: Min value in [s] to delay randomly the first offer. This parameter is mandatory for
      ServerService.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: SdServerTimerInitialOfferRepetitionBaseDelay
  长名称: ''
  描述: The base delay in [s] for offer repetitions. Successive offers have an exponential back off
      delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory
      for ServerService.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 4
  名称: SdServerTimerInitialOfferRepetitionsMax
  长名称: ''
  描述: Configure the maximum amount of offer repetition. This parameter is mandatory for
      ServerService.
  默认值: ''
  最小值: 0
  最大值: 10
- 
  序号: 5
  名称: SdServerTimerOfferCyclicDelay
  长名称: ''
  描述: Interval between cyclic offers in the main phase. This parameter is mandatory for
      ServerService.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 6
  名称: SdServerTimerRequestResponseMaxDelay
  长名称: ''
  描述: Maximum allowable response delay to entries received by multicast in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 7
  名称: SdServerTimerRequestResponseMinDelay
  长名称: ''
  描述: Minimum allowable response delay to entries received by multicast in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 8
  名称: SdServerTimerTTL
  长名称: ''
  描述: Time to live for offer service or subscribe EventGroup ack.
  默认值: ''
  最小值: 1
  最大值: 16777215
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
  描述: Enables and disables the development error detection and notification mechanism.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SdMainFunctionCycleTime
  长名称: ''
  描述: This parameter defines the cycle time in seconds of the periodic calling of Sd main function.
  默认值: ''
  最小值: 1E-4
  最大值: 1
- 
  序号: 3
  名称: SdVersionInfoApi
  长名称: ''
  描述: Enables and disables the version info API.
  默认值: ''
  最小值: ''
  最大值: ''
```

