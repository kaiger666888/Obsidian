# Rtm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:54

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Rtm](#rtm)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Rtm

#### 基本信息

- **UUID**: `310051e4-b34e-4b60-8dae-4f7667be206d`
- **模块名称**: `Rtm`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [1..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-LINK-TIME

#### 模块描述

Runtime Measurement.
Rtm allows the user to determine runtimes and CPU load of BSW modules and user code sections. Measurement is controlled- and evaluated in CANoe by RTM's frontend or a self-written RTM application. Data exchange between CANoe and the ECU is done by the XCP protocol.
#AMD #Xcp #CANoe #CANape #Monitoring #RuntimeMeasurement
#Vector

#### 版本历史

共有 **29** 个版本记录：

##### 1. 版本 1.0.0

- **发布日期**: 2012-10-12T10:20:00Z
- **发布者**: visazb

**变更内容**:

##### 2. 版本 1.0.1

- **发布日期**: 2013-07-09T12:52:39+02:00
- **发布者**: visore

**变更内容**:

##### 3. 版本 1.1.0

- **发布日期**: 2014-05-21T02:10:33+02:00
- **发布者**: visore

**变更内容**:

##### 4. 版本 1.1.1

- **发布日期**: 2014-05-21T02:10:38+02:00
- **发布者**: visore

**变更内容**:

##### 5. 版本 1.2.0

- **发布日期**: 2014-10-13T12:09:00+02:00
- **发布者**: viszda

**变更内容**:

##### 6. 版本 1.2.1

- **发布日期**: 2014-11-14T12:09:00+02:00
- **发布者**: viszda

**变更内容**:

##### 7. 版本 1.2.2

- **发布日期**: 2015-06-17T12:43:20+02:00
- **发布者**: viszda

**变更内容**:

##### 8. 版本 2.0.0

- **发布日期**: 2016-04-05T10:37:24+02:00
- **发布者**: viszda

**变更内容**:

##### 9. 版本 2.1.0

- **发布日期**: 2016-05-10T11:30:06+02:00
- **发布者**: viszda

**变更内容**:

##### 10. 版本 2.2.0

- **发布日期**: 2016-09-05T10:52:07+02:00
- **发布者**: viszda

**变更内容**:

##### 11. 版本 3.0.0

- **发布日期**: 2017-04-04T09:07:55+02:00
- **发布者**: viszda

*此版本无详细变更记录*

##### 12. 版本 3.1.0

- **发布日期**: 2017-04-19T01:14:01+02:00
- **发布者**: viszda

**变更内容**:

##### 13. 版本 3.1.1

- **发布日期**: 2017-06-09T15:26:08+02:00
- **发布者**: viszda

**变更内容**:

##### 14. 版本 3.1.2

- **发布日期**: 2018-03-01T16:42:36+01:00
- **发布者**: viszda

**变更内容**:

##### 15. 版本 3.1.3

- **发布日期**: 2018-10-09T10:12:08+02:00
- **发布者**: viszda

**变更内容**:

##### 16. 版本 4.0.0

- **发布日期**: 2020-11-26T14:22:38+01:00
- **发布者**: viszda

**变更内容**:

##### 17. 版本 5.0.0

- **发布日期**: 2021-05-17T08:27:31+02:00
- **发布者**: viszda

**变更内容**:

##### 18. 版本 6.0.0

- **发布日期**: 2021-05-17T08:34:52+02:00
- **发布者**: viszda

**变更内容**:

##### 19. 版本 6.1.0

- **发布日期**: 2021-06-16T07:16:23+02:00
- **发布者**: viszda

**变更内容**:

##### 20. 版本 6.2.0

- **发布日期**: 2021-08-09T08:26:24+02:00
- **发布者**: viszda

**变更内容**:

##### 21. 版本 7.0.0

- **发布日期**: 2021-09-27T08:00:26+02:00
- **发布者**: viszda

**变更内容**:

##### 22. 版本 7.1.0

- **发布日期**: 2021-11-23T07:31:01+01:00
- **发布者**: viszda

**变更内容**:

##### 23. 版本 8.0.0

- **发布日期**: 2022-04-12T12:22:12+02:00
- **发布者**: viszda

**变更内容**:

##### 24. 版本 8.0.1

- **发布日期**: 2022-07-16T11:00:10+02:00
- **发布者**: viszda

**变更内容**:

##### 25. 版本 9.0.0

- **发布日期**: 2022-09-26T08:45:21+02:00
- **发布者**: viszda

**变更内容**:

##### 26. 版本 9.1.0

- **发布日期**: 2022-11-16T08:49:17+01:00
- **发布者**: viszda

**变更内容**:

##### 27. 版本 9.1.1

- **发布日期**: 2023-02-13T09:10:38+01:00
- **发布者**: viszda

**变更内容**:

##### 28. 版本 10.0.0

- **发布日期**: 2023-07-04T10:54:23+02:00
- **发布者**: mgourabathi

**变更内容**:

##### 29. 版本 11.0.0

- **发布日期**: 2023-10-27T15:01:53+02:00
- **发布者**: mgourabathi

**变更内容**:

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. RtmGeneral

**容器属性**:

- **UUID**: `f7e11089-cf24-4557-8552-f6312177a4b5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RtmGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

General configuration parameters of the RTM.

###### 参数配置

此容器包含 **13** 个参数：

####### INTEGER 类型参数

######## 1. RtmMeasurementCtrFrequency

- **UUID**: `79646f7f-5da9-401c-8552-7c8a581c7403`
- **参数名**: `RtmMeasurementCtrFrequency`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10000`
- **取值范围**: [1000..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Number of ticks per [ms] provided by the hardware timer.

The frequency of the hardware timer used to acquire measurement timestamps has to be adjusted to provide a compromise between accuracy and maximal measurement duration.

If the timer has a frequency of 10MHz, then this parameter shall be set to 10000[Ticks/ms].

A higher frequency results in higher measurement accuracy but will also shorten the period which can be measured.

######## 2. RtmUsedCoreMask

- **UUID**: `0d49ed3f-e0d6-4c96-b709-92317eca80a3`
- **参数名**: `RtmUsedCoreMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specifies selection of cores to be measured.

This parameter must not be changed!
It is calculated automatically.

####### BOOLEAN 类型参数

######## 1. RtmDevErrorDetect

- **UUID**: `48da4d9e-31a2-4365-bbcd-9d92d1f8b142`
- **参数名**: `RtmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.
true:	Development error detection is enabled.
false:	Development error detection is disabled.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

######## 2. RtmTimerOverrunSupport

- **UUID**: `8baa44da-7888-4b4e-a4c1-816dc5d7e71b`
- **参数名**: `RtmTimerOverrunSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter switches the Support for Timer Overruns ON or OFF.
true:	Timer Overrun Handling is enabled.
false:	Timer Overrun Handling is disabled.

######## 3. Rtm32BitTimer

- **UUID**: `cb7ea73c-62a2-4c22-8a60-1047664f3e2a`
- **参数名**: `Rtm32BitTimer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if 32bit timer is used.
If set to true: a 32bit timer is used
If set to false: a 16bit timer is used

######## 4. RtmUseNestingCounter

- **UUID**: `e0fbab9a-7bf9-4012-a6da-f12baf5cf592`
- **参数名**: `RtmUseNestingCounter`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The nesting counter is used to detect successive activation of a measurement point before stopping.

######## 5. RtmControl

- **UUID**: `bec5a130-9142-4661-a37e-f74acc3b6415`
- **参数名**: `RtmControl`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the global variable Rtm_ControlState is provided which allows disabling and enabling the RTM functionality during runtime. The feature may be used to prevent unintended RTM activity by disabling the functionality on a special trigger.

If this option is disabled RTM will always be activated in the ECU.

######## 6. RtmSafeBswChecks

- **UUID**: `dacd3398-cd71-426c-84b4-2342600ad5db`
- **参数名**: `RtmSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

####### FLOAT 类型参数

######## 1. RtmMainfunctionCycleTime

- **UUID**: `db1f715d-bc84-44b6-85de-5a1c67a80a59`
- **参数名**: `RtmMainfunctionCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Cycle time of RTM main function.

A value of 0.01 [s] is recommended.
Lower values result in higher update-rates during live measurement but also require more bandwidth to transmit the measurement results.
Higher values may lead to erroneous results if the main function's cycle time has a jitter larger than a half of the hardware counters cycle time.

####### STRING 类型参数

######## 1. RtmGetMeasurementTimestampFct

- **UUID**: `8c18d2cd-ea1e-4a6c-9a61-c56165db19bd`
- **参数名**: `RtmGetMeasurementTimestampFct`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Rtm_GetTimeMeasurement`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the function or macro that shall be used by RTM to acquire the current value of a hardware counter. The prototype will be defined in Rtm_Cbk.h.

This function has to be provided by the application.
Prototype: Rtm_TimestampType Rtm_GetTimeMeasurement(void);
The return type Rtm_TimestampType depends on the parameter Rtm32BitTimer.

######## 2. RtmUserConfigFile

- **UUID**: `d59f7040-c2a7-43fd-879c-f357d1f582dd`
- **参数名**: `RtmUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A configuration file is generated by Cfg5. If you want to overwrite settings in the generated configuration file, you can specify a path to a user defined configuration file.

Note: The user defined configuration file will be included at the end of the generated file. Therefore definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The contents of the user defined configuration file is copied to the end of <Bsw>_Cfg.h.

######## 3. RtmEcuName

- **UUID**: `cf3ec9d7-c033-4e9b-b8da-1eec6e2ab0b4`
- **参数名**: `RtmEcuName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Rtm`
  - 最大长度: 50
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the ECU name within the XCP settings of CANoe.

####### ENUMERATION 类型参数

######## 1. RtmCtrDirection

- **UUID**: `12dea9f0-8ff4-4628-857e-6df07acd663f`
- **参数名**: `RtmCtrDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `RTM_UP`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RTM_UP`
  - `RTM_DOWN`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the counting direction of the hardware counter:
-RTM_UP: 0 to MAXVAL
-RTM_DOWN: MAXVAL to 0

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. RtmNvMTaskStackUsage

- **UUID**: `3cd199e6-8fa8-4e8f-bea7-9516282d3733`
- **引用名**: `RtmNvMTaskStackUsage`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This optional reference can be used to persist the task stack usage in the NvM.

######## 2. RtmNvMResults

- **UUID**: `9e943397-b48a-48b9-8a41-003d0c160ca4`
- **引用名**: `RtmNvMResults`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This optional reference can be used to persist all measurement results (Rtm_Results[]: uint32 time, uint32 count, uint32 min, uint32 max) as raw values (in ticks) in the NvM.

##### 2. RtmMeasurementPoint

**容器属性**:

- **UUID**: `7f99b07a-a665-4755-9f0c-d0a1261e953a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RtmMeasurementPoint`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Each measurement point describes one code area whose runtime shall be measured using the RTM module.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. RtmMeasurementId

- **UUID**: `b5a5b9a6-feb5-44b1-8632-d12318e79bf3`
- **参数名**: `RtmMeasurementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This ID defines the measurement object

######## 2. RtmTargetRuntime

- **UUID**: `6288da16-9524-4b0e-86ad-8d5ad3eeca35`
- **参数名**: `RtmTargetRuntime`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1000000]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter determines the target (respectively the expected) runtime of the Measurement Point (MP).

In the following use cases this value must be defined (greater than 0):
1. For /RtmThresholdCallback it defines when the callback is called.
2. For the calculation of relative maximum measurement results.
3. For LET MPs (configured by RTE) it is used to calculate the relative remaining time.
4. For task response time MPs (/RtmMeasurementPointType set to 'Task'), this value defines the runtime required for the 100% percentile.

####### BOOLEAN 类型参数

######## 1. RtmAutostartEnabled

- **UUID**: `c8e84ea3-0e57-4146-97cf-3371c19b187b`
- **参数名**: `RtmAutostartEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines if this measurement shall be activated during ECU startup automatically.

Autostart may be used for init-functions which are called only during the startup-phase the communication stack, XCP and RTM module are activated. 

Note: Each autostart measurement causes CPU-load. It is therefore advised to activate autostart only when it is required.

######## 2. RtmMeasurementEnabled

- **UUID**: `aa3996ee-af77-46db-890f-d679a8f13913`
- **参数名**: `RtmMeasurementEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter defines the availability of a measurement section during pre-compile time. If disabled, the measurement points of this section will be generated as empty macros. Hence this measurement section requires no memory- or runtime resources. Since the measurement settings are still part of the ECU configuration, the measurement enabled settings can be changed later.

######## 3. RtmDisableInterrupts

- **UUID**: `a6fe8a46-4912-4df4-8165-0b45f9569f32`
- **参数名**: `RtmDisableInterrupts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines if interrupts are locked during measurement.

If enabled, RTM locks interrupts during measurement using the critical section RTM_EXCLUSIVE_AREA_0. This results in more accurate measurement results but will increase the time spent with locked interrupt.

######## 4. RtmThresholdCallback

- **UUID**: `6cb2c853-cd28-4687-9060-050d661acbde`
- **参数名**: `RtmThresholdCallback`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables the call of an application callback if the configured threshold (/RtmTargetRuntime) is elapsed between the last calls of Rtm_Start() and Rtm_Stop).

The name scheme of the callback is "Rtm_<NameOfTheMP>_ThresholdCbk(Rtm_MeasurementTimestampType executionTime)".

####### STRING 类型参数

######## 1. RtmMeasurementGroup

- **UUID**: `91ab80a0-62f2-4209-a69c-1c02454e17f0`
- **参数名**: `RtmMeasurementGroup`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Default`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The name can be used to organize measurement sections into groups by defining a unique group name. The groups will be visible in CANoe and the generated measurement report.

####### ENUMERATION 类型参数

######## 1. RtmMeasurementType

- **UUID**: `33f7a4ce-b3f4-4397-bcc0-819e2c9841b7`
- **参数名**: `RtmMeasurementType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `GrossExecutionTime`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `GrossExecutionTime` (来源: Vector Informatik)
  - `FlatExecutionTime` (来源: Vector Informatik)
  - `NetExecutionTime` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The measurement type defines the measurement behavior of this measurement point.
If set to GrossExecutionTime: 
  - Measures the absolute time between measurement start and stop.
If set to NetExecutionTime: 
  - Measures like GrossExecutionTime  minus interruptions by task or ISR.
If set to FlatExecutionTime:
  - Measures like NetExecutionTime minus the execution time of nested measurement points.

######## 2. RtmMeasurementPointType

- **UUID**: `9589273f-b12b-471e-9530-5c20cc8d67a7`
- **参数名**: `RtmMeasurementPointType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Runtime`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Runtime` (来源: Vector Informatik)
  - `Task` (来源: Vector Informatik)
  - `CPU_Load` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter defines whether the measurement point measures:
Runtime: Regular runtime measurement point.
Task: Task response time measurement point.
CPU_Load: Core specific CPU load measurement point.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. RtmAssignedToCore

- **UUID**: `42325c46-b158-467b-a6d4-b267852cfa84`
- **引用名**: `RtmAssignedToCore`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RtmCoreDefinition`
- **完整路径**: `/MICROSAR/Rtm/RtmCoreDefinition`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines on which core the Measurement Point is running.

##### 3. RtmCoreDefinition

**容器属性**:

- **UUID**: `6656b902-da39-4c8d-a778-eef2c034527b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RtmCoreDefinition`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: true

**容器描述**:

Each Measurement Point needs to have a core description assigned. The core description defines on which core the Measurement Point is running on. There is a special case when no /MICROSAR/Rtm/RtmCoreDefinition/RtmCore is configured. This is for cross core applications where a measurement is started on one core and stopped on another core.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. RtmCoreDefinitionId

- **UUID**: `d493f63b-0db3-4faa-89c6-70025915460f`
- **参数名**: `RtmCoreDefinitionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Symbolic Name Value of this container.

######## 2. RtmNumberOfTaskResponseTimePercentiles

- **UUID**: `6c75be44-f76c-45ec-b95b-66b32d812d59`
- **参数名**: `RtmNumberOfTaskResponseTimePercentiles`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [2..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: When this feature is enabled (value > 0) a percentile histogram is calculated and managed by the RTM. The histogram is divided in as many divisions as here configured exclusively the additional 200% percentile.
Example: If this parameter is set to 2, there is the 0-99%, the 100-199%, and the 200% percentiles.
Please note: This feature requires additional runtime and memory. The histogram can be persisted in NvM.

If this parameter does not exist, this feature is disabled.

######## 3. RtmCore

- **UUID**: `fb04033b-e4e4-4a05-b049-37e3b1d4de54`
- **参数名**: `RtmCore`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the core the application is running on. For cross core measurement, leave this field empty.

####### BOOLEAN 类型参数

######## 1. RtmBSWCore

- **UUID**: `bc747f48-b551-47c5-b520-f7004b969030`
- **参数名**: `RtmBSWCore`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This parameter defines whether this Core is running the BSW software. Only one Core Definition can have this flag set.

####### STRING 类型参数

######## 1. RtmBackgroundTaskName

- **UUID**: `fd8e3bbc-1669-4ef1-a1d1-a56d2b776d18`
- **参数名**: `RtmBackgroundTaskName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `BackgroundTaskName`
  - 最大长度: 511
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Name of the background/idle task of this core.
This parameter is only required for CPU load measurement.

Per default, the IdleTask_OsCore<CoreId> is the correct background/idle task, but it is possible to cover this task by a custom background/idle task implementing an endless loop. As this task has a higher priority, the IdleTask_OsCore<CoreId> will never be called. Therefore, the custom background/idle task shall be set here.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. RtmNvMTaskResponseTimePersistencyBlock

- **UUID**: `6db58b67-be2b-415d-adad-7d35c4bac3b4`
- **引用名**: `RtmNvMTaskResponseTimePersistencyBlock`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This optional reference can be used to persist histogram information in the NvM. The histogram information is available for each core seperately and therefore requires a NvM block for each core.

##### 4. RtmCpuLoadMeasurement

**容器属性**:

- **UUID**: `4742e5b7-e49d-4b1e-8ae8-c7bf6fae8181`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `RtmCpuLoadMeasurement`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

If this container exists, the CPU load measurement is enabled.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. RtmNumberOfCpuLoadPercentiles

- **UUID**: `8ff9c0ff-6cbc-4f94-a41d-372ece24f5e7`
- **参数名**: `RtmNumberOfCpuLoadPercentiles`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [2..99]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: When this feature is enabled (this parameter exists) a percentile histogram is calculated and managed by the RTM. The histogram is divided in as many divisions as here configured exclusively the additional 100% percentile.
Example: If this parameter is set to 2, there is the 0-49%, the 50-99%, and the 100% percentiles.
Please note: This feature requires additional runtime and memory. The histogram can be persisted in NvM.

If this parameter does not exist, this feature is disabled.

####### FLOAT 类型参数

######## 1. RtmHyperperiod

- **UUID**: `c33401b4-3be5-43ad-aba2-557ef6521e93`
- **参数名**: `RtmHyperperiod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..60]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the time frame of the histogram information. Needs to be a multiple of the Rtm Mainfunction Cycle Time.

####### ENUMERATION 类型参数

######## 1. RtmCpuLoadControlMode

- **UUID**: `b9f31a9a-706d-4411-a4ca-3be4b5c3eec9`
- **参数名**: `RtmCpuLoadControlMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `C_API`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `C_API` (来源: Vector Informatik)
  - `Xcp` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define how the Cpu load is measured and the measurement is controlled.
If set to "C_API", the Cpu load measurement is started and stopped and the results are requested with C APIs.
If set to "Xcp", the Cpu load is measured by a measurement point. This measurement point can be activated like all other measurement points.

Hint:
For this feature a measurement point called "Rtm_CpuLoadMeasurement" (resp. in multi core "Rtm_CpuLoadMeasurement_<CoreId>") has to exist and must be enabled in order to measure the overall CPU load.
Please note that this measurement point(s) should not be called by an application.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. RtmNvMCpuLoadPersistencyBlock

- **UUID**: `aeefedac-460b-4043-9b0c-bc414f9a20b6`
- **引用名**: `RtmNvMCpuLoadPersistencyBlock`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This optional reference can be used to persist the CPU load histogram information in the NvM.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Rtm**

##### BSW-IMPLEMENTATION 类型元素

1. **Rtm_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Rtm_Pre**
2. **Rtm_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Rtm_Impl

- **UUID**: `b1461bd1-4237-4cfa-9b71-f3458c755c59`
- **实现名称**: `Rtm_Impl`
- **编程语言**: C
- **软件版本**: 11.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.02.02
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Rtm_Pre

- **UUID**: `142a4365-3674-44c1-8ab3-23916844a5a9`
- **配置名称**: `Rtm_Pre`
- **定义引用**: `/MICROSAR/Rtm`

### 2. Rtm_Rec

- **UUID**: `601730a0-4eb4-429e-972d-19668bd59dc6`
- **配置名称**: `Rtm_Rec`
- **定义引用**: `/MICROSAR/Rtm`
