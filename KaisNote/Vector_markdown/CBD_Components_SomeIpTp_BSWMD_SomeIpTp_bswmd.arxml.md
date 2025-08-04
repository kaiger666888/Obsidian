# SomeIpTp

## 模块描述

SOME/IP Transport Protocol. SOME/IP TP module segments SOME/IP packets, which do not fit into one
single UDP packet. On the reception side, it assembles the received SOME/IP segments.

#TP #Ethernet #SOMEIP
#AUTOSAR

## 容器列表

### 1. SomeIpTpChannel

**描述**: This container contains the configuration parameters of the SomeIpTp channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SomeIpTpNPduSeparationTime
  长名称: ''
  描述: Sets the duration of the minimum time in seconds the SomeIpTp module shall wait between the
      transmissions of N-PDUs.
  默认值: 0.001
  最小值: 0
  最大值: 65.535
- 
  序号: 2
  名称: SomeIpTpRxTimeoutTime
  长名称: ''
  描述: |
    Timer to monitor the successful reception. It is started when the first NPdu
    is received, restarted after reception of intermediate NPdus, and is stopped when the last NPdu
    has been received.
  默认值: 0.5
  最小值: 0
  最大值: 65.535
- 
  序号: 3
  名称: SomeIpTpTxConfTimeoutTime
  长名称: Tx Confirmation Timeout Time
  描述: Timer to monitor the successful Transmission Confirmation. It is started when the NPdu is
      triggered and is stopped when the Confirmation has been received.
  默认值: 0.5
  最小值: 0
  最大值: 65.535
```

### 2. SomeIpTpRxNSdu

**描述**: The following parameters needs to be configured for each N-SDU which has to be passed as one
assembled RxPdu to the upper layer.

该容器没有参数。

### 3. SomeIpTpRxNPdu

**描述**: This container contains the configuration parameters of the NPdu that is received from a lower layer

#### 参数列表

```yaml
- 
  序号: 1
  名称: SomeIpTpRxNPduHandleId
  长名称: ''
  描述: This parameter defines the handle ID that is used by the PduR when calling
      SomeIpTp_RxIndication.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 4. SomeIpTpTxNSdu

**描述**: The following parameters needs to be configured for each N-SDU that the SomeIpTp module transmits
via the SomeIpTpChannel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SomeIpTpTxNSduHandleId
  长名称: ''
  描述: This parameter defines the handle ID of the NSdu that represents the original TxSdu which is
      segmented and passed via the PduR to the lower layer. This handle ID is used by PduR
      when calling SomeIpTp_Transmit.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SomeIpTpTxBurstSize
  长名称: ''
  描述: Number of SomeIpTp segments transmitted consecutively in the SomeIpTp mainfunction without
      waiting for separation time.
  默认值: 1
  最小值: 1
  最大值: 255
```

### 5. SomeIpTpTxNPdu

**描述**: This container contains the configuration parameters of the segmented Tx NPdus that are transmitted
to a lower layer.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SomeIpTpTxNPduHandleId
  长名称: ''
  描述: This parameter defines the handle ID that is used by PduR when calling
      SomeIpTp_TriggerTransmit.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 6. SomeIpTpGeneral

**描述**: This container contains the general configuration parameters of the SomeIpTp module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SomeIpTpDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SomeIpTpRxMainFunctionPeriod
  长名称: ''
  描述: This parameter defines the cycle time in seconds of the periodic call of the
      SomeIpTp_MainFunctionRx.
  默认值: 0.001
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 3
  名称: SomeIpTpTxMainFunctionPeriod
  长名称: ''
  描述: This parameter defines the cycle time in seconds of the periodic call of the
      SomeIpTp_MainFunctionTx.
  默认值: 0.001
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 4
  名称: SomeIpTpVersionInfoApi
  长名称: ''
  描述: Activates the SomeIpTp_GetVersionInfo() API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SomeIpTpRuntimeErrorReport
  长名称: ''
  描述: Switches the Runtime Error Notification ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SomeIpTpUserConfigFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation to SomeIpTp_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SomeIpTpSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
```

