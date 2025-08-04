# Dio

## 模块描述

Configuration of the Dio (Digital IO) module.

## 容器列表

### 1. DioConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR DIO module.

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
  默认值: 0
  最小值: 0
  最大值: 40
```

### 3. DioChannel

**描述**: Configuration of an individual DIO channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DioChannelId
  长名称: ''
  描述: Channel Id of the DIO channel. This value will be assigned to the symbolic names.
  默认值: 0
  最小值: 0
  最大值: 15
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
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: DioPortOffset
  长名称: ''
  描述: The position of the Channel Group on the port, counted
  默认值: 0
  最小值: 0
  最大值: 15
```

### 5. DioGeneral

**描述**: General DIO module configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DioDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DioFlipChannelApi
  长名称: ''
  描述: Adds / removes the service Dio_FlipChannel() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DioVersionInfoApi
  长名称: ''
  描述: Adds / removes the service Dio_ GetVersionInfo() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DioSafetyEnable
  长名称: ''
  描述: Enable/Disable the Safety check and all associated notifications.
  默认值: true
  最小值: ''
  最大值: ''
```

### 6. CommonPublishedInformation

**描述**: Common container, aggregated by all modules. It contains published information about vendor and
versions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArMajorVersion
  长名称: ''
  描述: Major version number of AUTOSAR specification on which the appropriate implementation is based
      on.
  默认值: 4
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: ArMinorVersion
  长名称: ''
  描述: Minor version number of AUTOSAR specification on which the appropriate implementation is based
      on.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: ArPatchVersion
  长名称: ''
  描述: Patch level version number of AUTOSAR specification on which the appropriate implementation is
      based on.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: SwMajorVersion
  长名称: ''
  描述: Major version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 10
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: SwMinorVersion
  长名称: ''
  描述: Minor version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 40
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: SwPatchVersion
  长名称: ''
  描述: Patch level version number of the vendor specific implementation of the module. The numbering
      is vendor specific.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: ModuleId
  长名称: ''
  描述: Module ID of this module from Module List
  默认值: 120
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: VendorId
  长名称: ''
  描述: Vendor ID of the dedicated implementation of this module according to the AUTOSAR vendor list
  默认值: 17
  最小值: 0
  最大值: 65535
- 
  序号: 9
  名称: Release
  长名称: ''
  描述: Aurix2G derivative used for the implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

