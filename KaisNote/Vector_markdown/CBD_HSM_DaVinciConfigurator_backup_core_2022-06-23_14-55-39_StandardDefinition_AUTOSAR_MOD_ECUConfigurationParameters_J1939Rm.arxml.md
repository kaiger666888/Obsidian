# J1939Rm

## 模块描述

The SAE J1939 Nm module

## 容器列表

### 1. J1939RmConfigSet

**描述**: This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist
once per configuration set.

该容器没有参数。

### 2. J1939RmChannel

**描述**: Contains the parameters for a CAN channel supported by the J1939 Request Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939RmAckQueueSize
  长名称: ''
  描述: Number of transmitted acknowledgements that can be stored.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: J1939RmRequestQueueSize
  长名称: ''
  描述: Number of transmitted requests that can be stored.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: J1939RmRequestTimeoutMonitors
  长名称: ''
  描述: Number of transmitted requests that can be monitored for timeout.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 3. J1939RmAckmRxPdu

**描述**: Contains the configuration of the I-PDU used to receive the Acknowledgement PG.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939RmAckmRxPduId
  长名称: ''
  描述: The I-PDU identifier used for RxIndication from PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 4. J1939RmAckmTxPdu

**描述**: Contains the configuration of the I-PDU used to transmit the Acknowledgement PG.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939RmAckmTxPduId
  长名称: ''
  描述: The I-PDU identifier used for TxConfirmation from PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 5. J1939RmRqstRxPdu

**描述**: Contains the configuration of the I-PDU used to receive the Request PG.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939RmRqstRxPduId
  长名称: ''
  描述: The I-PDU identifier used for RxIndication from PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 6. J1939RmRqstTxPdu

**描述**: Contains the configuration of the I-PDU used to transmit the Request PG.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939RmRqstTxPduId
  长名称: ''
  描述: The I-PDU identifier used for TxConfirmation from PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 7. J1939RmNode

**描述**: Contains the parameters for the support of a logical J1939 node (identified by an ECU address).

该容器没有参数。

### 8. J1939RmUser

**描述**: Contains the configuration of a module that uses the request and acknowledgement interfaces of
J1939Rm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939RmUserAckIndication
  长名称: ''
  描述: Enable AckIndication for this module. In case of CDD, the name is
      <apiServicePrefix>_AckIndication. In case of RTE, the port is defined as
      J1939RmRPort<J1939RmUserId>, and the operation is called AckIndication. This parameter
      shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, or
      J1939RM_USER_COM.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: J1939RmUserAckPGN
  长名称: ''
  描述: PGN supported to be acknowledged to this module. The PGNs supported by different modules
      should usually be disjunctive. This parameter shall not be set for J1939RmUserType
      J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, and J1939RM_USER_COM.
  默认值: ''
  最小值: 0
  最大值: 262143
- 
  序号: 3
  名称: J1939RmUserComIPduRequestQueueSize
  长名称: ''
  描述: Number of received requests that can be stored for COM I-PDUs of this user.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: J1939RmUserId
  长名称: ''
  描述: Identifier used by a module using J1939Rm. This parameter is only required when the module
      uses transmission of requests.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: J1939RmUserPGN
  长名称: ''
  描述: PGN supported to be requested from this module. The PGNs supported by different modules should
      usually be disjunctive. This parameter is predefined to AC (0x0EE00) for J1939RmUserType
      J1939RM_USER_J1939NM and is derived from the J1939Dcm PDUs in the system description for
      J1939RmUserType J1939RM_USER_J1939DCM. It shall not be set for J1939RmUserType
      J1939RM_USER_COM.
  默认值: ''
  最小值: 0
  最大值: 262143
- 
  序号: 6
  名称: J1939RmUserRequestIndication
  长名称: ''
  描述: Enable RequestIndication for this module. In case of J1939Nm or J1939Dcm, the name is fixed.
      In case of CDD, the name is <apiServicePrefix>_RequestIndication. In case of RTE, the
      port is defined as J1939RmRPort<J1939RmUserId>, and the operation is called
      RequestIndication. This parameter shall not be set for J1939RmUserType J1939RM_USER_COM.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: J1939RmUserSendAck
  长名称: ''
  描述: Enable the SendAck API for this module. In case of RTE, the port is defined as
      J1939RmPPort<J1939RmUserId>, and the operation is called SendAck. This parameter shall
      not be set for J1939RmUserType J1939RM_USER_J1939NM or J1939RM_USER_COM.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: J1939RmUserSendRequest
  长名称: ''
  描述: Enable the SendRequest API for this module. In case of RTE, the port is defined as
      J1939RmPPort<J1939RmUserId>, and the operation is called SendRequest. This parameter
      shall not be set for J1939RmUserType J1939RM_USER_J1939NM, J1939RM_USER_J1939DCM, or
      J1939RM_USER_COM.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: J1939RmUserTimeoutSupervision
  长名称: ''
  描述: Enable RequestTimeoutIndication and CancelRequestTimeout for this module.
      RequestTimeoutIndication: In case of CDD, the name is
      <apiServicePrefix>_RequestTimeoutIndication.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: J1939RmUserType
  长名称: ''
  描述: Type of module using J1939Rm.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. J1939RmComIPdu

**描述**: Contains the configuration of an I-PDU that is to be transmitted on request by COM. This
configuration container is only relevant for J1939RmUserType J1939RM_USER_COM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939RmComIPduDA
  长名称: ''
  描述: Destination address of the COM I-PDU.
  默认值: ''
  最小值: 0
  最大值: 253
- 
  序号: 2
  名称: J1939RmComIPduPGN
  长名称: ''
  描述: PGN of the COM I-PDU.
  默认值: ''
  最小值: 0
  最大值: 262143
- 
  序号: 3
  名称: J1939RmComIPduSA
  长名称: ''
  描述: Source address of the COM I-PDU.
  默认值: ''
  最小值: 0
  最大值: 253
```

### 10. J1939RmLowerComIPdu

**描述**: Contains the configuration of the I-PDU that is sent from J1939Rm to CanIf or J1939Tp.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939RmLowerComIPduId
  长名称: ''
  描述: The I-PDU identifier used for communication with PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 11. J1939RmUpperComIPdu

**描述**: Contains the configuration of the I-PDU that is sent from COM to J1939Rm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939RmUpperComIPduId
  长名称: ''
  描述: The I-PDU identifier used for communication with PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 12. J1939RmGeneral

**描述**: Contains the general configuration parameters of the module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939RmDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling development error detection support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: J1939RmMainFunctionPeriod
  长名称: ''
  描述: Execution cycle of J1939Rm_MainFunction in seconds.
  默认值: ''
  最小值: 0.001
  最大值: 0.255
- 
  序号: 3
  名称: J1939RmSupportAckIndication
  长名称: ''
  描述: Pre-processor switch for enabling support of acknowledgement indications.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: J1939RmSupportAckTransmission
  长名称: ''
  描述: Pre-processor switch for enabling support of acknowledgement transmission.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: J1939RmSupportRequestIndication
  长名称: ''
  描述: Pre-processor switch for enabling support of request indications.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: J1939RmSupportRequestTransmission
  长名称: ''
  描述: Pre-processor switch for enabling support of request transmission.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: J1939RmSupportTimeoutSupervision
  长名称: ''
  描述: Pre-processor switch for enabling support of request timeout supervision.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: J1939RmTxConfirmationTimeout
  长名称: ''
  描述: Time in seconds to wait for a confirmation after transmission of a message. The behaviour when
      the time elapses depends on the transmitted message.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 9
  名称: J1939RmVersionInfoApi
  长名称: ''
  描述: Pre-processor switch for enabling version info API support.
  默认值: ''
  最小值: ''
  最大值: ''
```

