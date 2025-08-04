# Port

## 模块描述

Configuration of the Port module.

## 容器列表

### 1. PortConfigSet

**描述**: This container is the base of a multiple configuration set

该容器没有参数。

### 2. PortContainer

**描述**: Container collecting the PortPins.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PortNumberOfPortPins
  长名称: ''
  描述: The number of specified PortPins in this PortContainer.
  默认值: ''
  最小值: 1
  最大值: 65535
```

### 3. PortPin

**描述**: Configuration of the individual port pins.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PortPinDirection
  长名称: ''
  描述: The initial direction of the pin (IN or OUT). If the direction is not changeable, the value
      configured here is fixed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PortPinDirectionChangeable
  长名称: ''
  描述: Parameter to indicate if the direction is changeable on a port pin during runtime.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PortPinId
  长名称: ''
  描述: Pin Id of the port pin. This value will be assigned to the symbolic name derived from the port
      pin container short name.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: PortPinInitialMode
  长名称: ''
  描述: Port pin mode from mode list for use with Port_Init() function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PortPinLevelValue
  长名称: ''
  描述: Port Pin Level value from Port pin list.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PortPinMode
  长名称: ''
  描述: Port pin mode from mode list.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: PortPinModeChangeable
  长名称: ''
  描述: Parameter to indicate if the mode is changeable on a port pin during runtime. True: Port Pin
      mode changeable allowed. False: Port Pin mode changeable not permitted.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. PortGeneral

**描述**: Module wide configuration parameters of the PORT driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PortDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification on or off.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PortSetPinDirectionApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the use of the function Port_SetPinDirection().
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PortSetPinModeApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the use of the function Port_SetPinMode().
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: PortVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information.
  默认值: ''
  最小值: ''
  最大值: ''
```

