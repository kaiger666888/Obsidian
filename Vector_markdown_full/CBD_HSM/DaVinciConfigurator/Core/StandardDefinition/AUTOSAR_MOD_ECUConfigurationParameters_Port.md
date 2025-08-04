# Port - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:57

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Port](#port)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Port

#### 基本信息

- **UUID**: `ECUC:b7b62808-1e4b-40ce-b615-cf71937a43e1`
- **模块名称**: `Port`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Port module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. PortConfigSet

**容器属性**:

- **UUID**: `ECUC:d97c27ef-38b0-4bdf-8384-d10c0a3bba83`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container is the base of a multiple configuration set

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. PortContainer

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-8713-ac864fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortContainer`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container collecting the PortPins.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. PortNumberOfPortPins

- **UUID**: `ECUC:7356db38-0423-454b-ba4f-7e399810f532`
- **参数名**: `PortNumberOfPortPins`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The number of specified PortPins in this PortContainer.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. PortPin

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortPin`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of the individual port pins.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. PortPinId

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortPinId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pin Id of the port pin. This value will be assigned to the symbolic name derived from the port pin container short name.

########### BOOLEAN 类型参数

############ 1. PortPinDirectionChangeable

- **UUID**: `ECUC:686de592-2deb-4cdb-a0d1-e99d6f499e1b`
- **参数名**: `PortPinDirectionChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to indicate if the direction is changeable on a port pin during runtime.

############ 2. PortPinModeChangeable

- **UUID**: `ECUC:512d1759-4b72-4f02-bdec-2faa5bb45295`
- **参数名**: `PortPinModeChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to indicate if the mode is changeable on a port pin during runtime. True: Port Pin mode changeable allowed. False: Port Pin mode changeable not permitted.

########### ENUMERATION 类型参数

############ 1. PortPinDirection

- **UUID**: `ECUC:038b480e-bd05-4336-a32a-bf7cb3a68c2e`
- **参数名**: `PortPinDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_OUT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The initial direction of the pin (IN or OUT). If the direction is not changeable, the value configured here is fixed.

############ 2. PortPinInitialMode

- **UUID**: `ECUC:c95f0a90-5907-4ef7-9b50-3584bb8538ba`
- **参数名**: `PortPinInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ADC` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_CAN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_GPT` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_WDG` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ICU` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_LIN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_MEM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_PWM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_SPI` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port pin mode from mode list for use with Port_Init() function.

############ 3. PortPinLevelValue

- **UUID**: `ECUC:83fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinLevelValue`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_LEVEL_HIGH` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_LEVEL_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port Pin Level value from Port pin list.

############ 4. PortPinMode

- **UUID**: `ECUC:ff163464-81af-4158-8eeb-53f4fa69f397`
- **参数名**: `PortPinMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ADC` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_CAN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_GPT` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_WDG` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ICU` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_LIN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_MEM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_PWM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_SPI` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port pin mode from mode list.

####### 2. PortPin

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortPin`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of the individual port pins.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. PortPinId

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortPinId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pin Id of the port pin. This value will be assigned to the symbolic name derived from the port pin container short name.

######### BOOLEAN 类型参数

########## 1. PortPinDirectionChangeable

- **UUID**: `ECUC:686de592-2deb-4cdb-a0d1-e99d6f499e1b`
- **参数名**: `PortPinDirectionChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to indicate if the direction is changeable on a port pin during runtime.

########## 2. PortPinModeChangeable

- **UUID**: `ECUC:512d1759-4b72-4f02-bdec-2faa5bb45295`
- **参数名**: `PortPinModeChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to indicate if the mode is changeable on a port pin during runtime. True: Port Pin mode changeable allowed. False: Port Pin mode changeable not permitted.

######### ENUMERATION 类型参数

########## 1. PortPinDirection

- **UUID**: `ECUC:038b480e-bd05-4336-a32a-bf7cb3a68c2e`
- **参数名**: `PortPinDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_OUT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The initial direction of the pin (IN or OUT). If the direction is not changeable, the value configured here is fixed.

########## 2. PortPinInitialMode

- **UUID**: `ECUC:c95f0a90-5907-4ef7-9b50-3584bb8538ba`
- **参数名**: `PortPinInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ADC` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_CAN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_GPT` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_WDG` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ICU` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_LIN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_MEM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_PWM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_SPI` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port pin mode from mode list for use with Port_Init() function.

########## 3. PortPinLevelValue

- **UUID**: `ECUC:83fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinLevelValue`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_LEVEL_HIGH` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_LEVEL_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port Pin Level value from Port pin list.

########## 4. PortPinMode

- **UUID**: `ECUC:ff163464-81af-4158-8eeb-53f4fa69f397`
- **参数名**: `PortPinMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ADC` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_CAN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_GPT` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_WDG` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ICU` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_LIN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_MEM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_PWM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_SPI` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port pin mode from mode list.

##### 2. PortContainer

**容器属性**:

- **UUID**: `ECUC:6aa61659-c6de-4d25-8713-ac864fdf5e37`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortContainer`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container collecting the PortPins.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. PortNumberOfPortPins

- **UUID**: `ECUC:7356db38-0423-454b-ba4f-7e399810f532`
- **参数名**: `PortNumberOfPortPins`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The number of specified PortPins in this PortContainer.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. PortPin

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortPin`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of the individual port pins.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. PortPinId

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortPinId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pin Id of the port pin. This value will be assigned to the symbolic name derived from the port pin container short name.

######### BOOLEAN 类型参数

########## 1. PortPinDirectionChangeable

- **UUID**: `ECUC:686de592-2deb-4cdb-a0d1-e99d6f499e1b`
- **参数名**: `PortPinDirectionChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to indicate if the direction is changeable on a port pin during runtime.

########## 2. PortPinModeChangeable

- **UUID**: `ECUC:512d1759-4b72-4f02-bdec-2faa5bb45295`
- **参数名**: `PortPinModeChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to indicate if the mode is changeable on a port pin during runtime. True: Port Pin mode changeable allowed. False: Port Pin mode changeable not permitted.

######### ENUMERATION 类型参数

########## 1. PortPinDirection

- **UUID**: `ECUC:038b480e-bd05-4336-a32a-bf7cb3a68c2e`
- **参数名**: `PortPinDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_OUT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The initial direction of the pin (IN or OUT). If the direction is not changeable, the value configured here is fixed.

########## 2. PortPinInitialMode

- **UUID**: `ECUC:c95f0a90-5907-4ef7-9b50-3584bb8538ba`
- **参数名**: `PortPinInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ADC` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_CAN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_GPT` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_WDG` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ICU` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_LIN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_MEM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_PWM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_SPI` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port pin mode from mode list for use with Port_Init() function.

########## 3. PortPinLevelValue

- **UUID**: `ECUC:83fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinLevelValue`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_LEVEL_HIGH` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_LEVEL_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port Pin Level value from Port pin list.

########## 4. PortPinMode

- **UUID**: `ECUC:ff163464-81af-4158-8eeb-53f4fa69f397`
- **参数名**: `PortPinMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ADC` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_CAN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_GPT` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_WDG` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ICU` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_LIN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_MEM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_PWM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_SPI` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port pin mode from mode list.

##### 3. PortPin

**容器属性**:

- **UUID**: `ECUC:1768f065-a030-4205-8de9-30b561da3ba3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortPin`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of the individual port pins.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. PortPinId

- **UUID**: `ECUC:91633d90-a96c-46a2-b4fb-22d23da0c927`
- **参数名**: `PortPinId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pin Id of the port pin. This value will be assigned to the symbolic name derived from the port pin container short name.

####### BOOLEAN 类型参数

######## 1. PortPinDirectionChangeable

- **UUID**: `ECUC:686de592-2deb-4cdb-a0d1-e99d6f499e1b`
- **参数名**: `PortPinDirectionChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to indicate if the direction is changeable on a port pin during runtime.

######## 2. PortPinModeChangeable

- **UUID**: `ECUC:512d1759-4b72-4f02-bdec-2faa5bb45295`
- **参数名**: `PortPinModeChangeable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to indicate if the mode is changeable on a port pin during runtime. True: Port Pin mode changeable allowed. False: Port Pin mode changeable not permitted.

####### ENUMERATION 类型参数

######## 1. PortPinDirection

- **UUID**: `ECUC:038b480e-bd05-4336-a32a-bf7cb3a68c2e`
- **参数名**: `PortPinDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_IN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_OUT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The initial direction of the pin (IN or OUT). If the direction is not changeable, the value configured here is fixed.

######## 2. PortPinInitialMode

- **UUID**: `ECUC:c95f0a90-5907-4ef7-9b50-3584bb8538ba`
- **参数名**: `PortPinInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ADC` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_CAN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_GPT` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_WDG` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ICU` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_LIN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_MEM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_PWM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_SPI` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port pin mode from mode list for use with Port_Init() function.

######## 3. PortPinLevelValue

- **UUID**: `ECUC:83fdd686-ae98-423f-bdfb-c46dad6783f4`
- **参数名**: `PortPinLevelValue`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_LEVEL_HIGH` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_LEVEL_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port Pin Level value from Port pin list.

######## 4. PortPinMode

- **UUID**: `ECUC:ff163464-81af-4158-8eeb-53f4fa69f397`
- **参数名**: `PortPinMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PORT_PIN_MODE_ADC` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_CAN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_GPT` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_DIO_WDG` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_ICU` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_LIN` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_MEM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_PWM` (来源: AUTOSAR_ECUC)
  - `PORT_PIN_MODE_SPI` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Port pin mode from mode list.

##### 4. PortGeneral

**容器属性**:

- **UUID**: `ECUC:9d811d70-8cc9-4c5c-bb07-fc5de786d2ec`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PortGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Module wide configuration parameters of the PORT driver.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. PortDevErrorDetect

- **UUID**: `ECUC:348d2d10-2ba2-4a1e-aaa8-002dac40f627`
- **参数名**: `PortDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification on or off.

######## 2. PortSetPinDirectionApi

- **UUID**: `ECUC:3fc8ef56-7ddc-49ae-ae97-635ac0a7ab16`
- **参数名**: `PortSetPinDirectionApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the use of the function Port_SetPinDirection().

######## 3. PortSetPinModeApi

- **UUID**: `ECUC:9be9eec7-c8d6-41d4-a9ca-c27c3c5a83d6`
- **参数名**: `PortSetPinModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the use of the function Port_SetPinMode().

######## 4. PortVersionInfoApi

- **UUID**: `ECUC:512568ee-3407-4c5d-bd4c-6a0b65a83fba`
- **参数名**: `PortVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AUTOSAR

- **UUID**: `ECUC:AUTOSAR`
- **包名称**: `AUTOSAR`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Port**
