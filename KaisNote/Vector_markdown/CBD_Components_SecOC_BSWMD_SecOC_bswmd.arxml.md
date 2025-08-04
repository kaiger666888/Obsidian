# SecOC

## 模块描述

The Secure Onboard Communication module provides a mechanism to authenticate and verify I-PDUs.

## 容器列表

### 1. SecOCGeneral

**描述**: Contains the general configuration parameters of the SecOC module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling development error detection support.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SecOCEnableForcedPassOverride
  长名称: ''
  描述: If SecOCEnableForcedPassOverride is set to true the API SecOC_VerifyStatusOverride accepts the
      overrideStatus Pass.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SecOcIgnoreVerificationResult
  长名称: ''
  描述: If set to true the result of the authentication process (e.g. MAC Verify) is ignored after the
      first try and the SecOC proceeds like the result was a success. The calculation of the
      authenticator is still done, only its result will be ignored.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SecOCMaxAlignScalarType
  长名称: ''
  描述: |
    The scalar type which has the maximum alignment restrictions on the given platform. This type
    can be e.g. uint8, uint16 or uint32.
    
    This parameter is NOT used by the generator.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SecOCQueryFreshnessValue
  长名称: ''
  描述: |
    This parameter specifies if the freshness value shall be determined through a C-function (CDD)
    or a software component (SW-C).
    
    RTE     The SecOC queries the freshness for every PDU to process using the Rte service port
    FreshnessManagement
    CFUNC   The SecOC queries the freshness for every PDU to process using C function.
  默认值: CFUNC
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SecOCVerificationStatusCallout
  长名称: ''
  描述: Entry address of the customer specific call out routine which shall be invoked in case of a
      verification attempt.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SecOCVersionInfoApi
  长名称: ''
  描述: If true the SecOC_GetVersionInfo API is available.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SecOCUserConfigFile
  长名称: ''
  描述: |
    Reference to an external user configuration file that will be included during generation.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SecOCMaxMessageLinkerSizeOfRxPdus
  长名称: ''
  描述: Max byte size of Message Linker used with Rx Secured Collection Pdus.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 10
  名称: SecOCSafeBswChecks
  长名称: ''
  描述: |
    Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
    are checked before function is executed.
    This attribute has to be enabled for safety projects where this component is mapped to an ASIL
    partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SecOCPropagateOnlyFinalVerificationStatus
  长名称: ''
  描述: This parameter Is used to specify if the verification status shall be reported only after the
      final determination of the verification status (TRUE) or on every verification attempt
      (FALSE).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: SecOCEnableDevelopmentMode
  长名称: ''
  描述: |
    If the Development Mode is enabled the API SecOC_SetDevelopmentMode(True/False) is available.
    If the Development Mode is started with the API SecOC_SetDevelopmentMode(True) all received Pdus
    will be forwared to the Upper Layer, even if the verifcation fails.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: SecOCUseGetRxFreshness
  长名称: ''
  描述: This parameter enables the useage of the GetRxFreshness API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: SecOCUseGetRxFreshnessAuthData
  长名称: ''
  描述: This parameter enables the useage of the GetRxFreshnessAuthData API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: SecOCUseGetTxFreshness
  长名称: ''
  描述: This parameter enables the useage of the GetTxFreshness API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: SecOCUseGetTxFreshnessTruncData
  长名称: ''
  描述: This parameter enables the useage of the GetTxFreshnessTruncData API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: SecOCUseSPduTxConfirmation
  长名称: ''
  描述: This parameter enables the useage of the SPduTxConfirmation API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: SecOCVerificationStatusCalloutWithSecuredPdu
  长名称: ''
  描述: |
    Entry address of the customer specific call out routine which shall be invoked in case of a
    verification attempt.
    Compared to the SecOCVerificationStatusCallout this callout contains more detailed information
    about the received secured PDU and the freshness value.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: SecOCDefaultAuthenticationInformationPattern
  长名称: ''
  描述: Defines the key pattern which is used in case the fvm or csm returns a non-recoverrable error
      and development mode is enabled.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 20
  名称: SecOCEnableCustomAuthenticationAPI
  长名称: ''
  描述: Enable to do the authentication and verification in a customer callout. The authentication
      info must be calculated by the user in this callout and must be written to the
      corresponding pointer.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: SecOCCanFdPadding
  长名称: ''
  描述: |
    Adds padding bytes after the MAC generation of a container PDU to prevent that the CAN driver
    adds padding bytes
    and removes the padding bytes before verification if TRUE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: SecOCRetryFailedTransmitRequest
  长名称: ''
  描述: Retry transmit if lower layer reports an error
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: SecOCUseMSBAlignedTruncatedFreshnessValueInFvM
  长名称: ''
  描述: |
    This Parameter defines if the truncated freshness value that is passed to the FvM is MSB aligned
    or if it is passed byte array is LSB aligned.
    true: The truncated freshness value is MSB aligend
    false: The truncated freshness value is LSB aligned/value aligned
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: SecOCEnableAsyncCSMJobTimeout
  长名称: ''
  描述: Enables the Timeout for asynchronous CSM Job calls.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. SecOCSecurityEventRefs

**描述**: Container for the references to IdsMEvent elements representing the security events that the SecOC
module shall report to the IdsM in case the coresponding security related event occurs (and if
SecOCEnableSecurityEventReporting is set to "true"). The standardized security events in this
container can be extended by vendor-specific security events.

该容器没有参数。

### 3. SecOCGeneration

**描述**: Contains the generation configuration parameters of the module SecOC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCOutOfBoundsWriteProtectionStrategy
  长名称: ''
  描述: |
    This parameter is used to configure a strategy to protect the code to write out of bounds.
    
    NONE: no protection strategy is generated in the data access.
    INDEX_SATURATION: arrays are blown up and the data access index is saturated by an appropriate
    mask. The advantage is the speed of the data access, but own data elements at other indexes of
    the same variable can be overridden.
    INDEX_CHECKING: the data access index is validated by a runtime check. The advantage is that
    values are never written to incorrect indexes of the data access.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SecOCOutOfBoundsWriteSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds write problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SecOCOutOfBoundsReadSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds read problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SecOCShortSymbols
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate shortened symbol names.
    
    FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant
    names.
    TRUE: symbol names are generated based on the MIP and a CRC32.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SecOCInterfacesForDeactivatedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate bsw data interfaces for
    deactivated data elements. This is an advantage for the BSW developer to reduce the time to
    market with a development environment using auto completition and to investigate potential
    interfaces.
    
    FALSE: data interfaces are not generated if the data elementis deactivated.
    TRUE: data interfaces are generated as e.g. emty macros.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SecOCReferringKeysInComments
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate referring keys in comments. This
    is an advantage for the developer to investigate indirections, but this feature reduces the
    overall readability of the generated data.
    
    FALSE: referring keys are not generated in comments.
    TRUE: referring keys are generated in comments.
  默认值: false
  最小值: ''
  最大值: ''
```

### 4. SecOCRxPduProcessing

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
  最大值: 65535
- 
  序号: 2
  名称: SecOCAuthDataFreshnessStartPosition
  长名称: ''
  描述: This value determines the start position in bits (uint16) of the Authentic PDU that shall be
      passed on to the Freshness SWC. The bit position starts counting from the MSB of the
      first byte of the PDU.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SecOCAuthenticationBuildAttempts
  长名称: ''
  描述: This parameter specifies the number of authentication build attempts.
  默认值: 1
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: SecOCAuthenticationVerifyAttempts
  长名称: ''
  描述: This parameter specifies the number of authentication verify attempts that are to be carried
      out when the verification of the authentication information failed for a given Secured
      I-PDU. If zero is set, then only one authentication verification attempt is done.
  默认值: 1
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
  默认值: 0
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
  最大值: 256
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
  最大值: 256
- 
  序号: 10
  名称: SecOCReceptionOverflowStrategy
  长名称: ''
  描述: |
    This parameter defines the overflow strategy for receiving PDUs
    
  默认值: REJECT
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SecOCReceptionQueueSize
  长名称: ''
  描述: This parameter defines the queue size in case the overflow strategy for receiving PDUs is set
      to QUEUE.
  默认值: 0
  最小值: 0
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
  描述: |
    This parameter is used to describe the propagation of the status of each verification attempt
    from the SecOC module to SWCs.
    
    BOTH: 'True' and 'False' verification status will be propagated.
    FAILURE_ONLY: Only 'False' verification status will be propagated,
    NONE: No verification status will be propagated.
    
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: SecOCVerificationStatusWithSecuredPduPropagationMode
  长名称: ''
  描述: |
    This parameter is used to describe the propagation of the status of each verification attempt
    from the SecOC module to SWCs.
    
    BOTH: 'True' and 'False' verification status will be propagated.
    FAILURE_ONLY: Only 'False' verification status will be propagated,
    NONE: No verification status will be propagated.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: SecOCImmediateProcessingOfCsmCallback
  长名称: ''
  描述: Enable, if the result of MACVerify/ MACGenerate shall be processed immediately in the context
      of the callback. This parameter is only relevant if CsmMacVerifyProcessing/
      CsmMacGenerateProcessing is set to CSM_ASYNCHRONOUS. If disabled, the result of the
      callback will be processed in the context of the respective main function.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: SecOCPduProcessing
  长名称: ''
  描述: |
    Processing type which determines if the request shall be processed within the interrupt context
    of the SecOC_RxIndication or within the task level of SecOC_MainFunctionRx.
    
    Set to
    - DEFERRED: Pdu is processed within the task context of the SecOC_MainFunctionRx API
    - IMMEDIATE: Pdu is processed within the interrupt context of the SecOC_RxIndication API
  默认值: DEFERRED
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: SecOCAsyncCSMJobTimeout
  长名称: ''
  描述: |
    Defines the maximum time the SecOC waits for an asynchronous CSM job to finish.
    If the timeout occurs the SecOC will cancel the CSM job and release the buffers inside the
    SecOC.
    If not configured or configured to 0 the SecOC waits infinit.
  默认值: 0
  最小值: 0
  最大值: 10
- 
  序号: 18
  名称: SecOCClientServerVerificationStatusPropagationMode
  长名称: ''
  描述: |
    This parameter is used to determine the propagation of the verification status through
    the client/server interface to an SW-C.
    
    BOTH Both "TRUE" and "FALSE" AuthenticationStatus is propagated to SW-C
    FAILURE_ONLY Only "FALSE" Authentication Status is propagated to SW-C
    NONE No Authentication Status for this PDU is provided to SW-C
  默认值: NONE
  最小值: ''
  最大值: ''
```

### 5. SecOCRxAuthenticPduLayer

**描述**: This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac
was verified.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCPduType
  长名称: ''
  描述: This parameter defines API Type to use for communication with PduR.
  默认值: SECOC_IFPDU
  最小值: ''
  最大值: ''
```

### 6. SecOCRxSecuredPdu

**描述**: This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu
the Mac verification is provided.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCRxSecuredLayerPduId
  长名称: ''
  描述: PDU identifier assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SecOCSecuredRxPduVerification
  长名称: ''
  描述: |
    If this parameter is set to FALSE no authentication of received secured PDU will be performed.
    - true: enabled  (verification result is NOT ignored).
    - false: disabled (verification result is ignored).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SecOCAuthPduHeaderLength
  长名称: ''
  描述: This parameter indicates the length (in bytes) of the Secured I-PDU Header in the Secured
      I-PDU. The length of zero means there's no header in the PDU.
  默认值: 0
  最小值: 0
  最大值: 4
```

### 7. SecOCRxSecuredPduCollection

**描述**: This container specifies two Pdus that are received by the SecOC module from the PduR and a message
linking between them.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCSecuredRxPduVerification
  长名称: ''
  描述: |
    If this parameter is set to FALSE no authentication of received secured PDU will be performed.
    - true: enabled (verification result is NOT ignored).
    - false: disabled (verification result is ignored).
  默认值: true
  最小值: ''
  最大值: ''
```

### 8. SecOCRxAuthenticPdu

**描述**: This container specifies the Authentic Pdu that is received by the SecOC module from the PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCRxAuthenticPduId
  长名称: ''
  描述: PDU identifier of the Authentic I-PDU assigned by SecOC module. Used by PduR for
      SecOC_PduRRxIndication.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SecOCAuthPduHeaderLength
  长名称: ''
  描述: This parameter indicates the length (in bytes) of the Secured I-PDU Header in the Secured
      I-PDU. The length of zero means there's no header in the PDU.
  默认值: 0
  最小值: 0
  最大值: 4
```

### 9. SecOCRxCryptographicPdu

**描述**: This container specifies the Cryptographic Pdu that is received by the SecOC module from the PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCRxCryptographicPduId
  长名称: ''
  描述: PDU identifier of the Cryptographic I-PDU assigned by SecOC module. Used by PduR for
      SecOC_PduRRxIndication.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 10. SecOCUseMessageLink

**描述**: SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part
(Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCMessageLinkLen
  长名称: ''
  描述: Length of the Message Linker inside the Authentic I-PDU in bits.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SecOCMessageLinkPos
  长名称: ''
  描述: The position of the Message Linker inside the Authentic I-PDU in bits.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 11. SecOCRxPduSecuredArea

**描述**: This container specifies an area in the Authentic I-Pdu that will be the input to the Authenticator
verification algorithm. If this container does not exist in the configuration the complete Authentic
I-Pdu will be the input to the Authenticator verification algorithm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCSecuredRxPduLength
  长名称: ''
  描述: This parameter defines the length (in bytes) of the area within the Pdu which is secured
  默认值: ''
  最小值: 0
  最大值: 4294967294
- 
  序号: 2
  名称: SecOCSecuredRxPduOffset
  长名称: ''
  描述: This parameter defines the start position (offset in bytes) of the area within the Pdu which
      is secured
  默认值: ''
  最小值: 0
  最大值: 4294967294
```

### 12. SecOCSameBufferPduCollection

**描述**: SecOCBuffer configuration that may be used by a collection of Pdus.
Note: This container is not used by the generator.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCBufferLength
  长名称: ''
  描述: |
    This parameter defines the Buffer in bytes that is used by the SecOC module.
    Note: This parameter is not used by the generator.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 13. SecOCTxPduProcessing

**描述**: Contains the parameters to configure the TxPdus to be secured by the SecOC module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCAuthenticationBuildAttempts
  长名称: ''
  描述: This parameter specifies the number of authentication build attempts.
  默认值: 1
  最小值: 1
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
  默认值: 0
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
  最大值: 256
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
  最大值: 256
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
- 
  序号: 9
  名称: SecOCAddCANFDContainerPduPadding
  长名称: ''
  描述: |
    If enabled the SecOC adds the CAN FD padding after the Pdu was authenticated.
    Pdu Layout:
    Authentic Pdu | Padding | Truncated Freshness Value | Truncated Authenticater
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: SecOCImmediateProcessingOfCsmCallback
  长名称: ''
  描述: Enable, if the result of MACVerify/ MACGenerate shall be processed immediately in the context
      of the callback. This parameter is only relevant if CsmMacVerifyProcessing/
      CsmMacGenerateProcessing is set to CSM_ASYNCHRONOUS. If disabled, the result of the
      callback will be processed in the context of the respective main function.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SecOCPduProcessing
  长名称: ''
  描述: |
    Processing type which determines if the request shall be processed within the context of
    SecOC_Transmit or within the task level of SecOC_MainFunctionTx.
    
    Set to
    - DEFERRED: Pdu is processed within the task context of the SecOC_MainFunctionTx API
    - IMMEDIATE: Pdu is processed within the interrupt context of the SecOC_Transmit API
  默认值: DEFERRED
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: SecOCAsyncCSMJobTimeout
  长名称: ''
  描述: |
    Defines the maximum time the SecOC waits for an asynchronous CSM job to finish.
    If the timeout occurs the SecOC will cancel the CSM job and release the buffers inside the
    SecOC.
    If not configured or configured to 0 the SecOC waits infinit.
  默认值: 0
  最小值: 0
  最大值: 10
```

### 14. SecOCTxAuthenticPduLayer

**描述**: This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu
the Mac generation is provided.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCPduType
  长名称: ''
  描述: This parameter defines API Type to use for communication with PduR.
  默认值: SECOC_IFPDU
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SecOCTxAuthenticLayerPduId
  长名称: ''
  描述: PDU identifier assigned by SecOC module. Used by PduR for SecOC_PduRTransmit.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 15. SecOCTxSecuredPdu

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
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SecOCPduType
  长名称: ''
  描述: This parameter defines API Type to use for communication with PduR.
  默认值: SECOC_IFPDU
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SecOCAuthPduHeaderLength
  长名称: ''
  描述: This parameter indicates the length (in bytes) of the Secured I-PDU Header in the Secured
      I-PDU. The length of zero means there's no header in the PDU.
  默认值: 0
  最小值: 0
  最大值: 4
```

### 16. SecOCTxSecuredPduCollection

**描述**: This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac
was generated. Two separate Pdus are transmitted to the PduR:

该容器没有参数。

### 17. SecOCTxAuthenticPdu

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
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SecOCAuthPduHeaderLength
  长名称: ''
  描述: This parameter indicates the length (in bytes) of the Secured I-PDU Header in the Secured
      I-PDU. The length of zero means there's no header in the PDU.
  默认值: 0
  最小值: 0
  最大值: 4
```

### 18. SecOCTxCryptographicPdu

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
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 19. SecOCUseMessageLink

**描述**: SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part
(Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCMessageLinkLen
  长名称: ''
  描述: Length of the Message Linker inside the Authentic I-PDU in bits.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SecOCMessageLinkPos
  长名称: ''
  描述: The position of the Message Linker inside the Authentic I-PDU in bits.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 20. SecOCTxPduSecuredArea

**描述**: This container specifies an area in the Authentic I-Pdu that will be the input to the Authenticator
generation algorithm. If this container does not exist in the configuration the complete Authentic
I-Pdu will be the input to the Authenticator generation algorithm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCSecuredTxPduLength
  长名称: ''
  描述: This parameter defines the length (in bytes) of the area within the Pdu which shall be secured
  默认值: ''
  最小值: 0
  最大值: 4294967294
- 
  序号: 2
  名称: SecOCSecuredTxPduOffset
  长名称: ''
  描述: This parameter defines the start position (offset in bytes) of the area within the Pdu which
      shall be secured
  默认值: ''
  最小值: 0
  最大值: 4294967294
```

### 21. SecOCMainFunctionRx

**描述**: Each element of this container defines one instance of SecOC_MainFunctionRx.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCMainFunctionPeriodRx
  长名称: ''
  描述: Allows to configure the time for the respective MainFunction instance of the Rx path (as float
      in seconds).
  默认值: 0.01
  最小值: 0
  最大值: 3600
- 
  序号: 2
  名称: SecOCMainFunctionRxHandleId
  长名称: ''
  描述: The numerical value used as the ID of this MainFunctionRx.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 22. SecOCMainFunctionTx

**描述**: Each element of this container defines one instance of SecOC_MainFunctionTx.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SecOCMainFunctionPeriodTx
  长名称: ''
  描述: Allows to configure the time for the respective MainFunction instance of the Tx path (as float
      in seconds).
  默认值: 0.01
  最小值: 0
  最大值: 3600
- 
  序号: 2
  名称: SecOCMainFunctionTxHandleId
  长名称: ''
  描述: The numerical value used as the ID of this MainFunctionTx.
  默认值: 0
  最小值: 0
  最大值: 65535
```

