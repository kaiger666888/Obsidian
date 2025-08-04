# EthSM

## 模块描述

Configuration of the Ethernet State Manager

## 容器列表

### 1. EthSMGeneral

**描述**: This container contains the global parameter of the Ethernet State Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSMDevErrorDetect
  长名称: ''
  描述: Enables and disables the development error detection and notification mechanism.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthSMDummyMode
  长名称: ''
  描述: Disables the API to the EthIf. The API to the ComM is available but the functionality is
      deactivated. The function calls from the ComM will be answered with the return value
      E_OK.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthSMMainFunctionPeriod
  长名称: ''
  描述: Specifies the period in seconds that the MainFunction has to be triggered with.
  默认值: ''
  最小值: 0.005
  最大值: 1
- 
  序号: 4
  名称: EthSMVersionInfoApi
  长名称: ''
  描述: Enables and disables the version info API.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. EthSMNetwork

**描述**: This container contains the Ethernet network-specific parameters of each Ethernet network. It also
contains the controller and transceiver IDs assigned to a Ethernet network.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSMConfirmationTimeout
  长名称: ''
  描述: Timeout in seconds for the calls to EthIf:
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 3. EthSMDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

