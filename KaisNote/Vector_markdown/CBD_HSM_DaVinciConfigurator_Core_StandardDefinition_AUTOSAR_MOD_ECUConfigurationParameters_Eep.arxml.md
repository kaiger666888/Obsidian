# Eep

## 模块描述

Configuration of the Eep (internal or external EEPROM driver) module.

## 容器列表

### 1. EepGeneral

**描述**: Container for general configuration parameters of the EEPROM driver. These parameters are always
pre-compile.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EepDevErrorDetect
  长名称: ''
  描述: Pre-processor switch to enable and disable development error detection.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EepDriverIndex
  长名称: ''
  描述: Index of the driver, used by EA.
  默认值: ''
  最小值: 0
  最大值: 254
- 
  序号: 3
  名称: EepUseInterrupts
  长名称: ''
  描述: Switches to activate or deactivate interrupt controlled job processing.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EepVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EepWriteCycleReduction
  长名称: ''
  描述: Switches to activate or deactivate write cycle reduction (EEPROM value is read and compared
      before being overwritten).
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. EepInitConfiguration

**描述**: Container for runtime configuration parameters of the EEPROM driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EepBaseAddress
  长名称: ''
  描述: This parameter is the EEPROM device base address.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: EepDefaultMode
  长名称: ''
  描述: This parameter is the default EEPROM device mode after initialization.
  默认值: MEMIF_MODE_SLOW
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EepFastReadBlockSize
  长名称: ''
  描述: Number of bytes read within one job processing cycle in fast mode. If the hardware does not
      support burst mode this parameter shall be set to the same value as
      EepNormalReadBlockSize.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: EepFastWriteBlockSize
  长名称: ''
  描述: Number of bytes written within one job processing cycle in fast mode. If the hardware does not
      support burst mode this parameter shall be set to the same value as
      EepNormalWriteBlockSize.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: EepJobCallCycle
  长名称: ''
  描述: Call cycle time of the EEPROM driver's main function. Unit: [s]
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 6
  名称: EepJobEndNotification
  长名称: ''
  描述: This parameter is a reference to a callback function for positive job result (see EEP045).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EepJobErrorNotification
  长名称: ''
  描述: This parameter is a reference to a callback function for negative job result (see EEP046).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EepNormalReadBlockSize
  长名称: ''
  描述: Number of bytes read within one job processing cycle in normal mode.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 9
  名称: EepNormalWriteBlockSize
  长名称: ''
  描述: Number of bytes written within one job processing cycle in normal mode.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 10
  名称: EepSize
  长名称: ''
  描述: This parameter is the used size of EEPROM device in bytes.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 3. EepDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 4. EepExternalDriver

**描述**: This container is present for external EEPROM drivers only. Internal EEPROM drivers do not use the
parameter listed in this container, hence its multiplicity is 0 for internal drivers.

该容器没有参数。

### 5. EepPublishedInformation

**描述**: Additional published parameters not covered by CommonPublishedInformation container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EepAllowedWriteCycles
  长名称: ''
  描述: Specified maximum number of write cycles under worst case conditions of specific EEPROM
      hardware (e.g. +90°C)
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: EepEraseTime
  长名称: ''
  描述: Maximum time for erasing one EEPROM data unit.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: EepEraseUnitSize
  长名称: ''
  描述: Size of smallest erasable EEPROM data unit in bytes.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: EepEraseValue
  长名称: ''
  描述: Value of an erased EEPROM cell.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: EepMinimumAddressType
  长名称: ''
  描述: Minimum expected size of Eep_AddressType.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: EepMinimumLengthType
  长名称: ''
  描述: Minimum expected size of Eep_LengthType.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: EepReadUnitSize
  长名称: ''
  描述: Size of smallest readable EEPROM data unit in bytes.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 8
  名称: EepSpecifiedEraseCycles
  长名称: ''
  描述: Number of erase cycles specified for the EEP device (usually given in the device data sheet).
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 9
  名称: EepTotalSize
  长名称: ''
  描述: Total size of EEPROM in bytes.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 10
  名称: EepWriteTime
  长名称: ''
  描述: Maximum time for writing one EEPROM data unit.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 11
  名称: EepWriteUnitSize
  长名称: ''
  描述: Size of smallest writeable EEPROM data unit in bytes.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

