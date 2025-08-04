# Dem - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:41

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Dem](#dem)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Dem

#### 基本信息

- **UUID**: `ECUC:a72ca44c-5093-4cd1-b6f1-e197d31fdd75`
- **模块名称**: `Dem`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Dem (Diagnostic Event Manager) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.4.0

- **发布日期**: 2013-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **59** 个配置容器：

##### 1. DemConfigSet

**容器属性**:

- **UUID**: `ECUC:e85440ff-d0a6-4001-bcfc-aa36b340c94a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration parameters and sub containers of the Dem module supporting multiple configuration sets. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 配置容器

本模块包含 **18** 个配置容器：

####### 1. DemDTCClass

**容器属性**:

- **UUID**: `ECUC:10f37378-2b66-4089-aec4-382cb9316830`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDTCClass`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for DTCClass.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. DemDTCFunctionalUnit

- **UUID**: `ECUC:467cf2b5-284e-4cd6-9004-831fb0599388`
- **参数名**: `DemDTCFunctionalUnit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: DTCFuncitonalUnit is a 1-byte value which identifies the corresponding basic vehicle / system function which reports the DTC. This parameter is necessary for the report of severity information.

########## 2. DemJ1939DTC

- **UUID**: `ECUC:d62b52a5-97bd-4f04-a64d-e88dda34eb15`
- **参数名**: `DemJ1939DTC`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..16777214]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique Diagnostic Trouble Code value for J1939 (consiting of SPN and FMI)

########## 3. DemObdDTC

- **UUID**: `ECUC:e979a29e-4aef-405e-aee7-2dc1c41b6c04`
- **参数名**: `DemObdDTC`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique Diagnostic Trouble Code value for OBD

########## 4. DemUdsDTC

- **UUID**: `ECUC:c1fc7bad-0617-4667-8f03-ef4094b29060`
- **参数名**: `DemUdsDTC`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..16777214]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique Diagnostic Trouble Code value for UDS

######### BOOLEAN 类型参数

########## 1. DemImmediateNvStorage

- **UUID**: `ECUC:09b420be-542a-4655-beaa-bc967dfcd3e8`
- **参数名**: `DemImmediateNvStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to enable immediate storage triggering of an according event memory entriy persistently to NVRAM.

######### ENUMERATION 类型参数

########## 1. DemDTCSeverity

- **UUID**: `ECUC:ec5f19c2-2f59-4a05-a5a7-21fc4e8b49e3`
- **参数名**: `DemDTCSeverity`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DEM_DTC_SEV_NO_SEVERITY`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTC_SEV_CHECK_AT_NEXT_HALT` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_SEV_IMMEDIATELY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_SEV_MAINTENANCE_ONLY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_SEV_NO_SEVERITY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: DTC severity according to ISO 14229-1. This parameter depends on the automotive manufacturer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DemJ1939DTC_NodeAddressRef

- **UUID**: `ECUC:399fa3b9-2fc9-44ab-a7b2-25b1a2c7f40b`
- **引用名**: `DemJ1939DTC_NodeAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemJ1939NodeAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemJ1939NodeAddress`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a J1939 NodeAddress

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DemCallbackInitMForF

**容器属性**:

- **UUID**: `ECUC:d73df317-2911-4d4c-8d81-466df02d7e55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackInitMForF`
- **多重性**: [0..infinite]
- **多配置容器**: false

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackInitMForFFnc

- **UUID**: `ECUC:2415de0a-e9e7-45e0-b2fd-c955bc96b0ea`
- **参数名**: `DemCallbackInitMForFFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "InitMonitorForFunction".

####### 2. DemCallbackInitMForF

**容器属性**:

- **UUID**: `ECUC:d73df317-2911-4d4c-8d81-466df02d7e55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackInitMForF`
- **多重性**: [0..infinite]
- **多配置容器**: false

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackInitMForFFnc

- **UUID**: `ECUC:2415de0a-e9e7-45e0-b2fd-c955bc96b0ea`
- **参数名**: `DemCallbackInitMForFFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "InitMonitorForFunction".

####### 3. DemDtr

**容器属性**:

- **UUID**: `ECUC:048c7ac5-d3b3-4277-91af-bbdb75a2bd3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDtr`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container holds the configuration of one individual DTR.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. DemDtrId

- **UUID**: `ECUC:9c14e03c-5be7-4392-b637-ad7293e74d5f`
- **参数名**: `DemDtrId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The index identifier value assigned to this DTR. The value is generated during the Dem configuration process.

########## 2. DemDtrMid

- **UUID**: `ECUC:2cb52e21-b358-4631-82d4-ec342e69d3b8`
- **参数名**: `DemDtrMid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The OBDMID of the DTR.

########## 3. DemDtrTid

- **UUID**: `ECUC:4da5ac1a-81b6-454e-9da7-222ef76ea52d`
- **参数名**: `DemDtrTid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The OBDTID of the DTR.

########## 4. DemDtrUasid

- **UUID**: `ECUC:b29dfc82-e531-4ccd-a648-97a890536902`
- **参数名**: `DemDtrUasid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The UaSId the DTR data shall be scaled to, and reported together with the rescaled DTR data.

######### FLOAT 类型参数

########## 1. DemDtrCompuDenominator0

- **UUID**: `ECUC:5c85b81d-2f61-4fbd-b25f-e128ee47865a`
- **参数名**: `DemDtrCompuDenominator0`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Part of the conversion between the binary representation and the physical meaning analogous to the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1 denominator coefficient in the direction compuInternalToPhys.

########## 2. DemDtrCompuNumerator0

- **UUID**: `ECUC:2a37b812-08e6-4de4-8ebb-4268f02b47a3`
- **参数名**: `DemDtrCompuNumerator0`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Part of the conversion between the binary representation and the physical meaning analogous to the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1 denominator coefficient in the direction compuInternalToPhys.

########## 3. DemDtrCompuNumerator1

- **UUID**: `ECUC:ac631547-516f-4d48-8a71-1fe3c0d49638`
- **参数名**: `DemDtrCompuNumerator1`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Part of the conversion between the binary representation and the physical meaning analogous to the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1 denominator coefficient in the direction compuInternalToPhys.

######### ENUMERATION 类型参数

########## 1. DemDtrUpdateKind

- **UUID**: `ECUC:f58baecb-daa8-449b-b8b7-ddbe112c024d`
- **参数名**: `DemDtrUpdateKind`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTR_UPDATE_ALWAYS` (来源: AUTOSAR_ECUC)
  - `DEM_DTR_UPDATE_STEADY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Update conditions applied by the Dem to reports of DTR values. Only supported if a related Event is configured. If no related Event is configured, the Dem behaves as if DemDtrUpdateKind is configured to "DEM_DTR_UPDATE_ALWAYS".

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DemDtrEventRef

- **UUID**: `ECUC:b5eb778a-d83b-4f33-9432-a212ca1caa0c`
- **引用名**: `DemDtrEventRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter this DTR is related to. If the related event is not configured, the Dem cannot ensure consistency between the DTR and the event.

####### 4. DemEventParameter

**容器属性**:

- **UUID**: `ECUC:17edd206-934c-420b-a50a-75aef6269ac7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemEventParameter`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for events.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DemEventId

- **UUID**: `ECUC:a42e4864-6ec3-4459-ae25-2a314d4a0e42`
- **参数名**: `DemEventId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier of a diagnostic event.

########## 2. DemMaxNumberFreezeFrameRecords

- **UUID**: `ECUC:0c06d2a8-5789-4416-8c13-f331b2f5d081`
- **参数名**: `DemMaxNumberFreezeFrameRecords`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of according freeze frame records, which can maximal be stored for this event. Therefore all these freeze frame records have the same freeze frame class.

######### BOOLEAN 类型参数

########## 1. DemEventAvailable

- **UUID**: `ECUC:6b0b03bd-1d0c-47c8-b723-0bca376ea53a`
- **参数名**: `DemEventAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures an Event as unavailable.

######### ENUMERATION 类型参数

########## 1. DemEventKind

- **UUID**: `ECUC:44e8a61c-a95b-487d-908b-0ca87be434d4`
- **参数名**: `DemEventKind`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_EVENT_KIND_BSW` (来源: AUTOSAR_ECUC)
  - `DEM_EVENT_KIND_SWC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to distinguish between SW-C and BSW events. SW-C events are reported by Dem_SetEventStatus API and BSW events are reported by Dem_ReportErrorStatus API.

######## 引用关系

此容器包含 **7** 个引用：

######### REFERENCE 类型引用

########## 1. DemDTCClassRef

- **UUID**: `ECUC:89db0687-72d2-47f9-9e6a-6bcf25fde654`
- **引用名**: `DemDTCClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemDTCClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemDTCClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the DTC configuration associated with the diagnostic event.

########## 2. DemExtendedDataClassRef

- **UUID**: `ECUC:aad40479-8bd6-451a-86f6-d42e15b8bd26`
- **引用名**: `DemExtendedDataClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemExtendedDataClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemExtendedDataClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference defines the link to an extended data class sampler.

########## 3. DemFreezeFrameClassRef

- **UUID**: `ECUC:b980679e-9569-4f3b-8558-841069092eb2`
- **引用名**: `DemFreezeFrameClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemFreezeFrameClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemFreezeFrameClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: These references define the links to a freeze frame class sampler.

########## 4. DemFreezeFrameRecNumClassRef

- **UUID**: `ECUC:37ada416-5e4f-4e2d-82f8-f8f010feb2f4`
- **引用名**: `DemFreezeFrameRecNumClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemFreezeFrameRecNumClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemFreezeFrameRecNumClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the list of dedicated freeze frame record numbers associated with the diagnostic event. These record numbers are assigned to the freeze frame records (instead of calculated record numbers).

########## 5. DemJ1939ExpandedFreezeFrameClassRef

- **UUID**: `ECUC:f9add2f1-9447-4a3b-a021-8152d0c37857`
- **引用名**: `DemJ1939ExpandedFreezeFrameClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemJ1939FreezeFrameClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemGeneralJ1939/DemJ1939FreezeFrameClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: These references define the links to a J1939 freeze frame class sampler.

########## 6. DemJ1939FreezeFrameClassRef

- **UUID**: `ECUC:66c9848c-d60b-4263-80dd-d247536f8d13`
- **引用名**: `DemJ1939FreezeFrameClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemJ1939FreezeFrameClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemGeneralJ1939/DemJ1939FreezeFrameClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: These references define the links to a J1939 freeze frame class sampler.

########## 7. DemOBDGroupingAssociativeEventsRef

- **UUID**: `ECUC:e6a5765e-f9e2-43d8-9b3e-23b46ec06e7a`
- **引用名**: `DemOBDGroupingAssociativeEventsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a reference which points to a representative event of one group of associate events.

######## 配置容器

本模块包含 **11** 个配置容器：

######### 1. DemCallbackClearEventAllowed

**容器属性**:

- **UUID**: `ECUC:81830ba7-c118-43dd-baf9-d89bcec71b90`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackClearEventAllowed`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates that the Dem has access to a "ClearEventAllowed" callback.

########## 参数配置

此容器包含 **2** 个参数：

########### ENUMERATION 类型参数

############ 1. DemClearEventAllowedBehavior

- **UUID**: `ECUC:7411934a-7525-44dd-b02b-e0681e08b4c2`
- **参数名**: `DemClearEventAllowedBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DEM_NO_STATUS_BYTE_CHANGE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_NO_STATUS_BYTE_CHANGE` (来源: AUTOSAR_ECUC)
  - `DEM_ONLY_THIS_CYCLE_AND_READINESS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the resulting UDS status byte for the related event, which must not be cleared according to the ClearEventAllowed callback.

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackClearEventAllowedFnc

- **UUID**: `ECUC:f57a2f55-06b0-438d-9a41-d2626089d446`
- **参数名**: `DemCallbackClearEventAllowedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "ClearEventAllowed".

######### 2. DemCallbackEventDataChanged

**容器属性**:

- **UUID**: `ECUC:48673ef9-0ee2-44e2-a4da-c56610dd6792`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackEventDataChanged`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates that the Dem has access to an "EventDataChanged" callback.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackEventDataChangedFnc

- **UUID**: `ECUC:620931a3-319d-4e30-8896-df7694afa222`
- **参数名**: `DemCallbackEventDataChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "EventDataChanged"

######### 3. DemCallbackEventStatusChanged

**容器属性**:

- **UUID**: `ECUC:505d125c-04db-4d5e-92f4-d73e664f7174`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackEventStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to an "EventStatusChanged" callback, which the Dem will call to notify other components about the change in the status of an event.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackEventStatusChangedFnc

- **UUID**: `ECUC:0a1de324-a6d1-4b23-ba12-631c41dbd8cc`
- **参数名**: `DemCallbackEventStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "EventStatusChanged"

######### 4. DemCallbackInitMForE

**容器属性**:

- **UUID**: `ECUC:11b1adbe-fd9a-49a2-a43e-01bed9346c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackInitMForE`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to an "InitMonitorForEvent" callback, which the Dem will call to initialize a monitor.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackInitMForEFnc

- **UUID**: `ECUC:46ba0efd-c45e-4400-a6f9-0441ffe9df5b`
- **参数名**: `DemCallbackInitMForEFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "InitMonitorForEvent".

######### 5. DemEventClass

**容器属性**:

- **UUID**: `ECUC:5127af6d-f63f-46f2-9279-2ddfa6850162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemEventClass`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for EventClass

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. DemAgingCycleCounterThreshold

- **UUID**: `ECUC:c005de82-ee68-46ba-8069-ed248a20b11b`
- **参数名**: `DemAgingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of aging cycles needed to unlearn/delete the event.

############ 2. DemEventFailureCycleCounterThreshold

- **UUID**: `ECUC:6506cb9d-36d0-4f67-89f7-266b9f4cbc3a`
- **参数名**: `DemEventFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the event based fault confirmation.

############ 3. DemEventMemoryEntryFdcThresholdStorageValue

- **UUID**: `ECUC:8dd83213-1223-4eff-ac82-a316ef9d215d`
- **参数名**: `DemEventMemoryEntryFdcThresholdStorageValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold to allocate an event memory entry and to capture the Freeze Frame.

############ 4. DemEventPriority

- **UUID**: `ECUC:3ef7c809-cd40-4824-b0cd-da79a594c75d`
- **参数名**: `DemEventPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of the event, in view of full event buffer.

########### BOOLEAN 类型参数

############ 1. DemAgingAllowed

- **UUID**: `ECUC:13bf7d23-8cc0-4b57-8911-92658b0cb328`
- **参数名**: `DemAgingAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to allow aging/unlearning of the event or not.

############ 2. DemConsiderPtoStatus

- **UUID**: `ECUC:ade2dfbd-edda-4dba-82cf-889cca141ba3`
- **参数名**: `DemConsiderPtoStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is TRUE, when the event is affected by the Dem PTO handling.

############ 3. DemFFPrestorageSupported

- **UUID**: `ECUC:998abc59-21d6-4f48-98d2-f84c83c31b9e`
- **参数名**: `DemFFPrestorageSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter is set to true, then the Prestorage of FreezeFrames is supported by the assigned event. This parameter is useful to calculate the buffer size.

########### ENUMERATION 类型参数

############ 1. DemEventDestination

- **UUID**: `ECUC:3d77d2e5-cd5d-463c-a083-aca98fec267d`
- **参数名**: `DemEventDestination`
- **数据类型**: ENUMERATION
- **多重性**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTC_ORIGIN_MIRROR_MEMORY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_ORIGIN_PRIMARY_MEMORY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_ORIGIN_SECONDARY_MEMORY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The event destination assigns events to none, one or multiple origins.

############ 2. DemEventOBDReadinessGroup

- **UUID**: `ECUC:bd389f92-bcb8-4921-acc3-d96cb78371b6`
- **参数名**: `DemEventOBDReadinessGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_OBD_RDY_AC` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_BOOSTPR` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_CAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_CMPRCMPT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_EGSENS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_ERG` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_EVAP` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_FLSYS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_FLSYS_NONCONT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_HCCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_HTCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_MISF` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_NONE` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_NOXCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_O2SENS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_O2SENSHT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_PMFLT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_SECAIR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the Event OBD Readiness group for PID $01 and PID $41 computation.

############ 3. DemEventSignificance

- **UUID**: `ECUC:73be02e4-de26-4bf9-87d8-8f6d3b15f532`
- **参数名**: `DemEventSignificance`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_EVENT_SIGNIFICANCE_FAULT` (来源: AUTOSAR_ECUC)
  - `DEM_EVENT_SIGNIFICANCE_OCCURRENCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Significance of the event, which indicates additional information concerning fault classification and resolution.

########## 引用关系

此容器包含 **5** 个引用：

########### REFERENCE 类型引用

############ 1. DemEnableConditionGroupRef

- **UUID**: `ECUC:6953a02d-6999-4d84-8c1d-daede62dfc77`
- **引用名**: `DemEnableConditionGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEnableConditionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemEnableConditionGroup`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References an enable condition group.

############ 2. DemEventFailureCycleRef

- **UUID**: `ECUC:2f31cb98-c767-407b-82e7-fe6fcdf86076`
- **引用名**: `DemEventFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the event based fault confirmation.

############ 3. DemOperationCycleRef

- **UUID**: `ECUC:fc68bc01-d147-4b6d-95a2-36cfa577cacf`
- **引用名**: `DemOperationCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of operation cycle for the event (e.g. power cycle, driving cycle, ...)

############ 4. DemStorageConditionGroupRef

- **UUID**: `ECUC:92052d72-8af4-4f08-9d1f-2a901238caf9`
- **引用名**: `DemStorageConditionGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemStorageConditionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemStorageConditionGroup`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References a storage condition group.

########### CHOICE-REFERENCE 类型引用

############ 1. DemAgingCycleRef

- **UUID**: `ECUC:2c17db4a-8035-4b38-bca3-093e53f7d34d`
- **引用名**: `DemAgingCycleRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC V1.0.0
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemAgingCycle`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the cycle which is triggering the aging of the event. This can either be the same as the operation cycle of the event, or a separate aging cycle reported via API Dem_SetAgingCycleState. If external aging is configured (refer to DemAgingCycleCounterProcessing), this parameter is not used.

########## 配置容器

本模块包含 **6** 个配置容器：

########### 1. DemDebounceCounterBased

**容器属性**:

- **UUID**: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceCounterBased`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for counter based debouncing.

############ 参数配置

此容器包含 **10** 个参数：

############# INTEGER 类型参数

############## 1. DemDebounceCounterDecrementStepSize

- **UUID**: `ECUC:07c58e53-a31c-421d-a6eb-910f2d3cd2d8`
- **参数名**: `DemDebounceCounterDecrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32768]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for decrementation of the internal debounce counter (PREPASSED).

############## 2. DemDebounceCounterFailedThreshold

- **UUID**: `ECUC:aff278be-3537-4099-8858-212582caf8f2`
- **参数名**: `DemDebounceCounterFailedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the failed status.

############## 3. DemDebounceCounterIncrementStepSize

- **UUID**: `ECUC:7cde5c15-c87f-4eed-b0f5-38313a32efe2`
- **参数名**: `DemDebounceCounterIncrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for incrementation of the internal debounce counter (PREFAILED).

############## 4. DemDebounceCounterJumpDownValue

- **UUID**: `ECUC:7baa87e8-87d0-45bb-9937-a8c3a4ebc2b6`
- **参数名**: `DemDebounceCounterJumpDownValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Down value of the internal debounce counter which is taken as initialization value for the counter when the respective step-down occurs.

############## 5. DemDebounceCounterJumpUpValue

- **UUID**: `ECUC:86693810-0a0a-4927-91ae-5d3723761724`
- **参数名**: `DemDebounceCounterJumpUpValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Up value of the internal debounce counter which is taken as initialization value for the counter when the respective step-up occurs.

############## 6. DemDebounceCounterPassedThreshold

- **UUID**: `ECUC:2c4aba4f-9fc9-4572-a226-9562516ffac3`
- **参数名**: `DemDebounceCounterPassedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..-1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the passed status.

############# BOOLEAN 类型参数

############## 1. DemDebounceCounterJumpDown

- **UUID**: `ECUC:aa2d713a-ec74-4c4c-93a9-bd83b0c107b8`
- **参数名**: `DemDebounceCounterJumpDown`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Down.

############## 2. DemDebounceCounterJumpUp

- **UUID**: `ECUC:6f82b9d4-c3e1-4f00-8196-1f85c7be1562`
- **参数名**: `DemDebounceCounterJumpUp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Up.

############## 3. DemDebounceCounterStorage

- **UUID**: `ECUC:33babe76-7e6b-44dc-8233-e33933cf87e7`
- **参数名**: `DemDebounceCounterStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to store the debounce counter value non-volatile or not.

############# ENUMERATION 类型参数

############## 1. DemDebounceBehavior

- **UUID**: `ECUC:6fd7cbcb-976b-46c5-bd9c-2ac97686f52d`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will behave, if a related enable condition is not fulfilled or ControlDTCSetting of the related event is disabled.

########### 2. DemDebounceMonitorInternal

**容器属性**:

- **UUID**: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceMonitorInternal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for monitor internal debouncing.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

############## 参数配置

此容器包含 **1** 个参数：

############### FUNCTION-NAME 类型参数

################ 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

########### 3. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

############ 参数配置

此容器包含 **1** 个参数：

############# FUNCTION-NAME 类型参数

############## 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

########### 4. DemDebounceTimeBase

**容器属性**:

- **UUID**: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceTimeBase`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for time based debouncing.

############ 参数配置

此容器包含 **3** 个参数：

############# FLOAT 类型参数

############## 1. DemDebounceTimeFailedThreshold

- **UUID**: `ECUC:4579dd3e-fa1d-404c-a743-9b236697409b`
- **参数名**: `DemDebounceTimeFailedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Failed" qualification.

############## 2. DemDebounceTimePassedThreshold

- **UUID**: `ECUC:e3952bac-0313-43a6-ac7c-19204e3a2662`
- **参数名**: `DemDebounceTimePassedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Passed" qualification.

############# ENUMERATION 类型参数

############## 1. DemDebounceBehavior

- **UUID**: `ECUC:79236e41-97f0-418c-b2f2-241d6595589b`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will

########### 5. DemIndicatorAttribute

**容器属性**:

- **UUID**: `ECUC:38466ee0-81d6-4eb5-84ea-278631d94b99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemIndicatorAttribute`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the event specific configuration of Indicators.

############ 参数配置

此容器包含 **4** 个参数：

############# INTEGER 类型参数

############## 1. DemIndicatorFailureCycleCounterThreshold

- **UUID**: `ECUC:bc2a7554-29fe-4a08-a8a8-57087833e55c`
- **参数名**: `DemIndicatorFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the WarningIndicatorOnCriteria.

############## 2. DemIndicatorHealingCycleCounterThreshold

- **UUID**: `ECUC:4248526d-57f1-4519-bb2d-400a541280f5`
- **参数名**: `DemIndicatorHealingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of healing cycles for the WarningIndicatorOffCriteria.

############# ENUMERATION 类型参数

############## 1. DemIndicatorBehaviour

- **UUID**: `ECUC:26582faa-e852-45d6-a68d-cf0cc279ca26`
- **参数名**: `DemIndicatorBehaviour`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_INDICATOR_BLINKING` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_BLINK_CONT` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_FAST_FLASH` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_SLOW_FLASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Behaviour of the linked indicator

############## 2. DemIndicatorFailureCycleSource

- **UUID**: `ECUC:9224f6ca-d10a-4b8d-9b76-da543ec42a3a`
- **参数名**: `DemIndicatorFailureCycleSource`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_FAILURE_CYCLE_EVENT` (来源: AUTOSAR_ECUC)
  - `DEM_FAILURE_CYCLE_INDICATOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, which failure cycle is used for the WarningIndicatorOnCriteria handling.

############ 引用关系

此容器包含 **3** 个引用：

############# REFERENCE 类型引用

############## 1. DemIndicatorFailureCycleRef

- **UUID**: `ECUC:3fc5415b-ef0e-4616-84af-ac48fb00b4e7`
- **引用名**: `DemIndicatorFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the indicator controlled by the according event used for the WarningIndicatorOnCriteria.

############## 2. DemIndicatorHealingCycleRef

- **UUID**: `ECUC:01818b0e-d069-473b-bb27-f067edb1f453`
- **引用名**: `DemIndicatorHealingCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of healing cycle for the indicator controlled by the according event used for the WarningIndicatorOffCriteria.

############## 3. DemIndicatorRef

- **UUID**: `ECUC:328aa173-bf87-415a-a94c-8b48686226a6`
- **引用名**: `DemIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used indicator.

########### 6. DemDebounceAlgorithmClass

**容器属性**:

- **UUID**: `ECUC:98a5d79e-8975-48e4-bbc8-a174596e2dbb`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDebounceAlgorithmClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDebounceCounterBased**
  - UUID: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
  - 描述: This container contains the configuration (parameters) for counter based debouncing.
- **DemDebounceMonitorInternal**
  - UUID: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
  - 描述: This container contains the configuration (parameters) for monitor internal debouncing.
- **DemCallbackGetFDC**
  - UUID: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
  - 描述: The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.
- **DemDebounceTimeBase**
  - UUID: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
  - 描述: This container contains the configuration (parameters) for time based debouncing.

**容器描述**:

Debounce algorithm class: counter based, time based, or monitor internal.

######### 6. DemDebounceCounterBased

**容器属性**:

- **UUID**: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceCounterBased`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for counter based debouncing.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. DemDebounceCounterDecrementStepSize

- **UUID**: `ECUC:07c58e53-a31c-421d-a6eb-910f2d3cd2d8`
- **参数名**: `DemDebounceCounterDecrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32768]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for decrementation of the internal debounce counter (PREPASSED).

############ 2. DemDebounceCounterFailedThreshold

- **UUID**: `ECUC:aff278be-3537-4099-8858-212582caf8f2`
- **参数名**: `DemDebounceCounterFailedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the failed status.

############ 3. DemDebounceCounterIncrementStepSize

- **UUID**: `ECUC:7cde5c15-c87f-4eed-b0f5-38313a32efe2`
- **参数名**: `DemDebounceCounterIncrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for incrementation of the internal debounce counter (PREFAILED).

############ 4. DemDebounceCounterJumpDownValue

- **UUID**: `ECUC:7baa87e8-87d0-45bb-9937-a8c3a4ebc2b6`
- **参数名**: `DemDebounceCounterJumpDownValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Down value of the internal debounce counter which is taken as initialization value for the counter when the respective step-down occurs.

############ 5. DemDebounceCounterJumpUpValue

- **UUID**: `ECUC:86693810-0a0a-4927-91ae-5d3723761724`
- **参数名**: `DemDebounceCounterJumpUpValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Up value of the internal debounce counter which is taken as initialization value for the counter when the respective step-up occurs.

############ 6. DemDebounceCounterPassedThreshold

- **UUID**: `ECUC:2c4aba4f-9fc9-4572-a226-9562516ffac3`
- **参数名**: `DemDebounceCounterPassedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..-1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the passed status.

########### BOOLEAN 类型参数

############ 1. DemDebounceCounterJumpDown

- **UUID**: `ECUC:aa2d713a-ec74-4c4c-93a9-bd83b0c107b8`
- **参数名**: `DemDebounceCounterJumpDown`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Down.

############ 2. DemDebounceCounterJumpUp

- **UUID**: `ECUC:6f82b9d4-c3e1-4f00-8196-1f85c7be1562`
- **参数名**: `DemDebounceCounterJumpUp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Up.

############ 3. DemDebounceCounterStorage

- **UUID**: `ECUC:33babe76-7e6b-44dc-8233-e33933cf87e7`
- **参数名**: `DemDebounceCounterStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to store the debounce counter value non-volatile or not.

########### ENUMERATION 类型参数

############ 1. DemDebounceBehavior

- **UUID**: `ECUC:6fd7cbcb-976b-46c5-bd9c-2ac97686f52d`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will behave, if a related enable condition is not fulfilled or ControlDTCSetting of the related event is disabled.

######### 7. DemDebounceMonitorInternal

**容器属性**:

- **UUID**: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceMonitorInternal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for monitor internal debouncing.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

############ 参数配置

此容器包含 **1** 个参数：

############# FUNCTION-NAME 类型参数

############## 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

######### 8. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

######### 9. DemDebounceTimeBase

**容器属性**:

- **UUID**: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceTimeBase`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for time based debouncing.

########## 参数配置

此容器包含 **3** 个参数：

########### FLOAT 类型参数

############ 1. DemDebounceTimeFailedThreshold

- **UUID**: `ECUC:4579dd3e-fa1d-404c-a743-9b236697409b`
- **参数名**: `DemDebounceTimeFailedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Failed" qualification.

############ 2. DemDebounceTimePassedThreshold

- **UUID**: `ECUC:e3952bac-0313-43a6-ac7c-19204e3a2662`
- **参数名**: `DemDebounceTimePassedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Passed" qualification.

########### ENUMERATION 类型参数

############ 1. DemDebounceBehavior

- **UUID**: `ECUC:79236e41-97f0-418c-b2f2-241d6595589b`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will

######### 10. DemIndicatorAttribute

**容器属性**:

- **UUID**: `ECUC:38466ee0-81d6-4eb5-84ea-278631d94b99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemIndicatorAttribute`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the event specific configuration of Indicators.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. DemIndicatorFailureCycleCounterThreshold

- **UUID**: `ECUC:bc2a7554-29fe-4a08-a8a8-57087833e55c`
- **参数名**: `DemIndicatorFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the WarningIndicatorOnCriteria.

############ 2. DemIndicatorHealingCycleCounterThreshold

- **UUID**: `ECUC:4248526d-57f1-4519-bb2d-400a541280f5`
- **参数名**: `DemIndicatorHealingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of healing cycles for the WarningIndicatorOffCriteria.

########### ENUMERATION 类型参数

############ 1. DemIndicatorBehaviour

- **UUID**: `ECUC:26582faa-e852-45d6-a68d-cf0cc279ca26`
- **参数名**: `DemIndicatorBehaviour`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_INDICATOR_BLINKING` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_BLINK_CONT` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_FAST_FLASH` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_SLOW_FLASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Behaviour of the linked indicator

############ 2. DemIndicatorFailureCycleSource

- **UUID**: `ECUC:9224f6ca-d10a-4b8d-9b76-da543ec42a3a`
- **参数名**: `DemIndicatorFailureCycleSource`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_FAILURE_CYCLE_EVENT` (来源: AUTOSAR_ECUC)
  - `DEM_FAILURE_CYCLE_INDICATOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, which failure cycle is used for the WarningIndicatorOnCriteria handling.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. DemIndicatorFailureCycleRef

- **UUID**: `ECUC:3fc5415b-ef0e-4616-84af-ac48fb00b4e7`
- **引用名**: `DemIndicatorFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the indicator controlled by the according event used for the WarningIndicatorOnCriteria.

############ 2. DemIndicatorHealingCycleRef

- **UUID**: `ECUC:01818b0e-d069-473b-bb27-f067edb1f453`
- **引用名**: `DemIndicatorHealingCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of healing cycle for the indicator controlled by the according event used for the WarningIndicatorOffCriteria.

############ 3. DemIndicatorRef

- **UUID**: `ECUC:328aa173-bf87-415a-a94c-8b48686226a6`
- **引用名**: `DemIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used indicator.

######### 11. DemDebounceAlgorithmClass

**容器属性**:

- **UUID**: `ECUC:98a5d79e-8975-48e4-bbc8-a174596e2dbb`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDebounceAlgorithmClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDebounceCounterBased**
  - UUID: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
  - 描述: This container contains the configuration (parameters) for counter based debouncing.
- **DemDebounceMonitorInternal**
  - UUID: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
  - 描述: This container contains the configuration (parameters) for monitor internal debouncing.
- **DemCallbackGetFDC**
  - UUID: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
  - 描述: The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.
- **DemDebounceTimeBase**
  - UUID: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
  - 描述: This container contains the configuration (parameters) for time based debouncing.

**容器描述**:

Debounce algorithm class: counter based, time based, or monitor internal.

####### 5. DemCallbackClearEventAllowed

**容器属性**:

- **UUID**: `ECUC:81830ba7-c118-43dd-baf9-d89bcec71b90`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackClearEventAllowed`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates that the Dem has access to a "ClearEventAllowed" callback.

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. DemClearEventAllowedBehavior

- **UUID**: `ECUC:7411934a-7525-44dd-b02b-e0681e08b4c2`
- **参数名**: `DemClearEventAllowedBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DEM_NO_STATUS_BYTE_CHANGE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_NO_STATUS_BYTE_CHANGE` (来源: AUTOSAR_ECUC)
  - `DEM_ONLY_THIS_CYCLE_AND_READINESS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the resulting UDS status byte for the related event, which must not be cleared according to the ClearEventAllowed callback.

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackClearEventAllowedFnc

- **UUID**: `ECUC:f57a2f55-06b0-438d-9a41-d2626089d446`
- **参数名**: `DemCallbackClearEventAllowedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "ClearEventAllowed".

####### 6. DemCallbackEventDataChanged

**容器属性**:

- **UUID**: `ECUC:48673ef9-0ee2-44e2-a4da-c56610dd6792`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackEventDataChanged`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates that the Dem has access to an "EventDataChanged" callback.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackEventDataChangedFnc

- **UUID**: `ECUC:620931a3-319d-4e30-8896-df7694afa222`
- **参数名**: `DemCallbackEventDataChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "EventDataChanged"

####### 7. DemCallbackEventStatusChanged

**容器属性**:

- **UUID**: `ECUC:505d125c-04db-4d5e-92f4-d73e664f7174`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackEventStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to an "EventStatusChanged" callback, which the Dem will call to notify other components about the change in the status of an event.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackEventStatusChangedFnc

- **UUID**: `ECUC:0a1de324-a6d1-4b23-ba12-631c41dbd8cc`
- **参数名**: `DemCallbackEventStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "EventStatusChanged"

####### 8. DemCallbackInitMForE

**容器属性**:

- **UUID**: `ECUC:11b1adbe-fd9a-49a2-a43e-01bed9346c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackInitMForE`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to an "InitMonitorForEvent" callback, which the Dem will call to initialize a monitor.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackInitMForEFnc

- **UUID**: `ECUC:46ba0efd-c45e-4400-a6f9-0441ffe9df5b`
- **参数名**: `DemCallbackInitMForEFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "InitMonitorForEvent".

####### 9. DemEventClass

**容器属性**:

- **UUID**: `ECUC:5127af6d-f63f-46f2-9279-2ddfa6850162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemEventClass`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for EventClass

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. DemAgingCycleCounterThreshold

- **UUID**: `ECUC:c005de82-ee68-46ba-8069-ed248a20b11b`
- **参数名**: `DemAgingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of aging cycles needed to unlearn/delete the event.

########## 2. DemEventFailureCycleCounterThreshold

- **UUID**: `ECUC:6506cb9d-36d0-4f67-89f7-266b9f4cbc3a`
- **参数名**: `DemEventFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the event based fault confirmation.

########## 3. DemEventMemoryEntryFdcThresholdStorageValue

- **UUID**: `ECUC:8dd83213-1223-4eff-ac82-a316ef9d215d`
- **参数名**: `DemEventMemoryEntryFdcThresholdStorageValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold to allocate an event memory entry and to capture the Freeze Frame.

########## 4. DemEventPriority

- **UUID**: `ECUC:3ef7c809-cd40-4824-b0cd-da79a594c75d`
- **参数名**: `DemEventPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of the event, in view of full event buffer.

######### BOOLEAN 类型参数

########## 1. DemAgingAllowed

- **UUID**: `ECUC:13bf7d23-8cc0-4b57-8911-92658b0cb328`
- **参数名**: `DemAgingAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to allow aging/unlearning of the event or not.

########## 2. DemConsiderPtoStatus

- **UUID**: `ECUC:ade2dfbd-edda-4dba-82cf-889cca141ba3`
- **参数名**: `DemConsiderPtoStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is TRUE, when the event is affected by the Dem PTO handling.

########## 3. DemFFPrestorageSupported

- **UUID**: `ECUC:998abc59-21d6-4f48-98d2-f84c83c31b9e`
- **参数名**: `DemFFPrestorageSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter is set to true, then the Prestorage of FreezeFrames is supported by the assigned event. This parameter is useful to calculate the buffer size.

######### ENUMERATION 类型参数

########## 1. DemEventDestination

- **UUID**: `ECUC:3d77d2e5-cd5d-463c-a083-aca98fec267d`
- **参数名**: `DemEventDestination`
- **数据类型**: ENUMERATION
- **多重性**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTC_ORIGIN_MIRROR_MEMORY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_ORIGIN_PRIMARY_MEMORY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_ORIGIN_SECONDARY_MEMORY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The event destination assigns events to none, one or multiple origins.

########## 2. DemEventOBDReadinessGroup

- **UUID**: `ECUC:bd389f92-bcb8-4921-acc3-d96cb78371b6`
- **参数名**: `DemEventOBDReadinessGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_OBD_RDY_AC` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_BOOSTPR` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_CAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_CMPRCMPT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_EGSENS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_ERG` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_EVAP` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_FLSYS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_FLSYS_NONCONT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_HCCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_HTCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_MISF` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_NONE` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_NOXCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_O2SENS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_O2SENSHT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_PMFLT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_SECAIR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the Event OBD Readiness group for PID $01 and PID $41 computation.

########## 3. DemEventSignificance

- **UUID**: `ECUC:73be02e4-de26-4bf9-87d8-8f6d3b15f532`
- **参数名**: `DemEventSignificance`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_EVENT_SIGNIFICANCE_FAULT` (来源: AUTOSAR_ECUC)
  - `DEM_EVENT_SIGNIFICANCE_OCCURRENCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Significance of the event, which indicates additional information concerning fault classification and resolution.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. DemEnableConditionGroupRef

- **UUID**: `ECUC:6953a02d-6999-4d84-8c1d-daede62dfc77`
- **引用名**: `DemEnableConditionGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEnableConditionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemEnableConditionGroup`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References an enable condition group.

########## 2. DemEventFailureCycleRef

- **UUID**: `ECUC:2f31cb98-c767-407b-82e7-fe6fcdf86076`
- **引用名**: `DemEventFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the event based fault confirmation.

########## 3. DemOperationCycleRef

- **UUID**: `ECUC:fc68bc01-d147-4b6d-95a2-36cfa577cacf`
- **引用名**: `DemOperationCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of operation cycle for the event (e.g. power cycle, driving cycle, ...)

########## 4. DemStorageConditionGroupRef

- **UUID**: `ECUC:92052d72-8af4-4f08-9d1f-2a901238caf9`
- **引用名**: `DemStorageConditionGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemStorageConditionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemStorageConditionGroup`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References a storage condition group.

######### CHOICE-REFERENCE 类型引用

########## 1. DemAgingCycleRef

- **UUID**: `ECUC:2c17db4a-8035-4b38-bca3-093e53f7d34d`
- **引用名**: `DemAgingCycleRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC V1.0.0
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemAgingCycle`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the cycle which is triggering the aging of the event. This can either be the same as the operation cycle of the event, or a separate aging cycle reported via API Dem_SetAgingCycleState. If external aging is configured (refer to DemAgingCycleCounterProcessing), this parameter is not used.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. DemDebounceCounterBased

**容器属性**:

- **UUID**: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceCounterBased`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for counter based debouncing.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. DemDebounceCounterDecrementStepSize

- **UUID**: `ECUC:07c58e53-a31c-421d-a6eb-910f2d3cd2d8`
- **参数名**: `DemDebounceCounterDecrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32768]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for decrementation of the internal debounce counter (PREPASSED).

############ 2. DemDebounceCounterFailedThreshold

- **UUID**: `ECUC:aff278be-3537-4099-8858-212582caf8f2`
- **参数名**: `DemDebounceCounterFailedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the failed status.

############ 3. DemDebounceCounterIncrementStepSize

- **UUID**: `ECUC:7cde5c15-c87f-4eed-b0f5-38313a32efe2`
- **参数名**: `DemDebounceCounterIncrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for incrementation of the internal debounce counter (PREFAILED).

############ 4. DemDebounceCounterJumpDownValue

- **UUID**: `ECUC:7baa87e8-87d0-45bb-9937-a8c3a4ebc2b6`
- **参数名**: `DemDebounceCounterJumpDownValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Down value of the internal debounce counter which is taken as initialization value for the counter when the respective step-down occurs.

############ 5. DemDebounceCounterJumpUpValue

- **UUID**: `ECUC:86693810-0a0a-4927-91ae-5d3723761724`
- **参数名**: `DemDebounceCounterJumpUpValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Up value of the internal debounce counter which is taken as initialization value for the counter when the respective step-up occurs.

############ 6. DemDebounceCounterPassedThreshold

- **UUID**: `ECUC:2c4aba4f-9fc9-4572-a226-9562516ffac3`
- **参数名**: `DemDebounceCounterPassedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..-1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the passed status.

########### BOOLEAN 类型参数

############ 1. DemDebounceCounterJumpDown

- **UUID**: `ECUC:aa2d713a-ec74-4c4c-93a9-bd83b0c107b8`
- **参数名**: `DemDebounceCounterJumpDown`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Down.

############ 2. DemDebounceCounterJumpUp

- **UUID**: `ECUC:6f82b9d4-c3e1-4f00-8196-1f85c7be1562`
- **参数名**: `DemDebounceCounterJumpUp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Up.

############ 3. DemDebounceCounterStorage

- **UUID**: `ECUC:33babe76-7e6b-44dc-8233-e33933cf87e7`
- **参数名**: `DemDebounceCounterStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to store the debounce counter value non-volatile or not.

########### ENUMERATION 类型参数

############ 1. DemDebounceBehavior

- **UUID**: `ECUC:6fd7cbcb-976b-46c5-bd9c-2ac97686f52d`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will behave, if a related enable condition is not fulfilled or ControlDTCSetting of the related event is disabled.

######### 2. DemDebounceMonitorInternal

**容器属性**:

- **UUID**: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceMonitorInternal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for monitor internal debouncing.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

############ 参数配置

此容器包含 **1** 个参数：

############# FUNCTION-NAME 类型参数

############## 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

######### 3. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

######### 4. DemDebounceTimeBase

**容器属性**:

- **UUID**: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceTimeBase`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for time based debouncing.

########## 参数配置

此容器包含 **3** 个参数：

########### FLOAT 类型参数

############ 1. DemDebounceTimeFailedThreshold

- **UUID**: `ECUC:4579dd3e-fa1d-404c-a743-9b236697409b`
- **参数名**: `DemDebounceTimeFailedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Failed" qualification.

############ 2. DemDebounceTimePassedThreshold

- **UUID**: `ECUC:e3952bac-0313-43a6-ac7c-19204e3a2662`
- **参数名**: `DemDebounceTimePassedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Passed" qualification.

########### ENUMERATION 类型参数

############ 1. DemDebounceBehavior

- **UUID**: `ECUC:79236e41-97f0-418c-b2f2-241d6595589b`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will

######### 5. DemIndicatorAttribute

**容器属性**:

- **UUID**: `ECUC:38466ee0-81d6-4eb5-84ea-278631d94b99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemIndicatorAttribute`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the event specific configuration of Indicators.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. DemIndicatorFailureCycleCounterThreshold

- **UUID**: `ECUC:bc2a7554-29fe-4a08-a8a8-57087833e55c`
- **参数名**: `DemIndicatorFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the WarningIndicatorOnCriteria.

############ 2. DemIndicatorHealingCycleCounterThreshold

- **UUID**: `ECUC:4248526d-57f1-4519-bb2d-400a541280f5`
- **参数名**: `DemIndicatorHealingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of healing cycles for the WarningIndicatorOffCriteria.

########### ENUMERATION 类型参数

############ 1. DemIndicatorBehaviour

- **UUID**: `ECUC:26582faa-e852-45d6-a68d-cf0cc279ca26`
- **参数名**: `DemIndicatorBehaviour`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_INDICATOR_BLINKING` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_BLINK_CONT` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_FAST_FLASH` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_SLOW_FLASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Behaviour of the linked indicator

############ 2. DemIndicatorFailureCycleSource

- **UUID**: `ECUC:9224f6ca-d10a-4b8d-9b76-da543ec42a3a`
- **参数名**: `DemIndicatorFailureCycleSource`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_FAILURE_CYCLE_EVENT` (来源: AUTOSAR_ECUC)
  - `DEM_FAILURE_CYCLE_INDICATOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, which failure cycle is used for the WarningIndicatorOnCriteria handling.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. DemIndicatorFailureCycleRef

- **UUID**: `ECUC:3fc5415b-ef0e-4616-84af-ac48fb00b4e7`
- **引用名**: `DemIndicatorFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the indicator controlled by the according event used for the WarningIndicatorOnCriteria.

############ 2. DemIndicatorHealingCycleRef

- **UUID**: `ECUC:01818b0e-d069-473b-bb27-f067edb1f453`
- **引用名**: `DemIndicatorHealingCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of healing cycle for the indicator controlled by the according event used for the WarningIndicatorOffCriteria.

############ 3. DemIndicatorRef

- **UUID**: `ECUC:328aa173-bf87-415a-a94c-8b48686226a6`
- **引用名**: `DemIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used indicator.

######### 6. DemDebounceAlgorithmClass

**容器属性**:

- **UUID**: `ECUC:98a5d79e-8975-48e4-bbc8-a174596e2dbb`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDebounceAlgorithmClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDebounceCounterBased**
  - UUID: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
  - 描述: This container contains the configuration (parameters) for counter based debouncing.
- **DemDebounceMonitorInternal**
  - UUID: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
  - 描述: This container contains the configuration (parameters) for monitor internal debouncing.
- **DemCallbackGetFDC**
  - UUID: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
  - 描述: The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.
- **DemDebounceTimeBase**
  - UUID: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
  - 描述: This container contains the configuration (parameters) for time based debouncing.

**容器描述**:

Debounce algorithm class: counter based, time based, or monitor internal.

####### 10. DemDebounceCounterBased

**容器属性**:

- **UUID**: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceCounterBased`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for counter based debouncing.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. DemDebounceCounterDecrementStepSize

- **UUID**: `ECUC:07c58e53-a31c-421d-a6eb-910f2d3cd2d8`
- **参数名**: `DemDebounceCounterDecrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32768]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for decrementation of the internal debounce counter (PREPASSED).

########## 2. DemDebounceCounterFailedThreshold

- **UUID**: `ECUC:aff278be-3537-4099-8858-212582caf8f2`
- **参数名**: `DemDebounceCounterFailedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the failed status.

########## 3. DemDebounceCounterIncrementStepSize

- **UUID**: `ECUC:7cde5c15-c87f-4eed-b0f5-38313a32efe2`
- **参数名**: `DemDebounceCounterIncrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for incrementation of the internal debounce counter (PREFAILED).

########## 4. DemDebounceCounterJumpDownValue

- **UUID**: `ECUC:7baa87e8-87d0-45bb-9937-a8c3a4ebc2b6`
- **参数名**: `DemDebounceCounterJumpDownValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Down value of the internal debounce counter which is taken as initialization value for the counter when the respective step-down occurs.

########## 5. DemDebounceCounterJumpUpValue

- **UUID**: `ECUC:86693810-0a0a-4927-91ae-5d3723761724`
- **参数名**: `DemDebounceCounterJumpUpValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Up value of the internal debounce counter which is taken as initialization value for the counter when the respective step-up occurs.

########## 6. DemDebounceCounterPassedThreshold

- **UUID**: `ECUC:2c4aba4f-9fc9-4572-a226-9562516ffac3`
- **参数名**: `DemDebounceCounterPassedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..-1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the passed status.

######### BOOLEAN 类型参数

########## 1. DemDebounceCounterJumpDown

- **UUID**: `ECUC:aa2d713a-ec74-4c4c-93a9-bd83b0c107b8`
- **参数名**: `DemDebounceCounterJumpDown`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Down.

########## 2. DemDebounceCounterJumpUp

- **UUID**: `ECUC:6f82b9d4-c3e1-4f00-8196-1f85c7be1562`
- **参数名**: `DemDebounceCounterJumpUp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Up.

########## 3. DemDebounceCounterStorage

- **UUID**: `ECUC:33babe76-7e6b-44dc-8233-e33933cf87e7`
- **参数名**: `DemDebounceCounterStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to store the debounce counter value non-volatile or not.

######### ENUMERATION 类型参数

########## 1. DemDebounceBehavior

- **UUID**: `ECUC:6fd7cbcb-976b-46c5-bd9c-2ac97686f52d`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will behave, if a related enable condition is not fulfilled or ControlDTCSetting of the related event is disabled.

####### 11. DemDebounceMonitorInternal

**容器属性**:

- **UUID**: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceMonitorInternal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for monitor internal debouncing.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

####### 12. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

####### 13. DemDebounceTimeBase

**容器属性**:

- **UUID**: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceTimeBase`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for time based debouncing.

######## 参数配置

此容器包含 **3** 个参数：

######### FLOAT 类型参数

########## 1. DemDebounceTimeFailedThreshold

- **UUID**: `ECUC:4579dd3e-fa1d-404c-a743-9b236697409b`
- **参数名**: `DemDebounceTimeFailedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Failed" qualification.

########## 2. DemDebounceTimePassedThreshold

- **UUID**: `ECUC:e3952bac-0313-43a6-ac7c-19204e3a2662`
- **参数名**: `DemDebounceTimePassedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Passed" qualification.

######### ENUMERATION 类型参数

########## 1. DemDebounceBehavior

- **UUID**: `ECUC:79236e41-97f0-418c-b2f2-241d6595589b`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will

####### 14. DemIndicatorAttribute

**容器属性**:

- **UUID**: `ECUC:38466ee0-81d6-4eb5-84ea-278631d94b99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemIndicatorAttribute`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the event specific configuration of Indicators.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DemIndicatorFailureCycleCounterThreshold

- **UUID**: `ECUC:bc2a7554-29fe-4a08-a8a8-57087833e55c`
- **参数名**: `DemIndicatorFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the WarningIndicatorOnCriteria.

########## 2. DemIndicatorHealingCycleCounterThreshold

- **UUID**: `ECUC:4248526d-57f1-4519-bb2d-400a541280f5`
- **参数名**: `DemIndicatorHealingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of healing cycles for the WarningIndicatorOffCriteria.

######### ENUMERATION 类型参数

########## 1. DemIndicatorBehaviour

- **UUID**: `ECUC:26582faa-e852-45d6-a68d-cf0cc279ca26`
- **参数名**: `DemIndicatorBehaviour`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_INDICATOR_BLINKING` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_BLINK_CONT` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_FAST_FLASH` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_SLOW_FLASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Behaviour of the linked indicator

########## 2. DemIndicatorFailureCycleSource

- **UUID**: `ECUC:9224f6ca-d10a-4b8d-9b76-da543ec42a3a`
- **参数名**: `DemIndicatorFailureCycleSource`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_FAILURE_CYCLE_EVENT` (来源: AUTOSAR_ECUC)
  - `DEM_FAILURE_CYCLE_INDICATOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, which failure cycle is used for the WarningIndicatorOnCriteria handling.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. DemIndicatorFailureCycleRef

- **UUID**: `ECUC:3fc5415b-ef0e-4616-84af-ac48fb00b4e7`
- **引用名**: `DemIndicatorFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the indicator controlled by the according event used for the WarningIndicatorOnCriteria.

########## 2. DemIndicatorHealingCycleRef

- **UUID**: `ECUC:01818b0e-d069-473b-bb27-f067edb1f453`
- **引用名**: `DemIndicatorHealingCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of healing cycle for the indicator controlled by the according event used for the WarningIndicatorOffCriteria.

########## 3. DemIndicatorRef

- **UUID**: `ECUC:328aa173-bf87-415a-a94c-8b48686226a6`
- **引用名**: `DemIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used indicator.

####### 15. DemJ1939NodeAddress

**容器属性**:

- **UUID**: `ECUC:27441308-61a5-44f9-8352-4d8afd5c2f68`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemJ1939NodeAddress`
- **多重性**: [0..255]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the parameters for the support of a logical J1939 node (identified by an ECU address).

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. DemJ1939NmNodeRef

- **UUID**: `ECUC:a36d170a-9faa-439d-a951-d2bd5c8a6004`
- **引用名**: `DemJ1939NmNodeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..255]
- **目标**: `J1939NmNode`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Nm/J1939NmConfigSet/J1939NmNode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the corresponding J1939Nm node.

####### 16. DemPidClass

**容器属性**:

- **UUID**: `ECUC:44faa8c1-9430-4ce8-b572-a9033e48bdd5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemPidClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the different PIDs for the single global OBD relevant freeze frame class. It is assembled out of one or several data elements.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DemPidIdentifier

- **UUID**: `ECUC:18337b6d-c988-4e65-9896-c0814ac35f45`
- **参数名**: `DemPidIdentifier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: identifier of the PID

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DemPidDataElement

**容器属性**:

- **UUID**: `ECUC:08dbe78d-7b7b-4510-bfa9-3ce041b597d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemPidDataElement`
- **多重性**: [1..255]
- **多配置容器**: false

**容器描述**:

This container contains the different data elements contained in the specific PID.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. DemPidDataElementClassRef

- **UUID**: `ECUC:e55a5a69-f687-4fd6-9b48-17ca02603d1d`
- **引用名**: `DemPidDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

####### 17. DemPidDataElement

**容器属性**:

- **UUID**: `ECUC:08dbe78d-7b7b-4510-bfa9-3ce041b597d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemPidDataElement`
- **多重性**: [1..255]
- **多配置容器**: false

**容器描述**:

This container contains the different data elements contained in the specific PID.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DemPidDataElementClassRef

- **UUID**: `ECUC:e55a5a69-f687-4fd6-9b48-17ca02603d1d`
- **引用名**: `DemPidDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

####### 18. DemDebounceAlgorithmClass

**容器属性**:

- **UUID**: `ECUC:98a5d79e-8975-48e4-bbc8-a174596e2dbb`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDebounceAlgorithmClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDebounceCounterBased**
  - UUID: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
  - 描述: This container contains the configuration (parameters) for counter based debouncing.
- **DemDebounceMonitorInternal**
  - UUID: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
  - 描述: This container contains the configuration (parameters) for monitor internal debouncing.
- **DemCallbackGetFDC**
  - UUID: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
  - 描述: The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.
- **DemDebounceTimeBase**
  - UUID: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
  - 描述: This container contains the configuration (parameters) for time based debouncing.

**容器描述**:

Debounce algorithm class: counter based, time based, or monitor internal.

##### 2. DemDTCClass

**容器属性**:

- **UUID**: `ECUC:10f37378-2b66-4089-aec4-382cb9316830`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDTCClass`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for DTCClass.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. DemDTCFunctionalUnit

- **UUID**: `ECUC:467cf2b5-284e-4cd6-9004-831fb0599388`
- **参数名**: `DemDTCFunctionalUnit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: DTCFuncitonalUnit is a 1-byte value which identifies the corresponding basic vehicle / system function which reports the DTC. This parameter is necessary for the report of severity information.

######## 2. DemJ1939DTC

- **UUID**: `ECUC:d62b52a5-97bd-4f04-a64d-e88dda34eb15`
- **参数名**: `DemJ1939DTC`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..16777214]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique Diagnostic Trouble Code value for J1939 (consiting of SPN and FMI)

######## 3. DemObdDTC

- **UUID**: `ECUC:e979a29e-4aef-405e-aee7-2dc1c41b6c04`
- **参数名**: `DemObdDTC`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique Diagnostic Trouble Code value for OBD

######## 4. DemUdsDTC

- **UUID**: `ECUC:c1fc7bad-0617-4667-8f03-ef4094b29060`
- **参数名**: `DemUdsDTC`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..16777214]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique Diagnostic Trouble Code value for UDS

####### BOOLEAN 类型参数

######## 1. DemImmediateNvStorage

- **UUID**: `ECUC:09b420be-542a-4655-beaa-bc967dfcd3e8`
- **参数名**: `DemImmediateNvStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to enable immediate storage triggering of an according event memory entriy persistently to NVRAM.

####### ENUMERATION 类型参数

######## 1. DemDTCSeverity

- **UUID**: `ECUC:ec5f19c2-2f59-4a05-a5a7-21fc4e8b49e3`
- **参数名**: `DemDTCSeverity`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DEM_DTC_SEV_NO_SEVERITY`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTC_SEV_CHECK_AT_NEXT_HALT` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_SEV_IMMEDIATELY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_SEV_MAINTENANCE_ONLY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_SEV_NO_SEVERITY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: DTC severity according to ISO 14229-1. This parameter depends on the automotive manufacturer.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DemJ1939DTC_NodeAddressRef

- **UUID**: `ECUC:399fa3b9-2fc9-44ab-a7b2-25b1a2c7f40b`
- **引用名**: `DemJ1939DTC_NodeAddressRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemJ1939NodeAddress`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemJ1939NodeAddress`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a J1939 NodeAddress

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DemCallbackInitMForF

**容器属性**:

- **UUID**: `ECUC:d73df317-2911-4d4c-8d81-466df02d7e55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackInitMForF`
- **多重性**: [0..infinite]
- **多配置容器**: false

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackInitMForFFnc

- **UUID**: `ECUC:2415de0a-e9e7-45e0-b2fd-c955bc96b0ea`
- **参数名**: `DemCallbackInitMForFFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "InitMonitorForFunction".

##### 3. DemCallbackInitMForF

**容器属性**:

- **UUID**: `ECUC:d73df317-2911-4d4c-8d81-466df02d7e55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackInitMForF`
- **多重性**: [0..infinite]
- **多配置容器**: false

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DemCallbackInitMForFFnc

- **UUID**: `ECUC:2415de0a-e9e7-45e0-b2fd-c955bc96b0ea`
- **参数名**: `DemCallbackInitMForFFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "InitMonitorForFunction".

##### 4. DemDtr

**容器属性**:

- **UUID**: `ECUC:048c7ac5-d3b3-4277-91af-bbdb75a2bd3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDtr`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container holds the configuration of one individual DTR.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. DemDtrId

- **UUID**: `ECUC:9c14e03c-5be7-4392-b637-ad7293e74d5f`
- **参数名**: `DemDtrId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The index identifier value assigned to this DTR. The value is generated during the Dem configuration process.

######## 2. DemDtrMid

- **UUID**: `ECUC:2cb52e21-b358-4631-82d4-ec342e69d3b8`
- **参数名**: `DemDtrMid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The OBDMID of the DTR.

######## 3. DemDtrTid

- **UUID**: `ECUC:4da5ac1a-81b6-454e-9da7-222ef76ea52d`
- **参数名**: `DemDtrTid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The OBDTID of the DTR.

######## 4. DemDtrUasid

- **UUID**: `ECUC:b29dfc82-e531-4ccd-a648-97a890536902`
- **参数名**: `DemDtrUasid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The UaSId the DTR data shall be scaled to, and reported together with the rescaled DTR data.

####### FLOAT 类型参数

######## 1. DemDtrCompuDenominator0

- **UUID**: `ECUC:5c85b81d-2f61-4fbd-b25f-e128ee47865a`
- **参数名**: `DemDtrCompuDenominator0`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Part of the conversion between the binary representation and the physical meaning analogous to the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1 denominator coefficient in the direction compuInternalToPhys.

######## 2. DemDtrCompuNumerator0

- **UUID**: `ECUC:2a37b812-08e6-4de4-8ebb-4268f02b47a3`
- **参数名**: `DemDtrCompuNumerator0`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Part of the conversion between the binary representation and the physical meaning analogous to the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1 denominator coefficient in the direction compuInternalToPhys.

######## 3. DemDtrCompuNumerator1

- **UUID**: `ECUC:ac631547-516f-4d48-8a71-1fe3c0d49638`
- **参数名**: `DemDtrCompuNumerator1`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Part of the conversion between the binary representation and the physical meaning analogous to the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1 denominator coefficient in the direction compuInternalToPhys.

####### ENUMERATION 类型参数

######## 1. DemDtrUpdateKind

- **UUID**: `ECUC:f58baecb-daa8-449b-b8b7-ddbe112c024d`
- **参数名**: `DemDtrUpdateKind`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTR_UPDATE_ALWAYS` (来源: AUTOSAR_ECUC)
  - `DEM_DTR_UPDATE_STEADY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Update conditions applied by the Dem to reports of DTR values. Only supported if a related Event is configured. If no related Event is configured, the Dem behaves as if DemDtrUpdateKind is configured to "DEM_DTR_UPDATE_ALWAYS".

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DemDtrEventRef

- **UUID**: `ECUC:b5eb778a-d83b-4f33-9432-a212ca1caa0c`
- **引用名**: `DemDtrEventRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter this DTR is related to. If the related event is not configured, the Dem cannot ensure consistency between the DTR and the event.

##### 5. DemEventParameter

**容器属性**:

- **UUID**: `ECUC:17edd206-934c-420b-a50a-75aef6269ac7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemEventParameter`
- **多重性**: [1..65535]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for events.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. DemEventId

- **UUID**: `ECUC:a42e4864-6ec3-4459-ae25-2a314d4a0e42`
- **参数名**: `DemEventId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier of a diagnostic event.

######## 2. DemMaxNumberFreezeFrameRecords

- **UUID**: `ECUC:0c06d2a8-5789-4416-8c13-f331b2f5d081`
- **参数名**: `DemMaxNumberFreezeFrameRecords`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of according freeze frame records, which can maximal be stored for this event. Therefore all these freeze frame records have the same freeze frame class.

####### BOOLEAN 类型参数

######## 1. DemEventAvailable

- **UUID**: `ECUC:6b0b03bd-1d0c-47c8-b723-0bca376ea53a`
- **参数名**: `DemEventAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter configures an Event as unavailable.

####### ENUMERATION 类型参数

######## 1. DemEventKind

- **UUID**: `ECUC:44e8a61c-a95b-487d-908b-0ca87be434d4`
- **参数名**: `DemEventKind`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_EVENT_KIND_BSW` (来源: AUTOSAR_ECUC)
  - `DEM_EVENT_KIND_SWC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to distinguish between SW-C and BSW events. SW-C events are reported by Dem_SetEventStatus API and BSW events are reported by Dem_ReportErrorStatus API.

###### 引用关系

此容器包含 **7** 个引用：

####### REFERENCE 类型引用

######## 1. DemDTCClassRef

- **UUID**: `ECUC:89db0687-72d2-47f9-9e6a-6bcf25fde654`
- **引用名**: `DemDTCClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemDTCClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemDTCClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the DTC configuration associated with the diagnostic event.

######## 2. DemExtendedDataClassRef

- **UUID**: `ECUC:aad40479-8bd6-451a-86f6-d42e15b8bd26`
- **引用名**: `DemExtendedDataClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemExtendedDataClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemExtendedDataClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference defines the link to an extended data class sampler.

######## 3. DemFreezeFrameClassRef

- **UUID**: `ECUC:b980679e-9569-4f3b-8558-841069092eb2`
- **引用名**: `DemFreezeFrameClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemFreezeFrameClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemFreezeFrameClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: These references define the links to a freeze frame class sampler.

######## 4. DemFreezeFrameRecNumClassRef

- **UUID**: `ECUC:37ada416-5e4f-4e2d-82f8-f8f010feb2f4`
- **引用名**: `DemFreezeFrameRecNumClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemFreezeFrameRecNumClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemFreezeFrameRecNumClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the list of dedicated freeze frame record numbers associated with the diagnostic event. These record numbers are assigned to the freeze frame records (instead of calculated record numbers).

######## 5. DemJ1939ExpandedFreezeFrameClassRef

- **UUID**: `ECUC:f9add2f1-9447-4a3b-a021-8152d0c37857`
- **引用名**: `DemJ1939ExpandedFreezeFrameClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemJ1939FreezeFrameClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemGeneralJ1939/DemJ1939FreezeFrameClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: These references define the links to a J1939 freeze frame class sampler.

######## 6. DemJ1939FreezeFrameClassRef

- **UUID**: `ECUC:66c9848c-d60b-4263-80dd-d247536f8d13`
- **引用名**: `DemJ1939FreezeFrameClassRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemJ1939FreezeFrameClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemGeneralJ1939/DemJ1939FreezeFrameClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: These references define the links to a J1939 freeze frame class sampler.

######## 7. DemOBDGroupingAssociativeEventsRef

- **UUID**: `ECUC:e6a5765e-f9e2-43d8-9b3e-23b46ec06e7a`
- **引用名**: `DemOBDGroupingAssociativeEventsRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a reference which points to a representative event of one group of associate events.

###### 配置容器

本模块包含 **11** 个配置容器：

####### 1. DemCallbackClearEventAllowed

**容器属性**:

- **UUID**: `ECUC:81830ba7-c118-43dd-baf9-d89bcec71b90`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackClearEventAllowed`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates that the Dem has access to a "ClearEventAllowed" callback.

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. DemClearEventAllowedBehavior

- **UUID**: `ECUC:7411934a-7525-44dd-b02b-e0681e08b4c2`
- **参数名**: `DemClearEventAllowedBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DEM_NO_STATUS_BYTE_CHANGE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_NO_STATUS_BYTE_CHANGE` (来源: AUTOSAR_ECUC)
  - `DEM_ONLY_THIS_CYCLE_AND_READINESS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the resulting UDS status byte for the related event, which must not be cleared according to the ClearEventAllowed callback.

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackClearEventAllowedFnc

- **UUID**: `ECUC:f57a2f55-06b0-438d-9a41-d2626089d446`
- **参数名**: `DemCallbackClearEventAllowedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "ClearEventAllowed".

####### 2. DemCallbackEventDataChanged

**容器属性**:

- **UUID**: `ECUC:48673ef9-0ee2-44e2-a4da-c56610dd6792`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackEventDataChanged`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates that the Dem has access to an "EventDataChanged" callback.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackEventDataChangedFnc

- **UUID**: `ECUC:620931a3-319d-4e30-8896-df7694afa222`
- **参数名**: `DemCallbackEventDataChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "EventDataChanged"

####### 3. DemCallbackEventStatusChanged

**容器属性**:

- **UUID**: `ECUC:505d125c-04db-4d5e-92f4-d73e664f7174`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackEventStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to an "EventStatusChanged" callback, which the Dem will call to notify other components about the change in the status of an event.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackEventStatusChangedFnc

- **UUID**: `ECUC:0a1de324-a6d1-4b23-ba12-631c41dbd8cc`
- **参数名**: `DemCallbackEventStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "EventStatusChanged"

####### 4. DemCallbackInitMForE

**容器属性**:

- **UUID**: `ECUC:11b1adbe-fd9a-49a2-a43e-01bed9346c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackInitMForE`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to an "InitMonitorForEvent" callback, which the Dem will call to initialize a monitor.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackInitMForEFnc

- **UUID**: `ECUC:46ba0efd-c45e-4400-a6f9-0441ffe9df5b`
- **参数名**: `DemCallbackInitMForEFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "InitMonitorForEvent".

####### 5. DemEventClass

**容器属性**:

- **UUID**: `ECUC:5127af6d-f63f-46f2-9279-2ddfa6850162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemEventClass`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for EventClass

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. DemAgingCycleCounterThreshold

- **UUID**: `ECUC:c005de82-ee68-46ba-8069-ed248a20b11b`
- **参数名**: `DemAgingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of aging cycles needed to unlearn/delete the event.

########## 2. DemEventFailureCycleCounterThreshold

- **UUID**: `ECUC:6506cb9d-36d0-4f67-89f7-266b9f4cbc3a`
- **参数名**: `DemEventFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the event based fault confirmation.

########## 3. DemEventMemoryEntryFdcThresholdStorageValue

- **UUID**: `ECUC:8dd83213-1223-4eff-ac82-a316ef9d215d`
- **参数名**: `DemEventMemoryEntryFdcThresholdStorageValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold to allocate an event memory entry and to capture the Freeze Frame.

########## 4. DemEventPriority

- **UUID**: `ECUC:3ef7c809-cd40-4824-b0cd-da79a594c75d`
- **参数名**: `DemEventPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of the event, in view of full event buffer.

######### BOOLEAN 类型参数

########## 1. DemAgingAllowed

- **UUID**: `ECUC:13bf7d23-8cc0-4b57-8911-92658b0cb328`
- **参数名**: `DemAgingAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to allow aging/unlearning of the event or not.

########## 2. DemConsiderPtoStatus

- **UUID**: `ECUC:ade2dfbd-edda-4dba-82cf-889cca141ba3`
- **参数名**: `DemConsiderPtoStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is TRUE, when the event is affected by the Dem PTO handling.

########## 3. DemFFPrestorageSupported

- **UUID**: `ECUC:998abc59-21d6-4f48-98d2-f84c83c31b9e`
- **参数名**: `DemFFPrestorageSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter is set to true, then the Prestorage of FreezeFrames is supported by the assigned event. This parameter is useful to calculate the buffer size.

######### ENUMERATION 类型参数

########## 1. DemEventDestination

- **UUID**: `ECUC:3d77d2e5-cd5d-463c-a083-aca98fec267d`
- **参数名**: `DemEventDestination`
- **数据类型**: ENUMERATION
- **多重性**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTC_ORIGIN_MIRROR_MEMORY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_ORIGIN_PRIMARY_MEMORY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_ORIGIN_SECONDARY_MEMORY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The event destination assigns events to none, one or multiple origins.

########## 2. DemEventOBDReadinessGroup

- **UUID**: `ECUC:bd389f92-bcb8-4921-acc3-d96cb78371b6`
- **参数名**: `DemEventOBDReadinessGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_OBD_RDY_AC` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_BOOSTPR` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_CAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_CMPRCMPT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_EGSENS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_ERG` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_EVAP` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_FLSYS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_FLSYS_NONCONT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_HCCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_HTCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_MISF` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_NONE` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_NOXCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_O2SENS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_O2SENSHT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_PMFLT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_SECAIR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the Event OBD Readiness group for PID $01 and PID $41 computation.

########## 3. DemEventSignificance

- **UUID**: `ECUC:73be02e4-de26-4bf9-87d8-8f6d3b15f532`
- **参数名**: `DemEventSignificance`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_EVENT_SIGNIFICANCE_FAULT` (来源: AUTOSAR_ECUC)
  - `DEM_EVENT_SIGNIFICANCE_OCCURRENCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Significance of the event, which indicates additional information concerning fault classification and resolution.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. DemEnableConditionGroupRef

- **UUID**: `ECUC:6953a02d-6999-4d84-8c1d-daede62dfc77`
- **引用名**: `DemEnableConditionGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEnableConditionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemEnableConditionGroup`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References an enable condition group.

########## 2. DemEventFailureCycleRef

- **UUID**: `ECUC:2f31cb98-c767-407b-82e7-fe6fcdf86076`
- **引用名**: `DemEventFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the event based fault confirmation.

########## 3. DemOperationCycleRef

- **UUID**: `ECUC:fc68bc01-d147-4b6d-95a2-36cfa577cacf`
- **引用名**: `DemOperationCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of operation cycle for the event (e.g. power cycle, driving cycle, ...)

########## 4. DemStorageConditionGroupRef

- **UUID**: `ECUC:92052d72-8af4-4f08-9d1f-2a901238caf9`
- **引用名**: `DemStorageConditionGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemStorageConditionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemStorageConditionGroup`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References a storage condition group.

######### CHOICE-REFERENCE 类型引用

########## 1. DemAgingCycleRef

- **UUID**: `ECUC:2c17db4a-8035-4b38-bca3-093e53f7d34d`
- **引用名**: `DemAgingCycleRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC V1.0.0
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemAgingCycle`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the cycle which is triggering the aging of the event. This can either be the same as the operation cycle of the event, or a separate aging cycle reported via API Dem_SetAgingCycleState. If external aging is configured (refer to DemAgingCycleCounterProcessing), this parameter is not used.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. DemDebounceCounterBased

**容器属性**:

- **UUID**: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceCounterBased`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for counter based debouncing.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. DemDebounceCounterDecrementStepSize

- **UUID**: `ECUC:07c58e53-a31c-421d-a6eb-910f2d3cd2d8`
- **参数名**: `DemDebounceCounterDecrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32768]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for decrementation of the internal debounce counter (PREPASSED).

############ 2. DemDebounceCounterFailedThreshold

- **UUID**: `ECUC:aff278be-3537-4099-8858-212582caf8f2`
- **参数名**: `DemDebounceCounterFailedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the failed status.

############ 3. DemDebounceCounterIncrementStepSize

- **UUID**: `ECUC:7cde5c15-c87f-4eed-b0f5-38313a32efe2`
- **参数名**: `DemDebounceCounterIncrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for incrementation of the internal debounce counter (PREFAILED).

############ 4. DemDebounceCounterJumpDownValue

- **UUID**: `ECUC:7baa87e8-87d0-45bb-9937-a8c3a4ebc2b6`
- **参数名**: `DemDebounceCounterJumpDownValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Down value of the internal debounce counter which is taken as initialization value for the counter when the respective step-down occurs.

############ 5. DemDebounceCounterJumpUpValue

- **UUID**: `ECUC:86693810-0a0a-4927-91ae-5d3723761724`
- **参数名**: `DemDebounceCounterJumpUpValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Up value of the internal debounce counter which is taken as initialization value for the counter when the respective step-up occurs.

############ 6. DemDebounceCounterPassedThreshold

- **UUID**: `ECUC:2c4aba4f-9fc9-4572-a226-9562516ffac3`
- **参数名**: `DemDebounceCounterPassedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..-1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the passed status.

########### BOOLEAN 类型参数

############ 1. DemDebounceCounterJumpDown

- **UUID**: `ECUC:aa2d713a-ec74-4c4c-93a9-bd83b0c107b8`
- **参数名**: `DemDebounceCounterJumpDown`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Down.

############ 2. DemDebounceCounterJumpUp

- **UUID**: `ECUC:6f82b9d4-c3e1-4f00-8196-1f85c7be1562`
- **参数名**: `DemDebounceCounterJumpUp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Up.

############ 3. DemDebounceCounterStorage

- **UUID**: `ECUC:33babe76-7e6b-44dc-8233-e33933cf87e7`
- **参数名**: `DemDebounceCounterStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to store the debounce counter value non-volatile or not.

########### ENUMERATION 类型参数

############ 1. DemDebounceBehavior

- **UUID**: `ECUC:6fd7cbcb-976b-46c5-bd9c-2ac97686f52d`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will behave, if a related enable condition is not fulfilled or ControlDTCSetting of the related event is disabled.

######### 2. DemDebounceMonitorInternal

**容器属性**:

- **UUID**: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceMonitorInternal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for monitor internal debouncing.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

############ 参数配置

此容器包含 **1** 个参数：

############# FUNCTION-NAME 类型参数

############## 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

######### 3. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

######### 4. DemDebounceTimeBase

**容器属性**:

- **UUID**: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceTimeBase`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for time based debouncing.

########## 参数配置

此容器包含 **3** 个参数：

########### FLOAT 类型参数

############ 1. DemDebounceTimeFailedThreshold

- **UUID**: `ECUC:4579dd3e-fa1d-404c-a743-9b236697409b`
- **参数名**: `DemDebounceTimeFailedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Failed" qualification.

############ 2. DemDebounceTimePassedThreshold

- **UUID**: `ECUC:e3952bac-0313-43a6-ac7c-19204e3a2662`
- **参数名**: `DemDebounceTimePassedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Passed" qualification.

########### ENUMERATION 类型参数

############ 1. DemDebounceBehavior

- **UUID**: `ECUC:79236e41-97f0-418c-b2f2-241d6595589b`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will

######### 5. DemIndicatorAttribute

**容器属性**:

- **UUID**: `ECUC:38466ee0-81d6-4eb5-84ea-278631d94b99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemIndicatorAttribute`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the event specific configuration of Indicators.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. DemIndicatorFailureCycleCounterThreshold

- **UUID**: `ECUC:bc2a7554-29fe-4a08-a8a8-57087833e55c`
- **参数名**: `DemIndicatorFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the WarningIndicatorOnCriteria.

############ 2. DemIndicatorHealingCycleCounterThreshold

- **UUID**: `ECUC:4248526d-57f1-4519-bb2d-400a541280f5`
- **参数名**: `DemIndicatorHealingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of healing cycles for the WarningIndicatorOffCriteria.

########### ENUMERATION 类型参数

############ 1. DemIndicatorBehaviour

- **UUID**: `ECUC:26582faa-e852-45d6-a68d-cf0cc279ca26`
- **参数名**: `DemIndicatorBehaviour`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_INDICATOR_BLINKING` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_BLINK_CONT` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_FAST_FLASH` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_SLOW_FLASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Behaviour of the linked indicator

############ 2. DemIndicatorFailureCycleSource

- **UUID**: `ECUC:9224f6ca-d10a-4b8d-9b76-da543ec42a3a`
- **参数名**: `DemIndicatorFailureCycleSource`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_FAILURE_CYCLE_EVENT` (来源: AUTOSAR_ECUC)
  - `DEM_FAILURE_CYCLE_INDICATOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, which failure cycle is used for the WarningIndicatorOnCriteria handling.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. DemIndicatorFailureCycleRef

- **UUID**: `ECUC:3fc5415b-ef0e-4616-84af-ac48fb00b4e7`
- **引用名**: `DemIndicatorFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the indicator controlled by the according event used for the WarningIndicatorOnCriteria.

############ 2. DemIndicatorHealingCycleRef

- **UUID**: `ECUC:01818b0e-d069-473b-bb27-f067edb1f453`
- **引用名**: `DemIndicatorHealingCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of healing cycle for the indicator controlled by the according event used for the WarningIndicatorOffCriteria.

############ 3. DemIndicatorRef

- **UUID**: `ECUC:328aa173-bf87-415a-a94c-8b48686226a6`
- **引用名**: `DemIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used indicator.

######### 6. DemDebounceAlgorithmClass

**容器属性**:

- **UUID**: `ECUC:98a5d79e-8975-48e4-bbc8-a174596e2dbb`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDebounceAlgorithmClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDebounceCounterBased**
  - UUID: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
  - 描述: This container contains the configuration (parameters) for counter based debouncing.
- **DemDebounceMonitorInternal**
  - UUID: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
  - 描述: This container contains the configuration (parameters) for monitor internal debouncing.
- **DemCallbackGetFDC**
  - UUID: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
  - 描述: The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.
- **DemDebounceTimeBase**
  - UUID: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
  - 描述: This container contains the configuration (parameters) for time based debouncing.

**容器描述**:

Debounce algorithm class: counter based, time based, or monitor internal.

####### 6. DemDebounceCounterBased

**容器属性**:

- **UUID**: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceCounterBased`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for counter based debouncing.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. DemDebounceCounterDecrementStepSize

- **UUID**: `ECUC:07c58e53-a31c-421d-a6eb-910f2d3cd2d8`
- **参数名**: `DemDebounceCounterDecrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32768]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for decrementation of the internal debounce counter (PREPASSED).

########## 2. DemDebounceCounterFailedThreshold

- **UUID**: `ECUC:aff278be-3537-4099-8858-212582caf8f2`
- **参数名**: `DemDebounceCounterFailedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the failed status.

########## 3. DemDebounceCounterIncrementStepSize

- **UUID**: `ECUC:7cde5c15-c87f-4eed-b0f5-38313a32efe2`
- **参数名**: `DemDebounceCounterIncrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for incrementation of the internal debounce counter (PREFAILED).

########## 4. DemDebounceCounterJumpDownValue

- **UUID**: `ECUC:7baa87e8-87d0-45bb-9937-a8c3a4ebc2b6`
- **参数名**: `DemDebounceCounterJumpDownValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Down value of the internal debounce counter which is taken as initialization value for the counter when the respective step-down occurs.

########## 5. DemDebounceCounterJumpUpValue

- **UUID**: `ECUC:86693810-0a0a-4927-91ae-5d3723761724`
- **参数名**: `DemDebounceCounterJumpUpValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Up value of the internal debounce counter which is taken as initialization value for the counter when the respective step-up occurs.

########## 6. DemDebounceCounterPassedThreshold

- **UUID**: `ECUC:2c4aba4f-9fc9-4572-a226-9562516ffac3`
- **参数名**: `DemDebounceCounterPassedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..-1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the passed status.

######### BOOLEAN 类型参数

########## 1. DemDebounceCounterJumpDown

- **UUID**: `ECUC:aa2d713a-ec74-4c4c-93a9-bd83b0c107b8`
- **参数名**: `DemDebounceCounterJumpDown`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Down.

########## 2. DemDebounceCounterJumpUp

- **UUID**: `ECUC:6f82b9d4-c3e1-4f00-8196-1f85c7be1562`
- **参数名**: `DemDebounceCounterJumpUp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Up.

########## 3. DemDebounceCounterStorage

- **UUID**: `ECUC:33babe76-7e6b-44dc-8233-e33933cf87e7`
- **参数名**: `DemDebounceCounterStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to store the debounce counter value non-volatile or not.

######### ENUMERATION 类型参数

########## 1. DemDebounceBehavior

- **UUID**: `ECUC:6fd7cbcb-976b-46c5-bd9c-2ac97686f52d`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will behave, if a related enable condition is not fulfilled or ControlDTCSetting of the related event is disabled.

####### 7. DemDebounceMonitorInternal

**容器属性**:

- **UUID**: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceMonitorInternal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for monitor internal debouncing.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

####### 8. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

####### 9. DemDebounceTimeBase

**容器属性**:

- **UUID**: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceTimeBase`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for time based debouncing.

######## 参数配置

此容器包含 **3** 个参数：

######### FLOAT 类型参数

########## 1. DemDebounceTimeFailedThreshold

- **UUID**: `ECUC:4579dd3e-fa1d-404c-a743-9b236697409b`
- **参数名**: `DemDebounceTimeFailedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Failed" qualification.

########## 2. DemDebounceTimePassedThreshold

- **UUID**: `ECUC:e3952bac-0313-43a6-ac7c-19204e3a2662`
- **参数名**: `DemDebounceTimePassedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Passed" qualification.

######### ENUMERATION 类型参数

########## 1. DemDebounceBehavior

- **UUID**: `ECUC:79236e41-97f0-418c-b2f2-241d6595589b`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will

####### 10. DemIndicatorAttribute

**容器属性**:

- **UUID**: `ECUC:38466ee0-81d6-4eb5-84ea-278631d94b99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemIndicatorAttribute`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the event specific configuration of Indicators.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DemIndicatorFailureCycleCounterThreshold

- **UUID**: `ECUC:bc2a7554-29fe-4a08-a8a8-57087833e55c`
- **参数名**: `DemIndicatorFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the WarningIndicatorOnCriteria.

########## 2. DemIndicatorHealingCycleCounterThreshold

- **UUID**: `ECUC:4248526d-57f1-4519-bb2d-400a541280f5`
- **参数名**: `DemIndicatorHealingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of healing cycles for the WarningIndicatorOffCriteria.

######### ENUMERATION 类型参数

########## 1. DemIndicatorBehaviour

- **UUID**: `ECUC:26582faa-e852-45d6-a68d-cf0cc279ca26`
- **参数名**: `DemIndicatorBehaviour`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_INDICATOR_BLINKING` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_BLINK_CONT` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_FAST_FLASH` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_SLOW_FLASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Behaviour of the linked indicator

########## 2. DemIndicatorFailureCycleSource

- **UUID**: `ECUC:9224f6ca-d10a-4b8d-9b76-da543ec42a3a`
- **参数名**: `DemIndicatorFailureCycleSource`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_FAILURE_CYCLE_EVENT` (来源: AUTOSAR_ECUC)
  - `DEM_FAILURE_CYCLE_INDICATOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, which failure cycle is used for the WarningIndicatorOnCriteria handling.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. DemIndicatorFailureCycleRef

- **UUID**: `ECUC:3fc5415b-ef0e-4616-84af-ac48fb00b4e7`
- **引用名**: `DemIndicatorFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the indicator controlled by the according event used for the WarningIndicatorOnCriteria.

########## 2. DemIndicatorHealingCycleRef

- **UUID**: `ECUC:01818b0e-d069-473b-bb27-f067edb1f453`
- **引用名**: `DemIndicatorHealingCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of healing cycle for the indicator controlled by the according event used for the WarningIndicatorOffCriteria.

########## 3. DemIndicatorRef

- **UUID**: `ECUC:328aa173-bf87-415a-a94c-8b48686226a6`
- **引用名**: `DemIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used indicator.

####### 11. DemDebounceAlgorithmClass

**容器属性**:

- **UUID**: `ECUC:98a5d79e-8975-48e4-bbc8-a174596e2dbb`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDebounceAlgorithmClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDebounceCounterBased**
  - UUID: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
  - 描述: This container contains the configuration (parameters) for counter based debouncing.
- **DemDebounceMonitorInternal**
  - UUID: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
  - 描述: This container contains the configuration (parameters) for monitor internal debouncing.
- **DemCallbackGetFDC**
  - UUID: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
  - 描述: The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.
- **DemDebounceTimeBase**
  - UUID: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
  - 描述: This container contains the configuration (parameters) for time based debouncing.

**容器描述**:

Debounce algorithm class: counter based, time based, or monitor internal.

##### 6. DemCallbackClearEventAllowed

**容器属性**:

- **UUID**: `ECUC:81830ba7-c118-43dd-baf9-d89bcec71b90`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackClearEventAllowed`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates that the Dem has access to a "ClearEventAllowed" callback.

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. DemClearEventAllowedBehavior

- **UUID**: `ECUC:7411934a-7525-44dd-b02b-e0681e08b4c2`
- **参数名**: `DemClearEventAllowedBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DEM_NO_STATUS_BYTE_CHANGE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_NO_STATUS_BYTE_CHANGE` (来源: AUTOSAR_ECUC)
  - `DEM_ONLY_THIS_CYCLE_AND_READINESS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the resulting UDS status byte for the related event, which must not be cleared according to the ClearEventAllowed callback.

####### FUNCTION-NAME 类型参数

######## 1. DemCallbackClearEventAllowedFnc

- **UUID**: `ECUC:f57a2f55-06b0-438d-9a41-d2626089d446`
- **参数名**: `DemCallbackClearEventAllowedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "ClearEventAllowed".

##### 7. DemCallbackEventDataChanged

**容器属性**:

- **UUID**: `ECUC:48673ef9-0ee2-44e2-a4da-c56610dd6792`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackEventDataChanged`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates that the Dem has access to an "EventDataChanged" callback.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DemCallbackEventDataChangedFnc

- **UUID**: `ECUC:620931a3-319d-4e30-8896-df7694afa222`
- **参数名**: `DemCallbackEventDataChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "EventDataChanged"

##### 8. DemCallbackEventStatusChanged

**容器属性**:

- **UUID**: `ECUC:505d125c-04db-4d5e-92f4-d73e664f7174`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackEventStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to an "EventStatusChanged" callback, which the Dem will call to notify other components about the change in the status of an event.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DemCallbackEventStatusChangedFnc

- **UUID**: `ECUC:0a1de324-a6d1-4b23-ba12-631c41dbd8cc`
- **参数名**: `DemCallbackEventStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "EventStatusChanged"

##### 9. DemCallbackInitMForE

**容器属性**:

- **UUID**: `ECUC:11b1adbe-fd9a-49a2-a43e-01bed9346c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackInitMForE`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to an "InitMonitorForEvent" callback, which the Dem will call to initialize a monitor.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DemCallbackInitMForEFnc

- **UUID**: `ECUC:46ba0efd-c45e-4400-a6f9-0441ffe9df5b`
- **参数名**: `DemCallbackInitMForEFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "InitMonitorForEvent".

##### 10. DemEventClass

**容器属性**:

- **UUID**: `ECUC:5127af6d-f63f-46f2-9279-2ddfa6850162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemEventClass`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for EventClass

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. DemAgingCycleCounterThreshold

- **UUID**: `ECUC:c005de82-ee68-46ba-8069-ed248a20b11b`
- **参数名**: `DemAgingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of aging cycles needed to unlearn/delete the event.

######## 2. DemEventFailureCycleCounterThreshold

- **UUID**: `ECUC:6506cb9d-36d0-4f67-89f7-266b9f4cbc3a`
- **参数名**: `DemEventFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the event based fault confirmation.

######## 3. DemEventMemoryEntryFdcThresholdStorageValue

- **UUID**: `ECUC:8dd83213-1223-4eff-ac82-a316ef9d215d`
- **参数名**: `DemEventMemoryEntryFdcThresholdStorageValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold to allocate an event memory entry and to capture the Freeze Frame.

######## 4. DemEventPriority

- **UUID**: `ECUC:3ef7c809-cd40-4824-b0cd-da79a594c75d`
- **参数名**: `DemEventPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..256]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of the event, in view of full event buffer.

####### BOOLEAN 类型参数

######## 1. DemAgingAllowed

- **UUID**: `ECUC:13bf7d23-8cc0-4b57-8911-92658b0cb328`
- **参数名**: `DemAgingAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to allow aging/unlearning of the event or not.

######## 2. DemConsiderPtoStatus

- **UUID**: `ECUC:ade2dfbd-edda-4dba-82cf-889cca141ba3`
- **参数名**: `DemConsiderPtoStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is TRUE, when the event is affected by the Dem PTO handling.

######## 3. DemFFPrestorageSupported

- **UUID**: `ECUC:998abc59-21d6-4f48-98d2-f84c83c31b9e`
- **参数名**: `DemFFPrestorageSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter is set to true, then the Prestorage of FreezeFrames is supported by the assigned event. This parameter is useful to calculate the buffer size.

####### ENUMERATION 类型参数

######## 1. DemEventDestination

- **UUID**: `ECUC:3d77d2e5-cd5d-463c-a083-aca98fec267d`
- **参数名**: `DemEventDestination`
- **数据类型**: ENUMERATION
- **多重性**: [0..4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTC_ORIGIN_MIRROR_MEMORY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_ORIGIN_PRIMARY_MEMORY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_ORIGIN_SECONDARY_MEMORY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The event destination assigns events to none, one or multiple origins.

######## 2. DemEventOBDReadinessGroup

- **UUID**: `ECUC:bd389f92-bcb8-4921-acc3-d96cb78371b6`
- **参数名**: `DemEventOBDReadinessGroup`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_OBD_RDY_AC` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_BOOSTPR` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_CAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_CMPRCMPT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_EGSENS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_ERG` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_EVAP` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_FLSYS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_FLSYS_NONCONT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_HCCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_HTCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_MISF` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_NONE` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_NOXCAT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_O2SENS` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_O2SENSHT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_PMFLT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_RDY_SECAIR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the Event OBD Readiness group for PID $01 and PID $41 computation.

######## 3. DemEventSignificance

- **UUID**: `ECUC:73be02e4-de26-4bf9-87d8-8f6d3b15f532`
- **参数名**: `DemEventSignificance`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_EVENT_SIGNIFICANCE_FAULT` (来源: AUTOSAR_ECUC)
  - `DEM_EVENT_SIGNIFICANCE_OCCURRENCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Significance of the event, which indicates additional information concerning fault classification and resolution.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. DemEnableConditionGroupRef

- **UUID**: `ECUC:6953a02d-6999-4d84-8c1d-daede62dfc77`
- **引用名**: `DemEnableConditionGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEnableConditionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemEnableConditionGroup`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References an enable condition group.

######## 2. DemEventFailureCycleRef

- **UUID**: `ECUC:2f31cb98-c767-407b-82e7-fe6fcdf86076`
- **引用名**: `DemEventFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the event based fault confirmation.

######## 3. DemOperationCycleRef

- **UUID**: `ECUC:fc68bc01-d147-4b6d-95a2-36cfa577cacf`
- **引用名**: `DemOperationCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of operation cycle for the event (e.g. power cycle, driving cycle, ...)

######## 4. DemStorageConditionGroupRef

- **UUID**: `ECUC:92052d72-8af4-4f08-9d1f-2a901238caf9`
- **引用名**: `DemStorageConditionGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemStorageConditionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemStorageConditionGroup`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References a storage condition group.

####### CHOICE-REFERENCE 类型引用

######## 1. DemAgingCycleRef

- **UUID**: `ECUC:2c17db4a-8035-4b38-bca3-093e53f7d34d`
- **引用名**: `DemAgingCycleRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC V1.0.0
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemAgingCycle`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the cycle which is triggering the aging of the event. This can either be the same as the operation cycle of the event, or a separate aging cycle reported via API Dem_SetAgingCycleState. If external aging is configured (refer to DemAgingCycleCounterProcessing), this parameter is not used.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. DemDebounceCounterBased

**容器属性**:

- **UUID**: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceCounterBased`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for counter based debouncing.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. DemDebounceCounterDecrementStepSize

- **UUID**: `ECUC:07c58e53-a31c-421d-a6eb-910f2d3cd2d8`
- **参数名**: `DemDebounceCounterDecrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32768]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for decrementation of the internal debounce counter (PREPASSED).

########## 2. DemDebounceCounterFailedThreshold

- **UUID**: `ECUC:aff278be-3537-4099-8858-212582caf8f2`
- **参数名**: `DemDebounceCounterFailedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the failed status.

########## 3. DemDebounceCounterIncrementStepSize

- **UUID**: `ECUC:7cde5c15-c87f-4eed-b0f5-38313a32efe2`
- **参数名**: `DemDebounceCounterIncrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for incrementation of the internal debounce counter (PREFAILED).

########## 4. DemDebounceCounterJumpDownValue

- **UUID**: `ECUC:7baa87e8-87d0-45bb-9937-a8c3a4ebc2b6`
- **参数名**: `DemDebounceCounterJumpDownValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Down value of the internal debounce counter which is taken as initialization value for the counter when the respective step-down occurs.

########## 5. DemDebounceCounterJumpUpValue

- **UUID**: `ECUC:86693810-0a0a-4927-91ae-5d3723761724`
- **参数名**: `DemDebounceCounterJumpUpValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Up value of the internal debounce counter which is taken as initialization value for the counter when the respective step-up occurs.

########## 6. DemDebounceCounterPassedThreshold

- **UUID**: `ECUC:2c4aba4f-9fc9-4572-a226-9562516ffac3`
- **参数名**: `DemDebounceCounterPassedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..-1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the passed status.

######### BOOLEAN 类型参数

########## 1. DemDebounceCounterJumpDown

- **UUID**: `ECUC:aa2d713a-ec74-4c4c-93a9-bd83b0c107b8`
- **参数名**: `DemDebounceCounterJumpDown`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Down.

########## 2. DemDebounceCounterJumpUp

- **UUID**: `ECUC:6f82b9d4-c3e1-4f00-8196-1f85c7be1562`
- **参数名**: `DemDebounceCounterJumpUp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Up.

########## 3. DemDebounceCounterStorage

- **UUID**: `ECUC:33babe76-7e6b-44dc-8233-e33933cf87e7`
- **参数名**: `DemDebounceCounterStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to store the debounce counter value non-volatile or not.

######### ENUMERATION 类型参数

########## 1. DemDebounceBehavior

- **UUID**: `ECUC:6fd7cbcb-976b-46c5-bd9c-2ac97686f52d`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will behave, if a related enable condition is not fulfilled or ControlDTCSetting of the related event is disabled.

####### 2. DemDebounceMonitorInternal

**容器属性**:

- **UUID**: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceMonitorInternal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for monitor internal debouncing.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

####### 3. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

####### 4. DemDebounceTimeBase

**容器属性**:

- **UUID**: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceTimeBase`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for time based debouncing.

######## 参数配置

此容器包含 **3** 个参数：

######### FLOAT 类型参数

########## 1. DemDebounceTimeFailedThreshold

- **UUID**: `ECUC:4579dd3e-fa1d-404c-a743-9b236697409b`
- **参数名**: `DemDebounceTimeFailedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Failed" qualification.

########## 2. DemDebounceTimePassedThreshold

- **UUID**: `ECUC:e3952bac-0313-43a6-ac7c-19204e3a2662`
- **参数名**: `DemDebounceTimePassedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Passed" qualification.

######### ENUMERATION 类型参数

########## 1. DemDebounceBehavior

- **UUID**: `ECUC:79236e41-97f0-418c-b2f2-241d6595589b`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will

####### 5. DemIndicatorAttribute

**容器属性**:

- **UUID**: `ECUC:38466ee0-81d6-4eb5-84ea-278631d94b99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemIndicatorAttribute`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the event specific configuration of Indicators.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DemIndicatorFailureCycleCounterThreshold

- **UUID**: `ECUC:bc2a7554-29fe-4a08-a8a8-57087833e55c`
- **参数名**: `DemIndicatorFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the WarningIndicatorOnCriteria.

########## 2. DemIndicatorHealingCycleCounterThreshold

- **UUID**: `ECUC:4248526d-57f1-4519-bb2d-400a541280f5`
- **参数名**: `DemIndicatorHealingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of healing cycles for the WarningIndicatorOffCriteria.

######### ENUMERATION 类型参数

########## 1. DemIndicatorBehaviour

- **UUID**: `ECUC:26582faa-e852-45d6-a68d-cf0cc279ca26`
- **参数名**: `DemIndicatorBehaviour`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_INDICATOR_BLINKING` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_BLINK_CONT` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_FAST_FLASH` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_SLOW_FLASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Behaviour of the linked indicator

########## 2. DemIndicatorFailureCycleSource

- **UUID**: `ECUC:9224f6ca-d10a-4b8d-9b76-da543ec42a3a`
- **参数名**: `DemIndicatorFailureCycleSource`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_FAILURE_CYCLE_EVENT` (来源: AUTOSAR_ECUC)
  - `DEM_FAILURE_CYCLE_INDICATOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, which failure cycle is used for the WarningIndicatorOnCriteria handling.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. DemIndicatorFailureCycleRef

- **UUID**: `ECUC:3fc5415b-ef0e-4616-84af-ac48fb00b4e7`
- **引用名**: `DemIndicatorFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the indicator controlled by the according event used for the WarningIndicatorOnCriteria.

########## 2. DemIndicatorHealingCycleRef

- **UUID**: `ECUC:01818b0e-d069-473b-bb27-f067edb1f453`
- **引用名**: `DemIndicatorHealingCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of healing cycle for the indicator controlled by the according event used for the WarningIndicatorOffCriteria.

########## 3. DemIndicatorRef

- **UUID**: `ECUC:328aa173-bf87-415a-a94c-8b48686226a6`
- **引用名**: `DemIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used indicator.

####### 6. DemDebounceAlgorithmClass

**容器属性**:

- **UUID**: `ECUC:98a5d79e-8975-48e4-bbc8-a174596e2dbb`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDebounceAlgorithmClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDebounceCounterBased**
  - UUID: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
  - 描述: This container contains the configuration (parameters) for counter based debouncing.
- **DemDebounceMonitorInternal**
  - UUID: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
  - 描述: This container contains the configuration (parameters) for monitor internal debouncing.
- **DemCallbackGetFDC**
  - UUID: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
  - 描述: The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.
- **DemDebounceTimeBase**
  - UUID: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
  - 描述: This container contains the configuration (parameters) for time based debouncing.

**容器描述**:

Debounce algorithm class: counter based, time based, or monitor internal.

##### 11. DemDebounceCounterBased

**容器属性**:

- **UUID**: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceCounterBased`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for counter based debouncing.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. DemDebounceCounterDecrementStepSize

- **UUID**: `ECUC:07c58e53-a31c-421d-a6eb-910f2d3cd2d8`
- **参数名**: `DemDebounceCounterDecrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32768]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for decrementation of the internal debounce counter (PREPASSED).

######## 2. DemDebounceCounterFailedThreshold

- **UUID**: `ECUC:aff278be-3537-4099-8858-212582caf8f2`
- **参数名**: `DemDebounceCounterFailedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the failed status.

######## 3. DemDebounceCounterIncrementStepSize

- **UUID**: `ECUC:7cde5c15-c87f-4eed-b0f5-38313a32efe2`
- **参数名**: `DemDebounceCounterIncrementStepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the step size for incrementation of the internal debounce counter (PREFAILED).

######## 4. DemDebounceCounterJumpDownValue

- **UUID**: `ECUC:7baa87e8-87d0-45bb-9937-a8c3a4ebc2b6`
- **参数名**: `DemDebounceCounterJumpDownValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Down value of the internal debounce counter which is taken as initialization value for the counter when the respective step-down occurs.

######## 5. DemDebounceCounterJumpUpValue

- **UUID**: `ECUC:86693810-0a0a-4927-91ae-5d3723761724`
- **参数名**: `DemDebounceCounterJumpUpValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [-32768..32767]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Jump-Up value of the internal debounce counter which is taken as initialization value for the counter when the respective step-up occurs.

######## 6. DemDebounceCounterPassedThreshold

- **UUID**: `ECUC:2c4aba4f-9fc9-4572-a226-9562516ffac3`
- **参数名**: `DemDebounceCounterPassedThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [-32768..-1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value of the internal debounce counter, which indicates the passed status.

####### BOOLEAN 类型参数

######## 1. DemDebounceCounterJumpDown

- **UUID**: `ECUC:aa2d713a-ec74-4c4c-93a9-bd83b0c107b8`
- **参数名**: `DemDebounceCounterJumpDown`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Down.

######## 2. DemDebounceCounterJumpUp

- **UUID**: `ECUC:6f82b9d4-c3e1-4f00-8196-1f85c7be1562`
- **参数名**: `DemDebounceCounterJumpUp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for the activation of Jump-Up.

######## 3. DemDebounceCounterStorage

- **UUID**: `ECUC:33babe76-7e6b-44dc-8233-e33933cf87e7`
- **参数名**: `DemDebounceCounterStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to store the debounce counter value non-volatile or not.

####### ENUMERATION 类型参数

######## 1. DemDebounceBehavior

- **UUID**: `ECUC:6fd7cbcb-976b-46c5-bd9c-2ac97686f52d`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will behave, if a related enable condition is not fulfilled or ControlDTCSetting of the related event is disabled.

##### 12. DemDebounceMonitorInternal

**容器属性**:

- **UUID**: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceMonitorInternal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for monitor internal debouncing.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

##### 13. DemCallbackGetFDC

**容器属性**:

- **UUID**: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackGetFDC`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DemCallbackGetFDCFnc

- **UUID**: `ECUC:fc99fc77-96af-446e-9167-2db5d56b6f50`
- **参数名**: `DemCallbackGetFDCFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "GetFaultDetectionCounter".

##### 14. DemDebounceTimeBase

**容器属性**:

- **UUID**: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDebounceTimeBase`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for time based debouncing.

###### 参数配置

此容器包含 **3** 个参数：

####### FLOAT 类型参数

######## 1. DemDebounceTimeFailedThreshold

- **UUID**: `ECUC:4579dd3e-fa1d-404c-a743-9b236697409b`
- **参数名**: `DemDebounceTimeFailedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Failed" qualification.

######## 2. DemDebounceTimePassedThreshold

- **UUID**: `ECUC:e3952bac-0313-43a6-ac7c-19204e3a2662`
- **参数名**: `DemDebounceTimePassedThreshold`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time out duration for "Event Passed" qualification.

####### ENUMERATION 类型参数

######## 1. DemDebounceBehavior

- **UUID**: `ECUC:79236e41-97f0-418c-b2f2-241d6595589b`
- **参数名**: `DemDebounceBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DEBOUNCE_FREEZE` (来源: AUTOSAR_ECUC)
  - `DEM_DEBOUNCE_RESET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines how the event debounce algorithm will

##### 15. DemIndicatorAttribute

**容器属性**:

- **UUID**: `ECUC:38466ee0-81d6-4eb5-84ea-278631d94b99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemIndicatorAttribute`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the event specific configuration of Indicators.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. DemIndicatorFailureCycleCounterThreshold

- **UUID**: `ECUC:bc2a7554-29fe-4a08-a8a8-57087833e55c`
- **参数名**: `DemIndicatorFailureCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of failure cycles for the WarningIndicatorOnCriteria.

######## 2. DemIndicatorHealingCycleCounterThreshold

- **UUID**: `ECUC:4248526d-57f1-4519-bb2d-400a541280f5`
- **参数名**: `DemIndicatorHealingCycleCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of healing cycles for the WarningIndicatorOffCriteria.

####### ENUMERATION 类型参数

######## 1. DemIndicatorBehaviour

- **UUID**: `ECUC:26582faa-e852-45d6-a68d-cf0cc279ca26`
- **参数名**: `DemIndicatorBehaviour`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_INDICATOR_BLINKING` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_BLINK_CONT` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_FAST_FLASH` (来源: AUTOSAR_ECUC)
  - `DEM_INDICATOR_SLOW_FLASH` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Behaviour of the linked indicator

######## 2. DemIndicatorFailureCycleSource

- **UUID**: `ECUC:9224f6ca-d10a-4b8d-9b76-da543ec42a3a`
- **参数名**: `DemIndicatorFailureCycleSource`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_FAILURE_CYCLE_EVENT` (来源: AUTOSAR_ECUC)
  - `DEM_FAILURE_CYCLE_INDICATOR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines, which failure cycle is used for the WarningIndicatorOnCriteria handling.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. DemIndicatorFailureCycleRef

- **UUID**: `ECUC:3fc5415b-ef0e-4616-84af-ac48fb00b4e7`
- **引用名**: `DemIndicatorFailureCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of failure cycle for the indicator controlled by the according event used for the WarningIndicatorOnCriteria.

######## 2. DemIndicatorHealingCycleRef

- **UUID**: `ECUC:01818b0e-d069-473b-bb27-f067edb1f453`
- **引用名**: `DemIndicatorHealingCycleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemOperationCycle`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemOperationCycle`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Kind of healing cycle for the indicator controlled by the according event used for the WarningIndicatorOffCriteria.

######## 3. DemIndicatorRef

- **UUID**: `ECUC:328aa173-bf87-415a-a94c-8b48686226a6`
- **引用名**: `DemIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used indicator.

##### 16. DemJ1939NodeAddress

**容器属性**:

- **UUID**: `ECUC:27441308-61a5-44f9-8352-4d8afd5c2f68`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemJ1939NodeAddress`
- **多重性**: [0..255]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

Contains the parameters for the support of a logical J1939 node (identified by an ECU address).

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. DemJ1939NmNodeRef

- **UUID**: `ECUC:a36d170a-9faa-439d-a951-d2bd5c8a6004`
- **引用名**: `DemJ1939NmNodeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..255]
- **目标**: `J1939NmNode`
- **完整路径**: `/AUTOSAR/EcucDefs/J1939Nm/J1939NmConfigSet/J1939NmNode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the corresponding J1939Nm node.

##### 17. DemPidClass

**容器属性**:

- **UUID**: `ECUC:44faa8c1-9430-4ce8-b572-a9033e48bdd5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemPidClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the different PIDs for the single global OBD relevant freeze frame class. It is assembled out of one or several data elements.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DemPidIdentifier

- **UUID**: `ECUC:18337b6d-c988-4e65-9896-c0814ac35f45`
- **参数名**: `DemPidIdentifier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: identifier of the PID

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DemPidDataElement

**容器属性**:

- **UUID**: `ECUC:08dbe78d-7b7b-4510-bfa9-3ce041b597d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemPidDataElement`
- **多重性**: [1..255]
- **多配置容器**: false

**容器描述**:

This container contains the different data elements contained in the specific PID.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DemPidDataElementClassRef

- **UUID**: `ECUC:e55a5a69-f687-4fd6-9b48-17ca02603d1d`
- **引用名**: `DemPidDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

##### 18. DemPidDataElement

**容器属性**:

- **UUID**: `ECUC:08dbe78d-7b7b-4510-bfa9-3ce041b597d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemPidDataElement`
- **多重性**: [1..255]
- **多配置容器**: false

**容器描述**:

This container contains the different data elements contained in the specific PID.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. DemPidDataElementClassRef

- **UUID**: `ECUC:e55a5a69-f687-4fd6-9b48-17ca02603d1d`
- **引用名**: `DemPidDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

##### 19. DemGeneral

**容器属性**:

- **UUID**: `ECUC:6ca017f1-d32b-49c2-9624-9c1a628401c2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the BSW Dem

###### 参数配置

此容器包含 **43** 个参数：

####### INTEGER 类型参数

######## 1. DemBswErrorBufferSize

- **UUID**: `ECUC:6388fad6-ff27-41e9-bc9e-fa9d41faf0df`
- **参数名**: `DemBswErrorBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of elements in buffer for handling of BSW errors (ref. to Dem107).

######## 2. DemDtcStatusAvailabilityMask

- **UUID**: `ECUC:4a2afd78-57fb-4c89-a156-eae8fc5dcf37`
- **参数名**: `DemDtcStatusAvailabilityMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mask for the supported DTC status bits by the Dem. This mask is used by UDS service 0x19.

######## 3. DemImmediateNvStorageLimit

- **UUID**: `ECUC:8a2b8a2b-cffb-4401-8732-5de196039921`
- **参数名**: `DemImmediateNvStorageLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum number of occurrences, a specific event memory entry is allowed, to be stored in NVRAM immediately (refer to DemImmediateNvStorage).

######## 4. DemMaxNumberEventEntryMirror

- **UUID**: `ECUC:884c0df3-c917-44ef-adf6-a7d6f4638e20`
- **参数名**: `DemMaxNumberEventEntryMirror`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of events which can be stored in the mirror memory

######## 5. DemMaxNumberEventEntryPermanent

- **UUID**: `ECUC:cd9f6fcb-2134-4e0b-95fb-833dfca769bb`
- **参数名**: `DemMaxNumberEventEntryPermanent`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of events which can be stored in the permanent memory.

######## 6. DemMaxNumberEventEntryPrimary

- **UUID**: `ECUC:7fad4aa0-c3ce-4005-bb7f-dfb8b1a1172a`
- **参数名**: `DemMaxNumberEventEntryPrimary`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of events which can be stored in the primary memory

######## 7. DemMaxNumberEventEntrySecondary

- **UUID**: `ECUC:29cb4d86-003f-4d93-9e59-7105edd601f4`
- **参数名**: `DemMaxNumberEventEntrySecondary`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of events which can be stored in the secondary memory

######## 8. DemMaxNumberPrestoredFF

- **UUID**: `ECUC:a9b9d119-6ddf-46f6-93bd-5a990016cf70`
- **参数名**: `DemMaxNumberPrestoredFF`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number for prestored freeze frames.

####### BOOLEAN 类型参数

######## 1. DemAgingRequieresTestedCycle

- **UUID**: `ECUC:a3bd8297-60fe-44db-9094-40808a08b5f4`
- **参数名**: `DemAgingRequieresTestedCycle`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the aging cycle counter is processed every aging cycles or if only tested aging cycle are considered.

######## 2. DemDebounceCounterBasedSupport

- **UUID**: `ECUC:6d308999-a425-4904-aef3-a55c5e5db5e6`
- **参数名**: `DemDebounceCounterBasedSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether support for counter based debouncing is enabled or not.

######## 3. DemDebounceTimeBasedSupport

- **UUID**: `ECUC:306ac5ba-3e68-40cc-a248-b1bde6637e36`
- **参数名**: `DemDebounceTimeBasedSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether support for time based debouncing is enabled or not.

######## 4. DemDevErrorDetect

- **UUID**: `ECUC:21da3508-a0a5-4ecb-994e-b8378d8bcc8a`
- **参数名**: `DemDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the Development Error Detection and Notification.

######## 5. DemEnableConditionSupport

- **UUID**: `ECUC:a47fcf61-b9f1-4ad7-ac32-11a0b471653f`
- **参数名**: `DemEnableConditionSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether support for enable conditions is enabled or not.

######## 6. DemGeneralInterfaceSupport

- **UUID**: `ECUC:088bfcc2-3ffe-426c-9182-db21e7c3b259`
- **参数名**: `DemGeneralInterfaceSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The interfaces GeneralEvtInfo, GeneralCallbackEventDataChanged and GeneralCallbackEventStatusChange are provided if DemGeneralInterfaceSupport is equal to true.

######## 7. DemOperationCycleStatusStorage

- **UUID**: `ECUC:06baac28-6a64-46c0-b468-2b6e5f2571bc`
- **参数名**: `DemOperationCycleStatusStorage`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the operation cycle state is available over the power cycle (stored non-volatile) or not.

######## 8. DemPTOSupport

- **UUID**: `ECUC:40aaf4a3-811c-4ed4-b5ed-c364b32c4193`
- **参数名**: `DemPTOSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether PTO support (and therefore PID $1E support) is enabled or not.

######## 9. DemResetConfirmedBitOnOverflow

- **UUID**: `ECUC:af5bbe02-f227-411a-b071-9b9a5b48bf52`
- **参数名**: `DemResetConfirmedBitOnOverflow`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether the confirmed bit is reset or not while an event memory entry will be displaced.

######## 10. DemStatusBitStorageTestFailed

- **UUID**: `ECUC:b8232040-8309-438b-b16d-3bbf911191b0`
- **参数名**: `DemStatusBitStorageTestFailed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the permanent storage of the "TestFailed" status bits.

######## 11. DemStorageConditionSupport

- **UUID**: `ECUC:dd8247a4-4a28-4326-ad0d-8d23978fbcbf`
- **参数名**: `DemStorageConditionSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether support for storage conditions is enabled or not.

######## 12. DemTriggerDcmReports

- **UUID**: `ECUC:0b862943-7dc6-4a4e-9a7b-4b9cf27a0d19`
- **参数名**: `DemTriggerDcmReports`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the notification to the Diagnostic Communication Manager for ROE processing.

######## 13. DemTriggerDltReports

- **UUID**: `ECUC:1aae8fc4-5b22-4a6c-8744-a125dbf06efe`
- **参数名**: `DemTriggerDltReports`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the notification to the Diagnostic Log and Trace.

######## 14. DemTriggerFiMReports

- **UUID**: `ECUC:ffa4e7ab-5a53-4aab-89d5-faab430e6007`
- **参数名**: `DemTriggerFiMReports`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the notification to the Function Inhibition Manager.

######## 15. DemTriggerMonitorInitBeforeClearOk

- **UUID**: `ECUC:5fcadaa0-df21-4e86-ab87-636545aafe14`
- **参数名**: `DemTriggerMonitorInitBeforeClearOk`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the monitor re-initialization has to be triggered before or after the Dem module returns DEM_CLEAR_OK.

######## 16. DemVersionInfoApi

- **UUID**: `ECUC:2236d8b8-2712-47f4-9d0b-b77e5b5df6d7`
- **参数名**: `DemVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the version information API.

####### FLOAT 类型参数

######## 1. DemTaskTime

- **UUID**: `ECUC:2109a155-8685-4f62-9f8d-1df661889043`
- **参数名**: `DemTaskTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..0.1]
- **来源**: AUTOSAR_ECUC V1.0.0
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allow to configure the time for the periodic cyclic task. Please note: This configuration value shall be equal to the value in the Basic Software Scheduler configuration of the RTE module.

####### STRING 类型参数

######## 1. DemHeaderFileInclusion

- **UUID**: `ECUC:0d15ce1a-85f5-49a6-8e19-d6ef5c19fbf9`
- **参数名**: `DemHeaderFileInclusion`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 正则表达式: `[a-zA-Z0-9_]([a-zA-Z0-9\._])*`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the header file(s) to be included by the Dem module containing the used C-callback declarations.

####### ENUMERATION 类型参数

######## 1. DemAgingCycleCounterProcessing

- **UUID**: `ECUC:cf65f678-2be0-4cd4-91bb-8023cce9e2ff`
- **参数名**: `DemAgingCycleCounterProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_PROCESS_AGINGCTR_EXTERN` (来源: AUTOSAR_ECUC)
  - `DEM_PROCESS_AGINGCTR_INTERN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether the aging counter is calculated Dem-internally or provided via Dem_SetAgingCycleCounterValue.

######## 2. DemAvailabilitySupport

- **UUID**: `ECUC:04f071cf-22a9-4382-97a2-cecb921f771b`
- **参数名**: `DemAvailabilitySupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_EVENT_AVAILABILITY` (来源: AUTOSAR_ECUC)
  - `DEM_NO_AVAILABILITY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether support for availability is enabled or not.

######## 3. DemClearDTCBehavior

- **UUID**: `ECUC:e0481c61-58b6-42ce-af08-899ebe9c41d8`
- **参数名**: `DemClearDTCBehavior`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_CLRRESP_NONVOLATILE_FINISH` (来源: AUTOSAR_ECUC)
  - `DEM_CLRRESP_NONVOLATILE_TRIGGER` (来源: AUTOSAR_ECUC)
  - `DEM_CLRRESP_VOLATILE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the clearing process of diagnostic information for volatile and non-volatile memory and the positive response handling for the Dcm module.

######## 4. DemClearDTCLimitation

- **UUID**: `ECUC:27cbd13d-d1aa-4038-b93c-c83a0474cd1e`
- **参数名**: `DemClearDTCLimitation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DEM_ALL_SUPPORTED_DTCS`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_ALL_SUPPORTED_DTCS` (来源: AUTOSAR_ECUC)
  - `DEM_ONLY_CLEAR_ALL_DTCS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the supported Dem_<...>ClearDTC API scope.

######## 5. DemDataElementDefaultEndianness

- **UUID**: `ECUC:2c01e075-aad4-4de0-9d3e-801945176c2c`
- **参数名**: `DemDataElementDefaultEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the default endianness of the data belonging to a data element which is applicable if the DemExternalSRDataElementClass does not define a endianness.

######## 6. DemEventCombinationSupport

- **UUID**: `ECUC:f3fe6a87-b322-467a-aa77-e49d9ce66490`
- **参数名**: `DemEventCombinationSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_EVCOMB_DISABLED` (来源: AUTOSAR_ECUC)
  - `DEM_EVCOMB_TYPE1` (来源: AUTOSAR_ECUC)
  - `DEM_EVCOMB_TYPE2` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the type of event combination supported by the Dem.

######## 7. DemEventDisplacementStrategy

- **UUID**: `ECUC:6108bc87-5feb-439d-8100-cb20505e7e0e`
- **参数名**: `DemEventDisplacementStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DISPLACEMENT_FULL` (来源: AUTOSAR_ECUC)
  - `DEM_DISPLACEMENT_NONE` (来源: AUTOSAR_ECUC)
  - `DEM_DISPLACEMENT_PRIO_OCC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether support for event displacement is enabled or not, and which displacement strategy is followed.

######## 8. DemEventMemoryEntryStorageTrigger

- **UUID**: `ECUC:b074dc99-92e8-425c-bfa2-d900a2a78862`
- **参数名**: `DemEventMemoryEntryStorageTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DEM_STORAGE_ON_TEST_FAILED`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_STORAGE_ON_CONFIRMED` (来源: AUTOSAR_ECUC)
  - `DEM_STORAGE_ON_FDC_THRESHOLD` (来源: AUTOSAR_ECUC)
  - `DEM_STORAGE_ON_PENDING` (来源: AUTOSAR_ECUC)
  - `DEM_STORAGE_ON_TEST_FAILED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the primary trigger to allocate an event memory entry.

######## 9. DemExtendedDataCapture

- **UUID**: `ECUC:5e5bf7d4-5a8a-4bbf-aadd-d1072da3f2ed`
- **参数名**: `DemExtendedDataCapture`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_TRIGGER_EVENT_MEMORY_STORAGE` (来源: AUTOSAR_ECUC)
  - `DEM_TRIGGER_TESTFAILED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the point in time, when the extended data collection is done for the initial event memory entry.

######## 10. DemFreezeFrameCapture

- **UUID**: `ECUC:0cc73e66-4679-461b-929f-cd30f8ded7da`
- **参数名**: `DemFreezeFrameCapture`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_TRIGGER_EVENT_MEMORY_STORAGE` (来源: AUTOSAR_ECUC)
  - `DEM_TRIGGER_TESTFAILED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the point in time, when the freeze frame data collection is done for the initial event memory entry.

######## 11. DemOBDSupport

- **UUID**: `ECUC:8e668bd5-8855-4f56-a1b2-9dd2da07c076`
- **参数名**: `DemOBDSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_OBD_DEP_SEC_ECU` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_MASTER_ECU` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_NO_OBD_SUPPORT` (来源: AUTOSAR_ECUC)
  - `DEM_OBD_PRIMARY_ECU` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines OBD support and kind of OBD ECU.

######## 12. DemOccurrenceCounterProcessing

- **UUID**: `ECUC:ce89a944-4a2a-4473-ad59-f307a8e9103e`
- **参数名**: `DemOccurrenceCounterProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_PROCESS_OCCCTR_CDTC` (来源: AUTOSAR_ECUC)
  - `DEM_PROCESS_OCCCTR_TF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines the consideration of the fault confirmation process for the occurrence counter. For OBD and mixed systems (OBD/non OBD, refer to DemOBDSupport) configuration switch shall always set to DEM_PROCESS_OCCCTR_TF.

######## 13. DemOperationCycleProcessing

- **UUID**: `ECUC:c6300d57-88cb-4c33-b72e-18e346da8dfb`
- **参数名**: `DemOperationCycleProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DEM_PROCESS_OPCYC_STATE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_PROCESS_OPCYC_COUNTER` (来源: AUTOSAR_ECUC)
  - `DEM_PROCESS_OPCYC_STATE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether the operation cycles are triggered by DEM_CYCLE_STATE_START or collecting an external counter value, which results in respective state changes.

######## 14. DemStatusBitHandlingTestFailedSinceLastClear

- **UUID**: `ECUC:bcf344c1-e4b6-47b2-836b-93bda8616623`
- **参数名**: `DemStatusBitHandlingTestFailedSinceLastClear`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_STATUS_BIT_AGING_AND_DISPLACEMENT` (来源: AUTOSAR_ECUC)
  - `DEM_STATUS_BIT_NORMAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether the aging and displacement mechanism shall be applied to the "TestFailedSinceLastClear" status bits.

######## 15. DemSuppressionSupport

- **UUID**: `ECUC:b22c10e5-1781-4d5a-9320-781d8d6b2480`
- **参数名**: `DemSuppressionSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTC_SUPPRESSION` (来源: AUTOSAR_ECUC)
  - `DEM_EVENT_AND_DTC_SUPPRESSION` (来源: AUTOSAR_ECUC)
  - `DEM_EVENT_SUPPRESSION` (来源: AUTOSAR_ECUC)
  - `DEM_NO_SUPPRESSION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines, whether support for suppression is enabled or not.

######## 16. DemTypeOfDTCSupported

- **UUID**: `ECUC:2e118358-e52d-474d-95d0-6a4807a3bcbf`
- **参数名**: `DemTypeOfDTCSupported`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTC_TRANSLATION_ISO11992_4` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_TRANSLATION_ISO14229_1` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_TRANSLATION_ISO15031_6` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_TRANSLATION_SAEJ1939_73` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the format returned by Dem_DcmGetTranslationType and does not relate to/influence the supported Dem functionality.

######## 17. DemTypeOfFreezeFrameRecordNumeration

- **UUID**: `ECUC:3855ce15-b738-467e-a342-7ae2499366bd`
- **参数名**: `DemTypeOfFreezeFrameRecordNumeration`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_FF_RECNUM_CALCULATED` (来源: AUTOSAR_ECUC)
  - `DEM_FF_RECNUM_CONFIGURED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the type of assigning freeze frame record numbers for event-specific freeze frame records.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DemMILIndicatorRef

- **UUID**: `ECUC:32b33d8d-7755-49f6-8db4-6b12faef15fe`
- **引用名**: `DemMILIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the indicator representing the MIL.

###### 配置容器

本模块包含 **39** 个配置容器：

####### 1. DemAgingCycle

**容器属性**:

- **UUID**: `ECUC:25f625cb-f3db-4091-922d-c554992647c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAgingCycle`
- **多重性**: [0..256]
- **多配置容器**: false

**容器描述**:

Note that this container definition does not explicitly define a symbolic name parameter. Instead, the short name of the container will be used in the Ecu Configuration Description to specify the symbolic name of the aging cycle name. These aging cycles are reported via API Dem_SetAgingCycleState only.

####### 2. DemCallbackDTCStatusChanged

**容器属性**:

- **UUID**: `ECUC:101cdd27-4d18-467d-a6d0-d9561d5424e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackDTCStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback, which the Dem will call to notify other components about the change in the status of a DTC.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackDTCStatusChangedFnc

- **UUID**: `ECUC:f95f691b-c363-4c11-9b04-852adad46b90`
- **参数名**: `DemCallbackDTCStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "DTCStatusChanged".

####### 3. DemExternalCSDataElementClass

**容器属性**:

- **UUID**: `ECUC:731531ff-e865-4793-887a-8064686ae7d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemExternalCSDataElementClass`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for an external client/server based data element class.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DemDataElementDataSize

- **UUID**: `ECUC:a23991f9-25de-4d38-8aca-a06d784b6697`
- **参数名**: `DemDataElementDataSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the size of the data element in bytes.

######### BOOLEAN 类型参数

########## 1. DemDataElementUsePort

- **UUID**: `ECUC:9cf1ca4d-69eb-4ba4-bfbc-6e3c027526d2`
- **参数名**: `DemDataElementUsePort`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the parameter is set to True, a R-Port is generated, to obtain the data element (interface DataServices_<SyncDataElement>).

######### FUNCTION-NAME 类型参数

########## 1. DemDataElementReadFnc

- **UUID**: `ECUC:fa9c6503-853e-4f03-b603-dfee41f57709`
- **参数名**: `DemDataElementReadFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In case of DemDataElementUsePort is false, this parameter defines the prototype of the C function "ReadDataElement" used to get the according value.

####### 4. DemExternalSRDataElementClass

**容器属性**:

- **UUID**: `ECUC:8e6c8d7e-2a1f-44a9-a5cf-728b1478f58d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemExternalSRDataElementClass`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for an external sender/receiver based data element class. It defines, how the Dem can obtain the value of the data element from a SW-C, by using a sender/receiver port.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DemDataElementDataSize

- **UUID**: `ECUC:9d166994-cc93-44c6-9fa0-52f7bc28e02b`
- **参数名**: `DemDataElementDataSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the size of the data element in bits.

######### ENUMERATION 类型参数

########## 1. DemDataElementDataType

- **UUID**: `ECUC:25afee69-0327-4666-8baf-77218bb4a807`
- **参数名**: `DemDataElementDataType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Provide the implementation data type of data belonging to a external data.

########## 2. DemDataElementEndianness

- **UUID**: `ECUC:ccdad70a-e417-49cb-b2f5-ba55fd055f02`
- **参数名**: `DemDataElementEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the data belonging to an external data.

######## 配置容器

本模块包含 **11** 个配置容器：

######### 1. DemAlternativeDataInterface

**容器属性**:

- **UUID**: `ECUC:c494d1bc-6807-4116-868f-139fc9d4056c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataInterface`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of a VariableDataPrototoype in a DataInterface.

########## 引用关系

此容器包含 **2** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. DemDataElement

- **UUID**: `ECUC:a976f624-cf39-4827-bd93-dee061b141ee`
- **引用名**: `DemDataElement`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Alternative Diagnosis Representation for the data defined by the means of a VariableDataPrototoype in a DataInterface.

############ 2. DemPortInterfaceMapping

- **UUID**: `ECUC:2fa38569-4bc8-4f8a-be68-d40ed21fea34`
- **引用名**: `DemPortInterfaceMapping`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: PORT-INTERFACE-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to PortInterfaceMapping which defines the mapping rules.

######### 2. DemAlternativeDataProps

**容器属性**:

- **UUID**: `ECUC:3b554f3d-00a7-4269-b499-bed18222a6e6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataProps`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of ECU configuration parameters.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. DemDataTypeCategory

- **UUID**: `ECUC:4583a595-9cec-4832-a50a-8a7f8adb04c2`
- **参数名**: `DemDataTypeCategory`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `SCALE_LINEAR_AND_TEXTTABLE` (来源: AUTOSAR_ECUC)
  - `TEXTTABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data category of the alternative Diagnosis Representation.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DemLinearScale

**容器属性**:

- **UUID**: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemLinearScale`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.

############ 参数配置

此容器包含 **4** 个参数：

############# FLOAT 类型参数

############## 1. DemDiagnosisRepresentationDataLowerRange

- **UUID**: `ECUC:33ff4aeb-6e0d-4f56-bb9d-d9cbcf0b8a82`
- **参数名**: `DemDiagnosisRepresentationDataLowerRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower Range for this scale of the data in the alternative Diagnosis Representation.

############## 2. DemDiagnosisRepresentationDataOffset

- **UUID**: `ECUC:e493b157-9aa7-493c-a845-66d62947b562`
- **参数名**: `DemDiagnosisRepresentationDataOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data offset of the alternative Diagnosis Representation for this scale.

############## 3. DemDiagnosisRepresentationDataResolution

- **UUID**: `ECUC:1110fe8f-72d4-452e-9e82-1cae64436142`
- **参数名**: `DemDiagnosisRepresentationDataResolution`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data resolution of the alternative Diagnosis Representation for this scale.

############## 4. DemDiagnosisRepresentationDataUpperRange

- **UUID**: `ECUC:b594bd37-222e-4a99-8d02-458c91b9a1e8`
- **参数名**: `DemDiagnosisRepresentationDataUpperRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper Range for this scale of the data in the alternative Diagnosis Representation.

########### 2. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:d9d82ed7-7e85-ce90-e005-f83904bb6b90`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

############## 2. DemInternalDataValue

- **UUID**: `ECUC:642c2ec0-b782-d319-db3d-28112033f97e`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

######### 3. DemLinearScale

**容器属性**:

- **UUID**: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemLinearScale`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.

########## 参数配置

此容器包含 **4** 个参数：

########### FLOAT 类型参数

############ 1. DemDiagnosisRepresentationDataLowerRange

- **UUID**: `ECUC:33ff4aeb-6e0d-4f56-bb9d-d9cbcf0b8a82`
- **参数名**: `DemDiagnosisRepresentationDataLowerRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower Range for this scale of the data in the alternative Diagnosis Representation.

############ 2. DemDiagnosisRepresentationDataOffset

- **UUID**: `ECUC:e493b157-9aa7-493c-a845-66d62947b562`
- **参数名**: `DemDiagnosisRepresentationDataOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data offset of the alternative Diagnosis Representation for this scale.

############ 3. DemDiagnosisRepresentationDataResolution

- **UUID**: `ECUC:1110fe8f-72d4-452e-9e82-1cae64436142`
- **参数名**: `DemDiagnosisRepresentationDataResolution`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data resolution of the alternative Diagnosis Representation for this scale.

############ 4. DemDiagnosisRepresentationDataUpperRange

- **UUID**: `ECUC:b594bd37-222e-4a99-8d02-458c91b9a1e8`
- **参数名**: `DemDiagnosisRepresentationDataUpperRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper Range for this scale of the data in the alternative Diagnosis Representation.

######### 4. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:d9d82ed7-7e85-ce90-e005-f83904bb6b90`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

############ 2. DemInternalDataValue

- **UUID**: `ECUC:642c2ec0-b782-d319-db3d-28112033f97e`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

######### 5. DemAlternativeDataType

**容器属性**:

- **UUID**: `ECUC:f403e75d-f752-4e3d-aa66-4d086335d59f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataType`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of an ApplicationDataType.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. DemApplicationDataType

- **UUID**: `ECUC:438db0a6-b8c3-4e53-9e9f-fe7aa4530ed3`
- **引用名**: `DemApplicationDataType`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: APPLICATION-PRIMITIVE-DATA-TYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Alternative Diagnosis Representation for the data defined by the means of a ApplicationPrimitiveDataType of category VALUE or BOOLEAN.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:9286c6f8-7530-da64-d5d2-866fe5ce9a49`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

############## 2. DemInternalDataValue

- **UUID**: `ECUC:1cdac6e1-ae2d-deed-d109-b64801472837`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

######### 6. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:9286c6f8-7530-da64-d5d2-866fe5ce9a49`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

############ 2. DemInternalDataValue

- **UUID**: `ECUC:1cdac6e1-ae2d-deed-d109-b64801472837`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

######### 7. DemDataElementInstance

**容器属性**:

- **UUID**: `ECUC:1da3b6b3-d899-4105-96f5-eee7ed1ed32f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitive data in a port  where the data element is typed with an ApplicationPrimitveDataType or an ImplementationDataType.

########## 引用关系

此容器包含 **1** 个引用：

########### INSTANCE-REFERENCE 类型引用

############ 1. DemDataElementInstanceRef

- **UUID**: `ECUC:a420975a-5a17-48de-ad73-d7082549c962`
- **引用名**: `DemDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitive data which shall be read or written.

######### 8. DemSubElementInDataElementInstance

**容器属性**:

- **UUID**: `ECUC:5afd11aa-5406-45d4-b56a-6ea45ba3d010`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSubElementInDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ApplicationCompositeDataType.

########## 引用关系

此容器包含 **1** 个引用：

########### INSTANCE-REFERENCE 类型引用

############ 1. DemSubElementInDataElementInstanceRef

- **UUID**: `ECUC:6b0b0abb-b972-44f8-aae4-c32fcb78a982`
- **引用名**: `DemSubElementInDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port which shall be read or written.

######### 9. DemSubElementInImplDataElementInstance

**容器属性**:

- **UUID**: `ECUC:c8bd6556-b5be-4c93-9be9-37a70a4d8424`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSubElementInImplDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.

########## 引用关系

此容器包含 **1** 个引用：

########### INSTANCE-REFERENCE 类型引用

############ 1. DemSubElementInImplDataElementInstanceRef

- **UUID**: `ECUC:ad862330-1bb1-40f6-816f-bf8b49e5c159`
- **引用名**: `DemSubElementInImplDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE-ELEMENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port which shall be read or written.

######### 10. DemDiagnosisScaling

**容器属性**:

- **UUID**: `ECUC:1113d69e-4b70-4756-bea7-2f74de625fcf`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDiagnosisScaling`
- **多重性**: [0..1]

**容器选择**:

- **DemAlternativeDataInterface**
  - UUID: `ECUC:c494d1bc-6807-4116-868f-139fc9d4056c`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of a VariableDataPrototoype in a DataInterface.
- **DemAlternativeDataProps**
  - UUID: `ECUC:3b554f3d-00a7-4269-b499-bed18222a6e6`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of ECU configuration parameters.
- **DemLinearScale**
  - UUID: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
  - 描述: This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.
- **DemTextTableMapping**
  - UUID: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.
- **DemAlternativeDataType**
  - UUID: `ECUC:f403e75d-f752-4e3d-aa66-4d086335d59f`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of an ApplicationDataType.
- **DemTextTableMapping**
  - UUID: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation. Out if this the scaling between Diagnosis and ECU internal representation and vice versa can be calculated.

######### 11. DemSRDataElementClass

**容器属性**:

- **UUID**: `ECUC:cbfb18d6-1749-45e0-833d-34d9d30215d4`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemSRDataElementClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDataElementInstance**
  - UUID: `ECUC:1da3b6b3-d899-4105-96f5-eee7ed1ed32f`
  - 描述: Instance Reference to the primitive data in a port  where the data element is typed with an ApplicationPrimitveDataType or an ImplementationDataType.
- **DemSubElementInDataElementInstance**
  - UUID: `ECUC:5afd11aa-5406-45d4-b56a-6ea45ba3d010`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ApplicationCompositeDataType.
- **DemSubElementInImplDataElementInstance**
  - UUID: `ECUC:c8bd6556-b5be-4c93-9be9-37a70a4d8424`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.

**容器描述**:

This container defines the source of data in a provided port which shall be read for a external data element

####### 5. DemAlternativeDataInterface

**容器属性**:

- **UUID**: `ECUC:c494d1bc-6807-4116-868f-139fc9d4056c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataInterface`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of a VariableDataPrototoype in a DataInterface.

######## 引用关系

此容器包含 **2** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DemDataElement

- **UUID**: `ECUC:a976f624-cf39-4827-bd93-dee061b141ee`
- **引用名**: `DemDataElement`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Alternative Diagnosis Representation for the data defined by the means of a VariableDataPrototoype in a DataInterface.

########## 2. DemPortInterfaceMapping

- **UUID**: `ECUC:2fa38569-4bc8-4f8a-be68-d40ed21fea34`
- **引用名**: `DemPortInterfaceMapping`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: PORT-INTERFACE-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to PortInterfaceMapping which defines the mapping rules.

####### 6. DemAlternativeDataProps

**容器属性**:

- **UUID**: `ECUC:3b554f3d-00a7-4269-b499-bed18222a6e6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataProps`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of ECU configuration parameters.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. DemDataTypeCategory

- **UUID**: `ECUC:4583a595-9cec-4832-a50a-8a7f8adb04c2`
- **参数名**: `DemDataTypeCategory`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `SCALE_LINEAR_AND_TEXTTABLE` (来源: AUTOSAR_ECUC)
  - `TEXTTABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data category of the alternative Diagnosis Representation.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DemLinearScale

**容器属性**:

- **UUID**: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemLinearScale`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.

########## 参数配置

此容器包含 **4** 个参数：

########### FLOAT 类型参数

############ 1. DemDiagnosisRepresentationDataLowerRange

- **UUID**: `ECUC:33ff4aeb-6e0d-4f56-bb9d-d9cbcf0b8a82`
- **参数名**: `DemDiagnosisRepresentationDataLowerRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower Range for this scale of the data in the alternative Diagnosis Representation.

############ 2. DemDiagnosisRepresentationDataOffset

- **UUID**: `ECUC:e493b157-9aa7-493c-a845-66d62947b562`
- **参数名**: `DemDiagnosisRepresentationDataOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data offset of the alternative Diagnosis Representation for this scale.

############ 3. DemDiagnosisRepresentationDataResolution

- **UUID**: `ECUC:1110fe8f-72d4-452e-9e82-1cae64436142`
- **参数名**: `DemDiagnosisRepresentationDataResolution`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data resolution of the alternative Diagnosis Representation for this scale.

############ 4. DemDiagnosisRepresentationDataUpperRange

- **UUID**: `ECUC:b594bd37-222e-4a99-8d02-458c91b9a1e8`
- **参数名**: `DemDiagnosisRepresentationDataUpperRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper Range for this scale of the data in the alternative Diagnosis Representation.

######### 2. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:d9d82ed7-7e85-ce90-e005-f83904bb6b90`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

############ 2. DemInternalDataValue

- **UUID**: `ECUC:642c2ec0-b782-d319-db3d-28112033f97e`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

####### 7. DemLinearScale

**容器属性**:

- **UUID**: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemLinearScale`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.

######## 参数配置

此容器包含 **4** 个参数：

######### FLOAT 类型参数

########## 1. DemDiagnosisRepresentationDataLowerRange

- **UUID**: `ECUC:33ff4aeb-6e0d-4f56-bb9d-d9cbcf0b8a82`
- **参数名**: `DemDiagnosisRepresentationDataLowerRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower Range for this scale of the data in the alternative Diagnosis Representation.

########## 2. DemDiagnosisRepresentationDataOffset

- **UUID**: `ECUC:e493b157-9aa7-493c-a845-66d62947b562`
- **参数名**: `DemDiagnosisRepresentationDataOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data offset of the alternative Diagnosis Representation for this scale.

########## 3. DemDiagnosisRepresentationDataResolution

- **UUID**: `ECUC:1110fe8f-72d4-452e-9e82-1cae64436142`
- **参数名**: `DemDiagnosisRepresentationDataResolution`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data resolution of the alternative Diagnosis Representation for this scale.

########## 4. DemDiagnosisRepresentationDataUpperRange

- **UUID**: `ECUC:b594bd37-222e-4a99-8d02-458c91b9a1e8`
- **参数名**: `DemDiagnosisRepresentationDataUpperRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper Range for this scale of the data in the alternative Diagnosis Representation.

####### 8. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:d9d82ed7-7e85-ce90-e005-f83904bb6b90`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

########## 2. DemInternalDataValue

- **UUID**: `ECUC:642c2ec0-b782-d319-db3d-28112033f97e`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

####### 9. DemAlternativeDataType

**容器属性**:

- **UUID**: `ECUC:f403e75d-f752-4e3d-aa66-4d086335d59f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataType`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of an ApplicationDataType.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DemApplicationDataType

- **UUID**: `ECUC:438db0a6-b8c3-4e53-9e9f-fe7aa4530ed3`
- **引用名**: `DemApplicationDataType`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: APPLICATION-PRIMITIVE-DATA-TYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Alternative Diagnosis Representation for the data defined by the means of a ApplicationPrimitiveDataType of category VALUE or BOOLEAN.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:9286c6f8-7530-da64-d5d2-866fe5ce9a49`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

############ 2. DemInternalDataValue

- **UUID**: `ECUC:1cdac6e1-ae2d-deed-d109-b64801472837`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

####### 10. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:9286c6f8-7530-da64-d5d2-866fe5ce9a49`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

########## 2. DemInternalDataValue

- **UUID**: `ECUC:1cdac6e1-ae2d-deed-d109-b64801472837`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

####### 11. DemDataElementInstance

**容器属性**:

- **UUID**: `ECUC:1da3b6b3-d899-4105-96f5-eee7ed1ed32f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitive data in a port  where the data element is typed with an ApplicationPrimitveDataType or an ImplementationDataType.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. DemDataElementInstanceRef

- **UUID**: `ECUC:a420975a-5a17-48de-ad73-d7082549c962`
- **引用名**: `DemDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitive data which shall be read or written.

####### 12. DemSubElementInDataElementInstance

**容器属性**:

- **UUID**: `ECUC:5afd11aa-5406-45d4-b56a-6ea45ba3d010`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSubElementInDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ApplicationCompositeDataType.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. DemSubElementInDataElementInstanceRef

- **UUID**: `ECUC:6b0b0abb-b972-44f8-aae4-c32fcb78a982`
- **引用名**: `DemSubElementInDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port which shall be read or written.

####### 13. DemSubElementInImplDataElementInstance

**容器属性**:

- **UUID**: `ECUC:c8bd6556-b5be-4c93-9be9-37a70a4d8424`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSubElementInImplDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. DemSubElementInImplDataElementInstanceRef

- **UUID**: `ECUC:ad862330-1bb1-40f6-816f-bf8b49e5c159`
- **引用名**: `DemSubElementInImplDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE-ELEMENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port which shall be read or written.

####### 14. DemInternalDataElementClass

**容器属性**:

- **UUID**: `ECUC:3169b35f-f938-49a0-976c-91300ae5037d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemInternalDataElementClass`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for an internal data element class.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DemDataElementDataSize

- **UUID**: `ECUC:2c592a33-d99b-45f2-9427-5f246a99524d`
- **参数名**: `DemDataElementDataSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the size of the data element in bytes.

######### ENUMERATION 类型参数

########## 1. DemInternalDataElement

- **UUID**: `ECUC:fe434fc3-1ebf-40e6-9b79-a20a65a9dcf8`
- **参数名**: `DemInternalDataElement`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_AGINGCTR_DOWNCNT` (来源: AUTOSAR_ECUC)
  - `DEM_AGINGCTR_UPCNT` (来源: AUTOSAR_ECUC)
  - `DEM_CURRENT_FDC` (来源: AUTOSAR_ECUC)
  - `DEM_CYCLES_SINCE_FIRST_FAILED` (来源: AUTOSAR_ECUC)
  - `DEM_CYCLES_SINCE_LAST_FAILED` (来源: AUTOSAR_ECUC)
  - `DEM_FAILED_CYCLES` (来源: AUTOSAR_ECUC)
  - `DEM_MAX_FDC_DURING_CURRENT_CYCLE` (来源: AUTOSAR_ECUC)
  - `DEM_MAX_FDC_SINCE_LAST_CLEAR` (来源: AUTOSAR_ECUC)
  - `DEM_OCCCTR` (来源: AUTOSAR_ECUC)
  - `DEM_OVFLIND` (来源: AUTOSAR_ECUC)
  - `DEM_SIGNIFICANCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Dem-internal data value, which is mapped to the data element.

####### 15. DemDidClass

**容器属性**:

- **UUID**: `ECUC:e1cbc150-3dd5-4439-abf5-ccb4cde025c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDidClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for a data Id class. It is assembled out of one or several data elements.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DemDidIdentifier

- **UUID**: `ECUC:6fb72160-e0f8-4592-831c-05d34fe8c839`
- **参数名**: `DemDidIdentifier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Data ID.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DemDidDataElementClassRef

- **UUID**: `ECUC:30a0fb20-847a-43b2-ad30-0df10d7c2f68`
- **引用名**: `DemDidDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..255]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

####### 16. DemEnableCondition

**容器属性**:

- **UUID**: `ECUC:490f6445-7fad-4f11-9130-c78155a7fbe6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemEnableCondition`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for enable conditions.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DemEnableConditionId

- **UUID**: `ECUC:8941da71-f206-4351-8887-40650a034533`
- **参数名**: `DemEnableConditionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a unique enable condition Id.

######### BOOLEAN 类型参数

########## 1. DemEnableConditionStatus

- **UUID**: `ECUC:7e66af51-7547-4ead-9cc8-9dd2c2f112fe`
- **参数名**: `DemEnableConditionStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the initial status for enable or disable of acceptance of event reports of a diagnostic event.

####### 17. DemEnableConditionGroup

**容器属性**:

- **UUID**: `ECUC:32a02fa5-08ff-4668-b2a6-bcc8066eccd1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemEnableConditionGroup`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for enable condition groups.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DemEnableConditionRef

- **UUID**: `ECUC:2efef637-5844-4dfc-984b-a96a59d045f2`
- **引用名**: `DemEnableConditionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DemEnableCondition`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemEnableCondition`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References an enable condition.

####### 18. DemExtendedDataClass

**容器属性**:

- **UUID**: `ECUC:9a005bc7-bfcc-476f-a2fa-1152a1793b12`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemExtendedDataClass`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This class contains the combinations of extended data records for an extended data class.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DemExtendedDataRecordClassRef

- **UUID**: `ECUC:76ed7707-7ef4-4a49-8502-1182d3997425`
- **引用名**: `DemExtendedDataRecordClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..253]
- **目标**: `DemExtendedDataRecordClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemExtendedDataRecordClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to an extended data class record.

####### 19. DemExtendedDataRecordClass

**容器属性**:

- **UUID**: `ECUC:6821e454-6d75-4f8b-a6c1-c1e0fdc5f8d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemExtendedDataRecordClass`
- **多重性**: [0..253]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for an extended data record class.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DemExtendedDataRecordNumber

- **UUID**: `ECUC:a403cf7b-c80e-4d4b-9e39-5805c8992866`
- **参数名**: `DemExtendedDataRecordNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter specifies an unique identifier for an extended data record.

######### ENUMERATION 类型参数

########## 1. DemExtendedDataRecordTrigger

- **UUID**: `ECUC:2c092a02-741b-4363-b677-051dfa118690`
- **参数名**: `DemExtendedDataRecordTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_EXTENDED_DATA_CAPTURE_ON_CONFIRMED` (来源: AUTOSAR_ECUC)
  - `DEM_EXTENDED_DATA_CAPTURE_ON_FDC_THRESHOLD` (来源: AUTOSAR_ECUC)
  - `DEM_EXTENDED_DATA_CAPTURE_ON_PENDING` (来源: AUTOSAR_ECUC)
  - `DEM_EXTENDED_DATA_CAPTURE_ON_TEST_FAILED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the primary trigger to allocate an event memory entry.

########## 2. DemExtendedDataRecordUpdate

- **UUID**: `ECUC:221029aa-5a23-40f4-b9e0-b01c16eb1ecb`
- **参数名**: `DemExtendedDataRecordUpdate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_UPDATE_RECORD_NO` (来源: AUTOSAR_ECUC)
  - `DEM_UPDATE_RECORD_YES` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This extended data record is captured if the configured trigger condition in "DemExtendedDataRecordTrigger" is fulfilled.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DemDataElementClassRef

- **UUID**: `ECUC:97567e6b-f870-4e8a-ba55-b05cfd081266`
- **引用名**: `DemDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..255]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

####### 20. DemFreezeFrameClass

**容器属性**:

- **UUID**: `ECUC:0dd242a0-90fd-4d71-9506-bcab60321bf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemFreezeFrameClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the combinations of DIDs for a non OBD relevant freeze frame class.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DemDidClassRef

- **UUID**: `ECUC:f641607d-0dcf-4d67-80a5-3fddd327023a`
- **引用名**: `DemDidClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DemDidClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDidClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For OBD relevant data

####### 21. DemFreezeFrameRecNumClass

**容器属性**:

- **UUID**: `ECUC:e2e5fbe0-d229-4de6-a9db-3c1d6cf37722`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemFreezeFrameRecNumClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains a list of dedicated, different freeze frame record numbers assigned to an event. The order of record numbers in this list is assigned to the chronological order of the according freeze frame records.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DemFreezeFrameRecordClassRef

- **UUID**: `ECUC:0c808701-e72e-45ab-9efe-233c0ea65198`
- **引用名**: `DemFreezeFrameRecordClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..254]
- **目标**: `DemFreezeFrameRecordClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemFreezeFrameRecordClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references record number(s) for a freeze frame record.

####### 22. DemFreezeFrameRecordClass

**容器属性**:

- **UUID**: `ECUC:243fd8af-15d0-4af1-99db-c610b201491b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemFreezeFrameRecordClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains a list of dedicated, different freeze frame record numbers.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DemFreezeFrameRecordNumber

- **UUID**: `ECUC:8577a18a-a211-451a-86ba-332c3c551648`
- **参数名**: `DemFreezeFrameRecordNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a record number for a freeze frame record. This record number is unique per freeze frame record number class.

######### ENUMERATION 类型参数

########## 1. DemFreezeFrameRecordTrigger

- **UUID**: `ECUC:4386a02e-28bd-4dc9-b99a-1829f34a1792`
- **参数名**: `DemFreezeFrameRecordTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_FREEZE_FRAME_CAPTURE_ON_CONFIRMED` (来源: AUTOSAR_ECUC)
  - `DEM_FREEZE_FRAME_CAPTURE_ON_FDC_THRESHOLD` (来源: AUTOSAR_ECUC)
  - `DEM_FREEZE_FRAME_CAPTURE_ON_PENDING` (来源: AUTOSAR_ECUC)
  - `DEM_FREEZE_FRAME_CAPTURE_ON_TEST_FAILED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the primary trigger to allocate an event memory entry.

########## 2. DemFreezeFrameRecordUpdate

- **UUID**: `ECUC:b96da489-b522-43af-8733-2894c87542da`
- **参数名**: `DemFreezeFrameRecordUpdate`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_UPDATE_RECORD_NO` (来源: AUTOSAR_ECUC)
  - `DEM_UPDATE_RECORD_YES` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the case, when the freeze frame record is stored/updated.

####### 23. DemGeneralJ1939

**容器属性**:

- **UUID**: `ECUC:b8f84dc2-a70a-4523-8c77-0cef2f837fbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemGeneralJ1939`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the general J1939-specific configuration (parameters) of the Dem module.

######## 参数配置

此容器包含 **9** 个参数：

######### BOOLEAN 类型参数

########## 1. DemJ1939ClearDtcSupport

- **UUID**: `ECUC:006b1cb5-b415-4364-a2de-9716bb0336eb`
- **参数名**: `DemJ1939ClearDtcSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether clearing J1939 DTCs (DM3 und DM11) is supported or not.

########## 2. DemJ1939Dm31Support

- **UUID**: `ECUC:12b38ba3-011d-436c-bc42-997b08968c93`
- **参数名**: `DemJ1939Dm31Support`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 DM31 is supported or not.

########## 3. DemJ1939ExpandedFreezeFrameSupport

- **UUID**: `ECUC:c3285bd5-b3d6-48de-a1a2-9d1e46424e94`
- **参数名**: `DemJ1939ExpandedFreezeFrameSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 expanded freeze frames are supported or not.

########## 4. DemJ1939FreezeFrameSupport

- **UUID**: `ECUC:6cbd5bf9-7d09-474b-93ac-870ea2b2c62d`
- **参数名**: `DemJ1939FreezeFrameSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 freeze frames are supported or not.

########## 5. DemJ1939RatioSupport

- **UUID**: `ECUC:60ea9ba9-0c2d-4cb4-8a29-0ef5482137fe`
- **参数名**: `DemJ1939RatioSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 performance ratios are supported or not.

########## 6. DemJ1939Readiness1Support

- **UUID**: `ECUC:7a872ae9-095f-42ca-8442-ab9448998fab`
- **参数名**: `DemJ1939Readiness1Support`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 diagnostic readiness 1 is supported or not.

########## 7. DemJ1939Readiness2Support

- **UUID**: `ECUC:081b4af4-1e48-412f-ac0b-bb549d8cdd64`
- **参数名**: `DemJ1939Readiness2Support`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 diagnostic readiness 2 is supported or not.

########## 8. DemJ1939Readiness3Support

- **UUID**: `ECUC:6f94320e-b403-48e1-9a7c-3c3c34518b32`
- **参数名**: `DemJ1939Readiness3Support`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 diagnostic readiness 3 is supported or not.

########## 9. DemJ1939ReadingDtcSupport

- **UUID**: `ECUC:3594bc2e-8726-44f8-b638-e5be99388147`
- **参数名**: `DemJ1939ReadingDtcSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 DTC readout is supported or not.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. DemAmberWarningLampIndicatorRef

- **UUID**: `ECUC:cedf27e6-b9f5-4c36-800f-eab98917ec18`
- **引用名**: `DemAmberWarningLampIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the indicator representing the AmberWarningLamp . This parameter may be used for ECUs supporting J1939.

########## 2. DemProtectLampIndicatorRef

- **UUID**: `ECUC:76cac18f-6be9-4b81-866c-5150aa610a5c`
- **引用名**: `DemProtectLampIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the indicator representing the ProtectLamp. This parameter may be used for ECUs supporting J1939.

########## 3. DemRedStopLampIndicatorRef

- **UUID**: `ECUC:7f4fc974-67c0-418f-b4a7-d09d62b6c85e`
- **引用名**: `DemRedStopLampIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the indicator representing the RedStopLamp. This parameter may be used for ECUs supporting J1939.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. DemCallbackJ1939DTCStatusChanged

**容器属性**:

- **UUID**: `ECUC:0d124437-dcbb-45fc-b7fb-75077766d0bf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackJ1939DTCStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback, which the Dem will call to notify other components about the change in the status of a DTC.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackDTCStatusChangedFnc

- **UUID**: `ECUC:51d9c5c0-bb7f-4566-be08-1f2181bda434`
- **参数名**: `DemCallbackDTCStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "DTCStatusChanged".

######### 2. DemJ1939FreezeFrameClass

**容器属性**:

- **UUID**: `ECUC:86700f99-a606-494e-ae36-cee1fcd4331d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemJ1939FreezeFrameClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the combinations of SPNs s for a J1939 relevant freeze frame.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DemSPNClassRef

- **UUID**: `ECUC:eaead167-1f62-4a5c-bc75-25f40d834faa`
- **引用名**: `DemSPNClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DemSPNClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemGeneralJ1939/DemSPNClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an SPN. This reference defines requiresIndex = true since it represents a ordered list of references where the order describes the order of single SPNs in the J1939 Freeze Frame.

######### 3. DemSPNClass

**容器属性**:

- **UUID**: `ECUC:d77f4ee8-fef8-4b89-a725-1253893ad24a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSPNClass`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for a SPN.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DemSPNId

- **UUID**: `ECUC:2716b2e8-64bd-491e-8fad-735bc797fcd2`
- **参数名**: `DemSPNId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..524287]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Suspect parameter number

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. DemSPNDataElementClassRef

- **UUID**: `ECUC:1a039457-9359-433b-8fec-561253267c68`
- **引用名**: `DemSPNDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

####### 24. DemCallbackJ1939DTCStatusChanged

**容器属性**:

- **UUID**: `ECUC:0d124437-dcbb-45fc-b7fb-75077766d0bf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackJ1939DTCStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback, which the Dem will call to notify other components about the change in the status of a DTC.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackDTCStatusChangedFnc

- **UUID**: `ECUC:51d9c5c0-bb7f-4566-be08-1f2181bda434`
- **参数名**: `DemCallbackDTCStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "DTCStatusChanged".

####### 25. DemJ1939FreezeFrameClass

**容器属性**:

- **UUID**: `ECUC:86700f99-a606-494e-ae36-cee1fcd4331d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemJ1939FreezeFrameClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the combinations of SPNs s for a J1939 relevant freeze frame.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DemSPNClassRef

- **UUID**: `ECUC:eaead167-1f62-4a5c-bc75-25f40d834faa`
- **引用名**: `DemSPNClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DemSPNClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemGeneralJ1939/DemSPNClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an SPN. This reference defines requiresIndex = true since it represents a ordered list of references where the order describes the order of single SPNs in the J1939 Freeze Frame.

####### 26. DemSPNClass

**容器属性**:

- **UUID**: `ECUC:d77f4ee8-fef8-4b89-a725-1253893ad24a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSPNClass`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for a SPN.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DemSPNId

- **UUID**: `ECUC:2716b2e8-64bd-491e-8fad-735bc797fcd2`
- **参数名**: `DemSPNId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..524287]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Suspect parameter number

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DemSPNDataElementClassRef

- **UUID**: `ECUC:1a039457-9359-433b-8fec-561253267c68`
- **引用名**: `DemSPNDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

####### 27. DemGeneralOBD

**容器属性**:

- **UUID**: `ECUC:dc39405f-19df-4342-bf96-7955053c295f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemGeneralOBD`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the general OBD-specific configuration (parameters) of the Dem module.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. DemOBDCompliancy

- **UUID**: `ECUC:cfcbf5d3-1309-4a84-ac7c-247c321b34f1`
- **参数名**: `DemOBDCompliancy`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration value to define  the appropriate value to PID$1C "OBD requirements to which vehicle or engine is certified." according to the respective standards, e.g. OBD, OBDII, JOBD etc.

######### BOOLEAN 类型参数

########## 1. DemOBDCentralizedPID21Handling

- **UUID**: `ECUC:dcb3a818-296a-471f-944a-382dbe24efa3`
- **参数名**: `DemOBDCentralizedPID21Handling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to enable the centralized handling of PID $21.

########## 2. DemOBDCentralizedPID31Handling

- **UUID**: `ECUC:fd5a0bb6-54d2-4124-85b4-316cc364f4f3`
- **参数名**: `DemOBDCentralizedPID31Handling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to enable the centralized handling of PID $31.

########## 3. DemOBDEventDisplacement

- **UUID**: `ECUC:2b92632d-3dbf-4fc6-b488-3786c582eb80`
- **参数名**: `DemOBDEventDisplacement`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate a different displacement behavior for OBD events.

######### ENUMERATION 类型参数

########## 1. DemOBDDestinationOfEvents

- **UUID**: `ECUC:6fe71c89-ac19-4ddb-91b7-39582c4f59c6`
- **参数名**: `DemOBDDestinationOfEvents`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTC_ORIGIN_PRIMARY_MEMORY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_ORIGIN_SECONDARY_MEMORY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The destination of events assigns where the OBD events shall be stored.

######## 引用关系

此容器包含 **9** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DemOBDInputAcceleratorPedalInformation

- **UUID**: `ECUC:4e99443b-59a7-4f36-a2da-6bd7fca7143a`
- **引用名**: `DemOBDInputAcceleratorPedalInformation`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the accelerator padal information, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

########## 2. DemOBDInputAmbientPressure

- **UUID**: `ECUC:e7436253-fc7b-40af-856e-3843edd48fc4`
- **引用名**: `DemOBDInputAmbientPressure`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the ambient pressure, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

########## 3. DemOBDInputAmbientTemperature

- **UUID**: `ECUC:d21feba4-8962-41c4-b8a3-14bb9ee2b13e`
- **引用名**: `DemOBDInputAmbientTemperature`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the ambient temperature, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

########## 4. DemOBDInputDistanceInformation

- **UUID**: `ECUC:e4405450-1973-437f-9a72-6b4f3c1d6f30`
- **引用名**: `DemOBDInputDistanceInformation`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the distance information, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

########## 5. DemOBDInputEngineSpeed

- **UUID**: `ECUC:3c88edb4-d1bc-439d-a059-ae046bb4da25`
- **引用名**: `DemOBDInputEngineSpeed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the engine speed, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

########## 6. DemOBDInputEngineTemperature

- **UUID**: `ECUC:a77d2964-9355-4869-83f4-2f929f570dec`
- **引用名**: `DemOBDInputEngineTemperature`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the engine temperature, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

########## 7. DemOBDInputProgrammingEvent

- **UUID**: `ECUC:855ef6a6-5c64-4498-b6e8-a8f2b2aacc5d`
- **引用名**: `DemOBDInputProgrammingEvent`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the programming event, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

########## 8. DemOBDInputVehicleSpeed

- **UUID**: `ECUC:5256078f-f457-473b-945f-24f415eb398e`
- **引用名**: `DemOBDInputVehicleSpeed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the vehicle speed, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

########## 9. DemOBDTimeSinceEngineStart

- **UUID**: `ECUC:2edc7ce5-2f3c-4ce3-a381-1feb57738843`
- **引用名**: `DemOBDTimeSinceEngineStart`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the Time Since Engine Start information, which is assigned to a specific data element.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DemCallbackOBDDTCStatusChanged

**容器属性**:

- **UUID**: `ECUC:bb68bdbd-d314-4379-a7f5-797f07f6fab0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackOBDDTCStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback, which the Dem will call to notify other components about the change in the status of a DTC.

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. DemCallbackDTCStatusChangedFnc

- **UUID**: `ECUC:d8e3c461-3103-4e19-8243-a9ad31b83d65`
- **参数名**: `DemCallbackDTCStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "DTCStatusChanged".

####### 28. DemCallbackOBDDTCStatusChanged

**容器属性**:

- **UUID**: `ECUC:bb68bdbd-d314-4379-a7f5-797f07f6fab0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackOBDDTCStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback, which the Dem will call to notify other components about the change in the status of a DTC.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackDTCStatusChangedFnc

- **UUID**: `ECUC:d8e3c461-3103-4e19-8243-a9ad31b83d65`
- **参数名**: `DemCallbackDTCStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "DTCStatusChanged".

####### 29. DemGroupOfDTC

**容器属性**:

- **UUID**: `ECUC:c89875f9-acf6-428b-9a00-4c3f2c8afe19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemGroupOfDTC`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for DTC groups.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DemGroupDTCs

- **UUID**: `ECUC:2e622411-01bb-411b-90b1-6c0947dbad48`
- **参数名**: `DemGroupDTCs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..16777214]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: DTC value of the selected group of DTC

####### 30. DemIndicator

**容器属性**:

- **UUID**: `ECUC:3d9ac4b7-4eb9-4ac6-b433-30b5b6fa9fe9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemIndicator`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for Indicators.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DemIndicatorID

- **UUID**: `ECUC:7b5c78d8-ffb6-478c-a521-a8ebfeb21b00`
- **参数名**: `DemIndicatorID`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier of an indicator.

####### 31. DemNvRamBlockId

**容器属性**:

- **UUID**: `ECUC:3ab8406f-9f71-44c9-8200-0c9baf37a90a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemNvRamBlockId`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for a non-volatile memory block, which is used from the Dem. If no permanent storage of event memory entries is required, no block needs to be configured.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. DemNvRamBlockIdRef

- **UUID**: `ECUC:3dfa5a10-bb40-4111-9e8d-653298123dfc`
- **引用名**: `DemNvRamBlockIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a non-volatile memory block. For post build time configurations worst case scenario shall be used.

####### 32. DemOperationCycle

**容器属性**:

- **UUID**: `ECUC:edf2c803-842d-44ee-91cf-76c67f209935`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemOperationCycle`
- **多重性**: [1..256]
- **多配置容器**: false

**容器描述**:

Note that this container definition does not explicitly define a symbolic name parameter. Instead, the short name of the container will be used in the Ecu Configuration Description to specify the symbolic name of the operation cycle name.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. DemOperationCycleAutomaticEnd

- **UUID**: `ECUC:bd53f3b5-1f03-41df-b65a-5a892484e08c`
- **参数名**: `DemOperationCycleAutomaticEnd`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If DemOperationCycleAutomaticEnd is configured to TRUE, Dem shall automatically end the driving cycle at either Dem_Shutdown() or Dem_Init().

########## 2. DemOperationCycleAutostart

- **UUID**: `ECUC:99ec8223-f61d-498a-b636-fdd2b87159a9`
- **参数名**: `DemOperationCycleAutostart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The autostart property defines if the operation cycles is automatically (re-)started during Dem_PreInit.

######### ENUMERATION 类型参数

########## 1. DemOperationCycleType

- **UUID**: `ECUC:7544f8ce-f35f-4335-b2da-a0144b7c0dce`
- **参数名**: `DemOperationCycleType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_OPCYC_IGNITION` (来源: AUTOSAR_ECUC)
  - `DEM_OPCYC_OBD_DCY` (来源: AUTOSAR_ECUC)
  - `DEM_OPCYC_OTHER` (来源: AUTOSAR_ECUC)
  - `DEM_OPCYC_POWER` (来源: AUTOSAR_ECUC)
  - `DEM_OPCYC_TIME` (来源: AUTOSAR_ECUC)
  - `DEM_OPCYC_WARMUP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Operation cycles types for the Dem to be supported by cycle-state APIs.

####### 33. DemRatio

**容器属性**:

- **UUID**: `ECUC:bd1f9289-8c44-4164-9c8c-385ab2d911b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemRatio`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container contains the OBD-specific in-use-monitor performance ratio configuration.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DemRatioId

- **UUID**: `ECUC:25cf98a3-6dce-490d-a2f1-8a73b51507ad`
- **参数名**: `DemRatioId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a unique ratio Id.

######### ENUMERATION 类型参数

########## 1. DemIUMPRDenGroup

- **UUID**: `ECUC:f97b47cb-864b-4aef-beae-173913703bd0`
- **参数名**: `DemIUMPRDenGroup`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_IUMPR_DEN_500MILL` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_DEN_COLDSTART` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_DEN_EVAP` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_DEN_NONE` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_DEN_PHYS_API` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the assigned denominator type which is applied in addition to the General Denominator conditions.

########## 2. DemIUMPRGroup

- **UUID**: `ECUC:6210985c-4380-4b4b-adba-d12b8c40365f`
- **参数名**: `DemIUMPRGroup`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_IUMPR_BOOSTPRS` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_CAT1` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_CAT2` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_EGR` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_EGSENSOR` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_EVAP` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_FLSYS` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_NMHCCAT` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_NOXADSORB` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_NOXCAT` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_OXS1` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_OXS2` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_PMFILTER` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_PRIVATE` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_SAIR` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_SECOXS1` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_SECOXS2` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the assigned IUMPR group of the ratio Id.

########## 3. DemRatioKind

- **UUID**: `ECUC:5b7f3369-b175-4235-bd33-5f46fe1078d9`
- **参数名**: `DemRatioKind`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_RATIO_API` (来源: AUTOSAR_ECUC)
  - `DEM_RATIO_OBSERVER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the ratio will be calculated API or observer based.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. DemDiagnosticEventRef

- **UUID**: `ECUC:e4a17661-b438-44c2-b250-9d97e9cda20d`
- **引用名**: `DemDiagnosticEventRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a diagnostic event.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. DemFunctionIdRef

- **UUID**: `ECUC:36c5505e-2322-474d-8979-f5ca259d394d`
- **引用名**: `DemFunctionIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FiMFID`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMFID`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a function identifier within the FiM which is used as a primary FID.

########## 2. DemSecondaryFunctionIdRef

- **UUID**: `ECUC:48718548-1795-412d-a803-72c0e418f233`
- **引用名**: `DemSecondaryFunctionIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `FiMFID`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMFID`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a function identifier within the FiM which is used as a secondary FID.

####### 34. DemStorageCondition

**容器属性**:

- **UUID**: `ECUC:5f232bac-fe27-4d30-b072-1795f9af7ef6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemStorageCondition`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for storage conditions.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DemStorageConditionId

- **UUID**: `ECUC:67e309bf-b4b9-4de5-b0d1-47df01d36b84`
- **参数名**: `DemStorageConditionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a unique storage condition Id. This parameter should not be changeable by user, because the Id should be generated by Dem itself to prevent gaps and multiple use of an Id. The storage conditions should be sequentially ordered beginning with 0 and no gaps in between.

######### BOOLEAN 类型参数

########## 1. DemStorageConditionStatus

- **UUID**: `ECUC:57bb12c8-1d23-4314-a9fa-d0cb5116322f`
- **参数名**: `DemStorageConditionStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the initial status for enable or disable of storage of a diagnostic event.

####### 35. DemStorageConditionGroup

**容器属性**:

- **UUID**: `ECUC:713b95f5-b501-4a30-91c8-cedbe4ba692b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemStorageConditionGroup`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for storage condition groups.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DemStorageConditionRef

- **UUID**: `ECUC:94a93959-aae2-416d-a59a-bd0fae591f32`
- **引用名**: `DemStorageConditionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DemStorageCondition`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemStorageCondition`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References an enable condition.

####### 36. DemClient

**容器属性**:

- **UUID**: `ECUC:5d3c6e4a-6c4c-4754-b120-000eb60702c2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemClient`
- **多重性**: [1..255]

**容器描述**:

This container contains possible clients that are using the Dem APIs.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DemClientId

- **UUID**: `ECUC:06c5d156-e093-420c-a281-d73b792ba3f9`
- **参数名**: `DemClientId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Defines a unique identifier for a Dem client. This number is used by this client in the ClientID parameter in all API with this parameter.

####### 37. DemDataElementClass

**容器属性**:

- **UUID**: `ECUC:6505a151-66bd-4283-b004-9f267f7ce44e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDataElementClass`
- **多重性**: [0..255]

**容器选择**:

- **DemExternalCSDataElementClass**
  - UUID: `ECUC:731531ff-e865-4793-887a-8064686ae7d1`
  - 描述: This container contains the configuration (parameters) for an external client/server based data element class.
- **DemExternalSRDataElementClass**
  - UUID: `ECUC:8e6c8d7e-2a1f-44a9-a5cf-728b1478f58d`
  - 描述: This container contains the configuration (parameters) for an external sender/receiver based data element class. It defines, how the Dem can obtain the value of the data element from a SW-C, by using a sender/receiver port.
- **DemAlternativeDataInterface**
  - UUID: `ECUC:c494d1bc-6807-4116-868f-139fc9d4056c`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of a VariableDataPrototoype in a DataInterface.
- **DemAlternativeDataProps**
  - UUID: `ECUC:3b554f3d-00a7-4269-b499-bed18222a6e6`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of ECU configuration parameters.
- **DemLinearScale**
  - UUID: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
  - 描述: This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.
- **DemTextTableMapping**
  - UUID: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.
- **DemAlternativeDataType**
  - UUID: `ECUC:f403e75d-f752-4e3d-aa66-4d086335d59f`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of an ApplicationDataType.
- **DemTextTableMapping**
  - UUID: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.
- **DemDataElementInstance**
  - UUID: `ECUC:1da3b6b3-d899-4105-96f5-eee7ed1ed32f`
  - 描述: Instance Reference to the primitive data in a port  where the data element is typed with an ApplicationPrimitveDataType or an ImplementationDataType.
- **DemSubElementInDataElementInstance**
  - UUID: `ECUC:5afd11aa-5406-45d4-b56a-6ea45ba3d010`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ApplicationCompositeDataType.
- **DemSubElementInImplDataElementInstance**
  - UUID: `ECUC:c8bd6556-b5be-4c93-9be9-37a70a4d8424`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.
- **DemInternalDataElementClass**
  - UUID: `ECUC:3169b35f-f938-49a0-976c-91300ae5037d`
  - 描述: This container contains the configuration (parameters) for an internal data element class.

**容器描述**:

This container contains the configuration (parameters) for an internal/external data element class.

####### 38. DemDiagnosisScaling

**容器属性**:

- **UUID**: `ECUC:1113d69e-4b70-4756-bea7-2f74de625fcf`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDiagnosisScaling`
- **多重性**: [0..1]

**容器选择**:

- **DemAlternativeDataInterface**
  - UUID: `ECUC:c494d1bc-6807-4116-868f-139fc9d4056c`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of a VariableDataPrototoype in a DataInterface.
- **DemAlternativeDataProps**
  - UUID: `ECUC:3b554f3d-00a7-4269-b499-bed18222a6e6`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of ECU configuration parameters.
- **DemLinearScale**
  - UUID: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
  - 描述: This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.
- **DemTextTableMapping**
  - UUID: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.
- **DemAlternativeDataType**
  - UUID: `ECUC:f403e75d-f752-4e3d-aa66-4d086335d59f`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of an ApplicationDataType.
- **DemTextTableMapping**
  - UUID: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation. Out if this the scaling between Diagnosis and ECU internal representation and vice versa can be calculated.

####### 39. DemSRDataElementClass

**容器属性**:

- **UUID**: `ECUC:cbfb18d6-1749-45e0-833d-34d9d30215d4`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemSRDataElementClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDataElementInstance**
  - UUID: `ECUC:1da3b6b3-d899-4105-96f5-eee7ed1ed32f`
  - 描述: Instance Reference to the primitive data in a port  where the data element is typed with an ApplicationPrimitveDataType or an ImplementationDataType.
- **DemSubElementInDataElementInstance**
  - UUID: `ECUC:5afd11aa-5406-45d4-b56a-6ea45ba3d010`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ApplicationCompositeDataType.
- **DemSubElementInImplDataElementInstance**
  - UUID: `ECUC:c8bd6556-b5be-4c93-9be9-37a70a4d8424`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.

**容器描述**:

This container defines the source of data in a provided port which shall be read for a external data element

##### 20. DemAgingCycle

**容器属性**:

- **UUID**: `ECUC:25f625cb-f3db-4091-922d-c554992647c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAgingCycle`
- **多重性**: [0..256]
- **多配置容器**: false

**容器描述**:

Note that this container definition does not explicitly define a symbolic name parameter. Instead, the short name of the container will be used in the Ecu Configuration Description to specify the symbolic name of the aging cycle name. These aging cycles are reported via API Dem_SetAgingCycleState only.

##### 21. DemCallbackDTCStatusChanged

**容器属性**:

- **UUID**: `ECUC:101cdd27-4d18-467d-a6d0-d9561d5424e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackDTCStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback, which the Dem will call to notify other components about the change in the status of a DTC.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DemCallbackDTCStatusChangedFnc

- **UUID**: `ECUC:f95f691b-c363-4c11-9b04-852adad46b90`
- **参数名**: `DemCallbackDTCStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "DTCStatusChanged".

##### 22. DemExternalCSDataElementClass

**容器属性**:

- **UUID**: `ECUC:731531ff-e865-4793-887a-8064686ae7d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemExternalCSDataElementClass`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for an external client/server based data element class.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DemDataElementDataSize

- **UUID**: `ECUC:a23991f9-25de-4d38-8aca-a06d784b6697`
- **参数名**: `DemDataElementDataSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the size of the data element in bytes.

####### BOOLEAN 类型参数

######## 1. DemDataElementUsePort

- **UUID**: `ECUC:9cf1ca4d-69eb-4ba4-bfbc-6e3c027526d2`
- **参数名**: `DemDataElementUsePort`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the parameter is set to True, a R-Port is generated, to obtain the data element (interface DataServices_<SyncDataElement>).

####### FUNCTION-NAME 类型参数

######## 1. DemDataElementReadFnc

- **UUID**: `ECUC:fa9c6503-853e-4f03-b603-dfee41f57709`
- **参数名**: `DemDataElementReadFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In case of DemDataElementUsePort is false, this parameter defines the prototype of the C function "ReadDataElement" used to get the according value.

##### 23. DemExternalSRDataElementClass

**容器属性**:

- **UUID**: `ECUC:8e6c8d7e-2a1f-44a9-a5cf-728b1478f58d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemExternalSRDataElementClass`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for an external sender/receiver based data element class. It defines, how the Dem can obtain the value of the data element from a SW-C, by using a sender/receiver port.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DemDataElementDataSize

- **UUID**: `ECUC:9d166994-cc93-44c6-9fa0-52f7bc28e02b`
- **参数名**: `DemDataElementDataSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the size of the data element in bits.

####### ENUMERATION 类型参数

######## 1. DemDataElementDataType

- **UUID**: `ECUC:25afee69-0327-4666-8baf-77218bb4a807`
- **参数名**: `DemDataElementDataType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Provide the implementation data type of data belonging to a external data.

######## 2. DemDataElementEndianness

- **UUID**: `ECUC:ccdad70a-e417-49cb-b2f5-ba55fd055f02`
- **参数名**: `DemDataElementEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the data belonging to an external data.

###### 配置容器

本模块包含 **11** 个配置容器：

####### 1. DemAlternativeDataInterface

**容器属性**:

- **UUID**: `ECUC:c494d1bc-6807-4116-868f-139fc9d4056c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataInterface`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of a VariableDataPrototoype in a DataInterface.

######## 引用关系

此容器包含 **2** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DemDataElement

- **UUID**: `ECUC:a976f624-cf39-4827-bd93-dee061b141ee`
- **引用名**: `DemDataElement`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Alternative Diagnosis Representation for the data defined by the means of a VariableDataPrototoype in a DataInterface.

########## 2. DemPortInterfaceMapping

- **UUID**: `ECUC:2fa38569-4bc8-4f8a-be68-d40ed21fea34`
- **引用名**: `DemPortInterfaceMapping`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: PORT-INTERFACE-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to PortInterfaceMapping which defines the mapping rules.

####### 2. DemAlternativeDataProps

**容器属性**:

- **UUID**: `ECUC:3b554f3d-00a7-4269-b499-bed18222a6e6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataProps`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of ECU configuration parameters.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. DemDataTypeCategory

- **UUID**: `ECUC:4583a595-9cec-4832-a50a-8a7f8adb04c2`
- **参数名**: `DemDataTypeCategory`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `SCALE_LINEAR_AND_TEXTTABLE` (来源: AUTOSAR_ECUC)
  - `TEXTTABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data category of the alternative Diagnosis Representation.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DemLinearScale

**容器属性**:

- **UUID**: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemLinearScale`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.

########## 参数配置

此容器包含 **4** 个参数：

########### FLOAT 类型参数

############ 1. DemDiagnosisRepresentationDataLowerRange

- **UUID**: `ECUC:33ff4aeb-6e0d-4f56-bb9d-d9cbcf0b8a82`
- **参数名**: `DemDiagnosisRepresentationDataLowerRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower Range for this scale of the data in the alternative Diagnosis Representation.

############ 2. DemDiagnosisRepresentationDataOffset

- **UUID**: `ECUC:e493b157-9aa7-493c-a845-66d62947b562`
- **参数名**: `DemDiagnosisRepresentationDataOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data offset of the alternative Diagnosis Representation for this scale.

############ 3. DemDiagnosisRepresentationDataResolution

- **UUID**: `ECUC:1110fe8f-72d4-452e-9e82-1cae64436142`
- **参数名**: `DemDiagnosisRepresentationDataResolution`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data resolution of the alternative Diagnosis Representation for this scale.

############ 4. DemDiagnosisRepresentationDataUpperRange

- **UUID**: `ECUC:b594bd37-222e-4a99-8d02-458c91b9a1e8`
- **参数名**: `DemDiagnosisRepresentationDataUpperRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper Range for this scale of the data in the alternative Diagnosis Representation.

######### 2. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:d9d82ed7-7e85-ce90-e005-f83904bb6b90`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

############ 2. DemInternalDataValue

- **UUID**: `ECUC:642c2ec0-b782-d319-db3d-28112033f97e`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

####### 3. DemLinearScale

**容器属性**:

- **UUID**: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemLinearScale`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.

######## 参数配置

此容器包含 **4** 个参数：

######### FLOAT 类型参数

########## 1. DemDiagnosisRepresentationDataLowerRange

- **UUID**: `ECUC:33ff4aeb-6e0d-4f56-bb9d-d9cbcf0b8a82`
- **参数名**: `DemDiagnosisRepresentationDataLowerRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower Range for this scale of the data in the alternative Diagnosis Representation.

########## 2. DemDiagnosisRepresentationDataOffset

- **UUID**: `ECUC:e493b157-9aa7-493c-a845-66d62947b562`
- **参数名**: `DemDiagnosisRepresentationDataOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data offset of the alternative Diagnosis Representation for this scale.

########## 3. DemDiagnosisRepresentationDataResolution

- **UUID**: `ECUC:1110fe8f-72d4-452e-9e82-1cae64436142`
- **参数名**: `DemDiagnosisRepresentationDataResolution`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data resolution of the alternative Diagnosis Representation for this scale.

########## 4. DemDiagnosisRepresentationDataUpperRange

- **UUID**: `ECUC:b594bd37-222e-4a99-8d02-458c91b9a1e8`
- **参数名**: `DemDiagnosisRepresentationDataUpperRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper Range for this scale of the data in the alternative Diagnosis Representation.

####### 4. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:d9d82ed7-7e85-ce90-e005-f83904bb6b90`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

########## 2. DemInternalDataValue

- **UUID**: `ECUC:642c2ec0-b782-d319-db3d-28112033f97e`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

####### 5. DemAlternativeDataType

**容器属性**:

- **UUID**: `ECUC:f403e75d-f752-4e3d-aa66-4d086335d59f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataType`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of an ApplicationDataType.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DemApplicationDataType

- **UUID**: `ECUC:438db0a6-b8c3-4e53-9e9f-fe7aa4530ed3`
- **引用名**: `DemApplicationDataType`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: APPLICATION-PRIMITIVE-DATA-TYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Alternative Diagnosis Representation for the data defined by the means of a ApplicationPrimitiveDataType of category VALUE or BOOLEAN.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:9286c6f8-7530-da64-d5d2-866fe5ce9a49`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

############ 2. DemInternalDataValue

- **UUID**: `ECUC:1cdac6e1-ae2d-deed-d109-b64801472837`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

####### 6. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:9286c6f8-7530-da64-d5d2-866fe5ce9a49`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

########## 2. DemInternalDataValue

- **UUID**: `ECUC:1cdac6e1-ae2d-deed-d109-b64801472837`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

####### 7. DemDataElementInstance

**容器属性**:

- **UUID**: `ECUC:1da3b6b3-d899-4105-96f5-eee7ed1ed32f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitive data in a port  where the data element is typed with an ApplicationPrimitveDataType or an ImplementationDataType.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. DemDataElementInstanceRef

- **UUID**: `ECUC:a420975a-5a17-48de-ad73-d7082549c962`
- **引用名**: `DemDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitive data which shall be read or written.

####### 8. DemSubElementInDataElementInstance

**容器属性**:

- **UUID**: `ECUC:5afd11aa-5406-45d4-b56a-6ea45ba3d010`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSubElementInDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ApplicationCompositeDataType.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. DemSubElementInDataElementInstanceRef

- **UUID**: `ECUC:6b0b0abb-b972-44f8-aae4-c32fcb78a982`
- **引用名**: `DemSubElementInDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port which shall be read or written.

####### 9. DemSubElementInImplDataElementInstance

**容器属性**:

- **UUID**: `ECUC:c8bd6556-b5be-4c93-9be9-37a70a4d8424`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSubElementInImplDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. DemSubElementInImplDataElementInstanceRef

- **UUID**: `ECUC:ad862330-1bb1-40f6-816f-bf8b49e5c159`
- **引用名**: `DemSubElementInImplDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE-ELEMENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port which shall be read or written.

####### 10. DemDiagnosisScaling

**容器属性**:

- **UUID**: `ECUC:1113d69e-4b70-4756-bea7-2f74de625fcf`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDiagnosisScaling`
- **多重性**: [0..1]

**容器选择**:

- **DemAlternativeDataInterface**
  - UUID: `ECUC:c494d1bc-6807-4116-868f-139fc9d4056c`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of a VariableDataPrototoype in a DataInterface.
- **DemAlternativeDataProps**
  - UUID: `ECUC:3b554f3d-00a7-4269-b499-bed18222a6e6`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of ECU configuration parameters.
- **DemLinearScale**
  - UUID: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
  - 描述: This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.
- **DemTextTableMapping**
  - UUID: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.
- **DemAlternativeDataType**
  - UUID: `ECUC:f403e75d-f752-4e3d-aa66-4d086335d59f`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of an ApplicationDataType.
- **DemTextTableMapping**
  - UUID: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation. Out if this the scaling between Diagnosis and ECU internal representation and vice versa can be calculated.

####### 11. DemSRDataElementClass

**容器属性**:

- **UUID**: `ECUC:cbfb18d6-1749-45e0-833d-34d9d30215d4`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemSRDataElementClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDataElementInstance**
  - UUID: `ECUC:1da3b6b3-d899-4105-96f5-eee7ed1ed32f`
  - 描述: Instance Reference to the primitive data in a port  where the data element is typed with an ApplicationPrimitveDataType or an ImplementationDataType.
- **DemSubElementInDataElementInstance**
  - UUID: `ECUC:5afd11aa-5406-45d4-b56a-6ea45ba3d010`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ApplicationCompositeDataType.
- **DemSubElementInImplDataElementInstance**
  - UUID: `ECUC:c8bd6556-b5be-4c93-9be9-37a70a4d8424`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.

**容器描述**:

This container defines the source of data in a provided port which shall be read for a external data element

##### 24. DemAlternativeDataInterface

**容器属性**:

- **UUID**: `ECUC:c494d1bc-6807-4116-868f-139fc9d4056c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataInterface`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of a VariableDataPrototoype in a DataInterface.

###### 引用关系

此容器包含 **2** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. DemDataElement

- **UUID**: `ECUC:a976f624-cf39-4827-bd93-dee061b141ee`
- **引用名**: `DemDataElement`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Alternative Diagnosis Representation for the data defined by the means of a VariableDataPrototoype in a DataInterface.

######## 2. DemPortInterfaceMapping

- **UUID**: `ECUC:2fa38569-4bc8-4f8a-be68-d40ed21fea34`
- **引用名**: `DemPortInterfaceMapping`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: PORT-INTERFACE-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to PortInterfaceMapping which defines the mapping rules.

##### 25. DemAlternativeDataProps

**容器属性**:

- **UUID**: `ECUC:3b554f3d-00a7-4269-b499-bed18222a6e6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataProps`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of ECU configuration parameters.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. DemDataTypeCategory

- **UUID**: `ECUC:4583a595-9cec-4832-a50a-8a7f8adb04c2`
- **参数名**: `DemDataTypeCategory`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `SCALE_LINEAR_AND_TEXTTABLE` (来源: AUTOSAR_ECUC)
  - `TEXTTABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data category of the alternative Diagnosis Representation.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DemLinearScale

**容器属性**:

- **UUID**: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemLinearScale`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.

######## 参数配置

此容器包含 **4** 个参数：

######### FLOAT 类型参数

########## 1. DemDiagnosisRepresentationDataLowerRange

- **UUID**: `ECUC:33ff4aeb-6e0d-4f56-bb9d-d9cbcf0b8a82`
- **参数名**: `DemDiagnosisRepresentationDataLowerRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower Range for this scale of the data in the alternative Diagnosis Representation.

########## 2. DemDiagnosisRepresentationDataOffset

- **UUID**: `ECUC:e493b157-9aa7-493c-a845-66d62947b562`
- **参数名**: `DemDiagnosisRepresentationDataOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data offset of the alternative Diagnosis Representation for this scale.

########## 3. DemDiagnosisRepresentationDataResolution

- **UUID**: `ECUC:1110fe8f-72d4-452e-9e82-1cae64436142`
- **参数名**: `DemDiagnosisRepresentationDataResolution`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data resolution of the alternative Diagnosis Representation for this scale.

########## 4. DemDiagnosisRepresentationDataUpperRange

- **UUID**: `ECUC:b594bd37-222e-4a99-8d02-458c91b9a1e8`
- **参数名**: `DemDiagnosisRepresentationDataUpperRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper Range for this scale of the data in the alternative Diagnosis Representation.

####### 2. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:d9d82ed7-7e85-ce90-e005-f83904bb6b90`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

########## 2. DemInternalDataValue

- **UUID**: `ECUC:642c2ec0-b782-d319-db3d-28112033f97e`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

##### 26. DemLinearScale

**容器属性**:

- **UUID**: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemLinearScale`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.

###### 参数配置

此容器包含 **4** 个参数：

####### FLOAT 类型参数

######## 1. DemDiagnosisRepresentationDataLowerRange

- **UUID**: `ECUC:33ff4aeb-6e0d-4f56-bb9d-d9cbcf0b8a82`
- **参数名**: `DemDiagnosisRepresentationDataLowerRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower Range for this scale of the data in the alternative Diagnosis Representation.

######## 2. DemDiagnosisRepresentationDataOffset

- **UUID**: `ECUC:e493b157-9aa7-493c-a845-66d62947b562`
- **参数名**: `DemDiagnosisRepresentationDataOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data offset of the alternative Diagnosis Representation for this scale.

######## 3. DemDiagnosisRepresentationDataResolution

- **UUID**: `ECUC:1110fe8f-72d4-452e-9e82-1cae64436142`
- **参数名**: `DemDiagnosisRepresentationDataResolution`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data resolution of the alternative Diagnosis Representation for this scale.

######## 4. DemDiagnosisRepresentationDataUpperRange

- **UUID**: `ECUC:b594bd37-222e-4a99-8d02-458c91b9a1e8`
- **参数名**: `DemDiagnosisRepresentationDataUpperRange`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper Range for this scale of the data in the alternative Diagnosis Representation.

##### 27. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:d9d82ed7-7e85-ce90-e005-f83904bb6b90`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

######## 2. DemInternalDataValue

- **UUID**: `ECUC:642c2ec0-b782-d319-db3d-28112033f97e`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

##### 28. DemAlternativeDataType

**容器属性**:

- **UUID**: `ECUC:f403e75d-f752-4e3d-aa66-4d086335d59f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemAlternativeDataType`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of an ApplicationDataType.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. DemApplicationDataType

- **UUID**: `ECUC:438db0a6-b8c3-4e53-9e9f-fe7aa4530ed3`
- **引用名**: `DemApplicationDataType`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: APPLICATION-PRIMITIVE-DATA-TYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Alternative Diagnosis Representation for the data defined by the means of a ApplicationPrimitiveDataType of category VALUE or BOOLEAN.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:9286c6f8-7530-da64-d5d2-866fe5ce9a49`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

########## 2. DemInternalDataValue

- **UUID**: `ECUC:1cdac6e1-ae2d-deed-d109-b64801472837`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

##### 29. DemTextTableMapping

**容器属性**:

- **UUID**: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemTextTableMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DemDiagnosisRepresentationDataValue

- **UUID**: `ECUC:9286c6f8-7530-da64-d5d2-866fe5ce9a49`
- **参数名**: `DemDiagnosisRepresentationDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The data value in the diagnosis representation.

######## 2. DemInternalDataValue

- **UUID**: `ECUC:1cdac6e1-ae2d-deed-d109-b64801472837`
- **参数名**: `DemInternalDataValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ECU internal data value.

##### 30. DemDataElementInstance

**容器属性**:

- **UUID**: `ECUC:1da3b6b3-d899-4105-96f5-eee7ed1ed32f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitive data in a port  where the data element is typed with an ApplicationPrimitveDataType or an ImplementationDataType.

###### 引用关系

此容器包含 **1** 个引用：

####### INSTANCE-REFERENCE 类型引用

######## 1. DemDataElementInstanceRef

- **UUID**: `ECUC:a420975a-5a17-48de-ad73-d7082549c962`
- **引用名**: `DemDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitive data which shall be read or written.

##### 31. DemSubElementInDataElementInstance

**容器属性**:

- **UUID**: `ECUC:5afd11aa-5406-45d4-b56a-6ea45ba3d010`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSubElementInDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ApplicationCompositeDataType.

###### 引用关系

此容器包含 **1** 个引用：

####### INSTANCE-REFERENCE 类型引用

######## 1. DemSubElementInDataElementInstanceRef

- **UUID**: `ECUC:6b0b0abb-b972-44f8-aae4-c32fcb78a982`
- **引用名**: `DemSubElementInDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port which shall be read or written.

##### 32. DemSubElementInImplDataElementInstance

**容器属性**:

- **UUID**: `ECUC:c8bd6556-b5be-4c93-9be9-37a70a4d8424`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSubElementInImplDataElementInstance`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.

###### 引用关系

此容器包含 **1** 个引用：

####### INSTANCE-REFERENCE 类型引用

######## 1. DemSubElementInImplDataElementInstanceRef

- **UUID**: `ECUC:ad862330-1bb1-40f6-816f-bf8b49e5c159`
- **引用名**: `DemSubElementInImplDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE-ELEMENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port which shall be read or written.

##### 33. DemInternalDataElementClass

**容器属性**:

- **UUID**: `ECUC:3169b35f-f938-49a0-976c-91300ae5037d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemInternalDataElementClass`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for an internal data element class.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DemDataElementDataSize

- **UUID**: `ECUC:2c592a33-d99b-45f2-9427-5f246a99524d`
- **参数名**: `DemDataElementDataSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the size of the data element in bytes.

####### ENUMERATION 类型参数

######## 1. DemInternalDataElement

- **UUID**: `ECUC:fe434fc3-1ebf-40e6-9b79-a20a65a9dcf8`
- **参数名**: `DemInternalDataElement`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_AGINGCTR_DOWNCNT` (来源: AUTOSAR_ECUC)
  - `DEM_AGINGCTR_UPCNT` (来源: AUTOSAR_ECUC)
  - `DEM_CURRENT_FDC` (来源: AUTOSAR_ECUC)
  - `DEM_CYCLES_SINCE_FIRST_FAILED` (来源: AUTOSAR_ECUC)
  - `DEM_CYCLES_SINCE_LAST_FAILED` (来源: AUTOSAR_ECUC)
  - `DEM_FAILED_CYCLES` (来源: AUTOSAR_ECUC)
  - `DEM_MAX_FDC_DURING_CURRENT_CYCLE` (来源: AUTOSAR_ECUC)
  - `DEM_MAX_FDC_SINCE_LAST_CLEAR` (来源: AUTOSAR_ECUC)
  - `DEM_OCCCTR` (来源: AUTOSAR_ECUC)
  - `DEM_OVFLIND` (来源: AUTOSAR_ECUC)
  - `DEM_SIGNIFICANCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Dem-internal data value, which is mapped to the data element.

##### 34. DemDidClass

**容器属性**:

- **UUID**: `ECUC:e1cbc150-3dd5-4439-abf5-ccb4cde025c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemDidClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for a data Id class. It is assembled out of one or several data elements.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DemDidIdentifier

- **UUID**: `ECUC:6fb72160-e0f8-4592-831c-05d34fe8c839`
- **参数名**: `DemDidIdentifier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Data ID.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. DemDidDataElementClassRef

- **UUID**: `ECUC:30a0fb20-847a-43b2-ad30-0df10d7c2f68`
- **引用名**: `DemDidDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..255]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

##### 35. DemEnableCondition

**容器属性**:

- **UUID**: `ECUC:490f6445-7fad-4f11-9130-c78155a7fbe6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemEnableCondition`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for enable conditions.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DemEnableConditionId

- **UUID**: `ECUC:8941da71-f206-4351-8887-40650a034533`
- **参数名**: `DemEnableConditionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a unique enable condition Id.

####### BOOLEAN 类型参数

######## 1. DemEnableConditionStatus

- **UUID**: `ECUC:7e66af51-7547-4ead-9cc8-9dd2c2f112fe`
- **参数名**: `DemEnableConditionStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the initial status for enable or disable of acceptance of event reports of a diagnostic event.

##### 36. DemEnableConditionGroup

**容器属性**:

- **UUID**: `ECUC:32a02fa5-08ff-4668-b2a6-bcc8066eccd1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemEnableConditionGroup`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for enable condition groups.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DemEnableConditionRef

- **UUID**: `ECUC:2efef637-5844-4dfc-984b-a96a59d045f2`
- **引用名**: `DemEnableConditionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DemEnableCondition`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemEnableCondition`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References an enable condition.

##### 37. DemExtendedDataClass

**容器属性**:

- **UUID**: `ECUC:9a005bc7-bfcc-476f-a2fa-1152a1793b12`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemExtendedDataClass`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This class contains the combinations of extended data records for an extended data class.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DemExtendedDataRecordClassRef

- **UUID**: `ECUC:76ed7707-7ef4-4a49-8502-1182d3997425`
- **引用名**: `DemExtendedDataRecordClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..253]
- **目标**: `DemExtendedDataRecordClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemExtendedDataRecordClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to an extended data class record.

##### 38. DemExtendedDataRecordClass

**容器属性**:

- **UUID**: `ECUC:6821e454-6d75-4f8b-a6c1-c1e0fdc5f8d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemExtendedDataRecordClass`
- **多重性**: [0..253]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for an extended data record class.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DemExtendedDataRecordNumber

- **UUID**: `ECUC:a403cf7b-c80e-4d4b-9e39-5805c8992866`
- **参数名**: `DemExtendedDataRecordNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter specifies an unique identifier for an extended data record.

####### ENUMERATION 类型参数

######## 1. DemExtendedDataRecordTrigger

- **UUID**: `ECUC:2c092a02-741b-4363-b677-051dfa118690`
- **参数名**: `DemExtendedDataRecordTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_EXTENDED_DATA_CAPTURE_ON_CONFIRMED` (来源: AUTOSAR_ECUC)
  - `DEM_EXTENDED_DATA_CAPTURE_ON_FDC_THRESHOLD` (来源: AUTOSAR_ECUC)
  - `DEM_EXTENDED_DATA_CAPTURE_ON_PENDING` (来源: AUTOSAR_ECUC)
  - `DEM_EXTENDED_DATA_CAPTURE_ON_TEST_FAILED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the primary trigger to allocate an event memory entry.

######## 2. DemExtendedDataRecordUpdate

- **UUID**: `ECUC:221029aa-5a23-40f4-b9e0-b01c16eb1ecb`
- **参数名**: `DemExtendedDataRecordUpdate`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_UPDATE_RECORD_NO` (来源: AUTOSAR_ECUC)
  - `DEM_UPDATE_RECORD_YES` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This extended data record is captured if the configured trigger condition in "DemExtendedDataRecordTrigger" is fulfilled.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. DemDataElementClassRef

- **UUID**: `ECUC:97567e6b-f870-4e8a-ba55-b05cfd081266`
- **引用名**: `DemDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..255]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

##### 39. DemFreezeFrameClass

**容器属性**:

- **UUID**: `ECUC:0dd242a0-90fd-4d71-9506-bcab60321bf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemFreezeFrameClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the combinations of DIDs for a non OBD relevant freeze frame class.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DemDidClassRef

- **UUID**: `ECUC:f641607d-0dcf-4d67-80a5-3fddd327023a`
- **引用名**: `DemDidClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DemDidClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDidClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For OBD relevant data

##### 40. DemFreezeFrameRecNumClass

**容器属性**:

- **UUID**: `ECUC:e2e5fbe0-d229-4de6-a9db-3c1d6cf37722`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemFreezeFrameRecNumClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains a list of dedicated, different freeze frame record numbers assigned to an event. The order of record numbers in this list is assigned to the chronological order of the according freeze frame records.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DemFreezeFrameRecordClassRef

- **UUID**: `ECUC:0c808701-e72e-45ab-9efe-233c0ea65198`
- **引用名**: `DemFreezeFrameRecordClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..254]
- **目标**: `DemFreezeFrameRecordClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemFreezeFrameRecordClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references record number(s) for a freeze frame record.

##### 41. DemFreezeFrameRecordClass

**容器属性**:

- **UUID**: `ECUC:243fd8af-15d0-4af1-99db-c610b201491b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemFreezeFrameRecordClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains a list of dedicated, different freeze frame record numbers.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DemFreezeFrameRecordNumber

- **UUID**: `ECUC:8577a18a-a211-451a-86ba-332c3c551648`
- **参数名**: `DemFreezeFrameRecordNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a record number for a freeze frame record. This record number is unique per freeze frame record number class.

####### ENUMERATION 类型参数

######## 1. DemFreezeFrameRecordTrigger

- **UUID**: `ECUC:4386a02e-28bd-4dc9-b99a-1829f34a1792`
- **参数名**: `DemFreezeFrameRecordTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_FREEZE_FRAME_CAPTURE_ON_CONFIRMED` (来源: AUTOSAR_ECUC)
  - `DEM_FREEZE_FRAME_CAPTURE_ON_FDC_THRESHOLD` (来源: AUTOSAR_ECUC)
  - `DEM_FREEZE_FRAME_CAPTURE_ON_PENDING` (来源: AUTOSAR_ECUC)
  - `DEM_FREEZE_FRAME_CAPTURE_ON_TEST_FAILED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the primary trigger to allocate an event memory entry.

######## 2. DemFreezeFrameRecordUpdate

- **UUID**: `ECUC:b96da489-b522-43af-8733-2894c87542da`
- **参数名**: `DemFreezeFrameRecordUpdate`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_UPDATE_RECORD_NO` (来源: AUTOSAR_ECUC)
  - `DEM_UPDATE_RECORD_YES` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the case, when the freeze frame record is stored/updated.

##### 42. DemGeneralJ1939

**容器属性**:

- **UUID**: `ECUC:b8f84dc2-a70a-4523-8c77-0cef2f837fbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemGeneralJ1939`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the general J1939-specific configuration (parameters) of the Dem module.

###### 参数配置

此容器包含 **9** 个参数：

####### BOOLEAN 类型参数

######## 1. DemJ1939ClearDtcSupport

- **UUID**: `ECUC:006b1cb5-b415-4364-a2de-9716bb0336eb`
- **参数名**: `DemJ1939ClearDtcSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether clearing J1939 DTCs (DM3 und DM11) is supported or not.

######## 2. DemJ1939Dm31Support

- **UUID**: `ECUC:12b38ba3-011d-436c-bc42-997b08968c93`
- **参数名**: `DemJ1939Dm31Support`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 DM31 is supported or not.

######## 3. DemJ1939ExpandedFreezeFrameSupport

- **UUID**: `ECUC:c3285bd5-b3d6-48de-a1a2-9d1e46424e94`
- **参数名**: `DemJ1939ExpandedFreezeFrameSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 expanded freeze frames are supported or not.

######## 4. DemJ1939FreezeFrameSupport

- **UUID**: `ECUC:6cbd5bf9-7d09-474b-93ac-870ea2b2c62d`
- **参数名**: `DemJ1939FreezeFrameSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 freeze frames are supported or not.

######## 5. DemJ1939RatioSupport

- **UUID**: `ECUC:60ea9ba9-0c2d-4cb4-8a29-0ef5482137fe`
- **参数名**: `DemJ1939RatioSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 performance ratios are supported or not.

######## 6. DemJ1939Readiness1Support

- **UUID**: `ECUC:7a872ae9-095f-42ca-8442-ab9448998fab`
- **参数名**: `DemJ1939Readiness1Support`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 diagnostic readiness 1 is supported or not.

######## 7. DemJ1939Readiness2Support

- **UUID**: `ECUC:081b4af4-1e48-412f-ac0b-bb549d8cdd64`
- **参数名**: `DemJ1939Readiness2Support`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 diagnostic readiness 2 is supported or not.

######## 8. DemJ1939Readiness3Support

- **UUID**: `ECUC:6f94320e-b403-48e1-9a7c-3c3c34518b32`
- **参数名**: `DemJ1939Readiness3Support`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 diagnostic readiness 3 is supported or not.

######## 9. DemJ1939ReadingDtcSupport

- **UUID**: `ECUC:3594bc2e-8726-44f8-b638-e5be99388147`
- **参数名**: `DemJ1939ReadingDtcSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration switch defines whether J1939 DTC readout is supported or not.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. DemAmberWarningLampIndicatorRef

- **UUID**: `ECUC:cedf27e6-b9f5-4c36-800f-eab98917ec18`
- **引用名**: `DemAmberWarningLampIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the indicator representing the AmberWarningLamp . This parameter may be used for ECUs supporting J1939.

######## 2. DemProtectLampIndicatorRef

- **UUID**: `ECUC:76cac18f-6be9-4b81-866c-5150aa610a5c`
- **引用名**: `DemProtectLampIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the indicator representing the ProtectLamp. This parameter may be used for ECUs supporting J1939.

######## 3. DemRedStopLampIndicatorRef

- **UUID**: `ECUC:7f4fc974-67c0-418f-b4a7-d09d62b6c85e`
- **引用名**: `DemRedStopLampIndicatorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DemIndicator`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemIndicator`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the indicator representing the RedStopLamp. This parameter may be used for ECUs supporting J1939.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. DemCallbackJ1939DTCStatusChanged

**容器属性**:

- **UUID**: `ECUC:0d124437-dcbb-45fc-b7fb-75077766d0bf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackJ1939DTCStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback, which the Dem will call to notify other components about the change in the status of a DTC.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackDTCStatusChangedFnc

- **UUID**: `ECUC:51d9c5c0-bb7f-4566-be08-1f2181bda434`
- **参数名**: `DemCallbackDTCStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "DTCStatusChanged".

####### 2. DemJ1939FreezeFrameClass

**容器属性**:

- **UUID**: `ECUC:86700f99-a606-494e-ae36-cee1fcd4331d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemJ1939FreezeFrameClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the combinations of SPNs s for a J1939 relevant freeze frame.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DemSPNClassRef

- **UUID**: `ECUC:eaead167-1f62-4a5c-bc75-25f40d834faa`
- **引用名**: `DemSPNClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DemSPNClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemGeneralJ1939/DemSPNClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an SPN. This reference defines requiresIndex = true since it represents a ordered list of references where the order describes the order of single SPNs in the J1939 Freeze Frame.

####### 3. DemSPNClass

**容器属性**:

- **UUID**: `ECUC:d77f4ee8-fef8-4b89-a725-1253893ad24a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSPNClass`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for a SPN.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DemSPNId

- **UUID**: `ECUC:2716b2e8-64bd-491e-8fad-735bc797fcd2`
- **参数名**: `DemSPNId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..524287]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Suspect parameter number

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. DemSPNDataElementClassRef

- **UUID**: `ECUC:1a039457-9359-433b-8fec-561253267c68`
- **引用名**: `DemSPNDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

##### 43. DemCallbackJ1939DTCStatusChanged

**容器属性**:

- **UUID**: `ECUC:0d124437-dcbb-45fc-b7fb-75077766d0bf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackJ1939DTCStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback, which the Dem will call to notify other components about the change in the status of a DTC.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DemCallbackDTCStatusChangedFnc

- **UUID**: `ECUC:51d9c5c0-bb7f-4566-be08-1f2181bda434`
- **参数名**: `DemCallbackDTCStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "DTCStatusChanged".

##### 44. DemJ1939FreezeFrameClass

**容器属性**:

- **UUID**: `ECUC:86700f99-a606-494e-ae36-cee1fcd4331d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemJ1939FreezeFrameClass`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the combinations of SPNs s for a J1939 relevant freeze frame.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DemSPNClassRef

- **UUID**: `ECUC:eaead167-1f62-4a5c-bc75-25f40d834faa`
- **引用名**: `DemSPNClassRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DemSPNClass`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemGeneralJ1939/DemSPNClass`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an SPN. This reference defines requiresIndex = true since it represents a ordered list of references where the order describes the order of single SPNs in the J1939 Freeze Frame.

##### 45. DemSPNClass

**容器属性**:

- **UUID**: `ECUC:d77f4ee8-fef8-4b89-a725-1253893ad24a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemSPNClass`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for a SPN.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DemSPNId

- **UUID**: `ECUC:2716b2e8-64bd-491e-8fad-735bc797fcd2`
- **参数名**: `DemSPNId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..524287]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Suspect parameter number

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. DemSPNDataElementClassRef

- **UUID**: `ECUC:1a039457-9359-433b-8fec-561253267c68`
- **引用名**: `DemSPNDataElementClassRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a data element class.

##### 46. DemGeneralOBD

**容器属性**:

- **UUID**: `ECUC:dc39405f-19df-4342-bf96-7955053c295f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemGeneralOBD`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the general OBD-specific configuration (parameters) of the Dem module.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. DemOBDCompliancy

- **UUID**: `ECUC:cfcbf5d3-1309-4a84-ac7c-247c321b34f1`
- **参数名**: `DemOBDCompliancy`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration value to define  the appropriate value to PID$1C "OBD requirements to which vehicle or engine is certified." according to the respective standards, e.g. OBD, OBDII, JOBD etc.

####### BOOLEAN 类型参数

######## 1. DemOBDCentralizedPID21Handling

- **UUID**: `ECUC:dcb3a818-296a-471f-944a-382dbe24efa3`
- **参数名**: `DemOBDCentralizedPID21Handling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to enable the centralized handling of PID $21.

######## 2. DemOBDCentralizedPID31Handling

- **UUID**: `ECUC:fd5a0bb6-54d2-4124-85b4-316cc364f4f3`
- **参数名**: `DemOBDCentralizedPID31Handling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to enable the centralized handling of PID $31.

######## 3. DemOBDEventDisplacement

- **UUID**: `ECUC:2b92632d-3dbf-4fc6-b488-3786c582eb80`
- **参数名**: `DemOBDEventDisplacement`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate a different displacement behavior for OBD events.

####### ENUMERATION 类型参数

######## 1. DemOBDDestinationOfEvents

- **UUID**: `ECUC:6fe71c89-ac19-4ddb-91b7-39582c4f59c6`
- **参数名**: `DemOBDDestinationOfEvents`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_DTC_ORIGIN_PRIMARY_MEMORY` (来源: AUTOSAR_ECUC)
  - `DEM_DTC_ORIGIN_SECONDARY_MEMORY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The destination of events assigns where the OBD events shall be stored.

###### 引用关系

此容器包含 **9** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. DemOBDInputAcceleratorPedalInformation

- **UUID**: `ECUC:4e99443b-59a7-4f36-a2da-6bd7fca7143a`
- **引用名**: `DemOBDInputAcceleratorPedalInformation`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the accelerator padal information, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

######## 2. DemOBDInputAmbientPressure

- **UUID**: `ECUC:e7436253-fc7b-40af-856e-3843edd48fc4`
- **引用名**: `DemOBDInputAmbientPressure`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the ambient pressure, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

######## 3. DemOBDInputAmbientTemperature

- **UUID**: `ECUC:d21feba4-8962-41c4-b8a3-14bb9ee2b13e`
- **引用名**: `DemOBDInputAmbientTemperature`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the ambient temperature, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

######## 4. DemOBDInputDistanceInformation

- **UUID**: `ECUC:e4405450-1973-437f-9a72-6b4f3c1d6f30`
- **引用名**: `DemOBDInputDistanceInformation`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the distance information, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

######## 5. DemOBDInputEngineSpeed

- **UUID**: `ECUC:3c88edb4-d1bc-439d-a059-ae046bb4da25`
- **引用名**: `DemOBDInputEngineSpeed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the engine speed, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

######## 6. DemOBDInputEngineTemperature

- **UUID**: `ECUC:a77d2964-9355-4869-83f4-2f929f570dec`
- **引用名**: `DemOBDInputEngineTemperature`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the engine temperature, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

######## 7. DemOBDInputProgrammingEvent

- **UUID**: `ECUC:855ef6a6-5c64-4498-b6e8-a8f2b2aacc5d`
- **引用名**: `DemOBDInputProgrammingEvent`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the programming event, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

######## 8. DemOBDInputVehicleSpeed

- **UUID**: `ECUC:5256078f-f457-473b-945f-24f415eb398e`
- **引用名**: `DemOBDInputVehicleSpeed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the vehicle speed, which is assigned to a specific data element used as interface for the Dem-internal PID calculations.

######## 9. DemOBDTimeSinceEngineStart

- **UUID**: `ECUC:2edc7ce5-2f3c-4ce3-a381-1feb57738843`
- **引用名**: `DemOBDTimeSinceEngineStart`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalCSDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemExternalSRDataElementClass`
  - `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemDataElementClass/DemInternalDataElementClass`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Input variable for the Time Since Engine Start information, which is assigned to a specific data element.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DemCallbackOBDDTCStatusChanged

**容器属性**:

- **UUID**: `ECUC:bb68bdbd-d314-4379-a7f5-797f07f6fab0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackOBDDTCStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback, which the Dem will call to notify other components about the change in the status of a DTC.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. DemCallbackDTCStatusChangedFnc

- **UUID**: `ECUC:d8e3c461-3103-4e19-8243-a9ad31b83d65`
- **参数名**: `DemCallbackDTCStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "DTCStatusChanged".

##### 47. DemCallbackOBDDTCStatusChanged

**容器属性**:

- **UUID**: `ECUC:bb68bdbd-d314-4379-a7f5-797f07f6fab0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemCallbackOBDDTCStatusChanged`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback, which the Dem will call to notify other components about the change in the status of a DTC.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. DemCallbackDTCStatusChangedFnc

- **UUID**: `ECUC:d8e3c461-3103-4e19-8243-a9ad31b83d65`
- **参数名**: `DemCallbackDTCStatusChangedFnc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function name of prototype "DTCStatusChanged".

##### 48. DemGroupOfDTC

**容器属性**:

- **UUID**: `ECUC:c89875f9-acf6-428b-9a00-4c3f2c8afe19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemGroupOfDTC`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for DTC groups.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DemGroupDTCs

- **UUID**: `ECUC:2e622411-01bb-411b-90b1-6c0947dbad48`
- **参数名**: `DemGroupDTCs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..16777214]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: DTC value of the selected group of DTC

##### 49. DemIndicator

**容器属性**:

- **UUID**: `ECUC:3d9ac4b7-4eb9-4ac6-b433-30b5b6fa9fe9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemIndicator`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for Indicators.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DemIndicatorID

- **UUID**: `ECUC:7b5c78d8-ffb6-478c-a521-a8ebfeb21b00`
- **参数名**: `DemIndicatorID`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier of an indicator.

##### 50. DemNvRamBlockId

**容器属性**:

- **UUID**: `ECUC:3ab8406f-9f71-44c9-8200-0c9baf37a90a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemNvRamBlockId`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for a non-volatile memory block, which is used from the Dem. If no permanent storage of event memory entries is required, no block needs to be configured.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. DemNvRamBlockIdRef

- **UUID**: `ECUC:3dfa5a10-bb40-4111-9e8d-653298123dfc`
- **引用名**: `DemNvRamBlockIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a non-volatile memory block. For post build time configurations worst case scenario shall be used.

##### 51. DemOperationCycle

**容器属性**:

- **UUID**: `ECUC:edf2c803-842d-44ee-91cf-76c67f209935`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemOperationCycle`
- **多重性**: [1..256]
- **多配置容器**: false

**容器描述**:

Note that this container definition does not explicitly define a symbolic name parameter. Instead, the short name of the container will be used in the Ecu Configuration Description to specify the symbolic name of the operation cycle name.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. DemOperationCycleAutomaticEnd

- **UUID**: `ECUC:bd53f3b5-1f03-41df-b65a-5a892484e08c`
- **参数名**: `DemOperationCycleAutomaticEnd`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If DemOperationCycleAutomaticEnd is configured to TRUE, Dem shall automatically end the driving cycle at either Dem_Shutdown() or Dem_Init().

######## 2. DemOperationCycleAutostart

- **UUID**: `ECUC:99ec8223-f61d-498a-b636-fdd2b87159a9`
- **参数名**: `DemOperationCycleAutostart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The autostart property defines if the operation cycles is automatically (re-)started during Dem_PreInit.

####### ENUMERATION 类型参数

######## 1. DemOperationCycleType

- **UUID**: `ECUC:7544f8ce-f35f-4335-b2da-a0144b7c0dce`
- **参数名**: `DemOperationCycleType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_OPCYC_IGNITION` (来源: AUTOSAR_ECUC)
  - `DEM_OPCYC_OBD_DCY` (来源: AUTOSAR_ECUC)
  - `DEM_OPCYC_OTHER` (来源: AUTOSAR_ECUC)
  - `DEM_OPCYC_POWER` (来源: AUTOSAR_ECUC)
  - `DEM_OPCYC_TIME` (来源: AUTOSAR_ECUC)
  - `DEM_OPCYC_WARMUP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Operation cycles types for the Dem to be supported by cycle-state APIs.

##### 52. DemRatio

**容器属性**:

- **UUID**: `ECUC:bd1f9289-8c44-4164-9c8c-385ab2d911b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemRatio`
- **多重性**: [0..65535]
- **多配置容器**: false

**容器描述**:

This container contains the OBD-specific in-use-monitor performance ratio configuration.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. DemRatioId

- **UUID**: `ECUC:25cf98a3-6dce-490d-a2f1-8a73b51507ad`
- **参数名**: `DemRatioId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a unique ratio Id.

####### ENUMERATION 类型参数

######## 1. DemIUMPRDenGroup

- **UUID**: `ECUC:f97b47cb-864b-4aef-beae-173913703bd0`
- **参数名**: `DemIUMPRDenGroup`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_IUMPR_DEN_500MILL` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_DEN_COLDSTART` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_DEN_EVAP` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_DEN_NONE` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_DEN_PHYS_API` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the assigned denominator type which is applied in addition to the General Denominator conditions.

######## 2. DemIUMPRGroup

- **UUID**: `ECUC:6210985c-4380-4b4b-adba-d12b8c40365f`
- **参数名**: `DemIUMPRGroup`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_IUMPR_BOOSTPRS` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_CAT1` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_CAT2` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_EGR` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_EGSENSOR` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_EVAP` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_FLSYS` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_NMHCCAT` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_NOXADSORB` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_NOXCAT` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_OXS1` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_OXS2` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_PMFILTER` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_PRIVATE` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_SAIR` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_SECOXS1` (来源: AUTOSAR_ECUC)
  - `DEM_IUMPR_SECOXS2` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the assigned IUMPR group of the ratio Id.

######## 3. DemRatioKind

- **UUID**: `ECUC:5b7f3369-b175-4235-bd33-5f46fe1078d9`
- **参数名**: `DemRatioKind`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEM_RATIO_API` (来源: AUTOSAR_ECUC)
  - `DEM_RATIO_OBSERVER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the ratio will be calculated API or observer based.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. DemDiagnosticEventRef

- **UUID**: `ECUC:e4a17661-b438-44c2-b250-9d97e9cda20d`
- **引用名**: `DemDiagnosticEventRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a diagnostic event.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. DemFunctionIdRef

- **UUID**: `ECUC:36c5505e-2322-474d-8979-f5ca259d394d`
- **引用名**: `DemFunctionIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FiMFID`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMFID`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a function identifier within the FiM which is used as a primary FID.

######## 2. DemSecondaryFunctionIdRef

- **UUID**: `ECUC:48718548-1795-412d-a803-72c0e418f233`
- **引用名**: `DemSecondaryFunctionIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `FiMFID`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMFID`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference contains the link to a function identifier within the FiM which is used as a secondary FID.

##### 53. DemStorageCondition

**容器属性**:

- **UUID**: `ECUC:5f232bac-fe27-4d30-b072-1795f9af7ef6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemStorageCondition`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for storage conditions.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DemStorageConditionId

- **UUID**: `ECUC:67e309bf-b4b9-4de5-b0d1-47df01d36b84`
- **参数名**: `DemStorageConditionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a unique storage condition Id. This parameter should not be changeable by user, because the Id should be generated by Dem itself to prevent gaps and multiple use of an Id. The storage conditions should be sequentially ordered beginning with 0 and no gaps in between.

####### BOOLEAN 类型参数

######## 1. DemStorageConditionStatus

- **UUID**: `ECUC:57bb12c8-1d23-4314-a9fa-d0cb5116322f`
- **参数名**: `DemStorageConditionStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the initial status for enable or disable of storage of a diagnostic event.

##### 54. DemStorageConditionGroup

**容器属性**:

- **UUID**: `ECUC:713b95f5-b501-4a30-91c8-cedbe4ba692b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemStorageConditionGroup`
- **多重性**: [0..255]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for storage condition groups.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DemStorageConditionRef

- **UUID**: `ECUC:94a93959-aae2-416d-a59a-bd0fae591f32`
- **引用名**: `DemStorageConditionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..255]
- **目标**: `DemStorageCondition`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemGeneral/DemStorageCondition`
- **来源**: AUTOSAR_ECUC V1.0.0
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References an enable condition.

##### 55. DemClient

**容器属性**:

- **UUID**: `ECUC:5d3c6e4a-6c4c-4754-b120-000eb60702c2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DemClient`
- **多重性**: [1..255]

**容器描述**:

This container contains possible clients that are using the Dem APIs.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DemClientId

- **UUID**: `ECUC:06c5d156-e093-420c-a281-d73b792ba3f9`
- **参数名**: `DemClientId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Defines a unique identifier for a Dem client. This number is used by this client in the ClientID parameter in all API with this parameter.

##### 56. DemDebounceAlgorithmClass

**容器属性**:

- **UUID**: `ECUC:98a5d79e-8975-48e4-bbc8-a174596e2dbb`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDebounceAlgorithmClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDebounceCounterBased**
  - UUID: `ECUC:c20d7e84-9b93-4776-a3db-24113379f5f4`
  - 描述: This container contains the configuration (parameters) for counter based debouncing.
- **DemDebounceMonitorInternal**
  - UUID: `ECUC:cc0801d6-d390-4989-80bf-e5bf1d2832b6`
  - 描述: This container contains the configuration (parameters) for monitor internal debouncing.
- **DemCallbackGetFDC**
  - UUID: `ECUC:82f362d0-6c6f-47ea-b760-c561850bcfa2`
  - 描述: The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter" callback, which the Dem will call to obtain the value of the fault detection counter.
- **DemDebounceTimeBase**
  - UUID: `ECUC:498c5d2e-12d2-43c7-8892-9bb11701a6aa`
  - 描述: This container contains the configuration (parameters) for time based debouncing.

**容器描述**:

Debounce algorithm class: counter based, time based, or monitor internal.

##### 57. DemDataElementClass

**容器属性**:

- **UUID**: `ECUC:6505a151-66bd-4283-b004-9f267f7ce44e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDataElementClass`
- **多重性**: [0..255]

**容器选择**:

- **DemExternalCSDataElementClass**
  - UUID: `ECUC:731531ff-e865-4793-887a-8064686ae7d1`
  - 描述: This container contains the configuration (parameters) for an external client/server based data element class.
- **DemExternalSRDataElementClass**
  - UUID: `ECUC:8e6c8d7e-2a1f-44a9-a5cf-728b1478f58d`
  - 描述: This container contains the configuration (parameters) for an external sender/receiver based data element class. It defines, how the Dem can obtain the value of the data element from a SW-C, by using a sender/receiver port.
- **DemAlternativeDataInterface**
  - UUID: `ECUC:c494d1bc-6807-4116-868f-139fc9d4056c`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of a VariableDataPrototoype in a DataInterface.
- **DemAlternativeDataProps**
  - UUID: `ECUC:3b554f3d-00a7-4269-b499-bed18222a6e6`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of ECU configuration parameters.
- **DemLinearScale**
  - UUID: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
  - 描述: This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.
- **DemTextTableMapping**
  - UUID: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.
- **DemAlternativeDataType**
  - UUID: `ECUC:f403e75d-f752-4e3d-aa66-4d086335d59f`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of an ApplicationDataType.
- **DemTextTableMapping**
  - UUID: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.
- **DemDataElementInstance**
  - UUID: `ECUC:1da3b6b3-d899-4105-96f5-eee7ed1ed32f`
  - 描述: Instance Reference to the primitive data in a port  where the data element is typed with an ApplicationPrimitveDataType or an ImplementationDataType.
- **DemSubElementInDataElementInstance**
  - UUID: `ECUC:5afd11aa-5406-45d4-b56a-6ea45ba3d010`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ApplicationCompositeDataType.
- **DemSubElementInImplDataElementInstance**
  - UUID: `ECUC:c8bd6556-b5be-4c93-9be9-37a70a4d8424`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.
- **DemInternalDataElementClass**
  - UUID: `ECUC:3169b35f-f938-49a0-976c-91300ae5037d`
  - 描述: This container contains the configuration (parameters) for an internal data element class.

**容器描述**:

This container contains the configuration (parameters) for an internal/external data element class.

##### 58. DemDiagnosisScaling

**容器属性**:

- **UUID**: `ECUC:1113d69e-4b70-4756-bea7-2f74de625fcf`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemDiagnosisScaling`
- **多重性**: [0..1]

**容器选择**:

- **DemAlternativeDataInterface**
  - UUID: `ECUC:c494d1bc-6807-4116-868f-139fc9d4056c`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of a VariableDataPrototoype in a DataInterface.
- **DemAlternativeDataProps**
  - UUID: `ECUC:3b554f3d-00a7-4269-b499-bed18222a6e6`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of ECU configuration parameters.
- **DemLinearScale**
  - UUID: `ECUC:3543b2d3-c856-4976-815e-fd332f298fe3`
  - 描述: This container contains the configuration (parameters) of an linear scale of the alternative Diagnosis Representation.
- **DemTextTableMapping**
  - UUID: `ECUC:e937ef32-d52e-83a0-35ca-28d3ad8b7723`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.
- **DemAlternativeDataType**
  - UUID: `ECUC:f403e75d-f752-4e3d-aa66-4d086335d59f`
  - 描述: This container contains the configuration (parameters) of an alternative Diagnosis Representation by the means of an ApplicationDataType.
- **DemTextTableMapping**
  - UUID: `ECUC:a1e68753-cbd9-8f74-2b96-b70a8e9ea5dc`
  - 描述: This container contains the configuration (parameters) of the mapping a DataPrototype typed by AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

**容器描述**:

This container contains the configuration (parameters) of an alternative Diagnosis Representation. Out if this the scaling between Diagnosis and ECU internal representation and vice versa can be calculated.

##### 59. DemSRDataElementClass

**容器属性**:

- **UUID**: `ECUC:cbfb18d6-1749-45e0-833d-34d9d30215d4`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DemSRDataElementClass`
- **多重性**: [1..1]

**容器选择**:

- **DemDataElementInstance**
  - UUID: `ECUC:1da3b6b3-d899-4105-96f5-eee7ed1ed32f`
  - 描述: Instance Reference to the primitive data in a port  where the data element is typed with an ApplicationPrimitveDataType or an ImplementationDataType.
- **DemSubElementInDataElementInstance**
  - UUID: `ECUC:5afd11aa-5406-45d4-b56a-6ea45ba3d010`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ApplicationCompositeDataType.
- **DemSubElementInImplDataElementInstance**
  - UUID: `ECUC:c8bd6556-b5be-4c93-9be9-37a70a4d8424`
  - 描述: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.

**容器描述**:

This container defines the source of data in a provided port which shall be read for a external data element

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

1. **Dem**
