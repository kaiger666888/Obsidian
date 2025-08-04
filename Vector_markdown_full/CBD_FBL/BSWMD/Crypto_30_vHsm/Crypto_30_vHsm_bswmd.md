# Crypto - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:01

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Crypto](#crypto)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Crypto

#### 基本信息

- **UUID**: `cc13fd78-eae2-46e6-9953-10ab262fc418`
- **模块名称**: `Crypto`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Hardware Crypto Driver for the vHsm Firmware

#### 版本历史

共有 **17** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: beta
- **发布日期**: 2017-06-23T02:45:06+02:00
- **发布者**: vistof

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: beta
- **发布日期**: 2018-01-09T15:56:29+02:00
- **发布者**: vistof

**变更内容**:

##### 3. 版本 1.02.00

- **状态**: released
- **发布日期**: 2018-05-08T15:56:30+02:00
- **发布者**: vistof

**变更内容**:

##### 4. 版本 1.03.00

- **状态**: beta
- **发布日期**: 2018-06-20T19:38:49+02:00
- **发布者**: visjhi

**变更内容**:

##### 5. 版本 2.00.00

- **状态**: released
- **发布日期**: 2018-09-24T16:22:39+02:00
- **发布者**: visrpp

**变更内容**:

##### 6. 版本 2.01.00

- **状态**: released
- **发布日期**: 2019-01-11T20:28:24+01:00
- **发布者**: vistof

**变更内容**:

##### 7. 版本 2.01.01

- **状态**: released
- **发布日期**: 2019-05-13T11:11:27+02:00
- **发布者**: visjhi

**变更内容**:

##### 8. 版本 2.01.02

- **状态**: released
- **发布日期**: 2019-08-06T15:02:24+02:00
- **发布者**: vistof

**变更内容**:

##### 9. 版本 2.02.00

- **状态**: released
- **发布日期**: 2019-08-06T15:02:56+02:00
- **发布者**: vistof

**变更内容**:

##### 10. 版本 2.02.01

- **状态**: released
- **发布日期**: 2020-01-28T10:58:30+01:00
- **发布者**: vistof

**变更内容**:

##### 11. 版本 2.03.00

- **状态**: released
- **发布日期**: 2020-01-30T12:01:33+01:00
- **发布者**: vistof

**变更内容**:

##### 12. 版本 2.03.01

- **状态**: released
- **发布日期**: 2020-07-14T13:15:32+02:00
- **发布者**: vistof

**变更内容**:

##### 13. 版本 2.04.00

- **状态**: released
- **发布日期**: 2020-08-07T13:48:41+02:00
- **发布者**: vistof

**变更内容**:

##### 14. 版本 2.05.00

- **状态**: released
- **发布日期**: 2020-10-02T17:49:02+02:00
- **发布者**: vistof

**变更内容**:

##### 15. 版本 2.05.01

- **状态**: released
- **发布日期**: 2020-10-27T16:33:17+01:00
- **发布者**: vistof

**变更内容**:

##### 16. 版本 2.06.00

- **状态**: released
- **发布日期**: 2021-01-05T15:45:59+01:00
- **发布者**: vistof

**变更内容**:

##### 17. 版本 2.06.01

- **状态**: released
- **发布日期**: 2021-02-15T15:29:57+01:00
- **发布者**: vistof

**变更内容**:

#### 配置容器

本模块包含 **16** 个配置容器：

##### 1. CryptoDriverObjects

**容器属性**:

- **UUID**: `2afe0d42-e52c-4710-aac6-5a235560aaa6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoDriverObjects`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for Crypto Driver Objects

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. CryptoDriverObject

**容器属性**:

- **UUID**: `36e1af48-f681-4fde-b53b-1d6adf9636f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoDriverObject`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of Crypto Driver Object. The container name 
serves as a symbolic name for the identifier of a Crypto Driver Object.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. CryptoDriverObjectId

- **UUID**: `946cd5fc-473b-4957-a542-042ca3fd9171`
- **参数名**: `CryptoDriverObjectId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Crypto Driver Object. The Crypto Driver Object offers 
different crypto primitives.

########## 2. CryptoDriverObjectQueueSize

- **UUID**: `167b3a49-50a6-41a0-b110-77d036dee05c`
- **参数名**: `CryptoDriverObjectQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the queue in the Crypto Driver. Defines the maximum number of 
jobs in the Crypto Driver Object queue. If it is set to 0, queueing is disabled 
in the Crypto Driver Object.
This Crypto Driver does not support queuing but uses the buffer for asynchronous processing.

########## 3. CryptoBufferSize

- **UUID**: `98f617bd-43be-4317-8349-70e96dc415d2`
- **参数名**: `CryptoBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the buffer allocated in the global RAM for this driver object.
This buffer stores all the input and output data, which is not directly accessible by the vHsm,  of the to be processed job. If Memory is accessible or not is defined by the CryptoMemoryArea configuration, e.g. RAM accessible by local CPU only or protected by MPU.

Attention: The buffer may contain the data of up to 5 pointers. For better performance, the driver inserts padding bytes between the different data to ensure aligned access for vHsm. Therefore, the needed buffer size could be greater than the total size of the buffered data.

To avoid unnecessary big buffers and the time to copy the data, consider providing the data directly from code flash or global RAM.

The buffer can also be configured to 0 to avoid unecessary pointer checks against the whitelist of the driver (the vHsm firmware will still check the pointers). Pay attention that all input and output needs to be mapped correctly in this case as the driver will not take care about copying the data to and from memory which can be accessed by the vHsm firmware. For SafeBsw it is also no possible to use a buffersize of 0.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CryptoPrimitiveRef

- **UUID**: `bf3b888f-9dfb-492a-8529-e20199c5b85c`
- **引用名**: `CryptoPrimitiveRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoPrimitive`
- **完整路径**: `/MICROSAR/Crypto_30_vHsm/Crypto/CryptoPrimitives/CryptoPrimitive`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to primitive in the CRYPTO. 
The CryptoPrimitive is a pre-configured container of the crypto service that shall be used.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CryptovHsmBuffer

**容器属性**:

- **UUID**: `5ac8d059-dfd7-44de-9a7f-d7c54a7b2146`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptovHsmBuffer`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead. This parameter summarizes all buffers included in this container.

Container to specify the size of the buffers for each parameter which will be used when the pointer points to invalid memory e.g. local RAM.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. CryptoInputBufferSize

- **UUID**: `34c9323a-f58d-42dc-9092-008b236df6ec`
- **参数名**: `CryptoInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the input data which is provided from the local RAM.

############ 2. CryptoSecondaryInputBufferSize

- **UUID**: `1ca89522-797f-435f-90c2-246faffb8f11`
- **参数名**: `CryptoSecondaryInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the secondary input data which is provided from the local RAM.

############ 3. CryptoTertiaryInputBufferSize

- **UUID**: `e81f402c-d61c-46ee-ba70-08a17721a74c`
- **参数名**: `CryptoTertiaryInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the tertiary input data which is provided from the local RAM.

############ 4. CryptoOutputBufferSize

- **UUID**: `a4e8712f-8d48-4cc4-ad68-e2d43f72c2d4`
- **参数名**: `CryptoOutputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the output data which will be written to the local RAM.

############ 5. CryptoSecondaryOutputBufferSize

- **UUID**: `a8264d7a-b4f9-4fdb-8fa1-af8541fe7e66`
- **参数名**: `CryptoSecondaryOutputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the secondary output data which will be written to the local RAM.

####### 2. CryptovHsmBuffer

**容器属性**:

- **UUID**: `5ac8d059-dfd7-44de-9a7f-d7c54a7b2146`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptovHsmBuffer`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead. This parameter summarizes all buffers included in this container.

Container to specify the size of the buffers for each parameter which will be used when the pointer points to invalid memory e.g. local RAM.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. CryptoInputBufferSize

- **UUID**: `34c9323a-f58d-42dc-9092-008b236df6ec`
- **参数名**: `CryptoInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the input data which is provided from the local RAM.

########## 2. CryptoSecondaryInputBufferSize

- **UUID**: `1ca89522-797f-435f-90c2-246faffb8f11`
- **参数名**: `CryptoSecondaryInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the secondary input data which is provided from the local RAM.

########## 3. CryptoTertiaryInputBufferSize

- **UUID**: `e81f402c-d61c-46ee-ba70-08a17721a74c`
- **参数名**: `CryptoTertiaryInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the tertiary input data which is provided from the local RAM.

########## 4. CryptoOutputBufferSize

- **UUID**: `a4e8712f-8d48-4cc4-ad68-e2d43f72c2d4`
- **参数名**: `CryptoOutputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the output data which will be written to the local RAM.

########## 5. CryptoSecondaryOutputBufferSize

- **UUID**: `a8264d7a-b4f9-4fdb-8fa1-af8541fe7e66`
- **参数名**: `CryptoSecondaryOutputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the secondary output data which will be written to the local RAM.

##### 2. CryptoDriverObject

**容器属性**:

- **UUID**: `36e1af48-f681-4fde-b53b-1d6adf9636f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoDriverObject`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of Crypto Driver Object. The container name 
serves as a symbolic name for the identifier of a Crypto Driver Object.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. CryptoDriverObjectId

- **UUID**: `946cd5fc-473b-4957-a542-042ca3fd9171`
- **参数名**: `CryptoDriverObjectId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Crypto Driver Object. The Crypto Driver Object offers 
different crypto primitives.

######## 2. CryptoDriverObjectQueueSize

- **UUID**: `167b3a49-50a6-41a0-b110-77d036dee05c`
- **参数名**: `CryptoDriverObjectQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the queue in the Crypto Driver. Defines the maximum number of 
jobs in the Crypto Driver Object queue. If it is set to 0, queueing is disabled 
in the Crypto Driver Object.
This Crypto Driver does not support queuing but uses the buffer for asynchronous processing.

######## 3. CryptoBufferSize

- **UUID**: `98f617bd-43be-4317-8349-70e96dc415d2`
- **参数名**: `CryptoBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the buffer allocated in the global RAM for this driver object.
This buffer stores all the input and output data, which is not directly accessible by the vHsm,  of the to be processed job. If Memory is accessible or not is defined by the CryptoMemoryArea configuration, e.g. RAM accessible by local CPU only or protected by MPU.

Attention: The buffer may contain the data of up to 5 pointers. For better performance, the driver inserts padding bytes between the different data to ensure aligned access for vHsm. Therefore, the needed buffer size could be greater than the total size of the buffered data.

To avoid unnecessary big buffers and the time to copy the data, consider providing the data directly from code flash or global RAM.

The buffer can also be configured to 0 to avoid unecessary pointer checks against the whitelist of the driver (the vHsm firmware will still check the pointers). Pay attention that all input and output needs to be mapped correctly in this case as the driver will not take care about copying the data to and from memory which can be accessed by the vHsm firmware. For SafeBsw it is also no possible to use a buffersize of 0.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CryptoPrimitiveRef

- **UUID**: `bf3b888f-9dfb-492a-8529-e20199c5b85c`
- **引用名**: `CryptoPrimitiveRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoPrimitive`
- **完整路径**: `/MICROSAR/Crypto_30_vHsm/Crypto/CryptoPrimitives/CryptoPrimitive`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to primitive in the CRYPTO. 
The CryptoPrimitive is a pre-configured container of the crypto service that shall be used.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptovHsmBuffer

**容器属性**:

- **UUID**: `5ac8d059-dfd7-44de-9a7f-d7c54a7b2146`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptovHsmBuffer`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead. This parameter summarizes all buffers included in this container.

Container to specify the size of the buffers for each parameter which will be used when the pointer points to invalid memory e.g. local RAM.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. CryptoInputBufferSize

- **UUID**: `34c9323a-f58d-42dc-9092-008b236df6ec`
- **参数名**: `CryptoInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the input data which is provided from the local RAM.

########## 2. CryptoSecondaryInputBufferSize

- **UUID**: `1ca89522-797f-435f-90c2-246faffb8f11`
- **参数名**: `CryptoSecondaryInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the secondary input data which is provided from the local RAM.

########## 3. CryptoTertiaryInputBufferSize

- **UUID**: `e81f402c-d61c-46ee-ba70-08a17721a74c`
- **参数名**: `CryptoTertiaryInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the tertiary input data which is provided from the local RAM.

########## 4. CryptoOutputBufferSize

- **UUID**: `a4e8712f-8d48-4cc4-ad68-e2d43f72c2d4`
- **参数名**: `CryptoOutputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the output data which will be written to the local RAM.

########## 5. CryptoSecondaryOutputBufferSize

- **UUID**: `a8264d7a-b4f9-4fdb-8fa1-af8541fe7e66`
- **参数名**: `CryptoSecondaryOutputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the secondary output data which will be written to the local RAM.

##### 3. CryptovHsmBuffer

**容器属性**:

- **UUID**: `5ac8d059-dfd7-44de-9a7f-d7c54a7b2146`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptovHsmBuffer`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead. This parameter summarizes all buffers included in this container.

Container to specify the size of the buffers for each parameter which will be used when the pointer points to invalid memory e.g. local RAM.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. CryptoInputBufferSize

- **UUID**: `34c9323a-f58d-42dc-9092-008b236df6ec`
- **参数名**: `CryptoInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the input data which is provided from the local RAM.

######## 2. CryptoSecondaryInputBufferSize

- **UUID**: `1ca89522-797f-435f-90c2-246faffb8f11`
- **参数名**: `CryptoSecondaryInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the secondary input data which is provided from the local RAM.

######## 3. CryptoTertiaryInputBufferSize

- **UUID**: `e81f402c-d61c-46ee-ba70-08a17721a74c`
- **参数名**: `CryptoTertiaryInputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the tertiary input data which is provided from the local RAM.

######## 4. CryptoOutputBufferSize

- **UUID**: `a4e8712f-8d48-4cc4-ad68-e2d43f72c2d4`
- **参数名**: `CryptoOutputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the output data which will be written to the local RAM.

######## 5. CryptoSecondaryOutputBufferSize

- **UUID**: `a8264d7a-b4f9-4fdb-8fa1-af8541fe7e66`
- **参数名**: `CryptoSecondaryOutputBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967294]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter is deprecated and not used anymore. Only available for backward compatibility.
Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.

Size of the buffer on the global RAM to store the secondary output data which will be written to the local RAM.

##### 4. CryptoGeneral

**容器属性**:

- **UUID**: `9d7a263c-f3f9-4622-8d35-774922e676ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for common configuration options.

###### 参数配置

此容器包含 **5** 个参数：

####### BOOLEAN 类型参数

######## 1. CryptoDevErrorDetect

- **UUID**: `1520b4d1-7517-461f-b929-3f585a8444c2`
- **参数名**: `CryptoDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the development error detection and notification on or off. 
- True: detection and notification is enabled. 
- False: detection and notification is disabled.

######## 2. CryptoVersionInfoApi

- **UUID**: `e5dfd150-de23-42b2-af0e-0b5b9216d0d7`
- **参数名**: `CryptoVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable availability of the API Crypto_GetVersionInfo().  
- True: API Crypto_GetVersionInfo() is available 
- False: API Crypto_GetVersionInfo() is not available.

######## 3. CryptoSafeBswChecks

- **UUID**: `e60153cc-fdbb-4dbc-ac65-60a9b18a2047`
- **参数名**: `CryptoSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

####### FLOAT 类型参数

######## 1. CryptoMainFunctionPeriod

- **UUID**: `b4db62ae-2736-4a01-bd4a-7df64a309db0`
- **参数名**: `CryptoMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the period of main function Crypto_MainFunction in seconds.

####### STRING 类型参数

######## 1. CryptoUserConfigFile

- **UUID**: `814cfa35-b241-471c-9194-4981edba5cd6`
- **参数名**: `CryptoUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.

##### 5. CryptoKeyElements

**容器属性**:

- **UUID**: `a1c74b54-a95e-4dd7-a21d-a17097ae732d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyElements`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container  for CRYPTO  key elements

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoKeyElement

**容器属性**:

- **UUID**: `5651e7e5-1973-4837-b89a-81f1800729a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKeyElement

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. CryptoKeyElementId

- **UUID**: `e32bf300-e4c9-4e91-a217-63a33db70ec0`
- **参数名**: `CryptoKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO key element

########## 2. CryptoKeyElementSize

- **UUID**: `23426719-5b9d-4f8c-927c-b5969fc13cf1`
- **参数名**: `CryptoKeyElementSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum size of a CRYPTO key element in bytes

######### BOOLEAN 类型参数

########## 1. CryptoKeyElementAllowPartialAccess

- **UUID**: `828bf5c0-b857-4a8d-bf0f-2b18766633a9`
- **参数名**: `CryptoKeyElementAllowPartialAccess`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable writing and reading the key element with data smaller 
than the size of the element. 
- True: enable partial access of the key element 
- False: disable partial access of the key element

########## 2. CryptoKeyElementPersist

- **UUID**: `efaa990d-2bb0-4cfc-adde-25eb2703fa51`
- **参数名**: `CryptoKeyElementPersist`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable persisting of the key element in non-volatile storage. 
- True: enable persisting of the key element. 
- False: disable persisting of the key element.

######### STRING 类型参数

########## 1. CryptoKeyElementInitValue

- **UUID**: `a604d634-83d4-44fe-bda1-2d934d5b164f`
- **参数名**: `CryptoKeyElementInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which will be used to fill the element during initialization, when the element is not already initialized.

######### ENUMERATION 类型参数

########## 1. CryptoKeyElementReadAccess

- **UUID**: `06c3a235-d4c3-4b76-85cc-568f87ceedf4`
- **参数名**: `CryptoKeyElementReadAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `RA_ALLOWED`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RA_ALLOWED`
  - `RA_DENIED`
  - `RA_ENCRYPTED`
  - `RA_INTERNAL_COPY`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the reading access rights of the key element. 
CRYPTO_RA_DENIED = key element cannot be read from outside the Crypto 
Driver 
CRYPTO_RA INTERNAL_COPY = key element can be copied to another key 
element in the same crypto driver. 
CRYPTO_RA_ALLOWED = key element can be read as plaintext 
CRYPTO_RA_ENCRYPTED = key element can be read encrypted. E.g. SHE Ram-
Key export.

########## 2. CryptoKeyElementWriteAccess

- **UUID**: `e854aa62-3cd9-4b92-b5fb-e7108ac025dc`
- **参数名**: `CryptoKeyElementWriteAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WA_ALLOWED`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WA_ALLOWED`
  - `WA_DENIED`
  - `WA_ENCRYPTED`
  - `WA_INTERNAL_COPY`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the writing access rights of the key element 
CRYPTO_WA_DENIED = key element cannot be written from outside the Crypto Driver 
CRYPTO_WA INTERNAL_COPY = key element can be filled with another key element in the same crypto driver. 
CRYPTO_WA_ALLOWED = key element can be rewritten as plaintext 
CRYPTO_WA_ENCRYPTED = key element can be written encrypted. E.g. SHE load key.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CryptoKeyElementVirtualTargetRef

- **UUID**: `0ce7166a-8adc-4e94-b09d-0efbcf84375b`
- **引用名**: `CryptoKeyElementVirtualTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/Crypto_30_vHsm/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a key element which will contain the actual data. If the Reference 
is configured, the key element will be a virtual key element.

##### 6. CryptoKeyElement

**容器属性**:

- **UUID**: `5651e7e5-1973-4837-b89a-81f1800729a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKeyElement

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. CryptoKeyElementId

- **UUID**: `e32bf300-e4c9-4e91-a217-63a33db70ec0`
- **参数名**: `CryptoKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO key element

######## 2. CryptoKeyElementSize

- **UUID**: `23426719-5b9d-4f8c-927c-b5969fc13cf1`
- **参数名**: `CryptoKeyElementSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum size of a CRYPTO key element in bytes

####### BOOLEAN 类型参数

######## 1. CryptoKeyElementAllowPartialAccess

- **UUID**: `828bf5c0-b857-4a8d-bf0f-2b18766633a9`
- **参数名**: `CryptoKeyElementAllowPartialAccess`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable writing and reading the key element with data smaller 
than the size of the element. 
- True: enable partial access of the key element 
- False: disable partial access of the key element

######## 2. CryptoKeyElementPersist

- **UUID**: `efaa990d-2bb0-4cfc-adde-25eb2703fa51`
- **参数名**: `CryptoKeyElementPersist`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable persisting of the key element in non-volatile storage. 
- True: enable persisting of the key element. 
- False: disable persisting of the key element.

####### STRING 类型参数

######## 1. CryptoKeyElementInitValue

- **UUID**: `a604d634-83d4-44fe-bda1-2d934d5b164f`
- **参数名**: `CryptoKeyElementInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which will be used to fill the element during initialization, when the element is not already initialized.

####### ENUMERATION 类型参数

######## 1. CryptoKeyElementReadAccess

- **UUID**: `06c3a235-d4c3-4b76-85cc-568f87ceedf4`
- **参数名**: `CryptoKeyElementReadAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `RA_ALLOWED`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RA_ALLOWED`
  - `RA_DENIED`
  - `RA_ENCRYPTED`
  - `RA_INTERNAL_COPY`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the reading access rights of the key element. 
CRYPTO_RA_DENIED = key element cannot be read from outside the Crypto 
Driver 
CRYPTO_RA INTERNAL_COPY = key element can be copied to another key 
element in the same crypto driver. 
CRYPTO_RA_ALLOWED = key element can be read as plaintext 
CRYPTO_RA_ENCRYPTED = key element can be read encrypted. E.g. SHE Ram-
Key export.

######## 2. CryptoKeyElementWriteAccess

- **UUID**: `e854aa62-3cd9-4b92-b5fb-e7108ac025dc`
- **参数名**: `CryptoKeyElementWriteAccess`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WA_ALLOWED`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WA_ALLOWED`
  - `WA_DENIED`
  - `WA_ENCRYPTED`
  - `WA_INTERNAL_COPY`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the writing access rights of the key element 
CRYPTO_WA_DENIED = key element cannot be written from outside the Crypto Driver 
CRYPTO_WA INTERNAL_COPY = key element can be filled with another key element in the same crypto driver. 
CRYPTO_WA_ALLOWED = key element can be rewritten as plaintext 
CRYPTO_WA_ENCRYPTED = key element can be written encrypted. E.g. SHE load key.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CryptoKeyElementVirtualTargetRef

- **UUID**: `0ce7166a-8adc-4e94-b09d-0efbcf84375b`
- **引用名**: `CryptoKeyElementVirtualTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/Crypto_30_vHsm/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a key element which will contain the actual data. If the Reference 
is configured, the key element will be a virtual key element.

##### 7. CryptoKeyTypes

**容器属性**:

- **UUID**: `d1b389d2-77bf-4b01-8d26-0aeddded8d73`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyTypes`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for CRYPTO key types

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoKeyType

**容器属性**:

- **UUID**: `27c09eae-3124-4d7a-8ed6-b51847d309b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyType`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKeyType

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CryptoKeyElementRef

- **UUID**: `44e69a1d-c76e-45fe-8e10-afdf7ac0203e`
- **引用名**: `CryptoKeyElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/Crypto_30_vHsm/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTOCrypto Key Element, which holds the 
data of the crypto key element.

##### 8. CryptoKeyType

**容器属性**:

- **UUID**: `27c09eae-3124-4d7a-8ed6-b51847d309b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeyType`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKeyType

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CryptoKeyElementRef

- **UUID**: `44e69a1d-c76e-45fe-8e10-afdf7ac0203e`
- **引用名**: `CryptoKeyElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoKeyElement`
- **完整路径**: `/MICROSAR/Crypto_30_vHsm/Crypto/CryptoKeyElements/CryptoKeyElement`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTOCrypto Key Element, which holds the 
data of the crypto key element.

##### 9. CryptoKeys

**容器属性**:

- **UUID**: `538dbfae-1285-4cb2-8875-6710af8a5bd2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKeys`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for CRYPTO keys

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoKey

**容器属性**:

- **UUID**: `95137452-25b6-41c2-8700-0835d7959f2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKey`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKey

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CryptoKeyId

- **UUID**: `454851ad-c6ab-41c3-a722-16512f7cab89`
- **参数名**: `CryptoKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO key

########## 2. CryptoKeyDeriveIterations

- **UUID**: `5fd0a743-1fa8-421b-94cc-6da74607c181`
- **参数名**: `CryptoKeyDeriveIterations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Holds the number of iterations to be performed by the key derivation primitive

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CryptoKeyTypeRef

- **UUID**: `bf72d470-98c4-405e-abad-c8f7625eed69`
- **引用名**: `CryptoKeyTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyType`
- **完整路径**: `/MICROSAR/Crypto_30_vHsm/Crypto/CryptoKeyTypes/CryptoKeyType`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTO to a CryptoKeyType. The CryptoKeyType provides the information which key elements are contained in a CryptoKey.

##### 10. CryptoKey

**容器属性**:

- **UUID**: `95137452-25b6-41c2-8700-0835d7959f2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoKey`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoKey

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CryptoKeyId

- **UUID**: `454851ad-c6ab-41c3-a722-16512f7cab89`
- **参数名**: `CryptoKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CRYPTO key

######## 2. CryptoKeyDeriveIterations

- **UUID**: `5fd0a743-1fa8-421b-94cc-6da74607c181`
- **参数名**: `CryptoKeyDeriveIterations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Holds the number of iterations to be performed by the key derivation primitive

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CryptoKeyTypeRef

- **UUID**: `bf72d470-98c4-405e-abad-c8f7625eed69`
- **引用名**: `CryptoKeyTypeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CryptoKeyType`
- **完整路径**: `/MICROSAR/Crypto_30_vHsm/Crypto/CryptoKeyTypes/CryptoKeyType`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to a pointer in the CRYPTO to a CryptoKeyType. The CryptoKeyType provides the information which key elements are contained in a CryptoKey.

##### 11. CryptoPrimitives

**容器属性**:

- **UUID**: `2a8ff4d1-8449-4cd5-823c-116aaf8119f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitives`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for CRYPTO primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryptoPrimitive

**容器属性**:

- **UUID**: `3ff0ebef-9318-4e09-8319-9fb65d24df78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitive`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoPrimitive

######## 参数配置

此容器包含 **4** 个参数：

######### ENUMERATION 类型参数

########## 1. CryptoPrimitiveAlgorithmFamily

- **UUID**: `08d1a99e-20c0-4cf3-8618-1cdc87e836a5`
- **参数名**: `CryptoPrimitiveAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_NOT_SET`
  - `CRYPTO_ALGOFAM_SHA1`
  - `CRYPTO_ALGOFAM_SHA2_224`
  - `CRYPTO_ALGOFAM_SHA2_256`
  - `CRYPTO_ALGOFAM_SHA2_384`
  - `CRYPTO_ALGOFAM_SHA2_512`
  - `CRYPTO_ALGOFAM_SHA2_512_224`
  - `CRYPTO_ALGOFAM_SHA2_512_256`
  - `CRYPTO_ALGOFAM_SHA3_224`
  - `CRYPTO_ALGOFAM_SHA3_256`
  - `CRYPTO_ALGOFAM_SHA3_384`
  - `CRYPTO_ALGOFAM_SHA3_512`
  - `CRYPTO_ALGOFAM_SHAKE128`
  - `CRYPTO_ALGOFAM_SHAKE256`
  - `CRYPTO_ALGOFAM_RIPEMD160`
  - `CRYPTO_ALGOFAM_BLAKE_1_256`
  - `CRYPTO_ALGOFAM_BLAKE_1_512`
  - `CRYPTO_ALGOFAM_BLAKE_2s_256`
  - `CRYPTO_ALGOFAM_BLAKE_2s_512`
  - `CRYPTO_ALGOFAM_3DES`
  - `CRYPTO_ALGOFAM_AES`
  - `CRYPTO_ALGOFAM_CHACHA`
  - `CRYPTO_ALGOFAM_RSA`
  - `CRYPTO_ALGOFAM_ED25519`
  - `CRYPTO_ALGOFAM_BRAINPOOL`
  - `CRYPTO_ALGOFAM_ECCNIST`
  - `CRYPTO_ALGOFAM_SECURECOUNTER`
  - `CRYPTO_ALGOFAM_RNG`
  - `CRYPTO_ALGOFAM_SIPHASH`
  - `CRYPTO_ALGOFAM_ECIES`
  - `CRYPTO_ALGOFAM_CUSTOM`
  - `CRYPTO_ALGOFAM_CUSTOM_ECCANSI`
  - `CRYPTO_ALGOFAM_CUSTOM_DRBG`
  - `CRYPTO_ALGOFAM_CUSTOM_FIPS186`
  - `CRYPTO_ALGOFAM_CUSTOM_ECCSEC`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_SECURE_BOOT`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_SOFTWARE_DOWNLOAD`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_FIRMWARE_UPDATE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service.

########## 2. CryptoPrimitiveAlgorithmMode

- **UUID**: `20915b3f-0ad3-44a4-83cd-9deec09b45fa`
- **参数名**: `CryptoPrimitiveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_NOT_SET`
  - `CRYPTO_ALGOMODE_ECB`
  - `CRYPTO_ALGOMODE_CBC`
  - `CRYPTO_ALGOMODE_CFB`
  - `CRYPTO_ALGOMODE_OFB`
  - `CRYPTO_ALGOMODE_CTR`
  - `CRYPTO_ALGOMODE_GCM`
  - `CRYPTO_ALGOMODE_XTS`
  - `CRYPTO_ALGOMODE_RSAES_OAEP`
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5`
  - `CRYPTO_ALGOMODE_RSASSA_PSS`
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5`
  - `CRYPTO_ALGOMODE_8ROUNDS`
  - `CRYPTO_ALGOMODE_12ROUNDS`
  - `CRYPTO_ALGOMODE_20ROUNDS`
  - `CRYPTO_ALGOMODE_HMAC`
  - `CRYPTO_ALGOMODE_CMAC`
  - `CRYPTO_ALGOMODE_GMAC`
  - `CRYPTO_ALGOMODE_CTRDRBG`
  - `CRYPTO_ALGOMODE_SIPHASH_2_4`
  - `CRYPTO_ALGOMODE_SIPHASH_4_8`
  - `CRYPTO_ALGOMODE_CUSTOM`
  - `CRYPTO_ALGOMODE_CUSTOM_P256R1`
  - `CRYPTO_ALGOMODE_CUSTOM_RSASSA_PKCS1_v1_5_CRT`
  - `CRYPTO_ALGOMODE_CUSTOM_USE_DF`
  - `CRYPTO_ALGOMODE_CUSTOM_P384R1`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CryptoPrimitiveService

- **UUID**: `f76bb9a0-ff72-4eae-bc95-97cb6cb7a95f`
- **参数名**: `CryptoPrimitiveService`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_MAC_VERIFY`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_MAC_VERIFY`
  - `CRYPTO_MAC_GENERATE`
  - `CRYPTO_SIGNATURE_VERIFY`
  - `CRYPTO_SIGNATURE_GENERATE`
  - `CRYPTO_ENCRYPT`
  - `CRYPTO_DECRYPT`
  - `CRYPTO_AEADENCRYPT`
  - `CRYPTO_AEADDECRYPT`
  - `CRYPTO_HASH`
  - `CRYPTO_RANDOM`
  - `CRYPTO_KEY_SET_VALID` (来源: Vector Informatik)
  - `CRYPTO_RANDOM_SEED` (来源: Vector Informatik)
  - `CRYPTO_KEY_GENERATE` (来源: Vector Informatik)
  - `CRYPTO_KEY_DERIVE` (来源: Vector Informatik)
  - `CRYPTO_KEY_EXCHANGE_CALC_PUBVAL` (来源: Vector Informatik)
  - `CRYPTO_KEY_EXCHANGE_CALC_SECRET` (来源: Vector Informatik)
  - `CRYPTO_CERIFICATE_PARSE` (来源: Vector Informatik)
  - `CRYPTO_CERTIFICATE_VERIFY` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the crypto service used for defining the capabilities

########## 4. CryptoPrimitiveAlgorithmSecondaryFamily

- **UUID**: `7cba5f3b-9065-45c7-b087-e4153c17137c`
- **参数名**: `CryptoPrimitiveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_NOT_SET`
  - `CRYPTO_ALGOFAM_SHA1`
  - `CRYPTO_ALGOFAM_SHA2_224`
  - `CRYPTO_ALGOFAM_SHA2_256`
  - `CRYPTO_ALGOFAM_SHA2_384`
  - `CRYPTO_ALGOFAM_SHA2_512`
  - `CRYPTO_ALGOFAM_SHA2_512_224`
  - `CRYPTO_ALGOFAM_SHA2_512_256`
  - `CRYPTO_ALGOFAM_SHA3_224`
  - `CRYPTO_ALGOFAM_SHA3_256`
  - `CRYPTO_ALGOFAM_SHA3_384`
  - `CRYPTO_ALGOFAM_SHA3_512`
  - `CRYPTO_ALGOFAM_SHAKE128`
  - `CRYPTO_ALGOFAM_SHAKE256`
  - `CRYPTO_ALGOFAM_RIPEMD160`
  - `CRYPTO_ALGOFAM_BLAKE_1_256`
  - `CRYPTO_ALGOFAM_BLAKE_1_512`
  - `CRYPTO_ALGOFAM_BLAKE_2s_256`
  - `CRYPTO_ALGOFAM_BLAKE_2s_512`
  - `CRYPTO_ALGOFAM_3DES`
  - `CRYPTO_ALGOFAM_AES`
  - `CRYPTO_ALGOFAM_CHACHA`
  - `CRYPTO_ALGOFAM_RSA`
  - `CRYPTO_ALGOFAM_ED25519`
  - `CRYPTO_ALGOFAM_BRAINPOOL`
  - `CRYPTO_ALGOFAM_ECCNIST`
  - `CRYPTO_ALGOFAM_SECURECOUNTER`
  - `CRYPTO_ALGOFAM_RNG`
  - `CRYPTO_ALGOFAM_SIPHASH`
  - `CRYPTO_ALGOFAM_ECIES`
  - `CRYPTO_ALGOFAM_CUSTOM`
  - `CRYPTO_ALGOFAM_CUSTOM_PADDING_PKCS7`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm secondary family used for the crypto service

##### 12. CryptoPrimitive

**容器属性**:

- **UUID**: `3ff0ebef-9318-4e09-8319-9fb65d24df78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoPrimitive`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of a CryptoPrimitive

###### 参数配置

此容器包含 **4** 个参数：

####### ENUMERATION 类型参数

######## 1. CryptoPrimitiveAlgorithmFamily

- **UUID**: `08d1a99e-20c0-4cf3-8618-1cdc87e836a5`
- **参数名**: `CryptoPrimitiveAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_NOT_SET`
  - `CRYPTO_ALGOFAM_SHA1`
  - `CRYPTO_ALGOFAM_SHA2_224`
  - `CRYPTO_ALGOFAM_SHA2_256`
  - `CRYPTO_ALGOFAM_SHA2_384`
  - `CRYPTO_ALGOFAM_SHA2_512`
  - `CRYPTO_ALGOFAM_SHA2_512_224`
  - `CRYPTO_ALGOFAM_SHA2_512_256`
  - `CRYPTO_ALGOFAM_SHA3_224`
  - `CRYPTO_ALGOFAM_SHA3_256`
  - `CRYPTO_ALGOFAM_SHA3_384`
  - `CRYPTO_ALGOFAM_SHA3_512`
  - `CRYPTO_ALGOFAM_SHAKE128`
  - `CRYPTO_ALGOFAM_SHAKE256`
  - `CRYPTO_ALGOFAM_RIPEMD160`
  - `CRYPTO_ALGOFAM_BLAKE_1_256`
  - `CRYPTO_ALGOFAM_BLAKE_1_512`
  - `CRYPTO_ALGOFAM_BLAKE_2s_256`
  - `CRYPTO_ALGOFAM_BLAKE_2s_512`
  - `CRYPTO_ALGOFAM_3DES`
  - `CRYPTO_ALGOFAM_AES`
  - `CRYPTO_ALGOFAM_CHACHA`
  - `CRYPTO_ALGOFAM_RSA`
  - `CRYPTO_ALGOFAM_ED25519`
  - `CRYPTO_ALGOFAM_BRAINPOOL`
  - `CRYPTO_ALGOFAM_ECCNIST`
  - `CRYPTO_ALGOFAM_SECURECOUNTER`
  - `CRYPTO_ALGOFAM_RNG`
  - `CRYPTO_ALGOFAM_SIPHASH`
  - `CRYPTO_ALGOFAM_ECIES`
  - `CRYPTO_ALGOFAM_CUSTOM`
  - `CRYPTO_ALGOFAM_CUSTOM_ECCANSI`
  - `CRYPTO_ALGOFAM_CUSTOM_DRBG`
  - `CRYPTO_ALGOFAM_CUSTOM_FIPS186`
  - `CRYPTO_ALGOFAM_CUSTOM_ECCSEC`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_SECURE_BOOT`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_SOFTWARE_DOWNLOAD`
  - `CRYPTO_ALGOFAM_CUSTOM_VHSM_FIRMWARE_UPDATE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service.

######## 2. CryptoPrimitiveAlgorithmMode

- **UUID**: `20915b3f-0ad3-44a4-83cd-9deec09b45fa`
- **参数名**: `CryptoPrimitiveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_NOT_SET`
  - `CRYPTO_ALGOMODE_ECB`
  - `CRYPTO_ALGOMODE_CBC`
  - `CRYPTO_ALGOMODE_CFB`
  - `CRYPTO_ALGOMODE_OFB`
  - `CRYPTO_ALGOMODE_CTR`
  - `CRYPTO_ALGOMODE_GCM`
  - `CRYPTO_ALGOMODE_XTS`
  - `CRYPTO_ALGOMODE_RSAES_OAEP`
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5`
  - `CRYPTO_ALGOMODE_RSASSA_PSS`
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5`
  - `CRYPTO_ALGOMODE_8ROUNDS`
  - `CRYPTO_ALGOMODE_12ROUNDS`
  - `CRYPTO_ALGOMODE_20ROUNDS`
  - `CRYPTO_ALGOMODE_HMAC`
  - `CRYPTO_ALGOMODE_CMAC`
  - `CRYPTO_ALGOMODE_GMAC`
  - `CRYPTO_ALGOMODE_CTRDRBG`
  - `CRYPTO_ALGOMODE_SIPHASH_2_4`
  - `CRYPTO_ALGOMODE_SIPHASH_4_8`
  - `CRYPTO_ALGOMODE_CUSTOM`
  - `CRYPTO_ALGOMODE_CUSTOM_P256R1`
  - `CRYPTO_ALGOMODE_CUSTOM_RSASSA_PKCS1_v1_5_CRT`
  - `CRYPTO_ALGOMODE_CUSTOM_USE_DF`
  - `CRYPTO_ALGOMODE_CUSTOM_P384R1`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CryptoPrimitiveService

- **UUID**: `f76bb9a0-ff72-4eae-bc95-97cb6cb7a95f`
- **参数名**: `CryptoPrimitiveService`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_MAC_VERIFY`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_MAC_VERIFY`
  - `CRYPTO_MAC_GENERATE`
  - `CRYPTO_SIGNATURE_VERIFY`
  - `CRYPTO_SIGNATURE_GENERATE`
  - `CRYPTO_ENCRYPT`
  - `CRYPTO_DECRYPT`
  - `CRYPTO_AEADENCRYPT`
  - `CRYPTO_AEADDECRYPT`
  - `CRYPTO_HASH`
  - `CRYPTO_RANDOM`
  - `CRYPTO_KEY_SET_VALID` (来源: Vector Informatik)
  - `CRYPTO_RANDOM_SEED` (来源: Vector Informatik)
  - `CRYPTO_KEY_GENERATE` (来源: Vector Informatik)
  - `CRYPTO_KEY_DERIVE` (来源: Vector Informatik)
  - `CRYPTO_KEY_EXCHANGE_CALC_PUBVAL` (来源: Vector Informatik)
  - `CRYPTO_KEY_EXCHANGE_CALC_SECRET` (来源: Vector Informatik)
  - `CRYPTO_CERIFICATE_PARSE` (来源: Vector Informatik)
  - `CRYPTO_CERTIFICATE_VERIFY` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the crypto service used for defining the capabilities

######## 4. CryptoPrimitiveAlgorithmSecondaryFamily

- **UUID**: `7cba5f3b-9065-45c7-b087-e4153c17137c`
- **参数名**: `CryptoPrimitiveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_NOT_SET`
  - `CRYPTO_ALGOFAM_SHA1`
  - `CRYPTO_ALGOFAM_SHA2_224`
  - `CRYPTO_ALGOFAM_SHA2_256`
  - `CRYPTO_ALGOFAM_SHA2_384`
  - `CRYPTO_ALGOFAM_SHA2_512`
  - `CRYPTO_ALGOFAM_SHA2_512_224`
  - `CRYPTO_ALGOFAM_SHA2_512_256`
  - `CRYPTO_ALGOFAM_SHA3_224`
  - `CRYPTO_ALGOFAM_SHA3_256`
  - `CRYPTO_ALGOFAM_SHA3_384`
  - `CRYPTO_ALGOFAM_SHA3_512`
  - `CRYPTO_ALGOFAM_SHAKE128`
  - `CRYPTO_ALGOFAM_SHAKE256`
  - `CRYPTO_ALGOFAM_RIPEMD160`
  - `CRYPTO_ALGOFAM_BLAKE_1_256`
  - `CRYPTO_ALGOFAM_BLAKE_1_512`
  - `CRYPTO_ALGOFAM_BLAKE_2s_256`
  - `CRYPTO_ALGOFAM_BLAKE_2s_512`
  - `CRYPTO_ALGOFAM_3DES`
  - `CRYPTO_ALGOFAM_AES`
  - `CRYPTO_ALGOFAM_CHACHA`
  - `CRYPTO_ALGOFAM_RSA`
  - `CRYPTO_ALGOFAM_ED25519`
  - `CRYPTO_ALGOFAM_BRAINPOOL`
  - `CRYPTO_ALGOFAM_ECCNIST`
  - `CRYPTO_ALGOFAM_SECURECOUNTER`
  - `CRYPTO_ALGOFAM_RNG`
  - `CRYPTO_ALGOFAM_SIPHASH`
  - `CRYPTO_ALGOFAM_ECIES`
  - `CRYPTO_ALGOFAM_CUSTOM`
  - `CRYPTO_ALGOFAM_CUSTOM_PADDING_PKCS7`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm secondary family used for the crypto service

##### 13. CryptovHsm

**容器属性**:

- **UUID**: `87f8507e-debb-46c6-aa50-4064fae6e12a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptovHsm`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Basic configuration of the vHsm Driver

###### 参数配置

此容器包含 **14** 个参数：

####### INTEGER 类型参数

######## 1. CryptoIpcChannels

- **UUID**: `8c9dec8b-ba24-49e9-ac6b-e5346c6e88f9`
- **参数名**: `CryptoIpcChannels`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of IPC channels used to communicate with the vHsm

######## 2. CryptoIpcProtocolVersion

- **UUID**: `7dfb9543-343b-4924-bac5-b54e48606f1e`
- **参数名**: `CryptoIpcProtocolVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..2]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Protocol version used to communicate with the vHsm Firmware over IPC.
The used protocol version must be the same on both the driver and vHsm Firmware.

Info: IPC Protocol Version 1 is deprecated and will be removed in future versions.

######## 3. CryptoDetInstanceMask

- **UUID**: `15b96481-fcb7-4c7e-a72d-8c62e28277a3`
- **参数名**: `CryptoDetInstanceMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Det errors originating from the vHsm can be distinguished from det errors of the application cores by OR-ing the mask with instanceId before passing the received Det to Det_ErrorReport() on the application core.

######## 4. CryptoHost2HsmAddress

- **UUID**: `d1849fe7-6a78-41e4-af35-9620bc344e40`
- **参数名**: `CryptoHost2HsmAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Host to the HSM core

######## 5. CryptoHsm2HostAddress

- **UUID**: `23f10b1e-0c74-4493-8f5f-93e658263dbe`
- **参数名**: `CryptoHsm2HostAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to communicate from Hsm to the Host core

######## 6. CryptoIpcInstanceId

- **UUID**: `d3d0d88a-4f72-480e-99d2-0a7fe1aea7da`
- **参数名**: `CryptoIpcInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id of the Ipc instance inside the Hsm

####### BOOLEAN 类型参数

######## 1. CryptoKeyElementDeleteSupport

- **UUID**: `14fe25f1-6171-414c-89b8-ff60bb9de4b3`
- **参数名**: `CryptoKeyElementDeleteSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this option is enabled, it disables a DET check which checks if the keyLength and keyPtr is not zero. (This check is part of the AUTOSAR Specification.)

######## 2. CryptoInterruptMode

- **UUID**: `6db4d4e1-377b-4e54-aa7b-763db8e513eb`
- **参数名**: `CryptoInterruptMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the interrupt mode is enabled, the vHsm will inform the application core about a finished job with the help of an interrupt.
The interrupt will then call the CryIf callback from the interrupt context in case of an async job.

If the interrupt mode is disabled, the driver will poll the IPC for finished jobs.
- For async jobs, this will be done in the main function. Also the callback will be called from the main function.
- For sync jobs, this will be done in the waiting loop during the job.

######## 3. CryptoRedirection

- **UUID**: `4f9ac6ff-56f1-48a1-bedc-bbf7327d5446`
- **参数名**: `CryptoRedirection`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable job input/output redirection to key elements. This is a Autosar 4.4 feature. Therefore a Csm and CryIf is required which also needs to support this feature

######## 4. CryptoIpcMacJobOptimization

- **UUID**: `3ea0a49d-cb7b-4f5e-8d4d-ad1619a65731`
- **参数名**: `CryptoIpcMacJobOptimization`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: During MAC Verification only inputPtr, secondaryInputPtr and verifyPtr are needed. During MAC Generation only inputPtr and outputPtr are needed.

This optimization reduces the transmission of mac jobs to this pointers. This will lead to a faster processing of the MAC because unnecessary checks for validity can be omitted.

This feature may only be enabled if vHsm support this feature as well. This is true for vHsm starting from version 02.01.00 (R22)

######## 5. CryptoKeyDeriveJobSupport

- **UUID**: `9c61b459-0664-4065-aefe-0289a95968ad`
- **参数名**: `CryptoKeyDeriveJobSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables support for KeyDerive operations processed as jobs. This needs to be supported by both the HSM and Csm.

######## 6. CryptoIpcInitialization

- **UUID**: `bfde2e0a-607f-4ad4-9f18-61928496e618`
- **参数名**: `CryptoIpcInitialization`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the driver will initialize the IPC memory and notify the vHsm firmware about the now usable IPC memory via the HOST2HSM interface

####### STRING 类型参数

######## 1. CryptoHsmUserRevision

- **UUID**: `e8b1a9bc-a773-4b7e-869b-6488ff78c879`
- **参数名**: `CryptoHsmUserRevision`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0`
  - 最大长度: 255
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is always updated with the one located in the generated vHSM pre configuration file.
Attention: This parameter is freely configurable in the vHSM (/MICROSAR/vHsm/vHsmGeneral/vHsmUserRevision) and changes only if was manually adapted in vHSM config. Use this to make sure that application and HSM on the same revision.

####### FUNCTION-NAME 类型参数

######## 1. CryptoWaitLoopCallout

- **UUID**: `9708a23a-16e9-4a96-8068-1d808a6bbb4f`
- **参数名**: `CryptoWaitLoopCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Appl_Crypto_30_vHsm_WaitLoopCallout`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callout which is called while waiting for responses from the vHsm during synchronous jobs.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CryptoManagementDriverObject

- **UUID**: `346b64d0-f44e-4d28-966c-7519970bf43a`
- **引用名**: `CryptoManagementDriverObject`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CryptoDriverObject`
- **完整路径**: `/MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This driver object will be used for the Key management Functions.
The buffers of the referenced driver objects must be set to values sufficient for proper operation.
The driver object is used as transport medium for the communication with the vHsm.

Input data of Key functions will be handled as InputPtr
Output data of Key functions will be handled as OutputPtr

When multiple Key API calls need to be performed at the same time, multiple driver objects need to be referenced here.
During runtime the first free driver object of the references will be used.
To enable Key APIs to be processed on all driver objects, all referenced driver objects need to have the same buffer size configured.

Hint:
HSM Configuration:
There is only one vHsm_KeyM driver object in the HSM for the key management API.
As this driver object can already process parallel key requests, there is no need to create a further driver object.
To provide multiple driver object to the driver on application side where key API calls can be transmitted, create an additional CryIfChannel inside the vHsm and reference the already existing vHsm_KeyM driver object.
So multiple CryIfChannels will reference the same driver object vHsm_KeyM.
Furthermore make the new CryIfChannel available in the IPC under /MICROSAR/vHsm/vHsmIpc/vHsmIpcInstance/vHsmDriverObjectMapping.
The sync mechanism will make the new CryIfChannel visible as driver object in the Driver after the vHsm has been generated.

Driver Configuration:
Reference the new available driver object as additional management driver object.
Now the number of referenced driver objects will be the number of possible parallel key management API calls.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. CryptoMemoryArea

**容器属性**:

- **UUID**: `523ba6d3-dc21-4cab-b7a8-d0d7e8f77ab5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoMemoryArea`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

White list of memory areas used as input and output for crypto jobs or key management operations.
The areas from the whitelist of the vHsm configuration can be used also in the driver.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. CryptoAreaStart

- **UUID**: `681d78a5-ab8b-4b1a-b8d1-5f0d424e1873`
- **参数名**: `CryptoAreaStart`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of the memory area

########## 2. CryptoAreaStop

- **UUID**: `ce60372c-1a2c-458b-98c4-5e086b20dcc2`
- **参数名**: `CryptoAreaStop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4294967295`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of the memory area

########## 3. CryptoAreaPriority

- **UUID**: `0ee3ea5a-9138-4a66-a2a4-4e66aaea7a03`
- **参数名**: `CryptoAreaPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The priority of the memory area.
The higher the value, the higher the areas priority.
The area with the highest priority will be checked first.
To get the best performance assign a high priority to areas which are used very often.

######### BOOLEAN 类型参数

########## 1. CryptoAreaEnabled

- **UUID**: `0eba9741-d6e9-479f-9e90-d42a3ee8adf8`
- **参数名**: `CryptoAreaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Memory areas can be disabled if needed.
This can be used in the Safe Use-Case, when it is not allowed to have an enabled READWRITE area.

######### ENUMERATION 类型参数

########## 1. CryptoAreaType

- **UUID**: `e3a9e41f-3762-4f82-8e6d-ba42c28201dd`
- **参数名**: `CryptoAreaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_AREA_HSM_READ_ACCESS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_AREA_HSM_READ_ACCESS`
  - `CRYPTO_AREA_HSM_READWRITE_ACCESS`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of the memory area as seen from the vHsm.

####### 2. CryptoJobResponseInterrupt

**容器属性**:

- **UUID**: `f91f5788-ac57-4d6f-919e-60ee7fe030c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoJobResponseInterrupt`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Configures settings for receiving an interrupt from the hsm

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. CryptoJobResponseInterruptFlagClearAddress

- **UUID**: `1551a27b-3c0c-48b3-b941-208174eecbe3`
- **参数名**: `CryptoJobResponseInterruptFlagClearAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to clear the interrupt request flag

########## 2. CryptoJobResponseInterruptFlagClearMask

- **UUID**: `874ae42d-f71e-4cae-a25e-87619e2d4c8b`
- **参数名**: `CryptoJobResponseInterruptFlagClearMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mask which is used to set the value

########## 3. CryptoJobResponseInterruptFlagClearValue

- **UUID**: `b9a7a198-47cf-4924-9a66-aa34e192a065`
- **参数名**: `CryptoJobResponseInterruptFlagClearValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which will be set to the masked register

######### BOOLEAN 类型参数

########## 1. CryptoJobResponseInterruptFlagClearing

- **UUID**: `151f847a-6951-4e29-972f-c947c1a73aff`
- **参数名**: `CryptoJobResponseInterruptFlagClearing`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Clearing the flag is only needed when the OS does not clear the interrupt flag automatically.

####### 3. CryptoJobRequestInterrupt

**容器属性**:

- **UUID**: `b58575e0-ca04-4f66-9ac9-1a39a0119f09`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoJobRequestInterrupt`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Configures settings for triggering an interrupt to the hsm

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. CryptoJobRequestInterruptFlagSetAddress

- **UUID**: `773898b9-5acc-4e2b-816d-4a8c50beeaab`
- **参数名**: `CryptoJobRequestInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to clear the interrupt request flag

########## 2. CryptoJobRequestInterruptFlagSetMask

- **UUID**: `c4524e3f-bf97-4d94-aa53-88b2c54173b0`
- **参数名**: `CryptoJobRequestInterruptFlagSetMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mask which is used to set the value

######### BOOLEAN 类型参数

########## 1. CryptoJobRequestInterruptFlagSetting

- **UUID**: `7424f658-8b75-42d3-ad9b-aeb92247b1e4`
- **参数名**: `CryptoJobRequestInterruptFlagSetting`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Setting the interrupt flag and thus triggering an interrupt to the vHsm is only needed when isr support in vHsm is enabled.

##### 14. CryptoMemoryArea

**容器属性**:

- **UUID**: `523ba6d3-dc21-4cab-b7a8-d0d7e8f77ab5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoMemoryArea`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

White list of memory areas used as input and output for crypto jobs or key management operations.
The areas from the whitelist of the vHsm configuration can be used also in the driver.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. CryptoAreaStart

- **UUID**: `681d78a5-ab8b-4b1a-b8d1-5f0d424e1873`
- **参数名**: `CryptoAreaStart`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of the memory area

######## 2. CryptoAreaStop

- **UUID**: `ce60372c-1a2c-458b-98c4-5e086b20dcc2`
- **参数名**: `CryptoAreaStop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4294967295`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: End address of the memory area

######## 3. CryptoAreaPriority

- **UUID**: `0ee3ea5a-9138-4a66-a2a4-4e66aaea7a03`
- **参数名**: `CryptoAreaPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The priority of the memory area.
The higher the value, the higher the areas priority.
The area with the highest priority will be checked first.
To get the best performance assign a high priority to areas which are used very often.

####### BOOLEAN 类型参数

######## 1. CryptoAreaEnabled

- **UUID**: `0eba9741-d6e9-479f-9e90-d42a3ee8adf8`
- **参数名**: `CryptoAreaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Memory areas can be disabled if needed.
This can be used in the Safe Use-Case, when it is not allowed to have an enabled READWRITE area.

####### ENUMERATION 类型参数

######## 1. CryptoAreaType

- **UUID**: `e3a9e41f-3762-4f82-8e6d-ba42c28201dd`
- **参数名**: `CryptoAreaType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_AREA_HSM_READ_ACCESS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_AREA_HSM_READ_ACCESS`
  - `CRYPTO_AREA_HSM_READWRITE_ACCESS`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of the memory area as seen from the vHsm.

##### 15. CryptoJobResponseInterrupt

**容器属性**:

- **UUID**: `f91f5788-ac57-4d6f-919e-60ee7fe030c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoJobResponseInterrupt`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Configures settings for receiving an interrupt from the hsm

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. CryptoJobResponseInterruptFlagClearAddress

- **UUID**: `1551a27b-3c0c-48b3-b941-208174eecbe3`
- **参数名**: `CryptoJobResponseInterruptFlagClearAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to clear the interrupt request flag

######## 2. CryptoJobResponseInterruptFlagClearMask

- **UUID**: `874ae42d-f71e-4cae-a25e-87619e2d4c8b`
- **参数名**: `CryptoJobResponseInterruptFlagClearMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mask which is used to set the value

######## 3. CryptoJobResponseInterruptFlagClearValue

- **UUID**: `b9a7a198-47cf-4924-9a66-aa34e192a065`
- **参数名**: `CryptoJobResponseInterruptFlagClearValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value which will be set to the masked register

####### BOOLEAN 类型参数

######## 1. CryptoJobResponseInterruptFlagClearing

- **UUID**: `151f847a-6951-4e29-972f-c947c1a73aff`
- **参数名**: `CryptoJobResponseInterruptFlagClearing`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Clearing the flag is only needed when the OS does not clear the interrupt flag automatically.

##### 16. CryptoJobRequestInterrupt

**容器属性**:

- **UUID**: `b58575e0-ca04-4f66-9ac9-1a39a0119f09`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryptoJobRequestInterrupt`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Configures settings for triggering an interrupt to the hsm

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. CryptoJobRequestInterruptFlagSetAddress

- **UUID**: `773898b9-5acc-4e2b-816d-4a8c50beeaab`
- **参数名**: `CryptoJobRequestInterruptFlagSetAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the register which is used to clear the interrupt request flag

######## 2. CryptoJobRequestInterruptFlagSetMask

- **UUID**: `c4524e3f-bf97-4d94-aa53-88b2c54173b0`
- **参数名**: `CryptoJobRequestInterruptFlagSetMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mask which is used to set the value

####### BOOLEAN 类型参数

######## 1. CryptoJobRequestInterruptFlagSetting

- **UUID**: `7424f658-8b75-42d3-ad9b-aeb92247b1e4`
- **参数名**: `CryptoJobRequestInterruptFlagSetting`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Setting the interrupt flag and thus triggering an interrupt to the vHsm is only needed when isr support in vHsm is enabled.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. Crypto_30_vHsm

- **UUID**: `0c4e5e56-b5a6-40b9-8562-1babe381bf69`
- **包名称**: `Crypto_30_vHsm`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Crypto_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **Crypto**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Crypto_Pre**
2. **Crypto_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Crypto_Impl

- **UUID**: `661e93af-9a72-489e-bf84-112e3696e3dd`
- **实现名称**: `Crypto_Impl`
- **编程语言**: C
- **软件版本**: 2.06.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.01
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Crypto_Pre

- **UUID**: `bd7508ab-cf3e-4b73-b326-57de0c581a51`
- **配置名称**: `Crypto_Pre`
- **定义引用**: `/MICROSAR/Crypto_30_vHsm/Crypto`

### 2. Crypto_Rec

- **UUID**: `b1820846-3feb-4ece-982d-dc4980cca7b1`
- **配置名称**: `Crypto_Rec`
- **定义引用**: `/MICROSAR/Crypto_30_vHsm/Crypto`
