# FlsTst - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:19

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FlsTst](#flstst)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FlsTst

#### 基本信息

- **UUID**: `ECUC:93c62845-0468-4a62-a9e8-eb17927870c7`
- **模块名称**: `FlsTst`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. FlsTstConfigSet

**容器属性**:

- **UUID**: `ECUC:23d69abe-15bd-4ad1-be2f-7d74f72852ac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

Multiple Configuration Set Container

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. FlsTstBlockNumberBgnd

- **UUID**: `ECUC:7c76fc01-65e8-4fd6-af42-e2958a87dff6`
- **参数名**: `FlsTstBlockNumberBgnd`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the number of test blocks available for the background test.

######## 2. FlsTstBlockNumberFgnd

- **UUID**: `ECUC:c967b88a-8ce4-48d4-b624-979fa294a0c4`
- **参数名**: `FlsTstBlockNumberFgnd`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the number of test blocks available for the foreground test.

####### FUNCTION-NAME 类型参数

######## 1. FlsTstTestCompletedNotification

- **UUID**: `ECUC:d364b43b-6bd2-4604-b6f6-e7bee7dfaf2b`
- **参数名**: `FlsTstTestCompletedNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pointer to function, which shall be called after finishing the background Flash test interval.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. FlsTstBlockBgndConfigSet

**容器属性**:

- **UUID**: `ECUC:2d3da7f1-7c56-495c-986d-b3c84a2a0848`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlockBgndConfigSet`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the blocks in background mode.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FlsTstBlock

**容器属性**:

- **UUID**: `ECUC:608395df-56f2-978a-2fa5-c1e7e8bf6f23`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlock`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters for an individual test block.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. FlsTstBlockBaseAddress

- **UUID**: `ECUC:c26699be-228f-d99c-e235-de03d0c86d2d`
- **参数名**: `FlsTstBlockBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the Flash block.

############ 2. FlsTstBlockIndex

- **UUID**: `ECUC:8edcecfb-d1cc-e6c2-c955-f03ba1a27079`
- **参数名**: `FlsTstBlockIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreground Test: Index identifies block to be tested by FlsTst_StartFgnd();

############ 3. FlsTstBlockSize

- **UUID**: `ECUC:b23e2b15-0583-e0cb-b0bf-04c224528bd4`
- **参数名**: `FlsTstBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the Flash Test block size.

############ 4. FlsTstNumberOfTestedCells

- **UUID**: `ECUC:5e16d872-3253-dfd1-cf4c-60e46b05a0fb`
- **参数名**: `FlsTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the Number of cells to be tested in background mode during one scheduled task (FlsTst_MainFunction() call).

############ 5. FlsTstSignatureAddress

- **UUID**: `ECUC:51ef9e8f-bc7c-db4c-b028-ac2922cbb6ff`
- **参数名**: `FlsTstSignatureAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the signature reference value of the Flash test block.

########### ENUMERATION 类型参数

############ 1. FlsTstTestAlgorithm

- **UUID**: `ECUC:9a03033e-e89d-e322-b076-39c392b10d52`
- **参数名**: `FlsTstTestAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FLSTST_16BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_32BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_8BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_CHECKSUM` (来源: AUTOSAR_ECUC)
  - `FLSTST_DUPLICATED_MEMORY` (来源: AUTOSAR_ECUC)
  - `FLSTST_ECC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the configuration of the test algorithm for foreground mode and background mode. The availability of algorithm is implementation specific.

####### 2. FlsTstBlock

**容器属性**:

- **UUID**: `ECUC:608395df-56f2-978a-2fa5-c1e7e8bf6f23`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlock`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters for an individual test block.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. FlsTstBlockBaseAddress

- **UUID**: `ECUC:c26699be-228f-d99c-e235-de03d0c86d2d`
- **参数名**: `FlsTstBlockBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the Flash block.

########## 2. FlsTstBlockIndex

- **UUID**: `ECUC:8edcecfb-d1cc-e6c2-c955-f03ba1a27079`
- **参数名**: `FlsTstBlockIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreground Test: Index identifies block to be tested by FlsTst_StartFgnd();

########## 3. FlsTstBlockSize

- **UUID**: `ECUC:b23e2b15-0583-e0cb-b0bf-04c224528bd4`
- **参数名**: `FlsTstBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the Flash Test block size.

########## 4. FlsTstNumberOfTestedCells

- **UUID**: `ECUC:5e16d872-3253-dfd1-cf4c-60e46b05a0fb`
- **参数名**: `FlsTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the Number of cells to be tested in background mode during one scheduled task (FlsTst_MainFunction() call).

########## 5. FlsTstSignatureAddress

- **UUID**: `ECUC:51ef9e8f-bc7c-db4c-b028-ac2922cbb6ff`
- **参数名**: `FlsTstSignatureAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the signature reference value of the Flash test block.

######### ENUMERATION 类型参数

########## 1. FlsTstTestAlgorithm

- **UUID**: `ECUC:9a03033e-e89d-e322-b076-39c392b10d52`
- **参数名**: `FlsTstTestAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FLSTST_16BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_32BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_8BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_CHECKSUM` (来源: AUTOSAR_ECUC)
  - `FLSTST_DUPLICATED_MEMORY` (来源: AUTOSAR_ECUC)
  - `FLSTST_ECC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the configuration of the test algorithm for foreground mode and background mode. The availability of algorithm is implementation specific.

####### 3. FlsTstBlockFgndConfigSet

**容器属性**:

- **UUID**: `ECUC:5a0feb16-8c6e-4693-b653-481426f2b045`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlockFgndConfigSet`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the blocks in foreground mode.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FlsTstBlock

**容器属性**:

- **UUID**: `ECUC:8d55d904-670a-94c1-4d8b-5633c5881720`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlock`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters for an individual test block.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. FlsTstBlockBaseAddress

- **UUID**: `ECUC:ef38dce3-32a7-d6d3-001b-724fad91152a`
- **参数名**: `FlsTstBlockBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the Flash block.

############ 2. FlsTstBlockIndex

- **UUID**: `ECUC:bbaf3020-e1e4-e3f9-e73b-84877e6b1876`
- **参数名**: `FlsTstBlockIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreground Test: Index identifies block to be tested by FlsTst_StartFgnd();

############ 3. FlsTstBlockSize

- **UUID**: `ECUC:df106e3a-159b-de02-cea4-990e011b33d1`
- **参数名**: `FlsTstBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the Flash Test block size.

############ 4. FlsTstNumberOfTestedCells

- **UUID**: `ECUC:8ae91b97-426b-dd08-ed31-f53047ce48f8`
- **参数名**: `FlsTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the Number of cells to be tested in background mode during one scheduled task (FlsTst_MainFunction() call).

############ 5. FlsTstSignatureAddress

- **UUID**: `ECUC:7ec1e1b4-cc94-d883-ce0e-4074ff945efc`
- **参数名**: `FlsTstSignatureAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the signature reference value of the Flash test block.

########### ENUMERATION 类型参数

############ 1. FlsTstTestAlgorithm

- **UUID**: `ECUC:c6d54663-f8b5-e059-ce5b-ce0f6f79b54f`
- **参数名**: `FlsTstTestAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FLSTST_16BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_32BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_8BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_CHECKSUM` (来源: AUTOSAR_ECUC)
  - `FLSTST_DUPLICATED_MEMORY` (来源: AUTOSAR_ECUC)
  - `FLSTST_ECC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the configuration of the test algorithm for foreground mode and background mode. The availability of algorithm is implementation specific.

####### 4. FlsTstBlock

**容器属性**:

- **UUID**: `ECUC:8d55d904-670a-94c1-4d8b-5633c5881720`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlock`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters for an individual test block.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. FlsTstBlockBaseAddress

- **UUID**: `ECUC:ef38dce3-32a7-d6d3-001b-724fad91152a`
- **参数名**: `FlsTstBlockBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the Flash block.

########## 2. FlsTstBlockIndex

- **UUID**: `ECUC:bbaf3020-e1e4-e3f9-e73b-84877e6b1876`
- **参数名**: `FlsTstBlockIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreground Test: Index identifies block to be tested by FlsTst_StartFgnd();

########## 3. FlsTstBlockSize

- **UUID**: `ECUC:df106e3a-159b-de02-cea4-990e011b33d1`
- **参数名**: `FlsTstBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the Flash Test block size.

########## 4. FlsTstNumberOfTestedCells

- **UUID**: `ECUC:8ae91b97-426b-dd08-ed31-f53047ce48f8`
- **参数名**: `FlsTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the Number of cells to be tested in background mode during one scheduled task (FlsTst_MainFunction() call).

########## 5. FlsTstSignatureAddress

- **UUID**: `ECUC:7ec1e1b4-cc94-d883-ce0e-4074ff945efc`
- **参数名**: `FlsTstSignatureAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the signature reference value of the Flash test block.

######### ENUMERATION 类型参数

########## 1. FlsTstTestAlgorithm

- **UUID**: `ECUC:c6d54663-f8b5-e059-ce5b-ce0f6f79b54f`
- **参数名**: `FlsTstTestAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FLSTST_16BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_32BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_8BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_CHECKSUM` (来源: AUTOSAR_ECUC)
  - `FLSTST_DUPLICATED_MEMORY` (来源: AUTOSAR_ECUC)
  - `FLSTST_ECC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the configuration of the test algorithm for foreground mode and background mode. The availability of algorithm is implementation specific.

##### 2. FlsTstBlockBgndConfigSet

**容器属性**:

- **UUID**: `ECUC:2d3da7f1-7c56-495c-986d-b3c84a2a0848`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlockBgndConfigSet`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the blocks in background mode.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FlsTstBlock

**容器属性**:

- **UUID**: `ECUC:608395df-56f2-978a-2fa5-c1e7e8bf6f23`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlock`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters for an individual test block.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. FlsTstBlockBaseAddress

- **UUID**: `ECUC:c26699be-228f-d99c-e235-de03d0c86d2d`
- **参数名**: `FlsTstBlockBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the Flash block.

########## 2. FlsTstBlockIndex

- **UUID**: `ECUC:8edcecfb-d1cc-e6c2-c955-f03ba1a27079`
- **参数名**: `FlsTstBlockIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreground Test: Index identifies block to be tested by FlsTst_StartFgnd();

########## 3. FlsTstBlockSize

- **UUID**: `ECUC:b23e2b15-0583-e0cb-b0bf-04c224528bd4`
- **参数名**: `FlsTstBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the Flash Test block size.

########## 4. FlsTstNumberOfTestedCells

- **UUID**: `ECUC:5e16d872-3253-dfd1-cf4c-60e46b05a0fb`
- **参数名**: `FlsTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the Number of cells to be tested in background mode during one scheduled task (FlsTst_MainFunction() call).

########## 5. FlsTstSignatureAddress

- **UUID**: `ECUC:51ef9e8f-bc7c-db4c-b028-ac2922cbb6ff`
- **参数名**: `FlsTstSignatureAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the signature reference value of the Flash test block.

######### ENUMERATION 类型参数

########## 1. FlsTstTestAlgorithm

- **UUID**: `ECUC:9a03033e-e89d-e322-b076-39c392b10d52`
- **参数名**: `FlsTstTestAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FLSTST_16BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_32BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_8BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_CHECKSUM` (来源: AUTOSAR_ECUC)
  - `FLSTST_DUPLICATED_MEMORY` (来源: AUTOSAR_ECUC)
  - `FLSTST_ECC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the configuration of the test algorithm for foreground mode and background mode. The availability of algorithm is implementation specific.

##### 3. FlsTstBlock

**容器属性**:

- **UUID**: `ECUC:608395df-56f2-978a-2fa5-c1e7e8bf6f23`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlock`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters for an individual test block.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. FlsTstBlockBaseAddress

- **UUID**: `ECUC:c26699be-228f-d99c-e235-de03d0c86d2d`
- **参数名**: `FlsTstBlockBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the Flash block.

######## 2. FlsTstBlockIndex

- **UUID**: `ECUC:8edcecfb-d1cc-e6c2-c955-f03ba1a27079`
- **参数名**: `FlsTstBlockIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreground Test: Index identifies block to be tested by FlsTst_StartFgnd();

######## 3. FlsTstBlockSize

- **UUID**: `ECUC:b23e2b15-0583-e0cb-b0bf-04c224528bd4`
- **参数名**: `FlsTstBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the Flash Test block size.

######## 4. FlsTstNumberOfTestedCells

- **UUID**: `ECUC:5e16d872-3253-dfd1-cf4c-60e46b05a0fb`
- **参数名**: `FlsTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the Number of cells to be tested in background mode during one scheduled task (FlsTst_MainFunction() call).

######## 5. FlsTstSignatureAddress

- **UUID**: `ECUC:51ef9e8f-bc7c-db4c-b028-ac2922cbb6ff`
- **参数名**: `FlsTstSignatureAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the signature reference value of the Flash test block.

####### ENUMERATION 类型参数

######## 1. FlsTstTestAlgorithm

- **UUID**: `ECUC:9a03033e-e89d-e322-b076-39c392b10d52`
- **参数名**: `FlsTstTestAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FLSTST_16BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_32BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_8BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_CHECKSUM` (来源: AUTOSAR_ECUC)
  - `FLSTST_DUPLICATED_MEMORY` (来源: AUTOSAR_ECUC)
  - `FLSTST_ECC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the configuration of the test algorithm for foreground mode and background mode. The availability of algorithm is implementation specific.

##### 4. FlsTstBlockFgndConfigSet

**容器属性**:

- **UUID**: `ECUC:5a0feb16-8c6e-4693-b653-481426f2b045`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlockFgndConfigSet`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container defines the blocks in foreground mode.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FlsTstBlock

**容器属性**:

- **UUID**: `ECUC:8d55d904-670a-94c1-4d8b-5633c5881720`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlock`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters for an individual test block.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. FlsTstBlockBaseAddress

- **UUID**: `ECUC:ef38dce3-32a7-d6d3-001b-724fad91152a`
- **参数名**: `FlsTstBlockBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the Flash block.

########## 2. FlsTstBlockIndex

- **UUID**: `ECUC:bbaf3020-e1e4-e3f9-e73b-84877e6b1876`
- **参数名**: `FlsTstBlockIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreground Test: Index identifies block to be tested by FlsTst_StartFgnd();

########## 3. FlsTstBlockSize

- **UUID**: `ECUC:df106e3a-159b-de02-cea4-990e011b33d1`
- **参数名**: `FlsTstBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the Flash Test block size.

########## 4. FlsTstNumberOfTestedCells

- **UUID**: `ECUC:8ae91b97-426b-dd08-ed31-f53047ce48f8`
- **参数名**: `FlsTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the Number of cells to be tested in background mode during one scheduled task (FlsTst_MainFunction() call).

########## 5. FlsTstSignatureAddress

- **UUID**: `ECUC:7ec1e1b4-cc94-d883-ce0e-4074ff945efc`
- **参数名**: `FlsTstSignatureAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the signature reference value of the Flash test block.

######### ENUMERATION 类型参数

########## 1. FlsTstTestAlgorithm

- **UUID**: `ECUC:c6d54663-f8b5-e059-ce5b-ce0f6f79b54f`
- **参数名**: `FlsTstTestAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FLSTST_16BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_32BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_8BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_CHECKSUM` (来源: AUTOSAR_ECUC)
  - `FLSTST_DUPLICATED_MEMORY` (来源: AUTOSAR_ECUC)
  - `FLSTST_ECC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the configuration of the test algorithm for foreground mode and background mode. The availability of algorithm is implementation specific.

##### 5. FlsTstBlock

**容器属性**:

- **UUID**: `ECUC:8d55d904-670a-94c1-4d8b-5633c5881720`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstBlock`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters for an individual test block.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. FlsTstBlockBaseAddress

- **UUID**: `ECUC:ef38dce3-32a7-d6d3-001b-724fad91152a`
- **参数名**: `FlsTstBlockBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start Address of the Flash block.

######## 2. FlsTstBlockIndex

- **UUID**: `ECUC:bbaf3020-e1e4-e3f9-e73b-84877e6b1876`
- **参数名**: `FlsTstBlockIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreground Test: Index identifies block to be tested by FlsTst_StartFgnd();

######## 3. FlsTstBlockSize

- **UUID**: `ECUC:df106e3a-159b-de02-cea4-990e011b33d1`
- **参数名**: `FlsTstBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the Flash Test block size.

######## 4. FlsTstNumberOfTestedCells

- **UUID**: `ECUC:8ae91b97-426b-dd08-ed31-f53047ce48f8`
- **参数名**: `FlsTstNumberOfTestedCells`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the Number of cells to be tested in background mode during one scheduled task (FlsTst_MainFunction() call).

######## 5. FlsTstSignatureAddress

- **UUID**: `ECUC:7ec1e1b4-cc94-d883-ce0e-4074ff945efc`
- **参数名**: `FlsTstSignatureAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address of the signature reference value of the Flash test block.

####### ENUMERATION 类型参数

######## 1. FlsTstTestAlgorithm

- **UUID**: `ECUC:c6d54663-f8b5-e059-ce5b-ce0f6f79b54f`
- **参数名**: `FlsTstTestAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FLSTST_16BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_32BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_8BIT_CRC` (来源: AUTOSAR_ECUC)
  - `FLSTST_CHECKSUM` (来源: AUTOSAR_ECUC)
  - `FLSTST_DUPLICATED_MEMORY` (来源: AUTOSAR_ECUC)
  - `FLSTST_ECC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the configuration of the test algorithm for foreground mode and background mode. The availability of algorithm is implementation specific.

##### 6. FlsTstConfigurationOfOptApiServices

**容器属性**:

- **UUID**: `ECUC:ec60b8da-1d0d-4723-bf65-01447897a739`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstConfigurationOfOptApiServices`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **10** 个参数：

####### BOOLEAN 类型参数

######## 1. FlsTstGetCurrentStateApi

- **UUID**: `ECUC:601735b2-9e41-47ee-92e6-5c6517135bb2`
- **参数名**: `FlsTstGetCurrentStateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service FlsTst_GetCurrentState() from the code.

######## 2. FlsTstGetErrorDetailsApi

- **UUID**: `ECUC:04d8f2ad-9859-4896-82fb-6eb5f8c403c1`
- **参数名**: `FlsTstGetErrorDetailsApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service FlsTst_GetErrorDetails() from the code.

######## 3. FlsTstGetTestResultBgndApi

- **UUID**: `ECUC:3a6605ec-996d-44be-8c35-c9b118ac7dfa`
- **参数名**: `FlsTstGetTestResultBgndApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service FlsTst_GetTestResultBgnd() from the code.

######## 4. FlsTstGetTestResultFgndApi

- **UUID**: `ECUC:e0ad570a-29b9-4f78-b55e-56dad47cc6b4`
- **参数名**: `FlsTstGetTestResultFgndApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service FlsTst_GetTestResultFgnd() from the code.

######## 5. FlsTstGetTestSignatureBgndApi

- **UUID**: `ECUC:ec71d351-c85e-4707-ac6e-0085b1d98de1`
- **参数名**: `FlsTstGetTestSignatureBgndApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service FlsTst_GetTestSignatureBgnd() from the code.

######## 6. FlsTstGetTestSignatureFgndApi

- **UUID**: `ECUC:bbc3af3b-a049-4af1-b0dc-3706f7089ea8`
- **参数名**: `FlsTstGetTestSignatureFgndApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service FlsTst_GetTestSignatureFgnd() from the code.

######## 7. FlsTstStartFgndApi

- **UUID**: `ECUC:5f9f338e-9e84-421b-ae36-923db7b89b09`
- **参数名**: `FlsTstStartFgndApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service FlsTst_StartFgnd() from the code.

######## 8. FlsTstSuspendResumeApi

- **UUID**: `ECUC:f7482c3f-bee5-4425-a436-5613141742cd`
- **参数名**: `FlsTstSuspendResumeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the services FlsTst_Suspend() and FlsTst_Resume() from the code.

######## 9. FlsTstTestEccApi

- **UUID**: `ECUC:c461078f-ff6d-4cf3-9c9c-da135558510a`
- **参数名**: `FlsTstTestEccApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service FlsTst_TestEcc() from the code.

######## 10. FlsTstVersionInfoApi

- **UUID**: `ECUC:88fd2777-3ba7-4ca4-aba3-ebce8930ce59`
- **参数名**: `FlsTstVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service FlsTst_GetVersionInfo() from the code.

##### 7. FlsTstDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:4b71fe1e-41ad-4031-800a-8feacff53a65`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FLSTST_E_FLSTST_FAILURE

- **UUID**: `ECUC:9641dfcf-33f5-4cdf-96d8-894ec771cd80`
- **引用名**: `FLSTST_E_FLSTST_FAILURE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash Failure" has occurred.

##### 8. FlsTstGeneral

**容器属性**:

- **UUID**: `ECUC:584aed6b-3c67-4c26-9dba-cb5ead4c6e43`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsTstGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. FlsTstNumberOfTestedCellsAtomic

- **UUID**: `ECUC:de6df7a3-2b54-40be-8ec2-9fb59f51df97`
- **参数名**: `FlsTstNumberOfTestedCellsAtomic`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the Number of cells to be tested in background mode without checking user requests (Abort, Suspend).

######## 2. FlsTstTestIntervalIdEndValue

- **UUID**: `ECUC:591826e0-485c-4501-91e8-6f6b59f23278`
- **参数名**: `FlsTstTestIntervalIdEndValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the end value of the Test Interval Id.

####### BOOLEAN 类型参数

######## 1. FlsTstDevErrorDetect

- **UUID**: `ECUC:2f1d62e4-0908-4ebd-8777-9273474e6cdf`
- **参数名**: `FlsTstDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for enabling the development error detection.

######## 2. FlsTstTestCompletedNotificationSupported

- **UUID**: `ECUC:210ad56a-d1a4-45c4-b1cd-ec780ea493f3`
- **参数名**: `FlsTstTestCompletedNotificationSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to indicate that the notification is supported.

######## 3. FlsTstTestResultSignature

- **UUID**: `ECUC:395989c7-ed0c-4221-8673-221af7ae243e`
- **参数名**: `FlsTstTestResultSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the result of the test in background mode:

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

1. **FlsTst**
