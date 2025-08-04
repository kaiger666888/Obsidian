# KeyM

## 模块描述

Configuration of the Mcu (Microcontroller Unit) module.

## 容器列表

### 1. KeyMCertificate

**描述**: This container contains the certificate configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: KeyMCertAlgorithmType
  长名称: ''
  描述: Specify in which format the certificate will be provided.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: KeyMCertFormatType
  长名称: ''
  描述: Specify in which format the certificate will be provided.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: KeyMCertificateId
  长名称: ''
  描述: Identifier of the certificate. The set of configured identifiers shall be consecutive and
      gapless.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: KeyMCertificateMaxLength
  长名称: ''
  描述: Specify the maximum length in bytes of the certificate.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 5
  名称: KeyMCertificateName
  长名称: ''
  描述: Provides a unique name of the certificate for identification. The certificate provisional will
      reference certificates by this unique name.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: KeyMCertificateVerifyCallbackNotificationFunc
  长名称: ''
  描述: This parameter provides the function name for the callback
      <KeyM_CertificateVerifyCallbackNotification>. It indicates if a certificate verification
      operation was finished and provides its status. If this parameter is omitted, no
      callback will be provided.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: KeyMServiceCertificateCallbackNotificationFunc
  长名称: ''
  描述: This parameter provides the function name for the service certificate callback
      <KeyM_ServiceCertificateCallbackNotification>. It indicates if a certificate service
      operation was finished and provides its status. If this parameter is not set, no
      callback will be provided.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. KeyMCertificateElement

**描述**: This container contains the certificate element configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: KeyMCertificateElementHasIteration
  长名称: ''
  描述: Defines if the certificate element can occur more than one time. If so, the iterator can be
      used to retrieve the individual data values of this certificate element.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: KeyMCertificateElementId
  长名称: ''
  描述: Identifier of a certificate element.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: KeyMCertificateElementMaxLength
  长名称: ''
  描述: Maximum length in bytes
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: KeyMCertificateElementObjectId
  长名称: ''
  描述: This is the object identifier (OID) that is used to identify the certificate element within
      its element structure.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: KeyMCertificateElementObjectType
  长名称: ''
  描述: Certificate elements are stored in ASN.1 format. In this item the type of ASN.1 TLV can be
      specified (e.g. INTEGER has the value '2'). This can be used to identify only such
      certificate elements. If the type is different, the element is not included in the
      search.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: KeyMCertificateElementOfStructure
  长名称: ''
  描述: This defines in which structure the certificate element is located.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. KeyMCertificateElementVerification

**描述**: This container defines if and how certificate elements are to be verified.

该容器没有参数。

### 4. KeyMCertificateElementCondition

**描述**: This container contains the configuration of KeyElement compare conditions which can be used as
arguments for a KeyMCertificateElementRule.

#### 参数列表

```yaml
- 
  序号: 1
  名称: KeyMCertElementConditionType
  长名称: ''
  描述: This parameter specifies what kind of comparison that is made for the evaluation of the mode
      condition.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. KeyMCertificateElementConditionValue

**描述**: This container contains the configuration of a compare value.

该容器没有参数。

### 6. KeyMCertificateElementConditionArray

**描述**: This container contains the configuration of a array compare value.

该容器没有参数。

### 7. KeyMCertificateElementConditionArrayElement

**描述**: This container contains the configuration of a array compare value.

#### 参数列表

```yaml
- 
  序号: 1
  名称: KeyMCertificateElementConditionArrayElementIndex
  长名称: ''
  描述: Index to an element of the compare value array.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: KeyMCertificateElementConditionArrayElementValue
  长名称: ''
  描述: Value of an array element compare value.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 8. KeyMCertificateElementConditionCerificateElement

**描述**: This container contains the configuration of a certificate element as a compare value.

该容器没有参数。

### 9. KeyMCertificateElementConditionPrimitive

**描述**: This container contains the configuration of a primitive compare value.

#### 参数列表

```yaml
- 
  序号: 1
  名称: KeyMCertificateElementConditionPrimitiveValue
  长名称: ''
  描述: Primitive compare value
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 10. KeyMCertificateElementConditionSenderReceiver

**描述**: This container contains the configuration of a dynamic compare value in a sender-/receiver
interface.

该容器没有参数。

### 11. KeyMCertificateElementRule

**描述**: This container contains the configuration of a mode rule which represents a logical expression with
KeyMCertificateElementCondition or other KeyMCertificateElementRule as arguments.

#### 参数列表

```yaml
- 
  序号: 1
  名称: KeyMLogicalOperator
  长名称: ''
  描述: This parameter specifies the logical operator to be used in the logical expression. If the
      expression only consists of a single condition this parameter shall not be used.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 12. KeyMCryptoKey

**描述**: This container contains the crypto keys that can be updated.

#### 参数列表

```yaml
- 
  序号: 1
  名称: KeyMCryptoCsmVerifyJobType
  长名称: ''
  描述: Specifies what type of function for key verification operation is used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: KeyMCryptoKeyCryptoProps
  长名称: ''
  描述: If set, it will provide additional hints to the crypto key that is used by KeyM to identify
      the key.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: KeyMCryptoKeyGenerationInfo
  长名称: ''
  描述: This data may contain static data for key derivation. If a key is configured to be derived
      from another key and this configuration item is set, the data will be added as salt.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: KeyMCryptoKeyGenerationType
  长名称: ''
  描述: Specifies how the CryptoKey will be generated. If it is derived from another key or simply
      stored with KeyElementSet.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: KeyMCryptoKeyId
  长名称: ''
  描述: Identifier of the crypto key. The set of configured identifiers shall be consecutive and
      gapless.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: KeyMCryptoKeyMaxLength
  长名称: ''
  描述: The maximum size in bytes of a CryptoKey.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 7
  名称: KeyMCryptoKeyName
  长名称: ''
  描述: Provides a unique name of the key for identification. The key master will reference keys by
      this unique key name.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: KeyMCryptoKeyStorage
  长名称: ''
  描述: Specify the storage location of the certificate.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 13. KeyMNvmBlock

**描述**: Configuration of optional usage of Nvm in case the KeyM module requires non volatile memory in the
Ecu to store information (e.g. crypto keys or certificates).

该容器没有参数。

### 14. KeyMGeneral

**描述**: This container holds general configuration (parameters) for key manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: KeyMCertificateChainMaxDepth
  长名称: ''
  描述: Maximum number of certificates defined in a certificate chain.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: KeyMCertificateManagerEnabled
  长名称: ''
  描述: Enables (TRUE) or disables (FALSE) the part that manages certificates.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: KeyMCryptoKeyHandlerPrepareEnabled
  长名称: ''
  描述: Enables (TRUE) or disables (FALSE) the key handler prepare function call. If set to true, the
      corresponding key handler function shall be provided.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: KeyMCryptoKeyHandlerServiceCertificateEnabled
  长名称: ''
  描述: Enables (TRUE) or disables (FALSE) the key handler service function call. If set to true, the
      certificate submodule function KeyM_KH_ServiceCertificate() shall be provided.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: KeyMCryptoKeyHandlerStartFinalizeEnabled
  长名称: ''
  描述: Enables (TRUE) or disables (FALSE) the key handler start and finalize function call. If set to
      true, the key handler functions KeyM_KH_Start() and KeyM_KH_Finalize() shall be
      provided.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: KeyMCryptoKeyHandlerUpdateEnabled
  长名称: ''
  描述: Enables (TRUE) or disables (FALSE) the call to the key handler update function
      KeyM_KH_Update(). If set to true, the corresponding key handler function shall be
      provided.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: KeyMCryptoKeyHandlerVerifyEnabled
  长名称: ''
  描述: Enables (TRUE) or disables (FALSE) the call to the key handler verify function
      KeyM_KH_Verify(). If set to true, the corresponding key handler function shall be
      provided.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: KeyMCryptoKeyManagerEnabled
  长名称: ''
  描述: Enables (TRUE) or disables (FALSE) the part that manages crypto key operations.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: KeyMCryptoKeyPrepareFunctionEnabled
  长名称: ''
  描述: Enables (TRUE) or disables (FALSE) the prepare function of the key manager. If set to true,
      the KeyM_Prepare() function has to be called accordingly.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: KeyMCryptoKeyStartFinalizeFunctionEnabled
  长名称: ''
  描述: Enables (TRUE) or disables (FALSE) the start and Finish function of the key manager. If set to
      true, the KeyM_Start() and KeyM_Finalize() functions have to be called.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: KeyMCryptoKeyVerifyAsyncMode
  长名称: ''
  描述: This parameter defines if the function KeyM_Verify() runs in synchronous or asynchronous mode
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: KeyMCryptoKeyVerifyFunctionEnabled
  长名称: ''
  描述: Enables (TRUE) or disables (FALSE) the verify function of the key manager. If set to true, the
      KeyM_Verify() function can be called.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: KeyMDevErrorDetect
  长名称: ''
  描述: Switches the development error detection and notification on or off.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: KeyMKeyCertNameMaxLength
  长名称: ''
  描述: Maximum length in bytes of certificate or key names used for the service interface.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 15
  名称: KeyMMainFunctionPeriod
  长名称: ''
  描述: Specifies the period of main function KeyM_MainFunction in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 16
  名称: KeyMServiceCertificateFunctionEnabled
  长名称: ''
  描述: Enables (TRUE) or disables (FALSE) the certificate service function of the key manager. If set
      to true, the KeyM_ServiceCertificate() function has to be called accordingly.
  默认值: false
  最小值: ''
  最大值: ''
```

