# FrTrcv

## 模块描述

Configuration of the FrTrcv (FlexRay Transceiver driver) module.

## 容器列表

### 1. FrTrcvChannel

**描述**: Container gives FlexRay transceiver driver information about a single FlexRay transceiver channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTrcvChannelId
  长名称: ''
  描述: Unique identifier of the FlexRay Transceiver Channel.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: FrTrcvChannelUsed
  长名称: ''
  描述: Shall the related FlexRay transceiver channel be used?
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrTrcvControlsPowerSupply
  长名称: ''
  描述: Is ECU power supply controlled by this transceiver?
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrTrcvEnableInterruptCallout
  长名称: ''
  描述: This parameter defines the existence and the name of a callout function that enables the
      interrupt pin for the wakeup. If this parameter is omitted no callout shall take place.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FrTrcvInitState
  长名称: ''
  描述: State of FlexRay transceiver after power on.
  默认值: FRTRCV_OP_MODE_NORMAL
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FrTrcvMaxBaudrate
  长名称: ''
  描述: Max baudrate for transceiver hardware type. Only used for validation purposes. Value shall be
      configured by configuration tool based on
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FrTrcvWakeupByBusUsed
  长名称: ''
  描述: Is wake up by node supported? If FlexRay transceiver hardware does not support wake up by node
      value is always FALSE. If FlexRay transceiver hardware supports wake up by node value is
      TRUE or FALSE depending whether it is used or not.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. FrTrcvDioAccess

**描述**: Container gives FR transceiver driver information about accessing ports and port pins. If a FR
transceiver hardware has no Dio interface, there is no instance of this container.

该容器没有参数。

### 3. FrTrcvDioChannelAccess

**描述**: In this Container the relation between FR transceiver hardware pin names and Dio port access
information is given.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTrcvHardwareInterfaceName
  长名称: ''
  描述: FR transceiver hardware interface name. It is typically the name of a pin. From a Dio point of
      view it is either a port, a single channel or a channel group. Depending on this fact
      either FRTRCV_DIO_PORT_SYMBOLIC_NAME or FRTRCV_DIO_CHANNEL_SYMBOLIC_NAME or
      FRTRCV_DIO_CHANNEL_GROUP_SYMBOLIC_NAME shall reference a Dio configuration. The FR
      transceiver driver implementation description shall list up this name for the
      appropriate FR transceiver hardware.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. FrTrcvSpiSequence

**描述**: Container gives FlexRay transceiver driver information about one SPI sequence. One SPI sequence used
by FlexRay transceiver driver is in exclusive use for it. No other driver is allowed to access this
sequence. FlexRay transceiver driver may use one sequence to access n FlexRay transceiver hardwares
chips of the same type or n sequences are used to access one single FlexRay transceiver hardware
chip. If a FlexRay transceiver hardware has no SPI interface, there is no instance of this
container.

该容器没有参数。

### 5. FrTrcvBranchIdContainer

**描述**: Only one SymbolicNameValue can be defined per container. Therefore this container is necessary.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTrcvBranchId
  长名称: ''
  描述: Unique branch id. It is used by CDDs and internally.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 6. FrTrcvChannelDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 7. FrTrcvGeneral

**描述**: Container gives FlexRay transceiver driver basic information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTrcvDemReportErrorStatusConfiguration
  长名称: ''
  描述: Name of a C function which substitutes Dem_ReportErrorStatus.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrTrcvDevErrorDetect
  长名称: ''
  描述: Switches development error detection and notification on and off.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrTrcvErrorCheckDuringCommunication
  长名称: ''
  描述: Enable a functionality to check transceiver's state during communication.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrTrcvErrorCheckInInit
  长名称: ''
  描述: Enable a functionality to check transceiver's state while initialization process of FrTrcv.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FrTrcvGetVersionInfo
  长名称: ''
  描述: Switches version information API on and off. If switched off, function need not be present in
      compiled code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FrTrcvIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: FrTrcvMainFunctionCycleTime
  长名称: ''
  描述: Cyclic call time for function FrTrcvMainFunction in seconds. A call time of 0ms indicates no
      calls for this function. In this case function need not be present in compiled code.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 8
  名称: FrTrcvRetryCountInInit
  长名称: ''
  描述: Specifies the number of retry count when error occurs while initialization process of FrTrcv.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: FrTrcvWaitCount
  长名称: ''
  描述: Wait count for transceiver state changes.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 10
  名称: FrTrcvWakeUpSupport
  长名称: ''
  描述: Informs whether wake up is supported by polling or whether it is not supported.
  默认值: ''
  最小值: ''
  最大值: ''
```

