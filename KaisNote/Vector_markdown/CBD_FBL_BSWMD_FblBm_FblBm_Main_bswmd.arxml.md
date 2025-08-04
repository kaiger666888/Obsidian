# FblBm

## 模块描述

Configuration of the FblBm (Boot Manager) module.

## 容器列表

### 1. FblBmGeneral

**描述**: General configuration parameters of the FblBm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblBmHeaderAddress
  长名称: ''
  描述: This is the start address of the BootManager's BmHeader structure (defined in module
      bm_main.c). TheBootManager header can be located at an arbitrary address using the
      provided section #pragma instructions.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: FblBmUserConfigFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation to FblBm_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FblBmUserIncludeHeader
  长名称: ''
  描述: |
    This parameter is used to specify additional header files to be included in the generated
    FblBm_Cfg.h.
    
    Insert complete filenames including extension (e.g. MyHeader.h).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FblBmSecureBoot
  长名称: ''
  描述: |
    Enable or disable the secure boot functionality.
    
    True: The BootManager uses the hardware module (SHE/HSM) to verify that the memory has not been
    altered.
    False: The BootManger checks only the validity.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FblBmStandaloneMode
  长名称: ''
  描述: |
    This parameter defines whether the BootManager is compiled/linked standalone or with the
    Bootloader.
    
    True: The BootManager is compiled/linked standalone. BootManager and Bootloader will be two
    separate projects.
    False: The BootManager is compiled/linked together with the Bootloader.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FblBmIncludeOemConfiguration
  长名称: ''
  描述: |
    This parameter defines whether the OEM configuration file “bm_oem_cfg.h” should be included or
    not.
    
    True: The header file is included in FblBm_Cfg.h.
    False: The header is not included.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FblBmIncludeHardwareConfiguration
  长名称: ''
  描述: |
    This parameter defines whether the hardware configuration file “bm_hw_cfg.h” should be included
    or not.
    
    True: The header file is included in FblBm_Cfg.h.
    False: The header is not included.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FblBmFailsafeUpdater
  长名称: ''
  描述: |
    Enables or disables the feature failsafe updater, where the Bootmanager is searching for an
    updater in case the Bootloader is corrupted.
    
    True: BootManager searches for an updater and starts it.
    False: BootManager goes into a fail state (see callout function FBLBM_CALLOUT_FATAL_ERROR)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FblBmInitializeKeys
  长名称: ''
  描述: |
    Enables or disables the feature where the Bootmanager checks if the keys are programmed, see
    callout function FBLBM_CALLOUT_GET_KEYEMPTY.
    
    True: BootManager calls Bootloader in case keys are determined to be empty.
    False: Bootmanager continues sequence normally.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: FblBmInitializeMacOfBootloader
  长名称: ''
  描述: |
    Enables or disables the feature where the Bootmanager checks if the MAC of the Bootloader is
    present, see callout function FBLBM_CALLOUT_GET_FBL_CMACERASED.
    
    True: BootManager calls Bootloader in case MAC of Bootloader is determined to be not written so
    yet.
    False: Bootmanager continues sequence normally.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: FblBmExecutionInstance
  长名称: ''
  描述: Determines the context the software is getting build.
  默认值: BootManager
  最小值: ''
  最大值: ''
```

### 2. FblBmBootOrder

**描述**: Contains boot targets and related dependency targets

该容器没有参数。

### 3. FblBmDependency

**描述**: List of all dependency targets, which can be used by the boot targets

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblBmDisposability
  长名称: Disposability
  描述: Specify whether the dependency target should be mandatory or optional
  默认值: OPTIONAL
  最小值: ''
  最大值: ''
```

### 4. FblBmBootTarget

**描述**: List of all bootable targets

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblBmBootOrderId
  长名称: Boot Order Id
  描述: Identifier of the boot target order
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

