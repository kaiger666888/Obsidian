# ComM

## 模块描述

Configuration of the ComM (Communication Manager) module.

## 容器列表

### 1. ComMConfigSet

**描述**: This container is the base for a multiple configuration set.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMPncEnabled
  长名称: ''
  描述: |
    This parameter defines whether in this configuration set the Partial Networking is enabled.
    Dependency: this parameter is not used if Implementation Variant of ComM module is PreCompile or
    if parameter 'Pnc Support' is de-activated.
    
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. ComMChannel

**描述**: This container includes the configuration parameters of a ComM channel. The parameters shall be
harmonized within the whole communication stack.
The 'Short Name' is used to compose a channel handle (#define) which is published in ComM_Lcfg.h
during generation and has the format ComMConf_ComMChannel_<Short Name>.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMBusType
  长名称: ''
  描述: |
    This parameter defines the bus type of the channel.
    
    Note: COMM_BUS_TYPE_INTERNAL shall be configured if the channel is used for internal
    communication. Such channels have no corresponding bus interface.
  默认值: COMM_BUS_TYPE_CAN
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComMChannelId
  长名称: ''
  描述: This value specifies the channel identification number of the corresponding channel.
      Identification numbers must be unique and consecutive.
  默认值: 255
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: ComMFullCommRequestNotificationEnabled
  长名称: ''
  描述: |
    This parameter defines if the optional SenderReceiver Port of Interface
    ComM_CurrentChannelRequest will be provided for this channel.
    Dependency: The value must be false if 'Nm Variant' of the channel is PASSIVE (in this case the
    channel cannot be requested by users).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComMGlobalNvmBlockDescriptor
  长名称: ''
  描述: |
    Not used!
    ComM always stores the wake-up inhibition state of the channel in the block pointed to by
    ComMGlobalNvmBlockDescriptor.
    
    This parameter defines if the wake-up inhibition state of the channel shall be stored (in some
    implementation specific way) in the block pointed to by ComMGlobalNvmBlockDescriptor.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComMMainFunctionPeriod
  长名称: ''
  描述: |
    This value specifies the period that the MainFunction has to be triggered with.
    Comment: ComM scheduling shall be at least as fast as the communication stack.
  默认值: 0.02
  最小值: 0.001
  最大值: 0.1
- 
  序号: 6
  名称: ComMNoCom
  长名称: ''
  描述: |
    This parameter defines if the mode limitation for this channel is enabled. The value is set at
    initialization time and can be changed during runtime with ComM_LimitChannelToNoComMode() or
    ComM_LimitECUToNoComMode(). Note that the value of runtime variable is not stored in NVRAM (not
    kept during a reset).
    Dependency: If enabled, the parameter ComMModeLimitationEnabled shall be enabled as well.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: ComMNoWakeup
  长名称: ''
  描述: |
    This parameter defines if the wake-up inhibition for this channel is enabled. The parameter
    defines the default value, which is set only once at first ECU initialization or if the
    non-volatile data cannot be restored. The value can be changed during runtime with
    ComM_PreventWakeUp(). The current value can be stored in NVRAM (kept during a reset) if
    ComMGlobalNvMBlockDescriptor is configured.
    Dependency: If enabled, the parameter ComMWakeupInhibitionEnabled shall be enabled as well.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: ComMPncGatewayType
  长名称: ''
  描述: |
    This parameter defines the Partial Network Gateway behavior of this channel.
    
    Note: ComM does only allow coordinated ComMPncs with either all referenced ComMChannels having
    the ComMPncGatewayType set to COMM_GATEWAY_TYPE_NONE or no referenced ComMChannel has
    COMM_GATEWAY_TYPE_NONE set.
  默认值: COMM_GATEWAY_TYPE_NONE
  最小值: ''
  最大值: ''
```

### 3. ComMNetworkManagement

**描述**: This container includes the ComM configuration parameters for Network Management.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMNmLightTimeout
  长名称: ''
  描述: |
    This parameter is only available if Nm Variant is LIGHT.
    This value specifies the time duration spent in the COMM_FULL_COMMUNICATION sub-state
    COMM_FULL_COM_READY_SLEEP before ComM triggers the network shutdown.
    If the value is 0.0, ComM omits the state COMM_FULL_COM_READY_SLEEP.
    
    Dependency: the next state depends on the optional parameter ComMNmLightSilentTimeout.
  默认值: 10
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: ComMNmVariant
  长名称: ''
  描述: |
    This parameter defines which Network Management variant is supported on the channel:
    - FULL, AUTOSAR NM is used.
    - PASSIVE, AUTOSAR NM is used, but the ECU is not allowed to keep the network awake. It is not
    allowed to assign users to this channel. ComM ignores communication requests from DCM on this
    channel. The parameter ComMNoCom of the channel has to be set to true.
    - LIGHT, no AUTOSAR NM is used, but the shutdown is synchronized via timeout, which is
    configured with the parameter ComMNmLightTimeout.
    - NONE, no AUTOSAR NM is used and no shutdown synchronization is available. I.e. once a channel
    reached the COMM_FULL_COMMUNICATION mode, it will never leave it. Stop of communication is done
    via power off or reset. ComM ignores user requests of COMM_NO_COMMUNICATION mode and requests
    for No Communication Mode Limitation.
    - LINSLAVE, no AUTOSAR NM is used but LIN slave use case. Shutdown is synchronized by LIN
    master. Cannot keep the bus awake but LIN State Manager restarts wakeup repetition.
    Note: The parameter shall be harmonized with the configuration of Network Management modules (if
    any).
    Dependencies:
    For channels with Bus Type INTERNAL only the Nm Variant LIGHT is supported.
    For managing channels (see ComMManageReference), the ComMNmVariant FULL shall be configured.
    For managed channels (see ComMManageReference), the ComMNmVariant LIGHT shall be configured.
  默认值: FULL
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComMPncNmRequest
  长名称: ''
  描述: |
    This parameter defines if every time a Full Communication is requested due to a change in the
    PNC state machine to COMM_PNC_REQUESTED Nm shall be called using the API Nm_NetworkRequest(),
    even if the channel is already in Full Communication.
    Dependency: this parameter is considered only if 'Pnc Support' is activated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComMNmLightSilentTimeout
  长名称: ''
  描述: |
    This value specifies the time duration spent in the COMM_SILENT_COMMUNICATION state after
    leaving COMM_FULL_COM_READY_SLEEP state and before entering COMM_NO_COMMUNICATION state.
    The COMM_SILENT_COMMUNICATION state can be left in three ways:
    - The ComMNmLightSilentTimeout elapses: COMM_NO_COMMUNICATION is entered
    - On internal Full Comm request: COMM_FULL_COMMUNICATION is entered
    - On Dcm Diagnostics Active indication: COMM_FULL_COMMUNICATION is entered
    
    This is similar to the Prepare Bus Sleep Phase when Network Management is used.
    
    If the value is 0.0 or this parameter is missing, ComM omits the state COMM_SILENT_COMMUNICATION
    and enters COMM_NO_COMMUNICATION directly.
    
    Restrictions: This parameter is only available for Bus Type CAN with Nm Variant LIGHT.
  默认值: 1.5
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: ComMTMinFullComModeDurationOfChannel
  长名称: ''
  描述: |
    This value specifies the minimum time duration, spent in the COMM_FULL_COMMUNICATION sub-state
    COMM_FULL_COM_NETWORK_REQUESTED. The parameter is only available for channels with Nm Variants
    FULL and LIGHT.
    - If the channel has Nm Variant LIGHT, this parameter is used instead of the global TMin Full
    Com Mode Duration.
    - If the channel has Nm Variant FULL, it is recommended
    -- to use this parameter if the corresponding BusNm does not support the Repeat Message Time
    functionality (e.g. NmOsek).
    -- not to use this parameter if the corresponding BusNm supports the Repeat Message Time
    functionality (e.g. CanNm, FrNm or UdpNm).
  默认值: 5
  最小值: 0.001
  最大值: 65
```

### 4. ComMUserPerChannel

**描述**: This container includes a reference to a ComMUser that is assigned to this channel.

该容器没有参数。

### 5. ComMPnc

**描述**: This container includes the configuration of a Partial Network Cluster (PNC).
The 'Short Name' is used to compose a PNC handle (#define) which is published in ComM_Lcfg.h during
generation and has the format ComMConf_ComMPnc_<Short Name>.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMPncId
  长名称: ''
  描述: |
    This value specifies the partial network cluster (PNC) identification number. The number defines
    the bit position of the PNC status information in bit vectors EIRA and ERA.
    
    The concrete meaning depends on the value of the parameter ComMPncIdCounting. The example shows
    which PNC ID corresponds to the bit position 0 (LSB) in the bit vectors:
    - if ComMPncIdCounting = COMM_PNC_ID_COUNT_FROM_PNC_VECTOR, status information of PNC with
    ComMPncId = 0 is stored.
    - if ComMPncIdCounting = COMM_PNC_ID_COUNT_FROM_NM_MESSAGE, status information of PNC with
    ComMPncId = (Pnc Vector Offset * 8) is stored.
  默认值: ''
  最小值: 0
  最大值: 511
```

### 6. ComMPncComSignal

**描述**: This container includes PncComSignals which are used to communicate the EIRA and ERA status of this
PNC.
The following rules shall be considered:
- ERA is only needed if ComMPncGatewayEnabled is set to true and only for PNCs, which are assigned
to multiple ComM channels. In this case a separate PncComSignal with ComMPncComSignalKind = ERA and
ComMPncComSignalDirection = RX shall be configured for each channel assigned to the PNC.
- A separate PncComSignal with ComMPncComSignalKind = EIRA and ComMPncComSignalDirection = TX shall
be configured for each channel that is assigned to the PNC and has ComMNmVariant = FULL.
- A separate PncComSignal with ComMPncComSignalKind = EIRA and ComMPncComSignalDirection = RX shall
be configured for each bus type (e.g. one for CAN and one for FR if both CAN and FR channels are
assigned to the PNC).

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMPncComSignalDirection
  长名称: ''
  描述: This parameter defines the communication direction of this PncComSignal.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComMPncComSignalKind
  长名称: ''
  描述: This parameter defines whether this PncComSignal represents EIRA or ERA PNC information.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComMUseSignalIndependentlyOfChannelAssignment
  长名称: ''
  描述: |
    This parameter is only relevant:
     - if ComMPncExtendedFunctionalityEnabled is set to true and
     - the ComMPncComSignal is an ERA RX signals or an EIRA TX signal and
     - the ComMPncComSignal is configured for a ComMChannel which is not referenced by the ComMPnc.
    
    If all of the above conditions are true, this parameter has the following meaning:
    - If it is set to true, the signal will be used by the PNC (even if the ComMPnc has no
    ComMChannelPerPnc reference to the corresponding channel)
    -- For EIRA TX signals, this means that the corresponding PNC bit will be set in the signal data
    -- For ERA RX signals, this means that reception of a corresponding PNC bit will lead to
    activation of the PNC.
    - If it is set to false, the signal will NOT be used by the PNC
    -- For EIRA TX signals, this means that the corresponding PNC bit will not be set in the signal
    data
    -- For ERA RX signals, this means that reception of a corresponding PNC bit will not lead to
    activation of the PNC.
    
    Note: EIRA RX signals are always evaluated by ComM. If EIRA RX signals shall not be considered
    for some PNCs, a corresponding filter mask shall be defined in the BusNm.
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. ComMUser

**描述**: This container includes the information of a ComM User which is designated to request Communication
modes.
The 'Short Name' is used to compose a user handle (#define) which is published in ComM_Lcfg.h during
generation and has the format ComMConf_ComMUser_<Short Name>.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMUserIdentifier
  长名称: ''
  描述: |
    This value specifies the identifier that is needed to refer to a user in the system which is
    designated to request Communication Modes.
    
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: ComMUserModeNotification
  长名称: ''
  描述: This parameter defines if the mode notification to this user is enabled.
  默认值: false
  最小值: ''
  最大值: ''
```

### 8. ComMGeneral

**描述**: General configuration parameters of the Communication Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMDevErrorDetect
  长名称: ''
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    true:   Development error detection is enabled.
    false:  Development error detection is disabled.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComMDirectUserMapping
  长名称: ''
  描述: |
    Not used!
    
    This parameter defines if the configuration tool shall automatically create a ComMUser per
    ComMPnc and a ComMUser per ComMChannel.
    The 'Short Name' of the generated ComMUsers shall follow the following naming convention:
    PNCUser_ComMPncId, e.g. PNCUser_13
    ChannelUser_ComMChannelId, e.g. ChannelUser_25
    
    Restriction: ComMUser, which are created due to this configuration parameter, shall not be used
    by SWCs (only available for BswM).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComMEcuGroupClassification
  长名称: ''
  描述: |
    This value specifies whether a mode inhibition affects the ECU or not.
    0, not affected by mode inhibition
    1, only affected by the bus wake-up inhibition
    2, only affected by the mode limitation
    3, affected by both mode inhibitions above.
    
    The parameter defines the default value, which is set only once at first ECU initialization or
    if non-volatile data cannot be restored. It can be changed during runtime with
    ComM_SetECUGroupClassification().
    The current value can be stored in NVRAM (kept during a reset) if ComMGlobalNvMBlockDescriptor
    is configured.
    Note that the parameter does not control the availability of mode inhibition functionality. The
    functionality has to be enabled with parameters ComMModeLimitationEnabled and
    ComMWakeupInhibitionEnabled if needed.
  默认值: 3
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: ComMModeLimitationEnabled
  长名称: ''
  描述: |
    This parameter defines if Mode Limitation functionality shall be enabled.
    Dependencies:
    - If the value is true, the optional parameter ComMGlobalNvMBlockDescriptor can be configured.
    - The value shall be true if ComMNmVariant is PASSIVE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComMPncGatewayEnabled
  长名称: ''
  描述: This parameter defines if support of Partial Network Gateway is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: ComMPncPrepareSleepTimer
  长名称: ''
  描述: This value specifies the time the PNC state machine shall wait in COMM_PNC_PREPARE_SLEEP.
  默认值: 5
  最小值: 0
  最大值: 63
- 
  序号: 7
  名称: ComMPncSupport
  长名称: ''
  描述: This parameter defines if support of Partial Networking is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: ComMSynchronousWakeUp
  长名称: ''
  描述: |
    This parameter defines if a wake-up of one channel shall lead to a wake-up of all channels.
    Dependency: The value must be false if J1939 Network Management is used on a ComM channel and no
    AUTOSAR Network Management is used on this channel.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: ComMTMinFullComModeDuration
  长名称: ''
  描述: |
    This value specifies the minimum time duration, spent in the COMM_FULL_COMMUNICATION sub-state
    COMM_FULL_COM_NETWORK_REQUESTED.
    The parameter is only available for channels with ComMNmVariant = LIGHT.
  默认值: 5
  最小值: 0.001
  最大值: 65
- 
  序号: 10
  名称: ComMVersionInfoApi
  长名称: ''
  描述: This parameter enables/disables the function ComM_GetVersionInfo() to get major, minor and
      patch version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: ComMWakeupInhibitionEnabled
  长名称: ''
  描述: |
    This parameter defines if the wake-up inhibition functionality is enabled.
    Dependency: If the value is true, the optional parameter ComMGlobalNvMBlockDescriptor can be
    configured.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: ComMUserConfigurationFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation to ComM_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file ComM_Cfg.h and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: ComMNmPassiveModeEnable
  长名称: ''
  描述: |
    This parameter defines the possible values of the parameter ComMNmVariant:
    true: the values of ComMNmVariant are limited to LIGHT, NONE and PASSIVE.
    false: the values of ComMNmVariant are limited to LIGHT, NONE and FULL.
    If the parameter does not exist, all values of ComMNmVariant are potentially possible, as long
    as consistency with Network Management modules and consistency within ComM module itself is
    ensured.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: ComMOperationGetInhibitionStatusEnabled
  长名称: ''
  描述: |
    This parameter defines whether the client-server interface ComM_ChannelWakeUp contains the
    operation GetInhibitionStatus.
    true: the interface ComM_ChannelWakeUp contains the operation GetInhibitionStatus. This is the
    default value.
    false: the interface ComM_ChannelWakeUp does not contain the operation GetInhibitionStatus.
    If the parameter does not exist, the behavior is as if the value were true.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: ComMPncIdCounting
  长名称: ''
  描述: |
    This parameter specifies the meaning of the ComMPncId parameters.
    
    - If this parameter is set to COMM_PNC_ID_COUNT_FROM_PNC_VECTOR, then PNC IDs are counted from
    the beginning of the PNC Vector. The range of valid PNC IDs then goes from 0 to (8 * (#bytes in
    Pnc Vector)) - 1. This corresponds to the PNC ID handling as specified in AUTOSAR Specifications
    Version 4.0.x.
    - If this parameter is set to COMM_PNC_ID_COUNT_FROM_NM_MESSAGE, then PNC IDs are counted from
    the beginning of the NM Message. The range of valid PNC IDs then goes from (8 * Pnc Vector
    Offset) to (8 * (Pnc Vector Offset + #bytes in Pnc Vector)) - 1. This corresponds to the PNC ID
    handling as specified in AUTOSAR Specifications since Version 4.1.x.
  默认值: COMM_PNC_ID_COUNT_FROM_PNC_VECTOR
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: ComMPncExtendedFunctionalityEnabled
  长名称: ''
  描述: |
    This parameter specifies if Extended Partial Networking functionality is enabled. Please refer
    to the Startup User Manual for further information.
    Dependency: The value must be false if 'Pnc To Channel Routing Limitation Enabled' is true.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: ComMPncToChannelRoutingLimitationEnabled
  长名称: ''
  描述: |
    Enables or disables support of Partial Network Routing Limitation feature.
    
    False:
    Partial Network Routing Limitation is disabled. This is the default setting. In this case ComM
    will route Partial Networking requests to all channels mapped to the Partial Network according
    to AUTOSAR specification. The API ComM_LimitPncToChannelRouting() is not available.
    
    True:
    Partial Network Routing Limitation is enabled. In this case it is possible to limit the routing
    of Partial Networking requests on particular channels mapped to the Partial Network. The API
    ComM_LimitPncToChannelRouting() is available.
    If a Partial Network is requested, the behavior depends on the current limitation status of a
    channel:
    - if not limited, ComM keeps the channel awake and Nm sends its message containing PN request
    information as defined by AUTOSAR.
    - if limited, ComM does not keep the channel awake and Nm does not send its message.
    
    Dependencies:
    - The value must be false if 'Pnc Extended Functionality Enabled' is true.
    - The feature can be enabled only if 'Pnc Gateway Enabled' is set to true.
    - The feature is only available for channels having 'Pnc Gateway Type' set to
    COMM_GATEWAY_TYPE_ACTIVE or COMM_GATEWAY_TYPE_PASSIVE.
    
    Refer to the Technical Reference for further information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: ComMExtendedRamCheck
  长名称: ''
  描述: |
    This parameter enables/disables extended RAM check of the CAN registers and Message Boxes. If
    enabled, ComM evaluates the status of extended RAM check before starting communication on a
    channel.
    
    Dependency: The value must be false if 'Pnc Support' is true.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: ComMResetAfterForcingNoComm
  长名称: ''
  描述: |
    This parameter defines if ComM shall force an ECU reset by invoking BswM_ComM_InitiateReset()
    after a channel entered No Communication mode because of an active Mode Limitation.
    Dependencies:
    - if enabled, the parameter ComMModeLimitationEnabled must be enabled as well.
    - if enabled, at least one channel must have Nm Variant FULL or LIGHT (because Mode Limitation
    cannot be applied to channels with Nm Variant PASSIVE or NONE).
    - if enabled, you need to configure a BswM Mode Request Port with the Source
    BswMComMInitiateReset.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: ComMSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: ComM0PncVectorAvoidance
  长名称: ''
  描述: |
    This parameter defines, if ComM sends PNC-Vectors containing only '0' (no external or internal
    requests) on passive channels.
    If the parameter is set to TRUE and all signals for the referenced ComMChannel(s) are set to
    '0', ComM releases the corresponding ComMChannel. Thus, it is avoided to send the PNC-Vector
    containing only '0'.
    If the parameter is set to FALSE and all signals for the referenced ComMChannel(s) are set to
    '0', ComM does not release the corresponding ComMChannel. Thus, ComM continues sending the
    PNC-Vector containing only '0'.
    
    Note:
    This parameter can only be set to TRUE if ComMPncGatewayEnabled is enabled and a channel with
    gateway type passive exists. In this case, it is recommended to set this parameter to TRUE in
    order to avoid the passive channels to be kept awake unnecessarily and thus avoid sending
    PNC-Vectors containing only '0'.
  默认值: true
  最小值: ''
  最大值: ''
```

### 9. ComMGeneration

**描述**: Contains the generation configuration parameters of the Communication Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMOutOfBoundsWriteSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds write problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComMOutOfBoundsReadSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds read problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
  默认值: false
  最小值: ''
  最大值: ''
```

