# WrapNv - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:31

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [WrapNv](#wrapnv)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. WrapNv

#### 基本信息

- **UUID**: `c3bafc6b-f47d-47b4-9262-88a7f5e19fd0`
- **模块名称**: `WrapNv`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the WrapNv (Wrapper non-volatile) module.

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. WrapNvGeneral

**容器属性**:

- **UUID**: `77cc9f41-d4f4-4a82-882c-0cfc29174819`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WrapNvGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. WrapNvEEPROMBaseAddress

- **UUID**: `b102d35e-e990-4852-8256-f40786524a8f`
- **参数名**: `WrapNvEEPROMBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Base Address of the EEPROM memory. This parameter is only relevant if EEPROM Driver is chosen.

######## 2. WrapNvFirstHandle

- **UUID**: `7f571f98-225e-47a9-af9d-70c649d7e305`
- **参数名**: `WrapNvFirstHandle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specify the first handle of the EEPROM Manger.

####### BOOLEAN 类型参数

######## 1. WrapNvMainFunctionPolling

- **UUID**: `f9ab4e5d-6cde-4863-a91c-e9d69af4840e`
- **参数名**: `WrapNvMainFunctionPolling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies whether main functions should be polled automatically.

####### STRING 类型参数

######## 1. WrapNvUserConfigFile

- **UUID**: `66e0e8e9-2011-4cf7-bfb8-724df03b4531`
- **参数名**: `WrapNvUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If a file path will be specified, the file is read and its content is put at the end of the generated file.

####### ENUMERATION 类型参数

######## 1. WrapNvNVMDataHandling

- **UUID**: `39680a70-6045-493a-9765-2ff7dd0d8ff4`
- **参数名**: `WrapNvNVMDataHandling`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `EXTERNAL_EEPROM_DRIVER`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EXTERNAL_EEPROM_DRIVER` (来源: Vector Informatik)
  - `EEPROM_EMULATION_FOR_HIS_FLASH_DRIVER` (来源: Vector Informatik)
  - `MSR_NVM` (来源: Vector Informatik)
  - `FEE` (来源: Vector Informatik)
  - `EA` (来源: Vector Informatik)
  - `NONE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the underlying memory driver which should be wrapped.

EXTERNAL_EEPROM_DRIVER: a simple EEPROM driver
EEPROM_EMULATION_FOR_HIS_FLASH_DRIVER: EEPROM Manager
MSR_NVM: Microsar NvM
FEE: Fee / Fls driver (without NvM)
EA: Ea / Eep driver (without NvM)

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. WrapNvMainFunctionCycle

**容器属性**:

- **UUID**: `09260487-223a-4f8f-a576-3e631f1397c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WrapNvMainFunctionCycle`
- **多重性**: [0..5]
- **构建后可变**: false

**容器描述**:

Determines the value in which the MainFunction of the referenced module shall be called [in MS].

0: call it as soon as possible
> 0: call the mainfunction each [value] MS

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. WrapNvMainFunctionCycleValue

- **UUID**: `efec70d7-2a65-45e9-98b5-2ea36c6df0fd`
- **参数名**: `WrapNvMainFunctionCycleValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The cycle in MS.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. WrapNvMainFunctionCycleModuleRef

- **UUID**: `3eed7d2c-d705-491e-a9b9-5122dd1cae67`
- **引用名**: `WrapNvMainFunctionCycleModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The module this MainFunctionCycle referres to

##### 2. WrapNvMainFunctionCycle

**容器属性**:

- **UUID**: `09260487-223a-4f8f-a576-3e631f1397c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WrapNvMainFunctionCycle`
- **多重性**: [0..5]
- **构建后可变**: false

**容器描述**:

Determines the value in which the MainFunction of the referenced module shall be called [in MS].

0: call it as soon as possible
> 0: call the mainfunction each [value] MS

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. WrapNvMainFunctionCycleValue

- **UUID**: `efec70d7-2a65-45e9-98b5-2ea36c6df0fd`
- **参数名**: `WrapNvMainFunctionCycleValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The cycle in MS.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. WrapNvMainFunctionCycleModuleRef

- **UUID**: `3eed7d2c-d705-491e-a9b9-5122dd1cae67`
- **引用名**: `WrapNvMainFunctionCycleModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The module this MainFunctionCycle referres to

##### 3. WrapNvMemoryLayout

**容器属性**:

- **UUID**: `a1a20892-ab9d-4c3d-a95f-fea0660f8380`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WrapNvMemoryLayout`
- **多重性**: [1..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. WrapNvDataBlock

**容器属性**:

- **UUID**: `31b52828-282c-45a2-ac5a-a6248cf5017b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WrapNvDataBlock`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. WrapNvDbIndex

- **UUID**: `9ae09c91-bb5c-40ee-9cb2-853ae7a0e0d3`
- **参数名**: `WrapNvDbIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specify the order in which the data blocks are generated.

########## 2. WrapNvDbCount

- **UUID**: `d9d9395c-7233-4e24-83bc-2055dfa94bfa`
- **参数名**: `WrapNvDbCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of multiple data blocks in a contiguous area.

######### STRING 类型参数

########## 1. WrapNvDbDescription

- **UUID**: `32d99213-ddbb-464d-b049-44c19de6cf52`
- **参数名**: `WrapNvDbDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description of the data block.

######### ENUMERATION 类型参数

########## 1. WrapNvDbType

- **UUID**: `aaa6d251-4f21-46b5-81a8-551cfcea9442`
- **参数名**: `WrapNvDbType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SINGLE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SINGLE` (来源: Vector Informatik)
  - `LIST` (来源: Vector Informatik)
  - `STRUCT` (来源: Vector Informatik)
  - `TABLE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the type of the data block.
SINGLE: An atomic element
LIST: An array
STRUCT: A struct
TABLE: An array of structs

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. WrapNvDataElement

**容器属性**:

- **UUID**: `abc6d578-6b78-4bd3-896d-d26031feaeab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WrapNvDataElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Contains a list of data elements, which are associated with the data block.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. WrapNvDeIndex

- **UUID**: `b453e46f-0a0d-47ab-84eb-fddc0ebe6a47`
- **参数名**: `WrapNvDeIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specify the order in which the data elements are generated within the data block.

############ 2. WrapNvDeLength

- **UUID**: `d8f10175-ec37-45c4-9d10-7a603407a883`
- **参数名**: `WrapNvDeLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the data element length in bytes.

########### STRING 类型参数

############ 1. WrapNvDeDescription

- **UUID**: `ae498df3-7888-4514-ade1-fe77795f9d90`
- **参数名**: `WrapNvDeDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description of the data element.

############ 2. WrapNvDeDefaultValue

- **UUID**: `6f08dba2-3c75-4224-b5ed-a3b1cffc5c94`
- **参数名**: `WrapNvDeDefaultValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0xFF`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value of this data element.
Only used by NVM, FEE and EA configurations.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. WrapNvDeNVMBlockRef

- **UUID**: `611a9a97-49c4-462c-a3de-cd883350de61`
- **引用名**: `WrapNvDeNVMBlockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a NvM block.

####### 2. WrapNvDataElement

**容器属性**:

- **UUID**: `abc6d578-6b78-4bd3-896d-d26031feaeab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WrapNvDataElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Contains a list of data elements, which are associated with the data block.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. WrapNvDeIndex

- **UUID**: `b453e46f-0a0d-47ab-84eb-fddc0ebe6a47`
- **参数名**: `WrapNvDeIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specify the order in which the data elements are generated within the data block.

########## 2. WrapNvDeLength

- **UUID**: `d8f10175-ec37-45c4-9d10-7a603407a883`
- **参数名**: `WrapNvDeLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the data element length in bytes.

######### STRING 类型参数

########## 1. WrapNvDeDescription

- **UUID**: `ae498df3-7888-4514-ade1-fe77795f9d90`
- **参数名**: `WrapNvDeDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description of the data element.

########## 2. WrapNvDeDefaultValue

- **UUID**: `6f08dba2-3c75-4224-b5ed-a3b1cffc5c94`
- **参数名**: `WrapNvDeDefaultValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0xFF`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value of this data element.
Only used by NVM, FEE and EA configurations.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. WrapNvDeNVMBlockRef

- **UUID**: `611a9a97-49c4-462c-a3de-cd883350de61`
- **引用名**: `WrapNvDeNVMBlockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a NvM block.

##### 4. WrapNvDataBlock

**容器属性**:

- **UUID**: `31b52828-282c-45a2-ac5a-a6248cf5017b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WrapNvDataBlock`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. WrapNvDbIndex

- **UUID**: `9ae09c91-bb5c-40ee-9cb2-853ae7a0e0d3`
- **参数名**: `WrapNvDbIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specify the order in which the data blocks are generated.

######## 2. WrapNvDbCount

- **UUID**: `d9d9395c-7233-4e24-83bc-2055dfa94bfa`
- **参数名**: `WrapNvDbCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of multiple data blocks in a contiguous area.

####### STRING 类型参数

######## 1. WrapNvDbDescription

- **UUID**: `32d99213-ddbb-464d-b049-44c19de6cf52`
- **参数名**: `WrapNvDbDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description of the data block.

####### ENUMERATION 类型参数

######## 1. WrapNvDbType

- **UUID**: `aaa6d251-4f21-46b5-81a8-551cfcea9442`
- **参数名**: `WrapNvDbType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SINGLE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SINGLE` (来源: Vector Informatik)
  - `LIST` (来源: Vector Informatik)
  - `STRUCT` (来源: Vector Informatik)
  - `TABLE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the type of the data block.
SINGLE: An atomic element
LIST: An array
STRUCT: A struct
TABLE: An array of structs

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. WrapNvDataElement

**容器属性**:

- **UUID**: `abc6d578-6b78-4bd3-896d-d26031feaeab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WrapNvDataElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Contains a list of data elements, which are associated with the data block.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. WrapNvDeIndex

- **UUID**: `b453e46f-0a0d-47ab-84eb-fddc0ebe6a47`
- **参数名**: `WrapNvDeIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specify the order in which the data elements are generated within the data block.

########## 2. WrapNvDeLength

- **UUID**: `d8f10175-ec37-45c4-9d10-7a603407a883`
- **参数名**: `WrapNvDeLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the data element length in bytes.

######### STRING 类型参数

########## 1. WrapNvDeDescription

- **UUID**: `ae498df3-7888-4514-ade1-fe77795f9d90`
- **参数名**: `WrapNvDeDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description of the data element.

########## 2. WrapNvDeDefaultValue

- **UUID**: `6f08dba2-3c75-4224-b5ed-a3b1cffc5c94`
- **参数名**: `WrapNvDeDefaultValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0xFF`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value of this data element.
Only used by NVM, FEE and EA configurations.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. WrapNvDeNVMBlockRef

- **UUID**: `611a9a97-49c4-462c-a3de-cd883350de61`
- **引用名**: `WrapNvDeNVMBlockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a NvM block.

##### 5. WrapNvDataElement

**容器属性**:

- **UUID**: `abc6d578-6b78-4bd3-896d-d26031feaeab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WrapNvDataElement`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Contains a list of data elements, which are associated with the data block.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. WrapNvDeIndex

- **UUID**: `b453e46f-0a0d-47ab-84eb-fddc0ebe6a47`
- **参数名**: `WrapNvDeIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specify the order in which the data elements are generated within the data block.

######## 2. WrapNvDeLength

- **UUID**: `d8f10175-ec37-45c4-9d10-7a603407a883`
- **参数名**: `WrapNvDeLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the data element length in bytes.

####### STRING 类型参数

######## 1. WrapNvDeDescription

- **UUID**: `ae498df3-7888-4514-ade1-fe77795f9d90`
- **参数名**: `WrapNvDeDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description of the data element.

######## 2. WrapNvDeDefaultValue

- **UUID**: `6f08dba2-3c75-4224-b5ed-a3b1cffc5c94`
- **参数名**: `WrapNvDeDefaultValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0xFF`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value of this data element.
Only used by NVM, FEE and EA configurations.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. WrapNvDeNVMBlockRef

- **UUID**: `611a9a97-49c4-462c-a3de-cd883350de61`
- **引用名**: `WrapNvDeNVMBlockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a NvM block.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **WrapNv_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **WrapNv**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **WrapNv_Pre**
2. **WrapNv_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. WrapNv_Impl

- **UUID**: `6b5e7b81-ec50-4309-b2af-96b401993468`
- **实现名称**: `WrapNv_Impl`
- **编程语言**: C
- **软件版本**: 2.04.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. WrapNv_Pre

- **UUID**: `8f40bcd6-180c-44d7-821b-55b4547bd262`
- **配置名称**: `WrapNv_Pre`
- **定义引用**: `/MICROSAR/WrapNv`

### 2. WrapNv_Rec

- **UUID**: `456bc0fa-314d-4a04-9bf0-06f96bc93296`
- **配置名称**: `WrapNv_Rec`
- **定义引用**: `/MICROSAR/WrapNv`
