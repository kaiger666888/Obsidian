# Port - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:15

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Port](#port)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Port

#### 基本信息

- **UUID**: `ECUC:b7b62808-1e4b-40ce-b615-cf71937a43e1`
- **模块名称**: `Port`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the Port module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. PortConfigSet

**容器属性**:

- **UUID**: `ECUC:d97c27ef-38b0-4bdf-8384-d10c0a3bba83`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortConfigSet`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration parameters and sub containers of the Port module.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. PortContainer

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-8713-ac864fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortContainer`
- **多重性**: [17..17]

**容器描述**:

Container collecting the PortPins.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. PortNumber

- **UUID**: `ECUC:7356db38-0423-454b-ba4f-7e399810f532`
- **参数名**: `PortNumber`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..40]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The specified port number of this PortContainer.

########## 2. PortNumberOfPortPins

- **UUID**: `ECUC:7356db38-0423-454b-ba4f-7e399210f532`
- **参数名**: `PortNumberOfPortPins`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `13`
- **取值范围**: [1..16]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The number of specified PortPins in this PortContainer.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. PortPin

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortPin`
- **多重性**: [1..16]

**容器描述**:

Configuration of the individual port pins.

########## 参数配置

此容器包含 **15** 个参数：

########### INTEGER 类型参数

############ 1. PortPinId

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortPinId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..654]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pin Id of the port pin. This value will be assigned to the symbolic name derived from the port pin container short name.

########### BOOLEAN 类型参数

############ 1. PortPinDirectionChangeable

- **UUID**: `ECUC:686de592-2deb-4cdb-a0d1-e99d6f499e1b`
- **参数名**: `PortPinDirectionChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Parameter to indicate if the direction is changeable on a port pin during runtime.
                                  true: Port Pin direction changeable enabled.
                                  false: Port Pin direction changeable disabled.

############ 2. PortPinModeChangeable

- **UUID**: `ECUC:512d1759-4b72-4f02-bdec-2faa5bb45295`
- **参数名**: `PortPinModeChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Parameter to indicate if the mode is changeable on a port pin during runtime. True: Port Pin mode changeable allowed. False: Port Pin mode changeable not permitted.

############ 3. PortPinEmergencyStop

- **UUID**: `ECUC:90fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinEmergencyStop`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Parameter to enable/disable the Emergency Stop functionality of a pin configured as an output pin.                               With this feature enabled, an output pin will automatically be reconfigured as an input pin when emergency conditions are encountered.

########### STRING 类型参数

############ 1. PortPinSymbolicName

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22dd3da0c927`
- **参数名**: `PortPinSymbolicName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `PORT_0_PIN_0`
- **描述**: Symbolic name of the Port Pin.

########### ENUMERATION 类型参数

############ 1. PortPinDirection

- **UUID**: `ECUC:038b480e-bd05-4336-a32a-bf7cb3a68c2e`
- **参数名**: `PortPinDirection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_IN`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_OUT` (来源: AUTOSAR_ECUC)
- **描述**: The initial direction of the pin (IN or OUT). If the direction is not changeable, the value configured here is fixed.

############ 2. PortPinInitialMode

- **UUID**: `ECUC:c95f0a90-5907-4ef7-9b50-3584bb8538ba`
- **参数名**: `PortPinInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPIO`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `GPIO` (来源: AUTOSAR_ECUC)
  - `ALT1` (来源: AUTOSAR_ECUC)
  - `ALT2` (来源: AUTOSAR_ECUC)
  - `ALT3` (来源: AUTOSAR_ECUC)
  - `ALT4` (来源: AUTOSAR_ECUC)
  - `ALT5` (来源: AUTOSAR_ECUC)
  - `ALT6` (来源: AUTOSAR_ECUC)
  - `ALT7` (来源: AUTOSAR_ECUC)
- **描述**: Port pin mode from mode list for use with Port_Init() function.

############ 3. PortPinLevelValue

- **UUID**: `ECUC:83fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinLevelValue`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_LEVEL_LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_LEVEL_HIGH` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_LEVEL_LOW` (来源: AUTOSAR_ECUC)
- **描述**: Port Pin Level value from Port pin list.

############ 4. PortPinMode

- **UUID**: `ECUC:ff163464-81af-4158-8eeb-53f4fa69f397`
- **参数名**: `PortPinMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..8]
- **默认值**: `PORT_PIN_MODE_ALL`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ALL` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_GPIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT1` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT2` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT3` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT4` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT5` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT6` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT7` (来源: AUTOSAR_ECUC)
- **描述**: Supported modes for Port pin from mode list.

############ 5. PortPinInputPullResistor

- **UUID**: `ECUC:84fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinInputPullResistor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_IN_PULL_UP`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN_PULL_UP` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_IN_PULL_DOWN` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_IN_NO_PULL` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to indicate to the driver what type of internal Pull resistor [up/down] is to be connected to the PORT Pin.

############ 6. PortPinOutputPadDriveStrength

- **UUID**: `ECUC:85fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinOutputPadDriveStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_DEFAULT_DRIVER`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_STRONG_DRIVER_SHARP_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_STRONG_DRIVER_MEDIUM_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_MEDIUM_DRIVER_SHARP_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_MEDIUM_DRIVER` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_RGMII_DRIVER` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_DEFAULT_DRIVER` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to configure the output drive strength and slew rate of a PORT pin.

############ 7. PortPinOutputPinDriveMode

- **UUID**: `ECUC:86fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinOutputPinDriveMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_OUT_PUSHPULL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_OUT_PUSHPULL` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_OUT_OPENDRAIN` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to indicate how the output of the pad is to be connected to the package pin.

############ 8. PortPinInputPadLevel

- **UUID**: `ECUC:88fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinInputPadLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_INPUT_LEVEL_CMOS_AUTOMOTIVE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_INPUT_LEVEL_CMOS_AUTOMOTIVE` (来源: INFINEON_AURIX2G)
  - `PORT_INPUT_LEVEL_TTL_3_3V` (来源: INFINEON_AURIX2G)
  - `PORT_INPUT_LEVEL_TTL_5_0V` (来源: INFINEON_AURIX2G)
  - `PORT_RGMII_INPUT` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select between TTL and automotive level for input function of Port Pin.

############ 9. PortPinEnableAnalogInputOnly

- **UUID**: `ECUC:89fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinEnableAnalogInputOnly`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_ANALOG_INPUT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_ANALOG_INPUT_DISABLE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_ANALOG_INPUT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter allows configuration of the PDISC register.                                 Range:                                 ENABLE: Pin has support for Analog Input.                               DISABLE: Pin do not have support for Analog Input.

############ 10. PortPinControllerSelect

- **UUID**: `ECUC:91fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinControllerSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DISABLE` (来源: INFINEON_AURIX2G)
  - `ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: With this feature enabled, certain controllers can be allowed to take control of certain ports [e.g. SCR, VADC, ETH and SMU].

######### 2. PortLVDS

**容器属性**:

- **UUID**: `ECUC:1068f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortLVDS`
- **多重性**: [0..4]

**容器描述**:

Configuration of the individual port pins.

########## 参数配置

此容器包含 **9** 个参数：

########### BOOLEAN 类型参数

############ 1. PortLVDSRxPathEnable

- **UUID**: `ECUC:81633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSRxPathEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies whether the Pin-Pair is in LVDS mode or CMOS mode.

############ 2. PortLVDSTxPathEnable

- **UUID**: `ECUC:c1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxPathEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies whether the Pin-Pair is in LVDS mode or CMOS mode.

########### STRING 类型参数

############ 1. PortLVDSPinPair

- **UUID**: `ECUC:61633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSPinPair`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `Pin_X_Pin_Y`
- **描述**: Parameter identifies the PortPinPair supporting the LVDS feature..

########### ENUMERATION 类型参数

############ 1. PortLVDSRxEnController

- **UUID**: `ECUC:71633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSRxEnController`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_CONTROLLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_CONTROLLED` (来源: INFINEON_AURIX2G)
  - `HSCT_CONTROLLED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines who controls the LVDS enable/disable function - PORT controlled or HSCT controlled.

############ 2. PortLVDSRxTerminationMode

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0ce27`
- **参数名**: `PortLVDSRxTerminationMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INTERNAL_TERMINATION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INTERNAL_TERMINATION` (来源: INFINEON_AURIX2G)
  - `EXTERNAL_TERMINATION` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the internal load capacitance,                                 EXTERNAL_TERMINATION selects external termination on the PCB,                                 INTERNAL_TERMINATION selects an 100ohm Receiver internal termination

############ 3. PortLVDSMode

- **UUID**: `ECUC:a1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LVDSH`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `LVDSH` (来源: INFINEON_AURIX2G)
  - `LVDSM` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select reduced frequency mode ?LVDS-M? of the receiver

############ 4. PortLVDSPadSupply

- **UUID**: `ECUC:a1733d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSPadSupply`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `V3_3`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `V3_3` (来源: INFINEON_AURIX2G)
  - `V5_0` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select  pad supply value

############ 5. PortLVDSTxEnController

- **UUID**: `ECUC:b1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxEnController`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_CONTROLLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_CONTROLLED` (来源: INFINEON_AURIX2G)
  - `HSCT_CONTROLLED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines who controls the LVDS enable/disable function - PORT controlled or HSCT controlled.

############ 6. PortLVDSTxPowerDownPullDown

- **UUID**: `ECUC:d1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxPowerDownPullDown`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ENABLE` (来源: INFINEON_AURIX2G)
  - `DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter specifies the state of the Transmit Pull down resistor.

####### 2. PortPin

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortPin`
- **多重性**: [1..16]

**容器描述**:

Configuration of the individual port pins.

######## 参数配置

此容器包含 **15** 个参数：

######### INTEGER 类型参数

########## 1. PortPinId

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortPinId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..654]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pin Id of the port pin. This value will be assigned to the symbolic name derived from the port pin container short name.

######### BOOLEAN 类型参数

########## 1. PortPinDirectionChangeable

- **UUID**: `ECUC:686de592-2deb-4cdb-a0d1-e99d6f499e1b`
- **参数名**: `PortPinDirectionChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Parameter to indicate if the direction is changeable on a port pin during runtime.
                                  true: Port Pin direction changeable enabled.
                                  false: Port Pin direction changeable disabled.

########## 2. PortPinModeChangeable

- **UUID**: `ECUC:512d1759-4b72-4f02-bdec-2faa5bb45295`
- **参数名**: `PortPinModeChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Parameter to indicate if the mode is changeable on a port pin during runtime. True: Port Pin mode changeable allowed. False: Port Pin mode changeable not permitted.

########## 3. PortPinEmergencyStop

- **UUID**: `ECUC:90fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinEmergencyStop`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Parameter to enable/disable the Emergency Stop functionality of a pin configured as an output pin.                               With this feature enabled, an output pin will automatically be reconfigured as an input pin when emergency conditions are encountered.

######### STRING 类型参数

########## 1. PortPinSymbolicName

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22dd3da0c927`
- **参数名**: `PortPinSymbolicName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `PORT_0_PIN_0`
- **描述**: Symbolic name of the Port Pin.

######### ENUMERATION 类型参数

########## 1. PortPinDirection

- **UUID**: `ECUC:038b480e-bd05-4336-a32a-bf7cb3a68c2e`
- **参数名**: `PortPinDirection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_IN`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_OUT` (来源: AUTOSAR_ECUC)
- **描述**: The initial direction of the pin (IN or OUT). If the direction is not changeable, the value configured here is fixed.

########## 2. PortPinInitialMode

- **UUID**: `ECUC:c95f0a90-5907-4ef7-9b50-3584bb8538ba`
- **参数名**: `PortPinInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPIO`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `GPIO` (来源: AUTOSAR_ECUC)
  - `ALT1` (来源: AUTOSAR_ECUC)
  - `ALT2` (来源: AUTOSAR_ECUC)
  - `ALT3` (来源: AUTOSAR_ECUC)
  - `ALT4` (来源: AUTOSAR_ECUC)
  - `ALT5` (来源: AUTOSAR_ECUC)
  - `ALT6` (来源: AUTOSAR_ECUC)
  - `ALT7` (来源: AUTOSAR_ECUC)
- **描述**: Port pin mode from mode list for use with Port_Init() function.

########## 3. PortPinLevelValue

- **UUID**: `ECUC:83fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinLevelValue`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_LEVEL_LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_LEVEL_HIGH` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_LEVEL_LOW` (来源: AUTOSAR_ECUC)
- **描述**: Port Pin Level value from Port pin list.

########## 4. PortPinMode

- **UUID**: `ECUC:ff163464-81af-4158-8eeb-53f4fa69f397`
- **参数名**: `PortPinMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..8]
- **默认值**: `PORT_PIN_MODE_ALL`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ALL` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_GPIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT1` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT2` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT3` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT4` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT5` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT6` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT7` (来源: AUTOSAR_ECUC)
- **描述**: Supported modes for Port pin from mode list.

########## 5. PortPinInputPullResistor

- **UUID**: `ECUC:84fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinInputPullResistor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_IN_PULL_UP`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN_PULL_UP` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_IN_PULL_DOWN` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_IN_NO_PULL` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to indicate to the driver what type of internal Pull resistor [up/down] is to be connected to the PORT Pin.

########## 6. PortPinOutputPadDriveStrength

- **UUID**: `ECUC:85fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinOutputPadDriveStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_DEFAULT_DRIVER`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_STRONG_DRIVER_SHARP_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_STRONG_DRIVER_MEDIUM_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_MEDIUM_DRIVER_SHARP_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_MEDIUM_DRIVER` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_RGMII_DRIVER` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_DEFAULT_DRIVER` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to configure the output drive strength and slew rate of a PORT pin.

########## 7. PortPinOutputPinDriveMode

- **UUID**: `ECUC:86fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinOutputPinDriveMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_OUT_PUSHPULL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_OUT_PUSHPULL` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_OUT_OPENDRAIN` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to indicate how the output of the pad is to be connected to the package pin.

########## 8. PortPinInputPadLevel

- **UUID**: `ECUC:88fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinInputPadLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_INPUT_LEVEL_CMOS_AUTOMOTIVE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_INPUT_LEVEL_CMOS_AUTOMOTIVE` (来源: INFINEON_AURIX2G)
  - `PORT_INPUT_LEVEL_TTL_3_3V` (来源: INFINEON_AURIX2G)
  - `PORT_INPUT_LEVEL_TTL_5_0V` (来源: INFINEON_AURIX2G)
  - `PORT_RGMII_INPUT` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select between TTL and automotive level for input function of Port Pin.

########## 9. PortPinEnableAnalogInputOnly

- **UUID**: `ECUC:89fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinEnableAnalogInputOnly`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_ANALOG_INPUT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_ANALOG_INPUT_DISABLE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_ANALOG_INPUT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter allows configuration of the PDISC register.                                 Range:                                 ENABLE: Pin has support for Analog Input.                               DISABLE: Pin do not have support for Analog Input.

########## 10. PortPinControllerSelect

- **UUID**: `ECUC:91fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinControllerSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DISABLE` (来源: INFINEON_AURIX2G)
  - `ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: With this feature enabled, certain controllers can be allowed to take control of certain ports [e.g. SCR, VADC, ETH and SMU].

####### 3. PortLVDS

**容器属性**:

- **UUID**: `ECUC:1068f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortLVDS`
- **多重性**: [0..4]

**容器描述**:

Configuration of the individual port pins.

######## 参数配置

此容器包含 **9** 个参数：

######### BOOLEAN 类型参数

########## 1. PortLVDSRxPathEnable

- **UUID**: `ECUC:81633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSRxPathEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies whether the Pin-Pair is in LVDS mode or CMOS mode.

########## 2. PortLVDSTxPathEnable

- **UUID**: `ECUC:c1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxPathEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies whether the Pin-Pair is in LVDS mode or CMOS mode.

######### STRING 类型参数

########## 1. PortLVDSPinPair

- **UUID**: `ECUC:61633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSPinPair`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `Pin_X_Pin_Y`
- **描述**: Parameter identifies the PortPinPair supporting the LVDS feature..

######### ENUMERATION 类型参数

########## 1. PortLVDSRxEnController

- **UUID**: `ECUC:71633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSRxEnController`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_CONTROLLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_CONTROLLED` (来源: INFINEON_AURIX2G)
  - `HSCT_CONTROLLED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines who controls the LVDS enable/disable function - PORT controlled or HSCT controlled.

########## 2. PortLVDSRxTerminationMode

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0ce27`
- **参数名**: `PortLVDSRxTerminationMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INTERNAL_TERMINATION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INTERNAL_TERMINATION` (来源: INFINEON_AURIX2G)
  - `EXTERNAL_TERMINATION` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the internal load capacitance,                                 EXTERNAL_TERMINATION selects external termination on the PCB,                                 INTERNAL_TERMINATION selects an 100ohm Receiver internal termination

########## 3. PortLVDSMode

- **UUID**: `ECUC:a1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LVDSH`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `LVDSH` (来源: INFINEON_AURIX2G)
  - `LVDSM` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select reduced frequency mode ?LVDS-M? of the receiver

########## 4. PortLVDSPadSupply

- **UUID**: `ECUC:a1733d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSPadSupply`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `V3_3`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `V3_3` (来源: INFINEON_AURIX2G)
  - `V5_0` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select  pad supply value

########## 5. PortLVDSTxEnController

- **UUID**: `ECUC:b1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxEnController`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_CONTROLLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_CONTROLLED` (来源: INFINEON_AURIX2G)
  - `HSCT_CONTROLLED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines who controls the LVDS enable/disable function - PORT controlled or HSCT controlled.

########## 6. PortLVDSTxPowerDownPullDown

- **UUID**: `ECUC:d1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxPowerDownPullDown`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ENABLE` (来源: INFINEON_AURIX2G)
  - `DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter specifies the state of the Transmit Pull down resistor.

##### 2. PortContainer

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-8713-ac864fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortContainer`
- **多重性**: [17..17]

**容器描述**:

Container collecting the PortPins.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. PortNumber

- **UUID**: `ECUC:7356db38-0423-454b-ba4f-7e399810f532`
- **参数名**: `PortNumber`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..40]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The specified port number of this PortContainer.

######## 2. PortNumberOfPortPins

- **UUID**: `ECUC:7356db38-0423-454b-ba4f-7e399210f532`
- **参数名**: `PortNumberOfPortPins`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `13`
- **取值范围**: [1..16]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The number of specified PortPins in this PortContainer.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. PortPin

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortPin`
- **多重性**: [1..16]

**容器描述**:

Configuration of the individual port pins.

######## 参数配置

此容器包含 **15** 个参数：

######### INTEGER 类型参数

########## 1. PortPinId

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortPinId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..654]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pin Id of the port pin. This value will be assigned to the symbolic name derived from the port pin container short name.

######### BOOLEAN 类型参数

########## 1. PortPinDirectionChangeable

- **UUID**: `ECUC:686de592-2deb-4cdb-a0d1-e99d6f499e1b`
- **参数名**: `PortPinDirectionChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Parameter to indicate if the direction is changeable on a port pin during runtime.
                                  true: Port Pin direction changeable enabled.
                                  false: Port Pin direction changeable disabled.

########## 2. PortPinModeChangeable

- **UUID**: `ECUC:512d1759-4b72-4f02-bdec-2faa5bb45295`
- **参数名**: `PortPinModeChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Parameter to indicate if the mode is changeable on a port pin during runtime. True: Port Pin mode changeable allowed. False: Port Pin mode changeable not permitted.

########## 3. PortPinEmergencyStop

- **UUID**: `ECUC:90fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinEmergencyStop`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Parameter to enable/disable the Emergency Stop functionality of a pin configured as an output pin.                               With this feature enabled, an output pin will automatically be reconfigured as an input pin when emergency conditions are encountered.

######### STRING 类型参数

########## 1. PortPinSymbolicName

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22dd3da0c927`
- **参数名**: `PortPinSymbolicName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `PORT_0_PIN_0`
- **描述**: Symbolic name of the Port Pin.

######### ENUMERATION 类型参数

########## 1. PortPinDirection

- **UUID**: `ECUC:038b480e-bd05-4336-a32a-bf7cb3a68c2e`
- **参数名**: `PortPinDirection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_IN`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_OUT` (来源: AUTOSAR_ECUC)
- **描述**: The initial direction of the pin (IN or OUT). If the direction is not changeable, the value configured here is fixed.

########## 2. PortPinInitialMode

- **UUID**: `ECUC:c95f0a90-5907-4ef7-9b50-3584bb8538ba`
- **参数名**: `PortPinInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPIO`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `GPIO` (来源: AUTOSAR_ECUC)
  - `ALT1` (来源: AUTOSAR_ECUC)
  - `ALT2` (来源: AUTOSAR_ECUC)
  - `ALT3` (来源: AUTOSAR_ECUC)
  - `ALT4` (来源: AUTOSAR_ECUC)
  - `ALT5` (来源: AUTOSAR_ECUC)
  - `ALT6` (来源: AUTOSAR_ECUC)
  - `ALT7` (来源: AUTOSAR_ECUC)
- **描述**: Port pin mode from mode list for use with Port_Init() function.

########## 3. PortPinLevelValue

- **UUID**: `ECUC:83fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinLevelValue`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_LEVEL_LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_LEVEL_HIGH` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_LEVEL_LOW` (来源: AUTOSAR_ECUC)
- **描述**: Port Pin Level value from Port pin list.

########## 4. PortPinMode

- **UUID**: `ECUC:ff163464-81af-4158-8eeb-53f4fa69f397`
- **参数名**: `PortPinMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..8]
- **默认值**: `PORT_PIN_MODE_ALL`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ALL` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_GPIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT1` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT2` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT3` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT4` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT5` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT6` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT7` (来源: AUTOSAR_ECUC)
- **描述**: Supported modes for Port pin from mode list.

########## 5. PortPinInputPullResistor

- **UUID**: `ECUC:84fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinInputPullResistor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_IN_PULL_UP`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN_PULL_UP` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_IN_PULL_DOWN` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_IN_NO_PULL` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to indicate to the driver what type of internal Pull resistor [up/down] is to be connected to the PORT Pin.

########## 6. PortPinOutputPadDriveStrength

- **UUID**: `ECUC:85fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinOutputPadDriveStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_DEFAULT_DRIVER`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_STRONG_DRIVER_SHARP_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_STRONG_DRIVER_MEDIUM_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_MEDIUM_DRIVER_SHARP_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_MEDIUM_DRIVER` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_RGMII_DRIVER` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_DEFAULT_DRIVER` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to configure the output drive strength and slew rate of a PORT pin.

########## 7. PortPinOutputPinDriveMode

- **UUID**: `ECUC:86fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinOutputPinDriveMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_OUT_PUSHPULL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_OUT_PUSHPULL` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_OUT_OPENDRAIN` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to indicate how the output of the pad is to be connected to the package pin.

########## 8. PortPinInputPadLevel

- **UUID**: `ECUC:88fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinInputPadLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_INPUT_LEVEL_CMOS_AUTOMOTIVE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_INPUT_LEVEL_CMOS_AUTOMOTIVE` (来源: INFINEON_AURIX2G)
  - `PORT_INPUT_LEVEL_TTL_3_3V` (来源: INFINEON_AURIX2G)
  - `PORT_INPUT_LEVEL_TTL_5_0V` (来源: INFINEON_AURIX2G)
  - `PORT_RGMII_INPUT` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select between TTL and automotive level for input function of Port Pin.

########## 9. PortPinEnableAnalogInputOnly

- **UUID**: `ECUC:89fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinEnableAnalogInputOnly`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_ANALOG_INPUT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_ANALOG_INPUT_DISABLE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_ANALOG_INPUT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter allows configuration of the PDISC register.                                 Range:                                 ENABLE: Pin has support for Analog Input.                               DISABLE: Pin do not have support for Analog Input.

########## 10. PortPinControllerSelect

- **UUID**: `ECUC:91fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinControllerSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DISABLE` (来源: INFINEON_AURIX2G)
  - `ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: With this feature enabled, certain controllers can be allowed to take control of certain ports [e.g. SCR, VADC, ETH and SMU].

####### 2. PortLVDS

**容器属性**:

- **UUID**: `ECUC:1068f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortLVDS`
- **多重性**: [0..4]

**容器描述**:

Configuration of the individual port pins.

######## 参数配置

此容器包含 **9** 个参数：

######### BOOLEAN 类型参数

########## 1. PortLVDSRxPathEnable

- **UUID**: `ECUC:81633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSRxPathEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies whether the Pin-Pair is in LVDS mode or CMOS mode.

########## 2. PortLVDSTxPathEnable

- **UUID**: `ECUC:c1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxPathEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies whether the Pin-Pair is in LVDS mode or CMOS mode.

######### STRING 类型参数

########## 1. PortLVDSPinPair

- **UUID**: `ECUC:61633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSPinPair`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `Pin_X_Pin_Y`
- **描述**: Parameter identifies the PortPinPair supporting the LVDS feature..

######### ENUMERATION 类型参数

########## 1. PortLVDSRxEnController

- **UUID**: `ECUC:71633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSRxEnController`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_CONTROLLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_CONTROLLED` (来源: INFINEON_AURIX2G)
  - `HSCT_CONTROLLED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines who controls the LVDS enable/disable function - PORT controlled or HSCT controlled.

########## 2. PortLVDSRxTerminationMode

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0ce27`
- **参数名**: `PortLVDSRxTerminationMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INTERNAL_TERMINATION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INTERNAL_TERMINATION` (来源: INFINEON_AURIX2G)
  - `EXTERNAL_TERMINATION` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the internal load capacitance,                                 EXTERNAL_TERMINATION selects external termination on the PCB,                                 INTERNAL_TERMINATION selects an 100ohm Receiver internal termination

########## 3. PortLVDSMode

- **UUID**: `ECUC:a1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LVDSH`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `LVDSH` (来源: INFINEON_AURIX2G)
  - `LVDSM` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select reduced frequency mode ?LVDS-M? of the receiver

########## 4. PortLVDSPadSupply

- **UUID**: `ECUC:a1733d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSPadSupply`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `V3_3`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `V3_3` (来源: INFINEON_AURIX2G)
  - `V5_0` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select  pad supply value

########## 5. PortLVDSTxEnController

- **UUID**: `ECUC:b1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxEnController`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_CONTROLLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_CONTROLLED` (来源: INFINEON_AURIX2G)
  - `HSCT_CONTROLLED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines who controls the LVDS enable/disable function - PORT controlled or HSCT controlled.

########## 6. PortLVDSTxPowerDownPullDown

- **UUID**: `ECUC:d1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxPowerDownPullDown`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ENABLE` (来源: INFINEON_AURIX2G)
  - `DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter specifies the state of the Transmit Pull down resistor.

##### 3. PortPin

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortPin`
- **多重性**: [1..16]

**容器描述**:

Configuration of the individual port pins.

###### 参数配置

此容器包含 **15** 个参数：

####### INTEGER 类型参数

######## 1. PortPinId

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortPinId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..654]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pin Id of the port pin. This value will be assigned to the symbolic name derived from the port pin container short name.

####### BOOLEAN 类型参数

######## 1. PortPinDirectionChangeable

- **UUID**: `ECUC:686de592-2deb-4cdb-a0d1-e99d6f499e1b`
- **参数名**: `PortPinDirectionChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Parameter to indicate if the direction is changeable on a port pin during runtime.
                                  true: Port Pin direction changeable enabled.
                                  false: Port Pin direction changeable disabled.

######## 2. PortPinModeChangeable

- **UUID**: `ECUC:512d1759-4b72-4f02-bdec-2faa5bb45295`
- **参数名**: `PortPinModeChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Parameter to indicate if the mode is changeable on a port pin during runtime. True: Port Pin mode changeable allowed. False: Port Pin mode changeable not permitted.

######## 3. PortPinEmergencyStop

- **UUID**: `ECUC:90fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinEmergencyStop`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Parameter to enable/disable the Emergency Stop functionality of a pin configured as an output pin.                               With this feature enabled, an output pin will automatically be reconfigured as an input pin when emergency conditions are encountered.

####### STRING 类型参数

######## 1. PortPinSymbolicName

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22dd3da0c927`
- **参数名**: `PortPinSymbolicName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `PORT_0_PIN_0`
- **描述**: Symbolic name of the Port Pin.

####### ENUMERATION 类型参数

######## 1. PortPinDirection

- **UUID**: `ECUC:038b480e-bd05-4336-a32a-bf7cb3a68c2e`
- **参数名**: `PortPinDirection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_IN`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_OUT` (来源: AUTOSAR_ECUC)
- **描述**: The initial direction of the pin (IN or OUT). If the direction is not changeable, the value configured here is fixed.

######## 2. PortPinInitialMode

- **UUID**: `ECUC:c95f0a90-5907-4ef7-9b50-3584bb8538ba`
- **参数名**: `PortPinInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPIO`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `GPIO` (来源: AUTOSAR_ECUC)
  - `ALT1` (来源: AUTOSAR_ECUC)
  - `ALT2` (来源: AUTOSAR_ECUC)
  - `ALT3` (来源: AUTOSAR_ECUC)
  - `ALT4` (来源: AUTOSAR_ECUC)
  - `ALT5` (来源: AUTOSAR_ECUC)
  - `ALT6` (来源: AUTOSAR_ECUC)
  - `ALT7` (来源: AUTOSAR_ECUC)
- **描述**: Port pin mode from mode list for use with Port_Init() function.

######## 3. PortPinLevelValue

- **UUID**: `ECUC:83fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinLevelValue`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_LEVEL_LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_LEVEL_HIGH` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_LEVEL_LOW` (来源: AUTOSAR_ECUC)
- **描述**: Port Pin Level value from Port pin list.

######## 4. PortPinMode

- **UUID**: `ECUC:ff163464-81af-4158-8eeb-53f4fa69f397`
- **参数名**: `PortPinMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..8]
- **默认值**: `PORT_PIN_MODE_ALL`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ALL` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_GPIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT1` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT2` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT3` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT4` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT5` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT6` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ALT7` (来源: AUTOSAR_ECUC)
- **描述**: Supported modes for Port pin from mode list.

######## 5. PortPinInputPullResistor

- **UUID**: `ECUC:84fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinInputPullResistor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_IN_PULL_UP`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN_PULL_UP` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_IN_PULL_DOWN` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_IN_NO_PULL` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to indicate to the driver what type of internal Pull resistor [up/down] is to be connected to the PORT Pin.

######## 6. PortPinOutputPadDriveStrength

- **UUID**: `ECUC:85fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinOutputPadDriveStrength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_DEFAULT_DRIVER`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_STRONG_DRIVER_SHARP_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_STRONG_DRIVER_MEDIUM_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_MEDIUM_DRIVER_SHARP_EDGE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_MEDIUM_DRIVER` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_RGMII_DRIVER` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_DEFAULT_DRIVER` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to configure the output drive strength and slew rate of a PORT pin.

######## 7. PortPinOutputPinDriveMode

- **UUID**: `ECUC:86fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinOutputPinDriveMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_OUT_PUSHPULL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_OUT_PUSHPULL` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_OUT_OPENDRAIN` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to indicate how the output of the pad is to be connected to the package pin.

######## 8. PortPinInputPadLevel

- **UUID**: `ECUC:88fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinInputPadLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_INPUT_LEVEL_CMOS_AUTOMOTIVE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_INPUT_LEVEL_CMOS_AUTOMOTIVE` (来源: INFINEON_AURIX2G)
  - `PORT_INPUT_LEVEL_TTL_3_3V` (来源: INFINEON_AURIX2G)
  - `PORT_INPUT_LEVEL_TTL_5_0V` (来源: INFINEON_AURIX2G)
  - `PORT_RGMII_INPUT` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select between TTL and automotive level for input function of Port Pin.

######## 9. PortPinEnableAnalogInputOnly

- **UUID**: `ECUC:89fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinEnableAnalogInputOnly`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_PIN_ANALOG_INPUT_DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_ANALOG_INPUT_DISABLE` (来源: INFINEON_AURIX2G)
  - `PORT_PIN_ANALOG_INPUT_ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter allows configuration of the PDISC register.                                 Range:                                 ENABLE: Pin has support for Analog Input.                               DISABLE: Pin do not have support for Analog Input.

######## 10. PortPinControllerSelect

- **UUID**: `ECUC:91fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinControllerSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `DISABLE` (来源: INFINEON_AURIX2G)
  - `ENABLE` (来源: INFINEON_AURIX2G)
- **描述**: With this feature enabled, certain controllers can be allowed to take control of certain ports [e.g. SCR, VADC, ETH and SMU].

##### 4. PortLVDS

**容器属性**:

- **UUID**: `ECUC:1068f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortLVDS`
- **多重性**: [0..4]

**容器描述**:

Configuration of the individual port pins.

###### 参数配置

此容器包含 **9** 个参数：

####### BOOLEAN 类型参数

######## 1. PortLVDSRxPathEnable

- **UUID**: `ECUC:81633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSRxPathEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies whether the Pin-Pair is in LVDS mode or CMOS mode.

######## 2. PortLVDSTxPathEnable

- **UUID**: `ECUC:c1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxPathEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies whether the Pin-Pair is in LVDS mode or CMOS mode.

####### STRING 类型参数

######## 1. PortLVDSPinPair

- **UUID**: `ECUC:61633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSPinPair`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `Pin_X_Pin_Y`
- **描述**: Parameter identifies the PortPinPair supporting the LVDS feature..

####### ENUMERATION 类型参数

######## 1. PortLVDSRxEnController

- **UUID**: `ECUC:71633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSRxEnController`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_CONTROLLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_CONTROLLED` (来源: INFINEON_AURIX2G)
  - `HSCT_CONTROLLED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines who controls the LVDS enable/disable function - PORT controlled or HSCT controlled.

######## 2. PortLVDSRxTerminationMode

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0ce27`
- **参数名**: `PortLVDSRxTerminationMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INTERNAL_TERMINATION`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INTERNAL_TERMINATION` (来源: INFINEON_AURIX2G)
  - `EXTERNAL_TERMINATION` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the internal load capacitance,                                 EXTERNAL_TERMINATION selects external termination on the PCB,                                 INTERNAL_TERMINATION selects an 100ohm Receiver internal termination

######## 3. PortLVDSMode

- **UUID**: `ECUC:a1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LVDSH`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `LVDSH` (来源: INFINEON_AURIX2G)
  - `LVDSM` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select reduced frequency mode ?LVDS-M? of the receiver

######## 4. PortLVDSPadSupply

- **UUID**: `ECUC:a1733d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSPadSupply`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `V3_3`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `V3_3` (来源: INFINEON_AURIX2G)
  - `V5_0` (来源: INFINEON_AURIX2G)
- **描述**: Parameter to select  pad supply value

######## 5. PortLVDSTxEnController

- **UUID**: `ECUC:b1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxEnController`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_CONTROLLED`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_CONTROLLED` (来源: INFINEON_AURIX2G)
  - `HSCT_CONTROLLED` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines who controls the LVDS enable/disable function - PORT controlled or HSCT controlled.

######## 6. PortLVDSTxPowerDownPullDown

- **UUID**: `ECUC:d1633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortLVDSTxPowerDownPullDown`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DISABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ENABLE` (来源: INFINEON_AURIX2G)
  - `DISABLE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter specifies the state of the Transmit Pull down resistor.

##### 5. PortGeneral

**容器属性**:

- **UUID**: `ECUC:9d811d70-8cc9-4c5c-bb07-fc5de786d2ec`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortGeneral`
- **多重性**: [0..1]

**容器描述**:

Module wide configuration parameters of the PORT driver.

###### 参数配置

此容器包含 **7** 个参数：

####### BOOLEAN 类型参数

######## 1. PortDevErrorDetect

- **UUID**: `ECUC:348d2d10-2ba2-4a1e-aaa8-002dac40f627`
- **参数名**: `PortDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 2. PortSetPinDirectionApi

- **UUID**: `ECUC:3fc8ef56-7ddc-49ae-ae97-635ac0a7ab16`
- **参数名**: `PortSetPinDirectionApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pre-processor switch to enable / disable the use of the function Port_SetPinDirection().

######## 3. PortSetPinModeApi

- **UUID**: `ECUC:9be9eec7-c8d6-41d4-a9ca-c27c3c5a83d6`
- **参数名**: `PortSetPinModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pre-processor switch to enable / disable the use of the function Port_SetPinMode().

######## 4. PortVersionInfoApi

- **UUID**: `ECUC:512568ee-3407-4c5d-bd4c-6a0b65a84fba`
- **参数名**: `PortVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

######## 5. PortSafetyEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b17`
- **参数名**: `PortSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enable/Disable the Safety check and all associated notifications.

######## 6. PortInitCheckApi

- **UUID**: `ECUC:dbfab416-7231-4c9e-b7a2-2580d8484ecf`
- **参数名**: `PortInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Adds / removes the service  Port_InitCheck() from the code.

####### ENUMERATION 类型参数

######## 1. PortInitApiMode

- **UUID**: `ECUC:92c9cf6f-e2a3-45c4-af10-157a0b5ab06b`
- **参数名**: `PortInitApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PORT_MCAL_SUPERVISOR`
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `PORT_MCAL_USER1` (来源: INFINEON_AURIX2G)
  - `PORT_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
- **描述**: This configuration parameter defines the mode in which the Port Init  API will be used.

##### 6. CommonPublishedInformation

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
- **默认值**: `124`
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

1. **Port**
