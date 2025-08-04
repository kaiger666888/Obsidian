# EthTrcv

## 模块描述

Configuration of Ethernet Transceiver Driver module

## 容器列表

### 1. EthTrcvConfigSet

**描述**: All underlying parameters may be part of a multiple configuration set.

该容器没有参数。

### 2. EthTrcvConfig

**描述**: Configuration of the individual transceiver

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTrcvAutoNegotiationEnabled
  长名称: ''
  描述: Specifies if Auto-Negotiation is enabled (TRUE) or disabled (FALSE) for determination of the
      Ethernet transceiver speed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthTrcvCtrlIdx
  长名称: ''
  描述: Specifies the controller used for MII access to the transceiver
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: EthTrcvDuplexMode
  长名称: ''
  描述: Specifies the duplex mode of the Ethernet transceiver link if Auto-Negotiation is disabled.
      This parameter is ignored if Auto-Negotiation is enabled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthTrcvIdx
  长名称: ''
  描述: Specifies the instance ID of the configured transceiver.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: EthTrcvMiiIdx
  长名称: ''
  描述: Specifies the transceiver index used for MII access to the transceiver
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: EthTrcvSpeed
  长名称: ''
  描述: Specifies the speed of the Ethernet transceiver link in [MBit/s]. If AutoNegotiation is
      enabled this is the maximum speed advertised for Auto-Negotiation.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. EthTrcvDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 4. EthTrcvGeneral

**描述**: General configuration of Ethernet Transceiver Driver module

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTrcvDevErrorDetect
  长名称: ''
  描述: Enables / Disables development error detection
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthTrcvGetBaudRateApi
  长名称: ''
  描述: Enables / Disables EthTrcv_GetBaudRate API
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTrcvGetDuplexModeApi
  长名称: ''
  描述: Enables / Disables EthTrcv_GetDuplexMode API
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthTrcvGetLinkStateApi
  长名称: ''
  描述: Enables / Disables EthTrcv_GetLinkState API
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthTrcvGetTransceiverModeApi
  长名称: ''
  描述: Enables / Disables EthTrcv_GetTransceiverMode API
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthTrcvIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: EthTrcvMaxTrcvsSupported
  长名称: ''
  描述: ''
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: EthTrcvSetTransceiverModeApi
  长名称: ''
  描述: Enables / Disables EthTrcv_SetTransceiverMode API
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EthTrcvStartAutoNegotiationApi
  长名称: ''
  描述: Enables / Disables EthTrcv_StartAutoNegotiation API
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthTrcvVersionInfoApi
  长名称: ''
  描述: Enables / Disables version info API
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EthTrcvVersionInfoApiMacro
  长名称: ''
  描述: Enables / Disables version info API macro implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

