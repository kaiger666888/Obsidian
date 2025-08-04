# EcuC

## 模块描述

Virtual module to collect ECU Configuration specific / global configuration information.

## 容器列表

### 1. EcucConfigSet

**描述**: This container contains the configuration parameters and sub containers of the global PduCollection.

该容器没有参数。

### 2. EcucPduCollection

**描述**: Collection of all Pdu objects flowing through the Com-Stack.

该容器没有参数。

### 3. MetaDataType

**描述**: Meta data serves to transport information through the AUTOSAR layers. It is transported by the
PduInfoType structure via a separate pointer to a byte array alongside the length of and a pointer
to the payload of the PDU. This container defines the content of the meta data.

该容器没有参数。

### 4. MetaDataItem

**描述**: The content of meta data in a Pdu consists of an ordered list of meta data items.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MetaDataItemLength
  长名称: ''
  描述: This parameter defines the length of a meta data item in bytes.
  默认值: ''
  最小值: 1
  最大值: 64
- 
  序号: 2
  名称: MetaDataItemType
  长名称: ''
  描述: This parameter defines the type of a meta data item.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. EcucPartitionCollection

**描述**: Collection of Partitions defined for this ECU.

该容器没有参数。

### 6. EcucPartition

**描述**: Definition of one Partition on this ECU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcucPartitionBswModuleExecution
  长名称: ''
  描述: Denotes that this partition will execute all BSW Modules. BSW Modules can only be executed in
      one partition.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PartitionCanBeRestarted
  长名称: ''
  描述: Specifies the requirement whether the Partition can be restarted. If set to true all software
      executing in this partition shall be capable of handling a restart.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. EcucPduCollection

**描述**: Collection of all Pdu objects flowing through the Com-Stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduIdTypeEnum
  长名称: ''
  描述: The PduIdType is used within the entire AUTOSAR Com Stack except for bus drivers. The size of
      this global type depends on the maximum number of PDUs used within one software module.
      If no software module deals with more PDUs that 256, this type can be set to uint8. If
      at least one software module handles more than 256 PDUs, this type must be set to
      uint16. See AUTOSAR_SWS_CommunicationStackTypes for more details.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PduLengthTypeEnum
  长名称: ''
  描述: The PduLengthType is used within the entire AUTOSAR Com Stack except for bus drivers. The size
      of this global type depends on the maximum length of PDUs to be sent by an ECU. If no
      segmentation is used the length depends on the maximum payload size of a frame of the
      underlying communication system (for FlexRay maximum size is 255 bytes, therefore
      uint8). If segementation is used it depends on the maximum length of a  segmeneted N-PDU
      (in general uint16 is used). See AUTOSAR_SWS_CommunicationStackTypes for more details.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. Pdu

**描述**: One Pdu flowing through the COM-Stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduLength
  长名称: ''
  描述: Length of the Pdu in bytes.  It should be noted that in former AUTOSAR releases (Rel 2.1, Rel
      3.0, Rel 3.1, Rel 4.0 Rev. 1) this parameter was defined in bits.
  默认值: ''
  最小值: 0
  最大值: 4095
```

### 9. EcucPduDedicatedPartition

**描述**: Module specific container for Pdu to partition assignment.

该容器没有参数。

### 10. EcucVariationResolver

**描述**: Collection of PredefinedVariant elements containing definition of values for SwSystemconst which
shall be applied when resolving the variability during ECU Configuration.

该容器没有参数。

### 11. EcucHardware

**描述**: Hardware definition of this Ecu.

该容器没有参数。

### 12. EcucCoreDefinition

**描述**: Definition of one Core on this Ecu.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcucCoreId
  长名称: ''
  描述: ID of the core.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 13. EcucPostBuildVariants

**描述**: Collection of toplevel PostBuildSelectable variants. The PredefinedVariants linked inside this
container will determine how many PostBuildSelectableVariants exist. If this container exist the
name pattern for initialization of BSW modules will be <Mip>_Config_<PredefinedVariant.shortName>.
If this container does not exist the name pattern for initialization of BSW modlues will be
<Mip>_Config.

该容器没有参数。

