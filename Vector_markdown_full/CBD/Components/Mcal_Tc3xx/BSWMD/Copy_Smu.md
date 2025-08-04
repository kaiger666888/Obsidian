# Smu - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:11

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Smu](#smu)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Smu

#### 基本信息

- **UUID**: `ECUC:865c8c0e-f964-4d70-92a9-ff60c9da4cee`
- **模块名称**: `Smu`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the Smu (Safety Management Unit) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **16** 个配置容器：

##### 1. SmuConfigSet

**容器属性**:

- **UUID**: `ccda81dc-46cf-4171-858b-7c947884702f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuConfigSet`
- **多重性**: [0..1]

**容器描述**:

This is the base container that contains the post-build configuration parameters

###### 配置容器

本模块包含 **12** 个配置容器：

####### 1. SmuCoreConfig

**容器属性**:

- **UUID**: `ccda81dc-46cf-4171-858b-7c947884567f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreConfig`
- **多重性**: [0..1]

**容器描述**:

This is the base container that contains the post-build configuration parameters for SmuCore

######## 配置容器

本模块包含 **7** 个配置容器：

######### 1. SmuCoreRecoveryTimer

**容器属性**:

- **UUID**: `3ea7abca-6ba4-5d14-befd-8bb9351fe86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRecoveryTimer`
- **多重性**: [0..1]

**容器描述**:

SmuCore Recovery Timer configuration (parameters).

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. SmuCoreRTDuration

- **UUID**: `98ce928e-6ed1-4968-95b2-21d30b1fa49e`
- **参数名**: `SmuCoreRTDuration`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `16383`
- **取值范围**: [1..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the SmuCore Recovery Timer maximum duration.

########### ENUMERATION 类型参数

############ 1. SmuCoreEnableRT0

- **UUID**: `bfec07fb-567f-421e-b568-cb43a4ab5676`
- **参数名**: `SmuCoreEnableRT0`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_RT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_RT_DISABLE` (来源: INFINEON_AURIX2G)
  - `SMU_RT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Enabling or Disabling of SmuCore Recovery Timer 0.

############ 2. SmuCoreEnableRT1

- **UUID**: `bfec07fb-587f-421e-b564-cb43a4e5eda6`
- **参数名**: `SmuCoreEnableRT1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_RT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_RT_DISABLE` (来源: INFINEON_AURIX2G)
  - `SMU_RT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Enabling or Disabling of SmuCore Recovery Timer 1.

######### 2. SmuCoreRT0Alarm

**容器属性**:

- **UUID**: `97e6fd09-f2da-4944-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRT0Alarm`
- **多重性**: [4..4]

**容器描述**:

Alarms for Recovery Timer 0.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SmuCoreRT0AlarmId

- **UUID**: `98ce928e-6ed1-5968-93b2-24d3ab89549e`
- **参数名**: `SmuCoreRT0AlarmId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the alarm identifier of the selected group that can use the recovery timer 0.

########### ENUMERATION 类型参数

############ 1. SmuCoreRT0AlarmGroupId

- **UUID**: `bfec07fb-550f-421e-b568-cb43a4d8965a6`
- **参数名**: `SmuCoreRT0AlarmGroupId`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_GROUP0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_GROUP0` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP1` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP2` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP3` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP4` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP5` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP6` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP7` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP8` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP9` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP10` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP11` (来源: INFINEON_AURIX2G)
- **描述**: Defines the alarm group that can use the recovery timer 0.

######### 3. SmuCoreRT1Alarm

**容器属性**:

- **UUID**: `97e6fd09-f3da-4944-b2e1-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRT1Alarm`
- **多重性**: [4..4]

**容器描述**:

Alarms for the Recovery Timer 1.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SmuCoreRT1AlarmId

- **UUID**: `98ce938e-6ed1-5962-93b2-24d30b6789349e`
- **参数名**: `SmuCoreRT1AlarmId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the alarm identifier of the selected group that can use the recovery timer 1.

########### ENUMERATION 类型参数

############ 1. SmuCoreRT1AlarmGroupId

- **UUID**: `bfec07fb-550f-421e-b562-cb43a43w789a6`
- **参数名**: `SmuCoreRT1AlarmGroupId`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_GROUP0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_GROUP0` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP1` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP2` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP3` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP4` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP5` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP6` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP7` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP8` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP9` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP10` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP11` (来源: INFINEON_AURIX2G)
- **描述**: Defines the alarm group that can use the recovery timer 1.

######### 4. SmuCoreAlarmGlobalConfig

**容器属性**:

- **UUID**: `3ea7abca-6ca4-4d14-befd-82b3345ac678e86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmGlobalConfig`
- **多重性**: [0..1]

**容器描述**:

SmuCore Alarm Global Configuration .

########## 参数配置

此容器包含 **15** 个参数：

########### BOOLEAN 类型参数

############ 1. SmuCoreCpu0ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5ead6`
- **参数名**: `SmuCoreCpu0ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

############ 2. SmuCoreCpu1ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43b4e5eda6`
- **参数名**: `SmuCoreCpu1ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

############ 3. SmuCoreCpu2ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43c4e5eda6`
- **参数名**: `SmuCoreCpu2ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

############ 4. SmuCoreCpu3ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43d4e5eda6`
- **参数名**: `SmuCoreCpu3ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

############ 5. SmuCoreCpu4ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43e4e5eda6`
- **参数名**: `SmuCoreCpu4ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

############ 6. SmuCoreCpu5ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43f4e5eda6`
- **参数名**: `SmuCoreCpu5ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

############ 7. SmuCoreIGCS0ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43g4e5eda6`
- **参数名**: `SmuCoreIGCS0ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS0 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

############ 8. SmuCoreIGCS1ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edb6`
- **参数名**: `SmuCoreIGCS1ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS1 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

############ 9. SmuCoreIGCS2ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edc6`
- **参数名**: `SmuCoreIGCS2ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS2 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

############ 10. SmuCoreNMIActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edd6`
- **参数名**: `SmuCoreNMIActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when NMI configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

############ 11. SmuCoreCpuResetActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5ede6`
- **参数名**: `SmuCoreCpuResetActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when CPU RESET configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

########### ENUMERATION 类型参数

############ 1. SmuCoreInterruptSet0

- **UUID**: `bfec07fb-550f-421e-b578-cb43a567gha6`
- **参数名**: `SmuCoreInterruptSet0`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 0.

############ 2. SmuCoreInterruptSet1

- **UUID**: `bfec07fb-550f-421e-b578-cb43yshj096da6`
- **参数名**: `SmuCoreInterruptSet1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 1

############ 3. SmuCoreInterruptSet2

- **UUID**: `bfec07fb-550f-421e-b578-cb43a245eda6`
- **参数名**: `SmuCoreInterruptSet2`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 2

############ 4. SmuCoreEnableFaultToRunState

- **UUID**: `bfec07fb-550f-421e-b579-cb43a2e5eda6`
- **参数名**: `SmuCoreEnableFaultToRunState`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_EFRST_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_EFRST_ENABLE` (来源: INFINEON_AURIX2G)
  - `SMU_EFRST_DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the control of Fault State to Fault Free (Run) State transition. The state transition is possible only when this parameter is defined with SMU_EFRST_ENABLE

######### 5. SmuCoreFSPHandling

**容器属性**:

- **UUID**: `3ea7abca-6ba4-4d14-befd-82b3351fe89f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreFSPHandling`
- **多重性**: [0..1]

**容器描述**:

SmuCore driver FSP configuration (parameters) .

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. SmuCoreFSPFaultStateDuration

- **UUID**: `98ce928e-3ed1-4968-93b4-21d90b1fa49e`
- **参数名**: `SmuCoreFSPFaultStateDuration`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..1023]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter enables the maximum fault state duration of FSP signal. The value is written in TFSP_HIGH bits of SMU_FSP register. It shall be specified as a number of fSMU_FS ticks.

########### ENUMERATION 类型参数

############ 1. SmuCoreFSPPrescaler1

- **UUID**: `bfec07fb-551f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPPrescaler1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_REF_CLK_FRQ_DIV_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_REF_CLK_FRQ_DIV_2` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_4` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_8` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_16` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_32` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_64` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_128` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_256` (来源: INFINEON_AURIX2G)
- **描述**: Defines the dividing factor to apply to the reference clock FEVR_OSC. The divided clock is used as reference to generate the timing of the FSP fault state

############ 2. SmuCoreFSPPrescaler2

- **UUID**: `bfec07fb-551f-441e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPPrescaler2`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_REF_CLK_FRQ_DIV_512`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_REF_CLK_FRQ_DIV_512` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_1024` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_2048` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_4096` (来源: INFINEON_AURIX2G)
- **描述**: Defines the dividing factor to apply to the reference clock FEVR_OSC in order to generate the timing of the fault free state for the dynamic dual rail and time switching modes of the fault signaling protocol

############ 3. SmuCoreFSPSignalingMode

- **UUID**: `bfec07fb-561f-445e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPSignalingMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_FSP_BISTABLE_PROTOCOL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_FSP_BISTABLE_PROTOCOL` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_DUAL_RAIL_PROTOCOL` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_TIME_SWITCHING_PROTOCOL` (来源: INFINEON_AURIX2G)
- **描述**: Defines the type of signal output for FSP on an alarm event

############ 4. SmuCorePESOnFSP

- **UUID**: `bfec07fb-261f-445e-c568-cb43a2e5eda6`
- **参数名**: `SmuCorePESOnFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_FSP_PES_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_FSP_PES_ENABLE` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_PES_DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the PES to automatically request when an alarm event configured to start the FSP is detected

######### 6. SmuCoreAlarmGroup

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-ecc3dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmGroup`
- **多重性**: [12..12]

**容器描述**:

Container for SmuCore Alarm Group.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SmuCoreAlmGrpId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28766`
- **参数名**: `SmuCoreAlmGrpId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Group Id of the SMU alarm group. This value will be assigned to the symbolic name derived of the AlarmGroup container short name.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SmuCoreAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc78hj5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SMU Alarm Behavior.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. SmuCoreAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28786`
- **参数名**: `SmuCoreAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

############# ENUMERATION 类型参数

############## 1. SmuCoreAlarmIntBeh

- **UUID**: `bfec07fb-550f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmIntBeh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_NA_INT_ACTION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_NA_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS0_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS1_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS2_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_NMI_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_CPU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
- **描述**: Defines the internal behavior of an alarm event

############## 2. SmuCoreAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

######### 7. SmuCoreAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc78hj5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SMU Alarm Behavior.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. SmuCoreAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28786`
- **参数名**: `SmuCoreAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

########### ENUMERATION 类型参数

############ 1. SmuCoreAlarmIntBeh

- **UUID**: `bfec07fb-550f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmIntBeh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_NA_INT_ACTION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_NA_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS0_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS1_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS2_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_NMI_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_CPU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
- **描述**: Defines the internal behavior of an alarm event

############ 2. SmuCoreAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

####### 2. SmuCoreRecoveryTimer

**容器属性**:

- **UUID**: `3ea7abca-6ba4-5d14-befd-8bb9351fe86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRecoveryTimer`
- **多重性**: [0..1]

**容器描述**:

SmuCore Recovery Timer configuration (parameters).

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreRTDuration

- **UUID**: `98ce928e-6ed1-4968-95b2-21d30b1fa49e`
- **参数名**: `SmuCoreRTDuration`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `16383`
- **取值范围**: [1..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the SmuCore Recovery Timer maximum duration.

######### ENUMERATION 类型参数

########## 1. SmuCoreEnableRT0

- **UUID**: `bfec07fb-567f-421e-b568-cb43a4ab5676`
- **参数名**: `SmuCoreEnableRT0`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_RT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_RT_DISABLE` (来源: INFINEON_AURIX2G)
  - `SMU_RT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Enabling or Disabling of SmuCore Recovery Timer 0.

########## 2. SmuCoreEnableRT1

- **UUID**: `bfec07fb-587f-421e-b564-cb43a4e5eda6`
- **参数名**: `SmuCoreEnableRT1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_RT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_RT_DISABLE` (来源: INFINEON_AURIX2G)
  - `SMU_RT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Enabling or Disabling of SmuCore Recovery Timer 1.

####### 3. SmuCoreRT0Alarm

**容器属性**:

- **UUID**: `97e6fd09-f2da-4944-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRT0Alarm`
- **多重性**: [4..4]

**容器描述**:

Alarms for Recovery Timer 0.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreRT0AlarmId

- **UUID**: `98ce928e-6ed1-5968-93b2-24d3ab89549e`
- **参数名**: `SmuCoreRT0AlarmId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the alarm identifier of the selected group that can use the recovery timer 0.

######### ENUMERATION 类型参数

########## 1. SmuCoreRT0AlarmGroupId

- **UUID**: `bfec07fb-550f-421e-b568-cb43a4d8965a6`
- **参数名**: `SmuCoreRT0AlarmGroupId`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_GROUP0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_GROUP0` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP1` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP2` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP3` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP4` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP5` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP6` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP7` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP8` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP9` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP10` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP11` (来源: INFINEON_AURIX2G)
- **描述**: Defines the alarm group that can use the recovery timer 0.

####### 4. SmuCoreRT1Alarm

**容器属性**:

- **UUID**: `97e6fd09-f3da-4944-b2e1-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRT1Alarm`
- **多重性**: [4..4]

**容器描述**:

Alarms for the Recovery Timer 1.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreRT1AlarmId

- **UUID**: `98ce938e-6ed1-5962-93b2-24d30b6789349e`
- **参数名**: `SmuCoreRT1AlarmId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the alarm identifier of the selected group that can use the recovery timer 1.

######### ENUMERATION 类型参数

########## 1. SmuCoreRT1AlarmGroupId

- **UUID**: `bfec07fb-550f-421e-b562-cb43a43w789a6`
- **参数名**: `SmuCoreRT1AlarmGroupId`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_GROUP0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_GROUP0` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP1` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP2` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP3` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP4` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP5` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP6` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP7` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP8` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP9` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP10` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP11` (来源: INFINEON_AURIX2G)
- **描述**: Defines the alarm group that can use the recovery timer 1.

####### 5. SmuCoreAlarmGlobalConfig

**容器属性**:

- **UUID**: `3ea7abca-6ca4-4d14-befd-82b3345ac678e86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmGlobalConfig`
- **多重性**: [0..1]

**容器描述**:

SmuCore Alarm Global Configuration .

######## 参数配置

此容器包含 **15** 个参数：

######### BOOLEAN 类型参数

########## 1. SmuCoreCpu0ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5ead6`
- **参数名**: `SmuCoreCpu0ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 2. SmuCoreCpu1ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43b4e5eda6`
- **参数名**: `SmuCoreCpu1ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 3. SmuCoreCpu2ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43c4e5eda6`
- **参数名**: `SmuCoreCpu2ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 4. SmuCoreCpu3ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43d4e5eda6`
- **参数名**: `SmuCoreCpu3ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 5. SmuCoreCpu4ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43e4e5eda6`
- **参数名**: `SmuCoreCpu4ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 6. SmuCoreCpu5ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43f4e5eda6`
- **参数名**: `SmuCoreCpu5ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 7. SmuCoreIGCS0ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43g4e5eda6`
- **参数名**: `SmuCoreIGCS0ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS0 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

########## 8. SmuCoreIGCS1ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edb6`
- **参数名**: `SmuCoreIGCS1ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS1 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

########## 9. SmuCoreIGCS2ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edc6`
- **参数名**: `SmuCoreIGCS2ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS2 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

########## 10. SmuCoreNMIActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edd6`
- **参数名**: `SmuCoreNMIActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when NMI configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

########## 11. SmuCoreCpuResetActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5ede6`
- **参数名**: `SmuCoreCpuResetActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when CPU RESET configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

######### ENUMERATION 类型参数

########## 1. SmuCoreInterruptSet0

- **UUID**: `bfec07fb-550f-421e-b578-cb43a567gha6`
- **参数名**: `SmuCoreInterruptSet0`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 0.

########## 2. SmuCoreInterruptSet1

- **UUID**: `bfec07fb-550f-421e-b578-cb43yshj096da6`
- **参数名**: `SmuCoreInterruptSet1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 1

########## 3. SmuCoreInterruptSet2

- **UUID**: `bfec07fb-550f-421e-b578-cb43a245eda6`
- **参数名**: `SmuCoreInterruptSet2`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 2

########## 4. SmuCoreEnableFaultToRunState

- **UUID**: `bfec07fb-550f-421e-b579-cb43a2e5eda6`
- **参数名**: `SmuCoreEnableFaultToRunState`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_EFRST_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_EFRST_ENABLE` (来源: INFINEON_AURIX2G)
  - `SMU_EFRST_DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the control of Fault State to Fault Free (Run) State transition. The state transition is possible only when this parameter is defined with SMU_EFRST_ENABLE

####### 6. SmuCoreFSPHandling

**容器属性**:

- **UUID**: `3ea7abca-6ba4-4d14-befd-82b3351fe89f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreFSPHandling`
- **多重性**: [0..1]

**容器描述**:

SmuCore driver FSP configuration (parameters) .

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreFSPFaultStateDuration

- **UUID**: `98ce928e-3ed1-4968-93b4-21d90b1fa49e`
- **参数名**: `SmuCoreFSPFaultStateDuration`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..1023]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter enables the maximum fault state duration of FSP signal. The value is written in TFSP_HIGH bits of SMU_FSP register. It shall be specified as a number of fSMU_FS ticks.

######### ENUMERATION 类型参数

########## 1. SmuCoreFSPPrescaler1

- **UUID**: `bfec07fb-551f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPPrescaler1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_REF_CLK_FRQ_DIV_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_REF_CLK_FRQ_DIV_2` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_4` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_8` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_16` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_32` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_64` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_128` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_256` (来源: INFINEON_AURIX2G)
- **描述**: Defines the dividing factor to apply to the reference clock FEVR_OSC. The divided clock is used as reference to generate the timing of the FSP fault state

########## 2. SmuCoreFSPPrescaler2

- **UUID**: `bfec07fb-551f-441e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPPrescaler2`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_REF_CLK_FRQ_DIV_512`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_REF_CLK_FRQ_DIV_512` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_1024` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_2048` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_4096` (来源: INFINEON_AURIX2G)
- **描述**: Defines the dividing factor to apply to the reference clock FEVR_OSC in order to generate the timing of the fault free state for the dynamic dual rail and time switching modes of the fault signaling protocol

########## 3. SmuCoreFSPSignalingMode

- **UUID**: `bfec07fb-561f-445e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPSignalingMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_FSP_BISTABLE_PROTOCOL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_FSP_BISTABLE_PROTOCOL` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_DUAL_RAIL_PROTOCOL` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_TIME_SWITCHING_PROTOCOL` (来源: INFINEON_AURIX2G)
- **描述**: Defines the type of signal output for FSP on an alarm event

########## 4. SmuCorePESOnFSP

- **UUID**: `bfec07fb-261f-445e-c568-cb43a2e5eda6`
- **参数名**: `SmuCorePESOnFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_FSP_PES_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_FSP_PES_ENABLE` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_PES_DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the PES to automatically request when an alarm event configured to start the FSP is detected

####### 7. SmuCoreAlarmGroup

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-ecc3dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmGroup`
- **多重性**: [12..12]

**容器描述**:

Container for SmuCore Alarm Group.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreAlmGrpId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28766`
- **参数名**: `SmuCoreAlmGrpId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Group Id of the SMU alarm group. This value will be assigned to the symbolic name derived of the AlarmGroup container short name.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmuCoreAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc78hj5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SMU Alarm Behavior.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. SmuCoreAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28786`
- **参数名**: `SmuCoreAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

########### ENUMERATION 类型参数

############ 1. SmuCoreAlarmIntBeh

- **UUID**: `bfec07fb-550f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmIntBeh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_NA_INT_ACTION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_NA_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS0_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS1_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS2_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_NMI_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_CPU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
- **描述**: Defines the internal behavior of an alarm event

############ 2. SmuCoreAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

####### 8. SmuCoreAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc78hj5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SMU Alarm Behavior.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28786`
- **参数名**: `SmuCoreAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

######### ENUMERATION 类型参数

########## 1. SmuCoreAlarmIntBeh

- **UUID**: `bfec07fb-550f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmIntBeh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_NA_INT_ACTION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_NA_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS0_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS1_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS2_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_NMI_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_CPU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
- **描述**: Defines the internal behavior of an alarm event

########## 2. SmuCoreAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

####### 9. SmuStdbyConfig

**容器属性**:

- **UUID**: `ccda81dc-46cf-4171-858b-7c9478fg802f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyConfig`
- **多重性**: [0..1]

**容器描述**:

This is the base container that contains the post-build configuration parameters for SmuStdby

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. SmuStdbyAlarmGlobalConfig

**容器属性**:

- **UUID**: `3ea7abca-6ca4-4d14-befd-82b3351fe86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmGlobalConfig`
- **多重性**: [0..1]

**容器描述**:

SmuStdby Alarm Global Configuration .

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. SmuStdbyEnableFSP0

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4es67hd6`
- **参数名**: `SmuStdbyEnableFSP0`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the error pin 33.8 to be used for FSP

############ 2. SmuStdbyEnableFSP1

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e78ude6`
- **参数名**: `SmuStdbyEnableFSP1`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the error pin 33.10 to be used for FSP

######### 2. SmuStdbyAlarmGroup

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-ectyhdc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmGroup`
- **多重性**: [2..2]

**容器描述**:

Container for SmuStdby Alarm Group.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SmuStdbyAlmGrpId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4t1c29766`
- **参数名**: `SmuStdbyAlmGrpId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Group Id of the SMU alarm group. This value will be assigned to the symbolic name derived of the AlarmGroup container short name.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SmuStdbyAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SmuStdby Alarm Behavior.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. SmuStdbyAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b7gh1c28766`
- **参数名**: `SmuStdbyAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

############# ENUMERATION 类型参数

############## 1. SmuStdbyAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eyuj6`
- **参数名**: `SmuStdbyAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

######### 3. SmuStdbyAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SmuStdby Alarm Behavior.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SmuStdbyAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b7gh1c28766`
- **参数名**: `SmuStdbyAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

########### ENUMERATION 类型参数

############ 1. SmuStdbyAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eyuj6`
- **参数名**: `SmuStdbyAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

####### 10. SmuStdbyAlarmGlobalConfig

**容器属性**:

- **UUID**: `3ea7abca-6ca4-4d14-befd-82b3351fe86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmGlobalConfig`
- **多重性**: [0..1]

**容器描述**:

SmuStdby Alarm Global Configuration .

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. SmuStdbyEnableFSP0

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4es67hd6`
- **参数名**: `SmuStdbyEnableFSP0`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the error pin 33.8 to be used for FSP

########## 2. SmuStdbyEnableFSP1

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e78ude6`
- **参数名**: `SmuStdbyEnableFSP1`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the error pin 33.10 to be used for FSP

####### 11. SmuStdbyAlarmGroup

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-ectyhdc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmGroup`
- **多重性**: [2..2]

**容器描述**:

Container for SmuStdby Alarm Group.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SmuStdbyAlmGrpId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4t1c29766`
- **参数名**: `SmuStdbyAlmGrpId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Group Id of the SMU alarm group. This value will be assigned to the symbolic name derived of the AlarmGroup container short name.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmuStdbyAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SmuStdby Alarm Behavior.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SmuStdbyAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b7gh1c28766`
- **参数名**: `SmuStdbyAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

########### ENUMERATION 类型参数

############ 1. SmuStdbyAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eyuj6`
- **参数名**: `SmuStdbyAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

####### 12. SmuStdbyAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SmuStdby Alarm Behavior.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmuStdbyAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b7gh1c28766`
- **参数名**: `SmuStdbyAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

######### ENUMERATION 类型参数

########## 1. SmuStdbyAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eyuj6`
- **参数名**: `SmuStdbyAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

##### 2. SmuCoreConfig

**容器属性**:

- **UUID**: `ccda81dc-46cf-4171-858b-7c947884567f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreConfig`
- **多重性**: [0..1]

**容器描述**:

This is the base container that contains the post-build configuration parameters for SmuCore

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. SmuCoreRecoveryTimer

**容器属性**:

- **UUID**: `3ea7abca-6ba4-5d14-befd-8bb9351fe86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRecoveryTimer`
- **多重性**: [0..1]

**容器描述**:

SmuCore Recovery Timer configuration (parameters).

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreRTDuration

- **UUID**: `98ce928e-6ed1-4968-95b2-21d30b1fa49e`
- **参数名**: `SmuCoreRTDuration`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `16383`
- **取值范围**: [1..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the SmuCore Recovery Timer maximum duration.

######### ENUMERATION 类型参数

########## 1. SmuCoreEnableRT0

- **UUID**: `bfec07fb-567f-421e-b568-cb43a4ab5676`
- **参数名**: `SmuCoreEnableRT0`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_RT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_RT_DISABLE` (来源: INFINEON_AURIX2G)
  - `SMU_RT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Enabling or Disabling of SmuCore Recovery Timer 0.

########## 2. SmuCoreEnableRT1

- **UUID**: `bfec07fb-587f-421e-b564-cb43a4e5eda6`
- **参数名**: `SmuCoreEnableRT1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_RT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_RT_DISABLE` (来源: INFINEON_AURIX2G)
  - `SMU_RT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Enabling or Disabling of SmuCore Recovery Timer 1.

####### 2. SmuCoreRT0Alarm

**容器属性**:

- **UUID**: `97e6fd09-f2da-4944-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRT0Alarm`
- **多重性**: [4..4]

**容器描述**:

Alarms for Recovery Timer 0.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreRT0AlarmId

- **UUID**: `98ce928e-6ed1-5968-93b2-24d3ab89549e`
- **参数名**: `SmuCoreRT0AlarmId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the alarm identifier of the selected group that can use the recovery timer 0.

######### ENUMERATION 类型参数

########## 1. SmuCoreRT0AlarmGroupId

- **UUID**: `bfec07fb-550f-421e-b568-cb43a4d8965a6`
- **参数名**: `SmuCoreRT0AlarmGroupId`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_GROUP0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_GROUP0` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP1` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP2` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP3` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP4` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP5` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP6` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP7` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP8` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP9` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP10` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP11` (来源: INFINEON_AURIX2G)
- **描述**: Defines the alarm group that can use the recovery timer 0.

####### 3. SmuCoreRT1Alarm

**容器属性**:

- **UUID**: `97e6fd09-f3da-4944-b2e1-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRT1Alarm`
- **多重性**: [4..4]

**容器描述**:

Alarms for the Recovery Timer 1.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreRT1AlarmId

- **UUID**: `98ce938e-6ed1-5962-93b2-24d30b6789349e`
- **参数名**: `SmuCoreRT1AlarmId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the alarm identifier of the selected group that can use the recovery timer 1.

######### ENUMERATION 类型参数

########## 1. SmuCoreRT1AlarmGroupId

- **UUID**: `bfec07fb-550f-421e-b562-cb43a43w789a6`
- **参数名**: `SmuCoreRT1AlarmGroupId`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_GROUP0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_GROUP0` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP1` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP2` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP3` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP4` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP5` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP6` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP7` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP8` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP9` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP10` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP11` (来源: INFINEON_AURIX2G)
- **描述**: Defines the alarm group that can use the recovery timer 1.

####### 4. SmuCoreAlarmGlobalConfig

**容器属性**:

- **UUID**: `3ea7abca-6ca4-4d14-befd-82b3345ac678e86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmGlobalConfig`
- **多重性**: [0..1]

**容器描述**:

SmuCore Alarm Global Configuration .

######## 参数配置

此容器包含 **15** 个参数：

######### BOOLEAN 类型参数

########## 1. SmuCoreCpu0ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5ead6`
- **参数名**: `SmuCoreCpu0ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 2. SmuCoreCpu1ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43b4e5eda6`
- **参数名**: `SmuCoreCpu1ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 3. SmuCoreCpu2ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43c4e5eda6`
- **参数名**: `SmuCoreCpu2ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 4. SmuCoreCpu3ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43d4e5eda6`
- **参数名**: `SmuCoreCpu3ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 5. SmuCoreCpu4ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43e4e5eda6`
- **参数名**: `SmuCoreCpu4ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 6. SmuCoreCpu5ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43f4e5eda6`
- **参数名**: `SmuCoreCpu5ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

########## 7. SmuCoreIGCS0ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43g4e5eda6`
- **参数名**: `SmuCoreIGCS0ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS0 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

########## 8. SmuCoreIGCS1ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edb6`
- **参数名**: `SmuCoreIGCS1ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS1 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

########## 9. SmuCoreIGCS2ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edc6`
- **参数名**: `SmuCoreIGCS2ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS2 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

########## 10. SmuCoreNMIActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edd6`
- **参数名**: `SmuCoreNMIActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when NMI configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

########## 11. SmuCoreCpuResetActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5ede6`
- **参数名**: `SmuCoreCpuResetActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when CPU RESET configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

######### ENUMERATION 类型参数

########## 1. SmuCoreInterruptSet0

- **UUID**: `bfec07fb-550f-421e-b578-cb43a567gha6`
- **参数名**: `SmuCoreInterruptSet0`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 0.

########## 2. SmuCoreInterruptSet1

- **UUID**: `bfec07fb-550f-421e-b578-cb43yshj096da6`
- **参数名**: `SmuCoreInterruptSet1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 1

########## 3. SmuCoreInterruptSet2

- **UUID**: `bfec07fb-550f-421e-b578-cb43a245eda6`
- **参数名**: `SmuCoreInterruptSet2`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 2

########## 4. SmuCoreEnableFaultToRunState

- **UUID**: `bfec07fb-550f-421e-b579-cb43a2e5eda6`
- **参数名**: `SmuCoreEnableFaultToRunState`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_EFRST_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_EFRST_ENABLE` (来源: INFINEON_AURIX2G)
  - `SMU_EFRST_DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the control of Fault State to Fault Free (Run) State transition. The state transition is possible only when this parameter is defined with SMU_EFRST_ENABLE

####### 5. SmuCoreFSPHandling

**容器属性**:

- **UUID**: `3ea7abca-6ba4-4d14-befd-82b3351fe89f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreFSPHandling`
- **多重性**: [0..1]

**容器描述**:

SmuCore driver FSP configuration (parameters) .

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreFSPFaultStateDuration

- **UUID**: `98ce928e-3ed1-4968-93b4-21d90b1fa49e`
- **参数名**: `SmuCoreFSPFaultStateDuration`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..1023]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter enables the maximum fault state duration of FSP signal. The value is written in TFSP_HIGH bits of SMU_FSP register. It shall be specified as a number of fSMU_FS ticks.

######### ENUMERATION 类型参数

########## 1. SmuCoreFSPPrescaler1

- **UUID**: `bfec07fb-551f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPPrescaler1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_REF_CLK_FRQ_DIV_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_REF_CLK_FRQ_DIV_2` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_4` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_8` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_16` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_32` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_64` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_128` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_256` (来源: INFINEON_AURIX2G)
- **描述**: Defines the dividing factor to apply to the reference clock FEVR_OSC. The divided clock is used as reference to generate the timing of the FSP fault state

########## 2. SmuCoreFSPPrescaler2

- **UUID**: `bfec07fb-551f-441e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPPrescaler2`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_REF_CLK_FRQ_DIV_512`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_REF_CLK_FRQ_DIV_512` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_1024` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_2048` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_4096` (来源: INFINEON_AURIX2G)
- **描述**: Defines the dividing factor to apply to the reference clock FEVR_OSC in order to generate the timing of the fault free state for the dynamic dual rail and time switching modes of the fault signaling protocol

########## 3. SmuCoreFSPSignalingMode

- **UUID**: `bfec07fb-561f-445e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPSignalingMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_FSP_BISTABLE_PROTOCOL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_FSP_BISTABLE_PROTOCOL` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_DUAL_RAIL_PROTOCOL` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_TIME_SWITCHING_PROTOCOL` (来源: INFINEON_AURIX2G)
- **描述**: Defines the type of signal output for FSP on an alarm event

########## 4. SmuCorePESOnFSP

- **UUID**: `bfec07fb-261f-445e-c568-cb43a2e5eda6`
- **参数名**: `SmuCorePESOnFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_FSP_PES_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_FSP_PES_ENABLE` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_PES_DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the PES to automatically request when an alarm event configured to start the FSP is detected

####### 6. SmuCoreAlarmGroup

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-ecc3dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmGroup`
- **多重性**: [12..12]

**容器描述**:

Container for SmuCore Alarm Group.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreAlmGrpId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28766`
- **参数名**: `SmuCoreAlmGrpId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Group Id of the SMU alarm group. This value will be assigned to the symbolic name derived of the AlarmGroup container short name.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmuCoreAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc78hj5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SMU Alarm Behavior.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. SmuCoreAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28786`
- **参数名**: `SmuCoreAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

########### ENUMERATION 类型参数

############ 1. SmuCoreAlarmIntBeh

- **UUID**: `bfec07fb-550f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmIntBeh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_NA_INT_ACTION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_NA_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS0_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS1_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS2_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_NMI_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_CPU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
- **描述**: Defines the internal behavior of an alarm event

############ 2. SmuCoreAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

####### 7. SmuCoreAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc78hj5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SMU Alarm Behavior.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28786`
- **参数名**: `SmuCoreAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

######### ENUMERATION 类型参数

########## 1. SmuCoreAlarmIntBeh

- **UUID**: `bfec07fb-550f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmIntBeh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_NA_INT_ACTION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_NA_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS0_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS1_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS2_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_NMI_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_CPU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
- **描述**: Defines the internal behavior of an alarm event

########## 2. SmuCoreAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

##### 3. SmuCoreRecoveryTimer

**容器属性**:

- **UUID**: `3ea7abca-6ba4-5d14-befd-8bb9351fe86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRecoveryTimer`
- **多重性**: [0..1]

**容器描述**:

SmuCore Recovery Timer configuration (parameters).

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. SmuCoreRTDuration

- **UUID**: `98ce928e-6ed1-4968-95b2-21d30b1fa49e`
- **参数名**: `SmuCoreRTDuration`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `16383`
- **取值范围**: [1..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the SmuCore Recovery Timer maximum duration.

####### ENUMERATION 类型参数

######## 1. SmuCoreEnableRT0

- **UUID**: `bfec07fb-567f-421e-b568-cb43a4ab5676`
- **参数名**: `SmuCoreEnableRT0`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_RT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_RT_DISABLE` (来源: INFINEON_AURIX2G)
  - `SMU_RT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Enabling or Disabling of SmuCore Recovery Timer 0.

######## 2. SmuCoreEnableRT1

- **UUID**: `bfec07fb-587f-421e-b564-cb43a4e5eda6`
- **参数名**: `SmuCoreEnableRT1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_RT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_RT_DISABLE` (来源: INFINEON_AURIX2G)
  - `SMU_RT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Enabling or Disabling of SmuCore Recovery Timer 1.

##### 4. SmuCoreRT0Alarm

**容器属性**:

- **UUID**: `97e6fd09-f2da-4944-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRT0Alarm`
- **多重性**: [4..4]

**容器描述**:

Alarms for Recovery Timer 0.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SmuCoreRT0AlarmId

- **UUID**: `98ce928e-6ed1-5968-93b2-24d3ab89549e`
- **参数名**: `SmuCoreRT0AlarmId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the alarm identifier of the selected group that can use the recovery timer 0.

####### ENUMERATION 类型参数

######## 1. SmuCoreRT0AlarmGroupId

- **UUID**: `bfec07fb-550f-421e-b568-cb43a4d8965a6`
- **参数名**: `SmuCoreRT0AlarmGroupId`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_GROUP0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_GROUP0` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP1` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP2` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP3` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP4` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP5` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP6` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP7` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP8` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP9` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP10` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP11` (来源: INFINEON_AURIX2G)
- **描述**: Defines the alarm group that can use the recovery timer 0.

##### 5. SmuCoreRT1Alarm

**容器属性**:

- **UUID**: `97e6fd09-f3da-4944-b2e1-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreRT1Alarm`
- **多重性**: [4..4]

**容器描述**:

Alarms for the Recovery Timer 1.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SmuCoreRT1AlarmId

- **UUID**: `98ce938e-6ed1-5962-93b2-24d30b6789349e`
- **参数名**: `SmuCoreRT1AlarmId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Defines the alarm identifier of the selected group that can use the recovery timer 1.

####### ENUMERATION 类型参数

######## 1. SmuCoreRT1AlarmGroupId

- **UUID**: `bfec07fb-550f-421e-b562-cb43a43w789a6`
- **参数名**: `SmuCoreRT1AlarmGroupId`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_GROUP0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_GROUP0` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP1` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP2` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP3` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP4` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP5` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP6` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP7` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP8` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP9` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP10` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_GROUP11` (来源: INFINEON_AURIX2G)
- **描述**: Defines the alarm group that can use the recovery timer 1.

##### 6. SmuCoreAlarmGlobalConfig

**容器属性**:

- **UUID**: `3ea7abca-6ca4-4d14-befd-82b3345ac678e86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmGlobalConfig`
- **多重性**: [0..1]

**容器描述**:

SmuCore Alarm Global Configuration .

###### 参数配置

此容器包含 **15** 个参数：

####### BOOLEAN 类型参数

######## 1. SmuCoreCpu0ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5ead6`
- **参数名**: `SmuCoreCpu0ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

######## 2. SmuCoreCpu1ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43b4e5eda6`
- **参数名**: `SmuCoreCpu1ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

######## 3. SmuCoreCpu2ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43c4e5eda6`
- **参数名**: `SmuCoreCpu2ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

######## 4. SmuCoreCpu3ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43d4e5eda6`
- **参数名**: `SmuCoreCpu3ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

######## 5. SmuCoreCpu4ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43e4e5eda6`
- **参数名**: `SmuCoreCpu4ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

######## 6. SmuCoreCpu5ResetRequest

- **UUID**: `bfec07fb-550f-423e-b578-cb43f4e5eda6`
- **参数名**: `SmuCoreCpu5ResetRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the Cpu reset request to CPU.

######## 7. SmuCoreIGCS0ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43g4e5eda6`
- **参数名**: `SmuCoreIGCS0ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS0 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

######## 8. SmuCoreIGCS1ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edb6`
- **参数名**: `SmuCoreIGCS1ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS1 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

######## 9. SmuCoreIGCS2ActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edc6`
- **参数名**: `SmuCoreIGCS2ActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when IGCS2 configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

######## 10. SmuCoreNMIActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5edd6`
- **参数名**: `SmuCoreNMIActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when NMI configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

######## 11. SmuCoreCpuResetActivatePES

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e5ede6`
- **参数名**: `SmuCoreCpuResetActivatePES`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the control of the Port Emergency Stop (PES) feature when CPU RESET configured alarm is active. When an internal action is triggered, the hardware triggers automatically the PES on enabling

####### ENUMERATION 类型参数

######## 1. SmuCoreInterruptSet0

- **UUID**: `bfec07fb-550f-421e-b578-cb43a567gha6`
- **参数名**: `SmuCoreInterruptSet0`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 0.

######## 2. SmuCoreInterruptSet1

- **UUID**: `bfec07fb-550f-421e-b578-cb43yshj096da6`
- **参数名**: `SmuCoreInterruptSet1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 1

######## 3. SmuCoreInterruptSet2

- **UUID**: `bfec07fb-550f-421e-b578-cb43a245eda6`
- **参数名**: `SmuCoreInterruptSet2`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_SELECT_INT_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_SELECT_INT_NONE` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT1_INT2` (来源: INFINEON_AURIX2G)
  - `SMU_SELECT_INT0_INT1_INT2` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the interrupt request vector when the alarm configuration flag selects the interrupt configuration set 2

######## 4. SmuCoreEnableFaultToRunState

- **UUID**: `bfec07fb-550f-421e-b579-cb43a2e5eda6`
- **参数名**: `SmuCoreEnableFaultToRunState`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_EFRST_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_EFRST_ENABLE` (来源: INFINEON_AURIX2G)
  - `SMU_EFRST_DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the control of Fault State to Fault Free (Run) State transition. The state transition is possible only when this parameter is defined with SMU_EFRST_ENABLE

##### 7. SmuCoreFSPHandling

**容器属性**:

- **UUID**: `3ea7abca-6ba4-4d14-befd-82b3351fe89f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreFSPHandling`
- **多重性**: [0..1]

**容器描述**:

SmuCore driver FSP configuration (parameters) .

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. SmuCoreFSPFaultStateDuration

- **UUID**: `98ce928e-3ed1-4968-93b4-21d90b1fa49e`
- **参数名**: `SmuCoreFSPFaultStateDuration`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..1023]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter enables the maximum fault state duration of FSP signal. The value is written in TFSP_HIGH bits of SMU_FSP register. It shall be specified as a number of fSMU_FS ticks.

####### ENUMERATION 类型参数

######## 1. SmuCoreFSPPrescaler1

- **UUID**: `bfec07fb-551f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPPrescaler1`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_REF_CLK_FRQ_DIV_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_REF_CLK_FRQ_DIV_2` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_4` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_8` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_16` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_32` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_64` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_128` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_256` (来源: INFINEON_AURIX2G)
- **描述**: Defines the dividing factor to apply to the reference clock FEVR_OSC. The divided clock is used as reference to generate the timing of the FSP fault state

######## 2. SmuCoreFSPPrescaler2

- **UUID**: `bfec07fb-551f-441e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPPrescaler2`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_REF_CLK_FRQ_DIV_512`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_REF_CLK_FRQ_DIV_512` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_1024` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_2048` (来源: INFINEON_AURIX2G)
  - `SMU_REF_CLK_FRQ_DIV_4096` (来源: INFINEON_AURIX2G)
- **描述**: Defines the dividing factor to apply to the reference clock FEVR_OSC in order to generate the timing of the fault free state for the dynamic dual rail and time switching modes of the fault signaling protocol

######## 3. SmuCoreFSPSignalingMode

- **UUID**: `bfec07fb-561f-445e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreFSPSignalingMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_FSP_BISTABLE_PROTOCOL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_FSP_BISTABLE_PROTOCOL` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_DUAL_RAIL_PROTOCOL` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_TIME_SWITCHING_PROTOCOL` (来源: INFINEON_AURIX2G)
- **描述**: Defines the type of signal output for FSP on an alarm event

######## 4. SmuCorePESOnFSP

- **UUID**: `bfec07fb-261f-445e-c568-cb43a2e5eda6`
- **参数名**: `SmuCorePESOnFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_FSP_PES_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_FSP_PES_ENABLE` (来源: INFINEON_AURIX2G)
  - `SMU_FSP_PES_DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: Defines the PES to automatically request when an alarm event configured to start the FSP is detected

##### 8. SmuCoreAlarmGroup

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-ecc3dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmGroup`
- **多重性**: [12..12]

**容器描述**:

Container for SmuCore Alarm Group.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SmuCoreAlmGrpId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28766`
- **参数名**: `SmuCoreAlmGrpId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Group Id of the SMU alarm group. This value will be assigned to the symbolic name derived of the AlarmGroup container short name.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SmuCoreAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc78hj5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SMU Alarm Behavior.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. SmuCoreAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28786`
- **参数名**: `SmuCoreAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

######### ENUMERATION 类型参数

########## 1. SmuCoreAlarmIntBeh

- **UUID**: `bfec07fb-550f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmIntBeh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_NA_INT_ACTION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_NA_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS0_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS1_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS2_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_NMI_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_CPU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
- **描述**: Defines the internal behavior of an alarm event

########## 2. SmuCoreAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

##### 9. SmuCoreAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc78hj5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuCoreAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SMU Alarm Behavior.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. SmuCoreAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28786`
- **参数名**: `SmuCoreAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

####### ENUMERATION 类型参数

######## 1. SmuCoreAlarmIntBeh

- **UUID**: `bfec07fb-550f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmIntBeh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_NA_INT_ACTION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_NA_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS0_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS1_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_IGCS2_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_NMI_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
  - `SMU_CPU_RESET_INT_ACTION` (来源: INFINEON_AURIX2G)
- **描述**: Defines the internal behavior of an alarm event

######## 2. SmuCoreAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eda6`
- **参数名**: `SmuCoreAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

##### 10. SmuStdbyConfig

**容器属性**:

- **UUID**: `ccda81dc-46cf-4171-858b-7c9478fg802f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyConfig`
- **多重性**: [0..1]

**容器描述**:

This is the base container that contains the post-build configuration parameters for SmuStdby

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. SmuStdbyAlarmGlobalConfig

**容器属性**:

- **UUID**: `3ea7abca-6ca4-4d14-befd-82b3351fe86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmGlobalConfig`
- **多重性**: [0..1]

**容器描述**:

SmuStdby Alarm Global Configuration .

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. SmuStdbyEnableFSP0

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4es67hd6`
- **参数名**: `SmuStdbyEnableFSP0`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the error pin 33.8 to be used for FSP

########## 2. SmuStdbyEnableFSP1

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e78ude6`
- **参数名**: `SmuStdbyEnableFSP1`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the error pin 33.10 to be used for FSP

####### 2. SmuStdbyAlarmGroup

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-ectyhdc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmGroup`
- **多重性**: [2..2]

**容器描述**:

Container for SmuStdby Alarm Group.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SmuStdbyAlmGrpId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4t1c29766`
- **参数名**: `SmuStdbyAlmGrpId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Group Id of the SMU alarm group. This value will be assigned to the symbolic name derived of the AlarmGroup container short name.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SmuStdbyAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SmuStdby Alarm Behavior.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SmuStdbyAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b7gh1c28766`
- **参数名**: `SmuStdbyAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

########### ENUMERATION 类型参数

############ 1. SmuStdbyAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eyuj6`
- **参数名**: `SmuStdbyAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

####### 3. SmuStdbyAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SmuStdby Alarm Behavior.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmuStdbyAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b7gh1c28766`
- **参数名**: `SmuStdbyAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

######### ENUMERATION 类型参数

########## 1. SmuStdbyAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eyuj6`
- **参数名**: `SmuStdbyAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

##### 11. SmuStdbyAlarmGlobalConfig

**容器属性**:

- **UUID**: `3ea7abca-6ca4-4d14-befd-82b3351fe86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmGlobalConfig`
- **多重性**: [0..1]

**容器描述**:

SmuStdby Alarm Global Configuration .

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. SmuStdbyEnableFSP0

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4es67hd6`
- **参数名**: `SmuStdbyEnableFSP0`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the error pin 33.8 to be used for FSP

######## 2. SmuStdbyEnableFSP1

- **UUID**: `bfec07fb-550f-423e-b578-cb43a4e78ude6`
- **参数名**: `SmuStdbyEnableFSP1`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Defines the error pin 33.10 to be used for FSP

##### 12. SmuStdbyAlarmGroup

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-ectyhdc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmGroup`
- **多重性**: [2..2]

**容器描述**:

Container for SmuStdby Alarm Group.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SmuStdbyAlmGrpId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4t1c29766`
- **参数名**: `SmuStdbyAlmGrpId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Group Id of the SMU alarm group. This value will be assigned to the symbolic name derived of the AlarmGroup container short name.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SmuStdbyAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SmuStdby Alarm Behavior.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SmuStdbyAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b7gh1c28766`
- **参数名**: `SmuStdbyAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

######### ENUMERATION 类型参数

########## 1. SmuStdbyAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eyuj6`
- **参数名**: `SmuStdbyAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

##### 13. SmuStdbyAlarmBehavior

**容器属性**:

- **UUID**: `97e6fd09-f2da-4844-b2e0-edc4dc70e5a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuStdbyAlarmBehavior`
- **多重性**: [32..32]

**容器描述**:

Container for SmuStdby Alarm Behavior.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SmuStdbyAlmBehaviourId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b7gh1c28766`
- **参数名**: `SmuStdbyAlmBehaviourId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Alarm Id of the alarm group. This value will be assigned to the symbolic name derived of the AlarmBehaviour container short name.

####### ENUMERATION 类型参数

######## 1. SmuStdbyAlarmFSP

- **UUID**: `bfec07fb-650f-421e-b568-cb43a2e5eyuj6`
- **参数名**: `SmuStdbyAlarmFSP`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_ALARM_FSP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_ALARM_FSP_ENABLED` (来源: INFINEON_AURIX2G)
  - `SMU_ALARM_FSP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: Defines the Fault Signaling of an alarm event

##### 14. SmuGeneral

**容器属性**:

- **UUID**: `3ea7abca-6ba4-1d14-befd-8bb9351fe86f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuGeneral`
- **多重性**: [0..1]

**容器描述**:

SMU Module related generic configurations.

###### 参数配置

此容器包含 **13** 个参数：

####### BOOLEAN 类型参数

######## 1. SmuStdbyEnable

- **UUID**: `bfec07fb-550f-423e-b578-cb43e4e5eyj6`
- **参数名**: `SmuStdbyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter switches the SmuStdby on/off

######## 2. SmuDevErrorDetect

- **UUID**: `940168d-eeab-4151-a78e-381ce11c5706`
- **参数名**: `SmuDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 3. SmuSafetyEnable

- **UUID**: `940168d-eeab-4151-a78e-381ce11c67806`
- **参数名**: `SmuSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the safety Error Checking ON or OFF.

######## 4. SmuInitCheckApi

- **UUID**: `940168d-eeab-4151-a78e-381ce11c570gh6`
- **参数名**: `SmuInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the Smu_InitCheck detection and notification ON or OFF.

######## 5. SmuVersionInfoApi

- **UUID**: `ECUC:8ea4cb56-cf5e-4afc-95ce-cebac08ac0e6`
- **参数名**: `SmuVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Adds / removes the service Smu_GetVersionInfo() from the code.

######## 6. SmuCoreFSP0OutputEnable

- **UUID**: `bfec07fb-550f-423e-b578-sywnn876dk`
- **参数名**: `SmuCoreFSP0OutputEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter sets FSP[0] state to output if TRUE

######## 7. SmuCoreFSP1OutputEnable

- **UUID**: `bfec07fb-550f-423e-b578-cb467dhjeda6`
- **参数名**: `SmuCoreFSP1OutputEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter sets FSP[1] state to output if TRUE

######## 8. SmuCoreFSP0PortEnable

- **UUID**: `bfec07fb-550f-423e-b578-cb43e45689eda6`
- **参数名**: `SmuCoreFSP0PortEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter sets FSP[0] PORT enable TRUE

######## 9. SmuCoreFSP1PortEnable

- **UUID**: `bfec07fb-550f-423e-b578-cb43e4e5yudja6`
- **参数名**: `SmuCoreFSP1PortEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter sets FSP[1] PORT enable TRUE

######## 10. SmuCoreGlitchFilterSCU

- **UUID**: `bfec07fb-550f-423e-b578-cb43e4e5e89a6`
- **参数名**: `SmuCoreGlitchFilterSCU`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter sets glitch filter for SCU enabled

######## 11. SmuCoreGlitchFilterSTS

- **UUID**: `bfec07fb-550f-423e-b578-cb43e4e5fda6`
- **参数名**: `SmuCoreGlitchFilterSTS`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter sets glitch filter for SMU_STS enabled

####### ENUMERATION 类型参数

######## 1. SmuRuntimeApiMode

- **UUID**: `bfec07fb-550f-421e-b578-cb43a2eghta6`
- **参数名**: `SmuRuntimeApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `SMU_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the Runtime API mode

######## 2. SmuInitDeInitApiMode

- **UUID**: `bfec07fb-550f-421e-b578-cb43a2e1eda6`
- **参数名**: `SmuInitDeInitApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SMU_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `SMU_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `SMU_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: Defines the output value of the Init API mode

##### 15. CommonPublishedInformation

**容器属性**:

- **UUID**: `492f8482-3e2c-4bf1-b27f-01fd7a235788`
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
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 2. ArMinorVersion

- **UUID**: `73f87c7f-e230-4178-bff0-ea2704aae656`
- **参数名**: `ArMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 3. ArPatchVersion

- **UUID**: `2380135d-6778-417a-a34b-e100aad4dd54`
- **参数名**: `ArPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 4. SwMajorVersion

- **UUID**: `fca015e3-5f28-4cbe-8949-8fab87d86827`
- **参数名**: `SwMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 5. SwMinorVersion

- **UUID**: `14ab81e0-3d80-43dc-8b92-2a7e5a542df9`
- **参数名**: `SwMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 6. SwPatchVersion

- **UUID**: `32e37bfd-18b6-41d1-9248-a81dae0fe4c5`
- **参数名**: `SwPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 7. ModuleId

- **UUID**: `3b407478-6902-4f80-b7cf-f33b0854e638`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Module ID of this module from Module List

######## 8. VendorId

- **UUID**: `7d650b2d-4adb-41f0-aa8e-5f0c416501d1`
- **参数名**: `VendorId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `17`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Vendor ID of the dedicated implementation of this module according to the AUTOSAR vendor list

####### STRING 类型参数

######## 1. Release

- **UUID**: `3b407478-6902-4f40-b7cf-f33b0854e638`
- **参数名**: `Release`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `_TRICORE_TC397`
- **描述**: Aurix derivative used for the implementation

##### 16. SmuDemEventParameterRefsConf

**容器属性**:

- **UUID**: `ECUC:4c697a37-02d8-42df-8696-0c9f59aab8c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SmuDemEventParameterRefsConf`
- **多重性**: [0..1]

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId symbolic name. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **9** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SmuActivateRunStateFailureNotification

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695aa21788e`
- **引用名**: `SmuActivateRunStateFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to configured DEM event to report activate RUN state failure.

######## 2. SmuClearAlarmStatusFailureNotification

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695aa21898e`
- **引用名**: `SmuClearAlarmStatusFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to configured DEM event to report clear alarm status failure.

######## 3. SmuReleaseFSPFailureNotification

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695aa2erfg6e`
- **引用名**: `SmuReleaseFSPFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to configured DEM event to report release FSP failure.

######## 4. SmuCoreAliveFailureNotification

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695dbg1788e`
- **引用名**: `SmuCoreAliveFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to configured DEM event to report Smu_core_alive test failure.

######## 5. SmuRTStopFailureNotification

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695aa217yhui`
- **引用名**: `SmuRTStopFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to configured DEM event to report RT stop failure.

######## 6. SmuActivatePESFailureNotification

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695aa217ghns89`
- **引用名**: `SmuActivatePESFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to configured DEM event to activate PES failure.

######## 7. SmuActivateFSPFailureNotification

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695aa217898fhj`
- **引用名**: `SmuActivateFSPFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to configured DEM event to activate FSP failure.

######## 8. SmuSetAlarmStatusFailureNotification

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695aa217890hj`
- **引用名**: `SmuSetAlarmStatusFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to configured DEM event to set alarm status failure.

######## 9. SmuSffFailureNotification

- **UUID**: `ECUC:66c8e900-6197-42a3-8125-a695aa21780i8e`
- **引用名**: `SmuSffFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to configured DEM event for SFF test failure.

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

1. **Smu**
