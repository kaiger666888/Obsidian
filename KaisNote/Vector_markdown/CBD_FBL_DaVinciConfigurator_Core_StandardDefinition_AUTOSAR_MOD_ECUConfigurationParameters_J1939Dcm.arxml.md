# J1939Dcm

## 模块描述

The SAE J1939 Dcm module

## 容器列表

### 1. J1939DcmConfigSet

**描述**: This container contains the configuration parameters and sub containers of the J1939DCM module
supporting multiple configuration sets.

该容器没有参数。

### 2. J1939DcmChannel

**描述**: Contains the J1939DcmChannel parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939DcmBusType
  长名称: ''
  描述: Identifies the communication port
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. J1939DcmNode

**描述**: Contains the parameters for the support of a logical J1939 node (identified by an ECU address).

该容器没有参数。

### 4. J1939DcmDiagnosticMessageSupport

**描述**: Contains parameters to configure the diagnostic message support

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939DcmDmxSupport
  长名称: ''
  描述: This parameter is used to identify the actual DMx message.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. J1939DcmRxPdu

**描述**: Contains parameters to configure the J1939DcmRxPdu.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939DcmRxPduId
  长名称: ''
  描述: The I-PDU identifier used for communication with PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 6. J1939DcmTxPdu

**描述**: Contains parameters to configure the J1939DcmTxPdu.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939DcmTxPduId
  长名称: ''
  描述: The I-PDU identifier used to identify the Tx message.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 7. J1939DcmGeneral

**描述**: Contains the general configuration parameters of the module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939DcmCommonBufferSize
  长名称: ''
  描述: Size of common buffer (in Bytes). The buffer size should be as large as the longest command or
      response message.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: J1939DcmDM1BufferSize
  长名称: ''
  描述: Size of DM1 buffer (in Bytes). The buffer size should be as large as the longest DM1 response
      message.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: J1939DcmDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling development error detection support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: J1939DcmMainFunctionPeriod
  长名称: ''
  描述: Call cycle in seconds of J1939Dcm_MainFunction.
  默认值: ''
  最小值: 0.001
  最大值: 0.255
- 
  序号: 5
  名称: J1939DcmMaxDTCsPerMainFunction
  长名称: ''
  描述: Maximum threshold of DTCs filtered in a single MainFunction cycle.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 6
  名称: J1939DcmMaxFreezeFramesPerMainFunction
  长名称: ''
  描述: Maximum threshold of FreezeFrames filtered in a single MainFunction cycle.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 7
  名称: J1939DcmMaxRatiosPerMainFunction
  长名称: ''
  描述: Maximum threshold of Ratios filtered in a single MainFunction cycle.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 8
  名称: J1939DcmVersionInfoApi
  长名称: ''
  描述: Pre-processor switch for enabling version info API support.
  默认值: ''
  最小值: ''
  最大值: ''
```

