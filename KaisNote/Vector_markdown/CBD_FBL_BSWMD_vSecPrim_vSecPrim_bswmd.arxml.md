# vSecPrim

## 模块描述

Software Crypto Library

## 容器列表

### 1. vSecPrimBasicAlgorithms

**描述**: Container for basic algorithm configuration.

该容器没有参数。

### 2. vSecPrimHash

**描述**: Container for hash algorithm configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSecPrimSHA1Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    SHA1
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSecPrimRIPEMD160Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    RIPEMD160
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSecPrimSHA2_256Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithms can be used:
    SHA2-224
    SHA2-256
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vSecPrimSHA2_512Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithms can be used:
    SHA2-384
    SHA2-512
    SHA2-512_224
    SHA2-512_256
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vSecPrimSHA3Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithms can be used:
    SHA3-224
    SHA3-256
    SHA3-384
    SHA3-512
    SHAKE128
    SHAKE256
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vSecPrimMD5Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    MD5
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. vSecPrimRandomNumberGeneration

**描述**: Container for random number generation algorithm configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSecPrimFIPS186Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    FIPS186-2
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSecPrimCtrDrbgEnabled
  长名称: CTR DRBG Enabled
  描述: |
    If enabled, the following algorithm can be used:
    CTR_DRBG based on AES
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSecPrimHashDrbgEnabled
  长名称: HASH DRBG Enabled
  描述: |
    If enabled, the following algorithm can be used:
    HASH_DRBG based on SHA2-512
  默认值: false
  最小值: ''
  最大值: ''
```

### 4. vSecPrimSymmetricAlgorithms

**描述**: Container for symmetric algorithm configuration.

该容器没有参数。

### 5. vSecPrimCipher

**描述**: Container for symmetric cipher algorithm configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSecPrimAes128Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    AES128
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSecPrimAes192Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    AES192
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSecPrimAes256Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    AES256
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vSecPrimGcmEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithms can be used:
    AES-GCM
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vSecPrimAesCcmEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithms can be used:
    AES128-CCM
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vSecPrimDesEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    DES
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vSecPrimRC2Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    RC2 (ARC2)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vSecPrimTDesEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    TDES (3DES)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vSecPrimChaCha20Enabled
  长名称: ChaCha20 Enabled
  描述: |
    If enabled, the following algorithm can be used:
    ChaCha20
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: vSecPrimAeadChaCha20Poly1305Enabled
  长名称: Aead ChaCha20 and Poly1305 Enabled
  描述: |
    If enabled, the following algorithm can be used:
    Aead with ChaCha20 and Poly1305
  默认值: false
  最小值: ''
  最大值: ''
```

### 6. vSecPrimMac

**描述**: Container for Mac algorithm configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSecPrimSipHashEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    SipHash
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSecPrimCmacEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    CMAC
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSecPrimHMacSHA1Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    HMac using SHA1 as hash algorithm
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vSecPrimHMacRMD160Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    HMac using RMD160 as hash algorithm
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vSecPrimHMacSHA2_256Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    HMac using SHA2_256 as hash algorithm
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vSecPrimGMacEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    GMac
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vSecPrimPoly1305Enabled
  长名称: Poly1305 Enabled
  描述: |
    If enabled, the following algorithm can be used:
    Poly1305
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vSecPrimHMacSHA2_384Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    HMac using SHA2_384 as hash algorithm
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. vSecPrimAsymmetricAlgorithms

**描述**: Container for asymmetric algorithm configuration.

该容器没有参数。

### 8. vSecPrimSignature

**描述**: Container for signature algorithm configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSecPrimRSA_PSS_RIPEMD160Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    RSA Signature Generation / Verification according to PSS using RIPEMD160 as hash function
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSecPrimRSA_PSS_SHA1Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    RSA Signature Generation / Verification according to PSS using SHA1 as hash function
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSecPrimRSA_PSS_SHA2_256Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    RSA Signature Generation / Verification according to PSS using SHA2_256 as hash function
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vSecPrimRSA_V15_RIPEMD160Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    RSA Signature Generation / Verification according to RSASSA-PKCS1-v1_5 using RIPEMD160 as hash
    function
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vSecPrimRSA_V15_SHA1Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    RSA Signature Generation / Verification according to RSASSA-PKCS1-v1_5 using SHA1 as hash
    function
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vSecPrimRSA_V15_SHA2_256Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    RSA Signature Generation / Verification according to RSASSA-PKCS1-v1_5 using SHA2_256 as hash
    function
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vSecPrimECDSA_25519Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    ECDSA Signature Generation / Verification according to curve ED25519
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vSecPrimECDSA_GenericEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    ECDSA Signature Generation / Verification using generic curve
  默认值: false
  最小值: ''
  最大值: ''
```

### 9. vSecPrimKeyExchange

**描述**: Container for key exchange algorithm configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSecPrimECDH_25519Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    ECDH Key Exchange according to curve ED25519
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSecPrimECDH_GenericEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    ECDH Key Exchange using generic curve
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSecPrimECBD_GenericEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    EC Burmester Desmedt Key Exchange using generic curve
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vSecPrimSPAKE2pEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    SPAKE2+ preamble phase
    SPAKE2+ Key Exchange using curve SECP256r1, SHA256, HKDF HMAC SHA256 and CMAC AES128
  默认值: false
  最小值: ''
  最大值: ''
```

### 10. vSecPrimKeyDerivation

**描述**: Container for key derivation algorithm configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSecPrimPKCS5Enabled
  长名称: PKCS5 HMac SHA1 Enabled
  描述: |
    If enabled, the following algorithm can be used:
    Key Derivation according to PKCS5 / KDF2 with underlying primitive HMAC SHA1.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSecPrimANSI_X963Enabled
  长名称: ANSI X9.63 SHA1 Enabled
  描述: |
    If enabled, the following algorithm can be used:
    Key Derivation according to ANSI X963 SHA1
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSecPrimANSI_X963_SHA256Enabled
  长名称: ANSI X9.63 SHA256 Enabled
  描述: |
    If enabled, the following algorithm can be used:
    Key Derivation according to ANSI X963 SHA256
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vSecPrimPKCS5HMacSHA256Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    Key Derivation according to PKCS5 / KDF2 with underlying primitive HMAC SHA256.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vSecPrimANSI_X963_SHA512Enabled
  长名称: ANSI X9.63 SHA512 Enabled
  描述: |
    If enabled, the following algorithm can be used:
    Key Derivation according to ANSI X963 SHA512
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vSecPrimHKDF_HMAC_SHA256Enabled
  长名称: HKDF HMAC SHA256 Enabled
  描述: |
    If enabled, the following algorithm can be used:
    Key Derivation according to HKDF HMAC SHA256
    
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. vSecPrimCipher

**描述**: Container for asymmetric cipher algorithm configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSecPrimRSA_OAEP_SHA1Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    RSA Asymmetric encryption according to OAEP using SHA1 as hash algorithm
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSecPrimRSA_OAEP_SHA2_256Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    RSA Asymmetric encryption according to OAEP using SHA2_256 as hash algorithm
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSecPrimRSA_V15Enabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    RSA Asymmetric encryption according to RSASSA-PKCS1-v1_5
  默认值: false
  最小值: ''
  最大值: ''
```

### 12. vSecPrimKeyGeneration

**描述**: Container for key generation algorithm configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSecPrimECCEnabled
  长名称: ''
  描述: |
    If enabled, the following algorithm can be used:
    Key Generation using elliptic curves
  默认值: false
  最小值: ''
  最大值: ''
```

### 13. vSecPrimOptimization

**描述**: Container for optimization configuration options.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSecPrimAesSpeedUp
  长名称: ''
  描述: |
    Defines the optimization level of the Aes algorithms.
    The higher the level, the faster the code will be executed at the cost of a higher memory
    consumption.
  默认值: SPEED_UP_LEVEL_3
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSecPrimSha1SpeedUp
  长名称: ''
  描述: |
    Defines the optimization level of the SHA1 algorithms.
    The higher the level, the faster the code will be executed at the cost of a higher memory
    consumption.
  默认值: SPEED_UP_LEVEL_1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSecPrimSha256SpeedUp
  长名称: ''
  描述: |
    Defines the optimization level of the SHA2_256 algorithms.
    The higher the level, the faster the code will be executed at the cost of a higher memory
    consumption.
  默认值: SPEED_UP_LEVEL_0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vSecPrimSha512SpeedUp
  长名称: ''
  描述: |
    Defines the optimization level of the SHA2_512 algorithms.
    The higher the level, the faster the code will be executed at the cost of a higher memory
    consumption.
  默认值: SPEED_UP_LEVEL_0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vSecPrimChaCha20SpeedUp
  长名称: ChaCha20 Speed Up
  描述: |
    Defines the optimization level of the ChaCha20 algorithms.
    The higher the level, the faster the code will be executed at the cost of a higher memory
    consumption.
  默认值: SPEED_UP_LEVEL_1
  最小值: ''
  最大值: ''
```

### 14. vSecPrimGeneral

**描述**: Container for common configuration options.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSecPrimUserConfigFile
  长名称: ''
  描述: |
    User configuration file that shall be part of the vSecPrim configuration.
    If you want to overwrite or provide own settings in the generated configuration file, you can
    specify a path to a user defined configuration file. The user defined configuration file will be
    included at the end of the generated file. Thus definitions in the user defined configuration
    file can overwrite definitions in the generated configuration file.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSecPrimRSAMaxKeySize
  长名称: ''
  描述: |
    Maximum key size in Bits which can be used for the RSA algorithms.
    The range is from 512 to 4096 Bit.
  默认值: RSA_MAX_KEY_SIZE_2048
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSecPrimECPMaxKeySize
  长名称: ''
  描述: |
    Maximum key size in Bits which can be used for the ECP algorithms.
    The range is from 160 to 521 Bit.
  默认值: ECP_MAX_KEY_SIZE_256
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vSecPrimClearWorkspaceEnabled
  长名称: ''
  描述: If enabled, the workspace is cleared after the processing of any algorithm has finished.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vSecPrimSupportUInt64
  长名称: ''
  描述: Distinguish if uint64 is provided on the platform.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vSecPrimWatchdogLevel
  长名称: ''
  描述: |
    Defines the level of watchdog call frequency.
    WD_LEVEL_0: WD is disabled
    WD_LEVEL_1: WD called from outer functions only
    WD_LEVEL_2: WD called from inner functions as well
    WD_LEVEL_3: WD also called in inner hash loops
  默认值: WD_LEVEL_0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vSecPrimSizeOfEsltLength
  长名称: Size Of eslt_Length
  描述: |
    Decide which type is used for eslt_Length.
    If size is set to uint16 max input length for single update is limitied to 65535 bytes.
  默认值: SIZE_UINT32
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vSecPrimCTRDRBGAES128SecurityStrength
  长名称: Security Strength of CTRDRBG AES128
  描述: The security strength determines the minimum entropy input length for CTR DRBG AES128.
  默认值: SECURITY_STRENGTH_128
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vSecPrimDrbgReseedInterval
  长名称: ''
  描述: Number of requests for random number generation with CTR DRBG without reseeding.
  默认值: 4294967295
  最小值: 1
  最大值: 4294967295
- 
  序号: 10
  名称: vSecPrimSPAKE2pMaxAADSize
  长名称: ''
  描述: Maximum size of associated data for SPAKE2+ MAC key derivation in bytes. The range is between
      0 and (2^13 - 1) bytes.
  默认值: 16
  最小值: 1
  最大值: 8191
- 
  序号: 11
  名称: vSecPrimSPAKE2pPreambleOKMLength
  长名称: ''
  描述: Maximum size of PBKDF output data for SPAKE2+ in the preamble phase in bytes.
  默认值: 64
  最小值: 1
  最大值: 65535
```

