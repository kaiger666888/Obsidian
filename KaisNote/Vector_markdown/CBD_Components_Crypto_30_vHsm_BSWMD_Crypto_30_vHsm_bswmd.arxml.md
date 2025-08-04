# Crypto

## 模块描述

Vector Crypto Driver for the MICROSAR vHSM. The Crypto Driver (CRYPTO) is called by the Crypto
Interface (CRYIF) and forwards the specific cryptographic operations to the MICROSAR vHSM side.
The Crypto Driver interfaces are specificed by AUTOSAR. This software-based Crypto Driver offers
algorithms and features depending on the configuration of MICROSAR vHSM.

#Security #Crypto #Cryptography #HSM
#AUTOSAR

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
- 
  序号: 3
  名称: CryptoBufferSize
  长名称: ''
  描述: |
    Size of the buffer allocated in the global RAM for this driver object.
    This buffer stores all the input and output data, which is not directly accessible by the vHsm,
    of the to be processed job. If Memory is accessible or not is defined by the CryptoMemoryArea
    configuration, e.g. RAM accessible by local CPU only or protected by MPU.
    
    Attention: The buffer may contain the data of up to 5 pointers. For better performance, the
    driver inserts padding bytes between the different data to ensure aligned access for vHsm.
    Therefore, the needed buffer size could be greater than the total size of the buffered data.
    
    To avoid unnecessary big buffers and the time to copy the data, consider providing the data
    directly from code flash or global RAM.
    
    The buffer can also be configured to 0 to avoid unecessary pointer checks against the whitelist
    of the driver (the vHsm firmware will still check the pointers). Pay attention that all input
    and output needs to be mapped correctly in this case as the driver will not take care about
    copying the data to and from memory which can be accessed by the vHsm firmware. For SafeBsw it
    is also no possible to use a buffersize of 0.
  默认值: 128
  最小值: 0
  最大值: 4294967294
```

### 3. CryptovHsmBuffer

**描述**: Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize instead.
This parameter summarizes all buffers included in this container.

Container to specify the size of the buffers for each parameter which will be used when the pointer
points to invalid memory e.g. local RAM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoInputBufferSize
  长名称: ''
  描述: |
    Parameter is deprecated and not used anymore. Only available for backward compatibility.
    Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize
    instead.
    
    Size of the buffer on the global RAM to store the input data which is provided from the local
    RAM.
    
  默认值: 0
  最小值: 0
  最大值: 4294967294
- 
  序号: 2
  名称: CryptoSecondaryInputBufferSize
  长名称: ''
  描述: |
    Parameter is deprecated and not used anymore. Only available for backward compatibility.
    Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize
    instead.
    
    Size of the buffer on the global RAM to store the secondary input data which is provided from
    the local RAM.
  默认值: 0
  最小值: 0
  最大值: 4294967294
- 
  序号: 3
  名称: CryptoTertiaryInputBufferSize
  长名称: ''
  描述: |
    Parameter is deprecated and not used anymore. Only available for backward compatibility.
    Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize
    instead.
    
    Size of the buffer on the global RAM to store the tertiary input data which is provided from the
    local RAM.
  默认值: 0
  最小值: 0
  最大值: 4294967294
- 
  序号: 4
  名称: CryptoOutputBufferSize
  长名称: ''
  描述: |
    Parameter is deprecated and not used anymore. Only available for backward compatibility.
    Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize
    instead.
    
    Size of the buffer on the global RAM to store the output data which will be written to the local
    RAM.
  默认值: 0
  最小值: 0
  最大值: 4294967294
- 
  序号: 5
  名称: CryptoSecondaryOutputBufferSize
  长名称: ''
  描述: |
    Parameter is deprecated and not used anymore. Only available for backward compatibility.
    Use /MICROSAR/Crypto_30_vHsm/Crypto/CryptoDriverObjects/CryptoDriverObject/CryptoBufferSize
    instead.
    
    Size of the buffer on the global RAM to store the secondary output data which will be written to
    the local RAM.
  默认值: 0
  最小值: 0
  最大值: 4294967294
```

### 4. CryptoGeneral

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
  序号: 3
  名称: CryptoMainFunctionPeriod
  长名称: ''
  描述: Specifies the period of main function Crypto_MainFunction in seconds. 
  默认值: 0.01
  最小值: 0
  最大值: 3600
- 
  序号: 4
  名称: CryptoUserConfigFile
  长名称: ''
  描述: |
    Reference to an external user configuration file that will be included during generation.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CryptoSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CryptoMultiPartitionRuntimeChecks
  长名称: ''
  描述: If enabled, additional checks are performed to prevent the usage of driver objects by wrong
      partitions.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CryptoTimeoutCallout
  长名称: ''
  描述: |
    If this parameter is set to true, the following callout functions get called at each loop where
    the driver has to wait for the HSM core:
    Crypto_30_vHsm_TimeoutDetect_Start_Callout, Crypto_30_vHsm_TimeoutDetect_Loop_Callout,
    Crypto_30_vHsm_TimeoutDetect_End_Callout
    
    These callouts can be used to detect violations of freedom from interference with respect to
    timing of the loops.
    See the Technical Reference of this module for more information.
    
    If this parameter is set to false, the mentioned callout functions never get called.
  默认值: false
  最小值: ''
  最大值: ''
```

### 5. CryptoKeyElements

**描述**: Container  for CRYPTO  key elements

该容器没有参数。

### 6. CryptoKeyElement

**描述**: Configuration of a CryptoKeyElement

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoKeyElementId
  长名称: ''
  描述: Identifier of the CRYPTO key element 
  默认值: 0
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
    CRYPTO_RA_DENIED = key element cannot be read from outside the Crypto
    Driver
    CRYPTO_RA INTERNAL_COPY = key element can be copied to another key
    element in the same crypto driver.
    CRYPTO_RA_ALLOWED = key element can be read as plaintext
    CRYPTO_RA_ENCRYPTED = key element can be read encrypted. E.g. SHE Ram-
    Key export.
  默认值: RA_ALLOWED
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CryptoKeyElementAllowPartialAccess
  长名称: ''
  描述: |
    Enable or disable writing and reading the key element with data smaller
    than the size of the element.
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

### 7. CryptoKeyTypes

**描述**: Container for CRYPTO key types

该容器没有参数。

### 8. CryptoKeyType

**描述**: Configuration of a CryptoKeyType

该容器没有参数。

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
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoKeyDeriveIterations
  长名称: ''
  描述: Holds the number of iterations to be performed by the key derivation primitive
  默认值: 1
  最小值: 1
  最大值: 4294967295
```

### 11. CryptoPrimitives

**描述**: Container for CRYPTO primitives

该容器没有参数。

### 12. CryptoPrimitive

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
- 
  序号: 5
  名称: CryptoPrimitiveSupportContext
  长名称: ''
  描述: Configures if the crypto primitive supports to store or restore context data of the workspace.
      Since this option is vulnerable to security, it shall only set to TRUE if absolutely
      needed.
  默认值: false
  最小值: ''
  最大值: ''
```

### 13. CryptoPrimitiveAlgorithmFamilyCustom

**描述**: Container of custom algorithm family values.
The container name serves as a symbolic name for the identifier of the custom algorithm family type.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoPrimitiveAlgorithmFamilyCustomId
  长名称: ''
  描述: The custom value of this algorithm family
  默认值: 128
  最小值: 128
  最大值: 254
```

### 14. CryptoPrimitiveAlgorithmModeCustom

**描述**: Container of custom algorithm mode values.
The container name serves as a symbolic name for the identifier of the custom algorithm mode type.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoPrimitiveAlgorithmModeCustomId
  长名称: ''
  描述: The custom value of this algorithm mode
  默认值: 128
  最小值: 128
  最大值: 254
```

### 15. CryptovHsm

**描述**: Basic configuration of the vHsm Driver

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoKeyElementDeleteSupport
  长名称: ''
  描述: If this option is enabled, it disables a DET check which checks if the keyLength and keyPtr is
      not zero. (This check is part of the AUTOSAR Specification.)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryptoInterruptMode
  长名称: ''
  描述: |
    If the interrupt mode is enabled, the vHsm will inform the application core about a finished job
    with the help of an interrupt.
    The interrupt will then call the CryIf callback from the interrupt context in case of an async
    job.
    
    If the interrupt mode is disabled, the driver will poll the IPC for finished jobs.
    - For async jobs, this will be done in the main function. Also the callback will be called from
    the main function.
    - For sync jobs, this will be done in the waiting loop during the job.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CryptoIpcChannels
  长名称: ''
  描述: Number of IPC channels used to communicate with the vHsm
  默认值: 4
  最小值: 1
  最大值: 255
- 
  序号: 4
  名称: CryptoIpcProtocolVersion
  长名称: ''
  描述: |
    Protocol version used to communicate with the vHsm Firmware over IPC.
    The used protocol version must be the same on both the driver and vHsm Firmware.
    
    Info: IPC Protocol Version 2 is deprecated and will be removed in future versions.
    
  默认值: 3
  最小值: 2
  最大值: 3
- 
  序号: 5
  名称: CryptoWaitLoopCallout
  长名称: ''
  描述: Callout which is called while waiting for responses from the vHsm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CryptoHsmUserRevision
  长名称: ''
  描述: |
    This parameter is always updated with the one located in the generated vHSM pre configuration
    file.
    Attention: This parameter is freely configurable in the vHSM
    (/MICROSAR/vHsm/vHsmGeneral/vHsmUserRevision) and changes only if was manually adapted in vHSM
    config. Use this to make sure that application and HSM on the same revision.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CryptoRedirection
  长名称: ''
  描述: Enable job input/output redirection to key elements. This is a Autosar 4.4 feature. Therefore
      a Csm and CryIf is required which also needs to support this feature
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CryptoIpcMacJobOptimization
  长名称: ''
  描述: |
    During MAC Verification only inputPtr, secondaryInputPtr and verifyPtr are needed. During MAC
    Generation only inputPtr and outputPtr are needed.
    
    This optimization reduces the transmission of mac jobs to this pointers. This will lead to a
    faster processing of the MAC because unnecessary checks for validity can be omitted.
    
    This feature may only be enabled if vHsm support this feature as well. This is true for vHsm
    starting from version 02.01.00 (R22)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CryptoDetInstanceMask
  长名称: ''
  描述: Det errors originating from the vHsm can be distinguished from det errors of the application
      cores by OR-ing the mask with instanceId before passing the received Det to
      Det_ErrorReport() on the application core.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: CryptoKeyDeriveJobSupport
  长名称: ''
  描述: Enables support for KeyDerive operations processed as jobs. This needs to be supported by both
      the HSM and Csm.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CryptoHost2HsmAddress
  长名称: Host2Hsm Address
  描述: Address of the register which is used to communicate from Host to the HSM core
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 12
  名称: CryptoHsm2HostAddress
  长名称: Hsm2Host Address
  描述: Address of the register which is used to communicate from Hsm to the Host core
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 13
  名称: CryptoIpcInstanceId
  长名称: ''
  描述: Id of the Ipc instance inside the Hsm
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: CryptoIpcInitialization
  长名称: ''
  描述: If enabled, the driver will initialize the IPC memory and notify the vHsm firmware about the
      now usable IPC memory via the HOST2HSM interface
  默认值: true
  最小值: ''
  最大值: ''
```

### 16. CryptoMemoryArea

**描述**: White list of memory areas used as input and output for crypto jobs or key management operations.
The areas from the whitelist of the vHsm configuration can be used also in the driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoAreaStart
  长名称: ''
  描述: Start address of the memory area
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoAreaStop
  长名称: ''
  描述: End address of the memory area
  默认值: 4294967295
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: CryptoAreaType
  长名称: ''
  描述: Type of the memory area as seen from the vHsm.
  默认值: CRYPTO_AREA_HSM_READ_ACCESS
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CryptoAreaPriority
  长名称: ''
  描述: |
    The priority of the memory area.
    The higher the value, the higher the areas priority.
    The area with the highest priority will be checked first.
    To get the best performance assign a high priority to areas which are used very often.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: CryptoAreaEnabled
  长名称: ''
  描述: |
    Memory areas can be disabled if needed.
    This can be used in the Safe Use-Case, when it is not allowed to have an enabled READWRITE area.
  默认值: true
  最小值: ''
  最大值: ''
```

### 17. CryptoJobResponseInterrupt

**描述**: Configures settings for receiving an interrupt from the hsm

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoJobResponseInterruptFlagClearAddress
  长名称: ''
  描述: Address of the register which is used to clear the interrupt request flag
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoJobResponseInterruptFlagClearMask
  长名称: ''
  描述: Mask which is used to set the value
  默认值: 1
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: CryptoJobResponseInterruptFlagClearValue
  长名称: ''
  描述: Value which will be set to the masked register
  默认值: 1
  最小值: 0
  最大值: 1
- 
  序号: 4
  名称: CryptoJobResponseInterruptFlagClearing
  长名称: ''
  描述: Clearing the flag is only needed when the OS does not clear the interrupt flag automatically.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CryptoJobResponseInterruptFlagClearHandling
  长名称: ''
  描述: |
    Configures the way, how the interrupt flag is cleared.
    On different platforms a different access to e.g. registers is needed.
    Below is the corresponding code to each option which will be generated when clearing a flag:
    
    CRYPTO_CLEAR_INCLUSIVE_OR_ASSIGNMENT -&gt; *ClearAddress |= mask
    CRYPTO_CLEAR_INCLUSIVE_AND_NOT_ASSIGNMENT -&gt; *ClearAddress &= ~mask
    CRYPTO_CLEAR_ONLY_READ -&gt; dummyVar = *ClearAddress
    CRYPTO_CLEAR_CALLOUT -&gt; call of Crypto_30_vHsm_ResponseInterruptClear_Callout()
  默认值: CRYPTO_CLEAR_INCLUSIVE_OR_ASSIGNMENT
  最小值: ''
  最大值: ''
```

### 18. CryptoJobRequestInterrupt

**描述**: Configures settings for triggering an interrupt to the hsm

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoJobRequestInterruptFlagSetAddress
  长名称: ''
  描述: Address of the register which is used to clear the interrupt request flag
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: CryptoJobRequestInterruptFlagSetMask
  长名称: ''
  描述: Mask which is used to set the value
  默认值: 1
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: CryptoJobRequestInterruptFlagSetting
  长名称: ''
  描述: Setting the interrupt flag and thus triggering an interrupt to the vHsm is only needed when
      isr support in vHsm is enabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CryptoJobRequestInterruptFlagSetHandling
  长名称: ''
  描述: |
    Configures the way, how the interrupt flag is set.
    On different platforms a different access to e.g. registers is needed.
    Below is the corresponding code to each option which will be generated when clearing a flag:
    
    CRYPTO_SET_INCLUSIVE_OR_ASSIGNMENT -> *SetAddress |= mask
    CRYPTO_SET_ONLY_ASSIGNMENT -> *SetAddress = mask
    CRYPTO_SET_CALLOUT -> call of Crypto_30_vHsm_RequestInterruptSet_Callout()
  默认值: CRYPTO_SET_INCLUSIVE_OR_ASSIGNMENT
  最小值: ''
  最大值: ''
```

### 19. CryptoIpcInstance

**描述**: Specifies the Ecu MultiCore partitions to which each Ipc can be mapped to.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryptoIpcInstanceId
  长名称: ''
  描述: Id of the Ipc instance inside the Hsm
  默认值: 0
  最小值: 0
  最大值: 255
```

