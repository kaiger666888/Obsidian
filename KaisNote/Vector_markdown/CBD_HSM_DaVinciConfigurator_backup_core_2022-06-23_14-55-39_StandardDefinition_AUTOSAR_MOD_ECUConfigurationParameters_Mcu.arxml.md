# Mcu

## 模块描述

Configuration of the Mcu (Microcontroler Unit) module.

## 容器列表

### 1. McuGeneralConfiguration

**描述**: This container contains the configuration (parameters) of the MCU driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling the development error detection and reporting.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuGetRamStateApi
  长名称: ''
  描述: Pre-processor switch to enable/disable the API Mcu_GetRamState.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: McuInitClock
  长名称: ''
  描述: If this parameter is set to FALSE, the clock initialization has to be disabled from the MCU
      driver. This concept applies when there are some write once clock registers and a
      bootloader is present. If this parameter is set to TRUE, the MCU driver is responsible
      of the clock initialization.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: McuNoPll
  长名称: ''
  描述: This parameter shall be set True, if the H/W does not have a PLL or the PLL circuitry is
      enabled after the power on without S/W intervention. In this case MCU_DistributePllClock
      has to be disabled and  MCU_GetPllStatus has to return MCU_PLL_STATUS_UNDEFINED.
      Otherwise this parameters has to be set False
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: McuPerformResetApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the use of the function Mcu_PerformReset()
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: McuVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. McuModuleConfiguration

**描述**: This container contains the configuration (parameters) of the MCU driver

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuClockSrcFailureNotification
  长名称: ''
  描述: Enables/Disables clock failure notification. In case this feature is not supported by HW the
      setting should be disabled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: McuNumberOfMcuModes
  长名称: ''
  描述: This parameter shall represent the number of Modes available for the MCU.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 3
  名称: McuRamSectors
  长名称: ''
  描述: This parameter shall represent the number of RAM sectors available for the MCU.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 4
  名称: McuResetSetting
  长名称: ''
  描述: This parameter relates to the MCU specific reset configuration. This applies to the function
      Mcu_PerformReset, which performs a microcontroller reset using the hardware feature of
      the microcontroller.
  默认值: ''
  最小值: 1
  最大值: 255
```

### 3. McuClockSettingConfig

**描述**: This container contains the configuration (parameters) for the Clock settings of the MCU.  Please
see MCU031 for more information on the MCU clock settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuClockSettingId
  长名称: ''
  描述: The Id of this McuClockSettingConfig to be used as argument for the API call "Mcu_InitClock".
  默认值: ''
  最小值: 1
  最大值: 255
```

### 4. McuClockReferencePoint

**描述**: This container defines a reference point in the Mcu Clock tree. It defines the frequency which then
can be used by other modules as an input value. Lower multiplictiy is 1, as even in the simpliest
case (only one frequency is used), there is one frequency to be defined.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuClockReferencePointFrequency
  长名称: ''
  描述: This is the frequency for the specific instance of the McuClockReferencePoint container. It
      shall be given in Hz.
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 5. McuDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 6. McuModeSettingConf

**描述**: This container contains the configuration (parameters) for the Mode setting of the MCU.  Please see
MCU035 for more information on the MCU mode settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuMode
  长名称: ''
  描述: The parameter represents the MCU Mode settings.
  默认值: ''
  最小值: 1
  最大值: 255
```

### 7. McuRamSectorSettingConf

**描述**: This container contains the configuration (parameters) for the RAM Sector setting. Please see MCU030
for more information on RAM sec-tor settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuRamDefaultValue
  长名称: ''
  描述: This parameter shall represent the Data pre-setting to be initialized
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: McuRamSectionBaseAddress
  长名称: ''
  描述: This parameter shall represent the MCU RAM section base address
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: McuRamSectionSize
  长名称: ''
  描述: This parameter represents the MCU RAM Section size in bytes.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 8. McuPublishedInformation

**描述**: Container holding all MCU specific published information parameters

该容器没有参数。

### 9. McuResetReasonConf

**描述**: This container contains the configuration for the different type of reset reason that can be
retrieved from Mcu_GetResetReason Api.

#### 参数列表

```yaml
- 
  序号: 1
  名称: McuResetReason
  长名称: ''
  描述: The parameter represents the different type of reset that a Micro supports. This parameter is
      referenced by the parameter EcuMResetReason in the ECU State manager module.
  默认值: ''
  最小值: 0
  最大值: 255
```

