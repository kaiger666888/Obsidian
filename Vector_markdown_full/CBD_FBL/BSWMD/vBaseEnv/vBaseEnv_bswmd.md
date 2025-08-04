# vBaseEnv - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:25

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

- **UUID**: `520e746e-c7dd-4c58-99b7-ae3ab1339329`
- **模块名称**: `vBaseEnv`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the hardware.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 0.01.00

- **状态**: prototype
- **发布日期**: 2018-06-11
- **发布者**: vibwa

**变更内容**:

#### 配置容器

本模块包含 **25** 个配置容器：

##### 1. vBaseEnvGeneral

**容器属性**:

- **UUID**: `36bfbe61-fa45-4418-bdca-b4c641dda822`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBaseEnvTestedDerivativeRef

- **UUID**: `678b7739-4321-422f-a313-73754e9173f0`
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

本模块包含 **24** 个配置容器：

####### 1. vBaseEnvDerivativeInformation

**容器属性**:

- **UUID**: `b536cccb-fdc6-4f64-8db7-aeecbc0f583a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvDerivativeInformation`
- **多重性**: [1..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **13** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvCpuMaxFrequency

- **UUID**: `6372fa95-80fa-4154-b7e5-084796197335`
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

- **UUID**: `fed537f9-924e-42a0-a567-a626a5e40ba8`
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

- **UUID**: `aba5d6ca-abb3-4a10-b94a-83fa5411142e`
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

- **UUID**: `6e4e0fbb-ddde-4f30-901a-3ab09d7b79b9`
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

- **UUID**: `bcb37216-aa4c-4f98-a6d6-c09520446dc6`
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

- **UUID**: `040cbea7-7c2a-49ff-9a0a-b5fb3efd695e`
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

- **UUID**: `74d97346-1f4f-4847-b505-2ce151f94bb0`
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

- **UUID**: `9b1e6c72-d053-4386-bb68-f916ba28a320`
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

- **UUID**: `e7940b06-a8e3-47bc-a8d3-7432afdc521b`
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

######### STRING 类型参数

########## 1. vBaseEnvTestedDerivative

- **UUID**: `9aaccae4-85a2-442b-9db8-d199be13222b`
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

- **UUID**: `872bdfe9-aa6e-4c16-8118-f5ac2e38049b`
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

- **UUID**: `b5ce5f95-13d9-4a28-bdbf-eabf865db7a2`
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

- **UUID**: `ab16d57a-9dbb-411f-abd4-88bb83615862`
- **参数名**: `vBaseEnvCpuCore`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `OTHER` (来源: Vector Informatik)
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the core architecture of this derivative.
This value will be generated into vBrsCfg.h as
BRS_CPU_CORE_x

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. vBaseEnvAdditionalParameters

**容器属性**:

- **UUID**: `c1d9a404-967f-4991-8e85-05437d9f95bb`
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

- **UUID**: `2a0798ad-dc7d-4bb8-a2cc-434472cb9a5f`
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

- **UUID**: `6c60aa3b-1a48-44fd-8857-65a330434c15`
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

- **UUID**: `0164165d-f469-4f9d-bcfc-261ed161887c`
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
- **描述**: Configure the PLL Group of your derivative

############ 2. vBaseEnvClockGroup

- **UUID**: `1811e373-7a78-4632-ac63-0a783fb2787b`
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

- **UUID**: `eb9f584f-a9a0-43dd-9900-c23d78fdee2f`
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

- **UUID**: `1347312d-6baa-47f7-ac4c-784ea44a2d18`
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

- **UUID**: `9c44d3e1-c3f2-490e-aeab-53cddc52a177`
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

- **UUID**: `9a1276d0-3181-4055-8246-e683819e682c`
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

- **UUID**: `1d5f9ab1-9c27-47a8-bd2f-f7ad39088322`
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

- **UUID**: `24f6d986-eaa7-433c-9ff1-a6ae43d00db0`
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

- **UUID**: `eb21f87b-b6ec-4719-a9c7-dacdbb6b6869`
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

- **UUID**: `6ee5851b-58f9-41d2-8cd6-e11e83d8f9d8`
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

- **UUID**: `fe991146-26ad-46e2-a7ff-194d880bb1a7`
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

- **UUID**: `68a0a334-2d79-45af-974c-200097b63d67`
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

- **UUID**: `169fdfa6-1e71-4f05-acbf-82e7e750d49c`
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

####### 2. vBaseEnvAdditionalParameters

**容器属性**:

- **UUID**: `c1d9a404-967f-4991-8e85-05437d9f95bb`
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

- **UUID**: `2a0798ad-dc7d-4bb8-a2cc-434472cb9a5f`
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

- **UUID**: `6c60aa3b-1a48-44fd-8857-65a330434c15`
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

- **UUID**: `0164165d-f469-4f9d-bcfc-261ed161887c`
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
- **描述**: Configure the PLL Group of your derivative

########## 2. vBaseEnvClockGroup

- **UUID**: `1811e373-7a78-4632-ac63-0a783fb2787b`
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

- **UUID**: `eb9f584f-a9a0-43dd-9900-c23d78fdee2f`
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

- **UUID**: `1347312d-6baa-47f7-ac4c-784ea44a2d18`
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

- **UUID**: `9c44d3e1-c3f2-490e-aeab-53cddc52a177`
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

- **UUID**: `9a1276d0-3181-4055-8246-e683819e682c`
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

- **UUID**: `1d5f9ab1-9c27-47a8-bd2f-f7ad39088322`
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

- **UUID**: `24f6d986-eaa7-433c-9ff1-a6ae43d00db0`
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

- **UUID**: `eb21f87b-b6ec-4719-a9c7-dacdbb6b6869`
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

- **UUID**: `6ee5851b-58f9-41d2-8cd6-e11e83d8f9d8`
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

- **UUID**: `fe991146-26ad-46e2-a7ff-194d880bb1a7`
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

- **UUID**: `68a0a334-2d79-45af-974c-200097b63d67`
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

- **UUID**: `169fdfa6-1e71-4f05-acbf-82e7e750d49c`
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

####### 4. vBaseEnvMemLayoutHwRegion

**容器属性**:

- **UUID**: `dbd5200f-9bee-4b1e-83a0-2bb210fb0c80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvMemLayoutHwRegion`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to structure the configuration parameters of hardware memory regions.

####### 5. vBaseEnvInterruptHandling

**容器属性**:

- **UUID**: `0d46b873-5159-4f4b-9d41-add34afa2bf2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvInterruptHandling`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for family specific default interrupt settings

######## 配置容器

本模块包含 **12** 个配置容器：

######### 1. vBaseEnvCan

**容器属性**:

- **UUID**: `2a686f3f-d5a9-44ef-8b92-df2bf6ab3f74`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `c8b6dde1-038d-4a9f-b5eb-06adb9f57893`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `b4cadab5-977a-42d8-9159-fc70350faa9b`
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

- **UUID**: `1191b17c-c217-4973-80f3-ef2f7afebde0`
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

- **UUID**: `c2b23bb8-b802-4570-92f9-2f42a21dbfc3`
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

- **UUID**: `c8b6dde1-038d-4a9f-b5eb-06adb9f57893`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `b4cadab5-977a-42d8-9159-fc70350faa9b`
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

- **UUID**: `1191b17c-c217-4973-80f3-ef2f7afebde0`
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

- **UUID**: `c2b23bb8-b802-4570-92f9-2f42a21dbfc3`
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

- **UUID**: `7025aa7c-8ce8-45c6-9400-109bb77ae077`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `183ca6d5-5afc-43cf-af42-af7c53359920`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `c729ed6b-6ff0-43a3-90e0-8e6d85e70a7f`
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

- **UUID**: `003d33d5-2e10-4e3e-8640-2b50b1d858a5`
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

- **UUID**: `49fed7c0-d9bd-40db-8e1f-63a07abf01ed`
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

- **UUID**: `183ca6d5-5afc-43cf-af42-af7c53359920`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `c729ed6b-6ff0-43a3-90e0-8e6d85e70a7f`
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

- **UUID**: `003d33d5-2e10-4e3e-8640-2b50b1d858a5`
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

- **UUID**: `49fed7c0-d9bd-40db-8e1f-63a07abf01ed`
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

- **UUID**: `ba8359a0-6cf7-4521-b992-aac66c3bfab3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `4c8dcfc3-8998-4a2a-aa56-465b29e0b7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `da9f0fcf-e04c-45e2-bb36-7f08b6fd8139`
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

- **UUID**: `3f6e3105-803f-48d2-8b44-816f649ebffa`
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

- **UUID**: `cff7d8b3-b257-47c0-812e-e29b2169fc1f`
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

- **UUID**: `4c8dcfc3-8998-4a2a-aa56-465b29e0b7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `da9f0fcf-e04c-45e2-bb36-7f08b6fd8139`
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

- **UUID**: `3f6e3105-803f-48d2-8b44-816f649ebffa`
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

- **UUID**: `cff7d8b3-b257-47c0-812e-e29b2169fc1f`
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

- **UUID**: `f434df43-e5c7-47ef-a078-cbf24e74b231`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `d6b26782-a8dd-411f-9e86-0ae11e9a7fdf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `b3b68af2-3737-4999-8a84-d64230b0cde2`
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

- **UUID**: `b20c3af5-f4ef-4ce1-b07c-1fc5029d27d4`
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

- **UUID**: `5c48491f-fae8-4cfc-8d6d-69ab11a4962a`
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

- **UUID**: `d6b26782-a8dd-411f-9e86-0ae11e9a7fdf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `b3b68af2-3737-4999-8a84-d64230b0cde2`
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

- **UUID**: `b20c3af5-f4ef-4ce1-b07c-1fc5029d27d4`
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

- **UUID**: `5c48491f-fae8-4cfc-8d6d-69ab11a4962a`
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

- **UUID**: `15acb0fb-a614-4773-bbac-f1704adfc710`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `a35c95d1-e74e-46ab-90e2-eb6c69f681cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `0b7545f3-f8f3-4402-931d-9d81adedbbe5`
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

- **UUID**: `e20cb4fb-bdfb-4a29-aa54-ff6d82d57002`
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

- **UUID**: `f1fa0989-8360-40fe-8b9b-80c9a728e41c`
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

- **UUID**: `a35c95d1-e74e-46ab-90e2-eb6c69f681cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `0b7545f3-f8f3-4402-931d-9d81adedbbe5`
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

- **UUID**: `e20cb4fb-bdfb-4a29-aa54-ff6d82d57002`
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

- **UUID**: `f1fa0989-8360-40fe-8b9b-80c9a728e41c`
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

- **UUID**: `6a974cd3-a220-45c0-bba1-f656f8d4c738`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `b191c6d6-2270-45a7-8480-ea3e7f0e779b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vBaseEnvIndex

- **UUID**: `3882eb08-2cda-4519-a830-41e62533ec3f`
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

- **UUID**: `5de14007-0210-427d-a27f-f0ebf3c69f1d`
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

- **UUID**: `70d74e24-f320-4cc0-a157-6820f9c1e43b`
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

- **UUID**: `b191c6d6-2270-45a7-8480-ea3e7f0e779b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `3882eb08-2cda-4519-a830-41e62533ec3f`
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

- **UUID**: `5de14007-0210-427d-a27f-f0ebf3c69f1d`
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

- **UUID**: `70d74e24-f320-4cc0-a157-6820f9c1e43b`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 6. vBaseEnvCan

**容器属性**:

- **UUID**: `2a686f3f-d5a9-44ef-8b92-df2bf6ab3f74`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `c8b6dde1-038d-4a9f-b5eb-06adb9f57893`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `b4cadab5-977a-42d8-9159-fc70350faa9b`
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

- **UUID**: `1191b17c-c217-4973-80f3-ef2f7afebde0`
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

- **UUID**: `c2b23bb8-b802-4570-92f9-2f42a21dbfc3`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 7. vBaseEnvChannel

**容器属性**:

- **UUID**: `c8b6dde1-038d-4a9f-b5eb-06adb9f57893`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `b4cadab5-977a-42d8-9159-fc70350faa9b`
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

- **UUID**: `1191b17c-c217-4973-80f3-ef2f7afebde0`
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

- **UUID**: `c2b23bb8-b802-4570-92f9-2f42a21dbfc3`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 8. vBaseEnvLin

**容器属性**:

- **UUID**: `7025aa7c-8ce8-45c6-9400-109bb77ae077`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `183ca6d5-5afc-43cf-af42-af7c53359920`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `c729ed6b-6ff0-43a3-90e0-8e6d85e70a7f`
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

- **UUID**: `003d33d5-2e10-4e3e-8640-2b50b1d858a5`
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

- **UUID**: `49fed7c0-d9bd-40db-8e1f-63a07abf01ed`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 9. vBaseEnvChannel

**容器属性**:

- **UUID**: `183ca6d5-5afc-43cf-af42-af7c53359920`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `c729ed6b-6ff0-43a3-90e0-8e6d85e70a7f`
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

- **UUID**: `003d33d5-2e10-4e3e-8640-2b50b1d858a5`
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

- **UUID**: `49fed7c0-d9bd-40db-8e1f-63a07abf01ed`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 10. vBaseEnvFlexray

**容器属性**:

- **UUID**: `ba8359a0-6cf7-4521-b992-aac66c3bfab3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `4c8dcfc3-8998-4a2a-aa56-465b29e0b7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `da9f0fcf-e04c-45e2-bb36-7f08b6fd8139`
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

- **UUID**: `3f6e3105-803f-48d2-8b44-816f649ebffa`
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

- **UUID**: `cff7d8b3-b257-47c0-812e-e29b2169fc1f`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 11. vBaseEnvChannel

**容器属性**:

- **UUID**: `4c8dcfc3-8998-4a2a-aa56-465b29e0b7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `da9f0fcf-e04c-45e2-bb36-7f08b6fd8139`
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

- **UUID**: `3f6e3105-803f-48d2-8b44-816f649ebffa`
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

- **UUID**: `cff7d8b3-b257-47c0-812e-e29b2169fc1f`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 12. vBaseEnvEthernet

**容器属性**:

- **UUID**: `f434df43-e5c7-47ef-a078-cbf24e74b231`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `d6b26782-a8dd-411f-9e86-0ae11e9a7fdf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `b3b68af2-3737-4999-8a84-d64230b0cde2`
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

- **UUID**: `b20c3af5-f4ef-4ce1-b07c-1fc5029d27d4`
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

- **UUID**: `5c48491f-fae8-4cfc-8d6d-69ab11a4962a`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 13. vBaseEnvChannel

**容器属性**:

- **UUID**: `d6b26782-a8dd-411f-9e86-0ae11e9a7fdf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `b3b68af2-3737-4999-8a84-d64230b0cde2`
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

- **UUID**: `b20c3af5-f4ef-4ce1-b07c-1fc5029d27d4`
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

- **UUID**: `5c48491f-fae8-4cfc-8d6d-69ab11a4962a`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 14. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `15acb0fb-a614-4773-bbac-f1704adfc710`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `a35c95d1-e74e-46ab-90e2-eb6c69f681cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `0b7545f3-f8f3-4402-931d-9d81adedbbe5`
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

- **UUID**: `e20cb4fb-bdfb-4a29-aa54-ff6d82d57002`
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

- **UUID**: `f1fa0989-8360-40fe-8b9b-80c9a728e41c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 15. vBaseEnvChannel

**容器属性**:

- **UUID**: `a35c95d1-e74e-46ab-90e2-eb6c69f681cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `0b7545f3-f8f3-4402-931d-9d81adedbbe5`
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

- **UUID**: `e20cb4fb-bdfb-4a29-aa54-ff6d82d57002`
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

- **UUID**: `f1fa0989-8360-40fe-8b9b-80c9a728e41c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 16. vBaseEnvI2c

**容器属性**:

- **UUID**: `6a974cd3-a220-45c0-bba1-f656f8d4c738`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `b191c6d6-2270-45a7-8480-ea3e7f0e779b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `3882eb08-2cda-4519-a830-41e62533ec3f`
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

- **UUID**: `5de14007-0210-427d-a27f-f0ebf3c69f1d`
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

- **UUID**: `70d74e24-f320-4cc0-a157-6820f9c1e43b`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 17. vBaseEnvChannel

**容器属性**:

- **UUID**: `b191c6d6-2270-45a7-8480-ea3e7f0e779b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `3882eb08-2cda-4519-a830-41e62533ec3f`
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

- **UUID**: `5de14007-0210-427d-a27f-f0ebf3c69f1d`
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

- **UUID**: `70d74e24-f320-4cc0-a157-6820f9c1e43b`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 18. vBaseEnvPeripheralClocks

**容器属性**:

- **UUID**: `02859b55-98c6-481d-b86d-1cf9e970db7f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvPeripheralClocks`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for family specific default peripheral clock settings

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. vBaseEnvCan

**容器属性**:

- **UUID**: `ecdc4218-39c4-445e-9b9b-292e0c78195f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvCan_Clock

- **UUID**: `3f6c319f-60dc-4f6e-b75f-66c6adf67ecf`
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

- **UUID**: `fcf9bf71-f304-4a55-a578-a133e1023bc1`
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

- **UUID**: `5da695a4-b9be-4ad9-85a8-557a2b4ba857`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvLin_Clock

- **UUID**: `2859e1ef-f2d3-4b21-a520-2e7a244b3d6a`
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

- **UUID**: `d8b7fe8c-13eb-47e0-8f86-b8459072e1b8`
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

- **UUID**: `f476e74d-52b6-4c8d-acff-6abdbe910dbb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvFlexray_Clock

- **UUID**: `193bc9fe-3187-444f-a9da-668930ca363b`
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

- **UUID**: `7c648641-5985-4315-8231-c7efa49704f3`
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

- **UUID**: `3030cf48-07ba-44f7-8c35-c4fca66077b5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvEthernet_Clock

- **UUID**: `022860d8-b6b6-414d-9388-32ad6706b4a0`
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

- **UUID**: `ab15e55b-2c59-4805-9ec4-6d763a18e4f4`
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

- **UUID**: `728d370c-2a62-4857-a6ca-da588ae62885`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvHyperbus_Clock

- **UUID**: `125aeb3b-51af-42db-a5ea-c829a76c17ae`
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

- **UUID**: `373453ac-8104-4c9e-afad-6e42c9bc7495`
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

- **UUID**: `6dae2b38-7469-4677-a82d-4bee0c02258f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvI2c_Clock

- **UUID**: `84c03c75-e9e6-4503-b082-250fad4a5ed3`
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

- **UUID**: `55b34619-2502-4f71-8edc-9d8121e2f669`
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

####### 19. vBaseEnvCan

**容器属性**:

- **UUID**: `ecdc4218-39c4-445e-9b9b-292e0c78195f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvCan_Clock

- **UUID**: `3f6c319f-60dc-4f6e-b75f-66c6adf67ecf`
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

- **UUID**: `fcf9bf71-f304-4a55-a578-a133e1023bc1`
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

####### 20. vBaseEnvLin

**容器属性**:

- **UUID**: `5da695a4-b9be-4ad9-85a8-557a2b4ba857`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvLin_Clock

- **UUID**: `2859e1ef-f2d3-4b21-a520-2e7a244b3d6a`
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

- **UUID**: `d8b7fe8c-13eb-47e0-8f86-b8459072e1b8`
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

####### 21. vBaseEnvFlexray

**容器属性**:

- **UUID**: `f476e74d-52b6-4c8d-acff-6abdbe910dbb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvFlexray_Clock

- **UUID**: `193bc9fe-3187-444f-a9da-668930ca363b`
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

- **UUID**: `7c648641-5985-4315-8231-c7efa49704f3`
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

####### 22. vBaseEnvEthernet

**容器属性**:

- **UUID**: `3030cf48-07ba-44f7-8c35-c4fca66077b5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvEthernet_Clock

- **UUID**: `022860d8-b6b6-414d-9388-32ad6706b4a0`
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

- **UUID**: `ab15e55b-2c59-4805-9ec4-6d763a18e4f4`
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

####### 23. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `728d370c-2a62-4857-a6ca-da588ae62885`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvHyperbus_Clock

- **UUID**: `125aeb3b-51af-42db-a5ea-c829a76c17ae`
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

- **UUID**: `373453ac-8104-4c9e-afad-6e42c9bc7495`
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

####### 24. vBaseEnvI2c

**容器属性**:

- **UUID**: `6dae2b38-7469-4677-a82d-4bee0c02258f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvI2c_Clock

- **UUID**: `84c03c75-e9e6-4503-b082-250fad4a5ed3`
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

- **UUID**: `55b34619-2502-4f71-8edc-9d8121e2f669`
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

##### 2. vBaseEnvDerivativeInformation

**容器属性**:

- **UUID**: `b536cccb-fdc6-4f64-8db7-aeecbc0f583a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvDerivativeInformation`
- **多重性**: [1..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **13** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvCpuMaxFrequency

- **UUID**: `6372fa95-80fa-4154-b7e5-084796197335`
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

- **UUID**: `fed537f9-924e-42a0-a567-a626a5e40ba8`
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

- **UUID**: `aba5d6ca-abb3-4a10-b94a-83fa5411142e`
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

- **UUID**: `6e4e0fbb-ddde-4f30-901a-3ab09d7b79b9`
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

- **UUID**: `bcb37216-aa4c-4f98-a6d6-c09520446dc6`
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

- **UUID**: `040cbea7-7c2a-49ff-9a0a-b5fb3efd695e`
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

- **UUID**: `74d97346-1f4f-4847-b505-2ce151f94bb0`
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

- **UUID**: `9b1e6c72-d053-4386-bb68-f916ba28a320`
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

- **UUID**: `e7940b06-a8e3-47bc-a8d3-7432afdc521b`
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

####### STRING 类型参数

######## 1. vBaseEnvTestedDerivative

- **UUID**: `9aaccae4-85a2-442b-9db8-d199be13222b`
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

- **UUID**: `872bdfe9-aa6e-4c16-8118-f5ac2e38049b`
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

- **UUID**: `b5ce5f95-13d9-4a28-bdbf-eabf865db7a2`
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

- **UUID**: `ab16d57a-9dbb-411f-abd4-88bb83615862`
- **参数名**: `vBaseEnvCpuCore`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `OTHER` (来源: Vector Informatik)
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the core architecture of this derivative.
This value will be generated into vBrsCfg.h as
BRS_CPU_CORE_x

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vBaseEnvAdditionalParameters

**容器属性**:

- **UUID**: `c1d9a404-967f-4991-8e85-05437d9f95bb`
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

- **UUID**: `2a0798ad-dc7d-4bb8-a2cc-434472cb9a5f`
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

- **UUID**: `6c60aa3b-1a48-44fd-8857-65a330434c15`
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

- **UUID**: `0164165d-f469-4f9d-bcfc-261ed161887c`
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
- **描述**: Configure the PLL Group of your derivative

########## 2. vBaseEnvClockGroup

- **UUID**: `1811e373-7a78-4632-ac63-0a783fb2787b`
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

- **UUID**: `eb9f584f-a9a0-43dd-9900-c23d78fdee2f`
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

- **UUID**: `1347312d-6baa-47f7-ac4c-784ea44a2d18`
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

- **UUID**: `9c44d3e1-c3f2-490e-aeab-53cddc52a177`
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

- **UUID**: `9a1276d0-3181-4055-8246-e683819e682c`
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

- **UUID**: `1d5f9ab1-9c27-47a8-bd2f-f7ad39088322`
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

- **UUID**: `24f6d986-eaa7-433c-9ff1-a6ae43d00db0`
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

- **UUID**: `eb21f87b-b6ec-4719-a9c7-dacdbb6b6869`
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

- **UUID**: `6ee5851b-58f9-41d2-8cd6-e11e83d8f9d8`
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

- **UUID**: `fe991146-26ad-46e2-a7ff-194d880bb1a7`
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

- **UUID**: `68a0a334-2d79-45af-974c-200097b63d67`
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

- **UUID**: `169fdfa6-1e71-4f05-acbf-82e7e750d49c`
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

##### 3. vBaseEnvAdditionalParameters

**容器属性**:

- **UUID**: `c1d9a404-967f-4991-8e85-05437d9f95bb`
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

- **UUID**: `2a0798ad-dc7d-4bb8-a2cc-434472cb9a5f`
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

- **UUID**: `6c60aa3b-1a48-44fd-8857-65a330434c15`
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

- **UUID**: `0164165d-f469-4f9d-bcfc-261ed161887c`
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
- **描述**: Configure the PLL Group of your derivative

######## 2. vBaseEnvClockGroup

- **UUID**: `1811e373-7a78-4632-ac63-0a783fb2787b`
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

- **UUID**: `eb9f584f-a9a0-43dd-9900-c23d78fdee2f`
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

- **UUID**: `1347312d-6baa-47f7-ac4c-784ea44a2d18`
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

- **UUID**: `9c44d3e1-c3f2-490e-aeab-53cddc52a177`
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

- **UUID**: `9a1276d0-3181-4055-8246-e683819e682c`
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

- **UUID**: `1d5f9ab1-9c27-47a8-bd2f-f7ad39088322`
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

- **UUID**: `24f6d986-eaa7-433c-9ff1-a6ae43d00db0`
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

- **UUID**: `eb21f87b-b6ec-4719-a9c7-dacdbb6b6869`
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

- **UUID**: `6ee5851b-58f9-41d2-8cd6-e11e83d8f9d8`
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

- **UUID**: `fe991146-26ad-46e2-a7ff-194d880bb1a7`
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

- **UUID**: `68a0a334-2d79-45af-974c-200097b63d67`
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

- **UUID**: `169fdfa6-1e71-4f05-acbf-82e7e750d49c`
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

##### 5. vBaseEnvMemLayoutHwRegion

**容器属性**:

- **UUID**: `dbd5200f-9bee-4b1e-83a0-2bb210fb0c80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvMemLayoutHwRegion`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container to structure the configuration parameters of hardware memory regions.

##### 6. vBaseEnvInterruptHandling

**容器属性**:

- **UUID**: `0d46b873-5159-4f4b-9d41-add34afa2bf2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvInterruptHandling`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for family specific default interrupt settings

###### 配置容器

本模块包含 **12** 个配置容器：

####### 1. vBaseEnvCan

**容器属性**:

- **UUID**: `2a686f3f-d5a9-44ef-8b92-df2bf6ab3f74`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `c8b6dde1-038d-4a9f-b5eb-06adb9f57893`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `b4cadab5-977a-42d8-9159-fc70350faa9b`
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

- **UUID**: `1191b17c-c217-4973-80f3-ef2f7afebde0`
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

- **UUID**: `c2b23bb8-b802-4570-92f9-2f42a21dbfc3`
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

- **UUID**: `c8b6dde1-038d-4a9f-b5eb-06adb9f57893`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `b4cadab5-977a-42d8-9159-fc70350faa9b`
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

- **UUID**: `1191b17c-c217-4973-80f3-ef2f7afebde0`
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

- **UUID**: `c2b23bb8-b802-4570-92f9-2f42a21dbfc3`
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

- **UUID**: `7025aa7c-8ce8-45c6-9400-109bb77ae077`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `183ca6d5-5afc-43cf-af42-af7c53359920`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `c729ed6b-6ff0-43a3-90e0-8e6d85e70a7f`
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

- **UUID**: `003d33d5-2e10-4e3e-8640-2b50b1d858a5`
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

- **UUID**: `49fed7c0-d9bd-40db-8e1f-63a07abf01ed`
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

- **UUID**: `183ca6d5-5afc-43cf-af42-af7c53359920`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `c729ed6b-6ff0-43a3-90e0-8e6d85e70a7f`
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

- **UUID**: `003d33d5-2e10-4e3e-8640-2b50b1d858a5`
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

- **UUID**: `49fed7c0-d9bd-40db-8e1f-63a07abf01ed`
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

- **UUID**: `ba8359a0-6cf7-4521-b992-aac66c3bfab3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `4c8dcfc3-8998-4a2a-aa56-465b29e0b7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `da9f0fcf-e04c-45e2-bb36-7f08b6fd8139`
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

- **UUID**: `3f6e3105-803f-48d2-8b44-816f649ebffa`
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

- **UUID**: `cff7d8b3-b257-47c0-812e-e29b2169fc1f`
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

- **UUID**: `4c8dcfc3-8998-4a2a-aa56-465b29e0b7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `da9f0fcf-e04c-45e2-bb36-7f08b6fd8139`
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

- **UUID**: `3f6e3105-803f-48d2-8b44-816f649ebffa`
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

- **UUID**: `cff7d8b3-b257-47c0-812e-e29b2169fc1f`
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

- **UUID**: `f434df43-e5c7-47ef-a078-cbf24e74b231`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `d6b26782-a8dd-411f-9e86-0ae11e9a7fdf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `b3b68af2-3737-4999-8a84-d64230b0cde2`
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

- **UUID**: `b20c3af5-f4ef-4ce1-b07c-1fc5029d27d4`
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

- **UUID**: `5c48491f-fae8-4cfc-8d6d-69ab11a4962a`
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

- **UUID**: `d6b26782-a8dd-411f-9e86-0ae11e9a7fdf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `b3b68af2-3737-4999-8a84-d64230b0cde2`
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

- **UUID**: `b20c3af5-f4ef-4ce1-b07c-1fc5029d27d4`
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

- **UUID**: `5c48491f-fae8-4cfc-8d6d-69ab11a4962a`
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

- **UUID**: `15acb0fb-a614-4773-bbac-f1704adfc710`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `a35c95d1-e74e-46ab-90e2-eb6c69f681cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `0b7545f3-f8f3-4402-931d-9d81adedbbe5`
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

- **UUID**: `e20cb4fb-bdfb-4a29-aa54-ff6d82d57002`
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

- **UUID**: `f1fa0989-8360-40fe-8b9b-80c9a728e41c`
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

- **UUID**: `a35c95d1-e74e-46ab-90e2-eb6c69f681cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `0b7545f3-f8f3-4402-931d-9d81adedbbe5`
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

- **UUID**: `e20cb4fb-bdfb-4a29-aa54-ff6d82d57002`
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

- **UUID**: `f1fa0989-8360-40fe-8b9b-80c9a728e41c`
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

- **UUID**: `6a974cd3-a220-45c0-bba1-f656f8d4c738`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `b191c6d6-2270-45a7-8480-ea3e7f0e779b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vBaseEnvIndex

- **UUID**: `3882eb08-2cda-4519-a830-41e62533ec3f`
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

- **UUID**: `5de14007-0210-427d-a27f-f0ebf3c69f1d`
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

- **UUID**: `70d74e24-f320-4cc0-a157-6820f9c1e43b`
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

- **UUID**: `b191c6d6-2270-45a7-8480-ea3e7f0e779b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `3882eb08-2cda-4519-a830-41e62533ec3f`
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

- **UUID**: `5de14007-0210-427d-a27f-f0ebf3c69f1d`
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

- **UUID**: `70d74e24-f320-4cc0-a157-6820f9c1e43b`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 7. vBaseEnvCan

**容器属性**:

- **UUID**: `2a686f3f-d5a9-44ef-8b92-df2bf6ab3f74`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `c8b6dde1-038d-4a9f-b5eb-06adb9f57893`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `b4cadab5-977a-42d8-9159-fc70350faa9b`
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

- **UUID**: `1191b17c-c217-4973-80f3-ef2f7afebde0`
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

- **UUID**: `c2b23bb8-b802-4570-92f9-2f42a21dbfc3`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 8. vBaseEnvChannel

**容器属性**:

- **UUID**: `c8b6dde1-038d-4a9f-b5eb-06adb9f57893`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `b4cadab5-977a-42d8-9159-fc70350faa9b`
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

- **UUID**: `1191b17c-c217-4973-80f3-ef2f7afebde0`
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

- **UUID**: `c2b23bb8-b802-4570-92f9-2f42a21dbfc3`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 9. vBaseEnvLin

**容器属性**:

- **UUID**: `7025aa7c-8ce8-45c6-9400-109bb77ae077`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `183ca6d5-5afc-43cf-af42-af7c53359920`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `c729ed6b-6ff0-43a3-90e0-8e6d85e70a7f`
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

- **UUID**: `003d33d5-2e10-4e3e-8640-2b50b1d858a5`
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

- **UUID**: `49fed7c0-d9bd-40db-8e1f-63a07abf01ed`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 10. vBaseEnvChannel

**容器属性**:

- **UUID**: `183ca6d5-5afc-43cf-af42-af7c53359920`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `c729ed6b-6ff0-43a3-90e0-8e6d85e70a7f`
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

- **UUID**: `003d33d5-2e10-4e3e-8640-2b50b1d858a5`
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

- **UUID**: `49fed7c0-d9bd-40db-8e1f-63a07abf01ed`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 11. vBaseEnvFlexray

**容器属性**:

- **UUID**: `ba8359a0-6cf7-4521-b992-aac66c3bfab3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `4c8dcfc3-8998-4a2a-aa56-465b29e0b7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `da9f0fcf-e04c-45e2-bb36-7f08b6fd8139`
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

- **UUID**: `3f6e3105-803f-48d2-8b44-816f649ebffa`
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

- **UUID**: `cff7d8b3-b257-47c0-812e-e29b2169fc1f`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 12. vBaseEnvChannel

**容器属性**:

- **UUID**: `4c8dcfc3-8998-4a2a-aa56-465b29e0b7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `da9f0fcf-e04c-45e2-bb36-7f08b6fd8139`
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

- **UUID**: `3f6e3105-803f-48d2-8b44-816f649ebffa`
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

- **UUID**: `cff7d8b3-b257-47c0-812e-e29b2169fc1f`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 13. vBaseEnvEthernet

**容器属性**:

- **UUID**: `f434df43-e5c7-47ef-a078-cbf24e74b231`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `d6b26782-a8dd-411f-9e86-0ae11e9a7fdf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `b3b68af2-3737-4999-8a84-d64230b0cde2`
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

- **UUID**: `b20c3af5-f4ef-4ce1-b07c-1fc5029d27d4`
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

- **UUID**: `5c48491f-fae8-4cfc-8d6d-69ab11a4962a`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 14. vBaseEnvChannel

**容器属性**:

- **UUID**: `d6b26782-a8dd-411f-9e86-0ae11e9a7fdf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `b3b68af2-3737-4999-8a84-d64230b0cde2`
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

- **UUID**: `b20c3af5-f4ef-4ce1-b07c-1fc5029d27d4`
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

- **UUID**: `5c48491f-fae8-4cfc-8d6d-69ab11a4962a`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 15. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `15acb0fb-a614-4773-bbac-f1704adfc710`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `a35c95d1-e74e-46ab-90e2-eb6c69f681cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `0b7545f3-f8f3-4402-931d-9d81adedbbe5`
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

- **UUID**: `e20cb4fb-bdfb-4a29-aa54-ff6d82d57002`
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

- **UUID**: `f1fa0989-8360-40fe-8b9b-80c9a728e41c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 16. vBaseEnvChannel

**容器属性**:

- **UUID**: `a35c95d1-e74e-46ab-90e2-eb6c69f681cf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `0b7545f3-f8f3-4402-931d-9d81adedbbe5`
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

- **UUID**: `e20cb4fb-bdfb-4a29-aa54-ff6d82d57002`
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

- **UUID**: `f1fa0989-8360-40fe-8b9b-80c9a728e41c`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 17. vBaseEnvI2c

**容器属性**:

- **UUID**: `6a974cd3-a220-45c0-bba1-f656f8d4c738`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBaseEnvChannel

**容器属性**:

- **UUID**: `b191c6d6-2270-45a7-8480-ea3e7f0e779b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvIndex

- **UUID**: `3882eb08-2cda-4519-a830-41e62533ec3f`
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

- **UUID**: `5de14007-0210-427d-a27f-f0ebf3c69f1d`
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

- **UUID**: `70d74e24-f320-4cc0-a157-6820f9c1e43b`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 18. vBaseEnvChannel

**容器属性**:

- **UUID**: `b191c6d6-2270-45a7-8480-ea3e7f0e779b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvChannel`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvIndex

- **UUID**: `3882eb08-2cda-4519-a830-41e62533ec3f`
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

- **UUID**: `5de14007-0210-427d-a27f-f0ebf3c69f1d`
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

- **UUID**: `70d74e24-f320-4cc0-a157-6820f9c1e43b`
- **参数名**: `vBaseEnvIsrInterruptSource`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 19. vBaseEnvPeripheralClocks

**容器属性**:

- **UUID**: `02859b55-98c6-481d-b86d-1cf9e970db7f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvPeripheralClocks`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for family specific default peripheral clock settings

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. vBaseEnvCan

**容器属性**:

- **UUID**: `ecdc4218-39c4-445e-9b9b-292e0c78195f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvCan_Clock

- **UUID**: `3f6c319f-60dc-4f6e-b75f-66c6adf67ecf`
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

- **UUID**: `fcf9bf71-f304-4a55-a578-a133e1023bc1`
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

- **UUID**: `5da695a4-b9be-4ad9-85a8-557a2b4ba857`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvLin_Clock

- **UUID**: `2859e1ef-f2d3-4b21-a520-2e7a244b3d6a`
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

- **UUID**: `d8b7fe8c-13eb-47e0-8f86-b8459072e1b8`
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

- **UUID**: `f476e74d-52b6-4c8d-acff-6abdbe910dbb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvFlexray_Clock

- **UUID**: `193bc9fe-3187-444f-a9da-668930ca363b`
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

- **UUID**: `7c648641-5985-4315-8231-c7efa49704f3`
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

- **UUID**: `3030cf48-07ba-44f7-8c35-c4fca66077b5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvEthernet_Clock

- **UUID**: `022860d8-b6b6-414d-9388-32ad6706b4a0`
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

- **UUID**: `ab15e55b-2c59-4805-9ec4-6d763a18e4f4`
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

- **UUID**: `728d370c-2a62-4857-a6ca-da588ae62885`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvHyperbus_Clock

- **UUID**: `125aeb3b-51af-42db-a5ea-c829a76c17ae`
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

- **UUID**: `373453ac-8104-4c9e-afad-6e42c9bc7495`
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

- **UUID**: `6dae2b38-7469-4677-a82d-4bee0c02258f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBaseEnvI2c_Clock

- **UUID**: `84c03c75-e9e6-4503-b082-250fad4a5ed3`
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

- **UUID**: `55b34619-2502-4f71-8edc-9d8121e2f669`
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

##### 20. vBaseEnvCan

**容器属性**:

- **UUID**: `ecdc4218-39c4-445e-9b9b-292e0c78195f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvCan`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvCan_Clock

- **UUID**: `3f6c319f-60dc-4f6e-b75f-66c6adf67ecf`
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

- **UUID**: `fcf9bf71-f304-4a55-a578-a133e1023bc1`
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

##### 21. vBaseEnvLin

**容器属性**:

- **UUID**: `5da695a4-b9be-4ad9-85a8-557a2b4ba857`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvLin`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvLin_Clock

- **UUID**: `2859e1ef-f2d3-4b21-a520-2e7a244b3d6a`
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

- **UUID**: `d8b7fe8c-13eb-47e0-8f86-b8459072e1b8`
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

##### 22. vBaseEnvFlexray

**容器属性**:

- **UUID**: `f476e74d-52b6-4c8d-acff-6abdbe910dbb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvFlexray_Clock

- **UUID**: `193bc9fe-3187-444f-a9da-668930ca363b`
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

- **UUID**: `7c648641-5985-4315-8231-c7efa49704f3`
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

##### 23. vBaseEnvEthernet

**容器属性**:

- **UUID**: `3030cf48-07ba-44f7-8c35-c4fca66077b5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvEthernet_Clock

- **UUID**: `022860d8-b6b6-414d-9388-32ad6706b4a0`
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

- **UUID**: `ab15e55b-2c59-4805-9ec4-6d763a18e4f4`
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

##### 24. vBaseEnvHyperbus

**容器属性**:

- **UUID**: `728d370c-2a62-4857-a6ca-da588ae62885`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvHyperbus_Clock

- **UUID**: `125aeb3b-51af-42db-a5ea-c829a76c17ae`
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

- **UUID**: `373453ac-8104-4c9e-afad-6e42c9bc7495`
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

##### 25. vBaseEnvI2c

**容器属性**:

- **UUID**: `6dae2b38-7469-4677-a82d-4bee0c02258f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBaseEnvI2c`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBaseEnvI2c_Clock

- **UUID**: `84c03c75-e9e6-4503-b082-250fad4a5ed3`
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

- **UUID**: `55b34619-2502-4f71-8edc-9d8121e2f669`
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

- **UUID**: `159ca0aa-babb-4b42-9884-5b0625d2a6a7`
- **实现名称**: `vBaseEnv_Impl`
- **编程语言**: C
- **软件版本**: 1.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator
