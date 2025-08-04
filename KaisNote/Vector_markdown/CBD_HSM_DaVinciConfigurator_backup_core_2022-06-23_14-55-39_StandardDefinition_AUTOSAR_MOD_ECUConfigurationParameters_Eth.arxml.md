# Eth

## 模块描述

Configuration of the Eth (Ethernet Driver) module.

## 容器列表

### 1. EthConfigSet

**描述**: All included containers and parameters that may be part of a multiple configuration set.

该容器没有参数。

### 2. EthCtrlConfig

**描述**: Configuration of the individual controller

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthCtrlEnableMii
  长名称: ''
  描述: Enables / Disables Media Independent Interface (MII) for transceiver access
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthCtrlEnableRxInterrupt
  长名称: ''
  描述: Enables / Disables receive interrupt
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthCtrlEnableTxInterrupt
  长名称: ''
  描述: Enables / Disables transmit interrupt
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthCtrlIdx
  长名称: ''
  描述: Specifies the instance ID of the configured controller.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: EthCtrlPhyAddress
  长名称: ''
  描述: Specifies the unique 48-bit physical address (MAC address) of the controller in network byte
      order.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthCtrlRxBufLenByte
  长名称: ''
  描述: Limits the maximum receive buffer length (frame length) in bytes.
  默认值: ''
  最小值: 0
  最大值: 1522
- 
  序号: 7
  名称: EthCtrlTxBufLenByte
  长名称: ''
  描述: Limits the maximum transmit buffer length (frame length) in bytes.
  默认值: ''
  最小值: 0
  最大值: 1522
- 
  序号: 8
  名称: EthRxBufTotal
  长名称: ''
  描述: Configures the number of receive buffers.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: EthTxBufTotal
  长名称: ''
  描述: Configures the number of transmit buffers.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 3. EthDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 4. EthGeneral

**描述**: General configuration of Ethernet Driver module

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthDevErrorDetect
  长名称: ''
  描述: Enables / Disables development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: EthMaxCtrlsSupported
  长名称: ''
  描述: Limits the total number of supported controllers.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 4
  名称: EthUpdatePhysAddrFilter
  长名称: ''
  描述: Enables/Disables optional API Eth_UpdatePhysAddrFilter.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthVersionInfoApi
  长名称: ''
  描述: Enables / Disables version info API
  默认值: ''
  最小值: ''
  最大值: ''
```

