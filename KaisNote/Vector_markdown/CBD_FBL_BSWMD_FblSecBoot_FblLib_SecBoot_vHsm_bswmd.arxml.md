# FblSb

## 模块描述

Configuration of the FblSb (Secure Boot) module.

## 容器列表

### 1. FblSbGeneral

**描述**: General configuration parameters of the FblSb.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblSbUserConfigFile
  长名称: User Config File
  描述: |
    Reference to an external text file that will be included during generation to FblSb_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FblSbCopyFlashDriver
  长名称: Copy Flash Driver
  描述: |
    Enables or disables the copy flash driver API (FblSb_CopyFlashDriver), which copies the internal
    code flash driver into RAM.
    True: Copy routine is available.
    False: Copy routine is deactivated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FblSbHeaderVerification
  长名称: Header Verification
  描述: If enabled it is possible to verify the header structure separately
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FblSbFblLbtVerification
  长名称: Fbl Lbt Verification
  描述: If enabled it is possible to verify the LBT of the FBL separately
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FblSbVerificationList
  长名称: Verification List
  描述: Specify if a verification list in the FblBmHdrHeader structure is required
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FblSbSecureBootUpdateSignatureAlgorithm
  长名称: ''
  描述: |
    Specifies the algorithm used by the vHsm to determine the length of the signature.
    
    Note: If the algorithm is not listed, use CUSTOM and manually enter the signature length in
    FblSbSecureBootUpdateSignatureLength.
    
  默认值: ED25519
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FblSbSecureBootUpdateSignatureLength
  长名称: ''
  描述: |
    Length of the signature used by the vHsm during the SecureBootUpdate sequence.
    Automatically filled out in case the algorithm is already known.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 2. FblSbMacOperation

**描述**: Container for configuration of the MacOperation used to generate and verify MACs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblSbMacOperationId
  长名称: Mac Operation Id
  描述: Identifier of the MacOperation.
  默认值: 0
  最小值: 0
  最大值: 255
```

