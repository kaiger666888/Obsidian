# LinTp

## 模块描述

Singleton descriptor for the LIN Transport Protocol.

## 容器列表

### 1. LinTpGeneral

**描述**: Container that holds all LIN transport protocol general parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinTpVersionInfoApi
  长名称: ''
  描述: Switches the LinTp_GetVersionInfo function ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. LinTpGlobalConfig

**描述**: This container contains the global configuration parameter of the LinTp.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinTpMaxNumberOfRespPendingFrames
  长名称: ''
  描述: Configures the maximum number of allowed response pending frames.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: LinTpNumberOfRxNSdu
  长名称: ''
  描述: Number of transport protocol messages that can be received for all channels this node is
      connected to.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: LinTpNumberOfTxNSdu
  长名称: ''
  描述: Number of transport protocol messages that can be transmitted for all channels this node is
      connected to.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: LinTpP2Max
  长名称: ''
  描述: P2 Timeout when a response pending frame is expected in seconds.
  默认值: ''
  最小值: 0
  最大值: 5
- 
  序号: 5
  名称: LinTpP2Timing
  长名称: ''
  描述: Definition of the P2 timeout observation parameter in seconds.
  默认值: ''
  最小值: 0
  最大值: 5
```

### 3. LinTpChannelConfig

**描述**: This container contains the channel specific configuration parameter of LinTp.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinTpDropNotRequestedNad
  长名称: ''
  描述: Configures if TP Frames of not requested LIN-Slaves are dropped or not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: LinTpScheduleChangeDiag
  长名称: ''
  描述: Enables or disables the call of BswM_LinTp_RequestMode() to diagnostic request/response
      schedule.
  默认值: false
  最小值: ''
  最大值: ''
```

### 4. LinTpRxNSdu

**描述**: For each received N-SDU on any channel the node is connected to.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinTpDl
  长名称: ''
  描述: Data Length Code of this RxNsdu. In case of variable length message, this value indicates the
      minimum data length.
  默认值: ''
  最小值: 1
  最大值: 4095
- 
  序号: 2
  名称: LinTpNcr
  长名称: ''
  描述: Value in seconds of the N_Cr timeout. N_Cr is the time until reception of the next Consecutive
      Frame N_PDU.
  默认值: ''
  最小值: 0
  最大值: 1
- 
  序号: 3
  名称: LinTpRxNSduId
  长名称: ''
  描述: The identifier of the Transport Protocol message. This ID will be the one that is communicated
      with upper layers.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: LinTpRxNSduNad
  长名称: ''
  描述: A N-SDU transported on LIN is identified using the NAD for the specific slave.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 5. LinTpTxNSdu

**描述**: For each transmitted N-SDU on any channel the node is connected to.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinTpNas
  长名称: ''
  描述: Value in second of the N_As timeout. N_As is the time for transmission of a LIN frame (any
      N_PDU) on the part of the sender.
  默认值: ''
  最小值: 0
  最大值: 1
- 
  序号: 2
  名称: LinTpNcs
  长名称: ''
  描述: Value in seconds of the performance requirement of N_Cs. N_Cs is the time which elapses
      between the transmit request of a CF N-PDU until the transmit request of the next CF
      N-PDU.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: LinTpTxNSduId
  长名称: ''
  描述: The identifier of the Transport Protocol message. This ID will be the one that is communicated
      with upper layers.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: LinTpTxNSduNad
  长名称: ''
  描述: A N-SDU transported on LIN is identified using the NAD for the specific slave.
  默认值: ''
  最小值: 0
  最大值: 255
```

