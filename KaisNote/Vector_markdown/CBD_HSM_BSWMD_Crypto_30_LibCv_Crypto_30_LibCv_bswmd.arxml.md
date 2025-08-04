# Crypto

## 模块描述

Software Crypto Driver

## 容器列表

### 1. CryptoDriverObjects

**描述**: Container for Crypto Driver Objects

该容器没有参数。

### 2. CryptoDriverObject

**描述**: Container for configuration of Crypto Driver Object. The container name serves as a symbolic name
for the identifier of a Crypto Driver Object.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoDriverObjectId
  长名称: ''
  描述: Identifier of the Crypto Driver Object. The Crypto Driver Object offers different crypto
      primitives.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoDriverObjectQueueSize
  长名称: ''
  描述: Size of the queue in the Crypto Driver. Defines the maximum number of jobs in the Crypto
      Driver Object queue. If it is set to 0, queueing is disabled in the Crypto Driver
      Object. This Crypto Driver does not support queuing but uses the buffer for asynchronous
      processing therefore the value need to be set to 1.
  默认值: 1
  最小值: 1
  最大值: 1
```

### 3. CryptoGeneral

**描述**: Container for common configuration options.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoVersionInfoApi
  长名称: ''
  描述: |
    Pre-processor switch to enable and disable availability of the API Crypto_GetVersionInfo().
    - True: API Crypto_GetVersionInfo() is available
    - False: API Crypto_GetVersionInfo() is not available.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryptoMainFunctionPeriod
  长名称: ''
  描述: Specifies the period of main function Crypto_MainFunction in seconds. 
  默认值: 0.01
  最小值: 0
  最大值: 3600
- 
  序号: 3
  名称: CryptoDevErrorDetect
  长名称: ''
  描述: |
    Switches the development error detection and notification on or off.
    - True: detection and notification is enabled.
    - False: detection and notification is disabled.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CryptoSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CryptoUseVStdLib
  长名称: Use VStdLib
  描述: If enabled the VStdLib is used for copy and clear data operations. If there is no VStdLib,
      disable the switch to use the implementation of the Crypto.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CryptoKeyElementDelete
  长名称: ''
  描述: If Crypto_KeyElementSet is called with the length 0 the key will be overwritten with 0 and the
      length is set to 0. If KeyElementDelete is enabled the standard AUTOSAR DET check for
      the given key element length in Crypto_KeyElementSet will be disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CryptoAlignKeyStorage
  长名称: ''
  描述: Enable, to align each key inside the KeyStorage. The KeyStorage size will increase but the
      access will be faster.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CryptoNvMEnableSetRamBlockStatus
  长名称: NvM Enable SetRamBlockStatus
  描述: Select if SetRamBlockStatus shall be called in KeyValidSet.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CryptoRedirection
  长名称: ''
  描述: Enable job input/output redirection to key elements. This is a Autosar 4.4 feature. Therefore
      a Csm and CryIf is required which also supports this feature
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CryptoWatchdogTriggerFunction
  长名称: ''
  描述: |
    This function is called by the vSecPrim to trigger the watchdog. The vSecPrim watchdog level
    need to be set additional.
    void "WatchdogTriggerFunction"(void)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CryptoDefaultRandomMaxRetries
  长名称: ''
  描述: Number of max retries for default random number generation. The calculation is reexecuted if
      the default random source is used from two driver objects at the same time.
  默认值: 10
  最小值: 1
  最大值: 65535
- 
  序号: 12
  名称: CryptoUserConfigFile
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
  序号: 13
  名称: CryptoNumberOfLongTermPrimitiveWorkspace
  长名称: ''
  描述: |
    Determin the number of workspaces used for long term primitive exection.
    See Technical Reference for more information including which primitive use this workspace e.g.
    Spake2+ Key Exchange.
    
  默认值: 0
  最小值: 0
  最大值: 255
```

### 4. CryptoKeyExchangePrimitives

**描述**: Configuration of a Crypto Key Exchange Primitive. If there is an algorithm configured, key exchange
is usable via Crypto_KeyExchangeCalcPubVal and Crypto_KeyExchangeCalcSecret API.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoKeyExchangeAlgorithm
  长名称: ''
  描述: |
    Determines the algorithm used for the crypto key exchange.
    Disable to save ROM.
  默认值: CRYPTO_KEY_EXCHANGE_ALGORITHM_X25519
  最小值: ''
  最大值: ''
```

### 5. CryptoKeyDerivePrimitives

**描述**: If enabled, key derivation is usable via Crypto_KeyDerive API.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoKeyDeriveAlgorithm
  长名称: ''
  描述: |
    Determines the algorithm used for the crypto key derive.
    Disable to save ROM.
  默认值: CRYPTO_KDF_ALGO_SYM_NIST_800_108_CNT_MODE_SHA256
  最小值: ''
  最大值: ''
```

### 6. CryptoMacPrimitives

**描述**: Determines the algorithm used for the crypto mac jobs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoCmacAesRoundkeyReuse
  长名称: ''
  描述: |
    The AES CMAC supports the reuse of calculated AES round keys. If this feature is enabled
    the round keys are hold in the driver object. The round keys are hold until a different job type
    is processed (not CMAC AES128 and CMAC AES256) or the corresponding key has changed.
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. CryptoCipherPrimitives

**描述**: Determines the algorithm used for the crypto cipher jobs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoEnableAES256
  长名称: ''
  描述: Enable AES 256 for driver objects with AES. Otherwise only AES 128 is available.
  默认值: false
  最小值: ''
  最大值: ''
```

### 8. CryptoKeyGeneratePrimitives

**描述**: If enabled, key generate is usable via Crypto_KeyGenerate API.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoKeyGenerateAlgorithm
  长名称: ''
  描述: |
    Determines the algorithm used for the crypto key generation.
    Disable to save ROM.
  默认值: CRYPTO_KEY_GENERATE_ALGORITHM_SYMMETRIC_GENERIC
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryptoKeyGenerateMaxLength
  长名称: ''
  描述: Select the max key length in bytes.This parameter is only used for
      CRYPTO_KEY_GENERATE_ALGORITHM_SYMMETRIC_GENERIC.
  默认值: 32
  最小值: 1
  最大值: 65535
```

### 9. CryptoKeyElements

**描述**: Container for CRYPTO key elements.

该容器没有参数。

### 10. CryptoKeyElement

**描述**: Configuration of a CryptoKeyElement

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoKeyElementId
  长名称: ''
  描述: Identifier of the CRYPTO key element 
  默认值: 1
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoKeyElementSize
  长名称: ''
  描述: Maximum size of a CRYPTO key element in bytes 
  默认值: 16
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: CryptoKeyElementInitValue
  长名称: ''
  描述: Value which will be used to fill the element during initialization, when the element is not
      already initialized.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CryptoKeyElementReadAccess
  长名称: ''
  描述: |
    Define the reading access rights of the key element.
    CRYPTO_RA_DENIED = key element cannot be read from outside the Crypto Driver
    CRYPTO_RA INTERNAL_COPY = key element can be copied to another key element in the same crypto
    driver.
    CRYPTO_RA_ALLOWED = key element can be read as plaintext
    CRYPTO_RA_ENCRYPTED = key element can be read encrypted. E.g. SHE Ram-Key export.
  默认值: RA_ALLOWED
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CryptoKeyElementAllowPartialAccess
  长名称: ''
  描述: |
    Enable or disable writing and reading the key element with data smaller than the size of the
    element.
    - True: enable partial access of the key element
    - False: disable partial access of the key element
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CryptoKeyElementPersist
  长名称: ''
  描述: |
    Enable or disable persisting of the key element in non-volatile storage.
    - True: enable persisting of the key element.
    - False: disable persisting of the key element.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CryptoKeyElementWriteAccess
  长名称: ''
  描述: |
    Define the writing access rights of the key element
    CRYPTO_WA_DENIED = key element cannot be written from outside the Crypto Driver
    CRYPTO_WA INTERNAL_COPY = key element can be filled with another key element in the same crypto
    driver.
    CRYPTO_WA_ALLOWED = key element can be rewritten as plaintext
    CRYPTO_WA_ENCRYPTED = key element can be written encrypted. E.g. SHE load key.
    
  默认值: WA_ALLOWED
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CryptoKeyElementFormat
  长名称: ''
  描述: |
    Defines the format for the key element. This is the format used to provide or extract the key
    data from the driver.
    
    Parameter not used.
  默认值: CRYPTO_KE_FORMAT_BIN_OCTET
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CryptoKeyElementWriteOnce
  长名称: ''
  描述: |
    Determine if a key shall only be writeable once.
    - non-persist keys: Only once after start-up.
    - persist keys: Only once for all time.
    A init value does not affects this behavior.
    If a init value shall not be overwritable use CRYPTO_WA_DENIED.
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. CryptoKeyTypes

**描述**: Container for CRYPTO key types

该容器没有参数。

### 12. CryptoKeyType

**描述**: Configuration of a CryptoKeyType

该容器没有参数。

### 13. CryptoKeys

**描述**: Container for CRYPTO keys

该容器没有参数。

### 14. CryptoKey

**描述**: Configuration of a CryptoKey

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoKeyId
  长名称: ''
  描述: Identifier of the CRYPTO key
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoKeyDeriveIterations
  长名称: ''
  描述: |
    Holds the number of iterations to be performed by the key derivation primitive.
    
    Parameter not used.
  默认值: 1
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: CryptoKeyNvId
  长名称: ''
  描述: The CRYPTO_KEY_NV_ID is used to give a key a unique id for the complete lifecycle even if the
      CRYPTO_KEY_ID changed. The CRYPTO_KEY_NV_ID is used to identify a key within the Nv
      Block over several different configurations.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 15. CryptoPrimitives

**描述**: Container for CRYPTO primitives

该容器没有参数。

### 16. CryptoPrimitive

**描述**: Configuration of a CryptoPrimitive

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoPrimitiveAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service.
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryptoPrimitiveAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: CRYPTO_ALGOMODE_NOT_SET
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CryptoPrimitiveService
  长名称: ''
  描述: Determines the crypto service used for defining the capabilities
  默认值: CRYPTO_MAC_VERIFY
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CryptoPrimitiveAlgorithmSecondaryFamily
  长名称: ''
  描述: |
    Determines the algorithm secondary family used for the crypto service.
    See Technical Reference for cipher suites.
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
```

### 17. CryptoSheKeyUpdate

**描述**: Container for She key update,
Present Container, the She key update with M1,M2 and M3 can be used for setting/updating a She key.
Remove Container to save ROM and Runtime.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoSheEnableFid
  长名称: ''
  描述: |
    Enable check of FID.
    If the check is disabled all flags will be interpreted as 0 and the keys can be used for each
    service.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryptoSheEnableCounter
  长名称: ''
  描述: |
    Enable check of Counter.
    If the feature is enabled ech she key requires a key element with the Id
    CRYPTO_KE_CUSTOM_SHE_COUNTER. Otherwise the key element can be exclude to reduce KeyStorage
    size.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CryptoSheDebugCmd
  长名称: ''
  描述: |
    Enable She DEBUG_CMD.
    If the check is enabled the DEBUG_CMD requires the CryptoSheInfoKeyRef.
  默认值: false
  最小值: ''
  最大值: ''
```

### 18. CryptoShePage

**描述**: Container for a She page.
A she page includes up to 11 She keys.
Key_1 - Key_10 and one RAM_Key.
The Encryption and Mac constants are defined for each page.
The SECRET_KEY, MASTER_ECU_KEY, BOOT_MAC_KEY and BOOT_MAC are mapped to page 1,

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoShePageEncryptionConstant
  长名称: KEY_UPDATE_ENC_C
  描述: |
    KEY_UPDATE_ENC_C
    Page_1: 010153484500800000000000000000B0 h
    Page_2: 018153484500800000000000000000B0 h
    Page_N: Not Specified
    
    String may only consist concatenated hex values without leading 0x and any spaces. 32 Bytes are
    needed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryptoShePageMacConstant
  长名称: KEY_UPDATE_MAC_C
  描述: |
    KEY_UPDATE_MAC_C
    Page_1: 010253484500800000000000000000B0 h
    Page_2: 018253484500800000000000000000B0 h
    Page_N: Not Specified
    
    String may only consist concatenated hex values without leading 0x and any spaces. 32 Bytes are
    needed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CryptoShePageId
  长名称: ''
  描述: Id of the She Page.
  默认值: 1
  最小值: 1
  最大值: 255
```

### 19. CryptoSheKey

**描述**: Container for a She key.
It is possible to configure Key_1 - Key_10 and Ram_Key for each page.
Key_1 = She Id 4
...
Key_10 = She Id 13
RAM_Key = She Id 14

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoSheKeyId
  长名称: ''
  描述: |
    Set the She key Id.
    Key_1 = She Id 4
    ...
    Key_10 = She Id 13
    RAM_Key = She Id 14
  默认值: 4
  最小值: 4
  最大值: 14
```

### 20. CryptoNvStorage

**描述**: This container is used for the non-volatile storage of the key information

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoNvManagementDataPerKey
  长名称: ''
  描述: |
    This parameter is for information purposes only and can not be changed.
    
    This Parameter shows how many additional bytes are needed per key element when it is stored in
    the NVRAM.
    
    e.g. 16 bytes AES key needs 20 bytes of data flash inside the NvRam if the management data is 4
    bytes long.
  默认值: 4
  最小值: 4
  最大值: 4
- 
  序号: 2
  名称: CryptoNvWriteBlockFctName
  长名称: ''
  描述: This function is called by the LibCv to write a Nv Block.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 21. CryptoNvBlock

**描述**: A NvBlock describes the mapping of to be persisted keys and a NvM Decsriptor.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoNvBlockId
  长名称: ''
  描述: Id of the NvBlock. This value has to be unique.
  默认值: 0
  最小值: 0
  最大值: 4294967294
- 
  序号: 2
  名称: CryptoNvBlockLength
  长名称: ''
  描述: |
    Size of the Nv Block
    Must be the same size as the referenced Nv Block.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: CryptoNvBlockFillLevel
  长名称: ''
  描述: |
    Number of used bytes inside the Nv Block.
    This value is for information only.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: CryptoNvBlockProcessing
  长名称: ''
  描述: |
    Set the block processing type.
    DEFERRED: write block will not be triggered by the crypto.The block can be written manually and
    is written on shutdown.
    IMMEDIATE: write block will be triggered by the crypto with validation of the key.
  默认值: NV_PROCESSING_DEFERRED
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CryptoNvBlockConsistencyLevel
  长名称: ''
  描述: |
    Select the storage kind.
    NONE: none (deprecated)
    DETECT: CRC layout checksum, checks if the key storage layout has changed. If the layout has
    change the initial data is restored.
  默认值: NV_CONSISTENCY_LEVEL_DETECT
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CryptoNvBlockRevision
  长名称: ''
  描述: Revision of the NvBlock.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: CryptoNvBlockCrcLayoutChecksum
  长名称: ''
  描述: |
    CRC checksum over the NvBlock layout.
    
    CRC Calculation is influenced by:
    - CRYPTO_ALIGN_KEY_STORAGE
    - CRYPTO_NV_MANAGEMENT_DATA_PER_KEY
      - For each Block
        - CRYPTO_NV_BLOCK_REVISION
        - For each Key within the Block
          - CRYPTO_KEY_NV_ID
          - For each KeyElement within the Key
            - CRYPTO_KEY_ELEMENT_ID
            - CRYPTO_KEY_ELEMENT_SIZE
  默认值: 0
  最小值: 0
  最大值: 4294967294
```

