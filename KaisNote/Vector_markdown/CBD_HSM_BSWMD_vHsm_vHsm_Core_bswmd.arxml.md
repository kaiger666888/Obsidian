# Crypto

## 模块描述

Crypto Driver for the core functionality of the vHsm

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

### 5. CryptoKeys

**描述**: Container for CRYPTO keys

该容器没有参数。

### 6. CryptoKey

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

### 9. CryptoKeyTypes

**描述**: Container for CRYPTO key types

该容器没有参数。

### 10. CryptoKeyType

**描述**: Configuration of a CryptoKeyType

该容器没有参数。

