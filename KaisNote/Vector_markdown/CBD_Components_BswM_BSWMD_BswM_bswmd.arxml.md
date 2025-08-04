# BswM

## 模块描述

BSW Mode Manager. Implements the Vehicle Mode Management and Application Mode Management concept
including the state handling of the ECU. It's responsibility is to arbitrate mode requests from
application layer SW-Cs or other BSW modules based on rules, and perform actions based on the
arbitration result.
#ModeManagement #ModeRequest #Rules #Actionlist #Startup #Shutdown #StateHandling
#AUTOSAR #ServiceComponent

## 容器列表

### 1. BswMConfig

**描述**: This container includes the configuration parameters and sub containers of the AUTOSAR BswM module.
This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist
once per configuration set.

该容器没有参数。

### 2. BswMArbitration

**描述**: This container includes all configuration sub-containers and parameters related to the mode
arbitration functionality of the BswM.

该容器没有参数。

### 3. BswMLogicalExpression

**描述**: This container describes the logical expressions that can be used for the mode arbitration. The
logical expressions are built of a set of arguments and a logical operator. Each argument can either
be a mode condition or a sub-expression to allow definition of more complex logical expressions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMLogicalOperator
  长名称: ''
  描述: This parameter defines the logical operator to be used in the logical expression. If the
      expression only consists of a single condition this parameter is not considered.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. BswMModeCondition

**描述**: This container includes the BswM mode conditions that can be used either by itself to form a rule or
as a part of a logical expression.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMConditionType
  长名称: ''
  描述: This parameter defines what kind of comparison is made for the evaluation of the mode
      condition.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. BswMBswMode

**描述**: This container includes the value and type of a mode in the BSW.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMBswRequestedMode
  长名称: ''
  描述: This parameter defines the symbolic name (as a string) of a certain mode/state that can be
      requested/indicated by the BSW modules.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. BswMModeDeclaration

**描述**: This container includes a reference to a mode declaration. When the mode corresponds to a mode
request or mode indication interface the mode is defined by a mode declaration. The mode
declarations are defined in the SW-C Template and hence a foreign reference to the corresponding
Mode Declaration is used.

该容器没有参数。

### 7. BswMModeRequestPort

**描述**: Each instance of this container defines a mode request interface that is used to requests or
indicate modes from/to the BswM. These interfaces are implemented as ports or as ordinary
C-functions based upon if the request is made by an SW-C or a BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMArbitrateOnInit
  长名称: ''
  描述: |
    If enabled, rules which depend on this Request Port will be arbitrated on the init value of this
    port too. This will be performed at the end of BswM_Init.
    
    Only available for IMMEDIATE and FORCED_IMMEDIATE request processing.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: BswMRequestProcessing
  长名称: ''
  描述: This parameter defines the processing of the mode arbitration.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. BswMBswModeInitValue

**描述**: This is the choice for a initial mode value used for the initialization of mode requests in case the
request is made by a BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMBswModeInitValueMode
  长名称: ''
  描述: This parameter defines the initial mode value that is used by BswM for the corresponding mode
      request after initialization.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. BswMSwcModeInitValue

**描述**: This is the choice for a foreign reference to the Mode Declaration used for the initialization of
mode requests in case the request is made by a SW-C.

该容器没有参数。

### 10. BswMCompuScaleModeValue

**描述**: This container contains parameters used to define a mode value.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMCompuConstText
  长名称: ''
  描述: The value of this parameter shall match one VT member of the referenced CompuMethod
      (BswMCompuMethodRef).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. BswMBswModeNotification

**描述**: The source of the mode request is a BSW Module.

Not used parameter.

该容器没有参数。

### 12. BswMCanSMIndication

**描述**: This is an indication of the current state of the CAN State Manager.

该容器没有参数。

### 13. BswMComMIndication

**描述**: This is an indication of the current communication mode of a channel in the Communication Manager.

该容器没有参数。

### 14. BswMComMInitiateReset

**描述**: This is an indication from the ComM to indicate a reset. This container does not contain any
parameters since there is no further configuration needed for this type of request.

该容器没有参数。

### 15. BswMComMPncRequest

**描述**: This is a request of the current communication mode of a Partial Network Cluster in the
Communication Manager.

该容器没有参数。

### 16. BswMDcmApplicationUpdatedIndication

**描述**: This is a request to update application data from the DCM. This container does not contain any
parameters since there are no further configuration needed for this type of request.

该容器没有参数。

### 17. BswMDcmComModeRequest

**描述**: The source of the mode request is the Diagnostic Communication Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMDcmComMNetwork
  长名称: Dcm ComM Network
  描述: |
    This parameter specifies the network the request relates to.
    
    Not used parameter.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 18. BswMDoIPSetChannelReady

**描述**: This is a request from DoIP to report channel ready in case a routing activation has been
successfully performed.
This container does not contain any parameters since there are no further configuration needed for
this type of request.

该容器没有参数。

### 19. BswMDoIPIntSetChannelReady

**描述**: This is a request from DoIPInt to report channel ready in case a connection has been successfully
established.
This container does not contain any parameters since there are no further configuration needed for
this type of request.

该容器没有参数。

### 20. BswMEcuMIndication

**描述**: This is a notification of the current operation mode of the ECU State Manager. This container does
not contain any parameters since there are no further configuration needed for this type of request.

该容器没有参数。

### 21. BswMEcuMRUNRequestIndication

**描述**: This is an indication of the current State of the RUN Request Protocol.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMEcuMRUNRequestProtocolPort
  长名称: EcuM RUN Request Protocol Port
  描述: Identifies the EcuM State which is related to the mode request.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 22. BswMEcuMWakeupSource

**描述**: This is a notification of the current state of an ECU State Manager wakeup source.

该容器没有参数。

### 23. BswMEthIfPortGroupLinkStateChg

**描述**: This is an indication from the EthIf if the link state of a ethernet interface switch port group has
changed.

该容器没有参数。

### 24. BswMEthSMIndication

**描述**: This is an indication of the current state of the Ethernet State Manager.


该容器没有参数。

### 25. BswMFrSMIndication

**描述**: This is an indication of the current state of the FlexRay State Manager.

该容器没有参数。

### 26. BswMGenericRequest

**描述**: This mode request originates from a requester that is not among the list of standardized mode
requesters (i.e. the different resource managers).

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMModeRequesterId
  长名称: ''
  描述: This parameters identifies the different users of the generic mode request interface.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: BswMRequestedModeMax
  长名称: ''
  描述: |
    Not used parameter.
    
    This parameter defines the upper limit for the modes requested by this mode requester.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 27. BswMGenericRequestMode

**描述**: Each instance of this container defines a generic mode with name of this container.
In Code, name of this define will be "BSWM_GENERICVALUE_" + short name of of BswMModeRequestPort +
"_" + Short name of BswMGenericRequestMode

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMGenericRequestModeValue
  长名称: ''
  描述: Defines the value of the Generic Mode
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 28. BswMJ1939DcmBroadcastStatus

**描述**: This is a notification of the desired broadcast status per network, triggered via DM13.

该容器没有参数。

### 29. BswMJ1939NmIndication

**描述**: This is an indication of the current state of the J1939 network management module.

该容器没有参数。

### 30. BswMLinScheduleEndNotification

**描述**: Notifies the end of a schedule of configured LinSM channel.

该容器没有参数。

### 31. BswMLinSMIndication

**描述**: This is an indication of the current state of the LIN State Manager.

该容器没有参数。

### 32. BswMLinScheduleIndication

**描述**: This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.

该容器没有参数。

### 33. BswMLinTpModeRequest

**描述**: This is a LinTp mode request from the LinIf. This port corresponds to a call of the
BswM_LinTp_RequestMode API.

该容器没有参数。

### 34. BswMNmIndication

**描述**: This is an indication of the current state of the network management module.

该容器没有参数。

### 35. BswMNvMJobModeIndication

**描述**: Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g.
0x0c for NvmReadAll, 0x0d for NvmWriteAll.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMNvmService
  长名称: NvM Service
  描述: Identifies the NvM job which is related to the mode request.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 36. BswMNvMRequest

**描述**: Via this Mode Request Source the NvM indicates the current status of the specified block.

该容器没有参数。

### 37. BswMPduRPreTransmit

**描述**: This mode request port is called just before the <LowerDestModule>_Transmit function for the
referred PduRDestPdu is called. This mode request source can only be used for PduRDestPdus with
transmit direction.

该容器没有参数。

### 38. BswMPduRRxIndication

**描述**: This is a Rx Indication from the PduR.

该容器没有参数。

### 39. BswMPduRTpRxIndication

**描述**: This is a Tp Rx Indication from the PduR.

该容器没有参数。

### 40. BswMPduRTpStartOfReception

**描述**: This is a Start of Reception Nofitication from the PduR.

该容器没有参数。

### 41. BswMPduRTpTxConfirmation

**描述**: This is a Tp Tx Confirmation from the PduR.

该容器没有参数。

### 42. BswMPduRTransmit

**描述**: This is a Transmit Nofitication from the PduR.

该容器没有参数。

### 43. BswMPduRTxConfirmation

**描述**: This is a Tx Confirmation from the PduR.

该容器没有参数。

### 44. BswMSwcModeNotification

**描述**: This is a mode switch notification associated with a RTE switch interface.

该容器没有参数。

### 45. BswMSdClientServiceCurrentState

**描述**: Used by Service Discovery module to indicate current state of the Client Service (available/down).

该容器没有参数。

### 46. BswMSdConsumedEventGroupCurrentState

**描述**: Used by Service Discovery to indicate current status of the EventHandler (requested/released).

该容器没有参数。

### 47. BswMSdEventHandlerCurrentState

**描述**: Used by Service Discovery to indicate current status of the EventHandler (requested/released).

该容器没有参数。

### 48. BswMSwcModeRequest

**描述**: The source of the mode request is a SW Component.


#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMModeRequestDataElementPrototypeName
  长名称: ''
  描述: The parameter describes the name of the SR-Interface data element which contains the requested
      mode. The data element name must be identical to the data element name of the
      corresponding application SR-Interface.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 49. BswMTimer

**描述**: This is a timer which can be used for time depending rules.

该容器没有参数。

### 50. BswMUserConditionRequest

**描述**: The source of this Request can be any available function with a return value.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMUserCondition
  长名称: ''
  描述: Function with return value which shall be used as condition.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 51. BswMWdgMRequestPartitionReset

**描述**: This is a Partition Reset request fromthe WdgM. This port corresponds to a call of the
BswM_WdgM_RequestPartitionReset API.

该容器没有参数。

### 52. BswMRule

**描述**: Each instance of this container describes a BswM arbitration rule. The rule either consists of a
simple mode condition or a more complex logical expression. This container also references the
action lists that shall be invoked when the rule is evaluated to True or False.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMNestedExecutionOnly
  长名称: ''
  描述: This parameter defines for its related Rule if the Rule is an Independent rule or a
      Subordinate rule.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: BswMRuleId
  长名称: ''
  描述: This parameters identifies the different rules and is used for the rule control interface.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: BswMRuleInitState
  长名称: ''
  描述: This parameter is a part of the reset/initialization behavior of BswM.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 53. BswMDataTypeMappingSets

**描述**: Collection of references to DataTypeMappingSet.

该容器没有参数。

### 54. BswMModeControl

**描述**: This container includes all configuration sub-containers and parameters related to the mode control
functionality of the BswM.

该容器没有参数。

### 55. BswMAction

**描述**: Each container of this type defines an action. These actions can be part of one or several action
lists.

该容器没有参数。

### 56. BswMComMAllowCom

**描述**: This container includes all parameters for the action to allow or to block communication for a ComM
Channel. ComM_CommunicationAllowed is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMComAllowed
  长名称: ''
  描述: The parameter BswMComMAllowChannelRef refers to a channel which will allow or block
      communication using the function ComM_CommunicationAllowed().
  默认值: false
  最小值: ''
  最大值: ''
```

### 57. BswMComMModeLimitation

**描述**: This container includes all parameters related to a limitation of communication mode for a ComM
Channel. ComM_LimitChannelToNoComMode is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMComMLimitMode
  长名称: ComM Mode Limit Mode
  描述: The function ComM_LimitChannelToNoComMode() takes in this boolean parameter to limit the
      channel's communication mode to NO_COM mode.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 58. BswMComMModeSwitch

**描述**: This container includes all parameters related to a switch of communication mode for a ComM User.
ComM_RequestComMode is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMComMRequestedMode
  长名称: ComM Requested Mode
  描述: This parameter specifies the requested communication mode.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 59. BswMDeadlineMonitoringControl

**描述**: This container includes all parameters related to enabling and disabling of deadline monitoring for
one or several PDUs in COM.

该容器没有参数。

### 60. BswMDcmSetChannelReady

**描述**: This container defines the action to trigger the Dcm_SetChannelReady

该容器没有参数。

### 61. BswMEcuMGoDown

**描述**: This container defines the UserId which shall be forwarded to the GoDown request.

该容器没有参数。

### 62. BswMEcuMGoHalt

**描述**: This container defines the action to trigger the EcuM_GoHalt from BswM.

该容器没有参数。

### 63. BswMEcuMGoPoll

**描述**: This container defines the action to trigger the EcuM_GoPoll from BswM.

该容器没有参数。

### 64. BswMEcuMSelectShutdownTarget

**描述**: This container defines the shutdown target.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMEcuMShutdownTarget
  长名称: EcuM Shutdown Target
  描述: |
    This parameter contains the shutdown target that the BswM selects at the EcuM.
    If SLEEP is selected, BswMEcuMSleepModeRef must be set.
    If RESET is selected, BswMEcuMResetModeRef must be set.
  默认值: OFF
  最小值: ''
  最大值: ''
```

### 65. BswMEcuMStateSwitch

**描述**: This container defines the action to switch a State of the ECU State Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMEcuMState
  长名称: EcuM State
  描述: This parameter corresponds to the parameter "State" of the function EcuM_ SetState ().
  默认值: ''
  最小值: ''
  最大值: ''
```

### 66. BswMEthIfStartAllPorts

**描述**: This container defines the action to call EthIf_StartAllPorts from BswM
and thus to start all affected EthSwtPorts.

该容器没有参数。

### 67. BswMEthIfSwitchPortGroupRequestMode

**描述**: This container defines the action to call EthIf_SwitchPortGroupRequestMode()

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMEthIfGroupMode
  长名称: ''
  描述: This parameter contains the mode which will be requested.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 68. BswMGenericModeSwitch

**描述**: This container includes all parameters for the action to switch a Generic Mode. BswM_RequestMode is
called when this action is configured.

该容器没有参数。

### 69. BswMIdsMBlockStateChangeRequest

**描述**: This container includes all parameters related to a switch of a IdsM Block State.
IdsM_BswM_StateChanged is called when this action is configured.

该容器没有参数。

### 70. BswMJ1939DcmStateSwitch

**描述**: This container includes all parameters related to a switch of the J1939 Request Managers diagnostic
state for a J1939 node. J1939Dcm_SetState is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMJ1939DcmRequestedState
  长名称: ''
  描述: This parameter describes the communication state of the J1939 Request Manager and corresponds
      to the parameter "new state" of the function J1939Dcm_SetState.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 71. BswMJ1939RmStateSwitch

**描述**: This container includes all parameters related to a switch of the J1939 Request Manager's network
state for a J1939 node. J1939Rm_SetState is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMJ1939RmRequestedState
  长名称: ''
  描述: This parameter describes the communication state of the J1939 Request Manager and corresponds
      to the parameter "new state" of the function J1939Rm_SetState.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 72. BswMLinScheduleSwitch

**描述**: This container includes all parameters related to a switch of LIN schedule table.
LinSM_ScheduleRequest is called when this action is configured.

该容器没有参数。

### 73. BswMNMControl

**描述**: This container includes all parameters related to enabling and disabling of Network Management
communication. Disabling of NM communication can be requested by DCM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMNMAction
  长名称: ''
  描述: This parameter specifies if the communication of the corresponding NM channel should be
      enabled or disabled.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 74. BswMPduGroupSwitch

**描述**: This container includes references to the PDU groups that shall be enabled and disabled.
Com_IpduGroupStart or Com_IpduGroupStop is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMPduGroupSwitchReinit
  长名称: ''
  描述: This parameter defines if the values for the parameters like periodical timer, minimum delay
      timer etc. is retained or reinitialized during a PDU Group Switch.
  默认值: false
  最小值: ''
  最大值: ''
```

### 75. BswMPduRouterControl

**描述**: This container includes all parameters related to enabling and disabling of routing of Routing Path
Groups in the PDU Router. PduR_EnableRouting or PduR_DisableRouting is called when this action is
configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswPduRouterAction
  长名称: ''
  描述: This parameter specifies if the routing of the corresponding PDU should be enabled or
      disabled.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 76. BswMRteModeRequest

**描述**: This container defines a mode request that the BswM may send to a SW-C which is acting as a
mode-manager. RTE_Write is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMRequestedMode
  长名称: ''
  描述: This represents the RTE mode used for the mode request port.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 77. BswMRteSwitch

**描述**: This container defines a mode switch indication that the BswM provides to the SW-C that need to be
notified about the mode switch. RTE_Switch is called when this action is configured.

该容器没有参数。

### 78. BswMSchMSwitch

**描述**: This container defines a mode switch indication that the BswM provides to the SW-C that need to be
notified about the mode switch. SchM_Switch is called when this action is configured.

Not used parameter.

该容器没有参数。

### 79. BswMSdClientServiceModeRequest

**描述**: This container includes all parameters related to the selection of an client service of Sd.
Sd_ClientServiceSetState is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMSdClientServiceState
  长名称: ''
  描述: This parameter specifies if the corresponding client service shall be released or requested.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 80. BswMSdConsumedEventGroupModeRequest

**描述**: This container includes all parameters related to the selection of a consumed EventGroup of Sd.
Sd_ConsumedEventGroupSetState is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMSdConsumedEventGroupState
  长名称: ''
  描述: This parameter specifies if the corresponding consumed event group shall be released or
      requested.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 81. BswMSdServerServiceModeRequest

**描述**: This container includes all parameters related to the selection of a server service of Sd.
Sd_ServerServiceSetState is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMSdServerServiceState
  长名称: ''
  描述: This parameter specifies if the corresponding server service shall be down or available.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 82. BswMSdServiceGroupSwitch

**描述**: This container includes references to the SdServiceGroups that shall be enabled and disabled.

该容器没有参数。

### 83. BswMSwitchIPduMode

**描述**: This container includes all parameters related to the selection of the transmission mode an I-PDU to
be sent by COM. Com_SwitchIpduTxMode is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMSwitchIPduModeValue
  长名称: ''
  描述: This parameter defines which transmission mode shall be selected during this call.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 84. BswMTriggerIPduSend

**描述**: This container includes all parameters related to the triggering of an I-PDU to be sent by COM.
Com_TriggerIPDUSend is called when this action is configured.

该容器没有参数。

### 85. BswMTriggerSlaveRTEStop

**描述**: This container includes all parameters needed to stop the RTE on a slave core. This choice shall
only be chosen if multicore is used.

Not used parameter.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMCoreId
  长名称: ''
  描述: This parameter defines the identifier of the slave core that is used as input parameter for
      the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this
      parameter shall be synchronized with the OsApplicationCoreAssignment parameter.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 86. BswMTriggerStartUpPhase2

**描述**: This container includes all parameters needed to start phase two on a slave core. This choice shall
only be chosen if multicore is used.

Not used parameter.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMCoreId
  长名称: ''
  描述: This parameter defines the identifier of the slave core that is used as input parameter for
      the BswM_TriggerStartUpPhase2 and BswM_TriggerSlaveRTEStop functions. The value of this
      parameter shall be synchronized with the OsApplicationCoreAssignment parameter.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 87. BswMTimerControl

**描述**: This container includes all parameters for the action to start or to stop a timer. BswM_TimerControl
is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMTimerAction
  长名称: ''
  描述: Specify the action for the timer. The timer can be started or stopped.
  默认值: BSWM_TIMER_START
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: BswMTimerValue
  长名称: ''
  描述: Specify the timer value that is used when the timer is started.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 88. BswMUserCallout

**描述**: This container includes all details needed for a user defined function call.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMUserCalloutFunction
  长名称: ''
  描述: This parameter specifies the complete function call including all parameters. The parameters
      are specified during configuration time, and cannot be changed during run time. Any
      return values passed by the callout will be ignored.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: BswMCreateCallout
  长名称: ''
  描述: If enabled, function body will be defined in BswM_Callout_Stubs.c
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: BswMCalloutParameterList
  长名称: ''
  描述: |
    Semicolon separated list of parameters prototypes which are used for creating the Callout.
    (e.g: uint16 number; const uint8* ptr;)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: BswMUserCode
  长名称: ''
  描述: |
    This parameter defines an additional code in the callout function.
    
    RESTRICTIONS: 'BswMUserCode' is only available, if 'BswMCreateCallout' is enabled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: BswMUserIncludeFile
  长名称: ''
  描述: This parameter defines a header file name which shall be included by the BswM.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 89. BswMRuleControl

**描述**: This container includes all details needed for BswM Rule Control.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMRuleAction
  长名称: ''
  描述: Specify the action for the rule. The rule will be deactivated for BSWM_DEACTIVATED, all other
      will activate the rule.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 90. BswMActionList

**描述**: Each instance of this container defines an action list that is invoked based on the BswM Rules. An
action list contains a list of numbered action items to be processed. An action list can also
include other action lists.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMActionListExecution
  长名称: ''
  描述: This parameter controls if the corresponding action list shall be executed every time the rule
      is evaluated or only when the result of the evaluation changes.
  默认值: BSWM_TRIGGER
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: BswMActionListPriority
  长名称: ''
  描述: This parameter sets a priority for this action list. A greater value (higher priority) means
      earlier execution. If parameter is absent, 0 is assumed.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 91. BswMActionListItem

**描述**: This container defines an item in an action list.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMAbortOnFail
  长名称: ''
  描述: This parameter defines if the execution of the action list shall be aborted if this specific
      action returns E_NOT_OK. Note that this is only applicable for actions that have
      E_NOT_OK as a possible return value.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: BswMActionListItemIndex
  长名称: ''
  描述: This parameter defines the index of the action in the action list. It is used define in which
      order the actions shall be performed.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 92. BswMRteModeRequestPort

**描述**: This container defines a mode request port which the BswM may utilize to send a mode request to a
SW-C which is acting as a mode-manager.  If this container is referenced by a BswMRteModeRequest,
the BswM shall create a corresponding PPort in its service description.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMRteModeInitValue
  长名称: ''
  描述: This represents the value used for the init value of RTE mode request port.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 93. BswMSwitchPort

**描述**: This container specifies PPorts and/or provided ModeDeclarationGroups, which the BswM has to create
in its SWCD.

该容器没有参数。

### 94. BswMRteModeDclGroup

**描述**: This container describes a ModeDeclarationGroup which is created by the BswM.

该容器没有参数。

### 95. BswMRteMode

**描述**: This container describes a Mode of a ModeDeclarationGroup.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMModePhysicalValue
  长名称: ''
  描述: Describes the physical value of the Mode. Value is used in the CompuMehod of the
      ImplemenationType.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 96. BswMGeneral

**描述**: General configuration parameters of the Basic SW Mode Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMCanSMEnabled
  长名称: CanSM Enabled
  描述: This parameter defines if the CanSM module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: BswMComMEnabled
  长名称: ComM Enabled
  描述: This parameter defines if the ComM module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: BswMDcmEnabled
  长名称: ''
  描述: This parameter defines if the Dcm module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: BswMDevErrorDetect
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
  序号: 5
  名称: BswMDoIPEnabled
  长名称: DoIP Enabled
  描述: This parameter defines if the DoIP module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: BswMDoIPIntEnabled
  长名称: DoIPInt Enabled
  描述: This parameter defines if the DoIPInt module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: BswMEcuMEnabled
  长名称: EcuM Enabled
  描述: This parameter defines if the EcuM module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: BswMEthIfEnabled
  长名称: EthIf Enabled
  描述: This parameter defines if the EthIf module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: BswMEthSMEnabled
  长名称: EthSM Enabled
  描述: This parameter defines if the EthSM module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: BswMFrSMEnabled
  长名称: FrSM Enabled
  描述: This parameter defines if the FrSM module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: BswMGenericRequestEnabled
  长名称: ''
  描述: This parameter defines if the Generic Request related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: BswMJ1939DcmEnabled
  长名称: ''
  描述: This parameter defines if the 1939Dcm module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: BswMJ1939NmEnabled
  长名称: ''
  描述: This parameter defines if the 1939Nm module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: BswMLinSMEnabled
  长名称: LinSM Enabled
  描述: This parameter defines if the LinSM module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: BswMLinTPEnabled
  长名称: LinTP Enabled
  描述: This parameter defines if the LinTp module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: BswMMainFunctionPeriod
  长名称: ''
  描述: This value specifies the cycle time of the periodic main function of BswM
  默认值: 0.01
  最小值: 0
  最大值: 65.535
- 
  序号: 17
  名称: BswMNmEnabled
  长名称: ''
  描述: This parameter defines if the Nm module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: BswMNvMEnabled
  长名称: NvM Enabled
  描述: |
    This parameter defines if the NvM module related BswM API is enabled.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: BswMPduREnabled
  长名称: PduR Enabled
  描述: This parameter defines if the PduR module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: BswMRuleControlEnabled
  长名称: ''
  描述: This parameter defines if the Rule Control related BswM API (BswM_SetRuleState) is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: BswMSchMEnabled
  长名称: SchM Enabled
  描述: |
    This parameter defines if the SchM module related BswM API is enabled.
    
    Not used parameter.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: BswMSdEnabled
  长名称: ''
  描述: This parameter defines if the Sd module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: BswMVersionInfoApi
  长名称: ''
  描述: This parameter enables/disables the function BswM_GetVersionInfo() to get major, minor and
      patch version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: BswMWdgMEnabled
  长名称: WdgM Enabled
  描述: This parameter defines if the WdgM module related BswM API is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: BswMUserConfigurationFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation to BswM_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: BswMModeCheck
  长名称: ''
  描述: If enabled, mode values which are passed to the Mode Request APIs are checked. Only relevant
      if DevErrorDetect is enabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: BswMActionListQueueSearchAlgorithm
  长名称: ''
  描述: |
    This parameter determines the algorithm that shall be used for the action list execution.
    
    There are two possible algorithms:
    LINEAR_SEARCH: uses a sequential search for the action list execution.
    The insertion into the queue of action lists that shall be executed during rule arbitration has
    a constant complexity.
    The execution of the action lists after rule arbitration has a linear complexity (over the
    number of action lists).
    Use this search algorithm if there are only few action lists or if the ROM/RAM consumption shall
    be minimized.
    
    PRIORITY_QUEUE: uses a priority queue realized as heap for the action list execution.
    The insertion into the queue has a logarithmic complexity (over all existing elements in the
    queue).
    The execution of the queue has a linear complexity (over all existing elements in the queue).
    The RAM/ROM consumption of this search is higher compared to the LINEAR_SEARCH.
    In configurations with a large number of action lists, this option can improve the runtime.
    
  默认值: LINEAR_SEARCH
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: BswMSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
```

### 97. BswMUserIncludeFiles

**描述**: This container includes a collection of header file names which shall be included by the BswM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMUserIncludeFile
  长名称: ''
  描述: This parameter defines a header file name which shall be included by the BswM.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 98. BswMCommonData

**描述**: This container is used to store internal data of BswM. DO NOT REMOVE!

该容器没有参数。

### 99. BswMGeneration

**描述**: Contains parameters which have influence on the generation of the module

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMOutOfBoundsWriteSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds write problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
    
    For more details, refer to TechnicalReference_ComStackLib.pdf
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: BswMOutOfBoundsReadSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds read problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
    
    For more details, refer to TechnicalReference_ComStackLib.pdf
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: BswMReduceConstantData2Define
  长名称: Reduce Constant Data To a Define
  描述: |
    This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM
    arrays as constant define.
    
    FALSE: ROM arrays are generated as data even if all values are identical.
    TRUE: ROM arrays are generated as constant define if all values are identical.
    
    For more details, refer to TechnicalReference_ComStackLib.pdf
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: BswMBoolDataInArrayOfStructStrategy
  长名称: ''
  描述: |
    This parameter is used to tailor the usage of boolean data in structures in all CONFIG-CLASSES
    ROM data. The difference between BITFIELD and BITMASKING depends on your compiler options and
    memory mapping.
    
    BOOLEAN: the datatype of boolean data is native boolean.
    BITFIELD: the bitfield type is used and the compiler extracts the boolean data from structures.
    BITMASKING: generated masks are used to extract the boolean data from structures.
    
    For more details, refer to TechnicalReference_ComStackLib.pdf
  默认值: BITMASKING
  最小值: ''
  最大值: ''
```

