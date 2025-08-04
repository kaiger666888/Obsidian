# Dsadc - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:05

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Dsadc](#dsadc)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Dsadc

#### 基本信息

- **UUID**: `ECUC:c03229fe-4dca-445e-a47c-1ae11e6c1832`
- **模块名称**: `Dsadc`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the Dsadc (Delta Sigma Analog Digital Conversion) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **22** 个配置容器：

##### 1. DsadcGeneral

**容器属性**:

- **UUID**: `dcc39b88-cc2b-4358-ba88-30120722c6ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGeneral`
- **多重性**: [0..1]

**容器描述**:

This Container contains all the general configuration parameters for the DSADC driver

###### 参数配置

此容器包含 **7** 个参数：

####### BOOLEAN 类型参数

######## 1. DsadcDevErrorDetect

- **UUID**: `a4e850e4-be6b-4d72-b360-c13bb0bff7fa`
- **参数名**: `DsadcDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This Parameter Enables/Disables the Development Error Detection and reporting in the Dsadc Driver

######## 2. DsadcSafetyEnable

- **UUID**: `ECUC:412da385-6bf4-4819-11e4-8ec223fb5b17`
- **参数名**: `DsadcSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: ThisParameter determines whether to Enable/Disable the safety check and reporting.

######## 3. DsadcDeInitApi

- **UUID**: `b8ede77d-3270-4da8-b3b5-3bf169de9af0`
- **参数名**: `DsadcDeInitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This Parameter adds or removes the service Dsadc_DeInit() API from the code.

######## 4. DsadcInitCheckApi

- **UUID**: `ECUC:dbfab416-7231-4c9e-b7a2-2580d8484ecf`
- **参数名**: `DsadcInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This Parameter adds or removes the service Dsadc_InitCheck() API from the code.

######## 5. DsadcVersionInfoApi

- **UUID**: `ECUC:ee2b1f91-e6a6-4012-8329-e7ff99105dba`
- **参数名**: `DsadcVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This Parameter adds or removes the service Dsadc_GetVersionInfo() API from the code.

####### ENUMERATION 类型参数

######## 1. DsadcInitDeInitApiMode

- **UUID**: `ECUC:7e0e69e5-6004-1956-a113-f0559f2409d6`
- **参数名**: `DsadcInitDeInitApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `DSADC_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the privilege mode in which the Initialization and De-initialization APIs would operate.

######## 2. DsadcRuntimeApiMode

- **UUID**: `ECUC:7e0e69e5-6004-1956-2213-f0559f2409d6`
- **参数名**: `DsadcRuntimeApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `DSADC_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: This Parameter defines the privilege mode in which the runtime APIs would operate.

##### 2. CommonPublishedInformation

**容器属性**:

- **UUID**: `492f8482-3e2c-4bf1-b27f-01fd7ac35cc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CommonPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

This container contains the published information of the DSADC driver.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. ArMajorVersion

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b258bcca`
- **参数名**: `ArMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 2. ArMinorVersion

- **UUID**: `73f87c7f-e230-4178-3333-ea2704aaecc6`
- **参数名**: `ArMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 3. ArPatchVersion

- **UUID**: `2380135d-6778-417a-3333-e100aad4cc54`
- **参数名**: `ArPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 4. SwMajorVersion

- **UUID**: `fca015e3-5f28-4cbe-3333-8fab87d8cc27`
- **参数名**: `SwMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 5. SwMinorVersion

- **UUID**: `14ab81e0-3d80-43dc-3333-2a7e5a54ccf9`
- **参数名**: `SwMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 6. SwPatchVersion

- **UUID**: `32e37bfd-18b6-41d1-3333-a81dae0cc4c5`
- **参数名**: `SwPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 7. ModuleId

- **UUID**: `3b407478-6902-4f80-3333-f33b08cce638`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Module ID of this module from Module List

######## 8. VendorId

- **UUID**: `7d650b2d-4adb-41f0-3333-5f0c41cc01d1`
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

##### 3. DsadcDemEventParameterRefs

**容器属性**:

- **UUID**: `4c697a37-02d8-42df-8696-0c9f592108c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

Container list down the production errors supported by the DSADC driver.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. DsadcClcFailureNotification

- **UUID**: `66c8e900-6197-42a3-8125-a695aa21788a`
- **引用名**: `DsadcClcFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Parameter defines whether CLC failure DEM notification is enabled or not..

######## 2. DsadcFifoFailureNotification

- **UUID**: `be9bb670-d214-4aac-a1d7-9def944a46ea`
- **引用名**: `DsadcFifoFailureNotification`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Parameter defines whether FIFO failure DEM notification is enabled or not..

##### 4. DsadcConfigSet

**容器属性**:

- **UUID**: `ccda81dc-46cf-4145-858b-7c947884702f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcConfigSet`
- **多重性**: [0..1]

**容器描述**:

This is the base container that contains Dsadc module related parameters

###### 配置容器

本模块包含 **18** 个配置容器：

####### 1. DsadcGlobalConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGlobalConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the parameters to configure DSADC IP global configuration.

######## 参数配置

此容器包含 **4** 个参数：

######### ENUMERATION 类型参数

########## 1. DsadcDitheringTrimValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f55c6cc3`
- **参数名**: `DsadcDitheringTrimValue`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_DITHERING_MIN_50_MILVLT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_DITHERING_MIN_50_MILVLT` (来源: INFINEON_AURIX2G)
  - `DSADC_DITHERING_LOW_100_MILVLT` (来源: INFINEON_AURIX2G)
  - `DSADC_DITHERING_MED_200_MILVLT` (来源: INFINEON_AURIX2G)
  - `DSADC_DITHERING_HIGH_400_MILVLT` (来源: INFINEON_AURIX2G)
- **描述**: Defines trimming value for internal dithering function. This trimming value is used for all the modulators of DSADC

########## 2. DsadcSleepMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f55c6cc4`
- **参数名**: `DsadcSleepMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SLEEP_ENABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SLEEP_ENABLE` (来源: INFINEON_AURIX2G)
  - `SLEEP_DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: Parameter defines EDSADC reaction to the Sleep mode requests

########## 3. DsadcSupplyVoltageLevel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f55c6cc5`
- **参数名**: `DsadcSupplyVoltageLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `VOLTAGESUPPLY_AUTO`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `VOLTAGESUPPLY_AUTO` (来源: INFINEON_AURIX2G)
  - `VOLTAGESUPPLY_5V` (来源: INFINEON_AURIX2G)
  - `VOLTAGESUPPLY_3_3V` (来源: INFINEON_AURIX2G)
- **描述**: Parameter defines the supply voltage level to be used for DSADC internal operations

########## 4. DsadcSyncClockGen

- **UUID**: `DCE:d6ea9dd9-1d6e-4d4b-b3a3-23e9455c6ccc`
- **参数名**: `DsadcSyncClockGen`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `UNSYNCHRONIZED_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SYNCHRONIZED_MODE` (来源: INFINEON_AURIX2G)
  - `UNSYNCHRONIZED_MODE` (来源: INFINEON_AURIX2G)
- **描述**: Parameter defines the influence of Analog Phase synchronizer on the clock generated

####### 2. DsadcCarrierGeneratorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a5cccccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCarrierGeneratorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the Carrier Generation related Parameters.

######## 参数配置

此容器包含 **4** 个参数：

######### ENUMERATION 类型参数

########## 1. DsadcPwmGenerationMode

- **UUID**: `d4aec598-5cc7-4487-9530-36ee9e854cc6`
- **参数名**: `DsadcPwmGenerationMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_NORMAL_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_NORMAL_MODE` (来源: INFINEON_AURIX2G)
  - `DSADC_BIT_REVERSE_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the mode in which the Carrier Generator signal is generated.                                                       In case of Bit Reverse generation mode, it increases the frequency spectrum to yield a smoother induced sine signal. This is done by distributing the 0 and 1 bits over the 32 cycles of a PWM period.

########## 2. DsadcCarrierFrequencyClockDiv

- **UUID**: `d6ea9dd7-1d6e-4d4b-b3a3-24e9f55c6cc8`
- **参数名**: `DsadcCarrierFrequencyClockDiv`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CG_CLOCKDIVIDER_DIV2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CG_CLOCKDIVIDER_DIV2` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV6` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV10` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV12` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV14` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV16` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV18` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV20` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV22` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV24` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV26` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV28` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV30` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which is used to define the frequency of the carrier signal generator, which is derived from the selected internal clock source and divider factor.

########## 3. DsadcCarrierSignalPolarity

- **UUID**: `d4aec598-5cc7-4487-9530-36ee9e855cc7`
- **参数名**: `DsadcCarrierSignalPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CARR_SIG_NORMAL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CARR_SIG_NORMAL` (来源: INFINEON_AURIX2G)
  - `DSADC_CARR_SIG_INVERTED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the starting polarity of the carrier signal.

########## 4. DsadcCarrierSignalType

- **UUID**: `7a116fc8-99ac-44d9-b5c9-9413dc8aed29`
- **参数名**: `DsadcCarrierSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CARR_SIG_STOPPED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CARR_SIG_STOPPED` (来源: INFINEON_AURIX2G)
  - `DSADC_CARR_SIG_SQUAREWAVE` (来源: INFINEON_AURIX2G)
  - `DSADC_CARR_SIG_TRIANGLE` (来源: INFINEON_AURIX2G)
  - `DSADC_CARR_SIG_SINEWAVE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the carrier signal type to be generated.

####### 3. DsadcErsEtlConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-b6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcErsEtlConfig`
- **多重性**: [0..8]

**容器描述**:

This container configures the parameters for ERU input triggering

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. DsadcEruStatusFlagConfig

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-94e9f55c6ccc`
- **参数名**: `DsadcEruStatusFlagConfig`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_ETL_FALLING_EDGE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_ETL_FALLING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_ETL_RISING_EDGE` (来源: INFINEON_AURIX2G)
- **描述**: This parameters defines the condition on which the status flag in ETL block of ERU is set. On the inverse of the edge selected, the status flag is cleared.

########## 2. DsadcEruErsInputPin

- **UUID**: `7e0e69e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `DsadcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_0_REQ0A_PORTS_P15_4`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_0_REQ0A_PORTS_P15_4` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ0B_CCU60_COUT60` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ0C_PORTS_P10_7` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ0D_MSC0_FCLP` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ0E_STM5_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ0F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ1A_PORTS_P14_3` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ1B_CCU61_COUT60` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ1C_PORTS_P10_8` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ1D_STM0_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ1E_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ1F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ2A_PORTS_P10_2` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ2B_PORTS_P02_1` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ2C_PORTS_P00_4` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ2D_ERAY0_MT` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ2E_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ2F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ3A_PORTS_P10_3` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ3B_PORTS_P14_1` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ3C_PORTS_P02_0` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ3D_STM1_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ3E_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ3F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ4A_PORTS_P33_7` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ4B_GTM_TOM0_12` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ4C_GPT120_T3OUT` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ4D_PORTS_P15_5` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ4E_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ4F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ5A_PORTS_P15_8` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ5B_GTM_TOM1_12` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ5C_GPT120_T6OUT` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ5D_STM2_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ5E_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ5F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ6A_PORTS_P20_0` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ6B_PORTS_ESR0` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ6C_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ6D_PORTS_P11_10` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ6E_STM3_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ6F_GTM_TOM2_12` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ7A_PORTS_P20_9` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ7B_PORTS_ESR1` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ7C_PORTS_P15_1` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ7D_ERAY1_MT` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ7E_STM4_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ7F_GTM_TOM3_12` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DsadcEruErsRef

- **UUID**: `66c8e900-6193-42a3-8125-a695cc21788e`
- **引用名**: `DsadcEruErsRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

####### 4. DsadcChannelConfiguration

**容器属性**:

- **UUID**: `ccda81dc-46cf-4145-858b-bc9478cccccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcChannelConfiguration`
- **多重性**: [1..6]

**容器描述**:

This container contains the channel configuration (parameters) depending on the hardware capability.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. DsadcChannelId

- **UUID**: `d4aec598-5cc7-4487-9530-36ee9e11cccc`
- **参数名**: `DsadcChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..5]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Unique number to identify the channel

######### ENUMERATION 类型参数

########## 1. DsadcHwChannelNum

- **UUID**: `d4aec598-5cc7-4487-9530-36ee9e12cccc`
- **参数名**: `DsadcHwChannelNum`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CHANNEL_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CHANNEL_0` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_1` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_2` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_3` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_4` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_5` (来源: INFINEON_AURIX2G)
- **描述**: Hardware EDSADC channel number

########## 2. DsadcAccessMode

- **UUID**: `c46bbfe5-3c7e-4b1b-9127-79334c04d53c`
- **参数名**: `DsadcAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_SINGLE_READ`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_SINGLE_READ` (来源: INFINEON_AURIX2G)
  - `DSADC_CIRCULAR_BUFFER` (来源: INFINEON_AURIX2G)
  - `DSADC_STREAM_LINEAR_BUFFER` (来源: INFINEON_AURIX2G)
  - `DSADC_DMA_ACCESS` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the access mode selection for DSADC Driver. The available access mode is depends on parameter DsdcTriggerMode.If the DsadcTriggerMode is configured as TRIGGER_MODE_NORMAL then DsadcAccessMode can be any inside the Range. If DsadcTriggerMode is Configured as TRIGGER_MODE_WINDOW then DsadcAccessMode can be DSADC_SINGLE_READ or DSADC_STRERAM_LINEAR_BUFFER or DSADC_DMA_ACCESS.

########## 3. DsadcTriggerMode

- **UUID**: `a87c6432-965e-4c08-9f97-ed59fe64506f`
- **参数名**: `DsadcTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TRIGGER_MODE_NORMAL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TRIGGER_MODE_NORMAL` (来源: INFINEON_AURIX2G)
  - `DSADC_TRIGGER_MODE_WINDOW` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define the trigger mode. possbile conversion modes are DSADC_TRIGGER_MODE_NORMAL and DSADC_TRIGGER_MODE_WINDOW.                                                         DSADC_TRIGGER_MODE_NORMAL: Conversion starts after calling Dsadc_StartModulation() API.                                                         DSADC_TRIGGER_MODE_WINDOW: The result values are considered after Hardware trigger signal(GTM or ERU) is arrived.

########## 4. DsadcTimestampFeature

- **UUID**: `25863155-48e3-438d-98dc-754126a66d0c`
- **参数名**: `DsadcTimestampFeature`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TIMESTAMP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TIMESTAMP_ENABLED` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: This Parameter is used to define the timestamp Functionality availability for the DSADC Channel.                                                         DSADC_TIMESTAMP_ENABLED: Enable the Timestamp functionality.                                                         DSADC_TIMESTAMP_DISABLED: Disable the Timestamp Functionality.

########## 5. DsadcGateActiveLevel

- **UUID**: `72bfe4df-c1de-4e91-8687-9bf5b7a9485c`
- **参数名**: `DsadcGateActiveLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_GATE_HIGH_LEVEL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_GATE_HIGH_LEVEL` (来源: INFINEON_AURIX2G)
  - `DSADC_GATE_LOW_LEVEL` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define the active level for the trigger gate signal.

######### FUNCTION-NAME 类型参数

########## 1. DsadcBufferFullNotification

- **UUID**: `ECUC:13cdc2fe-cf3c-4a68-93cb-a3676a293fd3`
- **参数名**: `DsadcBufferFullNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Callback function for buffer full event. The availablity of this parameter depends on DsadcAccessMode. If the DsadcAccessMode is configured as ACCESS_MODE_SINGLE OR ACCESS_MODE_CIRCULAR_BUFFER or DSADC_DMA_ACCESS then this parameter is not available.

########## 2. DsadcNewResultNotification

- **UUID**: `ECUC:9918056e-9ee3-49ce-b4fc-d4b8fa37c2d9`
- **参数名**: `DsadcNewResultNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Callback function for new result event.

########## 3. DsadcWindowCloseNotification

- **UUID**: `ECUC:c7c6aad9-cd74-4df6-a2ec-b8d556521c92`
- **参数名**: `DsadcWindowCloseNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Callback function for window close event, the availability of this parameter depends on DsadcTriggerMode configured as DSADC_TRIGGER_MODE_NORMAL

######## 配置容器

本模块包含 **14** 个配置容器：

######### 1. DsadcModulatorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6010059e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcModulatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains configuration parameters related to the On-chip modulator, input pin selection and modulator clock configuration.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. DsadcAnalogClockSyncDelay

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-44e9f55c6ccc`
- **参数名**: `DsadcAnalogClockSyncDelay`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the delay in clock cycles after the sync signal provided from Phase synchronizer.

########### BOOLEAN 类型参数

############ 1. DsadcDitheringEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e3f55c6ccc`
- **参数名**: `DsadcDitheringEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of internal dithering functionality for the modulator.

############ 2. DsadcIntegratorResetEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e7f55c6ccc`
- **参数名**: `DsadcIntegratorResetEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the modulator overload handling.

########### ENUMERATION 类型参数

############ 1. DsadcClockDivider

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e2f55c6ccc`
- **参数名**: `DsadcClockDivider`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CLOCKDIVIDER_DIV4`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV6` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV10` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV12` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV14` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV16` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV18` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the frequency of the modulator clock, which is derived from the peripheral clock

############ 2. DsadcInputGain

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-54e9f55c6ccc`
- **参数名**: `DsadcInputGain`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INPUT_GAIN_FACTOR_1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INPUT_GAIN_FACTOR_1` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUT_GAIN_FACTOR_2` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUT_GAIN_FACTOR_4` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines multiplication Gain factor for the analog input signal.

############ 3. DsadcInputMuxActionMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e4f55c6ccc`
- **参数名**: `DsadcInputMuxActionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INPUTMUX_PRESET_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INPUTMUX_PRESET_MODE` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUTMUX_SINGLE_STEP_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the control mechanism for input multiplexer. It defines the action to be taken for the input multiplexer upon a trigger event for pin selection.

############ 4. DsadcInputMuxControlMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e5f55c6ccc`
- **参数名**: `DsadcInputMuxControlMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INMUX_SOFTWARE_CONTROL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INMUX_SOFTWARE_CONTROL` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_FALLING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_RISING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_BOTH_EDGES` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the condition for a trigger event to control the input multiplexer.

############ 5. DsadcInputPinSelection

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e6f55c6ccc`
- **参数名**: `DsadcInputPinSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_PIN_0_AN2_AN3`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_PIN_0_AN2_AN3` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN12_AN13` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN36_AN37` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN38_AN39` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_2_AN44_AN45` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_3_AN46_AN47` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN20_AN21` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN24_AN25` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN0_AN1` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN14_AN15` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_PORT_00_8_PORT_00_7` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_PORT_00_10_PORT_00_9` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_PORT_00_2_PORT_00_1` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_PORT_00_4_PORT_00_3` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the initial/permanent setting for the input multiplexer, based on the operating mode selected.

############ 6. DsadcNegativeInputLine

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-64e9f55c6ccc`
- **参数名**: `DsadcNegativeInputLine`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_NEG_INPUT_PIN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_NEG_INPUT_PIN` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_SUPPLY_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_COMMON_MODE_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_REFERENCE_GROUND` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the modulator internal connection of the negative input.

############ 7. DsadcPositiveInputLine

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e8f55c6ccc`
- **参数名**: `DsadcPositiveInputLine`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_POS_INPUT_PIN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_POS_INPUT_PIN` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_SUPPLY_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_COMMON_MODE_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_REFERENCE_GROUND` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the modulator internal connection of the positive input.

######### 2. DsadcDemodulatorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10259e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcDemodulatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains configuration parameters related to the de-modulator, input data stream and trigger selection.

########## 参数配置

此容器包含 **3** 个参数：

########### ENUMERATION 类型参数

############ 1. DsadcIntegratorTriggerMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f54c6ccc`
- **参数名**: `DsadcIntegratorTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INTR_BYPASSED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INTR_BYPASSED` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_FALLING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_RISING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_ALWAYS_ACTIVE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the Integrator trigger mode.

############ 2. DsadcResultDisplayMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f58c6ccc`
- **参数名**: `DsadcResultDisplayMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RES_SIGNED_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RES_SIGNED_MODE` (来源: INFINEON_AURIX2G)
  - `DSADC_RES_UNSIGNED_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the ranges of the result values i.e. result display modes.

############ 3. DsadcTriggerSelect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f59c6ccc`
- **参数名**: `DsadcTriggerSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TRIGGER_0_NO_DSADC_TRIG`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TRIGGER_0_NO_DSADC_TRIG` (来源: INFINEON_AURIX2G)
  - `TRIGGER_0_GTM_DSADC_TRIG0` (来源: INFINEON_AURIX2G)
  - `TRIGGER_1_GTM_DSADC_TRIG1` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT0` (来源: INFINEON_AURIX2G)
  - `TRIGGER_12_GTM_DSADC_TRIG2` (来源: INFINEON_AURIX2G)
  - `TRIGGER_13_GTM_DSADC_TRIG3` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT1` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT2` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT3` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT4` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines EDSADC channel trigger source.

########## 配置容器

本模块包含 **3** 个配置容器：

########### 1. DsadcOguConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-62fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOguConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

############ 参数配置

此容器包含 **8** 个参数：

############# BOOLEAN 类型参数

############## 1. DsadcEruErsCh0PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f20c6ccc`
- **参数名**: `DsadcEruErsCh0PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 0 is used for pattern detection for the selected OGU channel

############## 2. DsadcEruErsCh1PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-14e9f55c6ccc`
- **参数名**: `DsadcEruErsCh1PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 1 is used for pattern detection for the selected OGU channel

############## 3. DsadcEruErsCh2PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f21c6ccc`
- **参数名**: `DsadcEruErsCh2PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 2 is used for pattern detection for the selected OGU channel

############## 4. DsadcEruErsCh3PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f22c6ccc`
- **参数名**: `DsadcEruErsCh3PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 3 is used for pattern detection for the selected OGU channel

############## 5. DsadcEruErsCh4PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f23c6ccc`
- **参数名**: `DsadcEruErsCh4PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 4 is used for pattern detection for the selected OGU channel

############## 6. DsadcEruErsCh5PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f24c6ccc`
- **参数名**: `DsadcEruErsCh5PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 5 is used for pattern detection for the selected OGU channel

############## 7. DsadcEruErsCh6PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f25c6ccc`
- **参数名**: `DsadcEruErsCh6PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 6 is used for pattern detection for the selected OGU channel

############## 8. DsadcEruErsCh7PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f26c6ccc`
- **参数名**: `DsadcEruErsCh7PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 7 is used for pattern detection for the selected OGU channel

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. DsadcEruOguRef

- **UUID**: `66c8e900-6193-42a3-8125-a69abc21788e`
- **引用名**: `DsadcEruOguRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the DsadcHwChannelNum.

########### 2. DsadcTimestampConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6beea59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcTimestampConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters regarding the timestamp counter configuration.

############ 参数配置

此容器包含 **3** 个参数：

############# BOOLEAN 类型参数

############## 1. DsadcInputMuxSetCopyEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2cc6ccc`
- **参数名**: `DsadcInputMuxSetCopyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Analog MUX setting in the timestamp information.

############# ENUMERATION 类型参数

############## 1. DsadcTimestampCounterClockSel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2bc6ccc`
- **参数名**: `DsadcTimestampCounterClockSel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CLOCKDIVIDER_DIV1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CLOCKDIVIDER_DIV1` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV2` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the clock used for Timestamp counter.

############## 2. DsadcTimestampTriggerMode

- **UUID**: `6032d283-4ae2-4cf7-a415-2619568f6d10`
- **参数名**: `DsadcTimestampTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TIMESTAMP_WINDOWOPEN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TIMESTAMP_WINDOWOPEN` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_WINDOWCLOSE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define whether the timestamp has to be captured for window open event or window close event.

########### 3. DsadcIntegratorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6bbcd59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcIntegratorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to the Integrator functional block.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DsadcDiscardCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f30c6ccc`
- **参数名**: `DsadcDiscardCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be discarded before the start of the integration cycle.

############## 2. DsadcIntegrationCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f32c6ccc`
- **参数名**: `DsadcIntegrationCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [2..64]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be integrated.

######### 3. DsadcOguConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-62fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOguConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

########## 参数配置

此容器包含 **8** 个参数：

########### BOOLEAN 类型参数

############ 1. DsadcEruErsCh0PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f20c6ccc`
- **参数名**: `DsadcEruErsCh0PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 0 is used for pattern detection for the selected OGU channel

############ 2. DsadcEruErsCh1PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-14e9f55c6ccc`
- **参数名**: `DsadcEruErsCh1PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 1 is used for pattern detection for the selected OGU channel

############ 3. DsadcEruErsCh2PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f21c6ccc`
- **参数名**: `DsadcEruErsCh2PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 2 is used for pattern detection for the selected OGU channel

############ 4. DsadcEruErsCh3PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f22c6ccc`
- **参数名**: `DsadcEruErsCh3PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 3 is used for pattern detection for the selected OGU channel

############ 5. DsadcEruErsCh4PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f23c6ccc`
- **参数名**: `DsadcEruErsCh4PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 4 is used for pattern detection for the selected OGU channel

############ 6. DsadcEruErsCh5PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f24c6ccc`
- **参数名**: `DsadcEruErsCh5PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 5 is used for pattern detection for the selected OGU channel

############ 7. DsadcEruErsCh6PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f25c6ccc`
- **参数名**: `DsadcEruErsCh6PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 6 is used for pattern detection for the selected OGU channel

############ 8. DsadcEruErsCh7PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f26c6ccc`
- **参数名**: `DsadcEruErsCh7PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 7 is used for pattern detection for the selected OGU channel

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. DsadcEruOguRef

- **UUID**: `66c8e900-6193-42a3-8125-a69abc21788e`
- **引用名**: `DsadcEruOguRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the DsadcHwChannelNum.

######### 4. DsadcTimestampConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6beea59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcTimestampConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters regarding the timestamp counter configuration.

########## 参数配置

此容器包含 **3** 个参数：

########### BOOLEAN 类型参数

############ 1. DsadcInputMuxSetCopyEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2cc6ccc`
- **参数名**: `DsadcInputMuxSetCopyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Analog MUX setting in the timestamp information.

########### ENUMERATION 类型参数

############ 1. DsadcTimestampCounterClockSel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2bc6ccc`
- **参数名**: `DsadcTimestampCounterClockSel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CLOCKDIVIDER_DIV1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CLOCKDIVIDER_DIV1` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV2` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the clock used for Timestamp counter.

############ 2. DsadcTimestampTriggerMode

- **UUID**: `6032d283-4ae2-4cf7-a415-2619568f6d10`
- **参数名**: `DsadcTimestampTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TIMESTAMP_WINDOWOPEN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TIMESTAMP_WINDOWOPEN` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_WINDOWCLOSE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define whether the timestamp has to be captured for window open event or window close event.

######### 5. DsadcIntegratorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6bbcd59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcIntegratorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to the Integrator functional block.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DsadcDiscardCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f30c6ccc`
- **参数名**: `DsadcDiscardCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be discarded before the start of the integration cycle.

############ 2. DsadcIntegrationCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f32c6ccc`
- **参数名**: `DsadcIntegrationCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [2..64]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be integrated.

######### 6. DsadcRectificationConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10c59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcRectificationConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters of the rectifier block, used for resolver support, to determine position of the motor.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. DsadcPosSignDelayValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3bc6ccc`
- **参数名**: `DsadcPosSignDelayValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the value of Sign Delay counter (number of result values), for which to generate a positive delayed sign signal.

############ 2. DsadcNegSignDelayValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3cc6ccc`
- **参数名**: `DsadcNegSignDelayValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the value of Sign Delay counter (number of result values), for which to generate a negative delayed sign signal.

########### BOOLEAN 类型参数

############ 1. DsadcRectificationEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f38c6ccc`
- **参数名**: `DsadcRectificationEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter controls the action of the rectifier circuit on the input data.

########### ENUMERATION 类型参数

############ 1. DsadcSignSignalSource

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f39c6ccc`
- **参数名**: `DsadcSignSignalSource`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SRC_0_ON_CHIP_CARRIER_GENERATOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SRC_0_ON_CHIP_CARRIER_GENERATOR` (来源: INFINEON_AURIX2G)
  - `SRC_1_SIGNRESULT_FROM_DSADC_CHANNEL` (来源: INFINEON_AURIX2G)
  - `SRC_2_EXTERNAL_SIGN_SIGNAL_PORT00_4` (来源: INFINEON_AURIX2G)
  - `SRC_3_EXTERNAL_SIGN_SIGNAL_PORT33_13` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the source of the sign signal, which is to be delayed for the purpose of rectification.

############ 2. DsadcSignSignalChannel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3ac6ccc`
- **参数名**: `DsadcSignSignalChannel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CHANNEL_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CHANNEL_0` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_1` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_2` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_3` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_4` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the DSADC channel which provides the source of the sign signal, which is to be delayed for the purpose of rectification.

######### 7. DsadcCommonModeVoltConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b1ab59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCommonModeVoltConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to common mode voltage application to the inputs of the modulator channel.

########## 参数配置

此容器包含 **10** 个参数：

########### BOOLEAN 类型参数

############ 1. DsadcCommonModeVoltageEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f40c6ccc`
- **参数名**: `DsadcCommonModeVoltageEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Common Mode voltage to the input pins.

############ 2. DsadcComModeVoltPosAEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f43c6ccc`
- **参数名**: `DsadcComModeVoltPosAEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position A in the MUX needs to be connected to the Common Mode Voltage.

############ 3. DsadcComModeVoltPosBEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f45c6ccc`
- **参数名**: `DsadcComModeVoltPosBEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position B in the MUX needs to be connected to the Common Mode Voltage.

############ 4. DsadcComModeVoltPosCEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f47c6ccc`
- **参数名**: `DsadcComModeVoltPosCEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position C in the MUX needs to be connected to the Common Mode Voltage.

############ 5. DsadcComModeVoltPosDEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f49c6ccc`
- **参数名**: `DsadcComModeVoltPosDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position D in the MUX needs to be connected to the Common Mode Voltage.

############ 6. DsadcComModeVoltNegAEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f4cc6ccc`
- **参数名**: `DsadcComModeVoltNegAEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position A in the MUX needs to be connected to the Common Mode Voltage.

############ 7. DsadcComModeVoltNegBEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f4ec6ccc`
- **参数名**: `DsadcComModeVoltNegBEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position B in the MUX needs to be connected to the Common Mode Voltage.

############ 8. DsadcComModeVoltNegCEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9415c6ccc`
- **参数名**: `DsadcComModeVoltNegCEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position C in the MUX needs to be connected to the Common Mode Voltage.

############ 9. DsadcComModeVoltNegDEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9435c6ccc`
- **参数名**: `DsadcComModeVoltNegDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position D in the MUX needs to be connected to the Common Mode Voltage.

########### ENUMERATION 类型参数

############ 1. DsadcCommonModeVoltageSelect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f41c6ccc`
- **参数名**: `DsadcCommonModeVoltageSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_VCM_VREFX_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_VCM_VREFX_2` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_4` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_8` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the voltage level configured as Common Mode voltage, which can be connected to the input pins.

######### 8. DsadcFilterConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b13459e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcFilterConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to main filter chain.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. DsadcCICFilterDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f64c6ccc`
- **参数名**: `DsadcCICFilterDecimationFactor`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [4..512]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the oversampling rate/Decimation factor for the CIC filter.

############ 2. DsadcCICFilterStartValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f66c6ccc`
- **参数名**: `DsadcCICFilterStartValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [4..512]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the starting value of decimation counter, when the CIC filter is started/restarted.

############ 3. DsadcOffsetCompValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f6bc6ccc`
- **参数名**: `DsadcOffsetCompValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the offset component value to be removed(subtracted) from each result from the filter chain.

########### BOOLEAN 类型参数

############ 1. DsadcFIR0FilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f60c6ccc`
- **参数名**: `DsadcFIR0FilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of FIR0 filter in the filter chain of the DSADC channel.

############ 2. DsadcFIR1FilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f61c6ccc`
- **参数名**: `DsadcFIR1FilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of FIR1 filter in the filter chain of the DSADC channel.

############ 3. DsadcFIR1FilterDecimationEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f62c6ccc`
- **参数名**: `DsadcFIR1FilterDecimationEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the decimation rate of FIR1 filter.If selected as TRUE, then the filter decimates with a ratio 2:1

############ 4. DsadcPreFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f63c6ccc`
- **参数名**: `DsadcPreFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Prefilter in the filter chain of the DSADC channel

############ 5. DsadcOvershootCompensationEn

- **UUID**: `dea982da-0cb2-4bda-8324-e6e21fb90b04`
- **参数名**: `DsadcOvershootCompensationEn`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Overshoot compensation block in the filter chain of the DSADC channel.

############ 6. DsadcOffsetCompValueProtect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f6ac6ccc`
- **参数名**: `DsadcOffsetCompValueProtect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the protection of the Offset Compensation register from the calibration algorithm.

########### ENUMERATION 类型参数

############ 1. DsadcAlternateServiceReq

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f68c6ccc`
- **参数名**: `DsadcAlternateServiceReq`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_ALT_SERVICE_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_ALT_SERVICE_DISABLE` (来源: INFINEON_AURIX2G)
  - `DSADC_COMPARATOR_EVENT` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_EVENT` (来源: INFINEON_AURIX2G)
  - `DSADC_RESOLVER_EVENT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to generate alternate service request for any one of the following events, comparator event, time stamp event or alternate source.

############ 2. DsadcOffsetCompFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f69c6ccc`
- **参数名**: `DsadcOffsetCompFilterEnable`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_OFFCOMP_FILTER_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_OFFCOMP_FILTER_DISABLE` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_1` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_2` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_3` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_4` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_5` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_6` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter indicates availability of an Offset Compensation (IIR) filter (and its various operation modes) in Offset Compensation block.

########## 配置容器

本模块包含 **6** 个配置容器：

########### 1. DsadcAuxFilterConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10abcd2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcAuxFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This configuration container provides parameters related to Dsadc Auxiliary Filter configuration..

############ 参数配置

此容器包含 **2** 个参数：

############# BOOLEAN 类型参数

############## 1. DsadcAuxCicFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f82c6ccc`
- **参数名**: `DsadcAuxCicFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Dsadc Auxiliary filter.

############# ENUMERATION 类型参数

############## 1. DsadcAuxFilterCicDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f81c6ccc`
- **参数名**: `DsadcAuxFilterCicDecimationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_AUXCIC_OSR_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_AUXCIC_OSR_16` (来源: INFINEON_AURIX2G)
  - `DSADC_AUXCIC_OSR_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the over sampling rate/decimation factor for the Auxiliary CIC filter.

########### 2. DsadcGainCalibConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a5abcccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCalibConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain calibration.

############ 配置容器

本模块包含 **2** 个配置容器：

############# 1. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

############## 参数配置

此容器包含 **2** 个参数：

############### FLOAT 类型参数

################ 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

############### ENUMERATION 类型参数

################ 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

############# 2. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

############## 参数配置

此容器包含 **5** 个参数：

############### INTEGER 类型参数

################ 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

############### FLOAT 类型参数

################ 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

################ 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

############### ENUMERATION 类型参数

################ 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

################ 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

########### 3. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

############ 参数配置

此容器包含 **2** 个参数：

############# FLOAT 类型参数

############## 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

############# ENUMERATION 类型参数

############## 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

########### 4. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

############# FLOAT 类型参数

############## 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

############## 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

############# ENUMERATION 类型参数

############## 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

############## 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

########### 5. DsadcComparatorConfiguration

**容器属性**:

- **UUID**: `e2ada5c3-12ab-4571-b5ee-759cd5434db0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcComparatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for comparator configuration.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. DsadcLowerBoundaryValue

- **UUID**: `f807a909-ab39-4628-8111-68665be76339`
- **参数名**: `DsadcLowerBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the lower boundary used for limit checking.

############## 2. DsadcUpperBoundaryValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f80c6ccc`
- **参数名**: `DsadcUpperBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the upper boundary used for limit checking.

############# ENUMERATION 类型参数

############## 1. DsadcComparatorEventSelect

- **UUID**: `ff120d55-9be8-48c1-ac48-4e1270732d0f`
- **参数名**: `DsadcComparatorEventSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RESULT_ALWAYS`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RESULT_ALWAYS` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_INSIDE_RANGE` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_OUTSIDE_RANGE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the comparator mode selected to generate an alarm event (and also a service request, if selected auxiliary service request generation).

########### 6. DsadcOvershootCompenConfig

**容器属性**:

- **UUID**: `7fd025de-907b-4268-b461-e379b30f3bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOvershootCompenConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU input triggering

############ 参数配置

此容器包含 **4** 个参数：

############# INTEGER 类型参数

############## 1. DsadcStepDetectionThreshold

- **UUID**: `c0af7dc5-4445-4b46-8ec3-e2194a3e68ae`
- **参数名**: `DsadcStepDetectionThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..2047]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the threshold value (magnitude) used for step detection. The threshold value is DsadcStepDetectionThreshold * 32

############# ENUMERATION 类型参数

############## 1. DsadcStepDetectionMode

- **UUID**: `f3cc0efc-5fb1-4a43-a04d-0cac5d6c6682`
- **参数名**: `DsadcStepDetectionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_STEP_DETECT_CMP_LAST`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_STEP_DETECT_CMP_LAST` (来源: INFINEON_AURIX2G)
  - `DSADC_STEP_DETECT_CMP_SEC_LAST` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the when the slew rate filter has to be activated

############## 2. DsadcSlewRateFilterStrength

- **UUID**: `67ad9852-f061-486d-b362-7bc53c40d431`
- **参数名**: `DsadcSlewRateFilterStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_MINIMUM_FILTER_EFFECT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_MINIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_WEAK_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MEDIUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MAXIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the filter strength for the slew rate filter

############## 3. DsadcSlewRateFilterRunTime

- **UUID**: `a3c267ec-3099-4508-925c-09650a25f4bc`
- **参数名**: `DsadcSlewRateFilterRunTime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_SLEWRATE_FILTR_RUNTIME_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_SLEWRATE_FILTR_RUNTIME_2` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_4` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_8` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the time constant for the slew rate filter

######### 9. DsadcAuxFilterConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10abcd2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcAuxFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This configuration container provides parameters related to Dsadc Auxiliary Filter configuration..

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. DsadcAuxCicFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f82c6ccc`
- **参数名**: `DsadcAuxCicFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Dsadc Auxiliary filter.

########### ENUMERATION 类型参数

############ 1. DsadcAuxFilterCicDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f81c6ccc`
- **参数名**: `DsadcAuxFilterCicDecimationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_AUXCIC_OSR_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_AUXCIC_OSR_16` (来源: INFINEON_AURIX2G)
  - `DSADC_AUXCIC_OSR_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the over sampling rate/decimation factor for the Auxiliary CIC filter.

######### 10. DsadcGainCalibConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a5abcccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCalibConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain calibration.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

############ 参数配置

此容器包含 **2** 个参数：

############# FLOAT 类型参数

############## 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

############# ENUMERATION 类型参数

############## 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

########### 2. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

############# FLOAT 类型参数

############## 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

############## 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

############# ENUMERATION 类型参数

############## 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

############## 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

######### 11. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

########## 参数配置

此容器包含 **2** 个参数：

########### FLOAT 类型参数

############ 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

########### ENUMERATION 类型参数

############ 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

######### 12. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

########### FLOAT 类型参数

############ 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

############ 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

########### ENUMERATION 类型参数

############ 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

############ 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

######### 13. DsadcComparatorConfiguration

**容器属性**:

- **UUID**: `e2ada5c3-12ab-4571-b5ee-759cd5434db0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcComparatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for comparator configuration.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DsadcLowerBoundaryValue

- **UUID**: `f807a909-ab39-4628-8111-68665be76339`
- **参数名**: `DsadcLowerBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the lower boundary used for limit checking.

############ 2. DsadcUpperBoundaryValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f80c6ccc`
- **参数名**: `DsadcUpperBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the upper boundary used for limit checking.

########### ENUMERATION 类型参数

############ 1. DsadcComparatorEventSelect

- **UUID**: `ff120d55-9be8-48c1-ac48-4e1270732d0f`
- **参数名**: `DsadcComparatorEventSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RESULT_ALWAYS`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RESULT_ALWAYS` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_INSIDE_RANGE` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_OUTSIDE_RANGE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the comparator mode selected to generate an alarm event (and also a service request, if selected auxiliary service request generation).

######### 14. DsadcOvershootCompenConfig

**容器属性**:

- **UUID**: `7fd025de-907b-4268-b461-e379b30f3bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOvershootCompenConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU input triggering

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. DsadcStepDetectionThreshold

- **UUID**: `c0af7dc5-4445-4b46-8ec3-e2194a3e68ae`
- **参数名**: `DsadcStepDetectionThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..2047]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the threshold value (magnitude) used for step detection. The threshold value is DsadcStepDetectionThreshold * 32

########### ENUMERATION 类型参数

############ 1. DsadcStepDetectionMode

- **UUID**: `f3cc0efc-5fb1-4a43-a04d-0cac5d6c6682`
- **参数名**: `DsadcStepDetectionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_STEP_DETECT_CMP_LAST`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_STEP_DETECT_CMP_LAST` (来源: INFINEON_AURIX2G)
  - `DSADC_STEP_DETECT_CMP_SEC_LAST` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the when the slew rate filter has to be activated

############ 2. DsadcSlewRateFilterStrength

- **UUID**: `67ad9852-f061-486d-b362-7bc53c40d431`
- **参数名**: `DsadcSlewRateFilterStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_MINIMUM_FILTER_EFFECT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_MINIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_WEAK_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MEDIUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MAXIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the filter strength for the slew rate filter

############ 3. DsadcSlewRateFilterRunTime

- **UUID**: `a3c267ec-3099-4508-925c-09650a25f4bc`
- **参数名**: `DsadcSlewRateFilterRunTime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_SLEWRATE_FILTR_RUNTIME_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_SLEWRATE_FILTR_RUNTIME_2` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_4` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_8` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the time constant for the slew rate filter

####### 5. DsadcModulatorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6010059e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcModulatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains configuration parameters related to the On-chip modulator, input pin selection and modulator clock configuration.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. DsadcAnalogClockSyncDelay

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-44e9f55c6ccc`
- **参数名**: `DsadcAnalogClockSyncDelay`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the delay in clock cycles after the sync signal provided from Phase synchronizer.

######### BOOLEAN 类型参数

########## 1. DsadcDitheringEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e3f55c6ccc`
- **参数名**: `DsadcDitheringEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of internal dithering functionality for the modulator.

########## 2. DsadcIntegratorResetEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e7f55c6ccc`
- **参数名**: `DsadcIntegratorResetEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the modulator overload handling.

######### ENUMERATION 类型参数

########## 1. DsadcClockDivider

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e2f55c6ccc`
- **参数名**: `DsadcClockDivider`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CLOCKDIVIDER_DIV4`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV6` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV10` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV12` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV14` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV16` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV18` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the frequency of the modulator clock, which is derived from the peripheral clock

########## 2. DsadcInputGain

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-54e9f55c6ccc`
- **参数名**: `DsadcInputGain`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INPUT_GAIN_FACTOR_1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INPUT_GAIN_FACTOR_1` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUT_GAIN_FACTOR_2` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUT_GAIN_FACTOR_4` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines multiplication Gain factor for the analog input signal.

########## 3. DsadcInputMuxActionMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e4f55c6ccc`
- **参数名**: `DsadcInputMuxActionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INPUTMUX_PRESET_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INPUTMUX_PRESET_MODE` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUTMUX_SINGLE_STEP_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the control mechanism for input multiplexer. It defines the action to be taken for the input multiplexer upon a trigger event for pin selection.

########## 4. DsadcInputMuxControlMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e5f55c6ccc`
- **参数名**: `DsadcInputMuxControlMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INMUX_SOFTWARE_CONTROL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INMUX_SOFTWARE_CONTROL` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_FALLING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_RISING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_BOTH_EDGES` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the condition for a trigger event to control the input multiplexer.

########## 5. DsadcInputPinSelection

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e6f55c6ccc`
- **参数名**: `DsadcInputPinSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_PIN_0_AN2_AN3`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_PIN_0_AN2_AN3` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN12_AN13` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN36_AN37` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN38_AN39` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_2_AN44_AN45` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_3_AN46_AN47` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN20_AN21` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN24_AN25` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN0_AN1` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN14_AN15` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_PORT_00_8_PORT_00_7` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_PORT_00_10_PORT_00_9` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_PORT_00_2_PORT_00_1` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_PORT_00_4_PORT_00_3` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the initial/permanent setting for the input multiplexer, based on the operating mode selected.

########## 6. DsadcNegativeInputLine

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-64e9f55c6ccc`
- **参数名**: `DsadcNegativeInputLine`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_NEG_INPUT_PIN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_NEG_INPUT_PIN` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_SUPPLY_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_COMMON_MODE_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_REFERENCE_GROUND` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the modulator internal connection of the negative input.

########## 7. DsadcPositiveInputLine

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e8f55c6ccc`
- **参数名**: `DsadcPositiveInputLine`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_POS_INPUT_PIN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_POS_INPUT_PIN` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_SUPPLY_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_COMMON_MODE_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_REFERENCE_GROUND` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the modulator internal connection of the positive input.

####### 6. DsadcDemodulatorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10259e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcDemodulatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains configuration parameters related to the de-modulator, input data stream and trigger selection.

######## 参数配置

此容器包含 **3** 个参数：

######### ENUMERATION 类型参数

########## 1. DsadcIntegratorTriggerMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f54c6ccc`
- **参数名**: `DsadcIntegratorTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INTR_BYPASSED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INTR_BYPASSED` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_FALLING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_RISING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_ALWAYS_ACTIVE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the Integrator trigger mode.

########## 2. DsadcResultDisplayMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f58c6ccc`
- **参数名**: `DsadcResultDisplayMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RES_SIGNED_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RES_SIGNED_MODE` (来源: INFINEON_AURIX2G)
  - `DSADC_RES_UNSIGNED_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the ranges of the result values i.e. result display modes.

########## 3. DsadcTriggerSelect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f59c6ccc`
- **参数名**: `DsadcTriggerSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TRIGGER_0_NO_DSADC_TRIG`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TRIGGER_0_NO_DSADC_TRIG` (来源: INFINEON_AURIX2G)
  - `TRIGGER_0_GTM_DSADC_TRIG0` (来源: INFINEON_AURIX2G)
  - `TRIGGER_1_GTM_DSADC_TRIG1` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT0` (来源: INFINEON_AURIX2G)
  - `TRIGGER_12_GTM_DSADC_TRIG2` (来源: INFINEON_AURIX2G)
  - `TRIGGER_13_GTM_DSADC_TRIG3` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT1` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT2` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT3` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT4` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines EDSADC channel trigger source.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. DsadcOguConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-62fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOguConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

########## 参数配置

此容器包含 **8** 个参数：

########### BOOLEAN 类型参数

############ 1. DsadcEruErsCh0PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f20c6ccc`
- **参数名**: `DsadcEruErsCh0PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 0 is used for pattern detection for the selected OGU channel

############ 2. DsadcEruErsCh1PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-14e9f55c6ccc`
- **参数名**: `DsadcEruErsCh1PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 1 is used for pattern detection for the selected OGU channel

############ 3. DsadcEruErsCh2PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f21c6ccc`
- **参数名**: `DsadcEruErsCh2PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 2 is used for pattern detection for the selected OGU channel

############ 4. DsadcEruErsCh3PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f22c6ccc`
- **参数名**: `DsadcEruErsCh3PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 3 is used for pattern detection for the selected OGU channel

############ 5. DsadcEruErsCh4PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f23c6ccc`
- **参数名**: `DsadcEruErsCh4PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 4 is used for pattern detection for the selected OGU channel

############ 6. DsadcEruErsCh5PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f24c6ccc`
- **参数名**: `DsadcEruErsCh5PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 5 is used for pattern detection for the selected OGU channel

############ 7. DsadcEruErsCh6PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f25c6ccc`
- **参数名**: `DsadcEruErsCh6PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 6 is used for pattern detection for the selected OGU channel

############ 8. DsadcEruErsCh7PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f26c6ccc`
- **参数名**: `DsadcEruErsCh7PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 7 is used for pattern detection for the selected OGU channel

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. DsadcEruOguRef

- **UUID**: `66c8e900-6193-42a3-8125-a69abc21788e`
- **引用名**: `DsadcEruOguRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the DsadcHwChannelNum.

######### 2. DsadcTimestampConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6beea59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcTimestampConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters regarding the timestamp counter configuration.

########## 参数配置

此容器包含 **3** 个参数：

########### BOOLEAN 类型参数

############ 1. DsadcInputMuxSetCopyEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2cc6ccc`
- **参数名**: `DsadcInputMuxSetCopyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Analog MUX setting in the timestamp information.

########### ENUMERATION 类型参数

############ 1. DsadcTimestampCounterClockSel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2bc6ccc`
- **参数名**: `DsadcTimestampCounterClockSel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CLOCKDIVIDER_DIV1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CLOCKDIVIDER_DIV1` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV2` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the clock used for Timestamp counter.

############ 2. DsadcTimestampTriggerMode

- **UUID**: `6032d283-4ae2-4cf7-a415-2619568f6d10`
- **参数名**: `DsadcTimestampTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TIMESTAMP_WINDOWOPEN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TIMESTAMP_WINDOWOPEN` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_WINDOWCLOSE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define whether the timestamp has to be captured for window open event or window close event.

######### 3. DsadcIntegratorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6bbcd59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcIntegratorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to the Integrator functional block.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DsadcDiscardCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f30c6ccc`
- **参数名**: `DsadcDiscardCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be discarded before the start of the integration cycle.

############ 2. DsadcIntegrationCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f32c6ccc`
- **参数名**: `DsadcIntegrationCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [2..64]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be integrated.

####### 7. DsadcOguConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-62fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOguConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

######## 参数配置

此容器包含 **8** 个参数：

######### BOOLEAN 类型参数

########## 1. DsadcEruErsCh0PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f20c6ccc`
- **参数名**: `DsadcEruErsCh0PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 0 is used for pattern detection for the selected OGU channel

########## 2. DsadcEruErsCh1PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-14e9f55c6ccc`
- **参数名**: `DsadcEruErsCh1PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 1 is used for pattern detection for the selected OGU channel

########## 3. DsadcEruErsCh2PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f21c6ccc`
- **参数名**: `DsadcEruErsCh2PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 2 is used for pattern detection for the selected OGU channel

########## 4. DsadcEruErsCh3PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f22c6ccc`
- **参数名**: `DsadcEruErsCh3PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 3 is used for pattern detection for the selected OGU channel

########## 5. DsadcEruErsCh4PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f23c6ccc`
- **参数名**: `DsadcEruErsCh4PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 4 is used for pattern detection for the selected OGU channel

########## 6. DsadcEruErsCh5PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f24c6ccc`
- **参数名**: `DsadcEruErsCh5PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 5 is used for pattern detection for the selected OGU channel

########## 7. DsadcEruErsCh6PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f25c6ccc`
- **参数名**: `DsadcEruErsCh6PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 6 is used for pattern detection for the selected OGU channel

########## 8. DsadcEruErsCh7PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f26c6ccc`
- **参数名**: `DsadcEruErsCh7PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 7 is used for pattern detection for the selected OGU channel

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DsadcEruOguRef

- **UUID**: `66c8e900-6193-42a3-8125-a69abc21788e`
- **引用名**: `DsadcEruOguRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the DsadcHwChannelNum.

####### 8. DsadcTimestampConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6beea59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcTimestampConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters regarding the timestamp counter configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. DsadcInputMuxSetCopyEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2cc6ccc`
- **参数名**: `DsadcInputMuxSetCopyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Analog MUX setting in the timestamp information.

######### ENUMERATION 类型参数

########## 1. DsadcTimestampCounterClockSel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2bc6ccc`
- **参数名**: `DsadcTimestampCounterClockSel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CLOCKDIVIDER_DIV1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CLOCKDIVIDER_DIV1` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV2` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the clock used for Timestamp counter.

########## 2. DsadcTimestampTriggerMode

- **UUID**: `6032d283-4ae2-4cf7-a415-2619568f6d10`
- **参数名**: `DsadcTimestampTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TIMESTAMP_WINDOWOPEN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TIMESTAMP_WINDOWOPEN` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_WINDOWCLOSE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define whether the timestamp has to be captured for window open event or window close event.

####### 9. DsadcIntegratorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6bbcd59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcIntegratorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to the Integrator functional block.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DsadcDiscardCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f30c6ccc`
- **参数名**: `DsadcDiscardCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be discarded before the start of the integration cycle.

########## 2. DsadcIntegrationCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f32c6ccc`
- **参数名**: `DsadcIntegrationCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [2..64]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be integrated.

####### 10. DsadcRectificationConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10c59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcRectificationConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters of the rectifier block, used for resolver support, to determine position of the motor.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. DsadcPosSignDelayValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3bc6ccc`
- **参数名**: `DsadcPosSignDelayValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the value of Sign Delay counter (number of result values), for which to generate a positive delayed sign signal.

########## 2. DsadcNegSignDelayValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3cc6ccc`
- **参数名**: `DsadcNegSignDelayValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the value of Sign Delay counter (number of result values), for which to generate a negative delayed sign signal.

######### BOOLEAN 类型参数

########## 1. DsadcRectificationEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f38c6ccc`
- **参数名**: `DsadcRectificationEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter controls the action of the rectifier circuit on the input data.

######### ENUMERATION 类型参数

########## 1. DsadcSignSignalSource

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f39c6ccc`
- **参数名**: `DsadcSignSignalSource`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SRC_0_ON_CHIP_CARRIER_GENERATOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SRC_0_ON_CHIP_CARRIER_GENERATOR` (来源: INFINEON_AURIX2G)
  - `SRC_1_SIGNRESULT_FROM_DSADC_CHANNEL` (来源: INFINEON_AURIX2G)
  - `SRC_2_EXTERNAL_SIGN_SIGNAL_PORT00_4` (来源: INFINEON_AURIX2G)
  - `SRC_3_EXTERNAL_SIGN_SIGNAL_PORT33_13` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the source of the sign signal, which is to be delayed for the purpose of rectification.

########## 2. DsadcSignSignalChannel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3ac6ccc`
- **参数名**: `DsadcSignSignalChannel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CHANNEL_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CHANNEL_0` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_1` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_2` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_3` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_4` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the DSADC channel which provides the source of the sign signal, which is to be delayed for the purpose of rectification.

####### 11. DsadcCommonModeVoltConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b1ab59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCommonModeVoltConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to common mode voltage application to the inputs of the modulator channel.

######## 参数配置

此容器包含 **10** 个参数：

######### BOOLEAN 类型参数

########## 1. DsadcCommonModeVoltageEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f40c6ccc`
- **参数名**: `DsadcCommonModeVoltageEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Common Mode voltage to the input pins.

########## 2. DsadcComModeVoltPosAEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f43c6ccc`
- **参数名**: `DsadcComModeVoltPosAEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position A in the MUX needs to be connected to the Common Mode Voltage.

########## 3. DsadcComModeVoltPosBEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f45c6ccc`
- **参数名**: `DsadcComModeVoltPosBEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position B in the MUX needs to be connected to the Common Mode Voltage.

########## 4. DsadcComModeVoltPosCEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f47c6ccc`
- **参数名**: `DsadcComModeVoltPosCEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position C in the MUX needs to be connected to the Common Mode Voltage.

########## 5. DsadcComModeVoltPosDEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f49c6ccc`
- **参数名**: `DsadcComModeVoltPosDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position D in the MUX needs to be connected to the Common Mode Voltage.

########## 6. DsadcComModeVoltNegAEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f4cc6ccc`
- **参数名**: `DsadcComModeVoltNegAEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position A in the MUX needs to be connected to the Common Mode Voltage.

########## 7. DsadcComModeVoltNegBEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f4ec6ccc`
- **参数名**: `DsadcComModeVoltNegBEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position B in the MUX needs to be connected to the Common Mode Voltage.

########## 8. DsadcComModeVoltNegCEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9415c6ccc`
- **参数名**: `DsadcComModeVoltNegCEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position C in the MUX needs to be connected to the Common Mode Voltage.

########## 9. DsadcComModeVoltNegDEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9435c6ccc`
- **参数名**: `DsadcComModeVoltNegDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position D in the MUX needs to be connected to the Common Mode Voltage.

######### ENUMERATION 类型参数

########## 1. DsadcCommonModeVoltageSelect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f41c6ccc`
- **参数名**: `DsadcCommonModeVoltageSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_VCM_VREFX_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_VCM_VREFX_2` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_4` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_8` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the voltage level configured as Common Mode voltage, which can be connected to the input pins.

####### 12. DsadcFilterConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b13459e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcFilterConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to main filter chain.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. DsadcCICFilterDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f64c6ccc`
- **参数名**: `DsadcCICFilterDecimationFactor`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [4..512]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the oversampling rate/Decimation factor for the CIC filter.

########## 2. DsadcCICFilterStartValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f66c6ccc`
- **参数名**: `DsadcCICFilterStartValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [4..512]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the starting value of decimation counter, when the CIC filter is started/restarted.

########## 3. DsadcOffsetCompValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f6bc6ccc`
- **参数名**: `DsadcOffsetCompValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the offset component value to be removed(subtracted) from each result from the filter chain.

######### BOOLEAN 类型参数

########## 1. DsadcFIR0FilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f60c6ccc`
- **参数名**: `DsadcFIR0FilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of FIR0 filter in the filter chain of the DSADC channel.

########## 2. DsadcFIR1FilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f61c6ccc`
- **参数名**: `DsadcFIR1FilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of FIR1 filter in the filter chain of the DSADC channel.

########## 3. DsadcFIR1FilterDecimationEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f62c6ccc`
- **参数名**: `DsadcFIR1FilterDecimationEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the decimation rate of FIR1 filter.If selected as TRUE, then the filter decimates with a ratio 2:1

########## 4. DsadcPreFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f63c6ccc`
- **参数名**: `DsadcPreFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Prefilter in the filter chain of the DSADC channel

########## 5. DsadcOvershootCompensationEn

- **UUID**: `dea982da-0cb2-4bda-8324-e6e21fb90b04`
- **参数名**: `DsadcOvershootCompensationEn`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Overshoot compensation block in the filter chain of the DSADC channel.

########## 6. DsadcOffsetCompValueProtect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f6ac6ccc`
- **参数名**: `DsadcOffsetCompValueProtect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the protection of the Offset Compensation register from the calibration algorithm.

######### ENUMERATION 类型参数

########## 1. DsadcAlternateServiceReq

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f68c6ccc`
- **参数名**: `DsadcAlternateServiceReq`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_ALT_SERVICE_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_ALT_SERVICE_DISABLE` (来源: INFINEON_AURIX2G)
  - `DSADC_COMPARATOR_EVENT` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_EVENT` (来源: INFINEON_AURIX2G)
  - `DSADC_RESOLVER_EVENT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to generate alternate service request for any one of the following events, comparator event, time stamp event or alternate source.

########## 2. DsadcOffsetCompFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f69c6ccc`
- **参数名**: `DsadcOffsetCompFilterEnable`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_OFFCOMP_FILTER_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_OFFCOMP_FILTER_DISABLE` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_1` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_2` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_3` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_4` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_5` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_6` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter indicates availability of an Offset Compensation (IIR) filter (and its various operation modes) in Offset Compensation block.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. DsadcAuxFilterConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10abcd2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcAuxFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This configuration container provides parameters related to Dsadc Auxiliary Filter configuration..

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. DsadcAuxCicFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f82c6ccc`
- **参数名**: `DsadcAuxCicFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Dsadc Auxiliary filter.

########### ENUMERATION 类型参数

############ 1. DsadcAuxFilterCicDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f81c6ccc`
- **参数名**: `DsadcAuxFilterCicDecimationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_AUXCIC_OSR_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_AUXCIC_OSR_16` (来源: INFINEON_AURIX2G)
  - `DSADC_AUXCIC_OSR_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the over sampling rate/decimation factor for the Auxiliary CIC filter.

######### 2. DsadcGainCalibConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a5abcccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCalibConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain calibration.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

############ 参数配置

此容器包含 **2** 个参数：

############# FLOAT 类型参数

############## 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

############# ENUMERATION 类型参数

############## 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

########### 2. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

############# FLOAT 类型参数

############## 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

############## 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

############# ENUMERATION 类型参数

############## 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

############## 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

######### 3. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

########## 参数配置

此容器包含 **2** 个参数：

########### FLOAT 类型参数

############ 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

########### ENUMERATION 类型参数

############ 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

######### 4. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

########### FLOAT 类型参数

############ 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

############ 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

########### ENUMERATION 类型参数

############ 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

############ 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

######### 5. DsadcComparatorConfiguration

**容器属性**:

- **UUID**: `e2ada5c3-12ab-4571-b5ee-759cd5434db0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcComparatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for comparator configuration.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DsadcLowerBoundaryValue

- **UUID**: `f807a909-ab39-4628-8111-68665be76339`
- **参数名**: `DsadcLowerBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the lower boundary used for limit checking.

############ 2. DsadcUpperBoundaryValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f80c6ccc`
- **参数名**: `DsadcUpperBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the upper boundary used for limit checking.

########### ENUMERATION 类型参数

############ 1. DsadcComparatorEventSelect

- **UUID**: `ff120d55-9be8-48c1-ac48-4e1270732d0f`
- **参数名**: `DsadcComparatorEventSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RESULT_ALWAYS`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RESULT_ALWAYS` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_INSIDE_RANGE` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_OUTSIDE_RANGE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the comparator mode selected to generate an alarm event (and also a service request, if selected auxiliary service request generation).

######### 6. DsadcOvershootCompenConfig

**容器属性**:

- **UUID**: `7fd025de-907b-4268-b461-e379b30f3bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOvershootCompenConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU input triggering

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. DsadcStepDetectionThreshold

- **UUID**: `c0af7dc5-4445-4b46-8ec3-e2194a3e68ae`
- **参数名**: `DsadcStepDetectionThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..2047]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the threshold value (magnitude) used for step detection. The threshold value is DsadcStepDetectionThreshold * 32

########### ENUMERATION 类型参数

############ 1. DsadcStepDetectionMode

- **UUID**: `f3cc0efc-5fb1-4a43-a04d-0cac5d6c6682`
- **参数名**: `DsadcStepDetectionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_STEP_DETECT_CMP_LAST`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_STEP_DETECT_CMP_LAST` (来源: INFINEON_AURIX2G)
  - `DSADC_STEP_DETECT_CMP_SEC_LAST` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the when the slew rate filter has to be activated

############ 2. DsadcSlewRateFilterStrength

- **UUID**: `67ad9852-f061-486d-b362-7bc53c40d431`
- **参数名**: `DsadcSlewRateFilterStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_MINIMUM_FILTER_EFFECT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_MINIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_WEAK_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MEDIUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MAXIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the filter strength for the slew rate filter

############ 3. DsadcSlewRateFilterRunTime

- **UUID**: `a3c267ec-3099-4508-925c-09650a25f4bc`
- **参数名**: `DsadcSlewRateFilterRunTime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_SLEWRATE_FILTR_RUNTIME_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_SLEWRATE_FILTR_RUNTIME_2` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_4` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_8` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the time constant for the slew rate filter

####### 13. DsadcAuxFilterConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10abcd2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcAuxFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This configuration container provides parameters related to Dsadc Auxiliary Filter configuration..

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. DsadcAuxCicFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f82c6ccc`
- **参数名**: `DsadcAuxCicFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Dsadc Auxiliary filter.

######### ENUMERATION 类型参数

########## 1. DsadcAuxFilterCicDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f81c6ccc`
- **参数名**: `DsadcAuxFilterCicDecimationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_AUXCIC_OSR_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_AUXCIC_OSR_16` (来源: INFINEON_AURIX2G)
  - `DSADC_AUXCIC_OSR_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the over sampling rate/decimation factor for the Auxiliary CIC filter.

####### 14. DsadcGainCalibConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a5abcccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCalibConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain calibration.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

########## 参数配置

此容器包含 **2** 个参数：

########### FLOAT 类型参数

############ 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

########### ENUMERATION 类型参数

############ 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

######### 2. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

########### FLOAT 类型参数

############ 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

############ 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

########### ENUMERATION 类型参数

############ 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

############ 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

####### 15. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

######### ENUMERATION 类型参数

########## 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

####### 16. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

######### FLOAT 类型参数

########## 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

########## 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

######### ENUMERATION 类型参数

########## 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

########## 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

####### 17. DsadcComparatorConfiguration

**容器属性**:

- **UUID**: `e2ada5c3-12ab-4571-b5ee-759cd5434db0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcComparatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for comparator configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DsadcLowerBoundaryValue

- **UUID**: `f807a909-ab39-4628-8111-68665be76339`
- **参数名**: `DsadcLowerBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the lower boundary used for limit checking.

########## 2. DsadcUpperBoundaryValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f80c6ccc`
- **参数名**: `DsadcUpperBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the upper boundary used for limit checking.

######### ENUMERATION 类型参数

########## 1. DsadcComparatorEventSelect

- **UUID**: `ff120d55-9be8-48c1-ac48-4e1270732d0f`
- **参数名**: `DsadcComparatorEventSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RESULT_ALWAYS`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RESULT_ALWAYS` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_INSIDE_RANGE` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_OUTSIDE_RANGE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the comparator mode selected to generate an alarm event (and also a service request, if selected auxiliary service request generation).

####### 18. DsadcOvershootCompenConfig

**容器属性**:

- **UUID**: `7fd025de-907b-4268-b461-e379b30f3bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOvershootCompenConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU input triggering

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DsadcStepDetectionThreshold

- **UUID**: `c0af7dc5-4445-4b46-8ec3-e2194a3e68ae`
- **参数名**: `DsadcStepDetectionThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..2047]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the threshold value (magnitude) used for step detection. The threshold value is DsadcStepDetectionThreshold * 32

######### ENUMERATION 类型参数

########## 1. DsadcStepDetectionMode

- **UUID**: `f3cc0efc-5fb1-4a43-a04d-0cac5d6c6682`
- **参数名**: `DsadcStepDetectionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_STEP_DETECT_CMP_LAST`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_STEP_DETECT_CMP_LAST` (来源: INFINEON_AURIX2G)
  - `DSADC_STEP_DETECT_CMP_SEC_LAST` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the when the slew rate filter has to be activated

########## 2. DsadcSlewRateFilterStrength

- **UUID**: `67ad9852-f061-486d-b362-7bc53c40d431`
- **参数名**: `DsadcSlewRateFilterStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_MINIMUM_FILTER_EFFECT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_MINIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_WEAK_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MEDIUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MAXIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the filter strength for the slew rate filter

########## 3. DsadcSlewRateFilterRunTime

- **UUID**: `a3c267ec-3099-4508-925c-09650a25f4bc`
- **参数名**: `DsadcSlewRateFilterRunTime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_SLEWRATE_FILTR_RUNTIME_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_SLEWRATE_FILTR_RUNTIME_2` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_4` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_8` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the time constant for the slew rate filter

##### 5. DsadcGlobalConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGlobalConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the parameters to configure DSADC IP global configuration.

###### 参数配置

此容器包含 **4** 个参数：

####### ENUMERATION 类型参数

######## 1. DsadcDitheringTrimValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f55c6cc3`
- **参数名**: `DsadcDitheringTrimValue`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_DITHERING_MIN_50_MILVLT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_DITHERING_MIN_50_MILVLT` (来源: INFINEON_AURIX2G)
  - `DSADC_DITHERING_LOW_100_MILVLT` (来源: INFINEON_AURIX2G)
  - `DSADC_DITHERING_MED_200_MILVLT` (来源: INFINEON_AURIX2G)
  - `DSADC_DITHERING_HIGH_400_MILVLT` (来源: INFINEON_AURIX2G)
- **描述**: Defines trimming value for internal dithering function. This trimming value is used for all the modulators of DSADC

######## 2. DsadcSleepMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f55c6cc4`
- **参数名**: `DsadcSleepMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SLEEP_ENABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SLEEP_ENABLE` (来源: INFINEON_AURIX2G)
  - `SLEEP_DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: Parameter defines EDSADC reaction to the Sleep mode requests

######## 3. DsadcSupplyVoltageLevel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f55c6cc5`
- **参数名**: `DsadcSupplyVoltageLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `VOLTAGESUPPLY_AUTO`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `VOLTAGESUPPLY_AUTO` (来源: INFINEON_AURIX2G)
  - `VOLTAGESUPPLY_5V` (来源: INFINEON_AURIX2G)
  - `VOLTAGESUPPLY_3_3V` (来源: INFINEON_AURIX2G)
- **描述**: Parameter defines the supply voltage level to be used for DSADC internal operations

######## 4. DsadcSyncClockGen

- **UUID**: `DCE:d6ea9dd9-1d6e-4d4b-b3a3-23e9455c6ccc`
- **参数名**: `DsadcSyncClockGen`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `UNSYNCHRONIZED_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SYNCHRONIZED_MODE` (来源: INFINEON_AURIX2G)
  - `UNSYNCHRONIZED_MODE` (来源: INFINEON_AURIX2G)
- **描述**: Parameter defines the influence of Analog Phase synchronizer on the clock generated

##### 6. DsadcCarrierGeneratorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a5cccccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCarrierGeneratorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the Carrier Generation related Parameters.

###### 参数配置

此容器包含 **4** 个参数：

####### ENUMERATION 类型参数

######## 1. DsadcPwmGenerationMode

- **UUID**: `d4aec598-5cc7-4487-9530-36ee9e854cc6`
- **参数名**: `DsadcPwmGenerationMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_NORMAL_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_NORMAL_MODE` (来源: INFINEON_AURIX2G)
  - `DSADC_BIT_REVERSE_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the mode in which the Carrier Generator signal is generated.                                                       In case of Bit Reverse generation mode, it increases the frequency spectrum to yield a smoother induced sine signal. This is done by distributing the 0 and 1 bits over the 32 cycles of a PWM period.

######## 2. DsadcCarrierFrequencyClockDiv

- **UUID**: `d6ea9dd7-1d6e-4d4b-b3a3-24e9f55c6cc8`
- **参数名**: `DsadcCarrierFrequencyClockDiv`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CG_CLOCKDIVIDER_DIV2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CG_CLOCKDIVIDER_DIV2` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV6` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV10` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV12` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV14` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV16` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV18` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV20` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV22` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV24` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV26` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV28` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV30` (来源: INFINEON_AURIX2G)
  - `DSADC_CG_CLOCKDIVIDER_DIV32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which is used to define the frequency of the carrier signal generator, which is derived from the selected internal clock source and divider factor.

######## 3. DsadcCarrierSignalPolarity

- **UUID**: `d4aec598-5cc7-4487-9530-36ee9e855cc7`
- **参数名**: `DsadcCarrierSignalPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CARR_SIG_NORMAL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CARR_SIG_NORMAL` (来源: INFINEON_AURIX2G)
  - `DSADC_CARR_SIG_INVERTED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the starting polarity of the carrier signal.

######## 4. DsadcCarrierSignalType

- **UUID**: `7a116fc8-99ac-44d9-b5c9-9413dc8aed29`
- **参数名**: `DsadcCarrierSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CARR_SIG_STOPPED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CARR_SIG_STOPPED` (来源: INFINEON_AURIX2G)
  - `DSADC_CARR_SIG_SQUAREWAVE` (来源: INFINEON_AURIX2G)
  - `DSADC_CARR_SIG_TRIANGLE` (来源: INFINEON_AURIX2G)
  - `DSADC_CARR_SIG_SINEWAVE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the carrier signal type to be generated.

##### 7. DsadcErsEtlConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-b6fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcErsEtlConfig`
- **多重性**: [0..8]

**容器描述**:

This container configures the parameters for ERU input triggering

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. DsadcEruStatusFlagConfig

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-94e9f55c6ccc`
- **参数名**: `DsadcEruStatusFlagConfig`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_ETL_FALLING_EDGE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_ETL_FALLING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_ETL_RISING_EDGE` (来源: INFINEON_AURIX2G)
- **描述**: This parameters defines the condition on which the status flag in ETL block of ERU is set. On the inverse of the edge selected, the status flag is cleared.

######## 2. DsadcEruErsInputPin

- **UUID**: `7e0e69e5-6204-4564-a9c3-f4559f2409d6`
- **参数名**: `DsadcEruErsInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERS_0_REQ0A_PORTS_P15_4`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ERS_0_REQ0A_PORTS_P15_4` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ0B_CCU60_COUT60` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ0C_PORTS_P10_7` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ0D_MSC0_FCLP` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ0E_STM5_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ0F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ1A_PORTS_P14_3` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ1B_CCU61_COUT60` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ1C_PORTS_P10_8` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ1D_STM0_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ1E_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ1F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ2A_PORTS_P10_2` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ2B_PORTS_P02_1` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ2C_PORTS_P00_4` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ2D_ERAY0_MT` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ2E_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ2F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ3A_PORTS_P10_3` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ3B_PORTS_P14_1` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ3C_PORTS_P02_0` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ3D_STM1_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ3E_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ3F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ4A_PORTS_P33_7` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ4B_GTM_TOM0_12` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ4C_GPT120_T3OUT` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ4D_PORTS_P15_5` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ4E_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ4F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ5A_PORTS_P15_8` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ5B_GTM_TOM1_12` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ5C_GPT120_T6OUT` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ5D_STM2_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ5E_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ5F_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ6A_PORTS_P20_0` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ6B_PORTS_ESR0` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ6C_Reserved` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ6D_PORTS_P11_10` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ6E_STM3_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ6F_GTM_TOM2_12` (来源: INFINEON_AURIX2G)
  - `ERS_0_REQ7A_PORTS_P20_9` (来源: INFINEON_AURIX2G)
  - `ERS_1_REQ7B_PORTS_ESR1` (来源: INFINEON_AURIX2G)
  - `ERS_2_REQ7C_PORTS_P15_1` (来源: INFINEON_AURIX2G)
  - `ERS_3_REQ7D_ERAY1_MT` (来源: INFINEON_AURIX2G)
  - `ERS_4_REQ7E_STM4_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERS_5_REQ7F_GTM_TOM3_12` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the input pin for the selected ERS

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. DsadcEruErsRef

- **UUID**: `66c8e900-6193-42a3-8125-a695cc21788e`
- **引用名**: `DsadcEruErsRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-ERS channels available.

##### 8. DsadcChannelConfiguration

**容器属性**:

- **UUID**: `ccda81dc-46cf-4145-858b-bc9478cccccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcChannelConfiguration`
- **多重性**: [1..6]

**容器描述**:

This container contains the channel configuration (parameters) depending on the hardware capability.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. DsadcChannelId

- **UUID**: `d4aec598-5cc7-4487-9530-36ee9e11cccc`
- **参数名**: `DsadcChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..5]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: Unique number to identify the channel

####### ENUMERATION 类型参数

######## 1. DsadcHwChannelNum

- **UUID**: `d4aec598-5cc7-4487-9530-36ee9e12cccc`
- **参数名**: `DsadcHwChannelNum`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CHANNEL_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CHANNEL_0` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_1` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_2` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_3` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_4` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_5` (来源: INFINEON_AURIX2G)
- **描述**: Hardware EDSADC channel number

######## 2. DsadcAccessMode

- **UUID**: `c46bbfe5-3c7e-4b1b-9127-79334c04d53c`
- **参数名**: `DsadcAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_SINGLE_READ`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_SINGLE_READ` (来源: INFINEON_AURIX2G)
  - `DSADC_CIRCULAR_BUFFER` (来源: INFINEON_AURIX2G)
  - `DSADC_STREAM_LINEAR_BUFFER` (来源: INFINEON_AURIX2G)
  - `DSADC_DMA_ACCESS` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines the access mode selection for DSADC Driver. The available access mode is depends on parameter DsdcTriggerMode.If the DsadcTriggerMode is configured as TRIGGER_MODE_NORMAL then DsadcAccessMode can be any inside the Range. If DsadcTriggerMode is Configured as TRIGGER_MODE_WINDOW then DsadcAccessMode can be DSADC_SINGLE_READ or DSADC_STRERAM_LINEAR_BUFFER or DSADC_DMA_ACCESS.

######## 3. DsadcTriggerMode

- **UUID**: `a87c6432-965e-4c08-9f97-ed59fe64506f`
- **参数名**: `DsadcTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TRIGGER_MODE_NORMAL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TRIGGER_MODE_NORMAL` (来源: INFINEON_AURIX2G)
  - `DSADC_TRIGGER_MODE_WINDOW` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define the trigger mode. possbile conversion modes are DSADC_TRIGGER_MODE_NORMAL and DSADC_TRIGGER_MODE_WINDOW.                                                         DSADC_TRIGGER_MODE_NORMAL: Conversion starts after calling Dsadc_StartModulation() API.                                                         DSADC_TRIGGER_MODE_WINDOW: The result values are considered after Hardware trigger signal(GTM or ERU) is arrived.

######## 4. DsadcTimestampFeature

- **UUID**: `25863155-48e3-438d-98dc-754126a66d0c`
- **参数名**: `DsadcTimestampFeature`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TIMESTAMP_DISABLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TIMESTAMP_ENABLED` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_DISABLED` (来源: INFINEON_AURIX2G)
- **描述**: This Parameter is used to define the timestamp Functionality availability for the DSADC Channel.                                                         DSADC_TIMESTAMP_ENABLED: Enable the Timestamp functionality.                                                         DSADC_TIMESTAMP_DISABLED: Disable the Timestamp Functionality.

######## 5. DsadcGateActiveLevel

- **UUID**: `72bfe4df-c1de-4e91-8687-9bf5b7a9485c`
- **参数名**: `DsadcGateActiveLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_GATE_HIGH_LEVEL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_GATE_HIGH_LEVEL` (来源: INFINEON_AURIX2G)
  - `DSADC_GATE_LOW_LEVEL` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define the active level for the trigger gate signal.

####### FUNCTION-NAME 类型参数

######## 1. DsadcBufferFullNotification

- **UUID**: `ECUC:13cdc2fe-cf3c-4a68-93cb-a3676a293fd3`
- **参数名**: `DsadcBufferFullNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Callback function for buffer full event. The availablity of this parameter depends on DsadcAccessMode. If the DsadcAccessMode is configured as ACCESS_MODE_SINGLE OR ACCESS_MODE_CIRCULAR_BUFFER or DSADC_DMA_ACCESS then this parameter is not available.

######## 2. DsadcNewResultNotification

- **UUID**: `ECUC:9918056e-9ee3-49ce-b4fc-d4b8fa37c2d9`
- **参数名**: `DsadcNewResultNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Callback function for new result event.

######## 3. DsadcWindowCloseNotification

- **UUID**: `ECUC:c7c6aad9-cd74-4df6-a2ec-b8d556521c92`
- **参数名**: `DsadcWindowCloseNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Callback function for window close event, the availability of this parameter depends on DsadcTriggerMode configured as DSADC_TRIGGER_MODE_NORMAL

###### 配置容器

本模块包含 **14** 个配置容器：

####### 1. DsadcModulatorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6010059e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcModulatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains configuration parameters related to the On-chip modulator, input pin selection and modulator clock configuration.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. DsadcAnalogClockSyncDelay

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-44e9f55c6ccc`
- **参数名**: `DsadcAnalogClockSyncDelay`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the delay in clock cycles after the sync signal provided from Phase synchronizer.

######### BOOLEAN 类型参数

########## 1. DsadcDitheringEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e3f55c6ccc`
- **参数名**: `DsadcDitheringEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of internal dithering functionality for the modulator.

########## 2. DsadcIntegratorResetEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e7f55c6ccc`
- **参数名**: `DsadcIntegratorResetEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the modulator overload handling.

######### ENUMERATION 类型参数

########## 1. DsadcClockDivider

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e2f55c6ccc`
- **参数名**: `DsadcClockDivider`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CLOCKDIVIDER_DIV4`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV6` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV10` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV12` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV14` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV16` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV18` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the frequency of the modulator clock, which is derived from the peripheral clock

########## 2. DsadcInputGain

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-54e9f55c6ccc`
- **参数名**: `DsadcInputGain`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INPUT_GAIN_FACTOR_1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INPUT_GAIN_FACTOR_1` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUT_GAIN_FACTOR_2` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUT_GAIN_FACTOR_4` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines multiplication Gain factor for the analog input signal.

########## 3. DsadcInputMuxActionMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e4f55c6ccc`
- **参数名**: `DsadcInputMuxActionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INPUTMUX_PRESET_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INPUTMUX_PRESET_MODE` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUTMUX_SINGLE_STEP_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the control mechanism for input multiplexer. It defines the action to be taken for the input multiplexer upon a trigger event for pin selection.

########## 4. DsadcInputMuxControlMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e5f55c6ccc`
- **参数名**: `DsadcInputMuxControlMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INMUX_SOFTWARE_CONTROL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INMUX_SOFTWARE_CONTROL` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_FALLING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_RISING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_BOTH_EDGES` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the condition for a trigger event to control the input multiplexer.

########## 5. DsadcInputPinSelection

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e6f55c6ccc`
- **参数名**: `DsadcInputPinSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_PIN_0_AN2_AN3`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_PIN_0_AN2_AN3` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN12_AN13` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN36_AN37` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN38_AN39` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_2_AN44_AN45` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_3_AN46_AN47` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN20_AN21` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN24_AN25` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN0_AN1` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN14_AN15` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_PORT_00_8_PORT_00_7` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_PORT_00_10_PORT_00_9` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_PORT_00_2_PORT_00_1` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_PORT_00_4_PORT_00_3` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the initial/permanent setting for the input multiplexer, based on the operating mode selected.

########## 6. DsadcNegativeInputLine

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-64e9f55c6ccc`
- **参数名**: `DsadcNegativeInputLine`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_NEG_INPUT_PIN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_NEG_INPUT_PIN` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_SUPPLY_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_COMMON_MODE_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_REFERENCE_GROUND` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the modulator internal connection of the negative input.

########## 7. DsadcPositiveInputLine

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e8f55c6ccc`
- **参数名**: `DsadcPositiveInputLine`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_POS_INPUT_PIN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_POS_INPUT_PIN` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_SUPPLY_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_COMMON_MODE_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_REFERENCE_GROUND` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the modulator internal connection of the positive input.

####### 2. DsadcDemodulatorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10259e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcDemodulatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains configuration parameters related to the de-modulator, input data stream and trigger selection.

######## 参数配置

此容器包含 **3** 个参数：

######### ENUMERATION 类型参数

########## 1. DsadcIntegratorTriggerMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f54c6ccc`
- **参数名**: `DsadcIntegratorTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INTR_BYPASSED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INTR_BYPASSED` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_FALLING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_RISING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_ALWAYS_ACTIVE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the Integrator trigger mode.

########## 2. DsadcResultDisplayMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f58c6ccc`
- **参数名**: `DsadcResultDisplayMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RES_SIGNED_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RES_SIGNED_MODE` (来源: INFINEON_AURIX2G)
  - `DSADC_RES_UNSIGNED_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the ranges of the result values i.e. result display modes.

########## 3. DsadcTriggerSelect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f59c6ccc`
- **参数名**: `DsadcTriggerSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TRIGGER_0_NO_DSADC_TRIG`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TRIGGER_0_NO_DSADC_TRIG` (来源: INFINEON_AURIX2G)
  - `TRIGGER_0_GTM_DSADC_TRIG0` (来源: INFINEON_AURIX2G)
  - `TRIGGER_1_GTM_DSADC_TRIG1` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT0` (来源: INFINEON_AURIX2G)
  - `TRIGGER_12_GTM_DSADC_TRIG2` (来源: INFINEON_AURIX2G)
  - `TRIGGER_13_GTM_DSADC_TRIG3` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT1` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT2` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT3` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT4` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines EDSADC channel trigger source.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. DsadcOguConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-62fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOguConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

########## 参数配置

此容器包含 **8** 个参数：

########### BOOLEAN 类型参数

############ 1. DsadcEruErsCh0PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f20c6ccc`
- **参数名**: `DsadcEruErsCh0PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 0 is used for pattern detection for the selected OGU channel

############ 2. DsadcEruErsCh1PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-14e9f55c6ccc`
- **参数名**: `DsadcEruErsCh1PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 1 is used for pattern detection for the selected OGU channel

############ 3. DsadcEruErsCh2PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f21c6ccc`
- **参数名**: `DsadcEruErsCh2PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 2 is used for pattern detection for the selected OGU channel

############ 4. DsadcEruErsCh3PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f22c6ccc`
- **参数名**: `DsadcEruErsCh3PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 3 is used for pattern detection for the selected OGU channel

############ 5. DsadcEruErsCh4PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f23c6ccc`
- **参数名**: `DsadcEruErsCh4PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 4 is used for pattern detection for the selected OGU channel

############ 6. DsadcEruErsCh5PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f24c6ccc`
- **参数名**: `DsadcEruErsCh5PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 5 is used for pattern detection for the selected OGU channel

############ 7. DsadcEruErsCh6PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f25c6ccc`
- **参数名**: `DsadcEruErsCh6PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 6 is used for pattern detection for the selected OGU channel

############ 8. DsadcEruErsCh7PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f26c6ccc`
- **参数名**: `DsadcEruErsCh7PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 7 is used for pattern detection for the selected OGU channel

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. DsadcEruOguRef

- **UUID**: `66c8e900-6193-42a3-8125-a69abc21788e`
- **引用名**: `DsadcEruOguRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the DsadcHwChannelNum.

######### 2. DsadcTimestampConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6beea59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcTimestampConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters regarding the timestamp counter configuration.

########## 参数配置

此容器包含 **3** 个参数：

########### BOOLEAN 类型参数

############ 1. DsadcInputMuxSetCopyEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2cc6ccc`
- **参数名**: `DsadcInputMuxSetCopyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Analog MUX setting in the timestamp information.

########### ENUMERATION 类型参数

############ 1. DsadcTimestampCounterClockSel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2bc6ccc`
- **参数名**: `DsadcTimestampCounterClockSel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CLOCKDIVIDER_DIV1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CLOCKDIVIDER_DIV1` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV2` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the clock used for Timestamp counter.

############ 2. DsadcTimestampTriggerMode

- **UUID**: `6032d283-4ae2-4cf7-a415-2619568f6d10`
- **参数名**: `DsadcTimestampTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TIMESTAMP_WINDOWOPEN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TIMESTAMP_WINDOWOPEN` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_WINDOWCLOSE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define whether the timestamp has to be captured for window open event or window close event.

######### 3. DsadcIntegratorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6bbcd59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcIntegratorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to the Integrator functional block.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DsadcDiscardCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f30c6ccc`
- **参数名**: `DsadcDiscardCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be discarded before the start of the integration cycle.

############ 2. DsadcIntegrationCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f32c6ccc`
- **参数名**: `DsadcIntegrationCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [2..64]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be integrated.

####### 3. DsadcOguConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-62fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOguConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

######## 参数配置

此容器包含 **8** 个参数：

######### BOOLEAN 类型参数

########## 1. DsadcEruErsCh0PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f20c6ccc`
- **参数名**: `DsadcEruErsCh0PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 0 is used for pattern detection for the selected OGU channel

########## 2. DsadcEruErsCh1PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-14e9f55c6ccc`
- **参数名**: `DsadcEruErsCh1PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 1 is used for pattern detection for the selected OGU channel

########## 3. DsadcEruErsCh2PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f21c6ccc`
- **参数名**: `DsadcEruErsCh2PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 2 is used for pattern detection for the selected OGU channel

########## 4. DsadcEruErsCh3PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f22c6ccc`
- **参数名**: `DsadcEruErsCh3PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 3 is used for pattern detection for the selected OGU channel

########## 5. DsadcEruErsCh4PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f23c6ccc`
- **参数名**: `DsadcEruErsCh4PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 4 is used for pattern detection for the selected OGU channel

########## 6. DsadcEruErsCh5PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f24c6ccc`
- **参数名**: `DsadcEruErsCh5PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 5 is used for pattern detection for the selected OGU channel

########## 7. DsadcEruErsCh6PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f25c6ccc`
- **参数名**: `DsadcEruErsCh6PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 6 is used for pattern detection for the selected OGU channel

########## 8. DsadcEruErsCh7PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f26c6ccc`
- **参数名**: `DsadcEruErsCh7PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 7 is used for pattern detection for the selected OGU channel

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DsadcEruOguRef

- **UUID**: `66c8e900-6193-42a3-8125-a69abc21788e`
- **引用名**: `DsadcEruOguRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the DsadcHwChannelNum.

####### 4. DsadcTimestampConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6beea59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcTimestampConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters regarding the timestamp counter configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. DsadcInputMuxSetCopyEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2cc6ccc`
- **参数名**: `DsadcInputMuxSetCopyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Analog MUX setting in the timestamp information.

######### ENUMERATION 类型参数

########## 1. DsadcTimestampCounterClockSel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2bc6ccc`
- **参数名**: `DsadcTimestampCounterClockSel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CLOCKDIVIDER_DIV1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CLOCKDIVIDER_DIV1` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV2` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the clock used for Timestamp counter.

########## 2. DsadcTimestampTriggerMode

- **UUID**: `6032d283-4ae2-4cf7-a415-2619568f6d10`
- **参数名**: `DsadcTimestampTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TIMESTAMP_WINDOWOPEN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TIMESTAMP_WINDOWOPEN` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_WINDOWCLOSE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define whether the timestamp has to be captured for window open event or window close event.

####### 5. DsadcIntegratorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6bbcd59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcIntegratorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to the Integrator functional block.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DsadcDiscardCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f30c6ccc`
- **参数名**: `DsadcDiscardCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be discarded before the start of the integration cycle.

########## 2. DsadcIntegrationCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f32c6ccc`
- **参数名**: `DsadcIntegrationCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [2..64]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be integrated.

####### 6. DsadcRectificationConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10c59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcRectificationConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters of the rectifier block, used for resolver support, to determine position of the motor.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. DsadcPosSignDelayValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3bc6ccc`
- **参数名**: `DsadcPosSignDelayValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the value of Sign Delay counter (number of result values), for which to generate a positive delayed sign signal.

########## 2. DsadcNegSignDelayValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3cc6ccc`
- **参数名**: `DsadcNegSignDelayValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the value of Sign Delay counter (number of result values), for which to generate a negative delayed sign signal.

######### BOOLEAN 类型参数

########## 1. DsadcRectificationEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f38c6ccc`
- **参数名**: `DsadcRectificationEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter controls the action of the rectifier circuit on the input data.

######### ENUMERATION 类型参数

########## 1. DsadcSignSignalSource

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f39c6ccc`
- **参数名**: `DsadcSignSignalSource`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SRC_0_ON_CHIP_CARRIER_GENERATOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SRC_0_ON_CHIP_CARRIER_GENERATOR` (来源: INFINEON_AURIX2G)
  - `SRC_1_SIGNRESULT_FROM_DSADC_CHANNEL` (来源: INFINEON_AURIX2G)
  - `SRC_2_EXTERNAL_SIGN_SIGNAL_PORT00_4` (来源: INFINEON_AURIX2G)
  - `SRC_3_EXTERNAL_SIGN_SIGNAL_PORT33_13` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the source of the sign signal, which is to be delayed for the purpose of rectification.

########## 2. DsadcSignSignalChannel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3ac6ccc`
- **参数名**: `DsadcSignSignalChannel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CHANNEL_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CHANNEL_0` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_1` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_2` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_3` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_4` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the DSADC channel which provides the source of the sign signal, which is to be delayed for the purpose of rectification.

####### 7. DsadcCommonModeVoltConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b1ab59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCommonModeVoltConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to common mode voltage application to the inputs of the modulator channel.

######## 参数配置

此容器包含 **10** 个参数：

######### BOOLEAN 类型参数

########## 1. DsadcCommonModeVoltageEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f40c6ccc`
- **参数名**: `DsadcCommonModeVoltageEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Common Mode voltage to the input pins.

########## 2. DsadcComModeVoltPosAEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f43c6ccc`
- **参数名**: `DsadcComModeVoltPosAEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position A in the MUX needs to be connected to the Common Mode Voltage.

########## 3. DsadcComModeVoltPosBEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f45c6ccc`
- **参数名**: `DsadcComModeVoltPosBEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position B in the MUX needs to be connected to the Common Mode Voltage.

########## 4. DsadcComModeVoltPosCEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f47c6ccc`
- **参数名**: `DsadcComModeVoltPosCEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position C in the MUX needs to be connected to the Common Mode Voltage.

########## 5. DsadcComModeVoltPosDEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f49c6ccc`
- **参数名**: `DsadcComModeVoltPosDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position D in the MUX needs to be connected to the Common Mode Voltage.

########## 6. DsadcComModeVoltNegAEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f4cc6ccc`
- **参数名**: `DsadcComModeVoltNegAEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position A in the MUX needs to be connected to the Common Mode Voltage.

########## 7. DsadcComModeVoltNegBEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f4ec6ccc`
- **参数名**: `DsadcComModeVoltNegBEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position B in the MUX needs to be connected to the Common Mode Voltage.

########## 8. DsadcComModeVoltNegCEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9415c6ccc`
- **参数名**: `DsadcComModeVoltNegCEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position C in the MUX needs to be connected to the Common Mode Voltage.

########## 9. DsadcComModeVoltNegDEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9435c6ccc`
- **参数名**: `DsadcComModeVoltNegDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position D in the MUX needs to be connected to the Common Mode Voltage.

######### ENUMERATION 类型参数

########## 1. DsadcCommonModeVoltageSelect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f41c6ccc`
- **参数名**: `DsadcCommonModeVoltageSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_VCM_VREFX_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_VCM_VREFX_2` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_4` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_8` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the voltage level configured as Common Mode voltage, which can be connected to the input pins.

####### 8. DsadcFilterConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b13459e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcFilterConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to main filter chain.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. DsadcCICFilterDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f64c6ccc`
- **参数名**: `DsadcCICFilterDecimationFactor`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [4..512]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the oversampling rate/Decimation factor for the CIC filter.

########## 2. DsadcCICFilterStartValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f66c6ccc`
- **参数名**: `DsadcCICFilterStartValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [4..512]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the starting value of decimation counter, when the CIC filter is started/restarted.

########## 3. DsadcOffsetCompValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f6bc6ccc`
- **参数名**: `DsadcOffsetCompValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the offset component value to be removed(subtracted) from each result from the filter chain.

######### BOOLEAN 类型参数

########## 1. DsadcFIR0FilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f60c6ccc`
- **参数名**: `DsadcFIR0FilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of FIR0 filter in the filter chain of the DSADC channel.

########## 2. DsadcFIR1FilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f61c6ccc`
- **参数名**: `DsadcFIR1FilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of FIR1 filter in the filter chain of the DSADC channel.

########## 3. DsadcFIR1FilterDecimationEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f62c6ccc`
- **参数名**: `DsadcFIR1FilterDecimationEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the decimation rate of FIR1 filter.If selected as TRUE, then the filter decimates with a ratio 2:1

########## 4. DsadcPreFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f63c6ccc`
- **参数名**: `DsadcPreFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Prefilter in the filter chain of the DSADC channel

########## 5. DsadcOvershootCompensationEn

- **UUID**: `dea982da-0cb2-4bda-8324-e6e21fb90b04`
- **参数名**: `DsadcOvershootCompensationEn`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Overshoot compensation block in the filter chain of the DSADC channel.

########## 6. DsadcOffsetCompValueProtect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f6ac6ccc`
- **参数名**: `DsadcOffsetCompValueProtect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the protection of the Offset Compensation register from the calibration algorithm.

######### ENUMERATION 类型参数

########## 1. DsadcAlternateServiceReq

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f68c6ccc`
- **参数名**: `DsadcAlternateServiceReq`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_ALT_SERVICE_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_ALT_SERVICE_DISABLE` (来源: INFINEON_AURIX2G)
  - `DSADC_COMPARATOR_EVENT` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_EVENT` (来源: INFINEON_AURIX2G)
  - `DSADC_RESOLVER_EVENT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to generate alternate service request for any one of the following events, comparator event, time stamp event or alternate source.

########## 2. DsadcOffsetCompFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f69c6ccc`
- **参数名**: `DsadcOffsetCompFilterEnable`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_OFFCOMP_FILTER_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_OFFCOMP_FILTER_DISABLE` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_1` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_2` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_3` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_4` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_5` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_6` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter indicates availability of an Offset Compensation (IIR) filter (and its various operation modes) in Offset Compensation block.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. DsadcAuxFilterConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10abcd2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcAuxFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This configuration container provides parameters related to Dsadc Auxiliary Filter configuration..

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. DsadcAuxCicFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f82c6ccc`
- **参数名**: `DsadcAuxCicFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Dsadc Auxiliary filter.

########### ENUMERATION 类型参数

############ 1. DsadcAuxFilterCicDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f81c6ccc`
- **参数名**: `DsadcAuxFilterCicDecimationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_AUXCIC_OSR_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_AUXCIC_OSR_16` (来源: INFINEON_AURIX2G)
  - `DSADC_AUXCIC_OSR_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the over sampling rate/decimation factor for the Auxiliary CIC filter.

######### 2. DsadcGainCalibConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a5abcccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCalibConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain calibration.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

############ 参数配置

此容器包含 **2** 个参数：

############# FLOAT 类型参数

############## 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

############# ENUMERATION 类型参数

############## 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

########### 2. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

############# FLOAT 类型参数

############## 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

############## 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

############# ENUMERATION 类型参数

############## 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

############## 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

######### 3. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

########## 参数配置

此容器包含 **2** 个参数：

########### FLOAT 类型参数

############ 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

########### ENUMERATION 类型参数

############ 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

######### 4. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

########### FLOAT 类型参数

############ 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

############ 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

########### ENUMERATION 类型参数

############ 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

############ 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

######### 5. DsadcComparatorConfiguration

**容器属性**:

- **UUID**: `e2ada5c3-12ab-4571-b5ee-759cd5434db0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcComparatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for comparator configuration.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DsadcLowerBoundaryValue

- **UUID**: `f807a909-ab39-4628-8111-68665be76339`
- **参数名**: `DsadcLowerBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the lower boundary used for limit checking.

############ 2. DsadcUpperBoundaryValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f80c6ccc`
- **参数名**: `DsadcUpperBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the upper boundary used for limit checking.

########### ENUMERATION 类型参数

############ 1. DsadcComparatorEventSelect

- **UUID**: `ff120d55-9be8-48c1-ac48-4e1270732d0f`
- **参数名**: `DsadcComparatorEventSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RESULT_ALWAYS`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RESULT_ALWAYS` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_INSIDE_RANGE` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_OUTSIDE_RANGE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the comparator mode selected to generate an alarm event (and also a service request, if selected auxiliary service request generation).

######### 6. DsadcOvershootCompenConfig

**容器属性**:

- **UUID**: `7fd025de-907b-4268-b461-e379b30f3bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOvershootCompenConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU input triggering

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. DsadcStepDetectionThreshold

- **UUID**: `c0af7dc5-4445-4b46-8ec3-e2194a3e68ae`
- **参数名**: `DsadcStepDetectionThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..2047]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the threshold value (magnitude) used for step detection. The threshold value is DsadcStepDetectionThreshold * 32

########### ENUMERATION 类型参数

############ 1. DsadcStepDetectionMode

- **UUID**: `f3cc0efc-5fb1-4a43-a04d-0cac5d6c6682`
- **参数名**: `DsadcStepDetectionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_STEP_DETECT_CMP_LAST`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_STEP_DETECT_CMP_LAST` (来源: INFINEON_AURIX2G)
  - `DSADC_STEP_DETECT_CMP_SEC_LAST` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the when the slew rate filter has to be activated

############ 2. DsadcSlewRateFilterStrength

- **UUID**: `67ad9852-f061-486d-b362-7bc53c40d431`
- **参数名**: `DsadcSlewRateFilterStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_MINIMUM_FILTER_EFFECT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_MINIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_WEAK_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MEDIUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MAXIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the filter strength for the slew rate filter

############ 3. DsadcSlewRateFilterRunTime

- **UUID**: `a3c267ec-3099-4508-925c-09650a25f4bc`
- **参数名**: `DsadcSlewRateFilterRunTime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_SLEWRATE_FILTR_RUNTIME_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_SLEWRATE_FILTR_RUNTIME_2` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_4` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_8` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the time constant for the slew rate filter

####### 9. DsadcAuxFilterConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10abcd2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcAuxFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This configuration container provides parameters related to Dsadc Auxiliary Filter configuration..

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. DsadcAuxCicFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f82c6ccc`
- **参数名**: `DsadcAuxCicFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Dsadc Auxiliary filter.

######### ENUMERATION 类型参数

########## 1. DsadcAuxFilterCicDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f81c6ccc`
- **参数名**: `DsadcAuxFilterCicDecimationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_AUXCIC_OSR_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_AUXCIC_OSR_16` (来源: INFINEON_AURIX2G)
  - `DSADC_AUXCIC_OSR_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the over sampling rate/decimation factor for the Auxiliary CIC filter.

####### 10. DsadcGainCalibConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a5abcccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCalibConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain calibration.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

########## 参数配置

此容器包含 **2** 个参数：

########### FLOAT 类型参数

############ 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

########### ENUMERATION 类型参数

############ 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

######### 2. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

########### FLOAT 类型参数

############ 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

############ 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

########### ENUMERATION 类型参数

############ 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

############ 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

####### 11. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

######### ENUMERATION 类型参数

########## 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

####### 12. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

######### FLOAT 类型参数

########## 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

########## 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

######### ENUMERATION 类型参数

########## 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

########## 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

####### 13. DsadcComparatorConfiguration

**容器属性**:

- **UUID**: `e2ada5c3-12ab-4571-b5ee-759cd5434db0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcComparatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for comparator configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DsadcLowerBoundaryValue

- **UUID**: `f807a909-ab39-4628-8111-68665be76339`
- **参数名**: `DsadcLowerBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the lower boundary used for limit checking.

########## 2. DsadcUpperBoundaryValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f80c6ccc`
- **参数名**: `DsadcUpperBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the upper boundary used for limit checking.

######### ENUMERATION 类型参数

########## 1. DsadcComparatorEventSelect

- **UUID**: `ff120d55-9be8-48c1-ac48-4e1270732d0f`
- **参数名**: `DsadcComparatorEventSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RESULT_ALWAYS`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RESULT_ALWAYS` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_INSIDE_RANGE` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_OUTSIDE_RANGE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the comparator mode selected to generate an alarm event (and also a service request, if selected auxiliary service request generation).

####### 14. DsadcOvershootCompenConfig

**容器属性**:

- **UUID**: `7fd025de-907b-4268-b461-e379b30f3bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOvershootCompenConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU input triggering

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DsadcStepDetectionThreshold

- **UUID**: `c0af7dc5-4445-4b46-8ec3-e2194a3e68ae`
- **参数名**: `DsadcStepDetectionThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..2047]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the threshold value (magnitude) used for step detection. The threshold value is DsadcStepDetectionThreshold * 32

######### ENUMERATION 类型参数

########## 1. DsadcStepDetectionMode

- **UUID**: `f3cc0efc-5fb1-4a43-a04d-0cac5d6c6682`
- **参数名**: `DsadcStepDetectionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_STEP_DETECT_CMP_LAST`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_STEP_DETECT_CMP_LAST` (来源: INFINEON_AURIX2G)
  - `DSADC_STEP_DETECT_CMP_SEC_LAST` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the when the slew rate filter has to be activated

########## 2. DsadcSlewRateFilterStrength

- **UUID**: `67ad9852-f061-486d-b362-7bc53c40d431`
- **参数名**: `DsadcSlewRateFilterStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_MINIMUM_FILTER_EFFECT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_MINIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_WEAK_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MEDIUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MAXIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the filter strength for the slew rate filter

########## 3. DsadcSlewRateFilterRunTime

- **UUID**: `a3c267ec-3099-4508-925c-09650a25f4bc`
- **参数名**: `DsadcSlewRateFilterRunTime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_SLEWRATE_FILTR_RUNTIME_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_SLEWRATE_FILTR_RUNTIME_2` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_4` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_8` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the time constant for the slew rate filter

##### 9. DsadcModulatorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6010059e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcModulatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains configuration parameters related to the On-chip modulator, input pin selection and modulator clock configuration.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. DsadcAnalogClockSyncDelay

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-44e9f55c6ccc`
- **参数名**: `DsadcAnalogClockSyncDelay`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the delay in clock cycles after the sync signal provided from Phase synchronizer.

####### BOOLEAN 类型参数

######## 1. DsadcDitheringEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e3f55c6ccc`
- **参数名**: `DsadcDitheringEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of internal dithering functionality for the modulator.

######## 2. DsadcIntegratorResetEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e7f55c6ccc`
- **参数名**: `DsadcIntegratorResetEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the modulator overload handling.

####### ENUMERATION 类型参数

######## 1. DsadcClockDivider

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e2f55c6ccc`
- **参数名**: `DsadcClockDivider`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CLOCKDIVIDER_DIV4`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV6` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV10` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV12` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV14` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV16` (来源: INFINEON_AURIX2G)
  - `DSADC_CLOCKDIVIDER_DIV18` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the frequency of the modulator clock, which is derived from the peripheral clock

######## 2. DsadcInputGain

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-54e9f55c6ccc`
- **参数名**: `DsadcInputGain`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INPUT_GAIN_FACTOR_1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INPUT_GAIN_FACTOR_1` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUT_GAIN_FACTOR_2` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUT_GAIN_FACTOR_4` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines multiplication Gain factor for the analog input signal.

######## 3. DsadcInputMuxActionMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e4f55c6ccc`
- **参数名**: `DsadcInputMuxActionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INPUTMUX_PRESET_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INPUTMUX_PRESET_MODE` (来源: INFINEON_AURIX2G)
  - `DSADC_INPUTMUX_SINGLE_STEP_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the control mechanism for input multiplexer. It defines the action to be taken for the input multiplexer upon a trigger event for pin selection.

######## 4. DsadcInputMuxControlMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e5f55c6ccc`
- **参数名**: `DsadcInputMuxControlMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INMUX_SOFTWARE_CONTROL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INMUX_SOFTWARE_CONTROL` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_FALLING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_RISING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INMUX_TRIG_EVENT_BOTH_EDGES` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the condition for a trigger event to control the input multiplexer.

######## 5. DsadcInputPinSelection

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e6f55c6ccc`
- **参数名**: `DsadcInputPinSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_PIN_0_AN2_AN3`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_PIN_0_AN2_AN3` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN12_AN13` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN36_AN37` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN38_AN39` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_2_AN44_AN45` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_3_AN46_AN47` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN20_AN21` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN24_AN25` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_AN0_AN1` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_AN14_AN15` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_PORT_00_8_PORT_00_7` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_PORT_00_10_PORT_00_9` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_0_PORT_00_2_PORT_00_1` (来源: INFINEON_AURIX2G)
  - `INPUT_PIN_1_PORT_00_4_PORT_00_3` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the initial/permanent setting for the input multiplexer, based on the operating mode selected.

######## 6. DsadcNegativeInputLine

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-64e9f55c6ccc`
- **参数名**: `DsadcNegativeInputLine`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_NEG_INPUT_PIN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_NEG_INPUT_PIN` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_SUPPLY_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_COMMON_MODE_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_NEG_IN_REFERENCE_GROUND` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the modulator internal connection of the negative input.

######## 7. DsadcPositiveInputLine

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e8f55c6ccc`
- **参数名**: `DsadcPositiveInputLine`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_POS_INPUT_PIN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_POS_INPUT_PIN` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_SUPPLY_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_COMMON_MODE_VOLT` (来源: INFINEON_AURIX2G)
  - `DSADC_POS_IN_REFERENCE_GROUND` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the modulator internal connection of the positive input.

##### 10. DsadcDemodulatorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10259e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcDemodulatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains configuration parameters related to the de-modulator, input data stream and trigger selection.

###### 参数配置

此容器包含 **3** 个参数：

####### ENUMERATION 类型参数

######## 1. DsadcIntegratorTriggerMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f54c6ccc`
- **参数名**: `DsadcIntegratorTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_INTR_BYPASSED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_INTR_BYPASSED` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_FALLING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_RISING_EDGE` (来源: INFINEON_AURIX2G)
  - `DSADC_INTR_ALWAYS_ACTIVE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the Integrator trigger mode.

######## 2. DsadcResultDisplayMode

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f58c6ccc`
- **参数名**: `DsadcResultDisplayMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RES_SIGNED_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RES_SIGNED_MODE` (来源: INFINEON_AURIX2G)
  - `DSADC_RES_UNSIGNED_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the ranges of the result values i.e. result display modes.

######## 3. DsadcTriggerSelect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f59c6ccc`
- **参数名**: `DsadcTriggerSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TRIGGER_0_NO_DSADC_TRIG`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TRIGGER_0_NO_DSADC_TRIG` (来源: INFINEON_AURIX2G)
  - `TRIGGER_0_GTM_DSADC_TRIG0` (来源: INFINEON_AURIX2G)
  - `TRIGGER_1_GTM_DSADC_TRIG1` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT0` (来源: INFINEON_AURIX2G)
  - `TRIGGER_12_GTM_DSADC_TRIG2` (来源: INFINEON_AURIX2G)
  - `TRIGGER_13_GTM_DSADC_TRIG3` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT1` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT2` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT3` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT4` (来源: INFINEON_AURIX2G)
  - `TRIGGER_6_ERU_PDOUT5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines EDSADC channel trigger source.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. DsadcOguConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-62fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOguConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

######## 参数配置

此容器包含 **8** 个参数：

######### BOOLEAN 类型参数

########## 1. DsadcEruErsCh0PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f20c6ccc`
- **参数名**: `DsadcEruErsCh0PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 0 is used for pattern detection for the selected OGU channel

########## 2. DsadcEruErsCh1PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-14e9f55c6ccc`
- **参数名**: `DsadcEruErsCh1PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 1 is used for pattern detection for the selected OGU channel

########## 3. DsadcEruErsCh2PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f21c6ccc`
- **参数名**: `DsadcEruErsCh2PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 2 is used for pattern detection for the selected OGU channel

########## 4. DsadcEruErsCh3PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f22c6ccc`
- **参数名**: `DsadcEruErsCh3PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 3 is used for pattern detection for the selected OGU channel

########## 5. DsadcEruErsCh4PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f23c6ccc`
- **参数名**: `DsadcEruErsCh4PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 4 is used for pattern detection for the selected OGU channel

########## 6. DsadcEruErsCh5PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f24c6ccc`
- **参数名**: `DsadcEruErsCh5PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 5 is used for pattern detection for the selected OGU channel

########## 7. DsadcEruErsCh6PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f25c6ccc`
- **参数名**: `DsadcEruErsCh6PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 6 is used for pattern detection for the selected OGU channel

########## 8. DsadcEruErsCh7PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f26c6ccc`
- **参数名**: `DsadcEruErsCh7PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 7 is used for pattern detection for the selected OGU channel

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DsadcEruOguRef

- **UUID**: `66c8e900-6193-42a3-8125-a69abc21788e`
- **引用名**: `DsadcEruOguRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the DsadcHwChannelNum.

####### 2. DsadcTimestampConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6beea59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcTimestampConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters regarding the timestamp counter configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. DsadcInputMuxSetCopyEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2cc6ccc`
- **参数名**: `DsadcInputMuxSetCopyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Analog MUX setting in the timestamp information.

######### ENUMERATION 类型参数

########## 1. DsadcTimestampCounterClockSel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2bc6ccc`
- **参数名**: `DsadcTimestampCounterClockSel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CLOCKDIVIDER_DIV1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CLOCKDIVIDER_DIV1` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV2` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the clock used for Timestamp counter.

########## 2. DsadcTimestampTriggerMode

- **UUID**: `6032d283-4ae2-4cf7-a415-2619568f6d10`
- **参数名**: `DsadcTimestampTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TIMESTAMP_WINDOWOPEN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TIMESTAMP_WINDOWOPEN` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_WINDOWCLOSE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define whether the timestamp has to be captured for window open event or window close event.

####### 3. DsadcIntegratorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6bbcd59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcIntegratorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to the Integrator functional block.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DsadcDiscardCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f30c6ccc`
- **参数名**: `DsadcDiscardCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be discarded before the start of the integration cycle.

########## 2. DsadcIntegrationCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f32c6ccc`
- **参数名**: `DsadcIntegrationCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [2..64]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be integrated.

##### 11. DsadcOguConfig

**容器属性**:

- **UUID**: `83112075-2689-470a-b302-62fe4b0bd42d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOguConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU triggering

###### 参数配置

此容器包含 **8** 个参数：

####### BOOLEAN 类型参数

######## 1. DsadcEruErsCh0PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f20c6ccc`
- **参数名**: `DsadcEruErsCh0PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 0 is used for pattern detection for the selected OGU channel

######## 2. DsadcEruErsCh1PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-14e9f55c6ccc`
- **参数名**: `DsadcEruErsCh1PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 1 is used for pattern detection for the selected OGU channel

######## 3. DsadcEruErsCh2PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f21c6ccc`
- **参数名**: `DsadcEruErsCh2PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 2 is used for pattern detection for the selected OGU channel

######## 4. DsadcEruErsCh3PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f22c6ccc`
- **参数名**: `DsadcEruErsCh3PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 3 is used for pattern detection for the selected OGU channel

######## 5. DsadcEruErsCh4PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f23c6ccc`
- **参数名**: `DsadcEruErsCh4PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 4 is used for pattern detection for the selected OGU channel

######## 6. DsadcEruErsCh5PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f24c6ccc`
- **参数名**: `DsadcEruErsCh5PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 5 is used for pattern detection for the selected OGU channel

######## 7. DsadcEruErsCh6PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f25c6ccc`
- **参数名**: `DsadcEruErsCh6PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 6 is used for pattern detection for the selected OGU channel

######## 8. DsadcEruErsCh7PatternFlagEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f26c6ccc`
- **参数名**: `DsadcEruErsCh7PatternFlagEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the ERU ERS channel 7 is used for pattern detection for the selected OGU channel

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. DsadcEruOguRef

- **UUID**: `66c8e900-6193-42a3-8125-a69abc21788e`
- **引用名**: `DsadcEruOguRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **描述**: This parameter is a reference to the ERU container in the MCU. It lists down all the ERU-OGU channels available. The OGUs available is dependent on the DsadcHwChannelNum.

##### 12. DsadcTimestampConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6beea59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcTimestampConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters regarding the timestamp counter configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. DsadcInputMuxSetCopyEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2cc6ccc`
- **参数名**: `DsadcInputMuxSetCopyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Analog MUX setting in the timestamp information.

####### ENUMERATION 类型参数

######## 1. DsadcTimestampCounterClockSel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f2bc6ccc`
- **参数名**: `DsadcTimestampCounterClockSel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CLOCKDIVIDER_DIV1`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CLOCKDIVIDER_DIV1` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV2` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV4` (来源: INFINEON_AURIX2G)
  - `CLOCKDIVIDER_DIV8` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the divider factor, which defines the clock used for Timestamp counter.

######## 2. DsadcTimestampTriggerMode

- **UUID**: `6032d283-4ae2-4cf7-a415-2619568f6d10`
- **参数名**: `DsadcTimestampTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_TIMESTAMP_WINDOWOPEN`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_TIMESTAMP_WINDOWOPEN` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_WINDOWCLOSE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to define whether the timestamp has to be captured for window open event or window close event.

##### 13. DsadcIntegratorConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6bbcd59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcIntegratorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to the Integrator functional block.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DsadcDiscardCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f30c6ccc`
- **参数名**: `DsadcDiscardCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be discarded before the start of the integration cycle.

######## 2. DsadcIntegrationCount

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f32c6ccc`
- **参数名**: `DsadcIntegrationCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [2..64]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the number of result values to be integrated.

##### 14. DsadcRectificationConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10c59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcRectificationConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters of the rectifier block, used for resolver support, to determine position of the motor.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. DsadcPosSignDelayValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3bc6ccc`
- **参数名**: `DsadcPosSignDelayValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the value of Sign Delay counter (number of result values), for which to generate a positive delayed sign signal.

######## 2. DsadcNegSignDelayValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3cc6ccc`
- **参数名**: `DsadcNegSignDelayValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter determines the value of Sign Delay counter (number of result values), for which to generate a negative delayed sign signal.

####### BOOLEAN 类型参数

######## 1. DsadcRectificationEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f38c6ccc`
- **参数名**: `DsadcRectificationEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter controls the action of the rectifier circuit on the input data.

####### ENUMERATION 类型参数

######## 1. DsadcSignSignalSource

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f39c6ccc`
- **参数名**: `DsadcSignSignalSource`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SRC_0_ON_CHIP_CARRIER_GENERATOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SRC_0_ON_CHIP_CARRIER_GENERATOR` (来源: INFINEON_AURIX2G)
  - `SRC_1_SIGNRESULT_FROM_DSADC_CHANNEL` (来源: INFINEON_AURIX2G)
  - `SRC_2_EXTERNAL_SIGN_SIGNAL_PORT00_4` (来源: INFINEON_AURIX2G)
  - `SRC_3_EXTERNAL_SIGN_SIGNAL_PORT33_13` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the source of the sign signal, which is to be delayed for the purpose of rectification.

######## 2. DsadcSignSignalChannel

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f3ac6ccc`
- **参数名**: `DsadcSignSignalChannel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CHANNEL_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CHANNEL_0` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_1` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_2` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_3` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_4` (来源: INFINEON_AURIX2G)
  - `DSADC_CHANNEL_5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the DSADC channel which provides the source of the sign signal, which is to be delayed for the purpose of rectification.

##### 15. DsadcCommonModeVoltConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b1ab59e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCommonModeVoltConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to common mode voltage application to the inputs of the modulator channel.

###### 参数配置

此容器包含 **10** 个参数：

####### BOOLEAN 类型参数

######## 1. DsadcCommonModeVoltageEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f40c6ccc`
- **参数名**: `DsadcCommonModeVoltageEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Common Mode voltage to the input pins.

######## 2. DsadcComModeVoltPosAEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f43c6ccc`
- **参数名**: `DsadcComModeVoltPosAEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position A in the MUX needs to be connected to the Common Mode Voltage.

######## 3. DsadcComModeVoltPosBEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f45c6ccc`
- **参数名**: `DsadcComModeVoltPosBEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position B in the MUX needs to be connected to the Common Mode Voltage.

######## 4. DsadcComModeVoltPosCEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f47c6ccc`
- **参数名**: `DsadcComModeVoltPosCEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position C in the MUX needs to be connected to the Common Mode Voltage.

######## 5. DsadcComModeVoltPosDEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f49c6ccc`
- **参数名**: `DsadcComModeVoltPosDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the positive analog line connected to position D in the MUX needs to be connected to the Common Mode Voltage.

######## 6. DsadcComModeVoltNegAEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f4cc6ccc`
- **参数名**: `DsadcComModeVoltNegAEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position A in the MUX needs to be connected to the Common Mode Voltage.

######## 7. DsadcComModeVoltNegBEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f4ec6ccc`
- **参数名**: `DsadcComModeVoltNegBEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position B in the MUX needs to be connected to the Common Mode Voltage.

######## 8. DsadcComModeVoltNegCEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9415c6ccc`
- **参数名**: `DsadcComModeVoltNegCEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position C in the MUX needs to be connected to the Common Mode Voltage.

######## 9. DsadcComModeVoltNegDEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9435c6ccc`
- **参数名**: `DsadcComModeVoltNegDEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines if the negative analog line connected to position D in the MUX needs to be connected to the Common Mode Voltage.

####### ENUMERATION 类型参数

######## 1. DsadcCommonModeVoltageSelect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f41c6ccc`
- **参数名**: `DsadcCommonModeVoltageSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_VCM_VREFX_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_VCM_VREFX_2` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_4` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_8` (来源: INFINEON_AURIX2G)
  - `DSADC_VCM_VREFX_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the voltage level configured as Common Mode voltage, which can be connected to the input pins.

##### 16. DsadcFilterConfiguration

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b13459e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcFilterConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameter related to main filter chain.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. DsadcCICFilterDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f64c6ccc`
- **参数名**: `DsadcCICFilterDecimationFactor`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [4..512]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the oversampling rate/Decimation factor for the CIC filter.

######## 2. DsadcCICFilterStartValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f66c6ccc`
- **参数名**: `DsadcCICFilterStartValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [4..512]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the starting value of decimation counter, when the CIC filter is started/restarted.

######## 3. DsadcOffsetCompValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f6bc6ccc`
- **参数名**: `DsadcOffsetCompValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the offset component value to be removed(subtracted) from each result from the filter chain.

####### BOOLEAN 类型参数

######## 1. DsadcFIR0FilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f60c6ccc`
- **参数名**: `DsadcFIR0FilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of FIR0 filter in the filter chain of the DSADC channel.

######## 2. DsadcFIR1FilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f61c6ccc`
- **参数名**: `DsadcFIR1FilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of FIR1 filter in the filter chain of the DSADC channel.

######## 3. DsadcFIR1FilterDecimationEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f62c6ccc`
- **参数名**: `DsadcFIR1FilterDecimationEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the decimation rate of FIR1 filter.If selected as TRUE, then the filter decimates with a ratio 2:1

######## 4. DsadcPreFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f63c6ccc`
- **参数名**: `DsadcPreFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Prefilter in the filter chain of the DSADC channel

######## 5. DsadcOvershootCompensationEn

- **UUID**: `dea982da-0cb2-4bda-8324-e6e21fb90b04`
- **参数名**: `DsadcOvershootCompensationEn`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Overshoot compensation block in the filter chain of the DSADC channel.

######## 6. DsadcOffsetCompValueProtect

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f6ac6ccc`
- **参数名**: `DsadcOffsetCompValueProtect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the protection of the Offset Compensation register from the calibration algorithm.

####### ENUMERATION 类型参数

######## 1. DsadcAlternateServiceReq

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f68c6ccc`
- **参数名**: `DsadcAlternateServiceReq`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_ALT_SERVICE_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_ALT_SERVICE_DISABLE` (来源: INFINEON_AURIX2G)
  - `DSADC_COMPARATOR_EVENT` (来源: INFINEON_AURIX2G)
  - `DSADC_TIMESTAMP_EVENT` (来源: INFINEON_AURIX2G)
  - `DSADC_RESOLVER_EVENT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is used to generate alternate service request for any one of the following events, comparator event, time stamp event or alternate source.

######## 2. DsadcOffsetCompFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f69c6ccc`
- **参数名**: `DsadcOffsetCompFilterEnable`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_OFFCOMP_FILTER_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_OFFCOMP_FILTER_DISABLE` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_1` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_2` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_3` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_4` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_5` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_6` (来源: INFINEON_AURIX2G)
  - `DSADC_OFFCOMP_FILTER_RATE_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter indicates availability of an Offset Compensation (IIR) filter (and its various operation modes) in Offset Compensation block.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. DsadcAuxFilterConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10abcd2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcAuxFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This configuration container provides parameters related to Dsadc Auxiliary Filter configuration..

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. DsadcAuxCicFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f82c6ccc`
- **参数名**: `DsadcAuxCicFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Dsadc Auxiliary filter.

######### ENUMERATION 类型参数

########## 1. DsadcAuxFilterCicDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f81c6ccc`
- **参数名**: `DsadcAuxFilterCicDecimationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_AUXCIC_OSR_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_AUXCIC_OSR_16` (来源: INFINEON_AURIX2G)
  - `DSADC_AUXCIC_OSR_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the over sampling rate/decimation factor for the Auxiliary CIC filter.

####### 2. DsadcGainCalibConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a5abcccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCalibConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain calibration.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

########## 参数配置

此容器包含 **2** 个参数：

########### FLOAT 类型参数

############ 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

########### ENUMERATION 类型参数

############ 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

######### 2. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

########### FLOAT 类型参数

############ 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

############ 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

########### ENUMERATION 类型参数

############ 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

############ 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

####### 3. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

######### ENUMERATION 类型参数

########## 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

####### 4. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

######### FLOAT 类型参数

########## 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

########## 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

######### ENUMERATION 类型参数

########## 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

########## 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

####### 5. DsadcComparatorConfiguration

**容器属性**:

- **UUID**: `e2ada5c3-12ab-4571-b5ee-759cd5434db0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcComparatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for comparator configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DsadcLowerBoundaryValue

- **UUID**: `f807a909-ab39-4628-8111-68665be76339`
- **参数名**: `DsadcLowerBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the lower boundary used for limit checking.

########## 2. DsadcUpperBoundaryValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f80c6ccc`
- **参数名**: `DsadcUpperBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the upper boundary used for limit checking.

######### ENUMERATION 类型参数

########## 1. DsadcComparatorEventSelect

- **UUID**: `ff120d55-9be8-48c1-ac48-4e1270732d0f`
- **参数名**: `DsadcComparatorEventSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RESULT_ALWAYS`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RESULT_ALWAYS` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_INSIDE_RANGE` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_OUTSIDE_RANGE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the comparator mode selected to generate an alarm event (and also a service request, if selected auxiliary service request generation).

####### 6. DsadcOvershootCompenConfig

**容器属性**:

- **UUID**: `7fd025de-907b-4268-b461-e379b30f3bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOvershootCompenConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU input triggering

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DsadcStepDetectionThreshold

- **UUID**: `c0af7dc5-4445-4b46-8ec3-e2194a3e68ae`
- **参数名**: `DsadcStepDetectionThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..2047]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the threshold value (magnitude) used for step detection. The threshold value is DsadcStepDetectionThreshold * 32

######### ENUMERATION 类型参数

########## 1. DsadcStepDetectionMode

- **UUID**: `f3cc0efc-5fb1-4a43-a04d-0cac5d6c6682`
- **参数名**: `DsadcStepDetectionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_STEP_DETECT_CMP_LAST`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_STEP_DETECT_CMP_LAST` (来源: INFINEON_AURIX2G)
  - `DSADC_STEP_DETECT_CMP_SEC_LAST` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the when the slew rate filter has to be activated

########## 2. DsadcSlewRateFilterStrength

- **UUID**: `67ad9852-f061-486d-b362-7bc53c40d431`
- **参数名**: `DsadcSlewRateFilterStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_MINIMUM_FILTER_EFFECT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_MINIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_WEAK_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MEDIUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MAXIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the filter strength for the slew rate filter

########## 3. DsadcSlewRateFilterRunTime

- **UUID**: `a3c267ec-3099-4508-925c-09650a25f4bc`
- **参数名**: `DsadcSlewRateFilterRunTime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_SLEWRATE_FILTR_RUNTIME_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_SLEWRATE_FILTR_RUNTIME_2` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_4` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_8` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the time constant for the slew rate filter

##### 17. DsadcAuxFilterConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10abcd2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcAuxFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This configuration container provides parameters related to Dsadc Auxiliary Filter configuration..

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. DsadcAuxCicFilterEnable

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f82c6ccc`
- **参数名**: `DsadcAuxCicFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the availability of Dsadc Auxiliary filter.

####### ENUMERATION 类型参数

######## 1. DsadcAuxFilterCicDecimationFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f81c6ccc`
- **参数名**: `DsadcAuxFilterCicDecimationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_AUXCIC_OSR_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_AUXCIC_OSR_16` (来源: INFINEON_AURIX2G)
  - `DSADC_AUXCIC_OSR_32` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the over sampling rate/decimation factor for the Auxiliary CIC filter.

##### 18. DsadcGainCalibConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a5abcccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCalibConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain calibration.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

######### ENUMERATION 类型参数

########## 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

####### 2. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

######### FLOAT 类型参数

########## 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

########## 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

######### ENUMERATION 类型参数

########## 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

########## 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

##### 19. DsadcGainCorrConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10b79e2ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcGainCorrConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for Gain correction.

###### 参数配置

此容器包含 **2** 个参数：

####### FLOAT 类型参数

######## 1. DsadcGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f71c6ccc`
- **参数名**: `DsadcGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction.

####### ENUMERATION 类型参数

######## 1. DsadcCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f70c6ccc`
- **参数名**: `DsadcCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter.

##### 20. DsadcCalibAlgoConfig

**容器属性**:

- **UUID**: `6062ca80-76f1-43eb-8fae-6b10a4562ccc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcCalibAlgoConfig`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parmaters for gain calibration.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. DsadcCalibAlgoTargetValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f79c6ccc`
- **参数名**: `DsadcCalibAlgoTargetValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `25000`
- **取值范围**: [0..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the full scale target value for calibration algorithm

####### FLOAT 类型参数

######## 1. DsadcCalibGainCorrMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f76c6ccc`
- **参数名**: `DsadcCalibGainCorrMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain correction. This is valid only during execution of the calibration algorithm

######## 2. DsadcGainCalibMulFactor

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f78c6ccc`
- **参数名**: `DsadcGainCalibMulFactor`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0000`
- **取值范围**: [0.0..1.9999]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines multiplication factor for Gain calibration. This is valid only during execution of the calibration algorithm.

####### ENUMERATION 类型参数

######## 1. DsadcCalibCICFilterOutputShiftPos

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f75c6ccc`
- **参数名**: `DsadcCalibCICFilterOutputShiftPos`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `BITS_0_TO_16`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `BITS_0_TO_16` (来源: INFINEON_AURIX2G)
  - `BITS_1_TO_17` (来源: INFINEON_AURIX2G)
  - `BITS_2_TO_18` (来源: INFINEON_AURIX2G)
  - `BITS_3_TO_19` (来源: INFINEON_AURIX2G)
  - `BITS_4_TO_20` (来源: INFINEON_AURIX2G)
  - `BITS_5_TO_21` (来源: INFINEON_AURIX2G)
  - `BITS_6_TO_22` (来源: INFINEON_AURIX2G)
  - `BITS_7_TO_23` (来源: INFINEON_AURIX2G)
  - `BITS_8_TO_24` (来源: INFINEON_AURIX2G)
  - `BITS_9_TO_25` (来源: INFINEON_AURIX2G)
  - `BITS_10_TO_26` (来源: INFINEON_AURIX2G)
  - `BITS_11_TO_27` (来源: INFINEON_AURIX2G)
  - `BITS_12_TO_28` (来源: INFINEON_AURIX2G)
  - `BITS_13_TO_29` (来源: INFINEON_AURIX2G)
  - `BITS_14_TO_30` (来源: INFINEON_AURIX2G)
  - `BITS_15_TO_31` (来源: INFINEON_AURIX2G)
  - `BITS_16_TO_32` (来源: INFINEON_AURIX2G)
  - `BITS_17_TO_33` (来源: INFINEON_AURIX2G)
  - `BITS_18_TO_34` (来源: INFINEON_AURIX2G)
  - `BITS_19_TO_35` (来源: INFINEON_AURIX2G)
  - `BITS_20_TO_36` (来源: INFINEON_AURIX2G)
  - `BITS_21_TO_37` (来源: INFINEON_AURIX2G)
  - `BITS_22_TO_38` (来源: INFINEON_AURIX2G)
  - `BITS_23_TO_39` (来源: INFINEON_AURIX2G)
  - `BITS_24_TO_40` (来源: INFINEON_AURIX2G)
  - `BITS_25_TO_41` (来源: INFINEON_AURIX2G)
  - `BITS_26_TO_42` (来源: INFINEON_AURIX2G)
  - `BITS_27_TO_43` (来源: INFINEON_AURIX2G)
  - `BITS_28_TO_44` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the position of the CIC output shifter, which is to be used to select the valid output bits from the CIC filter. This is valid only during execution of the calibration algorithm.

######## 2. DsadcCICDecimationRate

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f77c6ccc`
- **参数名**: `DsadcCICDecimationRate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_CIC_DECIMATION_RATE_8`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_CIC_DECIMATION_RATE_8` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_16` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_32` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_64` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_128` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_256` (来源: INFINEON_AURIX2G)
  - `DSADC_CIC_DECIMATION_RATE_512` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines Decimation factor for the CIC filter. This is for only valid during execution of the calibration algorithm.

##### 21. DsadcComparatorConfiguration

**容器属性**:

- **UUID**: `e2ada5c3-12ab-4571-b5ee-759cd5434db0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcComparatorConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container provides configuration parameters for comparator configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DsadcLowerBoundaryValue

- **UUID**: `f807a909-ab39-4628-8111-68665be76339`
- **参数名**: `DsadcLowerBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the lower boundary used for limit checking.

######## 2. DsadcUpperBoundaryValue

- **UUID**: `d6ea9dd9-1d6e-4d4b-b3a3-24e9f80c6ccc`
- **参数名**: `DsadcUpperBoundaryValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the upper boundary used for limit checking.

####### ENUMERATION 类型参数

######## 1. DsadcComparatorEventSelect

- **UUID**: `ff120d55-9be8-48c1-ac48-4e1270732d0f`
- **参数名**: `DsadcComparatorEventSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_RESULT_ALWAYS`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_RESULT_ALWAYS` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_INSIDE_RANGE` (来源: INFINEON_AURIX2G)
  - `DSADC_RESULT_OUTSIDE_RANGE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the comparator mode selected to generate an alarm event (and also a service request, if selected auxiliary service request generation).

##### 22. DsadcOvershootCompenConfig

**容器属性**:

- **UUID**: `7fd025de-907b-4268-b461-e379b30f3bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DsadcOvershootCompenConfig`
- **多重性**: [0..1]

**容器描述**:

This container configures the parameters for ERU input triggering

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. DsadcStepDetectionThreshold

- **UUID**: `c0af7dc5-4445-4b46-8ec3-e2194a3e68ae`
- **参数名**: `DsadcStepDetectionThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..2047]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines the threshold value (magnitude) used for step detection. The threshold value is DsadcStepDetectionThreshold * 32

####### ENUMERATION 类型参数

######## 1. DsadcStepDetectionMode

- **UUID**: `f3cc0efc-5fb1-4a43-a04d-0cac5d6c6682`
- **参数名**: `DsadcStepDetectionMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_STEP_DETECT_CMP_LAST`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_STEP_DETECT_CMP_LAST` (来源: INFINEON_AURIX2G)
  - `DSADC_STEP_DETECT_CMP_SEC_LAST` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the when the slew rate filter has to be activated

######## 2. DsadcSlewRateFilterStrength

- **UUID**: `67ad9852-f061-486d-b362-7bc53c40d431`
- **参数名**: `DsadcSlewRateFilterStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_MINIMUM_FILTER_EFFECT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_MINIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_WEAK_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MEDIUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
  - `DSADC_MAXIMUM_FILTER_EFFECT` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the filter strength for the slew rate filter

######## 3. DsadcSlewRateFilterRunTime

- **UUID**: `a3c267ec-3099-4508-925c-09650a25f4bc`
- **参数名**: `DsadcSlewRateFilterRunTime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DSADC_SLEWRATE_FILTR_RUNTIME_2`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DSADC_SLEWRATE_FILTR_RUNTIME_2` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_4` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_8` (来源: INFINEON_AURIX2G)
  - `DSADC_SLEWRATE_FILTR_RUNTIME_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the time constant for the slew rate filter

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AURIX2G

- **UUID**: `ECUC:AURIX2G`
- **包名称**: `AURIX2G`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Dsadc**
