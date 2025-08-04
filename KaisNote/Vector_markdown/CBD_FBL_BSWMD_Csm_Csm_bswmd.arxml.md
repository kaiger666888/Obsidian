# Csm

## 模块描述

Configuration of the Csm (CryptoServiceManager) module.

## 容器列表

### 1. CsmCallbacks

**描述**: Container for callback function configurations

该容器没有参数。

### 2. CsmCallback

**描述**: Container for configuration of a callback function

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackFunc
  长名称: ''
  描述: Callback function to be called if an asynchronous operation has finished. The corresponding
      job has to be configured to be processed asynchronously.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmCallbackId
  长名称: ''
  描述: Identifier of the callback function.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: CsmBswCallbackAsrVersion
  长名称: ''
  描述: |
    Determines the signature of the configured callback when it is used as BSW callback.
    
    CSM_ASR_VERSION_4_03: void <CallbackFunc> (Crypto_JobType* job, Std_ReturnType result)
    CSM_ASR_VERSION_4_04: void <CallbackFunc> (const uint32 jobID, Csm_ResultType result)
    CSM_ASR_VERSION_R19_11: void <CallbackFunc> (const Crypto_JobType* job, Crypto_ResultType
    result)
    
    Defaults to CSM_ASR_VERSION_4_03 if unset.
  默认值: CSM_ASR_VERSION_4_03
  最小值: ''
  最大值: ''
```

### 3. CsmGeneral

**描述**: Container for common configuration options.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymPrivateKeyMaxLength
  长名称: ''
  描述: |
    Not used and not supported.
    Maximum length in bytes of an asymmetric public key for all algorithm.
  默认值: 32
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CsmAsymPublicKeyMaxLength
  长名称: ''
  描述: |
    Not used and not supported.
    Maximum length in bytes of an asymmetric key for all algorithm.
  默认值: 1024
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: CsmDevErrorDetect
  长名称: ''
  描述: Switches the development error detection and notification on or off.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmMainFunctionPeriod
  长名称: ''
  描述: Specifies the period of main function Csm_MainFunction in seconds.
  默认值: 0.01
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 5
  名称: CsmSymKeyMaxLength
  长名称: ''
  描述: |
    Not used and not supported.
    Maximum length in bytes of a symmetric key for all algorithm
  默认值: 16
  最小值: 1
  最大值: 4294967295
- 
  序号: 6
  名称: CsmUseDeprecated
  长名称: ''
  描述: |
    Not used and not supported.
    Decides if the deprecated interfaces shall be used (Backwards compatibility).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable and disable availability of the API Csm_GetVersionInfo().
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CsmCustomIncludeFiles
  长名称: ''
  描述: Include custom header file.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CsmCallbackStartNotification
  长名称: ''
  描述: In ASR 4.3.0, only callbacks for Update (if CsmJobPrimitiveCallbackUpdateNotification is
      enabled) and Finish shall be forwarded to application. If this switch is enabled,
      Callback is also notified if Start was handled and every Update is notified too
      (CsmJobPrimitiveCallbackUpdateNotification is ignored).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CsmCancelationDuringProcessing
  长名称: ''
  描述: |
    If enabled, Csm allows cancelation during the processing of an asynchronous job.
    Due to this, CRYPTO_E_JOB_CANCELED of lower layer is supported and forwarded to application
    (this return value was introduced in ASR 4.4).
    
    If enabled, the runtime of a asynchronous job is slightly increased because the callback needs
    to enter an exclusive area to check the state.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CsmSafeBswChecks
  长名称: ''
  描述: Enables safety checks. These checks improve robustness. E.g. invalid parameters are checked
      before function is executed. This attribute has to be enabled for safety projects where
      this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
```

### 4. CsmJobTypeLayout

**描述**: Container for configuration options for the Csm data structure Crypto_JobType and used sub data
structures.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmJobTypeLayoutAsr430Compatibility
  长名称: AUTOSAR 4.3.0 Compatibility
  描述: |
    The Crypto_JobType has - according to Autosar - the fields 'jobState' and
    'jobPrimitiveInputOutput'. These field names changed from AUTOSAR 4.3.0 to AUTOSAR 4.3.1. These
    fields defined by AUTOSAR 4.3.0 could be required by an underlying Crypto Driver.
    
    If enabled, the Crypto_JobType is extended by the fields 'state' and 'PrimitiveInputOutput' as
    they are named in AUTOSAR 4.3.0.
    If disabled, these fields are not contained in the definition of the Crypto_JobType and the
    Crypto_JobType is defined as specified in AUTOSAR 4.3.1.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmJobTypeLayoutVarMembers
  长名称: Var Members
  描述: |
    The Crypto_JobType has in its sub data structures - according to Autosar- certain fields (e.g.
    'jobId') which are defined as const fields. If a variable of this type shall be used in
    different use cases, these fields might be overwritten. This could be a requirement of an
    underlying Crypto Driver.
    
    If enabled, the const members of Crypto_JobType's sub data structures are defined as non-const
    members
    If disabled, the Crypto_JobType's sub data structures stay as defined according to Autosar.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmJobTypeLayoutInput64
  长名称: Input64
  描述: |
    The Crypto_JobPrimitiveInputOutputType has - according to Autosar - the field 'input64'. By
    default, this field is switched off in order to reduce memory usage.
    This field can be switched on if it is required by the underlying crypto driver.
    
    If enabled, the field 'input64' exists within the Crypto_JobPrimitiveInputOutputType.
    If disabled, the field 'input64' doesn't exist within the Crypto_JobPrimitiveInputOutputType.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmJobTypeLayoutOutput64Ptr
  长名称: Output64Ptr
  描述: |
    The Crypto_JobPrimitiveInputOutputType has - according to Autosar - the field 'output64Ptr'. By
    default, this field is switched off in order to reduce memory usage.
    This field can be switched on if it is required by the underlying crypto driver.
    
    If enabled, the field 'output64Ptr' exists within the Crypto_JobPrimitiveInputOutputType.
    If disabled, the field 'output64Ptr' doesn't exist within the
    Crypto_JobPrimitiveInputOutputType.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmJobTypeLayoutRedirectionInfoRef
  长名称: RedirectionInfoRef
  描述: |
    The Crypto_JobType has the field 'jobRedirectionInfoRef'. This field can be switched off if it
    not required in order to reduce memory usage.
    
    If enabled, the field 'jobRedirectionInfoRef' exists within the Crypto_JobType.
    If disabled, the field 'jobRedirectionInfoRef' doesn't exist within the Crypto_JobType.
  默认值: true
  最小值: ''
  最大值: ''
```

### 5. CsmJobs

**描述**: Container for configuration of CSM jobs.

该容器没有参数。

### 6. CsmJob

**描述**: Container for configuration of CSM job. The container name serves as a symbolic name for the
identifier of a job configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmJobId
  长名称: ''
  描述: Identifier of the CSM job
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: CsmJobPrimitiveCallbackUpdateNotification
  长名称: ''
  描述: This parameter indicates, whether the callback function shall be called, if the UPDATE
      operation has been finished.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmJobPriority
  长名称: ''
  描述: |
    Priority of the job.
    The higher the value, the higher the job's priority.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: CsmJobUsePort
  长名称: ''
  描述: Does the job need RTE interfaces?
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmProcessingMode
  长名称: ''
  描述: Determines how the interface shall be used for that job. Synchronous processing returns with
      the result while asynchronous processing returns without processing the job. The caller
      will be notified by the corresponding callback.
  默认值: CRYPTO_PROCESSING_SYNC
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmJobInterfaceUsePort
  长名称: ''
  描述: Does the job need RTE interfaces?
  默认值: CRYPTO_USE_FNC
  最小值: ''
  最大值: ''
```

### 7. CsmKeys

**描述**: Container for CSM key configurations.

该容器没有参数。

### 8. CsmKey

**描述**: Container for configuration of a CSM key. The container name serves as a symbolic name for the
identifier of a key configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmKeyId
  长名称: ''
  描述: Identifier of the CsmKey
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: CsmKeyUsePort
  长名称: ''
  描述: Does the key need RTE interfaces?
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmKeySwcInterfaceVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version that the Client-Server-Interfaces of this key should adhere to.
    
    CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
    CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
    
    Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 changes the direction of the operation KeyElementGet's
    keyLength parameter from OUT to INOUT and introduces the following additional error codes to the
    interface's operations:
    CertificateParse:               CSM_E_KEY_EMPTY
    CertificateVerify:              CSM_E_KEY_EMPTY
    KeyCopy:                        CSM_E_KEY_EMPTY
    KeyDerive:              CSM_E_KEY_EMPTY, CSM_E_BUSY, CSM_E_KEY_READ_FAIL, CSM_E_KEY_WRITE_FAIL,
    CSM_E_KEY_SIZE_MISMATCH
    KeyElementCopy:         CSM_E_KEY_EMPTY
    KeyElementGet:          CSM_E_KEY_EMPTY
    KeyExchangeCalcPubVal:  CSM_E_KEY_EMPTY, CSM_E_SMALL_BUFFER
    KeyExchangeCalcSecret:  CSM_E_KEY_EMPTY, CSM_E_SMALL_BUFFER
    KeyGenerate:            CSM_E_KEY_EMPTY, CSM_E_BUSY
  默认值: CSM_ASR_VERSION_4_04
  最小值: ''
  最大值: ''
```

### 9. CsmPrimitives

**描述**: Container for configuration of CsmPrimitives

该容器没有参数。

### 10. CsmAEADDecrypt

**描述**: Configuration of AEAD decryption primitives

该容器没有参数。

### 11. CsmAEADDecryptConfig

**描述**: Container for configuration of a CSM decryption interface. The container name serves as a symbolic
name for the identifier of an decryption interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAEADDecryptAlgorithmFamiliy
  长名称: ''
  描述: |
    Not used.
    Determines the algorithm family used for the crypto service. This parameter defines the most
    significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmAEADDecryptAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmAEADDecryptAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmAEADDecryptAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmAEADDecryptAlgorithmKeyLength
  长名称: ''
  描述: |
    Size of the AEAD decryption key.
    This value is generated as constant value without any modifications. Thus, this value needs to
    be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
    E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.
  默认值: 16
  最小值: 1
  最大值: 4294967295
- 
  序号: 5
  名称: CsmAEADDecryptAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmAEADDecryptAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmAEADDecryptAssociatedDataMaxLength
  长名称: ''
  描述: Max size of the input associated data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 8
  名称: CsmAEADDecryptCiphertextMaxLength
  长名称: ''
  描述: Max size of the input ciphertext in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmAEADDecryptPlaintextMaxLength
  长名称: ''
  描述: Size of the output plaintext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 10
  名称: CsmAEADDecryptProcessing
  长名称: ''
  描述: |
    Not used.
    Determines how the interface shall be used for that primitive. Synchronous processing returns
    with the result while asynchronous processing returns without processing the job. The caller
    will be notified by the corresponding callback
    
    Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules
    may still rely on its value.
    It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in
    the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the
    same Primitive, the respective Primitive may need to be duplicated and the duplicate's
    Processing parameter adapted accordingly.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CsmAEADDecryptTagLength
  长名称: ''
  描述: Size of the input Tag length in BITS
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 12
  名称: CsmAEADDecryptSwcInterfaceVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere
    to.
    
    CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
    CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
    
    Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the
    interface's operations:
    AEADDecrypt:    CSM_E_KEY_NOT_VALID,
                    CSM_E_KEY_SIZE_MISMATCH,
                    CSM_E_KEY_EMPTY
    CancelJob:      CSM_E_JOB_CANCELED
  默认值: CSM_ASR_VERSION_4_04
  最小值: ''
  最大值: ''
```

### 12. CsmAEADEncrypt

**描述**: Configuration of AEAD encryption primitives

该容器没有参数。

### 13. CsmAEADEncryptConfig

**描述**: Container for configuration of a CSM encryption interface. The container name serves as a symbolic
name for the identifier of an encryption interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAEADEncryptAlgorithmFamiliy
  长名称: ''
  描述: |
    Not used.
    Determines the algorithm family used for the crypto service. This parameter defines the most
    significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmAEADEncryptAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmAEADEncryptAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmAEADEncryptAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmAEADEncryptAlgorithmKeyLength
  长名称: ''
  描述: |
    Size of the AEAD encryption key.
    This value is generated as constant value without any modifications. Thus, this value needs to
    be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
    E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.
  默认值: 16
  最小值: 1
  最大值: 4294967295
- 
  序号: 5
  名称: CsmAEADEncryptAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmAEADEncryptAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmAEADEncryptAssociatedDataMaxLength
  长名称: ''
  描述: Max size of the input associated data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 8
  名称: CsmAEADEncryptCiphertextMaxLength
  长名称: ''
  描述: Max size of the output ciphertext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmAEADEncryptPlaintextMaxLength
  长名称: ''
  描述: Max size of the input plaintext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 10
  名称: CsmAEADEncryptProcessing
  长名称: ''
  描述: |
    Not used.
    Determines how the interface shall be used for that primitive. Synchronous processing returns
    with the result while asynchronous processing returns without processing the job. The caller
    will be notified by the corresponding callback
    
    Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules
    may still rely on its value.
    It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in
    the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the
    same Primitive, the respective Primitive may need to be duplicated and the duplicate's
    Processing parameter adapted accordingly.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CsmAEADEncryptTagLength
  长名称: ''
  描述: Size of the output Tag length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 12
  名称: CsmAEADEncryptSwcInterfaceVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere
    to.
    
    CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
    CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
    
    Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the
    interface's operations:
    Encrypt:                CSM_E_KEY_NOT_VALID,
                    CSM_E_KEY_SIZE_MISMATCH,
                    CSM_E_KEY_EMPTY
    CancelJob:      CSM_E_JOB_CANCELED
  默认值: CSM_ASR_VERSION_4_04
  最小值: ''
  最大值: ''
```

### 14. CsmDecrypt

**描述**: Configurations of Decryption primitives

该容器没有参数。

### 15. CsmDecryptConfig

**描述**: Container for configuration of a CSM decryption interface. The container name serves as a symbolic
name for the identifier of an decryption interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmDecryptAlgorithmFamiliy
  长名称: ''
  描述: |
    Not used.
    Determines the algorithm family used for the crypto service. This parameter defines the most
    significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmDecryptAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmDecryptAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmDecryptAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmDecryptAlgorithmKeyLength
  长名称: ''
  描述: |
    Size of the encryption key.
    This value is generated as constant value without any modifications. Thus, this value needs to
    be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
    E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.
  默认值: 16
  最小值: 1
  最大值: 4294967295
- 
  序号: 5
  名称: CsmDecryptAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmDecryptAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmDecryptAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the secondary algorithm family used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CsmDecryptAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: Name of the custom secondary algorithm family used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CsmDecryptDataMaxLength
  长名称: ''
  描述: Max size of the input ciphertext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 10
  名称: CsmDecryptProcessing
  长名称: ''
  描述: |
    Not used.
    Determines how the interface shall be used for that primitive. Synchronous processing returns
    with the result while asynchronous processing returns without processing the job. The caller
    will be notified by the corresponding callback
    
    Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules
    may still rely on its value.
    It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in
    the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the
    same Primitive, the respective Primitive may need to be duplicated and the duplicate's
    Processing parameter adapted accordingly.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CsmDecryptResultMaxLength
  长名称: ''
  描述: Max size of the output plaintext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 12
  名称: CsmDecryptSwcInterfaceVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere
    to.
    
    CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
    CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
    
    Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the
    interface's operations:
    Decrypt:                CSM_E_KEY_NOT_VALID,
                    CSM_E_KEY_SIZE_MISMATCH,
                    CSM_E_KEY_EMPTY
    CancelJob:      CSM_E_JOB_CANCELED
  默认值: CSM_ASR_VERSION_4_04
  最小值: ''
  最大值: ''
```

### 16. CsmEncrypt

**描述**: Configurations of Encryption primitives

该容器没有参数。

### 17. CsmEncryptConfig

**描述**: Container for configuration of a CSM encryption interface. The container name serves as a symbolic
name for the identifier of an encryption interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmEncryptAlgorithmFamiliy
  长名称: ''
  描述: |
    Not used.
    Determines the algorithm family used for the crypto service. This parameter defines the most
    significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmEncryptAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmEncryptAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmEncryptAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmEncryptAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmEncryptAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmEncryptAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmEncryptAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: Name of the custom secondary algorithm family used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CsmEncryptDataMaxLength
  长名称: ''
  描述: Max size of the input plaintext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmEncryptProcessing
  长名称: ''
  描述: |
    Not used.
    Determines how the interface shall be used for that primitive. Synchronous processing returns
    with the result while asynchronous processing returns without processing the job. The caller
    will be notified by the corresponding callback
    
    Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules
    may still rely on its value.
    It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in
    the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the
    same Primitive, the respective Primitive may need to be duplicated and the duplicate's
    Processing parameter adapted accordingly.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CsmEncryptResultMaxLength
  长名称: ''
  描述: Max size of the output cipher length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 11
  名称: CsmEncryptSwcInterfaceVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere
    to.
    
    CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
    CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
    
    Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the
    interface's operations:
    AEADEncrypt:    CSM_E_KEY_NOT_VALID,
                    CSM_E_KEY_SIZE_MISMATCH,
                    CSM_E_KEY_EMPTY
    CancelJob:      CSM_E_JOB_CANCELED
  默认值: CSM_ASR_VERSION_4_04
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: CsmEncryptAlgorithmKeyLength
  长名称: ''
  描述: |
    Size of the encryption key.
    This value is generated as constant value without any modifications. Thus, this value needs to
    be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
    E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.
  默认值: 16
  最小值: 1
  最大值: 4294967295
```

### 18. CsmHash

**描述**: Container for Hash Configurations

该容器没有参数。

### 19. CsmHashConfig

**描述**: Container for configuration of a CSM hash. The container name serves as a symbolic name for the
identifier of a key configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmHashAlgorithmFamiliy
  长名称: ''
  描述: |
    Not used.
    Determines the algorithm family used for the crypto service. This parameter defines the most
    significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmHashAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmHashAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmHashAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmHashAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: CRYPTO_ALGOMODE_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmHashAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom primitive mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmHashAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmHashAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as
      CsmHashAlgorithmSecondaryFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CsmHashDataMaxLength
  长名称: ''
  描述: Max size of the input data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmHashProcessing
  长名称: ''
  描述: |
    Not used.
    Determines how the interface shall be used for that primitive. Synchronous processing returns
    with the result while asynchronous processing returns without processing the job. The caller
    will be notified by the corresponding callback.
    
    Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules
    may still rely on its value.
    It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in
    the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the
    same Primitive, the respective Primitive may need to be duplicated and the duplicate's
    Processing parameter adapted accordingly.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CsmHashResultLength
  长名称: ''
  描述: Size of the output hash length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 11
  名称: CsmHashSwcInterfaceVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere
    to.
    
    CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
    CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
    
    Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the
    interface's operations:
    CancelJob:      CSM_E_JOB_CANCELED
  默认值: CSM_ASR_VERSION_4_04
  最小值: ''
  最大值: ''
```

### 20. CsmMacGenerate

**描述**: Configurations of MacGenerate primitives

该容器没有参数。

### 21. CsmMacGenerateConfig

**描述**: Container for configuration of a CSM mac generation interface. The container name serves as a
symbolic name for the identifier of a MAC generation interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmMacGenerateAlgorithmFamiliy
  长名称: ''
  描述: |
    Not used.
    Determines the algorithm family used for the crypto service. This parameter defines the most
    significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmMacGenerateAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmMacGenerateAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family,
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmMacGenerateAlgorithmKeyLength
  长名称: ''
  描述: |
    Size of the MAC key.
    This value is generated as constant value without any modifications. Thus, this value needs to
    be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
    E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.
  默认值: 16
  最小值: 1
  最大值: 4294967295
- 
  序号: 5
  名称: CsmMacGenerateAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmMacGenerateAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmMacGenerateAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the secondary algorithm family used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CsmMacGenerateAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as
      CsmHashAlgorithmSecondaryFamilyCustom.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CsmMacGenerateDataMaxLength
  长名称: ''
  描述: Max size of the input data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 10
  名称: CsmMacGenerateProcessing
  长名称: ''
  描述: |
    Not used.
    Determines how the interface shall be used for that primitive. Synchronous processing returns
    with the result while asynchronous processing returns without processing the job. The caller
    will be notified by the corresponding callback.
    
    Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules
    may still rely on its value.
    It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in
    the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the
    same Primitive, the respective Primitive may need to be duplicated and the duplicate's
    Processing parameter adapted accordingly.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CsmMacGenerateResultLength
  长名称: ''
  描述: Size of the output MAC length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 12
  名称: CsmMacGenerateSwcInterfaceVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere
    to.
    
    CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
    CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
    
    Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the
    interface's operations:
    MacGenerate:    CSM_E_KEY_NOT_VALID,
                    CSM_E_KEY_SIZE_MISMATCH,
                    CSM_E_KEY_EMPTY
    CancelJob:      CSM_E_JOB_CANCELED
  默认值: CSM_ASR_VERSION_4_04
  最小值: ''
  最大值: ''
```

### 22. CsmMacVerify

**描述**: Configurations of MacVerify primitives

该容器没有参数。

### 23. CsmMacVerifyConfig

**描述**: Container for configuration of a CSM MAC verification interface. The container name serves as a
symbolic name for the identifier of a MAC generation interface

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmMacVerifyAlgorithmFamiliy
  长名称: ''
  描述: |
    Not used.
    Determines the algorithm family used for the crypto service. This parameter defines the most
    significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmMacVerifyAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmMacVerifyAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmMacVerifyAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the secondary algorithm family used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmMacVerifyAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second the name of the custom algorithm, if CRYPTO_ALGOFAM_CUSTOM is set as
      CsmMacVerifyAlgorithmSecondaryFamily
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmMacVerifyCompareLength
  长名称: ''
  描述: Size of the input MAC length, that shall be verified, in BITS
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 7
  名称: CsmMacVerifyDataMaxLength
  长名称: ''
  描述: Max size of the input data length, for which MAC shall be verified, in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 8
  名称: CsmMacVerifyProcessing
  长名称: ''
  描述: |
    Not used.
    Determines how the interface shall be used for that primitive. Synchronous processing returns
    with the result while asynchronous processing returns without processing the job. The caller
    will be notified by the corresponding callback.
    
    Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules
    may still rely on its value.
    It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in
    the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the
    same Primitive, the respective Primitive may need to be duplicated and the duplicate's
    Processing parameter adapted accordingly.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CsmMacVerifyAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CsmMacVerifyAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CsmMacVerifySwcInterfaceVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere
    to.
    
    CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
    CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
    
    Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the
    interface's operations:
    MacVerify:      CSM_E_KEY_NOT_VALID,
                    CSM_E_KEY_SIZE_MISMATCH,
                    CSM_E_KEY_EMPTY
    CancelJob:      CSM_E_JOB_CANCELED
  默认值: CSM_ASR_VERSION_4_04
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: CsmMacVerifyAlgorithmKeyLength
  长名称: ''
  描述: |
    Size of the MAC key.
    This value is generated as constant value without any modifications. Thus, this value needs to
    be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
    E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.
  默认值: 16
  最小值: 1
  最大值: 4294967295
```

### 24. CsmRandomGenerate

**描述**: Configurations of RandomGenerate primitives

该容器没有参数。

### 25. CsmRandomGenerateConfig

**描述**: Container for configuration of a CSM random generator. The container name serves as a symbolic name
for the identifier of a random generator configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmRandomGenerateAlgorithmFamiliy
  长名称: ''
  描述: |
    Not used.
    Determines the algorithm family used for the crypto service. This parameter defines the most
    significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmRandomGenerateAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmRandomGenerateAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service. This is the name of the
      custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomAlgorithmFamily
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmRandomGenerateAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmRandomGenerateAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service. This is the name of the custom
      algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomGenerateAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmRandomGenerateAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmRandomGenerateAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: Name of the custom secondary algorithm family used for the crypto service. This is the second
      name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as Csm
      RandomAlgorithmSecondaryFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CsmRandomGenerateProcessing
  长名称: ''
  描述: |
    Not used.
    Determines how the interface shall be used for that primitive. Synchronous processing returns
    with the result while asynchronous processing returns without processing the job. The caller
    will be notified by the corresponding callback
    
    Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules
    may still rely on its value.
    It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in
    the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the
    same Primitive, the respective Primitive may need to be duplicated and the duplicate's
    Processing parameter adapted accordingly.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CsmRandomGenerateResultLength
  长名称: ''
  描述: Size of the random generate key in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 26. CsmSecureCounter

**描述**: Configurations of SecureCounter primitives

该容器没有参数。

### 27. CsmSecureCounterConfig

**描述**: Container for configuration of a CSM counter. The container name serves as a symbolic name for the
identifier of a secure counter configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSecureCounterProcessing
  长名称: ''
  描述: |
    Not used.
    Determines how the interface shall be used for that primitive. Synchronous processing returns
    with the result while asynchronous processing returns without processing the job. The caller
    will be notified by the corresponding callback
  默认值: CSM_SYNCHRONOUS
  最小值: ''
  最大值: ''
```

### 28. CsmSignatureGenerate

**描述**: Configurations of SignatureGenerate primitives

该容器没有参数。

### 29. CsmSignatureGenerateConfig

**描述**: Container for configuration of a CSM signature generation interface. The container name serves as a
symbolic name for the identifier of signature generation interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSignatureGenerateAlgorithmFamiliy
  长名称: ''
  描述: |
    Not used.
    Determines the algorithm family used for the crypto service. This parameter defines the most
    significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSignatureGenerateAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSignatureGenerateAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmSignatureGenerateAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmSignatureGenerateAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmSignatureGenerateAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmSignatureGenerateAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: Name of the custom secondary algorithm family used for the crypto service. This is the second
      name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as
      CsmSignatureGenerateAlgorithmSecondaryFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CsmSignatureGenerateDataMaxLength
  长名称: ''
  描述: Size of the input data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmSignatureGenerateKeyLength
  长名称: ''
  描述: |
    Size of the signature generate key.
    This value is generated as constant value without any modifications. Thus, this value needs to
    be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
    E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.
  默认值: 32
  最小值: 1
  最大值: 4294967295
- 
  序号: 10
  名称: CsmSignatureGenerateProcessing
  长名称: ''
  描述: |
    Not used.
    Determines how the interface shall be used for that primitive. Synchronous processing returns
    with the result while asynchronous processing returns without processing the job. The caller
    will be notified by the corresponding callback
    
    Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules
    may still rely on its value.
    It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in
    the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the
    same Primitive, the respective Primitive may need to be duplicated and the duplicate's
    Processing parameter adapted accordingly.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CsmSignatureGenerateResultLength
  长名称: ''
  描述: Size of the output signature length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 12
  名称: CsmSignatureGenerateSwcInterfaceVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere
    to.
    
    CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
    CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
    
    Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the
    interface's operations:
    SignatureVerify:        CSM_E_KEY_NOT_VALID,
                    CSM_E_KEY_SIZE_MISMATCH,
                    CSM_E_KEY_EMPTY
    CancelJob:      CSM_E_JOB_CANCELED
  默认值: CSM_ASR_VERSION_4_04
  最小值: ''
  最大值: ''
```

### 30. CsmSignatureVerify

**描述**: Configurations of SignatureVerify primitives

该容器没有参数。

### 31. CsmSignatureVerifyConfig

**描述**: Container for configuration of a CSM signature verification interface. The container name serves as
a symbolic name for the identifier of signature verification interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSignatureVerifyAlgorithmFamiliy
  长名称: ''
  描述: |
    Not used.
    Determines the algorithm family used for the crypto service. This parameter defines the most
    significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSignatureVerifyAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSignatureVerifyAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service. This is the name of the
      custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmSignatureVerifyAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmSignatureVerifyAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmSignatureVerifyAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmSignatureVerifyAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmSignatureVerifyAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: Name of the custom secondary algorithm family used for the crypto service. This is the name of
      the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmSignatureVerifyAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CsmSignatureVerifyCompareLength
  长名称: ''
  描述: Size of the input data length, for which signature shall be verified, in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmSignatureVerifyDataMaxLength
  长名称: ''
  描述: Size of the input data length, for which signature shall be verified, in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 10
  名称: CsmSignatureVerifyProcessing
  长名称: ''
  描述: |
    Not used.
    Determines how the interface shall be used for that primitive. Synchronous processing returns
    with the result while asynchronous processing returns without processing the job. The caller
    will be notified by the corresponding callback.
    
    Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules
    may still rely on its value.
    It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in
    the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the
    same Primitive, the respective Primitive may need to be duplicated and the duplicate's
    Processing parameter adapted accordingly.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CsmSignatureVerifySwcInterfaceVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere
    to.
    
    CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
    CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
    
    Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the
    interface's operations:
    SignatureVerify:        CSM_E_KEY_NOT_VALID,
                    CSM_E_KEY_SIZE_MISMATCH,
                    CSM_E_KEY_EMPTY
    CancelJob:      CSM_E_JOB_CANCELED
  默认值: CSM_ASR_VERSION_4_04
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: CsmSignatureVerifyKeyLength
  长名称: ''
  描述: |
    Size of the signature verify key.
    This value is generated as constant value without any modifications. Thus, this value needs to
    be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
    E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.
  默认值: 32
  最小值: 1
  最大值: 4294967295
```

### 32. CsmJobKeySetValid

**描述**: Configurations of KeySetValid primitives

该容器没有参数。

### 33. CsmJobKeySetValidConfig

**描述**: Container for configuration of a CSM key set valid operation. The container name serves as a
symbolic name for the identifier of a key configuration.

该容器没有参数。

### 34. CsmJobKeyExchangeCalcPubVal

**描述**: Configurations of KeyExchangeCalcPubVal primitives

该容器没有参数。

### 35. CsmJobKeyExchangeCalcPubValConfig

**描述**: Container for configuration of a CSM JobKeyExchangeCalcPubVal. The container name serves as a
symbolic name for the identifier of a key configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmJobKeyExchangeCalcPubValAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmJobKeyExchangeCalcPubValAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmJobKeyExchangeCalcPubValAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmJobKeyExchangeCalcPubValAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom primitive mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used .
  默认值: ''
  最小值: ''
  最大值: ''
```

### 36. CsmJobKeyExchangeCalcSecret

**描述**: Configurations of KeyExchangeCalcSecret primitives

该容器没有参数。

### 37. CsmJobKeyExchangeCalcSecretConfig

**描述**: Container for configuration of a CSM JobKeyExchangeCalcSecret. The container name serves as a
symbolic name for the identifier of a JobKeyExchangeCalcSecret configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmJobKeyExchangeCalcSecretAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmJobKeyExchangeCalcSecretAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmJobKeyExchangeCalcSecretAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmJobKeyExchangeCalcSecretAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom primitive mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 38. CsmJobKeyDerive

**描述**: Configurations of KeyDerive primitives

该容器没有参数。

### 39. CsmJobKeyDeriveConfig

**描述**: Container for configuration of a CSM key derive operation. The container name serves as a symbolic
name for the identifier of a key derive configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmJobKeyDeriveAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmJobKeyDeriveAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmJobKeyDeriveAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmJobKeyDeriveAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmJobKeyDeriveAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service.
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmJobKeyDeriveAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmJobKeyDeriveAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 40. CsmJobRandomSeed

**描述**: Configurations of RandomSeed primitives

该容器没有参数。

### 41. CsmJobRandomSeedConfig

**描述**: Container for configuration of a CSM random seed operation. The container name serves as a symbolic
name for the identifier of a random seed configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmJobRandomSeedAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service. This is the name of the
      custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmJobRandomSeedAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmJobRandomSeedAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service. This is the name of the custom
      algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmJobRandomSeedAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmJobRandomSeedAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: Name of the custom secondary algorithm family used for the crypto service. This is the second
      name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmRandomSeedAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 42. CsmJobKeyGenerate

**描述**: Configurations of KeyGenerate primitives

该容器没有参数。

### 43. CsmJobKeyGenerateConfig

**描述**: Container for configuration of a CSM key generate operation. The container name serves as a symbolic
name for the identifier of a key generate configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmJobKeyGenerateAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmJobKeyGenerateAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmJobKeyGenerateAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: CRYPTO_ALGOMODE_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmJobKeyGenerateAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmJobKeyGenerateAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service.
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmJobKeyGenerateAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmJobKeyGenerateAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 44. CsmJobCertificateParse

**描述**: Configurations of CertificateParse primitives

该容器没有参数。

### 45. CsmJobCertificateParseConfig

**描述**: Container for configuration of a CSM CsmJobCertificateParse. The container name serves as a symbolic
name for the identifier of a key configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmJobCertificateParseAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmJobCertificateParseAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmJobCertificateParseAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom primitive mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmJobCertificateParseAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmJobCertificateParseAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmJobCertificateParseDataMaxLength
  长名称: ''
  描述: Max size of the input data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 46. CsmJobCertificateVerify

**描述**: Configurations of CertificateVerify primitves

该容器没有参数。

### 47. CsmJobCertificateVerifyConfig

**描述**: Container for configuration of a CSM CsmJobCertificateVerify. The container name serves as a
symbolic name for the identifier of a key configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmJobCertificateVerifyAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmJobCertificateVerifyAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmJobCertificateVerifyAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmJobCertificateVerifyAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom primitive mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmJobCertificateVerifyAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmJobCertificateVerifyAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmJobCertificateVerifyDataMaxLength
  长名称: ''
  描述: Max size of the input data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 48. CsmQueues

**描述**: Container for CSM queue configurations

该容器没有参数。

### 49. CsmQueue

**描述**: Container for configuration of a CSM queue. The container name serves as a symbolic name for the
identifier of a queue configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmQueueSize
  长名称: ''
  描述: Size of the CsmQueue. If jobs cannot be processed by the underlying hardware since the
      hardware is busy, the jobs stay in the prioritized queue. If the queue is full, the next
      job will be rejected.
  默认值: 1
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CsmTriggerAsynchJobsInCallback
  长名称: ''
  描述: |
    If enabled, jobs will be triggered (given to the CryIf for processing) directly if the CryIf
    notifies the Csm that the last job was finished. Both is handled in the
    Csm_CallbackNotification().
    
    If not enabled, the next job will be given to the CryIf for processing in the next mainfunction
    cycle.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmJobSharing
  长名称: ''
  描述: |
    If enabled, Csm will use shared job objects per queue instead of reserving an own job object for
    each configured job. This highly reduces the amount of needed RAM but increases the runtime due
    to setting up the complete job with every usage.
    
    The Csm will reserve the following amount of job objects:
    1 for all synchrnous jobs of the queue (if there are any)
    Queue size + 1 for all asynchronous jobs (if there are any)
    This means the queue of the Csm can be filled completely while one job is currenlty processed by
    the crypto driver object.
    If the crypto driver object which handles the job of this queue also implements a queing
    mechanism, either increase the queue size of Csm accordingly to get the necessary amount of job
    objects, or deactivate the job sharing.
  默认值: true
  最小值: ''
  最大值: ''
```

### 50. CsmCallouts

**描述**: Container for callout function configurations

该容器没有参数。

### 51. CsmCallout

**描述**: Container for configuration of callout functions

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmPreJobCalloutFunc
  长名称: ''
  描述: Callout function which will be called before the corresponding job is executed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmPostJobCalloutFunc
  长名称: ''
  描述: Callout function which will be called after the corresponding job is executed.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 52. CsmInOutRedirections

**描述**: Configuration for Csm redirection configurations

该容器没有参数。

### 53. CsmInOutRedirection

**描述**: Container for configuration of a Csm redirection. A redirection lets a Csm job use a specific key
element as input or/and output.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmInputKeyElementId
  长名称: ''
  描述: Identifier of the key element used as input.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: CsmSecondaryInputKeyElementId
  长名称: ''
  描述: Identifier of the key element used as secondary input.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: CsmTertiaryInputKeyElementId
  长名称: ''
  描述: Identifier of the key element used as tertiary input.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: CsmOutputKeyElementId
  长名称: ''
  描述: Identifier of the key element used as output.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: CsmSecondaryOutputKeyElementId
  长名称: ''
  描述: Identifier of the key element used as secondary output.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

