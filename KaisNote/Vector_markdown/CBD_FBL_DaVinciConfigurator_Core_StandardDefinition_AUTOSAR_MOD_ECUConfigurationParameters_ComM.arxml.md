# ComM

## 模块描述

Configuration of the ComM (Communications Manager) module.

## 容器列表

### 1. ComMConfigSet

**描述**: This container is the base for a multiple configuration set.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMPncEnabled
  长名称: ''
  描述: Defines whether in this configuration set the partial networking is enabled.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. ComMChannel

**描述**: This container contains the configuration (parameters) of the bus channel(s). The channel parameters
shall be harmonized within the whole communication stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMBusType
  长名称: ''
  描述: Identifies the bus type of the channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComMChannelId
  长名称: ''
  描述: Channel identification number of the corresponding channel.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: ComMFullCommRequestNotificationEnabled
  长名称: ''
  描述: Defines if the optional SenderReceiver Port of Interface ComM_CurrentChannelRequest will be
      provided for this channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComMGlobalNvmBlockDescriptor
  长名称: ''
  描述: If this parameter is set to "true", the NoWakeUp inhibition state of the channel shall be
      stored (in some implementation specific way) in the block pointed to by
      ComMGlobalNvmBlockDescriptor.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComMMainFunctionPeriod
  长名称: ''
  描述: Specifies the period in seconds that the MainFunction has to be triggered with.
  默认值: 0.02
  最小值: 0.001
  最大值: 0.1
- 
  序号: 6
  名称: ComMNoCom
  长名称: ''
  描述: Not allowed to change state of ComM channel to COMM_SILENT_COMMUNICATION or
      COMM_FULL_COMMUNICATION.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: ComMNoWakeup
  长名称: ''
  描述: Defines if an ECU is not allowed to wake-up the channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: ComMPncGatewayType
  长名称: ''
  描述: Identifies the Partial Network Gateway behaviour of a ComMChannel.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. ComMNetworkManagement

**描述**: This container contains the configuration parameters of the networkmanagement.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMNmLightTimeout
  长名称: ''
  描述: Defines the timeout (in seconds) after COMM_FULL_COMMUNICATION sub-state
      COMM_FULL_COM_READY_SLEEP is left.
  默认值: 10
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: ComMNmVariant
  长名称: ''
  描述: Defines the functionality of the networkmanagement.
  默认值: FULL
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComMPncNmRequest
  长名称: ''
  描述: If this parameter equals true then every time a FULL Communication is requested due to a
      change in the PNC state machine to PNC_REQUESTED Nm shall be called using the API
      Nm_NetworkRequest.
  默认值: false
  最小值: ''
  最大值: ''
```

### 4. ComMUserPerChannel

**描述**: This container contains a list of identifiers that are needed to refer to a user in the system which
is linked to a channel.

该容器没有参数。

### 5. ComMPnc

**描述**: This container contains the configuration of the partial network cluster (PNC).

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMPncId
  长名称: ''
  描述: Partial network cluster identification number.
  默认值: ''
  最小值: 0
  最大值: 47
```

### 6. ComMPncComSignal

**描述**: Represents the PncComSignals which are used to communicate the EIRA and ERA status of this PNC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMPncComSignalDirection
  长名称: ''
  描述: Indicates the communication direction of this PncComSignal.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComMPncComSignalKind
  长名称: ''
  描述: Indicates whether this PncComSignal represents EIRA or ERA PNC information.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. ComMUser

**描述**: This container contains a list of identifiers that are needed to refer to a user in the system which
is designated to request Communication modes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMUserIdentifier
  长名称: ''
  描述: An identifier that is needed to refer to a user in the system which is designated to request
      Communication Modes.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 8. ComMGeneral

**描述**: General configuration parameters of the Communication Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComMDirectUserMapping
  长名称: ''
  描述: If this parameter is set to true the configuration tool shall automatically create a ComMUser
      per ComMPnc and a ComMUser per ComMChannel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComMEcuGroupClassification
  长名称: ''
  描述: Defines whether a mode inhibition affects the ECU or not.
  默认值: 3
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: ComMModeLimitationEnabled
  长名称: ''
  描述: true if mode limitation functionality shall be enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComMPncGatewayEnabled
  长名称: ''
  描述: Enables or disables support of Partial Network Gateway.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: ComMPncPrepareSleepTimer
  长名称: ''
  描述: Time in seconds the PNC state machine shall wait in PNC_PREPARE_SLEEP.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 7
  名称: ComMPncSupport
  长名称: ''
  描述: Enables or disables support of partial networking.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: ComMSynchronousWakeUp
  长名称: ''
  描述: Wake up of one channel shall lead to a wake up of all channels if true.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: ComMTMinFullComModeDuration
  长名称: ''
  描述: Minimum time duration in seconds, spent in the COMM_FULL_COMMUNICATION sub-state
      COMM_FULL_COM_NETWORK_REQUESTED.
  默认值: 5
  最小值: 0.001
  最大值: 65
- 
  序号: 10
  名称: ComMVersionInfoApi
  长名称: ''
  描述: Switches the possibility to read the published information with the service
      ComM_GetPublishedInformation().
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: ComMWakeupInhibitionEnabled
  长名称: ''
  描述: true if wake up inhibition functionality enabled.
  默认值: false
  最小值: ''
  最大值: ''
```

