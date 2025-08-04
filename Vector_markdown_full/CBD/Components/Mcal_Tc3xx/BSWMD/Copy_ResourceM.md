# ResourceM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:10

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [ResourceM](#resourcem)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. ResourceM

#### 基本信息

- **UUID**: `ECUC:13aa2440-e790-4121-9e12-3a380efb0d6b`
- **模块名称**: `ResourceM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of RM (Resource Manager) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **3** 个配置容器：

##### 1. ResourceMMcalConfig

**容器属性**:

- **UUID**: `2b452b26-b1b5-4998-8a7f-b51e8d257ca4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ResourceMMcalConfig`
- **多重性**: [0..1]

**容器描述**:

General container to select Master Core and allocate resources

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. ResourceMMasterCore

- **UUID**: `ECUC:31505abb-2290-4c99-bdb7-d0909f0440f2`
- **参数名**: `ResourceMMasterCore`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CORE0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CORE0` (来源: INFINEON_AURIX2G)
  - `CORE1` (来源: INFINEON_AURIX2G)
  - `CORE2` (来源: INFINEON_AURIX2G)
  - `CORE3` (来源: INFINEON_AURIX2G)
  - `CORE4` (来源: INFINEON_AURIX2G)
  - `CORE5` (来源: INFINEON_AURIX2G)
- **描述**: Select Master core.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. ResourceMMcalCore

**容器属性**:

- **UUID**: `2b452b26-b1b5-4999-8a7f-b51e8d257ca4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ResourceMMcalCore`
- **多重性**: [1..6]

**容器描述**:

General container to allocate Mcal resources to cores

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. ResourceMCoreID

- **UUID**: `ECUC:31505abb-2290-4c00-bdb7-d0909f0440f2`
- **参数名**: `ResourceMCoreID`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CORE0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CORE0` (来源: INFINEON_AURIX2G)
  - `CORE1` (来源: INFINEON_AURIX2G)
  - `CORE2` (来源: INFINEON_AURIX2G)
  - `CORE3` (来源: INFINEON_AURIX2G)
  - `CORE4` (来源: INFINEON_AURIX2G)
  - `CORE5` (来源: INFINEON_AURIX2G)
- **描述**: Select Master core.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ResourceMAllocation

**容器属性**:

- **UUID**: `2b452b26-b1b5-5000-8a7f-b51e8d257ca4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ResourceMAllocation`
- **多重性**: [0..1]

**容器描述**:

Container to allocate module resources.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. ResourceMModuleName

- **UUID**: `ECUC:31505abb-2296-4c99-bdb7-d0909f0440f2`
- **参数名**: `ResourceMModuleName`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC` (来源: INFINEON_AURIX2G)
  - `PWM` (来源: INFINEON_AURIX2G)
  - `ICU` (来源: INFINEON_AURIX2G)
  - `GPT` (来源: INFINEON_AURIX2G)
  - `DMA` (来源: INFINEON_AURIX2G)
  - `CAN` (来源: INFINEON_AURIX2G)
  - `STM` (来源: INFINEON_AURIX2G)
  - `SPI` (来源: INFINEON_AURIX2G)
  - `SENT` (来源: INFINEON_AURIX2G)
  - `OCU` (来源: INFINEON_AURIX2G)
  - `ETH` (来源: INFINEON_AURIX2G)
  - `LIN` (来源: INFINEON_AURIX2G)
- **描述**: Module name.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. ResourceMResourceRef

- **UUID**: `ECUC:c945dd5e-1a5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `ResourceMResourceRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
  - `/AUTOSAR/EcucDefs/Pwm/PwmChannelConfigSet/PwmChannel`
  - `/AUTOSAR/EcucDefs/Icu/IcuConfigSet/IcuChannel`
  - `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
  - `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController`
  - `/AURIX2G/EcucDefs/Sent/SentConfigSet/SentChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuStmAllocationConf`
  - `/AUTOSAR/EcucDefs/Spi/SpiHwConfiguration/SpiHwConfigurationQspi`
  - `/AUTOSAR/EcucDefs/Ocu/OcuConfigSet/OcuChannel`
  - `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
  - `/AUTOSAR/EcucDefs/Lin/LinGlobalConfig/LinChannel`
- **描述**: This parameter contains reference to resource

####### 2. ResourceMAllocation

**容器属性**:

- **UUID**: `2b452b26-b1b5-5000-8a7f-b51e8d257ca4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ResourceMAllocation`
- **多重性**: [0..1]

**容器描述**:

Container to allocate module resources.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. ResourceMModuleName

- **UUID**: `ECUC:31505abb-2296-4c99-bdb7-d0909f0440f2`
- **参数名**: `ResourceMModuleName`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC` (来源: INFINEON_AURIX2G)
  - `PWM` (来源: INFINEON_AURIX2G)
  - `ICU` (来源: INFINEON_AURIX2G)
  - `GPT` (来源: INFINEON_AURIX2G)
  - `DMA` (来源: INFINEON_AURIX2G)
  - `CAN` (来源: INFINEON_AURIX2G)
  - `STM` (来源: INFINEON_AURIX2G)
  - `SPI` (来源: INFINEON_AURIX2G)
  - `SENT` (来源: INFINEON_AURIX2G)
  - `OCU` (来源: INFINEON_AURIX2G)
  - `ETH` (来源: INFINEON_AURIX2G)
  - `LIN` (来源: INFINEON_AURIX2G)
- **描述**: Module name.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. ResourceMResourceRef

- **UUID**: `ECUC:c945dd5e-1a5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `ResourceMResourceRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
  - `/AUTOSAR/EcucDefs/Pwm/PwmChannelConfigSet/PwmChannel`
  - `/AUTOSAR/EcucDefs/Icu/IcuConfigSet/IcuChannel`
  - `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
  - `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController`
  - `/AURIX2G/EcucDefs/Sent/SentConfigSet/SentChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuStmAllocationConf`
  - `/AUTOSAR/EcucDefs/Spi/SpiHwConfiguration/SpiHwConfigurationQspi`
  - `/AUTOSAR/EcucDefs/Ocu/OcuConfigSet/OcuChannel`
  - `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
  - `/AUTOSAR/EcucDefs/Lin/LinGlobalConfig/LinChannel`
- **描述**: This parameter contains reference to resource

##### 2. ResourceMMcalCore

**容器属性**:

- **UUID**: `2b452b26-b1b5-4999-8a7f-b51e8d257ca4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ResourceMMcalCore`
- **多重性**: [1..6]

**容器描述**:

General container to allocate Mcal resources to cores

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. ResourceMCoreID

- **UUID**: `ECUC:31505abb-2290-4c00-bdb7-d0909f0440f2`
- **参数名**: `ResourceMCoreID`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CORE0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CORE0` (来源: INFINEON_AURIX2G)
  - `CORE1` (来源: INFINEON_AURIX2G)
  - `CORE2` (来源: INFINEON_AURIX2G)
  - `CORE3` (来源: INFINEON_AURIX2G)
  - `CORE4` (来源: INFINEON_AURIX2G)
  - `CORE5` (来源: INFINEON_AURIX2G)
- **描述**: Select Master core.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ResourceMAllocation

**容器属性**:

- **UUID**: `2b452b26-b1b5-5000-8a7f-b51e8d257ca4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ResourceMAllocation`
- **多重性**: [0..1]

**容器描述**:

Container to allocate module resources.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. ResourceMModuleName

- **UUID**: `ECUC:31505abb-2296-4c99-bdb7-d0909f0440f2`
- **参数名**: `ResourceMModuleName`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC` (来源: INFINEON_AURIX2G)
  - `PWM` (来源: INFINEON_AURIX2G)
  - `ICU` (来源: INFINEON_AURIX2G)
  - `GPT` (来源: INFINEON_AURIX2G)
  - `DMA` (来源: INFINEON_AURIX2G)
  - `CAN` (来源: INFINEON_AURIX2G)
  - `STM` (来源: INFINEON_AURIX2G)
  - `SPI` (来源: INFINEON_AURIX2G)
  - `SENT` (来源: INFINEON_AURIX2G)
  - `OCU` (来源: INFINEON_AURIX2G)
  - `ETH` (来源: INFINEON_AURIX2G)
  - `LIN` (来源: INFINEON_AURIX2G)
- **描述**: Module name.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. ResourceMResourceRef

- **UUID**: `ECUC:c945dd5e-1a5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `ResourceMResourceRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
  - `/AUTOSAR/EcucDefs/Pwm/PwmChannelConfigSet/PwmChannel`
  - `/AUTOSAR/EcucDefs/Icu/IcuConfigSet/IcuChannel`
  - `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
  - `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController`
  - `/AURIX2G/EcucDefs/Sent/SentConfigSet/SentChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuStmAllocationConf`
  - `/AUTOSAR/EcucDefs/Spi/SpiHwConfiguration/SpiHwConfigurationQspi`
  - `/AUTOSAR/EcucDefs/Ocu/OcuConfigSet/OcuChannel`
  - `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
  - `/AUTOSAR/EcucDefs/Lin/LinGlobalConfig/LinChannel`
- **描述**: This parameter contains reference to resource

##### 3. ResourceMAllocation

**容器属性**:

- **UUID**: `2b452b26-b1b5-5000-8a7f-b51e8d257ca4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ResourceMAllocation`
- **多重性**: [0..1]

**容器描述**:

Container to allocate module resources.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. ResourceMModuleName

- **UUID**: `ECUC:31505abb-2296-4c99-bdb7-d0909f0440f2`
- **参数名**: `ResourceMModuleName`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ADC`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ADC` (来源: INFINEON_AURIX2G)
  - `PWM` (来源: INFINEON_AURIX2G)
  - `ICU` (来源: INFINEON_AURIX2G)
  - `GPT` (来源: INFINEON_AURIX2G)
  - `DMA` (来源: INFINEON_AURIX2G)
  - `CAN` (来源: INFINEON_AURIX2G)
  - `STM` (来源: INFINEON_AURIX2G)
  - `SPI` (来源: INFINEON_AURIX2G)
  - `SENT` (来源: INFINEON_AURIX2G)
  - `OCU` (来源: INFINEON_AURIX2G)
  - `ETH` (来源: INFINEON_AURIX2G)
  - `LIN` (来源: INFINEON_AURIX2G)
- **描述**: Module name.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. ResourceMResourceRef

- **UUID**: `ECUC:c945dd5e-1a5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `ResourceMResourceRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
  - `/AUTOSAR/EcucDefs/Pwm/PwmChannelConfigSet/PwmChannel`
  - `/AUTOSAR/EcucDefs/Icu/IcuConfigSet/IcuChannel`
  - `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
  - `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController`
  - `/AURIX2G/EcucDefs/Sent/SentConfigSet/SentChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuStmAllocationConf`
  - `/AUTOSAR/EcucDefs/Spi/SpiHwConfiguration/SpiHwConfigurationQspi`
  - `/AUTOSAR/EcucDefs/Ocu/OcuConfigSet/OcuChannel`
  - `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
  - `/AUTOSAR/EcucDefs/Lin/LinGlobalConfig/LinChannel`
- **描述**: This parameter contains reference to resource

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

1. **ResourceM**
