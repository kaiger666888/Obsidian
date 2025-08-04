# Crypto

## 模块描述

Crypto Driver for hardware specific functionalities

## 容器列表

### 1. CryptoDriverObjects

**描述**: Container for Crypto Driver Objects

该容器没有参数。

### 2. CryptoDriverObject

**描述**: Container for configuration of Crypto Driver Object. The container name
serves as a symbolic name for the identifier of a Crypto Driver Object.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoDriverObjectId
  长名称: ''
  描述: |
    Identifier of the Crypto Driver Object. The Crypto Driver Object offers
    different crypto primitives.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoDriverObjectQueueSize
  长名称: ''
  描述: |
    Size of the queue in the Crypto Driver. Defines the maximum number of
    jobs in the Crypto Driver Object queue. If it is set to 0, queueing is disabled
    in the Crypto Driver Object.
    This Crypto Driver does not support queuing but uses the buffer for asynchronous processing.
  默认值: 1
  最小值: 1
  最大值: 1
```

### 3. CryptoPrimitives

**描述**: Container for CRYPTO primitives

该容器没有参数。

### 4. CryptoPrimitive

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
  描述: Determines the algorithm secondary family used for the crypto service
  默认值: CRYPTO_ALGOFAM_NOT_SET
  最小值: ''
  最大值: ''
```

### 5. CryptoGeneral

**描述**: Container for common configuration options.

#### 参数列表

```yaml
- 
  序号: 1
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
  序号: 2
  名称: CryptoClearWorkspaceBuffers
  长名称: ''
  描述: For improved security workspace buffers can be cleared before and after usage. This has some
      influence on runtime performance.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CryptoTrngPrefetchCapacity
  长名称: ''
  描述: |
    Capacity of the Trng Prefetching buffer.
    A size greater zero will allocate a buffer which is constantly filled up with random data from
    the Trng.
    This will speed up job requests for random numbers since they have been already generated in the
    background.
    A capacity of 0 will disable Trng Prefetching.
  默认值: 32
  最小值: 0
  最大值: 128
- 
  序号: 4
  名称: CryptoTrngPrefetchWithInterrupt
  长名称: ''
  描述: Enables/Disables trng number pre-fetching with interrupt of TRNG module
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CryptoProvideISRs
  长名称: ''
  描述: |
    Provide two interrupt service routines.
    One is a default handler which does a software reset, the other can handle ECC errors and do a
    software reset.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CryptoRequestIsrCategory
  长名称: ''
  描述: |
    Select the category of the interrupt triggered by application to indicate a job request.
    Determines how the interrupt will be processed.
    
    NONE: No interrupt will be processed
    CATEGORY_1: Interrupt which is handled by vHsm
  默认值: CATEGORY_1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CryptoNonPreemptiveChunkSize
  长名称: ''
  描述: |
    Defines a threshold in bytes at which data processing of crypto jobs stop to allow asynchronous
    jobs to interact with the hardware.
    
    The exact amount of bytes to process also depends on the primitive itself.
    E.g. AES-128 can only stop every 16 bytes at minimum.
    
    A value of 0xFFFFFFFF disables asynchronous job processing on the hardware.
  默认值: 1024
  最小值: 1
  最大值: 4294967295
- 
  序号: 8
  名称: CryptoApplicationGenerateNoise
  长名称: ''
  描述: |
    Let application cores generate noise while HSM secure boot is running.
    
    On configurations where the application cores are released by the HSM, the HSM can instruct the
    application cores (via HSM2HTS register) to generate random noise while it is busy.
    This obfuscates what the HSM is processing (power profile) and can protect from side channel
    attacks.
    
    Only enable this if DMU_SP_PROCONHSMCFG.SSWWAIT is set.
  默认值: false
  最小值: ''
  最大值: ''
```

### 6. CryptoKeyDerive

**描述**: Container for Key Derivation options.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoMaxInputLength
  长名称: ''
  描述: |
    Defines the maximal total input Length for Key Derivation in Byte. This value defines the size
    of an internal buffer for the key derivation.
    The concatenated input string (counter | label | zero octet | context | target key length) has
    to fit into the buffer.
  默认值: 100
  最小值: 3
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoSizeOfTargetKeyLength
  长名称: ''
  描述: |
    The numeric length of the requested target key is concatenated to the input of the KeyDerive
    function. This parameter sets the length in byte which are concatenated (the length of the
    binary string).
    Additionally the parameter limits the max. length of the derived key.
  默认值: 2
  最小值: 1
  最大值: 4
- 
  序号: 3
  名称: CryptoSizeOfIterationCounter
  长名称: ''
  描述: |
    On each iteration of the KeyDerive function the iteration counter is concatenated to the input
    data. This parameter sets the length in byte which are concatenated to the input (length of
    binary representation of the counter).
    Additionally the parameter limits the max. length of the derived key.
  默认值: 1
  最小值: 1
  最大值: 4
- 
  序号: 4
  名称: CryptoMaxOutputKeyLength
  长名称: ''
  描述: Defines the maximal length of the output key. This parameter defines the size of an buffer for
      the key derivation. The output key length is defined as the size of the output key
      element on id 1.
  默认值: 32
  最小值: 1
  最大值: 4294967295
- 
  序号: 5
  名称: CryptoAddZeroOctet
  长名称: ''
  描述: If this switch is activated a zero octet (0x00) is added between the label and the context
      input.
  默认值: true
  最小值: ''
  最大值: ''
```

### 7. CryptoKeyElements

**描述**: Container for CRYPTO key elements.

该容器没有参数。

### 8. CryptoKeyElement

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
```

### 9. CryptoKeys

**描述**: Container for CRYPTO keys

该容器没有参数。

### 10. CryptoKey

**描述**: Configuration of a CryptoKey

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoKeyId
  长名称: ''
  描述: Identifier of the CRYPTO key
  默认值: 30000
  最小值: 30000
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoKeyDeriveIterations
  长名称: ''
  描述: |
    Not used.
    Holds the number of iterations to be performed by the key derivation primitive.
  默认值: 1
  最小值: 1
  最大值: 4294967295
```

### 11. CryptoKeyTypes

**描述**: Container for CRYPTO key types

该容器没有参数。

### 12. CryptoKeyType

**描述**: Configuration of a CryptoKeyType

该容器没有参数。

