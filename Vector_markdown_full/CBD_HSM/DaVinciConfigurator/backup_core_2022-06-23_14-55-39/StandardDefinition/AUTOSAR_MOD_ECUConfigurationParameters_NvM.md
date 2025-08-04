# NvM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:27

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [NvM](#nvm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. NvM

#### 基本信息

- **UUID**: `ECUC:add28e00-89a6-45a7-91ec-b997291c0da6`
- **模块名称**: `NvM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the NvM (NvRam Manager) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. NvMBlockDescriptor

**容器属性**:

- **UUID**: `ECUC:592eb68c-8ec5-46e2-aa34-9d55999b105e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NvMBlockDescriptor`
- **多重性**: [1..65536]
- **多配置容器**: false

**容器描述**:

Container for a management structure to configure the composition of a given NVRAM Block Management Type. Its multiplicity describes the number of configured NVRAM blocks, one block is required to be configured. The NVRAM block descriptors are condensed in the NVRAM block descriptor table.

###### 参数配置

此容器包含 **29** 个参数：

####### INTEGER 类型参数

######## 1. NvMBlockJobPriority

- **UUID**: `ECUC:1d526dbf-73e8-4c71-abfb-b1d9a2cfa016`
- **参数名**: `NvMBlockJobPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the job priority for a NVRAM block (0 = Immediate priority).

######## 2. NvMMaxNumOfReadRetries

- **UUID**: `ECUC:1031f94b-1419-4708-9937-a3edac24e9a7`
- **参数名**: `NvMMaxNumOfReadRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of read retries.

######## 3. NvMMaxNumOfWriteRetries

- **UUID**: `ECUC:78e2ed49-7ea2-41fd-ac91-2f65c9cd8908`
- **参数名**: `NvMMaxNumOfWriteRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of write retries for a NVRAM block with [NVM061_Conf]. Regardless of configuration a consistency check (and maybe write retries) are always forced for each block which is processed by the request NvM_WriteAll and NvM_WriteBlock.

######## 4. NvMNvBlockBaseNumber

- **UUID**: `ECUC:087b96a3-afec-4a8f-b375-50fdeaa19b1c`
- **参数名**: `NvMNvBlockBaseNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to perform the link between the NVM_NVRAM_BLOCK_IDENTIFIER used by the SW-Cs and the FEE_BLOCK_NUMBER expected by the memory abstraction modules. The parameter value equals the FEE_BLOCK_NUMBER or EA_BLOCK_NUMBER shifted to the right by NvMDatasetSelectionBits bits. (ref. to chapter 7.1.2.1).

######## 5. NvMNvBlockLength

- **UUID**: `ECUC:60ef00b3-517e-49f5-8942-16bc295ac588`
- **参数名**: `NvMNvBlockLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the NV block data length in bytes.

######## 6. NvMNvBlockNum

- **UUID**: `ECUC:77ade3a7-ce59-440d-a7e7-15fd9adefe05`
- **参数名**: `NvMNvBlockNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of multiple NV blocks in a contiguous area according to the given block management type.

######## 7. NvMNvramBlockIdentifier

- **UUID**: `ECUC:6ad9681e-a4cf-4630-96f8-0843c5a1f5ab`
- **参数名**: `NvMNvramBlockIdentifier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identification of a NVRAM block via a unique block identifier.

######## 8. NvMNvramDeviceId

- **UUID**: `ECUC:90f689ce-cc95-450a-a7d9-8a7044711d54`
- **参数名**: `NvMNvramDeviceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the NVRAM device ID where the NVRAM block is located.

######## 9. NvMRomBlockNum

- **UUID**: `ECUC:ddfe3c46-ad54-463e-b8b4-1e15564ae1b8`
- **参数名**: `NvMRomBlockNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of multiple ROM blocks in a contiguous area according to the given block management type.

######## 10. NvMWriteVerificationDataSize

- **UUID**: `ECUC:e044b935-bdee-42de-8b16-eda9a7279e49`
- **参数名**: `NvMWriteVerificationDataSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [1..65536]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of bytes to compare in each step when comparing the content of a RAM Block and a block read back.

####### BOOLEAN 类型参数

######## 1. NvMBlockUseCrc

- **UUID**: `ECUC:8a736e46-360a-438b-9066-a9a52092e5eb`
- **参数名**: `NvMBlockUseCrc`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines CRC usage for the NVRAM block, i.e. memory space for CRC is reserved in RAM and NV memory.

######## 2. NvMBlockUseSyncMechanism

- **UUID**: `ECUC:17667a35-d32a-4544-85dc-32bd1dc2663f`
- **参数名**: `NvMBlockUseSyncMechanism`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether an explicit synchronization mechanism with a RAM mirror and callback routiness for transferring data to and from NvM module's RAM mirror is used for NV block. true if synchronization mechanism is used, false otherwise.

######## 3. NvMBlockWriteProt

- **UUID**: `ECUC:583499ba-6121-4c40-88ee-ef45f8ccc250`
- **参数名**: `NvMBlockWriteProt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines an initial write protection of the NV block

######## 4. NvMBswMBlockStatusInformation

- **UUID**: `ECUC:eccb246d-a8a5-41a2-a478-f85dc807d31b`
- **参数名**: `NvMBswMBlockStatusInformation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies whether BswM is informed about the current status of the specified block.

######## 5. NvMCalcRamBlockCrc

- **UUID**: `ECUC:7a30fc79-9a8f-482f-ad77-0bbdaa443670`
- **参数名**: `NvMCalcRamBlockCrc`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines CRC (re)calculation for the permanent RAM block

######## 6. NvMResistantToChangedSw

- **UUID**: `ECUC:b94632c6-fe1d-4b6f-9ba2-f39c2a5689f8`
- **参数名**: `NvMResistantToChangedSw`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether a NVRAM block shall be treated resistant to configuration changes or not. If there is no default data available at configuration time then the application shall be responsible for providing the default initialization data. In this case the application has to use NvM_GetErrorStatus()to be able to distinguish between first initialization and corrupted data.

######## 7. NvMSelectBlockForReadAll

- **UUID**: `ECUC:863190d4-9883-4087-87c3-d2d52d03a810`
- **参数名**: `NvMSelectBlockForReadAll`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: NVM117: Defines whether a NVRAM block shall be processed during NvM_ReadAll or not. This configuration parameter has only influence on those NVRAM blocks which are configured to have a permanent RAM block.

######## 8. NvMSelectBlockForWriteAll

- **UUID**: `ECUC:54fd91d0-941a-4b67-9cc6-3d54449cf164`
- **参数名**: `NvMSelectBlockForWriteAll`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether a NVRAM block shall be processed during NvM_WriteAll or not. This configuration parameter has only influence on those NVRAM blocks which are configured to have a permanent RAM block.

######## 9. NvMStaticBlockIDCheck

- **UUID**: `ECUC:1a7d96ce-bcbe-4b69-8322-f18851048bdd`
- **参数名**: `NvMStaticBlockIDCheck`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the Static Block ID check is enabled.

######## 10. NvMWriteBlockOnce

- **UUID**: `ECUC:95a53ff9-d845-4bc8-9b07-cfe70a131869`
- **参数名**: `NvMWriteBlockOnce`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines write protection after first write. The NVRAM manager sets the write protection bit after the NV block was written the first time. This means that some of the NV blocks in the NVRAM should never be erased nor be replaced with the default ROM data after first initialization. [NVM276].

######## 11. NvMWriteVerification

- **UUID**: `ECUC:536e74a6-5a54-441f-8a7e-3a59ca814898`
- **参数名**: `NvMWriteVerification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if Write Verification is enabled.

####### STRING 类型参数

######## 1. NvMRamBlockDataAddress

- **UUID**: `ECUC:dad1e4d8-a71a-4307-938f-cebe91afb72b`
- **参数名**: `NvMRamBlockDataAddress`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the start address of the RAM block data.

######## 2. NvMRomBlockDataAddress

- **UUID**: `ECUC:c211eaf4-e050-4bec-8a1b-3423cd203f7d`
- **参数名**: `NvMRomBlockDataAddress`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the start address of the ROM block data.

####### ENUMERATION 类型参数

######## 1. NvMBlockCrcType

- **UUID**: `ECUC:b7447ae4-f639-4432-9efb-cd26e048e87f`
- **参数名**: `NvMBlockCrcType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NVM_CRC16` (来源: AUTOSAR_ECUC)
  - `NVM_CRC32` (来源: AUTOSAR_ECUC)
  - `NVM_CRC8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines CRC data width for the NVRAM block. Default: NVM_CRC16, i.e. CRC16 will be used  if NVM_BLOCK_USE_CRC==true

######## 2. NvMBlockManagementType

- **UUID**: `ECUC:d1b453dc-59c8-49c2-a231-ea5134267534`
- **参数名**: `NvMBlockManagementType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NVM_BLOCK_DATASET` (来源: AUTOSAR_ECUC)
  - `NVM_BLOCK_NATIVE` (来源: AUTOSAR_ECUC)
  - `NVM_BLOCK_REDUNDANT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the block management type for the NVRAM block.[NVM137]

####### FUNCTION-NAME 类型参数

######## 1. NvMInitBlockCallback

- **UUID**: `ECUC:22bf4a2c-db27-4831-9f50-dcebf7417aa8`
- **参数名**: `NvMInitBlockCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Entry address of a block specific callback routine which shall be called if no ROM data is available for initialization of the NVRAM block.

######## 2. NvMReadRamBlockFromNvCallback

- **UUID**: `ECUC:d3023e40-444d-4c8e-a1f0-0456f60dbf22`
- **参数名**: `NvMReadRamBlockFromNvCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Entry address of a block specific callback routine which shall be called in order to let the application copy data from the NvM module's mirror to RAM block.

######## 3. NvMSingleBlockCallback

- **UUID**: `ECUC:a93648f0-18dc-4497-8e1f-0241129ae9d4`
- **参数名**: `NvMSingleBlockCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Entry address of the block specific callback routine which shall be invoked on termination of each asynchronous single block request [NVM113].

######## 4. NvMWriteRamBlockToNvCallback

- **UUID**: `ECUC:3b6b0539-92f3-4d2f-8d12-cbf3a056b262`
- **参数名**: `NvMWriteRamBlockToNvCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Entry address of a block specific callback routine which shall be called in order to let the application copy data from RAM block to NvM module's mirror.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. NvMEaRef

**容器属性**:

- **UUID**: `ECUC:90f4fd54-5801-429b-9642-06ef3acc3387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NvMEaRef`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

EEPROM Abstraction

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. NvMNameOfEaBlock

- **UUID**: `ECUC:378ccf77-6afa-4fb2-814c-d86e91c3bbc8`
- **引用名**: `NvMNameOfEaBlock`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EaBlockConfiguration`
- **完整路径**: `/AUTOSAR/EcucDefs/Ea/EaBlockConfiguration`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: reference to EaBlock

####### 2. NvMFeeRef

**容器属性**:

- **UUID**: `ECUC:5c319a41-37d1-4b63-8011-c8bf807095f5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NvMFeeRef`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Flash EEPROM Emulation

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. NvMNameOfFeeBlock

- **UUID**: `ECUC:48167eeb-a01f-4420-a942-3a98967b1fbb`
- **引用名**: `NvMNameOfFeeBlock`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FeeBlockConfiguration`
- **完整路径**: `/AUTOSAR/EcucDefs/Fee/FeeBlockConfiguration`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: reference to FeeBlock

####### 3. NvMTargetBlockReference

**容器属性**:

- **UUID**: `ECUC:bdbb119b-7ccd-46ea-9a91-2bfa0300418e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `NvMTargetBlockReference`
- **多重性**: [1..1]

**容器选择**:

- **NvMEaRef**
  - UUID: `ECUC:90f4fd54-5801-429b-9642-06ef3acc3387`
  - 描述: EEPROM Abstraction
- **NvMFeeRef**
  - UUID: `ECUC:5c319a41-37d1-4b63-8011-c8bf807095f5`
  - 描述: Flash EEPROM Emulation

**容器描述**:

This parameter is just a container for the parameters for EA and FEE

##### 2. NvMEaRef

**容器属性**:

- **UUID**: `ECUC:90f4fd54-5801-429b-9642-06ef3acc3387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NvMEaRef`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

EEPROM Abstraction

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. NvMNameOfEaBlock

- **UUID**: `ECUC:378ccf77-6afa-4fb2-814c-d86e91c3bbc8`
- **引用名**: `NvMNameOfEaBlock`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EaBlockConfiguration`
- **完整路径**: `/AUTOSAR/EcucDefs/Ea/EaBlockConfiguration`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: reference to EaBlock

##### 3. NvMFeeRef

**容器属性**:

- **UUID**: `ECUC:5c319a41-37d1-4b63-8011-c8bf807095f5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NvMFeeRef`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Flash EEPROM Emulation

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. NvMNameOfFeeBlock

- **UUID**: `ECUC:48167eeb-a01f-4420-a942-3a98967b1fbb`
- **引用名**: `NvMNameOfFeeBlock`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FeeBlockConfiguration`
- **完整路径**: `/AUTOSAR/EcucDefs/Fee/FeeBlockConfiguration`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: reference to FeeBlock

##### 4. NvMCommon

**容器属性**:

- **UUID**: `ECUC:629d2250-f495-4827-9660-195f8642e4fd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NvMCommon`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container for common configuration options.

###### 参数配置

此容器包含 **16** 个参数：

####### INTEGER 类型参数

######## 1. NvMCompiledConfigId

- **UUID**: `ECUC:5900b6cf-53e9-49d8-878f-65aed90f88f6`
- **参数名**: `NvMCompiledConfigId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration ID regarding the NV memory layout. This configuration ID shall be published as e.g. a SW-C shall have the possibility to write it to NV memory.

######## 2. NvMCrcNumOfBytes

- **UUID**: `ECUC:18ffdb77-2c48-49d0-a34c-55bad1ed237c`
- **参数名**: `NvMCrcNumOfBytes`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If CRC is configured for at least one NVRAM block, this parameter defines the maximum number of bytes which shall be processed within one cycle of job processing.

######## 3. NvMDatasetSelectionBits

- **UUID**: `ECUC:c9acf3f3-3f67-48b6-99b6-61a6378e6ed1`
- **参数名**: `NvMDatasetSelectionBits`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of least significant bits which shall be used to address a certain dataset of a NVRAM block within the interface to the memory hardware abstraction.

######## 4. NvMRepeatMirrorOperations

- **UUID**: `ECUC:51308b85-4893-4a39-a736-7283da5f78ca`
- **参数名**: `NvMRepeatMirrorOperations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of retries to let the application copy data to or from the NvM module's mirror before postponing the current job.

######## 5. NvMSizeImmediateJobQueue

- **UUID**: `ECUC:42bd46ac-fa9a-4160-8a9f-d6a3a223b3f2`
- **参数名**: `NvMSizeImmediateJobQueue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of queue entries for the immediate priority job queue. If NVM_JOB_PRIORITIZATION is switched OFF this parameter shall be out of scope.

######## 6. NvMSizeStandardJobQueue

- **UUID**: `ECUC:b6ee37b4-27bb-4334-8782-37a66ef6a5e5`
- **参数名**: `NvMSizeStandardJobQueue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of queue entries for the standard job queue.

####### BOOLEAN 类型参数

######## 1. NvMBswMMultiBlockJobStatusInformation

- **UUID**: `ECUC:70475090-57ec-4ce9-afdc-d82075f01a78`
- **参数名**: `NvMBswMMultiBlockJobStatusInformation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies whether BswM is informed about the current status of the multiblock job.

######## 2. NvMDevErrorDetect

- **UUID**: `ECUC:d54c9a22-5fb3-489c-9a6d-bbd5d848859c`
- **参数名**: `NvMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable development error detection.

######## 3. NvMDrvModeSwitch

- **UUID**: `ECUC:e2f92e79-6cf7-433b-89c4-7453b7617a22`
- **参数名**: `NvMDrvModeSwitch`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable switching memory drivers to fast mode during performing NvM_ReadAll and NvM_WriteAll

######## 4. NvMDynamicConfiguration

- **UUID**: `ECUC:87a82f46-5ed9-45cb-909e-6d826c161f36`
- **参数名**: `NvMDynamicConfiguration`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable the dynamic configuration management handling by the NvM_ReadAll request.

######## 5. NvMJobPrioritization

- **UUID**: `ECUC:8105b3ea-e773-4f2e-9f89-22e9e58f874b`
- **参数名**: `NvMJobPrioritization`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable job prioritization handling

######## 6. NvMPollingMode

- **UUID**: `ECUC:053fb1f7-d703-4773-a004-87391a430d45`
- **参数名**: `NvMPollingMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable/disable the polling mode in the NVRAM Manager and at the same time disable/enable the callback functions useable by lower layers

######## 7. NvMSetRamBlockStatusApi

- **UUID**: `ECUC:6e124429-e18f-4b2c-b790-6cad1259de79`
- **参数名**: `NvMSetRamBlockStatusApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable the API NvM_SetRamBlockStatus.

######## 8. NvMVersionInfoApi

- **UUID**: `ECUC:505b5889-cc12-4684-aef0-cf8c9d71176e`
- **参数名**: `NvMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information [NVM285], [NVM286].

####### ENUMERATION 类型参数

######## 1. NvMApiConfigClass

- **UUID**: `ECUC:5b839f42-032f-48fd-9d5f-a80f7eaf4e60`
- **参数名**: `NvMApiConfigClass`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NVM_API_CONFIG_CLASS_1` (来源: AUTOSAR_ECUC)
  - `NVM_API_CONFIG_CLASS_2` (来源: AUTOSAR_ECUC)
  - `NVM_API_CONFIG_CLASS_3` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Preprocessor switch to enable some API calls which are related to NVM API configuration classes.

####### FUNCTION-NAME 类型参数

######## 1. NvMMultiBlockCallback

- **UUID**: `ECUC:cd0e20fd-32f3-44cd-b73a-fed99a446e01`
- **参数名**: `NvMMultiBlockCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Entry address of the common callback routine which shall be invoked on termination of each asynchronous multi block request

##### 5. NvmDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:53c6dcf1-a51c-404e-9986-89750b749edb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NvmDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **7** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. NVM_E_INTEGRITY_FAILED

- **UUID**: `ECUC:7ab1f486-d96b-41ca-bf55-ada6c06abd6d`
- **引用名**: `NVM_E_INTEGRITY_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "API request integrity failed" has occured.

######## 2. NVM_E_LOSS_OF_REDUNDANCY

- **UUID**: `ECUC:7ae40494-2a5b-4076-9cf0-055cc7917e05`
- **引用名**: `NVM_E_LOSS_OF_REDUNDANCY`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "loss of redundancy" has occured.

######## 3. NVM_E_QUEUE_OVERFLOW

- **UUID**: `ECUC:a4d38dd4-d2b4-43c9-8f2c-37320a982e89`
- **引用名**: `NVM_E_QUEUE_OVERFLOW`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "NVRAM Managers job queue overflow" has occured.

######## 4. NVM_E_REQ_FAILED

- **UUID**: `ECUC:e67d652c-67ff-419e-aa7f-3b2d7c38b2a5`
- **引用名**: `NVM_E_REQ_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "API request failed" has occured.

######## 5. NVM_E_VERIFY_FAILED

- **UUID**: `ECUC:2b751628-9fc7-4bfb-b061-3c98d45ae44c`
- **引用名**: `NVM_E_VERIFY_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Write Verification failed" has occured.

######## 6. NVM_E_WRITE_PROTECTED

- **UUID**: `ECUC:83187ce0-6e2e-4905-94d0-8e924685ce3b`
- **引用名**: `NVM_E_WRITE_PROTECTED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "write attempt to NVRAM block with write protection" has occured.

######## 7. NVM_E_WRONG_BLOCK_ID

- **UUID**: `ECUC:76f309e7-892a-455a-87f2-2398607962ba`
- **引用名**: `NVM_E_WRONG_BLOCK_ID`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Static Block ID check failed" has occured.

##### 6. NvMTargetBlockReference

**容器属性**:

- **UUID**: `ECUC:bdbb119b-7ccd-46ea-9a91-2bfa0300418e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `NvMTargetBlockReference`
- **多重性**: [1..1]

**容器选择**:

- **NvMEaRef**
  - UUID: `ECUC:90f4fd54-5801-429b-9642-06ef3acc3387`
  - 描述: EEPROM Abstraction
- **NvMFeeRef**
  - UUID: `ECUC:5c319a41-37d1-4b63-8011-c8bf807095f5`
  - 描述: Flash EEPROM Emulation

**容器描述**:

This parameter is just a container for the parameters for EA and FEE

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

1. **NvM**
