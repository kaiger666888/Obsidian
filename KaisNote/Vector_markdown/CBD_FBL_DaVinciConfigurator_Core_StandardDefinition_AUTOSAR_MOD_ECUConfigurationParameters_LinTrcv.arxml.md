# LinTrcv

## 模块描述

Configuration of LIN Transceiver Driver module

## 容器列表

### 1. LinTrcvChannel

**描述**: Container gives LIN transceiver driver information about a single LIN transceiver channel. Any LIN
transceiver driver has such LIN transceiver channels.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinTrcvChannelId
  长名称: ''
  描述: Unique identifier of the LIN Transceiver Channel.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: LinTrcvChannelUsed
  长名称: ''
  描述: Shall the related LIN transceiver channel be used?
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: LinTrcvInitState
  长名称: ''
  描述: State of LIN transceiver after call to LinTrcv_Init.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: LinTrcvWakeupByBusUsed
  长名称: ''
  描述: Is wake up by bus supported? If LIN transceiver hardware does not support wake up by bus value
      is always FALSE. If LIN transceiver hardware supports wake up by bus value is TRUE or
      FALSE depending whether it is used or not.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. LinTrcvDioAccess

**描述**: Container gives LIN transceiver driver information about accessing ports and port pins. In addition
relation between LIN transceiver hardware pin names and Dio port access information is given. If a
LIN transceiver hardware has no Dio interface, there is no instance of this container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinTrcvHardwareInterfaceName
  长名称: ''
  描述: LIN transceiver hardware interface name. It is typically the name of a pin. From a Dio point
      of view it is either a port, a single channel or a channel group. Depending on this fact
      either LINTRCV_DIO_PORT_SYMBOLIC_NAME or LINTRCV_DIO_CHANNEL_SYMBOLIC_NAME or
      LINTRCV_DIO_CHANNEL_GROUP_SYMBOLIC_NAME shall reference a Dio configuration. The LIN
      transceiver driver implementation description shall list up this name for the
      appropriate LIN transceiver hardware.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. LinTrcvSpiSequence

**描述**: Container gives LIN transceiver driver information about one SPI sequence.

该容器没有参数。

### 4. LinTrcvGeneral

**描述**: Container gives LIN transceiver driver basic information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinTrcvDevErrorDetect
  长名称: ''
  描述: Switches development error detection and notification on and off. If switched on, #define
      LINTRCV_DEV_ERROR_DETECT ON shall be generated. If switched off, #define
      LINTRCV_DEV_ERROR_DETECT OFF shall be generated. Define shall be part of file
      LinTrcv_Cfg.h.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: LinTrcvGetVersionInfo
  长名称: ''
  描述: Switches version information API on and off. If switched off, function need not be present in
      compiled code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: LinTrcvIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: LinTrcvWaitCount
  长名称: ''
  描述: Wait count for transceiver state changes.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: LinTrcvWakeUpSupport
  长名称: ''
  描述: Informs whether wake up is supported or not. In case wake up is not supported by LIN
      transceiver hardware the setting shall be false. The wake up ability may be switched on
      or off for each channel of one LIN transceiver by LinTrcvWakeupSourceRef.
  默认值: ''
  最小值: ''
  最大值: ''
```

