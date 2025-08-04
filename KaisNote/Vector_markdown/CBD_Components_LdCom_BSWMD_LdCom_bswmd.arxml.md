# LdCom

## 模块描述

The large data communication module (LdCom) is a wrapper module which provides efficient
communication between the PduR and RTE module. It simply forwards all communication APIs between the
RTE and the PduR.
#Communication #RuntimeEnvironment #PduR
#AUTOSAR

## 容器列表

### 1. LdComGeneral

**描述**: Contains the general configuration parameters of the AUTOSAR LdCom module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LdComDevErrorDetect
  长名称: ''
  描述: |
    If 'Development Error Detection' is enabled, all development errors are reported to the
    Development Error Tracer (DET). The errors are described in the technical reference.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: LdComVersionInfoApi
  长名称: ''
  描述: |
    Activate/Deactivate the version information API (LdCom_GetVersionInfo).
    
    Activate/Deactivate the version information API LdCom_GetVersionInfo().
    - True: version information API activated
    - False: version information API deactivated
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: LdComUserConfigFile
  长名称: ''
  描述: |
    Reference to an external user configuration file that will be included during generation.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: LdComSafeBswChecks
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

### 2. LdComGeneration

**描述**: Contains the generation configuration parameters of the module LdCom.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LdComReduceConstantData2Define
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM
    arrays as constant define.
    
    FALSE: ROM arrays are generated as data even if all values are identical.
    TRUE: ROM arrays are generated as constant define if all values are identical.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: LdComReduceBoolDataByNumericalComparisonThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using numerical comparison with other ROM data.
    0: The optimization is not performed.
    >0: This is the threshold to activate the data optimization.
    
    Code: the code size is increased due to the usage of the operation in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the operation in the data access.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: LdComReduceDataByStreaming
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
  序号: 4
  名称: LdComReduceBoolDataByNumericalRelationThreshold
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
  最大值: 255
- 
  序号: 5
  名称: LdComOutOfBoundsReadSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds read problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: LdComShortSymbols
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
  序号: 7
  名称: LdComInterfacesForDeactivatedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate bsw data interfaces for
    deactivated data elements. This is an advantage for the BSW developer to reduce the time to
    market with a development environment using auto completition and to investigate potential
    interfaces.
    
    FALSE: data interfaces are not generated if the data elementis deactivated.
    TRUE: data interfaces are generated as e.g. empty macros.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: LdComReferringKeysInComments
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

### 3. LdComConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR LdCom module.
This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist
once per configuration set.

该容器没有参数。

### 4. LdComIPdu

**描述**: Contains the configuration parameters of the IPdu inside LdCom.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LdComHandleId
  长名称: ''
  描述: The numerical value used as the ID of this I-PDU. This ID is used by Rte to invoke LdCom. A
      corresponding shortName is created, which is used for the invocations of the Rte. The
      same ID is used for invocations by PduR.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: LdComApiType
  长名称: ''
  描述: |
    Indicates the desired API Type of the I-PDU.
    
    LDCOM_IF: indicates that the I-PDU is sent/received via communication interface API.
    LDCOM_TP: indicates that the I-PDU is send/received via transport protocol API.
  默认值: LDCOM_IF
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: LdComIPduDirection
  长名称: ''
  描述: The direction defines if this I-PDU, and therefore the contributing signal, shall be sent or
      received.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: LdComRxIndication
  长名称: ''
  描述: Only on receiver side: Name of Rte_LdComCbkRxIndication callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: LdComRxStartOfReception
  长名称: ''
  描述: Only on receiver side: Name of Rte_LdComCbkStartOfReception callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: LdComRxCopyRxData
  长名称: ''
  描述: Only on receiver side: Name of Rte_LdComCbkCopyRxData callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: LdComTpRxIndication
  长名称: ''
  描述: Only on receiver side: Name of Rte_LdComCbkTpRxIndication callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: LdComTxTriggerTransmit
  长名称: ''
  描述: Only on sender side: Name of Rte_LdComCbkTriggerTransmit callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: LdComTxConfirmation
  长名称: ''
  描述: Only on sender side: Name of Rte_LdComCbkTxConfirmation callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: LdComTxCopyTxData
  长名称: ''
  描述: Only on sender side: Name of Rte_LdComCbkCopyTxData callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: LdComTpTxConfirmation
  长名称: ''
  描述: Only on sender side: Name of Rte_LdComCbkTpTxConfirmation callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
```

