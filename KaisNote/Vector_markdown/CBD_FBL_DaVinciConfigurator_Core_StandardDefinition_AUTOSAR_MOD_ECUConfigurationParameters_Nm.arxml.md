# Nm

## 模块描述

The Generic Network Management Interface module

## 容器列表

### 1. NmChannelConfig

**描述**: This container contains the configuration (parameters) of the bus channel(s). The channel parameter
shall be harmonized within the whole communication stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmActiveCoordinator
  长名称: ''
  描述: This parameter indicates whether a NM Coordinator is an active gateway (NmActiveCoordinator =
      TRUE) or a passive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: NmChannelId
  长名称: ''
  描述: This parameter holds the unique channel index value. The value shall be the same as the
      ComMChannelId of the ComMChannel referenced by NmComMChannelRef.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: NmChannelSleepMaster
  长名称: ''
  描述: This parameter shall be set to indicate if the sleep of this network can be absolutely decided
      by the local node only and that no other nodes can oppose that decision.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: NmCoordClusterIndex
  长名称: ''
  描述: If this parameter is undefined for a channel, the corresponding bus does not belong to an NM
      coordination cluster.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: NmPassiveModeEnabled
  长名称: ''
  描述: Pre-processor switch for enabling support of Passive Mode of the <BusNm>s.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: NmShutdownDelayTimer
  长名称: ''
  描述: This parameter defines the time in seconds which the NM Coordination algorithm shall delay the
      release of this channel with.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 7
  名称: NmStateReportEnabled
  长名称: ''
  描述: Specifies if the NMS shall be set for the corresponding network.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: NmSynchronizingNetwork
  长名称: ''
  描述: If this parameter is true, then this network is a synchronizing network for the NM
      coordination cluster which it belongs to. The network is expected to call
      Nm_SynchronizationPoint() at regular intervals.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. NmGenericBusNmConfig

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmGenericBusNmPrefix
  长名称: ''
  描述: The prefix which identifies the generic <BusNm>. This will be used to determine the API name
      to be called by Nm for the provided interfaces of the <BusNm>. This string will used for
      the module prefix before the "_" character in the API call name.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. NmStandardBusNmConfig

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmStandardBusType
  长名称: ''
  描述: Identifies the bus type of the channel for standard AUTOSAR <BusNm>s and is used to determine
      which set of API calls to be called by Nm for the <BusNm>s.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. NmGlobalConfig

**描述**: This container contains all global configuration parameters of the Nm Interface.

该容器没有参数。

### 5. NmGlobalConstants

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmNumberOfChannels
  长名称: ''
  描述: Number of NM channels allowed within one ECU.
  默认值: ''
  最小值: 1
  最大值: 255
```

### 6. NmGlobalFeatures

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmBusSynchronizationEnabled
  长名称: ''
  描述: Pre-processor switch for enabling bus synchronization support of the <BusNm>s. This feature is
      required for NM Coordinator nodes only.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: NmCarWakeUpCallback
  长名称: ''
  描述: Name of the callback function to be called if Nm_CarWakeUpIndication() is called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: NmCarWakeUpRxEnabled
  长名称: ''
  描述: Enables or disables CWU detection.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: NmComControlEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the Communication Control support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: NmComUserDataSupport
  长名称: ''
  描述: Enable/Disable setting of NMUserData via SW-C. If NmComUserDataSupport is enabled the API
      Nm_SetUserData shall not be available.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: NmCoordinatorSupportEnabled
  长名称: ''
  描述: Pre-processor switch for enabling NM Coordinator support.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: NmGlobalCoordinatorTime
  长名称: ''
  描述: This parameter defines the maximum shutdown time of a connected and coordinated NM-Cluster.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 8
  名称: NmNodeDetectionEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the Node Detection feature.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: NmNodeIdEnabled
  长名称: ''
  描述: Pre-processor switch for enabling transmission of the source node identifier in NM messages.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: NmPduRxIndicationEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the PDU Rx Indication.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: NmRemoteSleepIndEnabled
  长名称: ''
  描述: Pre-processor switch for enabling Remote Sleep Indication support. This feature is required
      for NM Coordinator nodes only.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: NmRepeatMsgIndEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the Repeat Message Bit Indication.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: NmStateChangeIndEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the Network Management state change notification.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: NmUserDataEnabled
  长名称: ''
  描述: Pre-processor switch for enabling User Data support.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. NmGlobalProperties

#### 参数列表

```yaml
- 
  序号: 1
  名称: NmCycletimeMainFunction
  长名称: ''
  描述: The period between successive calls to the Main Function of the NM Interface in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: NmDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling development error detection and notification.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: NmVersionInfoApi
  长名称: ''
  描述: Pre-processor switch for enabling Version Info API support.
  默认值: ''
  最小值: ''
  最大值: ''
```

