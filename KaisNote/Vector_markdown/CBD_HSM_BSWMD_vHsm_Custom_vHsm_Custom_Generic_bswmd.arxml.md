# Crypto

## 模块描述

Software Crypto Driver

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

