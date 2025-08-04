# I2c - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:00

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [I2c](#i2c)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. I2c

#### 基本信息

- **UUID**: `8788921c-faeb-4ba6-b8a6-488a1ff0c840`
- **模块名称**: `I2c`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD-SELECTABLE
  - VARIANT-PRE-COMPILE

#### 模块描述

Inter-Integrated Circuit. The driver provides services for reading from and writing to devices connected via I2c buses. It provides access to I2c communication to several users (e.g. EEPROM, Watchdog, I/O ASICs) and the required mechanism to configure the onchip I2c peripheral.

#I2c #Driver
#MICROSAR #Vector

#### 版本历史

共有 **8** 个版本记录：

##### 1. 版本 2.00.00

- **发布日期**: 2019-10-18T07:56:36+02:00
- **发布者**: virmcn

**变更内容**:

##### 2. 版本 2.00.01

- **状态**: released
- **发布日期**: 2020-06-29T14:43:47+02:00
- **发布者**: virpam

**变更内容**:

##### 3. 版本 2.01.00

- **状态**: release
- **发布日期**: 2020-09-18T09:19:17+02:00
- **发布者**: virnba

**变更内容**:

##### 4. 版本 2.01.01

- **状态**: release
- **发布日期**: 2021-03-26T16:48:49+01:00
- **发布者**: virwsl

**变更内容**:

##### 5. 版本 2.01.02

- **状态**: release
- **发布日期**: 2021-04-12T11:17:24+02:00
- **发布者**: virnba

**变更内容**:

##### 6. 版本 3.00.00

- **状态**: release
- **发布日期**: 2022-05-19T10:51:24+02:00
- **发布者**: kscherk

**变更内容**:

##### 7. 版本 3.02.00

- **状态**: release
- **发布日期**: 2022-10-25T10:36:13+02:00
- **发布者**: rwerhahn

**变更内容**:

##### 8. 版本 3.03.00

- **状态**: release
- **发布日期**: 2023-08-22T14:08:45+02:00
- **发布者**: virzln

**变更内容**:

#### 配置容器

本模块包含 **11** 个配置容器：

##### 1. I2cConfigSet

**容器属性**:

- **UUID**: `4f17aa9d-4f6f-419b-9bfd-99ae63a530ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cConfigSet`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This container includes the base for a multiple configuration set.

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. I2cChannel

**容器属性**:

- **UUID**: `f5c21f19-3d77-4e6d-9283-79426582c30a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Channel specific configuration parameters of the I2c.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. I2cChannelId

- **UUID**: `e865ffcd-4289-435f-a006-5d5551a731bd`
- **参数名**: `I2cChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the identifier of a channel.

########## 2. I2cDeviceAddress

- **UUID**: `09de9803-2684-4c4d-a571-abc80cd4725b`
- **参数名**: `I2cDeviceAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1023]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the address of a slave device which is accessed by the master.

########## 3. I2cDefaultData

- **UUID**: `1452cca8-d3c5-4fa5-bf8d-a42cbbc3be57`
- **参数名**: `I2cDefaultData`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the default value of the channel.

Note: The default data is transmitted in case of TxBuffer and RxBuffer of the channel is set to NULL_PTR (e.g. via API I2c_SetupEB).

######### BOOLEAN 类型参数

########## 1. I2cChainChannel

- **UUID**: `e8594ea3-5a69-4186-9c2e-ef4abcc25c93`
- **参数名**: `I2cChainChannel`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the channel is chained.

True: The channel is chained.
False: The channel is not chained.

Note: A chained channel requires follow up to be set. It does not set a restart condition and the retransmission of the slave address is ommited.

####### 2. I2cBus

**容器属性**:

- **UUID**: `dcbd473b-5cd0-468a-8ea7-e6a669dde771`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cBus`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Bus specific configuration parameters of the I2c.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. I2cBusId

- **UUID**: `96aa5ffd-711b-41d0-8b03-7ac56de8a386`
- **参数名**: `I2cBusId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the identifier of a bus.

########## 2. I2cTransferRate

- **UUID**: `ef0c7b38-325e-48bd-9647-3854784df029`
- **参数名**: `I2cTransferRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [100..1001]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the baudrate of the bus in KHz.

######### FLOAT 类型参数

########## 1. I2cTimeout

- **UUID**: `34f6caf6-e628-4afe-b7da-da69c7e50f4c`
- **参数名**: `I2cTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the timeout for I2c in ms.

Note: If the timeout expires, the driver applies the configured timeout handling (via API I2c_SetTimeoutHandling).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. I2cHwUnitAssignment

- **UUID**: `0818a5b4-53ce-4cac-bc63-4f45382c241d`
- **引用名**: `I2cHwUnitAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cHardwareUnit`
- **完整路径**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c/I2cConfigSet/I2cHardwareUnit`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the I2cHardwareUnit to which the bus is assigned.

####### 3. I2cHardwareUnit

**容器属性**:

- **UUID**: `2733920f-d591-4c89-b6ed-a8c0b9732906`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cHardwareUnit`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Hardware unit specific configuration parameters of the I2c.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. I2cUnitId

- **UUID**: `3e38d81a-49d6-4bb9-bd43-3fab5c048cef`
- **参数名**: `I2cUnitId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the identifier of the hardware unit.

########## 2. I2cClockDivider

- **UUID**: `a5fe77c3-2c96-434b-ab23-fe1db71332f0`
- **参数名**: `I2cClockDivider`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter sets the clock divider for the i2c module.

########## 3. I2cDelayStageSDA

- **UUID**: `7c435407-4ca7-41a2-b981-49d2e6bb7bb6`
- **参数名**: `I2cDelayStageSDA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: SDA Delay stages for data hold time. The standard delay time is 0x00.
note: SDA delay from the SCL falling edge. This  will also affect SDA setup time relative to the next SCL rising edge.

######### FLOAT 类型参数

########## 1. I2cClockFrequencyManual

- **UUID**: `7753a951-68e7-408c-9ed5-e99f46346eb0`
- **参数名**: `I2cClockFrequencyManual`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `8000000`
- **取值范围**: [1..1.7976931348623157E+308]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the clock rate (in MHz) of the I2C hardware unit.

Note: This parameter is used to calculate baudrate settings in case the reference I2cClockConfiguration is not configured.

######### ENUMERATION 类型参数

########## 1. I2cPortSelect

- **UUID**: `5d9fa2ea-051e-418e-8e13-027e8152136f`
- **参数名**: `I2cPortSelect`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `PORTA`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `PORTA`
  - `PORTB`
  - `PORTC`
  - `PORTD`
  - `PORTE`
  - `PORTF`
  - `PORTG`
  - `PORTH`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifices the selected pins providing the serial data (SDA) and clock (SCL) signals.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. I2cHardwareConfigurationRef

- **UUID**: `f478442a-9470-4111-a545-7c60d441ed71`
- **引用名**: `I2cHardwareConfigurationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cHardwareConfiguration`
- **完整路径**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c/I2cHardwareConfiguration`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a hardware configuration.

######### CHOICE-REFERENCE 类型引用

########## 1. I2cClockConfiguration

- **UUID**: `1be475dc-e15b-4085-a2b3-30b24c033504`
- **引用名**: `I2cClockConfiguration`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
  - `/AUTOSAR/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a McuClockReferencePoint which is used to calculate the baudrate settings for transmissions on a hardware unit.

Note: If this parameter is set the clock is derived from the MCU.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. I2cRecovery

**容器属性**:

- **UUID**: `d38c917a-0a1c-4569-9b54-ad46d02722a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cRecovery`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes parameters which are required to perform I2c bus free.

########## 引用关系

此容器包含 **2** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. I2cPortPinScl

- **UUID**: `b49077fe-86ba-41ca-afce-b89240c037b1`
- **引用名**: `I2cPortPinScl`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Port/PortConfigSet/PortContainer/PortPin`
  - `/AUTOSAR/Port/PortConfigSet/PortContainer/PortPin`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PortPin which is used for pin mode switching.

Note: In case the module needs to apply the 'bus free' procedure the referenced PortPin is set do Dio mode and used to generate clock pulses. After the 'bus free' procedure the pin automatically gets set back to I2C mode.

############ 2. I2cDioSclPin

- **UUID**: `e39f19f2-0581-4f3a-8d78-1610c90c8dd9`
- **引用名**: `I2cDioSclPin`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioPort/DioChannel`
  - `/AUTOSAR/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/Dio/DioPort/DioChannel`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Dio pin, which is used for Bus Free and read the status of the SCL pin.

Note: Must be the same pin which is used from the I2C unit as SCL.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. I2cPinMode

**容器属性**:

- **UUID**: `b4707010-b77e-4685-8d5e-48f6503aec4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cPinMode`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration parameters to switch the SCL pin between Dio/I2c function.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. I2cPortPinModeI2c

- **UUID**: `8423be8f-9243-4cdf-896e-f102a88528fd`
- **参数名**: `I2cPortPinModeI2c`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_ALT6`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into I2c mode.

############## 2. I2cPortPinModeDio

- **UUID**: `f79767f4-e351-4703-9a55-7618a06aa01c`
- **参数名**: `I2cPortPinModeDio`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_GPIO`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into DIO mode.

######### 2. I2cPinMode

**容器属性**:

- **UUID**: `b4707010-b77e-4685-8d5e-48f6503aec4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cPinMode`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration parameters to switch the SCL pin between Dio/I2c function.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. I2cPortPinModeI2c

- **UUID**: `8423be8f-9243-4cdf-896e-f102a88528fd`
- **参数名**: `I2cPortPinModeI2c`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_ALT6`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into I2c mode.

############ 2. I2cPortPinModeDio

- **UUID**: `f79767f4-e351-4703-9a55-7618a06aa01c`
- **参数名**: `I2cPortPinModeDio`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_GPIO`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into DIO mode.

####### 4. I2cRecovery

**容器属性**:

- **UUID**: `d38c917a-0a1c-4569-9b54-ad46d02722a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cRecovery`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes parameters which are required to perform I2c bus free.

######## 引用关系

此容器包含 **2** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. I2cPortPinScl

- **UUID**: `b49077fe-86ba-41ca-afce-b89240c037b1`
- **引用名**: `I2cPortPinScl`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Port/PortConfigSet/PortContainer/PortPin`
  - `/AUTOSAR/Port/PortConfigSet/PortContainer/PortPin`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PortPin which is used for pin mode switching.

Note: In case the module needs to apply the 'bus free' procedure the referenced PortPin is set do Dio mode and used to generate clock pulses. After the 'bus free' procedure the pin automatically gets set back to I2C mode.

########## 2. I2cDioSclPin

- **UUID**: `e39f19f2-0581-4f3a-8d78-1610c90c8dd9`
- **引用名**: `I2cDioSclPin`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioPort/DioChannel`
  - `/AUTOSAR/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/Dio/DioPort/DioChannel`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Dio pin, which is used for Bus Free and read the status of the SCL pin.

Note: Must be the same pin which is used from the I2C unit as SCL.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. I2cPinMode

**容器属性**:

- **UUID**: `b4707010-b77e-4685-8d5e-48f6503aec4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cPinMode`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration parameters to switch the SCL pin between Dio/I2c function.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. I2cPortPinModeI2c

- **UUID**: `8423be8f-9243-4cdf-896e-f102a88528fd`
- **参数名**: `I2cPortPinModeI2c`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_ALT6`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into I2c mode.

############ 2. I2cPortPinModeDio

- **UUID**: `f79767f4-e351-4703-9a55-7618a06aa01c`
- **参数名**: `I2cPortPinModeDio`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_GPIO`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into DIO mode.

####### 5. I2cPinMode

**容器属性**:

- **UUID**: `b4707010-b77e-4685-8d5e-48f6503aec4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cPinMode`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration parameters to switch the SCL pin between Dio/I2c function.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. I2cPortPinModeI2c

- **UUID**: `8423be8f-9243-4cdf-896e-f102a88528fd`
- **参数名**: `I2cPortPinModeI2c`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_ALT6`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into I2c mode.

########## 2. I2cPortPinModeDio

- **UUID**: `f79767f4-e351-4703-9a55-7618a06aa01c`
- **参数名**: `I2cPortPinModeDio`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_GPIO`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into DIO mode.

####### 6. I2cDemEventParameterRefs

**容器属性**:

- **UUID**: `5ff74129-5e4a-4989-af15-2ecc1dbcac5f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration of the DemEvents.

######## 引用关系

此容器包含 **3** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. I2C_E_ADDRESSING_FAILURE

- **UUID**: `e16fe5c3-a39f-4203-b618-f597e92bf815`
- **引用名**: `I2C_E_ADDRESSING_FAILURE`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
  - `/AUTOSAR/Dem/DemConfigSet/DemEventParameter`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the configured DEM event to report "Addressing failure".

Note: "Addressing failure" occurs in case a NACK response is detected and the corresponding sequence is configured to handle NACK as error.

########## 2. I2C_E_ARBITRATION_FAILURE

- **UUID**: `923e41ed-3c05-40e1-bd76-83576b82d6aa`
- **引用名**: `I2C_E_ARBITRATION_FAILURE`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
  - `/AUTOSAR/Dem/DemConfigSet/DemEventParameter`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the configured DEM event to report "Arbitration failure".

Note: "Arbitration failure" occurs in case the master loses arbitration. This usually happens if the SDA is stuck low.

########## 3. I2C_E_BUS_FAILURE

- **UUID**: `648f9d1a-dd97-4d4d-a26f-d3bbe7dfbe83`
- **引用名**: `I2C_E_BUS_FAILURE`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
  - `/AUTOSAR/Dem/DemConfigSet/DemEventParameter`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the configured DEM event to report "Bus failure".

Note: "Bus failure" occurs in case SCL line is stuck low.

####### 7. I2cSequence

**容器属性**:

- **UUID**: `edaad989-9574-40cd-b4cb-4869c4100c11`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Sequence specific configuration parameters of the I2c.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. I2cPriority

- **UUID**: `d33fca3d-ca80-4577-a43b-52d18c5cfc5a`
- **参数名**: `I2cPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the priority of a sequence. Going from 0 (highest)  to 255 (lowest).

########## 2. I2cSequenceId

- **UUID**: `eaf03216-b0b5-4e4c-a9f2-418e1c3994d5`
- **参数名**: `I2cSequenceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the Id of a I2c Sequence.

######### BOOLEAN 类型参数

########## 1. I2cHandleNackAsError

- **UUID**: `af94749d-4497-492e-aa03-6f124bfd1652`
- **参数名**: `I2cHandleNackAsError`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether a NACK is handeld as error. 

True: NACK is handled as error (I2cErrorNotification callback is called, DEM event is reported).
False: NACK is not handled as error (I2cEndNotification is called).

######### FUNCTION-NAME 类型参数

########## 1. I2cEndNotification

- **UUID**: `51789c08-4555-43a8-b39c-1b2662c9d558`
- **参数名**: `I2cEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the transmission end notification to inform the user that a transmission request has been serviced.

########## 2. I2cErrorNotification

- **UUID**: `8ad6b70f-4edf-45c6-892b-06c268eeb895`
- **参数名**: `I2cErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the transmission error notification to inform the user that a transmission request has failed.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. I2cAssignedBus

- **UUID**: `aa09c793-c58b-4bdd-8b9d-bd6f9103c251`
- **引用名**: `I2cAssignedBus`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cBus`
- **完整路径**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c/I2cConfigSet/I2cBus`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References the bus which is assigned to the channel

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. I2cChannelList

**容器属性**:

- **UUID**: `5f2c47af-55c2-4ffa-94fe-8ff6b19611a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cChannelList`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

References to channels and their order within the Sequence.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. I2cChannelIndex

- **UUID**: `cdff4233-9f2b-41f6-a02d-dc5b3e9b8c31`
- **参数名**: `I2cChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the position of a channel in list.
A channel with index 0 is processed first.
The index is incremented an the next channel is processed.
The index shall not have gaps.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. I2cChannelAssignment

- **UUID**: `33f5726c-711d-4971-a64b-4b4b64309ef1`
- **引用名**: `I2cChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a channel.

####### 8. I2cChannelList

**容器属性**:

- **UUID**: `5f2c47af-55c2-4ffa-94fe-8ff6b19611a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cChannelList`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

References to channels and their order within the Sequence.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. I2cChannelIndex

- **UUID**: `cdff4233-9f2b-41f6-a02d-dc5b3e9b8c31`
- **参数名**: `I2cChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the position of a channel in list.
A channel with index 0 is processed first.
The index is incremented an the next channel is processed.
The index shall not have gaps.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. I2cChannelAssignment

- **UUID**: `33f5726c-711d-4971-a64b-4b4b64309ef1`
- **引用名**: `I2cChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a channel.

##### 2. I2cChannel

**容器属性**:

- **UUID**: `f5c21f19-3d77-4e6d-9283-79426582c30a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Channel specific configuration parameters of the I2c.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. I2cChannelId

- **UUID**: `e865ffcd-4289-435f-a006-5d5551a731bd`
- **参数名**: `I2cChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the identifier of a channel.

######## 2. I2cDeviceAddress

- **UUID**: `09de9803-2684-4c4d-a571-abc80cd4725b`
- **参数名**: `I2cDeviceAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1023]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the address of a slave device which is accessed by the master.

######## 3. I2cDefaultData

- **UUID**: `1452cca8-d3c5-4fa5-bf8d-a42cbbc3be57`
- **参数名**: `I2cDefaultData`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the default value of the channel.

Note: The default data is transmitted in case of TxBuffer and RxBuffer of the channel is set to NULL_PTR (e.g. via API I2c_SetupEB).

####### BOOLEAN 类型参数

######## 1. I2cChainChannel

- **UUID**: `e8594ea3-5a69-4186-9c2e-ef4abcc25c93`
- **参数名**: `I2cChainChannel`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the channel is chained.

True: The channel is chained.
False: The channel is not chained.

Note: A chained channel requires follow up to be set. It does not set a restart condition and the retransmission of the slave address is ommited.

##### 3. I2cBus

**容器属性**:

- **UUID**: `dcbd473b-5cd0-468a-8ea7-e6a669dde771`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cBus`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Bus specific configuration parameters of the I2c.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. I2cBusId

- **UUID**: `96aa5ffd-711b-41d0-8b03-7ac56de8a386`
- **参数名**: `I2cBusId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the identifier of a bus.

######## 2. I2cTransferRate

- **UUID**: `ef0c7b38-325e-48bd-9647-3854784df029`
- **参数名**: `I2cTransferRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [100..1001]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the baudrate of the bus in KHz.

####### FLOAT 类型参数

######## 1. I2cTimeout

- **UUID**: `34f6caf6-e628-4afe-b7da-da69c7e50f4c`
- **参数名**: `I2cTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the timeout for I2c in ms.

Note: If the timeout expires, the driver applies the configured timeout handling (via API I2c_SetTimeoutHandling).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. I2cHwUnitAssignment

- **UUID**: `0818a5b4-53ce-4cac-bc63-4f45382c241d`
- **引用名**: `I2cHwUnitAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cHardwareUnit`
- **完整路径**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c/I2cConfigSet/I2cHardwareUnit`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the I2cHardwareUnit to which the bus is assigned.

##### 4. I2cHardwareUnit

**容器属性**:

- **UUID**: `2733920f-d591-4c89-b6ed-a8c0b9732906`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cHardwareUnit`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Hardware unit specific configuration parameters of the I2c.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. I2cUnitId

- **UUID**: `3e38d81a-49d6-4bb9-bd43-3fab5c048cef`
- **参数名**: `I2cUnitId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the identifier of the hardware unit.

######## 2. I2cClockDivider

- **UUID**: `a5fe77c3-2c96-434b-ab23-fe1db71332f0`
- **参数名**: `I2cClockDivider`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter sets the clock divider for the i2c module.

######## 3. I2cDelayStageSDA

- **UUID**: `7c435407-4ca7-41a2-b981-49d2e6bb7bb6`
- **参数名**: `I2cDelayStageSDA`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: SDA Delay stages for data hold time. The standard delay time is 0x00.
note: SDA delay from the SCL falling edge. This  will also affect SDA setup time relative to the next SCL rising edge.

####### FLOAT 类型参数

######## 1. I2cClockFrequencyManual

- **UUID**: `7753a951-68e7-408c-9ed5-e99f46346eb0`
- **参数名**: `I2cClockFrequencyManual`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `8000000`
- **取值范围**: [1..1.7976931348623157E+308]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the clock rate (in MHz) of the I2C hardware unit.

Note: This parameter is used to calculate baudrate settings in case the reference I2cClockConfiguration is not configured.

####### ENUMERATION 类型参数

######## 1. I2cPortSelect

- **UUID**: `5d9fa2ea-051e-418e-8e13-027e8152136f`
- **参数名**: `I2cPortSelect`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `PORTA`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `PORTA`
  - `PORTB`
  - `PORTC`
  - `PORTD`
  - `PORTE`
  - `PORTF`
  - `PORTG`
  - `PORTH`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifices the selected pins providing the serial data (SDA) and clock (SCL) signals.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. I2cHardwareConfigurationRef

- **UUID**: `f478442a-9470-4111-a545-7c60d441ed71`
- **引用名**: `I2cHardwareConfigurationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cHardwareConfiguration`
- **完整路径**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c/I2cHardwareConfiguration`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a hardware configuration.

####### CHOICE-REFERENCE 类型引用

######## 1. I2cClockConfiguration

- **UUID**: `1be475dc-e15b-4085-a2b3-30b24c033504`
- **引用名**: `I2cClockConfiguration`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
  - `/AUTOSAR/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a McuClockReferencePoint which is used to calculate the baudrate settings for transmissions on a hardware unit.

Note: If this parameter is set the clock is derived from the MCU.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. I2cRecovery

**容器属性**:

- **UUID**: `d38c917a-0a1c-4569-9b54-ad46d02722a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cRecovery`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes parameters which are required to perform I2c bus free.

######## 引用关系

此容器包含 **2** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. I2cPortPinScl

- **UUID**: `b49077fe-86ba-41ca-afce-b89240c037b1`
- **引用名**: `I2cPortPinScl`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Port/PortConfigSet/PortContainer/PortPin`
  - `/AUTOSAR/Port/PortConfigSet/PortContainer/PortPin`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PortPin which is used for pin mode switching.

Note: In case the module needs to apply the 'bus free' procedure the referenced PortPin is set do Dio mode and used to generate clock pulses. After the 'bus free' procedure the pin automatically gets set back to I2C mode.

########## 2. I2cDioSclPin

- **UUID**: `e39f19f2-0581-4f3a-8d78-1610c90c8dd9`
- **引用名**: `I2cDioSclPin`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioPort/DioChannel`
  - `/AUTOSAR/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/Dio/DioPort/DioChannel`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Dio pin, which is used for Bus Free and read the status of the SCL pin.

Note: Must be the same pin which is used from the I2C unit as SCL.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. I2cPinMode

**容器属性**:

- **UUID**: `b4707010-b77e-4685-8d5e-48f6503aec4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cPinMode`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration parameters to switch the SCL pin between Dio/I2c function.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. I2cPortPinModeI2c

- **UUID**: `8423be8f-9243-4cdf-896e-f102a88528fd`
- **参数名**: `I2cPortPinModeI2c`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_ALT6`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into I2c mode.

############ 2. I2cPortPinModeDio

- **UUID**: `f79767f4-e351-4703-9a55-7618a06aa01c`
- **参数名**: `I2cPortPinModeDio`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_GPIO`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into DIO mode.

####### 2. I2cPinMode

**容器属性**:

- **UUID**: `b4707010-b77e-4685-8d5e-48f6503aec4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cPinMode`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration parameters to switch the SCL pin between Dio/I2c function.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. I2cPortPinModeI2c

- **UUID**: `8423be8f-9243-4cdf-896e-f102a88528fd`
- **参数名**: `I2cPortPinModeI2c`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_ALT6`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into I2c mode.

########## 2. I2cPortPinModeDio

- **UUID**: `f79767f4-e351-4703-9a55-7618a06aa01c`
- **参数名**: `I2cPortPinModeDio`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_GPIO`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into DIO mode.

##### 5. I2cRecovery

**容器属性**:

- **UUID**: `d38c917a-0a1c-4569-9b54-ad46d02722a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cRecovery`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes parameters which are required to perform I2c bus free.

###### 引用关系

此容器包含 **2** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. I2cPortPinScl

- **UUID**: `b49077fe-86ba-41ca-afce-b89240c037b1`
- **引用名**: `I2cPortPinScl`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Port/PortConfigSet/PortContainer/PortPin`
  - `/AUTOSAR/Port/PortConfigSet/PortContainer/PortPin`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PortPin which is used for pin mode switching.

Note: In case the module needs to apply the 'bus free' procedure the referenced PortPin is set do Dio mode and used to generate clock pulses. After the 'bus free' procedure the pin automatically gets set back to I2C mode.

######## 2. I2cDioSclPin

- **UUID**: `e39f19f2-0581-4f3a-8d78-1610c90c8dd9`
- **引用名**: `I2cDioSclPin`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioPort/DioChannel`
  - `/AUTOSAR/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/Dio/DioPort/DioChannel`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Dio pin, which is used for Bus Free and read the status of the SCL pin.

Note: Must be the same pin which is used from the I2C unit as SCL.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. I2cPinMode

**容器属性**:

- **UUID**: `b4707010-b77e-4685-8d5e-48f6503aec4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cPinMode`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration parameters to switch the SCL pin between Dio/I2c function.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. I2cPortPinModeI2c

- **UUID**: `8423be8f-9243-4cdf-896e-f102a88528fd`
- **参数名**: `I2cPortPinModeI2c`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_ALT6`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into I2c mode.

########## 2. I2cPortPinModeDio

- **UUID**: `f79767f4-e351-4703-9a55-7618a06aa01c`
- **参数名**: `I2cPortPinModeDio`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_GPIO`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into DIO mode.

##### 6. I2cPinMode

**容器属性**:

- **UUID**: `b4707010-b77e-4685-8d5e-48f6503aec4d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cPinMode`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration parameters to switch the SCL pin between Dio/I2c function.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. I2cPortPinModeI2c

- **UUID**: `8423be8f-9243-4cdf-896e-f102a88528fd`
- **参数名**: `I2cPortPinModeI2c`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_ALT6`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into I2c mode.

######## 2. I2cPortPinModeDio

- **UUID**: `f79767f4-e351-4703-9a55-7618a06aa01c`
- **参数名**: `I2cPortPinModeDio`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `PORT_PIN_MODE_GPIO`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the symbolic define from the generated PORT files for the pin mode which is used for switching the pin into DIO mode.

##### 7. I2cDemEventParameterRefs

**容器属性**:

- **UUID**: `5ff74129-5e4a-4989-af15-2ecc1dbcac5f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration of the DemEvents.

###### 引用关系

此容器包含 **3** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. I2C_E_ADDRESSING_FAILURE

- **UUID**: `e16fe5c3-a39f-4203-b618-f597e92bf815`
- **引用名**: `I2C_E_ADDRESSING_FAILURE`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
  - `/AUTOSAR/Dem/DemConfigSet/DemEventParameter`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the configured DEM event to report "Addressing failure".

Note: "Addressing failure" occurs in case a NACK response is detected and the corresponding sequence is configured to handle NACK as error.

######## 2. I2C_E_ARBITRATION_FAILURE

- **UUID**: `923e41ed-3c05-40e1-bd76-83576b82d6aa`
- **引用名**: `I2C_E_ARBITRATION_FAILURE`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
  - `/AUTOSAR/Dem/DemConfigSet/DemEventParameter`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the configured DEM event to report "Arbitration failure".

Note: "Arbitration failure" occurs in case the master loses arbitration. This usually happens if the SDA is stuck low.

######## 3. I2C_E_BUS_FAILURE

- **UUID**: `648f9d1a-dd97-4d4d-a26f-d3bbe7dfbe83`
- **引用名**: `I2C_E_BUS_FAILURE`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
  - `/AUTOSAR/Dem/DemConfigSet/DemEventParameter`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the configured DEM event to report "Bus failure".

Note: "Bus failure" occurs in case SCL line is stuck low.

##### 8. I2cSequence

**容器属性**:

- **UUID**: `edaad989-9574-40cd-b4cb-4869c4100c11`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Sequence specific configuration parameters of the I2c.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. I2cPriority

- **UUID**: `d33fca3d-ca80-4577-a43b-52d18c5cfc5a`
- **参数名**: `I2cPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the priority of a sequence. Going from 0 (highest)  to 255 (lowest).

######## 2. I2cSequenceId

- **UUID**: `eaf03216-b0b5-4e4c-a9f2-418e1c3994d5`
- **参数名**: `I2cSequenceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the Id of a I2c Sequence.

####### BOOLEAN 类型参数

######## 1. I2cHandleNackAsError

- **UUID**: `af94749d-4497-492e-aa03-6f124bfd1652`
- **参数名**: `I2cHandleNackAsError`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether a NACK is handeld as error. 

True: NACK is handled as error (I2cErrorNotification callback is called, DEM event is reported).
False: NACK is not handled as error (I2cEndNotification is called).

####### FUNCTION-NAME 类型参数

######## 1. I2cEndNotification

- **UUID**: `51789c08-4555-43a8-b39c-1b2662c9d558`
- **参数名**: `I2cEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the transmission end notification to inform the user that a transmission request has been serviced.

######## 2. I2cErrorNotification

- **UUID**: `8ad6b70f-4edf-45c6-892b-06c268eeb895`
- **参数名**: `I2cErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the transmission error notification to inform the user that a transmission request has failed.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. I2cAssignedBus

- **UUID**: `aa09c793-c58b-4bdd-8b9d-bd6f9103c251`
- **引用名**: `I2cAssignedBus`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cBus`
- **完整路径**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c/I2cConfigSet/I2cBus`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References the bus which is assigned to the channel

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. I2cChannelList

**容器属性**:

- **UUID**: `5f2c47af-55c2-4ffa-94fe-8ff6b19611a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cChannelList`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

References to channels and their order within the Sequence.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. I2cChannelIndex

- **UUID**: `cdff4233-9f2b-41f6-a02d-dc5b3e9b8c31`
- **参数名**: `I2cChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the position of a channel in list.
A channel with index 0 is processed first.
The index is incremented an the next channel is processed.
The index shall not have gaps.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. I2cChannelAssignment

- **UUID**: `33f5726c-711d-4971-a64b-4b4b64309ef1`
- **引用名**: `I2cChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a channel.

##### 9. I2cChannelList

**容器属性**:

- **UUID**: `5f2c47af-55c2-4ffa-94fe-8ff6b19611a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cChannelList`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

References to channels and their order within the Sequence.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. I2cChannelIndex

- **UUID**: `cdff4233-9f2b-41f6-a02d-dc5b3e9b8c31`
- **参数名**: `I2cChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the position of a channel in list.
A channel with index 0 is processed first.
The index is incremented an the next channel is processed.
The index shall not have gaps.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. I2cChannelAssignment

- **UUID**: `33f5726c-711d-4971-a64b-4b4b64309ef1`
- **引用名**: `I2cChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a channel.

##### 10. I2cGeneral

**容器属性**:

- **UUID**: `1a62cce8-1a13-48c6-9b1b-54e9ea959a50`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

General configuration parameters of the I2c.

###### 参数配置

此容器包含 **18** 个参数：

####### INTEGER 类型参数

######## 1. I2cQueueDepth

- **UUID**: `4929306d-f218-45cb-83f7-0cf21140065a`
- **参数名**: `I2cQueueDepth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the depth of the queue.

######## 2. I2cMaxHwLoopCycles

- **UUID**: `3502c29b-c642-4ab6-abdc-b95e0cf568eb`
- **参数名**: `I2cMaxHwLoopCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [1..65534]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum amount of HW-loops waited before a DEM-error is thrown.

####### BOOLEAN 类型参数

######## 1. I2cDevErrorDetect

- **UUID**: `bb41df79-6516-46c4-addb-62799eb1d16f`
- **参数名**: `I2cDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.

True: Development error detection is enabled.
False: Development error detection is disabled.

######## 2. I2cGetStatusApi

- **UUID**: `5416e910-7d19-458d-aa9f-267b5bc71d6b`
- **参数名**: `I2cGetStatusApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the function I2c_GetStatus() to get the status of a channel.

######## 3. I2cCancelApi

- **UUID**: `3c4c79b3-8efa-46b8-80ce-82e421055ca7`
- **参数名**: `I2cCancelApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the function I2c_Cancel() to cancel the transmission request of a sequence.

######## 4. I2cVersionInfoApi

- **UUID**: `54437cfe-932a-4645-9ca4-413905f7a229`
- **参数名**: `I2cVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the function I2c_GetVersionInfo() to get major, minor and patch version information.

######## 5. I2cProtectedMode

- **UUID**: `6d4d2520-98b0-4dfd-8c2a-25075882042a`
- **参数名**: `I2cProtectedMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies whether the module should use osPeripheralAccess-API (e.g. because memory access is restricted by MMU)  to access memory mapped registers.

True: Module uses APIs provided by OS to access memory mapped registers.
False: Module uses direct memory access to access memory mapped registers.

######## 6. I2cSafeBswChecks

- **UUID**: `9d2dad3d-5634-4b48-8f8c-bebb30da5487`
- **参数名**: `I2cSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######## 7. I2cPollingMode

- **UUID**: `93c2f8cd-f772-4a93-b177-0fef82fdd1b0`
- **参数名**: `I2cPollingMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies whether I2c Polling mode is used.
When enabled:
- Transactions are carried out without CPU interrupts.
- User needs to call I2c_PollingModeProcessing() repeatedly after triggering the transmission until the end of the transmission. Repeated call needs to be in regular intervals (typ. 100us - 2ms) depending on the platform specific I2c implementation and configured I2c transfer rate. For more information on regular intervals please refer to the documentation of the I2c low-level part and check your communication timings manually with logic analyzer.

####### FLOAT 类型参数

######## 1. I2cMainFunctionPeriod

- **UUID**: `a816a7de-b271-4ba9-ae63-6c7f275da28c`
- **参数名**: `I2cMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the main function period of the I2c in ms.

####### STRING 类型参数

######## 1. I2cUserCallbackHeaderFile

- **UUID**: `2a521d94-41b1-449c-9121-2b965ee8989e`
- **参数名**: `I2cUserCallbackHeaderFile`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `NULL`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines header file name which will be included by the I2c.

######## 2. I2cUserConfigFile

- **UUID**: `b9a5ba9a-f5a0-4e5c-9ebc-81e0c4c2be94`
- **参数名**: `I2cUserConfigFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `NULL`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an external text file that will be included during generation to I2c_Cfg.h.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

######## 3. I2cMcalSetAccess

- **UUID**: `a4ca0794-9e06-4441-82b9-b5cdce503467`
- **参数名**: `I2cMcalSetAccess`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Mcal_ResetENDINIT`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This function enables access to protected registers.

Note: Add the dependend header file to the user defined header files.

######## 4. I2cMcalClearAccess

- **UUID**: `f7171bc1-cefb-4299-a09a-075e3a21ac72`
- **参数名**: `I2cMcalClearAccess`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Mcal_SetENDINIT`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This function clears access to protected registers.

Note: Add the dependend header file to the user defined header files.

######## 5. I2cMcalPortSetPinMode

- **UUID**: `398d8cc8-3282-4df0-977b-f3fcafb5f9eb`
- **参数名**: `I2cMcalPortSetPinMode`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Port_SetPinMode`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This function changes the mode of the pin.

Note: Add the dependend heade rfile to the user defined header files.

######## 6. I2cMcalDioFlipChannel

- **UUID**: `941f62cd-9d09-4691-9ada-01ce167f500f`
- **参数名**: `I2cMcalDioFlipChannel`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Dio_FlipChannel`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This function changes the channel level.

Note: Add the dependend header file to the user defined header files.

######## 7. I2cUserDefinedHeaderFile

- **UUID**: `f1c5109e-886c-483f-b5db-5a4492ae0e42`
- **参数名**: `I2cUserDefinedHeaderFile`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `NULL`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines header file name which will be included by the I2c.

####### ENUMERATION 类型参数

######## 1. I2cIrqType

- **UUID**: `535e6cdb-c4ec-4891-a77b-01d019f5b8d6`
- **参数名**: `I2cIrqType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `I2C_ISR_CAT2`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `I2C_ISR_VOID`
  - `I2C_ISR_CAT1`
  - `I2C_ISR_CAT2`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the type of the generated ISR functions.

I2C_ISR_VOID: void function (void)
I2C_ISR_CAT1: CAT1 interrupt (__isr void function(void))
I2C_ISR_CAT2: CAT2 interrupt (ISR(function))

##### 11. I2cHardwareConfiguration

**容器属性**:

- **UUID**: `f0e93bac-e3a4-4f41-97d5-27fd6612df54`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cHardwareConfiguration`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This container includes the hardware specific configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. I2cUnitBase

- **UUID**: `8f243dda-4490-4d77-a2ca-d3793ff06508`
- **参数名**: `I2cUnitBase`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the hardware unit base address.

Caution: An incorrect address may lead to system crash.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. I2c_Tc2xxInfi2c01

- **UUID**: `2afd2722-b011-4ac6-b029-c255316f929d`
- **包名称**: `I2c_Tc2xxInfi2c01`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **I2c_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **I2c**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **I2c_Pre**
2. **I2c_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. I2c_Impl

- **UUID**: `f62bcad4-3d09-44c8-a657-7f06e12d818a`
- **实现名称**: `I2c_Impl`
- **编程语言**: C
- **软件版本**: 2.05.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.02
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. I2c_Pre

- **UUID**: `9a31d296-680c-4d05-8521-d51a3f55e42f`
- **配置名称**: `I2c_Pre`
- **定义引用**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c`

### 2. I2c_Rec

- **UUID**: `a8248ac5-9b21-47e7-b452-d60e354f3b16`
- **配置名称**: `I2c_Rec`
- **定义引用**: `/MICROSAR/I2c_Tc2xxInfi2c01/I2c`
