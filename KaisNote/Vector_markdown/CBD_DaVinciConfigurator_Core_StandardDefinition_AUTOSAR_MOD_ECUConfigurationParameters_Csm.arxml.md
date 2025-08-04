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
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 3. CsmGeneral

**描述**: Container for common configuration options.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymPrivateKeyMaxLength
  长名称: ''
  描述: Maximum length in bytes of an asymmetric public key for all algorithm
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CsmAsymPublicKeyMaxLength
  长名称: ''
  描述: Maximum length in bytes of an asymmetric key for all algorithm
  默认值: ''
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
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 5
  名称: CsmSymKeyMaxLength
  长名称: ''
  描述: Maximum length in bytes of a symmetric key for all algorithm
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 6
  名称: CsmUseDeprecated
  长名称: ''
  描述: Decides if the deprecated interfaces shall be used (Backwards combatibility).
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
  名称: CsmMaxAlignScalarType
  长名称: ''
  描述: The scalar type which has the maximum alignment restrictions on the given platform.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CsmMaximumBlockingTime
  长名称: ''
  描述: If interruption is turned on with the configuration option CsmUseInterruption, this option
      configures the maximum time in microseconds the main function shall be allowed to run
      before it must interrupt itself. The lowest allowed value for the option is
      implementation dependent.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 10
  名称: CsmUseInterruption
  长名称: ''
  描述: Pre-processor switch to enable and disable interruption of job processing.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CsmUseSyncJobProcessing
  长名称: ''
  描述: Pre-processor switch to enable and disable synchronous job processing.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: CsmCustomIncludeFiles
  长名称: ''
  描述: ''
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. CsmJobs

**描述**: Container for configuration of CSM jobs.

该容器没有参数。

### 5. CsmJob

**描述**: Container for configuration of CSM job. The container name serves as a symbolic name for the
identifier of a job configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmJobId
  长名称: ''
  描述: Identifier of the CSM job
  默认值: ''
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
  描述: Priority of the job.
  默认值: ''
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
```

### 6. CsmKeys

**描述**: Container for CSM key configurations.

该容器没有参数。

### 7. CsmKey

**描述**: Container for configuration of a CSM key. The container name serves as a symbolic name for the
identifier of a key configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmKeyId
  长名称: ''
  描述: Identifier of the CsmKey
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CsmKeyUsePort
  长名称: ''
  描述: Does the key need RTE interfaces?
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. CsmPrimitives

**描述**: Container for configuration of CsmPrimitives

该容器没有参数。

### 9. CsmAEADDecrypt

**描述**: Configuration of AEAD decryption primitives

该容器没有参数。

### 10. CsmAEADDecryptConfig

**描述**: Container for configuration of a CSM decryption interface. The container name serves as a symbolic
name for the identifier of an decryption interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAEADDecryptAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmAEADDecryptAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmAEADDecryptAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmAEADDecryptAlgorithmKeyLength
  长名称: ''
  描述: Size of the AEAD decryption key in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 4
  名称: CsmAEADDecryptAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmAEADDecryptAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmAEADDecryptAssociatedDataMaxLength
  长名称: ''
  描述: Max size of the input associated data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 7
  名称: CsmAEADDecryptCiphertextMaxLength
  长名称: ''
  描述: Max size of the input ciphertext in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 8
  名称: CsmAEADDecryptPlaintextMaxLength
  长名称: ''
  描述: Size of the output plaintext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmAEADDecryptProcessing
  长名称: ''
  描述: Determines how the interface shall be used for that primitive. Synchronous processing returns
      with the result while asynchronous processing returns without processing the job. The
      caller will be notified by the corresponding callback
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CsmAEADDecryptTagLength
  长名称: ''
  描述: Size of the input Tag length in BITS
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 11. CsmAEADEncrypt

**描述**: Configuration of AEAD encryption primitives

该容器没有参数。

### 12. CsmAEADEncryptConfig

**描述**: Container for configuration of a CSM encryption interface. The container name serves as a symbolic
name for the identifier of an encryption interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAEADEncryptAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmAEADEncryptAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmAEADEncryptAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmAEADEncryptAlgorithmKeyLength
  长名称: ''
  描述: Size of the AEAD encryption key in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 4
  名称: CsmAEADEncryptAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmAEADEncryptAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmAEADEncryptAssociatedDataMaxLength
  长名称: ''
  描述: Max size of the input associated data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 7
  名称: CsmAEADEncryptCiphertextMaxLength
  长名称: ''
  描述: Max size of the output ciphertext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 8
  名称: CsmAEADEncryptPlaintextMaxLength
  长名称: ''
  描述: Max size of the input plaintext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmAEADEncryptProcessing
  长名称: ''
  描述: Determines how the interface shall be used for that primitive. Synchronous processing returns
      with the result while asynchronous processing returns without processing the job. The
      caller will be notified by the corresponding callback
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CsmAEADEncryptTagLength
  长名称: ''
  描述: Size of the output Tag length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 13. CsmDecrypt

**描述**: Configurations of Decryption primitives

该容器没有参数。

### 14. CsmDecryptConfig

**描述**: Container for configuration of a CSM decryption interface. The container name serves as a symbolic
name for the identifier of an decryption interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmDecryptAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmDecryptAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmDecryptAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmDecryptAlgorithmKeyLength
  长名称: ''
  描述: Size of the encryption key in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 4
  名称: CsmDecryptAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmDecryptAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmDecryptAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the secondary algorithm family used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmDecryptAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: Name of the custom secondary algorithm family used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CsmDecryptDataMaxLength
  长名称: ''
  描述: Max size of the input ciphertext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmDecryptProcessing
  长名称: ''
  描述: Determines how the interface shall be used for that primitive. Synchronous processing returns
      with the result while asynchronous processing returns without processing the job. The
      caller will be notified by the corresponding callback
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CsmDecryptResultMaxLength
  长名称: ''
  描述: Max size of the output plaintext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 15. CsmEncrypt

**描述**: Configurations of Encryption primitives

该容器没有参数。

### 16. CsmEncryptConfig

**描述**: Container for configuration of a CSM encryption interface. The container name serves as a symbolic
name for the identifier of an encryption interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmEncryptAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmEncryptAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmEncryptAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmEncryptAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmEncryptAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmEncryptAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmEncryptAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: Name of the custom secondary algorithm family used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmEncryptDataMaxLength
  长名称: ''
  描述: Max size of the input plaintext length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 8
  名称: CsmEncryptProcessing
  长名称: ''
  描述: Determines how the interface shall be used for that primitive. Synchronous processing returns
      with the result while asynchronous processing returns without processing the job. The
      caller will be notified by the corresponding callback
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CsmEncryptResultMaxLength
  长名称: ''
  描述: Max size of the output cipher length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 17. CsmHash

**描述**: Container for Hash Configurations

该容器没有参数。

### 18. CsmHashConfig

**描述**: Container for configuration of a CSM hash. The container name serves as a symbolic name for the
identifier of a key configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmHashAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmHashAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmHashAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmHashAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: CRYPTO_ALGOMODE_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmHashAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom primitive mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmHashAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmHashAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as
      CsmHashAlgorithmSecondaryFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmHashDataMaxLength
  长名称: ''
  描述: Max size of the input data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 8
  名称: CsmHashProcessing
  长名称: ''
  描述: Determines how the interface shall be used for that primitive. Synchronous processing returns
      with the result while asynchronous processing returns without processing the job. The
      caller will be notified by the corresponding callback.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CsmHashResultLength
  长名称: ''
  描述: Size of the output hash length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 19. CsmMacGenerate

**描述**: Configurations of MacGenerate primitives

该容器没有参数。

### 20. CsmMacGenerateConfig

**描述**: Container for configuration of a CSM mac generation interface. The container name serves as a
symbolic name for the identifier of a MAC generation interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmMacGenerateAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmMacGenerateAlgorithmFamilyCustom
  长名称: ''
  描述: This is the name of the custom algorithm family,
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmMacGenerateAlgorithmKeyLength
  长名称: ''
  描述: Size of the MAC key in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 4
  名称: CsmMacGenerateAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmMacGenerateAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmMacGenerateAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the secondary algorithm family used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmMacGenerateAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as
      CsmHashAlgorithmSecondaryFamilyCustom.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CsmMacGenerateDataMaxLength
  长名称: ''
  描述: Max size of the input data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmMacGenerateProcessing
  长名称: ''
  描述: Determines how the interface shall be used for that primitive. Synchronous processing returns
      with the result while asynchronous processing returns without processing the job. The
      caller will be notified by the corresponding callback.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CsmMacGenerateResultLength
  长名称: ''
  描述: Size of the output MAC length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 21. CsmMacVerify

**描述**: Configurations of MacVerify primitives

该容器没有参数。

### 22. CsmMacVerifyConfig

**描述**: Container for configuration of a CSM MAC verification interface. The container name serves as a
symbolic name for the identifier of a MAC generation interface

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmMacVerifyAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmMacVerifyAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmMacVerifyAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the secondary algorithm family used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmMacVerifyAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: This is the second the name of the custom algorithm, if CRYPTO_ALGOFAM_CUSTOM is set as
      CsmMacVerifyAlgorithmSecondaryFamily
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmMacVerifyCompareLength
  长名称: ''
  描述: Size of the input MAC length, that shall be verified, in BITS
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 6
  名称: CsmMacVerifyDataMaxLength
  长名称: ''
  描述: Max size of the input data length, for whichs MAC shall be verified, in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 7
  名称: CsmMacVerifyProcessing
  长名称: ''
  描述: Determines how the interface shall be used for that primitive. Synchronous processing returns
      with the result while asynchronous processing returns without processing the job. The
      caller will be notified by the corresponding callback.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 23. CsmRandomGenerate

**描述**: Configurations of RandomGenerate primitives

该容器没有参数。

### 24. CsmRandomGenerateConfig

**描述**: Container for configuration of a CSM random generator. The container name serves as a symbolic name
for the identifier of a random generator configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmRandomGenerateAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmRandomGenerateAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service. This is the name of the
      custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomAlgorithmFamily
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmRandomGenerateAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmRandomGenerateAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service. This is the name of the custom
      algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomGenerateAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmRandomGenerateAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmRandomGenerateAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: Name of the custom secondary algorithm family used for the crypto service. This is the second
      name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as Csm
      RandomAlgorithmSecondaryFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmRandomGenerateProcessing
  长名称: ''
  描述: Determines how the interface shall be used for that primitive. Synchronous processing returns
      with the result while asynchronous processing returns without processing the job. The
      caller will be notified by the corresponding callback
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CsmRandomGenerateResultLength
  长名称: ''
  描述: Size of the random generate key in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 25. CsmSecureCounter

**描述**: Configurations of SecureCounter primitives

该容器没有参数。

### 26. CsmSecureCounterConfig

**描述**: Container for configuration of a CSM counter. The container name serves as a symbolic name for the
identifier of a secure counter configuration.

该容器没有参数。

### 27. CsmSignatureGenerate

**描述**: Configurations of SignatureGenerate primitives

该容器没有参数。

### 28. CsmSignatureGenerateConfig

**描述**: Container for configuration of a CSM signature generation interface. The container name serves as a
symbolic name for the identifier of signature generation interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSignatureGenerateAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSignatureGenerateAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSignatureGenerateAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmSignatureGenerateAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmSignatureGenerateAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmSignatureGenerateAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: Name of the custom secondary algorithm family used for the crypto service. This is the second
      name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as
      CsmSignatureGenerateAlgorithmSecondaryFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmSignatureGenerateDataMaxLength
  长名称: ''
  描述: Size of the input data length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 8
  名称: CsmSignatureGenerateKeyLength
  长名称: ''
  描述: Size of the signature generate key in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmSignatureGenerateProcessing
  长名称: ''
  描述: Determines how the interface shall be used for that primitive. Synchronous processing returns
      with the result while asynchronous processing returns without processing the job. The
      caller will be notified by the corresponding callback
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CsmSignatureGenerateResultLength
  长名称: ''
  描述: Size of the output signature length in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 29. CsmSignatureVerify

**描述**: Configurations of SignatureVerify primitives

该容器没有参数。

### 30. CsmSignatureVerifyConfig

**描述**: Container for configuration of a CSM signature verification interface. The container name serves as
a symbolic name for the identifier of signature verification interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSignatureVerifyAlgorithmFamiliy
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSignatureVerifyAlgorithmFamilyCustom
  长名称: ''
  描述: Name of the custom algorithm family used for the crypto service. This is the name of the
      custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmSignatureVerifyAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSignatureVerifyAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CsmSignatureVerifyAlgorithmModeCustom
  长名称: ''
  描述: Name of the custom algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CsmSignatureVerifyAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service. This parameter defines the most
      significant part of the algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CsmSignatureVerifyAlgorithmSecondaryFamilyCustom
  长名称: ''
  描述: Name of the custom secondary algorithm family used for the crypto service. This is the name of
      the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as
      CsmSignatureVerifyAlgorithmFamily.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CsmSignatureVerifyCompareLength
  长名称: ''
  描述: Size of the input data length, for whichs signature shall be verified, in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 8
  名称: CsmSignatureVerifyDataMaxLength
  长名称: ''
  描述: Size of the input data length, for whichs signature shall be verified, in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 9
  名称: CsmSignatureVerifyProcessing
  长名称: ''
  描述: Determines how the interface shall be used for that primitive. Synchronous processing returns
      with the result while asynchronous processing returns without processing the job. The
      caller will be notified by the corresponding callback.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 31. CsmQueues

**描述**: Container for CSM queue configurations

该容器没有参数。

### 32. CsmQueue

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
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 33. CsmAsymDecrypt

**描述**: Container for incorporation of AsymDecrypt primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymDecryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an
      asymmetrical decryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 34. CsmAsymDecryptConfig

**描述**: Container for configuration of service AsymDecrypt. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymDecryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmAsymDecryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmCallbackAsymDecrypt
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 35. CsmAsymEncrypt

**描述**: Container for incorporation of AsymEncrypt primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymEncryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an
      asymmetrical encryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 36. CsmAsymEncryptConfig

**描述**: Container for configuration of service AsymEncrypt. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymEncryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmAsymEncryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmCallbackAsymEncrypt
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 37. CsmAsymPrivateKeyExtract

**描述**: Container for incorporation of AsymPrivateKeyExtract primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymPrivateKeyExtractMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an
      asymmetrical private key extraction.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 38. CsmAsymPrivateKeyExtractConfig

**描述**: Container for configuration of service AsymPrivateKeyExtract.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymPrivateKeyExtractInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmAsymPrivateKeyExtractPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmCallbackAsymPrivateKeyExtract
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 39. CsmAsymPrivateKeyWrapAsym

**描述**: Container for incorporation of AsymPrivateKeyWrapSym primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymPrivateKeyWrapAsymMaxPrivKeySize
  长名称: ''
  描述: The maximum length, in bytes, of all private key types used in all CRY primitives which
      implement an asymmetrical private key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CsmAsymPrivateKeyWrapAsymMaxPubKeySize
  长名称: ''
  描述: The maximum length, in bytes, of all public key types used in all CRY primitives which
      implement an asymmetrical private key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 40. CsmAsymPrivateKeyWrapAsymConfig

**描述**: Container for configuration of service SymKeyWrapAsym. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymPrivateKeyWrapAsymInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmAsymPrivateKeyWrapAsymPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmCallbackAsymPrivateKeyWrapAsym
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 41. CsmAsymPrivateKeyWrapSym

**描述**: Container for incorporation of AsymPrivateKeyWrapSym primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymPrivateKeyWrapSymMaxPrivKeySize
  长名称: ''
  描述: The maximum length, in bytes, of all private information types used in all CRY primitives
      which implement an asymetric private key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CsmAsymPrivateKeyWrapSymMaxSymKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an
      asymetrical private key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 42. CsmAsymPrivateKeyWrapSymConfig

**描述**: Container for configuration of service AsymPrivateKeyWrapSym. The container name serves as a
symbolic name for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymPrivateKeyWrapSymInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmAsymPrivateKeyWrapSymPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmCallbackAsymPrivateKeyWrapSym
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 43. CsmAsymPublicKeyExtract

**描述**: Container for incorporation of AsymPublicKeyExtract primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymPublicKeyExtractMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an
      asymmetrical public key extraction.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 44. CsmAsymPublicKeyExtractConfig

**描述**: Container for configuration of service AsymPublicKeyExtract.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmAsymPublicKeyExtractInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmAsymPublicKeyExtractPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmCallbackAsymPublicKeyExtract
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 45. CsmChecksum

**描述**: Container for incorporation of Checksum primitives.

该容器没有参数。

### 46. CsmChecksumConfig

**描述**: Container for configuration of service Checksum. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackChecksum
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmChecksumInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmChecksumPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 47. CsmDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 48. CsmHash

**描述**: Container for incorporation of Hash primitives.

该容器没有参数。

### 49. CsmHashConfig

**描述**: Configurations for the Hash service. The container name serves as a symbolic name for the identifier
of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackHash
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmHashInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmHashPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 50. CsmKeyDerive

**描述**: Container for incorporation of KeyDerive primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmKeyDeriveMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a key
      derivation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 51. CsmKeyDeriveConfig

**描述**: Container for configuration of service KeyDerive. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackKeyDerive
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmKeyDeriveInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmKeyDerivePrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 52. CsmKeyDeriveSymKey

**描述**: Container for incorporation of CsmKeyDeriveSymKey primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmKeyDeriveSymKeyMaxSymKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a key
      derivation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 53. CsmKeyDeriveSymKeyConfig

**描述**: Container for configuration of service CsmKeyDeriveSymKey. The container name serves as a symbolic
name for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackKeyDeriveSymKey
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmKeyDeriveSymKeyInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmKeyDeriveSymKeyPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 54. CsmKeyExchangeCalcPubVal

**描述**: Container for incorporation of KeyExchangeCalcPubVal primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmKeyExchangeCalcPubValMaxBaseTypeSize
  长名称: ''
  描述: The maximum length, in bytes, of all base types used in all CRY primitives which implement a
      public value calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CsmKeyExchangeCalcPubValMaxPrivateTypeSize
  长名称: ''
  描述: The maximum length, in bytes, of all private information types used in all CRY primitives
      which implement a public value calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 55. CsmKeyExchangeCalcPubValConfig

**描述**: Container for configuration of service KeyExchangeCalcPubVal. The container name serves as a
symbolic name for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackKeyExchangeCalcPubVal
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmKeyExchangeCalcPubValInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmKeyExchangeCalcPubValPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 56. CsmKeyExchangeCalcSecret

**描述**: Container for incorporation of KeyExchangeCalcSecret primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmKeyExchangeCalcSecretMaxBaseTypeSize
  长名称: ''
  描述: The maximum length, in bytes, of all base types used in all CRY primitives which implement a
      shared secret calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CsmKeyExchangeCalcSecretMaxPrivateTypeSize
  长名称: ''
  描述: The maximum length, in bytes, of all private information types used in all CRY primitives
      which implement a shared secret calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 57. CsmKeyExchangeCalcSecretConfig

**描述**: Container for configuration of service KeyExchangeCalcSecret. The container name serves as a
symbolic name for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackKeyExchangeCalcSecret
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmKeyExchangeCalcSecretInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmKeyExchangeCalcSecretPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 58. CsmKeyExchangeCalcSymKey

**描述**: Container for incorporation of KeyExchangeCalcSymKey primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmKeyExchangeCalcSymKeyMaxBaseTypeSize
  长名称: ''
  描述: The maximum length, in bytes, of all base types used in all CRY primitives which implement a
      symmetrical key calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CsmKeyExchangeCalcSymKeyMaxPrivateTypeSize
  长名称: ''
  描述: The maximum length, in bytes, of all private information types used in all CRY primitives
      which implement a symmetrical key calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: CsmKeyExchangeCalcSymKeyMaxSymKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a
      symmetrical key calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 59. CsmKeyExchangeCalcSymKeyConfig

**描述**: Container for configuration of service KeyExchangeCalcSymKey. The container name serves as a
symbolic name for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackKeyExchangeCalcSymKey
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmKeyExchangeCalcSymKeyInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmKeyExchangeCalcSymKeyPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 60. CsmMacGenerate

**描述**: Container for incorporation of MacGenerate primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmMacGenerateMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a MAC
      generation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 61. CsmMacGenerateConfig

**描述**: Configurations for the MacGenerate service. The container name serves as a symbolic name for the
identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackMacGenerate
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmMacGenerateInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmMacGeneratePrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 62. CsmMacVerify

**描述**: Container for incorporation of MacVerify primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmMacVerifyMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a MAC
      verification.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 63. CsmMacVerifyConfig

**描述**: Container for configuration of service MacVerify. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackMacVerify
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmMacVerifyInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmMacVerifyPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 64. CsmRandomGenerate

**描述**: Container for incorporation of RandomGenerate primitives.

该容器没有参数。

### 65. CsmRandomGenerateConfig

**描述**: Container for configuration of service RandomGenerate. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackRandomGenerate
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmRandomGenerateInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmRandomGeneratePrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 66. CsmRandomSeed

**描述**: Container for incorporation of RandomSeed primitives.

该容器没有参数。

### 67. CsmRandomSeedConfig

**描述**: Container for configuration of service RandomSeed. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackRandomSeed
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmRandomSeedInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmRandomSeedPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 68. CsmSignatureGenerate

**描述**: Container for incorporation of SignatureGenerate primitives

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSignatureGenerateMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a
      signature generation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 69. CsmSignatureGenerateConfig

**描述**: Container for configuration of service SignatureGenerate. The container name serves as a symbolic
name for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackSignatureGenerate
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSignatureGenerateInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSignatureGeneratePrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 70. CsmSignatureVerify

**描述**: Container for incorporation of SignatureVerify primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSignatureVerifyMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a
      signature verification.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 71. CsmSignatureVerifyConfig

**描述**: Container for configuration of service SignatureVerify. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackSignatureVerify
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSignatureVerifyInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSignatureVerifyPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 72. CsmSymBlockDecrypt

**描述**: Container for incorporation of SymBlockDecrypt primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSymBlockDecryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a
      symmetrical block decryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 73. CsmSymBlockDecryptConfig

**描述**: Container for configuration of service SymBlockDecrypt. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackSymBlockDecrypt
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSymBlockDecryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSymBlockDecryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 74. CsmSymBlockEncrypt

**描述**: Container for incorporation of SymBlockEncrypt primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSymBlockEncryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a
      symmetrical block encryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 75. CsmSymBlockEncryptConfig

**描述**: Container for configuration of service SymBlockEncrypt. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackSymBlockEncrypt
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSymBlockEncryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSymBlockEncryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 76. CsmSymDecrypt

**描述**: Container for incorporation of SymDecrypt primitives

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSymDecryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a
      symmetrical decryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 77. CsmSymDecryptConfig

**描述**: Container for configuration of service SymDecrypt.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackSymDecrypt
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSymDecryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSymDecryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 78. CsmSymEncrypt

**描述**: Container for incorporation of SymEncrypt primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSymEncryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a
      symmetrical encryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 79. CsmSymEncryptConfig

**描述**: Container for configuration of service SymEncrypt. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackSymEncrypt
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSymBlockEncryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSymEncryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 80. CsmSymKeyExtract

**描述**: Container for incorporation of SymKeyExtract primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSymKeyExtractMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a
      symmetrical key extraction.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 81. CsmSymKeyExtractConfig

**描述**: Container for configuration of service SymKeyExtract. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackSymKeyExtract
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSymKeyExtractInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSymKeyExtractPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 82. CsmSymKeyWrapAsym

**描述**: Container for incorporation of SymKeyWrapSym primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSymKeyWrapAsymMaxPubKeySize
  长名称: ''
  描述: The maximum length, in bytes, of all public key  types used in all CRY primitives which
      implement an asymmetrical key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CsmSymKeyWrapAsymMaxSymKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an
      asymmetrical key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 83. CsmSymKeyWrapAsymConfig

**描述**: Container for configuration of service SymKeyWrapAsym. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackSymKeyWrapAsym
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSymKeyWrapAsymInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSymKeyWrapAsymPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 84. CsmSymKeyWrapSym

**描述**: Container for incorporation of SymKeyWrapSym primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmSymKeyWrapSymMaxSymKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an
      symmetrical key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 85. CsmSymKeyWrapSymConfig

**描述**: Container for configuration of service SymKeyWrapSym. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CsmCallbackSymKeyWrapSym
  长名称: ''
  描述: Callback function to be called if service has finished.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CsmSymKeyWrapSymInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CsmSymKeyWrapSymPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

