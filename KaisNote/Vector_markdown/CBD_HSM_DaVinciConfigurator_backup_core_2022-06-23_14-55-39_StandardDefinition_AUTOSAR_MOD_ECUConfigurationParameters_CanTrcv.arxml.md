# CanTrcv

## 模块描述

Configuration of the CanTrcv (CAN Transceiver driver) module.

## 容器列表

### 1. CanTrcvConfigSet

**描述**: This is the multiple configuration set container for CAN Transceiver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTrcvSPICommRetries
  长名称: ''
  描述: Indicates the maximum number of communication retries in case of a failed SPI communication
      (applies both to timed out communication and to errors/NACK in the response data).
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: CanTrcvSPICommTimeout
  长名称: ''
  描述: Indicates the maximum time allowed to the CanTrcv for replying (either positively or
      negatively) to a SPI command.
  默认值: 0
  最小值: 0
  最大值: 100
```

### 2. CanTrcvChannel

**描述**: Container gives CAN transceiver driver information about a single CAN

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTrcvChannelId
  长名称: ''
  描述: Unique identifier of the CAN Transceiver Channel.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: CanTrcvChannelUsed
  长名称: ''
  描述: Shall the related CAN transceiver channel be used?
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanTrcvControlsPowerSupply
  长名称: ''
  描述: Is ECU power supply controlled by this transceiver?
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CanTrcvHwPnSupport
  长名称: ''
  描述: Indicates whether the HW supports the selective wake-up function
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CanTrcvInitState
  长名称: ''
  描述: State of CAN transceiver after call to CanTrcv_Init.
  默认值: CANTRCV_OP_MODE_NORMAL
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CanTrcvMaxBaudrate
  长名称: ''
  描述: Max baudrate for transceiver hardware type. Only used for validation purposes. Value shall be
      configured by configuration tool based on
  默认值: ''
  最小值: 0
  最大值: 1000
- 
  序号: 7
  名称: CanTrcvWakeupByBusUsed
  长名称: ''
  描述: Is wake up by bus supported? If CAN transceiver hardware does not support wake up by bus value
      is always FALSE. If CAN transceiver hardware supports wake up by bus value is TRUE or
      FALSE depending whether it is used or not.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. CanTrcvDioAccess

**描述**: Container gives CAN transceiver driver information about accessing ports and port pins. In addition
relation between CAN transceiver hardware pin names and Dio port access information is given.

该容器没有参数。

### 4. CanTrcvDioChannelAccess

**描述**: Container gives DIO channel access by single Can transceiver channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTrcvHardwareInterfaceName
  长名称: ''
  描述: CAN transceiver hardware interface name. It is typically the name of a pin. From a Dio point
      of view it is either a port, a single channel or a channel group. Depending on this fact
      either
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. CanTrcvSpiSequence

**描述**: Container gives CAN transceiver driver information about one SPI sequence.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTrcvSpiAccessSynchronous
  长名称: ''
  描述: This parameter is used to define whether the access to the Spi sequence is synchronous or
      asynchronous.
  默认值: false
  最小值: ''
  最大值: ''
```

### 6. CanTrcvPartialNetwork

**描述**: Container gives CAN transceiver driver information about the configuration of Partial Networking
functionality.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTrcvBaudRate
  长名称: ''
  描述: Indicates the CAN Bus communication baud rate in kbps.
  默认值: ''
  最小值: 0
  最大值: 1000
- 
  序号: 2
  名称: CanTrcvBusErrFlag
  长名称: ''
  描述: Indicates if the Bus Error (BUSERR) flag is managed by the BSW. This flag is set if a bus
      failure is detected by the transceiver.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanTrcvPnCanIdIsExtended
  长名称: ''
  描述: Indicates whether extended or standard ID is used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CanTrcvPnEnabled
  长名称: ''
  描述: Indicates whether the selective wake-up function is enabled or disabled in HW.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CanTrcvPnFrameCanId
  长名称: ''
  描述: CAN ID of the Wake-up Frame (WUF).
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: CanTrcvPnFrameCanIdMask
  长名称: ''
  描述: ID Mask for the selective activation of the transceiver. It is used to enableFrame Wake-up
      (WUF) on a group of IDs.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: CanTrcvPnFrameDlc
  长名称: ''
  描述: Data Length of the Wake-up Frame (WUF).
  默认值: ''
  最小值: 0
  最大值: 8
- 
  序号: 8
  名称: CanTrcvPowerOnFlag
  长名称: ''
  描述: Description: Indicates if the Power On Reset (POR) flag is available and is managed by the
      transceiver.
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. CanTrcvPnFrameDataMaskSpec

**描述**: Defines data payload mask to be used on the received payload in order to determine if the
transceiver must be woken up by the received Wake-up Frame (WUF).

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTrcvPnFrameDataMask
  长名称: ''
  描述: Defines the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload
      in order to determine if the transceiver must be woken up by the received Wake-up Frame
      (WUF).
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: CanTrcvPnFrameDataMaskIndex
  长名称: ''
  描述: holds the position n in frame of the mask-part
  默认值: ''
  最小值: 0
  最大值: 7
```

### 8. CanTrcvGeneral

**描述**: Container gives CAN transceiver driver basic information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTrcvDevErrorDetect
  长名称: ''
  描述: Switches development error detection and notification on and off.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanTrcvGetVersionInfo
  长名称: ''
  描述: Switches version information API on and off. If switched off, function need not be present in
      compiled code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanTrcvSPICommRetries
  长名称: ''
  描述: Indicates the maximal number of communication retries in case of failed SPI communication
      (applies both to timed out communication and to errors/NACK in the response data).
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: CanTrcvSPICommTimeout
  长名称: ''
  描述: Indicates the maximal time allowed to the Transceiver in order to reply
  默认值: 0
  最小值: 0
  最大值: 100
- 
  序号: 5
  名称: CanTrcvWaitCount
  长名称: ''
  描述: Indicates the number of wait states to change the transceiver operation mode. Transceiver
      hardware may need wait states for some transitions.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: CanTrcvWakeUpSupport
  长名称: ''
  描述: Informs whether wake up is supported by polling or not supported. In case no
  默认值: ''
  最小值: ''
  最大值: ''
```

