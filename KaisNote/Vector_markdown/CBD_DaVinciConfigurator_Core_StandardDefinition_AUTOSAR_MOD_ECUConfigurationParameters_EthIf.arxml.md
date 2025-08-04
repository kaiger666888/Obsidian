# EthIf

## 模块描述

Configuration of the EthIf (Ethernet Interface) module.

## 容器列表

### 1. EthIfConfigSet

**描述**: Collecting container for all parameters with post-build configuration classes.

该容器没有参数。

### 2. EthIfController

**描述**: This container contains the configuration of EthIfController.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfCtrlIdx
  长名称: ''
  描述: This parameter provides a zero-based consecutive index of the Ethernet Communication
      Controllers. Upper layer BSW modules and the EthIf itself use this index to identify a
      Ethernet CC.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: EthIfCtrlMtu
  长名称: ''
  描述: Specifies the maximum transmission unit (MTU) of the EthIfCtrl in [bytes].
  默认值: ''
  最小值: 64
  最大值: 9000
- 
  序号: 3
  名称: EthIfVlanId
  长名称: ''
  描述: A virtual-LAN is identified by this attribute according to IEEE 802.1Q.
  默认值: ''
  最小值: 0
  最大值: 4095
```

### 3. EthIfFrameOwnerConfig

**描述**: Configuration of Ethernet frame owner

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfFrameType
  长名称: ''
  描述: Selects the Ethernet frame type.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: EthIfOwner
  长名称: ''
  描述: Selects the owner of an Ethernet frame type. The owner is a zero based index into the callback
      function configuration 'EthIfRxIndicationConfig'. I.e. an Ethernet frame of type IPv4
      (0x800) at index 0 will call the first callback function configured in
      'EthIfRxIndicationConfig'.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 4. EthIfRxIndicationConfig

**描述**: Configuration of receive callback functions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfRxIndicationFunction
  长名称: ''
  描述: Specifies receive indication callback function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. EthIfTrcvLinkStateChgConfig

**描述**: Specifies link state change callback function

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfTrcvLinkStateChgFunction
  长名称: ''
  描述: Specifies link state change callback function
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. EthIfTxConfirmationConfig

**描述**: Configuration of transmit indication callback functions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfTxConfirmationFunction
  长名称: ''
  描述: Specifies transmit indication callback function
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. EthIfSwitch

**描述**: This container is used to globally index all hardware switches that are used by the Ethernet
Interface. The index may be used by upper layers like the DHCP server component as a unique
identifier when calling a Ethernet Interface API. Besides the global index a reference to a hardware
switch configuration container resides in this container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfSwitchIndex
  长名称: ''
  描述: This value specifies a globally unique index for each hardware Ethernet Switch that is used by
      the Ethernet Interface. The index is zero-based and incremented by one for each hardware
      switch.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 8. EthIfGeneral

**描述**: This container contains the general configuration parameters of the Ethernet Interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIfDevErrorDetect
  长名称: ''
  描述: Enables / Disables development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthIfEnableRxInterrupt
  长名称: ''
  描述: Enables / Disables receive interrupt.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthIfEnableTxInterrupt
  长名称: ''
  描述: Enables / Disables the transmit interrupt.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthIfGetBaudRate
  长名称: ''
  描述: Enables / Disables GetBaudRate API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthIfGetCounterState
  长名称: ''
  描述: Enables / Disables GetCounterState API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthIfMainFunctionPeriod
  长名称: ''
  描述: Specifies the period of main function EthIf_MainFunctionRx and EthIf_MainFunctionTx in
      seconds. Ethernet Interface does not require this information but the BSW scheduler.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 7
  名称: EthIfMainFunctionRxTimeout
  长名称: ''
  描述: Timeout in seconds after which the EthIf stops to receive frames in an EthIfMainFunctionRx
      period.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 8
  名称: EthIfMaxTrcvsTotal
  长名称: ''
  描述: Limits the total number of transceivers.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 9
  名称: EthIfMaxTxBufsTotal
  长名称: ''
  描述: Limits the total number of transmit buffers.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 10
  名称: EthIfPublicCddHeaderFile
  长名称: ''
  描述: Defines header files for callback functions which shall be included in case of CDDs. Range of
      characters is 1.. 32.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EthIfRxIndicationIterations
  长名称: ''
  描述: Maximum number of Ethernet frames per Ethernet controller polled from the Ethernet driver
      within EthIf_MainFunctionRx.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 12
  名称: EthIfStartAutoNegotiation
  长名称: ''
  描述: Enables / Disables StartAutoNegotiation API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: EthIfTrcvLinkStateChgMainReload
  长名称: ''
  描述: Specifies the frequency of transceiver link state change checks in each
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 14
  名称: EthIfVersionInfoApi
  长名称: ''
  描述: Enables / Disables version info API
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: EthIfVersionInfoApiMacro
  长名称: ''
  描述: Enables / Disables version info API macro implementation.
  默认值: ''
  最小值: ''
  最大值: ''
```

