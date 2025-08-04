# IpduM

## 模块描述

The I-PDU Multiplexer realizes two distinct functionalities:
(1) PDU multiplexing. One PDU on the bus can have different, static data layouts, defined by a
selector value. The multiplexed PDU usually is of similar size for all layouts.
(2) Container handling. Multiple PDUs are combined in one container in static or dynamic order,
transmitted as one large PDU, and then unpacked into separate PDUs at the receiver again. The
containers are usually much larger than the individual PDUs.


## 容器列表

### 1. IpduMGeneral

**描述**: Global configuration parameters of the IpduM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMContainedTxPduPriorityHandling
  长名称: ''
  描述: This parameter enables/disables handling of priority for IpduMContainedTxPdu's with
      IpduMContainedTxPduCollectionSemantics IPDUM_LAST_IS_BEST.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMConfigurationTimeBase
  长名称: ''
  描述: |
    The cycle time with which IpduM_MainFunction is invoked.
    Note: This parameter is not used by the generator.
  默认值: 0.01
  最小值: 0
  最大值: 3600
- 
  序号: 3
  名称: IpduMRxTimeBase
  长名称: ''
  描述: The period between successive calls to IpduM_MainFunctionRx. This parameter is used by the
      IpduM generator to transform the values of the reception related timing configuration
      parameters of the IpduM module to internal implementation specific counter or tick
      values.
  默认值: 0.01
  最小值: 0
  最大值: 3600
- 
  序号: 4
  名称: IpduMTxTimeBase
  长名称: ''
  描述: The period between successive calls to IpduM_MainFunctionTx. This parameter is used by the
      IpduM generator to transform the values of the transmission related timing configuration
      parameters of the IpduM module to internal implementation specific counter or tick
      values.
  默认值: 0.01
  最小值: 0
  最大值: 3600
- 
  序号: 5
  名称: IpduMDevErrorDetect
  长名称: ''
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    true: Development Error Detection is enabled.
    false: Development Error Detection is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IpduMHeaderByteOrder
  长名称: ''
  描述: This parameter defines the ByteOrder of the headers inside a Container I-PDU.
  默认值: IPDUM_BIG_ENDIAN
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IpduMStaticPartExists
  长名称: ''
  描述: |
    Allow optimizations in the case the IpduM will never be used with a static part.
    Note that this is a pre-compile option. If it is de-activated, it will not be possible to
    configure static parts after compilation.
    True: A static part may exist.
    False: A static part will never exist.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IpduMVersionInfoApi
  长名称: ''
  描述: |
    This parameter enables/disables the function IpduM_GetVersionInfo() to get major, minor and
    patch version information.
    True: version information activated.
    False: version information de-activated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IpduMUserConfigFile
  长名称: ''
  描述: |
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IpduMSafeBswChecks
  长名称: ''
  描述: |
    Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
    are checked before function is executed.
    This attribute has to be enabled for safety projects where this component is mapped to an ASIL
    partition.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. IpduMGeneration

**描述**: Contains the generation configuration parameters of the module IpduM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMOutOfBoundsWriteProtectionStrategy
  长名称: ''
  描述: |
    This parameter is used to configure a strategy to protect the code to write out of bounds.
    
    NONE: no protection strategy is generated in the data access.
    INDEX_SATURATION: arrays are blown up and the data access index is saturated by an appropriate
    mask. The advantage is the speed of the data access, but own data elements at other indexes of
    the same variable can be overridden. This debugging feature must not be used in production code!
    INDEX_CHECKING: the data access index is validated by a runtime check. The advantage is that
    values are never written to incorrect indexes of the data access. This debugging feature must
    not be used in production code!
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMOutOfBoundsWriteSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds write problems.
    This debugging feature must not be used in production code!
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IpduMOutOfBoundsReadSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds read problems.
    This debugging feature must not be used in production code!
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IpduMReduceConstantData2Define
  长名称: Reduce Constant Data To a Define
  描述: |
    This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM
    arrays as constant define.
    
    FALSE: ROM arrays are generated as data even if all values are identical.
    TRUE: ROM arrays are generated as constant define if all values are identical.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IpduMBoolDataInArrayOfStructStrategy
  长名称: ''
  描述: |
    This parameter is used to tailor the usage of boolean data in structures in all CONFIG-CLASSES.
    The difference between BITFIELD and BITMASKING depends on your compiler options and memory
    mapping.
    
    BOOLEAN: The datatype of boolean data is native boolean.
    Code: the code size is small.
    RAM: no change expected.
    ROM: the ROM size is large.
    Runtime: the runtime is fast.
    
    BITFIELD: The bitfield type is used and the compiler extracts the boolean data from structures.
    Code: the code size is larger than using BOOLEAN.
    RAM: no change expected.
    ROM: the ROM size is smaller than using BOOLEAN.
    Runtime: the runtime is larger than using BOOLEAN.
    
    BITMASKING: Generated Masks are used to extract the boolean data from structures.
    Code: the code size is larger than using BOOLEAN.
    RAM: no change expected.
    ROM: the ROM size is smaller than using BOOLEAN.
    Runtime: the runtime is larger than using BOOLEAN.
  默认值: BITMASKING
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IpduMDeduplicateIndirectedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress 0:N relational ROM data in all
    CONFIG-CLASSES without increasing the runtime.
    This option can be used in lib builds and in postbuild configurations.
    
    TRUE: 0:N relational ROM data is compressed without decreasing the runtime.
    Code: no change expected.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: no change expected.
    
    FALSE: 0:N relational ROM data is not compressed.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IpduMDataDeduplicationStrategy
  长名称: ''
  描述: |
    This parameter is used to deduplicate CONFIG-CLASS PRE-COMPILE  ROM data.
    
    NONE: The generated data is not deduplicated.
    
    WITHOUT_CAST: The data is deduplicated without using casts.
    Code: no change expected.
    RAM: no change expected.
    ROM: the ROM size can be minimized.
    Runtime: no change expected.
    
    WITH_CAST: The data is deduplicated using casts.
    Code: no change expected.
    RAM: no change expected.
    ROM: the ROM size can be minimized more than in DEDUPLICATE_CONST_DATA_WITHOUT_CAST.
    Runtime: no change expected.
  默认值: WITH_CAST
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IpduMReduceBoolDataByNegationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using the negation operator.
    0: The optimization is not performed.
    >0: This is the threshold to activate the data optimization.
    
    Code: the code size is increased due to the usage of the negation operator in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the negation operator in the data access.
  默认值: 2
  最小值: 0
  最大值: ''
- 
  序号: 9
  名称: IpduMReduceBoolDataByNumericalComparisonThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using comparison with other ROM data.
    0: The optimization is not performed.
    >0: This is the threshold to activate the data optimization.
    
    Code: the code size is increased due to the usage of the operation in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the operation in the data access.
  默认值: 2
  最小值: 0
  最大值: ''
- 
  序号: 10
  名称: IpduMReduceBoolDataByNumericalRelationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using relational comparison with other ROM data.
    0: The optimization is not performed.
    >0: This is the threshold to activate the data optimization.
    
    Code: the code size is increased due to the usage of the operation in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the operation in the data access.
  默认值: 2
  最小值: 0
  最大值: ''
- 
  序号: 11
  名称: IpduMReduceBoolDataByNumericalOperandStrategy
  长名称: ''
  描述: |
    This parameter is used to taylor the CONFIG-CLASS PRE-COMPILE ROM data deduplication mechaisms.
    A comparison with 0 is very efficient, but a numerical comparison with a value not 0 can be used
    to increase the ROM data compression rate.
    
    NONE: ROM data deduplications are switched off.
    Code: the code size is small.
    RAM: no change expected.
    ROM: the ROM size is large.
    Runtime: the runtime is fast.
    
    WITH_ZERO: ROM data deduplications can be applied with the value 0.
    Code: the code size is larger than using NONE
    RAM: no change expected.
    ROM: the ROM size is smaller than using NONE.
    Runtime: the runtime is larger than using NONE.
    
    WITH_ANY_VALUE: ROM data deduplications can be applied with any numerical value.
    Code: the code size is larger than using NONE
    RAM: no change expected.
    ROM: the ROM size is smaller than using DEDUPLICATE_DATA_WITH_ZERO.
    Runtime: the runtime is larger than using NONE.
  默认值: WITH_ANY_VALUE
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IpduMReduceNumericalDataByOffsetThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS
    PRE-COMPILE ROM data by using a constant offset.
    0: The optimization is not performed.
    >0: This is the threshold to activate the data optimization.
    
    Code: the code size is increased due to the usage of the constant offset operation in the data
    access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the constant offset operation in the data
    access.
  默认值: 2
  最小值: 0
  最大值: ''
- 
  序号: 13
  名称: IpduMReduceNumericalDataByArraySubtractionThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS
    PRE-COMPILE ROM data by using a subtraction with other ROM data.
    0: The optimization is not performed.
    >0: This is the threshold to activate the data optimization.
    
    Code: the code size is increased due to the usage of the operation in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the operation in the data access.
  默认值: 2
  最小值: 0
  最大值: ''
- 
  序号: 14
  名称: IpduMReduceDataByStreaming
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to pack generated CONFIG-CLASS PRE-COMPILE
    ROM data into a data type dependent stream.
    
    TRUE: generated const data is packed into a data type dependent stream.
    Code: no change expected.
    RAM: no change expected.
    ROM: configuration dependent smaller than with FALSE.
    Runtime: no change expected.
    
    FALSE: generated const data is not packed into a data type dependent stream.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IpduMShortSymbols
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate shortened symbol names.
    
    FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant
    names.
    TRUE: symbol names are generated based on the MIP and a CRC32.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IpduMInterfacesForDeactivatedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate bsw data interfaces for
    deactivated data elements. This is an advantage for the BSW developer to reduce the time to
    market with a development environment using auto completition and to investigate potential
    interfaces.
    
    FALSE: data interfaces are not generated if the data elementis deactivated.
    TRUE: data interfaces are generated as e.g. emty macros.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: IpduMReferringKeysInComments
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate referring keys in comments. This
    is an advantage for the developer to investigate indirections, but this feature reduces the
    overall readability of the generated data.
    
    FALSE: referring keys are not generated in comments.
    TRUE: referring keys are generated in comments.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. IpduMConfig

**描述**: This container contains the sub containers of the IpduM module. The IpduMTxPathway subcontainer
includes information about transmitted multiplex I-PDUs. The IpduMRxPathway includes information
about received multiplex I-PDUs.

该容器没有参数。

### 4. IpduMContainedRxPdu

**描述**: Configuration of a received contained Pdu.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMContainedPduHeaderId
  长名称: ''
  描述: Header Id which is part of the ContainerPdu when this ContainedPdu is inside.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: IpduMContainedPduOffset
  长名称: ''
  描述: Static offset (in bytes) of the ContainedPdu.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: IpduMPduUpdateBitPosition
  长名称: ''
  描述: This value specifies where the PDU's Update-Bit is stored in the Container PDU (bit location
      of PDU's Update-Bit in the Container PDU).
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 5. IpduMContainedTxPdu

**描述**: Configuration of a sender ContainedPdu.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMContainedPduHeaderId
  长名称: ''
  描述: Header Id which is part of the ContainerPdu when this ContainedPdu is inside.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: IpduMContainedPduOffset
  长名称: ''
  描述: Static offset (in bytes) of the ContainedPdu.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: IpduMContainedTxPduCollectionSemantics
  长名称: ''
  描述: Defines whether this IpduMContainedTxPdu shall be collected using a last-is-best or queued
      semantics.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IpduMContainedTxPduConfirmation
  长名称: ''
  描述: This Parameter determines whether for this contained I-PDU a TxConfirmation shall be provided.
      If set to TRUE a TxConfirmation is issued. It is not used when an I-PDU is requested
      using the trigger transmit API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IpduMContainedTxPduHandleId
  长名称: ''
  描述: Handle Id of the ContainedPdu.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: IpduMContainedTxPduPriority
  长名称: ''
  描述: Defines a priority of a ContainedTxPdu. 255 represents the lowest priority and 0 represent the
      highest priority.
  默认值: 255
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IpduMContainedTxPduSendTimeout
  长名称: ''
  描述: |
    Defines a ContainedPdu specific sender timeout which can reduce the ContainerPdu timer when this
    ContainedPdu is put inside the ContainerPdu.
    
    If this parameter is omitted, the linked Container-PDU must have a SendTimeout configured.
    
    The value 0 does not have special semantics here, 0 is a normal, valid value.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 8
  名称: IpduMContainedTxPduTrigger
  长名称: ''
  描述: Defines whether this Pdu triggers the sending of the ContainerPdu.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IpduMPduUpdateBitPosition
  长名称: ''
  描述: This value specifies where the PDU's Update-Bit is stored in the Container PDU (bit location
      of PDU's Update-Bit in the Container PDU).
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 6. IpduMContainerRxPdu

**描述**: Configuration of a receiver ContainerPdu which may collect several ContainedPdus.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMContainerHeaderSize
  长名称: ''
  描述: Defines the layout of the header information (header id and length).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMContainerPduProcessing
  长名称: ''
  描述: Defines whether the handling of this ContainerPdu shall be done in the context of the caller
      (IMMEDIATE) or in the next IpduM main function (DEFERRED).
  默认值: IPDUM_PROCESSING_IMMEDIATE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IpduMContainerQueueSize
  长名称: ''
  描述: Defines a local queue for handling of each ContainerPdu.
  默认值: 1
  最小值: 0
  最大值: 254
- 
  序号: 4
  名称: IpduMContainerRxAcceptContainedPdu
  长名称: ''
  描述: Defines for the received IpduMRxContainerPdu whether the list of referencing
      IpduMRxContainedPdus (via the reference IpduMRxContainedPduContainerRef) is a closed
      set.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IpduMContainerRxHandleId
  长名称: ''
  描述: Handle Id used by the PduR for RxIndication.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 7. IpduMContainerTxPdu

**描述**: Configuration of a transmitted container Pdu.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMContainerHeaderSize
  长名称: ''
  描述: Defines the layout of the header information (header id and length).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMContainerQueueSize
  长名称: ''
  描述: |
    Defines a local queue for handling of each ContainerPdu.
    
    The actual queue length in the implementation is incremented by 1 as a performance optimization.
    So the current instance is within the queue and does not need additional copy instructions. The
    maximum value was lowered to 254 to enable this performance optimization.
  默认值: 1
  最小值: 1
  最大值: 254
- 
  序号: 3
  名称: IpduMContainerTxConfirmationTimeout
  长名称: ''
  描述: This timeout (in seconds) defines the timeout period for monitoring the reception of the
      TxConfirmation. It is not used when an I-PDU is requested using the trigger transmit
      API.
  默认值: 0
  最小值: 0
  最大值: 65.535
- 
  序号: 4
  名称: IpduMContainerTxFirstContainedPduTrigger
  长名称: ''
  描述: Defines if the transmission of this IpduMContainerTxPdu shall be requested right after the
      first IpduMContainedTxPdu was put into it.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IpduMContainerTxHandleId
  长名称: ''
  描述: Handle Id used by the PduR for TxConfirmation and for TriggerTransmit of the ContainerPdu.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: IpduMContainerTxSendTimeout
  长名称: ''
  描述: When this timeout expires the ContainerPdu is triggered for sending. The respective timer is
      started when the first Pdu is put into the ContainerPdu.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 7
  名称: IpduMContainerTxSizeThreshold
  长名称: ''
  描述: Defines the size threshold in bytes which, when exceeded, triggers the sending of the
      ContainerPdu although the maxium Pdu size (PduLength parameter of Pdu object)  has not
      been reached yet.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 8
  名称: IpduMContainerTxTriggerMode
  长名称: ''
  描述: Defines whether this ContainerPdu is fetched via trigger transmit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IpduMUnusedAreasDefault
  长名称: ''
  描述: IpduM fills not updated areas of the Container PDU with this byte-pattern.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 8. IpduMRxPathway

**描述**: Defines one lower layer I-PDU that is received from the network and resolved to multiple upper layer
I-PDUs depending on the selector field value.

该容器没有参数。

### 9. IpduMRxIndication

**描述**: Contains the configuration for incoming calls to the IpduM_RxIndication API.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMByteOrder
  长名称: ''
  描述: |
    This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the
    selectorField within the MultiplexedPdu.
    This is necessary because the positions are defined differently (LSB for little endian and MSB
    for big endian) based on endianness.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMRxHandleId
  长名称: ''
  描述: This is the I-PDU ID of the incoming I-PDU. If an incoming RxIndication's I-PDU ID matches
      this value then it is unpacked according to the specification in this container.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 10. IpduMRxDynamicPart

**描述**: This container contains the configuration for the dynamic part of incoming RxIndication calls. If an
incoming received I-PDU's selector field matches the IpduMRxSelectorValue of any of the dynamic
parts, the new outgoing I-PDU for the dynamic part is de-multiplexed according to the corresponding
dynamic IpduMSegment specification and sent out with the I-PDU ID referenced by
IpduMOutgoingDynamicPduRef.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMRxSelectorValue
  长名称: ''
  描述: |
    Identifies the dynamic part that is transmitted within the received multiplexed I-PDU.
    If the selector field value of the received multiplex I-PDU matches this value. It will be
    de-multiplexed according to the configuration in the parent IpduMRxDynamicPart container.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 11. IpduMSegment

**描述**: Defines the location and the length of a segment that is used to describe the composition of a
multiplexed I-PDU for one selector field value. The data area that is covered by the configured
segment(s) is copied from the lower layer I-PDU t the upper layer I-DU. Thereby the data is copied
to the same location within the upper layer I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSegmentLength
  长名称: ''
  描述: Length of the segment [bit].
  默认值: ''
  最小值: 1
  最大值: 2032
- 
  序号: 2
  名称: IpduMSegmentPosition
  长名称: ''
  描述: |
    Segments bit position in the multiplexed Pdu.
    Bits within a byte are always numbered in ascending order. Bytes are ordered based on
    IpduMByteOrder.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 12. IpduMRxStaticPart

**描述**: This container describes the optional static part of incoming lower layer I-PDU. If a static part is
defined any reception of the lower layer I-PDU will cause the notification of the upper layer I-PDU
representing the static part. This is independent from the selector field value.

该容器没有参数。

### 13. IpduMSegment

**描述**: This contains the location and the length of a segment. A segment must fit inside the I-PDU. The
segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same
position in the destination I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSegmentLength
  长名称: ''
  描述: Length of the segment [bit].
  默认值: ''
  最小值: 1
  最大值: 2032
- 
  序号: 2
  名称: IpduMSegmentPosition
  长名称: ''
  描述: Segments bit position in the multiplexed Pdu.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 14. IpduMSelectorFieldPosition

**描述**: Defines the location and the length of the selector field that is used to identify the dynamic part
of each multiplexed I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSelectorFieldLength
  长名称: ''
  描述: Length of the selector field [bit].
  默认值: ''
  最小值: 1
  最大值: 16
- 
  序号: 2
  名称: IpduMSelectorFieldPosition
  长名称: ''
  描述: |
    Selector field bit position in the multiplexed Pdu.
    Bits are numbered ascending, bytes depending on the endianness defined in IpduMByteOrder.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 15. IpduMTxPathway

**描述**: Defines one lower layer I-PDU that is assembled from multiple upper layer I-PDUs depending on the
selector field value.

该容器没有参数。

### 16. IpduMTxRequest

**描述**: This is used to specify the configuration for Transmit requests.

There will one instance of this container for each I-PDU that can be requested for transmission (the
outgoing I-PDUs) by the IpduM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMByteOrder
  长名称: ''
  描述: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for
      the selectorField within the MultiplexedPdu.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMIPduUnusedAreasDefault
  长名称: ''
  描述: |
    IPDUM  module fills unused areas of a transmitted multiplexed I-PDU with this bit-pattern.
    If this attribute is undefined unused areas are not initialized any may have an arbitrary value
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IpduMTxConfirmationPduId
  长名称: Tx Confirmation Pdu Id
  描述: The handle Id used by the lower layer to identify this IPDUM I-PDU during TriggerTransmit and
      TxConfirmation calls.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: IpduMTxConfirmationTimeout
  长名称: ''
  描述: |
    Specifies the timeout time for monitoring the TxConfirmation call from the lower layer (i.e. the
    transmission of the corresponding multiplex I-PDU occured).
    Parameter is not used for lower layer I-PDU that use the TriggerTransmit API.
  默认值: 0
  最小值: 0
  最大值: 3600
- 
  序号: 5
  名称: IpduMTxTriggerMode
  长名称: ''
  描述: |
    Specifies the upper layer transmission event that causes the transmission of the multiplexed
    I-PDU through the lower layer.
            NONE: do not trigger transmission on upper layer transmission events
            STATIC_PART_TRIGGER: trigger transmission if the static part I-PDU is transmitted to
    IpduM
            DYNAMIC_PART_TRIGGER: trigger transmission if the dynamic part I-PDU is transmitted to
    IpduM
            STATIC_OR_DYNAMIC_PART_TRIGGER: trigger transmission if the static or dynamic part I-PDU
    is transmitted to IpduM
  默认值: DYNAMIC_PART_TRIGGER
  最小值: ''
  最大值: ''
```

### 17. IpduMSelectorFieldPosition

**描述**: This contains the location and the length of the selector field.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSelectorFieldLength
  长名称: ''
  描述: Length of the selector field [bit].
  默认值: ''
  最小值: 1
  最大值: 16
- 
  序号: 2
  名称: IpduMSelectorFieldPosition
  长名称: ''
  描述: Selector field bit position in the multiplexed Pdu.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 18. IpduMTxDynamicPart

**描述**: Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with
the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are
copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honored. This
container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing
I-PDU there will be one instance of this container for the dynamic part.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMJitUpdate
  长名称: ''
  描述: |
    If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of
    the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be
    cleared correctly.
    
    If configured to false, the data currently present in the IpduM's buffer for this dynamic part
    I-PDU is used, i.e. the dynamic part that was transmitted last. This way, transmissions may be
    on the bus faster, depending on configuration.
    
    Jit update can be activated independently from the lower layer.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMTxDynamicConfirmation
  长名称: ''
  描述: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission
      of the multiplexed I-PDU by the lower layer.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IpduMTxDynamicHandleId
  长名称: ''
  描述: This is the handle id of a requested transmit. When the handle of an incoming Tx Request
      matches this, the TxDynamicPart is multiplexed according to the corresponding
      IpduMSegments.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 19. IpduMSegment

**描述**: Defines the location and the length of a segment that is used to describe the composition of a
multiplexed I-PDU for one selector field value. The data area that is covered by the configured
segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied
to the same location within the upper layer I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSegmentLength
  长名称: ''
  描述: Length of the segment in bits.
  默认值: ''
  最小值: 1
  最大值: 2032
- 
  序号: 2
  名称: IpduMSegmentPosition
  长名称: ''
  描述: Segments bit position in the multiplexed Pdu.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 20. IpduMTxStaticPart

**描述**: This container describes the optional static part of outgoing multiplexed lower layer I-PDU. If a
static part is defined any transmission of the lower layer I-PDU will include I-PDU data provided by
the static part. This is independent from the selector field value that shall be transmitted.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMJitUpdate
  长名称: ''
  描述: |
    If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of
    the PduR. This way, transmitted data is always up-to-date and update bits in Autosar Com can be
    cleared correctly.
    
    If configured to false, the data currently present in the IpduM's buffer for the static part
    I-PDU is used, i.e. the static part that was transmitted last. This way, transmissions may be on
    the bus faster, depending on configuration.
    
    Jit update can be activated independently from the lower layer.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMTxStaticConfirmation
  长名称: ''
  描述: If enabled the I-PDU transmission is confirmed to the upper layer upon successful transmission
      of the multiplexed I-PDU by the lower layer.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IpduMTxStaticHandleId
  长名称: ''
  描述: This is the handle id of a requested transmit. If the handle of an incoming Tx Request matches
      this, the TxStaticPart is multiplexed according to the corresponding IpduMSegments and
      the send mode is honored.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 21. IpduMSegment

**描述**: Defines the location and the length of a segment that is used to describe the composition of a
multiplexed I-PDU for one selector field value. The data area that is covered by the configured
segment(s) is copied from the lower layer I-PDU to the upper layer I-PDU. Thereby the data is copied
to the same location within the upper layer I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSegmentLength
  长名称: ''
  描述: Length of the segment in bits.
  默认值: ''
  最小值: 1
  最大值: 2032
- 
  序号: 2
  名称: IpduMSegmentPosition
  长名称: ''
  描述: Segments bit position in the multiplexed Pdu.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 22. IpduMPublishedInformation

**描述**: Additional published parameters not covered by CommonPublishedInformation container. Note that these
parameters do not have any configuration class setting, since they are published information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMRxDirectComInvocation
  长名称: Direct Com Invocation
  描述: If set to TRUE the methods Com_RxIndication and Com_TriggerTransmit are invocated directly
      without using the PduR as intermediate module. This is required by the AUTOSAR
      requirement IPDUM140.
  默认值: true
  最小值: ''
  最大值: ''
```

