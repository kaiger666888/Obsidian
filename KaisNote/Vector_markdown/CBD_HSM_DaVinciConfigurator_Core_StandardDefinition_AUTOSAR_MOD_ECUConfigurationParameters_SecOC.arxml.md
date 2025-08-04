# SecOC

## 模块描述

Configuration of the SecOC (SecureOnboardCommunication) module.

## 容器列表

### 1. SecOCGeneral

**描述**: Contains the general configuration parameters of the SecOC module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCDevErrorDetect
  长名称: ''
  描述: Switches the development error detection and notification on or off.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SecOCEnableForcedPassOverride
  长名称: ''
  描述: When this configuration option is set to TRUE then the functionality inside the function
      SecOC_VerifyStatusOverride to forcibly override the VerifyStatus to "Pass" is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SecOcIgnoreVerificationResult
  长名称: ''
  描述: The result of the authentication process (e.g. MAC Verify) is ignored after the first try and
      the SecOC proceeds like the result was a success. The calculation of the authenticator
      is still done, only its result will be ignored.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SecOCMainFunctionPeriodRx
  长名称: ''
  描述: Allows to configure the time for the MainFunction of the Rx path (as float in seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 5
  名称: SecOCMainFunctionPeriodTx
  长名称: ''
  描述: Allows to configure the time for the MainFunction of the Tx path (as float in seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 6
  名称: SecOCMaxAlignScalarType
  长名称: ''
  描述: The scalar type which has the maximum alignment restrictions on the given platform. This type
      can be e.g. uint8, uint16 or uint32.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SecOCQueryFreshnessValue
  长名称: ''
  描述: This parameter specifies if the freshness value shall be determined through a C-function (CD)
      or a software component (SW-C).
  默认值: CFUNC
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SecOCVerificationStatusCallout
  长名称: ''
  描述: Entry address of the customer specific call out routine which shall be invoked in case of a
      verification attempt.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SecOCVersionInfoApi
  长名称: ''
  描述: If true the SecOC_GetVersionInfo API is available.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. SecOCRxPduProcessing

**描述**: Contains the parameters to configure the RxPdus to be verified by the SecOC module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCAuthDataFreshnessLen
  长名称: ''
  描述: The length of the external authentic PDU data in bits (uint16).
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: SecOCAuthDataFreshnessStartPosition
  长名称: ''
  描述: This value determines the start position in bits (uint16) of the Authentic PDU that shall be
      passed on to the Freshness SWC. The bit position starts counting from the MSB of the
      first byte of the PDU.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 3
  名称: SecOCAuthenticationBuildAttempts
  长名称: ''
  描述: This parameter specifies the number of authentication build attempts.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: SecOCAuthenticationVerifyAttempts
  长名称: ''
  描述: This parameter specifies the number of authentication verify attempts that are to be carried
      out when the verification of the authentication information failed for a given Secured
      I-PDU. If zero is set, then only one authentication verification attempt is done.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: SecOCAuthInfoTxLength
  长名称: ''
  描述: This parameter defines the length in bits of the authentication code to be included in the
      payload of the Secured I-PDU.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: SecOCDataId
  长名称: ''
  描述: This parameter defines a unique numerical identifier for the Secured I-PDU.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: SecOCFreshnessValueId
  长名称: ''
  描述: This parameter defines the Id of the Freshness Value.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: SecOCFreshnessValueLength
  长名称: ''
  描述: This parameter defines the complete length in bits of the Freshness Value. As long as the key
      doesn't change the counter shall not overflow. The length of the counter shall be
      determined based on the expected life time of the corresponding key and frequency of
      usage of the counter.
  默认值: ''
  最小值: 0
  最大值: 64
- 
  序号: 9
  名称: SecOCFreshnessValueTxLength
  长名称: ''
  描述: This parameter defines the length in bits of the Freshness Value to be included in the payload
      of the Secured I-PDU. This length is specific to the least significant bits of the
      complete Freshness Counter. If the parameter is 0 no Freshness Value is included in the
      Secured I-PDU.
  默认值: ''
  最小值: 0
  最大值: 64
- 
  序号: 10
  名称: SecOCReceptionOverflowStrategy
  长名称: ''
  描述: This parameter defines the overflow strategy for receiving PDUs
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SecOCReceptionQueueSize
  长名称: ''
  描述: This parameter defines the queue size in case the overflow strategy for receiving PDUs is set
      to QUEUE.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 12
  名称: SecOCUseAuthDataFreshness
  长名称: ''
  描述: A Boolean value that indicates if a part of the Authentic-PDU shall be passed on to the SWC
      that verifies and generates the Freshness. If it is set to TRUE, the values
      SecOCAuthDataFreshnessStartPosition and SecOCAuthDataFreshnessLen must be set to specify
      the bit position and length within the Authentic-PDU.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: SecOCVerificationStatusPropagationMode
  长名称: ''
  描述: This parameter is used to describe the propagation of the status of each verification attempt
      from the SecOC module to SWCs.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. SecOCRxAuthenticPduLayer

**描述**: This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac
was verified.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCPduType
  长名称: ''
  描述: This parameter defines API Type to use for communication with PduR.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. SecOCRxSecuredPdu

**描述**: This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu
the Mac verification is provided.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCRxSecuredLayerPduId
  长名称: ''
  描述: PDU identifier assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 5. SecOCRxSecuredPduCollection

**描述**: This container specifies two Pdus that are received by the SecOC module from the PduR and a message
linking between them.

该容器没有参数。

### 6. SecOCRxAuthenticPdu

**描述**: This container specifies the Authetic Pdu that is received by the SecOC module from the PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCRxAuthenticPduId
  长名称: ''
  描述: PDU identifier of the Authentic I-PDU assigned by SecOC module. Used by PduR for
      SecOC_PduRRxIndication.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 7. SecOCRxCryptographicPdu

**描述**: This container specifies the Cryptographic Pdu that is received by the SecOC module from the PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCRxCryptographicPduId
  长名称: ''
  描述: PDU identifier of the Cryptographic I-PDU assigned by SecOC module. Used by PduR for
      SecOC_PduRRxIndication.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 8. SecOCUseMessageLink

**描述**: SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part
(Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCMessageLinkLen
  长名称: ''
  描述: Length of the Message Linker inside the Authentic I-PDU in bits.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SecOCMessageLinkPos
  长名称: ''
  描述: The position of the Message Linker inside the Authentic I-PDU in bits.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 9. SecOCSameBufferPduCollection

**描述**: SecOCBuffer configuration that may be used by a collection of Pdus.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCBufferLength
  长名称: ''
  描述: This parameter defines the Buffer in bytes that is used by the SecOC module.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 10. SecOCTxPduProcessing

**描述**: Contains the parameters to configure the TxPdus to be secured by the SecOC module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCAuthenticationBuildAttempts
  长名称: ''
  描述: This parameter specifies the number of authentication build attempts.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SecOCAuthInfoTxLength
  长名称: ''
  描述: This parameter defines the length in bits of the authentication code to be included in the
      payload of the Secured I-PDU.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: SecOCDataId
  长名称: ''
  描述: This parameter defines a unique numerical identifier for the Secured I-PDU.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: SecOCFreshnessValueId
  长名称: ''
  描述: This parameter defines the Id of the Freshness Value.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: SecOCFreshnessValueLength
  长名称: ''
  描述: This parameter defines the complete length in bits of the Freshness Value. As long as the key
      doesn't change the counter shall not overflow. The length of the counter shall be
      determined based on the expected life time of the corresponding key and frequency of
      usage of the counter.
  默认值: ''
  最小值: 0
  最大值: 64
- 
  序号: 6
  名称: SecOCFreshnessValueTxLength
  长名称: ''
  描述: This parameter defines the length in bits of the Freshness Value to be included in the payload
      of the Secured I-PDU. This length is specific to the least significant bits of the
      complete Freshness Counter. If the parameter is 0 no Freshness Value is included in the
      Secured I-PDU.
  默认值: ''
  最小值: 0
  最大值: 64
- 
  序号: 7
  名称: SecOCProvideTxTruncatedFreshnessValue
  长名称: ''
  描述: This parameter specifies if the Tx query freshness function provides the truncated freshness
      info instead of generating this by SecOC In this case, SecOC shall add this data to the
      Authentic PDU instead of truncating the freshness value.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SecOCUseTxConfirmation
  长名称: ''
  描述: A Boolean value that indicates if the function SecOC_SPduTxConfirmation shall be called for
      this PDU.
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. SecOCTxAuthenticPduLayer

**描述**: This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu
the Mac generation is provided.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCPduType
  长名称: ''
  描述: This parameter defines API Type to use for communication with PduR.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SecOCTxAuthenticLayerPduId
  长名称: ''
  描述: PDU identifier assigned by SecOC module. Used by PduR for SecOC_PduRTransmit.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 12. SecOCTxSecuredPdu

**描述**: This container specifies one Pdu that is transmitted by the SecOC module to the PduR after the Mac
was generated. This Pdu contains the cryptographic information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCTxSecuredLayerPduId
  长名称: ''
  描述: PDU identifier assigned by SecOC module. Used by PduR for confirmation
      (SecOC_PduRTxConfirmation) and for TriggerTransmit.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 13. SecOCTxSecuredPduCollection

**描述**: This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac
was generated. Two separate Pdus are transmitted to the PduR:

该容器没有参数。

### 14. SecOCTxAuthenticPdu

**描述**: This container specifies the Authetic Pdu that is transmitted by the SecOC module to the PduR after
the Mac was generated.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCTxAuthenticPduId
  长名称: ''
  描述: PDU identifier of the Authentic I-PDU assigned by SecOC module. Used by PduR for confirmation
      (SecOC_PduRTxConfirmation) and for TriggerTransmit.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 15. SecOCTxCryptographicPdu

**描述**: This container specifies the Cryptographic Pdu that is transmitted by the SecOC module to the PduR
after the Mac was generated.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCTxCryptographicPduId
  长名称: ''
  描述: PDU identifier of the Cryptographic I-PDU assigned by SecOC module. Used by PduR for
      confirmation (SecOC_PduRTxConfirmation) and for TriggerTransmit.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 16. SecOCUseMessageLink

**描述**: SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part
(Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCMessageLinkLen
  长名称: ''
  描述: Length of the Message Linker inside the Authentic I-PDU in bits.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SecOCMessageLinkPos
  长名称: ''
  描述: The position of the Message Linker inside the Authentic I-PDU in bits.
  默认值: ''
  最小值: 0
  最大值: 65535
```

