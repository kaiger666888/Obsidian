# Adc - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:04

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Adc](#adc)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Adc

#### 基本信息

- **UUID**: `ECUC:c03229fe-4dca-445e-a47c-1ae11e6c1832`
- **模块名称**: `Adc`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the Adc (Analog Digital Conversion) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **15** 个配置容器：

##### 1. AdcConfigSet

**容器属性**:

- **UUID**: `ECUC:fc6e0617-8c73-4b71-b09e-dfb10b76e50d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcConfigSet`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR Adc module.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. AdcSyncClockDisable

- **UUID**: `ECUC:e5c85e73-38e2-47ae-85e9-c39d1b361249`
- **参数名**: `AdcSyncClockDisable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines whether the analog clock is generated in synchronized/unsynchronized mode. The configuration of the Converter  Control (CONVCTRL) clock is done by the MCU driver

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. AdcSystemClock

- **UUID**: `ECUC:66c8e900-6197-56a3-8125-a695aa21788e`
- **引用名**: `AdcSystemClock`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePointConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePointConfig`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter refers to the system clock configured by the MCU driver. With this system clock, the reload value corresponding to the configured timer is calculated for the timer triggered ADC groups.

###### 配置容器

本模块包含 **9** 个配置容器：

####### 1. AdcGlobalInputClass

**容器属性**:

- **UUID**: `DCE:dcc39b88-cc3b-4358-ba87-30120722c6c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGlobalInputClass`
- **多重性**: [2..2]

**容器描述**:

This container defines the Global Input Class for A-D conversion

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. AdcChSampleTime

- **UUID**: `ECUC:ea7f906d-5d18-4bc4-808e-dc02c4c233ac`
- **参数名**: `AdcChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles.

########## 2. AdcEmuxChSampleTime

- **UUID**: `ECUC:0c679c6d-1e71-47e0-9381-6305a40ca8fd`
- **参数名**: `AdcEmuxChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles for EMUX conversions.

######### BOOLEAN 类型参数

########## 1. AdcChSESPSEnable

- **UUID**: `ECUC:6fe4295d-02b9-4f34-b9f2-337c2df6bd58`
- **参数名**: `AdcChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for Standard Conversions is enabled/disabled.

########## 2. AdcEmuxChSESPSEnable

- **UUID**: `ECUC:da1dc2b9-97dc-4c1a-82cf-6a66656f6246`
- **参数名**: `AdcEmuxChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for EMUX conversions is enabled/disabled.

######### ENUMERATION 类型参数

########## 1. AdcChPreChargeClkCycles

- **UUID**: `ECUC:7e0e69e5-6224-4364-a9b3-f0559f2409d6`
- **参数名**: `AdcChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for standard conversions.

########## 2. AdcChConvMode

- **UUID**: `ECUC:7e0e69e5-6004-5564-a9b3-f0559f2409d6`
- **参数名**: `AdcChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for Standard Conversions.

########## 3. AdcEmuxChPreChargeClkCycles

- **UUID**: `ECUC:4f520abb-60fd-4ea8-b02e-9bad6a36f264`
- **参数名**: `AdcEmuxChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for EMUX conversions.

########## 4. AdcEmuxChConvMode

- **UUID**: `ECUC:e266f886-48fd-4481-812f-1e8a7f22b218`
- **参数名**: `AdcEmuxChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for EMUX conversions.

####### 2. AdcHwUnit

**容器属性**:

- **UUID**: `ECUC:c67e7c58-3daf-455b-a213-95ae94b248d8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcHwUnit`
- **多重性**: [1..9]

**容器描述**:

This container contains the Driver configuration (parameters) depending on grouping of channels

######## 参数配置

此容器包含 **16** 个参数：

######### INTEGER 类型参数

########## 1. AdcAnalogClockSyncDelay

- **UUID**: `ECUC:482b876b-9787-4e46-875a-559b7a1427f2`
- **参数名**: `AdcAnalogClockSyncDelay`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines analog clock synchronization delay.

########## 2. AdcPrescale

- **UUID**: `ECUC:ea7f8f6d-5d98-4bc4-808e-dc02c4c233ac`
- **参数名**: `AdcPrescale`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [2..32]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the divider for generating the analog internal clock (fADCDI) from fADC.

######### BOOLEAN 类型参数

########## 1. AdcIdlePrechargeEnable

- **UUID**: `ECUC:6fe4295d-02b9-4f64-b9f2-33732df6bd58`
- **参数名**: `AdcIdlePrechargeEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines whether precharge of the sampling capacitor is enabled or not.

########## 2. AdcInputBufferEnable

- **UUID**: `ECUC:6fe4295d-02b5-4f64-b9f2-33732df6bd58`
- **参数名**: `AdcInputBufferEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines whether input buffering is enabled or not. If enabled buffering time is selected via AIPS(AdcChPreChargeClkCycles).

########## 3. AdcPostCalibrationDisable

- **UUID**: `ECUC:6fe42a5d-02b5-4f64-a9f2-33732df6bd58`
- **参数名**: `AdcPostCalibrationDisable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines whether the post calibration is enabled or disabled.

########## 4. AdcSampleSyncEnable

- **UUID**: `ECUC:6fe43a5d-02b5-4f64-a9f2-33732df6bd58`
- **参数名**: `AdcSampleSyncEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines whether the Adc Sample Time Synchronization is enabled or disabled.

########## 5. AdcMSBDoubleClkEnable

- **UUID**: `ECUC:6fe44a5d-02b5-4f65-a9f2-33732df6bd58`
- **参数名**: `AdcMSBDoubleClkEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the number of clock cycles for MSB conversions.

######### ENUMERATION 类型参数

########## 1. AdcClockSource

- **UUID**: `ECUC:08f7956c-d858-438f-9504-12df1ba10e73`
- **参数名**: `AdcClockSource`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_SYSTEM_CLK`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_SYSTEM_CLK` (来源: AUTOSAR_ECUC)
- **描述**: The ADC module specific clock input for the ADC. This parameter is not used for AURIX 2G. The clock source for the complete EVADC IP can be selected through node Adc/AdcSystemClock

########## 2. AdcHwUnitId

- **UUID**: `ECUC:7aa61340-e385-4037-b899-40ce3e595755`
- **参数名**: `AdcHwUnitId`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `HWUNIT_ADC0`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `HWUNIT_ADC0` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC1` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC2` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC3` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC4` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC8` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC9` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC10` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC11` (来源: AUTOSAR_ECUC)
- **描述**: Description: Numeric ID of the HW Unit. This symbolic name allows accessing Hw Unit data. Enumeration literals are defined vendor specific.

########## 3. AdcPrechargeReference

- **UUID**: `ECUC:7e0e69e5-1104-5164-a9b3-f0559f2409d6`
- **参数名**: `AdcPrechargeReference`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_VDD_VSM_USED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_VDD_VSM_USED` (来源: INFINEON_AURIX2G)
  - `ADC_VDD_VSM_NOT_USED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines whether VDDM/VSSM is used for pre-charging or not.

########## 4. AdcReferencePrechargePhases

- **UUID**: `ECUC:7e0e69d5-1104-5164-a9b3-f0559f2409d6`
- **参数名**: `AdcReferencePrechargePhases`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_PRECHARGE_PHASE_1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_PRECHARGE_PHASE_1` (来源: INFINEON_AURIX2G)
  - `ADC_PRECHARGE_PHASE_2` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the precharge clock phases for the reference input.

########## 5. AdcCalibrationSampleTime

- **UUID**: `ECUC:7e0e69d4-2104-5164-a9b3-f0559f2409d6`
- **参数名**: `AdcCalibrationSampleTime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_CAL_TIME_2_TIMES_TADCI`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_CAL_TIME_2_TIMES_TADCI` (来源: INFINEON_AURIX2G)
  - `ADC_CAL_TIME_4_TIMES_TADCI` (来源: INFINEON_AURIX2G)
  - `ADC_CAL_TIME_6_TIMES_TADCI` (来源: INFINEON_AURIX2G)
  - `ADC_CAL_TIME_8_TIMES_TADCI` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the calibration sample time.

########## 6. AdcRequestSource0ConvMode

- **UUID**: `ECUC:8a1e64d4-2114-5165-a9b3-f0559f2409d6`
- **参数名**: `AdcRequestSource0ConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_WAIT_FOR_START_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_WAIT_FOR_START_MODE` (来源: INFINEON_AURIX2G)
  - `ADC_CANCEL_INJECT_REPEAT_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines conversion start mode for a request source.

########## 7. AdcRequestSource1ConvMode

- **UUID**: `ECUC:8a0e64d4-2113-5165-a9b3-f0559f2409d6`
- **参数名**: `AdcRequestSource1ConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_WAIT_FOR_START_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_WAIT_FOR_START_MODE` (来源: INFINEON_AURIX2G)
  - `ADC_CANCEL_INJECT_REPEAT_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines conversion start mode for a request source.

########## 8. AdcRequestSource2ConvMode

- **UUID**: `ECUC:8a0e64d5-2114-5165-a9b3-f0559f2409d6`
- **参数名**: `AdcRequestSource2ConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_WAIT_FOR_START_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_WAIT_FOR_START_MODE` (来源: INFINEON_AURIX2G)
  - `ADC_CANCEL_INJECT_REPEAT_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines conversion start mode for a request source.

########## 9. AdcSyncConvMode

- **UUID**: `ECUC:7e0e69e5-6004-1956-a9b3-f0559f2409d6`
- **参数名**: `AdcSyncConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_STAND_ALONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_STAND_ALONE` (来源: INFINEON_AURIX2G)
  - `ADC_SYNC_MASTER` (来源: INFINEON_AURIX2G)
  - `ADC_SYNC_SLAVE` (来源: INFINEON_AURIX2G)
- **描述**: Determines whether the HW groups operates in Stand-Alone or Master/Slave Sync Mode.

######## 配置容器

本模块包含 **7** 个配置容器：

######### 1. AdcHwUnitInputClass

**容器属性**:

- **UUID**: `DCE:dcc39b88-cc3b-4358-b687-30120722c6c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcHwUnitInputClass`
- **多重性**: [2..2]

**容器描述**:

This container defines the Hw unit input class for A-D conversion

########## 参数配置

此容器包含 **8** 个参数：

########### INTEGER 类型参数

############ 1. AdcChSampleTime

- **UUID**: `ECUC:ea7f9f3d-5d18-4bc4-808e-dc02c4c233ac`
- **参数名**: `AdcChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles.

############ 2. AdcEmuxChSampleTime

- **UUID**: `ECUC:2d556c2f-44db-4727-9de1-02b26fccba7a`
- **参数名**: `AdcEmuxChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles for EMUX conversions.

########### BOOLEAN 类型参数

############ 1. AdcChSESPSEnable

- **UUID**: `ECUC:6fe4295d-02b9-4f34-b9f2-337c2df6bd28`
- **参数名**: `AdcChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for Standard Conversions is enabled/disabled.

############ 2. AdcEmuxChSESPSEnable

- **UUID**: `ECUC:d5d1eacd-09a8-41f6-bb66-7fd06e4af3b8`
- **参数名**: `AdcEmuxChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for EMUX conversions is enabled/disabled.

########### ENUMERATION 类型参数

############ 1. AdcChPreChargeClkCycles

- **UUID**: `ECUC:7e0e6955-6004-4364-a9b3-f0559f2409d6`
- **参数名**: `AdcChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for standard conversions.

############ 2. AdcChConvMode

- **UUID**: `ECUC:7e0e69e5-6004-5564-a1b3-f0559f2409d6`
- **参数名**: `AdcChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for Standard Conversions.

############ 3. AdcEmuxChPreChargeClkCycles

- **UUID**: `ECUC:f6735f9d-b34e-471c-8b46-05f48c8438ef`
- **参数名**: `AdcEmuxChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for EMUX conversions.

############ 4. AdcEmuxChConvMode

- **UUID**: `ECUC:d7ad1fc7-868e-4a04-a63b-65e44411a564`
- **参数名**: `AdcEmuxChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for EMUX conversions.

######### 2. AdcChannel

**容器属性**:

- **UUID**: `ECUC:bfd7d43b-017d-4755-9a41-2bf12e38403d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcChannel`
- **多重性**: [1..255]

**容器描述**:

This container contains the channel configuration (parameters) depending on the hardware capability. This value will be assigned to the symbolic name derived of the AdcChannel container short name. Channel ID 0xFF is considered as invalid

########## 参数配置

此容器包含 **20** 个参数：

########### INTEGER 类型参数

############ 1. AdcChannelConvTime

- **UUID**: `ECUC:cda3fa6e-3f00-43a3-a05e-5c97744e6aaf`
- **参数名**: `AdcChannelConvTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of conversion time, i.e. the time during which the analogue value is converted into digital representation, (in clock cycles) for each channel, if supported by hardware.

############ 2. AdcChannelHighLimit

- **UUID**: `ECUC:65b39edf-db50-479b-becd-268512557336`
- **参数名**: `AdcChannelHighLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4095`
- **取值范围**: [0..4095]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: High limit - used for limit checking.

############ 3. AdcChannelId

- **UUID**: `ECUC:482b876b-1787-4e46-875a-559b7a1427f2`
- **参数名**: `AdcChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the assignment of the channel to the physical ADC  hardware channel.

############ 4. AdcChannelLowLimit

- **UUID**: `ECUC:bd3f78a2-2b94-419a-961c-5ad47f5a8bcb`
- **参数名**: `AdcChannelLowLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4095]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Low limit - used for limit checking.

############ 5. AdcChannelResolution

- **UUID**: `ECUC:c05e44f5-f418-4772-9ed3-ba767591baf1`
- **参数名**: `AdcChannelResolution`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `12`
- **取值范围**: [1..63]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Channel resolution in bits.

############ 6. AdcChannelSampTime

- **UUID**: `ECUC:d11259ac-99d0-488f-9cc6-a66170fbb368`
- **参数名**: `AdcChannelSampTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of sampling time, i.e. the time during which the value is sampled, (in clock cycles) for each channel, if supported by hardware.

########### BOOLEAN 类型参数

############ 1. AdcChannelLimitCheck

- **UUID**: `ECUC:6c8938e0-f362-4cdc-8711-6d4b429215b3`
- **参数名**: `AdcChannelLimitCheck`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables or disables limit checking for an ADC channel.

############ 2. AdcSyncConvChannelEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b17`
- **参数名**: `AdcSyncConvChannelEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables the synchronous conversion for this channel.Conversion of this channel will trigger conversion for the same analog channel number on slave HW groups also.

############ 3. AdcBWDEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b18`
- **参数名**: `AdcBWDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the broken wire detection feature for the channel.

############ 4. AdcPullDownDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec203fb5b18`
- **参数名**: `AdcPullDownDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Pull Down diagnostics feature for the channel.

############ 5. AdcMultiplexerDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec203fb5018`
- **参数名**: `AdcMultiplexerDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Multiplexer diagnostics feature for the channel.

############ 6. AdcConverterDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec220fb5b18`
- **参数名**: `AdcConverterDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Converter diagnostics feature for the channel.

########### ENUMERATION 类型参数

############ 1. AdcChannelRangeSelect

- **UUID**: `ECUC:8b1c1853-c817-448a-982b-cb15f700c87d`
- **参数名**: `AdcChannelRangeSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_RANGE_ALWAYS`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_RANGE_ALWAYS` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_UNDER_LOW` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_UNDER_LOW` (来源: AUTOSAR_ECUC)
- **描述**: In case of active limit checking: defines which conversion values are taken into account related to the boarders defined with AdcChannelLowLimit and AdcChannelHighLimit.

############ 2. AdcChannelRefVoltsrcHigh

- **UUID**: `ECUC:94395609-bae2-465a-9878-df86ada9bffb`
- **参数名**: `AdcChannelRefVoltsrcHigh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_USES_VREF`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_USES_VREF` (来源: AUTOSAR_ECUC)
  - `ADC_USES_CH0` (来源: AUTOSAR_ECUC)
- **描述**: Upper reference voltage source for each channel.

############ 3. AdcChannelRefVoltsrcLow

- **UUID**: `ECUC:582225d2-20d0-47eb-a3c1-f387a68cb7c4`
- **参数名**: `AdcChannelRefVoltsrcLow`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_USES_VAGND`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_USES_VAGND` (来源: AUTOSAR_ECUC)
- **描述**: Lower reference voltage source for each channel.

############ 4. AdcAnChannelNum

- **UUID**: `55b16180-ed10-4e98-a14d-f205643c08a0`
- **参数名**: `AdcAnChannelNum`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `G0CH0`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `G0CH0` (来源: INFINEON_AURIX2G)
  - `G0CH1` (来源: INFINEON_AURIX2G)
  - `G0CH2` (来源: INFINEON_AURIX2G)
  - `G0CH3` (来源: INFINEON_AURIX2G)
  - `G0CH4` (来源: INFINEON_AURIX2G)
  - `G0CH5` (来源: INFINEON_AURIX2G)
  - `G0CH6` (来源: INFINEON_AURIX2G)
  - `G0CH7` (来源: INFINEON_AURIX2G)
  - `G1CH0` (来源: INFINEON_AURIX2G)
  - `G1CH1` (来源: INFINEON_AURIX2G)
  - `G1CH2` (来源: INFINEON_AURIX2G)
  - `G1CH3` (来源: INFINEON_AURIX2G)
  - `G1CH4` (来源: INFINEON_AURIX2G)
  - `G1CH5` (来源: INFINEON_AURIX2G)
  - `G1CH6` (来源: INFINEON_AURIX2G)
  - `G1CH7` (来源: INFINEON_AURIX2G)
  - `G2CH0` (来源: INFINEON_AURIX2G)
  - `G2CH1` (来源: INFINEON_AURIX2G)
  - `G2CH2` (来源: INFINEON_AURIX2G)
  - `G2CH3` (来源: INFINEON_AURIX2G)
  - `G2CH4` (来源: INFINEON_AURIX2G)
  - `G2CH5` (来源: INFINEON_AURIX2G)
  - `G2CH6` (来源: INFINEON_AURIX2G)
  - `G2CH7` (来源: INFINEON_AURIX2G)
  - `G3CH0` (来源: INFINEON_AURIX2G)
  - `G3CH1` (来源: INFINEON_AURIX2G)
  - `G3CH2` (来源: INFINEON_AURIX2G)
  - `G3CH3` (来源: INFINEON_AURIX2G)
  - `G3CH4` (来源: INFINEON_AURIX2G)
  - `G3CH5` (来源: INFINEON_AURIX2G)
  - `G3CH6` (来源: INFINEON_AURIX2G)
  - `G3CH7` (来源: INFINEON_AURIX2G)
  - `G4CH0` (来源: INFINEON_AURIX2G)
  - `G4CH1` (来源: INFINEON_AURIX2G)
  - `G4CH2` (来源: INFINEON_AURIX2G)
  - `G4CH3` (来源: INFINEON_AURIX2G)
  - `G4CH4` (来源: INFINEON_AURIX2G)
  - `G4CH5` (来源: INFINEON_AURIX2G)
  - `G4CH6` (来源: INFINEON_AURIX2G)
  - `G4CH7` (来源: INFINEON_AURIX2G)
  - `G8CH0` (来源: INFINEON_AURIX2G)
  - `G8CH1` (来源: INFINEON_AURIX2G)
  - `G8CH2` (来源: INFINEON_AURIX2G)
  - `G8CH3` (来源: INFINEON_AURIX2G)
  - `G8CH4` (来源: INFINEON_AURIX2G)
  - `G8CH5` (来源: INFINEON_AURIX2G)
  - `G8CH6` (来源: INFINEON_AURIX2G)
  - `G8CH7` (来源: INFINEON_AURIX2G)
  - `G8CH8` (来源: INFINEON_AURIX2G)
  - `G8CH9` (来源: INFINEON_AURIX2G)
  - `G8CH10` (来源: INFINEON_AURIX2G)
  - `G8CH11` (来源: INFINEON_AURIX2G)
  - `G8CH12` (来源: INFINEON_AURIX2G)
  - `G8CH13` (来源: INFINEON_AURIX2G)
  - `G8CH14` (来源: INFINEON_AURIX2G)
  - `G8CH15` (来源: INFINEON_AURIX2G)
  - `G9CH0` (来源: INFINEON_AURIX2G)
  - `G9CH1` (来源: INFINEON_AURIX2G)
  - `G9CH2` (来源: INFINEON_AURIX2G)
  - `G9CH3` (来源: INFINEON_AURIX2G)
  - `G9CH4` (来源: INFINEON_AURIX2G)
  - `G9CH5` (来源: INFINEON_AURIX2G)
  - `G9CH6` (来源: INFINEON_AURIX2G)
  - `G9CH7` (来源: INFINEON_AURIX2G)
  - `G9CH8` (来源: INFINEON_AURIX2G)
  - `G9CH9` (来源: INFINEON_AURIX2G)
  - `G9CH10` (来源: INFINEON_AURIX2G)
  - `G9CH11` (来源: INFINEON_AURIX2G)
  - `G9CH12` (来源: INFINEON_AURIX2G)
  - `G9CH13` (来源: INFINEON_AURIX2G)
  - `G9CH14` (来源: INFINEON_AURIX2G)
  - `G9CH15` (来源: INFINEON_AURIX2G)
  - `G10CH0` (来源: INFINEON_AURIX2G)
  - `G10CH1` (来源: INFINEON_AURIX2G)
  - `G10CH2` (来源: INFINEON_AURIX2G)
  - `G10CH3` (来源: INFINEON_AURIX2G)
  - `G10CH4` (来源: INFINEON_AURIX2G)
  - `G10CH5` (来源: INFINEON_AURIX2G)
  - `G10CH6` (来源: INFINEON_AURIX2G)
  - `G10CH7` (来源: INFINEON_AURIX2G)
  - `G10CH8` (来源: INFINEON_AURIX2G)
  - `G10CH9` (来源: INFINEON_AURIX2G)
  - `G10CH10` (来源: INFINEON_AURIX2G)
  - `G10CH11` (来源: INFINEON_AURIX2G)
  - `G11CH0` (来源: INFINEON_AURIX2G)
  - `G11CH1` (来源: INFINEON_AURIX2G)
  - `G11CH2` (来源: INFINEON_AURIX2G)
  - `G11CH3` (来源: INFINEON_AURIX2G)
  - `G11CH4` (来源: INFINEON_AURIX2G)
  - `G11CH5` (来源: INFINEON_AURIX2G)
  - `G11CH6` (来源: INFINEON_AURIX2G)
  - `G11CH7` (来源: INFINEON_AURIX2G)
  - `G11CH8` (来源: INFINEON_AURIX2G)
  - `G11CH9` (来源: INFINEON_AURIX2G)
  - `G11CH10` (来源: INFINEON_AURIX2G)
  - `G11CH11` (来源: INFINEON_AURIX2G)
  - `G11CH12` (来源: INFINEON_AURIX2G)
  - `G11CH13` (来源: INFINEON_AURIX2G)
  - `G11CH14` (来源: INFINEON_AURIX2G)
  - `G11CH15` (来源: INFINEON_AURIX2G)
- **描述**: Analog Input Channel Number.There are upto 8 analog inputs for each Primary Kernel and upto 16 analog inputs for each Secondary Kernel.

############ 5. AdcInputClassSelection

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2409d6`
- **参数名**: `AdcInputClassSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_HWUNIT_CLASS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_HWUNIT_CLASS_0` (来源: INFINEON_AURIX2G)
  - `ADC_HWUNIT_CLASS_1` (来源: INFINEON_AURIX2G)
  - `ADC_GLOBAL_CLASS_0` (来源: INFINEON_AURIX2G)
  - `ADC_GLOBAL_CLASS_1` (来源: INFINEON_AURIX2G)
- **描述**: defines the input class for the analog channel. Input class determines the channel conversion properties like sample time and data conversion mode for each channel.

############ 6. AdcBWDPrechargeLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2409d7`
- **参数名**: `AdcBWDPrechargeLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_BWD_PRECH_VAGND`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_BWD_PRECH_VAGND` (来源: INFINEON_AURIX2G)
  - `ADC_BWD_PRECH_VAREF` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the VAREF/VAGND pre-charging for the broken wire detection channel.

############ 7. AdcMultiplexerDiagnosticLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0550f2409d7`
- **参数名**: `AdcMultiplexerDiagnosticLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_MD_PULL_DOWN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_MD_PULL_DOWN` (来源: INFINEON_AURIX2G)
  - `ADC_MD_PULL_UP` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the Multiplexer diagnostics level for the channel.

############ 8. AdcConverterDiagnosticsLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2009d7`
- **参数名**: `AdcConverterDiagnosticsLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_CD_PULL_DEVICE_VDDM`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_CD_PULL_DEVICE_VDDM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_VSSM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_HALF_VDDM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_TWOTHIRD_VDDM` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the Converter diagnostics level for the channel.

######### 3. AdcGroup

**容器属性**:

- **UUID**: `ECUC:21b450f5-989b-4095-a451-d237d777751c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGroup`
- **多重性**: [1..32]

**容器描述**:

This container contains the Group configuration (parameters).

########## 参数配置

此容器包含 **19** 个参数：

########### INTEGER 类型参数

############ 1. AdcGroupId

- **UUID**: `ECUC:65e3660c-73a4-4172-8d28-4edb71e96153`
- **参数名**: `AdcGroupId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..383]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Numeric Id of the ADC channel group.  This value will be assigned to the symbolic name derived of the AdcGroup containers short name. The range of IDs for each ADC Hw Unit:
                                    ADC0: 0 to 31, ADC1: 32 to 63, ADC2: 64 to 95, ADC3: 96 to 127, ADC4: 128 to 159, ADC5: 160 to 191, ADC6: 192 to 223, ADC7: 224 to 255, ADC8: 256 to 287
                                    ADC9: 288 to 319, ADC10: 320 to 351, ADC11: 352 to 383
                                  Recommendation  : Use AUTO-CALCULATE-VALUE option for all nodes AdcGroupId

############ 2. AdcGroupPriority

- **UUID**: `ECUC:c3c0273d-3fbb-48ea-b64a-6c6592d6a05c`
- **参数名**: `AdcGroupPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Priority level of the AdcGroup.

############ 3. AdcHwTrigTimer

- **UUID**: `ECUC:ac85f536-5cf6-43f3-a6a7-d824eed38461`
- **参数名**: `AdcHwTrigTimer`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..1023]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Reload value of the ADC module embedded timer (only if supported by ADC hardware).

############ 4. AdcStreamingNumSamples

- **UUID**: `ECUC:ba5e660f-1505-40bb-9b17-7ce8a5655235`
- **参数名**: `AdcStreamingNumSamples`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of ADC values to be acquired per channel in streaming access mode.

############ 5. AdcChannel0Alias

- **UUID**: `ECUC:8ea93903-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcChannel0Alias`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter configures the alias channel to be used for Channel 0.

############ 6. AdcChannel1Alias

- **UUID**: `ECUC:8ea93913-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcChannel1Alias`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter configures the alias channel to be used for Channel 1.

############ 7. AdcEmuxStartSelection

- **UUID**: `ECUC:bb7a337b-c160-470a-8b8f-bc8bd4b16a7b`
- **参数名**: `AdcEmuxStartSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the EMUX start selection.

############ 8. AdcResRegDefinition

- **UUID**: `ECUC:ea7f8f6d-5d98-4bc4-321e-dc02c4c233fc`
- **参数名**: `AdcResRegDefinition`
- **数据类型**: INTEGER
- **多重性**: [1..16]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the result register used for storing the result of this particular ADC conversion. This value of this parameter should be in descending order for the nodes of AdcGroupDefinition.

########### BOOLEAN 类型参数

############ 1. AdcEmuxChGroup

- **UUID**: `ECUC:29e7f838-395d-461f-9e5d-541c0cb3d670`
- **参数名**: `AdcEmuxChGroup`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Group is EMUX or not.

########### ENUMERATION 类型参数

############ 1. AdcGroupAccessMode

- **UUID**: `ECUC:faad1eb6-43b4-4195-bacc-6245556acb07`
- **参数名**: `AdcGroupAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_ACCESS_MODE_SINGLE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_ACCESS_MODE_SINGLE` (来源: AUTOSAR_ECUC)
  - `ADC_ACCESS_MODE_STREAMING` (来源: AUTOSAR_ECUC)
- **描述**: Type of access mode to group conversion results.

############ 2. AdcGroupConversionMode

- **UUID**: `ECUC:25721d0a-d8a7-4ea3-96ab-49ced3030fce`
- **参数名**: `AdcGroupConversionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_CONV_MODE_ONESHOT`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_CONV_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `ADC_CONV_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **描述**: Type of conversion mode supported by the driver.

############ 3. AdcGroupReplacement

- **UUID**: `ECUC:f348b1d0-aabc-46ee-a71a-02cc6e49dca6`
- **参数名**: `AdcGroupReplacement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GROUP_REPL_ABORT_RESTART`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_GROUP_REPL_ABORT_RESTART` (来源: AUTOSAR_ECUC)
  - `ADC_GROUP_REPL_SUSPEND_RESUME` (来源: AUTOSAR_ECUC)
- **描述**: Replacement mechanism, which is used on ADC group level, if a group conversion is interrupted by a group which has a higher priority.

############ 4. AdcGroupTriggSrc

- **UUID**: `ECUC:1fb3e310-c03a-4a29-b2d2-f8d71765c6fc`
- **参数名**: `AdcGroupTriggSrc`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_TRIGG_SRC_SW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_TRIGG_SRC_HW` (来源: AUTOSAR_ECUC)
  - `ADC_TRIGG_SRC_SW` (来源: AUTOSAR_ECUC)
- **描述**: Type of source event that starts a group conversion.

############ 5. AdcHwTrigSignal

- **UUID**: `ECUC:70c09b6d-3cac-4db1-bee8-aafef6b9d2cf`
- **参数名**: `AdcHwTrigSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_HW_TRIG_RISING_EDGE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_HW_TRIG_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **描述**: Configures on which edge of the hardware trigger signal the driver should react, i.e. start the conversion (only if supported by the ADC hardware).

############ 6. AdcStreamingBufferMode

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf2-d2575ef9e9c8`
- **参数名**: `AdcStreamingBufferMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_STREAM_BUFFER_LINEAR`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_STREAM_BUFFER_CIRCULAR` (来源: AUTOSAR_ECUC)
  - `ADC_STREAM_BUFFER_LINEAR` (来源: AUTOSAR_ECUC)
- **描述**: Configure streaming buffer as "linear buffer" (i.e. the ADC Driver stops the conversion as soon as the stream buffer is full) or as "ring buffer" (wraps around if the end of the stream buffer is reached).

############ 7. AdcHwExtTrigSelect

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-2af2-d2575ef9e9c8`
- **参数名**: `AdcHwExtTrigSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_TRIG_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_TRIG_NONE` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_0_GxREQTRA_CCU60_SR3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_1_GxREQTRB_CCU61_SR3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_2_GxREQTRC_HSPDM` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_3_GxREQTRD_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_4_GxREQTRE_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_5_GxREQTRF_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_6_GxREQTRG_GTM_ADCx_TRIG4` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_7_GxREQTRH_ERUIOUTx` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_8_GxREQTRI_GTM_ADCx_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_9_GxREQTRJ_GTM_ADCx_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_10_GxREQTRK_GTM_ADCx_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_11_GxREQTRL_GTM_ADCx_TRIG3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_12_GxREQTRM_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_13_GxREQTRN_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_14_GxREQTRO_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_15_GxREQTRP_GxREQGTySEL` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW trigger source for the group.

############ 8. AdcHwExtGateSelect

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcHwExtGateSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GATE_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_GATE_NONE` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_0_GxREQGTA_GTM_ADCx_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_1_GxREQGTB_GTM_ADCx_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_2_GxREQGTC_CCU6061_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_3_GxREQGTD_CCU6061_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_4_GxREQGTE_CCU6061_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_5_GxREQGTF_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_6_GxREQGTG_GTM_ADCx_TRIG4` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_7_GxREQGTH_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_8_GxREQGTI_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_9_GxREQGTJ_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_10_GxREQGTK_GTM_ADCx_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_11_GxREQGTL_GTM_ADCx_TRIG3` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_12_GxREQGTM_ERUPDOUTx` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_13_GxREQGTN_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_14_GxREQGTO_UNUSED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW gating source for the group.

############ 9. AdcHwGateSignal

- **UUID**: `ECUC:8ea9390c-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcHwGateSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GATE_LVL_HIGH`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_GATE_LVL_HIGH` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_LVL_LOW` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW gating signal level.

########### FUNCTION-NAME 类型参数

############ 1. AdcNotification

- **UUID**: `ECUC:f43bffda-8d3a-4520-b424-b558fcbe752c`
- **参数名**: `AdcNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `IoHwAb_AdcNotification0`
- **描述**: Callback function for each group

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. AdcGroupDefinition

- **UUID**: `ECUC:fc412877-d8ab-4b65-96e8-0498ac13762e`
- **引用名**: `AdcGroupDefinition`
- **引用类型**: REFERENCE
- **多重性**: [1..16]
- **目标**: `AdcChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit/AdcChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Assignment of AdcChannels to a AdcGroups.

########## 配置容器

本模块包含 **4** 个配置容器：

########### 1. EruTriggerConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruTriggerConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

############ 参数配置

此容器包含 **1** 个参数：

############# ENUMERATION 类型参数

############## 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e69e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

############## 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e900-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

########### 2. EruGatingConfig

**容器属性**:

- **UUID**: `83452075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruGatingConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU Gating

############ 参数配置

此容器包含 **1** 个参数：

############# ENUMERATION 类型参数

############## 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e39e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e911-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

############## 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e780-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

########### 3. GtmTriggerTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTriggerTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for TRIGGER. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb114e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

############## 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e0aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

############# ENUMERATION 类型参数

############## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l6b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

########### 4. GtmGatingTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2213a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmGatingTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for GATING. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb664e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

############## 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e1aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

############# ENUMERATION 类型参数

############## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-1db7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3685`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

######### 4. EruTriggerConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruTriggerConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e69e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

############ 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e900-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

######### 5. EruGatingConfig

**容器属性**:

- **UUID**: `83452075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruGatingConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU Gating

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e39e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e911-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

############ 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e780-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

######### 6. GtmTriggerTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTriggerTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for TRIGGER. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb114e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

############ 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e0aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

########### ENUMERATION 类型参数

############ 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l6b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

######### 7. GtmGatingTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2213a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmGatingTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for GATING. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb664e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

############ 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e1aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

########### ENUMERATION 类型参数

############ 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-1db7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3685`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 3. AdcHwUnitInputClass

**容器属性**:

- **UUID**: `DCE:dcc39b88-cc3b-4358-b687-30120722c6c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcHwUnitInputClass`
- **多重性**: [2..2]

**容器描述**:

This container defines the Hw unit input class for A-D conversion

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. AdcChSampleTime

- **UUID**: `ECUC:ea7f9f3d-5d18-4bc4-808e-dc02c4c233ac`
- **参数名**: `AdcChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles.

########## 2. AdcEmuxChSampleTime

- **UUID**: `ECUC:2d556c2f-44db-4727-9de1-02b26fccba7a`
- **参数名**: `AdcEmuxChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles for EMUX conversions.

######### BOOLEAN 类型参数

########## 1. AdcChSESPSEnable

- **UUID**: `ECUC:6fe4295d-02b9-4f34-b9f2-337c2df6bd28`
- **参数名**: `AdcChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for Standard Conversions is enabled/disabled.

########## 2. AdcEmuxChSESPSEnable

- **UUID**: `ECUC:d5d1eacd-09a8-41f6-bb66-7fd06e4af3b8`
- **参数名**: `AdcEmuxChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for EMUX conversions is enabled/disabled.

######### ENUMERATION 类型参数

########## 1. AdcChPreChargeClkCycles

- **UUID**: `ECUC:7e0e6955-6004-4364-a9b3-f0559f2409d6`
- **参数名**: `AdcChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for standard conversions.

########## 2. AdcChConvMode

- **UUID**: `ECUC:7e0e69e5-6004-5564-a1b3-f0559f2409d6`
- **参数名**: `AdcChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for Standard Conversions.

########## 3. AdcEmuxChPreChargeClkCycles

- **UUID**: `ECUC:f6735f9d-b34e-471c-8b46-05f48c8438ef`
- **参数名**: `AdcEmuxChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for EMUX conversions.

########## 4. AdcEmuxChConvMode

- **UUID**: `ECUC:d7ad1fc7-868e-4a04-a63b-65e44411a564`
- **参数名**: `AdcEmuxChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for EMUX conversions.

####### 4. AdcChannel

**容器属性**:

- **UUID**: `ECUC:bfd7d43b-017d-4755-9a41-2bf12e38403d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcChannel`
- **多重性**: [1..255]

**容器描述**:

This container contains the channel configuration (parameters) depending on the hardware capability. This value will be assigned to the symbolic name derived of the AdcChannel container short name. Channel ID 0xFF is considered as invalid

######## 参数配置

此容器包含 **20** 个参数：

######### INTEGER 类型参数

########## 1. AdcChannelConvTime

- **UUID**: `ECUC:cda3fa6e-3f00-43a3-a05e-5c97744e6aaf`
- **参数名**: `AdcChannelConvTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of conversion time, i.e. the time during which the analogue value is converted into digital representation, (in clock cycles) for each channel, if supported by hardware.

########## 2. AdcChannelHighLimit

- **UUID**: `ECUC:65b39edf-db50-479b-becd-268512557336`
- **参数名**: `AdcChannelHighLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4095`
- **取值范围**: [0..4095]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: High limit - used for limit checking.

########## 3. AdcChannelId

- **UUID**: `ECUC:482b876b-1787-4e46-875a-559b7a1427f2`
- **参数名**: `AdcChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the assignment of the channel to the physical ADC  hardware channel.

########## 4. AdcChannelLowLimit

- **UUID**: `ECUC:bd3f78a2-2b94-419a-961c-5ad47f5a8bcb`
- **参数名**: `AdcChannelLowLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4095]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Low limit - used for limit checking.

########## 5. AdcChannelResolution

- **UUID**: `ECUC:c05e44f5-f418-4772-9ed3-ba767591baf1`
- **参数名**: `AdcChannelResolution`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `12`
- **取值范围**: [1..63]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Channel resolution in bits.

########## 6. AdcChannelSampTime

- **UUID**: `ECUC:d11259ac-99d0-488f-9cc6-a66170fbb368`
- **参数名**: `AdcChannelSampTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of sampling time, i.e. the time during which the value is sampled, (in clock cycles) for each channel, if supported by hardware.

######### BOOLEAN 类型参数

########## 1. AdcChannelLimitCheck

- **UUID**: `ECUC:6c8938e0-f362-4cdc-8711-6d4b429215b3`
- **参数名**: `AdcChannelLimitCheck`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables or disables limit checking for an ADC channel.

########## 2. AdcSyncConvChannelEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b17`
- **参数名**: `AdcSyncConvChannelEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables the synchronous conversion for this channel.Conversion of this channel will trigger conversion for the same analog channel number on slave HW groups also.

########## 3. AdcBWDEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b18`
- **参数名**: `AdcBWDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the broken wire detection feature for the channel.

########## 4. AdcPullDownDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec203fb5b18`
- **参数名**: `AdcPullDownDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Pull Down diagnostics feature for the channel.

########## 5. AdcMultiplexerDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec203fb5018`
- **参数名**: `AdcMultiplexerDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Multiplexer diagnostics feature for the channel.

########## 6. AdcConverterDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec220fb5b18`
- **参数名**: `AdcConverterDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Converter diagnostics feature for the channel.

######### ENUMERATION 类型参数

########## 1. AdcChannelRangeSelect

- **UUID**: `ECUC:8b1c1853-c817-448a-982b-cb15f700c87d`
- **参数名**: `AdcChannelRangeSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_RANGE_ALWAYS`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_RANGE_ALWAYS` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_UNDER_LOW` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_UNDER_LOW` (来源: AUTOSAR_ECUC)
- **描述**: In case of active limit checking: defines which conversion values are taken into account related to the boarders defined with AdcChannelLowLimit and AdcChannelHighLimit.

########## 2. AdcChannelRefVoltsrcHigh

- **UUID**: `ECUC:94395609-bae2-465a-9878-df86ada9bffb`
- **参数名**: `AdcChannelRefVoltsrcHigh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_USES_VREF`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_USES_VREF` (来源: AUTOSAR_ECUC)
  - `ADC_USES_CH0` (来源: AUTOSAR_ECUC)
- **描述**: Upper reference voltage source for each channel.

########## 3. AdcChannelRefVoltsrcLow

- **UUID**: `ECUC:582225d2-20d0-47eb-a3c1-f387a68cb7c4`
- **参数名**: `AdcChannelRefVoltsrcLow`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_USES_VAGND`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_USES_VAGND` (来源: AUTOSAR_ECUC)
- **描述**: Lower reference voltage source for each channel.

########## 4. AdcAnChannelNum

- **UUID**: `55b16180-ed10-4e98-a14d-f205643c08a0`
- **参数名**: `AdcAnChannelNum`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `G0CH0`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `G0CH0` (来源: INFINEON_AURIX2G)
  - `G0CH1` (来源: INFINEON_AURIX2G)
  - `G0CH2` (来源: INFINEON_AURIX2G)
  - `G0CH3` (来源: INFINEON_AURIX2G)
  - `G0CH4` (来源: INFINEON_AURIX2G)
  - `G0CH5` (来源: INFINEON_AURIX2G)
  - `G0CH6` (来源: INFINEON_AURIX2G)
  - `G0CH7` (来源: INFINEON_AURIX2G)
  - `G1CH0` (来源: INFINEON_AURIX2G)
  - `G1CH1` (来源: INFINEON_AURIX2G)
  - `G1CH2` (来源: INFINEON_AURIX2G)
  - `G1CH3` (来源: INFINEON_AURIX2G)
  - `G1CH4` (来源: INFINEON_AURIX2G)
  - `G1CH5` (来源: INFINEON_AURIX2G)
  - `G1CH6` (来源: INFINEON_AURIX2G)
  - `G1CH7` (来源: INFINEON_AURIX2G)
  - `G2CH0` (来源: INFINEON_AURIX2G)
  - `G2CH1` (来源: INFINEON_AURIX2G)
  - `G2CH2` (来源: INFINEON_AURIX2G)
  - `G2CH3` (来源: INFINEON_AURIX2G)
  - `G2CH4` (来源: INFINEON_AURIX2G)
  - `G2CH5` (来源: INFINEON_AURIX2G)
  - `G2CH6` (来源: INFINEON_AURIX2G)
  - `G2CH7` (来源: INFINEON_AURIX2G)
  - `G3CH0` (来源: INFINEON_AURIX2G)
  - `G3CH1` (来源: INFINEON_AURIX2G)
  - `G3CH2` (来源: INFINEON_AURIX2G)
  - `G3CH3` (来源: INFINEON_AURIX2G)
  - `G3CH4` (来源: INFINEON_AURIX2G)
  - `G3CH5` (来源: INFINEON_AURIX2G)
  - `G3CH6` (来源: INFINEON_AURIX2G)
  - `G3CH7` (来源: INFINEON_AURIX2G)
  - `G4CH0` (来源: INFINEON_AURIX2G)
  - `G4CH1` (来源: INFINEON_AURIX2G)
  - `G4CH2` (来源: INFINEON_AURIX2G)
  - `G4CH3` (来源: INFINEON_AURIX2G)
  - `G4CH4` (来源: INFINEON_AURIX2G)
  - `G4CH5` (来源: INFINEON_AURIX2G)
  - `G4CH6` (来源: INFINEON_AURIX2G)
  - `G4CH7` (来源: INFINEON_AURIX2G)
  - `G8CH0` (来源: INFINEON_AURIX2G)
  - `G8CH1` (来源: INFINEON_AURIX2G)
  - `G8CH2` (来源: INFINEON_AURIX2G)
  - `G8CH3` (来源: INFINEON_AURIX2G)
  - `G8CH4` (来源: INFINEON_AURIX2G)
  - `G8CH5` (来源: INFINEON_AURIX2G)
  - `G8CH6` (来源: INFINEON_AURIX2G)
  - `G8CH7` (来源: INFINEON_AURIX2G)
  - `G8CH8` (来源: INFINEON_AURIX2G)
  - `G8CH9` (来源: INFINEON_AURIX2G)
  - `G8CH10` (来源: INFINEON_AURIX2G)
  - `G8CH11` (来源: INFINEON_AURIX2G)
  - `G8CH12` (来源: INFINEON_AURIX2G)
  - `G8CH13` (来源: INFINEON_AURIX2G)
  - `G8CH14` (来源: INFINEON_AURIX2G)
  - `G8CH15` (来源: INFINEON_AURIX2G)
  - `G9CH0` (来源: INFINEON_AURIX2G)
  - `G9CH1` (来源: INFINEON_AURIX2G)
  - `G9CH2` (来源: INFINEON_AURIX2G)
  - `G9CH3` (来源: INFINEON_AURIX2G)
  - `G9CH4` (来源: INFINEON_AURIX2G)
  - `G9CH5` (来源: INFINEON_AURIX2G)
  - `G9CH6` (来源: INFINEON_AURIX2G)
  - `G9CH7` (来源: INFINEON_AURIX2G)
  - `G9CH8` (来源: INFINEON_AURIX2G)
  - `G9CH9` (来源: INFINEON_AURIX2G)
  - `G9CH10` (来源: INFINEON_AURIX2G)
  - `G9CH11` (来源: INFINEON_AURIX2G)
  - `G9CH12` (来源: INFINEON_AURIX2G)
  - `G9CH13` (来源: INFINEON_AURIX2G)
  - `G9CH14` (来源: INFINEON_AURIX2G)
  - `G9CH15` (来源: INFINEON_AURIX2G)
  - `G10CH0` (来源: INFINEON_AURIX2G)
  - `G10CH1` (来源: INFINEON_AURIX2G)
  - `G10CH2` (来源: INFINEON_AURIX2G)
  - `G10CH3` (来源: INFINEON_AURIX2G)
  - `G10CH4` (来源: INFINEON_AURIX2G)
  - `G10CH5` (来源: INFINEON_AURIX2G)
  - `G10CH6` (来源: INFINEON_AURIX2G)
  - `G10CH7` (来源: INFINEON_AURIX2G)
  - `G10CH8` (来源: INFINEON_AURIX2G)
  - `G10CH9` (来源: INFINEON_AURIX2G)
  - `G10CH10` (来源: INFINEON_AURIX2G)
  - `G10CH11` (来源: INFINEON_AURIX2G)
  - `G11CH0` (来源: INFINEON_AURIX2G)
  - `G11CH1` (来源: INFINEON_AURIX2G)
  - `G11CH2` (来源: INFINEON_AURIX2G)
  - `G11CH3` (来源: INFINEON_AURIX2G)
  - `G11CH4` (来源: INFINEON_AURIX2G)
  - `G11CH5` (来源: INFINEON_AURIX2G)
  - `G11CH6` (来源: INFINEON_AURIX2G)
  - `G11CH7` (来源: INFINEON_AURIX2G)
  - `G11CH8` (来源: INFINEON_AURIX2G)
  - `G11CH9` (来源: INFINEON_AURIX2G)
  - `G11CH10` (来源: INFINEON_AURIX2G)
  - `G11CH11` (来源: INFINEON_AURIX2G)
  - `G11CH12` (来源: INFINEON_AURIX2G)
  - `G11CH13` (来源: INFINEON_AURIX2G)
  - `G11CH14` (来源: INFINEON_AURIX2G)
  - `G11CH15` (来源: INFINEON_AURIX2G)
- **描述**: Analog Input Channel Number.There are upto 8 analog inputs for each Primary Kernel and upto 16 analog inputs for each Secondary Kernel.

########## 5. AdcInputClassSelection

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2409d6`
- **参数名**: `AdcInputClassSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_HWUNIT_CLASS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_HWUNIT_CLASS_0` (来源: INFINEON_AURIX2G)
  - `ADC_HWUNIT_CLASS_1` (来源: INFINEON_AURIX2G)
  - `ADC_GLOBAL_CLASS_0` (来源: INFINEON_AURIX2G)
  - `ADC_GLOBAL_CLASS_1` (来源: INFINEON_AURIX2G)
- **描述**: defines the input class for the analog channel. Input class determines the channel conversion properties like sample time and data conversion mode for each channel.

########## 6. AdcBWDPrechargeLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2409d7`
- **参数名**: `AdcBWDPrechargeLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_BWD_PRECH_VAGND`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_BWD_PRECH_VAGND` (来源: INFINEON_AURIX2G)
  - `ADC_BWD_PRECH_VAREF` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the VAREF/VAGND pre-charging for the broken wire detection channel.

########## 7. AdcMultiplexerDiagnosticLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0550f2409d7`
- **参数名**: `AdcMultiplexerDiagnosticLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_MD_PULL_DOWN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_MD_PULL_DOWN` (来源: INFINEON_AURIX2G)
  - `ADC_MD_PULL_UP` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the Multiplexer diagnostics level for the channel.

########## 8. AdcConverterDiagnosticsLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2009d7`
- **参数名**: `AdcConverterDiagnosticsLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_CD_PULL_DEVICE_VDDM`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_CD_PULL_DEVICE_VDDM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_VSSM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_HALF_VDDM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_TWOTHIRD_VDDM` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the Converter diagnostics level for the channel.

####### 5. AdcGroup

**容器属性**:

- **UUID**: `ECUC:21b450f5-989b-4095-a451-d237d777751c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGroup`
- **多重性**: [1..32]

**容器描述**:

This container contains the Group configuration (parameters).

######## 参数配置

此容器包含 **19** 个参数：

######### INTEGER 类型参数

########## 1. AdcGroupId

- **UUID**: `ECUC:65e3660c-73a4-4172-8d28-4edb71e96153`
- **参数名**: `AdcGroupId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..383]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Numeric Id of the ADC channel group.  This value will be assigned to the symbolic name derived of the AdcGroup containers short name. The range of IDs for each ADC Hw Unit:
                                    ADC0: 0 to 31, ADC1: 32 to 63, ADC2: 64 to 95, ADC3: 96 to 127, ADC4: 128 to 159, ADC5: 160 to 191, ADC6: 192 to 223, ADC7: 224 to 255, ADC8: 256 to 287
                                    ADC9: 288 to 319, ADC10: 320 to 351, ADC11: 352 to 383
                                  Recommendation  : Use AUTO-CALCULATE-VALUE option for all nodes AdcGroupId

########## 2. AdcGroupPriority

- **UUID**: `ECUC:c3c0273d-3fbb-48ea-b64a-6c6592d6a05c`
- **参数名**: `AdcGroupPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Priority level of the AdcGroup.

########## 3. AdcHwTrigTimer

- **UUID**: `ECUC:ac85f536-5cf6-43f3-a6a7-d824eed38461`
- **参数名**: `AdcHwTrigTimer`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..1023]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Reload value of the ADC module embedded timer (only if supported by ADC hardware).

########## 4. AdcStreamingNumSamples

- **UUID**: `ECUC:ba5e660f-1505-40bb-9b17-7ce8a5655235`
- **参数名**: `AdcStreamingNumSamples`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of ADC values to be acquired per channel in streaming access mode.

########## 5. AdcChannel0Alias

- **UUID**: `ECUC:8ea93903-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcChannel0Alias`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter configures the alias channel to be used for Channel 0.

########## 6. AdcChannel1Alias

- **UUID**: `ECUC:8ea93913-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcChannel1Alias`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter configures the alias channel to be used for Channel 1.

########## 7. AdcEmuxStartSelection

- **UUID**: `ECUC:bb7a337b-c160-470a-8b8f-bc8bd4b16a7b`
- **参数名**: `AdcEmuxStartSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the EMUX start selection.

########## 8. AdcResRegDefinition

- **UUID**: `ECUC:ea7f8f6d-5d98-4bc4-321e-dc02c4c233fc`
- **参数名**: `AdcResRegDefinition`
- **数据类型**: INTEGER
- **多重性**: [1..16]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the result register used for storing the result of this particular ADC conversion. This value of this parameter should be in descending order for the nodes of AdcGroupDefinition.

######### BOOLEAN 类型参数

########## 1. AdcEmuxChGroup

- **UUID**: `ECUC:29e7f838-395d-461f-9e5d-541c0cb3d670`
- **参数名**: `AdcEmuxChGroup`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Group is EMUX or not.

######### ENUMERATION 类型参数

########## 1. AdcGroupAccessMode

- **UUID**: `ECUC:faad1eb6-43b4-4195-bacc-6245556acb07`
- **参数名**: `AdcGroupAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_ACCESS_MODE_SINGLE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_ACCESS_MODE_SINGLE` (来源: AUTOSAR_ECUC)
  - `ADC_ACCESS_MODE_STREAMING` (来源: AUTOSAR_ECUC)
- **描述**: Type of access mode to group conversion results.

########## 2. AdcGroupConversionMode

- **UUID**: `ECUC:25721d0a-d8a7-4ea3-96ab-49ced3030fce`
- **参数名**: `AdcGroupConversionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_CONV_MODE_ONESHOT`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_CONV_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `ADC_CONV_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **描述**: Type of conversion mode supported by the driver.

########## 3. AdcGroupReplacement

- **UUID**: `ECUC:f348b1d0-aabc-46ee-a71a-02cc6e49dca6`
- **参数名**: `AdcGroupReplacement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GROUP_REPL_ABORT_RESTART`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_GROUP_REPL_ABORT_RESTART` (来源: AUTOSAR_ECUC)
  - `ADC_GROUP_REPL_SUSPEND_RESUME` (来源: AUTOSAR_ECUC)
- **描述**: Replacement mechanism, which is used on ADC group level, if a group conversion is interrupted by a group which has a higher priority.

########## 4. AdcGroupTriggSrc

- **UUID**: `ECUC:1fb3e310-c03a-4a29-b2d2-f8d71765c6fc`
- **参数名**: `AdcGroupTriggSrc`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_TRIGG_SRC_SW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_TRIGG_SRC_HW` (来源: AUTOSAR_ECUC)
  - `ADC_TRIGG_SRC_SW` (来源: AUTOSAR_ECUC)
- **描述**: Type of source event that starts a group conversion.

########## 5. AdcHwTrigSignal

- **UUID**: `ECUC:70c09b6d-3cac-4db1-bee8-aafef6b9d2cf`
- **参数名**: `AdcHwTrigSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_HW_TRIG_RISING_EDGE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_HW_TRIG_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **描述**: Configures on which edge of the hardware trigger signal the driver should react, i.e. start the conversion (only if supported by the ADC hardware).

########## 6. AdcStreamingBufferMode

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf2-d2575ef9e9c8`
- **参数名**: `AdcStreamingBufferMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_STREAM_BUFFER_LINEAR`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_STREAM_BUFFER_CIRCULAR` (来源: AUTOSAR_ECUC)
  - `ADC_STREAM_BUFFER_LINEAR` (来源: AUTOSAR_ECUC)
- **描述**: Configure streaming buffer as "linear buffer" (i.e. the ADC Driver stops the conversion as soon as the stream buffer is full) or as "ring buffer" (wraps around if the end of the stream buffer is reached).

########## 7. AdcHwExtTrigSelect

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-2af2-d2575ef9e9c8`
- **参数名**: `AdcHwExtTrigSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_TRIG_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_TRIG_NONE` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_0_GxREQTRA_CCU60_SR3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_1_GxREQTRB_CCU61_SR3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_2_GxREQTRC_HSPDM` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_3_GxREQTRD_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_4_GxREQTRE_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_5_GxREQTRF_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_6_GxREQTRG_GTM_ADCx_TRIG4` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_7_GxREQTRH_ERUIOUTx` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_8_GxREQTRI_GTM_ADCx_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_9_GxREQTRJ_GTM_ADCx_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_10_GxREQTRK_GTM_ADCx_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_11_GxREQTRL_GTM_ADCx_TRIG3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_12_GxREQTRM_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_13_GxREQTRN_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_14_GxREQTRO_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_15_GxREQTRP_GxREQGTySEL` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW trigger source for the group.

########## 8. AdcHwExtGateSelect

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcHwExtGateSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GATE_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_GATE_NONE` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_0_GxREQGTA_GTM_ADCx_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_1_GxREQGTB_GTM_ADCx_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_2_GxREQGTC_CCU6061_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_3_GxREQGTD_CCU6061_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_4_GxREQGTE_CCU6061_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_5_GxREQGTF_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_6_GxREQGTG_GTM_ADCx_TRIG4` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_7_GxREQGTH_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_8_GxREQGTI_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_9_GxREQGTJ_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_10_GxREQGTK_GTM_ADCx_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_11_GxREQGTL_GTM_ADCx_TRIG3` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_12_GxREQGTM_ERUPDOUTx` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_13_GxREQGTN_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_14_GxREQGTO_UNUSED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW gating source for the group.

########## 9. AdcHwGateSignal

- **UUID**: `ECUC:8ea9390c-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcHwGateSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GATE_LVL_HIGH`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_GATE_LVL_HIGH` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_LVL_LOW` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW gating signal level.

######### FUNCTION-NAME 类型参数

########## 1. AdcNotification

- **UUID**: `ECUC:f43bffda-8d3a-4520-b424-b558fcbe752c`
- **参数名**: `AdcNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `IoHwAb_AdcNotification0`
- **描述**: Callback function for each group

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. AdcGroupDefinition

- **UUID**: `ECUC:fc412877-d8ab-4b65-96e8-0498ac13762e`
- **引用名**: `AdcGroupDefinition`
- **引用类型**: REFERENCE
- **多重性**: [1..16]
- **目标**: `AdcChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit/AdcChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Assignment of AdcChannels to a AdcGroups.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. EruTriggerConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruTriggerConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e69e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

############ 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e900-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

######### 2. EruGatingConfig

**容器属性**:

- **UUID**: `83452075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruGatingConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU Gating

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e39e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e911-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

############ 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e780-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

######### 3. GtmTriggerTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTriggerTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for TRIGGER. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb114e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

############ 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e0aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

########### ENUMERATION 类型参数

############ 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l6b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

######### 4. GtmGatingTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2213a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmGatingTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for GATING. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb664e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

############ 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e1aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

########### ENUMERATION 类型参数

############ 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-1db7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3685`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 6. EruTriggerConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruTriggerConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e69e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

########## 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e900-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

####### 7. EruGatingConfig

**容器属性**:

- **UUID**: `83452075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruGatingConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU Gating

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e39e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e911-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

########## 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e780-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

####### 8. GtmTriggerTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTriggerTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for TRIGGER. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb114e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

########## 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e0aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l6b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 9. GtmGatingTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2213a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmGatingTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for GATING. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb664e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

########## 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e1aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-1db7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3685`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 2. AdcGlobalInputClass

**容器属性**:

- **UUID**: `DCE:dcc39b88-cc3b-4358-ba87-30120722c6c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGlobalInputClass`
- **多重性**: [2..2]

**容器描述**:

This container defines the Global Input Class for A-D conversion

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. AdcChSampleTime

- **UUID**: `ECUC:ea7f906d-5d18-4bc4-808e-dc02c4c233ac`
- **参数名**: `AdcChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles.

######## 2. AdcEmuxChSampleTime

- **UUID**: `ECUC:0c679c6d-1e71-47e0-9381-6305a40ca8fd`
- **参数名**: `AdcEmuxChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles for EMUX conversions.

####### BOOLEAN 类型参数

######## 1. AdcChSESPSEnable

- **UUID**: `ECUC:6fe4295d-02b9-4f34-b9f2-337c2df6bd58`
- **参数名**: `AdcChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for Standard Conversions is enabled/disabled.

######## 2. AdcEmuxChSESPSEnable

- **UUID**: `ECUC:da1dc2b9-97dc-4c1a-82cf-6a66656f6246`
- **参数名**: `AdcEmuxChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for EMUX conversions is enabled/disabled.

####### ENUMERATION 类型参数

######## 1. AdcChPreChargeClkCycles

- **UUID**: `ECUC:7e0e69e5-6224-4364-a9b3-f0559f2409d6`
- **参数名**: `AdcChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for standard conversions.

######## 2. AdcChConvMode

- **UUID**: `ECUC:7e0e69e5-6004-5564-a9b3-f0559f2409d6`
- **参数名**: `AdcChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for Standard Conversions.

######## 3. AdcEmuxChPreChargeClkCycles

- **UUID**: `ECUC:4f520abb-60fd-4ea8-b02e-9bad6a36f264`
- **参数名**: `AdcEmuxChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for EMUX conversions.

######## 4. AdcEmuxChConvMode

- **UUID**: `ECUC:e266f886-48fd-4481-812f-1e8a7f22b218`
- **参数名**: `AdcEmuxChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for EMUX conversions.

##### 3. AdcHwUnit

**容器属性**:

- **UUID**: `ECUC:c67e7c58-3daf-455b-a213-95ae94b248d8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcHwUnit`
- **多重性**: [1..9]

**容器描述**:

This container contains the Driver configuration (parameters) depending on grouping of channels

###### 参数配置

此容器包含 **16** 个参数：

####### INTEGER 类型参数

######## 1. AdcAnalogClockSyncDelay

- **UUID**: `ECUC:482b876b-9787-4e46-875a-559b7a1427f2`
- **参数名**: `AdcAnalogClockSyncDelay`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines analog clock synchronization delay.

######## 2. AdcPrescale

- **UUID**: `ECUC:ea7f8f6d-5d98-4bc4-808e-dc02c4c233ac`
- **参数名**: `AdcPrescale`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [2..32]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the divider for generating the analog internal clock (fADCDI) from fADC.

####### BOOLEAN 类型参数

######## 1. AdcIdlePrechargeEnable

- **UUID**: `ECUC:6fe4295d-02b9-4f64-b9f2-33732df6bd58`
- **参数名**: `AdcIdlePrechargeEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines whether precharge of the sampling capacitor is enabled or not.

######## 2. AdcInputBufferEnable

- **UUID**: `ECUC:6fe4295d-02b5-4f64-b9f2-33732df6bd58`
- **参数名**: `AdcInputBufferEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines whether input buffering is enabled or not. If enabled buffering time is selected via AIPS(AdcChPreChargeClkCycles).

######## 3. AdcPostCalibrationDisable

- **UUID**: `ECUC:6fe42a5d-02b5-4f64-a9f2-33732df6bd58`
- **参数名**: `AdcPostCalibrationDisable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines whether the post calibration is enabled or disabled.

######## 4. AdcSampleSyncEnable

- **UUID**: `ECUC:6fe43a5d-02b5-4f64-a9f2-33732df6bd58`
- **参数名**: `AdcSampleSyncEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines whether the Adc Sample Time Synchronization is enabled or disabled.

######## 5. AdcMSBDoubleClkEnable

- **UUID**: `ECUC:6fe44a5d-02b5-4f65-a9f2-33732df6bd58`
- **参数名**: `AdcMSBDoubleClkEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the number of clock cycles for MSB conversions.

####### ENUMERATION 类型参数

######## 1. AdcClockSource

- **UUID**: `ECUC:08f7956c-d858-438f-9504-12df1ba10e73`
- **参数名**: `AdcClockSource`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_SYSTEM_CLK`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_SYSTEM_CLK` (来源: AUTOSAR_ECUC)
- **描述**: The ADC module specific clock input for the ADC. This parameter is not used for AURIX 2G. The clock source for the complete EVADC IP can be selected through node Adc/AdcSystemClock

######## 2. AdcHwUnitId

- **UUID**: `ECUC:7aa61340-e385-4037-b899-40ce3e595755`
- **参数名**: `AdcHwUnitId`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `HWUNIT_ADC0`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `HWUNIT_ADC0` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC1` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC2` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC3` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC4` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC8` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC9` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC10` (来源: AUTOSAR_ECUC)
  - `HWUNIT_ADC11` (来源: AUTOSAR_ECUC)
- **描述**: Description: Numeric ID of the HW Unit. This symbolic name allows accessing Hw Unit data. Enumeration literals are defined vendor specific.

######## 3. AdcPrechargeReference

- **UUID**: `ECUC:7e0e69e5-1104-5164-a9b3-f0559f2409d6`
- **参数名**: `AdcPrechargeReference`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_VDD_VSM_USED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_VDD_VSM_USED` (来源: INFINEON_AURIX2G)
  - `ADC_VDD_VSM_NOT_USED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines whether VDDM/VSSM is used for pre-charging or not.

######## 4. AdcReferencePrechargePhases

- **UUID**: `ECUC:7e0e69d5-1104-5164-a9b3-f0559f2409d6`
- **参数名**: `AdcReferencePrechargePhases`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_PRECHARGE_PHASE_1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_PRECHARGE_PHASE_1` (来源: INFINEON_AURIX2G)
  - `ADC_PRECHARGE_PHASE_2` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the precharge clock phases for the reference input.

######## 5. AdcCalibrationSampleTime

- **UUID**: `ECUC:7e0e69d4-2104-5164-a9b3-f0559f2409d6`
- **参数名**: `AdcCalibrationSampleTime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_CAL_TIME_2_TIMES_TADCI`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_CAL_TIME_2_TIMES_TADCI` (来源: INFINEON_AURIX2G)
  - `ADC_CAL_TIME_4_TIMES_TADCI` (来源: INFINEON_AURIX2G)
  - `ADC_CAL_TIME_6_TIMES_TADCI` (来源: INFINEON_AURIX2G)
  - `ADC_CAL_TIME_8_TIMES_TADCI` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the calibration sample time.

######## 6. AdcRequestSource0ConvMode

- **UUID**: `ECUC:8a1e64d4-2114-5165-a9b3-f0559f2409d6`
- **参数名**: `AdcRequestSource0ConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_WAIT_FOR_START_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_WAIT_FOR_START_MODE` (来源: INFINEON_AURIX2G)
  - `ADC_CANCEL_INJECT_REPEAT_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines conversion start mode for a request source.

######## 7. AdcRequestSource1ConvMode

- **UUID**: `ECUC:8a0e64d4-2113-5165-a9b3-f0559f2409d6`
- **参数名**: `AdcRequestSource1ConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_WAIT_FOR_START_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_WAIT_FOR_START_MODE` (来源: INFINEON_AURIX2G)
  - `ADC_CANCEL_INJECT_REPEAT_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines conversion start mode for a request source.

######## 8. AdcRequestSource2ConvMode

- **UUID**: `ECUC:8a0e64d5-2114-5165-a9b3-f0559f2409d6`
- **参数名**: `AdcRequestSource2ConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_WAIT_FOR_START_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_WAIT_FOR_START_MODE` (来源: INFINEON_AURIX2G)
  - `ADC_CANCEL_INJECT_REPEAT_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines conversion start mode for a request source.

######## 9. AdcSyncConvMode

- **UUID**: `ECUC:7e0e69e5-6004-1956-a9b3-f0559f2409d6`
- **参数名**: `AdcSyncConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_STAND_ALONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_STAND_ALONE` (来源: INFINEON_AURIX2G)
  - `ADC_SYNC_MASTER` (来源: INFINEON_AURIX2G)
  - `ADC_SYNC_SLAVE` (来源: INFINEON_AURIX2G)
- **描述**: Determines whether the HW groups operates in Stand-Alone or Master/Slave Sync Mode.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. AdcHwUnitInputClass

**容器属性**:

- **UUID**: `DCE:dcc39b88-cc3b-4358-b687-30120722c6c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcHwUnitInputClass`
- **多重性**: [2..2]

**容器描述**:

This container defines the Hw unit input class for A-D conversion

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. AdcChSampleTime

- **UUID**: `ECUC:ea7f9f3d-5d18-4bc4-808e-dc02c4c233ac`
- **参数名**: `AdcChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles.

########## 2. AdcEmuxChSampleTime

- **UUID**: `ECUC:2d556c2f-44db-4727-9de1-02b26fccba7a`
- **参数名**: `AdcEmuxChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles for EMUX conversions.

######### BOOLEAN 类型参数

########## 1. AdcChSESPSEnable

- **UUID**: `ECUC:6fe4295d-02b9-4f34-b9f2-337c2df6bd28`
- **参数名**: `AdcChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for Standard Conversions is enabled/disabled.

########## 2. AdcEmuxChSESPSEnable

- **UUID**: `ECUC:d5d1eacd-09a8-41f6-bb66-7fd06e4af3b8`
- **参数名**: `AdcEmuxChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for EMUX conversions is enabled/disabled.

######### ENUMERATION 类型参数

########## 1. AdcChPreChargeClkCycles

- **UUID**: `ECUC:7e0e6955-6004-4364-a9b3-f0559f2409d6`
- **参数名**: `AdcChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for standard conversions.

########## 2. AdcChConvMode

- **UUID**: `ECUC:7e0e69e5-6004-5564-a1b3-f0559f2409d6`
- **参数名**: `AdcChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for Standard Conversions.

########## 3. AdcEmuxChPreChargeClkCycles

- **UUID**: `ECUC:f6735f9d-b34e-471c-8b46-05f48c8438ef`
- **参数名**: `AdcEmuxChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for EMUX conversions.

########## 4. AdcEmuxChConvMode

- **UUID**: `ECUC:d7ad1fc7-868e-4a04-a63b-65e44411a564`
- **参数名**: `AdcEmuxChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for EMUX conversions.

####### 2. AdcChannel

**容器属性**:

- **UUID**: `ECUC:bfd7d43b-017d-4755-9a41-2bf12e38403d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcChannel`
- **多重性**: [1..255]

**容器描述**:

This container contains the channel configuration (parameters) depending on the hardware capability. This value will be assigned to the symbolic name derived of the AdcChannel container short name. Channel ID 0xFF is considered as invalid

######## 参数配置

此容器包含 **20** 个参数：

######### INTEGER 类型参数

########## 1. AdcChannelConvTime

- **UUID**: `ECUC:cda3fa6e-3f00-43a3-a05e-5c97744e6aaf`
- **参数名**: `AdcChannelConvTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of conversion time, i.e. the time during which the analogue value is converted into digital representation, (in clock cycles) for each channel, if supported by hardware.

########## 2. AdcChannelHighLimit

- **UUID**: `ECUC:65b39edf-db50-479b-becd-268512557336`
- **参数名**: `AdcChannelHighLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4095`
- **取值范围**: [0..4095]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: High limit - used for limit checking.

########## 3. AdcChannelId

- **UUID**: `ECUC:482b876b-1787-4e46-875a-559b7a1427f2`
- **参数名**: `AdcChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the assignment of the channel to the physical ADC  hardware channel.

########## 4. AdcChannelLowLimit

- **UUID**: `ECUC:bd3f78a2-2b94-419a-961c-5ad47f5a8bcb`
- **参数名**: `AdcChannelLowLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4095]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Low limit - used for limit checking.

########## 5. AdcChannelResolution

- **UUID**: `ECUC:c05e44f5-f418-4772-9ed3-ba767591baf1`
- **参数名**: `AdcChannelResolution`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `12`
- **取值范围**: [1..63]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Channel resolution in bits.

########## 6. AdcChannelSampTime

- **UUID**: `ECUC:d11259ac-99d0-488f-9cc6-a66170fbb368`
- **参数名**: `AdcChannelSampTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of sampling time, i.e. the time during which the value is sampled, (in clock cycles) for each channel, if supported by hardware.

######### BOOLEAN 类型参数

########## 1. AdcChannelLimitCheck

- **UUID**: `ECUC:6c8938e0-f362-4cdc-8711-6d4b429215b3`
- **参数名**: `AdcChannelLimitCheck`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables or disables limit checking for an ADC channel.

########## 2. AdcSyncConvChannelEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b17`
- **参数名**: `AdcSyncConvChannelEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables the synchronous conversion for this channel.Conversion of this channel will trigger conversion for the same analog channel number on slave HW groups also.

########## 3. AdcBWDEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b18`
- **参数名**: `AdcBWDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the broken wire detection feature for the channel.

########## 4. AdcPullDownDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec203fb5b18`
- **参数名**: `AdcPullDownDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Pull Down diagnostics feature for the channel.

########## 5. AdcMultiplexerDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec203fb5018`
- **参数名**: `AdcMultiplexerDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Multiplexer diagnostics feature for the channel.

########## 6. AdcConverterDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec220fb5b18`
- **参数名**: `AdcConverterDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Converter diagnostics feature for the channel.

######### ENUMERATION 类型参数

########## 1. AdcChannelRangeSelect

- **UUID**: `ECUC:8b1c1853-c817-448a-982b-cb15f700c87d`
- **参数名**: `AdcChannelRangeSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_RANGE_ALWAYS`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_RANGE_ALWAYS` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_UNDER_LOW` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_UNDER_LOW` (来源: AUTOSAR_ECUC)
- **描述**: In case of active limit checking: defines which conversion values are taken into account related to the boarders defined with AdcChannelLowLimit and AdcChannelHighLimit.

########## 2. AdcChannelRefVoltsrcHigh

- **UUID**: `ECUC:94395609-bae2-465a-9878-df86ada9bffb`
- **参数名**: `AdcChannelRefVoltsrcHigh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_USES_VREF`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_USES_VREF` (来源: AUTOSAR_ECUC)
  - `ADC_USES_CH0` (来源: AUTOSAR_ECUC)
- **描述**: Upper reference voltage source for each channel.

########## 3. AdcChannelRefVoltsrcLow

- **UUID**: `ECUC:582225d2-20d0-47eb-a3c1-f387a68cb7c4`
- **参数名**: `AdcChannelRefVoltsrcLow`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_USES_VAGND`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_USES_VAGND` (来源: AUTOSAR_ECUC)
- **描述**: Lower reference voltage source for each channel.

########## 4. AdcAnChannelNum

- **UUID**: `55b16180-ed10-4e98-a14d-f205643c08a0`
- **参数名**: `AdcAnChannelNum`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `G0CH0`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `G0CH0` (来源: INFINEON_AURIX2G)
  - `G0CH1` (来源: INFINEON_AURIX2G)
  - `G0CH2` (来源: INFINEON_AURIX2G)
  - `G0CH3` (来源: INFINEON_AURIX2G)
  - `G0CH4` (来源: INFINEON_AURIX2G)
  - `G0CH5` (来源: INFINEON_AURIX2G)
  - `G0CH6` (来源: INFINEON_AURIX2G)
  - `G0CH7` (来源: INFINEON_AURIX2G)
  - `G1CH0` (来源: INFINEON_AURIX2G)
  - `G1CH1` (来源: INFINEON_AURIX2G)
  - `G1CH2` (来源: INFINEON_AURIX2G)
  - `G1CH3` (来源: INFINEON_AURIX2G)
  - `G1CH4` (来源: INFINEON_AURIX2G)
  - `G1CH5` (来源: INFINEON_AURIX2G)
  - `G1CH6` (来源: INFINEON_AURIX2G)
  - `G1CH7` (来源: INFINEON_AURIX2G)
  - `G2CH0` (来源: INFINEON_AURIX2G)
  - `G2CH1` (来源: INFINEON_AURIX2G)
  - `G2CH2` (来源: INFINEON_AURIX2G)
  - `G2CH3` (来源: INFINEON_AURIX2G)
  - `G2CH4` (来源: INFINEON_AURIX2G)
  - `G2CH5` (来源: INFINEON_AURIX2G)
  - `G2CH6` (来源: INFINEON_AURIX2G)
  - `G2CH7` (来源: INFINEON_AURIX2G)
  - `G3CH0` (来源: INFINEON_AURIX2G)
  - `G3CH1` (来源: INFINEON_AURIX2G)
  - `G3CH2` (来源: INFINEON_AURIX2G)
  - `G3CH3` (来源: INFINEON_AURIX2G)
  - `G3CH4` (来源: INFINEON_AURIX2G)
  - `G3CH5` (来源: INFINEON_AURIX2G)
  - `G3CH6` (来源: INFINEON_AURIX2G)
  - `G3CH7` (来源: INFINEON_AURIX2G)
  - `G4CH0` (来源: INFINEON_AURIX2G)
  - `G4CH1` (来源: INFINEON_AURIX2G)
  - `G4CH2` (来源: INFINEON_AURIX2G)
  - `G4CH3` (来源: INFINEON_AURIX2G)
  - `G4CH4` (来源: INFINEON_AURIX2G)
  - `G4CH5` (来源: INFINEON_AURIX2G)
  - `G4CH6` (来源: INFINEON_AURIX2G)
  - `G4CH7` (来源: INFINEON_AURIX2G)
  - `G8CH0` (来源: INFINEON_AURIX2G)
  - `G8CH1` (来源: INFINEON_AURIX2G)
  - `G8CH2` (来源: INFINEON_AURIX2G)
  - `G8CH3` (来源: INFINEON_AURIX2G)
  - `G8CH4` (来源: INFINEON_AURIX2G)
  - `G8CH5` (来源: INFINEON_AURIX2G)
  - `G8CH6` (来源: INFINEON_AURIX2G)
  - `G8CH7` (来源: INFINEON_AURIX2G)
  - `G8CH8` (来源: INFINEON_AURIX2G)
  - `G8CH9` (来源: INFINEON_AURIX2G)
  - `G8CH10` (来源: INFINEON_AURIX2G)
  - `G8CH11` (来源: INFINEON_AURIX2G)
  - `G8CH12` (来源: INFINEON_AURIX2G)
  - `G8CH13` (来源: INFINEON_AURIX2G)
  - `G8CH14` (来源: INFINEON_AURIX2G)
  - `G8CH15` (来源: INFINEON_AURIX2G)
  - `G9CH0` (来源: INFINEON_AURIX2G)
  - `G9CH1` (来源: INFINEON_AURIX2G)
  - `G9CH2` (来源: INFINEON_AURIX2G)
  - `G9CH3` (来源: INFINEON_AURIX2G)
  - `G9CH4` (来源: INFINEON_AURIX2G)
  - `G9CH5` (来源: INFINEON_AURIX2G)
  - `G9CH6` (来源: INFINEON_AURIX2G)
  - `G9CH7` (来源: INFINEON_AURIX2G)
  - `G9CH8` (来源: INFINEON_AURIX2G)
  - `G9CH9` (来源: INFINEON_AURIX2G)
  - `G9CH10` (来源: INFINEON_AURIX2G)
  - `G9CH11` (来源: INFINEON_AURIX2G)
  - `G9CH12` (来源: INFINEON_AURIX2G)
  - `G9CH13` (来源: INFINEON_AURIX2G)
  - `G9CH14` (来源: INFINEON_AURIX2G)
  - `G9CH15` (来源: INFINEON_AURIX2G)
  - `G10CH0` (来源: INFINEON_AURIX2G)
  - `G10CH1` (来源: INFINEON_AURIX2G)
  - `G10CH2` (来源: INFINEON_AURIX2G)
  - `G10CH3` (来源: INFINEON_AURIX2G)
  - `G10CH4` (来源: INFINEON_AURIX2G)
  - `G10CH5` (来源: INFINEON_AURIX2G)
  - `G10CH6` (来源: INFINEON_AURIX2G)
  - `G10CH7` (来源: INFINEON_AURIX2G)
  - `G10CH8` (来源: INFINEON_AURIX2G)
  - `G10CH9` (来源: INFINEON_AURIX2G)
  - `G10CH10` (来源: INFINEON_AURIX2G)
  - `G10CH11` (来源: INFINEON_AURIX2G)
  - `G11CH0` (来源: INFINEON_AURIX2G)
  - `G11CH1` (来源: INFINEON_AURIX2G)
  - `G11CH2` (来源: INFINEON_AURIX2G)
  - `G11CH3` (来源: INFINEON_AURIX2G)
  - `G11CH4` (来源: INFINEON_AURIX2G)
  - `G11CH5` (来源: INFINEON_AURIX2G)
  - `G11CH6` (来源: INFINEON_AURIX2G)
  - `G11CH7` (来源: INFINEON_AURIX2G)
  - `G11CH8` (来源: INFINEON_AURIX2G)
  - `G11CH9` (来源: INFINEON_AURIX2G)
  - `G11CH10` (来源: INFINEON_AURIX2G)
  - `G11CH11` (来源: INFINEON_AURIX2G)
  - `G11CH12` (来源: INFINEON_AURIX2G)
  - `G11CH13` (来源: INFINEON_AURIX2G)
  - `G11CH14` (来源: INFINEON_AURIX2G)
  - `G11CH15` (来源: INFINEON_AURIX2G)
- **描述**: Analog Input Channel Number.There are upto 8 analog inputs for each Primary Kernel and upto 16 analog inputs for each Secondary Kernel.

########## 5. AdcInputClassSelection

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2409d6`
- **参数名**: `AdcInputClassSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_HWUNIT_CLASS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_HWUNIT_CLASS_0` (来源: INFINEON_AURIX2G)
  - `ADC_HWUNIT_CLASS_1` (来源: INFINEON_AURIX2G)
  - `ADC_GLOBAL_CLASS_0` (来源: INFINEON_AURIX2G)
  - `ADC_GLOBAL_CLASS_1` (来源: INFINEON_AURIX2G)
- **描述**: defines the input class for the analog channel. Input class determines the channel conversion properties like sample time and data conversion mode for each channel.

########## 6. AdcBWDPrechargeLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2409d7`
- **参数名**: `AdcBWDPrechargeLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_BWD_PRECH_VAGND`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_BWD_PRECH_VAGND` (来源: INFINEON_AURIX2G)
  - `ADC_BWD_PRECH_VAREF` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the VAREF/VAGND pre-charging for the broken wire detection channel.

########## 7. AdcMultiplexerDiagnosticLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0550f2409d7`
- **参数名**: `AdcMultiplexerDiagnosticLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_MD_PULL_DOWN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_MD_PULL_DOWN` (来源: INFINEON_AURIX2G)
  - `ADC_MD_PULL_UP` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the Multiplexer diagnostics level for the channel.

########## 8. AdcConverterDiagnosticsLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2009d7`
- **参数名**: `AdcConverterDiagnosticsLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_CD_PULL_DEVICE_VDDM`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_CD_PULL_DEVICE_VDDM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_VSSM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_HALF_VDDM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_TWOTHIRD_VDDM` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the Converter diagnostics level for the channel.

####### 3. AdcGroup

**容器属性**:

- **UUID**: `ECUC:21b450f5-989b-4095-a451-d237d777751c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGroup`
- **多重性**: [1..32]

**容器描述**:

This container contains the Group configuration (parameters).

######## 参数配置

此容器包含 **19** 个参数：

######### INTEGER 类型参数

########## 1. AdcGroupId

- **UUID**: `ECUC:65e3660c-73a4-4172-8d28-4edb71e96153`
- **参数名**: `AdcGroupId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..383]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Numeric Id of the ADC channel group.  This value will be assigned to the symbolic name derived of the AdcGroup containers short name. The range of IDs for each ADC Hw Unit:
                                    ADC0: 0 to 31, ADC1: 32 to 63, ADC2: 64 to 95, ADC3: 96 to 127, ADC4: 128 to 159, ADC5: 160 to 191, ADC6: 192 to 223, ADC7: 224 to 255, ADC8: 256 to 287
                                    ADC9: 288 to 319, ADC10: 320 to 351, ADC11: 352 to 383
                                  Recommendation  : Use AUTO-CALCULATE-VALUE option for all nodes AdcGroupId

########## 2. AdcGroupPriority

- **UUID**: `ECUC:c3c0273d-3fbb-48ea-b64a-6c6592d6a05c`
- **参数名**: `AdcGroupPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Priority level of the AdcGroup.

########## 3. AdcHwTrigTimer

- **UUID**: `ECUC:ac85f536-5cf6-43f3-a6a7-d824eed38461`
- **参数名**: `AdcHwTrigTimer`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..1023]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Reload value of the ADC module embedded timer (only if supported by ADC hardware).

########## 4. AdcStreamingNumSamples

- **UUID**: `ECUC:ba5e660f-1505-40bb-9b17-7ce8a5655235`
- **参数名**: `AdcStreamingNumSamples`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of ADC values to be acquired per channel in streaming access mode.

########## 5. AdcChannel0Alias

- **UUID**: `ECUC:8ea93903-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcChannel0Alias`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter configures the alias channel to be used for Channel 0.

########## 6. AdcChannel1Alias

- **UUID**: `ECUC:8ea93913-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcChannel1Alias`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter configures the alias channel to be used for Channel 1.

########## 7. AdcEmuxStartSelection

- **UUID**: `ECUC:bb7a337b-c160-470a-8b8f-bc8bd4b16a7b`
- **参数名**: `AdcEmuxStartSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the EMUX start selection.

########## 8. AdcResRegDefinition

- **UUID**: `ECUC:ea7f8f6d-5d98-4bc4-321e-dc02c4c233fc`
- **参数名**: `AdcResRegDefinition`
- **数据类型**: INTEGER
- **多重性**: [1..16]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the result register used for storing the result of this particular ADC conversion. This value of this parameter should be in descending order for the nodes of AdcGroupDefinition.

######### BOOLEAN 类型参数

########## 1. AdcEmuxChGroup

- **UUID**: `ECUC:29e7f838-395d-461f-9e5d-541c0cb3d670`
- **参数名**: `AdcEmuxChGroup`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Group is EMUX or not.

######### ENUMERATION 类型参数

########## 1. AdcGroupAccessMode

- **UUID**: `ECUC:faad1eb6-43b4-4195-bacc-6245556acb07`
- **参数名**: `AdcGroupAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_ACCESS_MODE_SINGLE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_ACCESS_MODE_SINGLE` (来源: AUTOSAR_ECUC)
  - `ADC_ACCESS_MODE_STREAMING` (来源: AUTOSAR_ECUC)
- **描述**: Type of access mode to group conversion results.

########## 2. AdcGroupConversionMode

- **UUID**: `ECUC:25721d0a-d8a7-4ea3-96ab-49ced3030fce`
- **参数名**: `AdcGroupConversionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_CONV_MODE_ONESHOT`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_CONV_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `ADC_CONV_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **描述**: Type of conversion mode supported by the driver.

########## 3. AdcGroupReplacement

- **UUID**: `ECUC:f348b1d0-aabc-46ee-a71a-02cc6e49dca6`
- **参数名**: `AdcGroupReplacement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GROUP_REPL_ABORT_RESTART`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_GROUP_REPL_ABORT_RESTART` (来源: AUTOSAR_ECUC)
  - `ADC_GROUP_REPL_SUSPEND_RESUME` (来源: AUTOSAR_ECUC)
- **描述**: Replacement mechanism, which is used on ADC group level, if a group conversion is interrupted by a group which has a higher priority.

########## 4. AdcGroupTriggSrc

- **UUID**: `ECUC:1fb3e310-c03a-4a29-b2d2-f8d71765c6fc`
- **参数名**: `AdcGroupTriggSrc`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_TRIGG_SRC_SW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_TRIGG_SRC_HW` (来源: AUTOSAR_ECUC)
  - `ADC_TRIGG_SRC_SW` (来源: AUTOSAR_ECUC)
- **描述**: Type of source event that starts a group conversion.

########## 5. AdcHwTrigSignal

- **UUID**: `ECUC:70c09b6d-3cac-4db1-bee8-aafef6b9d2cf`
- **参数名**: `AdcHwTrigSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_HW_TRIG_RISING_EDGE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_HW_TRIG_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **描述**: Configures on which edge of the hardware trigger signal the driver should react, i.e. start the conversion (only if supported by the ADC hardware).

########## 6. AdcStreamingBufferMode

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf2-d2575ef9e9c8`
- **参数名**: `AdcStreamingBufferMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_STREAM_BUFFER_LINEAR`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_STREAM_BUFFER_CIRCULAR` (来源: AUTOSAR_ECUC)
  - `ADC_STREAM_BUFFER_LINEAR` (来源: AUTOSAR_ECUC)
- **描述**: Configure streaming buffer as "linear buffer" (i.e. the ADC Driver stops the conversion as soon as the stream buffer is full) or as "ring buffer" (wraps around if the end of the stream buffer is reached).

########## 7. AdcHwExtTrigSelect

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-2af2-d2575ef9e9c8`
- **参数名**: `AdcHwExtTrigSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_TRIG_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_TRIG_NONE` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_0_GxREQTRA_CCU60_SR3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_1_GxREQTRB_CCU61_SR3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_2_GxREQTRC_HSPDM` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_3_GxREQTRD_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_4_GxREQTRE_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_5_GxREQTRF_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_6_GxREQTRG_GTM_ADCx_TRIG4` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_7_GxREQTRH_ERUIOUTx` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_8_GxREQTRI_GTM_ADCx_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_9_GxREQTRJ_GTM_ADCx_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_10_GxREQTRK_GTM_ADCx_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_11_GxREQTRL_GTM_ADCx_TRIG3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_12_GxREQTRM_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_13_GxREQTRN_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_14_GxREQTRO_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_15_GxREQTRP_GxREQGTySEL` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW trigger source for the group.

########## 8. AdcHwExtGateSelect

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcHwExtGateSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GATE_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_GATE_NONE` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_0_GxREQGTA_GTM_ADCx_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_1_GxREQGTB_GTM_ADCx_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_2_GxREQGTC_CCU6061_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_3_GxREQGTD_CCU6061_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_4_GxREQGTE_CCU6061_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_5_GxREQGTF_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_6_GxREQGTG_GTM_ADCx_TRIG4` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_7_GxREQGTH_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_8_GxREQGTI_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_9_GxREQGTJ_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_10_GxREQGTK_GTM_ADCx_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_11_GxREQGTL_GTM_ADCx_TRIG3` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_12_GxREQGTM_ERUPDOUTx` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_13_GxREQGTN_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_14_GxREQGTO_UNUSED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW gating source for the group.

########## 9. AdcHwGateSignal

- **UUID**: `ECUC:8ea9390c-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcHwGateSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GATE_LVL_HIGH`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_GATE_LVL_HIGH` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_LVL_LOW` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW gating signal level.

######### FUNCTION-NAME 类型参数

########## 1. AdcNotification

- **UUID**: `ECUC:f43bffda-8d3a-4520-b424-b558fcbe752c`
- **参数名**: `AdcNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `IoHwAb_AdcNotification0`
- **描述**: Callback function for each group

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. AdcGroupDefinition

- **UUID**: `ECUC:fc412877-d8ab-4b65-96e8-0498ac13762e`
- **引用名**: `AdcGroupDefinition`
- **引用类型**: REFERENCE
- **多重性**: [1..16]
- **目标**: `AdcChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit/AdcChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Assignment of AdcChannels to a AdcGroups.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. EruTriggerConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruTriggerConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e69e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

############ 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e900-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

######### 2. EruGatingConfig

**容器属性**:

- **UUID**: `83452075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruGatingConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU Gating

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e39e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e911-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

############ 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e780-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

######### 3. GtmTriggerTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTriggerTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for TRIGGER. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb114e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

############ 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e0aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

########### ENUMERATION 类型参数

############ 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l6b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

######### 4. GtmGatingTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2213a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmGatingTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for GATING. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb664e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

############ 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e1aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

########### ENUMERATION 类型参数

############ 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-1db7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3685`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 4. EruTriggerConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruTriggerConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e69e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

########## 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e900-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

####### 5. EruGatingConfig

**容器属性**:

- **UUID**: `83452075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruGatingConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU Gating

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e39e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e911-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

########## 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e780-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

####### 6. GtmTriggerTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTriggerTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for TRIGGER. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb114e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

########## 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e0aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l6b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 7. GtmGatingTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2213a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmGatingTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for GATING. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb664e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

########## 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e1aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-1db7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3685`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 4. AdcHwUnitInputClass

**容器属性**:

- **UUID**: `DCE:dcc39b88-cc3b-4358-b687-30120722c6c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcHwUnitInputClass`
- **多重性**: [2..2]

**容器描述**:

This container defines the Hw unit input class for A-D conversion

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. AdcChSampleTime

- **UUID**: `ECUC:ea7f9f3d-5d18-4bc4-808e-dc02c4c233ac`
- **参数名**: `AdcChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles.

######## 2. AdcEmuxChSampleTime

- **UUID**: `ECUC:2d556c2f-44db-4727-9de1-02b26fccba7a`
- **参数名**: `AdcEmuxChSampleTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of additional clock cycles to be added to the minimum sample phase of 2 sample clock cycles for EMUX conversions.

####### BOOLEAN 类型参数

######## 1. AdcChSESPSEnable

- **UUID**: `ECUC:6fe4295d-02b9-4f34-b9f2-337c2df6bd28`
- **参数名**: `AdcChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for Standard Conversions is enabled/disabled.

######## 2. AdcEmuxChSESPSEnable

- **UUID**: `ECUC:d5d1eacd-09a8-41f6-bb66-7fd06e4af3b8`
- **参数名**: `AdcEmuxChSESPSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Spread Early Sample Point for EMUX conversions is enabled/disabled.

####### ENUMERATION 类型参数

######## 1. AdcChPreChargeClkCycles

- **UUID**: `ECUC:7e0e6955-6004-4364-a9b3-f0559f2409d6`
- **参数名**: `AdcChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for standard conversions.

######## 2. AdcChConvMode

- **UUID**: `ECUC:7e0e69e5-6004-5564-a1b3-f0559f2409d6`
- **参数名**: `AdcChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for Standard Conversions.

######## 3. AdcEmuxChPreChargeClkCycles

- **UUID**: `ECUC:f6735f9d-b34e-471c-8b46-05f48c8438ef`
- **参数名**: `AdcEmuxChPreChargeClkCycles`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INPUT_PRECHARGE_CYCLES_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INPUT_PRECHARGE_CYCLES_0` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_8` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_16` (来源: INFINEON_AURIX2G)
  - `ADC_INPUT_PRECHARGE_CYCLES_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of analog input precharge clock cycles for EMUX conversions.

######## 4. AdcEmuxChConvMode

- **UUID**: `ECUC:d7ad1fc7-868e-4a04-a63b-65e44411a564`
- **参数名**: `AdcEmuxChConvMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_NOISE_REDUCTION_STEPS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_NOISE_REDUCTION_STEPS_0` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_1` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_3` (来源: INFINEON_AURIX2G)
  - `ADC_NOISE_REDUCTION_STEPS_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the noise reduction level for EMUX conversions.

##### 5. AdcChannel

**容器属性**:

- **UUID**: `ECUC:bfd7d43b-017d-4755-9a41-2bf12e38403d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcChannel`
- **多重性**: [1..255]

**容器描述**:

This container contains the channel configuration (parameters) depending on the hardware capability. This value will be assigned to the symbolic name derived of the AdcChannel container short name. Channel ID 0xFF is considered as invalid

###### 参数配置

此容器包含 **20** 个参数：

####### INTEGER 类型参数

######## 1. AdcChannelConvTime

- **UUID**: `ECUC:cda3fa6e-3f00-43a3-a05e-5c97744e6aaf`
- **参数名**: `AdcChannelConvTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of conversion time, i.e. the time during which the analogue value is converted into digital representation, (in clock cycles) for each channel, if supported by hardware.

######## 2. AdcChannelHighLimit

- **UUID**: `ECUC:65b39edf-db50-479b-becd-268512557336`
- **参数名**: `AdcChannelHighLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4095`
- **取值范围**: [0..4095]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: High limit - used for limit checking.

######## 3. AdcChannelId

- **UUID**: `ECUC:482b876b-1787-4e46-875a-559b7a1427f2`
- **参数名**: `AdcChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the assignment of the channel to the physical ADC  hardware channel.

######## 4. AdcChannelLowLimit

- **UUID**: `ECUC:bd3f78a2-2b94-419a-961c-5ad47f5a8bcb`
- **参数名**: `AdcChannelLowLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4095]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Low limit - used for limit checking.

######## 5. AdcChannelResolution

- **UUID**: `ECUC:c05e44f5-f418-4772-9ed3-ba767591baf1`
- **参数名**: `AdcChannelResolution`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `12`
- **取值范围**: [1..63]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Channel resolution in bits.

######## 6. AdcChannelSampTime

- **UUID**: `ECUC:d11259ac-99d0-488f-9cc6-a66170fbb368`
- **参数名**: `AdcChannelSampTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of sampling time, i.e. the time during which the value is sampled, (in clock cycles) for each channel, if supported by hardware.

####### BOOLEAN 类型参数

######## 1. AdcChannelLimitCheck

- **UUID**: `ECUC:6c8938e0-f362-4cdc-8711-6d4b429215b3`
- **参数名**: `AdcChannelLimitCheck`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables or disables limit checking for an ADC channel.

######## 2. AdcSyncConvChannelEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b17`
- **参数名**: `AdcSyncConvChannelEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables the synchronous conversion for this channel.Conversion of this channel will trigger conversion for the same analog channel number on slave HW groups also.

######## 3. AdcBWDEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b18`
- **参数名**: `AdcBWDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the broken wire detection feature for the channel.

######## 4. AdcPullDownDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec203fb5b18`
- **参数名**: `AdcPullDownDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Pull Down diagnostics feature for the channel.

######## 5. AdcMultiplexerDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec203fb5018`
- **参数名**: `AdcMultiplexerDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Multiplexer diagnostics feature for the channel.

######## 6. AdcConverterDiagnosticEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec220fb5b18`
- **参数名**: `AdcConverterDiagnosticEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables or disables the Converter diagnostics feature for the channel.

####### ENUMERATION 类型参数

######## 1. AdcChannelRangeSelect

- **UUID**: `ECUC:8b1c1853-c817-448a-982b-cb15f700c87d`
- **参数名**: `AdcChannelRangeSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_RANGE_ALWAYS`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_RANGE_ALWAYS` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_UNDER_LOW` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_UNDER_LOW` (来源: AUTOSAR_ECUC)
- **描述**: In case of active limit checking: defines which conversion values are taken into account related to the boarders defined with AdcChannelLowLimit and AdcChannelHighLimit.

######## 2. AdcChannelRefVoltsrcHigh

- **UUID**: `ECUC:94395609-bae2-465a-9878-df86ada9bffb`
- **参数名**: `AdcChannelRefVoltsrcHigh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_USES_VREF`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_USES_VREF` (来源: AUTOSAR_ECUC)
  - `ADC_USES_CH0` (来源: AUTOSAR_ECUC)
- **描述**: Upper reference voltage source for each channel.

######## 3. AdcChannelRefVoltsrcLow

- **UUID**: `ECUC:582225d2-20d0-47eb-a3c1-f387a68cb7c4`
- **参数名**: `AdcChannelRefVoltsrcLow`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_USES_VAGND`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_USES_VAGND` (来源: AUTOSAR_ECUC)
- **描述**: Lower reference voltage source for each channel.

######## 4. AdcAnChannelNum

- **UUID**: `55b16180-ed10-4e98-a14d-f205643c08a0`
- **参数名**: `AdcAnChannelNum`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `G0CH0`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `G0CH0` (来源: INFINEON_AURIX2G)
  - `G0CH1` (来源: INFINEON_AURIX2G)
  - `G0CH2` (来源: INFINEON_AURIX2G)
  - `G0CH3` (来源: INFINEON_AURIX2G)
  - `G0CH4` (来源: INFINEON_AURIX2G)
  - `G0CH5` (来源: INFINEON_AURIX2G)
  - `G0CH6` (来源: INFINEON_AURIX2G)
  - `G0CH7` (来源: INFINEON_AURIX2G)
  - `G1CH0` (来源: INFINEON_AURIX2G)
  - `G1CH1` (来源: INFINEON_AURIX2G)
  - `G1CH2` (来源: INFINEON_AURIX2G)
  - `G1CH3` (来源: INFINEON_AURIX2G)
  - `G1CH4` (来源: INFINEON_AURIX2G)
  - `G1CH5` (来源: INFINEON_AURIX2G)
  - `G1CH6` (来源: INFINEON_AURIX2G)
  - `G1CH7` (来源: INFINEON_AURIX2G)
  - `G2CH0` (来源: INFINEON_AURIX2G)
  - `G2CH1` (来源: INFINEON_AURIX2G)
  - `G2CH2` (来源: INFINEON_AURIX2G)
  - `G2CH3` (来源: INFINEON_AURIX2G)
  - `G2CH4` (来源: INFINEON_AURIX2G)
  - `G2CH5` (来源: INFINEON_AURIX2G)
  - `G2CH6` (来源: INFINEON_AURIX2G)
  - `G2CH7` (来源: INFINEON_AURIX2G)
  - `G3CH0` (来源: INFINEON_AURIX2G)
  - `G3CH1` (来源: INFINEON_AURIX2G)
  - `G3CH2` (来源: INFINEON_AURIX2G)
  - `G3CH3` (来源: INFINEON_AURIX2G)
  - `G3CH4` (来源: INFINEON_AURIX2G)
  - `G3CH5` (来源: INFINEON_AURIX2G)
  - `G3CH6` (来源: INFINEON_AURIX2G)
  - `G3CH7` (来源: INFINEON_AURIX2G)
  - `G4CH0` (来源: INFINEON_AURIX2G)
  - `G4CH1` (来源: INFINEON_AURIX2G)
  - `G4CH2` (来源: INFINEON_AURIX2G)
  - `G4CH3` (来源: INFINEON_AURIX2G)
  - `G4CH4` (来源: INFINEON_AURIX2G)
  - `G4CH5` (来源: INFINEON_AURIX2G)
  - `G4CH6` (来源: INFINEON_AURIX2G)
  - `G4CH7` (来源: INFINEON_AURIX2G)
  - `G8CH0` (来源: INFINEON_AURIX2G)
  - `G8CH1` (来源: INFINEON_AURIX2G)
  - `G8CH2` (来源: INFINEON_AURIX2G)
  - `G8CH3` (来源: INFINEON_AURIX2G)
  - `G8CH4` (来源: INFINEON_AURIX2G)
  - `G8CH5` (来源: INFINEON_AURIX2G)
  - `G8CH6` (来源: INFINEON_AURIX2G)
  - `G8CH7` (来源: INFINEON_AURIX2G)
  - `G8CH8` (来源: INFINEON_AURIX2G)
  - `G8CH9` (来源: INFINEON_AURIX2G)
  - `G8CH10` (来源: INFINEON_AURIX2G)
  - `G8CH11` (来源: INFINEON_AURIX2G)
  - `G8CH12` (来源: INFINEON_AURIX2G)
  - `G8CH13` (来源: INFINEON_AURIX2G)
  - `G8CH14` (来源: INFINEON_AURIX2G)
  - `G8CH15` (来源: INFINEON_AURIX2G)
  - `G9CH0` (来源: INFINEON_AURIX2G)
  - `G9CH1` (来源: INFINEON_AURIX2G)
  - `G9CH2` (来源: INFINEON_AURIX2G)
  - `G9CH3` (来源: INFINEON_AURIX2G)
  - `G9CH4` (来源: INFINEON_AURIX2G)
  - `G9CH5` (来源: INFINEON_AURIX2G)
  - `G9CH6` (来源: INFINEON_AURIX2G)
  - `G9CH7` (来源: INFINEON_AURIX2G)
  - `G9CH8` (来源: INFINEON_AURIX2G)
  - `G9CH9` (来源: INFINEON_AURIX2G)
  - `G9CH10` (来源: INFINEON_AURIX2G)
  - `G9CH11` (来源: INFINEON_AURIX2G)
  - `G9CH12` (来源: INFINEON_AURIX2G)
  - `G9CH13` (来源: INFINEON_AURIX2G)
  - `G9CH14` (来源: INFINEON_AURIX2G)
  - `G9CH15` (来源: INFINEON_AURIX2G)
  - `G10CH0` (来源: INFINEON_AURIX2G)
  - `G10CH1` (来源: INFINEON_AURIX2G)
  - `G10CH2` (来源: INFINEON_AURIX2G)
  - `G10CH3` (来源: INFINEON_AURIX2G)
  - `G10CH4` (来源: INFINEON_AURIX2G)
  - `G10CH5` (来源: INFINEON_AURIX2G)
  - `G10CH6` (来源: INFINEON_AURIX2G)
  - `G10CH7` (来源: INFINEON_AURIX2G)
  - `G10CH8` (来源: INFINEON_AURIX2G)
  - `G10CH9` (来源: INFINEON_AURIX2G)
  - `G10CH10` (来源: INFINEON_AURIX2G)
  - `G10CH11` (来源: INFINEON_AURIX2G)
  - `G11CH0` (来源: INFINEON_AURIX2G)
  - `G11CH1` (来源: INFINEON_AURIX2G)
  - `G11CH2` (来源: INFINEON_AURIX2G)
  - `G11CH3` (来源: INFINEON_AURIX2G)
  - `G11CH4` (来源: INFINEON_AURIX2G)
  - `G11CH5` (来源: INFINEON_AURIX2G)
  - `G11CH6` (来源: INFINEON_AURIX2G)
  - `G11CH7` (来源: INFINEON_AURIX2G)
  - `G11CH8` (来源: INFINEON_AURIX2G)
  - `G11CH9` (来源: INFINEON_AURIX2G)
  - `G11CH10` (来源: INFINEON_AURIX2G)
  - `G11CH11` (来源: INFINEON_AURIX2G)
  - `G11CH12` (来源: INFINEON_AURIX2G)
  - `G11CH13` (来源: INFINEON_AURIX2G)
  - `G11CH14` (来源: INFINEON_AURIX2G)
  - `G11CH15` (来源: INFINEON_AURIX2G)
- **描述**: Analog Input Channel Number.There are upto 8 analog inputs for each Primary Kernel and upto 16 analog inputs for each Secondary Kernel.

######## 5. AdcInputClassSelection

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2409d6`
- **参数名**: `AdcInputClassSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_HWUNIT_CLASS_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_HWUNIT_CLASS_0` (来源: INFINEON_AURIX2G)
  - `ADC_HWUNIT_CLASS_1` (来源: INFINEON_AURIX2G)
  - `ADC_GLOBAL_CLASS_0` (来源: INFINEON_AURIX2G)
  - `ADC_GLOBAL_CLASS_1` (来源: INFINEON_AURIX2G)
- **描述**: defines the input class for the analog channel. Input class determines the channel conversion properties like sample time and data conversion mode for each channel.

######## 6. AdcBWDPrechargeLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2409d7`
- **参数名**: `AdcBWDPrechargeLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_BWD_PRECH_VAGND`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_BWD_PRECH_VAGND` (来源: INFINEON_AURIX2G)
  - `ADC_BWD_PRECH_VAREF` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the VAREF/VAGND pre-charging for the broken wire detection channel.

######## 7. AdcMultiplexerDiagnosticLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0550f2409d7`
- **参数名**: `AdcMultiplexerDiagnosticLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_MD_PULL_DOWN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_MD_PULL_DOWN` (来源: INFINEON_AURIX2G)
  - `ADC_MD_PULL_UP` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the Multiplexer diagnostics level for the channel.

######## 8. AdcConverterDiagnosticsLevel

- **UUID**: `ECUC:7e0e69e5-6654-4264-a9b3-f0559f2009d7`
- **参数名**: `AdcConverterDiagnosticsLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_CD_PULL_DEVICE_VDDM`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_CD_PULL_DEVICE_VDDM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_VSSM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_HALF_VDDM` (来源: INFINEON_AURIX2G)
  - `ADC_CD_PULL_DEVICE_TWOTHIRD_VDDM` (来源: INFINEON_AURIX2G)
- **描述**: Parameter determines the Converter diagnostics level for the channel.

##### 6. AdcGroup

**容器属性**:

- **UUID**: `ECUC:21b450f5-989b-4095-a451-d237d777751c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGroup`
- **多重性**: [1..32]

**容器描述**:

This container contains the Group configuration (parameters).

###### 参数配置

此容器包含 **19** 个参数：

####### INTEGER 类型参数

######## 1. AdcGroupId

- **UUID**: `ECUC:65e3660c-73a4-4172-8d28-4edb71e96153`
- **参数名**: `AdcGroupId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..383]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Numeric Id of the ADC channel group.  This value will be assigned to the symbolic name derived of the AdcGroup containers short name. The range of IDs for each ADC Hw Unit:
                                    ADC0: 0 to 31, ADC1: 32 to 63, ADC2: 64 to 95, ADC3: 96 to 127, ADC4: 128 to 159, ADC5: 160 to 191, ADC6: 192 to 223, ADC7: 224 to 255, ADC8: 256 to 287
                                    ADC9: 288 to 319, ADC10: 320 to 351, ADC11: 352 to 383
                                  Recommendation  : Use AUTO-CALCULATE-VALUE option for all nodes AdcGroupId

######## 2. AdcGroupPriority

- **UUID**: `ECUC:c3c0273d-3fbb-48ea-b64a-6c6592d6a05c`
- **参数名**: `AdcGroupPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Priority level of the AdcGroup.

######## 3. AdcHwTrigTimer

- **UUID**: `ECUC:ac85f536-5cf6-43f3-a6a7-d824eed38461`
- **参数名**: `AdcHwTrigTimer`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..1023]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Reload value of the ADC module embedded timer (only if supported by ADC hardware).

######## 4. AdcStreamingNumSamples

- **UUID**: `ECUC:ba5e660f-1505-40bb-9b17-7ce8a5655235`
- **参数名**: `AdcStreamingNumSamples`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of ADC values to be acquired per channel in streaming access mode.

######## 5. AdcChannel0Alias

- **UUID**: `ECUC:8ea93903-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcChannel0Alias`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter configures the alias channel to be used for Channel 0.

######## 6. AdcChannel1Alias

- **UUID**: `ECUC:8ea93913-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcChannel1Alias`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter configures the alias channel to be used for Channel 1.

######## 7. AdcEmuxStartSelection

- **UUID**: `ECUC:bb7a337b-c160-470a-8b8f-bc8bd4b16a7b`
- **参数名**: `AdcEmuxStartSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the EMUX start selection.

######## 8. AdcResRegDefinition

- **UUID**: `ECUC:ea7f8f6d-5d98-4bc4-321e-dc02c4c233fc`
- **参数名**: `AdcResRegDefinition`
- **数据类型**: INTEGER
- **多重性**: [1..16]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the result register used for storing the result of this particular ADC conversion. This value of this parameter should be in descending order for the nodes of AdcGroupDefinition.

####### BOOLEAN 类型参数

######## 1. AdcEmuxChGroup

- **UUID**: `ECUC:29e7f838-395d-461f-9e5d-541c0cb3d670`
- **参数名**: `AdcEmuxChGroup`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines whether Group is EMUX or not.

####### ENUMERATION 类型参数

######## 1. AdcGroupAccessMode

- **UUID**: `ECUC:faad1eb6-43b4-4195-bacc-6245556acb07`
- **参数名**: `AdcGroupAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_ACCESS_MODE_SINGLE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_ACCESS_MODE_SINGLE` (来源: AUTOSAR_ECUC)
  - `ADC_ACCESS_MODE_STREAMING` (来源: AUTOSAR_ECUC)
- **描述**: Type of access mode to group conversion results.

######## 2. AdcGroupConversionMode

- **UUID**: `ECUC:25721d0a-d8a7-4ea3-96ab-49ced3030fce`
- **参数名**: `AdcGroupConversionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_CONV_MODE_ONESHOT`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_CONV_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `ADC_CONV_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **描述**: Type of conversion mode supported by the driver.

######## 3. AdcGroupReplacement

- **UUID**: `ECUC:f348b1d0-aabc-46ee-a71a-02cc6e49dca6`
- **参数名**: `AdcGroupReplacement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GROUP_REPL_ABORT_RESTART`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_GROUP_REPL_ABORT_RESTART` (来源: AUTOSAR_ECUC)
  - `ADC_GROUP_REPL_SUSPEND_RESUME` (来源: AUTOSAR_ECUC)
- **描述**: Replacement mechanism, which is used on ADC group level, if a group conversion is interrupted by a group which has a higher priority.

######## 4. AdcGroupTriggSrc

- **UUID**: `ECUC:1fb3e310-c03a-4a29-b2d2-f8d71765c6fc`
- **参数名**: `AdcGroupTriggSrc`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_TRIGG_SRC_SW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_TRIGG_SRC_HW` (来源: AUTOSAR_ECUC)
  - `ADC_TRIGG_SRC_SW` (来源: AUTOSAR_ECUC)
- **描述**: Type of source event that starts a group conversion.

######## 5. AdcHwTrigSignal

- **UUID**: `ECUC:70c09b6d-3cac-4db1-bee8-aafef6b9d2cf`
- **参数名**: `AdcHwTrigSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_HW_TRIG_RISING_EDGE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_HW_TRIG_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **描述**: Configures on which edge of the hardware trigger signal the driver should react, i.e. start the conversion (only if supported by the ADC hardware).

######## 6. AdcStreamingBufferMode

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf2-d2575ef9e9c8`
- **参数名**: `AdcStreamingBufferMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_STREAM_BUFFER_LINEAR`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_STREAM_BUFFER_CIRCULAR` (来源: AUTOSAR_ECUC)
  - `ADC_STREAM_BUFFER_LINEAR` (来源: AUTOSAR_ECUC)
- **描述**: Configure streaming buffer as "linear buffer" (i.e. the ADC Driver stops the conversion as soon as the stream buffer is full) or as "ring buffer" (wraps around if the end of the stream buffer is reached).

######## 7. AdcHwExtTrigSelect

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-2af2-d2575ef9e9c8`
- **参数名**: `AdcHwExtTrigSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_TRIG_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_TRIG_NONE` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_0_GxREQTRA_CCU60_SR3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_1_GxREQTRB_CCU61_SR3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_2_GxREQTRC_HSPDM` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_3_GxREQTRD_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_4_GxREQTRE_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_5_GxREQTRF_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_6_GxREQTRG_GTM_ADCx_TRIG4` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_7_GxREQTRH_ERUIOUTx` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_8_GxREQTRI_GTM_ADCx_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_9_GxREQTRJ_GTM_ADCx_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_10_GxREQTRK_GTM_ADCx_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_11_GxREQTRL_GTM_ADCx_TRIG3` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_12_GxREQTRM_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_13_GxREQTRN_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_14_GxREQTRO_EVADC_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_TRIG_15_GxREQTRP_GxREQGTySEL` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW trigger source for the group.

######## 8. AdcHwExtGateSelect

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcHwExtGateSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GATE_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_GATE_NONE` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_0_GxREQGTA_GTM_ADCx_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_1_GxREQGTB_GTM_ADCx_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_2_GxREQGTC_CCU6061_TRIG0` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_3_GxREQGTD_CCU6061_TRIG1` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_4_GxREQGTE_CCU6061_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_5_GxREQGTF_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_6_GxREQGTG_GTM_ADCx_TRIG4` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_7_GxREQGTH_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_8_GxREQGTI_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_9_GxREQGTJ_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_10_GxREQGTK_GTM_ADCx_TRIG2` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_11_GxREQGTL_GTM_ADCx_TRIG3` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_12_GxREQGTM_ERUPDOUTx` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_13_GxREQGTN_UNUSED` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_14_GxREQGTO_UNUSED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW gating source for the group.

######## 9. AdcHwGateSignal

- **UUID**: `ECUC:8ea9390c-d8f5-44c3-baf1-d2575ef9e9c8`
- **参数名**: `AdcHwGateSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_GATE_LVL_HIGH`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_GATE_LVL_HIGH` (来源: INFINEON_AURIX2G)
  - `ADC_GATE_LVL_LOW` (来源: INFINEON_AURIX2G)
- **描述**: This parameter configures the HW gating signal level.

####### FUNCTION-NAME 类型参数

######## 1. AdcNotification

- **UUID**: `ECUC:f43bffda-8d3a-4520-b424-b558fcbe752c`
- **参数名**: `AdcNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `IoHwAb_AdcNotification0`
- **描述**: Callback function for each group

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. AdcGroupDefinition

- **UUID**: `ECUC:fc412877-d8ab-4b65-96e8-0498ac13762e`
- **引用名**: `AdcGroupDefinition`
- **引用类型**: REFERENCE
- **多重性**: [1..16]
- **目标**: `AdcChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit/AdcChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Assignment of AdcChannels to a AdcGroups.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. EruTriggerConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruTriggerConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e69e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

########## 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e900-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

####### 2. EruGatingConfig

**容器属性**:

- **UUID**: `83452075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruGatingConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU Gating

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e39e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e911-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

########## 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e780-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

####### 3. GtmTriggerTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTriggerTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for TRIGGER. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb114e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

########## 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e0aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l6b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 4. GtmGatingTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2213a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmGatingTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for GATING. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb664e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

########## 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e1aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-1db7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3685`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 7. EruTriggerConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruTriggerConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e69e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

######## 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e900-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

##### 8. EruGatingConfig

**容器属性**:

- **UUID**: `83452075-2689-470a-b302-a6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EruGatingConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU Gating

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. AdcEruErsInputPin

- **UUID**: `ECUC:7e0e39e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `AdcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_REQ0A_PORTS_P15_4_SEL0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_REQ0A_PORTS_P15_4_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0B_CCU60_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0C_PORTS_P10_7_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0D_MSC0_FCLP_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0E_STM5_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ0F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1A_PORTS_P14_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1B_CCU61_COUT60_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1C_PORTS_P10_8_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1D_STM0_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ1F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2A_PORTS_P10_2_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2B_PORTS_P02_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2C_PORTS_P00_4_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2D_ERAY0_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ2F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3A_PORTS_P10_3_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3B_PORTS_P14_1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3C_PORTS_P02_0_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3D_STM1_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ3F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4A_PORTS_P33_7_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4B_GTM_TOM0_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4C_GPT120_T3OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4D_PORTS_P15_5_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ4F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5A_PORTS_P15_8_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5B_GTM_TOM1_12_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5C_GPT120_T6OUT_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5D_STM2_STMIR0_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5E_Reserved_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ5F_Reserved_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6A_PORTS_P20_0_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6B_PORTS_ESR0_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6C_Reserved_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6D_PORTS_P11_10_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6E_STM3_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ6F_GTM_TOM2_12_SEL5` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7A_PORTS_P20_9_SEL0` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7B_PORTS_ESR1_SEL1` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7C_PORTS_P15_1_SEL2` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7D_ERAY1_MT_SEL3` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7E_STM4_STMIR0_SEL4` (来源: INFINEON_AURIX2G)
  - `ERS_REQ7F_GTM_TOM3_12_SEL5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. AdcEruErsRef

- **UUID**: `ECUC:66c8e911-6197-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruErsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

######## 2. AdcEruOguRef

- **UUID**: `ECUC:66c8e780-6193-42a3-8125-a695cc21788e`
- **引用名**: `AdcEruOguRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the AdcHwUnitId.

##### 9. GtmTriggerTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTriggerTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for TRIGGER. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb114e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

######## 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e0aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

####### ENUMERATION 类型参数

######## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l6b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 10. GtmGatingTimerConfig

**容器属性**:

- **UUID**: `ECUC:c2213a76-e0d8-4a8f-b303-ce70ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmGatingTimerConfig`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this AdcGroup for GATING. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. GtmTimerTimePeriod

- **UUID**: `c6a84657-cf20-43cf-8e24-9cb664e0aa1c`
- **参数名**: `GtmTimerTimePeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20000`
- **取值范围**: [0..65536000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter is used for selecting the time period of the GTM timer in micro seconds.

######## 2. GtmTimerCM0Ticks

- **UUID**: `c6a84657-cf20-43cf-8e14-9cb114e1aa1c`
- **参数名**: `GtmTimerCM0Ticks`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.

####### ENUMERATION 类型参数

######## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-1db7-d0909f1440f2`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3685`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 11. AdcDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:4c697a37-02d8-42df-8696-0c9f592108c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId symbolic name.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. AdcClcFailureNotification

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695aa21788e`
- **引用名**: `AdcClcFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to configured DEM event to report CLC Failure.

######## 2. AdcConvStopTimeNotification

- **UUID**: `ECUC:66c8e900-6217-42a3-8125-a695aa21788e`
- **引用名**: `AdcConvStopTimeNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to configured DEM event to report, wait counts configured at AdcMaxChConvTimeCount to stop the conversion is not sufficient.

##### 12. AdcGeneral

**容器属性**:

- **UUID**: `ECUC:da0aaff6-3ed6-4a15-824e-dc32f3a8bd93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGeneral`
- **多重性**: [0..1]

**容器描述**:

General configuration (parameters) of the ADC Driver software module.

###### 参数配置

此容器包含 **28** 个参数：

####### INTEGER 类型参数

######## 1. AdcMaxChConvTimeCount

- **UUID**: `ECUC:ea7f8f6d-5d98-4bc4-808e-dc02c4c233fc`
- **参数名**: `AdcMaxChConvTimeCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16962]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: On stop of conversion request, the ongoing channel conversion in the A/D converter cannot be stopped immediately. Instead the software needs to wait for the channel conversion to get over. Inorder to ensure the converter is idle, a wait on coverter status polling is required and its maximum wait time is defined by the value entered in the AdcMaxChConvTimeCount

####### BOOLEAN 类型参数

######## 1. AdcDeInitApi

- **UUID**: `ECUC:16c0e8fd-6160-4ffb-b5a0-0fa22757dbae`
- **参数名**: `AdcDeInitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Adc_DeInit() from the code.

######## 2. AdcDevErrorDetect

- **UUID**: `ECUC:db321b92-621a-4a62-8778-09b8845d8f2c`
- **参数名**: `AdcDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 3. AdcSafetyEnable

- **UUID**: `ECUC:412da385-6bf4-4819-11e4-8ec223fb5b17`
- **参数名**: `AdcSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enable/Disable the Safety check and all associated notifications.

######## 4. AdcMultiCoreErrorDetect

- **UUID**: `ECUC:dbfab416-7231-4c5e-a7a2-2580d8484ece`
- **参数名**: `AdcMultiCoreErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Adds / removes the Multicore error detection feature from the code.

######## 5. AdcInitCheckApi

- **UUID**: `ECUC:dbfab416-7231-4c9e-b7a2-2580d8484ecf`
- **参数名**: `AdcInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Adds / removes the service Adc_InitCheck() from the code.

######## 6. AdcEnableLimitCheck

- **UUID**: `ECUC:36543fc4-cdc1-453b-9706-844d76e6fa30`
- **参数名**: `AdcEnableLimitCheck`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables or disables limit checking feature in the ADC driver.

######## 7. AdcEnableQueuing

- **UUID**: `ECUC:cf5318b5-011b-4128-8393-02dd46fe52b5`
- **参数名**: `AdcEnableQueuing`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines, if the queuing mechanism is active in case of priority mechanism disabled.

######## 8. AdcEnableStartStopGroupApi

- **UUID**: `ECUC:94b12c2c-4231-424c-90c9-a55ee72663fe`
- **参数名**: `AdcEnableStartStopGroupApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the services Adc_StartGroupConversion() and Adc_StopGroupConversion() from the code.

######## 9. AdcGrpNotifCapability

- **UUID**: `ECUC:b2cfcb7b-0a84-4c50-bebd-32ee405e4300`
- **参数名**: `AdcGrpNotifCapability`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines, if the group notification mechanism (the functions to enable and disable the notifications) is available at runtime.

######## 10. AdcHwTriggerApi

- **UUID**: `ECUC:e5c85e73-38e2-47ae-81e9-c39d1b361249`
- **参数名**: `AdcHwTriggerApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the services Adc_EnableHardwareTrigger() and Adc_DisableHardwareTrigger() from the code.

######## 11. AdcReadGroupApi

- **UUID**: `ECUC:6fe4295d-02b9-4c34-b9f2-337c2df6bd58`
- **参数名**: `AdcReadGroupApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Adc_ReadGroup() and from the code.

######## 12. AdcVersionInfoApi

- **UUID**: `ECUC:8ea4cb56-cf5e-4afc-95ce-cebac08ac0e6`
- **参数名**: `AdcVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Adc_GetVersionInfo() from the code.

######## 13. AdcStartupCalibApi

- **UUID**: `ECUC:8ea42236-cf5e-4afc-95ce-cebac08ac0e6`
- **参数名**: `AdcStartupCalibApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Adds / removes the service Adc_GetStartupCalStatus() and Adc_TriggerStartupCal() from the code.

######## 14. AdcTriggerOneConversionEnable

- **UUID**: `ECUC:8ea42236-cf5e-4afc-11ce-c1bac08ac0e6`
- **参数名**: `AdcTriggerOneConversionEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter enables the execution of one dummy conversion for each configured HW unit, before start-up calibration is triggered in the API Adc_TriggerStartupCal(). Refer Errata ADC_TC.083

######## 15. AdcSyncConvEnable

- **UUID**: `ECUC:8ea42236-cf5e-4afc-15ce-cebac08ac0e6`
- **参数名**: `AdcSyncConvEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables the synchronous conversions across ADC HW groups.

######## 16. AdcLowPowerStatesSupport

- **UUID**: `ECUC:c44c41aa-bff4-460d-980a-79bde5bad6c5`
- **参数名**: `AdcLowPowerStatesSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes all power state management related APIs (ADC_SetPowerState, ADC_GetCurrentPowerState, ADC_GetTargetPowerState, ADC_PreparePowerState), indicating if the HW offers low power state management.

######## 17. AdcPowerStateAsynchTransitionMode

- **UUID**: `ECUC:01a8d9c1-3bfd-4b88-8ab6-7d5bebca802c`
- **参数名**: `AdcPowerStateAsynchTransitionMode`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / disables support of the ADCDriver to the asynchronous power state transition.

######## 18. AdcEmuxEnable

- **UUID**: `ECUC:22d6d867-a427-46d4-a39a-452a5e0e90f2`
- **参数名**: `AdcEmuxEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Determines, if the EMUX is used.

####### ENUMERATION 类型参数

######## 1. AdcPriorityImplementation

- **UUID**: `ECUC:7e0e69e5-6004-4264-a9b3-f0559f2409d6`
- **参数名**: `AdcPriorityImplementation`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_PRIORITY_NONE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_PRIORITY_NONE` (来源: AUTOSAR_ECUC)
  - `ADC_PRIORITY_HW` (来源: AUTOSAR_ECUC)
  - `ADC_PRIORITY_HW_SW` (来源: AUTOSAR_ECUC)
- **描述**: Determines whether a priority mechanism is available for prioritization of the conversion requests and if available, the type of prioritization mechanism. The selection applies for groups with trigger source software and trigger source hardware. Two

######## 2. AdcResultHandlingImplementation

- **UUID**: `ECUC:7e0e69e5-6004-1956-22b3-f0559f2409d6`
- **参数名**: `AdcResultHandlingImplementation`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_INTERRUPT_MODE_RESULT_HANDLING`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_INTERRUPT_MODE_RESULT_HANDLING` (来源: INFINEON_AURIX2G)
  - `ADC_DMA_MODE_RESULT_HANDLING` (来源: INFINEON_AURIX2G)
- **描述**: Determines the result handling mode for the ADC driver.ADC_INTERRUPT_MODE_RESULT_HANDLING: Conversion results are transferred in the Request Source ISR (AUTOSAR Mode).                       ADC_DMA_MODE_RESULT_HANDLING: Conversion results are transferred using a DMA channel. ADC_POLLING_MODE_RESULT_HANDLING: Conversion results are transferred using synchronous APIs.

######## 3. AdcResultAlignment

- **UUID**: `ECUC:b269a17e-8b68-4182-8879-338205ac27ca`
- **参数名**: `AdcResultAlignment`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_ALIGN_RIGHT`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_ALIGN_LEFT` (来源: AUTOSAR_ECUC)
  - `ADC_ALIGN_RIGHT` (来源: AUTOSAR_ECUC)
- **描述**: Alignment of ADC raw results in ADC result buffer (left/right alignment).

######## 4. AdcSleepMode

- **UUID**: `ECUC:b269a17e-8b68-4282-8879-338205ac271a`
- **参数名**: `AdcSleepMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_SLEEP_MODE_ACCEPT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_SLEEP_MODE_ACCEPT` (来源: INFINEON_AURIX2G)
  - `ADC_SLEEP_MODE_REJECT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines whether, ADC Driver accepts or rejects the sleep mode request from SCU.

######## 5. AdcSupplyVoltage

- **UUID**: `ECUC:b269a17e-8b68-4282-8871-338205ac271a`
- **参数名**: `AdcSupplyVoltage`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_VOLTAGE_CONTROLLED_BY_SUPPLY`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_VOLTAGE_CONTROLLED_BY_SUPPLY` (来源: INFINEON_AURIX2G)
  - `ADC_VOLTAGE_5V` (来源: INFINEON_AURIX2G)
  - `ADC_VOLTAGE_3P3V` (来源: INFINEON_AURIX2G)
- **描述**: This parameter adjusts the analog circuitry to the selected supply voltage.

######## 6. AdcRuntimeApiMode

- **UUID**: `ECUC:7e0e69e5-6004-1956-2213-f0559f2409d6`
- **参数名**: `AdcRuntimeApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `ADC_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: Defines the privilege mode in which the runtime APIs would operate.

######## 7. AdcInitDeInitApiMode

- **UUID**: `ECUC:7e0e69e5-6004-1956-a113-f0559f2409d6`
- **参数名**: `AdcInitDeInitApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `ADC_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: Defines the privilege mode in which the Initialization and De-initialization APIs would operate.

######## 8. AdcEmuxGroupInterface0

- **UUID**: `ECUC:43e34dae-996e-48e1-b1e0-3ffb30bb6f78`
- **参数名**: `AdcEmuxGroupInterface0`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `HWUNIT_ADC0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `HWUNIT_ADC0` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC1` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC2` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC3` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC4` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC8` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC9` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC10` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC11` (来源: INFINEON_AURIX2G)
- **描述**: Description: Numeric ID of the HW Unit. This symbolic name allows accessing Hw Unit data. Enumeration literals are defined vendor specific.

######## 9. AdcEmuxGroupInterface1

- **UUID**: `ECUC:522be67d-c9c5-4c4c-87ff-15142355e2ff`
- **参数名**: `AdcEmuxGroupInterface1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `HWUNIT_ADC1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `HWUNIT_ADC0` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC1` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC2` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC3` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC4` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC8` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC9` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC10` (来源: INFINEON_AURIX2G)
  - `HWUNIT_ADC11` (来源: INFINEON_AURIX2G)
- **描述**: Description: Numeric ID of the HW Unit. This symbolic name allows accessing Hw Unit data. Enumeration literals are defined vendor specific.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. AdcPowerStateConfig

**容器属性**:

- **UUID**: `ECUC:5cd16e43-9c9f-4be1-933d-cc22cd917ec0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcPowerStateConfig`
- **多重性**: [0..4]

**容器描述**:

Each instance of this parameter defines a power state and the callback to be called when this power state is reached.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. AdcPowerState

- **UUID**: `ECUC:7b71ca9d-846d-4ebe-bb34-f0defbf45e09`
- **参数名**: `AdcPowerState`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..3]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Each instance of this parameter describes a different power state supported by the ADC HW. It should be defined by the HW supplier and used by the ADCDriver to reference specific HW configurations which set the  ADC HW module in the referenced power state.

######### FUNCTION-NAME 类型参数

########## 1. AdcPowerStateReadyCbkRef

- **UUID**: `ECUC:13cdc2fe-cf3c-4a68-93cb-a3676a293fd3`
- **参数名**: `AdcPowerStateReadyCbkRef`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Each instance of this parameter contains a reference to a power mode callback defined in a CDD or IoHwAbs component.

##### 13. AdcPowerStateConfig

**容器属性**:

- **UUID**: `ECUC:5cd16e43-9c9f-4be1-933d-cc22cd917ec0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcPowerStateConfig`
- **多重性**: [0..4]

**容器描述**:

Each instance of this parameter defines a power state and the callback to be called when this power state is reached.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. AdcPowerState

- **UUID**: `ECUC:7b71ca9d-846d-4ebe-bb34-f0defbf45e09`
- **参数名**: `AdcPowerState`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..3]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Each instance of this parameter describes a different power state supported by the ADC HW. It should be defined by the HW supplier and used by the ADCDriver to reference specific HW configurations which set the  ADC HW module in the referenced power state.

####### FUNCTION-NAME 类型参数

######## 1. AdcPowerStateReadyCbkRef

- **UUID**: `ECUC:13cdc2fe-cf3c-4a68-93cb-a3676a293fd3`
- **参数名**: `AdcPowerStateReadyCbkRef`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Each instance of this parameter contains a reference to a power mode callback defined in a CDD or IoHwAbs component.

##### 14. AdcPublishedInformation

**容器属性**:

- **UUID**: `ECUC:e435c52c-58b2-4506-ae6c-da9a9b76ad99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Additional published parameters not covered by Common Published Information. Note that these parameters have "PUBLISHED-INFORMATION" configuration class setting, since they are published information.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. AdcMaxChannelResolution

- **UUID**: `ECUC:8f00599e-47d5-4046-bce8-9cbefac7e41a`
- **参数名**: `AdcMaxChannelResolution`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `12`
- **取值范围**: [1..63]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum Channel resolution in bits (does not specify accuracy).

####### BOOLEAN 类型参数

######## 1. AdcChannelValueSigned

- **UUID**: `ECUC:f002ab5c-bf89-4fc2-ba13-6909a2c2e75a`
- **参数名**: `AdcChannelValueSigned`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Information whether the result value of the ADC driver has sign information (true) or not (false). If the result shall be interpreted as signed value it shall apply to C-language rules.

######## 2. AdcGroupFirstChannelFixed

- **UUID**: `ECUC:1c22f85b-d656-4563-86ec-1823df41ebed`
- **参数名**: `AdcGroupFirstChannelFixed`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Information whether the first channel of an ADC Channel group can be configured (false) or is fixed (true) to a value determined by the ADC HW Unit.

##### 15. CommonPublishedInformation

**容器属性**:

- **UUID**: `492f8482-3e2c-4bf1-b27f-01fd7ac35788`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CommonPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Common container, aggregated by all modules. It contains published information about vendor and versions.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. ArMajorVersion

- **UUID**: `bd0a8d38-4d8c-4ee9-88fe-1166b258bb8a`
- **参数名**: `ArMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 2. ArMinorVersion

- **UUID**: `73f87c7f-e230-4178-bff0-eb2704aae656`
- **参数名**: `ArMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 3. ArPatchVersion

- **UUID**: `2380135d-6778-417a-a34b-e10017d4dd54`
- **参数名**: `ArPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 4. SwMajorVersion

- **UUID**: `fca015e3-5f28-4cbe-8949-8f4b87d86827`
- **参数名**: `SwMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 5. SwMinorVersion

- **UUID**: `14ab81e0-3d80-43dc-8b92-247e5a542df9`
- **参数名**: `SwMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 6. SwPatchVersion

- **UUID**: `32e37bfd-18b6-41d1-9248-a81dbe0fe4c5`
- **参数名**: `SwPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 7. ModuleId

- **UUID**: `3b407478-6902-4f80-b7cf-f33b0854e638`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `123`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Module ID of this module from Module List

######## 8. VendorId

- **UUID**: `7d650b2d-4adb-41f0-a68e-5f0c416501d1`
- **参数名**: `VendorId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `17`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Vendor ID of the dedicated implementation of this module according to the AUTOSAR vendor list

####### STRING 类型参数

######## 1. Release

- **UUID**: `3b407478-6902-4f40-b712-f33b0854e638`
- **参数名**: `Release`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `_TRICORE_TC397`
- **描述**: Aurix2G derivative used for the implementation

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AURIX2G

- **UUID**: `ECUC:AUTOSAR`
- **包名称**: `AURIX2G`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Adc**
