# Cal

## 模块描述

Configuration of the Cal (CryptoAbstractionLibrary) module.

## 容器列表

### 1. CalAsymDecrypt

**描述**: Container for incorporation of AsymDecrypt primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymDecryptMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement an
      asymmetrical decryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalAsymDecryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement an
      asymmetrical decryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 2. CalAsymDecryptConfig

**描述**: Container for configuration of service AsymDecrypt. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymDecryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalAsymDecryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. CalAsymEncrypt

**描述**: Container for incorporation of AsymEncrypt primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymEncryptMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement an
      asymmetrical encryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalAsymEncryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement an
      asymmetrical encryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 4. CalAsymEncryptConfig

**描述**: Container for configuration of service AsymEncrypt. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymEncryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalAsymEncryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. CalAsymPrivateKeyExtract

**描述**: Container for incorporation of AsymPrivateKeyExtract primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymPrivateKeyExtractMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement an
      asymmetrical private key extraction.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalAsymPrivateKeyExtractMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement an
      asymmetrical private key extraction.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 6. CalAsymPrivateKeyExtractConfig

**描述**: Container for configuration of service AsymPrivateKeyExtract.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymPrivateKeyExtractInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalAsymPrivateKeyExtractPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. CalAsymPrivateKeyWrapAsym

**描述**: Container for incorporation of AsymPrivateKeyWrapAsym primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymPrivateKeyWrapAsymMaxPrivKeySize
  长名称: ''
  描述: The maximum length, in bytes, of all private information types used in all CPL primitives
      which implement an asymmetrical key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalAsymPrivateKeyWrapAsymMaxPubKeySize
  长名称: ''
  描述: The maximum length, in bytes, of all public key types used in all CPL primitives which
      implement an asymmetrical key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 8. CalAsymPrivateKeyWrapAsymConfig

**描述**: Container for configuration of service AsymPrivateKeyWrapAsym.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymPrivateKeyWrapAsymInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalAsymPrivateKeyWrapAsymPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. CalAsymPrivateKeyWrapSym

**描述**: Container for incorporation of AsymPrivateKeyWrapSym primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymPrivateKeyWrapSymMaxPrivKeySize
  长名称: ''
  描述: The maximum length, in bytes, of all private information types used in all CPL primitives
      which implement an asymmetrical key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalAsymPrivateKeyWrapSymMaxSymKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement an
      asymmetrical key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 10. CalAsymPrivateKeyWrapSymConfig

**描述**: Container for configuration of service AsymPrivateKeyWrapSym.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymPrivateKeyWrapSymInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalAsymPrivateKeyWrapSymPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. CalAsymPublicKeyExtract

**描述**: Container for incorporation of AsymPublicKeyExtract primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymPublicKeyExtractMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement an
      asymmetrical public key extraction.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalAsymPublicKeyExtractMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement an
      asymmetrical public key extraction.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 12. CalAsymPublicKeyExtractConfig

**描述**: Container for configuration of service AsymPublicKeyExtract.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalAsymPublicKeyExtractInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalAsymPublicKeyExtractPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 13. CalChecksum

**描述**: Container for incorporation of Checksum primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalChecksumMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a
      checksum computation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 14. CalChecksumConfig

**描述**: Container for configuration of service Checksum. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalChecksumInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalChecksumPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 15. CalGeneral

**描述**: Container for common configuration options.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalMaxAlignScalarType
  长名称: ''
  描述: The scalar type which has the maximum alignment restrictions on the given platform.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 16. CalHash

**描述**: Container for incorporation of Hash primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalHashMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a
      hash computation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 17. CalHashConfig

**描述**: Configurations for the Hash service. The container name serves as a symbolic name for the identifier
of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalHashInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalHashPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 18. CalKeyDerive

**描述**: Container for incorporation of KeyDerive primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalKeyDeriveMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a key
      derivation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalKeyDeriveMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CRL primitives which implement a key
      derivation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 19. CalKeyDeriveConfig

**描述**: Container for configuration of service KeyDerive. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalKeyDeriveInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalKeyDerivePrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 20. CalKeyExchangeCalcPubVal

**描述**: Container for incorporation of KeyExchangeCalcPubVal primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalKeyExchangeCalcPubValMaxBaseTypeSize
  长名称: ''
  描述: The maximum length, in bytes, of all base types used in all CPL primitives which implement a
      public value calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalKeyExchangeCalcPubValMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a
      public value calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: CalKeyExchangeCalcPubValMaxPrivateTypeSize
  长名称: ''
  描述: The maximum length, in bytes, of all private information types used in all CPL primitives
      which implement a public value calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 21. CalKeyExchangeCalcPubValConfig

**描述**: Container for configuration of service KeyExchangeCalcPubVal. The container name serves as a
symbolic name for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalKeyExchangeCalcPubValInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalKeyExchangeCalcPubValPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 22. CalKeyExchangeCalcSecret

**描述**: Container for incorporation of KeyExchangeCalcSecret primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalKeyExchangeCalcSecretMaxBaseTypeSize
  长名称: ''
  描述: The maximum length, in bytes, of all base types used in all CPL primitives which implement a
      shared secret calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalKeyExchangeCalcSecretMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a
      shared secret calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: CalKeyExchangeCalcSecretMaxPrivateTypeSize
  长名称: ''
  描述: The maximum length, in bytes, of all private information types used in all CPL primitives
      which implement a shared secret calculation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 23. CalKeyExchangeCalcSecretConfig

**描述**: Container for configuration of service KeyExchangeCalcSecret. The container name serves as a
symbolic name for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalKeyExchangeCalcSecretInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalKeyExchangeCalcSecretPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 24. CalMacGenerate

**描述**: Container for incorporation of MacGenerate primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalMacGenerateMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a MAC
      generation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalMacGenerateMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a MAC
      generation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 25. CalMacGenerateConfig

**描述**: Configurations for the MacGenerate service. The container name serves as a symbolic name for the
identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalMacGenerateInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalMacGeneratePrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 26. CalMacVerify

**描述**: Container for incorporation of MacVerify primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalMacVerifyMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a MAC
      verification.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalMacVerifyMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a MAC
      verification.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 27. CalMacVerifyConfig

**描述**: Container for configuration of service MacVerify. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalMacVerifyInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalMacVerifyPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 28. CalRandomGenerate

**描述**: Container for incorporation of RandomGenerate primitives.

该容器没有参数。

### 29. CalRandomGenerateConfig

**描述**: Container for configuration of service RandomGenerate. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalRandomGenerateInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalRandomGeneratePrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 30. CalRandomSeed

**描述**: Container for incorporation of RandomSeed primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalRandomMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement
      seeding or generating a random number.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 31. CalRandomSeedConfig

**描述**: Container for configuration of service RandomSeed. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalRandomSeedInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalRandomSeedPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 32. CalSignatureGenerate

**描述**: Container for incorporation of SignatureGenerate primitives

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSignatureGenerateMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a
      signature generation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalSignatureGenerateMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a
      signature generation.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 33. CalSignatureGenerateConfig

**描述**: Container for configuration of service SignatureGenerate. The container name serves as a symbolic
name for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSignatureGenerateInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalSignatureGeneratePrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 34. CalSignatureVerify

**描述**: Container for incorporation of SignatureVerify primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSignatureVerifyMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a
      signature verification.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalSignatureVerifyMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a
      signature verification.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 35. CalSignatureVerifyConfig

**描述**: Container for configuration of service SignatureVerify. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSignatureVerifyInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalSignatureVerifyPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 36. CalSymBlockDecrypt

**描述**: Container for incorporation of SymBlockDecrypt primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymBlockDecryptMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a
      symmetrical block decryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalSymBlockDecryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a
      symmetrical block decryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 37. CalSymBlockDecryptConfig

**描述**: Container for configuration of service SymBlockDecrypt. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymBlockDecryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalSymBlockDecryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 38. CalSymBlockEncrypt

**描述**: Container for incorporation of SymBlockEncrypt primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymBlockEncryptMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a
      symmetrical block encryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalSymBlockEncryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a
      symmetrical block encryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 39. CalSymBlockEncryptConfig

**描述**: Container for configuration of service SymBlockEncrypt. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymBlockEncryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalSymBlockEncryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 40. CalSymDecrypt

**描述**: Container for incorporation of SymDecrypt primitives

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymDecryptMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a
      symmetrical decryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalSymDecryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a
      symmetrical decryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 41. CalSymDecryptConfig

**描述**: Container for configuration of service SymDecrypt.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymDecryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalSymDecryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 42. CalSymEncrypt

**描述**: Container for incorporation of SymEncrypt primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymEncryptMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a
      symmetrical encryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalSymEncryptMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a
      symmetrical encryption.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 43. CalSymEncryptConfig

**描述**: Container for configuration of service SymEncrypt. The container name serves as a symbolic name for
the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymBlockEncryptInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalSymEncryptPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 44. CalSymKeyExtract

**描述**: Container for incorporation of SymKeyExtract primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymKeyExtractMaxCtxBufByteSize
  长名称: ''
  描述: The maximum, in bytes, of all context buffers used in all CPL primitives which implement a
      symmetrical key extraction.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalSymKeyExtractMaxKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a
      symmetrical key extraction.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 45. CalSymKeyExtractConfig

**描述**: Container for configuration of service SymKeyExtract. The container name serves as a symbolic name
for the identifier of a service configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymKeyExtractInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalSymKeyExtractPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 46. CalSymKeyWrapAsym

**描述**: Container for incorporation of SymKeyWrapAsym primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymKeyWrapAsymMaxPubKeySize
  长名称: ''
  描述: The maximum length, in bytes, of all public key  types used in all CPL primitives which
      implement a symmetrical key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CalSymKeyWrapAsymMaxSymKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a
      symmetrical key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 47. CalSymKeyWrapAsymConfig

**描述**: Container for configuration of service SymKeyWrapAsym.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymKeyWrapAsymInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalSymKeyWrapAsymPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 48. CalSymKeyWrapSym

**描述**: Container for incorporation of SymKeyWrapSym primitives.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymKeyWrapSymMaxSymKeySize
  长名称: ''
  描述: The maximum, in bytes, of all key lengths used in all CPL primitives which implement a
      symmetrical key wrapping.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 49. CalSymKeyWrapSymConfig

**描述**: Container for configuration of service SymKeyWrapSym.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CalSymKeyWrapSymInitConfiguration
  长名称: ''
  描述: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CalSymKeyWrapSymPrimitiveName
  长名称: ''
  描述: Name of the cryptographic primitive to use.
  默认值: ''
  最小值: ''
  最大值: ''
```

