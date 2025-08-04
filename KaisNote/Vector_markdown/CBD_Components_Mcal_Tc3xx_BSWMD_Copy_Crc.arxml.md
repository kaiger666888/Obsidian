# Crc

## 模块描述

Configuration of the Crc (Crc routines) module.

## 容器列表

### 1. CrcGeneral

**描述**: General configuration of CRC module

#### 参数列表

```yaml
- 
  序号: 1
  名称: Crc16ARCMode
  长名称: ''
  描述: Switch to select one of the available 16-bit CRC16ARC polynomial methods
  默认值: CRC_16_ARC_HARDWARE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Crc16Mode
  长名称: ''
  描述: Switch to select one of the available CRC 16-bit (CCITT) calculation methods
  默认值: CRC_16_HARDWARE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Crc32Mode
  长名称: ''
  描述: Switch to select one of the available CRC 32-bit (IEEE-802.3 CRC32 Ethernet Standard)
      calculation methods
  默认值: CRC_32_HARDWARE
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Crc32P4Mode
  长名称: ''
  描述: Switch to select one of the available CRC 32-bit E2E Profile 4 calculation methods.
  默认值: CRC_32P4_TABLE
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Crc64Mode
  长名称: ''
  描述: Switch to select one of the available CRC 64-bit calculation methods.
  默认值: CRC_64_TABLE
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Crc8H2FMode
  长名称: ''
  描述: Switch to select one of the available CRC 8-bit (2Fh polynomial) calculation methods
  默认值: CRC_8H2F_HARDWARE
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Crc8Mode
  长名称: ''
  描述: Switch to select one of the available CRC 8-bit (SAE J1850) calculation methods
  默认值: CRC_8_HARDWARE
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CrcVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CrcSafetyEnable
  长名称: ''
  描述: Pre-processor switch to enable / disable the Safety checks for all APIs
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CrcDma8bitApi
  长名称: ''
  描述: Switch to enable/disable 8-bit SAE J1850 polynomial for CRC calculation while using the DMA
      based API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CrcDma16bitApi
  长名称: ''
  描述: Switch to enable/disable 16-bit CCITT-FALSE CRC16 polynomial for CRC calculation while using
      the DMA based API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: CrcDma32bitApi
  长名称: ''
  描述: Switch to enable/disable 32-bit IEEE-802.3 polynomial for CRC calculation while using the DMA
      based API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: CrcDma32P4bitApi
  长名称: ''
  描述: Switch to enable/disable 32-bit (0xF4ACFB13) polynomail for CRC calculation while using the
      DMA based API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: CrcRuntimeApiMode
  长名称: ''
  描述: Switch to select one of the available CRC implementation mode
  默认值: CRC_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: Crc8ReturnErrorValue
  长名称: ''
  描述: Error value that will be returned in case of an invalid input parameter.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: Crc8H2FReturnErrorValue
  长名称: ''
  描述: Error value that will be returned in case of an invalid input parameter.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 17
  名称: Crc16ReturnErrorValue
  长名称: ''
  描述: Error value that will be returned in case of an invalid input parameter.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 18
  名称: Crc16ARCReturnErrorValue
  长名称: ''
  描述: Error value that will be returned in case of an invalid input parameter.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 19
  名称: Crc32ReturnErrorValue
  长名称: ''
  描述: Error value that will be returned in case of an invalid input parameter.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 20
  名称: Crc32P4ReturnErrorValue
  长名称: ''
  描述: Error value that will be returned in case of an invalid input parameter.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 21
  名称: Crc64ReturnErrorValue
  长名称: ''
  描述: Error value that will be returned in case of an invalid input parameter.
  默认值: 0
  最小值: 0
  最大值: 9223372036854775807
```

### 2. CrcChannelConfig

**描述**: CRC Configuration of FCE channels, callback functions and alloctaion of DMA channel

#### 参数列表

```yaml
- 
  序号: 1
  名称: CrcChannelId
  长名称: ''
  描述: CRC Allocation of FCE channels
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: CrcResultNotification
  长名称: ''
  描述: User defined result callback function
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CrcErrorNotification
  长名称: ''
  描述: User defined error callback functionr
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. CrcPublishedInformation

**描述**: Additional published parameters not covered by CommonPublishedInformation container.

Note that these parameters do not have any configuration class setting, since they are published
information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CrcInitialValue16
  长名称: ''
  描述: Initial value for the 16-bit CRC calculation.
  默认值: 65535
  最小值: 65535
  最大值: 65535
- 
  序号: 2
  名称: CrcInitialValue16ARC
  长名称: ''
  描述: Initial value for the 16-bit CRC16ARC calculation
  默认值: 0
  最小值: 0
  最大值: 0
- 
  序号: 3
  名称: CrcInitialValue8
  长名称: ''
  描述: Initial value for the 8-bit CRC calculation.
  默认值: 255
  最小值: 255
  最大值: 255
- 
  序号: 4
  名称: CrcInitialValue8H2F
  长名称: ''
  描述: Initial value for the 8-bit CRC8H2F calculation.
  默认值: 255
  最小值: 255
  最大值: 255
- 
  序号: 5
  名称: CrcInitialValue32
  长名称: ''
  描述: Initial value for the 32-bit CRC calculation.
  默认值: 4294967295
  最小值: 4294967295
  最大值: 4294967295
- 
  序号: 6
  名称: CrcInitialValue32P4
  长名称: ''
  描述: Initial value for the 32-bit CRC32P4 calculation.
  默认值: 4294967295
  最小值: 4294967295
  最大值: 4294967295
- 
  序号: 7
  名称: CrcInitialValue64
  长名称: ''
  描述: Initial value for the 64-bit CRC64 calculation.
  默认值: 18446744073709551615
  最小值: 0
  最大值: 18446744073709551615
```

### 4. CommonPublishedInformation

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
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: ModuleId
  长名称: ''
  描述: Module ID of this module from Module List
  默认值: 201
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
  描述: Aurix derivative used for the implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

