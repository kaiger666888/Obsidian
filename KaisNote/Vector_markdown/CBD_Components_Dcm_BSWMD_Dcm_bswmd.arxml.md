# Dcm

## 模块描述

Diagnostic Communication Manager. Handles the diagnostic communication between the tester and the
application of the ECU. Implements UDS and (WWH-)OBD services providing abstract interfaces to the
application.
#Diag #UDS #OBD #WWHOBD
#AUTOSAR #ServiceComponent

## 容器列表

### 1. DcmConfigSet

**描述**: This container contains the configuration parameters and sub containers of the Dcm module supporting
multiple configuration sets.

该容器没有参数。

### 2. DcmDsd

**描述**: These parameters apply to Diagnostic Service Dispatcher. All parameters for all service dispatchers
are included in this one configuration container.

该容器没有参数。

### 3. DcmDsdServiceTable

**描述**: This container contains the configuration (DSD parameters) for Service Identifier Table.

Effect:
------------------------------------
If a certain diagnostic services shall be supported, it has to be declared within this container
with all of its properties. Any received diagnostic request with a service ID not declared here,
will be rejected by Dcm.

Constraints:
------------------------------------
Some services are required and must exist, other are optional or no allowed at all. During the
configuration the Configurator 5 validators will notify you about wrongly configured or missing
service declaration.

Dependencies:
------------------------------------
Depending on the service identifier, some "/Dcm/DcmConfigSet/DcmDsp" sub-containers/parameters will
be required additionally. Refer to any "/Dcm/DcmConfigSet/DcmDsp" sub-container/parameter for
dependencies to this container type.

Runtime effects:
------------------------------------
The Dcm service identification runtime will scale linearly with the amount of services specified
here.

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The ROM usage of the configuration part of Dcm will scale linearly with the amount of services
specified here.

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
  名称: DcmDsdSidTabId
  长名称: ''
  描述: NOT USED
  默认值: 0
  最小值: 0
  最大值: 255
```

### 4. DcmDsdService

**描述**: This container defines a single diagnostic service.

Effect:
------------------------------------
If a certain diagnostic services shall be supported, it has to be declared within this container
with all of its properties. Any received diagnostic request with a service ID not declared here,
will be rejected by Dcm.

Constraints:
------------------------------------
Some services are required and must exist, other are optional or no allowed at all. During the
configuration the Configurator 5 validators will notify you about wrongly configured or missing
service declaration.

Dependencies:
------------------------------------
Depending on the service identifier, some "/Dcm/DcmConfigSet/DcmDsp" sub-containers/parameters will
be required additionally. Refer to any "/Dcm/DcmConfigSet/DcmDsp" sub-container/parameter for
dependencies to this container type.

Runtime effects:
------------------------------------
The Dcm service identification runtime will scale linearly with the amount of services specified
here.

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The ROM usage of the configuration part of Dcm will scale linearly with the amount of services
specified here.

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
  名称: DcmDsdSidTabFnc
  长名称: ''
  描述: |
    Optional callback function of the ECU supplier specific component for the particular
    DcmDsdSidTabServiceId.
    
    Effect:
    ------------------------------------
    Dcm implements internally only some specific diagnostic services. For all other valid services
    an application function name shall be entered here that will be called by Dcm to handle the
    concrete diagnostic service.
    
    Constraints:
    ------------------------------------
    The Configurator 5 validators will notify you for any invalid setting on this parameter.
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    Only application code will be affected.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    The required stack size by the Dcm task may increase depending on the implementation of the
    specified application function.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDsdSidTabServiceId
  长名称: ''
  描述: |
    Specifies the value of the diagnostic service identifier. The possible parameter values are
    predefined in the ISO 14229-1, ISO 15031-5 and can be restricted by the OEM.
    
    Effect:
    ------------------------------------
    Dcm will identify only those sub-services of the corresponding diagnostic service that are
    defined here.
    
    Constraints:
    ------------------------------------
    All allowed and supported service identifiers are validated during the configuration time. The
    valid values are diagnostic protocol, diagnostic service and OEM specific.
    
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
  最大值: 255
- 
  序号: 3
  名称: DcmDsdSidTabSubfuncAvail
  长名称: ''
  描述: |
    Information whether the DcmDsdSidTabServiceId includes Sub functions or not. Used for the
    Handling of "suppressPosRspMsgIndicationBit" ISO14229-1 can be referenced here, as this
    specification gives fix definition, if an SID includes sub-function or not.
    
    Effect:
    ------------------------------------
    If this option is set to TRUE, any received sub-function byte of the diagnostic service will be
    evaluated for the SPRMIB (bit 7). This bit will be masked out, so the later service and
    sub-service processors will not need to consider it any more. If the SPRMIB information is still
    needed, it will be accessible through the Dcm_MessageContextType.
    
    Constraints:
    ------------------------------------
    Only services with a sub-function shall set this option to TRUE. The Configurator 5 will
    validate for inappropriate setting of this option, depending on its SID.
    
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
  序号: 4
  名称: DcmDsdSidTabServiceDispatcher
  长名称: ''
  描述: |
    Specifies whether the Dcm shall dispatch between internal and external service handler.
    
    Effect:
    ------------------------------------
    If this option is set to TRUE, any received request of the diagnostic service will be dispatched
    via a call-out. The service processing will then be handled either internally or externally.
    
    Constraints:
    ------------------------------------
    Only services that can be externally defined and have an internal service processor shall set
    this option to TRUE.
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    The Dcm task will have a slightly longer run time at reception of a request, since application
    call-out is done. This time depends on the complexity of the modeled application service
    dispatching.
    
    Code ROM usage effects:
    ------------------------------------
    The code usage will increase slightly.
    
    Const data ROM usage effects:
    ------------------------------------
    The code usage will increase slightly.
    
    Global RAM usage effects:
    ------------------------------------
    The RAM usage will increase slightly.
    
    Stack RAM usage effects:
    ------------------------------------
    During the service dispatching the stack usage will slightly increase. It will depend on the
    implementation of the application callback.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DcmDsdSidTabUsed
  长名称: ''
  描述: |
    The parameter can be used to temporarily disable a complete Service in the Dcm configuration
    without the need to delete all its configuration parameters.
    
    Effect:
    ------------------------------------
    If set to FALSE, the Service and all its dependent objects will not be used in the Dcm generated
    code.
    
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
    If set to FALSE, no data ROM for this Service will be used.
    
    Const data ROM usage effects:
    ------------------------------------
    If set to FALSE, no data ROM for this Service will be used in the Dcm configuration sources.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DcmDsdSidTabPreHandler
  长名称: ''
  描述: |
    Specifies the call out function name for service pre-processing.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function before processing the
    service.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    The Dcm task will have a slightly longer run time during the processing of a service, since an
    application call-out is done. This time depends on the complexity of the modelled application
    call-out.
    
    Code ROM usage effects:
    ------------------------------------
    The code usage will increase slightly.
    
    Const data ROM usage effects:
    ------------------------------------
    The code usage will increase slightly.
    
    Global RAM usage effects:
    ------------------------------------
    The RAM usage will increase slightly.
    
    Stack RAM usage effects:
    ------------------------------------
    During the service processing the stack usage will slightly increase. It will depend on the
    implementation of the application callback.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DcmDsdSidTabPostHandler
  长名称: ''
  描述: |
    Specifies the call out function name for service post-processing.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function after processing the
    service.
    
    Constraints:
    ------------------------------------
    This feature is not allowed for services 0x19 (ReadDTCInformation) and 0x22
    (ReadDataByIdentifier) with enabled paged buffer.
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    The Dcm task will have a slightly longer run time during the processing of a service, since an
    application call-out is done. This time depends on the complexity of the modelled application
    call-out.
    
    Code ROM usage effects:
    ------------------------------------
    The code usage will increase slightly.
    
    Const data ROM usage effects:
    ------------------------------------
    The code usage will increase slightly.
    
    Global RAM usage effects:
    ------------------------------------
    The RAM usage will increase slightly.
    
    Stack RAM usage effects:
    ------------------------------------
    During the service processing the stack usage will slightly increase. It will depend on the
    implementation of the application callback.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. DcmDsdSubService

**描述**: This container contains the configuration (DSD parameters) for sub-services of a diagnostic service.

Effect:
------------------------------------
If a certain diagnostic sub-services of a service shall be supported, it has to be declared within
this container with all of its properties. Any received diagnostic request with a sub-service ID not
declared here, will be rejected by Dcm.

Constraints:
------------------------------------
This container exists only if parameter DcmDsdSidTabSubfuncAvail, of this service, is set to TRUE
and the parameter DcmDsdSidTabFnc is not existing.

Some services are required and must exist, other are optional or no allowed at all. During the
configuration the Configurator 5 validators will notify you about wrongly configured or missing
service declaration.

Dependencies:
------------------------------------
Depending on the service identifier, some "/Dcm/DcmConfigSet/DcmDsp" sub-containers/parameters will
be required additionally. Refer to any "/Dcm/DcmConfigSet/DcmDsp" sub-container/parameter for
dependencies to this container type.

Runtime effects:
------------------------------------
The Dcm sub-service identification runtime will scale linearly with the amount of services specified
here.

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The ROM usage of the configuration part of Dcm will scale linearly with the amount of sub-services
specified here.

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
  名称: DcmDsdSubServiceFnc
  长名称: ''
  描述: |
    Optional callback function of the ECU Supplier specific component. This parameter is related to
    the interface <Module>_<DiagnosticService>_<SubService>.
    
    Effect:
    ------------------------------------
    Dcm implements internally for specific diagnostic services, some specific sub-services. For all
    other valid sub-services an application function name shall be entered here that will be called
    by Dcm to handle the concrete sub-service.
    
    Constraints:
    ------------------------------------
    The Configurator 5 validators will notify you for any invalid setting on this parameter.
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    Only application code will be affected.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    The required stack size by the Dcm task may increase depending on the implementation of the
    specified application function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDsdSubServiceId
  长名称: ''
  描述: |
    Specifies the value of the sub-service identifier. The possible sub-function parameter value are
    predefined in the ISO 14229-1, ISO 15031-5 and can be restricted OEM.
    
    Effect:
    ------------------------------------
    Dcm will identify only those sub-services of the corresponding diagnostic service that are
    defined here.
    
    Constraints:
    ------------------------------------
    All allowed and supported sub-function identifiers are validated during the configuration time.
    The valid values are diagnostic protocol, diagnostic service and OEM specific.
    
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
  最大值: 255
```

### 6. DcmDsl

**描述**: These parameters apply to a Diagnostic Session Layer. There may be a parameter set (DSL
Configuration) per protocol.

该容器没有参数。

### 7. DcmDslBuffer

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
    It depends on the communication bus system how much buffer shall be reserved.
    
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

### 8. DcmDslCallbackDCMRequestService

**描述**: The name of the container will specify the SWC name of the "StartProtocol" notification function.

Effect:
-----------------------------------------
For each available container of this type, there will be a notification call into the corresponding
SWC for getting permission of received protocol start/switch.

Constraints:
-----------------------------------------
Has effect only if there are more than one protocols configured in DCM.

Dependencies:
-----------------------------------------
Configuration parameters: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow"

Runtime effects:
-----------------------------------------
Enabling this feature will increase the Dcm task time at any protocol switch (e.g. no protocol-> UDS
-> OBD, etc.).

Code ROM usage effects:
------------------------------------
Enabling this feature leads to a minor increase of the Dcm static code ROM usage.

Const data ROM usage effects:
-----------------------------------------
Enabling this feature increases the Dcm configuration ROM usage. The usage scales linearly with the
amount of SWCs to be notified.

Global RAM usage effects:
-----------------------------------------
none

Stack RAM usage effects:
-----------------------------------------
Enabling this feature can lead to a insignificant increased stack size required by the
Dcm_MainFunction.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslCallbackDCMRequestServiceUsePort
  长名称: ''
  描述: |
    Defines which kind of interface shall be used to access the application.
    
    Effect:
    ------------------------------------
    Depending on the selected type, either a RTE call or a call out will be required to be
    implemented in the Dcm application.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    The function names generated in case of FALSE will depend on the function name parameter.
    
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
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDslCallbackDCMRequestServiceStartFnc
  长名称: ''
  描述: |
    Specifies the call out function name for notification call.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on each received
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the DcmDslCallbackDCMRequestServiceUsePort is set to FALSE.
    
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
```

### 9. DcmDslDiagResp

**描述**: This container contains the configuration (parameters) for the ResponsePending handling

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslDiagRespMaxNumRespPend
  长名称: ''
  描述: |
    Specifies the maximum number of negative responses with response code 0x78
    (requestCorrectlyReceived-ResponsePending) allowed per request.
    
    Effect:
    ------------------------------------
    If set to a value > 0:
    Dcm will cancel any ongoing diagnostic service processing and send a negative response with
    response code 0x10 (generalReject), in case the limit value gets reached.
    If set to 0: no limitation will apply. The DCM will wait endlessly for the application to finish
    its job.
    
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
    If the limitation is enabled (value > 0), the Dcm code usage will slightly increase due to the
    additional functionality.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    If the limitation is enabled (value > 0), the Dcm RAM usage will insignificantly increase due to
    the additional functionality.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
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
  序号: 3
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
- 
  序号: 4
  名称: DcmDslDiagRespPeriodicMsgPaddingPattern
  长名称: ''
  描述: |
    Determines the padding byte value for the unused data bytes in the periodic message
    
    Effect:
    ------------------------------------
    If this parameter does not exist, no padding will apply, and the periodic message will have the
    length of the data to be sent.
    If this parameter exists, the periodic message will always have the maximum length of the UUDT
    CAN frame (8 bytes). All unused data will be filled with the pattern specified by this parameter
    value.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x2A.
    
    Runtime effects:
    ------------------------------------
    If padding is to be supported the periodic message transmission will always take constant run
    time for copying the data. Due to the additional loop needed for filling up the data, the run
    time usage will be increased insignificantly.
    
    Code ROM usage effects:
    ------------------------------------
    If padding is to be supported additional loop will be executed to fill up the unused data bytes
    with the pattern value. This increases insignificantly the code ROM usage.
    
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
```

### 10. DcmDslProtocol

**描述**: This container contains the configuration (parameters) for the protocol configuration (for each
protocol) The following parameters needs to be configured per protocol.

该容器没有参数。

### 11. DcmDslProtocolRow

**描述**: Definition of a single Row of configuration for the protocol configuration (for each protocol)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslProtocolEndiannessConvEnabled
  长名称: ''
  描述: NOT USED
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
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
- 
  序号: 3
  名称: DcmDslProtocolMaximumResponseSize
  长名称: ''
  描述: |
    This parameter is mandatory and defines the maximum length of the response message if a
    PagedBuffer (/MICROSAR/Dcm/DcmConfigSet/DcmDsp/DcmDspReadPagedDataPageSize) is configured.
    Note: The maximum length of the response is not checked in case of a ReadDTCInformation request
  默认值: 4095
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: DcmDslProtocolPreemptTimeout
  长名称: ''
  描述: NOT USED
  默认值: 0
  最小值: 0
  最大值: 1000
- 
  序号: 5
  名称: DcmDslProtocolPriority
  长名称: ''
  描述: |
    Specifies the diagnostic protocol priority the Dcm shall manage.
    
    Effect:
    ------------------------------------
    On a multi protocol configuration Dcm will be able to distinguish among different protocols and
    preempt lower priority protocols by higher priority ones (e.g. interrupt UDS protocol by an OBD
    request).
    Values:
    0             - highest priority protocol
    1..Max-1 - lower priority protocol
    Max        - lowest priority protocol
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has any effect only if multi protocol configuration is used.
    
    Runtime effects:
    ------------------------------------
    On multi protocol configurations additional code for the protocol arbitration will be enabled in
    DCM. This will slightly increase the run time of the first Dcm_MainFunction call each time a new
    request is received,
    
    Code ROM usage effects:
    ------------------------------------
    On multi protocol configurations additional code for the protocol arbitration will be enabled in
    DCM. This will increase the code ROM usage,
    
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    On multi protocol configurations usually there are multiple buffers configured and assigned to
    each protocol. This increases the global RAM usage,
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: DcmDslProtocolTransType
  长名称: ''
  描述: NOT USED
  默认值: TYPE1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DcmSendRespPendOnTransToBoot
  长名称: ''
  描述: |
    NOT USED
    Replaced by parameter DcmSendRespPendOnRestart.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DcmTimStrP2ServerAdjust
  长名称: ''
  描述: |
    This parameter is used to guarantee that the DCM response is available on the bus before
    reaching P2.This parameter value in seconds has to be configured as a multiple of DcmTaskTime.
    
    Effect:
    ------------------------------------
    The time specified here will be subtracted from the P2server time of the currently active
    session. The result will be used by Dcm for triggering the first RCR-RP response after a
    successful diagnostic request reception.
    
    Constraints:
    ------------------------------------
    This time shall not be greater than the minimum P2server time of any diagnostic session.
    
    Dependencies:
    ------------------------------------
    - refer to the:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspSession/DcmDspSessionRow/DcmDspSessionP2ServerMax"
    
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
  最大值: 1000
- 
  序号: 9
  名称: DcmTimStrP2StarServerAdjust
  长名称: ''
  描述: |
    This parameter is used to guarantee that the DCM response is available on the bus before
    reaching P2*.This parameter value in seconds has to be configured as multiple of DcmTaskTime and
    is minimum in the timing handling of P2*.
    
    Effect:
    ------------------------------------
    The time specified here will be subtracted from the P2StarServer time of the currently active
    session. The result will be used by Dcm for triggering the second and further RCR-RP responses.
    
    Constraints:
    ------------------------------------
    This time shall not be greater than the minimum P2StarServer time of any diagnostic session.
    
    Dependencies:
    ------------------------------------
    - refer to the:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspSession/DcmDspSessionRow/DcmDspSessionP2StarServerMax"
    
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
  最大值: 5000
- 
  序号: 10
  名称: DcmSendRespPendOnRestart
  长名称: ''
  描述: |
    Specifies whether the Dcm shall send a RCR-RP response prior jumping to the boot
    loader/restarting the Ecu or not.
    
    Effect:
    ------------------------------------
    If set to TRUE, the Dcm will send a RCR-RP response prior jumping to the boot loader on
    diagnostic service 0x10 0x02 (enter programming session) or prior to an Ecu reset on diagnostic
    service 0x11 (0x01 - 0x03).
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Service 0x10:
    This parameter has no effect if none of the diagnostic session specified in DcmDspSessionRow has
    any boot type other than NO_BOOT.
    Refer to /Dcm/DcmConfigSet/DcmDsp/DcmDspSession/DcmDspSessionRow/DcmDspSessionForBoot.
    
    Service 0x11:
    This parameter has no effect if none of the sub-services 0x01 - 0x03 of diagnostic service 0x11
    (EcuReset) are configured.
    
    
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
  默认值: true
  最小值: ''
  最大值: ''
```

### 12. DcmDslMainConnection

**描述**: This container contains configuration for Diagnostic Main Connection

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslProtocolRxTesterSourceAddr
  长名称: ''
  描述: |
    Specifies a unique identifier of a diagnostic client connection. This value is an abstract
    identifier and does not need to be a real source address.
    
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
  名称: DcmDslPhysicalEcuAddress
  长名称: ''
  描述: |
    Specifies the ECU address from the concrete client connection.
    
    Effect:
    ------------------------------------
    The Dcm is able to identify different multiple ECUs addressed from a diagnostic client.
    
    Constraints:
    ------------------------------------
    For single ECU use case:
    For each DcmDslConnection there shall be the same value assigned to this parameter.
    For virtual ECU use case:
    For each DcmDslConnection there shall be set the appropriate value of the concrete virtual ECU.
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    For virtual ECU use case the number of supported ECUs will determine the run time during
    diagnostic client request reception.
    
    Code ROM usage effects:
    ------------------------------------
    For virtual ECU use case the code ROM usage is slightly increased.
    
    Const data ROM usage effects:
    ------------------------------------
    For virtual ECU use case the data ROM usage is slightly increased.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: DcmDslAddressingType
  长名称: ''
  描述: |
    Specifies the address type for a concrete diagnostic client connection.
    
    Effect:
    ------------------------------------
    The Dcm is able to identify the addressing type of a certain diagnostic connection.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    It depends on the addressing type and the concrete implementation in DCM.
    
    Code ROM usage effects:
    ------------------------------------
    It depends on the addressing type and the concrete implementation in DCM.
    
    Const data ROM usage effects:
    ------------------------------------
    It depends on the addressing type and the concrete implementation in DCM.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: DCM_NET_ADDR_NORMAL
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDslProtocolRxConnectionId
  长名称: ''
  描述: |
    Unique identifier of the tester which uses this connection for diagnostic communication.
    
    Effect:
    ------------------------------------
    Using this value Dcm is able to distinguish the different main connections.
    
    Constraints:
    ------------------------------------
    The connection Id value must be unique within a DcmConfigset.
    
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
  序号: 5
  名称: DcmDslChannelReadyIndicationEnabled
  长名称: ''
  描述: |
    Choose whether Dcm shall use a callout to determine the readiness of the current connection for
    message transmission or not.
    
    Effect:
    ------------------------------------
    By using this value, Dcm will wait for DoIP until notified about an established connection
    before sending a final response after reset.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    The Dcm task will have a slightly longer run time at transmission of a response, since call-out
    is done.
    
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
  默认值: false
  最小值: ''
  最大值: ''
```

### 13. DcmDslProtocolRx

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
  名称: DcmDslProtocolRxChannelId
  长名称: ''
  描述: NOT USED
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
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
- 
  序号: 4
  名称: DcmDslProtocolRxTpRxPduId
  长名称: ''
  描述: |
    Specifies the corresponding TP RxPduId for a concrete client connection request message.
    
    Effect:
    ------------------------------------
    In some situations DCM shall be able to convert TpRxPduIds to DcmRxPduIds.
    
    Constraints:
    ------------------------------------
    Use case driven parameter usage. See technical reference if or when this parameter is required
    in your project.
    
    Dependencies:
    ------------------------------------
    Project specific.
    
    Runtime effects:
    ------------------------------------
    Project specific.
    
    Code ROM usage effects:
    ------------------------------------
    If this parameter values are used, the code ROM usage will slightly increase.
    
    Const data ROM usage effects:
    ------------------------------------
    If this parameter values are used, the data ROM usage will slightly increase.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: DcmDslProtocolRxGlobalEcuAddress
  长名称: ''
  描述: NOT USED
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 14. DcmDslProtocolTx

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

### 15. DcmDslPeriodicTransmission

**描述**: Defines periodic messages for the corresponding client main connection.

Effect:
------------------------------------
If this parameter exists, the DCM will be able to send periodic responses to the client identified
by the main connection that refers to this container.

Constraints:
------------------------------------
This parameter shall be used only if service 0x2A (ReadDataByPeriodicIdentifier) is to be supported.

Dependencies:
------------------------------------
- The diagnostic service 0x2A (ReadDataByPeriodicIdentifier) must be supported by Dcm (refer to
/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
- The main connection for the given client shall refer to this container  (see
/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslPeriodicTranmissionConRef).

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
Due to the additional information to be stored the Dcm configuration ROM usage will increase.

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
  名称: DcmDslPeriodicTxConfirmationTimeout
  长名称: ''
  描述: |
    This parameter is used to specify the Dcm periodic response message TTL (time to live). This is
    required in case the network layer interface does not support own message TTL monitoring (e.g.
    on CAN).
    
    Effect:
    ------------------------------------
    The time specified here will be used by Dcm for canceling an ongoing periodic message
    transmission that take too long. In that way deadlocks in Dcm will be avoided when the network
    interface never calls the Dcm_TxConfirmation function (e.g. in case of communication bus
    errors).
    
    Constraints:
    ------------------------------------
    This parameter shall never be zero.
    
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
  默认值: 0.1
  最小值: 0
  最大值: 1000
```

### 16. DcmDslPeriodicConnection

**描述**: Holding the TxPduId configuration for PeriodicTransmission.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslPeriodicTxConfirmationPduId
  长名称: ''
  描述: |
    Specifies the logical handle value of a concrete Dcm periodic transmit PDU.
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

### 17. DcmDslResponseOnEvent

**描述**: NOT USED

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslRoeTxConfirmationPduId
  长名称: ''
  描述: Handle Id to be used by the Lower Layer to confirm the transmission of the DcmDslRoeTxPdu to
      the LowerLayer.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 18. DcmDslServiceRequestManufacturerNotification

**描述**: The name of this container is used to define the name of the R-Port through which the DCM accesses
the interface ServiceRequestNotification.

Effect:
------------------------------------
If used, the Dcm will ask the application for permission to start the diagnostic service evaluation.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
The more notifications configured, the more run time will be needed to process them. Also the run
time usage of each notification call affects the Dcm task run time.

Code ROM usage effects:
------------------------------------
If used, the Dcm will have slightly increased code ROM usage.

Const data ROM usage effects:
------------------------------------
If used, the Dcm will have slightly increased constant data ROM usage. The usage linearly scales
with the amount of notification.


Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
If used, the Dcm will have slightly increased stack usage, executing all of the notification calls.
The callee's stack usage directly affects the Dcm task stack usage.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslServiceRequestManufacturerNotificationUsePort
  长名称: ''
  描述: |
    Defines which kind of interface shall be used to access the application.
    
    Effect:
    ------------------------------------
    Depending on the selected type, either a RTE call or a call out will be required to be
    implemented in the Dcm application.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    The function names generated in case of FALSE will depend on the function name parameter.
    
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
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDslServiceRequestManufacturerNotificationIndicationFnc
  长名称: ''
  描述: |
    Specifies the call out function name for notification call.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on each received
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the DcmDslServiceRequestManufacturerNotificationUsePort is set to FALSE.
    
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
  序号: 3
  名称: DcmDslServiceRequestManufacturerNotificationConfirmationFnc
  长名称: ''
  描述: |
    Specifies the call out function name for notification call.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on each received
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the DcmDslServiceRequestManufacturerNotificationUsePort is set to FALSE.
    
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
```

### 19. DcmDslServiceRequestSupplierNotification

**描述**: The name of this container is used to define the name of the R-Port through which the DCM accesses
the interface ServiceRequestNotification.

Effect:
------------------------------------
If used, the Dcm will ask the application for permission to start the diagnostic service evaluation.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
The more notifications configured, the more run time will be needed to process them. Also the run
time usage of each notification call affects the Dcm task run time.

Code ROM usage effects:
------------------------------------
If used, the Dcm will have slightly increased code ROM usage.

Const data ROM usage effects:
------------------------------------
If used, the Dcm will have slightly increased constant data ROM usage. The usage linearly scales
with the amount of notification.


Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
If used, the Dcm will have slightly increased stack usage, executing all of the notification calls.
The callee's stack usage directly affects the Dcm task stack usage.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslServiceRequestSupplierNotificationUsePort
  长名称: ''
  描述: |
    Defines which kind of interface shall be used to access the application.
    
    Effect:
    ------------------------------------
    Depending on the selected type, either a RTE call or a call out will be required to be
    implemented in the Dcm application.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    The function names generated in case of FALSE will depend on the function name parameter.
    
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
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDslServiceRequestSupplierNotificationIndicationFnc
  长名称: ''
  描述: |
    Specifies the call out function name for notification call.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on each received
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the DcmDslServiceRequestSupplierNotificationUsePort is set to FALSE.
    
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
  序号: 3
  名称: DcmDslServiceRequestSupplierNotificationConfirmationFnc
  长名称: ''
  描述: |
    Specifies the call out function name for notification call.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on each received
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the DcmDslServiceRequestSupplierNotificationUsePort is set to FALSE.
    
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
```

### 20. DcmDsp

**描述**: These parameters apply to Diagnostic Service Processing. There will always be one set of these
parameters per DCM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspMaxDidToRead
  长名称: ''
  描述: |
    Indicates the maximum allowed DIDs in a single "ReadDataByIdentifier" request.
    
    Effect:
    ------------------------------------
    Any diagnostic request for service 0x22 with more DIDs as specified by this parameter will be
    rejected by a negative response.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x22.
    
    Runtime effects:
    ------------------------------------
    The larger number of DIDs per request, the longer the Dcm task execution time, since in the
    worst case (all DIDs are synchronous) all requested DIDs will be processed within the same Dcm
    task activation.
    
    Code ROM usage effects:
    ------------------------------------
    If more than one DID is specified to be allowed, the Dcm code usage may slightly increase due to
    the iteration loops.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    The RAM usage can increase with increasing the value of this parameter.
    
    Stack RAM usage effects:
    ------------------------------------
    none
    
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: DcmDspPowerDownTime
  长名称: ''
  描述: |
    This parameter indicates to the client the minimum time of the stand-by sequence the server will
    remain in the power-down sequence.
    
    Effect:
    ------------------------------------
    The value specified in this parameter will be returned by Dcm on the positive response of
    diagnostic service 0x11 0x04.
    Note: If this parameter is missing, but service 0x11 0x04 is supported, the value used by Dcm
    will be 0xFF.
    
    Constraints:
    ------------------------------------
    Makes sense to be specified only if diagnostic service 0x11 0x04 shall be supported by the ECU
    and Dcm will handle it.
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x11 and
    "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService" for sub-service
    0x04. Both shall not be overridden by an callout function name.
    
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
  默认值: 255
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DcmDspDDDidCheckPerSourceDid
  长名称: Dsp Dynamically Defined Did Check Per Source Did
  描述: |
    Specifies whether DCM module shall check the session, security and mode dependencies per source
    DIDs/MemoryRanges with a ReadDataByIdentifier (0x22) with DID in the range 0xF200 to 0xF3FF or
    with a ReadDataByPeriodicIdentifier (0x2A) in the range 0xF200-0xF2FF.
    
    Effect:
    ------------------------------------
    If set to TRUE, DCM will check additionally to the DDID's execution preconditions also these of
    the included items (DIDs or memory blocks). This will ensure that if the DDID contains any
    secured sources, in case of losing the security access level relevant to these sources, the
    protected information will not be accessible.
    
    If set to FALSE, DCM will only consider the DDID's execution preconditions. This saves resources
    (ROM, stack, run-time), but can be a security backdoor if the DDID itself is not secured, but
    includes secured sources.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x2C.
    The
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidDefine/DcmDspDDDidMaxElements"
    parameter determines the run time usage.
    
    Runtime effects:
    ------------------------------------
    The larger number of DDID's source list, the longer the Dcm task execution time, since all
    contained sources will be processed within the same Dcm task activation.
    
    Code ROM usage effects:
    ------------------------------------
    If set to TRUE, the code usage will increase by a constant amount, independent of the number of
    number of DDIDs or their number of sources.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    If set to TRUE, the stack usage will be increased slightly due to the additional checks
    performed in the context of an ongoing diagnostic service processor. The more complex and deep
    mode rule condition expression nesting, the more stack will be needed.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspDDDidCheckConditionReadPerSourceDid
  长名称: Dsp Dynamically Defined Did Check Condition Read Per Source Did
  描述: |
    Specifies whether DCM module shall call the "CheckConditionRead" per source DIDs with a
    ReadDataByIdentifier (0x22) with DID in the range 0xF200 to 0xF3FF or with a
    ReadDataByPeriodicIdentifier (0x2A) in the range 0xF200-0xF2FF.
    
    Effect:
    ------------------------------------
    If set to TRUE, DCM will call the DDID's included DID "ConditionCheckRead" operations of the
    corresponding port interface. This can be useful if any static DIDs do really use the condition
    check read API for accepting an external read request.
    
    If set to FALSE, DCM will not perform any condition check call on the source DIDs. This saves
    resources (ROM, stack, run-time).
    
    Constraints:
    ------------------------------------
    Since the memory blocks do not have such a functionality, this setting does not affect any
    include in a DDID memory ranges.
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x2C.
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService" is defined for
    sub-service 0x2C 0x01.
    
    The
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidDefine/DcmDspDDDidMaxElements"
    parameter determines the run time usage.
    
    Runtime effects:
    ------------------------------------
    The larger number of DDID's source list, the longer the Dcm task execution time, since in the
    worst case (all DIDs are synchronous) all contained DID sources will be processed within the
    same Dcm task activation.
    
    Code ROM usage effects:
    ------------------------------------
    If set to TRUE, the code usage will increase by a constant amount, independent of the number of
    number of DDIDs or their number of sources.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    If set to TRUE, the stack usage will be increased due to the additional checks performed in the
    context of an ongoing diagnostic service processor. The actual stack usage depends on the
    implementation of the corresponding application "ConditionCheckRead" stack usage.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DcmDspMaxPeriodicDidToRead
  长名称: ''
  描述: |
    Indicates the maximum allowed DIDs in a single "ReadDataByPeriodicIdentifier" request.
    
    Effect:
    ------------------------------------
    Any diagnostic request for service 0x2A with more DIDs as specified by this parameter will be
    rejected by a negative response.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x2A.
    
    Runtime effects:
    ------------------------------------
    The larger number of DIDs per request, the longer the Dcm task execution time, since in the
    worst case (all DIDs are synchronous) all requested DIDs will be processed within the same Dcm
    task activation.
    
    Code ROM usage effects:
    ------------------------------------
    If more than one DID is specified to be allowed, the Dcm code usage may slightly increase due to
    the iteration loops.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    The RAM usage can increase with increasing the value of this parameter.
    
    Stack RAM usage effects:
    ------------------------------------
    none
    
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: DcmDspDDDidClearOnStateChange
  长名称: Dsp Dynamically Defined Did Clear On State Change
  描述: |
    Specifies whether DCM module shall clear a DDID when a session/security level change occurs and
    the DDID (or its content) is no longer accessible in the new state.
    
    Effect:
    ------------------------------------
    If set to TRUE, DCM will verify whether any defined DDID (or its content) is still accessible
    under the new DCM session/security/mode condition states.
    Note: If the DDID is also a periodic DID, then it will be removed from the scheduler too.
    
    If set to FALSE, DCM will not automatically clear any affected DDID. This saves resources (ROM,
    stack, run-time), but can be a security backdoor if the DDID itself is not secured, but includes
    secured sources and the option: /Dcm/DcmConfigSet/DcmDsp/DcmDspDDDidCheckPerSourceDid is not
    turned on.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x2C.
    The
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidDefine/DcmDspDDDidMaxElements"
    parameter determines the run time usage.
    
    Runtime effects:
    ------------------------------------
    The larger number of DDID's source list, the longer the Dcm task execution time, since all
    contained sources will be processed within the same Dcm task activation.
    
    Code ROM usage effects:
    ------------------------------------
    If set to TRUE, the code usage will increase by a constant amount, independent of the number of
    number of DDIDs or their number of sources.
    
    Const data ROM usage effects:
    ------------------------------------
    If set to TRUE, the code usage will increase by a amount, dependent of the number of number of
    DDIDs.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    If set to TRUE, the stack usage will be increased slightly due to the additional checks
    performed in the context of an ongoing diagnostic service processor. The more complex and deep
    mode rule condition expression nesting, the more stack will be needed.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DcmDspDidLookUpFilterEnabled
  长名称: ''
  描述: |
    Specifies whether external DID look up filtering will be supported.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will call an application function that can classify a valid DID as (temporarily)
    not supported. This is useful in case of variant handling.
    If disabled, Dcm uses only the internal look-up engine result and accepts any valid DID
    configured in ECUC.
    
    Constraints:
    -----------------------------------------
    This option has any effect only if at least one DID diagnostic service is handled within DCM.
    
    Dependencies:
    -----------------------------------------
    There must be at least one DcmDsdService related to DIDs that is internally handled by DCM.
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature will slightly increase the Dcm task time during any DID request validation
    operation.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    Enabling this feature may lead to a minor increase of the Dcm static code RAM usage.
    
    Stack RAM usage effects:
    ------------------------------------
    Due to the additional calls done from within the Dcm_MainFunction for gathering the DID
    filtering, the stack usage may increase. It will depend on the implementation of the application
    callback.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DcmDspRidLookUpFilterEnabled
  长名称: ''
  描述: |
    Specifies whether external RID look up filtering will be supported.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will call an application function that can classify a valid RID as (temporarily)
    not supported. This is useful in case of variant handling.
    If disabled, Dcm uses only the internal look-up engine result and accepts any valid RID
    configured in ECUC.
    
    Constraints:
    -----------------------------------------
    This option has any effect only if service 0x31 (RoutineControl) is handled within DCM.
    
    Dependencies:
    -----------------------------------------
    A DcmDsdService with SID 0x31 must be handled internally by DCM.
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature will slightly increase the Dcm task time during any request for SID 0x31.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    Due to the additional calls done from within the Dcm_MainFunction for gathering the DID
    filtering, the stack usage may increase. It will depend on the implementation of the application
    callback.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DcmDspReadDIDReportsNODIByte
  长名称: ''
  描述: |
    Specifies whether the NODI byte of an OBD VID shall be reported when reading the corresponding
    OBD DID (0xF801-0xF8FF).
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will completely mirror the OBD2 VID data, including the NODI byte in the
    corresponding DID.
    If disabled, Dcm will comply with the ISO27145-3 (WWH-OBD) and AR 4.2.2 SWS omitting the NODI
    byte in the DID data.
    
    Constraints:
    -----------------------------------------
    This option has any effect only if:
    - Service 0x09 (RequestVehicleInformation) is handled within DCM.
    AND
    - Service 0x22 (ReadDataByIdentifier) is handled within DCM.
    AND
    - There are any DIDs in the range 0xF8XX that overlap with any VIDs of SID 0x09.
    
    
    Dependencies:
    -----------------------------------------
    A DcmDsdService with SID 0x22 must be handled internally by DCM.
    There shall be at least one DID in range 0xF8XX that overlaps with an OBD2 VID, so the automatic
    OBD mirroring is enabled.
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature will slightly decrease the Dcm task time during any request for SID 0x22
    of 0xF8XX.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor decrease of the Dcm generated code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    Due to the additional calls done from within the Dcm_MainFunction for gathering the DID
    filtering, the stack usage may increase. It will depend on the implementation of the application
    callback.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DcmDspRteImplicitComEnabled
  长名称: ''
  描述: |
    Specifies whether an intermediate buffer is used for paged read operations or when reading a
    linear signal with a variable length.
    Note: This feature is only required if the RTE has to copy data between SW-C and DCM.
    
    Effect:
    -----------------------------------------
    If enabled, a dedicated buffer shall be established to copy data from the RTE.
    
    Constraints:
    -----------------------------------------
    This option has an effect only if:
    - Service 0x22 (ReadDataByIdentifier) is handled within DCM.
    AND
    - There is at least one static DID with a paged signal or with variable length.
    AND
    - The variable length/paged signal of that DID uses a C/S interface.
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature will slightly increase the Dcm task time during any request for SID 0x22.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm generated code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    Enabling this feature leads to an increase of global RAM usage. The amount depends on the
    configuration.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DcmDspReadPagedDataPageSize
  长名称: ''
  描述: |
    Specifies the size of the paged buffer.
    
    Effect:
    -----------------------------------------
    If enabled, that value shall be used as the buffer size for paged read operations.
    
    Constraints:
    -----------------------------------------
    This option has an effect only if:
    - /MICROSAR/Dcm/DcmConfigSet/DcmDsp/DcmDspRteImplicitComEnabled is enabled.
    AND
    - Service 0x22 (ReadDataByIdentifier) is handled within DCM.
    AND
    - There is at least one static DID with a paged signal.
    AND
    - That paged signal uses a C/S interface.
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    Runtime efficiency depends on the configured size.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    RAM usage depends on the configured size.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 7
  最小值: 1
  最大值: 4294967294
```

### 21. DcmDspAuthentication

**描述**: This container contains the configuration for the UDS service Authentication (0x29).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspAuthenticationRoleSize
  长名称: ''
  描述: |
    Defines the size in bytes for the role element within a certificate.
    
    Effect:
    ------------------------------------
    Dcm expects a role of this size within the certificate.
    
    Constraints:
    ------------------------------------
    All role parameters (e.g. DcmDspServiceRole) shall have a size smaller or equal to this
    parameter.
    
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
  默认值: 1
  最小值: 1
  最大值: 4
- 
  序号: 2
  名称: DcmDspAuthenticationWhiteListDIDMaxSize
  长名称: ''
  描述: |
    Defines the maximum size in bytes for a DID white list element within a certificate.
    
    Effect:
    ------------------------------------
    Any DID white list within a certificate with more bytes as specified by this parameter will be
    rejected with a negative response.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    Increasing this value will increase the Dcm task time depending on the actual size of the white
    list during authentication verification of any request and request processing of SID 0x29 with
    subfunction 0x03.
    
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    The RAM usage increases with increasing the value of this parameter.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 3
  名称: DcmDspAuthenticationWhiteListMemorySelectionMaxSize
  长名称: ''
  描述: |
    Defines the maximum size in bytes for a memory selection white list element within a
    certificate.
    
    Effect:
    ------------------------------------
    Any memory selection white list within a certificate with more bytes as specified by this
    parameter will be rejected with a negative response.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x19 with
    "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService" equal to 0x17, 0x18
    or 0x19.
    
    Runtime effects:
    ------------------------------------
    Increasing this value will increase the Dcm task time depending on the actual size of the white
    list during authentication verification of any request and request processing of SID 0x29 with
    subfunction 0x03.
    
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    The RAM usage increases with increasing the value of this parameter.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 4
  名称: DcmDspAuthenticationWhiteListRIDMaxSize
  长名称: ''
  描述: |
    Defines the maximum size in bytes for a RID white list element within a certificate.
    
    Effect:
    ------------------------------------
    Any RID white list within a certificate with more bytes as specified by this parameter will be
    rejected with a negative response.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x31.
    
    Runtime effects:
    ------------------------------------
    Increasing this value will increase the Dcm task time depending on the actual size of the white
    list during authentication verification of any request and request processing of SID 0x29 with
    subfunction 0x03.
    
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    The RAM usage increases with increasing the value of this parameter.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 5
  名称: DcmDspAuthenticationWhiteListServicesMaxSize
  长名称: ''
  描述: |
    Defines the maximum size in bytes for a services white list element within a certificate.
    
    Effect:
    ------------------------------------
    Any services white list within a certificate with more bytes as specified by this parameter will
    be rejected with a negative response.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    Increasing this value will increase the Dcm task time depending on the actual size of the white
    list during authentication verification of any request and request processing of SID 0x29 with
    subfunction 0x03.
    
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    The RAM usage increases with increasing the value of this parameter.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 6
  名称: DcmDspAuthenticationChallengeClientMaxSize
  长名称: ''
  描述: |
    Defines the maximum size in bytes for the client challenge.
    
    Effect:
    ------------------------------------
    If this parameter exists, Dcm will consider this value for the buffer size validation during
    configuration time.
    
    Constraints:
    ------------------------------------
    The buffer size validation will only be exact if all dependent parameters exist.
    
    Dependencies:
    ------------------------------------
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateClientMaxSize
    -
    /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationProofOfOwnershipClientMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateEcuMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationProofOfOwnershipEcuMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateDataMaxSize
    
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
  最小值: 1
  最大值: 65535
- 
  序号: 7
  名称: DcmDspAuthenticationCertificateClientMaxSize
  长名称: ''
  描述: |
    Defines the maximum size in bytes for the client certificate.
    
    Effect:
    ------------------------------------
    If this parameter exists, Dcm will consider this value for the buffer size validation during
    configuration time.
    
    Constraints:
    ------------------------------------
    The buffer size validation will only be exact if all dependent parameters exist.
    
    Dependencies:
    ------------------------------------
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationChallengeClientMaxSize
    -
    /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationProofOfOwnershipClientMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateEcuMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationProofOfOwnershipEcuMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateDataMaxSize
    
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
  最小值: 1
  最大值: 65535
- 
  序号: 8
  名称: DcmDspAuthenticationProofOfOwnershipClientMaxSize
  长名称: ''
  描述: |
    Defines the maximum size in bytes for the client proof of ownership.
    
    Effect:
    ------------------------------------
    If this parameter exists, Dcm will consider this value for the buffer size validation during
    configuration time.
    
    Constraints:
    ------------------------------------
    The buffer size validation will only be exact if all dependent parameters exist.
    
    Dependencies:
    ------------------------------------
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationChallengeClientMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateClientMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateEcuMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationProofOfOwnershipEcuMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateDataMaxSize
    
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
  最小值: 1
  最大值: 65535
- 
  序号: 9
  名称: DcmDspAuthenticationCertificateEcuMaxSize
  长名称: ''
  描述: |
    Defines the maximum size in bytes for the Ecu certificate.
    
    Effect:
    ------------------------------------
    If this parameter exists, Dcm will consider this value for the buffer size validation during
    configuration time.
    
    Constraints:
    ------------------------------------
    The buffer size validation will only be exact if all dependent parameters exist.
    
    Dependencies:
    ------------------------------------
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationChallengeClientMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateClientMaxSize
    -
    /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationProofOfOwnershipClientMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationProofOfOwnershipEcuMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateDataMaxSize
    
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
  最小值: 1
  最大值: 65535
- 
  序号: 10
  名称: DcmDspAuthenticationProofOfOwnershipEcuMaxSize
  长名称: ''
  描述: |
    Defines the maximum size in bytes for the Ecu proof of ownership.
    
    Effect:
    ------------------------------------
    If this parameter exists, Dcm will consider this value for the buffer size validation during
    configuration time.
    
    Constraints:
    ------------------------------------
    The buffer size validation will only be exact if all dependent parameters exist.
    
    Dependencies:
    ------------------------------------
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationChallengeClientMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateClientMaxSize
    -
    /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationProofOfOwnershipClientMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateEcuMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateDataMaxSize
    
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
  最小值: 1
  最大值: 65535
- 
  序号: 11
  名称: DcmDspAuthenticationGeneralNRC
  长名称: ''
  描述: |
    Defines the NRC that shall be sent as replacement of all ISO 14229-1 defined NRCs in case of
    invalid certificate or content.
    
    Effect:
    ------------------------------------
    If the mode rule "DcmDspAuthenticationGeneralNRCModeRuleRef" is evaluated to true, Dcm will send
    this general NRC instead of the specific NRC codes for the cases whenever a "Certificate
    verification failed" NRC is returned.
    
    Constraints:
    ------------------------------------
    Has an effect during runtime only if "DcmDspAuthenticationGeneralNRCModeRuleRef" is evaluated to
    true.
    
    Dependencies:
    ------------------------------------
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationGeneralNRCModeRuleRef
    
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
  最大值: 255
- 
  序号: 12
  名称: DcmDspAuthenticationDefaultSessionTimeOut
  长名称: ''
  描述: |
    Defines the number of seconds after which the Dcm makes a transition to deauthenticated state,
    in case of no active communication in default session.
    
    Effect:
    ------------------------------------
    Dcm will start the configured time after request processing in default session.
    
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
- 
  序号: 13
  名称: DcmDspAuthenticationSetDeauthenticatedRoleApi
  长名称: ''
  描述: |
    Specifies whether Dcm shall provide setting Deauthenticated Role or not.
    
    Effect:
    -----------------------------------------
    By enabling this feature, the Dcm will provide an API "Dcm_SetDeauthenticatedRole" for setting a
    Deauthenticated Role. If this information is not needed within the ECU project, leave this
    feature disabled for minimum ROM usage.
    
    Constraints:
    -----------------------------------------
    none
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature leads to an insignificant increase of the Runtime, caused by handling the
    API in the mainfunction.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    Enabling this feature leads to an insignificant increase of the ROM usage, caused by the API
    function implementation.
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    none
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: DcmDspAuthenticationCertificateDataMaxSize
  长名称: ''
  描述: |
    Defines the maximum size in bytes for the certificate data for subfunction trasmitCertificate
    (0x04).
    
    Effect:
    ------------------------------------
    If this parameter exists, Dcm will consider this value for the buffer size validation during
    configuration time.
    
    Constraints:
    ------------------------------------
    The buffer size validation will only be exact if all dependent parameters exist.
    
    Dependencies:
    ------------------------------------
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateClientMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationChallengeClientMaxSize
    -
    /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationProofOfOwnershipClientMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationCertificateEcuMaxSize
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationProofOfOwnershipEcuMaxSize
    
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
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 15
  名称: DcmDspAuthenticationUserSpecificRoles
  长名称: ''
  描述: |
    Defines whether Dcm shall use the standard KeyM_CertElementGet() interface to read the
    authentication roles from the certificate during processing of sub-function 0x03, or to call
    Dcm_GetAuthenticationRole() to read them from the application one by one.
    
    Effect:
    ------------------------------------
    Enables the Dcm_GetAuthenticationRole() callback.
    
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
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: DcmDspAuthenticationBypassEnabled
  长名称: ''
  描述: |
    Specifies whether DCM module shall support a bypass mode for precondition checks related to
    authentication or not.
    
    Effect:
    ------------------------------------
    If set to TRUE, DCM will support a bypass mode for precondition checks for Authentication.
    
    Constraints:
    ------------------------------------
    This attribute is enabled only when Service 0x29 is implemented completely externally or
    completely internally.
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x29.
    
    Runtime effects:
    ------------------------------------
    Enabling this feature will slightly increase the Dcm task time.
    
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
  默认值: false
  最小值: ''
  最大值: ''
```

### 22. DcmDspAuthenticationConnection

**描述**: This container contains the authentication configuration used for a dsl connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspAuthenticationEcuChallengeLength
  长名称: ''
  描述: |
    Specifies the length of the server challenge.
    
    Effect:
    ------------------------------------
    Dcm will send a server challenge of this length for authentication to the client.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    Increasing this value will slightly increase the Dcm task time during request processing for SID
    0x29 with subfunction 0x01 or 0x02.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    The RAM usage increases with increasing the value of this parameter.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: ''
  最小值: 1
  最大值: 65535
```

### 23. DcmDspAuthenticationRow

**描述**: This container contains the configuration for each DcmDspAuthentication role.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspAuthenticationRoleBitPosition
  长名称: ''
  描述: |
    Role that can be referenced by certain elements.
    
    Effect:
    ------------------------------------
    Defines the bit number that represents the role in the authentication bit field. The bit mask is
    aligned with the logical bit calculations: 2^DcmDspAuthenticationRoleBitPosition.
    
    Constraints:
    ------------------------------------
    The value must be in the range of
    '/Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationRoleSize'.
    
    Dependencies:
    ------------------------------------
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspAuthentication/DcmDspAuthenticationRoleSize
    
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
  默认值: 1
  最小值: 0
  最大值: 31
```

### 24. DcmDspAuthenticationTransmitCertificate

**描述**: This container contains the authentication configuration for the subfunction trasnmitCertificate.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspAuthenticationTransmitCertificateEvaluationId
  长名称: ''
  描述: |
    Certificate evaluation id.
    
    Effect:
    ------------------------------------
    This parameter is used to define the evaluation id used for sub-function transmitCertificate
    (0x04).
    The value is not standardized by either the ISO 14229-1 or AUTOSAR and therefore has an
    OEM-specific meaning.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    non
    
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
- 
  序号: 2
  名称: DcmDspAuthenticationTransmitCertificateFunction
  长名称: ''
  描述: Provides a fixed semantics to this certificate that will lead to predefined actions in the
      Dcm.
  默认值: SECURE_CODING
  最小值: ''
  最大值: ''
```

### 25. DcmDspClearDTC

**描述**: This container contains the configuration for the DCM DTC memory related information. This container
exists only if the UDS Service ClearDiagnosticInformation (0x14) is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspClearDTCMemorySelectionEnabled
  长名称: ''
  描述: |
    Specifies whether UserDefined Memory selection for diagnostic service 0x14 is supported or not.
    
    Effect:
    ------------------------------------
    If enabled, Dcm accepts diagnostic service 0x14 requests with a byte for the memory selection.
    
    Constraints:
    ------------------------------------
    -
    
    Dependencies:
    ------------------------------------
    Will be used only if the diagnostic service 0x14 is to be supported by DCM and DEM API version
    4.3.0 or newer is selected.
    
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
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspClearDTCMemoryUserMemoryId
  长名称: ''
  描述: |
    Specifies the supported user memory id for service 0x14.
    
    Effect:
    ------------------------------------
    If specified a user memory identifier, DCM will accept only the user memory ID that is
    configured here.
    If no user memory identifier specified, DCM will accept any value in the request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Will be used only if DcmDspClearDTCMemorySelectionEnabled is set to true.
    
    Runtime effects:
    ------------------------------------
    If any user memory id specified, the DCM will check any related request upon this value and this
    leads to an insignificantly increased run time usage.
    
    Code ROM usage effects:
    ------------------------------------
    If any user memory id specified, the DCM will check any related request upon this value and this
    leads to an insignificantly increased code ROM usage.
    
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
```

### 26. DcmDspComControl

**描述**: This container provides configuration parameters for service 0x28 (CommunciationControl).

该容器没有参数。

### 27. DcmDspComControlAllChannel

**描述**: Collection of ComM channels which shall be controlled if all networks are addressed.

Effect:
------------------------------------
Each container of this type will specify a ComM channel to be controlled if all networks are
addressed.


Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
The more channels to be managed by Dcm the longer the processing time during execution of
communication control over all channels.

Code ROM usage effects:
------------------------------------
The minimum ROM usage is on a single channel systems. For two or more channels there is no overhead.

Const data ROM usage effects:
------------------------------------
The data ROM usage in the Dcm configuration scales with the number of references specified by this
setting.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
If more than one channel is specified here, the Dcm stack usage will insignificantly increase during
the all network communication control command execution.

该容器没有参数。

### 28. DcmDspComControlSetting

**描述**: Provide the configuration of the Communication control.

该容器没有参数。

### 29. DcmDspComControlSpecificChannel

**描述**: NOT USED

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspSubnetNumber
  长名称: ''
  描述: Subnet Number which controls the specific ComMChannel.
  默认值: ''
  最小值: 1
  最大值: 14
```

### 30. DcmDspControlDTCSetting

**描述**: Provide the configuration of the ControlDTCSetting mechanism.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmSupportDTCSettingControlOptionRecord
  长名称: ''
  描述: |
    This configuration switch defines if the DTCSettingControlOptionRecord is in general supported
    in the request message or not.
    
    Effect:
    ------------------------------------
    If enabled, the Dcm will expect a DTC group to be specified in the request message for service
    0x85 (ControlDTCSetting).
    If disabled, Dcm will reject any request of this service if sent with a DTC group parameter.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - Service 0x85 is supported by Dcm;
    
    Runtime effects:
    ------------------------------------
    If enabled, the DTC group extraction from the request will increase insignificantly the Dcm main
    function run time on processing service 0x85.
    
    Code ROM usage effects:
    ------------------------------------
    If enabled, the DTC group extraction from the request will increase insignificantly the Dcm code
    ROM usage.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    If enabled, the DTC group extraction from the request may increase insignificantly the Dcm main
    function stack usage.
  默认值: false
  最小值: ''
  最大值: ''
```

### 31. DcmDspData

**描述**: This container contains the configuration (parameters) of a Data belonging to a DID.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDataConditionCheckReadFnc
  长名称: ''
  描述: |
    Specifies the call out function name for checking DID reading conditions.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on DID reading
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x22 (ReadDataByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to support read access (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidRead)
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort)
    
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
  名称: DcmDspDataEcuSignal
  长名称: ''
  描述: |
    Specifies the function name for control access of a certain ECU Signal by the Dcm.
    
    Effect:
    ------------------------------------
    The Dcm will use the name specified by this parameter to call the corresponding IoHwAb function:
    IoHwAb_Dcm_<EcuSignalName>.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to, supports IO control access (refer to
    Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidControl)
    - the DcmDspDataUsePort is set to one of the USE_ECU_SIGNAL (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort)
    
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
  序号: 3
  名称: DcmDspDataFreezeCurrentStateFnc
  长名称: ''
  描述: |
    Specifies the call out function name for freezing the current IO state.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on DID IO control
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to support IO control access (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidControl/DcmDspDidFreezeCurrentState)
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort)
    
    
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
  序号: 4
  名称: DcmDspDataGetScalingInfoFnc
  长名称: ''
  描述: |
    Specifies the call out function name for reading the DID data object scaling information.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on DID reading scaling
    information diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x24 (ReadScalingDataByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort)
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    For each DID signal that has scaling information additional information will be stored. This
    leads to an additional small ROM data usage.
    
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
  序号: 5
  名称: DcmDspDataReadDataLengthFnc
  长名称: ''
  描述: |
    Specifies the call out function name for reading the DID data object length.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on DID reading
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x22 (ReadDataByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService);
    - the DID to which the data object is mapped to support read access (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidRead);
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort);
    - the data object has variable length (refer
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDataInfo/DcmDspDataFixedLength).
    
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
  序号: 6
  名称: DcmDspDataReadEcuSignal
  长名称: ''
  描述: |
    Specifies the function name for read access of a certain ECU Signal by the Dcm.
    
    Effect:
    ------------------------------------
    The Dcm will use the name specified by this parameter to call the corresponding IoHwAb function:
    IoHwAb_Dcm_Read<EcuSignalName>.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x22 (ReadDataByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to, supports IO control access (refer to
    Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidControl)
    - the DcmDspDataUsePort is set to one of the USE_ECU_SIGNAL (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort)
    
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
  序号: 7
  名称: DcmDspDataReadFnc
  长名称: ''
  描述: |
    Specifies the call out function name for reading the data object content.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on DID reading
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x22 (ReadDataByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to, supports read access (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidRead)
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort)
    
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
  序号: 8
  名称: DcmDspDataResetToDefaultFnc
  长名称: ''
  描述: |
    Specifies the call out function name for resetting the current IO state to its default state.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on DID IO control
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to, supports IO control access (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidControl/DcmDspDidResetToDefault)
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort)
    
    
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
  序号: 9
  名称: DcmDspDataReturnControlToEcuFnc
  长名称: ''
  描述: |
    Specifies the call out function name for returning the IO control to the application.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on DID IO control
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to, supports IO control access (refer to
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidControl/DcmDspDidReturnControlToEcu")
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort)
    
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
  序号: 10
  名称: DcmDspDataShortTermAdjustmentFnc
  长名称: ''
  描述: |
    Specifies the call out function name for adjusting the IO state.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on DID IO control
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to, supports IO control access (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidControl/DcmDspDidShortTermAdjustment)
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort)
    
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
  序号: 11
  名称: DcmDspDataSize
  长名称: ''
  描述: |
    Specifies the length of DID data in bits. If Data has variable data length, this parameter
    specifies the maximum data length.
    
    Effect:
    ------------------------------------
    The sum of all data object lengths of a DID specifies the total DID length which, depending on
    the DID operation (e.g. write/read), will be validated at request reception resp. used for
    response composition.
    
    Constraints:
    ------------------------------------
    The size shall always be a multiple of 8 (byte borders).
    On S/R data access the following constraints shall be considered:
    - if the data type is one of the multi byte atomics: (U|S)INT(16|32), the value of this
    parameter will not be evaluated.
    - if the data type is UINT8 and the size is a multiple (more than 1) of 8, the result
    implementation data type will be the same as if the data type was set to UINT8_N.
    
    
    Dependencies:
    ------------------------------------
    The size parameter is either the concrete or maximum data object size, depending on the
    DcmDspDataFixedLength parameter value (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDataInfo/DcmDspDataFixedLength).
    
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
  默认值: 65535
  最小值: 8
  最大值: 524280
- 
  序号: 12
  名称: DcmDspDataUsePort
  长名称: ''
  描述: |
    Defines which kind of interface shall be used to access the data.
    
    Effect:
    ------------------------------------
    Depending on the selected type, the Dcm application has to implement either a RTE call, a call
    out or nothing at all.
    
    Note: USE_NO_DATA is applied for gaps at the end of DID to fill up the DID layout. Since they do
    not carry and data, no callback will be invoked.
    
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
    If set USE_BLOCK_ID, the code usage of DCM will slightly increase.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: USE_DATA_ASYNCH_CLIENT_SERVER
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: DcmDspDataWriteFnc
  长名称: ''
  描述: |
    Specifies the call out function name for writing the data object content.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on DID write diagnostic
    request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x2E (WriteDataByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to, supports read access (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidWrite)
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort)
    
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
  序号: 14
  名称: DcmDspDataConditionCheckReadFncUsed
  长名称: ''
  描述: |
    This parameter determines if a condition check function is available or not.
    
    Effect:
    ------------------------------------
    If set to TRUE and DcmDspDataUsePort is set to
     - 'USE_DATA_ASYNCH_CLIENT_SERVER' or 'USE_DATA_SYNCH_CLIENT_SERVER', the SWC will be called to
    get access permission.
     - 'USE_DATA_SYNCH_FNC' or 'USE_DATA_ASYNCH_FNC', the  parameter
    'DcmDspDataConditionCheckReadFnc shall contain a valid C-function name.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x22 (ReadDataByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to, supports read access (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidRead)
    - the DcmDspDataUsePort is set to one of the FNC or CLIENT_SERVER types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort)
    
    
    Runtime effects:
    ------------------------------------
    If disabled, the run-time of a DID is speed up.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    For each data element that needs this function call, the constant ROM usage will increase by
    several bytes.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: DcmDspDataType
  长名称: ''
  描述: |
    Provide the data type of a data object belonging to a DID signal.
    
    Effect:
    ------------------------------------
    Affects the data object access interface.
    
    Constraints:
    ------------------------------------
    Only applicable for S/R and EcuSignal port interfaces.
    For C/S ports any set up type will be interpret as an UINT8 type. In this cases the actual
    signal size will be determined by corresponding parameter
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataSize.
    
    Dependencies:
    ------------------------------------
    Usage depends on the parameter /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataUsePort.
    
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
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: DcmDspDataEndianness
  长名称: ''
  描述: Defines the endianness of the data belonging to a DID in a diagnostic request or response
      message.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: DcmDspDataTypedDataInterfaceEnabled
  长名称: ''
  描述: |
    Overwrites the default setting specified by DcmGeneral/DcmTypedDataInterfacesEnabled for a
    specific DID data object.
    
    Effect:
    -----------------------------------------
    See DcmGeneral/DcmTypedDataInterfacesEnabled
    
    Constraints:
    -----------------------------------------
    See DcmGeneral/DcmTypedDataInterfacesEnabled
    
    Dependencies:
    -----------------------------------------
    See DcmGeneral/DcmTypedDataInterfacesEnabled
    
    Runtime effects:
    -----------------------------------------
    See DcmGeneral/DcmTypedDataInterfacesEnabled
    
    Code ROM usage effects:
    ------------------------------------
    See DcmGeneral/DcmTypedDataInterfacesEnabled
    
    Const data ROM usage effects:
    -----------------------------------------
    See DcmGeneral/DcmTypedDataInterfacesEnabled
    
    Global RAM usage effects:
    -----------------------------------------
    See DcmGeneral/DcmTypedDataInterfacesEnabled
    
    Stack RAM usage effects:
    -----------------------------------------
    See DcmGeneral/DcmTypedDataInterfacesEnabled
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: DcmDspDataConstantValue
  长名称: ''
  描述: |
    Specifies the constant content of this signal.
    
    Effect:
    ------------------------------------
    For a read access (i.e. via service 0x22) the content of this parameter gets reported. The DCM
    will handle the read access to this data signal internally, there will be no port available. The
    DCM will add padding bytes (0xFF) in case of the configured data size (DcmDspDataSize) is larger
    than the constant content.
    
    Constraints:
    ------------------------------------
    The allowed characters/digits depend on the selected value of parameter
    /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataConstantValueType.
    
    Dependencies:
    ------------------------------------
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataConstantValueType
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataSize
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to an increas of the Dcm generated code ROM usage.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    Enabling this feature can lead to a major increased stack size required by the Dcm_MainFunction.
    The amount of additional RAM usage depends on the provided constant vlaue and the related
    DcmDspDataSize.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: DcmDspDataConstantValueType
  长名称: ''
  描述: |
    Specifies the type of the content provided within parameter DcmDspDataConstantValue.
    
    Effect:
    ------------------------------------
    Defines how the DCM interprets the content of parameter DcmDspDataConstantValue.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataConstantValue
    
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
  默认值: HEX
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: DcmDspDataConstantValuePaddingPattern
  长名称: ''
  描述: |
    Determines the padding byte value for the unused data bytes for the constant value.
    
    Effect:
    ------------------------------------
    If this parameter does not exist, padding will be applied with value 0xFF.
    If this parameter exists, the selected value will be used for padding in case of the configured
    data size (DcmDspDataSize) is larger than the constant content.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataConstantValue
    - /Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataSize
    
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
  默认值: 255
  最小值: 0
  最大值: 255
```

### 32. DcmDspDataInfo

**描述**: This container contains the configuration (parameters) of a Data

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDataFixedLength
  长名称: ''
  描述: |
    Specifies whether the data object has a constant (fixed) or variable length.
    
    Effect:
    ------------------------------------
    If set to TRUE, the Dcm will use the data length parameter value of a data object directly from
    the configuration. If set to FALSE, the Dcm will gather the concrete length from the
    application.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Affects the interpretation of the length parameter
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspData/DcmDspDataSize".
    
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
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspDataScalingInfoSize
  长名称: ''
  描述: |
    If scaling information service is available for this data object, it provides the size of the
    scaling information in bytes.
    
    Effect:
    ------------------------------------
    The Dcm uses this value to put the correct amount of scaling information for service 0x24
    (GetScalingInfoByIdentifier).
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x24 (ReadScalingDataByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to support scaling info access (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidScaling)
    
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

### 33. DcmDspDid

**描述**: This container contains the configuration (parameters) of the DID.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDidIdentifier
  长名称: ''
  描述: |
    Specifies the identifier value of a DID.
    
    Effect:
    ------------------------------------
    The Dcm only recognizes DIDs with the value specified in this parameter.
    
    Constraints:
    ------------------------------------
    The DID value must be unique within a DcmConfigset.
    
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
  名称: DcmDspDidRoeQueueEnabled
  长名称: ''
  描述: NOT USED
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspDidUsed
  长名称: ''
  描述: |
    Allows to activate or deactivate the usage of a DID for multi purpose ECUs.
    In a single configurations the parameter can be used to temporarily disable a complete DID in
    the Dcm configuration without the need to delete all its configuration parameters.
    
    Effect:
    ------------------------------------
    If set to FALSE, the DID and all its signals will not be used in the Dcm generated code.
    
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
    If set to FALSE, no data ROM for this DID will be used in the Dcm configuration sources.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspDidUsePort
  长名称: ''
  描述: |
    Allows to combine the signals of this DID to a struct data type, and provides corresponding
    ports.
    
    
    Effect:
    ------------------------------------
    If set to USE_ATOMIC_SENDER_RECEIVER_INTERFACE_AS_SERVICE (resp. USE_ATOMIC_NV_DATA_INTERFACE),
    Sender-Receiver-Ports (resp. NvData-Ports) are created for
     (a) the struct, in addition to a Data-Transformation-Set,
     (b) a uint8-byte-stream of size equal to the combined signal.
    
    If set to USE_DATA_ELEMENT_SPECIFIC_INTERFACES (default), a separate port is created for each
    signal of the DID. The type of the port is determined by the configuration of the signal
    DspData.
    
    Constraints:
    ------------------------------------
    If set to USE_ATOMIC_NV_DATA_INTERFACE then DID does not support IO-Control-Operation.
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    If value other than the USE_DATA_ELEMENT_SPECIFIC_INTERFACES selected, DCM will have only single
    data element DID access. This will reduce the runtime usage for DID access services (e.g. 0x22,
    0x2A, 0x2E) when requested especially if no other multiple data element DIDs are configured.
    
    Code ROM usage effects:
    ------------------------------------
    If value other than the USE_DATA_ELEMENT_SPECIFIC_INTERFACES selected, DCM will have only single
    data element DID access, which may reduce the code ROM usage if no other multiple data element
    DID still exists.
    
    Const data ROM usage effects:
    ------------------------------------
    If value other than the USE_DATA_ELEMENT_SPECIFIC_INTERFACES selected, DCM will have only single
    data element DID access, which will slightly reduce the ROM data usage per DID.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: USE_DATA_ELEMENT_SPECIFIC_INTERFACES
  最小值: ''
  最大值: ''
```

### 34. DcmDspDidSignal

**描述**: This container defines the reference to 1 DcmDspData container and position relevant for this DID.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDidDataPos
  长名称: ''
  描述: |
    Specifies the position of the signal in the DID.
    
    Effect:
    ------------------------------------
    Affects the call out/service call function calling order.
    
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
  最大值: 524280
```

### 35. DcmDspDidInfo

**描述**: This container contains the configuration (parameters) of the DID's Info

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDidDynamicallyDefined
  长名称: ''
  描述: |
    Specifies whether the DID shall be treated as a dynamically defined DID (DDID).
    
    Effect:
    ------------------------------------
    If set to TRUE, the DID this setting belongs to will be treated as a DDID with the constraints
    described below.
    
    Constraints:
    ------------------------------------
    A DID specified to be DDID by this parameter:
    - has no data signals specified at configuration time:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspDid/DcmDspDidSignal" shall not exist.
    - is only readable (no scaling, IO and write operations are allowed).
    
    Dependencies:
    ------------------------------------
    The following parameters have to be considered too:
    -"/Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidDefine/DcmDspDDDidMaxElements"
    -"/Dcm/DcmConfigSet/DcmDsp/DcmDspDDDidCheckPerSourceDid"
    -"/Dcm/DcmConfigSet/DcmDsp/DcmDspDDDidCheckConditionReadPerSourceDid"
    -"/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x2C.
    -"/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService" is defined for
    sub-service 0x2C 0x01.
    
    Runtime effects:
    ------------------------------------
    Due to the nature of a DDID (container of multiple other DID or memory sources) the processing
    of a DDID (reading, validating) increases the DCM main-function run-time. The worst case of this
    effect is while processing only synchronous source DIDs/memory ranges, since in this case the
    complete definition list of the DDID will be processed within the same DCM main-function
    activation.
    
    Code ROM usage effects:
    ------------------------------------
    The DDID management requires a significant amount of ROM code. The actual usage does not depend
    on the amount of DDID in the ECU configuration, but depends on a complex relationship among
    multiple configuration parameters.
    
    Const data ROM usage effects:
    ------------------------------------
    If no DDID are to be supported, the Dcm configuration ROM usage will be reduced significantly
    (depends on the total number of DIDs in the configuration).
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    Since the processing of a DDID (reading, validating it) is performed within a running DCM main
    function service processor context, the stack usage will increase significantly. The actual
    stack usage depends mostly on the stack usage of the application DID and memory range read
    access implementations.
  默认值: false
  最小值: ''
  最大值: ''
```

### 36. DcmDspDidAccess

**描述**: This container contains the configuration (parameters) of the DID access

该容器没有参数。

### 37. DcmDspDidControl

**描述**: Specifies whether the DID shall support IO control operation.

Effect:
------------------------------------
If set to TRUE, Dcm will accept a IO control operation request on this DID. Otherwise, the Dcm will
reject the request with a NRC 0x31 (RequestOutOfRange).

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
Has effect only if the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm
(refer to /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
If no DID supports IO control operation the Dcm code ROM usage will decrease due to the removed
functionality.

Const data ROM usage effects:
------------------------------------
If set to TRUE, the Dcm configuration data ROM usage will increase due to the additional data to be
hold for this operation.

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
  名称: DcmDspDidFreezeCurrentState
  长名称: ''
  描述: |
    Specifies whether the DID shall support IO control freeze current state operation.
    
    Effect:
    ------------------------------------
    If set to TRUE, Dcm will accept a IO control freeze current state operation request on this DID.
    Otherwise, the Dcm will reject the request with a NRC 0x31 (RequestOutOfRange).
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm
    (refer to /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    If no DID supports IO control freeze current state operation the Dcm code ROM usage will
    decrease due to the removed functionality.
    
    Const data ROM usage effects:
    ------------------------------------
    If set to TRUE, the Dcm configuration data ROM usage will increase due to the additional data to
    be hold for this operation.
    
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
  名称: DcmDspDidResetToDefault
  长名称: ''
  描述: |
    Specifies whether the DID shall support IO control reset to default state operation.
    
    Effect:
    ------------------------------------
    If set to TRUE, Dcm will accept a IO control reset to default state operation request on this
    DID. Otherwise, the Dcm will reject the request with a NRC 0x31 (RequestOutOfRange).
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm
    (refer to /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    If no DID supports IO control reset to default state operation the Dcm code ROM usage will
    decrease due to the removed functionality.
    
    Const data ROM usage effects:
    ------------------------------------
    If set to TRUE, the Dcm configuration data ROM usage will increase due to the additional data to
    be hold for this operation.
    
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
  序号: 3
  名称: DcmDspDidReturnControlToEcu
  长名称: ''
  描述: |
    Specifies whether the DID shall support IO control return control to ECU operation.
    
    Effect:
    ------------------------------------
    If set to TRUE, Dcm will accept a IO control return control to ECU operation request on this
    DID. Otherwise, the Dcm will reject the request with a NRC 0x31 (RequestOutOfRange).
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm
    (refer to /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    If no DID supports IO control return control to ECU operation the Dcm code ROM usage will
    decrease due to the removed functionality.
    
    Const data ROM usage effects:
    ------------------------------------
    If set to TRUE, the Dcm configuration data ROM usage will increase due to the additional data to
    be hold for this operation.
    
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
  序号: 4
  名称: DcmDspDidShortTermAdjustment
  长名称: ''
  描述: |
    Specifies whether the DID shall support IO control short term adjustment to ECU operation.
    
    Effect:
    ------------------------------------
    If set to TRUE, Dcm will accept a IO control short term adjustment operation request on this
    DID. Otherwise, the Dcm will reject the request with a NRC 0x31 (RequestOutOfRange).
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm
    (refer to /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    If no DID supports IO control short term adjustment operation the Dcm code ROM usage will
    decrease due to the removed functionality.
    
    Const data ROM usage effects:
    ------------------------------------
    If set to TRUE, the Dcm configuration data ROM usage will increase due to the additional data to
    be hold for this operation.
    
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
  序号: 5
  名称: DcmDspDidControlMask
  长名称: ''
  描述: |
    Specifies the type of an IO DID control enable mask record handling.
    
    Effect:
    ------------------------------------
    If set to "INTERNAL", DCM will automatically calculate the required CEMR size depending on the
    amount of IODID data elements. If a single data element is defined - no CEMR will be used.
    If set to "NO", DCM will not expect any CEMR for this IO DID in its request, and will reject any
    CEMR sent along with this IO DID.
    If set to "EXTERNAL", DCM will forward the requested CEMR to the application function associated
    with only data element allowed to be configured.
    
    Constraints:
    ------------------------------------
    If set to "EXTERNAL", the IO DID must have only single data element that covers all IO signals
    to be controlled by service 0x2F.
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm
    (refer to /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    Runtime effects:
    ------------------------------------
    IO DIDs using external CEMR does have only single signal and thus less run-time overhead in DCM,
    but in the application.
    
    Code ROM usage effects:
    ------------------------------------
    If no IO controlled DID supports the IO CEM record, the Dcm code ROM usage will be reduced.
    
    Const data ROM usage effects:
    ------------------------------------
    If no IO controlled DID supports the IO control enable mask record, the Dcm configuration ROM
    usage will be reduced significantly (depends on the total number of DIDs in the configuration).
    
    Global RAM usage effects:
    ------------------------------------
    For external CEMRs with more than four bytes, additional global RAM buffer is allocated for a
    diagnostic session change in order to reset all states under control properly.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: DCM_CONTROLMASK_INTERNAL
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DcmDspDidControlMaskSize
  长名称: ''
  描述: |
    Specifies the size of the IO DID control enable mask record in bytes.
    
    Effect:
    ------------------------------------
    DCM automatically calculates the CEM (Control Enable Mask) if an IO DID refers to more than one
    DcmDspData object. In cases where a single DcmDspData covers multiple IO signals (i.e.
    bit-mapped signals), the CEM shall be overridden using this parameter. The Dcm will use the
    value of this parameter in order to validate the diagnostic request length properly.
    
    Constraints:
    ------------------------------------
    This setting is required to be set only if an IO DID shall support the enable mask record in the
    diagnostic request. Otherwise DCM will not be able to evaluate the request length correctly.
    
    Dependencies:
    ------------------------------------
    Has effect only if
    - the diagnostic service 0x2F (IOControlByDataIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    - Parameter
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidControl/DcmDspDidControlMask is
    set to "EXTERNAL".
    
    Runtime effects:
    ------------------------------------
    IO DIDs using external CEMR does have only single signal and thus less run-time overhead in DCM,
    but in the application.
    
    Code ROM usage effects:
    ------------------------------------
    If no IO controlled DID supports the IO CEM record, the Dcm code ROM usage will be reduced.
    
    Const data ROM usage effects:
    ------------------------------------
    If no IO controlled DID supports the IO control enable mask record, the Dcm configuration ROM
    usage will be reduced significantly (depends on the total number of DIDs in the configuration).
    
    Global RAM usage effects:
    ------------------------------------
    For external CEMRs with more than four bytes, additional global RAM buffer is allocated for a
    diagnostic session change in order to reset all states under control properly.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 1
  最小值: 0
  最大值: 65535
```

### 38. DcmDspDidRead

**描述**: Specifies whether the DID shall support read operation.

Effect:
------------------------------------
If set to TRUE, Dcm will accept a read operation request on this DID. Otherwise, the Dcm will reject
the request with a NRC 0x31 (RequestOutOfRange).

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
Has effect only if the diagnostic service 0x22 (ReadDataByIdentifier) is supported by Dcm (refer to
/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
If no DID supports read operation the Dcm code ROM usage will decrease due to the removed
functionality.

Const data ROM usage effects:
------------------------------------
If set to TRUE, the Dcm configuration data ROM usage will increase due to the additional data to be
hold for this operation.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

该容器没有参数。

### 39. DcmDspDidWrite

**描述**: Specifies whether the DID shall support write operation.

Effect:
------------------------------------
If set to TRUE, Dcm will accept a write operation request on this DID. Otherwise, the Dcm will
reject the request with a NRC 0x31 (RequestOutOfRange).

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
Has effect only if the diagnostic service 0x2E (WriteDataByIdentifier) is supported by Dcm (refer to
/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
If no DID supports write operation the Dcm code ROM usage will decrease due to the removed
functionality.

Const data ROM usage effects:
------------------------------------
If set to TRUE, the Dcm configuration data ROM usage will increase due to the additional data to be
hold for this operation.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

该容器没有参数。

### 40. DcmDspDidDefine

**描述**: Specifies whether the DID shall support define operation.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDDDidMaxElements
  长名称: Dsp Dynamically Defined Did Max Number of Elements
  描述: Maximum number of source elements of a DDDID.
  默认值: 1
  最小值: 1
  最大值: 255
```

### 41. DcmDspDidRange

**描述**: This container defines the DID Range.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDidRangeHasGaps
  长名称: ''
  描述: |
    Parameter specifies whether there are gaps in the DID range or not.
    
    Effect:
    ------------------------------------
    If set to TRUE, Dcm will call the IsDidAvailable operation for any requested DID from within
    this range in order to get additional information whether the concrete DID is supported or not.
    If set to FALSE, Dcm will accept any requested DID from within this range and call the
    corresponding operation (Read/Write) over the data.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    Slightly increased run time at request time due to the additional function call.
    
    Code ROM usage effects:
    ------------------------------------
    Slightly increased code usage due to the additional function call.
    
    Const data ROM usage effects:
    ------------------------------------
    Slightly increased ROM usage due to the additional function call.
    
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    Might be slightly increased run time at request time due to the additional function call. It
    depends on its implementation stack usage.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspDidRangeIdentifierLowerLimit
  长名称: ''
  描述: |
    Specifies the first DID of a range that will be accepted by DCM.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the start of a valid DID range.
    
    Constraints:
    ------------------------------------
    This value shall be lower or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspDidRange/DcmDspDidRangeIdentifierUpperLimit"
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspDidRange/DcmDspDidRangeIdentifierUpperLimit"
    
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
  序号: 3
  名称: DcmDspDidRangeIdentifierUpperLimit
  长名称: ''
  描述: |
    Specifies the last DID of a range that will be accepted by DCM.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the end of a valid DID range.
    
    Constraints:
    ------------------------------------
    This value shall be higher or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspDidRange/DcmDspDidRangeIdentifierLowerLimit"
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspDidRange/DcmDspDidRangeIdentifierLowerLimit"
    
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
  序号: 4
  名称: DcmDspDidRangeIsDidAvailableFnc
  长名称: ''
  描述: Function name to request from application if a specific DID is available within the range or
      not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DcmDspDidRangeMaxDataLength
  长名称: ''
  描述: |
    Specifies the maximum length over all DIDs of a range in bytes.
    
    Effect:
    ------------------------------------
    For the write range operation this value will be validated at request reception for a valid
    length (top value only). The concrete request/response length shall be validated/returned by the
    implementation of the DIDrange port/callback.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    The size parameter is either the concrete or maximum data object size, depending on the
    DcmDspDataFixedLength parameter value (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDataInfo/DcmDspDataFixedLength).
    
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
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: DcmDspDidRangeReadDidFnc
  长名称: ''
  描述: |
    Specifies the call out function name for reading the data of a DID from this range.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on DID range reading
    data diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x22 (ReadDataByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to, supports read access (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidRead)
    - the DcmDspDidRangeUsePort is set to FALSE (e.g. call out)  (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidRange/DcmDspDidRangeUsePort)
    
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
  序号: 7
  名称: DcmDspDidRangeUsePort
  长名称: ''
  描述: |
    Defines which kind of interface shall be used to access the data.
    
    Effect:
    ------------------------------------
    If set to TRUE:  the Dcm application has to provide an a RTE R-Port implementation
    If set to FALSE: the Dcm application has to implement a call out.
    
    
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
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DcmDspDidRangeWriteDidFnc
  长名称: ''
  描述: |
    Specifies the call out function name for writing the data of a DID from this range.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on DID range writing
    data diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x2E (WriteDataByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DID to which the data object is mapped to, supports read access (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidInfo/DcmDspDidAccess/DcmDspDidWrite)
    - the DcmDspDidRangeUsePort is set to FALSE (e.g. call out)  (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspDidRange/DcmDspDidRangeUsePort)
    
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
```

### 42. DcmDspEcuReset

**描述**: This container contains the configuration for DcmDspEcuReset service.

该容器没有参数。

### 43. DcmDspEcuResetRow

**描述**: This container contains the configuration for each DcmDspEcuReset subservice.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspEcuResetId
  长名称: ''
  描述: |
    Specifies the value of the corresponding sub-service of service 0x11 (EcuReset).
    
    Effect:
    ------------------------------------
    none
    
    Constraints:
    ------------------------------------
    For each EcuReset sub-service, there can be a EcuResetRow.
    
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
  最大值: 127
- 
  序号: 2
  名称: DcmResponseToEcuReset
  长名称: ''
  描述: |
    This parameter defines whether the answer to EcuReset service should be sent before or after the
    reset.
    
    Effect:
    ------------------------------------
    On receiving the corresponding EcuReset sub-service request, the Dcm will send the answer
    depending on the selection.
    
    Constraints:
    ------------------------------------
    This parameter has only an effect, if the corresponding sub-service Id is 0x01, 0x02 or 0x03 and
    it is internally handled.
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    If all of the EcuReset sub-services specify for this parameter "BEFORE_RESET", the Dcm code ROM
    usage will be reduced.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    If all of the EcuReset sub-services specify for this parameter "BEFORE_RESET", the Dcm code RAM
    usage will be reduced.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: BEFORE_RESET
  最小值: ''
  最大值: ''
```

### 44. DcmDspFaultMemory

**描述**: This container contains the configuration for the DCM fault memory related information. This
container exists only if the UDS Service ReadDTCInformation (0x19) is configured.

该容器没有参数。

### 45. DcmDspFaultMemoryUserMemoryIdInfo

**描述**: Specifies the a supported user memory id for services 0x19 0x17,0x18 and 0x19.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspFaultMemoryUserMemoryId
  长名称: ''
  描述: |
    Specifies the a supported user memory id for services 0x19 0x17,0x18 and 0x19.
    
    Effect:
    ------------------------------------
    If specified a user memory identifier, DCM will accept only these user memory IDs that are
    configured here and address the secondary fault memory.
    If no user memory identifier specified, DCM will accept any value in the request, and address
    with it the fault memory.
    
    Constraints:
    ------------------------------------
    -
    
    Dependencies:
    ------------------------------------
    Will be used only if one of the diagnostic services 0x19 0x17,0x18 and 0x19 is to be supported
    by DCM.
    
    Runtime effects:
    ------------------------------------
    If any user memory id specified, the DCM will check any related request upon this value and this
    leads to an insignificantly increased run time usage.
    
    Code ROM usage effects:
    ------------------------------------
    If any user memory id specified, the DCM will check any related request upon this value and this
    leads to an insignificantly increased code ROM usage.
    
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
```

### 46. DcmDspFaultMemoryRecords

**描述**: Specifies all supported fault memory environment data records (extended data and snapshot).
All of the sub-containers here are derived from the detected DEM configuration located in this ECU
project.

Import: If no DEM configuration has been detected, the DCM will respond to all SID 0x19 related
sub-functions with empty report lists.

If no DEM related configuration has been detected or you need to add additional record ranges, you
can change the sub-containers.

该容器没有参数。

### 47. DcmDspFaultMemoryFFRecord

**描述**: Specifies a supported fault memory snapshot record ID range.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspFaultMemoryFFRecordNumberLower
  长名称: ''
  描述: |
    Specifies the first record ID of a range.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the start of a valid record ID range.
    
    Constraints:
    ------------------------------------
    - This value shall be lower or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspFaultMemory/DcmDspFaultMemoryRecords/DcmDspFaultMemoryFFRecord/DcmDspFaultMemoryFFRecordNumberUpper"
    - If a single value is required to be specified, this parameter will specify it. The
    "DcmDspFaultMemoryFFRecordNumberUpper" shall not be used.
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspFaultMemory/DcmDspFaultMemoryRecords/DcmDspFaultMemoryFFRecord/DcmDspFaultMemoryFFRecordNumberUpper"
    
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
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DcmDspFaultMemoryFFRecordNumberUpper
  长名称: ''
  描述: |
    Specifies the last record ID of a range.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the end of a valid record ID range.
    
    Constraints:
    ------------------------------------
    - This value shall be greater or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspFaultMemory/DcmDspFaultMemoryRecords/DcmDspFaultMemoryFFRecord/DcmDspFaultMemoryFFRecordNumberLower"
    - If a single value is required to be specified, this parameter can be removed. Then
    "DcmDspFaultMemoryFFRecordNumberLower" will determine the record ID.
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspFaultMemory/DcmDspFaultMemoryRecords/DcmDspFaultMemoryFFRecord/DcmDspFaultMemoryFFRecordNumberLower"
    
    Runtime effects:
    ------------------------------------
    The run time (number of DEM iterations) usage is proportional to the number of record IDs
    determined by the record ID range.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    The ROM usage is proportional to the number of record IDs determined by the record ID range.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 1
  最小值: 1
  最大值: 255
```

### 48. DcmDspFaultMemoryExtDataRecord

**描述**: Specifies a supported fault memory extended data record ID range.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspFaultMemoryExtDataRecordNumberLower
  长名称: ''
  描述: |
    Specifies the first record ID of a range.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the start of a valid record ID range.
    
    Constraints:
    ------------------------------------
    - This value shall be lower or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspFaultMemory/DcmDspFaultMemoryRecords/DcmDspFaultMemoryFFRecord/DcmDspFaultMemoryFFRecordNumberUpper"
    - If a single value is required to be specified, this parameter will specify it. The
    "DcmDspFaultMemoryFFRecordNumberUpper" shall not be used.
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspFaultMemory/DcmDspFaultMemoryRecords/DcmDspFaultMemoryFFRecord/DcmDspFaultMemoryFFRecordNumberUpper"
    
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
  默认值: 1
  最小值: 0
  最大值: 253
- 
  序号: 2
  名称: DcmDspFaultMemoryExtDataRecordNumberUpper
  长名称: ''
  描述: |
    Specifies the last record ID of a range.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the end of a valid record ID range.
    
    Constraints:
    ------------------------------------
    - This value shall be greater or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspFaultMemory/DcmDspFaultMemoryRecords/DcmDspFaultMemoryFFRecord/DcmDspFaultMemoryFFRecordNumberLower"
    - If a single value is required to be specified, this parameter can be removed. Then
    "DcmDspFaultMemoryFFRecordNumberLower" will determine the record ID.
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspFaultMemory/DcmDspFaultMemoryRecords/DcmDspFaultMemoryFFRecord/DcmDspFaultMemoryFFRecordNumberLower"
    
    Runtime effects:
    ------------------------------------
    The run time (number of DEM iterations) usage is proportional to the number of record IDs
    determined by the record ID range.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    The ROM usage is proportional to the number of record IDs determined by the record ID range.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 1
  最小值: 1
  最大值: 253
```

### 49. DcmDspMemory

**描述**: This container includes all ECU memory area access information

Effect:
------------------------------------
For each memory area that shall be accessible via diagnostics there shall a range defined under this
container.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
This container makes only sense if one of the direct memory access diagnostic services (0x23 or
0x3D) is configured under "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration data ROM usage scales straight proportionally to the number of memory ranges
defined.

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
  名称: DcmDspUseMemoryId
  长名称: ''
  描述: |
    Specifies whether the requested memory access service will contain a memory identifier byte or
    not.
    
    Effect:
    ------------------------------------
    If set to TRUE, DCM will treat the first byte of the requested memory address as a memory
    identifier (MID). If set to FALSE, the whole byte stream specified by the address and length
    format identifier (ALFID) byte will be treated as a physical memory address.
    
    Constraints:
    ------------------------------------
    This setting affects the global view of DCM to the ECU's memory organization. Each diagnostic
    service that uses memory addresses will be affected by this setting.
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x23 or
    0x3D.
    If enabled, the "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspMemoryIdValue"
    must be defined.
    
    Runtime effects:
    ------------------------------------
    No significant run time effects.
    
    Code ROM usage effects:
    ------------------------------------
    Due to the additional MID management, the code ROM usage will slightly increase.
    
    Const data ROM usage effects:
    ------------------------------------
    If enable, the data ROM usage will be slightly increased, but will not scale with the number of
    memory ranges in the ECU.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspMemoryMaxGapSizeBetweenTwoBlocks
  长名称: ''
  描述: |
    Specifies the maximum gap size in bytes between two memory blocks that shall be ignored during
    memory block layout optimization
    
    Effect:
    ------------------------------------
    During the DCM code generation, all memory ranges (blocks) will be optimized for faster lookup
    and low ROM data usage. In this process consecutive ranges (gap size between then is zero) with
    the same properties will be merged to a single memory range. The gap size specified by this
    parameter allows to concatenate memory ranges with some gap bytes in between, which are
    irrelevant and were caused by the CPU data alignment.
    
    Constraints:
    ------------------------------------
    This parameter affects only "Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo"
    containers, which use address values and not labels.
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x23 or
    0x3D.
    
    Runtime effects:
    ------------------------------------
    The bigger the gap the better the chance to merge more blocks together into a single memory
    block. This reduces run time usage of the memory block lookup engine in DCM's code.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    The bigger the gap size the better the chance to have less memory blocks to be described in the
    DCM configuration data tables.
    
    
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

### 50. DcmDspMemoryIdInfo

**描述**: Provides a memory identifier (MID) specific memory map.

Effect:
------------------------------------
For each MID there shall be specified a list of memory ranges for reading and/or writing.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x23 or 0x3D.

Runtime effects:
------------------------------------
The more memory range are specified, the longer the run time needed to validate the diagnostic
memory access request.

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The more ranges you specify the more data ROM could be required to store them in the DCM
configuration. The DCM generator tries to optimize all configured memory ranges into as less as
possible memory areas within the DCM's internal configuration memory layout map.

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
  名称: DcmDspMemoryIdValue
  长名称: ''
  描述: Value of the memory device identifier used. This parameter is only relevant if the memory Id
      parameter use is enabled. (DcmDspUseMemoryId = TRUE)
  默认值: 0
  最小值: 0
  最大值: 255
```

### 51. DcmDspReadMemoryRangeInfo

**描述**: Provides the range of memory address allowed for reading.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspReadMemoryRangeHigh
  长名称: ''
  描述: |
    Specifies the last memory address of a range allowed for reading.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the end of a valid memory range.
    
    Constraints:
    ------------------------------------
    This value shall be greater or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspReadMemoryRangeInfo/DcmDspReadMemoryRangeLow"
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspReadMemoryRangeInfo/DcmDspReadMemoryRangeLow"
    
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
  最大值: 4294967294
- 
  序号: 2
  名称: DcmDspReadMemoryRangeLow
  长名称: ''
  描述: |
    Specifies the first memory address of a range allowed for reading.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the beginning of a valid memory range.
    
    Constraints:
    ------------------------------------
    This value shall be lower or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspReadMemoryRangeInfo/DcmDspReadMemoryRangeHigh"
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspReadMemoryRangeInfo/DcmDspReadMemoryRangeHigh"
    
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
  最大值: 4294967294
```

### 52. DcmDspWriteMemoryRangeInfo

**描述**: Provides the range of memory address allowed for writing.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspWriteMemoryRangeHigh
  长名称: ''
  描述: |
    Specifies the last memory address of a range allowed for writing.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the end of a valid memory range.
    
    Constraints:
    ------------------------------------
    This value shall be greater or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspWriteMemoryRangeInfo/DcmDspWriteMemoryRangeLow"
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspWriteMemoryRangeInfo/DcmDspWriteMemoryRangeLow"
    
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
  最大值: 4294967294
- 
  序号: 2
  名称: DcmDspWriteMemoryRangeLow
  长名称: ''
  描述: |
    Specifies the first memory address of a range allowed for writing.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the beginning of a valid memory range.
    
    Constraints:
    ------------------------------------
    This value shall be lower or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspWriteMemoryRangeInfo/DcmDspWriteMemoryRangeHigh"
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspWriteMemoryRangeInfo/DcmDspWriteMemoryRangeHigh"
    
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
  最大值: 4294967294
```

### 53. DcmDspReadMemoryRangeByLabelInfo

**描述**: Provides a memory range allowed for reading via labels (lower and higher address configured as
strings).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspReadMemoryRangeByLabelHigh
  长名称: ''
  描述: |
    Specifies the last memory address as label (string) of a range allowed for reading.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the end of a valid memory range.
    
    Constraints:
    ------------------------------------
    This value shall be greater or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspReadMemoryRangeByLabelInfo/DcmDspReadMemoryRangeByLabelLow"
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspReadMemoryRangeByLabelInfo/DcmDspReadMemoryRangeByLabelLow"
    
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
  名称: DcmDspReadMemoryRangeByLabelLow
  长名称: ''
  描述: |
    Specifies the first memory address as label (string) of a range allowed for reading.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the beginning of a valid memory range.
    
    Constraints:
    ------------------------------------
    This value shall be lower or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspReadMemoryRangeByLabelInfo/DcmDspReadMemoryRangeByLabelHigh"
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspReadMemoryRangeByLabelInfo/DcmDspReadMemoryRangeByLabelHigh"
    
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
```

### 54. DcmDspWriteMemoryRangeByLabelInfo

**描述**: Provides a memory range allowed for writing via labels (lower and higher address configured as
strings).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspWriteMemoryRangeByLabelHigh
  长名称: ''
  描述: |
    Specifies the last memory address as label (string) of a range allowed for writing.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the end of a valid memory range.
    
    Constraints:
    ------------------------------------
    This value shall be greater or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspWriteMemoryRangeByLabelInfo/DcmDspWriteMemoryRangeByLabelLow"
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspWriteMemoryRangeByLabelInfo/DcmDspWriteMemoryRangeByLabelLow"
    
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
  名称: DcmDspWriteMemoryRangeByLabelLow
  长名称: ''
  描述: |
    Specifies the first memory address as label (string) of a range allowed for writing.
    
    Effect:
    ------------------------------------
    DCM uses this value to determine the beginning of a valid memory range.
    
    Constraints:
    ------------------------------------
    This value shall be lower or equal to the corresponding
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspWriteMemoryRangeByLabelInfo/DcmDspWriteMemoryRangeByLabelHigh"
    
    Dependencies:
    ------------------------------------
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryIdInfo/DcmDspWriteMemoryRangeByLabelInfo/DcmDspWriteMemoryRangeByLabelHigh"
    
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
```

### 55. DcmDspMemoryAddressAndLengthFormatIdentifier

**描述**: Specifies whether only specific ALFID(s) shall only be supported by the ECU or any valid by UDS.

Effect:
------------------------------------
If this container is missing, then DCM will accept any requested ALFID value in the range
[0x11-0x45] (the valid byte nibble values are 1-4 for memory size and address in case of no memory
ID usage and 2-5 for memory address in case memory ID shall be supported!).
If the container persists, DCM will only accept the values specified by the parameters within this
container.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x23 or 0x3D.
You have to specify all valid ALFID values:
"/Dcm/DcmConfigSet/DcmDsp/DcmDspMemory/DcmDspMemoryAddressAndLengthFormatIdentifier/DcmDspMemorySupportedAddressAndLengthFormatIdentifier"

Runtime effects:
------------------------------------
If the container exists, the DCM will use a lookup engine to determine the validity of the requested
ALFID which can increase the run time. If any UDS valid ALFID is to be supported, the DCM run time
at validating a memory access service is constant.

Code ROM usage effects:
------------------------------------
If the container exists, the DCM will use a lookup engine to determine the validity of the requested
ALFID which can increase the code ROM usage insignificantly.

Const data ROM usage effects:
------------------------------------
The data ROM usage scales with the amount of ALFIDs to be supported (1 byte per ALFID).


Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
A slightly increased stack usage may occur due to the fact that the ALFID look up engine runs within
the diagnostic service processor context.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspMemorySupportedAddressAndLengthFormatIdentifier
  长名称: ''
  描述: |
    Specifies a concrete ALFID value to be only supported by the ECU.
    
    Effect:
    ------------------------------------
    The DCM will accept only those ALFIDs of a memory access diagnostic request that are defined by
    this parameter.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x23 or
    0x3D.
    
    Runtime effects:
    ------------------------------------
    The more ALFIDs the longer the run time of the ALFID look up engine in DCM.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    The data ROM usage scales with the amount of ALFIDs to be supported (1 byte per ALFID).
    
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    A slightly increased stack usage may occur due to the fact that the ALFID look up engine runs
    within the diagnostic service processor context.
  默认值: 36
  最小值: 0
  最大值: 255
```

### 56. DcmDspMemoryTransfer

**描述**: This container contains the configuration of the memory transfer.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspMemoryTransferUsePort
  长名称: ''
  描述: |
    Defines which kind of interface shall be used to transfer the data.
    
    Effect:
    ------------------------------------
    If set to TRUE, a RTE call will be required to be implemented in the Dcm application.
    If set to FALSE - a call out will be required to be implemented in the Dcm application.
    
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
    
  默认值: false
  最小值: ''
  最大值: ''
```

### 57. DcmDspMemoryTransferIdInfo

**描述**: Provides a list of memory identifier (MID).

Effect:
------------------------------------
For each MID there shall be specified a list of memory ranges for reading and/or writing.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x34, 0x35,
0x36 or 0x37.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The more ranges you specify the more data ROM could be required to store them in the DCM
configuration. The DCM generator tries to optimize all configured memory ranges into as less as
possible memory areas within the DCM's internal configuration memory layout map.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
noneferExit

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspMemoryIdValue
  长名称: ''
  描述: Value of the memory transfer device identifier used.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 58. DcmDspAddressAndLengthFormatIdentifier

**描述**: Specifies whether only specific ALFID(s) shall only be supported by the ECU or any valid by UDS.

Effect:
------------------------------------
If this container is missing, then DCM will accept any requested ALFID value in the range
[0x11-0x45] (the valid byte nibble values are 1-4 for memory size and address in case of no memory
ID usage and 2-5 for memory address in case memory ID shall be supported!).
If the container exists, DCM will only accept the values specified by the parameters within this
container.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x34, 0x35,
0x36 or 0x37.
Specify all valid ALFID values:
"/Dcm/DcmConfigSet/DcmDsp/DcmDspMemoryTransfer/DcmDspAddressAndLengthFormatIdentifier/DcmDspAddressAndLengthFormatIdentifier"

Runtime effects:
------------------------------------
If the container exists, the DCM will use a lookup engine to determine the validity of the requested
ALFID which can increase the run time. If any UDS valid ALFID is to be supported, the DCM run time
at validating a memory transfer service is constant.

Code ROM usage effects:
------------------------------------
If the container exists, the DCM will use a lookup engine to determine the validity of the requested
ALFID which can increase the code ROM usage insignificantly.

Const data ROM usage effects:
------------------------------------
The data ROM usage scales with the amount of ALFIDs to be supported (1 byte per ALFID).


Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
A slightly increased stack usage may occur due to the fact that the ALFID look up engine runs within
the diagnostic service processor context.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspAddressAndLengthFormatIdentifier
  长名称: ''
  描述: |
    Specifies a concrete ALFID value to be only supported by the ECU.
    
    Effect:
    ------------------------------------
    The DCM will accept only those ALFIDs of a memory transfer diagnostic request that are defined
    by this parameter.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x34,
    0x35, 0x36 or 0x37.
    
    Runtime effects:
    ------------------------------------
    The more ALFIDs the longer the run time of the ALFID look up engine in DCM.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    The data ROM usage scales with the amount of ALFIDs to be supported (1 byte per ALFID).
    
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    A slightly increased stack usage may occur due to the fact that the ALFID look up engine runs
    within the diagnostic service processor context.
  默认值: 36
  最小值: 0
  最大值: 255
```

### 59. DcmDspPeriodicDidTransmission

**描述**: This container contains the configuration for the Periodic DID transmission. This container exists
only if the UDS Service ReadDataByPeriodicIdentifier(0x2A) is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspMaxPeriodicDidScheduler
  长名称: ''
  描述: |
    Defines the maximum number of periodicDataIdentifiers that can be scheduled concurrently.
    
    Effect:
    ------------------------------------
    Any diagnostic request for service 0x2A with DIDs that do not (no more) fit into the scheduler
    table will be rejected by a negative response.
    
    Constraints:
    ------------------------------------
    Has any effect only if service 0x2A is supported.
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x2A.
    
    Runtime effects:
    ------------------------------------
    The larger number of DIDs in the scheduler, the longer the Dcm task execution time, since in the
    worst case (scheduler fully utilized and all DID timers are in timeout) all requested DIDs may
    be processed within the same Dcm task activation.
    
    Code ROM usage effects:
    ------------------------------------
    If more than one DID is specified to be scheduled, the Dcm code usage will increase due to the
    iteration loops.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    The RAM usage can increase with increasing the value of this parameter.
    
    Stack RAM usage effects:
    ------------------------------------
    If more than one DID is specified to be scheduled, the Dcm task stack usage may insignificantly
    increase due to the additional local variables for the iteration loops.
    
  默认值: 5
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: DcmDspPeriodicDidStopOnStateChange
  长名称: Dsp Periodic Did Stop On State Change
  描述: |
    Specifies whether DCM module shall stop a PDID when a session/security level change occurs and
    the PDID is no longer accessible in the new state.
    
    Effect:
    ------------------------------------
    If set to TRUE, DCM will verify whether any scheduled PDID is still accessible under the new DCM
    session/security/mode condition states. If not, it will be removed from the scheduler.
    Note: If the PDID is also a DDID, then it will depend on
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspDDDidCheckPerSourceDid" whether only the DDID configured
    execution preconditions will only be considered or its content too.
    
    If set to FALSE, DCM will not automatically stop any affected PDID transmission. This saves
    resources (ROM, stack, run-time), but can be a security backdoor.
    
    Note: If option "/Dcm/DcmConfigSet/DcmDsp/DcmDspDDDidClearOnStateChange" is enabled, then any
    PDID that is also a DDID, will be removed from the scheduler independently of the state of this
    parameter.
    
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x2A.
    The "/Dcm/DcmConfigSet/DcmDsp/DcmDspPeriodicDidTransmission/DcmDspMaxPeriodicDidScheduler"
    parameter determines the run time usage.
    
    Runtime effects:
    ------------------------------------
    The larger number of simultaneously scheduled PDIDs, the longer the Dcm task execution time,
    since all contained sources will be processed within the same Dcm task activation.
    
    Code ROM usage effects:
    ------------------------------------
    If set to TRUE, the code usage will increase by a constant amount, independent of the number of
    number of PDIDs or their number of sources.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    If set to TRUE, the stack usage will be increased slightly due to the additional checks
    performed in the context of an ongoing diagnostic service processor. The more complex and deep
    mode rule condition expression nesting, the more stack will be needed.
  默认值: false
  最小值: ''
  最大值: ''
```

### 60. DcmDspPeriodicTransmission

**描述**: This container contains the configuration (parameters) for Periodic Transmission Processing.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspPeriodicTransmissionSlowRate
  长名称: ''
  描述: |
    This parameter give the transmission rate of the requested periodicDataIdentifiers to be used if
    the parameter transmissionMode given in the ReadDataByPeriodicID request is equal to 0x01
    ("sendAtSlowRate").
    
    Effect:
    ------------------------------------
    If the parameter is missing or its value is zero: this scheduling rate will not be supported in
    service 0x2A (ReadDataByPeriodicID).
    
    If the parameter value is > 0:
    If periodic DID is scheduled with the rate this parameter defines, the DCM will send a periodic
    response message for this DID at least with the period of this time parameter. The transmission
    can be slowed down due to different reasons, like high bus load, scheduler overload (too many
    DIDs to be processed and responded over the same response message).
    
    
    Constraints:
    ------------------------------------
    This parameter value in seconds have to be configured as a multiple of DcmTaskTime.
    
    Dependencies:
    ------------------------------------
    Refer to: "/Dcm/DcmConfigSet/DcmGeneral/DcmTaskTime".
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    If this is the only scheduling rate to be supported, the Dcm code usage for service 0x2A will be
    significantly reduced.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    If this is the only scheduling rate to be supported, the Dcm RAM usage for service 0x2A will be
    slightly reduced.
    
    Stack RAM usage effects:
    ------------------------------------
    If this is the only scheduling rate to be supported, the Dcm RAM usage for service 0x2A may be
    slightly reduced.
  默认值: 1
  最小值: 0
  最大值: 1000
- 
  序号: 2
  名称: DcmDspPeriodicTransmissionMediumRate
  长名称: ''
  描述: |
    This parameter give the transmission rate of the requested periodicDataIdentifiers to be used if
    the parameter transmissionMode given in the ReadDataByPeriodicID request is equal to 0x02
    ("sendAtMediumRate").
    
    Effect:
    ------------------------------------
    If the parameter is missing or its value is zero: this scheduling rate will not be supported in
    service 0x2A (ReadDataByPeriodicID).
    
    If the parameter value is > 0:
    If periodic DID is scheduled with the rate this parameter defines, the DCM will send a periodic
    response message for this DID at least with the period of this time parameter. The transmission
    can be slowed down due to different reasons, like high bus load, scheduler overload (too many
    DIDs to be processed and responded over the same response message).
    
    
    Constraints:
    ------------------------------------
    This parameter value in seconds have to be configured as a multiple of DcmTaskTime.
    
    Dependencies:
    ------------------------------------
    Refer to: "/Dcm/DcmConfigSet/DcmGeneral/DcmTaskTime".
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    If this is the only scheduling rate to be supported, the Dcm code usage for service 0x2A will be
    significantly reduced.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    If this is the only scheduling rate to be supported, the Dcm RAM usage for service 0x2A will be
    slightly reduced.
    
    Stack RAM usage effects:
    ------------------------------------
    If this is the only scheduling rate to be supported, the Dcm RAM usage for service 0x2A may be
    slightly reduced.
  默认值: 0.1
  最小值: 0
  最大值: 1000
- 
  序号: 3
  名称: DcmDspPeriodicTransmissionFastRate
  长名称: ''
  描述: |
    This parameter give the transmission rate of the requested periodicDataIdentifiers to be used if
    the parameter transmissionMode given in the ReadDataByPeriodicID request is equal to 0x03
    ("sendAtFastRate").
    
    Effect:
    ------------------------------------
    If the parameter is missing or its value is zero: this scheduling rate will not be supported in
    service 0x2A (ReadDataByPeriodicID).
    
    If the parameter value is > 0:
    If periodic DID is scheduled with the rate this parameter defines, the DCM will send a periodic
    response message for this DID at least with the period of this time parameter. The transmission
    can be slowed down due to different reasons, like high bus load, scheduler overload (too many
    DIDs to be processed and responded over the same response message).
    
    
    Constraints:
    ------------------------------------
    This parameter value in seconds have to be configured as a multiple of DcmTaskTime.
    
    Dependencies:
    ------------------------------------
    Refer to: "/Dcm/DcmConfigSet/DcmGeneral/DcmTaskTime".
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    If this is the only scheduling rate to be supported, the Dcm code usage for service 0x2A will be
    significantly reduced.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    If this is the only scheduling rate to be supported, the Dcm RAM usage for service 0x2A will be
    slightly reduced.
    
    Stack RAM usage effects:
    ------------------------------------
    If this is the only scheduling rate to be supported, the Dcm RAM usage for service 0x2A may be
    slightly reduced.
  默认值: 0.05
  最小值: 0
  最大值: 1000
- 
  序号: 4
  名称: DcmDspPeriodicTransmissionDelaySlowRate
  长名称: ''
  描述: |
    This parameter specifies the time in which at most two periodic messages can be sent when the
    fastest transmissionMode given in any active ReadDataByPeriodicID request is equal to 0x01
    ("sendAtSlowRate").
    
    Effect:
    ------------------------------------
    If the parameter is missing or its value is zero: the periodic responses of service 0x2A are
    sent as soon as possible.
    
    If the parameter value is > 0:
    If the fastest scheduled periodic DID is to be sent at "Slow Rate", at most two periodic
    response messages are sent within the delay time configured by this parameter.
    
    Constraints:
    ------------------------------------
    This parameter value is in seconds and has to be configured as a multiple of DcmTaskTime. It is
    effective only if DcmDspPeriodicTransmissionSlowRate is > 0.
    
    Dependencies:
    ------------------------------------
    Refer to:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspPeriodicTransmission/DcmDspPeriodicTransmissionSlowRate",
    "/Dcm/DcmConfigSet/DcmGeneral/DcmTaskTime".
    Additionally, if applicable:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspPeriodicTransmission/DcmDspPeriodicTransmissionDelayMediumRate"
    and
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspPeriodicTransmission/DcmDspPeriodicTransmissionDelayFastRate".
    
    Runtime effects:
    ------------------------------------
    Due to the additional management code required for this feature, the runtime will increase
    slightly.
    
    Code ROM usage effects:
    ------------------------------------
    Due to the additional management code required for this feature, the code ROM usage will
    increase.
    
    Const data ROM usage effects:
    ------------------------------------
    Due to the additional parameters required for this feature, the data ROM usage will increase
    insignificantly.
    
    Global RAM usage effects:
    ------------------------------------
    Due to the additional timers required for this feature, the global RAM usage will increase
    insignificantly.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 1
  最小值: 0
  最大值: 1000
- 
  序号: 5
  名称: DcmDspPeriodicTransmissionDelayMediumRate
  长名称: ''
  描述: |
    This parameter specifies the time in which at most two periodic messages can be sent when the
    fastest transmissionMode given in any active ReadDataByPeriodicID request is equal to 0x02
    ("sendAtMediumRate").
    
    Effect:
    ------------------------------------
    If the parameter is missing or its value is zero: the periodic responses of service 0x2A are
    sent as soon as possible.
    
    If the parameter value is > 0:
    If the fastest scheduled periodic DID is to be sent at "Medium Rate", at most two periodic
    response messages are sent within the delay time configured by this parameter.
    
    Constraints:
    ------------------------------------
    This parameter value is in seconds and has to be configured as a multiple of DcmTaskTime. It is
    effective only if DcmDspPeriodicTransmissionMediumRate is > 0.
    
    Dependencies:
    ------------------------------------
    Refer to:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspPeriodicTransmission/DcmDspPeriodicTransmissionMediumRate",
    "/Dcm/DcmConfigSet/DcmGeneral/DcmTaskTime".
    Additionally, if applicable:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspPeriodicTransmission/DcmDspPeriodicTransmissionDelaySlowRate"
    and
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspPeriodicTransmission/DcmDspPeriodicTransmissionDelayFastRate".
    
    Runtime effects:
    ------------------------------------
    Due to the additional management code required for this feature, the runtime will increase
    slightly.
    
    Code ROM usage effects:
    ------------------------------------
    Due to the additional management code required for this feature, the code ROM usage will
    increase.
    
    Const data ROM usage effects:
    ------------------------------------
    Due to the additional parameters required for this feature, the data ROM usage will increase
    insignificantly.
    
    Global RAM usage effects:
    ------------------------------------
    Due to the additional timers required for this feature, the global RAM usage will increase
    insignificantly.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0.1
  最小值: 0
  最大值: 1000
- 
  序号: 6
  名称: DcmDspPeriodicTransmissionDelayFastRate
  长名称: ''
  描述: |
    This parameter specifies the time in which at most two periodic messages can be sent when the
    fastest transmissionMode given in any active ReadDataByPeriodicID request is equal to 0x03
    ("sendAtFastRate").
    
    Effect:
    ------------------------------------
    If the parameter is missing or its value is zero: the periodic responses of service 0x2A are
    sent as soon as possible.
    
    If the parameter value is > 0:
    If the fastest scheduled periodic DID is to be sent at "Fast Rate", at most two periodic
    response messages are sent within the delay time configured by this parameter.
    
    Constraints:
    ------------------------------------
    This parameter value is in seconds and has to be configured as a multiple of DcmTaskTime. It is
    effective only if DcmDspPeriodicTransmissionFastRate is > 0.
    
    Dependencies:
    ------------------------------------
    Refer to:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspPeriodicTransmission/DcmDspPeriodicTransmissionFastRate",
    "/Dcm/DcmConfigSet/DcmGeneral/DcmTaskTime".
    Additionally, if applicable:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspPeriodicTransmission/DcmDspPeriodicTransmissionDelaySlowRate"
    and
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspPeriodicTransmission/DcmDspPeriodicTransmissionDelayMediumRate".
    
    Runtime effects:
    ------------------------------------
    Due to the additional management code required for this feature, the runtime will increase
    slightly.
    
    Code ROM usage effects:
    ------------------------------------
    Due to the additional management code required for this feature, the code ROM usage will
    increase.
    
    Const data ROM usage effects:
    ------------------------------------
    Due to the additional parameters required for this feature, the data ROM usage will increase
    insignificantly.
    
    Global RAM usage effects:
    ------------------------------------
    Due to the additional timers required for this feature, the global RAM usage will increase
    insignificantly.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0.05
  最小值: 0
  最大值: 1000
```

### 61. DcmDspPid

**描述**: This container defines the availability of a PID to the DCM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspPidIdentifier
  长名称: ''
  描述: |
    Specifies the identifier value of a PID.
    
    Effect:
    ------------------------------------
    The Dcm only recognizes PIDs with the value specified in this parameter.
    
    Constraints:
    ------------------------------------
    The PID value must be unique within a DcmConfigset.
    
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
  最大值: 255
- 
  序号: 2
  名称: DcmDspPidService
  长名称: ''
  描述: Allow to indicate if this PID is used for service $01 or/and $02.
  默认值: DCM_SERVICE_01
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspPidSize
  长名称: ''
  描述: |
    NOT USED
    
    The PID size is defined by the DcmDspPidDataSize as long as the whole PID data is provided
    through a single DcmDspPidData element.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: DcmDspPidUsed
  长名称: ''
  描述: |
    Allows to activate or deactivate the usage of a PID, for multi  purpose ECUs.
    In a single configurations the parameter can be used to temporarily disable a complete PID in
    the Dcm configuration without the need to delete all its configuration parameters.
    
    Effect:
    ------------------------------------
    If set to FALSE, the PID and all its signals will not be used in the Dcm generated code.
    
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
    If set to FALSE, no data ROM for this PID will be used in the Dcm configuration sources.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
    
  默认值: true
  最小值: ''
  最大值: ''
```

### 62. DcmDspPidData

**描述**: This container defines the parameter for a Signal in the PID.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspPidDataPos
  长名称: ''
  描述: |
    Specifies the position of the signal in the PID in bytes.
    
    Effect:
    ------------------------------------
    Affects the call out/service call function calling order.
    
    Constraints:
    ------------------------------------
    Shall be always zero, since only single data object configurations are supported.
    
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
  最大值: 0
- 
  序号: 2
  名称: DcmDspPidDataSize
  长名称: ''
  描述: |
    Specifies the length of PID data in bits.
    
    Effect:
    ------------------------------------
    The sum of all data object lengths of a PID specifies the total PID length which will be used
    for response composition.
    
    Constraints:
    ------------------------------------
    The size shall always be a multiple of 8 (byte borders).
    
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
    
  默认值: 65535
  最小值: 0
  最大值: 524280
```

### 63. DcmDspPidDataSupportInfo

**描述**: NOT USED

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspPidDataSupportInfoBit
  长名称: ''
  描述: referenced Bit of the SupportInfo
  默认值: ''
  最小值: 0
  最大值: 255
```

### 64. DcmDspPidService01

**描述**: Contains specific configuration parameter of PID for service $01. This container exists only if
DcmDspPidService is set to DCM_SERVICE_01 or DCM_SERVICE_01_02.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspPidDataReadFnc
  长名称: ''
  描述: |
    Specifies the call out function name for reading the data object content.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on PID reading
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x01 (RequestCurrentDowertrainDiagnosticData) is supported by Dcm
    (refer to /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspPid/DcmDspPidData/DcmDspPidService01/DcmDspPidDataUsePort)
    
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
  名称: DcmDspPidDataUsePort
  长名称: ''
  描述: |
    Defines which kind of interface shall be used to access the data.
    
    Effect:
    ------------------------------------
    Depending on the selected type, either a RTE call or a call out will be required to be
    implemented in the Dcm application.
    
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
    
  默认值: USE_DATA_SYNCH_CLIENT_SERVER
  最小值: ''
  最大值: ''
```

### 65. DcmDspPidService02

**描述**: NOT USED

该容器没有参数。

### 66. DcmDspPidSupportInfo

**描述**: NOT USED

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspPidSupportInfoLen
  长名称: ''
  描述: Length of the supported information in bytes.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DcmDspPidSupportInfoPos
  长名称: ''
  描述: Position of the supported information in bytes.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 67. DcmDspRequestControl

**描述**: This container contains the configuration (parameters) of the "Request control of on-board system,
test or component" service (Service $08).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRequestControlInBufferSize
  长名称: ''
  描述: |
    Specifies the request length of TID data in bytes.
    
    Effect:
    ------------------------------------
    The value of this parameter will be used to validated the request length.
    
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
  最大值: 4294967295
- 
  序号: 2
  名称: DcmDspRequestControlOutBufferSize
  长名称: ''
  描述: |
    Specifies the response length of TID data in bytes.
    
    Effect:
    ------------------------------------
    The value of this parameter will be used to compose the response length.
    
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
  最大值: 4294967295
- 
  序号: 3
  名称: DcmDspRequestControlTestId
  长名称: ''
  描述: |
    Specifies the identifier value of a TID.
    
    Effect:
    ------------------------------------
    The Dcm only recognizes TIDs with the value specified in this parameter.
    
    Constraints:
    ------------------------------------
    The TID value must be unique within a DcmConfigset.
    
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
  最大值: 255
- 
  序号: 4
  名称: DcmDspRequestControlFnc
  长名称: ''
  描述: |
    Specifies the call out function name for control.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on TID reading
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x08 (RequestControlOfOnBoardDevice) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspRequestControl/DcmDspRequestControlUsePort)
    
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
  序号: 5
  名称: DcmDspRequestControlUsePort
  长名称: ''
  描述: |
    Defines which kind of interface shall be used to control.
    
    Effect:
    ------------------------------------
    If set to TRUE, a RTE call will be required to be implemented in the Dcm application.
    If set to FALSE - a call out will be required to be implemented in the Dcm application.
    
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
    
  默认值: true
  最小值: ''
  最大值: ''
```

### 68. DcmDspRoe

**描述**: Provide the configuration of the ResponseOnEvent mechanism.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoeBufSize
  长名称: ''
  描述: NOT USED
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DcmDspRoeInitFnc
  长名称: ''
  描述: NOT USED
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspRoeInitOnDSC
  长名称: ''
  描述: |
    Specifies whether the RoE shall be deactivated on each diagnostic session transition: either
    caused by reception of SID 0x10 (DiagnosticSessionControl) or S3 timeout.
    
    Effect:
    ------------------------------------
    If set to TRUE, an activated RoE will be deactivated on each diagnostic session transition.
    If set to FALSE diagnostic session transitions will not affect any running RoE task.
    
    
    Constraints:
    ------------------------------------
    Supported only for some OEMs. Refer to the DCM technical reference to see whether this setting
    is supported for your project.
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x86 (ResponseOnEvent) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    
    Runtime effects:
    ------------------------------------
    Since this feature activates additional functionality implemented in DCM, the runtime usage will
    slightly increase on any diagnostic session transition.
    
    Code ROM usage effects:
    ------------------------------------
    Since this feature activates additional functionality implemented in DCM, the code usage will
    slightly increase.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspRoeInterMessageTime
  长名称: ''
  描述: |
    Specifies the minimum time period in seconds in which the RoE responses will be sent.
    
    Effect:
    ------------------------------------
    This parameter is used for both:
    - RoE response message intermediate time;
    and
    - DEM polling rate time for monitoring changed number of DTCs for "onDtcStatusChange" event
    type.
    
    Constraints:
    ------------------------------------
    Supported only for some OEMs. Refer to the DCM technical reference to see whether this setting
    is supported for your project.
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x86 (ResponseOnEvent) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    
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
  最大值: 5
- 
  序号: 5
  名称: DcmDspRoeMaxEventLength
  长名称: ''
  描述: NOT USED
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: DcmDspRoeMaxNumberOfRetry
  长名称: ''
  描述: NOT USED
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: DcmDspRoeMaxQueueLength
  长名称: ''
  描述: NOT USED
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 8
  名称: DcmDspRoeQueueEnabled
  长名称: ''
  描述: NOT USED
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DcmDspRoeStopFnc
  长名称: ''
  描述: NOT USED
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DcmDspRoeSTRTMaxLength
  长名称: ''
  描述: NOT USED
  默认值: 3
  最小值: 1
  最大值: 65535
- 
  序号: 11
  名称: DcmDspRoeSchedulerRate
  长名称: ''
  描述: |
    Specifies the call rate of the periodic scheduler in ms to compare the values of the Dids or to
    detect DTC status changes.
    
    Effect:
    ------------------------------------
    Polling rate time for monitoring Dids or changed number of DTCs to trigger an event when the
    conditions met.
    
    Constraints:
    ------------------------------------
    The "periodic RoE scheduler" feature is only available and/or mandatory for certain customers.
    For all others this option will not have any effect.
    Please refer to the technical reference to find out whether this option is applicable for your
    project or not (if not documented).
    
    This parameter value in milliseconds has to be configured as a multiple of DcmTaskTime.
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x86 (ResponseOnEvent) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    
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
  默认值: 0.01
  最小值: 0
  最大值: 1000
- 
  序号: 12
  名称: DcmDspRoeMaxSupportedDidLength
  长名称: ''
  描述: |
    Specifies the maximum number of measurable data bytes allowed for each DID that is used for
    subfunction onChangeOfDataIdentifier(0x03) or onComparisonOfValues (0x07).
    
    Effect:
    ------------------------------------
    Maximum legth of a DID that can be stored.
    
    Constraints:
    ------------------------------------
    This parameter is only available and/or mandatory for certain customers. For all others this
    option will not have any effect.
    Please refer to the technical reference to find out whether this option is applicable for your
    project or not (if not documented).
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x86 (ResponseOnEvent) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    
    Runtime effects:
    ------------------------------------
    Increased runtime depending on the configured DID length.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    Increased RAM usage depending on the configured DID length.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 13
  名称: DcmDspRoeMaxNumChangeOfDidEvents
  长名称: ''
  描述: |
    Specifies the maximum number of events that can be simultaneously configured with subfunction
    onChangeOfDataIdentifier (0x03).
    
    Effect:
    ------------------------------------
    Number of events that can be monitored at a time.
    
    Constraints:
    ------------------------------------
    This parameter is only available and/or mandatory for certain customers. For all others this
    option will not have any effect.
    Please refer to the technical reference to find out whether this option is applicable for your
    project or not (if not documented).
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x86 (ResponseOnEvent) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    
    Runtime effects:
    ------------------------------------
    Increased runtime depending on the number of events configured.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    Increased RAM usage depending on the number of events configured.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 14
  名称: DcmDspRoeMaxNumComparisonOfValueEvents
  长名称: ''
  描述: |
    Specifies the maximum number of events that can be simultaneously configured with subfunction
    onComparisonOfValues (0x07).
    
    Effect:
    ------------------------------------
    Number of events that can be monitored at a time.
    
    Constraints:
    ------------------------------------
    This parameter is only available and/or mandatory for certain customers. For all others this
    option will not have any effect.
    Please refer to the technical reference to find out whether this option is applicable for your
    project or not (if not documented).
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x86 (ResponseOnEvent) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    
    Runtime effects:
    ------------------------------------
    Increased runtime depending on the number of events configured.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    Increased RAM usage depending on the number of events configured.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 15
  名称: DcmDspRoeMaxNumStoredDTCStatusChangedEvents
  长名称: ''
  描述: |
    Specifies the event queue size for subfunction reportDTCRecordInformationOnDtcStatusChange
    (0x09).
    
    Effect:
    ------------------------------------
    Number of DTC status change events which can be queued.
    
    Constraints:
    ------------------------------------
    This parameter is only available and/or mandatory for certain customers. For all others this
    option will not have any effect.
    Please refer to the technical reference to find out whether this option is applicable for your
    project or not (if not documented).
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x86 (ResponseOnEvent) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    
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
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 16
  名称: DcmDspRoeStorageStateStoreEventEnabled
  长名称: ''
  描述: |
    Specifies whether the storeEvent for subfunction 0x05 (startResponseOnEvent) of service 0x86 is
    supported or not.
    
    Effect:
    ------------------------------------
    If set to TRUE, the subfunction 0x05 with storeEvent set is allowed.
    If set to FALSE, the subfunction 0x05 with storeEvent set will be rejected with a NRC.
    
    
    Constraints:
    ------------------------------------
    Supported only for some OEMs. Refer to the DCM technical reference to see whether this setting
    is supported for your project.
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x86 (ResponseOnEvent) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    
    Runtime effects:
    ------------------------------------
    Since this feature activates additional functionality implemented in DCM, the runtime usage will
    slightly increase.
    
    Code ROM usage effects:
    ------------------------------------
    Since this feature activates additional functionality implemented in DCM, the code usage will
    slightly increase.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
```

### 69. DcmDspRoeEvent

**描述**: This container contains a list of all supported Roe eventTypeRecords which are accepted by this ECU.
At most one DcmDspRoeEvent container is allowed to define a DcmDspRoeEventProperties container with
the choice DcmDspRoeOnDTCStatusChange.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoeEventId
  长名称: ''
  描述: |
    Specifies the EventId for a global identification of this ROE event.
    
    Effect:
    ------------------------------------
    The EventId is used within APIs Dcm_TriggerOnEvent() and the ModeDeclarationGroup.
    
    Constraints:
    ------------------------------------
    Supported only for some OEMs. Refer to the DCM technical reference to see whether this setting
    is supported for your project.
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    -  the diagnostic service 0x86 (ResponseOnEvent) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    - AR 4.2.1 RoE API is licensed
    
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
  最大值: 254
```

### 70. DcmDspRoeOnChangeOfDataIdentifier

**描述**: This container contains configuration of a eventTypeRecord onChangeOfDataIdentifier accepted by this
ECU.

该容器没有参数。

### 71. DcmDspRoeOnDTCStatusChange

**描述**: This container contains configuration of aeventTypeRecord onDTCStatusChange accepted by  this ECU.

Please note that currently are no additional parameters for DcmDspRoeOnDTCStatusChange are defined.
Therefore the existence of the container denotes the choice.

该容器没有参数。

### 72. DcmDspRoeEventWindowTime

**描述**: This container configures the available EventWindowTime in this ECU.
This container contains a sub-set of EventWindowTimes supported by the
Dcm, to limit the ECU resources.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoeEventWindowTime
  长名称: ''
  描述: |
    Specifies the value of the EventWindowTime.
    
    Effect:
    ------------------------------------
    If a RoE request is received with a EWT value not specified here, DCM will reject it with NRC
    0x31.
    
    Constraints:
    ------------------------------------
    Supported only for some OEMs. Refer to the DCM technical reference to see whether this setting
    is supported for your project.
    
    Dependencies:
    ------------------------------------
    Has effect only if the diagnostic service 0x86 (ResponseOnEvent) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService).
    
    Runtime effects:
    ------------------------------------
    Depending on the defined count of EWT to be supported a RoE service request can take
    insignificantly longer time.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    Depending on the defined count of EWT to be supported, the used amount of ROM data will
    insignificantly change.
    
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: ''
  最小值: ''
  最大值: ''
```

### 73. DcmDspRoutine

**描述**: This container contains the configuration (parameters) for Routines.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRequestResultsRoutineFnc
  长名称: ''
  描述: |
    Specifies the call out function name for requesting RID results.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on RID request results
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x31 (RoutineControlByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the RID supports the operation request routine results (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspRoutine/DcmDspRequestResultsRoutineSupported)
    - the DcmDspRoutineUsePort is set to FALSE (i.e. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspRoutine/DcmDspRoutineUsePort)
    
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
  名称: DcmDspRequestResultsRoutineSupported
  长名称: ''
  描述: |
    Specifies whether the RID shall support request result operation.
    
    Effect:
    ------------------------------------
    If set to TRUE, Dcm will accept a request result operation request on this RID. Otherwise, the
    Dcm will reject the request with a NRC 0x12 (SubFunctionNotSupported).
    
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
    If set to TRUE, the Dcm configuration data ROM usage will increase due to the additional data to
    be hold for this operation.
    
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
  序号: 3
  名称: DcmDspRoutineFixedLength
  长名称: ''
  描述: |
    NOT USED
    
    Instead,  the corresponding routine operation request/response data type specifies whether a
    signal has fixed/variable length.
    Example:
    /Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/DcmDspRoutineRequestResOut/DcmDspRoutineRequestResOutSignal/DcmDspRoutineSignalType
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspRoutineIdentifier
  长名称: ''
  描述: 2 bytes Identifier of the RID
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: DcmDspRoutineUsePort
  长名称: ''
  描述: If this parameter is set to true, the DCM uses a port requiring a PortInterface
      RoutineServices_<ROUTINENAME>.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DcmDspRoutineUsed
  长名称: ''
  描述: |
    Allow to activate or deactivate the usage of a Routine, for multi  purpose ECUs
    In a single configurations the parameter can be used to temporarily disable a complete RID in
    the Dcm configuration without the need to delete all its configuration parameters.
    
    Effect:
    ------------------------------------
    If set to FALSE, the RID and all its signals will not be used in the Dcm generated code.
    
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
    If set to FALSE, no data ROM for this RID will be used in the Dcm configuration sources.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DcmDspStartRoutineFnc
  长名称: ''
  描述: |
    Specifies the call out function name for starting a RID.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on RID start diagnostic
    request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x31 (RoutineControlByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DcmDspRoutineUsePort is set to FALSE (i.e. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspRoutine/DcmDspRoutineUsePort)
    
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
  序号: 8
  名称: DcmDspStopRoutineFnc
  长名称: ''
  描述: |
    Specifies the call out function name for stopping a RID.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on RID stop diagnostic
    request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x31 (RoutineControlByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the RID supports the operation request routine results (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspRoutine/DcmDspStopRoutineSupported)
    - the DcmDspRoutineUsePort is set to FALSE (i.e. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspRoutine/DcmDspRoutineUsePort)
    
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
  序号: 9
  名称: DcmDspStopRoutineSupported
  长名称: ''
  描述: |
    Specifies whether the RID shall support stop operation.
    
    Effect:
    ------------------------------------
    If set to TRUE, Dcm will accept a stop operation request on this RID. Otherwise, the Dcm will
    reject the request with a NRC 0x12 (SubFunctionNotSupported).
    
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
    If set to TRUE, the Dcm configuration data ROM usage will increase due to the additional data to
    be hold for this operation.
    
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
  序号: 10
  名称: DcmDspRoutineInfoByte
  长名称: ''
  描述: |
    Manufacturer specific value reported to the tester for the record identifiers. (OBD use cases)
    
    Effect:
    ------------------------------------
    If this parameter exists, DCM will report it automatically to the client, without the need of
    application intervention.
    If this parameter does not exist (default), the application shall provide the RIB value if
    needed.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    If exists, the additional byte copy functionality will insignificantly increase the DCM run time
    usage.
    
    Code ROM usage effects:
    ------------------------------------
    If exists, the additional byte copy functionality will insignificantly increase the DCM code ROM
    usage.
    
    
    Const data ROM usage effects:
    ------------------------------------
    If exists, the additional configuration data is stored to each routine identifier which will
    slightly increase the const data ROM usage.
    
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: DcmDspStopRoutineInterfaceArgumentIntegrity
  长名称: ''
  描述: |
    If this parameter is set to TRUE, the integrity of the stop routine operation parameters is
    ensured.
    
    Effect:
    ------------------------------------
    Defines the value of ClientServerOperation.diagArgIntegrity for the created C/S interface
    respectively the callout function of the stop routine operation.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x31 (RoutineControlByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    
    Runtime effects:
    ------------------------------------
    Enabling this feature will slightly increase the Dcm task time during the stop routine operation
    due to the parameter copying.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    Enabling this feature leads to an increase of the Dcm static code RAM usage (depending on the
    size of the stop routine operation parameters).
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: DcmDspStartRoutineInterfaceArgumentIntegrity
  长名称: ''
  描述: |
    If this parameter is set to TRUE, the integrity of the start routine operation parameters is
    ensured.
    
    Effect:
    ------------------------------------
    Defines the value of ClientServerOperation.diagArgIntegrity for the created C/S interface
    respectively the callout function of the start routine operation.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x31 (RoutineControlByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    
    Runtime effects:
    ------------------------------------
    Enabling this feature will slightly increase the Dcm task time during the start routine
    operation due to the parameter copying.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    Enabling this feature leads to an increase of the Dcm static code RAM usage (depending on the
    size of the start routine operation parameters).
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: DcmDspRequestResultsRoutineInterfaceArgumentIntegrity
  长名称: ''
  描述: |
    If this parameter is set to TRUE, the integrity of the request result routine operation
    parameters is ensured.
    
    Effect:
    ------------------------------------
    Defines the value of ClientServerOperation.diagArgIntegrity for the created C/S interface
    respectively the callout function of the request result routine operation.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x31 (RoutineControlByIdentifier) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    
    Runtime effects:
    ------------------------------------
    Enabling this feature will slightly increase the Dcm task time during the request result routine
    operation due to the parameter copying.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    Enabling this feature leads to an increase of the Dcm static code RAM usage (depending on the
    size of the request result routine operation parameters).
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
```

### 74. DcmDspRoutineInfo

**描述**: This container contains the configuration (parameters) for Routine's Info.

该容器没有参数。

### 75. DcmDspStartRoutineIn

**描述**: Provide description of input parameter of Start sub-service for RoutineControl service

该容器没有参数。

### 76. DcmDspStartRoutineInSignal

**描述**: Provide description of a routine signal used in RoutineControl service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoutineSignalLength
  长名称: ''
  描述: |
    Specifies the length of RID data in bits. If Data has variable data length, this parameter
    specifies the maximum data length.
    
    Effect:
    ------------------------------------
    The sum of all data object lengths of a RID operation specifies the total RID operation length
    which will be validated at request reception resp. used for response composition.
    
    Constraints:
    ------------------------------------
    The size shall always be a multiple of 8 (byte borders).
    
    Dependencies:
    ------------------------------------
    The size parameter is either the concrete or maximum data object size, depending on the
    corresponding  DcmDspRoutineSignalType parameter value (refer to
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalType").
    
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
  默认值: 65535
  最小值: 1
  最大值: 524280
- 
  序号: 2
  名称: DcmDspRoutineSignalPos
  长名称: ''
  描述: |
    Specifies the position of the signal in the RID request/response.
    
    Effect:
    ------------------------------------
    Affects the call out/service call function signature.
    
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
  最大值: 524280
- 
  序号: 3
  名称: DcmDspRoutineSignalType
  长名称: ''
  描述: |
    Specifies whether the data object has a constant (fixed) or variable length.
    
    Effect:
    ------------------------------------
    If set to other value than VARIABLE_LENGTH, the Dcm will use the data length parameter value of
    a data object directly from the configuration. Otherwise, the Dcm will gather the concrete
    length from the application.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Affects the interpretation of the corresponding DcmDspRoutineSignalLength parameter:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalLength".
    
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
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspRoutineSignalEndianness
  长名称: ''
  描述: Defines the endianness for all this routine signal.
  默认值: OPAQUE
  最小值: ''
  最大值: ''
```

### 77. DcmDspStartRoutineOut

**描述**: Provide description of output parameter of Start sub-service for RoutineControl service.

该容器没有参数。

### 78. DcmDspStartRoutineOutSignal

**描述**: Provide description of a routine signal used in RoutineControl service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoutineSignalLength
  长名称: ''
  描述: |
    Specifies the length of RID data in bits. If Data has variable data length, this parameter
    specifies the maximum data length.
    
    Effect:
    ------------------------------------
    The sum of all data object lengths of a RID operation specifies the total RID operation length
    which will be validated at request reception resp. used for response composition.
    
    Constraints:
    ------------------------------------
    The size shall always be a multiple of 8 (byte borders).
    
    Dependencies:
    ------------------------------------
    The size parameter is either the concrete or maximum data object size, depending on the
    corresponding  DcmDspRoutineSignalType parameter value (refer to
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalType").
    
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
  默认值: 65535
  最小值: 1
  最大值: 524280
- 
  序号: 2
  名称: DcmDspRoutineSignalPos
  长名称: ''
  描述: |
    Specifies the position of the signal in the RID request/response.
    
    Effect:
    ------------------------------------
    Affects the call out/service call function signature.
    
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
  最大值: 524280
- 
  序号: 3
  名称: DcmDspRoutineSignalType
  长名称: ''
  描述: |
    Specifies whether the data object has a constant (fixed) or variable length.
    
    Effect:
    ------------------------------------
    If set to other value than VARIABLE_LENGTH, the Dcm will use the data length parameter value of
    a data object directly from the configuration. Otherwise, the Dcm will gather the concrete
    length from the application.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Affects the interpretation of the corresponding DcmDspRoutineSignalLength parameter:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalLength".
    
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
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspRoutineSignalEndianness
  长名称: ''
  描述: Defines the endianness for all this routine signal.
  默认值: OPAQUE
  最小值: ''
  最大值: ''
```

### 79. DcmDspRoutineStopIn

**描述**: Provide description of input parameter of Stop sub-service for RoutineControl service.

该容器没有参数。

### 80. DcmDspRoutineStopInSignal

**描述**: Provide description of a routine signal used in RoutineControl service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoutineSignalLength
  长名称: ''
  描述: |
    Specifies the length of RID data in bits. If Data has variable data length, this parameter
    specifies the maximum data length.
    
    Effect:
    ------------------------------------
    The sum of all data object lengths of a RID operation specifies the total RID operation length
    which will be validated at request reception resp. used for response composition.
    
    Constraints:
    ------------------------------------
    The size shall always be a multiple of 8 (byte borders).
    
    Dependencies:
    ------------------------------------
    The size parameter is either the concrete or maximum data object size, depending on the
    corresponding  DcmDspRoutineSignalType parameter value (refer to
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalType").
    
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
  默认值: 65535
  最小值: 1
  最大值: 524280
- 
  序号: 2
  名称: DcmDspRoutineSignalPos
  长名称: ''
  描述: |
    Specifies the position of the signal in the RID request/response.
    
    Effect:
    ------------------------------------
    Affects the call out/service call function signature.
    
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
  最大值: 524280
- 
  序号: 3
  名称: DcmDspRoutineSignalType
  长名称: ''
  描述: |
    Specifies whether the data object has a constant (fixed) or variable length.
    
    Effect:
    ------------------------------------
    If set to other value than VARIABLE_LENGTH, the Dcm will use the data length parameter value of
    a data object directly from the configuration. Otherwise, the Dcm will gather the concrete
    length from the application.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Affects the interpretation of the corresponding DcmDspRoutineSignalLength parameter:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalLength".
    
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
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspRoutineSignalEndianness
  长名称: ''
  描述: Defines the endianness for all this routine signal.
  默认值: OPAQUE
  最小值: ''
  最大值: ''
```

### 81. DcmDspRoutineStopOut

**描述**: Provide description of output parameter of Stop sub-service for RoutineControl service.

该容器没有参数。

### 82. DcmDspRoutineStopOutSignal

**描述**: Provide description of a routine signal used in RoutineControl service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoutineSignalLength
  长名称: ''
  描述: |
    Specifies the length of RID data in bits. If Data has variable data length, this parameter
    specifies the maximum data length.
    
    Effect:
    ------------------------------------
    The sum of all data object lengths of a RID operation specifies the total RID operation length
    which will be validated at request reception resp. used for response composition.
    
    Constraints:
    ------------------------------------
    The size shall always be a multiple of 8 (byte borders).
    
    Dependencies:
    ------------------------------------
    The size parameter is either the concrete or maximum data object size, depending on the
    corresponding  DcmDspRoutineSignalType parameter value (refer to
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalType").
    
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
  默认值: 65535
  最小值: 1
  最大值: 524280
- 
  序号: 2
  名称: DcmDspRoutineSignalPos
  长名称: ''
  描述: |
    Specifies the position of the signal in the RID request/response.
    
    Effect:
    ------------------------------------
    Affects the call out/service call function signature.
    
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
  最大值: 524280
- 
  序号: 3
  名称: DcmDspRoutineSignalType
  长名称: ''
  描述: |
    Specifies whether the data object has a constant (fixed) or variable length.
    
    Effect:
    ------------------------------------
    If set to other value than VARIABLE_LENGTH, the Dcm will use the data length parameter value of
    a data object directly from the configuration. Otherwise, the Dcm will gather the concrete
    length from the application.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Affects the interpretation of the corresponding DcmDspRoutineSignalLength parameter:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalLength".
    
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
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspRoutineSignalEndianness
  长名称: ''
  描述: Defines the endianness for all this routine signal.
  默认值: OPAQUE
  最小值: ''
  最大值: ''
```

### 83. DcmDspRoutineRequestResIn

**描述**: Provide description of input parameter of RequestResult sub-service for RoutineControl service.

该容器没有参数。

### 84. DcmDspRoutineRequestResInSignal

**描述**: Provide description of a routine signal used in RoutineControl service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoutineSignalLength
  长名称: ''
  描述: |
    Specifies the length of RID data in bits. If Data has variable data length, this parameter
    specifies the maximum data length.
    
    Effect:
    ------------------------------------
    The sum of all data object lengths of a RID operation specifies the total RID operation length
    which will be validated at request reception resp. used for response composition.
    
    Constraints:
    ------------------------------------
    The size shall always be a multiple of 8 (byte borders).
    
    Dependencies:
    ------------------------------------
    The size parameter is either the concrete or maximum data object size, depending on the
    corresponding  DcmDspRoutineSignalType parameter value (refer to
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalType").
    
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
  默认值: 65535
  最小值: 1
  最大值: 524280
- 
  序号: 2
  名称: DcmDspRoutineSignalPos
  长名称: ''
  描述: |
    Specifies the position of the signal in the RID request/response.
    
    Effect:
    ------------------------------------
    Affects the call out/service call function signature.
    
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
  最大值: 524280
- 
  序号: 3
  名称: DcmDspRoutineSignalType
  长名称: ''
  描述: |
    Specifies whether the data object has a constant (fixed) or variable length.
    
    Effect:
    ------------------------------------
    If set to other value than VARIABLE_LENGTH, the Dcm will use the data length parameter value of
    a data object directly from the configuration. Otherwise, the Dcm will gather the concrete
    length from the application.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Affects the interpretation of the corresponding DcmDspRoutineSignalLength parameter:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalLength".
    
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
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspRoutineSignalEndianness
  长名称: ''
  描述: Defines the endianness for all this routine signal.
  默认值: OPAQUE
  最小值: ''
  最大值: ''
```

### 85. DcmDspRoutineRequestResOut

**描述**: Provide description of output parameter of RequestResult sub-service for RoutineControl service.

该容器没有参数。

### 86. DcmDspRoutineRequestResOutSignal

**描述**: Provide description of a routine signal used in RoutineControl service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoutineSignalLength
  长名称: ''
  描述: |
    Specifies the length of RID data in bits. If Data has variable data length, this parameter
    specifies the maximum data length.
    
    Effect:
    ------------------------------------
    The sum of all data object lengths of a RID operation specifies the total RID operation length
    which will be validated at request reception resp. used for response composition.
    
    Constraints:
    ------------------------------------
    The size shall always be a multiple of 8 (byte borders).
    
    Dependencies:
    ------------------------------------
    The size parameter is either the concrete or maximum data object size, depending on the
    corresponding  DcmDspRoutineSignalType parameter value (refer to
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalType").
    
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
  默认值: 65535
  最小值: 1
  最大值: 524280
- 
  序号: 2
  名称: DcmDspRoutineSignalPos
  长名称: ''
  描述: |
    Specifies the position of the signal in the RID request/response.
    
    Effect:
    ------------------------------------
    Affects the call out/service call function signature.
    
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
  最大值: 524280
- 
  序号: 3
  名称: DcmDspRoutineSignalType
  长名称: ''
  描述: |
    Specifies whether the data object has a constant (fixed) or variable length.
    
    Effect:
    ------------------------------------
    If set to other value than VARIABLE_LENGTH, the Dcm will use the data length parameter value of
    a data object directly from the configuration. Otherwise, the Dcm will gather the concrete
    length from the application.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Affects the interpretation of the corresponding DcmDspRoutineSignalLength parameter:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspRoutineInfo/XXX/YYY/DcmDspRoutineSignalLength".
    
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
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspRoutineSignalEndianness
  长名称: ''
  描述: Defines the endianness for all this routine signal.
  默认值: OPAQUE
  最小值: ''
  最大值: ''
```

### 87. DcmDspRoutineAuthorization

**描述**: This container contains the configuration (parameters) for the Routine Authorization.

该容器没有参数。

### 88. DcmDspSecurity

**描述**: This container includes all security access levels the Dcm shall support.

Effect:
------------------------------------
For each security level to be supported by Dcm a DcmDspSecurityRow sub-container shall be defined.
Note: It is not recommended to define the "Locked" level.

Constraints:
------------------------------------
For each security level, there shall always be a corresponding pair of sub-services for service
0x27:
 - one for the "get seed" operation with sub-service identifier value equal to this parameter value
(e.g. 0x03);
 - one for the "send key" operation with sub-service identifier value equal to this parameter value
plus one (e.g. 0x04);

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
The Dcm configuration data ROM usage scales straight proportionally to the number of security levels
defined.

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
  名称: DcmDspSecuritySingleInstanceAttemptMonitor
  长名称: ''
  描述: |
    Specifies whether DCM module shall support a single AttemptCounter for security access levels or
    not.
    
    Effect:
    ------------------------------------
    If set to TRUE, DCM will support a single/shared memory for the security AttemptCounter among
    all configured DcmDspSecurityRows.
    If not existing or FALSE, DCM will instantiate the AttemptCounter per configured
    DcmDspSecurityRow as per ISO14229-1.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x27.
    
    Runtime effects:
    ------------------------------------
    none.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    If set to TRUE, the code usage will decrease by the amount, dependent of the number of number of
    DcmDspSecurityRows.
    
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspSecuritySingleInstanceDelayTimer
  长名称: ''
  描述: |
    Specifies whether DCM module shall support a single DelayTimer for security access levels or
    not.
    
    Effect:
    ------------------------------------
    If set to TRUE, DCM will support a single DelayTimer among all configured DcmDspSecurityRows.
    If not set or FALSE, DCM will instantiate the DelayTimer per configured DcmDspSecurityRow as per
    ISO14229-1.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x27.
    
    Runtime effects:
    ------------------------------------
    none.
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    If set to TRUE, the code usage will decrease by the amount, dependent of the number of number of
    DcmDspSecurityRows.
    
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspSecurityResetAttemptCounterOnTimeout
  长名称: ''
  描述: |
    Specifies whether DCM module shall reset the security attempt counter when the delay timer is
    expired.
    
    Effect:
    ------------------------------------
    If set to TRUE, DCM will reset the security attempt counter when the delay timer expires.
    If not set or FALSE, DCM will not reset the security attempt counter when the delay timer
    expires. DCM will reset the security attempt counter only when a successful sendKey subfunction
    request is performed.
    
    Constraints:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    none.
    
    Global RAM usage effects:
    ------------------------------------
    none.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspSecurityBypassEnabled
  长名称: ''
  描述: |
    Specifies whether DCM module shall support a bypass mode for security access levels or not.
    
    Effect:
    ------------------------------------
    If set to TRUE, DCM will support a bypass mode for security access levels.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x27.
    
    Runtime effects:
    ------------------------------------
    Enabling this feature will slightly increase the Dcm task time.
    
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
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DcmDspSecurityRetainOnSessionSelfTransition
  长名称: ''
  描述: |
    Specifies whether DCM module shall retain the security level during the self-transition of
    sessions or not.
    
    Effect:
    ------------------------------------
    If set to TRUE, DCM will not reset the security state during the self-transition of sessions.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for service 0x27.
    
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
  默认值: false
  最小值: ''
  最大值: ''
```

### 89. DcmDspSecurityRow

**描述**: Definition of a single Row of configuration for security level configuration (per security level).

The name of this container is used to define the name of the
R-Port through which the DCM accesses the interface
SecurityAccess_{SecurityLevel}. The R-Port is named
SecurityAccess_{SecurityLevel} where {SecurityLevel} is the
name of the container DcmDspSecurityRow. If there is no
reference, no check of security level shall be done.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspSecurityADRSize
  长名称: ''
  描述: |
    Specifies the size in bytes of the AccessDataRecord used in GetSeed diagnostic request of the
    corresponding security level.
    
    Effect:
    ------------------------------------
    The Dcm will consider this parameter during the diagnostic request evaluation for sub-functions
    "get seed" of service 0x27 for the corresponding security level.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Affects the minimum required Dcm buffer size
    ("/MICROSAR/Dcm/DcmConfigSet/DcmDsl/DcmDslBuffer/DcmDslBufferSize").
    
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
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: DcmDspSecurityAttemptCounterEnabled
  长名称: Dsp Security AttemptCounter Enabled
  描述: |
    Allows to enable the external storage of the security attempt counter (e.g. to survival a reset
    of the ECU).
    
    Effect:
    ------------------------------------
    If ENABLED, the Dcm will call two APIs for reading/storing the attempt counter assigned with
    this security level.
    If DISABLED, each time Dcm is initialized the counter value for the security level will be zero.
    
    Constraints:
    ------------------------------------
    This setting will have any effect only if the security level supports attempt counter
    monitoring.
    
    Dependencies:
    ------------------------------------
     - Setting "/Dcm/DcmConfigSet/DcmDsp/DcmDspSecurity/DcmDspSecurityRow/DcmDspSecurityNumAttDelay"
    must have the value that enables attempt counter usage for this level.
    
    Runtime effects:
    ------------------------------------
    If ENABLED, at the corresponding get and set attempt counter APIs will be supported. This will
    lead to a run time usage increase in cases the attempt counter is read or updated.
    
    Code ROM usage effects:
    ------------------------------------
    If ENABLED, the code ROM usage will increase a little bit due to the new feature activation and
    synchronizing mechanisms.
    
    Const data ROM usage effects:
    ------------------------------------
    If ENABLED, the data ROM usage will slightly increased. The total amount depends on the number
    of security levels.
    
    Global RAM usage effects:
    ------------------------------------
    IF ENABLED, the RAM usage will insignificantly increase.
    
    Stack RAM usage effects:
    ------------------------------------
    If ENABLED, the stack usage will depend on the stack usage of the implemented set and get
    attempt counter APIs.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspSecurityCompareKeyFnc
  长名称: Dsp Security CompareKey Fnc
  描述: Function name to request the result of a key comparison.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspSecurityDelayTime
  长名称: ''
  描述: |
    Specifies the delay time in seconds during which the Dcm will not accept any security access
    request.
    
    Effect:
    ------------------------------------
    Dcm will start the configured time after given number of failed security access attempts has
    failed.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if the corresponding level DcmDspSecurityNumAttDelay parameter is not zero.
    Refer to: "/Dcm/DcmConfigSet/DcmDsp/DcmDspSecurity/DcmDspSecurityRow/DcmDspSecurityNumAttDelay".
    
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
  最大值: 20000
- 
  序号: 5
  名称: DcmDspSecurityDelayTimeOnBoot
  长名称: ''
  描述: |
    Specifies the delay time in seconds at each Dcm power on cycle during which the Dcm will not
    accept any security access request.
    
    Effect:
    ------------------------------------
    If the parameter is set to a non-zero value, the Dcm will start monitor this time once
    initialized until and reject any security access diagnostic request until this time is not
    elapsed.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if the corresponding level DcmDspSecurityNumAttDelay parameter is not zero.
    Refer to: "/Dcm/DcmConfigSet/DcmDsp/DcmDspSecurity/DcmDspSecurityRow/DcmDspSecurityNumAttDelay".
    
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
  最大值: 20000
- 
  序号: 6
  名称: DcmDspSecurityDelayTimeOnFailedGetAttemptCounter
  长名称: Dsp Security Delay Time On Failed GetAttemptCounter
  描述: |
    Specifies the delay time in seconds during which the Dcm will not accept any security access
    request if the GetSecurityAttemptCounter API fails to return a valid value.
    
    Effect:
    ------------------------------------
    Once Dcm is initialized and configured to restore previous (pre-reset) AttemptCounter values, it
    will start reading all security level specific AttemptCounter values using the corresponding
    GetSecurityAttemptCounter API. If this read attempt fails, the Dcm will react depending on this
    configuration option:
    - If the time value ==  0 is configured, Dcm will start the corresponding delay timer for an
    infinite time. During this power on cycle, no security access request will be accepted.
    - If a time value >0 is configured, Dcm will start the corresponding delay timer with the
    configured time. For this time, no security access request (for this security level) will be
    accepted.
    - if the parameter is missing (default), Dcm will assume the retrieved counter value as zero and
    thus will not start any power on time. A security access request will be accepted immediately.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if the corresponding level DcmDspSecurityAttemptCounterEnabled parameter is
    ENABLED. Refer to:
    "/Dcm/DcmConfigSet/DcmDsp/DcmDspSecurity/DcmDspSecurityRow/DcmDspSecurityAttemptCounterEnabled".
    
    Runtime effects:
    ------------------------------------
    Supporting infinite delay time requires insignificantly more run time.
    
    Code ROM usage effects:
    ------------------------------------
    Supporting infinite delay time requires insignificantly more code ROM.
    
    Const data ROM usage effects:
    ------------------------------------
    Supporting infinite delay time requires insignificantly more data ROM.
    
    Global RAM usage effects:
    ------------------------------------
    Supporting infinite delay time requires insignificantly more RAM.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0
  最小值: 0
  最大值: 20000
- 
  序号: 7
  名称: DcmDspSecurityGetAttemptCounterFnc
  长名称: Dsp Security GetAttemptCounter Fnc
  描述: |
    Specifies the call out function name for re-storing the attempt counter.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function each time Dcm is
    initialized (Dcm_Init is called).
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    - the DcmDspSecurityAttemptCounterEnabled is ENABLED (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspSecurity/DcmDspSecurityRow/DcmDspSecurityAttemptCounterEnabled)
    - the DcmDspSecurityUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspSecurity/DcmDspSecurityRow/DcmDspSecurityUsePort)
    
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
  序号: 8
  名称: DcmDspSecurityGetSeedFnc
  长名称: Dsp Security GetSeed Fnc
  描述: Function name to request a seed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DcmDspSecurityKeySize
  长名称: ''
  描述: |
    Specifies the size in bytes of the security access key for the corresponding security level.
    
    Effect:
    ------------------------------------
    The Dcm will consider this parameter during the diagnostic request length validation for
    sub-functions "send key" of service 0x27 for the corresponding security level.
    
    Constraints:
    ------------------------------------
    The key size shall fit the configured diagnostic buffer including the diagnostic protocol
    request header information.
    
    Dependencies:
    ------------------------------------
    Affects the minimum required Dcm buffer size
    ("/MICROSAR/Dcm/DcmConfigSet/DcmDsl/DcmDslBuffer/DcmDslBufferSize").
    
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
  默认值: 4
  最小值: 1
  最大值: 4294967295
- 
  序号: 10
  名称: DcmDspSecurityLevel
  长名称: ''
  描述: |
    Specifies the value of the corresponding security level.
    
    Effect:
    ------------------------------------
    This value will be used when the Dcm_GetSecurityLevel API is called from the application to
    report the currently active security level.
    
    Constraints:
    ------------------------------------
    For any security level, except locked, this value must not be zero.
    For each security level (except locked), there shall always be a corresponding pair of
    sub-services for service 0x27:
     - one for the "get seed" operation with an odd sub-service identifier value (e.g. 0x01);
     - one for the "send key" operation with an even sub-service identifier value equal to "get
    seed" plus one (e.g. 0x02);
    
    The parameter value shall always match the "get seed/send-key" pair's sub-function id of the
    service 0x27 configuration container as follows:
    SecurityLevel = (<sub-function id> + 1) / 2
    
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
  最大值: 63
- 
  序号: 11
  名称: DcmDspSecurityNumAttDelay
  长名称: ''
  描述: |
    Specifies the number of failed security accesses after which the delay time is activated.
    
    Effect:
    ------------------------------------
    If set to a value other than 0, the Dcm will count the failed attempts and initiate a penalty
    strategy on reaching the configured value.
    If set to 0, the Dcm will not implement any failed attempt penalty strategy and will be always
    be ready for a new try.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    If set to a non zero value, the parameters DcmDspSecurityDelayTime and
    DcmDspSecurityDelayTimeOnBoot shall be additionally configured.
    Refer to:
     - "/Dcm/DcmConfigSet/DcmDsp/DcmDspSecurity/DcmDspSecurityRow/DcmDspSecurityDelayTime"
     - "/Dcm/DcmConfigSet/DcmDsp/DcmDspSecurity/DcmDspSecurityRow/DcmDspSecurityDelayTimeOnBoot"
    
    Runtime effects:
    ------------------------------------
    If set to a non zero value, the Dcm main function will additionally need time to monitor the
    configured penalty time in parallel to all other tasks it has to complete. The service 0x27
    handler will take slightly more time due to the attempt counter and timer management
    functionality this parameter enables.
    
    Code ROM usage effects:
    ------------------------------------
    If set to a non zero value, the Dcm code ROM usage will increase due to the attempt counter and
    timer management functionality this parameter enables.
    
    Const data ROM usage effects:
    ------------------------------------
    If set to a non zero value, the Dcm configuration data ROM usage will increase due to the
    additional information storage this parameter enables.
    
    Global RAM usage effects:
    ------------------------------------
    If set to a non zero value, the Dcm RAM usage will increase due to the additional information
    storage this parameter enables.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: DcmDspSecuritySeedSize
  长名称: ''
  描述: |
    Specifies the size in bytes of the security access seed for the corresponding security level.
    
    Effect:
    ------------------------------------
    The Dcm will consider this parameter during the diagnostic response composition for
    sub-functions "get seed" of service 0x27 for the corresponding security level.
    
    Constraints:
    ------------------------------------
    The key size shall fit the configured diagnostic buffer including the diagnostic protocol
    response header information.
    
    Dependencies:
    ------------------------------------
    Affects the minimum required Dcm buffer size
    ("/MICROSAR/Dcm/DcmConfigSet/DcmDsl/DcmDslBuffer/DcmDslBufferSize").
    
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
    
  默认值: 4
  最小值: 1
  最大值: 4294967295
- 
  序号: 13
  名称: DcmDspSecuritySetAttemptCounterFnc
  长名称: Dsp Security SetAttemptCounter Fnc
  描述: |
    Specifies the call out function name for storing the attempt counter.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function each time the attempt
    counter changes for the corresponding security level.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    - the DcmDspSecurityAttemptCounterEnabled is ENABLED (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspSecurity/DcmDspSecurityRow/DcmDspSecurityAttemptCounterEnabled)
    - the DcmDspSecurityUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspSecurity/DcmDspSecurityRow/DcmDspSecurityUsePort)
    
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
  序号: 14
  名称: DcmDspSecurityUsePort
  长名称: ''
  描述: |
    Defines which kind of interface shall be used for security access.
    
    Effect:
    ------------------------------------
    USE_ASYNCH_CLIENT_SERVER: The DCM will access the data using an R-Port requiring an asynchronous
    ClientServertInterface SecurityAccess_{SecurityLevel}. The R-Port is described in
    DcmDspSecurityRow description.
    
    USE_ASYNCH_FNC: The DCM will access the data using the functions that are defined in the
    parameters DcmDspSecurityGetSeedFnc and DcmDspSecurityCompareKeyFnc.
    DCM_E_PENDING return is allowed and OpStatus is existing as IN parameter.
    
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
  默认值: USE_ASYNCH_CLIENT_SERVER
  最小值: ''
  最大值: ''
```

### 90. DcmDspSecurityFixedBytes

**描述**: Provides a set of security fixed bytes for this security level.

Effect:
------------------------------------
Optionally a security level can get a single or multiple sets of fixed bytes, that later can be
accessed by the SW-C for calculating the corresponding seed or/and key.

Constraints:
------------------------------------
A security level shall have multiple fixed byte sets only if there are any Vehicle System Groups
(VSGs) and the sets refer to different VSGs.

Dependencies:
------------------------------------
Multiple sets need VSGs: "/Dcm/DcmConfigSet/DcmDsp/DcmDspVehicleSystemGroups"

Runtime effects:
------------------------------------
Since typically the SW-C will access these fixed bytes within a callout invoked by Dcm, the overall
Dcm runtime processing SID 0x27 will insignificantly increase.

Code ROM usage effects:
------------------------------------
By defining at least one security level related fixed byte set, the code ROM usage will slightly
increase due to the activation of the new API Dcm_GetSecurityLevelFixedBytes().

Const data ROM usage effects:
------------------------------------
The Dcm configuration data ROM usage scales straight proportionally to the number of fixed bytes
defined.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
Since typically the SW-C will access these fixed bytes within a callout invoked by Dcm, the overall
Dcm stack RAM usage will insignificantly increase.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspSecurityFixedByteValue
  长名称: ''
  描述: |
    Specifies a fixed byte value for this security level.
    
    Effect:
    ------------------------------------
    The Dcm will provide this data at runtime via API
    
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
    Additional code to retrieve the byte values by API is enabled, increasing the ROM usage
    
    Const data ROM usage effects:
    ------------------------------------
    The byte values provided as well as control structures will increase the ROM consumption.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 0
  最小值: 0
  最大值: 255
```

### 91. DcmDspSecurityCallback

**描述**: Configures a single callback to be called on security access state change.

Effect:
-----------------------------------------
For each available container of this type, there will be a notification call.
Dcm will make a function on each security access state change (NOT on self-transitions).

Constraints:
-----------------------------------------
-

Dependencies:
-----------------------------------------
-

Runtime effects:
-----------------------------------------
Enabling this feature will increase the Dcm task time at any security access state change (e.g.
"Locked -&amp;amp;gt; Level1" or vice versa).

Code ROM usage effects:
------------------------------------
Enabling this feature leads to a minor increase of the Dcm static code ROM usage.

Const data ROM usage effects:
-----------------------------------------
Enabling this feature increases the Dcm configuration ROM usage. The usage scales linearly with the
amount of callouts.

Global RAM usage effects:
-----------------------------------------
none

Stack RAM usage effects:
-----------------------------------------
Enabling this feature can lead to a insignificant increased stack size required by the
Dcm_MainFunction.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspSecurityCallbackFnc
  长名称: ''
  描述: |
    Specifies the call out function name for notification call.
    
    Effect:
    ------------------------------------
    Dcm calls the function which name is set here.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if service 0x27 is supported.
    
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
```

### 92. DcmDspSession

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

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmSessionTimerS3Enabled
  长名称: ''
  描述: |
    Specifies whether the S3 timer is supported or not.
    
    Effect:
    -----------------------------------------
    If enabled or missing, the S3 timer is handled according to ISO 14229-2.
    If disabled, Dcm will never start S3 timer in a non-default sessions. In this case a S3 timeout
    will never occur.
    
    Constraints:
    -----------------------------------------
    Has effect only if a non-default session is supported.
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    Disabling this feature leads to a insignificant decrease of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    none
    
    
  默认值: true
  最小值: ''
  最大值: ''
```

### 93. DcmDspSessionRow

**描述**: Definition of a single Row of session control configuration (per session control)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspSessionForBoot
  长名称: ''
  描述: |
    This parameter defines whether the concrete diagnostic session allows to jump to bootloader (OEM
    bootloader or system supplier bootloader). If this diagnostic session doesn't allow to jump to
    Bootloader the value DCM_NO_BOOT shall be chosen.
    
    Effect:
    ------------------------------------
    If set to any value other than "DCM_NO_BOOT", on receiving the corresponding session activation
    diagnostic request will cause Dcm to jump to Bootloader.
    
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
    If all of the session levels specify for this parameter "DCM_NO_BOOT", the Dcm code ROM usage
    will be reduced.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    If all of the session levels specify for this parameter "DCM_NO_BOOT", the Dcm code RAM usage
    will be reduced.
    
    Stack RAM usage effects:
    ------------------------------------
    For a session levels specifying for this parameter value other than "DCM_NO_BOOT", the Dcm main
    function stack usage may slightly increase. The total stack usage in case of jump to Bootloader
    depends then mostly on the implementation of the Dcm_SetProgConditions call out.
  默认值: DCM_NO_BOOT
  最小值: ''
  最大值: ''
- 
  序号: 2
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
  序号: 3
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
  序号: 4
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

### 94. DcmDspSessionCallback

**描述**: Configures a single callback to be called on diagnostic session state change.

Effect:
-----------------------------------------
For each available container of this type, there will be a notification call.
Dcm will make a function on each diagnostic session access state change (ALSO on self-transitions).

Constraints:
-----------------------------------------
-

Dependencies:
-----------------------------------------
-

Runtime effects:
-----------------------------------------
Enabling this feature will increase the Dcm task time at any diagnostic session state change (e.g.
"Default->Extended" or "Default->Default", etc.).

Code ROM usage effects:
------------------------------------
Enabling this feature leads to a minor increase of the Dcm static code ROM usage.

Const data ROM usage effects:
-----------------------------------------
Enabling this feature increases the Dcm configuration ROM usage. The usage scales linearly with the
amount of callouts.

Global RAM usage effects:
-----------------------------------------
none

Stack RAM usage effects:
-----------------------------------------
Enabling this feature can lead to a insignificant increased stack size required by the
Dcm_MainFunction.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspSessionCallbackFnc
  长名称: ''
  描述: |
    Specifies the call out function name for notification call.
    
    Effect:
    ------------------------------------
    Dcm calls the function which name is set here.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if service 0x10 is supported.
    
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
```

### 95. DcmDspTestResultByObdmid

**描述**: This container contains the configuration (parameters) of the "Request on-board monitoring test
results" service (Service $06).

该容器没有参数。

### 96. DcmDspTestResultObdmidTid

**描述**: This container contains the configuration (parameters) of a OBDMID and the assigned TIDs for the
"Request on-board monitoring test results" service (Service $06).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspTestResultObdmid
  长名称: ''
  描述: OBDMID for Service $06
  默认值: ''
  最小值: 0
  最大值: 255
```

### 97. DcmDspTestResultObdmidTids

**描述**: This container contains the configuration (parameters) of the TIDs belonging to the OBDMID for the
"Request on-board monitoring test results" service (Service $06).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspTestResultObdmidTidUaSid
  长名称: Dsp Test Result Obdmid Tid UaSid
  描述: Unit And Scaling ID for Service $06
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DcmDspTestResultObdmidTidFnc
  长名称: ''
  描述: |
    Specifies the call out function name for control.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on MIDTID reading
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x06 (RequesOnBoardMonitorTestResults) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DcmDspDataUsePort is set to one of the FNC (e.g. call out) types (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspPid/DcmDspPidData/DcmDspPidService01/DcmDspPidDataUsePort)
    
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
  序号: 3
  名称: DcmDspTestResultObdmidTidUsePort
  长名称: ''
  描述: |
    Defines which kind of interface shall be used to control.
    
    Effect:
    ------------------------------------
    If set to TRUE, a RTE call will be required to be implemented in the Dcm application.
    If set to FALSE, a callout will be required to be implemented in the Dcm application.
    
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
    
  默认值: true
  最小值: ''
  最大值: ''
```

### 98. DcmDspTestResultTid

**描述**: This container contains the configuration (parameters) of a single TID for the "Request on-board
monitoring test results" service (Service $06).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspTestResultTestId
  长名称: ''
  描述: Test Id for Service $06
  默认值: ''
  最小值: 0
  最大值: 255
```

### 99. DcmDspVehicleSystemGroups

**描述**: This container includes all Dcm related Vehicle System Groups (VSGs).

Effect:
------------------------------------
For each VSG to be supported by Dcm a DcmDspVehicleSystemGroupRow sub-container shall be defined.
If this container does not exist, VSG support will be deactivated.


Constraints:
------------------------------------
The Base-VSG (i.e. the one which is automatically activated at ECU power on/reset) must not to be
defined!

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
By defining at least one VSG, the runtime of diagnostic request processing will slightly increase
(comparable with PBS runtime usage).

Code ROM usage effects:
------------------------------------
By defining at least one VSG, the code ROM usage will slightly increase (comparable with PBS code
ROM usage).

Const data ROM usage effects:
------------------------------------
The Dcm configuration data ROM usage scales straight proportionally to the number of VSGs defined.

Global RAM usage effects:
------------------------------------
By defining at least one VSG, the RAM usage will insignificantly increase.

Stack RAM usage effects:
------------------------------------
By defining at least one VSG, the stack RAM usage will slightly increase (comparable with PBS stack
RAM usage).

该容器没有参数。

### 100. DcmDspVehicleSystemGroupRow

**描述**: Represents a single Vehicle System Group (VSG) related to Dcm.


#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspVehicleSystemGroupId
  长名称: ''
  描述: |
    Specifies an abstract ID of the corresponding Vehicle System Group.
    
    Effect:
    ------------------------------------
    This ID will be used when the VSG getter/setter API are called from the application to
    report/change the currently active VSG(s).
    
    Constraints:
    ------------------------------------
    For each VSG, there shall always be a unique ID.
    ID 0 is reserved for the base variant (i.e. for all those diagnostic entities that are allowed
    in all VSGs)
    
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
  最小值: 1
  最大值: 65535
```

### 101. DcmDspVehInfo

**描述**: This container contains the configuration (parameters) of the "Request vehicle information service"
(service $09).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspVehInfoInfoType
  长名称: ''
  描述: |
    Specifies the identifier value of a InfoType.
    
    Effect:
    ------------------------------------
    The Dcm only recognizes InfoTypes with the value specified in this parameter.
    
    Constraints:
    ------------------------------------
    The InfoType value must be unique within a DcmConfigset.
    
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
  最大值: 255
- 
  序号: 2
  名称: DcmDspVehInfoUsed
  长名称: ''
  描述: |
    Allows to activate or deactivate the usage of a VehInfoType, for multi purpose ECUs.
    In a single configuration the parameter can be used to temporarily disable a complete
    VehInfoType in the Dcm configuration without the need to delete all its configuration
    parameters.
    
    Effect:
    ------------------------------------
    If set to FALSE, the VehInfoType and all its signals will not be used in the Dcm generated code.
    
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
    If set to FALSE, no data ROM for this VehInfoType will be used in the Dcm configuration sources.
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: true
  最小值: ''
  最大值: ''
```

### 102. DcmDspVehInfoData

**描述**: Data Item of an InfoType; post-fix of the port interface name.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspVehInfoDataOrder
  长名称: ''
  描述: NOT USED
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DcmDspVehInfoDataReadFnc
  长名称: ''
  描述: |
    Specifies the call out function name for reading the data object content.
    
    Effect:
    ------------------------------------
    If this parameter is not empty, the Dcm will call the specified function on InfoType reading
    diagnostic request.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Has effect only if:
    - the diagnostic service 0x09 (RequestVehicleInformation) is supported by Dcm (refer to
    /Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService)
    - the DcmDspVehInfoDataUsePort is set to FALSE (e.g. call out) type (refer to
    /Dcm/DcmConfigSet/DcmDsp/DcmDspVehInfo/DcmDspVehInfoData/DcmDspVehInfoDataUsePort)
    
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
  序号: 3
  名称: DcmDspVehInfoDataSize
  长名称: ''
  描述: |
    Specifies the length of InfoType ID data including NODI in bytes.
    
    Effect:
    ------------------------------------
    The sum of all data object lengths of a InfoType ID and the NODI byte do specify the total
    InfoType ID length which used for response composition.
    
    Constraints:
    ------------------------------------
    Since the NODI byte is always included in the data stream, and at least one data element shall
    be reported, the minimum data length shall be at minimum two bytes.
    
    Dependencies:
    ------------------------------------
    The size parameter is the concrete or maximum data object size.
    
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
    
  默认值: 255
  最小值: 2
  最大值: 255
- 
  序号: 4
  名称: DcmDspVehInfoDataUsePort
  长名称: ''
  描述: |
    Defines which kind of interface shall be used to access the data.
    
    Effect:
    ------------------------------------
    If set to TRUE, a RTE call will be required to be implemented in the Dcm application.
    If set to FALSE - a call out will be required to be implemented in the Dcm application.
    
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
    
  默认值: true
  最小值: ''
  最大值: ''
```

### 103. DcmDspReadDTCInformation

**描述**: Provides further configuration for the UDS service ReadDTCInformation processing.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspReadDTCInformationSupportedObdUdsDtcSeparation
  长名称: ''
  描述: |
    If this parameter is set to true, the OBDonUDS for DTC separation is enabled. If this parameter
    is not configured or set to false, the OBD UDS DTC separation is disabled.
    
    Effect:
    ------------------------------------
    If enabled, the Dcm service processor for all diagnostic requests according to SAE J1979-2 shall
    use the Dem APIs with the parameter DTCFormat set to DEM_DTC_FORMAT_OBD_3BYTE to query and
    process DTC related information.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    Will be used only if the diagnostic service 0x19 is supported by DCM and DEM API version 4.3.0
    or newer is selected.
    
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
  默认值: false
  最小值: ''
  最大值: ''
```

### 104. DcmGeneral

**描述**: This container contains the configuration (parameters) for Component wide parameters

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDevErrorDetect
  长名称: ''
  描述: |
    Specifies whether the Dcm shall monitor the API input and output parameters and internal
    behavior with notification to the DET BSW.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will monitor any critical code sections for proper function in order to avoid
    unpredictable software behavior in situations such as: null pointers, out of boundary accesses,
    unexpected parameter values, etc.
    
    Constraints:
    -----------------------------------------
    It is recommended to leave this parameter enabled during the first integration steps and test
    executions with Dcm for getting stable code and traceable errors.
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature will increase the overall CPU load during the Dcm task activity. Also all
    Dcm APIs called within an interrupt will lead to a minor increased of interrupt latency.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature increases the Dcm code ROM usage due to the additional check code sections
    activated by this setting.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    Enabling this feature will lead to an insignificant increase of the RAM usage for some
    additional management variables.
    
    Stack RAM usage effects:
    ------------------------------------
    none
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmRequestManufacturerNotificationEnabled
  长名称: ''
  描述: |
    Specifies whether the diagnostic request notification mechanism for the manufacturer shall be
    used or not.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will call all configured manufacturer indication functions. These will decide
    whether the Dcm shall proceed with the service processing or not.
    
    Constraints:
    -----------------------------------------
    Can be enabled only if there is at least one
    "/Dcm/DcmConfigSet/DcmDsl/DcmDslServiceRequestManufacturerNotification" parameter defined.
    
    Dependencies:
    -----------------------------------------
    Configuration parameters:
    "/Dcm/DcmConfigSet/DcmDsl/DcmDslServiceRequestManufacturerNotification"
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature will increase the Dcm task time during its first activation on any
    diagnostic request been received.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    Enabling this feature increases the Dcm configuration ROM usage. The usage scales linearly with
    the amount of SWCs to be notified.
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    Enabling this feature can lead to a insignificant increased stack size required by the
    Dcm_MainFunction.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmRequestSupplierNotificationEnabled
  长名称: ''
  描述: |
    Specifies whether the diagnostic request notification mechanism for the suppliers shall be used
    or not.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will call all configured supplier indication functions. These will decide
    whether the Dcm shall proceed with the service processing or not.
    
    Constraints:
    -----------------------------------------
    Can be enabled only if there is at least one
    "/Dcm/DcmConfigSet/DcmDsl/DcmDslServiceRequestSupplierNotification" parameter defined.
    
    Dependencies:
    -----------------------------------------
    Configuration parameters: "/Dcm/DcmConfigSet/DcmDsl/DcmDslServiceRequestSupplierNotification"
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature will increase the Dcm task time during its first activation on any
    diagnostic request been received.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    Enabling this feature increases the Dcm configuration ROM usage. The usage scales linearly with
    the amount of SWCs to be notified.
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    Enabling this feature can lead to a insignificant increased stack size required by the
    Dcm_MainFunction.
    
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmRespondAllRequest
  长名称: ''
  描述: |
    Specifies whether Dcm shall process any received diagnostic request or not.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will accept and process any requested service ID. If disabled, Dcm will accept
    the reception of any diagnostic service ID, but will not process any belonging to the range
    [0x40,0x7F]U[0xC0, 0xFF].
    
    Constraints:
    -----------------------------------------
    none
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    Disabling this feature will lead to an insignificant runtime overhead at the end of a request
    reception.
    
    Code ROM usage effects:
    ------------------------------------
    Disabling this feature leads to a insignificant increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    Disabling this feature will lead to an insignificant ROM usage overhead due to the additional
    evaluation of the SID.
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    none
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
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
  序号: 6
  名称: DcmVersionInfoApi
  长名称: ''
  描述: |
    Specifies whether Dcm shall provide access to its version information or not.
    
    Effect:
    -----------------------------------------
    By enabling this feature, the Dcm will provide an API "Dcm_GetVersionInfo" for reading its
    version information. If this information is not needed within the ECU project, leave this
    feature disabled for minimum ROM usage.
    
    Constraints:
    -----------------------------------------
    none
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    Enabling this feature leads to an insignificant increase of the ROM usage, caused by the API
    function implementation.
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    none
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
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
  序号: 8
  名称: DcmDefensiveBehaviorEnabled
  长名称: ''
  描述: |
    Specifies whether the Dcm shall monitor the API input and output parameters and internal
    behavior, but without notifying the DET BSW.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will monitor any critical code sections for proper function in order to avoid
    unpredictable software behavior in situations such as: null pointers, out of boundary accesses,
    unexpected parameter values, etc.
    
    Constraints:
    -----------------------------------------
    It is recommended to leave this parameter enabled during the first integration steps and test
    executions with Dcm for getting stable code and traceable errors.
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature will increase the overall CPU load during the Dcm task activity. Also some
    Dcm APIs called within an interrupt will lead to a minor increased of interrupt latency.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a major increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    Enabling this feature will lead to an insignificant increase of the RAM usage for some
    additional management variables.
    
    Stack RAM usage effects:
    -----------------------------------------
    none
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DcmMaxNumberIterationsPerTask
  长名称: ''
  描述: |
    Specifies the maximum number of iterations on an external module API per single Dcm_MainFunction
    activation. Applicable primarily on any diagnostic service.
    
    Effect:
    -----------------------------------------
    If any limitation value other than zero is specified, Dcm will monitor the number of internal
    jobs iterations per task activation to save CPU time.
    Note: A too low value will lead to RCR-RP responses. Refer to the technical reference for more
    details on this feature.
    
    Constraints:
    -----------------------------------------
    Possible values:
      0  - no limitation (default)
    >0  - specific number of iterations per task
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    If a limitation is enabled, all complex diagnostic services will have an insignificantly
    increased runtime due to the additional monitor code.
    
    Code ROM usage effects:
    ------------------------------------
    If a limitation is enabled, all Dem iterators will have an insignificantly increased ROM usage
    due to the additional monitor code.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    If a limitation is enabled, the Dcm_MainFunction will require insignificantly more stack.
    
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: DcmFinalResponseToFblEnabled
  长名称: ''
  描述: |
    Specifies whether the Dcm shall support the FBL final response transmission, defined by HIS.
    
    Effect:
    -----------------------------------------
    If enabled, the Dcm will use the "Dcm_GetProgConditions" callout to check whether a final
    response shall be sent or not.
    
    Constraints:
    -----------------------------------------
    none
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature leads to an automatic activation of the Dcm task for reading the
    programming conditions and if needed triggering the acquired final response.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to an increased ROM usage for reading the programming conditions and
    processing the final response transmission.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    Enabling this feature leads to an insignificant increase of RAM usage.
    
    Stack RAM usage effects:
    -----------------------------------------
    Enabling this feature can lead to an insignificant increase of stack usage during the first
    several Dcm_MainFunction activations.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DcmResetToFblAfterSessionFinalResponseEnabled
  长名称: ''
  描述: |
    Specifies whether the Dcm shall reset to the FBL before or after the final response transmission
    of service 0x10 (DiagnosticSessionControl).
    
    Effect:
    -----------------------------------------
    If enabled, the Dcm will reset the ECU only after the positive response for diagnostic service
    0x10 has been sent.
    If disabled, the Dcm will behave according to HIS - on reception of diagnostic service 0x10 with
    a session configured to cause a jump to the FBL, Dcm will reset the ECU without sending a final
    positive response for this request. The FBL later will do that.
    
    Constraints:
    -----------------------------------------
    none
    
    Dependencies:
    -----------------------------------------
    Has effect only if:
    - At least one diagnostic session has been configured to support jump to the FBL (refer to:
    /Dcm/DcmConfigSet/DcmDsp/DcmDspSession/DcmDspSessionRow/DcmDspSessionForBoot)
    
    
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
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: DcmCalibrationOfObdIdsEnabled
  长名称: ''
  描述: |
    Specifies whether the Dcm shall support calibratable OBD IDs  or not.
    
    Effect:
    -----------------------------------------
    If enabled, the Dcm will put all "availability ID" mask values (e.g. for PID 0x00, 0x20, etc.)
    into the calibratable memory section. Later the embedded code will use these values for knowing
    whether an OBD identifier is enabled or not.
    If disabled, the Dcm will always use only the generated configuration for each OBD ID
    availability.
    Note: These settings affects also the UDS OBD DIDs and RIDs.
    
    Constraints:
    -----------------------------------------
    Applies only to OBD ID objects, e.g. services 0x01, 0x02, 0x06, 0x08 and 0x09. On UDS: 0x22 and
    0x31.
    
    Dependencies:
    -----------------------------------------
    OBD must be licensed.
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature leads to an additional check for enabled OBD identifier after the default
    lookup engine has finished its job. This will insignificantly increase the run time usage.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to an insignificantly increase ROM usage for the additional enabling
    checks.
    
    Const data ROM usage effects:
    -----------------------------------------
    Enabling this feature leads to an insignificantly increase ROM usage for the supporting
    indirection tables.
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    none
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: DcmCalibrationOfObdIdsMemoryType
  长名称: ''
  描述: |
    Specifies the memory location of the calibratable OBD ID data.
    
    Effect:
    -----------------------------------------
    This option determines the memory location of the OBD "availability ID" mask values:
    
    If selected memory type VOLATILE - RAM tables will be generated. These have to be initialized by
    the application before the DCM is initialized.
    If selected memory type NON_VOLATILE - the generated tables are located in a special CONST
    (calibratable) area.
    
    If this parameter is not set the DCM will use the backward compatible selection: NON_VOLATILE.
    
    Constraints:
    -----------------------------------------
    Applies only to calibratable OBD ID objects, e.g. services 0x01, 0x02, 0x06, 0x08 and 0x09. On
    UDS: 0x22 and 0x31.
    
    Dependencies:
    -----------------------------------------
    The following option must be enabled first:
    /Dcm/DcmConfigSet/DcmGeneral/DcmCalibrationOfObdIdsEnabled
    
    Runtime effects:
    -----------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    none
    
    Const data ROM usage effects:
    -----------------------------------------
    If selected type is NON_VOLATILE, then global ROM usage will increase according to the number of
    OBD IDs supported by the ECU.
    
    Global RAM usage effects:
    -----------------------------------------
    If selected type is VOLATILE, then global RAM usage will increase according to the number of OBD
    IDs supported by the ECU.
    
    Stack RAM usage effects:
    -----------------------------------------
    none
  默认值: DCM_OBD_CALIB_MEM_NON_VOLATILE
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: DcmDspDataDefaultEndianness
  长名称: ''
  描述: Defines the default endianness for all data elements in DcmDsp.
  默认值: LITTLE_ENDIAN
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: DcmDemApiVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version of the integrated Dem API
    
    Effect:
    ------------------------------------
    Switches Dcm internal Dem interaction to the corresponding AUTOSAR version specification.
    If this parameter is missing, the native AUTOSAR version (4.03.00) will be active.
    
    Constraints:
    ------------------------------------
    Has effect only if the Dem related diagnostic services are handled within Dcm.
    
    Dependencies:
    ------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for any SID, that
    results in interaction between Dcm and Dem.
    
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    Code ROM usage slightly vary between Dem AR versions due to different API specifications.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
    
  默认值: DCM_DEM_API_4_03_00
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: DcmSecurityLevelChangeNotificationEnabled
  长名称: ''
  描述: |
    Specifies whether a SWCs will be notified or not for a changed security access level state by a
    mode-switch.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will invoke a RTE  mode switch on any non-self state transition e.g. for
    Locked->Level1, but not for Locked->Locked when for example a session transition
    Default->Default occurs.
    
    Constraints:
    -----------------------------------------
    Has effect only if service 0x27 is internally handled by Dcm.
    
    Dependencies:
    -----------------------------------------
    If "/Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService" is defined for SID 0x27.
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature will slightly increase the Dcm task time during any security access level
    change.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    Enabling this feature insignificantly increases the Dcm configuration ROM usage. The usage
    scales linearly with the configured amount of security access levels.
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: DcmSplitTasksEnabled
  长名称: ''
  描述: |
    Specifies whether only one main-function shall be used for timing and processing or one worker-
    and one timer-task.
    
    Effect:
    -----------------------------------------
    If disabled or missing the Dcm has only one main function: Dcm_MainFunction.
    If enabled the Dcm_MainFunction is split into to tasks: Dcm_MainFunctionTimer,
    Dcm_MainFunctionWorker.
    
    Constraints:
    -----------------------------------------
    If enabled, the timer- and worker-tasks shall be scheduled as described in the technical
    reference.
    
    Dependencies:
    -----------------------------------------
    If enabled, the parameter /Dcm/DcmConfigSet/DcmGeneral/DcmTaskTime can be used to set up timing
    for the worker task other than the DcmTaskTime.
    
    
    Runtime effects:
    -----------------------------------------
    If enabled, the Dcm behavior will depend on the concrete task scheduling. It may happen that Dcm
    will send more RCR-RP responses as before.
    
    Code ROM usage effects:
    ------------------------------------
    If enabled, the code ROM usage will slightly increase.
    
    Const data ROM usage effects:
    -----------------------------------------
    If enabled, the data ROM usage will insignificantly increase.
    
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    If enabled, stack usage may slightly increase due to the fact that now the Dcm_MainFunctionTimer
    may interrupt the Dcm_MainFunctionWorker.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: DcmMainFunctionWorkerTaskTime
  长名称: ''
  描述: |
    Allow to configure the time for the service processing task in seconds.
    
    Effect:
    -----------------------------------------
    This value is used to set up the Dcm Service-Description and BSW scheduler. Service processing
    speed of DCM will depend on this setting i.e. how fast the DCM will poll the application in case
    of E_PENDING.
    
    If this parameter is missing, but split task is selected
    (/Dcm/DcmConfigSet/DcmGeneral/DcmSplitTasksEnabled = TRUE), then the worker task will be called
    with the time period specified in /Dcm/DcmConfigSet/DcmGeneral/DcmTaskTime.
    
    Constraints:
    -----------------------------------------
    The specified time shall be a equal or smaller than the time in DcmTaskTime. This will prevent
    unnecessary RCR-RP responses.
    
    Dependencies:
    -----------------------------------------
    Has any effect only if parameter /Dcm/DcmConfigSet/DcmGeneral/DcmSplitTasksEnabled is set to
    TRUE.
    
    Runtime effects:
    -----------------------------------------
    Too low values will increase the Dcm responsiveness, but will increase the CPU load.
    
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
  序号: 19
  名称: DcmStateRecoveryAfterResetEnabled
  长名称: ''
  描述: |
    Specifies whether a context switch through ECU reset shall preserve some DCM internal states.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will read after each Dcm_Init call the context information from the application
    in order to restore it or leave the initial state as per default.
    If disabled, Dcm will boot up AR manner without any recovery information acquisition process.
    
    Constraints:
    -----------------------------------------
    -
    
    Dependencies:
    -----------------------------------------
    -
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature will slightly increase the Dcm task time after each Dcm_Init and only if
    there is some context to be recovered.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    Due to the additional calls done from within the Dcm_MainFunction for gathering the context
    information, the stack usage during the recovery phase (only after Dcm_Init) may increase. It
    will depend on the implementation of the application callback for getting recovery information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: DcmKeepAliveTime
  长名称: ''
  描述: |
    Specifies the time in seconds after each diagnostic request is processed during which the Dcm
    will keep the Diag-Active user in ComM registered.
    
    Effect:
    ------------------------------------
    If this parameter exists and contains a non-zero value, Dcm will keep the Diag-User active in
    ComM as long as either this time has not elapsed yet OR the diagnostic session is still a
    non-default one.
    Primarily this timer has effect while the Dcm is in the default session since, in that case Dcm
    would deactivate the user immediately after each request processing.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    none
    
    Runtime effects:
    ------------------------------------
    If additional keep alive logic is required, the run time on (un-)registering a ComM user per
    channel may insignificantly increase.
    
    Code ROM usage effects:
    ------------------------------------
    If additional keep alive logic is required, the code ROM usage on (un-)registering a ComM user
    per channel may insignificantly increase.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    If additional keep alive logic is required, the RAM usage may insignificantly increase.
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: 5
  最小值: 0
  最大值: 20000
- 
  序号: 21
  名称: DcmSafeBswChecks
  长名称: ''
  描述: |
    Specifies whether DCM will be put into SafeBSW mode.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm is considered as a ASIL component. Some features will not be supported (refer to
    SafetyManual for details). The code generator will automatically deactivate particular features
    if not yet released for ASIL application. Especially PBL configuration will be restricted to
    limited features.
    If disabled, Dcm will provide full featured support.
    
    Constraints:
    -----------------------------------------
    none
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    If enabled Dcm runtime usage may significantly increase due to the additional runtime checks
    that prevent from illegal API usage or buffer overflows.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: DcmVirtualRequestEnabled
  长名称: ''
  描述: |
    Specifies whether DCM provide a means for support of virtual requests.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will provide an API set to allow virtual requests to be made from the
    application (i.e. for external RoE implementation).
    
    Constraints:
    -----------------------------------------
    none
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    If enabled Dcm run time during request reception and diagnostic service post-processing will be
    insignificantly increased.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: DcmSupportedIDCalculationSuppressionEnabled
  长名称: ''
  描述: |
    Specifies whether DCM shall omit the automatic "supported parameter ID" calculation.
    
    Note: This option does not affect the WWH-OBD automatic calculation of the "SupportedIDs".
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will NOT calculate the "supported parameter ID" and not handle internally the
    corresponding reporting services.
    
    Constraints:
    -----------------------------------------
    The "supported parameter ID" feature is only available for certain customers. For all others
    this option will not have any effect.
    Please refer to the technical reference to find out whether this option is applicable for your
    project or not (if not documented).
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor decrease of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    Enabling this feature leads to a minor decrease of the Dcm data ROM usage.
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: DcmDtrDataProvisionViaDemEnabled
  长名称: DTR Data Provision via DEM Enabled
  描述: |
    Specifies whether DCM or DEM handles the OBD MID DTR data acquisition.
    
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will interact with the Dem on each request for OBD MID DTR value retrieval (i.e.
    SID 0x06 or DID 0xF600). This corresponds to the behavior described in the AR 4.2.2 DCM SWS.
    If disabled, Dcm uses the OBD MID configuration defined by this BSWMD file and invokes the
    corresponding application callouts to get the DTR values.
    
    Constraints:
    -----------------------------------------
    If this feature is enabled:
    - any available in the Dcm configuration OBD MIDs will be ignored.
    - any available in the Dcm configuration OBD MID DIDs (DID in range 0xF600-0xF6XX) will be
    ignored, but Dcm will redirect any request of such a DID to the Dem.
      -  This implies that no DID in this range shall have other application than the one specified
    for OBD MID handling.
    
    Dependencies:
    -----------------------------------------
    This option has any effect only if the ECU project is licensed for OBD purposes.
    
    Runtime effects:
    -----------------------------------------
    Depending on the option state, a completely different implementation will be used for the OBD
    MID DTR value reading. If this option is enabled, the runtime usage will mostly depend on the
    Dem implementation efficiency.
    
    Code ROM usage effects:
    ------------------------------------
    Depending on the option state, a completely different implementation will be used for the OBD
    MID DTR value reading. Some small increase of code ROM usage can be expected.
    
    Const data ROM usage effects:
    -----------------------------------------
    If this option is enabled, the amount of OBD MID DIDs is drastically reduced (to a single range
    DID). Also DCM internal tables for MID information will no more be generated, thus the overall
    result is a significant ROM data usage reduction.
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    If this option is enabled, the stack usage will now include the Dem APIs stack usage which will
    now call the application to gather the DTR values, thus at least a small stack usage increase is
    expected.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: DcmForeignDiagnosticRequestDetectionEnabled
  长名称: ''
  描述: |
    Specifies whether DCM shall listen for diagnostic requests to other ECUs.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will monitor for diagnostic requests, sent from one of its related clients, but
    addressed to other ECU on the network. Depending on the TP connection type, the effect will be
    to cancel any already in processing jobs from this client.
    
    Constraints:
    -----------------------------------------
    Currently this feature shall be enabled only if:
    - Vector MSR3/4 CanTp is used in the ECU project
    AND
    - Dcm shall communicate over at least one "Mixed11Addressing" CanTp connection.
    
    Dependencies:
    -----------------------------------------
    A Vector MSR4/MSR3 CanTp is used in the ECU project (not only in Configurator5).
    
    Runtime effects:
    -----------------------------------------
    If enabled, the CanTp_RxIndication() function will take slightly longer due to the additional
    call to the Dcm.
    
    Code ROM usage effects:
    ------------------------------------
    If enabled, Dcm code ROM usage will slightly increase due to the additional functionality within
    this TP callout.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: DcmSuppressResponseOnCanTpFuncMixedAddrRequests
  长名称: ''
  描述: |
    Specifies whether DCM shall suppress any response on a functionally addressed request made over
    a MixedAddressing CanTp connection.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm will not send a response to a functionally addressed request from a client using
    ISO15765-2 MixedAddressing. This is useful for system network concepts using shared CANids for
    all ECUs accessible by a particular client.
    
    Constraints:
    -----------------------------------------
    Currently this feature shall be enabled only if:
    - ASR CanTp is used in the ECU project
    AND
    - Dcm shall communicate over at least one "MixedAddressing" CanTp connection.
    AND
    - The ISO15765-2 design with shared Rx/Tx diagnostic CANids for all servers per single client is
    chosen.
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    If enabled, the Dcm runtime usage will insignificantly increase due to the small additional code
    added by this functionality.
    
    Code ROM usage effects:
    ------------------------------------
    If enabled, the Dcm code ROM usage will insignificantly increase due to the small additional
    code added by this functionality.
    
    Const data ROM usage effects:
    -----------------------------------------
    If enabled, the Dcm code ROM usage will insignificantly increase due to the small additional
    data added by this functionality.
    
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: DcmSenderReceiverPRPortsEnabled
  长名称: ''
  描述: |
    Specifies whether Dcm shall generate separate P-Port and R-port or a single PR-Port for
    Sender-Receiver DID that has read and write operations of data services or IO control request
    interfaces.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm shall generate a single PR-Port for Sender-Receiver DID that has read, write,
    and if configured IO control operations.
    If disabled, Dcm shall generate separate P-Port and R-Port for Sender-Receiver DID that has
    read, write, or IO control operations.
    
    Constraints:
    -----------------------------------------
    PR-Ports for Sender-Receiver interface are not applicable in AR3.
    
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
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: DcmMaxNumberOfThreads
  长名称: ''
  描述: |
    Specifies how many thread resources will be reserved for parallel service processing.
    The configured value represents the limit for the number of protocols that can be processed in
    parallel.
    
    Effect:
    -----------------------------------------
    Dcm allocates resources in form of global variables to be able to process multiple service
    requests in parallel.
    
    Constraints:
    -----------------------------------------
    This value is only relevant for Postbuild-Loadable configurations and allows to configure
    additional protocols in Postbuild phase.
    Therefore the value must be set to the overall number of protocols inclusive the ones added
    during Postbuild phase.
    
    Dependencies:
    -----------------------------------------
    Whether protocols can be processed in parallel is defined by
    /Dcm/DcmConfigSet/DcmGeneral/DcmParallelProtocolProcessingEnabled
    
    Runtime effects:
    -----------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    Increasing this number leads to a slightly increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    Increasing this number leads to a slightly increase of the Dcm data ROM usage.
    
    Global RAM usage effects:
    -----------------------------------------
    Increasing this number leads to a massive increase of global RAM usage.
    
    Stack RAM usage effects:
    -----------------------------------------
    none
  默认值: 1
  最小值: 1
  最大值: 16
- 
  序号: 29
  名称: DcmTypedDataInterfacesEnabled
  长名称: ''
  描述: |
    Specifies whether Dcm shall use typed data interfaces for DIDs in general or not.
    
    Effect:
    -----------------------------------------
    If enabled, Dcm shall generate typed data interfaces for DID signals.
    If disabled, Dcm shall generate uint8-array-typed interfaces for DID signals.
    
    Constraints:
    -----------------------------------------
    none
    
    Dependencies:
    -----------------------------------------
    This option has only an effect if DspDataUsePort is set to either:
      - USE_DATA_ASYNCH_CLIENT_SERVER or
      - USE_DATA_SYNCH_CLIENT_SERVER or
      - USE_DATA_SENDER_RECEIVER or
      - USE_DATA_NV_DATA_INTERFACE
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature may lead to a major increase of the runtime.
    The amount of additional runtime depends on the DcmDspDataType and DcmDspDataSize of the
    configured DcmDspData elements using this feature.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    Enabling this feature can lead to a major increased stack size required by the Dcm_MainFunction.
    The amount of additional RAM usage depends on the DcmDspDataType and DcmDspDataSize of the
    configured DcmDspData elements using this feature.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: DcmKeepAliveTimeStartOnFunc3E80
  长名称: Keep Alive Time Start On Func 3E 80
  描述: |
    Specifies whether a functional TesterPresent request with suppressed bit set (0x3E 80) starts
    the KeepAliveTimer during which the Dcm will keep the Diag-Active user in ComM registered or
    not, when the timer was in idle before.
    
    Effect:
    ------------------------------------
    If this parameter is enabled, a functional TesterPresent request with suppressed bit set (0x3E
    80) will start the KeepAliveTimer when the ECU was in inactive diagnostic state before.
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    This option has only an effect if DcmDspKeepAliveTime is configured and not 0.
    
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
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: DcmAutosarVersion
  长名称: ''
  描述: |
    Specifies whether DCM shall be based on the AUTOSAR version 4.2.1 and older, AUTOSAR version
    4.2.2 or AUTOSAR version R19-11 and newer.
    
    Effect:
    ------------------------------------
    Mainly affects the signatures of some interfaces and port operations, like:
    - Module_DiagnosticService()
    - Module_DiagnosticService_SubService()
    - Dcm_ReadMemory()
    - Dcm_WriteMemory()
    - Dcm_SetProgConditions()
    - Xxx_Indication()
    - Xxx_Confirmation()
    - Xxx_StartProtocol()
    - Xxx_GetInfoTypeValueData()
    
    Constraints:
    ------------------------------------
    none
    
    Dependencies:
    ------------------------------------
    This parameter has impact on the whole Dcm functionality and API parameters.
    Please note, that the interface towards Dem can be configured independently by DcmDemApiVersion.
    
    
    Runtime effects:
    ------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    Code ROM usage slightly vary between Dcm AR versions due to different API specifications.
    
    Const data ROM usage effects:
    ------------------------------------
    none
    
    Global RAM usage effects:
    ------------------------------------
    none
    
    Stack RAM usage effects:
    ------------------------------------
    none
  默认值: AUTOSAR_4_02_02
  最小值: ''
  最大值: ''
- 
  序号: 32
  名称: DcmParallelProtocolProcessingEnabled
  长名称: ''
  描述: |
    Specifies whether all protocols can be processed in parallel during the Default Session.
    
    Effect:
    -----------------------------------------
    If enabled, service requests of all protocols in default session will be processed in parallel.
    Dcm will not cancel ongoing service requests from protocols of lower priority.
    
    Constraints:
    -----------------------------------------
    Not all UDS services can be processed in parallel.
    This feature enforces a Dem interface with AUTOSAR version 4.3.0 or newer. See the technical
    reference for more details.
    
    Dependencies:
    -----------------------------------------
    The maximum number of protocols that can be processed in parallel for postbuild configurations
    shall be configured here:
    /Dcm/DcmConfigSet/DcmGeneral/DcmMaxNumberOfThreads
    
    Runtime effects:
    -----------------------------------------
    If enabled, the runtime will insignificantly increase.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a slightly increase of the Dcm static code ROM usage.
    
    Const data ROM usage effects:
    -----------------------------------------
    Enabling this feature leads to a slightly increase of the Dcm data ROM usage.
    
    Global RAM usage effects:
    -----------------------------------------
    Enabling this feature leads to a massive increase of the Dcm global RAM usage.
    
    Stack RAM usage effects:
    -----------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 33
  名称: DcmHeaderFileInclusion
  长名称: ''
  描述: |
    Name of the header file(s) to be included by the Dcm configuration files.
    
    Effect:
    ------------------------------------
    Can affect the whole Dcm configuration files, depending on the included headers.
    
    Constraints:
    ------------------------------------
    Should be only used to include header files, which provide the symbol definitions used for
    DcmDspReadMemoryRangeByLabelInfo or DcmDspWriteMemoryRangeByLabelInfo containers.
    
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
```

### 105. DcmSecurityEventRefs

**描述**: Container for the references to IdsMEvent elements representing the security events that the Dcm
module shall report to the IdsM in case the coresponding security related event occurs (and if
DcmEnableSecurityEventReporting is set to "true").

该容器没有参数。

### 106. DcmSecureCoding

**描述**: Contains references to diagnostic elements that are used for the secure coding process.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmSecureCodingDataBufferSize
  长名称: ''
  描述: Provides the size of the Dcm internal buffer to store data during the secure coding sequence.
  默认值: 3
  最小值: 3
  最大值: 4294967295
```

### 107. DcmPageBufferCfg

**描述**: This container contains the configuration (parameters) for Page Buffer handling

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmPagedBufferEnabled
  长名称: ''
  描述: |
    Specifies whether the Dcm will use the page buffer mechanism for transmitting the response data
    (only for reading fault memory).
    
    Effect:
    -----------------------------------------
    By enabling this feature Dcm will process the fault memory reading diagnostic services in a way
    which reduces the need of large Dcm buffers, but can lead to a different communication behavior.
    
    Constraints:
    -----------------------------------------
    It is recommended to leave this feature enabled if the ECU shall support large amount of DTCs
    and the Dcm shall handle service 0x19 internally. In some cases where the ECU has a minimum
    amount DTC configuration this option an be turned off to save ROM and runtime resources.
    
    Dependencies:
    -----------------------------------------
    Makes sense to be enabled only if the diagnostic service 0x19 is available in the configuration
    and it is handled by Dcm internally i.e. its parameter
    "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSidTabFnc" is left empty.
    
    Runtime effects:
    -----------------------------------------
    If enabled the Dcm task will have increased runtime usage while executing diagnostic service
    0x19 with a positive response.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a minor increase of the Dcm ROM usage, caused by the additional
    functionality.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    Enabling this feature leads to a minor increase of the Dcm RAM usage, caused by the additional
    functionality management storage.
    
    Stack RAM usage effects:
    -----------------------------------------
    Enabling this feature can lead to a minor increase of the Dcm task stack usage, caused by the
    additional functions to be executed within the diagnostic service data providers.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmPagedBufferTimeout
  长名称: ''
  描述: NOT USED
  默认值: 0
  最小值: 0
  最大值: 1000
```

### 108. DcmProcessingConditions

**描述**: This container contains the configuration ( DSP parameter) for mode arbitration functionality of the
Dcm

Effect:
-----------------------------------------
Using this configuration option, the Dcm will be able to verify any ECU states beyond the diagnostic
session and security access before executing a diagnostic request.

Constraints:
-----------------------------------------
none

Dependencies:
-----------------------------------------
none

Runtime effects:
-----------------------------------------
The usage of processing conditions leads to an increase of Dcm task the runtime during the
diagnostic request evaluation. The amount of time needed, depends on the condition expression
complexity.

Code ROM usage effects:
------------------------------------
The usage of processing conditions leads to a insignificant increase of ROM usage in the static
code.

Const data ROM usage effects:
-----------------------------------------
The usage of processing conditions leads to a scalable increase of ROM usage in the Dcm
configuration part.

Global RAM usage effects:
-----------------------------------------
none

Stack RAM usage effects:
-----------------------------------------
none


该容器没有参数。

### 109. DcmModeCondition

**描述**: This container contains the configuration of a mode condition which can be used as argument in
DcmModeRules.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmConditionType
  长名称: ''
  描述: |
    Specifies what kind of comparison that is made for the evaluation of the mode condition.
    
    Effect:
    -----------------------------------------
    The generated code will reflect this parameter by using different logical expressions.
    
    Constraints:
    -----------------------------------------
    none
    
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
  默认值: DCM_EQUALS
  最小值: ''
  最大值: ''
```

### 110. DcmModeRule

**描述**: This container contains the configuration of a mode rule which represents a logical expression with
DcmModeConditions or other DcmModeRules as arguments.

Effect:
-----------------------------------------
Using this configuration option, the Dcm will be able to verify any ECU states beyond the diagnostic
session and security access before executing a diagnostic request.

Constraints:
-----------------------------------------
none

Dependencies:
-----------------------------------------
none

Runtime effects:
-----------------------------------------
The usage of processing conditions leads to an increase of Dcm task the runtime during the
diagnostic request evaluation. The amount of time needed, depends on the condition expression
complexity.

Code ROM usage effects:
------------------------------------
The usage of processing conditions leads to an insignificant increase of ROM usage in the static
code.

Const data ROM usage effects:
-----------------------------------------
The usage of processing conditions leads a scalable increase of ROM usage in the Dcm configuration
part, depending on the configuration.

Global RAM usage effects:
-----------------------------------------
none

Stack RAM usage effects:
-----------------------------------------
The usage of processing conditions can lead to an minor increase of required stack size by the
Dcm_MainFunction in the static code. The concrete amount depends on the configured rule cascading
depth.


#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmLogicalOperator
  长名称: ''
  描述: |
    This parameter specifies the logical operator to be used in the logical expression. If the
    expression only consists of a single condition this parameter shall not be used.
    
    Effect:
    -----------------------------------------
    The generated code will reflect this parameter by using different logical expressions.
    
    Constraints:
    -----------------------------------------
    none
    
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
  默认值: DCM_AND
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmModeRuleNrcValue
  长名称: ''
  描述: |
    Optional parameter which defines the NRC to be sent in case the mode rule condition is not
    valid.
    
    Effect:
    -----------------------------------------
    The generated code will reflect this parameter by using different NRC return values.
    
    Constraints:
    -----------------------------------------
    none
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    If NRC specified, the generated rule checking function will need insignificantly longer
    execution time.
    
    Code ROM usage effects:
    ------------------------------------
    If NRC specified, the generated rule checking function will need insignificantly more ROM.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    If NRC specified, the generated rule checking function will need insignificantly more stack.
  默认值: 34
  最小值: 0
  最大值: 255
```

### 111. DcmMiscellaneous

**描述**: This container includes all parameters that may override/disable some standard DCM features.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmSendingNrc7e7fOnFuncRequestEnabled
  长名称: ''
  描述: |
    Specifies whether NRC 0x7E and 0x7F shall be responded on functional requests.
    
    Effect:
    -----------------------------------------
    By enabling this feature Dcm will respond with NRC 0x7E resp. 0x7F on functional requests.
    Note: This behavior contradicts with the ISO14229-1:2013.
    
    Constraints:
    -----------------------------------------
    It is recommended to leave this feature disabled to achieve maximum ISO14229-1:2013 compliance.
    
    Dependencies:
    -----------------------------------------
    For some OEMs DCM is already pre-configured to use the matching behavior (i.e. already enables
    this feature).
    
    Runtime effects:
    -----------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a very small decrease of the Dcm ROM usage, caused by the
    additional functionality deactivated.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    none
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmAcceptingOtherClientsDuringNonDefaultSessionEnabled
  长名称: ''
  描述: |
    Specifies whether DCM shall accept requests from clients other than the one that has initiated a
    non-default session.
    
    Effect:
    -----------------------------------------
    By enabling this feature Dcm will accept also requests from other clients belonging to the same
    DcmDslProtocolRow while the ECU is a non-default session.
    Note: This behavior contradicts with the AR DCM SWS and ISO14229-1.
    
    Constraints:
    -----------------------------------------
    It is recommended to leave this feature disabled to achieve maximum AR resp. ISO14229-1
    compliance.
    
    Dependencies:
    -----------------------------------------
    For some OEMs DCM is already pre-configured to use the matching behavior (i.e. already enables
    this feature).
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature may slightly decrease the DCM run time on request reception/processing.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a small decrease of the Dcm ROM usage, caused by the additional
    functionality deactivated.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmOmitComControlCurrentChannelParamEnabled
  长名称: ''
  描述: |
    Specifies whether DCM shall not accept CommunicationType parameter value "current channel"
    (0xFx).
    
    Effect:
    -----------------------------------------
    By enabling this feature Dcm will respond with NRC 0x31 on a valid request for SID 0x28 with
    communication type parameter set to 0xFx.
    
    Constraints:
    -----------------------------------------
    It is recommended to leave this feature disabled to achieve maximum OEM/ISO14229-1 and AR
    compatibility.
    
    Dependencies:
    -----------------------------------------
    This switch has any effect only if SID 0x28 is to be supported by the ECU and internally handled
    by DCM.
    
    Runtime effects:
    -----------------------------------------
    Enabling this feature may slightly decrease the DCM run time on request for SID 0x28.
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a small decrease of the Dcm ROM usage, caused by the additional
    functionality deactivated.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    none
    
    Stack RAM usage effects:
    -----------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmHighPerformancePeriodicTxEnabled
  长名称: ''
  描述: NOT USED
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DcmSpecificCauseCodeEnabled
  长名称: ''
  描述: |
    Specifies whether DCM shall support an additional byte (specific cause code) for negative
    response messages.
    
    Effect:
    -----------------------------------------
    By enabling this feature Dcm will allow the application to register an additional cause code for
    a negative response message.
    
    Constraints:
    -----------------------------------------
    none
    
    Dependencies:
    -----------------------------------------
    none
    
    Runtime effects:
    -----------------------------------------
    none
    
    Code ROM usage effects:
    ------------------------------------
    Enabling this feature leads to a small increase of the Dcm ROM usage, caused by the additional
    functionality activated.
    
    Const data ROM usage effects:
    -----------------------------------------
    none
    
    Global RAM usage effects:
    -----------------------------------------
    Enabling this feature leads to a small increase of the Dcm RAM usage.
    
    Stack RAM usage effects:
    -----------------------------------------
    none
  默认值: false
  最小值: ''
  最大值: ''
```

