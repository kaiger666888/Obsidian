# Uart - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:17

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Uart](#uart)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Uart

#### 基本信息

- **UUID**: `ECUC:13aa2440-e790-4121-9e12-3a380efb0d6b`
- **模块名称**: `Uart`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the UART Module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: IFX

*此版本无详细变更记录*

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. UartGeneral

**容器属性**:

- **UUID**: `a868aef7-06f0-5e10-9482-3b9f6ca77cb2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UartGeneral`
- **多重性**: [0..1]

**容器描述**:

General configuration (parameters) of the UART driver software module.

###### 参数配置

此容器包含 **15** 个参数：

####### INTEGER 类型参数

######## 1. UartIndex

- **UUID**: `a9361f42-ca28-4ec5-8a32-aca0597add15`
- **参数名**: `UartIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **描述**: Specifies the InstanceId of this module instance.

######## 2. UartTimeoutCount

- **UUID**: `ECUC:f4b834a6-9fce-4cf9-9f80-98e4a6ad9eed`
- **参数名**: `UartTimeoutCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4294967295`
- **取值范围**: [100..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the maximum time in nanoseconds to wait for hardware timeout errors(Reported as hardware access error).

####### BOOLEAN 类型参数

######## 1. UartDevErrorDetect

- **UUID**: `DCE:a4e951e4-be6b-4d72-b360-c13bb0bff7f6`
- **参数名**: `UartDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 2. UartRunTimeErrorDetect

- **UUID**: `DCE:a4e95104-be6b-4d72-b360-c13bb0bff7f6`
- **参数名**: `UartRunTimeErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: INFINEON_AURIX2G
- **描述**: Switches the Runtime Error Detection and Notification ON or OFF.

######## 3. UartSafetyEnable

- **UUID**: `13cc7127-ef8d-4893-b0e5-495c0b3a7765`
- **参数名**: `UartSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enable/Disable safety feature in Uart driver

######## 4. UartVersionInfoApi

- **UUID**: `3f862ba7-4f88-4980-950b-a3117f65e387`
- **参数名**: `UartVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Switches the Uart_GetVersionInfo function ON or OFF.

######## 5. UartInitCheckApi

- **UUID**: `2f362bd7-4f28-498d-95db-a31d7f65ed87`
- **参数名**: `UartInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Switches the Uart_InitCheck function ON or OFF.

######## 6. UartDeInitApi

- **UUID**: `2f362bd7-4f28-498d-95db-a31d7f99ed87`
- **参数名**: `UartDeInitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Switches the Uart_Deinit function ON or OFF.

######## 7. UartAbortReadApi

- **UUID**: `3f823ba7-4bf8-49f8-9f0b-a311ff65ef87`
- **参数名**: `UartAbortReadApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Switches the Uart_AbortRead function ON or OFF.

######## 8. UartAbortWriteApi

- **UUID**: `3f82dba7-4df8-49d8-9fdb-a312ff65ef87`
- **参数名**: `UartAbortWriteApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Switches the Uart_AbortWrite function ON or OFF.

######## 9. UartSleepEnable

- **UUID**: `13dc6427-ed8d-4484-b0d4-494cdb3a7764`
- **参数名**: `UartSleepEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enable/Disable parameter for the ASCLIN Hw module Sleep triggered by SCU

####### FLOAT 类型参数

######## 1. UartMainFunctionReadPeriod

- **UUID**: `ECUC:ca545039-b3f3-4a63-8b04-29ebac136e9d`
- **参数名**: `UartMainFunctionReadPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.005`
- **取值范围**: [0.0..10.0]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the period of main function Uart_MainFunction_Read in seconds. Uart driver does not require this information but the BSW scheduler.

######## 2. UartMainFunctionWritePeriod

- **UUID**: `ECUC:ca545039-b3f3-4a63-8b04-29ebac136r9d`
- **参数名**: `UartMainFunctionWritePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.005`
- **取值范围**: [0.0..10.0]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the period of main function Uart_MainFunction_Write in seconds. Uart driver does not require this information but the BSW scheduler.

####### ENUMERATION 类型参数

######## 1. UartCsrClksel

- **UUID**: `ECUC:03f6c9e0-e3b7-4907-84c0-a96e099b4435`
- **参数名**: `UartCsrClksel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ASCLINF`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ASCLINF` (来源: INFINEON_AURIX2G)
  - `ASCLINS` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the Baud Rate Logic Clock for the Uart Driver.

######## 2. UartInitDeInitApiMode

- **UUID**: `ECUC:7e0e69e5-6004-1956-a113-f0559f2409d6`
- **参数名**: `UartInitDeInitApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: Defines the privilege mode in which the Initialization and De-initialization APIs would operate.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. UartClockRef

- **UUID**: `ECUC:03f6c9e0-e3b7-4907-84c0-a96e099b4433`
- **引用名**: `UartClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePointConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePointConfig`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter refers to the system clock configured by MCU driver.This reference is used for BaudRate computation.

##### 2. UartConfigSet

**容器属性**:

- **UUID**: `439b823d-f723-43d7-b3d6-8e4c38733021`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UartConfigSet`
- **多重性**: [0..1]

**容器描述**:

This container contains the Channel configuration of the Uart driver. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exit once per configuration set.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. UartChannel

**容器属性**:

- **UUID**: `eee1d64f-d2e3-4e79-a5ed-c142334dee3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UartChannel`
- **多重性**: [1..12]

**容器描述**:

This container contains the configuration (parameters) of the UART Controller(s).

######## 参数配置

此容器包含 **17** 个参数：

######### INTEGER 类型参数

########## 1. UartBaudRate

- **UUID**: `8db8dbce-1d4b-4315-8d1b-edad5df02cb1`
- **参数名**: `UartBaudRate`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `9600`
- **取值范围**: [1000..6250000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the baud rate in bits per second of the UART channel. This parameter shall be disabled when 'UartAutoCalcBaudParams' is false

########## 2. UartChannelId

- **UUID**: `575c5e2f-5aba-43b2-be5d-e3b62b05a6e7`
- **参数名**: `UartChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..11]
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Identifies the UART channel.

########## 3. UartChanBaudNumerator

- **UUID**: `967b5282-8ce2-4638-9586-3a3a28391b69`
- **参数名**: `UartChanBaudNumerator`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `24`
- **取值范围**: [1..4095]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the BRG register numerator value used for Baudrate calculation. The value configured in this parameter will be written to the BRG.NUMERATOR register field. This parameter will be disabled when 'UartAutoCalcBaudParams' is true

########## 4. UartChanBaudDenominator

- **UUID**: `967b5282-8ce2-4638-9586-3a3a28394b69`
- **参数名**: `UartChanBaudDenominator`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1000`
- **取值范围**: [1..4095]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the BRG register Denominator value used for Baudrate calculation. The value configured in this parameter will be written to the BRG.DENOMINATOR register field.This parameter will be disabled when 'UartAutoCalcBaudParams' is true

########## 5. UartChanBaudPrescalar

- **UUID**: `96ab5282-8cea-46a8-9586-3a3a28394b69`
- **参数名**: `UartChanBaudPrescalar`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `24`
- **取值范围**: [0..4095]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the BITCON register Prescalar value used for Baudrate calculation. The value configured in this parameter will be written to the BITCON.PRESCALAR register field.This parameter will be disabled when 'UartAutoCalcBaudParams' is true

########## 6. UartChanBaudOverSampling

- **UUID**: `96ac5282-8cea-4628-9286-3a3a18394b69`
- **参数名**: `UartChanBaudOverSampling`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `9`
- **取值范围**: [3..15]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the BITCON register Oversampling value used for Baudrate calculation.The value configured in this parameter will be written to the BITCON.OVERSAMPLING register field. This parameter will be disabled when 'UartAutoCalcBaudParams' is true

########## 7. UartDataLength

- **UUID**: `a9361d42-cb28-4bc5-8ae2-aca0597ade15`
- **参数名**: `UartDataLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8`
- **取值范围**: [2..16]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the number of bits to be transmitted or recieved.

########## 8. UartStopBits

- **UUID**: `4f862ba7-4f88-4980-950b-a3117f65e387`
- **参数名**: `UartStopBits`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..2]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the number of stop bits Range is one or two.

######### BOOLEAN 类型参数

########## 1. UartAutoCalcBaudParams

- **UUID**: `13cc2127-e28d-4433-b0e5-495c1b3a7765`
- **参数名**: `UartAutoCalcBaudParams`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enable/Disable Automatic calculation of Asclin Baudrate params UartChanBaudNumerator, UartChanBaudDenominator, UartChanBaudPrescalar,UartChanBaudOVERSAMPLING

########## 2. UartCTSEnable

- **UUID**: `5aae2e0e1-309-8d1f-8142-45531dc8a9b0`
- **参数名**: `UartCTSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch to enable the CTS signal .

######### ENUMERATION 类型参数

########## 1. UartHwUnit

- **UUID**: `989b798d-d7b4-479e-909c-b8479ac98b69`
- **参数名**: `UartHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ASCLIN0`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ASCLIN0` (来源: INFINEON_AURIX2G)
  - `ASCLIN1` (来源: INFINEON_AURIX2G)
  - `ASCLIN2` (来源: INFINEON_AURIX2G)
  - `ASCLIN3` (来源: INFINEON_AURIX2G)
  - `ASCLIN4` (来源: INFINEON_AURIX2G)
  - `ASCLIN5` (来源: INFINEON_AURIX2G)
  - `ASCLIN6` (来源: INFINEON_AURIX2G)
  - `ASCLIN7` (来源: INFINEON_AURIX2G)
  - `ASCLIN8` (来源: INFINEON_AURIX2G)
  - `ASCLIN9` (来源: INFINEON_AURIX2G)
  - `ASCLIN10` (来源: INFINEON_AURIX2G)
  - `ASCLIN11` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the hardware unit used by Uart channel.

########## 2. UartRxPinSelection

- **UUID**: `571e4e1f-8aba-43b2-be1e-e2b62b02a6d7`
- **参数名**: `UartRxPinSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SELECT_A_PORT14_PIN1`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SELECT_A_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT15_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT14_PIN8` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `SELECT_G_PORT02_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT33_PIN8` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_G_PORT2_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT32_PIN2` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT33_PIN4` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT22_PIN4` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT13_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT13_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT21_PIN5` (来源: INFINEON_AURIX2G)
- **描述**: Selects the alternate input for the RX signal for the given Uart channel

########## 3. UartCTSPinSelection

- **UUID**: `571e4e1f-8aba-4302-be1e-e2b62b02a6d7`
- **参数名**: `UartCTSPinSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SELECT_CTS_A_PORT14_PIN9`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SELECT_CTS_A_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SELECT_CTS_A_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_CTS_B_PORT32_PIN4` (来源: INFINEON_AURIX2G)
  - `SELECT_CTS_A_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_CTS_B_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SELECT_CTS_A_PORT00_PIN12` (来源: INFINEON_AURIX2G)
- **描述**: Selects the alternate input for the CTS signal for the given Uart channel

########## 4. UartCTSPolarity

- **UUID**: `962b718d-d1b6-149e-139c-b8419ac68b46`
- **参数名**: `UartCTSPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `HIGH`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `LOW` (来源: INFINEON_AURIX2G)
  - `HIGH` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the active level or the RTS and CTS signals. Active means ready/clear to send.

########## 5. UartParityBit

- **UUID**: `939b718d-d2b4-429e-109c-b8489ac98b96`
- **参数名**: `UartParityBit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NOPARITY`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NOPARITY` (来源: INFINEON_AURIX2G)
  - `ODDPARITY` (来源: INFINEON_AURIX2G)
  - `EVENPARITY` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the parity even or odd or no parity.

########## 6. UartTxChannelMode

- **UUID**: `939b718d-d2b4-429e-109c-b8480ac98b96`
- **参数名**: `UartTxChannelMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INTERRUPT`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `POLLING` (来源: INFINEON_AURIX2G)
  - `INTERRUPT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the Tx channel mode polling or interrupt.

########## 7. UartRxChannelMode

- **UUID**: `939b718d-d2b4-429e-109c-b8489dc98b96`
- **参数名**: `UartRxChannelMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INTERRUPT`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `POLLING` (来源: INFINEON_AURIX2G)
  - `INTERRUPT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the Rx channel mode polling or interrupt.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. UartNotification

**容器属性**:

- **UUID**: `eea1d64f-d2e3-4b79-a5ed-ca42334dea3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UartNotification`
- **多重性**: [0..1]

**容器描述**:

This container contains the Notification function pointers .

########## 参数配置

此容器包含 **4** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. UartTransmitNotifPtr

- **UUID**: `999ccf11-8b4f-4719-abde-2f2d65e8614a`
- **参数名**: `UartTransmitNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

############ 2. UartReceiveNotifPtr

- **UUID**: `956fcf11-1b4f-4719-ab2e-2f2d75e8624a`
- **参数名**: `UartReceiveNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

############ 3. UartAbortTransmitNotifPtr

- **UUID**: `929fcf11-8b2f-4719-aaee-2f2d73e8614a`
- **参数名**: `UartAbortTransmitNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

############ 4. UartAbortReceiveNotifPtr

- **UUID**: `199fcf11-8a4f-4719-acee-2f2d75e7614a`
- **参数名**: `UartAbortReceiveNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

####### 2. UartNotification

**容器属性**:

- **UUID**: `eea1d64f-d2e3-4b79-a5ed-ca42334dea3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UartNotification`
- **多重性**: [0..1]

**容器描述**:

This container contains the Notification function pointers .

######## 参数配置

此容器包含 **4** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. UartTransmitNotifPtr

- **UUID**: `999ccf11-8b4f-4719-abde-2f2d65e8614a`
- **参数名**: `UartTransmitNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

########## 2. UartReceiveNotifPtr

- **UUID**: `956fcf11-1b4f-4719-ab2e-2f2d75e8624a`
- **参数名**: `UartReceiveNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

########## 3. UartAbortTransmitNotifPtr

- **UUID**: `929fcf11-8b2f-4719-aaee-2f2d73e8614a`
- **参数名**: `UartAbortTransmitNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

########## 4. UartAbortReceiveNotifPtr

- **UUID**: `199fcf11-8a4f-4719-acee-2f2d75e7614a`
- **参数名**: `UartAbortReceiveNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

##### 3. UartChannel

**容器属性**:

- **UUID**: `eee1d64f-d2e3-4e79-a5ed-c142334dee3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UartChannel`
- **多重性**: [1..12]

**容器描述**:

This container contains the configuration (parameters) of the UART Controller(s).

###### 参数配置

此容器包含 **17** 个参数：

####### INTEGER 类型参数

######## 1. UartBaudRate

- **UUID**: `8db8dbce-1d4b-4315-8d1b-edad5df02cb1`
- **参数名**: `UartBaudRate`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `9600`
- **取值范围**: [1000..6250000]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the baud rate in bits per second of the UART channel. This parameter shall be disabled when 'UartAutoCalcBaudParams' is false

######## 2. UartChannelId

- **UUID**: `575c5e2f-5aba-43b2-be5d-e3b62b05a6e7`
- **参数名**: `UartChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..11]
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Identifies the UART channel.

######## 3. UartChanBaudNumerator

- **UUID**: `967b5282-8ce2-4638-9586-3a3a28391b69`
- **参数名**: `UartChanBaudNumerator`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `24`
- **取值范围**: [1..4095]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the BRG register numerator value used for Baudrate calculation. The value configured in this parameter will be written to the BRG.NUMERATOR register field. This parameter will be disabled when 'UartAutoCalcBaudParams' is true

######## 4. UartChanBaudDenominator

- **UUID**: `967b5282-8ce2-4638-9586-3a3a28394b69`
- **参数名**: `UartChanBaudDenominator`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1000`
- **取值范围**: [1..4095]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the BRG register Denominator value used for Baudrate calculation. The value configured in this parameter will be written to the BRG.DENOMINATOR register field.This parameter will be disabled when 'UartAutoCalcBaudParams' is true

######## 5. UartChanBaudPrescalar

- **UUID**: `96ab5282-8cea-46a8-9586-3a3a28394b69`
- **参数名**: `UartChanBaudPrescalar`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `24`
- **取值范围**: [0..4095]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the BITCON register Prescalar value used for Baudrate calculation. The value configured in this parameter will be written to the BITCON.PRESCALAR register field.This parameter will be disabled when 'UartAutoCalcBaudParams' is true

######## 6. UartChanBaudOverSampling

- **UUID**: `96ac5282-8cea-4628-9286-3a3a18394b69`
- **参数名**: `UartChanBaudOverSampling`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `9`
- **取值范围**: [3..15]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the BITCON register Oversampling value used for Baudrate calculation.The value configured in this parameter will be written to the BITCON.OVERSAMPLING register field. This parameter will be disabled when 'UartAutoCalcBaudParams' is true

######## 7. UartDataLength

- **UUID**: `a9361d42-cb28-4bc5-8ae2-aca0597ade15`
- **参数名**: `UartDataLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8`
- **取值范围**: [2..16]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the number of bits to be transmitted or recieved.

######## 8. UartStopBits

- **UUID**: `4f862ba7-4f88-4980-950b-a3117f65e387`
- **参数名**: `UartStopBits`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..2]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Specifies the number of stop bits Range is one or two.

####### BOOLEAN 类型参数

######## 1. UartAutoCalcBaudParams

- **UUID**: `13cc2127-e28d-4433-b0e5-495c1b3a7765`
- **参数名**: `UartAutoCalcBaudParams`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enable/Disable Automatic calculation of Asclin Baudrate params UartChanBaudNumerator, UartChanBaudDenominator, UartChanBaudPrescalar,UartChanBaudOVERSAMPLING

######## 2. UartCTSEnable

- **UUID**: `5aae2e0e1-309-8d1f-8142-45531dc8a9b0`
- **参数名**: `UartCTSEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch to enable the CTS signal .

####### ENUMERATION 类型参数

######## 1. UartHwUnit

- **UUID**: `989b798d-d7b4-479e-909c-b8479ac98b69`
- **参数名**: `UartHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ASCLIN0`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ASCLIN0` (来源: INFINEON_AURIX2G)
  - `ASCLIN1` (来源: INFINEON_AURIX2G)
  - `ASCLIN2` (来源: INFINEON_AURIX2G)
  - `ASCLIN3` (来源: INFINEON_AURIX2G)
  - `ASCLIN4` (来源: INFINEON_AURIX2G)
  - `ASCLIN5` (来源: INFINEON_AURIX2G)
  - `ASCLIN6` (来源: INFINEON_AURIX2G)
  - `ASCLIN7` (来源: INFINEON_AURIX2G)
  - `ASCLIN8` (来源: INFINEON_AURIX2G)
  - `ASCLIN9` (来源: INFINEON_AURIX2G)
  - `ASCLIN10` (来源: INFINEON_AURIX2G)
  - `ASCLIN11` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the hardware unit used by Uart channel.

######## 2. UartRxPinSelection

- **UUID**: `571e4e1f-8aba-43b2-be1e-e2b62b02a6d7`
- **参数名**: `UartRxPinSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SELECT_A_PORT14_PIN1`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SELECT_A_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT15_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT14_PIN8` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `SELECT_G_PORT02_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT33_PIN8` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_G_PORT2_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT32_PIN2` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT33_PIN4` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT22_PIN4` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT13_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT13_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_A_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_B_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SELECT_C_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SELECT_D_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SELECT_E_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SELECT_F_PORT21_PIN5` (来源: INFINEON_AURIX2G)
- **描述**: Selects the alternate input for the RX signal for the given Uart channel

######## 3. UartCTSPinSelection

- **UUID**: `571e4e1f-8aba-4302-be1e-e2b62b02a6d7`
- **参数名**: `UartCTSPinSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SELECT_CTS_A_PORT14_PIN9`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SELECT_CTS_A_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SELECT_CTS_A_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_CTS_B_PORT32_PIN4` (来源: INFINEON_AURIX2G)
  - `SELECT_CTS_A_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `SELECT_CTS_B_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SELECT_CTS_A_PORT00_PIN12` (来源: INFINEON_AURIX2G)
- **描述**: Selects the alternate input for the CTS signal for the given Uart channel

######## 4. UartCTSPolarity

- **UUID**: `962b718d-d1b6-149e-139c-b8419ac68b46`
- **参数名**: `UartCTSPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `HIGH`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `LOW` (来源: INFINEON_AURIX2G)
  - `HIGH` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the active level or the RTS and CTS signals. Active means ready/clear to send.

######## 5. UartParityBit

- **UUID**: `939b718d-d2b4-429e-109c-b8489ac98b96`
- **参数名**: `UartParityBit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NOPARITY`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NOPARITY` (来源: INFINEON_AURIX2G)
  - `ODDPARITY` (来源: INFINEON_AURIX2G)
  - `EVENPARITY` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the parity even or odd or no parity.

######## 6. UartTxChannelMode

- **UUID**: `939b718d-d2b4-429e-109c-b8480ac98b96`
- **参数名**: `UartTxChannelMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INTERRUPT`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `POLLING` (来源: INFINEON_AURIX2G)
  - `INTERRUPT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the Tx channel mode polling or interrupt.

######## 7. UartRxChannelMode

- **UUID**: `939b718d-d2b4-429e-109c-b8489dc98b96`
- **参数名**: `UartRxChannelMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INTERRUPT`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `POLLING` (来源: INFINEON_AURIX2G)
  - `INTERRUPT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the Rx channel mode polling or interrupt.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. UartNotification

**容器属性**:

- **UUID**: `eea1d64f-d2e3-4b79-a5ed-ca42334dea3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UartNotification`
- **多重性**: [0..1]

**容器描述**:

This container contains the Notification function pointers .

######## 参数配置

此容器包含 **4** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. UartTransmitNotifPtr

- **UUID**: `999ccf11-8b4f-4719-abde-2f2d65e8614a`
- **参数名**: `UartTransmitNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

########## 2. UartReceiveNotifPtr

- **UUID**: `956fcf11-1b4f-4719-ab2e-2f2d75e8624a`
- **参数名**: `UartReceiveNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

########## 3. UartAbortTransmitNotifPtr

- **UUID**: `929fcf11-8b2f-4719-aaee-2f2d73e8614a`
- **参数名**: `UartAbortTransmitNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

########## 4. UartAbortReceiveNotifPtr

- **UUID**: `199fcf11-8a4f-4719-acee-2f2d75e7614a`
- **参数名**: `UartAbortReceiveNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

##### 4. UartNotification

**容器属性**:

- **UUID**: `eea1d64f-d2e3-4b79-a5ed-ca42334dea3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UartNotification`
- **多重性**: [0..1]

**容器描述**:

This container contains the Notification function pointers .

###### 参数配置

此容器包含 **4** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. UartTransmitNotifPtr

- **UUID**: `999ccf11-8b4f-4719-abde-2f2d65e8614a`
- **参数名**: `UartTransmitNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

######## 2. UartReceiveNotifPtr

- **UUID**: `956fcf11-1b4f-4719-ab2e-2f2d75e8624a`
- **参数名**: `UartReceiveNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

######## 3. UartAbortTransmitNotifPtr

- **UUID**: `929fcf11-8b2f-4719-aaee-2f2d73e8614a`
- **参数名**: `UartAbortTransmitNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

######## 4. UartAbortReceiveNotifPtr

- **UUID**: `199fcf11-8a4f-4719-acee-2f2d75e7614a`
- **参数名**: `UartAbortReceiveNotifPtr`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

##### 5. CommonPublishedInformation

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
- **默认值**: `10`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 5. SwMinorVersion

- **UUID**: `14ab81e0-3d80-43dc-8b92-247e5a542df9`
- **参数名**: `SwMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `40`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 6. SwPatchVersion

- **UUID**: `32e37bfd-18b6-41d1-9248-a81dbe0fe4c5`
- **参数名**: `SwPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..255]
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

- **UUID**: `3b407478-6902-4f40-b7cf-f33b0854e638`
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

1. **Uart**
