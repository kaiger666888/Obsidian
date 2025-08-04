# Dlt

## 模块描述

"Diagnostic Log and Trace.
DLT receives log information from DET, DEM, SW-Cs, or trace information of the RTE. The DLT module
transmits this data either via communication busses or via XCP to make this information visible
outside the ECU.
#AMD #Xcp #CANoe #CANape #Monitoring #Logging
#AUTOSAR #ServiceComponent"

## 容器列表

### 1. DltConfigSet

**描述**: This container lists all the global Dlt functionalities that can be enabled or disabled at
pre-compile time to optimize resource consumption.

该容器没有参数。

### 2. DltLogLevelSetting

**描述**: Contains settings for thresholds.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltDefaultLogLevel
  长名称: ''
  描述: This is the effective log level used in case no filter matches the given AppicationId and
      ContextId. This can be seen as a fall-through filter definition with wildcard for
      AppicationId and ContextId, which will be used, when no other filter matches.
  默认值: DLT_LOG_WARN
  最小值: ''
  最大值: ''
```

### 3. DltLogLevelThreshold

**描述**: Contains settings for thresholds.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltThreshold
  长名称: ''
  描述: The actual threshold.
  默认值: DLT_LOG_WARN
  最小值: ''
  最大值: ''
```

### 4. DltLogOutput

**描述**: Contains settings for log/trace message output

该容器没有参数。

### 5. DltLogChannel

**描述**: Contains settings for log/trace message output

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltLogChannelBufferOverflowTimer
  长名称: ''
  描述: Specifies the cycle time in seconds for resetting the buffer overflow flag in case a buffer
      overflow occurred.
  默认值: 0.1
  最小值: 0.001
  最大值: 1
- 
  序号: 2
  名称: DltLogChannelBufferSize
  长名称: ''
  描述: Buffer size in bytes for the LogChannel specific message buffer.
  默认值: 1024
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: DltLogChannelId
  长名称: ''
  描述: This is the 4 ASCII character long name of the log channel as used in the Dlt control messages
      as parameter name Dlt_interface
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DltLogChannelMaxMessageLength
  长名称: ''
  描述: The maximum length of a Dlt log or trace message.
  默认值: 256
  最小值: 8
  最大值: 65535
- 
  序号: 5
  名称: DltLogChannelMaxNumOfRetries
  长名称: ''
  描述: |
    The maximum length of a Dlt log or trace message.
    This parameter is not supported!
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: DltLogChannelThreshold
  长名称: ''
  描述: LogLevel Threshold
  默认值: DLT_LOG_WARN
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DltLogChannelTrafficShapingBandwidth
  长名称: ''
  描述: |
    Set the maximum possible bandwith in bit/s.
    
    Notes:
    1. This value is re-calculated to bytes/MainFunction to support the leaky bucket method.
    Example:
     - MainFunction cycle is 10ms, so the configured value is divided by 8 (bit/8 = byte) and by 100
    (MainFunction cycle = 10ms = 0.01s)
     - If 1024 bytes shall be transmittable per MainFunction cycle:
        - 1024[byte]*8*100[1/s] = 819200[bit/s]
    
    2. If the traffic shaping value is not used completely in a MainFunction cycle, the unused bytes
    are not usable in the next MainFunction cycle. So, in each MainFunction cycle only the
    configured TrafficShaping value is available for transmission.
  默认值: 4294967295
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 8
  名称: DltLogChannelTransmitCycle
  长名称: ''
  描述: |
    Specifies the cycle time in seconds of the transmit functionality of this log channel.
    This parameter is not supported!
  默认值: 0.01
  最小值: 0.001
  最大值: 1
- 
  序号: 9
  名称: DltLogTraceStatusFlag
  长名称: ''
  描述: Parameter to turn on/off on this LogChannel completely.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DltLogChannelDebugMode
  长名称: ''
  描述: |
    Specifies the debug mode of the log channel.
    The debug mode can be changed during runtime via Dlt_SetDebugMode() and be requested during
    runtime via Dlt_GetDebugMode().
    This parameter decides when buffering of Dlt log and trace messages happens and when sending
    happens.
    
    The debug modes:
    1. Continuous_FirstIsBest:
      - Buffering and sending is continuous.
      - When buffer is overflown, new log and trace messages are rejected.
    2. OnEvent_FirstIsBest:
      - Buffering starts on event.
      - When buffer is overflown, buffering is stopped and sending is performed until buffer is
    empty.
      - The event can be triggered during runtime via Dlt_TriggerDebugEvent().
  默认值: Continuous_FirstIsBest
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DltLogChannelInitialDebugEvent
  长名称: ''
  描述: |
    This parameter is only relevant if DltLogChannelDebugMode is set to OnEvent_FirstIsBest!
    
    Defines if log and trace messages shall be gathered before initialization.
    This simulates a call of port "TriggerLogChannelDebugEvent" before initialization, as this port
    is only available after initialization.
  默认值: false
  最小值: ''
  最大值: ''
```

### 6. DltTxPdu

**描述**: Contains the configuration parameters of the AUTOSAR Dlt module's Tx Pdus.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltITxPduHandleId
  长名称: ''
  描述: The numerical value used as the ID of this I-PDU.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DltITxPduUsesTp
  长名称: ''
  描述: If set to TRUE, the PDU is transmitted using the TP API. If FALSE, the IF API is used.
  默认值: true
  最小值: ''
  最大值: ''
```

### 7. DltLogChannelAssignment

**描述**: This container contains a preconfiguration of ApplicationId / ContextId pairs and their assigned log
channel.

该容器没有参数。

### 8. DltProtocol

**描述**: Configuration parameters for handling the specific protocol variants.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltHeaderUseEcuId
  长名称: ''
  描述: Corresponds to field WEID (With ECU ID). If set ECU ID shall be placed in the header, else
      not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DltHeaderUseSessionID
  长名称: ''
  描述: Corresponds to field WSID (with Session ID). If set the Session ID shall be placed in the
      header, else not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DltHeaderUseTimestamp
  长名称: ''
  描述: Corresponds to field WTMS (With Timestamp). If set the timestamp shall be placed in the
      header, else not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DltUseExtHeaderInNonVerbMode
  长名称: ''
  描述: Non Verbose messages (opposed to verbose messages) do not need an extended header. If this
      flag is set to true the extended header shall also be used for non verbose messages.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DltUseVerboseMode
  长名称: ''
  描述: If this flag is set to TRUE, the payload shall be transmitted in verbose mode, else the
      payload shall be transmitted in none-verbose mode.
  默认值: false
  最小值: ''
  最大值: ''
```

### 9. DltEcuIdCalloutChoice

**描述**: EcuId via user defined callout.
This choice is not supported!

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltEcuIdCallout
  长名称: ''
  描述: |
    If this choice is used the EcuId shall be fetched by calling the here configured callout
    function.
    This parameter is not supported!
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. DltEcuIdValueChoice

**描述**: EcuId value configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltEcuIdValue
  长名称: ''
  描述: If this choice is used the EcuId shall be taken from the configured string.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. DltRxPdu

**描述**: Contains the Pdu IDs to be used for Dlt control messages reception.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltIRxPduHandleId
  长名称: ''
  描述: The numerical value used as the ID of this I-PDU. The DltRxPduHandleId is required by the API
      calls Dlt_RxIndication, Dlt_TpRxIndication, Dlt_StartOfReception and Dlt_CopyRxData to
      receive I-PDUs from the PduR (DltIPduDirection: Receive), as well as the PduId passed to
      an Rx-I-PDU-callout.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DltIRxPduUsesTp
  长名称: ''
  描述: If set to TRUE, the PDU is received using the TP API. If FALSE, the IF API is used.
  默认值: true
  最小值: ''
  最大值: ''
```

### 12. DltTraceStatusSetting

**描述**: Contains settings for trace status

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltDefaultTraceStatus
  长名称: ''
  描述: This is the effective trace status used in case no filter matches the given ApplicationId and
      ContextId. This can be seen as a fall-through filter definition with wildcard for
      ApplicationId and ContextId, which will be used, when no other filter matches.
  默认值: true
  最小值: ''
  最大值: ''
```

### 13. DltTraceStatusAssignment

**描述**: This container contains a preconfiguration of ApplicationId / ContextId pairs and their assigned
trace status.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltTraceStatus
  长名称: ''
  描述: Trace status for the given ApplicationId/ContextId tuple.
  默认值: true
  最小值: ''
  最大值: ''
```

### 14. DltGeneral

**描述**: This container lists all the global Dlt functionalities that can be enabled or disabled at
pre-compile time to optimize resource consumption.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltGeneralDevErrorDetect
  长名称: ''
  描述: If the Default Error Tracer (Det) shall be used, this parameter shall be set to TRUE.
      Otherwise, it shall be set to FALSE.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DltGeneralInjectionSupport
  长名称: ''
  描述: Enables or disables the Dlt Injection feature.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DltGeneralRegisterContextNotification
  长名称: ''
  描述: |
    If this parameter is set to TRUE, a Dlt Control Message is sent every time a SWC registeres
    and/or de-registers at/from the Dlt Module. Else, this notification is not sent.
    This parameter is not supported!
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DltGeneralRxDataPathSupport
  长名称: ''
  描述: |
    Enables or disables the Rx Data Path to control the Dlt module.
    
    Note:
    If this parameter is disabled: The used SocketConnection must know a specific Remote Address and
    Remote Port, otherwise the socket connection cannot be opened!
    If this parameter is enabled: The Remote Address and Remote Port may be undefined. Then the
    socket is opened with the first received message.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DltGeneralStartUpDelayTimer
  长名称: ''
  描述: |
    Configurable delay in s of starting the transmission of Log and Trace messages after the Dlt
    module has been initialized.
    This parameter is not supported!
  默认值: 0.001
  最小值: 0.001
  最大值: 10
- 
  序号: 6
  名称: DltGeneralTimeStampSupport
  长名称: ''
  描述: If a Time Stamp shall be added to the Dlt messages, this configuration parameter shall be set
      to TRUE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DltGeneralTrafficShapingSupport
  长名称: ''
  描述: |
    Enables or disables the TrafficShaping feature to limit the maximum bandwidth for Dlt messages.
    If enabled, the maximum bandwidth can be configured per LogChannel.
    
    Note: The TrafficShaping is based on the leaky bucket method. This means, transmissions are
    allowed in each call of Dlt_MainFunction, but it is limited to the configured maximum value.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DltGeneralVersionInfoApi
  长名称: ''
  描述: Pre-processor switch for enabling Version Info API support.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DltComLayer
  长名称: ''
  描述: |
    Defines the communication layer to be used.
     - XCP: Use XCP as transport protocol
     - PduR: Use PduR as transport protocol
  默认值: XCP
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DltMainFunctionCycleTime
  长名称: ''
  描述: |
    Cycle time of DLT mainfunction.
    
    A value of 10 [ms] is recommended.
  默认值: 0.01
  最小值: 0.001
  最大值: 1
- 
  序号: 11
  名称: DltUserConfigFile
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
  序号: 12
  名称: DltSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: DltMaxNumberOfApplications
  长名称: ''
  描述: |
    Defines the maximum number of registered applications.
    
    Note:
    1. The configured value includes all configured applications.
         - Therefore, if additional applications shall be able to register at runtime, this value
    must be greater than the configured number of applications.
         - The minimum value is the number of configured applications + 1 for DEM + 1 for DET (+ 1
    for OS if DltOsSoftwareTracing is enabled).
    2. This value affects the required RAM usage of the Dlt.
  默认值: 10
  最小值: 2
  最大值: 65535
- 
  序号: 14
  名称: DltMaxNumberOfContextsPerApplication
  长名称: ''
  描述: |
    Defines the maximum number of registered contexts for any application.
    
    Note:
    1. The configured value includes the configured contexts.
         - Therefore, if additional contexts shall be able to register at runtime, this value must
    be greater than the configured number of contexts.
         - The minimum value is the maximum number of contexts any configured application has (+ 3
    if DltOsSoftwareTracing is enabled).
    2. This value affects the required RAM usage of the Dlt.
  默认值: 5
  最小值: 1
  最大值: 65535
- 
  序号: 15
  名称: DltDemEventFiltering
  长名称: ''
  描述: |
    If active, forwarded DEM events are filtered if event status has not changed.
    If inactive, all DEM events are sent.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: DltGeneralNvRAMSupport
  长名称: ''
  描述: |
    If active, part of Dlt settings are persisted in non-volatile memory. During initalization the
    persisted settings are restored and used for initalization instead of the configured values.
    If inactive, always the configured values are used for initialization.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: DltSupportDefaultAPI
  长名称: ''
  描述: |
    This parameter defines if the Dlt API is generated as specified by AUTOSAR:
    If enabled:
    - The API Dlt_(Get/Set)DefaultTraceStatus has a second parameter "LogChannelName".
    - As specified by AUTOSAR
    If disabled:
    - The API Dlt_(Get/Set)DefaultTraceStatus has only one parameter.
    - Deviation from AUTOSAR
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: DltServerPortQueueSizeForLogAndTraceMessages
  长名称: ''
  描述: |
    Defines how many requests of SendLogMessage and SendTraceMessage can be triggered for same
    Server-Client Port.
    Values greater one only required if multiple runnables of same SWC are using the same Dlt
    Server-Client Port to send log and trace messages.
  默认值: 1
  最小值: 1
  最大值: 256
- 
  序号: 19
  名称: DltOsSoftwareTracing
  长名称: ''
  描述: |
    This parameter defines if the OS Software Tracing is enabled or not.
    
    The OS Software Tracing make use of the Vector TimingHooks:
    - OS_VTH_SCHEDULE
    - OS_VTH_SETEVENT
    - OS_VTH_ACTIVATION
    
    If this feature is enabled, the DltGeneralTimeStampSupport shall be enabled to provide
    timestamps in the OS Tracing messages.
    
    If this feature is enabled and the BSW runs on multiple cores, DltAssignedEcucCoreRef shall be
    set to provide the DLT on which core it is executed.
    
    If DltGeneralNvRAMSupport is enabled, this parameter increases the required Nv memory of Dlt.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: DltInitialGlobalState
  长名称: ''
  描述: |
    Defines if the DLT shall be OFFLINE after initialization or ONLINE.
    OFFLINE: Rejects log and trace messages after initialization.
    ONLINE: Accepts log and trace messages after initialization.
    
    In both cases, the state can be changed by the application with the port "SetState".
    
    OFFLINE is the default state, but if DltOsSoftwareTracing is enabled, it is recommended to set
    this parameter to ONLINE. Otherwise, some thread transitions are missed in the trace.
  默认值: OFFLINE
  最小值: ''
  最大值: ''
```

### 15. DltSwc

**描述**: Contains necessary configuration parameters of the AUTOSAR Dlt module to interact with SWCs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltSwcSessionId
  长名称: ''
  描述: An ECU wide unique ID to identify the port a SWC (instance) uses.
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: DltSwcSupportLogLevelChangeNotification
  长名称: ''
  描述: Flag indicating, whether Dlt has to provide a R-Port for the notification of the SWC about
      LogLevel changes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: MaxSwcLogMessageLength
  长名称: ''
  描述: |
    Defines the maximum allowed length (unit16) for LogMessages.
    This parameter is not supported!
  默认值: 256
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: MaxSwcTraceMessageLength
  长名称: ''
  描述: |
    Defines the maximum allowed length (unit16) for TraceMessages.
    This parameter is not supported!
  默认值: 256
  最小值: 0
  最大值: 65535
```

### 16. DltSwcContext

**描述**: This container contains the configuration of ApplicationId / ContextId pairs which are supported by
this SWC.

If DltGeneralNvRAMSupport is enabled, increasing the number of this container will also increase the
required Nv memory of Dlt.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltSwcApplicationId
  长名称: ''
  描述: Abbreviation for the SWC (4 characters)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DltSwcContextId
  长名称: ''
  描述: Abbreviation for the ContextId (4 characters)
  默认值: ''
  最小值: ''
  最大值: ''
```

### 17. DltNonVerboseMessage

**描述**: Non-Verbose messages require a minimum bandwith as only its identifier will be transmitted over the
network. The XCP tool will then resolve the identifier to the string defined as static data. To
transmit a non-verbose message use the API: <Name>.

Hint: Use the verbose message API to transmit a runtime defined string over the network.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DltMessageId
  长名称: ''
  描述: |
    Message ID is the unique ID to characterize the information, which is transported by the
    non-verbose message itself. The message ID will be assigned automatically.
    
    RESTRICTIONS: Message IDs used for Dem (1) and Det (2) are reserved and not usable for the
    application.
  默认值: 3
  最小值: 3
  最大值: 4294967295
- 
  序号: 2
  名称: DltStaticData
  长名称: ''
  描述: Data of static information that is associated with the Message ID. This data is not
      transmitted with the non-verbose message but is stored in the A2L file.
  默认值: ''
  最小值: ''
  最大值: ''
```

