# Sd - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:56

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Sd](#sd)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Sd

#### 基本信息

- **UUID**: `ECUC:c615f2af-7fcc-4347-b3df-17f203284f1d`
- **模块名称**: `Sd`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Service Discovery module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.4.0

- **发布日期**: 2013-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **21** 个配置容器：

##### 1. SdConfig

**容器属性**:

- **UUID**: `ECUC:130bd546-f092-45a3-b09e-073504d54f03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR Service Discovery module. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 配置容器

本模块包含 **19** 个配置容器：

####### 1. SdInstance

**容器属性**:

- **UUID**: `ECUC:3c4bbbc4-1c53-4234-a90c-9373ba4d3f3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstance`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container represents an instance of the SD; i.e. the SD configuration for a certain link.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. SdInstanceHostname

- **UUID**: `ECUC:ae63ecde-952c-49e6-a911-49c039a553d3`
- **参数名**: `SdInstanceHostname`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to specify the Hostname.

######## 配置容器

本模块包含 **18** 个配置容器：

######### 1. SdClientService

**容器属性**:

- **UUID**: `ECUC:f68e3db6-757e-43b3-9103-2f606844e25c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientService`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all parameters used by Client services.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. SdClientServiceHandleId

- **UUID**: `ECUC:e55d49c4-21ba-4b1c-8dbd-5d33c6c343c0`
- **参数名**: `SdClientServiceHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this Client Service Instance.

############ 2. SdClientServiceId

- **UUID**: `ECUC:55150245-ac37-4a34-bf4a-cd44c7d77ee7`
- **参数名**: `SdClientServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id to identify the service. This is unique for the service interface.

############ 3. SdClientServiceInstanceId

- **UUID**: `ECUC:89e8e56f-96f8-4a54-9229-0b15538df8ba`
- **参数名**: `SdClientServiceInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to specify Instance Id of the service as used in SD entries.

############ 4. SdClientServiceMajorVersion

- **UUID**: `ECUC:76ba4bba-a54e-4a52-b129-57fe3959dd5c`
- **参数名**: `SdClientServiceMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Major version number of the Service as used in the SD entries.

############ 5. SdClientServiceMinorVersion

- **UUID**: `ECUC:def32508-2c8f-49f2-bc83-24607c4befef`
- **参数名**: `SdClientServiceMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minor version number of the Service as used in the SD Service Entries.

########### BOOLEAN 类型参数

############ 1. SdClientServiceAutoRequire

- **UUID**: `ECUC:b0aefe0b-0801-4486-8807-37c44397bf5a`
- **参数名**: `SdClientServiceAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this Service will be set to "required" on start.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SdClientServiceTimerRef

- **UUID**: `ECUC:50712e7a-7cf2-42a0-b9bf-0c74635c7890`
- **引用名**: `SdClientServiceTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this service.

########## 配置容器

本模块包含 **4** 个配置容器：

########### 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:aac361f2-7417-8d40-2c11-28fd180bafe0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:036b1450-e10e-d0f7-e2e4-4591149fe6db`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:62783abe-e3b8-d599-c2f1-9a4db2fed89d`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

########### 2. SdConsumedEventGroup

**容器属性**:

- **UUID**: `ECUC:83329fec-a819-451e-96f0-64151aa3524a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedEventGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

A Service may have event groups which can be consumed. A service consumer has to subscribe to the corresponding event-group. After the subscription the event consumer takes the role of a server and the event provider that of a client.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. SdConsumedEventGroupHandleId

- **UUID**: `ECUC:9f56182e-3725-4353-afd4-b8ba2347ec42`
- **参数名**: `SdConsumedEventGroupHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

############## 2. SdConsumedEventGroupId

- **UUID**: `ECUC:505b0b9e-3cc1-4549-bb8b-47e02ee0c7d6`
- **参数名**: `SdConsumedEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Eventgroup Id of this eventGroup as a unique identifier of the eventgroup in this service. This identifier is used for EventGroup entries as well.

############# BOOLEAN 类型参数

############## 1. SdConsumedEventGroupAutoRequire

- **UUID**: `ECUC:ba0a63f1-7167-438d-8854-3b0ad958e3c4`
- **参数名**: `SdConsumedEventGroupAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "required" on start.

############ 引用关系

此容器包含 **4** 个引用：

############# REFERENCE 类型引用

############## 1. SdConsumedEventGroupTimerRef

- **UUID**: `ECUC:c3bd7117-3c06-4440-ba51-604e0969d72e`
- **引用名**: `SdConsumedEventGroupTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this eventGroup.

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdConsumedEventGroupMulticastActivationRef

- **UUID**: `ECUC:44ad17a6-751c-42a5-98b1-f061bd1ef9bd`
- **引用名**: `SdConsumedEventGroupMulticastActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of a Routing Group in order to activate and setup the Socket Connection for Multicast Events of this EventGroup. The multicast address from the received Multicast option is setup by SoAd_RequestIpAddrAssignment.

############## 2. SdConsumedEventGroupTcpActivationRef

- **UUID**: `ECUC:cc5bdf5c-9c41-4731-813b-675d5de9f72e`
- **引用名**: `SdConsumedEventGroupTcpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving TCP events.

############## 3. SdConsumedEventGroupUdpActivationRef

- **UUID**: `ECUC:741ee45e-e2c6-48da-aa09-ef7bd1361513`
- **引用名**: `SdConsumedEventGroupUdpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving UDP events.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############## 参数配置

此容器包含 **2** 个参数：

############### STRING 类型参数

################ 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

################ 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

########### 3. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

########### 4. SdConsumedMethods

**容器属性**:

- **UUID**: `ECUC:9df5f68a-cff8-4c24-9d91-ab14d93739d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the data path for accessing the server methods.

############ 引用关系

此容器包含 **3** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdClientServiceActivationRef

- **UUID**: `ECUC:312665e5-3bbf-42cc-a0d6-2cfcb81e2f75`
- **引用名**: `SdClientServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroupRef to activate/deactivate the data path for the methods.

############## 2. SdClientServiceTcpRef

- **UUID**: `ECUC:bd317a9e-01ab-44f2-9361-55f035da9043`
- **引用名**: `SdClientServiceTcpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (TCP) for communication with methods.

############## 3. SdClientServiceUdpRef

- **UUID**: `ECUC:bccf7329-9e29-44af-be83-148ca6537803`
- **引用名**: `SdClientServiceUdpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (UDP) for communication with methods.

######### 2. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:aac361f2-7417-8d40-2c11-28fd180bafe0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:036b1450-e10e-d0f7-e2e4-4591149fe6db`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:62783abe-e3b8-d599-c2f1-9a4db2fed89d`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 3. SdConsumedEventGroup

**容器属性**:

- **UUID**: `ECUC:83329fec-a819-451e-96f0-64151aa3524a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedEventGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

A Service may have event groups which can be consumed. A service consumer has to subscribe to the corresponding event-group. After the subscription the event consumer takes the role of a server and the event provider that of a client.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. SdConsumedEventGroupHandleId

- **UUID**: `ECUC:9f56182e-3725-4353-afd4-b8ba2347ec42`
- **参数名**: `SdConsumedEventGroupHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

############ 2. SdConsumedEventGroupId

- **UUID**: `ECUC:505b0b9e-3cc1-4549-bb8b-47e02ee0c7d6`
- **参数名**: `SdConsumedEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Eventgroup Id of this eventGroup as a unique identifier of the eventgroup in this service. This identifier is used for EventGroup entries as well.

########### BOOLEAN 类型参数

############ 1. SdConsumedEventGroupAutoRequire

- **UUID**: `ECUC:ba0a63f1-7167-438d-8854-3b0ad958e3c4`
- **参数名**: `SdConsumedEventGroupAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "required" on start.

########## 引用关系

此容器包含 **4** 个引用：

########### REFERENCE 类型引用

############ 1. SdConsumedEventGroupTimerRef

- **UUID**: `ECUC:c3bd7117-3c06-4440-ba51-604e0969d72e`
- **引用名**: `SdConsumedEventGroupTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this eventGroup.

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdConsumedEventGroupMulticastActivationRef

- **UUID**: `ECUC:44ad17a6-751c-42a5-98b1-f061bd1ef9bd`
- **引用名**: `SdConsumedEventGroupMulticastActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of a Routing Group in order to activate and setup the Socket Connection for Multicast Events of this EventGroup. The multicast address from the received Multicast option is setup by SoAd_RequestIpAddrAssignment.

############ 2. SdConsumedEventGroupTcpActivationRef

- **UUID**: `ECUC:cc5bdf5c-9c41-4731-813b-675d5de9f72e`
- **引用名**: `SdConsumedEventGroupTcpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving TCP events.

############ 3. SdConsumedEventGroupUdpActivationRef

- **UUID**: `ECUC:741ee45e-e2c6-48da-aa09-ef7bd1361513`
- **引用名**: `SdConsumedEventGroupUdpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving UDP events.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 4. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 5. SdConsumedMethods

**容器属性**:

- **UUID**: `ECUC:9df5f68a-cff8-4c24-9d91-ab14d93739d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the data path for accessing the server methods.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdClientServiceActivationRef

- **UUID**: `ECUC:312665e5-3bbf-42cc-a0d6-2cfcb81e2f75`
- **引用名**: `SdClientServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroupRef to activate/deactivate the data path for the methods.

############ 2. SdClientServiceTcpRef

- **UUID**: `ECUC:bd317a9e-01ab-44f2-9361-55f035da9043`
- **引用名**: `SdClientServiceTcpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (TCP) for communication with methods.

############ 3. SdClientServiceUdpRef

- **UUID**: `ECUC:bccf7329-9e29-44af-be83-148ca6537803`
- **引用名**: `SdClientServiceUdpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (UDP) for communication with methods.

######### 6. SdClientTimer

**容器属性**:

- **UUID**: `ECUC:c443f1b3-de9c-4af4-8002-1dd9afaf083b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientTimer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all timers used by the Service Discovery module for Client Services.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. SdClientTimerInitialFindRepetitionsMax

- **UUID**: `ECUC:3d026bb0-8af3-498a-9c13-ea6881c55780`
- **参数名**: `SdClientTimerInitialFindRepetitionsMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration for the maximum number of find repetitions. This parameter is mandatory for ClientService.

############ 2. SdClientTimerTTL

- **UUID**: `ECUC:68fd030c-092e-45b6-9510-b120cdcc8054`
- **参数名**: `SdClientTimerTTL`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16777215]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time to live for find and subscribe messages.

########### FLOAT 类型参数

############ 1. SdClientTimerInitialFindDelayMax

- **UUID**: `ECUC:1a21c6e5-384a-4e0d-9629-c2c8818e3853`
- **参数名**: `SdClientTimerInitialFindDelayMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max value in [s] to delay randomly the transmission of a find message. This parameter is mandatory for ClientService.

############ 2. SdClientTimerInitialFindDelayMin

- **UUID**: `ECUC:d9c73e19-0364-4c48-9879-8db8d02ab112`
- **参数名**: `SdClientTimerInitialFindDelayMin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Min value in [s] to delay randomly the transmission of a find message. This parameter is mandatory for ClientService.

############ 3. SdClientTimerInitialFindRepetitionsBaseDelay

- **UUID**: `ECUC:8e1d6e7e-9f2d-418a-905e-de3054e5331f`
- **参数名**: `SdClientTimerInitialFindRepetitionsBaseDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The base delay in [s] for find repetitions. Successive finds have an exponential back off delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory for ClientService.

############ 4. SdClientTimerRequestResponseMaxDelay

- **UUID**: `ECUC:6b73d0a8-21a2-426f-8b4b-416d9349c512`
- **参数名**: `SdClientTimerRequestResponseMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum allowable response delay to entries received by multicast in seconds. This parameter is mandatory for ConsumedEventGroups.

############ 5. SdClientTimerRequestResponseMinDelay

- **UUID**: `ECUC:c19c4138-80e9-4299-b797-f94616832cb8`
- **参数名**: `SdClientTimerRequestResponseMinDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum allowable response delay to the find message in seconds. This parameter is mandatory for ConsumedEventGroups.

######### 7. SdInstanceMulticastRxPdu

**容器属性**:

- **UUID**: `ECUC:bea12c80-f2e7-436e-8b0c-84c85b798f0f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceMulticastRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the received PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SdRxPduId

- **UUID**: `ECUC:1be8da89-4233-4359-aa0c-af5ab04dbec1`
- **参数名**: `SdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received via the API Sd_SoAdIfRxIndication().

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SdRxPduRef

- **UUID**: `ECUC:98ef8aa7-6ae3-46cc-aa15-16489eaf952e`
- **引用名**: `SdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 8. SdInstanceTxPdu

**容器属性**:

- **UUID**: `ECUC:9860bb63-3785-4422-9f84-c1ebed9be61a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceTxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the transmitted PDU.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SdTxPduRef

- **UUID**: `ECUC:6d7b96cb-5291-42d9-9f11-18526e08f918`
- **引用名**: `SdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 9. SdInstanceUnicastRxPdu

**容器属性**:

- **UUID**: `ECUC:2c61fb83-0189-4677-b735-a69f39ddf17e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceUnicastRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the received PDU.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SdRxPduId

- **UUID**: `ECUC:60ade062-f122-45e5-b8e3-5ee8dd3e5742`
- **参数名**: `SdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received via the API Sd_SoAdIfRxIndication().

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SdRxPduRef

- **UUID**: `ECUC:0665655e-b25c-45a0-b5f6-f29616d77fd7`
- **引用名**: `SdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 10. SdServerService

**容器属性**:

- **UUID**: `ECUC:73a79f80-245a-4417-9d68-1307e90f6f60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerService`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all parameters used by Server services.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. SdServerServiceHandleId

- **UUID**: `ECUC:ce2a7cd7-64ff-4d90-916b-ba896157fa67`
- **参数名**: `SdServerServiceHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this Server Service Instance.

############ 2. SdServerServiceId

- **UUID**: `ECUC:3525b90b-f352-4412-8bb6-8c5fe5368a8d`
- **参数名**: `SdServerServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id to identify the service. This is unique for the service interface.

############ 3. SdServerServiceInstanceId

- **UUID**: `ECUC:0cc94fdc-f6e0-41a5-9f94-702e1eeca869`
- **参数名**: `SdServerServiceInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to specify Instance Id of the Service implemented by the Server Service.

############ 4. SdServerServiceMajorVersion

- **UUID**: `ECUC:b978e561-cc50-49bb-9904-5dcdd7b5f942`
- **参数名**: `SdServerServiceMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Major version number of the Service as used in SD Entries.

############ 5. SdServerServiceMinorVersion

- **UUID**: `ECUC:6fe78ada-4229-4652-91a4-61b0a7f93811`
- **参数名**: `SdServerServiceMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967294]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minor version number of the Service as used e.g. in Offer Service entries.

########### BOOLEAN 类型参数

############ 1. SdServerServiceAutoAvailable

- **UUID**: `ECUC:84312806-2ac0-4c8c-a910-7c1f3ad6f752`
- **参数名**: `SdServerServiceAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this Service will be set to "Available" on start.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SdServerServiceTimerRef

- **UUID**: `ECUC:8d4c6253-06aa-4cc4-9b4e-7f4b621e6a11`
- **引用名**: `SdServerServiceTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this service.

########## 配置容器

本模块包含 **7** 个配置容器：

########### 1. SdEventHandler

**容器属性**:

- **UUID**: `ECUC:cd0817ff-4984-4c30-945b-17d9f12a5937`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandler`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container Element for representing an EventGroup as part of the Service Instance.

############ 参数配置

此容器包含 **4** 个参数：

############# INTEGER 类型参数

############## 1. SdEventHandlerEventGroupId

- **UUID**: `ECUC:f35274e5-c81e-46db-85e0-c8c87a035ceb`
- **参数名**: `SdEventHandlerEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The EventGroup Id of this EventGroup as a unique identifier of the EventGroup in this service. This identifier is used for EventGroup entries as well.

############## 2. SdEventHandlerHandleId

- **UUID**: `ECUC:82078ed5-703f-4f07-a18f-96d753123380`
- **参数名**: `SdEventHandlerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

############## 3. SdEventHandlerMulticastThreshold

- **UUID**: `ECUC:c1839189-c609-4754-b527-ac6fbab2d338`
- **参数名**: `SdEventHandlerMulticastThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the number of subscribed clients that trigger the Server to change the transmission of events to Multicast.

############# BOOLEAN 类型参数

############## 1. SdEventHandlerAutoAvailable

- **UUID**: `ECUC:3b035334-4b5d-4df2-9d37-a821507d89ee`
- **参数名**: `SdEventHandlerAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "available" on start.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. SdEventHandlerTimerRef

- **UUID**: `ECUC:cb252f3e-aecf-4f25-86d8-bead3b24302a`
- **引用名**: `SdEventHandlerTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this EventGroup.

############ 配置容器

本模块包含 **4** 个配置容器：

############# 1. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

############## 引用关系

此容器包含 **1** 个引用：

############### SYMBOLIC-NAME-REFERENCE 类型引用

################ 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############# 2. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

############## 引用关系

此容器包含 **2** 个引用：

############### SYMBOLIC-NAME-REFERENCE 类型引用

################ 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

################ 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

############# 3. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

############## 引用关系

此容器包含 **2** 个引用：

############### SYMBOLIC-NAME-REFERENCE 类型引用

################ 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

################ 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

############# 4. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############## 参数配置

此容器包含 **2** 个参数：

############### STRING 类型参数

################ 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

################ 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

########### 2. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########### 3. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############## 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

########### 4. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############## 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

########### 5. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

########### 6. SdProvidedMethods

**容器属性**:

- **UUID**: `ECUC:c44675a1-0711-453d-875f-d581bcf43cfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdProvidedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the needed elements of the data path for the methods provided by the service.

############ 引用关系

此容器包含 **3** 个引用：

############# REFERENCE 类型引用

############## 1. SdServerServiceTcpRef

- **UUID**: `ECUC:b3498ae5-faa5-42b7-ad50-c0a6c9230366`
- **引用名**: `SdServerServiceTcpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

############## 2. SdServerServiceUdpRef

- **UUID**: `ECUC:cf179e95-120d-46f9-9af3-ffe21c5853fa`
- **引用名**: `SdServerServiceUdpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdServerServiceActivationRef

- **UUID**: `ECUC:41afbb7c-420b-4239-bcc8-a2aaeaf9bd27`
- **引用名**: `SdServerServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup to activated and deactivate the data path for methods of the service.

########### 7. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:874b7563-1cb2-8eb2-5927-b700f35c97e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:2bf79f01-8d7d-dcdd-fa22-be8fe3ac494f`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:cffe4887-b805-d572-05cd-e1d6708816a7`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 11. SdEventHandler

**容器属性**:

- **UUID**: `ECUC:cd0817ff-4984-4c30-945b-17d9f12a5937`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandler`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container Element for representing an EventGroup as part of the Service Instance.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SdEventHandlerEventGroupId

- **UUID**: `ECUC:f35274e5-c81e-46db-85e0-c8c87a035ceb`
- **参数名**: `SdEventHandlerEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The EventGroup Id of this EventGroup as a unique identifier of the EventGroup in this service. This identifier is used for EventGroup entries as well.

############ 2. SdEventHandlerHandleId

- **UUID**: `ECUC:82078ed5-703f-4f07-a18f-96d753123380`
- **参数名**: `SdEventHandlerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

############ 3. SdEventHandlerMulticastThreshold

- **UUID**: `ECUC:c1839189-c609-4754-b527-ac6fbab2d338`
- **参数名**: `SdEventHandlerMulticastThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the number of subscribed clients that trigger the Server to change the transmission of events to Multicast.

########### BOOLEAN 类型参数

############ 1. SdEventHandlerAutoAvailable

- **UUID**: `ECUC:3b035334-4b5d-4df2-9d37-a821507d89ee`
- **参数名**: `SdEventHandlerAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "available" on start.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SdEventHandlerTimerRef

- **UUID**: `ECUC:cb252f3e-aecf-4f25-86d8-bead3b24302a`
- **引用名**: `SdEventHandlerTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this EventGroup.

########## 配置容器

本模块包含 **4** 个配置容器：

########### 1. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########### 2. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############## 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

########### 3. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############## 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

########### 4. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 12. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

######### 13. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 14. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 15. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 16. SdProvidedMethods

**容器属性**:

- **UUID**: `ECUC:c44675a1-0711-453d-875f-d581bcf43cfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdProvidedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the needed elements of the data path for the methods provided by the service.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. SdServerServiceTcpRef

- **UUID**: `ECUC:b3498ae5-faa5-42b7-ad50-c0a6c9230366`
- **引用名**: `SdServerServiceTcpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

############ 2. SdServerServiceUdpRef

- **UUID**: `ECUC:cf179e95-120d-46f9-9af3-ffe21c5853fa`
- **引用名**: `SdServerServiceUdpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdServerServiceActivationRef

- **UUID**: `ECUC:41afbb7c-420b-4239-bcc8-a2aaeaf9bd27`
- **引用名**: `SdServerServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup to activated and deactivate the data path for methods of the service.

######### 17. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:874b7563-1cb2-8eb2-5927-b700f35c97e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:2bf79f01-8d7d-dcdd-fa22-be8fe3ac494f`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:cffe4887-b805-d572-05cd-e1d6708816a7`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 18. SdServerTimer

**容器属性**:

- **UUID**: `ECUC:04b00855-be0a-4099-8d3a-c29a817984af`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerTimer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all timers used by the Service Discovery module for Server Services.

########## 参数配置

此容器包含 **8** 个参数：

########### INTEGER 类型参数

############ 1. SdServerTimerInitialOfferRepetitionsMax

- **UUID**: `ECUC:39dd75c8-8b0d-4180-9f2c-35d51b39a4b7`
- **参数名**: `SdServerTimerInitialOfferRepetitionsMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the maximum amount of offer repetition. This parameter is mandatory for ServerService.

############ 2. SdServerTimerTTL

- **UUID**: `ECUC:18853e91-cd2f-4c33-a05d-a7ff072a496f`
- **参数名**: `SdServerTimerTTL`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16777215]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time to live for offer service or subscribe EventGroup ack.

########### FLOAT 类型参数

############ 1. SdServerTimerInitialOfferDelayMax

- **UUID**: `ECUC:8396d06c-fc84-48c0-aeea-10994e019bef`
- **参数名**: `SdServerTimerInitialOfferDelayMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max value in [s] to delay randomly the first offer. This parameter is mandatory for ServerService.

############ 2. SdServerTimerInitialOfferDelayMin

- **UUID**: `ECUC:4a39de00-b0fb-42e5-a5d8-53c0921bd820`
- **参数名**: `SdServerTimerInitialOfferDelayMin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Min value in [s] to delay randomly the first offer. This parameter is mandatory for ServerService.

############ 3. SdServerTimerInitialOfferRepetitionBaseDelay

- **UUID**: `ECUC:d29dcea0-ce20-48c0-9107-19d90b75f6ff`
- **参数名**: `SdServerTimerInitialOfferRepetitionBaseDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The base delay in [s] for offer repetitions. Successive offers have an exponential back off delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory for ServerService.

############ 4. SdServerTimerOfferCyclicDelay

- **UUID**: `ECUC:b411f88e-04c1-4a0d-b989-f4900d2b505d`
- **参数名**: `SdServerTimerOfferCyclicDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Interval between cyclic offers in the main phase. This parameter is mandatory for ServerService.

############ 5. SdServerTimerRequestResponseMaxDelay

- **UUID**: `ECUC:bb0ae042-d899-4a43-81e0-f91af146126b`
- **参数名**: `SdServerTimerRequestResponseMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum allowable response delay to entries received by multicast in seconds.

############ 6. SdServerTimerRequestResponseMinDelay

- **UUID**: `ECUC:f78f66b8-1294-4000-8b73-7dccb6614a1e`
- **参数名**: `SdServerTimerRequestResponseMinDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum allowable response delay to entries received by multicast in seconds.

####### 2. SdClientService

**容器属性**:

- **UUID**: `ECUC:f68e3db6-757e-43b3-9103-2f606844e25c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientService`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all parameters used by Client services.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. SdClientServiceHandleId

- **UUID**: `ECUC:e55d49c4-21ba-4b1c-8dbd-5d33c6c343c0`
- **参数名**: `SdClientServiceHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this Client Service Instance.

########## 2. SdClientServiceId

- **UUID**: `ECUC:55150245-ac37-4a34-bf4a-cd44c7d77ee7`
- **参数名**: `SdClientServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id to identify the service. This is unique for the service interface.

########## 3. SdClientServiceInstanceId

- **UUID**: `ECUC:89e8e56f-96f8-4a54-9229-0b15538df8ba`
- **参数名**: `SdClientServiceInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to specify Instance Id of the service as used in SD entries.

########## 4. SdClientServiceMajorVersion

- **UUID**: `ECUC:76ba4bba-a54e-4a52-b129-57fe3959dd5c`
- **参数名**: `SdClientServiceMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Major version number of the Service as used in the SD entries.

########## 5. SdClientServiceMinorVersion

- **UUID**: `ECUC:def32508-2c8f-49f2-bc83-24607c4befef`
- **参数名**: `SdClientServiceMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minor version number of the Service as used in the SD Service Entries.

######### BOOLEAN 类型参数

########## 1. SdClientServiceAutoRequire

- **UUID**: `ECUC:b0aefe0b-0801-4486-8807-37c44397bf5a`
- **参数名**: `SdClientServiceAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this Service will be set to "required" on start.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdClientServiceTimerRef

- **UUID**: `ECUC:50712e7a-7cf2-42a0-b9bf-0c74635c7890`
- **引用名**: `SdClientServiceTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this service.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:aac361f2-7417-8d40-2c11-28fd180bafe0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:036b1450-e10e-d0f7-e2e4-4591149fe6db`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:62783abe-e3b8-d599-c2f1-9a4db2fed89d`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 2. SdConsumedEventGroup

**容器属性**:

- **UUID**: `ECUC:83329fec-a819-451e-96f0-64151aa3524a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedEventGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

A Service may have event groups which can be consumed. A service consumer has to subscribe to the corresponding event-group. After the subscription the event consumer takes the role of a server and the event provider that of a client.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. SdConsumedEventGroupHandleId

- **UUID**: `ECUC:9f56182e-3725-4353-afd4-b8ba2347ec42`
- **参数名**: `SdConsumedEventGroupHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

############ 2. SdConsumedEventGroupId

- **UUID**: `ECUC:505b0b9e-3cc1-4549-bb8b-47e02ee0c7d6`
- **参数名**: `SdConsumedEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Eventgroup Id of this eventGroup as a unique identifier of the eventgroup in this service. This identifier is used for EventGroup entries as well.

########### BOOLEAN 类型参数

############ 1. SdConsumedEventGroupAutoRequire

- **UUID**: `ECUC:ba0a63f1-7167-438d-8854-3b0ad958e3c4`
- **参数名**: `SdConsumedEventGroupAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "required" on start.

########## 引用关系

此容器包含 **4** 个引用：

########### REFERENCE 类型引用

############ 1. SdConsumedEventGroupTimerRef

- **UUID**: `ECUC:c3bd7117-3c06-4440-ba51-604e0969d72e`
- **引用名**: `SdConsumedEventGroupTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this eventGroup.

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdConsumedEventGroupMulticastActivationRef

- **UUID**: `ECUC:44ad17a6-751c-42a5-98b1-f061bd1ef9bd`
- **引用名**: `SdConsumedEventGroupMulticastActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of a Routing Group in order to activate and setup the Socket Connection for Multicast Events of this EventGroup. The multicast address from the received Multicast option is setup by SoAd_RequestIpAddrAssignment.

############ 2. SdConsumedEventGroupTcpActivationRef

- **UUID**: `ECUC:cc5bdf5c-9c41-4731-813b-675d5de9f72e`
- **引用名**: `SdConsumedEventGroupTcpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving TCP events.

############ 3. SdConsumedEventGroupUdpActivationRef

- **UUID**: `ECUC:741ee45e-e2c6-48da-aa09-ef7bd1361513`
- **引用名**: `SdConsumedEventGroupUdpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving UDP events.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 3. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 4. SdConsumedMethods

**容器属性**:

- **UUID**: `ECUC:9df5f68a-cff8-4c24-9d91-ab14d93739d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the data path for accessing the server methods.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdClientServiceActivationRef

- **UUID**: `ECUC:312665e5-3bbf-42cc-a0d6-2cfcb81e2f75`
- **引用名**: `SdClientServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroupRef to activate/deactivate the data path for the methods.

############ 2. SdClientServiceTcpRef

- **UUID**: `ECUC:bd317a9e-01ab-44f2-9361-55f035da9043`
- **引用名**: `SdClientServiceTcpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (TCP) for communication with methods.

############ 3. SdClientServiceUdpRef

- **UUID**: `ECUC:bccf7329-9e29-44af-be83-148ca6537803`
- **引用名**: `SdClientServiceUdpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (UDP) for communication with methods.

####### 3. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:aac361f2-7417-8d40-2c11-28fd180bafe0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:036b1450-e10e-d0f7-e2e4-4591149fe6db`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:62783abe-e3b8-d599-c2f1-9a4db2fed89d`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 4. SdConsumedEventGroup

**容器属性**:

- **UUID**: `ECUC:83329fec-a819-451e-96f0-64151aa3524a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedEventGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

A Service may have event groups which can be consumed. A service consumer has to subscribe to the corresponding event-group. After the subscription the event consumer takes the role of a server and the event provider that of a client.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. SdConsumedEventGroupHandleId

- **UUID**: `ECUC:9f56182e-3725-4353-afd4-b8ba2347ec42`
- **参数名**: `SdConsumedEventGroupHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

########## 2. SdConsumedEventGroupId

- **UUID**: `ECUC:505b0b9e-3cc1-4549-bb8b-47e02ee0c7d6`
- **参数名**: `SdConsumedEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Eventgroup Id of this eventGroup as a unique identifier of the eventgroup in this service. This identifier is used for EventGroup entries as well.

######### BOOLEAN 类型参数

########## 1. SdConsumedEventGroupAutoRequire

- **UUID**: `ECUC:ba0a63f1-7167-438d-8854-3b0ad958e3c4`
- **参数名**: `SdConsumedEventGroupAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "required" on start.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. SdConsumedEventGroupTimerRef

- **UUID**: `ECUC:c3bd7117-3c06-4440-ba51-604e0969d72e`
- **引用名**: `SdConsumedEventGroupTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this eventGroup.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdConsumedEventGroupMulticastActivationRef

- **UUID**: `ECUC:44ad17a6-751c-42a5-98b1-f061bd1ef9bd`
- **引用名**: `SdConsumedEventGroupMulticastActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of a Routing Group in order to activate and setup the Socket Connection for Multicast Events of this EventGroup. The multicast address from the received Multicast option is setup by SoAd_RequestIpAddrAssignment.

########## 2. SdConsumedEventGroupTcpActivationRef

- **UUID**: `ECUC:cc5bdf5c-9c41-4731-813b-675d5de9f72e`
- **引用名**: `SdConsumedEventGroupTcpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving TCP events.

########## 3. SdConsumedEventGroupUdpActivationRef

- **UUID**: `ECUC:741ee45e-e2c6-48da-aa09-ef7bd1361513`
- **引用名**: `SdConsumedEventGroupUdpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving UDP events.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 5. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 6. SdConsumedMethods

**容器属性**:

- **UUID**: `ECUC:9df5f68a-cff8-4c24-9d91-ab14d93739d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the data path for accessing the server methods.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdClientServiceActivationRef

- **UUID**: `ECUC:312665e5-3bbf-42cc-a0d6-2cfcb81e2f75`
- **引用名**: `SdClientServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroupRef to activate/deactivate the data path for the methods.

########## 2. SdClientServiceTcpRef

- **UUID**: `ECUC:bd317a9e-01ab-44f2-9361-55f035da9043`
- **引用名**: `SdClientServiceTcpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (TCP) for communication with methods.

########## 3. SdClientServiceUdpRef

- **UUID**: `ECUC:bccf7329-9e29-44af-be83-148ca6537803`
- **引用名**: `SdClientServiceUdpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (UDP) for communication with methods.

####### 7. SdClientTimer

**容器属性**:

- **UUID**: `ECUC:c443f1b3-de9c-4af4-8002-1dd9afaf083b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientTimer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all timers used by the Service Discovery module for Client Services.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. SdClientTimerInitialFindRepetitionsMax

- **UUID**: `ECUC:3d026bb0-8af3-498a-9c13-ea6881c55780`
- **参数名**: `SdClientTimerInitialFindRepetitionsMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration for the maximum number of find repetitions. This parameter is mandatory for ClientService.

########## 2. SdClientTimerTTL

- **UUID**: `ECUC:68fd030c-092e-45b6-9510-b120cdcc8054`
- **参数名**: `SdClientTimerTTL`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16777215]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time to live for find and subscribe messages.

######### FLOAT 类型参数

########## 1. SdClientTimerInitialFindDelayMax

- **UUID**: `ECUC:1a21c6e5-384a-4e0d-9629-c2c8818e3853`
- **参数名**: `SdClientTimerInitialFindDelayMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max value in [s] to delay randomly the transmission of a find message. This parameter is mandatory for ClientService.

########## 2. SdClientTimerInitialFindDelayMin

- **UUID**: `ECUC:d9c73e19-0364-4c48-9879-8db8d02ab112`
- **参数名**: `SdClientTimerInitialFindDelayMin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Min value in [s] to delay randomly the transmission of a find message. This parameter is mandatory for ClientService.

########## 3. SdClientTimerInitialFindRepetitionsBaseDelay

- **UUID**: `ECUC:8e1d6e7e-9f2d-418a-905e-de3054e5331f`
- **参数名**: `SdClientTimerInitialFindRepetitionsBaseDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The base delay in [s] for find repetitions. Successive finds have an exponential back off delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory for ClientService.

########## 4. SdClientTimerRequestResponseMaxDelay

- **UUID**: `ECUC:6b73d0a8-21a2-426f-8b4b-416d9349c512`
- **参数名**: `SdClientTimerRequestResponseMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum allowable response delay to entries received by multicast in seconds. This parameter is mandatory for ConsumedEventGroups.

########## 5. SdClientTimerRequestResponseMinDelay

- **UUID**: `ECUC:c19c4138-80e9-4299-b797-f94616832cb8`
- **参数名**: `SdClientTimerRequestResponseMinDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum allowable response delay to the find message in seconds. This parameter is mandatory for ConsumedEventGroups.

####### 8. SdInstanceMulticastRxPdu

**容器属性**:

- **UUID**: `ECUC:bea12c80-f2e7-436e-8b0c-84c85b798f0f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceMulticastRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the received PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SdRxPduId

- **UUID**: `ECUC:1be8da89-4233-4359-aa0c-af5ab04dbec1`
- **参数名**: `SdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received via the API Sd_SoAdIfRxIndication().

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdRxPduRef

- **UUID**: `ECUC:98ef8aa7-6ae3-46cc-aa15-16489eaf952e`
- **引用名**: `SdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 9. SdInstanceTxPdu

**容器属性**:

- **UUID**: `ECUC:9860bb63-3785-4422-9f84-c1ebed9be61a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceTxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the transmitted PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdTxPduRef

- **UUID**: `ECUC:6d7b96cb-5291-42d9-9f11-18526e08f918`
- **引用名**: `SdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 10. SdInstanceUnicastRxPdu

**容器属性**:

- **UUID**: `ECUC:2c61fb83-0189-4677-b735-a69f39ddf17e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceUnicastRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the received PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SdRxPduId

- **UUID**: `ECUC:60ade062-f122-45e5-b8e3-5ee8dd3e5742`
- **参数名**: `SdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received via the API Sd_SoAdIfRxIndication().

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdRxPduRef

- **UUID**: `ECUC:0665655e-b25c-45a0-b5f6-f29616d77fd7`
- **引用名**: `SdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 11. SdServerService

**容器属性**:

- **UUID**: `ECUC:73a79f80-245a-4417-9d68-1307e90f6f60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerService`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all parameters used by Server services.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. SdServerServiceHandleId

- **UUID**: `ECUC:ce2a7cd7-64ff-4d90-916b-ba896157fa67`
- **参数名**: `SdServerServiceHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this Server Service Instance.

########## 2. SdServerServiceId

- **UUID**: `ECUC:3525b90b-f352-4412-8bb6-8c5fe5368a8d`
- **参数名**: `SdServerServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id to identify the service. This is unique for the service interface.

########## 3. SdServerServiceInstanceId

- **UUID**: `ECUC:0cc94fdc-f6e0-41a5-9f94-702e1eeca869`
- **参数名**: `SdServerServiceInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to specify Instance Id of the Service implemented by the Server Service.

########## 4. SdServerServiceMajorVersion

- **UUID**: `ECUC:b978e561-cc50-49bb-9904-5dcdd7b5f942`
- **参数名**: `SdServerServiceMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Major version number of the Service as used in SD Entries.

########## 5. SdServerServiceMinorVersion

- **UUID**: `ECUC:6fe78ada-4229-4652-91a4-61b0a7f93811`
- **参数名**: `SdServerServiceMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967294]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minor version number of the Service as used e.g. in Offer Service entries.

######### BOOLEAN 类型参数

########## 1. SdServerServiceAutoAvailable

- **UUID**: `ECUC:84312806-2ac0-4c8c-a910-7c1f3ad6f752`
- **参数名**: `SdServerServiceAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this Service will be set to "Available" on start.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdServerServiceTimerRef

- **UUID**: `ECUC:8d4c6253-06aa-4cc4-9b4e-7f4b621e6a11`
- **引用名**: `SdServerServiceTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this service.

######## 配置容器

本模块包含 **7** 个配置容器：

######### 1. SdEventHandler

**容器属性**:

- **UUID**: `ECUC:cd0817ff-4984-4c30-945b-17d9f12a5937`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandler`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container Element for representing an EventGroup as part of the Service Instance.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SdEventHandlerEventGroupId

- **UUID**: `ECUC:f35274e5-c81e-46db-85e0-c8c87a035ceb`
- **参数名**: `SdEventHandlerEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The EventGroup Id of this EventGroup as a unique identifier of the EventGroup in this service. This identifier is used for EventGroup entries as well.

############ 2. SdEventHandlerHandleId

- **UUID**: `ECUC:82078ed5-703f-4f07-a18f-96d753123380`
- **参数名**: `SdEventHandlerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

############ 3. SdEventHandlerMulticastThreshold

- **UUID**: `ECUC:c1839189-c609-4754-b527-ac6fbab2d338`
- **参数名**: `SdEventHandlerMulticastThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the number of subscribed clients that trigger the Server to change the transmission of events to Multicast.

########### BOOLEAN 类型参数

############ 1. SdEventHandlerAutoAvailable

- **UUID**: `ECUC:3b035334-4b5d-4df2-9d37-a821507d89ee`
- **参数名**: `SdEventHandlerAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "available" on start.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SdEventHandlerTimerRef

- **UUID**: `ECUC:cb252f3e-aecf-4f25-86d8-bead3b24302a`
- **引用名**: `SdEventHandlerTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this EventGroup.

########## 配置容器

本模块包含 **4** 个配置容器：

########### 1. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########### 2. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############## 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

########### 3. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############## 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

########### 4. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 2. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

######### 3. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 4. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 5. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 6. SdProvidedMethods

**容器属性**:

- **UUID**: `ECUC:c44675a1-0711-453d-875f-d581bcf43cfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdProvidedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the needed elements of the data path for the methods provided by the service.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. SdServerServiceTcpRef

- **UUID**: `ECUC:b3498ae5-faa5-42b7-ad50-c0a6c9230366`
- **引用名**: `SdServerServiceTcpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

############ 2. SdServerServiceUdpRef

- **UUID**: `ECUC:cf179e95-120d-46f9-9af3-ffe21c5853fa`
- **引用名**: `SdServerServiceUdpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdServerServiceActivationRef

- **UUID**: `ECUC:41afbb7c-420b-4239-bcc8-a2aaeaf9bd27`
- **引用名**: `SdServerServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup to activated and deactivate the data path for methods of the service.

######### 7. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:874b7563-1cb2-8eb2-5927-b700f35c97e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:2bf79f01-8d7d-dcdd-fa22-be8fe3ac494f`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:cffe4887-b805-d572-05cd-e1d6708816a7`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 12. SdEventHandler

**容器属性**:

- **UUID**: `ECUC:cd0817ff-4984-4c30-945b-17d9f12a5937`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandler`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container Element for representing an EventGroup as part of the Service Instance.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SdEventHandlerEventGroupId

- **UUID**: `ECUC:f35274e5-c81e-46db-85e0-c8c87a035ceb`
- **参数名**: `SdEventHandlerEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The EventGroup Id of this EventGroup as a unique identifier of the EventGroup in this service. This identifier is used for EventGroup entries as well.

########## 2. SdEventHandlerHandleId

- **UUID**: `ECUC:82078ed5-703f-4f07-a18f-96d753123380`
- **参数名**: `SdEventHandlerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

########## 3. SdEventHandlerMulticastThreshold

- **UUID**: `ECUC:c1839189-c609-4754-b527-ac6fbab2d338`
- **参数名**: `SdEventHandlerMulticastThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the number of subscribed clients that trigger the Server to change the transmission of events to Multicast.

######### BOOLEAN 类型参数

########## 1. SdEventHandlerAutoAvailable

- **UUID**: `ECUC:3b035334-4b5d-4df2-9d37-a821507d89ee`
- **参数名**: `SdEventHandlerAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "available" on start.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdEventHandlerTimerRef

- **UUID**: `ECUC:cb252f3e-aecf-4f25-86d8-bead3b24302a`
- **引用名**: `SdEventHandlerTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this EventGroup.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

######### 2. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 3. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 4. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 13. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

####### 14. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########## 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

####### 15. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########## 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

####### 16. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 17. SdProvidedMethods

**容器属性**:

- **UUID**: `ECUC:c44675a1-0711-453d-875f-d581bcf43cfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdProvidedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the needed elements of the data path for the methods provided by the service.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. SdServerServiceTcpRef

- **UUID**: `ECUC:b3498ae5-faa5-42b7-ad50-c0a6c9230366`
- **引用名**: `SdServerServiceTcpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

########## 2. SdServerServiceUdpRef

- **UUID**: `ECUC:cf179e95-120d-46f9-9af3-ffe21c5853fa`
- **引用名**: `SdServerServiceUdpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdServerServiceActivationRef

- **UUID**: `ECUC:41afbb7c-420b-4239-bcc8-a2aaeaf9bd27`
- **引用名**: `SdServerServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup to activated and deactivate the data path for methods of the service.

####### 18. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:874b7563-1cb2-8eb2-5927-b700f35c97e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:2bf79f01-8d7d-dcdd-fa22-be8fe3ac494f`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:cffe4887-b805-d572-05cd-e1d6708816a7`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 19. SdServerTimer

**容器属性**:

- **UUID**: `ECUC:04b00855-be0a-4099-8d3a-c29a817984af`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerTimer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all timers used by the Service Discovery module for Server Services.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. SdServerTimerInitialOfferRepetitionsMax

- **UUID**: `ECUC:39dd75c8-8b0d-4180-9f2c-35d51b39a4b7`
- **参数名**: `SdServerTimerInitialOfferRepetitionsMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the maximum amount of offer repetition. This parameter is mandatory for ServerService.

########## 2. SdServerTimerTTL

- **UUID**: `ECUC:18853e91-cd2f-4c33-a05d-a7ff072a496f`
- **参数名**: `SdServerTimerTTL`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16777215]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time to live for offer service or subscribe EventGroup ack.

######### FLOAT 类型参数

########## 1. SdServerTimerInitialOfferDelayMax

- **UUID**: `ECUC:8396d06c-fc84-48c0-aeea-10994e019bef`
- **参数名**: `SdServerTimerInitialOfferDelayMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max value in [s] to delay randomly the first offer. This parameter is mandatory for ServerService.

########## 2. SdServerTimerInitialOfferDelayMin

- **UUID**: `ECUC:4a39de00-b0fb-42e5-a5d8-53c0921bd820`
- **参数名**: `SdServerTimerInitialOfferDelayMin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Min value in [s] to delay randomly the first offer. This parameter is mandatory for ServerService.

########## 3. SdServerTimerInitialOfferRepetitionBaseDelay

- **UUID**: `ECUC:d29dcea0-ce20-48c0-9107-19d90b75f6ff`
- **参数名**: `SdServerTimerInitialOfferRepetitionBaseDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The base delay in [s] for offer repetitions. Successive offers have an exponential back off delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory for ServerService.

########## 4. SdServerTimerOfferCyclicDelay

- **UUID**: `ECUC:b411f88e-04c1-4a0d-b989-f4900d2b505d`
- **参数名**: `SdServerTimerOfferCyclicDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Interval between cyclic offers in the main phase. This parameter is mandatory for ServerService.

########## 5. SdServerTimerRequestResponseMaxDelay

- **UUID**: `ECUC:bb0ae042-d899-4a43-81e0-f91af146126b`
- **参数名**: `SdServerTimerRequestResponseMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum allowable response delay to entries received by multicast in seconds.

########## 6. SdServerTimerRequestResponseMinDelay

- **UUID**: `ECUC:f78f66b8-1294-4000-8b73-7dccb6614a1e`
- **参数名**: `SdServerTimerRequestResponseMinDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum allowable response delay to entries received by multicast in seconds.

##### 2. SdInstance

**容器属性**:

- **UUID**: `ECUC:3c4bbbc4-1c53-4234-a90c-9373ba4d3f3c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstance`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container represents an instance of the SD; i.e. the SD configuration for a certain link.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. SdInstanceHostname

- **UUID**: `ECUC:ae63ecde-952c-49e6-a911-49c039a553d3`
- **参数名**: `SdInstanceHostname`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to specify the Hostname.

###### 配置容器

本模块包含 **18** 个配置容器：

####### 1. SdClientService

**容器属性**:

- **UUID**: `ECUC:f68e3db6-757e-43b3-9103-2f606844e25c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientService`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all parameters used by Client services.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. SdClientServiceHandleId

- **UUID**: `ECUC:e55d49c4-21ba-4b1c-8dbd-5d33c6c343c0`
- **参数名**: `SdClientServiceHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this Client Service Instance.

########## 2. SdClientServiceId

- **UUID**: `ECUC:55150245-ac37-4a34-bf4a-cd44c7d77ee7`
- **参数名**: `SdClientServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id to identify the service. This is unique for the service interface.

########## 3. SdClientServiceInstanceId

- **UUID**: `ECUC:89e8e56f-96f8-4a54-9229-0b15538df8ba`
- **参数名**: `SdClientServiceInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to specify Instance Id of the service as used in SD entries.

########## 4. SdClientServiceMajorVersion

- **UUID**: `ECUC:76ba4bba-a54e-4a52-b129-57fe3959dd5c`
- **参数名**: `SdClientServiceMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Major version number of the Service as used in the SD entries.

########## 5. SdClientServiceMinorVersion

- **UUID**: `ECUC:def32508-2c8f-49f2-bc83-24607c4befef`
- **参数名**: `SdClientServiceMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minor version number of the Service as used in the SD Service Entries.

######### BOOLEAN 类型参数

########## 1. SdClientServiceAutoRequire

- **UUID**: `ECUC:b0aefe0b-0801-4486-8807-37c44397bf5a`
- **参数名**: `SdClientServiceAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this Service will be set to "required" on start.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdClientServiceTimerRef

- **UUID**: `ECUC:50712e7a-7cf2-42a0-b9bf-0c74635c7890`
- **引用名**: `SdClientServiceTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this service.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:aac361f2-7417-8d40-2c11-28fd180bafe0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:036b1450-e10e-d0f7-e2e4-4591149fe6db`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:62783abe-e3b8-d599-c2f1-9a4db2fed89d`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 2. SdConsumedEventGroup

**容器属性**:

- **UUID**: `ECUC:83329fec-a819-451e-96f0-64151aa3524a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedEventGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

A Service may have event groups which can be consumed. A service consumer has to subscribe to the corresponding event-group. After the subscription the event consumer takes the role of a server and the event provider that of a client.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. SdConsumedEventGroupHandleId

- **UUID**: `ECUC:9f56182e-3725-4353-afd4-b8ba2347ec42`
- **参数名**: `SdConsumedEventGroupHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

############ 2. SdConsumedEventGroupId

- **UUID**: `ECUC:505b0b9e-3cc1-4549-bb8b-47e02ee0c7d6`
- **参数名**: `SdConsumedEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Eventgroup Id of this eventGroup as a unique identifier of the eventgroup in this service. This identifier is used for EventGroup entries as well.

########### BOOLEAN 类型参数

############ 1. SdConsumedEventGroupAutoRequire

- **UUID**: `ECUC:ba0a63f1-7167-438d-8854-3b0ad958e3c4`
- **参数名**: `SdConsumedEventGroupAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "required" on start.

########## 引用关系

此容器包含 **4** 个引用：

########### REFERENCE 类型引用

############ 1. SdConsumedEventGroupTimerRef

- **UUID**: `ECUC:c3bd7117-3c06-4440-ba51-604e0969d72e`
- **引用名**: `SdConsumedEventGroupTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this eventGroup.

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdConsumedEventGroupMulticastActivationRef

- **UUID**: `ECUC:44ad17a6-751c-42a5-98b1-f061bd1ef9bd`
- **引用名**: `SdConsumedEventGroupMulticastActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of a Routing Group in order to activate and setup the Socket Connection for Multicast Events of this EventGroup. The multicast address from the received Multicast option is setup by SoAd_RequestIpAddrAssignment.

############ 2. SdConsumedEventGroupTcpActivationRef

- **UUID**: `ECUC:cc5bdf5c-9c41-4731-813b-675d5de9f72e`
- **引用名**: `SdConsumedEventGroupTcpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving TCP events.

############ 3. SdConsumedEventGroupUdpActivationRef

- **UUID**: `ECUC:741ee45e-e2c6-48da-aa09-ef7bd1361513`
- **引用名**: `SdConsumedEventGroupUdpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving UDP events.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 3. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 4. SdConsumedMethods

**容器属性**:

- **UUID**: `ECUC:9df5f68a-cff8-4c24-9d91-ab14d93739d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the data path for accessing the server methods.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdClientServiceActivationRef

- **UUID**: `ECUC:312665e5-3bbf-42cc-a0d6-2cfcb81e2f75`
- **引用名**: `SdClientServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroupRef to activate/deactivate the data path for the methods.

############ 2. SdClientServiceTcpRef

- **UUID**: `ECUC:bd317a9e-01ab-44f2-9361-55f035da9043`
- **引用名**: `SdClientServiceTcpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (TCP) for communication with methods.

############ 3. SdClientServiceUdpRef

- **UUID**: `ECUC:bccf7329-9e29-44af-be83-148ca6537803`
- **引用名**: `SdClientServiceUdpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (UDP) for communication with methods.

####### 2. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:aac361f2-7417-8d40-2c11-28fd180bafe0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:036b1450-e10e-d0f7-e2e4-4591149fe6db`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:62783abe-e3b8-d599-c2f1-9a4db2fed89d`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 3. SdConsumedEventGroup

**容器属性**:

- **UUID**: `ECUC:83329fec-a819-451e-96f0-64151aa3524a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedEventGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

A Service may have event groups which can be consumed. A service consumer has to subscribe to the corresponding event-group. After the subscription the event consumer takes the role of a server and the event provider that of a client.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. SdConsumedEventGroupHandleId

- **UUID**: `ECUC:9f56182e-3725-4353-afd4-b8ba2347ec42`
- **参数名**: `SdConsumedEventGroupHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

########## 2. SdConsumedEventGroupId

- **UUID**: `ECUC:505b0b9e-3cc1-4549-bb8b-47e02ee0c7d6`
- **参数名**: `SdConsumedEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Eventgroup Id of this eventGroup as a unique identifier of the eventgroup in this service. This identifier is used for EventGroup entries as well.

######### BOOLEAN 类型参数

########## 1. SdConsumedEventGroupAutoRequire

- **UUID**: `ECUC:ba0a63f1-7167-438d-8854-3b0ad958e3c4`
- **参数名**: `SdConsumedEventGroupAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "required" on start.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. SdConsumedEventGroupTimerRef

- **UUID**: `ECUC:c3bd7117-3c06-4440-ba51-604e0969d72e`
- **引用名**: `SdConsumedEventGroupTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this eventGroup.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdConsumedEventGroupMulticastActivationRef

- **UUID**: `ECUC:44ad17a6-751c-42a5-98b1-f061bd1ef9bd`
- **引用名**: `SdConsumedEventGroupMulticastActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of a Routing Group in order to activate and setup the Socket Connection for Multicast Events of this EventGroup. The multicast address from the received Multicast option is setup by SoAd_RequestIpAddrAssignment.

########## 2. SdConsumedEventGroupTcpActivationRef

- **UUID**: `ECUC:cc5bdf5c-9c41-4731-813b-675d5de9f72e`
- **引用名**: `SdConsumedEventGroupTcpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving TCP events.

########## 3. SdConsumedEventGroupUdpActivationRef

- **UUID**: `ECUC:741ee45e-e2c6-48da-aa09-ef7bd1361513`
- **引用名**: `SdConsumedEventGroupUdpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving UDP events.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 4. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 5. SdConsumedMethods

**容器属性**:

- **UUID**: `ECUC:9df5f68a-cff8-4c24-9d91-ab14d93739d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the data path for accessing the server methods.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdClientServiceActivationRef

- **UUID**: `ECUC:312665e5-3bbf-42cc-a0d6-2cfcb81e2f75`
- **引用名**: `SdClientServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroupRef to activate/deactivate the data path for the methods.

########## 2. SdClientServiceTcpRef

- **UUID**: `ECUC:bd317a9e-01ab-44f2-9361-55f035da9043`
- **引用名**: `SdClientServiceTcpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (TCP) for communication with methods.

########## 3. SdClientServiceUdpRef

- **UUID**: `ECUC:bccf7329-9e29-44af-be83-148ca6537803`
- **引用名**: `SdClientServiceUdpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (UDP) for communication with methods.

####### 6. SdClientTimer

**容器属性**:

- **UUID**: `ECUC:c443f1b3-de9c-4af4-8002-1dd9afaf083b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientTimer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all timers used by the Service Discovery module for Client Services.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. SdClientTimerInitialFindRepetitionsMax

- **UUID**: `ECUC:3d026bb0-8af3-498a-9c13-ea6881c55780`
- **参数名**: `SdClientTimerInitialFindRepetitionsMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration for the maximum number of find repetitions. This parameter is mandatory for ClientService.

########## 2. SdClientTimerTTL

- **UUID**: `ECUC:68fd030c-092e-45b6-9510-b120cdcc8054`
- **参数名**: `SdClientTimerTTL`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16777215]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time to live for find and subscribe messages.

######### FLOAT 类型参数

########## 1. SdClientTimerInitialFindDelayMax

- **UUID**: `ECUC:1a21c6e5-384a-4e0d-9629-c2c8818e3853`
- **参数名**: `SdClientTimerInitialFindDelayMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max value in [s] to delay randomly the transmission of a find message. This parameter is mandatory for ClientService.

########## 2. SdClientTimerInitialFindDelayMin

- **UUID**: `ECUC:d9c73e19-0364-4c48-9879-8db8d02ab112`
- **参数名**: `SdClientTimerInitialFindDelayMin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Min value in [s] to delay randomly the transmission of a find message. This parameter is mandatory for ClientService.

########## 3. SdClientTimerInitialFindRepetitionsBaseDelay

- **UUID**: `ECUC:8e1d6e7e-9f2d-418a-905e-de3054e5331f`
- **参数名**: `SdClientTimerInitialFindRepetitionsBaseDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The base delay in [s] for find repetitions. Successive finds have an exponential back off delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory for ClientService.

########## 4. SdClientTimerRequestResponseMaxDelay

- **UUID**: `ECUC:6b73d0a8-21a2-426f-8b4b-416d9349c512`
- **参数名**: `SdClientTimerRequestResponseMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum allowable response delay to entries received by multicast in seconds. This parameter is mandatory for ConsumedEventGroups.

########## 5. SdClientTimerRequestResponseMinDelay

- **UUID**: `ECUC:c19c4138-80e9-4299-b797-f94616832cb8`
- **参数名**: `SdClientTimerRequestResponseMinDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum allowable response delay to the find message in seconds. This parameter is mandatory for ConsumedEventGroups.

####### 7. SdInstanceMulticastRxPdu

**容器属性**:

- **UUID**: `ECUC:bea12c80-f2e7-436e-8b0c-84c85b798f0f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceMulticastRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the received PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SdRxPduId

- **UUID**: `ECUC:1be8da89-4233-4359-aa0c-af5ab04dbec1`
- **参数名**: `SdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received via the API Sd_SoAdIfRxIndication().

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdRxPduRef

- **UUID**: `ECUC:98ef8aa7-6ae3-46cc-aa15-16489eaf952e`
- **引用名**: `SdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 8. SdInstanceTxPdu

**容器属性**:

- **UUID**: `ECUC:9860bb63-3785-4422-9f84-c1ebed9be61a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceTxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the transmitted PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdTxPduRef

- **UUID**: `ECUC:6d7b96cb-5291-42d9-9f11-18526e08f918`
- **引用名**: `SdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 9. SdInstanceUnicastRxPdu

**容器属性**:

- **UUID**: `ECUC:2c61fb83-0189-4677-b735-a69f39ddf17e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceUnicastRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the received PDU.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SdRxPduId

- **UUID**: `ECUC:60ade062-f122-45e5-b8e3-5ee8dd3e5742`
- **参数名**: `SdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received via the API Sd_SoAdIfRxIndication().

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdRxPduRef

- **UUID**: `ECUC:0665655e-b25c-45a0-b5f6-f29616d77fd7`
- **引用名**: `SdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 10. SdServerService

**容器属性**:

- **UUID**: `ECUC:73a79f80-245a-4417-9d68-1307e90f6f60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerService`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all parameters used by Server services.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. SdServerServiceHandleId

- **UUID**: `ECUC:ce2a7cd7-64ff-4d90-916b-ba896157fa67`
- **参数名**: `SdServerServiceHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this Server Service Instance.

########## 2. SdServerServiceId

- **UUID**: `ECUC:3525b90b-f352-4412-8bb6-8c5fe5368a8d`
- **参数名**: `SdServerServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id to identify the service. This is unique for the service interface.

########## 3. SdServerServiceInstanceId

- **UUID**: `ECUC:0cc94fdc-f6e0-41a5-9f94-702e1eeca869`
- **参数名**: `SdServerServiceInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to specify Instance Id of the Service implemented by the Server Service.

########## 4. SdServerServiceMajorVersion

- **UUID**: `ECUC:b978e561-cc50-49bb-9904-5dcdd7b5f942`
- **参数名**: `SdServerServiceMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Major version number of the Service as used in SD Entries.

########## 5. SdServerServiceMinorVersion

- **UUID**: `ECUC:6fe78ada-4229-4652-91a4-61b0a7f93811`
- **参数名**: `SdServerServiceMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967294]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minor version number of the Service as used e.g. in Offer Service entries.

######### BOOLEAN 类型参数

########## 1. SdServerServiceAutoAvailable

- **UUID**: `ECUC:84312806-2ac0-4c8c-a910-7c1f3ad6f752`
- **参数名**: `SdServerServiceAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this Service will be set to "Available" on start.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdServerServiceTimerRef

- **UUID**: `ECUC:8d4c6253-06aa-4cc4-9b4e-7f4b621e6a11`
- **引用名**: `SdServerServiceTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this service.

######## 配置容器

本模块包含 **7** 个配置容器：

######### 1. SdEventHandler

**容器属性**:

- **UUID**: `ECUC:cd0817ff-4984-4c30-945b-17d9f12a5937`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandler`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container Element for representing an EventGroup as part of the Service Instance.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SdEventHandlerEventGroupId

- **UUID**: `ECUC:f35274e5-c81e-46db-85e0-c8c87a035ceb`
- **参数名**: `SdEventHandlerEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The EventGroup Id of this EventGroup as a unique identifier of the EventGroup in this service. This identifier is used for EventGroup entries as well.

############ 2. SdEventHandlerHandleId

- **UUID**: `ECUC:82078ed5-703f-4f07-a18f-96d753123380`
- **参数名**: `SdEventHandlerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

############ 3. SdEventHandlerMulticastThreshold

- **UUID**: `ECUC:c1839189-c609-4754-b527-ac6fbab2d338`
- **参数名**: `SdEventHandlerMulticastThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the number of subscribed clients that trigger the Server to change the transmission of events to Multicast.

########### BOOLEAN 类型参数

############ 1. SdEventHandlerAutoAvailable

- **UUID**: `ECUC:3b035334-4b5d-4df2-9d37-a821507d89ee`
- **参数名**: `SdEventHandlerAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "available" on start.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SdEventHandlerTimerRef

- **UUID**: `ECUC:cb252f3e-aecf-4f25-86d8-bead3b24302a`
- **引用名**: `SdEventHandlerTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this EventGroup.

########## 配置容器

本模块包含 **4** 个配置容器：

########### 1. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########### 2. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############## 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

########### 3. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

############ 引用关系

此容器包含 **2** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############## 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

########### 4. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 2. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

######### 3. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 4. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 5. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

######### 6. SdProvidedMethods

**容器属性**:

- **UUID**: `ECUC:c44675a1-0711-453d-875f-d581bcf43cfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdProvidedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the needed elements of the data path for the methods provided by the service.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. SdServerServiceTcpRef

- **UUID**: `ECUC:b3498ae5-faa5-42b7-ad50-c0a6c9230366`
- **引用名**: `SdServerServiceTcpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

############ 2. SdServerServiceUdpRef

- **UUID**: `ECUC:cf179e95-120d-46f9-9af3-ffe21c5853fa`
- **引用名**: `SdServerServiceUdpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdServerServiceActivationRef

- **UUID**: `ECUC:41afbb7c-420b-4239-bcc8-a2aaeaf9bd27`
- **引用名**: `SdServerServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup to activated and deactivate the data path for methods of the service.

######### 7. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:874b7563-1cb2-8eb2-5927-b700f35c97e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:2bf79f01-8d7d-dcdd-fa22-be8fe3ac494f`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:cffe4887-b805-d572-05cd-e1d6708816a7`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 11. SdEventHandler

**容器属性**:

- **UUID**: `ECUC:cd0817ff-4984-4c30-945b-17d9f12a5937`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandler`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container Element for representing an EventGroup as part of the Service Instance.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SdEventHandlerEventGroupId

- **UUID**: `ECUC:f35274e5-c81e-46db-85e0-c8c87a035ceb`
- **参数名**: `SdEventHandlerEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The EventGroup Id of this EventGroup as a unique identifier of the EventGroup in this service. This identifier is used for EventGroup entries as well.

########## 2. SdEventHandlerHandleId

- **UUID**: `ECUC:82078ed5-703f-4f07-a18f-96d753123380`
- **参数名**: `SdEventHandlerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

########## 3. SdEventHandlerMulticastThreshold

- **UUID**: `ECUC:c1839189-c609-4754-b527-ac6fbab2d338`
- **参数名**: `SdEventHandlerMulticastThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the number of subscribed clients that trigger the Server to change the transmission of events to Multicast.

######### BOOLEAN 类型参数

########## 1. SdEventHandlerAutoAvailable

- **UUID**: `ECUC:3b035334-4b5d-4df2-9d37-a821507d89ee`
- **参数名**: `SdEventHandlerAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "available" on start.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdEventHandlerTimerRef

- **UUID**: `ECUC:cb252f3e-aecf-4f25-86d8-bead3b24302a`
- **引用名**: `SdEventHandlerTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this EventGroup.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

######### 2. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 3. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 4. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 12. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

####### 13. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########## 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

####### 14. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########## 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

####### 15. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 16. SdProvidedMethods

**容器属性**:

- **UUID**: `ECUC:c44675a1-0711-453d-875f-d581bcf43cfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdProvidedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the needed elements of the data path for the methods provided by the service.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. SdServerServiceTcpRef

- **UUID**: `ECUC:b3498ae5-faa5-42b7-ad50-c0a6c9230366`
- **引用名**: `SdServerServiceTcpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

########## 2. SdServerServiceUdpRef

- **UUID**: `ECUC:cf179e95-120d-46f9-9af3-ffe21c5853fa`
- **引用名**: `SdServerServiceUdpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdServerServiceActivationRef

- **UUID**: `ECUC:41afbb7c-420b-4239-bcc8-a2aaeaf9bd27`
- **引用名**: `SdServerServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup to activated and deactivate the data path for methods of the service.

####### 17. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:874b7563-1cb2-8eb2-5927-b700f35c97e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:2bf79f01-8d7d-dcdd-fa22-be8fe3ac494f`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:cffe4887-b805-d572-05cd-e1d6708816a7`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 18. SdServerTimer

**容器属性**:

- **UUID**: `ECUC:04b00855-be0a-4099-8d3a-c29a817984af`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerTimer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all timers used by the Service Discovery module for Server Services.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. SdServerTimerInitialOfferRepetitionsMax

- **UUID**: `ECUC:39dd75c8-8b0d-4180-9f2c-35d51b39a4b7`
- **参数名**: `SdServerTimerInitialOfferRepetitionsMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the maximum amount of offer repetition. This parameter is mandatory for ServerService.

########## 2. SdServerTimerTTL

- **UUID**: `ECUC:18853e91-cd2f-4c33-a05d-a7ff072a496f`
- **参数名**: `SdServerTimerTTL`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16777215]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time to live for offer service or subscribe EventGroup ack.

######### FLOAT 类型参数

########## 1. SdServerTimerInitialOfferDelayMax

- **UUID**: `ECUC:8396d06c-fc84-48c0-aeea-10994e019bef`
- **参数名**: `SdServerTimerInitialOfferDelayMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max value in [s] to delay randomly the first offer. This parameter is mandatory for ServerService.

########## 2. SdServerTimerInitialOfferDelayMin

- **UUID**: `ECUC:4a39de00-b0fb-42e5-a5d8-53c0921bd820`
- **参数名**: `SdServerTimerInitialOfferDelayMin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Min value in [s] to delay randomly the first offer. This parameter is mandatory for ServerService.

########## 3. SdServerTimerInitialOfferRepetitionBaseDelay

- **UUID**: `ECUC:d29dcea0-ce20-48c0-9107-19d90b75f6ff`
- **参数名**: `SdServerTimerInitialOfferRepetitionBaseDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The base delay in [s] for offer repetitions. Successive offers have an exponential back off delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory for ServerService.

########## 4. SdServerTimerOfferCyclicDelay

- **UUID**: `ECUC:b411f88e-04c1-4a0d-b989-f4900d2b505d`
- **参数名**: `SdServerTimerOfferCyclicDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Interval between cyclic offers in the main phase. This parameter is mandatory for ServerService.

########## 5. SdServerTimerRequestResponseMaxDelay

- **UUID**: `ECUC:bb0ae042-d899-4a43-81e0-f91af146126b`
- **参数名**: `SdServerTimerRequestResponseMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum allowable response delay to entries received by multicast in seconds.

########## 6. SdServerTimerRequestResponseMinDelay

- **UUID**: `ECUC:f78f66b8-1294-4000-8b73-7dccb6614a1e`
- **参数名**: `SdServerTimerRequestResponseMinDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum allowable response delay to entries received by multicast in seconds.

##### 3. SdClientService

**容器属性**:

- **UUID**: `ECUC:f68e3db6-757e-43b3-9103-2f606844e25c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientService`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all parameters used by Client services.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. SdClientServiceHandleId

- **UUID**: `ECUC:e55d49c4-21ba-4b1c-8dbd-5d33c6c343c0`
- **参数名**: `SdClientServiceHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this Client Service Instance.

######## 2. SdClientServiceId

- **UUID**: `ECUC:55150245-ac37-4a34-bf4a-cd44c7d77ee7`
- **参数名**: `SdClientServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id to identify the service. This is unique for the service interface.

######## 3. SdClientServiceInstanceId

- **UUID**: `ECUC:89e8e56f-96f8-4a54-9229-0b15538df8ba`
- **参数名**: `SdClientServiceInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to specify Instance Id of the service as used in SD entries.

######## 4. SdClientServiceMajorVersion

- **UUID**: `ECUC:76ba4bba-a54e-4a52-b129-57fe3959dd5c`
- **参数名**: `SdClientServiceMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Major version number of the Service as used in the SD entries.

######## 5. SdClientServiceMinorVersion

- **UUID**: `ECUC:def32508-2c8f-49f2-bc83-24607c4befef`
- **参数名**: `SdClientServiceMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minor version number of the Service as used in the SD Service Entries.

####### BOOLEAN 类型参数

######## 1. SdClientServiceAutoRequire

- **UUID**: `ECUC:b0aefe0b-0801-4486-8807-37c44397bf5a`
- **参数名**: `SdClientServiceAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this Service will be set to "required" on start.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SdClientServiceTimerRef

- **UUID**: `ECUC:50712e7a-7cf2-42a0-b9bf-0c74635c7890`
- **引用名**: `SdClientServiceTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this service.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:aac361f2-7417-8d40-2c11-28fd180bafe0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:036b1450-e10e-d0f7-e2e4-4591149fe6db`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:62783abe-e3b8-d599-c2f1-9a4db2fed89d`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 2. SdConsumedEventGroup

**容器属性**:

- **UUID**: `ECUC:83329fec-a819-451e-96f0-64151aa3524a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedEventGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

A Service may have event groups which can be consumed. A service consumer has to subscribe to the corresponding event-group. After the subscription the event consumer takes the role of a server and the event provider that of a client.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. SdConsumedEventGroupHandleId

- **UUID**: `ECUC:9f56182e-3725-4353-afd4-b8ba2347ec42`
- **参数名**: `SdConsumedEventGroupHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

########## 2. SdConsumedEventGroupId

- **UUID**: `ECUC:505b0b9e-3cc1-4549-bb8b-47e02ee0c7d6`
- **参数名**: `SdConsumedEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Eventgroup Id of this eventGroup as a unique identifier of the eventgroup in this service. This identifier is used for EventGroup entries as well.

######### BOOLEAN 类型参数

########## 1. SdConsumedEventGroupAutoRequire

- **UUID**: `ECUC:ba0a63f1-7167-438d-8854-3b0ad958e3c4`
- **参数名**: `SdConsumedEventGroupAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "required" on start.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. SdConsumedEventGroupTimerRef

- **UUID**: `ECUC:c3bd7117-3c06-4440-ba51-604e0969d72e`
- **引用名**: `SdConsumedEventGroupTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this eventGroup.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdConsumedEventGroupMulticastActivationRef

- **UUID**: `ECUC:44ad17a6-751c-42a5-98b1-f061bd1ef9bd`
- **引用名**: `SdConsumedEventGroupMulticastActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of a Routing Group in order to activate and setup the Socket Connection for Multicast Events of this EventGroup. The multicast address from the received Multicast option is setup by SoAd_RequestIpAddrAssignment.

########## 2. SdConsumedEventGroupTcpActivationRef

- **UUID**: `ECUC:cc5bdf5c-9c41-4731-813b-675d5de9f72e`
- **引用名**: `SdConsumedEventGroupTcpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving TCP events.

########## 3. SdConsumedEventGroupUdpActivationRef

- **UUID**: `ECUC:741ee45e-e2c6-48da-aa09-ef7bd1361513`
- **引用名**: `SdConsumedEventGroupUdpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving UDP events.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 3. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 4. SdConsumedMethods

**容器属性**:

- **UUID**: `ECUC:9df5f68a-cff8-4c24-9d91-ab14d93739d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the data path for accessing the server methods.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdClientServiceActivationRef

- **UUID**: `ECUC:312665e5-3bbf-42cc-a0d6-2cfcb81e2f75`
- **引用名**: `SdClientServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroupRef to activate/deactivate the data path for the methods.

########## 2. SdClientServiceTcpRef

- **UUID**: `ECUC:bd317a9e-01ab-44f2-9361-55f035da9043`
- **引用名**: `SdClientServiceTcpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (TCP) for communication with methods.

########## 3. SdClientServiceUdpRef

- **UUID**: `ECUC:bccf7329-9e29-44af-be83-148ca6537803`
- **引用名**: `SdClientServiceUdpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (UDP) for communication with methods.

##### 4. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:aac361f2-7417-8d40-2c11-28fd180bafe0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:036b1450-e10e-d0f7-e2e4-4591149fe6db`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

######## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:62783abe-e3b8-d599-c2f1-9a4db2fed89d`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

##### 5. SdConsumedEventGroup

**容器属性**:

- **UUID**: `ECUC:83329fec-a819-451e-96f0-64151aa3524a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedEventGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

A Service may have event groups which can be consumed. A service consumer has to subscribe to the corresponding event-group. After the subscription the event consumer takes the role of a server and the event provider that of a client.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. SdConsumedEventGroupHandleId

- **UUID**: `ECUC:9f56182e-3725-4353-afd4-b8ba2347ec42`
- **参数名**: `SdConsumedEventGroupHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

######## 2. SdConsumedEventGroupId

- **UUID**: `ECUC:505b0b9e-3cc1-4549-bb8b-47e02ee0c7d6`
- **参数名**: `SdConsumedEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Eventgroup Id of this eventGroup as a unique identifier of the eventgroup in this service. This identifier is used for EventGroup entries as well.

####### BOOLEAN 类型参数

######## 1. SdConsumedEventGroupAutoRequire

- **UUID**: `ECUC:ba0a63f1-7167-438d-8854-3b0ad958e3c4`
- **参数名**: `SdConsumedEventGroupAutoRequire`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "required" on start.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. SdConsumedEventGroupTimerRef

- **UUID**: `ECUC:c3bd7117-3c06-4440-ba51-604e0969d72e`
- **引用名**: `SdConsumedEventGroupTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdClientTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdClientTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdClientTimer container for this eventGroup.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SdConsumedEventGroupMulticastActivationRef

- **UUID**: `ECUC:44ad17a6-751c-42a5-98b1-f061bd1ef9bd`
- **引用名**: `SdConsumedEventGroupMulticastActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of a Routing Group in order to activate and setup the Socket Connection for Multicast Events of this EventGroup. The multicast address from the received Multicast option is setup by SoAd_RequestIpAddrAssignment.

######## 2. SdConsumedEventGroupTcpActivationRef

- **UUID**: `ECUC:cc5bdf5c-9c41-4731-813b-675d5de9f72e`
- **引用名**: `SdConsumedEventGroupTcpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving TCP events.

######## 3. SdConsumedEventGroupUdpActivationRef

- **UUID**: `ECUC:741ee45e-e2c6-48da-aa09-ef7bd1361513`
- **引用名**: `SdConsumedEventGroupUdpActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the Routing Group for activation of the data path for receiving UDP events.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

##### 6. SdClientCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:3767c428-a6b2-8eab-31fe-5db1ca6a1fce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. SdClientServiceCapabilityRecordKey

- **UUID**: `ECUC:900f7687-13a9-d262-e8d1-7a45c6fe56c9`
- **参数名**: `SdClientServiceCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

######## 2. SdClientServiceCapabilityRecordValue

- **UUID**: `ECUC:ef1c9cf5-1653-d704-c8de-cf02655d488b`
- **参数名**: `SdClientServiceCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

##### 7. SdConsumedMethods

**容器属性**:

- **UUID**: `ECUC:9df5f68a-cff8-4c24-9d91-ab14d93739d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdConsumedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the data path for accessing the server methods.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SdClientServiceActivationRef

- **UUID**: `ECUC:312665e5-3bbf-42cc-a0d6-2cfcb81e2f75`
- **引用名**: `SdClientServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroupRef to activate/deactivate the data path for the methods.

######## 2. SdClientServiceTcpRef

- **UUID**: `ECUC:bd317a9e-01ab-44f2-9361-55f035da9043`
- **引用名**: `SdClientServiceTcpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (TCP) for communication with methods.

######## 3. SdClientServiceUdpRef

- **UUID**: `ECUC:bccf7329-9e29-44af-be83-148ca6537803`
- **引用名**: `SdClientServiceUdpRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SoAdSocketConnection representing the data path (UDP) for communication with methods.

##### 8. SdClientTimer

**容器属性**:

- **UUID**: `ECUC:c443f1b3-de9c-4af4-8002-1dd9afaf083b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdClientTimer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all timers used by the Service Discovery module for Client Services.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. SdClientTimerInitialFindRepetitionsMax

- **UUID**: `ECUC:3d026bb0-8af3-498a-9c13-ea6881c55780`
- **参数名**: `SdClientTimerInitialFindRepetitionsMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration for the maximum number of find repetitions. This parameter is mandatory for ClientService.

######## 2. SdClientTimerTTL

- **UUID**: `ECUC:68fd030c-092e-45b6-9510-b120cdcc8054`
- **参数名**: `SdClientTimerTTL`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16777215]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time to live for find and subscribe messages.

####### FLOAT 类型参数

######## 1. SdClientTimerInitialFindDelayMax

- **UUID**: `ECUC:1a21c6e5-384a-4e0d-9629-c2c8818e3853`
- **参数名**: `SdClientTimerInitialFindDelayMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max value in [s] to delay randomly the transmission of a find message. This parameter is mandatory for ClientService.

######## 2. SdClientTimerInitialFindDelayMin

- **UUID**: `ECUC:d9c73e19-0364-4c48-9879-8db8d02ab112`
- **参数名**: `SdClientTimerInitialFindDelayMin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Min value in [s] to delay randomly the transmission of a find message. This parameter is mandatory for ClientService.

######## 3. SdClientTimerInitialFindRepetitionsBaseDelay

- **UUID**: `ECUC:8e1d6e7e-9f2d-418a-905e-de3054e5331f`
- **参数名**: `SdClientTimerInitialFindRepetitionsBaseDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The base delay in [s] for find repetitions. Successive finds have an exponential back off delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory for ClientService.

######## 4. SdClientTimerRequestResponseMaxDelay

- **UUID**: `ECUC:6b73d0a8-21a2-426f-8b4b-416d9349c512`
- **参数名**: `SdClientTimerRequestResponseMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum allowable response delay to entries received by multicast in seconds. This parameter is mandatory for ConsumedEventGroups.

######## 5. SdClientTimerRequestResponseMinDelay

- **UUID**: `ECUC:c19c4138-80e9-4299-b797-f94616832cb8`
- **参数名**: `SdClientTimerRequestResponseMinDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum allowable response delay to the find message in seconds. This parameter is mandatory for ConsumedEventGroups.

##### 9. SdInstanceMulticastRxPdu

**容器属性**:

- **UUID**: `ECUC:bea12c80-f2e7-436e-8b0c-84c85b798f0f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceMulticastRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the received PDU.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SdRxPduId

- **UUID**: `ECUC:1be8da89-4233-4359-aa0c-af5ab04dbec1`
- **参数名**: `SdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received via the API Sd_SoAdIfRxIndication().

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SdRxPduRef

- **UUID**: `ECUC:98ef8aa7-6ae3-46cc-aa15-16489eaf952e`
- **引用名**: `SdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 10. SdInstanceTxPdu

**容器属性**:

- **UUID**: `ECUC:9860bb63-3785-4422-9f84-c1ebed9be61a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceTxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the transmitted PDU.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SdTxPduRef

- **UUID**: `ECUC:6d7b96cb-5291-42d9-9f11-18526e08f918`
- **引用名**: `SdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 11. SdInstanceUnicastRxPdu

**容器属性**:

- **UUID**: `ECUC:2c61fb83-0189-4677-b735-a69f39ddf17e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdInstanceUnicastRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies the received PDU.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SdRxPduId

- **UUID**: `ECUC:60ade062-f122-45e5-b8e3-5ee8dd3e5742`
- **参数名**: `SdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the PDU that will be received via the API Sd_SoAdIfRxIndication().

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SdRxPduRef

- **UUID**: `ECUC:0665655e-b25c-45a0-b5f6-f29616d77fd7`
- **引用名**: `SdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 12. SdServerService

**容器属性**:

- **UUID**: `ECUC:73a79f80-245a-4417-9d68-1307e90f6f60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerService`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all parameters used by Server services.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. SdServerServiceHandleId

- **UUID**: `ECUC:ce2a7cd7-64ff-4d90-916b-ba896157fa67`
- **参数名**: `SdServerServiceHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this Server Service Instance.

######## 2. SdServerServiceId

- **UUID**: `ECUC:3525b90b-f352-4412-8bb6-8c5fe5368a8d`
- **参数名**: `SdServerServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id to identify the service. This is unique for the service interface.

######## 3. SdServerServiceInstanceId

- **UUID**: `ECUC:0cc94fdc-f6e0-41a5-9f94-702e1eeca869`
- **参数名**: `SdServerServiceInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to specify Instance Id of the Service implemented by the Server Service.

######## 4. SdServerServiceMajorVersion

- **UUID**: `ECUC:b978e561-cc50-49bb-9904-5dcdd7b5f942`
- **参数名**: `SdServerServiceMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Major version number of the Service as used in SD Entries.

######## 5. SdServerServiceMinorVersion

- **UUID**: `ECUC:6fe78ada-4229-4652-91a4-61b0a7f93811`
- **参数名**: `SdServerServiceMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967294]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minor version number of the Service as used e.g. in Offer Service entries.

####### BOOLEAN 类型参数

######## 1. SdServerServiceAutoAvailable

- **UUID**: `ECUC:84312806-2ac0-4c8c-a910-7c1f3ad6f752`
- **参数名**: `SdServerServiceAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this Service will be set to "Available" on start.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SdServerServiceTimerRef

- **UUID**: `ECUC:8d4c6253-06aa-4cc4-9b4e-7f4b621e6a11`
- **引用名**: `SdServerServiceTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this service.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. SdEventHandler

**容器属性**:

- **UUID**: `ECUC:cd0817ff-4984-4c30-945b-17d9f12a5937`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandler`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container Element for representing an EventGroup as part of the Service Instance.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SdEventHandlerEventGroupId

- **UUID**: `ECUC:f35274e5-c81e-46db-85e0-c8c87a035ceb`
- **参数名**: `SdEventHandlerEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The EventGroup Id of this EventGroup as a unique identifier of the EventGroup in this service. This identifier is used for EventGroup entries as well.

########## 2. SdEventHandlerHandleId

- **UUID**: `ECUC:82078ed5-703f-4f07-a18f-96d753123380`
- **参数名**: `SdEventHandlerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

########## 3. SdEventHandlerMulticastThreshold

- **UUID**: `ECUC:c1839189-c609-4754-b527-ac6fbab2d338`
- **参数名**: `SdEventHandlerMulticastThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the number of subscribed clients that trigger the Server to change the transmission of events to Multicast.

######### BOOLEAN 类型参数

########## 1. SdEventHandlerAutoAvailable

- **UUID**: `ECUC:3b035334-4b5d-4df2-9d37-a821507d89ee`
- **参数名**: `SdEventHandlerAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "available" on start.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SdEventHandlerTimerRef

- **UUID**: `ECUC:cb252f3e-aecf-4f25-86d8-bead3b24302a`
- **引用名**: `SdEventHandlerTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this EventGroup.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

######### 2. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 3. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

############ 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

######### 4. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

############ 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 2. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

####### 3. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########## 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

####### 4. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########## 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

####### 5. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

####### 6. SdProvidedMethods

**容器属性**:

- **UUID**: `ECUC:c44675a1-0711-453d-875f-d581bcf43cfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdProvidedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the needed elements of the data path for the methods provided by the service.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. SdServerServiceTcpRef

- **UUID**: `ECUC:b3498ae5-faa5-42b7-ad50-c0a6c9230366`
- **引用名**: `SdServerServiceTcpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

########## 2. SdServerServiceUdpRef

- **UUID**: `ECUC:cf179e95-120d-46f9-9af3-ffe21c5853fa`
- **引用名**: `SdServerServiceUdpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdServerServiceActivationRef

- **UUID**: `ECUC:41afbb7c-420b-4239-bcc8-a2aaeaf9bd27`
- **引用名**: `SdServerServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup to activated and deactivate the data path for methods of the service.

####### 7. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:874b7563-1cb2-8eb2-5927-b700f35c97e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:2bf79f01-8d7d-dcdd-fa22-be8fe3ac494f`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:cffe4887-b805-d572-05cd-e1d6708816a7`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

##### 13. SdEventHandler

**容器属性**:

- **UUID**: `ECUC:cd0817ff-4984-4c30-945b-17d9f12a5937`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandler`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container Element for representing an EventGroup as part of the Service Instance.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. SdEventHandlerEventGroupId

- **UUID**: `ECUC:f35274e5-c81e-46db-85e0-c8c87a035ceb`
- **参数名**: `SdEventHandlerEventGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The EventGroup Id of this EventGroup as a unique identifier of the EventGroup in this service. This identifier is used for EventGroup entries as well.

######## 2. SdEventHandlerHandleId

- **UUID**: `ECUC:82078ed5-703f-4f07-a18f-96d753123380`
- **参数名**: `SdEventHandlerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HandleId by which the BswM can identify this EventGroup.

######## 3. SdEventHandlerMulticastThreshold

- **UUID**: `ECUC:c1839189-c609-4754-b527-ac6fbab2d338`
- **参数名**: `SdEventHandlerMulticastThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the number of subscribed clients that trigger the Server to change the transmission of events to Multicast.

####### BOOLEAN 类型参数

######## 1. SdEventHandlerAutoAvailable

- **UUID**: `ECUC:3b035334-4b5d-4df2-9d37-a821507d89ee`
- **参数名**: `SdEventHandlerAutoAvailable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If existing and set to true, this EventGroup will be set to "available" on start.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SdEventHandlerTimerRef

- **UUID**: `ECUC:cb252f3e-aecf-4f25-86d8-bead3b24302a`
- **引用名**: `SdEventHandlerTimerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SdServerTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Sd/SdConfig/SdInstance/SdServerTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference of the SdServerTimer container for this EventGroup.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

####### 2. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########## 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

####### 3. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

########## 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

####### 4. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

########## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

##### 14. SdEventHandlerMulticast

**容器属性**:

- **UUID**: `ECUC:7455adf8-6cdb-48c7-bf10-411438fafd5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerMulticast`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Group for Activation of Events sent over Multicast.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SdEventActivationRef

- **UUID**: `ECUC:fcee271a-c77c-92c3-553c-54fc8ffcb6ba`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

##### 15. SdEventHandlerTcp

**容器属性**:

- **UUID**: `ECUC:3d220a87-fd1d-487b-bee2-f7fc26292376`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerTcp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over TCP.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SdEventActivationRef

- **UUID**: `ECUC:c5ba83aa-57be-9277-550f-0be47d2adcd3`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

######## 2. SdEventTriggeringRef

- **UUID**: `ECUC:3ff6e054-70b5-8f1c-79a4-ba9fd271e728`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

##### 16. SdEventHandlerUdp

**容器属性**:

- **UUID**: `ECUC:f05233fc-2597-4821-8251-36a0248e328b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdEventHandlerUdp`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The subcontainer including the Routing Groups for Activation and Trigger Transmit for Events sent over UDP.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SdEventActivationRef

- **UUID**: `ECUC:78eaad1e-8038-921d-187d-4a887b8febe8`
- **引用名**: `SdEventActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup for activation of the data path for a subscribed client (start sending events after subscribe).

######## 2. SdEventTriggeringRef

- **UUID**: `ECUC:f32709c8-992f-8ec2-3d12-f943d0d6f63d`
- **引用名**: `SdEventTriggeringRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup that is used for triggered transmit. Triggering is needed to sent out initial events on the server side after a client got subscribed.

##### 17. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:e0abede2-41dc-96cb-501a-bbd2fb7781be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:85581780-b2a7-e4f6-f115-c361ebc73326`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

######## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:295ec106-dd2f-dd8b-fcc0-e6a878a3007e`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

##### 18. SdProvidedMethods

**容器属性**:

- **UUID**: `ECUC:c44675a1-0711-453d-875f-d581bcf43cfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdProvidedMethods`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container element for representing the needed elements of the data path for the methods provided by the service.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. SdServerServiceTcpRef

- **UUID**: `ECUC:b3498ae5-faa5-42b7-ad50-c0a6c9230366`
- **引用名**: `SdServerServiceTcpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

######## 2. SdServerServiceUdpRef

- **UUID**: `ECUC:cf179e95-120d-46f9-9af3-ffe21c5853fa`
- **引用名**: `SdServerServiceUdpRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdSocketConnectionGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SoAdSocketConnectionGroup used for methods.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SdServerServiceActivationRef

- **UUID**: `ECUC:41afbb7c-420b-4239-bcc8-a2aaeaf9bd27`
- **引用名**: `SdServerServiceActivationRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a SoAdRoutingGroup to activated and deactivate the data path for methods of the service.

##### 19. SdServerCapabilityRecord

**容器属性**:

- **UUID**: `ECUC:874b7563-1cb2-8eb2-5927-b700f35c97e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerCapabilityRecord`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Sd uses capability records to store arbitrary name/value pairs conveying additional information about the named service.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. SdServerCapabilityRecordKey

- **UUID**: `ECUC:2bf79f01-8d7d-dcdd-fa22-be8fe3ac494f`
- **参数名**: `SdServerCapabilityRecordKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a CapabilityRecord key.

######## 2. SdServerCapabilityRecordValue

- **UUID**: `ECUC:cffe4887-b805-d572-05cd-e1d6708816a7`
- **参数名**: `SdServerCapabilityRecordValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the corresponding CapabilityRecord value.

##### 20. SdServerTimer

**容器属性**:

- **UUID**: `ECUC:04b00855-be0a-4099-8d3a-c29a817984af`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdServerTimer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies all timers used by the Service Discovery module for Server Services.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. SdServerTimerInitialOfferRepetitionsMax

- **UUID**: `ECUC:39dd75c8-8b0d-4180-9f2c-35d51b39a4b7`
- **参数名**: `SdServerTimerInitialOfferRepetitionsMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the maximum amount of offer repetition. This parameter is mandatory for ServerService.

######## 2. SdServerTimerTTL

- **UUID**: `ECUC:18853e91-cd2f-4c33-a05d-a7ff072a496f`
- **参数名**: `SdServerTimerTTL`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16777215]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time to live for offer service or subscribe EventGroup ack.

####### FLOAT 类型参数

######## 1. SdServerTimerInitialOfferDelayMax

- **UUID**: `ECUC:8396d06c-fc84-48c0-aeea-10994e019bef`
- **参数名**: `SdServerTimerInitialOfferDelayMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max value in [s] to delay randomly the first offer. This parameter is mandatory for ServerService.

######## 2. SdServerTimerInitialOfferDelayMin

- **UUID**: `ECUC:4a39de00-b0fb-42e5-a5d8-53c0921bd820`
- **参数名**: `SdServerTimerInitialOfferDelayMin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Min value in [s] to delay randomly the first offer. This parameter is mandatory for ServerService.

######## 3. SdServerTimerInitialOfferRepetitionBaseDelay

- **UUID**: `ECUC:d29dcea0-ce20-48c0-9107-19d90b75f6ff`
- **参数名**: `SdServerTimerInitialOfferRepetitionBaseDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The base delay in [s] for offer repetitions. Successive offers have an exponential back off delay (1x base delay, 2x base delay, 4x base delay, ...). This parameter is mandatory for ServerService.

######## 4. SdServerTimerOfferCyclicDelay

- **UUID**: `ECUC:b411f88e-04c1-4a0d-b989-f4900d2b505d`
- **参数名**: `SdServerTimerOfferCyclicDelay`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Interval between cyclic offers in the main phase. This parameter is mandatory for ServerService.

######## 5. SdServerTimerRequestResponseMaxDelay

- **UUID**: `ECUC:bb0ae042-d899-4a43-81e0-f91af146126b`
- **参数名**: `SdServerTimerRequestResponseMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum allowable response delay to entries received by multicast in seconds.

######## 6. SdServerTimerRequestResponseMinDelay

- **UUID**: `ECUC:f78f66b8-1294-4000-8b73-7dccb6614a1e`
- **参数名**: `SdServerTimerRequestResponseMinDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum allowable response delay to entries received by multicast in seconds.

##### 21. SdGeneral

**容器属性**:

- **UUID**: `ECUC:7b79cd36-3be0-4156-bb91-48a55e906fde`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SdGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container lists the general configuration parameters for the Service Discovery module.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. SdDevErrorDetect

- **UUID**: `ECUC:e33af6e9-d274-4e33-9b24-13a11b7cedd9`
- **参数名**: `SdDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the development error detection and notification mechanism.

######## 2. SdVersionInfoApi

- **UUID**: `ECUC:1cd5d766-78b8-42f5-8c15-cdc197aa01fd`
- **参数名**: `SdVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the version info API.

####### FLOAT 类型参数

######## 1. SdMainFunctionCycleTime

- **UUID**: `ECUC:5f971779-d2f5-4db7-af61-05b803d0c8ea`
- **参数名**: `SdMainFunctionCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [1E-4..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the cycle time in seconds of the periodic calling of Sd main function.

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

1. **Sd**
