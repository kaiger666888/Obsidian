# Dcm

## 模块描述

Configuration of the Dcm (Diagnostic Communications Manager) module.

## 容器列表

### 1. DcmConfigSet

**描述**: This container contains the configuration parameters and sub containers of the Dcm module supporting
multiple configuration sets.

该容器没有参数。

### 2. DcmDsl

**描述**: These parameters apply to a Diagnostic Session Layer. There may be a parameter set (DSL
Configuration) per protocol.

该容器没有参数。

### 3. DcmDslBuffer

**描述**: This container contains the configuration (parameters) for the diagnostic buffer.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslBufferSize
  长名称: ''
  描述: |
    Specifies the size of a diagnostic buffer (in Bytes).
    
    Effect:
    ------------------------------------
    Determines the longest request and in some cases - response the Dcm will be able to receive,
    resp. transmit.
    
    Constraints:
    ------------------------------------
    It depends on the communication bus system how much buffer shall be reserved. For example on CAN
    a buffer of more than 4095 will not bring any advantage since the CanTp can transfer only up to
    4095 bytes.
    
    Dependencies:
    ------------------------------------
    In case of Paged Buffer usage (refer to DcmPageBufferCfg), the buffer size shall be chosen such
    that at least the longest snapshot record/extended data record of the Dem plus some additional
    bytes (i.e. in case of CAN -> 6 additional bytes) will fit it.
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    The greater the buffer the more RAM will be required.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 50
  最小值: 8
  最大值: 4294967294
```

### 4. DcmDslDiagResp

**描述**: This container contains the configuration (parameters) for the ResponsePending handling

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslDiagRespOnSecondDeclinedRequest
  长名称: ''
  描述: |
    Defines the reaction upon a second request (ClientB) that can not be processed (e.g. due to
    priority assessment).
    
    Effect:
    ------------------------------------
    If enabled, the Dcm will reject any nested diagnostic request by NRC 0x21 (BusyRepeatRequest).
    
    Constraints:
    ------------------------------------
    For optimization reasons not all Dcm managed connection will support this feature by default. It
    is configurable how many parallel (nested) request to be handled at a time to save RAM and run
    time resources.
    
    Dependencies:
    ------------------------------------
    Refer to DcmDslDiagRespMaxNumOfDeclinedRequests.
    
    Runtime effects:
    ------------------------------------
    If enabled the Dcm diagnostic request reception functionality will have slightly increased run
    time usage.
    
    Code ROM usage effects:
    ------------------------------------
    If enabled the Dcm will have slightly increased code ROM usage.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    If enabled the Dcm will have slightly increased RAM usage.
    
    Stack RAM usage effects:
    ------------------------------------
    If enabled the Dcm will have insignificantly increased stack usage within the Rx ISRs.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDslDiagRespMaxNumOfDeclinedRequests
  长名称: ''
  描述: |
    Defines the maximum number of reactions upon a second request (ClientB) that can not be
    processed (e.g. due to priority assessment).
    
    Effect:
    ------------------------------------
    The Dcm will calculate the required amount of resources upon the specified by this option
    resource for parallel client processing.
    
    Constraints:
    ------------------------------------
    If the amount of configured requests exceeds the total number of Dcm connections, during the
    code generation the resource usage optimization will be disabled and only as many as available
    diagnostic connection objects will be allocated. This will also shorten the run time usage (see
    below).
    
    Dependencies:
    ------------------------------------
    Has any effect only if DcmDslDiagRespOnSecondDeclinedRequest is enabled.
    
    Runtime effects:
    ------------------------------------
    The more clients to be handled the longer the run time for looking up for free resources. If the
    number of declined requests matches the total number of Dcm connection, no look up will be
    necessary, and the run time will be minimal.
    
    Code ROM usage effects:
    ------------------------------------
    If the number of declined requests matches the total number of Dcm connection, no look up will
    be necessary, and the code ROM will be minimal.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    The more clients to be handled the more RAM will be required for handling them.
    
    Stack RAM usage effects:
    ------------------------------------
    If the number of declined requests matches the total number of Dcm connection, no look up will
    be necessary, and the stack usage will be minimal.
    
  默认值: 3
  最小值: 1
  最大值: 255
```

### 5. DcmDslProtocol

**描述**: This container contains the configuration (parameters) for the protocol configuration (for each
protocol) The following parameters needs to be configured per protocol.

该容器没有参数。

### 6. DcmDslProtocolRow

**描述**: Definition of a single Row of configuration for the protocol configuration (for each protocol)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslProtocolID
  长名称: ''
  描述: |
    Specifies the diagnostic protocol type the Dcm shall manage.
    
    Effect:
    ------------------------------------
    On a multi protocol configuration Dcm will be able to distinguish among different protocols and
    notify the application for activation/deactivation of a concrete protocol, specified by this
    parameter.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has any effect only if multi protocol configuration is used.
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: DCM_UDS_ON_CAN
  最小值: ''
  最大值: ''
```

### 7. DcmDslMainConnection

**描述**: This container contains configuration for Diagnostic Main Connection

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslProtocolRxTesterSourceAddr
  长名称: ''
  描述: |
    Specifies a unique identifier of a diagnostic client connection.
    
    Effect:
    ------------------------------------
    The Dcm is able to identify different clients or the same client on multiple channels using this
    identifier.
    
    Constraints:
    ------------------------------------
    For each DcmDslConnection there shall be a unique value assigned to this parameter.
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DcmDslPayloadLimit
  长名称: ''
  描述: ''
  默认值: 4095
  最小值: 0
  最大值: 4294967295
```

### 8. DcmDslProtocolRx

**描述**: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslProtocolRxAddrType
  长名称: ''
  描述: |
    Specifies the request addressing type on a concrete receive Dcm PduId.
    
    Effect:
    ------------------------------------
    Depending on the request type specified here, the Dcm will be able to react correctly according
    to the ISO14229-1.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDslProtocolRxPduId
  长名称: ''
  描述: |
    Specifies the logical handle value of a concrete Dcm receive PDU.
    NOTE: This value is generated automatically by the Configurator 5 tool.
    
    Effect:
    ------------------------------------
    Using this value Dcm is able to distinguish the different transport layer connections.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 9. DcmDslProtocolTx

**描述**: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the
associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslTxConfirmationPduId
  长名称: ''
  描述: |
    Specifies the logical handle value of a concrete Dcm transmit PDU.
    NOTE: This value is generated automatically by the Configurator 5 tool.
    
    Effect:
    ------------------------------------
    Using this value Dcm is able to distinguish the different transport layer connections at
    response confirmation time.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 10. DcmDslConnectionGroup

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslConnectionGroupId
  长名称: ''
  描述: Specifies the logical handle value of a concrete DcmDslConnectionGroup.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 11. DcmDslBroadcastGroup

**描述**: Aggregate DcmDslMainConnections to a group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslBroadcastGroupId
  长名称: ''
  描述: Specifies the logical handle value of a concrete DcmDslConnectionGroup.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 12. DcmDsp

**描述**: These parameters apply to Diagnostic Service Processing. There will always be one set of these
parameters per DCM.

该容器没有参数。

### 13. DcmDspSession

**描述**: This container includes all diagnostic sessions the Dcm shall support.

Effect:
------------------------------------
For each diagnostic session to be supported by Dcm a DcmDspSessionRow sub-container shall be
defined.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to
"Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration data ROM usage scales straight proportionally to the number of sessions
defined.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

该容器没有参数。

### 14. DcmDspSessionRow

**描述**: Definition of a single Row of session control configuration (per session control)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspSessionLevel
  长名称: ''
  描述: |
    Specifies the value of the corresponding diagnostic session.
    
    Effect:
    ------------------------------------
    This value will be used when the Dcm_GetSesCtrlType API is called from the application to report
    the currently active session.
    
    Constraints:
    ------------------------------------
    For each session level, there shall always be a corresponding sub-services for service 0x10.
    
    Dependencies:
    ------------------------------------
    Refer to
    "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DcmDspSessionP2ServerMax
  长名称: Dsp Session P2ServerMax
  描述: |
    Determines the diagnostic session specific P2 time in seconds.
    
    Effect:
    ------------------------------------
    This parameter will be reported by Dcm within the positive response to the corresponding session
    activation request. The really monitored time by Dcm is specified from the currently active
    protocol.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    For the real monitored time adjustment refer to
    "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2ServerAdjust".
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0.05
  最小值: 0
  最大值: 1000
- 
  序号: 3
  名称: DcmDspSessionP2StarServerMax
  长名称: Dsp Session P2StarServerMax
  描述: |
    Determines the diagnostic session specific P2* time in seconds.
    
    Effect:
    ------------------------------------
    This parameter will be reported by Dcm within the positive response to the corresponding session
    activation request. The really monitored time by Dcm is specified from the currently active
    protocol.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    For the real monitored time adjustment refer to
    "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2StarServerAdjust".
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 5
  最小值: 0
  最大值: 100000
```

### 15. DcmGeneral

**描述**: This container contains the configuration (parameters) for Component wide parameters

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmTaskTime
  长名称: ''
  描述: |
    Allow to configure the time for the periodic cyclic task in seconds.
    
    Effect:
    -----------------------------------------
    This value is used to set up the Dcm Service-Description and BSW scheduler. All diagnostic
    timers managed by Dcm use this setting as a base time for the internal time constants'
    calculation.
    
    Constraints:
    -----------------------------------------
    The specified time shall be a multiple of the time values defined in all diagnostic timing
    settings in the Dcm configuration.
    
    Dependencies:
    -----------------------------------------
    All diagnostic timing parameters.
    
    Runtime effects:
    -----------------------------------------
    Too low values will increase the Dcm responsiveness, but will increase the CPU load. Too high
    values of this parameter will lead to rear Dcm task activation (lower CPU load), but the Dcm
    internal timers' accuracy will not be optimal.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    none
    
  默认值: 0.01
  最小值: 0
  最大值: 100
- 
  序号: 2
  名称: DcmUserConfigFile
  长名称: ''
  描述: |
    Path to an external user configuration file used by the Configurator 5 generation tool.
    
    Effect:
    -----------------------------------------
    If you want to overwrite some of the settings in the generated configuration file (Dcm_Cfg.h),
    you can specify a path to a user defined configuration file. The user defined configuration file
    will be included at the end of the generated preprocessor switches. Definitions in the user
    defined configuration file can overwrite definitions in the generated configuration file.
    
    The path shall be a valid path to the user configuration file. For simplified and project
    specific user configuration files references, the following Configurator 5 environment variables
    can be used:
    
    $(DpaProjectFolder) Absolute directory of the loaded *.dpa file.
    $(EcuProjectName) Name of the project defined in the loaded *.dpa file.
    $(EcucFile) Absolute directory "ECUC", defined by the loaded *.dpa file, containing files
    $(EcuProjectName).ecuc.arxml and $(EcuProjectName).ecuc.Initial.arxml .
    $(EcucFolder) Parent directory of $(EcucFile).
    $(SipRootPath) Absolute directory "SIP", defined by the loaded *.dpa file.
    $(OutputFolder) (Relative) directory "GenData", defined by the loaded *.dpa file. See setting
    "Root Target Folder" of Configurator 5.
    $(ServiceSwcFolder) Absolute directory "ServiceComponents", defined by the loaded *.dpa file.
    
    
    Constraints:
    -----------------------------------------
    Not all of the settings can be overwritten simply by triggering the preprocessor switch. Some of
    the options are complex and the code generator generates less or more code depending on the
    setting.
    
    USE SUCH A FILE ONLY AFTER DISCUSSION WITH VECTOR.
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    none
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmQueuedRequest
  长名称: ''
  描述: ''
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmKeySlotMode
  长名称: ''
  描述: Enable switching from key slot to all slot mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DcmBaudrateSwitch
  长名称: ''
  描述: |
    This parameter switches the APIs FblCwCheckBaudrate and FblCwSwitchBaudrate ON or OFF.
    true: APIs are enabled.
    false: APIs are disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DcmNwStatusRxBufferSize
  长名称: ''
  描述: Buffer size for the network status reception buffer.
  默认值: 32
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DcmCanHardwareLoopTimeout
  长名称: ''
  描述: Timeout value for CAN hardware loops (in cycles, typically 1 ms)
  默认值: 100
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DcmTaskCycle
  长名称: ''
  描述: Cycle count of CanTp, FrSM, EthSM and ComM tasks. Other tasks are either called every timer
      cycle (Ethernet) or polled (CAN)
  默认值: 5
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DcmVersionInfoApi
  长名称: ''
  描述: Preprocessor switch to enable or disable the output Version info of the functionality.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DcmDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DcmRespondAllRequest
  长名称: ''
  描述: If set to FALSE the Dcm will not respond to diagnostic request  that contains a service ID
      which is in the range from 0x40 to 0x7F or in the  range from 0xC0 to 0xFF (Response
      IDs).
  默认值: true
  最小值: ''
  最大值: ''
```

### 16. DcmGeneration

**描述**: Contains the generation configuration parameters of the module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmReduceConstantData2Define
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
  序号: 2
  名称: DcmReduceNumericalDataByOffsetThreshold
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
  序号: 3
  名称: DcmShortSymbols
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
  序号: 4
  名称: DcmInterfacesForDeactivatedData
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
  序号: 5
  名称: DcmReferringKeysInComments
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

