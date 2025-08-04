# Fls - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:12

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Fls](#fls)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Fls

#### 基本信息

- **UUID**: `ECUC:d05369fd-d6e0-44c1-8a9f-9d2a5561badf`
- **模块名称**: `Fls`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the Fls (internal or external flash driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **9** 个配置容器：

##### 1. FlsConfigSet

**容器属性**:

- **UUID**: `ECUC:3d6f9ca5-bb01-4ee7-bd4f-253b60f2cc46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsConfigSet`
- **多重性**: [0..1]

**容器描述**:

Container for runtime configuration parameters of the flash driver.

###### 参数配置

此容器包含 **15** 个参数：

####### INTEGER 类型参数

######## 1. FlsAcErase

- **UUID**: `ECUC:2a204be2-76ae-465c-b358-c7c06f4d42ce`
- **参数名**: `FlsAcErase`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Address offset in RAM to which the erase flash access code shall be loaded.

######## 2. FlsAcWrite

- **UUID**: `ECUC:326f888f-0676-4eec-a10e-f8159c0655ee`
- **参数名**: `FlsAcWrite`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Address offset in RAM to which the write flash access code shall be loaded.

######## 3. FlsMaxReadFastMode

- **UUID**: `ECUC:1095bfd8-716a-4dfb-a62d-89ee6d513df9`
- **参数名**: `FlsMaxReadFastMode`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `64`
- **取值范围**: [1..1048576]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum number of bytes to read or compare in one cycle of the flash driver's job processing function in fast mode.                             Note: The value configured for FlsMaxReadFastMode should be more than the value configured for FlsMaxReadNormalMode

######## 4. FlsMaxReadNormalMode

- **UUID**: `ECUC:fc26eec9-3ec1-4860-a1e2-905f73d14265`
- **参数名**: `FlsMaxReadNormalMode`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `32`
- **取值范围**: [1..1048576]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum number of bytes to read or compare in one cycle of the flash driver's job processing function in normal mode.

######## 5. FlsMaxWriteFastMode

- **UUID**: `ECUC:006f40ff-e794-490e-9ec6-057e04aada0c`
- **参数名**: `FlsMaxWriteFastMode`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `32`
- **取值范围**: [32..32]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum number of bytes to write in one cycle of the flash driver's job processing function in fast mode.

######## 6. FlsMaxWriteNormalMode

- **UUID**: `ECUC:b03a7114-6d17-46c2-9f4b-2853f0e44291`
- **参数名**: `FlsMaxWriteNormalMode`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `32`
- **取值范围**: [32..32]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: The maximum number of bytes to write in one cycle of the flash driver's job processing function in normal mode.

######## 7. FlsProtection

- **UUID**: `ECUC:78d9a61d-5c1e-494b-95b2-09349577769b`
- **参数名**: `FlsProtection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Erase/write protection settings. Only relevant if supported by hardware.

####### FLOAT 类型参数

######## 1. FlsCallCycle

- **UUID**: `ECUC:cec56299-7876-4cfc-9811-10a8cdc9b035`
- **参数名**: `FlsCallCycle`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.01`
- **取值范围**: [1.0E-4..1.0]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Cycle time of calls of the flash driver's main function (in seconds).

####### ENUMERATION 类型参数

######## 1. FlsDefaultMode

- **UUID**: `ECUC:f72e69f0-f52b-4383-9077-224b9258cf31`
- **参数名**: `FlsDefaultMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `MEMIF_MODE_SLOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `MEMIF_MODE_FAST` (来源: AUTOSAR_ECUC)
  - `MEMIF_MODE_SLOW` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is the default FLS device mode after initialization.

######## 2. FlsWaitStateRead

- **UUID**: `3cca11e7-34f6-4608-8ec3-c68789b57dc6`
- **参数名**: `FlsWaitStateRead`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `FLS_17_DMU_WAIT_STATE_READACCESS9`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `FLS_17_DMU_WAIT_STATE_READACCESS0` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS1` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS2` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS3` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS4` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS5` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS6` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS7` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS8` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS9` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS10` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS11` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS12` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS13` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS14` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS15` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS16` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS17` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS18` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS19` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS20` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS21` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS22` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS23` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS24` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS25` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS26` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS27` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS28` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS29` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS30` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS31` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS32` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS33` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS34` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS35` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS36` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS37` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS38` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS39` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS40` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS41` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS42` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS43` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS44` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS45` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS46` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS47` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS48` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS49` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS50` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS51` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS52` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS53` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS54` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS55` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS56` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS57` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS58` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS59` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS60` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS61` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS62` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS63` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS64` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS65` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS66` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS67` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS68` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS69` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS70` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS71` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS72` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS73` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS74` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS75` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS76` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS77` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS78` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS79` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS80` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS81` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS82` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS83` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS84` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS85` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS86` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS87` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS88` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS89` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS90` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS91` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS92` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS93` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS94` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS95` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS96` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS97` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS98` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS99` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS100` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS101` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS102` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS103` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS104` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS105` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS106` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS107` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS108` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS109` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS110` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS111` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS112` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS113` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS114` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS115` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS116` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS117` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS118` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS119` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS120` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS121` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS122` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS123` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS124` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS125` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS126` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS127` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS128` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS129` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS130` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS131` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS132` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS133` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS134` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS135` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS136` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS137` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS138` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS139` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS140` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS141` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS142` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS143` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS144` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS145` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS146` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS147` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS148` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS149` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS150` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS151` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS152` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS153` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS154` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS155` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS156` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS157` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS158` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS159` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS160` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS161` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS162` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS163` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS164` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS165` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS166` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS167` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS168` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS169` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS170` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS171` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS172` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS173` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS174` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS175` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS176` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS177` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS178` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS179` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS180` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS181` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS182` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS183` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS184` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS185` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS186` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS187` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS188` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS189` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS190` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS191` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS192` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS193` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS194` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS195` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS196` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS197` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS198` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS199` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS200` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS201` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS202` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS203` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS204` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS205` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS206` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS207` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS208` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS209` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS210` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS211` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS212` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS213` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS214` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS215` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS216` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS217` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS218` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS219` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS220` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS221` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS222` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS223` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS224` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS225` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS226` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS227` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS228` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS229` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS230` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS231` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS232` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS233` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS234` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS235` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS236` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS237` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS238` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS239` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS240` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS241` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS242` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS243` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS244` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS245` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS246` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS247` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS248` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS249` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS250` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS251` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS252` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS253` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS254` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_READACCESS255` (来源: INFINEON_AURIX2G)
- **描述**: Defines Wait State Configuration for read access from DFLASH.

######## 3. FlsWaitStateErrorCorrection

- **UUID**: `c6a74b25-c548-4a6b-8a9a-6ee0f11926f5`
- **参数名**: `FlsWaitStateErrorCorrection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `FLS_17_DMU_WAIT_STATE_ERRORCORRECTION1`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `FLS_17_DMU_WAIT_STATE_ERRORCORRECTION0` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_ERRORCORRECTION1` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_ERRORCORRECTION2` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_ERRORCORRECTION3` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_ERRORCORRECTION4` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_ERRORCORRECTION5` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_ERRORCORRECTION6` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_WAIT_STATE_ERRORCORRECTION7` (来源: INFINEON_AURIX2G)
- **描述**: Defines Wait State Configuration for error correction

####### FUNCTION-NAME 类型参数

######## 1. FlsJobEndNotification

- **UUID**: `ECUC:01bf35d4-f65a-4e62-8fcb-bc18bb89b960`
- **参数名**: `FlsJobEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `Fee_JobEndNotification`
- **描述**: Mapped to the job end notification routine provided by some upper layer module, typically the Fee module.

######## 2. FlsJobErrorNotification

- **UUID**: `ECUC:da44a748-916b-4a62-a4cf-44f5fbb45d0c`
- **参数名**: `FlsJobErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `Fee_JobErrorNotification`
- **描述**: Mapped to the job error notification routine provided by some upper layer module, typically the Fee module.

######## 3. FlsEraseVerifyErrNotif

- **UUID**: `ECUC:01bf25d4-f65a-4e62-8fcb-bc18bb89b960`
- **参数名**: `FlsEraseVerifyErrNotif`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `Fee_17_JobEraseErrorNotification`
- **描述**: Mapped to the EVER notification routine provided by some upper layer module, typically the Fee module.

######## 4. FlsProgVerifyErrNotif

- **UUID**: `ECUC:01bf35d4-f65a-4e62-8fcb-bc28bb89b960`
- **参数名**: `FlsProgVerifyErrNotif`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `Fee_17_JobProgErrorNotification`
- **描述**: Mapped to the PVER notification routine provided by some upper layer module, typically the Fee module.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. FlsDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:fe9f0540-d42d-403b-800e-5698c8b8f894`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **5** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FLS_E_COMPARE_FAILED

- **UUID**: `ECUC:1afc7fa9-2d93-470a-a7e9-d183ba72fb34`
- **引用名**: `FLS_E_COMPARE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash compare failed (HW)" has occurred.

########## 2. FLS_E_ERASE_FAILED

- **UUID**: `ECUC:f339bf7e-b28f-4c49-a70b-75a714eace96`
- **引用名**: `FLS_E_ERASE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash erase failed (HW)" has occurred.

########## 3. FLS_E_READ_FAILED

- **UUID**: `ECUC:494d3058-fb65-44de-bed8-0231d2858800`
- **引用名**: `FLS_E_READ_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash read failed (HW)" has occurred.

########## 4. FLS_E_UNEXPECTED_FLASH_ID

- **UUID**: `ECUC:c32b2d32-9bdc-4b84-af48-c829dc459d97`
- **引用名**: `FLS_E_UNEXPECTED_FLASH_ID`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Expected hardware ID not matched" has occurred.

########## 5. FLS_E_WRITE_FAILED

- **UUID**: `ECUC:cfc28b37-3775-4e16-8d98-e05917d2ed66`
- **引用名**: `FLS_E_WRITE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash write failed (HW)" has occurred.

####### 2. FlsExternalDriver

**容器属性**:

- **UUID**: `ECUC:81c36c86-d308-47d4-bc55-a02b401446e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsExternalDriver`
- **多重性**: [0..1]

**容器描述**:

This container is present for external Flash drivers only. Internal Flash drivers do not use the parameter listed in this container, hence its multiplicity is 0 for internal drivers.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FlsSpiReference

- **UUID**: `ECUC:0124051e-19cb-4f30-8c5a-476d3847afb6`
- **引用名**: `FlsSpiReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to SPI sequence (required for external Flash drivers).

####### 3. FlsSectorList

**容器属性**:

- **UUID**: `ECUC:48a5cfc6-7ab9-44e4-a3eb-9e4eb901c845`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSectorList`
- **多重性**: [0..1]

**容器描述**:

List of flashable sectors and pages.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FlsSector

**容器属性**:

- **UUID**: `ECUC:4a46d887-b3be-41a3-aa7b-031bfa23ac7c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSector`
- **多重性**: [1..1]

**容器描述**:

Configuration description of a flashable sector

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. FlsNumberOfSectors

- **UUID**: `ECUC:182b2aa9-9cd0-4305-91a4-e9a69decf610`
- **参数名**: `FlsNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [1..2]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of continuous sectors with identical values for FlsSectorSize and

############ 2. FlsPageSize

- **UUID**: `ECUC:ad1fae4e-3ea1-4584-a148-c8669780a684`
- **参数名**: `FlsPageSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8`
- **取值范围**: [8..8]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of one page of this sector.

############ 3. FlsSectorSize

- **UUID**: `ECUC:3994527a-0bfb-4ec5-8864-374a51cade70`
- **参数名**: `FlsSectorSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `524288`
- **取值范围**: [4096..1048576]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of this sector.

############ 4. FlsSectorStartaddress

- **UUID**: `ECUC:61630dd0-0649-4365-ad45-d691f452ce17`
- **参数名**: `FlsSectorStartaddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..1048575]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Start address of this sector.

####### 4. FlsSector

**容器属性**:

- **UUID**: `ECUC:4a46d887-b3be-41a3-aa7b-031bfa23ac7c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSector`
- **多重性**: [1..1]

**容器描述**:

Configuration description of a flashable sector

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. FlsNumberOfSectors

- **UUID**: `ECUC:182b2aa9-9cd0-4305-91a4-e9a69decf610`
- **参数名**: `FlsNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [1..2]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of continuous sectors with identical values for FlsSectorSize and

########## 2. FlsPageSize

- **UUID**: `ECUC:ad1fae4e-3ea1-4584-a148-c8669780a684`
- **参数名**: `FlsPageSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8`
- **取值范围**: [8..8]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of one page of this sector.

########## 3. FlsSectorSize

- **UUID**: `ECUC:3994527a-0bfb-4ec5-8864-374a51cade70`
- **参数名**: `FlsSectorSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `524288`
- **取值范围**: [4096..1048576]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of this sector.

########## 4. FlsSectorStartaddress

- **UUID**: `ECUC:61630dd0-0649-4365-ad45-d691f452ce17`
- **参数名**: `FlsSectorStartaddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..1048575]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Start address of this sector.

##### 2. FlsDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:fe9f0540-d42d-403b-800e-5698c8b8f894`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **5** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FLS_E_COMPARE_FAILED

- **UUID**: `ECUC:1afc7fa9-2d93-470a-a7e9-d183ba72fb34`
- **引用名**: `FLS_E_COMPARE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash compare failed (HW)" has occurred.

######## 2. FLS_E_ERASE_FAILED

- **UUID**: `ECUC:f339bf7e-b28f-4c49-a70b-75a714eace96`
- **引用名**: `FLS_E_ERASE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash erase failed (HW)" has occurred.

######## 3. FLS_E_READ_FAILED

- **UUID**: `ECUC:494d3058-fb65-44de-bed8-0231d2858800`
- **引用名**: `FLS_E_READ_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash read failed (HW)" has occurred.

######## 4. FLS_E_UNEXPECTED_FLASH_ID

- **UUID**: `ECUC:c32b2d32-9bdc-4b84-af48-c829dc459d97`
- **引用名**: `FLS_E_UNEXPECTED_FLASH_ID`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Expected hardware ID not matched" has occurred.

######## 5. FLS_E_WRITE_FAILED

- **UUID**: `ECUC:cfc28b37-3775-4e16-8d98-e05917d2ed66`
- **引用名**: `FLS_E_WRITE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash write failed (HW)" has occurred.

##### 3. FlsExternalDriver

**容器属性**:

- **UUID**: `ECUC:81c36c86-d308-47d4-bc55-a02b401446e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsExternalDriver`
- **多重性**: [0..1]

**容器描述**:

This container is present for external Flash drivers only. Internal Flash drivers do not use the parameter listed in this container, hence its multiplicity is 0 for internal drivers.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FlsSpiReference

- **UUID**: `ECUC:0124051e-19cb-4f30-8c5a-476d3847afb6`
- **引用名**: `FlsSpiReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to SPI sequence (required for external Flash drivers).

##### 4. FlsSectorList

**容器属性**:

- **UUID**: `ECUC:48a5cfc6-7ab9-44e4-a3eb-9e4eb901c845`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSectorList`
- **多重性**: [0..1]

**容器描述**:

List of flashable sectors and pages.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FlsSector

**容器属性**:

- **UUID**: `ECUC:4a46d887-b3be-41a3-aa7b-031bfa23ac7c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSector`
- **多重性**: [1..1]

**容器描述**:

Configuration description of a flashable sector

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. FlsNumberOfSectors

- **UUID**: `ECUC:182b2aa9-9cd0-4305-91a4-e9a69decf610`
- **参数名**: `FlsNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [1..2]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of continuous sectors with identical values for FlsSectorSize and

########## 2. FlsPageSize

- **UUID**: `ECUC:ad1fae4e-3ea1-4584-a148-c8669780a684`
- **参数名**: `FlsPageSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8`
- **取值范围**: [8..8]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of one page of this sector.

########## 3. FlsSectorSize

- **UUID**: `ECUC:3994527a-0bfb-4ec5-8864-374a51cade70`
- **参数名**: `FlsSectorSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `524288`
- **取值范围**: [4096..1048576]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of this sector.

########## 4. FlsSectorStartaddress

- **UUID**: `ECUC:61630dd0-0649-4365-ad45-d691f452ce17`
- **参数名**: `FlsSectorStartaddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..1048575]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Start address of this sector.

##### 5. FlsSector

**容器属性**:

- **UUID**: `ECUC:4a46d887-b3be-41a3-aa7b-031bfa23ac7c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSector`
- **多重性**: [1..1]

**容器描述**:

Configuration description of a flashable sector

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. FlsNumberOfSectors

- **UUID**: `ECUC:182b2aa9-9cd0-4305-91a4-e9a69decf610`
- **参数名**: `FlsNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [1..2]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of continuous sectors with identical values for FlsSectorSize and

######## 2. FlsPageSize

- **UUID**: `ECUC:ad1fae4e-3ea1-4584-a148-c8669780a684`
- **参数名**: `FlsPageSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8`
- **取值范围**: [8..8]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of one page of this sector.

######## 3. FlsSectorSize

- **UUID**: `ECUC:3994527a-0bfb-4ec5-8864-374a51cade70`
- **参数名**: `FlsSectorSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `524288`
- **取值范围**: [4096..1048576]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of this sector.

######## 4. FlsSectorStartaddress

- **UUID**: `ECUC:61630dd0-0649-4365-ad45-d691f452ce17`
- **参数名**: `FlsSectorStartaddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..1048575]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Start address of this sector.

##### 6. FlsGeneral

**容器属性**:

- **UUID**: `ECUC:3091e295-abe7-43a0-98f4-e60da9dc4945`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsGeneral`
- **多重性**: [0..1]

**容器描述**:

Container for general parameters of the flash driver. These parameters are always pre-compile.

###### 参数配置

此容器包含 **19** 个参数：

####### INTEGER 类型参数

######## 1. FlsBaseAddress

- **UUID**: `ECUC:ea05556a-aa1f-4a79-8824-757f1614471c`
- **参数名**: `FlsBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2936012800`
- **取值范围**: [2936012800..2936012800]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The flash memory start address (see also SWS_Fls_00208 and SWS_Fls_00209).

######## 2. FlsDriverIndex

- **UUID**: `ECUC:24f7c0cd-07e7-40be-82f4-001abe599d00`
- **参数名**: `FlsDriverIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Index of the driver, used by FEE.

######## 3. FlsTotalSize

- **UUID**: `ECUC:a8cdc4a9-dcbe-4c4e-82e9-d76da4755fe2`
- **参数名**: `FlsTotalSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1048576`
- **取值范围**: [4096..1048576]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The total amount of flash memory in bytes (see also SWS_Fls_00208 and SWS_Fls_00209).

####### BOOLEAN 类型参数

######## 1. FlsAcLoadOnJobStart

- **UUID**: `ECUC:622bd1f2-a9e0-4043-9b1a-8baa38771911`
- **参数名**: `FlsAcLoadOnJobStart`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The flash driver shall load the flash access code to RAM whenever an erase or write job is started and unload (overwrite) it after that job has been finished or canceled.

######## 2. FlsBlankCheckApi

- **UUID**: `ECUC:42263743-7eb8-48f0-9feb-b4fd15246438`
- **参数名**: `FlsBlankCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Compile switch to enable/disable the Fls_BlankCheck function.

######## 3. FlsInitCheckApi

- **UUID**: `ECUC:4d3911ac-2593-4da7-a69e-66453109d78a`
- **参数名**: `FlsInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Adds / removes the service Fls_17_Dmu_InitCheck() from the code.                            true: Fls_17_Dmu_InitCheck() can be used.                            false: Fls_17_Dmu_InitCheck() can not be used.

######## 4. FlsCancelApi

- **UUID**: `ECUC:893eebfb-c839-4cbf-8310-bdb18b1a08e5`
- **参数名**: `FlsCancelApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Compile switch to enable and disable the Fls_Cancel function.

######## 5. FlsCompareApi

- **UUID**: `ECUC:b694dc7a-1a2c-45f5-84df-452bb9b75354`
- **参数名**: `FlsCompareApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Compile switch to enable and disable the Fls_Compare function.

######## 6. FlsDevErrorDetect

- **UUID**: `ECUC:6f390fca-9815-44eb-91ab-841f2b962337`
- **参数名**: `FlsDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 7. FlsRunTimeErrorDetect

- **UUID**: `ECUC:6f390fca-9815-44eb-91ab-841f2b062337`
- **参数名**: `FlsRunTimeErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the Runtime Error Tracer detection and notification ON or OFF.

######## 8. FlsSafetyEnable

- **UUID**: `be837339-bdd5-4cda-123w-74e2e11c110a`
- **参数名**: `FlsSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch to enable/disable the Safety Error.

######## 9. FlsIfxFeeUse

- **UUID**: `ECUC:6f390fca-9815-44eb-91ab-841f3b962337`
- **参数名**: `FlsIfxFeeUse`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables/Disables the use of IFX FEE functions.

######## 10. FlsGetJobResultApi

- **UUID**: `ECUC:760f215b-bb6c-4810-950c-be3df14fa844`
- **参数名**: `FlsGetJobResultApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Compile switch to enable and disable the Fls_GetJobResult function.

######## 11. FlsGetStatusApi

- **UUID**: `ECUC:e5af54cf-a0b9-49e0-87a3-044cafdfe2c1`
- **参数名**: `FlsGetStatusApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Compile switch to enable and disable the Fls_GetStatus function.

######## 12. FlsSetModeApi

- **UUID**: `ECUC:b5756f12-6f52-4348-9416-7cf894e79a8d`
- **参数名**: `FlsSetModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Compile switch to enable and disable the Fls_SetMode function.

######## 13. FlsUseInterrupts

- **UUID**: `ECUC:88a2d255-2439-43a9-888a-c21a750ac380`
- **参数名**: `FlsUseInterrupts`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Job processing triggered by hardware interrupt.

######## 14. FlsVersionInfoApi

- **UUID**: `ECUC:b18ae536-69a0-4336-a3ca-9d170d7b33d9`
- **参数名**: `FlsVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

####### ENUMERATION 类型参数

######## 1. FlsInitApiMode

- **UUID**: `bd0a8d38-4d8c-4eab-cdfe-1166b2583107`
- **参数名**: `FlsInitApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `FLS_17_DMU_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `FLS_17_DMU_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the operating modes for FlexRay initialization

######## 2. FlsRuntimeApiMode

- **UUID**: `bd0a8d38-4d7c-4eab-cdfe-1166b2583107`
- **参数名**: `FlsRuntimeApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `FLS_17_DMU_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `FLS_17_DMU_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `FLS_17_DMU_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the operating modes for FlexRay initialization

##### 7. FlsPublishedInformation

**容器属性**:

- **UUID**: `ECUC:8e0d2c5d-45de-462e-ba90-f372ccf8e6de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Additional published parameters not covered by CommonPublishedInformation container.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. FlsAcLocationErase

- **UUID**: `ECUC:2ed61e35-84bc-47f4-9c77-22b984edd9ba`
- **参数名**: `FlsAcLocationErase`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Position in RAM, to which the erase flash access code has to be loaded.

######## 2. FlsAcLocationWrite

- **UUID**: `ECUC:a5573b35-3446-4cb4-8396-4c7db3aa207a`
- **参数名**: `FlsAcLocationWrite`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Position in RAM, to which the write flash access code has to be loaded.

######## 3. FlsAcSizeErase

- **UUID**: `ECUC:b60ed9c5-bf85-4cb5-84ed-a9de40ed10a6`
- **参数名**: `FlsAcSizeErase`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of bytes in RAM needed for the erase flash access code.

######## 4. FlsAcSizeWrite

- **UUID**: `ECUC:06a20d0b-9d96-42d3-96e2-e2eb5171101f`
- **参数名**: `FlsAcSizeWrite`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of bytes in RAM needed for the write flash access code.

######## 5. FlsErasedValue

- **UUID**: `ECUC:4b2ea1ec-cdcb-4ba5-b243-4ec4a94fe866`
- **参数名**: `FlsErasedValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The contents of an erased flash memory cell.

######## 6. FlsSpecifiedEraseCycles

- **UUID**: `ECUC:0fed8a26-c89e-4a57-9a52-08d5e936bc27`
- **参数名**: `FlsSpecifiedEraseCycles`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `125000`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of erase cycles specified for the flash device (usually given in the device data sheet).

####### FLOAT 类型参数

######## 1. FlsEraseTime

- **UUID**: `ECUC:9854b5e9-7313-45e6-b78e-52fa98bd13d8`
- **参数名**: `FlsEraseTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1500000`
- **取值范围**: [0.0..4.294967295E9]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum time to erase one complete flash sector.

######## 2. FlsWriteTime

- **UUID**: `ECUC:61ce65fd-81a1-4a8e-93b4-9ab14d046848`
- **参数名**: `FlsWriteTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `140`
- **取值范围**: [0.0..4.294967295E9]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum time to program one complete flash page.

####### STRING 类型参数

######## 1. FlsExpectedHwId

- **UUID**: `ECUC:b75b0b3e-e68a-4a74-984c-875387d3aa04`
- **参数名**: `FlsExpectedHwId`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `0`
- **描述**: Unique identifier of the hardware device that is expected by this driver (the device for which this driver has been implemented).

##### 8. FlsIfxSpecificConfig

**容器属性**:

- **UUID**: `DCE:452efcdb-ab65-6f92-b846-7a8ffd2c16e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsIfxSpecificConfig`
- **多重性**: [0..1]

**容器描述**:

This container is used to provide the Ifx specific parameters.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. FlsEraseSuspendTimeout

- **UUID**: `2380135d-6778-417a-a35c-e10017d4dd54`
- **参数名**: `FlsEraseSuspendTimeout`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `12000`
- **取值范围**: [12000..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Timeout for Erase Suspend feature(loop count).

####### BOOLEAN 类型参数

######## 1. FlsUseEraseSuspend

- **UUID**: `9bf20cc6-90c5-428e-ae45-8983baa7d7a2`
- **参数名**: `FlsUseEraseSuspend`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Compile switch to enable or disable the FLS erase suspend and erase resume feature

####### STRING 类型参数

######## 1. FlsStateVarStruct

- **UUID**: `c4f7ac5f-7114-4bc8-94cd-b142365dfee8`
- **参数名**: `FlsStateVarStruct`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `FlsStateVar`
- **描述**: This parameter is used to provide the name of the structure containing the entire global variables specific to the Flash driver.

####### FUNCTION-NAME 类型参数

######## 1. FlsIllegalStateNotification

- **UUID**: `6a28daf7-b174-4e5c-a3fd-e10e22a84bcf`
- **参数名**: `FlsIllegalStateNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a pointer to a notification function, which is called when FLS reaches an Illegal state. Illegal state here means that FLS is not able to proceed. No more FLS request shall be triggered; Reset of the system is recommended.

##### 9. CommonPublishedInformation

**容器属性**:

- **UUID**: `492f8482-3e2c-4bf1-b27f-01fd7ac35788`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CommonPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Common container, aggregated by all modules. It contains published information about vendor and versions.

###### 参数配置

此容器包含 **10** 个参数：

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
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 7. ModuleId

- **UUID**: `3b407478-6902-4f80-b7cf-f33b0854e638`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `92`
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

######## 1. VendorApiInfix

- **UUID**: `ad363b41-e945-4717-b12f-c2bc00ef138e`
- **参数名**: `VendorApiInfix`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `Dmu`
- **描述**: In driver modules which can be instantiated several times on a single ECU, BSW00347 requires that the name of APIs is extended by the VendorId and a vendor specific name. 
                  This parameter is used to specify the vendor specific name. In total, the implementation specific name is generated as follows:
                  <ModuleName>_>VendorId>_<VendorApiInfix><Api name from SWS>

######## 2. Release

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

1. **Fls**
