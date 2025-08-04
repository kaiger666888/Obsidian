# Smh

## 模块描述

Configuration of the Smh (SecModHis, Security Module implementing the HIS specification) module.

## 容器列表

### 1. SmhGeneral

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhOperationMode
  长名称: ''
  描述: The mode of the security component is set to Production. The setting is displayed for
      documentation purposes only.
  默认值: PRODUCTION
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhWatchdogCycleCount
  长名称: ''
  描述: |
    Controls frequency of polling function calls within loops including SEC_WATCHDOG_CYCLE_TRIGGER
    macro calls, e.g. from Sec_Crc.c.
    The called function will typically be the Bootloader Polling (Watchdog Trigger) function and by
    this configuration will happen every Nth call (where N == configured cycle Count).
  默认值: 1
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: SmhCryptographicKeysLocatedInRAM
  长名称: ''
  描述: Specify the location of the SmhCryptographicKeys.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SmhUserConfigFile
  长名称: ''
  描述: |
    If a file path is specified, the file is read and its contents are put at the end of the SMH
    config file (SecM_cfg.h).
    
    If you want to overwrite some of the settings in the generated configuration file (SecM_cfg.h),
    you can specify a path to a user defined configuration file. The user defined configuration file
    will be included at the end of the generated preprocessor switches. Definitions in the user
    defined configuration file can overwrite definitions in the generated configuration file.
    
    To specify the file name, you can use "$(var)" sequence(s) in the specified path. Each such
    sequence is replaced by the content of the related environment variable "var".
    Additionally you can use following predefined sequences:
    $(DpaProjectFolder) Absolute directory of the loaded *.dpa file.
    $(EcuProjectName) Name of the project defined in the loaded *.dpa file.
    $(EcucFile) Absolute directory "ECUC", defined by the loaded *.dpa file, containing files
    $(EcuProjectName).ecuc.arxml and $(EcuProjectName).ecuc.Initial.arxml .
    $(EcucFolder) Parent directory of $(EcucFile).
    $(SipRootPath) Absolute directory "SIP", defined by the loaded *.dpa file.
    $(OutputFolder) (Relative) directory "GenData", defined by the loaded *.dpa file. See setting
    "Root Target Folder" of Configurator 5.
    $(ServiceSwcFolder) Absolute directory "ServiceComponents", defined by the loaded *.dpa file.
    $(cwd) Current working directory when starting Configurator 5.
    
    RESTRICTIONS: Not all of the settings can be overwritten simply by triggering the preprocessor
    switch. Some of the options are complex and the code generator generates less or more code
    depending on the setting.
    
    USE SUCH A FILE ONLY AFTER DISCUSSION WITH VECTOR.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SmhProvidevSecPrimRandomFunction
  长名称: Provide vSecPrim Random Function
  描述: If enabled the SMH will generate the callout esl_getBytesRNG function required by the vSecPrim
      module. Please check the vSecPrim TechRef/Implementation for the API description. The
      default implementation of the function just returns E_NOT_OK. User code can be added to
      the function to implement custom behavior.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. SmhEncryption

**描述**: Container to configure the HIS security class
AAA: encryption and decryption

该容器没有参数。

### 3. SmhEncryptionConfig

**描述**: Container to configure encryption jobs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhFunctionName
  长名称: ''
  描述: |
    Name of the encryption function, e.g.:
    SecM_EncryptAes128NoneEcb
    SecM_EncryptAes128Iso7816_4Ecb
    SecM_EncryptAes192PkcsCbc
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. SmhDecryptionConfig

**描述**: Container to configure decryption jobs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhFunctionName
  长名称: ''
  描述: |
    Name of the decryption function, e.g.:
    SecM_DecryptAes128NoneEcb
    SecM_DecryptAes128Iso7816_4Ecb
    SecM_DecryptAes192PkcsCbc
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. SmhSeedKey

**描述**: Container for configuration of SeedKey (challenge/response authentication).

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhKeyTimeout
  长名称: ''
  描述: |
    This parameter is currently not used and is only provided for compatibility reasons to the HIS
    specification.
    The timeout handling of the authorization is managed within the diagnostic layer, not in the
    security component according to OEM specification and cannot be adjusted.
  默认值: 100
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SmhCallCycle
  长名称: ''
  描述: Specifies the call cycle to the function SecTask(). Commonly SecTask() is not used. In most
      cases this parameter is only for HIS-conformance.
  默认值: 10
  最小值: 0
  最大值: 65535
```

### 6. SmhSeedConfig

**描述**: Container to configure the Seed generation.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhSeedLength
  长名称: ''
  描述: Specify the length of the seed in bytes.
  默认值: 4
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: SmhSeedType
  长名称: ''
  描述: |
    Specify the data structure of the seed:
    HIS: Seed is according to the HIS specification
    BYTE_ARRAY: Seed is stored in a byte array
    WORD_ARRAY: Seed is stored in a word array
    
    Note: BYTE_ARRAY and WORD_ARRAY are deviation from the HIS specification.
  默认值: HIS
  最小值: ''
  最大值: ''
```

### 7. SmhEntropy

**描述**: Specify if the Seed generation requires an entropy.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhEntropySize
  长名称: ''
  描述: Size of the used entropy
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: SmhEntropyUsage
  长名称: ''
  描述: |
    Specify the usage of the entropy:
    EXPLICIT: entropy musst be filled externnally
    IMPLICIT: entropy is implicitly filled
  默认值: IMPLICIT
  最小值: ''
  最大值: ''
```

### 8. SmhCsm

**描述**: Container to configure a respecive SmhJob (CsmJob) to generate a seed.

该容器没有参数。

### 9. SmhLcg

**描述**: Container to configure the LCG (linear congruential generator) algorithm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhMultiplier
  长名称: ''
  描述: |
    Multiplier of the LCG algorithm.
    Default value is taken from BCPL language.
  默认值: 2147001325
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: SmhIncrement
  长名称: ''
  描述: |
    Increment of the LCG algorithm.
    Default value is taken from BCPL language.
  默认值: 715136305
  最小值: 0
  最大值: 4294967295
```

### 10. SmhKeyConfig

**描述**: Container to configure the key computation parameter.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhKeyConstant
  长名称: ''
  描述: This is the key constant to adjust the authentication algorithm for a specific ype of ECU.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: SmhExternalComparison
  长名称: ''
  描述: If enaled, the security module will call the function SecM_CompareKeyVendor. This function
      needs to performt the key computation and the comparison.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SmhKeyType
  长名称: ''
  描述: |
    Specify the data structure of the key:
    HIS: Key is according to the HIS specification
    BYTE_ARRAY: Key is stored in a byte array
    
    Note: BYTE_ARRAY are deviation from the HIS specification.
  默认值: HIS
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SmhKeyLength
  长名称: ''
  描述: Specify the length of the key in bytes.
  默认值: 4
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: SmhSecretKeyLength
  长名称: ''
  描述: Specify the length of the secret key in bytes.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: SmhExtendedApi
  长名称: ''
  描述: |
    If enabled, the parameter SecM_ConstType of SecM_ComputeKey (SecM_ComputeKeyVendor) will change
    to a structure containing an additional context member.
    This is a deviation from the HIS specification. Modified to support configurations, where
    additional context information is required, e.g. workspace.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SmhAsymmetric
  长名称: ''
  描述: |
    If enabled, the API of SecM_ComputeKey (SecM_ComputeKeyVendor) will change from key=f(seed,k) to
    seed=f(key,k).
    This is a deviation from the HIS specification. Modified to support asymmetric key calculation
    where only the tester is able to generate the key from the original seed value, e.g. using a
    private key.
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. SmhKeyJobs

**描述**: Container to configure several SmhJobs, which can be used by SecM_ComputeKeyVendor or
SecM_CompareKeyVendor.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhFunctionName
  长名称: ''
  描述: |
    Configure the function name of the key computation job, e.g.:
    - SecM_SeedKeySha512
    - SecM_SeedKeyEncrypt
  默认值: ''
  最小值: ''
  最大值: ''
```

### 12. SmhVerification

**描述**: Container to configure the HIS security class
DDD: CRC and hash
C: MAC
CCC: Signatures

该容器没有参数。

### 13. SmhMonolithicVerification

**描述**: Container to configure the monolythic verifications.
Monolythic verifications are used to verify the data after a complete download has been performed
(OutputVerification).

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhExportVerificationWrapper
  长名称: ''
  描述: Configure if the function SecM_VerificationWrapper can be accessed externally.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhOperationCountOfWrapper
  长名称: ''
  描述: |
    Specify the number of operations:
    - SecurityClass Verification
    - CRC Total
    - Vendor Verification
    - CRC Written
  默认值: 4
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: SmhCheckAddressRangeOverflow
  长名称: ''
  描述: If enable, the security module will check that the memory range defined by address and length
      create an address range overflow.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SmhAssertReadCount
  长名称: ''
  描述: Enabled a check to verify that the read count matches the requested read length.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SmhCRCTotal
  长名称: ''
  描述: The security component always calculates a CRCtotal for a logical block when enabled. Thus,
      the application is able to verify the values within the application.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SmhCRCWritten
  长名称: ''
  描述: The security component calculates the CRC value of the written (segments) data and compares it
      against the provided verification data at offset SmhCRCOffset.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SmhMemoryAccessMode
  长名称: ''
  描述: The access mode of the security component is fixed to the memory access function. The setting
      is displayed for documentation purposes only.
  默认值: ADDRESS
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SmhReadBufferSize
  长名称: ''
  描述: Specify the length of the read buffer. The security module will read data with this size from
      the memory and provides it to the verification function.
  默认值: 64
  最小值: 0
  最大值: 4294967295
- 
  序号: 9
  名称: SmhCRCWrittenGet
  长名称: ''
  描述: The security component calculates the CRC value of the written (segments) data and provides it
      to the caller to be verified externally.
  默认值: false
  最小值: ''
  最大值: ''
```

### 14. SmhSecurityClassDDD

**描述**: Container to configure the monolythic verification for security class DDD.

该容器没有参数。

### 15. SmhSecurityClassDDDConfig

**描述**: Container to configure the monolythic verifications for security class DDD.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhIncludeAddressAndLengthInSignature
  长名称: ''
  描述: Specify if the address and length of the segments shall be taken into account in the
      verification.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhSignatureOffset
  长名称: ''
  描述: Specify the offset to the signature (CRC or hash value).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: SmhCRCOffset
  长名称: ''
  描述: Specify the offset to the CRC value (used by CRC written)
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: SmhFunctionName
  长名称: ''
  描述: |
    Configure the function name to execute the monolythic verification, e.g.:
    - SecM_VerificationClassDDD_Crc32
    - SecM_VerificationClassDDD_Sha512
  默认值: ''
  最小值: ''
  最大值: ''
```

### 16. SmhSecurityClassC

**描述**: Container to configure the monolythic verification for security class C.

该容器没有参数。

### 17. SmhSecurityClassCConfig

**描述**: Container to configure the monolythic verifications for security class C.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhIncludeAddressAndLengthInSignature
  长名称: ''
  描述: Specify if the address and length of the segments shall be taken into account in the
      verification.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhSignatureOffset
  长名称: ''
  描述: Specify the offset to the signature (MAC).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: SmhCRCOffset
  长名称: ''
  描述: Specify the offset to the CRC value (used by CRC written)
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: SmhFunctionName
  长名称: ''
  描述: |
    Configure the function name to execute the monolythic verification, e.g.:
    - SecM_VerificationClassC_HmacSha1
    - SecM_VerificationClassC_Cmac
  默认值: ''
  最小值: ''
  最大值: ''
```

### 18. SmhSecurityClassCCC

**描述**: Container to configure the monolythic verification for security class CCC.

该容器没有参数。

### 19. SmhSecurityClassCCCConfig

**描述**: Container to configure the monolythic verifications for security class CCC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhIncludeAddressAndLengthInSignature
  长名称: ''
  描述: Specify if the address and length of the segments shall be taken into account in the
      verification.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhSignatureOffset
  长名称: ''
  描述: Specify the offset to the signature.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: SmhCRCOffset
  长名称: ''
  描述: Specify the offset to the CRC value (used by CRC written)
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: SmhFunctionName
  长名称: ''
  描述: |
    Configure the function name to execute the monolythic verification, e.g.:
    - SecM_VerificationClassCCC_RsaPssSha256
    - SecM_VerificationClassCCC_Ed25519PH
  默认值: ''
  最小值: ''
  最大值: ''
```

### 20. SmhSecurityClassVendor

**描述**: Container to configure the monolythic verification for security class Vendor.

该容器没有参数。

### 21. SmhSecurityClassVendorConfig

**描述**: Container to configure the monolythic verifications for security class Vendor.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhIncludeAddressAndLengthInSignature
  长名称: ''
  描述: Specify if the address and length of the segments shall be taken into account in the
      verification.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhSignatureOffset
  长名称: ''
  描述: Specify the offset to the signature.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: SmhCRCOffset
  长名称: ''
  描述: Specify the offset to the CRC value (used by CRC written)
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: SmhFunctionName
  长名称: ''
  描述: Configure the function name to execute the monolythic verification.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 22. SmhStreamVerification

**描述**: Container to configure the stream verifications.
Stream verifications are used to verify the data during the download (InputVerification,
ProcessedVerification and PipelinedVerification).

该容器没有参数。

### 23. SmhSecurityClassDDD

**描述**: Container to configure the stream verification for security class DDD.

该容器没有参数。

### 24. SmhSecurityClassDDDConfig

**描述**: Container to configure the stream verifications for security class DDD.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhUpdateLengthOfHashedData
  长名称: ''
  描述: If enabled, the security module will update the current length of hashed data in
      SecM_SignatureParamtype::currentDataLength.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhComputationOnly
  长名称: ''
  描述: If enabled the security module will just compute the CRC/hash without verifying it. The
      computed CRC/hash is provided via SecM_SignatureParamtype::sigSourceBuffer.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SmhFunctionName
  长名称: ''
  描述: |
    Configure the function name of the stream verification, e.g.:
    - SecM_VerifyCrc32
    - SecM_VerifyHashSha512
  默认值: ''
  最小值: ''
  最大值: ''
```

### 25. SmhCrc

**描述**: Container to configure the CRC

该容器没有参数。

### 26. SmhHash

**描述**: Container to configure the hash

该容器没有参数。

### 27. SmhSecurityClassC

**描述**: Container to configure the stream verification for security class C.

该容器没有参数。

### 28. SmhSecurityClassCConfig

**描述**: Container to configure the stream verifications for security class C.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhUpdateLengthOfHashedData
  长名称: ''
  描述: If enabled, the security module will update the current length of hashed data in
      SecM_SignatureParamtype::currentDataLength.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhComputationOnly
  长名称: ''
  描述: If enabled the security module will just compute the MAC without verifying it. The computed
      MAC is provided via SecM_SignatureParamtype::sigSourceBuffer.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SmhFunctionName
  长名称: ''
  描述: |
    Configure the function name of the stream verification, e.g.:
    - SecM_VerifyMacHmacSha1
    - SecM_VerifyMacCmac
  默认值: ''
  最小值: ''
  最大值: ''
```

### 29. SmhSecurityClassCCC

**描述**: Container to configure the stream verification for security class CCC.

该容器没有参数。

### 30. SmhSecurityClassCCCConfig

**描述**: Container to configure the stream verifications for security class CCC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhFunctionName
  长名称: ''
  描述: |
    Configure the function name of the stream verification, e.g.:
    - SecM_VerifySigRsaPssSha256
    - SecM_VerifySigEd25519PH
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhUpdateLengthOfHashedData
  长名称: ''
  描述: If enabled, the security module will update the current length of hashed data in
      SecM_SignatureParamtype::currentDataLength.
  默认值: false
  最小值: ''
  最大值: ''
```

### 31. SmhDiscretHashConfig

**描述**: Configure a discrete hash for the verification, which is used to calculate a hash before verifying
the signature.

该容器没有参数。

### 32. SmhSecurityClassVendor

**描述**: Container to configure the stream verification for security class CCC.

该容器没有参数。

### 33. SmhSecurityClassVendorConfig

**描述**: Container to configure the stream verifications for security class CCC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhSizeOfVendorChecksum
  长名称: ''
  描述: Configure the size of the vendor checksum.
  默认值: 1
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SmhClassVendorFunctionName
  长名称: ''
  描述: Configure the function name of the stream verification.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 34. SmhCryptographicKeys

**描述**: Configure the cryptographic keys which are used by the SmhJob to initialize the key elements in the
crypto module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhElementIdRSAPublicExponent
  长名称: ''
  描述: Key element ID of the RSA public exponent
  默认值: 161
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: SmhElementIdRSAModulus
  长名称: ''
  描述: Key element ID of the RSA modulus.
  默认值: 160
  最小值: 0
  最大值: 4294967295
```

### 35. SmhKey

**描述**: Contains the configuration of keys.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhDescription
  长名称: ''
  描述: Short description of the key.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 36. SmhKeyValue

**描述**: Contains the configuration of key values.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhSuffix
  长名称: ''
  描述: Additional suffix to the key value.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhValue
  长名称: ''
  描述: |
    Actual key value.
    
    The value can be left empty. In this case the security module has no internal key and will only
    try to write a key if it was provided.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SmhDescription
  长名称: ''
  描述: Short description of the key value.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 37. SmhKeyOperations

**描述**: Contains the configuration for key operations

该容器没有参数。

### 38. SmhAccessKeyElementOperation

**描述**: Contains the configuration to access (Get/Set) Keys Elements

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhSetKeyElementMacroName
  长名称: ''
  描述: Name of the generated function-like macro to set the given key element.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhGetKeyElementMacroName
  长名称: ''
  描述: Name of the generated function-like macro to get the given key element.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 39. SmhCopyKeyOperation

**描述**: Contains the configuration to copy complete keys

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhCopyKeyMacroName
  长名称: ''
  描述: Name of the generated function-like macro to copy the given key.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 40. SmhCopyKeyElementOperation

**描述**: Contains the configuration to copy keys elements

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhCopyKeyElementMacroName
  长名称: ''
  描述: Name of the generated function-like macro to copy the given key element.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 41. SmhCrc

**描述**: Container to configure the CRC module

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhCRCType
  长名称: ''
  描述: Select the default CRC algorithm. This default CRC will be used for CRCTotal, CRCWritten,
      SecM_VerifyChecksumCrc and SecM_ComputeCRC.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 42. SmhCrc16

**描述**: Container to configure the CRC16.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhOptimization
  长名称: ''
  描述: Select the optimization of the CRC calculation.
  默认值: SPEED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhInitialValue
  长名称: ''
  描述: Initialization value for CRC.
  默认值: 65535
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SmhPolynomial
  长名称: ''
  描述: |
    Polynomial of the CRC calculation.
    Default value is the CCITT CRC-16 standard.
  默认值: 4129
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: SmhMode
  长名称: ''
  描述: Operation mode of the CRC calculation.
  默认值: NON_REFLECTED
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SmhComplementValue
  长名称: ''
  描述: Finalization value for CRC.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 43. SmhCrc32

**描述**: Container to configure the CRC32.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhOptimization
  长名称: ''
  描述: Select the optimization of the CRC calculation.
  默认值: SPEED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhInitialValue
  长名称: ''
  描述: Initialization value for CRC.
  默认值: 4294967295
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: SmhPolynomial
  长名称: ''
  描述: |
    Polynomial of the CRC calculation.
    The default value is a reflected value and can be found in literature in reverse bit order:
    0x04C11DB7.
  默认值: 3988292384
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: SmhMode
  长名称: ''
  描述: Operation mode of the CRC calculation.
  默认值: REFLECTED
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SmhComplementValue
  长名称: ''
  描述: Finalization value for CRC.
  默认值: 4294967295
  最小值: 0
  最大值: 4294967295
```

### 44. SmhCrc64

**描述**: Container to configure the CRC64.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SmhOptimization
  长名称: ''
  描述: Select the optimization of the CRC calculation.
  默认值: SPEED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SmhInitialValue
  长名称: ''
  描述: Initialization value for CRC.
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 3
  名称: SmhPolynomial
  长名称: ''
  描述: |
    Polynomial of the CRC calculation.
    The default value is a reflected value and can be found in literature in reverse bit order:
    0x1B.
  默认值: 15564440312192434176
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 4
  名称: SmhMode
  长名称: ''
  描述: Operation mode of the CRC calculation.
  默认值: REFLECTED
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SmhComplementValue
  长名称: ''
  描述: Finalization value for CRC.
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

### 45. SmhJob

**描述**: Container for configuration of SmhJob. The container name serves as a symbolic name for the
identifier of a job configuration.

该容器没有参数。

### 46. SmhHash

**描述**: Container for Hash configurations.

该容器没有参数。

### 47. SmhEncryption

**描述**: Container for Encryption configurations.

该容器没有参数。

### 48. SmhDecryption

**描述**: Container for Decryption configurations.

该容器没有参数。

### 49. SmhMacGenerate

**描述**: Container for MacGenerate configurations.

该容器没有参数。

### 50. SmhMacVerify

**描述**: Container for MacVerify configurations.

该容器没有参数。

### 51. SmhRandomGenerate

**描述**: Container for RandomGenerate configurations.

该容器没有参数。

### 52. SmhSignatureVerify

**描述**: Container for SignatureVerify configurations.

该容器没有参数。

### 53. SmhRandomSeed

**描述**: Container for RandomSeed configurations.

该容器没有参数。

