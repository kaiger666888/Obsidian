# PduR

## 模块描述

Configuration of the PDUR (PDU Router) module.

## 容器列表

### 1. PduRBswModules

**描述**: Each container describes a specific BSW module  that the PDU Router shall interface to. All
interfacing modules (below and above the PDUR) including their API requirements need to be
configured explicitly.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRCancelReceive
  长名称: ''
  描述: |
    Specifies if the transport protocol BSW module supports the CancelReceive API or not. The API
    allows to cancel an ongoing transport protocol reception.
    
    Value true means that the BSW module supports the CancelReceive interface which an upper layer
    module can call and also that it can call the CancelReceive interface of a lower layer module.
    Value false means that the BSW module does not support the CancelReceive interface which an
    upper layer module can call and also that it shall not call the CancelReceive interface of a
    lower layer module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PduRCancelTransmit
  长名称: ''
  描述: |
    Specifies if the BSW module supports the CancelTransmit API or not. The API allows to cancel an
    ongoing transport protocol transmission.
    
    Value true means that the BSW module supports the CancelTransmit interface which an upper layer
    module can call and also that it can call the CancelTransmit interface of a lower layer module.
    Value false means that the BSW module does not support the CancelTransmit interface which an
    upper layer module can call and also that it shall not call the CancelTransmit interface of a
    lower layer module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PduRChangeParameterRequestApi
  长名称: ''
  描述: |
    Specifies if the transport protocol BSW module supports the ChangeParameter API or not. The API
    allows to change transport protocol parameters like BS or STmin.
    
    Value true means that the BSW module supports the ChangeParameter interface which an upper layer
    module can call and also that it can call the ChangeParameter interface of a lower layer module.
    Value false means that the BSW module does not support the ChangeParameter interface which an
    upper layer module can call and also that it shall not call the ChangeParameter interface of a
    lower layer module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: PduRCommunicationInterface
  长名称: ''
  描述: |
    Specifies if the BSW module supports the communication interface APIs or not. A module can have
    both APIs, communication interface and transport protocol (e.g. the Com module).
    
    Value true means that the BSW module supports the communication interface APIs.
    Value false means that the BSW module does not support the communication interface APIs.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PduRLowerModule
  长名称: ''
  描述: |
    Specifies who will call the BSW module APIs and who will implement the called APIs. An upper
    module can also be an lower module (e.g. the IpduM module).
    
    For example, if the CanIf module is referenced then the PduR module will implement the
    PduR_CanIfRxIndication API. And the PduR module will call the CanIf_Transmit API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PduRRetransmission
  长名称: ''
  描述: |
    This parameter is not used by the PduR. This featue is not supported.
    
    Specifies if the destination transport protocol BSW module supports the the retransmission
    feature. This parameter might be set to false if the retransmission feature is not used, even
    though the destination transport protocol is supporting it.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: PduRTransportProtocol
  长名称: ''
  描述: |
    Specifies if the BSW module supports the transport protocol APIs or not.
    
    Value true means that the BSW module supports the transport protocol APIs.
    Value false means that the BSW module does not support the transport protocol APIs.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: PduRTriggertransmit
  长名称: ''
  描述: |
    Specifies if the BSW module supports the TriggerTransmit API or not.
    
    Value true means that the BSW module supports the TriggerTransmit interface which a lower layer
    module can call and also that it can call the TriggerTransmit interface of an upper layer
    module.
    Value false means that the BSW module does not support the TriggerTransmit interface which a
    lower layer module can call and also that it shall not call the TriggerTransmit interface of an
    upper layer module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: PduRTxConfirmation
  长名称: ''
  描述: |
    Specifies if the transport protocol BSW module supports the TxConfirmation API or not.
    
    Value true means that the BSW module supports the TxConfirmation interface which a lower layer
    module can call and also that it can call the TxConfirmation interface of an upper layer module.
    Value false means that the BSW module does not support the TxConfirmation interface which a
    lower layer module can call and also that it shall not call the TxConfirmation interface of an
    upper layer module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: PduRUpperModule
  长名称: ''
  描述: |
    Specifies who will call the BSW module APIs and who will implement the called APIs. An upper
    module can also be an lower module (e.g. the IpduM module).
    
    For example, if the Com module is referenced then the PduR module will implement the
    PduR_ComTransmit API. And the PduR module will call the Com_RxIndication API. Other APIs are of
    course also covered.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: PduRUseTag
  长名称: ''
  描述: |
    True enables the usage of the tag "<Up>" in the following API calls:
    - PduR_<Up>CancelReceive
    - PduR_<Up>CancelTransmit
    - PduR_<Up>ChangeParameter
    
    Example: If used by Com and the parameter is enabled the PduR_ComCancelTransmit is used. The
    background is that upper layer modules differ in usage of this tag (e.g. Com is using the tag,
    Dcm is not).
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. PduRGeneral

**描述**: Contains the general configuration parameters of the module PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRDevErrorDetect
  长名称: ''
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    true: Development error detection is enabled.
    false: Development error detection is disabled.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PduRVersionInfoApi
  长名称: ''
  描述: This parameter enables/disables the function PduR_GetVersionInfo() to get major, minor and
      patch version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PduRZeroCostOperation
  长名称: ''
  描述: |
    This parameter is not used by the PduR. This featue is not supported.
    
    If set the PduR configuration generator will report an error if zero-cost-operation cannot be
    fulfilled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: PduRUserConfigurationFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation to PduR_Cfg.h
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PduRMetaDataSupport
  长名称: ''
  描述: |
    Enable this switch if aTransport protocol uses MetaData. The size of the MetaData is defined by
    the configuration parameter MetaDataLength of the global PDU definitions.
    
    The setting of this switch is irrelevant for the routing of communication interface metadata
    Pdus.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PduRPduCallback
  长名称: ''
  描述: |
    This parameter activates / deactivates Pdu callbacks.
    The activation of routing path specific BswM callbacks is done by BswM mode request source
    references.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: PduRSwitching
  长名称: ''
  描述: |
    The PduR switching functionality can be used to dynamically learn the destination of routing
    paths. This will be done using the contents of the Pdu metadata. For a detailed description of
    this feature see the PduR technical reference.
    This parameter activates / deactivates the switching functionality.
    The configuration of the switching behavior is done by the PduRDataPlane configuration
    structure.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: PduR_QueueOverflowNotification
  长名称: ''
  描述: |
    This parameter activates / deactivates a PduR InterfaceTxBuffer overflow notification. The
    PduR_ErrorNotification.h and _PduR_ErrorNotification.c (the C- file is a template) is generated
    by the PduR if the "PduR Queue Overflow Notification" is enabled. This header must be included
    and the function must be implemented.
    
    Backround: In case of a communication interface routing with unfavourable FIFO configuration or
    if the destination bus is not available a buffer overflow can occurs. In this case the FIFO is
    flushed.
    
    Caution: The function is called in the interrupt context
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: PduR_ErrorNotificationModuleName
  长名称: Error Notification Module Name
  描述: If the PduR_QueueOverflowNotification is enabled the parameter can be used to set an
      individual error notification module name. The header file name is <Prefix>_Cbk.h. The
      default prefix is "ErrorNotification"
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: PduRSafeBswChecks
  长名称: ''
  描述: |
    Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
    are checked before function is executed.
    This attribute has to be enabled for safety projects where this component is mapped to an ASIL
    partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: PduRMainFunctionPeriod
  长名称: ''
  描述: The time between two MainFunction calls (as float in seconds).
  默认值: 0.01
  最小值: 0
  最大值: 0.255
- 
  序号: 12
  名称: PduREnableDeferredTransmission
  长名称: ''
  描述: Must be enabled if deferred transmission shall be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: PduREnableDeferredReception
  长名称: ''
  描述: Must be enabled if deferred reception shall be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: PduRSupportMulticore
  长名称: ''
  描述: Enable, if multicore capabilities are required.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: PduRDeferredEventCacheSize
  长名称: ''
  描述: |
    Size of the Deferred Event Cache. It caches the handle Ids of Deferred routing paths which then
    will be processed in the next MainFunction.
    The size is used per Core. The size corresponds to the amount of deferred events which can be
    cached.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 16
  名称: PduRRoutingTypeGateway
  长名称: ''
  描述: Activate/Deactivate the routing between lower layer modules.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: PduRSpinlockRetryCounter
  长名称: ''
  描述: |
    After this value is reached, the Spinlock is assumed to be aquired even if the TryToGetSpinlock
    API says otherwise.
    
    This value is ignored if there are no Spinlocks configured.
  默认值: 4294967295
  最小值: 1
  最大值: 4294967295
- 
  序号: 18
  名称: PduRExtendedErrorChecks
  长名称: ''
  描述: Enables the extended error checks for PduR Ram variables. The PduR administration variables
      will be checked when read. This is only required for multi-application configurations
      with OsApplications of different quality level.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. PduRGeneration

**描述**: Contains the generation configuration parameters of the module PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduROutOfBoundsWriteProtectionStrategy
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
  名称: PduROutOfBoundsWriteSanitizer
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
  名称: PduROutOfBoundsReadSanitizer
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
  名称: PduRNumericalDataTypeMinimizationStrategy
  长名称: ''
  描述: |
    This parameter is used to minimize the datatypes of CONFIG-CLASS PRE-COMPILE numerical data
    based on the used values.
    
    NONE: the datatype is not minimized.
    WITHOUT_CAST: the datatype of numerical data is minimized. Unsigned data types are not changed
    to signed datatypes.
    WITH_CAST: the datatype of numerical data is minimized. Unsigned data types can be optimized to
    signed datatypes.
  默认值: WITH_CAST
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PduRReduceConstantData2Define
  长名称: Reduce Constant Data To a Define
  描述: |
    This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM
    arrays as constant define.
    
    FALSE: ROM arrays are generated as data even if all values are identical.
    TRUE: ROM arrays are generated as constant define if all values are identical.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PduRBoolDataInArrayOfStructStrategy
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
  序号: 7
  名称: PduRDeduplicateIndirectedData
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
  序号: 8
  名称: PduRDataDeduplicationStrategy
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
  序号: 9
  名称: PduRReduceBoolDataByNegationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using the negation operator.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
    
    Code: the code size is increased due to the usage of the negation operator in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the negation operator in the data access.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 10
  名称: PduRReduceBoolDataByNumericalComparisonThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using numerical comparison with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
    
    Code: the code size is increased due to the usage of the operation in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the operation in the data access.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 11
  名称: PduRReduceBoolDataByNumericalRelationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using relational comparison with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
    
    Code: the code size is increased due to the usage of the operation in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the operation in the data access.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 12
  名称: PduRReduceBoolDataByNumericalOperandStrategy
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
  序号: 13
  名称: PduRReduceNumericalDataByOffsetThreshold
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
  最大值: 9223372036854775807
- 
  序号: 14
  名称: PduRReduceNumericalDataByArraySubtractionThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS
    PRE-COMPILE ROM data by using a sutraction with other ROM data.
    0: The optimization is not performed.
    >0: This is the threshold to activate the data optimization.
    
    Code: the code size is increased due to the usage of the operation in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the operation in the data access.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 15
  名称: PduRReduceDataByStreaming
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
  序号: 16
  名称: PduRShortSymbols
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
  序号: 17
  名称: PduRInterfacesForDeactivatedData
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
  序号: 18
  名称: PduRReferringKeysInComments
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

### 4. PduRRoutingTables

**描述**: This container groups multiple configuration containers that are used to specify the routing
behaviour of the PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRConfigurationId
  长名称: ''
  描述: Identification of the configuration of the PDUR configuration.This identification can be read
      using the PduR API (PduR_GetConfigurationId).
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 5. PduRRoutingPathGroup

**描述**: A routing path group is a group of PduRDestPdus that can be disabled and enabled during runtime. The
group contains the PduRDestPdus and not the routing path itself. This way the destinations of a
routing path can be enabled and disabled independently. Enabling and disabling of routing path
groups is typically used by the BswM module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRIsEnabledAtInit
  长名称: ''
  描述: If set to true this routing path group will be enabled after initializing the PDU Router
      module (i.e. enabled in the PduR_Init function). If set to false the routing path group
      will be disabled after initializing the PDU Router module
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PduRRoutingPathGroupId
  长名称: ''
  描述: Identification of the routing group.This numerical Identifier will be calculate automatically.
      Use the generated symbolic value to enable/disable the group.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 6. PduRRoutingTable

**描述**: Contains routing path containers

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRIsMinimumRouting
  长名称: ''
  描述: This parameter is not used by the PduR. This featue is not supported.
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. PduRRoutingPath

**描述**: This container contains the routing pathways.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRRoutingPathCommunicationType
  长名称: ''
  描述: |
    This parameter must never be changed manually. It is calculated automatically by the PduR
    validation.
    
    PduR routing path communication type.
    
    The communication type determines the used API type of the routing path:
    COMMUNICATION_INTERFACE: Unsegmented Pdus.
    TRANSPORT_PROTOCOL: Segmented Pdus
    UNDEFINED: The communication type cannot be determined.
  默认值: UNDEFINED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PduRMulticoreRoutingPath
  长名称: ''
  描述: |
    This parameter must never be changed manually. It is calculated automatically by the PduR
    validation.
    
    This parameter is enabled, if this routing path is a cross-core routing path.
  默认值: false
  最小值: ''
  最大值: ''
```

### 8. PduRDestPdu

**描述**: This container specifies one destination for the PDU to be routed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRDestPduDataProvision
  长名称: ''
  描述: Specifies how data is provided: direct (as part of the Transmit call) or via the
      TriggerTransmit callback function after the transmission request. Only required for
      communication interface Tx DestPdus.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PduRDestPduHandleId
  长名称: ''
  描述: |
    This parameter must never be changed manually. It is calculated automatically by the PduR
    validation.
    
    PDU identifier assigned by PDU Router. Used by communication interface and transport protocol
    modules for confirmation and trigger transmit API calls
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: PduRTpThreshold
  长名称: ''
  描述: |
    Defines the number of bytes which shall be received before transmission on the destination shall
    be triggered (DestModule_Transmit is called).
    It is only relevant for queued transport protocol routing paths. This parameter is only used for
    derived routing paths due to compatibility reasons.
    It is sychronized to the corresponding
    /MICROSAR/PduR/PduRRoutingTables/PduRQueue/PduRSharedBufferQueue/PduRTpThreshold parameter.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: PduRTransmissionConfirmation
  长名称: ''
  描述: |
    Specifies if the destination BSW module will call the TxConfirmation API.
    
    This parameter is only relevant for communication interface routing paths. Transport protocol
    modules will always call the TxConfirmation API.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PduRDestPduDirection
  长名称: ''
  描述: |
    This parameter must never be changed manually. It is calculated automatically by the PduR
    validation.
    
    PduR routing path destination Pdu communication direction.
    
    RECEIVE: The routing path destination is a reception Pdu.
    TRANSMIT: The routing path destination is a transmission Pdu.
    UNDEFINED: The communication direction cannot be determined.
  默认值: UNDEFINED
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PduRDestPduRoutingType
  长名称: ''
  描述: |
    This parameter must never be changed manually. It is calculated automatically by the PduR
    validation.
    
    PduR routing path destination Pdu routing type.
    
    The routing type determines the routing operation mode of the routing path:
    API_FORWARDING: Routing between a lower layer and an upper layer module.
    GATEWAY_ROUTING: Routing between a lower layer module(s).
    UNDEFINED: The routing type cannot be determined.
  默认值: UNDEFINED
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: PduRDestPduQueueDepth
  长名称: ''
  描述: |
    This parameter is deprecated and can't be used anymore.
    
    The parameter was moved to the corresponding /MICROSAR/PduR/PduRRoutingTables/PduRQueue
    container which shall be referenced by this PduRDestPdu.
  默认值: 2
  最小值: 1
  最大值: 65535
- 
  序号: 8
  名称: PduRDestPduDataProcessing
  长名称: ''
  描述: |
    This option determines in which context the routing to the destination module is performed.
    IMMEDIATE: The routing is performed in either transmit or indication function.
    DEFERRED: The routing is performed in the context of a main function.
  默认值: IMMEDIATE
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: PduRPduLengthHandlingStrategy
  长名称: ''
  描述: |
    This parameter is only used for communication interface routings. It is ignored for transport
    protocol routings.
    UNUSED: use this value for Tp routing paths or unqueued If routing paths
    SHORTEN: the If Pdu is shortened to the configured global Pdu length if a larger Pdu is received
    at the source (default value from previous PduR versions)
    DISCARD: the If Pdu is discarded if a larger Pdu than configured is received at the source
    IGNORE: the If Pdu length is ignored and handed over to the Destination modules. (only for
    unqueued IF Routing paths)
  默认值: UNUSED
  最小值: ''
  最大值: ''
```

### 9. PduRDefaultValue

**描述**: Specifies the default value of the I-PDU. Only required if this PduRDestPdu uses a SingleBuffer
usecase with data provistion trigger transmit.

该容器没有参数。

### 10. PduRDefaultValueElement

**描述**: Each value element is represented by the element and the position in an array.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRDefaultValueElement
  长名称: ''
  描述: The default value consists of a number of elements. Each element is one byte long and the
      number of elements is specified by SduLength. The position of this parameter in the
      container is specified by the PduRElementBytePosition parameter.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: PduRDefaultValueElementBytePosition
  长名称: ''
  描述: This parameter specifies the byte position of the element within the default value
  默认值: 0
  最小值: 0
  最大值: 255
```

### 11. PduRSrcPdu

**描述**: This container specifies the source of the PDU to be routed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRSourcePduHandleId
  长名称: ''
  描述: |
    This parameter must never be changed manually. It is calculated automatically by the PduR
    validation.
    
    PDU identifier assigned by PDU Router.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: PduRSrcPduDirection
  长名称: ''
  描述: |
    This parameter must never be changed manually. It is calculated automatically by the PduR
    validation.
    
    PduR routing path source Pdu communication direction.
    
    RECEIVE: The routing path source is a reception Pdu.
    TRANSMIT: The routing path source is a transmission Pdu.
    UNDEFINED: The communication direction cannot be determined.
  默认值: UNDEFINED
  最小值: ''
  最大值: ''
```

### 12. PduRTpBufferTable

**描述**: Please add Tp Buffers to the PduRTxBufferTable. TpBufferTable is not used anymore!

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRMaxTpBufferNumber
  长名称: ''
  描述: Please add Tp Buffers to the PduRTxBufferTable. TpBufferTable is not used anymore!
  默认值: 0
  最小值: 0
  最大值: 0
```

### 13. PduRTpBuffer

**描述**: Please add Tp Buffers to the PduRTxBufferTable. TpBufferTable is not used anymore!

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRTpBufferLength
  长名称: ''
  描述: Length of the TP buffer in number of bytes
  默认值: ''
  最小值: 1
  最大值: 65535
```

### 14. PduRTxBufferTable

**描述**: This container contains the buffers used for queueing communication interfaces and transport
protocol Pdus.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRMaxTxBufferNumber
  长名称: ''
  描述: |
    This parameter is not used by the PduR.
    
    maximum number of Tx buffers.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 15. PduRTxBuffer

**描述**: Specifies a buffer used for communication interface and transport protocol gatway routing.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRPduMaxLength
  长名称: ''
  描述: Length of the Tx buffer in number of bytes.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: PduRTxBufferDepth
  长名称: ''
  描述: |
    PduRTxBufferDepth is not used anymore.
    
    Set the depth at the corresponding /MICROSAR/PduR/PduRRoutingTables/PduRQueue container.
  默认值: 1
  最小值: 1
  最大值: 67108864
- 
  序号: 3
  名称: PduRTxBufferUsageType
  长名称: ''
  描述: |
    This parameter must never be changed manually. It is calculated automatically by the PduR
    validation.
    
    IMPLICIT_BUFFER: This TxBuffer is not referenced by any PduRSharedBufferQueue. It can be used by
    all PduRSharedBufferQueues which have no PduRTxBuffer assigned.
    EXPLICIT_BUFFER: This TxBuffer is referenced by one or many PduRSharedBufferQueues. It is only
    used by these Queues.
  默认值: IMPLICIT_BUFFER
  最小值: ''
  最大值: ''
```

### 16. PduRDataPlaneTable

**描述**: This container specifies the available DataPlanes.

该容器没有参数。

### 17. PduRDataPlane

**描述**: This container specifies the behavior of an PduR data plane. A data plane is used for dynamic
learning of routing relations between communication sources (e.g. external testers) and
communication destinations (e.g. diagnosed onboard ECUs).

该容器没有参数。

### 18. PduRConnection

**描述**: Specifies the communication relation between the communication sources (e.g. request transmitted by
external tester) and related communication destinations (e.g. response transmitted by diagnosed
onboard ECU).

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRConnectionHandleId
  长名称: ''
  描述: Connection handle ID
  默认值: 1
  最小值: 1
  最大值: 254
```

### 19. PduRSaTaSwitchingStrategy

**描述**: Switching strategy based on a source and target address.

- Learn source address location (PduRConnection) from every received Pdu
- Broadcast the received Pdu if the target address location is not yet known
- Route the received Pdu to the learned location (PduRConnection) if the target address is already
known

该容器没有参数。

### 20. PduRLinearTaToSaCalculationStrategy

**描述**: The target address is the CAN ID of the received Pdu.
The source address is calculated by adding/subtracting a offset to target address and application of
a bit mask.

Calculation:
for Pdus referenced by PduRAddOffsetSrcPduRef:
    source address = ( target address + offset) & mask
for Pdus referenced by PduRSubtractOffsetSrcPduRef:
    source address = ( target address - offset) & mask

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduROffset
  长名称: ''
  描述: Offset added to the target address.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: PduRMask
  长名称: ''
  描述: Bit mask applied to the meta data of the received Pdus.
  默认值: 255
  最小值: 0
  最大值: 4294967295
```

### 21. PduRSaTaFromMetaDataCalculationStrategy

**描述**: The source- and target address are determined from the Pdu meta data (e.g. the CAN ID) based on the
configured start- and end bit positions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRSaStartBitPosition
  长名称: ''
  描述: Start bit position of the source address.
  默认值: 0
  最小值: 0
  最大值: 31
- 
  序号: 2
  名称: PduRSaEndBitPosition
  长名称: ''
  描述: End bit position of the source address.
  默认值: 0
  最小值: 0
  最大值: 31
- 
  序号: 3
  名称: PduRTaStartBitPosition
  长名称: ''
  描述: Start bit position of the target address.
  默认值: 0
  最小值: 0
  最大值: 31
- 
  序号: 4
  名称: PduRTaEndBitPosition
  长名称: ''
  描述: End bit position of the target address.
  默认值: 0
  最小值: 0
  最大值: 31
```

### 22. PduRExclusiveArea

**描述**: Exclusive Area that shall protect shared memory in a single core routing relation.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRExclusiveAreaId
  长名称: ''
  描述: Id of the ExclusiveArea that shall protect the shared memory.
  默认值: 0
  最小值: 0
  最大值: 0
```

### 23. PduRSpinLock

**描述**: Spinlock to protect shared memory in multicore usescase. For each Spinlock a designated variable is
created which must be locked by a user specific Appl_Get/ReleaseSpinlock function.

该容器没有参数。

### 24. PduRSingleBuffer

**描述**: A single buffer can only be used for Communication Interface routings with TriggerTransmit data
provision. It can be used for a last-is-best use case. The Pdu in the queue will always be
overwritten. The destination can read the queue and will always get the latest data.

该容器没有参数。

### 25. PduRSharedBufferQueue

**描述**: This queue can be used for both communication interface and transport protocol routing paths. It has
a First-In-First-Out behaviour (FIFO).
The actual memory used by this queue must be reserved using PduRTxBuffer container. These will be
used by queues of this type.

A PduRTxBuffer can either be referenced explicitly by the corresponding parameter or it can be used
implicitly by not referencing any PduRTxBuffer.
One PduRTxBuffer can either be allocated by all queues which explicitly reference this buffer or by
all queues which do not reference any buffer.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRQueueDepth
  长名称: ''
  描述: This parameter defines how many Pdus can be stored in the queue.
  默认值: 2
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: PduRTpThreshold
  长名称: ''
  描述: |
    This parameter is only required if this queue is used by transport protocol routing paths.
    
    Defines the number of bytes which shall be received before transmission on the destination shall
    be triggered (DestModule_Transmit is called).
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 26. PduRCommunicationInterfaceQueue

**描述**: This queue can only be used for communication interface routing paths. It has a First-In-First-Out
behaviour (FIFO).

The memory for this queue is automatically allocated. It is only used by this queue and can not be
shared.
This dedicated memory results in much less overhead than in a shared buffer queue.
For small communication interface Pdus it is advised to use this queue (if FIFO behaviour is
required) as buffer sharing results in a large overhead.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRQueueDepth
  长名称: ''
  描述: This parameter defines how many Pdus can be stored in the queue.
  默认值: 2
  最小值: 1
  最大值: 65535
```

### 27. PduRMulticoreQueue

**描述**: Multicore queue is used to perform the routing of communication interface routings between different
applications.

Each container consists of two unidirectional multicore queues from application A to application B
and vice versa.
Applications A and B can be a source and a destination at the same time. It is possible to specify
the queue size for each direction independently.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRMulticoreQueueSizeAtoB
  长名称: ''
  描述: Size of the multicore queue for communication from application A to application B.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: PduRMulticoreQueueSizeBtoA
  长名称: ''
  描述: Size of the multicore queue for communication from application B to application A.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

