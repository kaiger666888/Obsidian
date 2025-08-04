# vBaseEnv

## 模块描述

Configuration of the hardware.

## 容器列表

### 1. vBaseEnvGeneral

该容器没有参数。

### 2. vBaseEnvDerivativeInformation

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBaseEnvCpuMaxFrequency
  长名称: ''
  描述: |
    Configure the maximum frequency of this derivative.
    This value is used to validate the vBRS PLL configuration.
  默认值: 100000000
  最小值: 0
  最大值: ''
- 
  序号: 2
  名称: vBaseEnvAvailableChannels_Flexray
  长名称: ''
  描述: Configure the amount of Flexray channels, available on this derivative.
  默认值: 0
  最小值: 0
  最大值: 256
- 
  序号: 3
  名称: vBaseEnvAvailableChannels_Can
  长名称: ''
  描述: Configure the amount of CAN channels, available on this derivative.
  默认值: 0
  最小值: 0
  最大值: 256
- 
  序号: 4
  名称: vBaseEnvAvailableChannels_Lin
  长名称: ''
  描述: Configure the amount of LIN channels, available on this derivative.
  默认值: 0
  最小值: 0
  最大值: 256
- 
  序号: 5
  名称: vBaseEnvAvailableChannels_Ethernet
  长名称: ''
  描述: Configure the amount of Ethernet channels, available on this derivative.
  默认值: 0
  最小值: 0
  最大值: 256
- 
  序号: 6
  名称: vBaseEnvCpuCoreAmount
  长名称: ''
  描述: |
    Configure the amount of cores, available on this derivative.
    This value will be generated into vBrsCfg.h as
    BRS_CPU_CORE_AMOUNT
  默认值: 1
  最小值: 1
  最大值: 256
- 
  序号: 7
  名称: vBaseEnvTestedDerivative
  长名称: ''
  描述: |
    Configure the correct Mcu_Derivative value of this derivative.
    This value will be generated into vBrsCfg.h as
    BRS_DERIVATIVE_x
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vBaseEnvTestedDerivativeDescription
  长名称: ''
  描述: |
    Describe here more precisely this derivative.
    This description is only textual information for the user.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vBaseEnvCpuCore
  长名称: ''
  描述: |
    Configure the core architecture of this derivative.
    This value will be generated into vBrsCfg.h as
    BRS_CPU_CORE_x
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: vBaseEnvCpuInitCore
  长名称: ''
  描述: |
    Configure the core ID of the core, which should be used for general initialization.
    For normal, this is the boot core.
    This value will be generated into vBrsCfg.h as
    BRS_CPU_INIT_CORE
  默认值: ''
  最小值: 0
  最大值: 255
```

### 3. vBaseEnvAdditionalParameters

**描述**: Additional parameters for generation of additional defines, if necessary for the depending platform.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBaseEnvDerivativeGroup
  长名称: ''
  描述: Define the Derivative Group of this derivative
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vBaseEnvPllGroup
  长名称: ''
  描述: Configure the PLL Group of your derivative
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vBaseEnvClockGroup
  长名称: ''
  描述: Configure the Clock Group of your derivative
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vBaseEnvPortGroup
  长名称: ''
  描述: Configure the Port Group of your derivative
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vBaseEnvProtectionGroup
  长名称: ''
  描述: Configure the Protection Group of your derivative
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vBaseEnvResetGroup
  长名称: ''
  描述: Configure the Reset Group of your derivative
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vBaseEnvWatchdogGroup
  长名称: ''
  描述: Configure the Watchdog Group of your derivative
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vBaseEnvOpModeGroup
  长名称: ''
  描述: Configure the Operation Mode Group of your derivative
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vBaseEnvUserModeAccessGroup
  长名称: ''
  描述: Configure the User Mode Access Group of your derivative
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: vBaseEnvPowerDownModes
  长名称: ''
  描述: Configure, if Power Down Modes to be used for your derivative
  默认值: false
  最小值: ''
  最大值: ''
```

### 4. vBaseEnvMemLayoutHwRegion

**描述**: Container to structure the configuration parameters of hardware memory regions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBaseEnvHwRegionStartAddress
  长名称: Hardware Region Start Address
  描述: Start address of the hardware memory region.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vBaseEnvHwRegionSize
  长名称: Hardware Region Size
  描述: Size of the hardware memory region.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vBaseEnvHwRegionEccAlignment
  长名称: Hardware Region ECC Alignment
  描述: Required ECC Alignment of the hardware memory region.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vBaseEnvHwRegionType
  长名称: Hardware Region Type
  描述: |
    Type of the hardware memory region.
    This parameter is necessary for some linkers (e.g. Tasking), to distinguish between
    RAM/ROM/NVRAM.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. vBaseEnvMemLayoutHwRegion

**描述**: Container to structure the configuration parameters of hardware memory regions.

该容器没有参数。

### 6. vBaseEnvInterruptHandling

**描述**: Container for family specific default interrupt settings

该容器没有参数。

### 7. vBaseEnvCan

该容器没有参数。

### 8. vBaseEnvChannel

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBaseEnvIndex
  长名称: Channel Index
  描述: Logical channel
  默认值: ''
  最小值: 0
  最大值: ''
- 
  序号: 2
  名称: vBaseEnvIsrInterruptPriority
  长名称: Channel Priority
  描述: ''
  默认值: ''
  最小值: 0
  最大值: ''
- 
  序号: 3
  名称: vBaseEnvIsrInterruptSource
  长名称: Channel Source Number
  描述: ''
  默认值: ''
  最小值: 0
  最大值: ''
```

### 9. vBaseEnvLin

该容器没有参数。

### 10. vBaseEnvChannel

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBaseEnvIndex
  长名称: Channel Index
  描述: Logical channel
  默认值: ''
  最小值: 0
  最大值: ''
- 
  序号: 2
  名称: vBaseEnvIsrInterruptPriority
  长名称: Channel Priority
  描述: ''
  默认值: ''
  最小值: 0
  最大值: ''
- 
  序号: 3
  名称: vBaseEnvIsrInterruptSource
  长名称: Channel Source Number
  描述: ''
  默认值: ''
  最小值: 0
  最大值: ''
```

### 11. vBaseEnvFlexray

该容器没有参数。

### 12. vBaseEnvChannel

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBaseEnvIndex
  长名称: Channel Index
  描述: Logical channel
  默认值: ''
  最小值: 0
  最大值: ''
- 
  序号: 2
  名称: vBaseEnvIsrInterruptPriority
  长名称: Channel Priority
  描述: ''
  默认值: ''
  最小值: 0
  最大值: ''
- 
  序号: 3
  名称: vBaseEnvIsrInterruptSource
  长名称: Channel Source Number
  描述: ''
  默认值: ''
  最小值: 0
  最大值: ''
```

### 13. vBaseEnvEthernet

该容器没有参数。

### 14. vBaseEnvChannel

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBaseEnvIndex
  长名称: Channel Index
  描述: Logical channel
  默认值: ''
  最小值: 0
  最大值: ''
- 
  序号: 2
  名称: vBaseEnvIsrInterruptPriority
  长名称: Channel Priority
  描述: ''
  默认值: ''
  最小值: 0
  最大值: ''
- 
  序号: 3
  名称: vBaseEnvIsrInterruptSource
  长名称: Channel Source Number
  描述: ''
  默认值: ''
  最小值: 0
  最大值: ''
```

### 15. vBaseEnvPeripheralClocks

**描述**: Container for family specific default peripheral clock settings

该容器没有参数。

### 16. vBaseEnvCan

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBaseEnvCan_Clock
  长名称: Frequency of CAN peripheral clock
  描述: Default frequency, used for PLL calculation of CAN driver peripheral clock.
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

### 17. vBaseEnvLin

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBaseEnvLin_Clock
  长名称: Frequency of LIN peripheral clock
  描述: Default frequency, used for PLL calculation of LIN driver peripheral clock.
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

### 18. vBaseEnvFlexray

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBaseEnvFlexray_Clock
  长名称: Frequency of FlexRay peripheral clock
  描述: Default frequency, used for PLL calculation of FlexRay driver peripheral clock.
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

### 19. vBaseEnvEthernet

#### 参数列表

```yaml
- 
  序号: 1
  名称: vBaseEnvEthernet_Clock
  长名称: Frequency of EtherNet peripheral clock
  描述: Default frequency, used for PLL calculation of EtherNet driver peripheral clock.
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

