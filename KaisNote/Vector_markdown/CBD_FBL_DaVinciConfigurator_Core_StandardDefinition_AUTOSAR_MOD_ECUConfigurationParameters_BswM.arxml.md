# BswM

## 模块描述

Configuration of the BswM (Basic SW Mode Manager) module.

## 容器列表

### 1. BswMConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR BswM module.
This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist
once per configuration set.

该容器没有参数。

### 2. BswMArbitration

**描述**: This container includes all configuration sub-containers and parameters related to the mode
arbitration functionality of the BswM.

该容器没有参数。

### 3. BswMLogicalExpression

**描述**: This container describes the logical expressions that can be used for the mode arbitration. The
logical expressions are built of a set of arguments and a logical operator.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMLogicalOperator
  长名称: ''
  描述: This parameter specifies the logical operator to be used in the logical expression. If the
      expression only consists of a single condition this parameter shall not be used.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. BswMModeCondition

**描述**: This container describes the BswM mode conditions that can be used either by itself to form a rule
or as a part of a logical expression.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMConditionType
  长名称: ''
  描述: This parameter specifies what kind of comparison that is made for the evaluation of the mode
      condition.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. BswMBswMode

**描述**: This container defines the value and type of a mode in the BSW.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMBswRequestedMode
  长名称: ''
  描述: This parameter contains the symbolic name (as a string) of a certain mode/state that can be
      requested/indicated by the BSW modules.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. BswMModeDeclaration

**描述**: When the mode corresponds to a mode request or mode indication interface the mode is defined by a
mode declaration. The mode declarations are defined in the SW-C Template and hence a foreign
reference to the corresponding Mode Declaration is used.

该容器没有参数。

### 7. BswMModeRequestPort

**描述**: Each instance of this container defines a mode request interface that is used to requests or
indicate modes from/to the BswM. These interfaces are implemented as ports or as ordinary
C-functions based upon if the request is made by an SW-C or a BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMRequestProcessing
  长名称: ''
  描述: This parameter defines if the processing of the mode arbitration shall be done immediately
      when a mode request is received or if it shall be deferred to the processing of the main
      function of BswM.
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

### 10. BswMBswModeNotification

**描述**: The source of the mode request is a Bsw Module.

该容器没有参数。

### 11. BswMCanSMIndication

**描述**: This is an indication of the current state of the CAN State Manager.

该容器没有参数。

### 12. BswMComMIndication

**描述**: This is an indication of the current communication mode of a channel in the Communication Manager.

该容器没有参数。

### 13. BswMComMPncRequest

**描述**: This is a request of the current communication mode of a Partial Network Cluster in the
Communication Manager.

该容器没有参数。

### 14. BswMDcmApplicationUpdatedIndication

**描述**: This is a request to update application data from the DCM. This container does not contain any
parameters since there are no further configuration needed for this type of request.

该容器没有参数。

### 15. BswMDcmComModeRequest

**描述**: The source of the mode request is the Diagnostic Communication Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMDcmComMNetwork
  长名称: ''
  描述: This parameter specifies the network the request relates to.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 16. BswMEcuMIndication

**描述**: This is a notification of the current operation mode of the ECU State Manager. This container does
not contain any parameters since there are no further configuration needed for this type of request.

该容器没有参数。

### 17. BswMEcuMWakeupSource

**描述**: This is a notification of the current state of an ECU State Manager wakeup source.

该容器没有参数。

### 18. BswMEthSMIndication

**描述**: This is an indication of the current state of the Ethernet State Manager.

该容器没有参数。

### 19. BswMFrSMIndication

**描述**: This is an indication of the current state of the FlexRay State Manager.

该容器没有参数。

### 20. BswMGenericRequest

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
  描述: This parameter defines the upper limit for the modes requested by this mode requester.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 21. BswMLinSMIndication

**描述**: This is an indication of the current state of the LIN State Manager.

该容器没有参数。

### 22. BswMLinScheduleIndication

**描述**: This is an indication of the currently active LIN Schedule Table for a specific LIN Interface.

该容器没有参数。

### 23. BswMLinTpModeRequest

**描述**: This is a LinTp mode request from the LinIf. This port corresponds to a call of the
BswM_LinTp_RequestMode API.

该容器没有参数。

### 24. BswMNvMJobModeIndication

**描述**: Indicates the current status of the multiblock job. The job is identified via BswMNvmService, e.g.
0x0c for NvmReadAll, 0x0d for NvmWriteAll. Possible Values are:

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMNvmService
  长名称: ''
  描述: Identifies the Nvm job which is related to the mode request.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 25. BswMNvMRequest

**描述**: Via this Mode Request Source the NvM indicates the current status of the specified block. Possible
Values are:

该容器没有参数。

### 26. BswMSwcModeNotification

**描述**: This is a mode switch notification associated with a RTE switch interface.

该容器没有参数。

### 27. BswMSwcModeRequest

**描述**: The source of the mode request is a SW Component.

该容器没有参数。

### 28. BswMWdgMRequestPartitionReset

**描述**: This is a Partition Reset request from from the WdgM. This port

该容器没有参数。

### 29. BswMRule

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
      Subordinate rule;
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: BswMRuleInitState
  长名称: ''
  描述: This parameter is a part of the reset/initialization behavior of BswM.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 30. BswMDataTypeMappingSets

**描述**: Collection of references to DataTypeMappingSet.

该容器没有参数。

### 31. BswMModeControl

**描述**: This container includes all configuration sub-containers and parameters related to the mode control
functionality of the BswM.

该容器没有参数。

### 32. BswMAction

**描述**: Each container of this type defines an action. These actions can be part of one or several action
lists.

该容器没有参数。

### 33. BswMComMAllowCom

**描述**: This container includes all parameters for the action to allow or to block communication for a ComM
Channel. ComM_CommunicationAllowed  is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMComAllowed
  长名称: ''
  描述: The parameter BswMComMAllowChannelRef refers to a channel which will allow or block
      communication using the function ComM_CommunicationAllowed().
  默认值: ''
  最小值: ''
  最大值: ''
```

### 34. BswMComMModeLimitation

**描述**: This container includes all parameters related to a limitation of communication mode for a ComM
Channel. ComM_LimitChannelToNoComMode is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMComMLimitMode
  长名称: ''
  描述: The function ComM_LimitChannelToNoComMode() takes in this boolean parameter to limit the
      channel's com mode to no-com mode.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 35. BswMComMModeSwitch

**描述**: This container includes all parameters related to a switch of communication mode for a ComM User.
ComM_RequestComMode is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMComMRequestedMode
  长名称: ''
  描述: This parameter specifies if the requested communication mode.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 36. BswMDeadlineMonitoringControl

**描述**: This container includes all parameters related to enabling and disabling of deadline monitoring for
one or several PDUs in COM.

该容器没有参数。

### 37. BswMEcuMGoDown

**描述**: This container defines the UserId which shall be forwarded to the GoDown request.

该容器没有参数。

### 38. BswMEcuMSelectShutdownTarget

**描述**: This container defines the shutdown target.

该容器没有参数。

### 39. BswMLinScheduleSwitch

**描述**: This container includes all parameters related to a switch of LIN schedule table.
LinSM_ScheduleRequest is called when this action is configured.

该容器没有参数。

### 40. BswMNMControl

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

### 41. BswMPduGroupSwitch

**描述**: This container includes references to the PDU groups that shall be enabled and disabled.
Com_IpduGroupControl is called when this action is configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMPduGroupSwitchReinit
  长名称: ''
  描述: This parameter defines if the values for the parameters like periodical timer, minimum delay
      timer etc is retainer or reinitialized during a PDU Group Switch.
  默认值: false
  最小值: ''
  最大值: ''
```

### 42. BswMPduRouterControl

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

### 43. BswMRteSwitch

**描述**: This container defines a mode switch indication that the BswM provides to the SW-C that need to be
notified about the mode switch. RTE_Switch is called when this action is configured.

该容器没有参数。

### 44. BswMSchMSwitch

**描述**: This container defines a mode switch indication that the BswM provides to the SW-C that need to be
notified about the mode switch. SchM_Switch is called when this action is configured.

该容器没有参数。

### 45. BswMSwitchIPduMode

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

### 46. BswMTriggerIPduSend

**描述**: This container includes all parameters related to the triggering of an I-PDU to be sent by COM.
Com_TriggerIPDUSend is called when this action is configured.

该容器没有参数。

### 47. BswMTriggerSlaveRTEStop

**描述**: This container includes all parameters needed to stop the RTE on a slave core. This choice shall
only be chosen if multicore is used.

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

### 48. BswMTriggerStartUpPhase2

**描述**: This container includes all parameters needed to start phase two on a slave core. This choice shall
only be chosen if multicore is used.

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

### 49. BswMUserCallout

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
```

### 50. BswMActionList

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
  默认值: ''
  最小值: ''
  最大值: ''
```

### 51. BswMActionListItem

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

### 52. BswMSwitchPort

**描述**: This container specifies PPorts and/or providedModeDeclarationGroups, which the BswM has to create
in its SWCD resp. BSWMD.

该容器没有参数。

### 53. BswMGeneral

**描述**: General configuration parameters of the Basic SW Mode Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMCanSMEnabled
  长名称: ''
  描述: enable/disable CanSM module related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: BswMComMEnabled
  长名称: ''
  描述: enable/disable ComM module related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: BswMDcmEnabled
  长名称: ''
  描述: enable/disable Dcm module related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: BswMDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: BswMEcuMEnabled
  长名称: ''
  描述: enable/disable EcuM module related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: BswMEthSMEnabled
  长名称: ''
  描述: enable/disable EthSM module related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: BswMFrSMEnabled
  长名称: ''
  描述: enable/disable FrSM module related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: BswMGenericRequestEnabled
  长名称: ''
  描述: enable/disable Generic Request related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: BswMLinSMEnabled
  长名称: ''
  描述: enable/disable LinSM module related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: BswMLinTPEnabled
  长名称: ''
  描述: enable/disable LinTP module related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: BswMMainFunctionPeriod
  长名称: ''
  描述: The cycle time of the periodic main function of BswM. Defined in seconds .
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 12
  名称: BswMNvMEnabled
  长名称: ''
  描述: enable/disable NvM module related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: BswMSchMEnabled
  长名称: ''
  描述: enable/disable SchM module related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: BswMVersionInfoApi
  长名称: ''
  描述: Switches the possibility to read the version information with the service
      BswM_GetVersionInfo().
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: BswMWdgMEnabled
  长名称: ''
  描述: enable/disable WdgM module related BswM API:
  默认值: false
  最小值: ''
  最大值: ''
```

### 54. BswMUserIncludeFiles

**描述**: Collection of header file names which shall be included by the BswM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: BswMUserIncludeFile
  长名称: ''
  描述: Header file name which shall be included by the BswM.
  默认值: ''
  最小值: ''
  最大值: ''
```

