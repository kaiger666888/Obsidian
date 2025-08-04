# FlsLoader

## 模块描述

Configuration of the FlsLoader module.

## 容器列表

### 1. FlsLoaderGeneral

**描述**: FlsLoader driver configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderDevErrorDetect
  长名称: ''
  描述: Preprocessor switch to enable/disable the FlsLoaderDevErrorDetect.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FlsLoaderEnableLockCheck
  长名称: ''
  描述: Preprocessor switch to enable/disable the Lock Check functionality in Erase and Write API's.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FlsLoaderCallOutFunction
  长名称: ''
  描述: User defined call out function. User can provide either a call out function name or address of
      call out function. Default value of NULL_PTR is considered as call out disabled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FlsLoaderCallOutTime
  长名称: ''
  描述: Specifies the maximum time in nanoseconds to wait before invoking call-out function to
      application
  默认值: 5000000
  最小值: 10000
  最大值: 4294967295
```

### 2. FlsLoaderOptionalApi

**描述**: FlsLoader driver optional API Configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderDeInitApi
  长名称: ''
  描述: Preprocessor switch to enable/disable the FlsLoader_DeInit API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FlsLoaderLockUnlockApi
  长名称: ''
  描述: Preprocessor switch to enable/disable the FlsLoader_Lock and FlsLoader_Unlock APIs
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FlsLoaderVersionInfoApi
  长名称: ''
  描述: Preprocessor switch to enable/disable the FlsLoader_GetVersionInfo API
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. FlsLoaderPFLASHConfig

**描述**: This container contains the sub containers for each PFLASH Bank configuration.

该容器没有参数。

### 4. FlsLoaderPFlash0ProtConfig

**描述**: PFLASH Bank 0 protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFLash0WriteProt
  长名称: ''
  描述: PFLASH Bank 0 protection configuration.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FlsLoaderPFUcbPW0_0
  长名称: ''
  描述: 1th least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FlsLoaderPFUcbPW0_1
  长名称: ''
  描述: 2nd least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: FlsLoaderPFUcbPW1_0
  长名称: ''
  描述: 3rd least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: FlsLoaderPFUcbPW1_1
  长名称: ''
  描述: 4th least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: FlsLoaderPFUcbPW2_0
  长名称: ''
  描述: 5th least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: FlsLoaderPFUcbPW2_1
  长名称: ''
  描述: 6th least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 8
  名称: FlsLoaderPFUcbPW3_0
  长名称: ''
  描述: 7th least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 9
  名称: FlsLoaderPFUcbPW3_1
  长名称: ''
  描述: Most significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 5. FlsLoaderPF0Sector

**描述**: Configuration of the individual PF0 sectors.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFSectorWriteProtection
  长名称: ''
  描述: Sector Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
```

### 6. FlsLoaderPFlash1ProtConfig

**描述**: PFLASH Bank 1 protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFLash1WriteProt
  长名称: ''
  描述: PFlash Read/Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
```

### 7. FlsLoaderPF1Sector

**描述**: PFLASH Bank 1 sector protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFSectorWriteProtection
  长名称: ''
  描述: Sector Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
```

### 8. FlsLoaderPFlash2ProtConfig

**描述**: PFLASH Bank 2 protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFLash2WriteProt
  长名称: ''
  描述: PFlash Read/Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
```

### 9. FlsLoaderPF2Sector

**描述**: PFLASH Bank 2 sector protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFSectorWriteProtection
  长名称: ''
  描述: Sector Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
```

### 10. FlsLoaderPFlash3ProtConfig

**描述**: PFLASH Bank 3 protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFLash3WriteProt
  长名称: ''
  描述: PFlash Read/Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
```

### 11. FlsLoaderPF3Sector

**描述**: PFLASH Bank 3 sector protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFSectorWriteProtection
  长名称: ''
  描述: Sector Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
```

### 12. FlsLoaderPFlash4ProtConfig

**描述**: PFLASH Bank 4 protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFLash4WriteProt
  长名称: ''
  描述: PFlash Read/Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
```

### 13. FlsLoaderPF4Sector

**描述**: PFLASH Bank 1 sector protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFSectorWriteProtection
  长名称: ''
  描述: Sector Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
```

### 14. FlsLoaderPFlash5ProtConfig

**描述**: PFLASH Bank 5 protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFLash5WriteProt
  长名称: ''
  描述: PFlash Read/Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
```

### 15. FlsLoaderPF5Sector

**描述**: PFLASH Bank 5 sector protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderPFSectorWriteProtection
  长名称: ''
  描述: Sector Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
```

### 16. FlsLoaderDFLASHConfig

**描述**: This container contains the configuration parameters and sub containers of the FlsLoader module.

该容器没有参数。

### 17. FlsLoaderDFlash0ProtConfig

**描述**: DF protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsLoaderDF0Prot
  长名称: ''
  描述: DF0 Read/Write protection.
  默认值: NO_PROTECTION
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FlsLoaderDF0UcbPW0_0
  长名称: ''
  描述: 1st least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FlsLoaderDF0UcbPW0_1
  长名称: ''
  描述: 2nd least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: FlsLoaderDF0UcbPW1_0
  长名称: ''
  描述: 3rd least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: FlsLoaderDF0UcbPW1_1
  长名称: ''
  描述: 4th least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: FlsLoaderDF0UcbPW2_0
  长名称: ''
  描述: 5th least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: FlsLoaderDF0UcbPW2_1
  长名称: ''
  描述: 6th least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 8
  名称: FlsLoaderDF0UcbPW3_0
  长名称: ''
  描述: 7th least significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 9
  名称: FlsLoaderDF0UcbPW3_1
  长名称: ''
  描述: Most significant word password out of 8 words  password
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 18. CommonPublishedInformation

**描述**: Common container, aggregated by all modules. It contains published information about vendor and
versions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArMajorVersion
  长名称: ''
  描述: Major version number of AUTOSAR specification on which the appropriate implementation is based
      on.
  默认值: 4
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: ArMinorVersion
  长名称: ''
  描述: Minor version number of AUTOSAR specification on which the appropriate implementation is based
      on.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: ArPatchVersion
  长名称: ''
  描述: Patch level version number of AUTOSAR specification on which the appropriate implementation is
      based on.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: SwMajorVersion
  长名称: ''
  描述: Major version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 20
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: SwMinorVersion
  长名称: ''
  描述: Minor version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: SwPatchVersion
  长名称: ''
  描述: Patch level version number of the vendor specific implementation of the module. The numbering
      is vendor specific.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: ModuleId
  长名称: ''
  描述: Module ID of this module from Module List
  默认值: 255
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: VendorId
  长名称: ''
  描述: Vendor ID of the dedicated implementation of this module according to the AUTOSAR vendor list
  默认值: 17
  最小值: 0
  最大值: 65535
- 
  序号: 9
  名称: Release
  长名称: ''
  描述: Aurix2G derivative used for the implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

