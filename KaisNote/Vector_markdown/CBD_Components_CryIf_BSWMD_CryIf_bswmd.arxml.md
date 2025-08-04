# CryIf

## 模块描述

The Crypto Interface (CRYIF) is called by the Cryptographic Service Manager (CSM) to
forward its service requests to the underlying Crypto Drivers (CRYPTO).
#Crypto #Cryptographic #Cryptography #Security
#AUTOSAR
#ServiceComponent

## 容器列表

### 1. CryIfChannel

**描述**: Container for incorporation of CryIfChannel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryIfChannelId
  长名称: ''
  描述: Identifier of the crypto channel.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 2. CryIfGeneral

**描述**: Container for incorporation of CryIfGeneral.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryIfDevErrorDetect
  长名称: ''
  描述: Switches the development error detection and notification on or off.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryIfVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable and disable availability of the API CryIf_GetVersionInfo().
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CryIfMaxNumberOfKeyElements
  长名称: ''
  描述: Maximum number of key elements in one key which needs to be copied from one driver to another.
  默认值: 10
  最小值: 1
  最大值: 4294967295
- 
  序号: 4
  名称: CryIfMaxSizeOfKeyElement
  长名称: ''
  描述: Size of the largest key element which needs to be copied from one driver to another.
  默认值: 32
  最小值: 1
  最大值: 4294967295
- 
  序号: 5
  名称: CryIfRedirection
  长名称: ''
  描述: |
    If enabled, the CryIf supports the redirection feature of ASR 4.4. It is mandatory that the used
    Csm is also capable of this feature.
    If disabled, the CryIf ignores any kind of redirection.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CryIfSafeBswChecks
  长名称: ''
  描述: Enables safety checks. These checks improve robustness. E.g. invalid parameters are checked
      before function is executed. This attribute has to be enabled for safety projects where
      this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. CryIfKey

**描述**: Container for incorporation of CryIfKey.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryIfKeyId
  长名称: ''
  描述: Identifier of the CryIf key.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 4. CryIfCryptoModule

**描述**: Container for incorporation of Crypto Modules

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryIfSupportsKeyElementCopyPartial
  长名称: ''
  描述: |
    If enabled, the referenced driver provides the service Crypto_KeyElementCopyPartial. This
    service is available since ASR 4.4.x.
    
    If disabled, CryIf emulates the service by getting and setting the key. If driver prevents
    reading or writing one of the involved keys, the service fails with an error.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryIfCryptoIncludeFile
  长名称: ''
  描述: Include file of the Crypto module. If CryIfCryptoIncludeFile is not existent, the following
      pattern is applied for inclusion: Crypto_{Vendor Id}_{Vendor Api Infix}.h
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CryIfCryptoMip
  长名称: ''
  描述: Module implementation prefix for the referenced Crypto Module. If not set, then the Mip is
      determined from BSW-Configuration in the following way:  Crypto_{Vendor Id}_{Vendor Api
      Infix}
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CryIfCryptoKeySetValidAPI
  长名称: ''
  描述: |
    The Crypto Api Crypto_KeyValidSet was renamed in ASR 4.3.1 to Crypto_KeySetValid. In order to
    ensure compatibility, this parameter enables renaming the API call to the corresponding Crypto
    driver.
    
    If this parameter is not present, CryIf will default to KeyValidSet.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CryIfCancelJobApiUsesJobType
  长名称: ''
  描述: |
    Specifies whether the referenced driver's Job Cancellation interface uses the Crypto_JobType
    instead of the Crypto_JobInfoType data type.
    
    Set to TRUE for compatibility with ASR R19-11 and the MICROSAR crypto driver.
    Set to FALSE for compatibility with third-party crypto drivers implementing ASR 4.4 and older.
    
    Attention: There is an inconsistency in the ASR specs 4.4 and older which, by default, makes it
    impossible to implement this interface in standard-compliant way. If you set this switch to
    FALSE, you also need to set the parameter
    /MICROSAR/Csm/CsmGeneral/CsmJobTypeLayout/CsmJobTypeLayoutVarMembers to TRUE. This circumvents
    the limitations of the ASR spec and makes it possible to provide a compliant interface.
    Note that this Csm switch only exists in MICROSAR Csm 4.2.0 and above. In MICROSAR Csm versions
    earlier than 5.1.0, the switch resides directly under Csm/CsmGeneral.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CryIfSupportsCertificateAPI
  长名称: ''
  描述: |
    If enabled, the referenced driver provides the services CertificateParse and CertificateVerify.
    This service was removed in ASR R19-11.
    
    If disabled, CryIf always returns E_NOT_OK when service is called for this driver. If
    CryIfDevErrorDetect is enabled, also a development error is reported.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CryIfSupportsKeyStatusAPI
  长名称: ''
  描述: |
    If enabled, the referenced driver provides the services KeyGetStatus and KeySetInvalid. These
    services are available since ASR R20-11.
    
    If disabled, CryIf always returns E_NOT_OK when service is called for this driver. If
    CryIfDevErrorDetect is enabled, also a development error is reported.
  默认值: false
  最小值: ''
  最大值: ''
```

