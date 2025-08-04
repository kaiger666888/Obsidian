# vBaseEnv - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:14

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [vBaseEnv](#vbaseenv)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. vBaseEnv

#### 基本信息

- **UUID**: `cd5d2b77-7c41-4c5b-86d7-ec8d25b5b55e`
- **模块名称**: `vBaseEnv`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

The Vector Base Environment (vBaseEnv) provides everything necessary to get a microcontroller project compiled/linked and performs a basic hardware setup (inlcuding memory init, PLL init, Port init and Watchdog init) in order to get a cyclic runtime behavior.
#vBRS #OS #vLinkGen #Startup
#Vector

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 0.01.00

- **状态**: prototype
- **发布日期**: 2018-06-11
- **发布者**: vibwa

**变更内容**:

#### 配置容器

本模块包含 **30** 个配置容器：

##### 1. vBaseEnvGeneral

**容器属性**:

- **UUID**: `5084d491-1d5d-48e2-8e41-4ab6029f32ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBaseEnvTestedDerivativeRef

- **UUID**: `5c069ae2-ce60-49d1-8494-6679883a4e43`
- **引用名**: `vBaseEnvTestedDerivativeRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vBaseEnvDerivativeInformation`
- **完整路径**: `/MICROSAR/vBaseEnv/vBaseEnvGeneral/vBaseEnvDerivativeInformation`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Select a Tested Derivative from the list of supported ones.

###### 配置容器

本模块包含 **29** 个配置容器：

####### 1. vBaseEnvDerivativeInformation

**容器属性**:

- **UUID**: `2c77318d-738c-43db-b2cd-99d2d85156c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvDerivativeInformation`
- **多重性**: [1..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **14** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvCpuMaxFrequency

- **UUID**: `ba23d239-2143-4656-bb01-bd72aa3f610f`
- **参数名**: `vBaseEnvCpuMaxFrequency`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100000000`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the maximum frequency of this derivative.
This value is used to validate the vBRS PLL configuration.

########## 2. vBaseEnvAvailableChannels_Flexray

- **UUID**: `2c58ac76-8424-4f2b-8458-fc2d5826f0e1`
- **参数名**: `vBaseEnvAvailableChannels_Flexray`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of Flexray channels, available on this derivative.

########## 3. vBaseEnvAvailableChannels_Can

- **UUID**: `a17836b8-f071-4666-9ee0-ba303f5a3534`
- **参数名**: `vBaseEnvAvailableChannels_Can`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of CAN channels, available on this derivative.

########## 4. vBaseEnvAvailableChannels_Lin

- **UUID**: `46ed0478-2cf8-4ca0-8d59-96a3adc09901`
- **参数名**: `vBaseEnvAvailableChannels_Lin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of LIN channels, available on this derivative.

########## 5. vBaseEnvAvailableChannels_Ethernet

- **UUID**: `3542c1f3-c9fb-4ea1-890c-cabe858701ba`
- **参数名**: `vBaseEnvAvailableChannels_Ethernet`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of Ethernet channels, available on this derivative.

########## 6. vBaseEnvCpuCoreAmount

- **UUID**: `d770a952-9a90-4534-9c63-9fedc2166b04`
- **参数名**: `vBaseEnvCpuCoreAmount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of cores, available on this derivative.
This value will be generated into vBrsCfg.h as
BRS_CPU_CORE_AMOUNT

########## 7. vBaseEnvCpuInitCore

- **UUID**: `3251fcec-50ee-4a60-acd4-a8562fe47a30`
- **参数名**: `vBaseEnvCpuInitCore`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the core ID of the core, which should be used for general initialization.
For normal, this is the boot core.
This value will be generated into vBrsCfg.h as
BRS_CPU_INIT_CORE

########## 8. vBaseEnvAvailableChannels_Hyperbus

- **UUID**: `3e60240a-d3a2-4de4-b246-b6a8bd2d0c78`
- **参数名**: `vBaseEnvAvailableChannels_Hyperbus`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of Hyperbus channels, available on this derivative.

########## 9. vBaseEnvAvailableChannels_I2c

- **UUID**: `c04ed28f-ace3-4748-80e8-0716941da4f9`
- **参数名**: `vBaseEnvAvailableChannels_I2c`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of I2C channels, available on this derivative.

########## 10. vBaseEnvAvailableChannels_Spi

- **UUID**: `6678f63b-3328-436f-b3b7-65b4a4020c68`
- **参数名**: `vBaseEnvAvailableChannels_Spi`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of Spi channels, available on this derivative.

######### STRING 类型参数

########## 1. vBaseEnvTestedDerivative

- **UUID**: `a00a3575-fcc4-4f42-b149-4fa6d00ea1b6`
- **参数名**: `vBaseEnvTestedDerivative`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the correct Mcu_Derivative value of this derivative.
This value will be generated into vBrsCfg.h as
BRS_DERIVATIVE_x

########## 2. vBaseEnvTestedDerivativeDescription

- **UUID**: `62d154b0-f82a-4891-a6c0-0816e988f0f7`
- **参数名**: `vBaseEnvTestedDerivativeDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describe here more precisely this derivative.
This description is only textual information for the user.

########## 3. vBaseEnvUsedManual

- **UUID**: `93f47fc4-890e-493c-a209-2dc0166c8039`
- **参数名**: `vBaseEnvUsedManual`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Manual and version, used for the development of the vBaseEnv preconfig

######### ENUMERATION 类型参数

########## 1. vBaseEnvCpuCore

- **UUID**: `f0d41453-7510-49bd-b117-a3e6bd397e54`
- **参数名**: `vBaseEnvCpuCore`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `OTHER` (来源: Vector Informatik)
  - `ARC_EM6` (来源: Vector Informatik)
  - `CORTEX_M0` (来源: Vector Informatik)
  - `CORTEX_M0PLUS` (来源: Vector Informatik)
  - `CORTEX_M3` (来源: Vector Informatik)
  - `CORTEX_M4` (来源: Vector Informatik)
  - `CORTEX_M4F` (来源: Vector Informatik)
  - `CORTEX_M7` (来源: Vector Informatik)
  - `CORTEX_M33` (来源: Vector Informatik)
  - `CORTEX_R4` (来源: Vector Informatik)
  - `CORTEX_R4F` (来源: Vector Informatik)
  - `CORTEX_R5` (来源: Vector Informatik)
  - `CORTEX_R5F` (来源: Vector Informatik)
  - `CORTEX_R7` (来源: Vector Informatik)
  - `CORTEX_R52` (来源: Vector Informatik)
  - `E200Z0` (来源: Vector Informatik)
  - `E200Z210` (来源: Vector Informatik)
  - `E200Z215` (来源: Vector Informatik)
  - `E200Z225` (来源: Vector Informatik)
  - `E200Z410` (来源: Vector Informatik)
  - `E200Z420` (来源: Vector Informatik)
  - `E200Z425` (来源: Vector Informatik)
  - `E200Z710` (来源: Vector Informatik)
  - `E200Z720` (来源: Vector Informatik)
  - `E200Z726` (来源: Vector Informatik)
  - `E200Z759` (来源: Vector Informatik)
  - `G3K` (来源: Vector Informatik)
  - `G3KH` (来源: Vector Informatik)
  - `G3M` (来源: Vector Informatik)
  - `G4MH` (来源: Vector Informatik)
  - `TC161` (来源: Vector Informatik)
  - `TC162` (来源: Vector Informatik)
  - `TC18` (来源: Vector Informatik)
  - `RISCV32` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the core architecture of this derivative.
This value will be generated into vBrsCfg.h as
BRS_CPU_CORE_x

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. vBaseEnvAdditionalParameters

**容器属性**:

- **UUID**: `b8e6419f-522a-4258-8358-22c51c77e4a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvAdditionalParameters`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Additional parameters for generation of additional defines, if necessary for the depending platform.

########## 参数配置

此容器包含 **10** 个参数：

########### BOOLEAN 类型参数

############ 1. vBaseEnvPowerDownModes

- **UUID**: `898a7dfa-a750-4879-a587-22cabff2b55d`
- **参数名**: `vBaseEnvPowerDownModes`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure, if Power Down Modes to be used for your derivative

########### STRING 类型参数

############ 1. vBaseEnvDerivativeGroup

- **UUID**: `2baac809-cdc2-447d-9f20-a18beb8d886d`
- **参数名**: `vBaseEnvDerivativeGroup`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the Derivative Group of this derivative

########### ENUMERATION 类型参数

############ 1. vBaseEnvPllGroup

- **UUID**: `67f97e88-2817-4d79-9876-bbc3026774c0`
- **参数名**: `vBaseEnvPllGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `A5` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `D1` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `E1` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the PLL Group of your derivative

############ 2. vBaseEnvClockGroup

- **UUID**: `64e82637-3452-4005-833e-ec2c010b3866`
- **参数名**: `vBaseEnvClockGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Clock Group of your derivative

############ 3. vBaseEnvPortGroup

- **UUID**: `e9fa5662-e278-4ce0-a764-9145857ecddb`
- **参数名**: `vBaseEnvPortGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `B1` (来源: Vector Informatik)
  - `B2` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Port Group of your derivative

############ 4. vBaseEnvProtectionGroup

- **UUID**: `ee45913a-dd7e-46ba-a6e6-2cdc2aa9d5ea`
- **参数名**: `vBaseEnvProtectionGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
  - `NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Protection Group of your derivative

############ 5. vBaseEnvResetGroup

- **UUID**: `4e273998-de1f-4220-b71a-3434a80b031a`
- **参数名**: `vBaseEnvResetGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Reset Group of your derivative

############ 6. vBaseEnvWatchdogGroup

- **UUID**: `b8ee0017-d3f4-4f99-b7f5-9125c02ac2ee`
- **参数名**: `vBaseEnvWatchdogGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `A5` (来源: Vector Informatik)
  - `A6` (来源: Vector Informatik)
  - `A7` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Watchdog Group of your derivative

############ 7. vBaseEnvOpModeGroup

- **UUID**: `fe20961e-dd08-42da-852d-984a16b8f502`
- **参数名**: `vBaseEnvOpModeGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Operation Mode Group of your derivative

############ 8. vBaseEnvUserModeAccessGroup

- **UUID**: `6b314d2d-7838-4204-a9ed-acdcd694018c`
- **参数名**: `vBaseEnvUserModeAccessGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the User Mode Access Group of your derivative

######### 2. vBaseEnvMemLayoutHwRegion

**容器属性**:

- **UUID**: `67914085-ee03-4fe5-9d01-5ff933738178`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvMemLayoutHwRegion`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to structure the configuration parameters of hardware memory regions.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvHwRegionStartAddress

- **UUID**: `0cc34936-30b0-4113-8e8b-12ce777c4a07`
- **参数名**: `vBaseEnvHwRegionStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of the hardware memory region.

############ 2. vBaseEnvHwRegionSize

- **UUID**: `d56f3651-1f2a-4460-ad87-a74f34e6c2ae`
- **参数名**: `vBaseEnvHwRegionSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the hardware memory region.

############ 3. vBaseEnvHwRegionEccAlignment

- **UUID**: `8a3ee4a1-ae6b-4124-a67f-b669ac35fc9d`
- **参数名**: `vBaseEnvHwRegionEccAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Required ECC Alignment of the hardware memory region.

########### ENUMERATION 类型参数

############ 1. vBaseEnvHwRegionType

- **UUID**: `eec4f426-5c61-4f4e-bb84-9b79a5fd74d6`
- **参数名**: `vBaseEnvHwRegionType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RAM` (来源: Vector Informatik)
  - `ROM` (来源: Vector Informatik)
  - `NVRAM` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of the hardware memory region.
This parameter is necessary for some linkers (e.g. Tasking), to distinguish between RAM/ROM/NVRAM.

######### 3. vBaseEnvClockSettings

**容器属性**:

- **UUID**: `95c6c99c-78c7-405a-8641-69e062c29cf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvClockSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for derivative specific default clock settings (oscillator + peripherals).
This allows solving actions to update the depending frequncy settings in the vBRSHwConfig container.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvOscClock

- **UUID**: `bad86329-f64d-46ce-87c0-0beedbb27820`
- **参数名**: `vBaseEnvOscClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of the board specific external oscillator.

############ 2. vBaseEnvTimebaseClock

- **UUID**: `63919a76-214f-4231-8fbb-d197ccbd76f6`
- **参数名**: `vBaseEnvTimebaseClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation (normally used as CPU core clock).

############ 3. vBaseEnvPeriphClock

- **UUID**: `2211f913-7211-4a2a-ad6f-7b183e303ead`
- **参数名**: `vBaseEnvPeriphClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of the controller peripherals, at least for the default timer, used by the OS.
If the frequencies for communication peripherals differ from this peripheral clock, they could be configured through the depending communictaion peripheral clock parameter.

############ 4. vBaseEnvCanClock

- **UUID**: `237fe032-59c4-4f1b-9435-13cfcce46ef4`
- **参数名**: `vBaseEnvCanClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of CAN driver peripheral clock.

############ 5. vBaseEnvLinClock

- **UUID**: `77a40253-8044-475e-b72b-91f1f103b571`
- **参数名**: `vBaseEnvLinClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of LIN driver peripheral clock.

############ 6. vBaseEnvFlexrayClock

- **UUID**: `9c723370-7286-4a2a-af3d-0a22a1c24f82`
- **参数名**: `vBaseEnvFlexrayClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of FlexRay driver peripheral clock.

############ 7. vBaseEnvEthernetClock

- **UUID**: `e30ab088-36c9-4df1-a52d-95c0b8cb285d`
- **参数名**: `vBaseEnvEthernetClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of EtherNet driver peripheral clock.

############ 8. vBaseEnvHyperbusClock

- **UUID**: `43f04887-b69b-4946-b254-c6aa14b43873`
- **参数名**: `vBaseEnvHyperbusClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Hyperbus driver peripheral clock.

############ 9. vBaseEnvI2cClock

- **UUID**: `dbe1d32a-047f-4168-9415-f66bad94a402`
- **参数名**: `vBaseEnvI2cClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of I2C driver peripheral clock.

############ 10. vBaseEnvSpiClock

- **UUID**: `76a75dd0-f430-4714-92cf-1aa5972e9882`
- **参数名**: `vBaseEnvSpiClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Spi driver peripheral clock.

####### 2. vBaseEnvAdditionalParameters

**容器属性**:

- **UUID**: `b8e6419f-522a-4258-8358-22c51c77e4a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvAdditionalParameters`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Additional parameters for generation of additional defines, if necessary for the depending platform.

######## 参数配置

此容器包含 **10** 个参数：

######### BOOLEAN 类型参数

########## 1. vBaseEnvPowerDownModes

- **UUID**: `898a7dfa-a750-4879-a587-22cabff2b55d`
- **参数名**: `vBaseEnvPowerDownModes`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure, if Power Down Modes to be used for your derivative

######### STRING 类型参数

########## 1. vBaseEnvDerivativeGroup

- **UUID**: `2baac809-cdc2-447d-9f20-a18beb8d886d`
- **参数名**: `vBaseEnvDerivativeGroup`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the Derivative Group of this derivative

######### ENUMERATION 类型参数

########## 1. vBaseEnvPllGroup

- **UUID**: `67f97e88-2817-4d79-9876-bbc3026774c0`
- **参数名**: `vBaseEnvPllGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `A5` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `D1` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `E1` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the PLL Group of your derivative

########## 2. vBaseEnvClockGroup

- **UUID**: `64e82637-3452-4005-833e-ec2c010b3866`
- **参数名**: `vBaseEnvClockGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Clock Group of your derivative

########## 3. vBaseEnvPortGroup

- **UUID**: `e9fa5662-e278-4ce0-a764-9145857ecddb`
- **参数名**: `vBaseEnvPortGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `B1` (来源: Vector Informatik)
  - `B2` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Port Group of your derivative

########## 4. vBaseEnvProtectionGroup

- **UUID**: `ee45913a-dd7e-46ba-a6e6-2cdc2aa9d5ea`
- **参数名**: `vBaseEnvProtectionGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
  - `NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Protection Group of your derivative

########## 5. vBaseEnvResetGroup

- **UUID**: `4e273998-de1f-4220-b71a-3434a80b031a`
- **参数名**: `vBaseEnvResetGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Reset Group of your derivative

########## 6. vBaseEnvWatchdogGroup

- **UUID**: `b8ee0017-d3f4-4f99-b7f5-9125c02ac2ee`
- **参数名**: `vBaseEnvWatchdogGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `A5` (来源: Vector Informatik)
  - `A6` (来源: Vector Informatik)
  - `A7` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Watchdog Group of your derivative

########## 7. vBaseEnvOpModeGroup

- **UUID**: `fe20961e-dd08-42da-852d-984a16b8f502`
- **参数名**: `vBaseEnvOpModeGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Operation Mode Group of your derivative

########## 8. vBaseEnvUserModeAccessGroup

- **UUID**: `6b314d2d-7838-4204-a9ed-acdcd694018c`
- **参数名**: `vBaseEnvUserModeAccessGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the User Mode Access Group of your derivative

####### 3. vBaseEnvMemLayoutHwRegion

**容器属性**:

- **UUID**: `67914085-ee03-4fe5-9d01-5ff933738178`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvMemLayoutHwRegion`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to structure the configuration parameters of hardware memory regions.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvHwRegionStartAddress

- **UUID**: `0cc34936-30b0-4113-8e8b-12ce777c4a07`
- **参数名**: `vBaseEnvHwRegionStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of the hardware memory region.

########## 2. vBaseEnvHwRegionSize

- **UUID**: `d56f3651-1f2a-4460-ad87-a74f34e6c2ae`
- **参数名**: `vBaseEnvHwRegionSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the hardware memory region.

########## 3. vBaseEnvHwRegionEccAlignment

- **UUID**: `8a3ee4a1-ae6b-4124-a67f-b669ac35fc9d`
- **参数名**: `vBaseEnvHwRegionEccAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Required ECC Alignment of the hardware memory region.

######### ENUMERATION 类型参数

########## 1. vBaseEnvHwRegionType

- **UUID**: `eec4f426-5c61-4f4e-bb84-9b79a5fd74d6`
- **参数名**: `vBaseEnvHwRegionType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RAM` (来源: Vector Informatik)
  - `ROM` (来源: Vector Informatik)
  - `NVRAM` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of the hardware memory region.
This parameter is necessary for some linkers (e.g. Tasking), to distinguish between RAM/ROM/NVRAM.

####### 4. vBaseEnvClockSettings

**容器属性**:

- **UUID**: `95c6c99c-78c7-405a-8641-69e062c29cf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvClockSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for derivative specific default clock settings (oscillator + peripherals).
This allows solving actions to update the depending frequncy settings in the vBRSHwConfig container.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvOscClock

- **UUID**: `bad86329-f64d-46ce-87c0-0beedbb27820`
- **参数名**: `vBaseEnvOscClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of the board specific external oscillator.

########## 2. vBaseEnvTimebaseClock

- **UUID**: `63919a76-214f-4231-8fbb-d197ccbd76f6`
- **参数名**: `vBaseEnvTimebaseClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation (normally used as CPU core clock).

########## 3. vBaseEnvPeriphClock

- **UUID**: `2211f913-7211-4a2a-ad6f-7b183e303ead`
- **参数名**: `vBaseEnvPeriphClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of the controller peripherals, at least for the default timer, used by the OS.
If the frequencies for communication peripherals differ from this peripheral clock, they could be configured through the depending communictaion peripheral clock parameter.

########## 4. vBaseEnvCanClock

- **UUID**: `237fe032-59c4-4f1b-9435-13cfcce46ef4`
- **参数名**: `vBaseEnvCanClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of CAN driver peripheral clock.

########## 5. vBaseEnvLinClock

- **UUID**: `77a40253-8044-475e-b72b-91f1f103b571`
- **参数名**: `vBaseEnvLinClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of LIN driver peripheral clock.

########## 6. vBaseEnvFlexrayClock

- **UUID**: `9c723370-7286-4a2a-af3d-0a22a1c24f82`
- **参数名**: `vBaseEnvFlexrayClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of FlexRay driver peripheral clock.

########## 7. vBaseEnvEthernetClock

- **UUID**: `e30ab088-36c9-4df1-a52d-95c0b8cb285d`
- **参数名**: `vBaseEnvEthernetClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of EtherNet driver peripheral clock.

########## 8. vBaseEnvHyperbusClock

- **UUID**: `43f04887-b69b-4946-b254-c6aa14b43873`
- **参数名**: `vBaseEnvHyperbusClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Hyperbus driver peripheral clock.

########## 9. vBaseEnvI2cClock

- **UUID**: `dbe1d32a-047f-4168-9415-f66bad94a402`
- **参数名**: `vBaseEnvI2cClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of I2C driver peripheral clock.

########## 10. vBaseEnvSpiClock

- **UUID**: `76a75dd0-f430-4714-92cf-1aa5972e9882`
- **参数名**: `vBaseEnvSpiClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Spi driver peripheral clock.

####### 5. vBaseEnvMemLayoutHwRegion

**容器属性**:

- **UUID**: `517ff7b1-ca16-4b22-a1b7-b27a2390d92f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvMemLayoutHwRegion`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to structure the configuration parameters of hardware memory regions.

####### 6. vBaseEnvInterruptHandling

**容器属性**:

- **UUID**: `5a6bc7a8-95e1-4d35-92d8-dad872b4fbb9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvInterruptHandling`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for family specific default interrupt settings

######## 配置容器

本模块包含 **14** 个配置容器：

######### 1. vBaseEnvCan

**容器属性**:

- **UUID**: `451fe3fa-d259-4663-a518-f2e044f67d6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `a70aa265-a413-4e33-99fe-35bed058efe2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `4e5452f7-0e33-4db7-b278-4fb5f1c59342`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `17a6698c-215e-4022-b971-660f61448c1c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############## 3. vBaseEnvIsrInterruptSource

- **UUID**: `ebd4214c-557c-461b-bf67-0820ecd0b5cd`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 2. vBaseEnvChannel

**容器属性**:

- **UUID**: `a70aa265-a413-4e33-99fe-35bed058efe2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `4e5452f7-0e33-4db7-b278-4fb5f1c59342`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `17a6698c-215e-4022-b971-660f61448c1c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `ebd4214c-557c-461b-bf67-0820ecd0b5cd`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 3. vBaseEnvLin

**容器属性**:

- **UUID**: `94d8f1fc-3c8a-4ad3-9d92-5471c72d5c94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `4a2f382c-fa69-4fe0-a745-f3a704e24e47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `9b3119d3-8c12-42e1-bd43-2cf8740ebeb7`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `429ada8b-93b4-44a2-8ec1-abc82c33232d`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############## 3. vBaseEnvIsrInterruptSource

- **UUID**: `42c64964-38e2-4691-9d12-85d6e3629020`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 4. vBaseEnvChannel

**容器属性**:

- **UUID**: `4a2f382c-fa69-4fe0-a745-f3a704e24e47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `9b3119d3-8c12-42e1-bd43-2cf8740ebeb7`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `429ada8b-93b4-44a2-8ec1-abc82c33232d`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `42c64964-38e2-4691-9d12-85d6e3629020`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 5. vBaseEnvFlexray

**容器属性**:

- **UUID**: `2cbfd57a-cd96-4313-a0ae-94222b331d0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `131db306-7656-44d5-9b3f-372d16387b0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `dd35061c-b1c2-4e96-b859-7df07977b418`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `04db9a0b-ca5c-4fb4-a60d-594f6216392c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############## 3. vBaseEnvIsrInterruptSource

- **UUID**: `aa8c240b-9427-4e23-a9d3-8473baaa965c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 6. vBaseEnvChannel

**容器属性**:

- **UUID**: `131db306-7656-44d5-9b3f-372d16387b0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `dd35061c-b1c2-4e96-b859-7df07977b418`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `04db9a0b-ca5c-4fb4-a60d-594f6216392c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `aa8c240b-9427-4e23-a9d3-8473baaa965c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 7. vBaseEnvEthernet

**容器属性**:

- **UUID**: `2ab3b67f-9e27-4a21-b067-3c567df25b7d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `0911853b-f95e-48d9-a91e-a9813877ac7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `7286691d-d55b-43bd-ac98-6916e5655101`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `37357d8f-3ab6-46da-8ac8-b1f8ad8b40ff`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############## 3. vBaseEnvIsrInterruptSource

- **UUID**: `45ccbe36-749c-49dd-97b2-f5691530bdc0`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 8. vBaseEnvChannel

**容器属性**:

- **UUID**: `0911853b-f95e-48d9-a91e-a9813877ac7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `7286691d-d55b-43bd-ac98-6916e5655101`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `37357d8f-3ab6-46da-8ac8-b1f8ad8b40ff`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `45ccbe36-749c-49dd-97b2-f5691530bdc0`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 9. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `c5dc0332-1f44-412c-8ed5-d9bc01da42cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `2fb8456a-0e80-4102-96db-d4d403e7f869`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `7246a15d-007c-409c-9255-b69796f1a9d4`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `09547154-1498-41e3-ab46-a3803f94600f`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############## 3. vBaseEnvIsrInterruptSource

- **UUID**: `2ff27a30-a956-4d39-ad39-82d5421195b5`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 10. vBaseEnvChannel

**容器属性**:

- **UUID**: `2fb8456a-0e80-4102-96db-d4d403e7f869`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `7246a15d-007c-409c-9255-b69796f1a9d4`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `09547154-1498-41e3-ab46-a3803f94600f`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `2ff27a30-a956-4d39-ad39-82d5421195b5`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 11. vBaseEnvI2c

**容器属性**:

- **UUID**: `6a580f8d-1de8-4f9f-bfdf-eae2d53f6343`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `ed508309-983a-4e1b-9706-14df8f0bd9cb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `1c8e1683-f6bd-4da7-ae30-981dd20b5bf9`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `47ef3894-e0ab-4810-b1ff-761b8fad5bb7`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############## 3. vBaseEnvIsrInterruptSource

- **UUID**: `bdc812e9-6aa7-44fc-8d70-80eb20290daf`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 12. vBaseEnvChannel

**容器属性**:

- **UUID**: `ed508309-983a-4e1b-9706-14df8f0bd9cb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `1c8e1683-f6bd-4da7-ae30-981dd20b5bf9`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `47ef3894-e0ab-4810-b1ff-761b8fad5bb7`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `bdc812e9-6aa7-44fc-8d70-80eb20290daf`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 13. vBaseEnvSpi

**容器属性**:

- **UUID**: `b782e61f-1eb0-4c68-ad36-27fc03273d2f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvSpi`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `59783252-d501-48a3-be38-53b4c22bc41c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `c421c56c-ea53-4550-81e8-f4d554b6fdc6`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `b984cdf2-7f54-45b6-880a-0d838dd471b9`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############## 3. vBaseEnvIsrInterruptSource

- **UUID**: `cc10d3c0-f508-4d4e-883d-78a71cf59450`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######### 14. vBaseEnvChannel

**容器属性**:

- **UUID**: `59783252-d501-48a3-be38-53b4c22bc41c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `c421c56c-ea53-4550-81e8-f4d554b6fdc6`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `b984cdf2-7f54-45b6-880a-0d838dd471b9`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `cc10d3c0-f508-4d4e-883d-78a71cf59450`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 7. vBaseEnvCan

**容器属性**:

- **UUID**: `451fe3fa-d259-4663-a518-f2e044f67d6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `a70aa265-a413-4e33-99fe-35bed058efe2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `4e5452f7-0e33-4db7-b278-4fb5f1c59342`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `17a6698c-215e-4022-b971-660f61448c1c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `ebd4214c-557c-461b-bf67-0820ecd0b5cd`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 8. vBaseEnvChannel

**容器属性**:

- **UUID**: `a70aa265-a413-4e33-99fe-35bed058efe2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `4e5452f7-0e33-4db7-b278-4fb5f1c59342`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `17a6698c-215e-4022-b971-660f61448c1c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `ebd4214c-557c-461b-bf67-0820ecd0b5cd`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 9. vBaseEnvLin

**容器属性**:

- **UUID**: `94d8f1fc-3c8a-4ad3-9d92-5471c72d5c94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `4a2f382c-fa69-4fe0-a745-f3a704e24e47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `9b3119d3-8c12-42e1-bd43-2cf8740ebeb7`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `429ada8b-93b4-44a2-8ec1-abc82c33232d`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `42c64964-38e2-4691-9d12-85d6e3629020`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 10. vBaseEnvChannel

**容器属性**:

- **UUID**: `4a2f382c-fa69-4fe0-a745-f3a704e24e47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `9b3119d3-8c12-42e1-bd43-2cf8740ebeb7`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `429ada8b-93b4-44a2-8ec1-abc82c33232d`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `42c64964-38e2-4691-9d12-85d6e3629020`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 11. vBaseEnvFlexray

**容器属性**:

- **UUID**: `2cbfd57a-cd96-4313-a0ae-94222b331d0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `131db306-7656-44d5-9b3f-372d16387b0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `dd35061c-b1c2-4e96-b859-7df07977b418`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `04db9a0b-ca5c-4fb4-a60d-594f6216392c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `aa8c240b-9427-4e23-a9d3-8473baaa965c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 12. vBaseEnvChannel

**容器属性**:

- **UUID**: `131db306-7656-44d5-9b3f-372d16387b0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `dd35061c-b1c2-4e96-b859-7df07977b418`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `04db9a0b-ca5c-4fb4-a60d-594f6216392c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `aa8c240b-9427-4e23-a9d3-8473baaa965c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 13. vBaseEnvEthernet

**容器属性**:

- **UUID**: `2ab3b67f-9e27-4a21-b067-3c567df25b7d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `0911853b-f95e-48d9-a91e-a9813877ac7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `7286691d-d55b-43bd-ac98-6916e5655101`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `37357d8f-3ab6-46da-8ac8-b1f8ad8b40ff`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `45ccbe36-749c-49dd-97b2-f5691530bdc0`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 14. vBaseEnvChannel

**容器属性**:

- **UUID**: `0911853b-f95e-48d9-a91e-a9813877ac7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `7286691d-d55b-43bd-ac98-6916e5655101`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `37357d8f-3ab6-46da-8ac8-b1f8ad8b40ff`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `45ccbe36-749c-49dd-97b2-f5691530bdc0`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 15. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `c5dc0332-1f44-412c-8ed5-d9bc01da42cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `2fb8456a-0e80-4102-96db-d4d403e7f869`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `7246a15d-007c-409c-9255-b69796f1a9d4`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `09547154-1498-41e3-ab46-a3803f94600f`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `2ff27a30-a956-4d39-ad39-82d5421195b5`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 16. vBaseEnvChannel

**容器属性**:

- **UUID**: `2fb8456a-0e80-4102-96db-d4d403e7f869`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `7246a15d-007c-409c-9255-b69796f1a9d4`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `09547154-1498-41e3-ab46-a3803f94600f`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `2ff27a30-a956-4d39-ad39-82d5421195b5`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 17. vBaseEnvI2c

**容器属性**:

- **UUID**: `6a580f8d-1de8-4f9f-bfdf-eae2d53f6343`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `ed508309-983a-4e1b-9706-14df8f0bd9cb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `1c8e1683-f6bd-4da7-ae30-981dd20b5bf9`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `47ef3894-e0ab-4810-b1ff-761b8fad5bb7`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `bdc812e9-6aa7-44fc-8d70-80eb20290daf`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 18. vBaseEnvChannel

**容器属性**:

- **UUID**: `ed508309-983a-4e1b-9706-14df8f0bd9cb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `1c8e1683-f6bd-4da7-ae30-981dd20b5bf9`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `47ef3894-e0ab-4810-b1ff-761b8fad5bb7`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `bdc812e9-6aa7-44fc-8d70-80eb20290daf`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 19. vBaseEnvSpi

**容器属性**:

- **UUID**: `b782e61f-1eb0-4c68-ad36-27fc03273d2f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvSpi`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `59783252-d501-48a3-be38-53b4c22bc41c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `c421c56c-ea53-4550-81e8-f4d554b6fdc6`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `b984cdf2-7f54-45b6-880a-0d838dd471b9`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `cc10d3c0-f508-4d4e-883d-78a71cf59450`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 20. vBaseEnvChannel

**容器属性**:

- **UUID**: `59783252-d501-48a3-be38-53b4c22bc41c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `c421c56c-ea53-4550-81e8-f4d554b6fdc6`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `b984cdf2-7f54-45b6-880a-0d838dd471b9`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `cc10d3c0-f508-4d4e-883d-78a71cf59450`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 21. vBaseEnvPeripheralClocks

**容器属性**:

- **UUID**: `7204be40-e226-4fc8-94b2-99b2d31b0bb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvPeripheralClocks`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for family specific default peripheral clock settings

######## 配置容器

本模块包含 **7** 个配置容器：

######### 1. vBaseEnvCan

**容器属性**:

- **UUID**: `16953022-2882-44de-85d9-fbd534995dc3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvCan_Clock

- **UUID**: `38bbe5a7-4c50-44b3-800d-38ad05f8a427`
- **参数名**: `vBaseEnvCan_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of CAN driver peripheral clock.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vBaseEnvCan_ClockRef

- **UUID**: `10005c4d-597e-4c80-9d0c-1846315834b4`
- **引用名**: `vBaseEnvCan_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for CAN peripheral clock setting.

######### 2. vBaseEnvLin

**容器属性**:

- **UUID**: `1d9b0444-3a94-480f-b1b7-5bab6c833512`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvLin_Clock

- **UUID**: `d15e8388-e8b0-44d9-ad17-53b089102b7f`
- **参数名**: `vBaseEnvLin_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of LIN driver peripheral clock.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vBaseEnvLin_ClockRef

- **UUID**: `103738af-fdb0-4141-9970-175cedb0ebfb`
- **引用名**: `vBaseEnvLin_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for LIN peripheral clock setting.

######### 3. vBaseEnvFlexray

**容器属性**:

- **UUID**: `12e6ef72-a1c3-4d36-bf1d-9903fd1a64af`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvFlexray_Clock

- **UUID**: `8b4dd0b8-0945-4e8d-aa9c-b556b848e984`
- **参数名**: `vBaseEnvFlexray_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of FlexRay driver peripheral clock.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vBaseEnvFlexray_ClockRef

- **UUID**: `fd657ce0-7a1b-4617-8b91-820a466b6bb8`
- **引用名**: `vBaseEnvFlexray_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for FlexRay peripheral clock setting.

######### 4. vBaseEnvEthernet

**容器属性**:

- **UUID**: `3148881d-91b4-4386-9179-8037d07bb898`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvEthernet_Clock

- **UUID**: `0cbbf93a-e102-44fd-900d-cdbcd8932216`
- **参数名**: `vBaseEnvEthernet_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of EtherNet driver peripheral clock.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vBaseEnvEthernet_ClockRef

- **UUID**: `4ef49ae5-a390-4cb9-846e-48d8bb6ca0e4`
- **引用名**: `vBaseEnvEthernet_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for EtherNet peripheral clock setting.

######### 5. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `faea3e8d-9bab-41a6-b927-dfcfabf24027`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvHyperbus_Clock

- **UUID**: `e06337e0-e742-4bab-9b58-c72593eaab14`
- **参数名**: `vBaseEnvHyperbus_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Hyperbus driver peripheral clock.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vBaseEnvHyperbus_ClockRef

- **UUID**: `1d1c4c36-88e7-48cc-818c-f54c09ac2794`
- **引用名**: `vBaseEnvHyperbus_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for Hyperbus peripheral clock setting.

######### 6. vBaseEnvI2c

**容器属性**:

- **UUID**: `0d793117-aebb-4feb-bb64-e2709fd141df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvI2c_Clock

- **UUID**: `af7760ab-61bd-4909-803f-925f4f6638fc`
- **参数名**: `vBaseEnvI2c_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of I2C driver peripheral clock.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vBaseEnvI2c_ClockRef

- **UUID**: `8dace219-3411-43eb-8b71-7c3bf113b69c`
- **引用名**: `vBaseEnvI2c_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for I2C peripheral clock setting.

######### 7. vBaseEnvSpi

**容器属性**:

- **UUID**: `65914f10-55c6-4bda-9e8b-65652bee9ad2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvSpi`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvSpi_Clock

- **UUID**: `9201db51-51b8-4182-8fee-cc748a160225`
- **参数名**: `vBaseEnvSpi_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Spi driver peripheral clock.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vBaseEnvSpi_ClockRef

- **UUID**: `f974d0a7-959d-4a28-9ae4-12ed2f1287e8`
- **引用名**: `vBaseEnvSpi_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for Spi peripheral clock setting.

####### 22. vBaseEnvCan

**容器属性**:

- **UUID**: `16953022-2882-44de-85d9-fbd534995dc3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvCan_Clock

- **UUID**: `38bbe5a7-4c50-44b3-800d-38ad05f8a427`
- **参数名**: `vBaseEnvCan_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of CAN driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvCan_ClockRef

- **UUID**: `10005c4d-597e-4c80-9d0c-1846315834b4`
- **引用名**: `vBaseEnvCan_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for CAN peripheral clock setting.

####### 23. vBaseEnvLin

**容器属性**:

- **UUID**: `1d9b0444-3a94-480f-b1b7-5bab6c833512`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvLin_Clock

- **UUID**: `d15e8388-e8b0-44d9-ad17-53b089102b7f`
- **参数名**: `vBaseEnvLin_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of LIN driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvLin_ClockRef

- **UUID**: `103738af-fdb0-4141-9970-175cedb0ebfb`
- **引用名**: `vBaseEnvLin_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for LIN peripheral clock setting.

####### 24. vBaseEnvFlexray

**容器属性**:

- **UUID**: `12e6ef72-a1c3-4d36-bf1d-9903fd1a64af`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvFlexray_Clock

- **UUID**: `8b4dd0b8-0945-4e8d-aa9c-b556b848e984`
- **参数名**: `vBaseEnvFlexray_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of FlexRay driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvFlexray_ClockRef

- **UUID**: `fd657ce0-7a1b-4617-8b91-820a466b6bb8`
- **引用名**: `vBaseEnvFlexray_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for FlexRay peripheral clock setting.

####### 25. vBaseEnvEthernet

**容器属性**:

- **UUID**: `3148881d-91b4-4386-9179-8037d07bb898`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvEthernet_Clock

- **UUID**: `0cbbf93a-e102-44fd-900d-cdbcd8932216`
- **参数名**: `vBaseEnvEthernet_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of EtherNet driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvEthernet_ClockRef

- **UUID**: `4ef49ae5-a390-4cb9-846e-48d8bb6ca0e4`
- **引用名**: `vBaseEnvEthernet_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for EtherNet peripheral clock setting.

####### 26. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `faea3e8d-9bab-41a6-b927-dfcfabf24027`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvHyperbus_Clock

- **UUID**: `e06337e0-e742-4bab-9b58-c72593eaab14`
- **参数名**: `vBaseEnvHyperbus_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Hyperbus driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvHyperbus_ClockRef

- **UUID**: `1d1c4c36-88e7-48cc-818c-f54c09ac2794`
- **引用名**: `vBaseEnvHyperbus_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for Hyperbus peripheral clock setting.

####### 27. vBaseEnvI2c

**容器属性**:

- **UUID**: `0d793117-aebb-4feb-bb64-e2709fd141df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvI2c_Clock

- **UUID**: `af7760ab-61bd-4909-803f-925f4f6638fc`
- **参数名**: `vBaseEnvI2c_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of I2C driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvI2c_ClockRef

- **UUID**: `8dace219-3411-43eb-8b71-7c3bf113b69c`
- **引用名**: `vBaseEnvI2c_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for I2C peripheral clock setting.

####### 28. vBaseEnvSpi

**容器属性**:

- **UUID**: `65914f10-55c6-4bda-9e8b-65652bee9ad2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvSpi`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvSpi_Clock

- **UUID**: `9201db51-51b8-4182-8fee-cc748a160225`
- **参数名**: `vBaseEnvSpi_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Spi driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvSpi_ClockRef

- **UUID**: `f974d0a7-959d-4a28-9ae4-12ed2f1287e8`
- **引用名**: `vBaseEnvSpi_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for Spi peripheral clock setting.

####### 29. vBaseEnvStartupStackSettings

**容器属性**:

- **UUID**: `cf544d9c-fdb5-43a0-ae4e-038350216485`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvStartupStackSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for family specific startup stack settings, if they differ to the default settings

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvStackAlignment

- **UUID**: `35ed3050-d006-4f69-be9e-ba979c6043e5`
- **参数名**: `vBaseEnvStackAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the startup stack alignment for each core.
This value will be validated in the vLinkGen stack section.
This value is only needed, if the default value 4 is not sufficient for this platform.

########## 2. vBaseEnvStackEndAlignment

- **UUID**: `365e6fed-142c-4e72-bd85-63e5df913928`
- **参数名**: `vBaseEnvStackEndAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the startup stack end alignment for each core.
This value will be validated in the vLinkGen stack section.
This value is only needed, if the default value 4 is not sufficient for this platform.

########## 3. vBaseEnvStackSize

- **UUID**: `56a730b2-0aa5-45c4-8d3d-17f32e4d2ab5`
- **参数名**: `vBaseEnvStackSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1024`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the startup stack size for each core.
This value will be validated in the vLinkGen stack section and generated into vBrs_Lcfg.c as StartupStackSize.
This value is only needed, if the default value 1024 is not sufficient for this platform.

##### 2. vBaseEnvDerivativeInformation

**容器属性**:

- **UUID**: `2c77318d-738c-43db-b2cd-99d2d85156c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvDerivativeInformation`
- **多重性**: [1..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **14** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvCpuMaxFrequency

- **UUID**: `ba23d239-2143-4656-bb01-bd72aa3f610f`
- **参数名**: `vBaseEnvCpuMaxFrequency`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100000000`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the maximum frequency of this derivative.
This value is used to validate the vBRS PLL configuration.

######## 2. vBaseEnvAvailableChannels_Flexray

- **UUID**: `2c58ac76-8424-4f2b-8458-fc2d5826f0e1`
- **参数名**: `vBaseEnvAvailableChannels_Flexray`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of Flexray channels, available on this derivative.

######## 3. vBaseEnvAvailableChannels_Can

- **UUID**: `a17836b8-f071-4666-9ee0-ba303f5a3534`
- **参数名**: `vBaseEnvAvailableChannels_Can`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of CAN channels, available on this derivative.

######## 4. vBaseEnvAvailableChannels_Lin

- **UUID**: `46ed0478-2cf8-4ca0-8d59-96a3adc09901`
- **参数名**: `vBaseEnvAvailableChannels_Lin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of LIN channels, available on this derivative.

######## 5. vBaseEnvAvailableChannels_Ethernet

- **UUID**: `3542c1f3-c9fb-4ea1-890c-cabe858701ba`
- **参数名**: `vBaseEnvAvailableChannels_Ethernet`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of Ethernet channels, available on this derivative.

######## 6. vBaseEnvCpuCoreAmount

- **UUID**: `d770a952-9a90-4534-9c63-9fedc2166b04`
- **参数名**: `vBaseEnvCpuCoreAmount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of cores, available on this derivative.
This value will be generated into vBrsCfg.h as
BRS_CPU_CORE_AMOUNT

######## 7. vBaseEnvCpuInitCore

- **UUID**: `3251fcec-50ee-4a60-acd4-a8562fe47a30`
- **参数名**: `vBaseEnvCpuInitCore`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the core ID of the core, which should be used for general initialization.
For normal, this is the boot core.
This value will be generated into vBrsCfg.h as
BRS_CPU_INIT_CORE

######## 8. vBaseEnvAvailableChannels_Hyperbus

- **UUID**: `3e60240a-d3a2-4de4-b246-b6a8bd2d0c78`
- **参数名**: `vBaseEnvAvailableChannels_Hyperbus`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of Hyperbus channels, available on this derivative.

######## 9. vBaseEnvAvailableChannels_I2c

- **UUID**: `c04ed28f-ace3-4748-80e8-0716941da4f9`
- **参数名**: `vBaseEnvAvailableChannels_I2c`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of I2C channels, available on this derivative.

######## 10. vBaseEnvAvailableChannels_Spi

- **UUID**: `6678f63b-3328-436f-b3b7-65b4a4020c68`
- **参数名**: `vBaseEnvAvailableChannels_Spi`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the amount of Spi channels, available on this derivative.

####### STRING 类型参数

######## 1. vBaseEnvTestedDerivative

- **UUID**: `a00a3575-fcc4-4f42-b149-4fa6d00ea1b6`
- **参数名**: `vBaseEnvTestedDerivative`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the correct Mcu_Derivative value of this derivative.
This value will be generated into vBrsCfg.h as
BRS_DERIVATIVE_x

######## 2. vBaseEnvTestedDerivativeDescription

- **UUID**: `62d154b0-f82a-4891-a6c0-0816e988f0f7`
- **参数名**: `vBaseEnvTestedDerivativeDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describe here more precisely this derivative.
This description is only textual information for the user.

######## 3. vBaseEnvUsedManual

- **UUID**: `93f47fc4-890e-493c-a209-2dc0166c8039`
- **参数名**: `vBaseEnvUsedManual`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Manual and version, used for the development of the vBaseEnv preconfig

####### ENUMERATION 类型参数

######## 1. vBaseEnvCpuCore

- **UUID**: `f0d41453-7510-49bd-b117-a3e6bd397e54`
- **参数名**: `vBaseEnvCpuCore`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `OTHER` (来源: Vector Informatik)
  - `ARC_EM6` (来源: Vector Informatik)
  - `CORTEX_M0` (来源: Vector Informatik)
  - `CORTEX_M0PLUS` (来源: Vector Informatik)
  - `CORTEX_M3` (来源: Vector Informatik)
  - `CORTEX_M4` (来源: Vector Informatik)
  - `CORTEX_M4F` (来源: Vector Informatik)
  - `CORTEX_M7` (来源: Vector Informatik)
  - `CORTEX_M33` (来源: Vector Informatik)
  - `CORTEX_R4` (来源: Vector Informatik)
  - `CORTEX_R4F` (来源: Vector Informatik)
  - `CORTEX_R5` (来源: Vector Informatik)
  - `CORTEX_R5F` (来源: Vector Informatik)
  - `CORTEX_R7` (来源: Vector Informatik)
  - `CORTEX_R52` (来源: Vector Informatik)
  - `E200Z0` (来源: Vector Informatik)
  - `E200Z210` (来源: Vector Informatik)
  - `E200Z215` (来源: Vector Informatik)
  - `E200Z225` (来源: Vector Informatik)
  - `E200Z410` (来源: Vector Informatik)
  - `E200Z420` (来源: Vector Informatik)
  - `E200Z425` (来源: Vector Informatik)
  - `E200Z710` (来源: Vector Informatik)
  - `E200Z720` (来源: Vector Informatik)
  - `E200Z726` (来源: Vector Informatik)
  - `E200Z759` (来源: Vector Informatik)
  - `G3K` (来源: Vector Informatik)
  - `G3KH` (来源: Vector Informatik)
  - `G3M` (来源: Vector Informatik)
  - `G4MH` (来源: Vector Informatik)
  - `TC161` (来源: Vector Informatik)
  - `TC162` (来源: Vector Informatik)
  - `TC18` (来源: Vector Informatik)
  - `RISCV32` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the core architecture of this derivative.
This value will be generated into vBrsCfg.h as
BRS_CPU_CORE_x

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. vBaseEnvAdditionalParameters

**容器属性**:

- **UUID**: `b8e6419f-522a-4258-8358-22c51c77e4a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvAdditionalParameters`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Additional parameters for generation of additional defines, if necessary for the depending platform.

######## 参数配置

此容器包含 **10** 个参数：

######### BOOLEAN 类型参数

########## 1. vBaseEnvPowerDownModes

- **UUID**: `898a7dfa-a750-4879-a587-22cabff2b55d`
- **参数名**: `vBaseEnvPowerDownModes`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure, if Power Down Modes to be used for your derivative

######### STRING 类型参数

########## 1. vBaseEnvDerivativeGroup

- **UUID**: `2baac809-cdc2-447d-9f20-a18beb8d886d`
- **参数名**: `vBaseEnvDerivativeGroup`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the Derivative Group of this derivative

######### ENUMERATION 类型参数

########## 1. vBaseEnvPllGroup

- **UUID**: `67f97e88-2817-4d79-9876-bbc3026774c0`
- **参数名**: `vBaseEnvPllGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `A5` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `D1` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `E1` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the PLL Group of your derivative

########## 2. vBaseEnvClockGroup

- **UUID**: `64e82637-3452-4005-833e-ec2c010b3866`
- **参数名**: `vBaseEnvClockGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Clock Group of your derivative

########## 3. vBaseEnvPortGroup

- **UUID**: `e9fa5662-e278-4ce0-a764-9145857ecddb`
- **参数名**: `vBaseEnvPortGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `B1` (来源: Vector Informatik)
  - `B2` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Port Group of your derivative

########## 4. vBaseEnvProtectionGroup

- **UUID**: `ee45913a-dd7e-46ba-a6e6-2cdc2aa9d5ea`
- **参数名**: `vBaseEnvProtectionGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
  - `NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Protection Group of your derivative

########## 5. vBaseEnvResetGroup

- **UUID**: `4e273998-de1f-4220-b71a-3434a80b031a`
- **参数名**: `vBaseEnvResetGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Reset Group of your derivative

########## 6. vBaseEnvWatchdogGroup

- **UUID**: `b8ee0017-d3f4-4f99-b7f5-9125c02ac2ee`
- **参数名**: `vBaseEnvWatchdogGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `A5` (来源: Vector Informatik)
  - `A6` (来源: Vector Informatik)
  - `A7` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Watchdog Group of your derivative

########## 7. vBaseEnvOpModeGroup

- **UUID**: `fe20961e-dd08-42da-852d-984a16b8f502`
- **参数名**: `vBaseEnvOpModeGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Operation Mode Group of your derivative

########## 8. vBaseEnvUserModeAccessGroup

- **UUID**: `6b314d2d-7838-4204-a9ed-acdcd694018c`
- **参数名**: `vBaseEnvUserModeAccessGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the User Mode Access Group of your derivative

####### 2. vBaseEnvMemLayoutHwRegion

**容器属性**:

- **UUID**: `67914085-ee03-4fe5-9d01-5ff933738178`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvMemLayoutHwRegion`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to structure the configuration parameters of hardware memory regions.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvHwRegionStartAddress

- **UUID**: `0cc34936-30b0-4113-8e8b-12ce777c4a07`
- **参数名**: `vBaseEnvHwRegionStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of the hardware memory region.

########## 2. vBaseEnvHwRegionSize

- **UUID**: `d56f3651-1f2a-4460-ad87-a74f34e6c2ae`
- **参数名**: `vBaseEnvHwRegionSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the hardware memory region.

########## 3. vBaseEnvHwRegionEccAlignment

- **UUID**: `8a3ee4a1-ae6b-4124-a67f-b669ac35fc9d`
- **参数名**: `vBaseEnvHwRegionEccAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Required ECC Alignment of the hardware memory region.

######### ENUMERATION 类型参数

########## 1. vBaseEnvHwRegionType

- **UUID**: `eec4f426-5c61-4f4e-bb84-9b79a5fd74d6`
- **参数名**: `vBaseEnvHwRegionType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RAM` (来源: Vector Informatik)
  - `ROM` (来源: Vector Informatik)
  - `NVRAM` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of the hardware memory region.
This parameter is necessary for some linkers (e.g. Tasking), to distinguish between RAM/ROM/NVRAM.

####### 3. vBaseEnvClockSettings

**容器属性**:

- **UUID**: `95c6c99c-78c7-405a-8641-69e062c29cf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvClockSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for derivative specific default clock settings (oscillator + peripherals).
This allows solving actions to update the depending frequncy settings in the vBRSHwConfig container.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvOscClock

- **UUID**: `bad86329-f64d-46ce-87c0-0beedbb27820`
- **参数名**: `vBaseEnvOscClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of the board specific external oscillator.

########## 2. vBaseEnvTimebaseClock

- **UUID**: `63919a76-214f-4231-8fbb-d197ccbd76f6`
- **参数名**: `vBaseEnvTimebaseClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation (normally used as CPU core clock).

########## 3. vBaseEnvPeriphClock

- **UUID**: `2211f913-7211-4a2a-ad6f-7b183e303ead`
- **参数名**: `vBaseEnvPeriphClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of the controller peripherals, at least for the default timer, used by the OS.
If the frequencies for communication peripherals differ from this peripheral clock, they could be configured through the depending communictaion peripheral clock parameter.

########## 4. vBaseEnvCanClock

- **UUID**: `237fe032-59c4-4f1b-9435-13cfcce46ef4`
- **参数名**: `vBaseEnvCanClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of CAN driver peripheral clock.

########## 5. vBaseEnvLinClock

- **UUID**: `77a40253-8044-475e-b72b-91f1f103b571`
- **参数名**: `vBaseEnvLinClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of LIN driver peripheral clock.

########## 6. vBaseEnvFlexrayClock

- **UUID**: `9c723370-7286-4a2a-af3d-0a22a1c24f82`
- **参数名**: `vBaseEnvFlexrayClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of FlexRay driver peripheral clock.

########## 7. vBaseEnvEthernetClock

- **UUID**: `e30ab088-36c9-4df1-a52d-95c0b8cb285d`
- **参数名**: `vBaseEnvEthernetClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of EtherNet driver peripheral clock.

########## 8. vBaseEnvHyperbusClock

- **UUID**: `43f04887-b69b-4946-b254-c6aa14b43873`
- **参数名**: `vBaseEnvHyperbusClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Hyperbus driver peripheral clock.

########## 9. vBaseEnvI2cClock

- **UUID**: `dbe1d32a-047f-4168-9415-f66bad94a402`
- **参数名**: `vBaseEnvI2cClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of I2C driver peripheral clock.

########## 10. vBaseEnvSpiClock

- **UUID**: `76a75dd0-f430-4714-92cf-1aa5972e9882`
- **参数名**: `vBaseEnvSpiClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Spi driver peripheral clock.

##### 3. vBaseEnvAdditionalParameters

**容器属性**:

- **UUID**: `b8e6419f-522a-4258-8358-22c51c77e4a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvAdditionalParameters`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Additional parameters for generation of additional defines, if necessary for the depending platform.

###### 参数配置

此容器包含 **10** 个参数：

####### BOOLEAN 类型参数

######## 1. vBaseEnvPowerDownModes

- **UUID**: `898a7dfa-a750-4879-a587-22cabff2b55d`
- **参数名**: `vBaseEnvPowerDownModes`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure, if Power Down Modes to be used for your derivative

####### STRING 类型参数

######## 1. vBaseEnvDerivativeGroup

- **UUID**: `2baac809-cdc2-447d-9f20-a18beb8d886d`
- **参数名**: `vBaseEnvDerivativeGroup`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define the Derivative Group of this derivative

####### ENUMERATION 类型参数

######## 1. vBaseEnvPllGroup

- **UUID**: `67f97e88-2817-4d79-9876-bbc3026774c0`
- **参数名**: `vBaseEnvPllGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `A5` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `D1` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `E1` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the PLL Group of your derivative

######## 2. vBaseEnvClockGroup

- **UUID**: `64e82637-3452-4005-833e-ec2c010b3866`
- **参数名**: `vBaseEnvClockGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Clock Group of your derivative

######## 3. vBaseEnvPortGroup

- **UUID**: `e9fa5662-e278-4ce0-a764-9145857ecddb`
- **参数名**: `vBaseEnvPortGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `B1` (来源: Vector Informatik)
  - `B2` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Port Group of your derivative

######## 4. vBaseEnvProtectionGroup

- **UUID**: `ee45913a-dd7e-46ba-a6e6-2cdc2aa9d5ea`
- **参数名**: `vBaseEnvProtectionGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
  - `NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Protection Group of your derivative

######## 5. vBaseEnvResetGroup

- **UUID**: `4e273998-de1f-4220-b71a-3434a80b031a`
- **参数名**: `vBaseEnvResetGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
  - `G` (来源: Vector Informatik)
  - `H` (来源: Vector Informatik)
  - `I` (来源: Vector Informatik)
  - `J` (来源: Vector Informatik)
  - `K` (来源: Vector Informatik)
  - `L` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Reset Group of your derivative

######## 6. vBaseEnvWatchdogGroup

- **UUID**: `b8ee0017-d3f4-4f99-b7f5-9125c02ac2ee`
- **参数名**: `vBaseEnvWatchdogGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `A3` (来源: Vector Informatik)
  - `A4` (来源: Vector Informatik)
  - `A5` (来源: Vector Informatik)
  - `A6` (来源: Vector Informatik)
  - `A7` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Watchdog Group of your derivative

######## 7. vBaseEnvOpModeGroup

- **UUID**: `fe20961e-dd08-42da-852d-984a16b8f502`
- **参数名**: `vBaseEnvOpModeGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the Operation Mode Group of your derivative

######## 8. vBaseEnvUserModeAccessGroup

- **UUID**: `6b314d2d-7838-4204-a9ed-acdcd694018c`
- **参数名**: `vBaseEnvUserModeAccessGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `A` (来源: Vector Informatik)
  - `A1` (来源: Vector Informatik)
  - `A2` (来源: Vector Informatik)
  - `B` (来源: Vector Informatik)
  - `C` (来源: Vector Informatik)
  - `D` (来源: Vector Informatik)
  - `E` (来源: Vector Informatik)
  - `F` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the User Mode Access Group of your derivative

##### 4. vBaseEnvMemLayoutHwRegion

**容器属性**:

- **UUID**: `67914085-ee03-4fe5-9d01-5ff933738178`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvMemLayoutHwRegion`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to structure the configuration parameters of hardware memory regions.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvHwRegionStartAddress

- **UUID**: `0cc34936-30b0-4113-8e8b-12ce777c4a07`
- **参数名**: `vBaseEnvHwRegionStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of the hardware memory region.

######## 2. vBaseEnvHwRegionSize

- **UUID**: `d56f3651-1f2a-4460-ad87-a74f34e6c2ae`
- **参数名**: `vBaseEnvHwRegionSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the hardware memory region.

######## 3. vBaseEnvHwRegionEccAlignment

- **UUID**: `8a3ee4a1-ae6b-4124-a67f-b669ac35fc9d`
- **参数名**: `vBaseEnvHwRegionEccAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Required ECC Alignment of the hardware memory region.

####### ENUMERATION 类型参数

######## 1. vBaseEnvHwRegionType

- **UUID**: `eec4f426-5c61-4f4e-bb84-9b79a5fd74d6`
- **参数名**: `vBaseEnvHwRegionType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RAM` (来源: Vector Informatik)
  - `ROM` (来源: Vector Informatik)
  - `NVRAM` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of the hardware memory region.
This parameter is necessary for some linkers (e.g. Tasking), to distinguish between RAM/ROM/NVRAM.

##### 5. vBaseEnvClockSettings

**容器属性**:

- **UUID**: `95c6c99c-78c7-405a-8641-69e062c29cf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvClockSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for derivative specific default clock settings (oscillator + peripherals).
This allows solving actions to update the depending frequncy settings in the vBRSHwConfig container.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvOscClock

- **UUID**: `bad86329-f64d-46ce-87c0-0beedbb27820`
- **参数名**: `vBaseEnvOscClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of the board specific external oscillator.

######## 2. vBaseEnvTimebaseClock

- **UUID**: `63919a76-214f-4231-8fbb-d197ccbd76f6`
- **参数名**: `vBaseEnvTimebaseClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation (normally used as CPU core clock).

######## 3. vBaseEnvPeriphClock

- **UUID**: `2211f913-7211-4a2a-ad6f-7b183e303ead`
- **参数名**: `vBaseEnvPeriphClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of the controller peripherals, at least for the default timer, used by the OS.
If the frequencies for communication peripherals differ from this peripheral clock, they could be configured through the depending communictaion peripheral clock parameter.

######## 4. vBaseEnvCanClock

- **UUID**: `237fe032-59c4-4f1b-9435-13cfcce46ef4`
- **参数名**: `vBaseEnvCanClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of CAN driver peripheral clock.

######## 5. vBaseEnvLinClock

- **UUID**: `77a40253-8044-475e-b72b-91f1f103b571`
- **参数名**: `vBaseEnvLinClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of LIN driver peripheral clock.

######## 6. vBaseEnvFlexrayClock

- **UUID**: `9c723370-7286-4a2a-af3d-0a22a1c24f82`
- **参数名**: `vBaseEnvFlexrayClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of FlexRay driver peripheral clock.

######## 7. vBaseEnvEthernetClock

- **UUID**: `e30ab088-36c9-4df1-a52d-95c0b8cb285d`
- **参数名**: `vBaseEnvEthernetClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of EtherNet driver peripheral clock.

######## 8. vBaseEnvHyperbusClock

- **UUID**: `43f04887-b69b-4946-b254-c6aa14b43873`
- **参数名**: `vBaseEnvHyperbusClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Hyperbus driver peripheral clock.

######## 9. vBaseEnvI2cClock

- **UUID**: `dbe1d32a-047f-4168-9415-f66bad94a402`
- **参数名**: `vBaseEnvI2cClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of I2C driver peripheral clock.

######## 10. vBaseEnvSpiClock

- **UUID**: `76a75dd0-f430-4714-92cf-1aa5972e9882`
- **参数名**: `vBaseEnvSpiClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Spi driver peripheral clock.

##### 6. vBaseEnvMemLayoutHwRegion

**容器属性**:

- **UUID**: `517ff7b1-ca16-4b22-a1b7-b27a2390d92f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvMemLayoutHwRegion`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to structure the configuration parameters of hardware memory regions.

##### 7. vBaseEnvInterruptHandling

**容器属性**:

- **UUID**: `5a6bc7a8-95e1-4d35-92d8-dad872b4fbb9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvInterruptHandling`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for family specific default interrupt settings

###### 配置容器

本模块包含 **14** 个配置容器：

####### 1. vBaseEnvCan

**容器属性**:

- **UUID**: `451fe3fa-d259-4663-a518-f2e044f67d6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `a70aa265-a413-4e33-99fe-35bed058efe2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `4e5452f7-0e33-4db7-b278-4fb5f1c59342`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `17a6698c-215e-4022-b971-660f61448c1c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `ebd4214c-557c-461b-bf67-0820ecd0b5cd`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 2. vBaseEnvChannel

**容器属性**:

- **UUID**: `a70aa265-a413-4e33-99fe-35bed058efe2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `4e5452f7-0e33-4db7-b278-4fb5f1c59342`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `17a6698c-215e-4022-b971-660f61448c1c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `ebd4214c-557c-461b-bf67-0820ecd0b5cd`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 3. vBaseEnvLin

**容器属性**:

- **UUID**: `94d8f1fc-3c8a-4ad3-9d92-5471c72d5c94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `4a2f382c-fa69-4fe0-a745-f3a704e24e47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `9b3119d3-8c12-42e1-bd43-2cf8740ebeb7`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `429ada8b-93b4-44a2-8ec1-abc82c33232d`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `42c64964-38e2-4691-9d12-85d6e3629020`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 4. vBaseEnvChannel

**容器属性**:

- **UUID**: `4a2f382c-fa69-4fe0-a745-f3a704e24e47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `9b3119d3-8c12-42e1-bd43-2cf8740ebeb7`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `429ada8b-93b4-44a2-8ec1-abc82c33232d`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `42c64964-38e2-4691-9d12-85d6e3629020`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 5. vBaseEnvFlexray

**容器属性**:

- **UUID**: `2cbfd57a-cd96-4313-a0ae-94222b331d0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `131db306-7656-44d5-9b3f-372d16387b0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `dd35061c-b1c2-4e96-b859-7df07977b418`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `04db9a0b-ca5c-4fb4-a60d-594f6216392c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `aa8c240b-9427-4e23-a9d3-8473baaa965c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 6. vBaseEnvChannel

**容器属性**:

- **UUID**: `131db306-7656-44d5-9b3f-372d16387b0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `dd35061c-b1c2-4e96-b859-7df07977b418`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `04db9a0b-ca5c-4fb4-a60d-594f6216392c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `aa8c240b-9427-4e23-a9d3-8473baaa965c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 7. vBaseEnvEthernet

**容器属性**:

- **UUID**: `2ab3b67f-9e27-4a21-b067-3c567df25b7d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `0911853b-f95e-48d9-a91e-a9813877ac7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `7286691d-d55b-43bd-ac98-6916e5655101`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `37357d8f-3ab6-46da-8ac8-b1f8ad8b40ff`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `45ccbe36-749c-49dd-97b2-f5691530bdc0`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 8. vBaseEnvChannel

**容器属性**:

- **UUID**: `0911853b-f95e-48d9-a91e-a9813877ac7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `7286691d-d55b-43bd-ac98-6916e5655101`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `37357d8f-3ab6-46da-8ac8-b1f8ad8b40ff`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `45ccbe36-749c-49dd-97b2-f5691530bdc0`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 9. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `c5dc0332-1f44-412c-8ed5-d9bc01da42cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `2fb8456a-0e80-4102-96db-d4d403e7f869`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `7246a15d-007c-409c-9255-b69796f1a9d4`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `09547154-1498-41e3-ab46-a3803f94600f`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `2ff27a30-a956-4d39-ad39-82d5421195b5`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 10. vBaseEnvChannel

**容器属性**:

- **UUID**: `2fb8456a-0e80-4102-96db-d4d403e7f869`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `7246a15d-007c-409c-9255-b69796f1a9d4`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `09547154-1498-41e3-ab46-a3803f94600f`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `2ff27a30-a956-4d39-ad39-82d5421195b5`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 11. vBaseEnvI2c

**容器属性**:

- **UUID**: `6a580f8d-1de8-4f9f-bfdf-eae2d53f6343`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `ed508309-983a-4e1b-9706-14df8f0bd9cb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `1c8e1683-f6bd-4da7-ae30-981dd20b5bf9`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `47ef3894-e0ab-4810-b1ff-761b8fad5bb7`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `bdc812e9-6aa7-44fc-8d70-80eb20290daf`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 12. vBaseEnvChannel

**容器属性**:

- **UUID**: `ed508309-983a-4e1b-9706-14df8f0bd9cb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `1c8e1683-f6bd-4da7-ae30-981dd20b5bf9`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `47ef3894-e0ab-4810-b1ff-761b8fad5bb7`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `bdc812e9-6aa7-44fc-8d70-80eb20290daf`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 13. vBaseEnvSpi

**容器属性**:

- **UUID**: `b782e61f-1eb0-4c68-ad36-27fc03273d2f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvSpi`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `59783252-d501-48a3-be38-53b4c22bc41c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `c421c56c-ea53-4550-81e8-f4d554b6fdc6`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

############ 2. vBaseEnvIsrInterruptPriority

- **UUID**: `b984cdf2-7f54-45b6-880a-0d838dd471b9`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

############ 3. vBaseEnvIsrInterruptSource

- **UUID**: `cc10d3c0-f508-4d4e-883d-78a71cf59450`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 14. vBaseEnvChannel

**容器属性**:

- **UUID**: `59783252-d501-48a3-be38-53b4c22bc41c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `c421c56c-ea53-4550-81e8-f4d554b6fdc6`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `b984cdf2-7f54-45b6-880a-0d838dd471b9`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `cc10d3c0-f508-4d4e-883d-78a71cf59450`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 8. vBaseEnvCan

**容器属性**:

- **UUID**: `451fe3fa-d259-4663-a518-f2e044f67d6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `a70aa265-a413-4e33-99fe-35bed058efe2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `4e5452f7-0e33-4db7-b278-4fb5f1c59342`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `17a6698c-215e-4022-b971-660f61448c1c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `ebd4214c-557c-461b-bf67-0820ecd0b5cd`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 9. vBaseEnvChannel

**容器属性**:

- **UUID**: `a70aa265-a413-4e33-99fe-35bed058efe2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `4e5452f7-0e33-4db7-b278-4fb5f1c59342`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

######## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `17a6698c-215e-4022-b971-660f61448c1c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 3. vBaseEnvIsrInterruptSource

- **UUID**: `ebd4214c-557c-461b-bf67-0820ecd0b5cd`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 10. vBaseEnvLin

**容器属性**:

- **UUID**: `94d8f1fc-3c8a-4ad3-9d92-5471c72d5c94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `4a2f382c-fa69-4fe0-a745-f3a704e24e47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `9b3119d3-8c12-42e1-bd43-2cf8740ebeb7`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `429ada8b-93b4-44a2-8ec1-abc82c33232d`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `42c64964-38e2-4691-9d12-85d6e3629020`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 11. vBaseEnvChannel

**容器属性**:

- **UUID**: `4a2f382c-fa69-4fe0-a745-f3a704e24e47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `9b3119d3-8c12-42e1-bd43-2cf8740ebeb7`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

######## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `429ada8b-93b4-44a2-8ec1-abc82c33232d`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 3. vBaseEnvIsrInterruptSource

- **UUID**: `42c64964-38e2-4691-9d12-85d6e3629020`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 12. vBaseEnvFlexray

**容器属性**:

- **UUID**: `2cbfd57a-cd96-4313-a0ae-94222b331d0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `131db306-7656-44d5-9b3f-372d16387b0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `dd35061c-b1c2-4e96-b859-7df07977b418`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `04db9a0b-ca5c-4fb4-a60d-594f6216392c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `aa8c240b-9427-4e23-a9d3-8473baaa965c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 13. vBaseEnvChannel

**容器属性**:

- **UUID**: `131db306-7656-44d5-9b3f-372d16387b0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `dd35061c-b1c2-4e96-b859-7df07977b418`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

######## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `04db9a0b-ca5c-4fb4-a60d-594f6216392c`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 3. vBaseEnvIsrInterruptSource

- **UUID**: `aa8c240b-9427-4e23-a9d3-8473baaa965c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 14. vBaseEnvEthernet

**容器属性**:

- **UUID**: `2ab3b67f-9e27-4a21-b067-3c567df25b7d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `0911853b-f95e-48d9-a91e-a9813877ac7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `7286691d-d55b-43bd-ac98-6916e5655101`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `37357d8f-3ab6-46da-8ac8-b1f8ad8b40ff`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `45ccbe36-749c-49dd-97b2-f5691530bdc0`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 15. vBaseEnvChannel

**容器属性**:

- **UUID**: `0911853b-f95e-48d9-a91e-a9813877ac7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `7286691d-d55b-43bd-ac98-6916e5655101`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

######## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `37357d8f-3ab6-46da-8ac8-b1f8ad8b40ff`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 3. vBaseEnvIsrInterruptSource

- **UUID**: `45ccbe36-749c-49dd-97b2-f5691530bdc0`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 16. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `c5dc0332-1f44-412c-8ed5-d9bc01da42cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `2fb8456a-0e80-4102-96db-d4d403e7f869`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `7246a15d-007c-409c-9255-b69796f1a9d4`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `09547154-1498-41e3-ab46-a3803f94600f`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `2ff27a30-a956-4d39-ad39-82d5421195b5`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 17. vBaseEnvChannel

**容器属性**:

- **UUID**: `2fb8456a-0e80-4102-96db-d4d403e7f869`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `7246a15d-007c-409c-9255-b69796f1a9d4`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

######## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `09547154-1498-41e3-ab46-a3803f94600f`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 3. vBaseEnvIsrInterruptSource

- **UUID**: `2ff27a30-a956-4d39-ad39-82d5421195b5`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 18. vBaseEnvI2c

**容器属性**:

- **UUID**: `6a580f8d-1de8-4f9f-bfdf-eae2d53f6343`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `ed508309-983a-4e1b-9706-14df8f0bd9cb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `1c8e1683-f6bd-4da7-ae30-981dd20b5bf9`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `47ef3894-e0ab-4810-b1ff-761b8fad5bb7`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `bdc812e9-6aa7-44fc-8d70-80eb20290daf`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 19. vBaseEnvChannel

**容器属性**:

- **UUID**: `ed508309-983a-4e1b-9706-14df8f0bd9cb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `1c8e1683-f6bd-4da7-ae30-981dd20b5bf9`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

######## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `47ef3894-e0ab-4810-b1ff-761b8fad5bb7`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 3. vBaseEnvIsrInterruptSource

- **UUID**: `bdc812e9-6aa7-44fc-8d70-80eb20290daf`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 20. vBaseEnvSpi

**容器属性**:

- **UUID**: `b782e61f-1eb0-4c68-ad36-27fc03273d2f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvSpi`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `59783252-d501-48a3-be38-53b4c22bc41c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `c421c56c-ea53-4550-81e8-f4d554b6fdc6`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

########## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `b984cdf2-7f54-45b6-880a-0d838dd471b9`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 3. vBaseEnvIsrInterruptSource

- **UUID**: `cc10d3c0-f508-4d4e-883d-78a71cf59450`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 21. vBaseEnvChannel

**容器属性**:

- **UUID**: `59783252-d501-48a3-be38-53b4c22bc41c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `c421c56c-ea53-4550-81e8-f4d554b6fdc6`
- **参数名**: `vBaseEnvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical channel

######## 2. vBaseEnvIsrInterruptPriority

- **UUID**: `b984cdf2-7f54-45b6-880a-0d838dd471b9`
- **参数名**: `vBaseEnvIsrInterruptPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 3. vBaseEnvIsrInterruptSource

- **UUID**: `cc10d3c0-f508-4d4e-883d-78a71cf59450`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 22. vBaseEnvPeripheralClocks

**容器属性**:

- **UUID**: `7204be40-e226-4fc8-94b2-99b2d31b0bb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvPeripheralClocks`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for family specific default peripheral clock settings

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. vBaseEnvCan

**容器属性**:

- **UUID**: `16953022-2882-44de-85d9-fbd534995dc3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvCan_Clock

- **UUID**: `38bbe5a7-4c50-44b3-800d-38ad05f8a427`
- **参数名**: `vBaseEnvCan_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of CAN driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvCan_ClockRef

- **UUID**: `10005c4d-597e-4c80-9d0c-1846315834b4`
- **引用名**: `vBaseEnvCan_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for CAN peripheral clock setting.

####### 2. vBaseEnvLin

**容器属性**:

- **UUID**: `1d9b0444-3a94-480f-b1b7-5bab6c833512`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvLin_Clock

- **UUID**: `d15e8388-e8b0-44d9-ad17-53b089102b7f`
- **参数名**: `vBaseEnvLin_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of LIN driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvLin_ClockRef

- **UUID**: `103738af-fdb0-4141-9970-175cedb0ebfb`
- **引用名**: `vBaseEnvLin_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for LIN peripheral clock setting.

####### 3. vBaseEnvFlexray

**容器属性**:

- **UUID**: `12e6ef72-a1c3-4d36-bf1d-9903fd1a64af`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvFlexray_Clock

- **UUID**: `8b4dd0b8-0945-4e8d-aa9c-b556b848e984`
- **参数名**: `vBaseEnvFlexray_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of FlexRay driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvFlexray_ClockRef

- **UUID**: `fd657ce0-7a1b-4617-8b91-820a466b6bb8`
- **引用名**: `vBaseEnvFlexray_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for FlexRay peripheral clock setting.

####### 4. vBaseEnvEthernet

**容器属性**:

- **UUID**: `3148881d-91b4-4386-9179-8037d07bb898`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvEthernet_Clock

- **UUID**: `0cbbf93a-e102-44fd-900d-cdbcd8932216`
- **参数名**: `vBaseEnvEthernet_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of EtherNet driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvEthernet_ClockRef

- **UUID**: `4ef49ae5-a390-4cb9-846e-48d8bb6ca0e4`
- **引用名**: `vBaseEnvEthernet_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for EtherNet peripheral clock setting.

####### 5. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `faea3e8d-9bab-41a6-b927-dfcfabf24027`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvHyperbus_Clock

- **UUID**: `e06337e0-e742-4bab-9b58-c72593eaab14`
- **参数名**: `vBaseEnvHyperbus_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Hyperbus driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvHyperbus_ClockRef

- **UUID**: `1d1c4c36-88e7-48cc-818c-f54c09ac2794`
- **引用名**: `vBaseEnvHyperbus_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for Hyperbus peripheral clock setting.

####### 6. vBaseEnvI2c

**容器属性**:

- **UUID**: `0d793117-aebb-4feb-bb64-e2709fd141df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvI2c_Clock

- **UUID**: `af7760ab-61bd-4909-803f-925f4f6638fc`
- **参数名**: `vBaseEnvI2c_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of I2C driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvI2c_ClockRef

- **UUID**: `8dace219-3411-43eb-8b71-7c3bf113b69c`
- **引用名**: `vBaseEnvI2c_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for I2C peripheral clock setting.

####### 7. vBaseEnvSpi

**容器属性**:

- **UUID**: `65914f10-55c6-4bda-9e8b-65652bee9ad2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvSpi`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvSpi_Clock

- **UUID**: `9201db51-51b8-4182-8fee-cc748a160225`
- **参数名**: `vBaseEnvSpi_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Spi driver peripheral clock.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBaseEnvSpi_ClockRef

- **UUID**: `f974d0a7-959d-4a28-9ae4-12ed2f1287e8`
- **引用名**: `vBaseEnvSpi_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for Spi peripheral clock setting.

##### 23. vBaseEnvCan

**容器属性**:

- **UUID**: `16953022-2882-44de-85d9-fbd534995dc3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvCan_Clock

- **UUID**: `38bbe5a7-4c50-44b3-800d-38ad05f8a427`
- **参数名**: `vBaseEnvCan_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of CAN driver peripheral clock.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBaseEnvCan_ClockRef

- **UUID**: `10005c4d-597e-4c80-9d0c-1846315834b4`
- **引用名**: `vBaseEnvCan_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for CAN peripheral clock setting.

##### 24. vBaseEnvLin

**容器属性**:

- **UUID**: `1d9b0444-3a94-480f-b1b7-5bab6c833512`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvLin_Clock

- **UUID**: `d15e8388-e8b0-44d9-ad17-53b089102b7f`
- **参数名**: `vBaseEnvLin_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of LIN driver peripheral clock.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBaseEnvLin_ClockRef

- **UUID**: `103738af-fdb0-4141-9970-175cedb0ebfb`
- **引用名**: `vBaseEnvLin_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for LIN peripheral clock setting.

##### 25. vBaseEnvFlexray

**容器属性**:

- **UUID**: `12e6ef72-a1c3-4d36-bf1d-9903fd1a64af`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvFlexray_Clock

- **UUID**: `8b4dd0b8-0945-4e8d-aa9c-b556b848e984`
- **参数名**: `vBaseEnvFlexray_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of FlexRay driver peripheral clock.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBaseEnvFlexray_ClockRef

- **UUID**: `fd657ce0-7a1b-4617-8b91-820a466b6bb8`
- **引用名**: `vBaseEnvFlexray_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for FlexRay peripheral clock setting.

##### 26. vBaseEnvEthernet

**容器属性**:

- **UUID**: `3148881d-91b4-4386-9179-8037d07bb898`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvEthernet_Clock

- **UUID**: `0cbbf93a-e102-44fd-900d-cdbcd8932216`
- **参数名**: `vBaseEnvEthernet_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of EtherNet driver peripheral clock.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBaseEnvEthernet_ClockRef

- **UUID**: `4ef49ae5-a390-4cb9-846e-48d8bb6ca0e4`
- **引用名**: `vBaseEnvEthernet_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for EtherNet peripheral clock setting.

##### 27. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `faea3e8d-9bab-41a6-b927-dfcfabf24027`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvHyperbus_Clock

- **UUID**: `e06337e0-e742-4bab-9b58-c72593eaab14`
- **参数名**: `vBaseEnvHyperbus_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Hyperbus driver peripheral clock.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBaseEnvHyperbus_ClockRef

- **UUID**: `1d1c4c36-88e7-48cc-818c-f54c09ac2794`
- **引用名**: `vBaseEnvHyperbus_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for Hyperbus peripheral clock setting.

##### 28. vBaseEnvI2c

**容器属性**:

- **UUID**: `0d793117-aebb-4feb-bb64-e2709fd141df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvI2c_Clock

- **UUID**: `af7760ab-61bd-4909-803f-925f4f6638fc`
- **参数名**: `vBaseEnvI2c_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of I2C driver peripheral clock.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBaseEnvI2c_ClockRef

- **UUID**: `8dace219-3411-43eb-8b71-7c3bf113b69c`
- **引用名**: `vBaseEnvI2c_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for I2C peripheral clock setting.

##### 29. vBaseEnvSpi

**容器属性**:

- **UUID**: `65914f10-55c6-4bda-9e8b-65652bee9ad2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvSpi`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvSpi_Clock

- **UUID**: `9201db51-51b8-4182-8fee-cc748a160225`
- **参数名**: `vBaseEnvSpi_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default frequency, used for PLL calculation of Spi driver peripheral clock.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBaseEnvSpi_ClockRef

- **UUID**: `f974d0a7-959d-4a28-9ae4-12ed2f1287e8`
- **引用名**: `vBaseEnvSpi_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default McuClockReferencePoint reference for Spi peripheral clock setting.

##### 30. vBaseEnvStartupStackSettings

**容器属性**:

- **UUID**: `cf544d9c-fdb5-43a0-ae4e-038350216485`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvStartupStackSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for family specific startup stack settings, if they differ to the default settings

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvStackAlignment

- **UUID**: `35ed3050-d006-4f69-be9e-ba979c6043e5`
- **参数名**: `vBaseEnvStackAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the startup stack alignment for each core.
This value will be validated in the vLinkGen stack section.
This value is only needed, if the default value 4 is not sufficient for this platform.

######## 2. vBaseEnvStackEndAlignment

- **UUID**: `365e6fed-142c-4e72-bd85-63e5df913928`
- **参数名**: `vBaseEnvStackEndAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the startup stack end alignment for each core.
This value will be validated in the vLinkGen stack section.
This value is only needed, if the default value 4 is not sufficient for this platform.

######## 3. vBaseEnvStackSize

- **UUID**: `56a730b2-0aa5-45c4-8d3d-17f32e4d2ab5`
- **参数名**: `vBaseEnvStackSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1024`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the startup stack size for each core.
This value will be validated in the vLinkGen stack section and generated into vBrs_Lcfg.c as StartupStackSize.
This value is only needed, if the default value 1024 is not sufficient for this platform.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 2

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **vBaseEnv_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **vBaseEnv**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vBaseEnv_Impl

- **UUID**: `01566413-2fa2-4b8d-96ab-d43849a358e2`
- **实现名称**: `vBaseEnv_Impl`
- **编程语言**: C
- **软件版本**: 1.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator
