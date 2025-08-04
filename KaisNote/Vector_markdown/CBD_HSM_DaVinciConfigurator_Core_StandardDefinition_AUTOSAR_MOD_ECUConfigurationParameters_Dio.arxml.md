# Dio

## 模块描述

Configuration of the Dio (Digital IO) module.

## 容器列表

### 1. DioConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR DIO module.
This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist
once per configuration set.

该容器没有参数。

### 2. DioPort

**描述**: Configuration of individual DIO ports, consisting of channels and possible channel groups.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DioPortId
  长名称: ''
  描述: Numeric identifier of the DIO port. Not all MCU ports may be used for DIO, thus there may be
      "gaps" in the list of all IDs. This value will be
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 3. DioChannel

**描述**: Configuration of an individual DIO channel. Besides a HW specific channel name which is typically
fixed for a specific micro controller, additional symbolic names can be defined per channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DioChannelId
  长名称: ''
  描述: Channel Id of the DIO channel. This value will be assigned to the symbolic names.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 4. DioChannelGroup

**描述**: Definition and configuration of DIO channel groups. A channel group represents several adjoining DIO
channels represented by a logical group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DioChannelGroupIdentification
  长名称: ''
  描述: The DIO channel group is identified in DIO API by a pointer to a data structure (of type
      Dio_ChannelGroupType). That data structure contains the channel group information.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DioPortMask
  长名称: ''
  描述: This shall be the mask which defines the positions of the channel
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: DioPortOffset
  长名称: ''
  描述: The position of the Channel Group on the port, counted
  默认值: ''
  最小值: 0
  最大值: 31
```

### 5. DioGeneral

**描述**: General DIO module configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DioDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DioFlipChannelApi
  长名称: ''
  描述: Adds / removes the service Dio_FlipChannel() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DioVersionInfoApi
  长名称: ''
  描述: Adds / removes the service Dio_ GetVersionInfo() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
```

