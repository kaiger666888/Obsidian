# Crypto

## 模块描述

Configuration of the Crypto (CryptoDriver) module

## 容器列表

### 1. CryptoDriverObjects

**描述**: Container for CRYPTO Objects

该容器没有参数。

### 2. CryptoDriverObject

**描述**: Configuration of a CryptoDriverObject

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoDriverObjectId
  长名称: ''
  描述: Identifier of the Crypto Driver Object. The Crypto Driver Object offers different crypto
      primitives.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoQueueSize
  长名称: ''
  描述: Size of the queue in the Crypto Driver. Defines the maximum number of jobs in the Crypto
      Driver Object queue. If it is set to 0, queueing is disabled in the Crypto Driver
      Object.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 3. CryptoGeneral

**描述**: Container for common configuration options

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoDevErrorDetect
  长名称: ''
  描述: Switches the development error detection and notification on or off.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryptoMainFunctionPeriod
  长名称: ''
  描述: Specifies the period of main function Crypto_MainFunction in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: CryptoVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable and disable availability of the API Crypto_GetVersionInfo().
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. CryptoKeyElements

**描述**: Container for Crypto key elements

该容器没有参数。

### 5. CryptoKeyElement

**描述**: Configuration of a CryptoKeyElement

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoKeyElementAllowPartialAccess
  长名称: ''
  描述: Enable or disable writing and reading the key element with data smaller than the size of the
      element.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryptoKeyElementId
  长名称: ''
  描述: Identifier of the CRYPTO key element
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: CryptoKeyElementInitValue
  长名称: ''
  描述: Value which will be used to fill the element during initialisation, when the element is not
      already initialized.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CryptoKeyElementPersist
  长名称: ''
  描述: Enable or disable persisting of the key element in non-volatile storage.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CryptoKeyElementReadAccess
  长名称: ''
  描述: Define the reading access rights of the key element.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CryptoKeyElementSize
  长名称: ''
  描述: Maximum Size size of a CRYPTO key element in bytes
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 7
  名称: CryptoKeyElementWriteAccess
  长名称: ''
  描述: Define the writing access rights of the key element
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. CryptoKeyTypes

**描述**: Container for CRYPTO key types

该容器没有参数。

### 7. CryptoKeyType

**描述**: Configuration of a CryptoKeyType

该容器没有参数。

### 8. CryptoKeys

**描述**: Container for CRYPTO keys

该容器没有参数。

### 9. CryptoKey

**描述**: Configuration of a CryptoKey

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoKeyDeriveIterations
  长名称: ''
  描述: Holds the number of iterations to be performed by the key derivation primitive
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoKeyId
  长名称: ''
  描述: Identifier of the CRYPTO Key
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 10. CryptoPrimitives

**描述**: Container for CRYPTO primitives

该容器没有参数。

### 11. CryptoPrimitive

**描述**: Configuration of a CryptoPrimitive

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoPrimitiveAlgorithmFamily
  长名称: ''
  描述: Determines the algorithm family used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryptoPrimitiveAlgorithmMode
  长名称: ''
  描述: Determines the algorithm mode used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CryptoPrimitiveAlgorithmSecondaryFamily
  长名称: ''
  描述: Determines the algorithm secondary family used for the crypto service
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CryptoPrimitiveService
  长名称: ''
  描述: Determines the crypto service used for defining the capabilities
  默认值: ''
  最小值: ''
  最大值: ''
```

