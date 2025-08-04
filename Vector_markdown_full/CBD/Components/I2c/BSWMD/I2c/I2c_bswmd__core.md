# I2c - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:59

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

- **UUID**: `c4735642-e1c1-446d-afa7-ccffb9f8a0e1`
- **模块名称**: `I2c`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD-SELECTABLE
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the I2c (Inter-Integrated Circuit) module.

#### 版本历史

共有 **11** 个版本记录：

##### 1. 版本 2.00.00

- **状态**: released
- **发布日期**: 2018-03-13T16:17:11+01:00
- **发布者**: virmid

**变更内容**:

##### 2. 版本 2.00.01

- **状态**: released
- **发布日期**: 2018-06-06T15:36:26+02:00
- **发布者**: virmid

*此版本无详细变更记录*

##### 3. 版本 2.00.02

- **状态**: released
- **发布日期**: 2019-03-07T03:32:58+01:00
- **发布者**: virrdl

**变更内容**:

##### 4. 版本 2.00.03

- **状态**: released
- **发布日期**: 2019-11-21T12:44:31+01:00
- **发布者**: virmid

**变更内容**:

##### 5. 版本 2.00.04

- **状态**: released
- **发布日期**: 2020-03-18T11:21:23+01:00
- **发布者**: virnba

**变更内容**:

##### 6. 版本 2.00.05

- **状态**: released
- **发布日期**: 2020-03-18T11:22:37+01:00
- **发布者**: virnba

**变更内容**:

##### 7. 版本 2.00.06

- **状态**: released
- **发布日期**: 2020-06-23T09:07:53+02:00
- **发布者**: coberpriller

**变更内容**:

##### 8. 版本 2.00.07

- **状态**: released
- **发布日期**: 2020-07-07T15:00:20+02:00
- **发布者**: virwsl

**变更内容**:

##### 9. 版本 2.00.08

- **状态**: released
- **发布日期**: 2021-06-24T13:24:15+02:00
- **发布者**: virrdl

**变更内容**:

##### 10. 版本 3.00.00

- **状态**: released
- **发布日期**: 2022-02-15T15:50:56+01:00
- **发布者**: virzln

**变更内容**:

##### 11. 版本 3.00.01

- **状态**: released
- **发布日期**: 2022-06-29T11:27:21+02:00
- **发布者**: rwerhahn

**变更内容**:

#### 配置容器

本模块包含 **9** 个配置容器：

##### 1. I2cConfigSet

**容器属性**:

- **UUID**: `19bdff06-c6ed-45e8-a37b-29fccf4bd40a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cConfigSet`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This container includes the base for a multiple configuration set.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. I2cChannel

**容器属性**:

- **UUID**: `0cd1a6ab-3d1b-4aba-aedf-63586b360497`
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

- **UUID**: `52b4ae67-8e5c-40f6-9d8f-e52bc99e08e8`
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

- **UUID**: `196050d0-e2ca-4b85-adcd-ffd9874f2d1f`
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

Note: Values bigger than 0x7F (127) lead to Extended Addressing.

########## 3. I2cDefaultData

- **UUID**: `ab1a213b-67a2-446b-9ff0-939e0a806cd8`
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

- **UUID**: `512913ff-cbba-4887-bd7c-242443e924a7`
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

- **UUID**: `51322062-8b3b-4231-9267-8e6687d65cc0`
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

- **UUID**: `a4bed955-bf5c-447a-824e-cf01696ea816`
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

- **UUID**: `b9e7951b-6b17-4de5-b74e-3a111af769de`
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

- **UUID**: `6a31fac4-18ae-4756-ba7b-06b5d6dfb741`
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
- **描述**: This parameter specifies the timeout for I2c in s.

Note: If the timeout expires, the driver applies the configured timeout handling (via API I2c_SetTimeoutHandling).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. I2cHwUnitAssignment

- **UUID**: `fd2539ad-c3fc-4d13-afbf-93ab0d128fee`
- **引用名**: `I2cHwUnitAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cHardwareUnit`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cHardwareUnit`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the I2cHardwareUnit to which the bus is assigned.

####### 3. I2cHardwareUnit

**容器属性**:

- **UUID**: `7e7452e6-9a34-420b-8171-f92fce396339`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cHardwareUnit`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Hardware unit specific configuration parameters of the I2c.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. I2cUnitId

- **UUID**: `0e3f115d-cd49-40f2-84cb-e5670351c1d7`
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

######### FLOAT 类型参数

########## 1. I2cClockFrequencyManual

- **UUID**: `8400e46d-cb8c-4eaa-9ce1-0fc06f8df197`
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
- **描述**: This parameter specifies the clock rate (in Hz) of the I2C hardware unit.

Note: This parameter is used to calculate baudrate settings in case the reference I2cClockConfiguration is not configured.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. I2cHardwareConfigurationRef

- **UUID**: `d33e1739-29d5-456a-9b0e-92cc643656e1`
- **引用名**: `I2cHardwareConfigurationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cHardwareConfiguration`
- **完整路径**: `/MICROSAR/I2c/I2cHardwareConfiguration`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a hardware configuration.

######### CHOICE-REFERENCE 类型引用

########## 1. I2cClockConfiguration

- **UUID**: `b54b0b03-eb99-4434-88a5-8bcf74e3c414`
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

####### 4. I2cDemEventParameterRefs

**容器属性**:

- **UUID**: `16abef0a-0bdf-4098-bed7-5cf2f6948837`
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

- **UUID**: `198c53c5-c15e-48a0-9f73-ce1a9ae8b52b`
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

- **UUID**: `6f195270-10f9-4929-86d2-c04f1ced1a8e`
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

- **UUID**: `6cf06c41-f675-4728-b787-aa0281bedbcb`
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

####### 5. I2cSequence

**容器属性**:

- **UUID**: `a858f67f-758c-4325-9e00-d1d3e6ddb440`
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

- **UUID**: `f6cd461f-5c0a-4b7d-8871-4ff1041bd6ef`
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

- **UUID**: `e35b7f4c-67b9-4961-8728-dcd2d5fa866c`
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

- **UUID**: `50122df1-1180-46a5-9cb1-f4aae4d6563c`
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

- **UUID**: `7a75ac6a-8e88-4e66-bf68-5f891e8c758d`
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

- **UUID**: `ac84810e-34ac-4b6a-89f9-3f11f8e17478`
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

- **UUID**: `a0e4d9db-4c7b-42a2-9e3c-fc8de04aef96`
- **引用名**: `I2cAssignedBus`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cBus`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cBus`
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

- **UUID**: `074d45db-e6eb-46b2-87d5-bc9caba6d877`
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

- **UUID**: `51f821fc-3f1c-4fe6-a96c-f38ca68156c9`
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

- **UUID**: `4457cbf5-c38f-44cd-85b9-ccfe311ecc5b`
- **引用名**: `I2cChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a channel.

####### 6. I2cChannelList

**容器属性**:

- **UUID**: `074d45db-e6eb-46b2-87d5-bc9caba6d877`
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

- **UUID**: `51f821fc-3f1c-4fe6-a96c-f38ca68156c9`
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

- **UUID**: `4457cbf5-c38f-44cd-85b9-ccfe311ecc5b`
- **引用名**: `I2cChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a channel.

##### 2. I2cChannel

**容器属性**:

- **UUID**: `0cd1a6ab-3d1b-4aba-aedf-63586b360497`
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

- **UUID**: `52b4ae67-8e5c-40f6-9d8f-e52bc99e08e8`
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

- **UUID**: `196050d0-e2ca-4b85-adcd-ffd9874f2d1f`
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

Note: Values bigger than 0x7F (127) lead to Extended Addressing.

######## 3. I2cDefaultData

- **UUID**: `ab1a213b-67a2-446b-9ff0-939e0a806cd8`
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

- **UUID**: `512913ff-cbba-4887-bd7c-242443e924a7`
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

- **UUID**: `51322062-8b3b-4231-9267-8e6687d65cc0`
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

- **UUID**: `a4bed955-bf5c-447a-824e-cf01696ea816`
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

- **UUID**: `b9e7951b-6b17-4de5-b74e-3a111af769de`
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

- **UUID**: `6a31fac4-18ae-4756-ba7b-06b5d6dfb741`
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
- **描述**: This parameter specifies the timeout for I2c in s.

Note: If the timeout expires, the driver applies the configured timeout handling (via API I2c_SetTimeoutHandling).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. I2cHwUnitAssignment

- **UUID**: `fd2539ad-c3fc-4d13-afbf-93ab0d128fee`
- **引用名**: `I2cHwUnitAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cHardwareUnit`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cHardwareUnit`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the I2cHardwareUnit to which the bus is assigned.

##### 4. I2cHardwareUnit

**容器属性**:

- **UUID**: `7e7452e6-9a34-420b-8171-f92fce396339`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cHardwareUnit`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Hardware unit specific configuration parameters of the I2c.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. I2cUnitId

- **UUID**: `0e3f115d-cd49-40f2-84cb-e5670351c1d7`
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

####### FLOAT 类型参数

######## 1. I2cClockFrequencyManual

- **UUID**: `8400e46d-cb8c-4eaa-9ce1-0fc06f8df197`
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
- **描述**: This parameter specifies the clock rate (in Hz) of the I2C hardware unit.

Note: This parameter is used to calculate baudrate settings in case the reference I2cClockConfiguration is not configured.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. I2cHardwareConfigurationRef

- **UUID**: `d33e1739-29d5-456a-9b0e-92cc643656e1`
- **引用名**: `I2cHardwareConfigurationRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cHardwareConfiguration`
- **完整路径**: `/MICROSAR/I2c/I2cHardwareConfiguration`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a hardware configuration.

####### CHOICE-REFERENCE 类型引用

######## 1. I2cClockConfiguration

- **UUID**: `b54b0b03-eb99-4434-88a5-8bcf74e3c414`
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

##### 5. I2cDemEventParameterRefs

**容器属性**:

- **UUID**: `16abef0a-0bdf-4098-bed7-5cf2f6948837`
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

- **UUID**: `198c53c5-c15e-48a0-9f73-ce1a9ae8b52b`
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

- **UUID**: `6f195270-10f9-4929-86d2-c04f1ced1a8e`
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

- **UUID**: `6cf06c41-f675-4728-b787-aa0281bedbcb`
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

##### 6. I2cSequence

**容器属性**:

- **UUID**: `a858f67f-758c-4325-9e00-d1d3e6ddb440`
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

- **UUID**: `f6cd461f-5c0a-4b7d-8871-4ff1041bd6ef`
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

- **UUID**: `e35b7f4c-67b9-4961-8728-dcd2d5fa866c`
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

- **UUID**: `50122df1-1180-46a5-9cb1-f4aae4d6563c`
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

- **UUID**: `7a75ac6a-8e88-4e66-bf68-5f891e8c758d`
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

- **UUID**: `ac84810e-34ac-4b6a-89f9-3f11f8e17478`
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

- **UUID**: `a0e4d9db-4c7b-42a2-9e3c-fc8de04aef96`
- **引用名**: `I2cAssignedBus`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cBus`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cBus`
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

- **UUID**: `074d45db-e6eb-46b2-87d5-bc9caba6d877`
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

- **UUID**: `51f821fc-3f1c-4fe6-a96c-f38ca68156c9`
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

- **UUID**: `4457cbf5-c38f-44cd-85b9-ccfe311ecc5b`
- **引用名**: `I2cChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a channel.

##### 7. I2cChannelList

**容器属性**:

- **UUID**: `074d45db-e6eb-46b2-87d5-bc9caba6d877`
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

- **UUID**: `51f821fc-3f1c-4fe6-a96c-f38ca68156c9`
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

- **UUID**: `4457cbf5-c38f-44cd-85b9-ccfe311ecc5b`
- **引用名**: `I2cChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a channel.

##### 8. I2cGeneral

**容器属性**:

- **UUID**: `9ce07640-fa38-4ca8-90d5-2780c52b2d1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `I2cGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

General configuration parameters of the I2c.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. I2cQueueDepth

- **UUID**: `758f019e-f1a8-422c-b093-a30af2d08449`
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

####### BOOLEAN 类型参数

######## 1. I2cDevErrorDetect

- **UUID**: `2321dd3f-d738-46c5-867a-da57bf35b8a4`
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

- **UUID**: `8aa7740f-ca60-41d4-8a04-e50be6fb4538`
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

- **UUID**: `d1347280-f21e-4da9-a9ba-e575f06425ef`
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

- **UUID**: `f2db7f19-81b0-4545-959b-ff55db1b7a1b`
- **参数名**: `I2cVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the function I2c_GetVersionInfo() to get major, minor and patch version information.

######## 5. I2cProtectedMode

- **UUID**: `63f2953c-b4c7-4d1b-9adf-6411afafbbe2`
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

- **UUID**: `5a020ff4-1230-4fab-b50e-aff65e01acf2`
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

- **UUID**: `f1e20073-2f05-4a07-8b87-bc2315a24c03`
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
- User needs to call I2c_PollingModeProcessing() repeatedly after triggering the transmission until the end of the transmission. Repeated call needs to be in regular intervals (typ. 100us - 2ms) depending on the platform specific i2c implementation and configured i2c transfer rate. For more information on regular intervals  please refer to the documentation of the i2c low-level part and check your communication timings manually with Logic analyzer.

####### FLOAT 类型参数

######## 1. I2cMainFunctionPeriod

- **UUID**: `33612fe2-7736-4edd-ba81-e4ba1aa6dab9`
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
- **描述**: This parameter specifies the main function period of the I2c in s.

####### STRING 类型参数

######## 1. I2cUserCallbackHeaderFile

- **UUID**: `b68c9ee8-eee9-4c9b-a1e3-4a4dcf486504`
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

- **UUID**: `c4c491e8-29a4-4637-baf9-22f6bb93a855`
- **参数名**: `I2cUserConfigFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an external text file that will be included during generation to I2c_Cfg.h.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

####### ENUMERATION 类型参数

######## 1. I2cIrqType

- **UUID**: `8c5488d0-8135-4d24-a3e4-a53d9b70141b`
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

##### 9. I2cHardwareConfiguration

**容器属性**:

- **UUID**: `45ba8d9c-b16f-4b83-b5b4-7cc844e37cb3`
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

- **UUID**: `89efd991-8d9c-4e7d-8142-7031edba0559`
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

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **I2c**

##### BSW-IMPLEMENTATION 类型元素

1. **I2c_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **I2c_Pre**
2. **I2c_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. I2c_Impl

- **UUID**: `f1e97c16-0cd2-4e2b-9b23-b705c77330ca`
- **实现名称**: `I2c_Impl`
- **编程语言**: C
- **软件版本**: 5.00.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. I2c_Pre

- **UUID**: `227d35f9-56ea-4eb8-a01c-40bc8d44da13`
- **配置名称**: `I2c_Pre`
- **定义引用**: `/MICROSAR/I2c`

### 2. I2c_Rec

- **UUID**: `8753bd92-0761-4817-8fe5-5d0b68dda0c7`
- **配置名称**: `I2c_Rec`
- **定义引用**: `/MICROSAR/I2c`
