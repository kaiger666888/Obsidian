# CanIf

## 模块描述

This container includes all necessary configuration sub-containers according the CAN Interface
configuration structure.

## 容器列表

### 1. CanIfCtrlDrvCfg

**描述**: Configuration parameters for all the underlying CAN Driver modules are aggregated under this
container. For each CAN Driver module a seperate instance of this container has to be provided.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfCtrlDrvTxCancellation
  长名称: ''
  描述: Selects whether transmit cancellation is supported and if the appropriate callback will be
      provided to the CAN Driver module.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. CanIfCtrlCfg

**描述**: This container contains the configuration (parameters) of an adressed CAN controller by an
underlying CAN Driver module. This container is configurable per CAN controller.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfCtrlId
  长名称: ''
  描述: This parameter abstracts from the CAN Driver specific parameter Controller. Each controller of
      all connected CAN Driver modules shall be assigned to one specific ControllerId of the
      CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: CanIfCtrlWakeupSupport
  长名称: ''
  描述: This parameter defines if a respective controller of the referenced CAN Driver modules is
      queriable for wake up events.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. CanIfDispatchCfg

**描述**: Callback functions provided by upper layer modules of the CanIf. The callback functions defined in
this container are common to all configured CAN Driver / CAN Transceiver Driver modules.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfDispatchUserCheckTrcvWakeFlagIndicationName
  长名称: ''
  描述: This parameter defines the name of <User_ClearTrcvWufFlagIndication>.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanIfDispatchUserCheckTrcvWakeFlagIndicationUL
  长名称: ''
  描述: This parameter defines the upper layer module to which the CheckTrcvWakeFlagIndication from
      the Driver modules have to be routed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanIfDispatchUserClearTrcvWufFlagIndicationName
  长名称: ''
  描述: This parameter defines the name of <User_ClearTrcvWufFlagIndication>.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CanIfDispatchUserClearTrcvWufFlagIndicationUL
  长名称: ''
  描述: This parameter defines the upper layer module to which the ClearTrcvWufFlagIndication from the
      Driver modules have to be routed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CanIfDispatchUserConfirmPnAvailabilityName
  长名称: ''
  描述: This parameter defines the name of <User_ConfirmPnAvailability>. If
      CANIF_DISPATCH_USERCONFIRMPNAVAILABILITY_UL equals CAN_SM the name of
      <User_ConfirmPnAvailability> is fixed. If it equals CDD, the name is selectable. If
      CANIF_PUBLIC_PN_SUPPORT equals False, this parameter shall not be configurable.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CanIfDispatchUserConfirmPnAvailabilityUL
  长名称: ''
  描述: This parameter defines the upper layer module to which the ConfirmPnAvailability notification
      from the Driver modules have to be routed. If CANIF_PUBLIC_PN_SUPPORT equals False, this
      parameter shall not be configurable.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CanIfDispatchUserCtrlBusOffName
  长名称: ''
  描述: This parameter defines the name of <User_ControllerBusOff>.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CanIfDispatchUserCtrlBusOffUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the notifications of all
      ControllerBusOff events from the CAN Driver modules have to be routed via
      <User_ControllerBusOff>.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CanIfDispatchUserCtrlModeIndicationName
  长名称: ''
  描述: This parameter defines the name of <User_ControllerModeIndication>.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CanIfDispatchUserCtrlModeIndicationUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the notifications of all
      ControllerTransition events from the CAN Driver modules have to be routed
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CanIfDispatchUserTrcvModeIndicationName
  长名称: ''
  描述: This parameter defines the name of <User_TrcvModeIndication>.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: CanIfDispatchUserTrcvModeIndicationUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the notifications of all
      TransceiverTransition events from the CAN Transceiver Driver modules have to be routed
      via <User_TrcvModeIndication>. If no UL module is configured, no upper layer callback
      function will be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: CanIfDispatchUserValidateWakeupEventName
  长名称: ''
  描述: This parameter defines the name of <User_ValidateWakeupEvent>. This
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: CanIfDispatchUserValidateWakeupEventUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the notifications about positive
      former requested wake up sources have to be routed via <User_ValidateWakeupEvent>. If
      parameter CANIF_WAKEUP_CHECK_VALIDATION_API is disabled, this parameter cannot be
      configured.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. CanIfInitCfg

**描述**: This container contains the init parameters of the CAN Interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfInitCfgSet
  长名称: ''
  描述: Selects the CAN Interface specific configuration setup. This type of the external data
      structure shall contain the post build initialization data for the CAN Interface for all
      underlying CAN Dirvers.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. CanIfBufferCfg

**描述**: This container contains the Txbuffer configuration. Multiple buffers with different sizes could be
configured. If CanIfBufferSize (CANIF834_Conf) equals 0, the CanIf Tx L-PDU only refers via this
CanIfBufferCfg the corresponding CanIfHthCfg.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfBufferSize
  长名称: ''
  描述: This parameter defines the number of CanIf Tx L-PDUs which can be buffered in one Txbuffer. If
      this value equals 0, the CanIf does not perform Txbuffering for the CanIf Tx L-PDUs
      which are assigned to this Txbuffer. If CanIfPublicTxBuffering equals False, this
      parameter equals 0 for all TxBuffer. If the CanHandleType of the referred HTH equals
      FULL, this parameter equals 0 for this TxBuffer.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 6. CanIfInitHohCfg

**描述**: This container contains the references to the configuration setup of each underlying CAN Driver.

该容器没有参数。

### 7. CanIfHrhCfg

**描述**: This container contains configuration parameters for each hardware receive object (HRH).

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfHrhSoftwareFilter
  长名称: ''
  描述: Selects the hardware receive objects by using the HRH range/list from CAN Driver configuration
      to define, for which HRH a software filtering has to be performed at during receive
      processing.
  默认值: true
  最小值: ''
  最大值: ''
```

### 8. CanIfHrhRangeCfg

**描述**: Defines the parameters required for configurating multiple CANID ranges for a given same HRH.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfHrhRangeRxPduLowerCanId
  长名称: ''
  描述: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN
      Ids shall pass the software filtering.
  默认值: ''
  最小值: 0
  最大值: 536870911
- 
  序号: 2
  名称: CanIfHrhRangeRxPduRangeCanIdType
  长名称: ''
  描述: Specifies whether a configured Range of CAN Ids shall only consider standard CAN Ids or
      extended CAN Ids.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanIfHrhRangeRxPduUpperCanId
  长名称: ''
  描述: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN
      Ids shall pass the software filtering.
  默认值: ''
  最小值: 0
  最大值: 536870911
```

### 9. CanIfHthCfg

**描述**: This container contains parameters related to each HTH.

该容器没有参数。

### 10. CanIfRxPduCfg

**描述**: This container contains the configuration (parameters) of each receive CAN L-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfRxPduCanId
  长名称: ''
  描述: CAN Identifier of Receive CAN L-PDUs used by the CAN Interface. Exa: Software Filtering. This
      parameter is used if exactly one Can Identifier is assigned to the Pdu. If a range is
      assigned then the CanIfRxPduCanIdRange parameter shall be used.
  默认值: ''
  最小值: 0
  最大值: 536870911
- 
  序号: 2
  名称: CanIfRxPduCanIdType
  长名称: ''
  描述: CAN Identifier of receive CAN L-PDUs used by the CAN Driver for CAN L-PDU reception.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanIfRxPduDlc
  长名称: ''
  描述: Data Length code of received CAN L-PDUs used by the CAN Interface. Exa: DLC check.
  默认值: ''
  最小值: 0
  最大值: 8
- 
  序号: 4
  名称: CanIfRxPduId
  长名称: ''
  描述: ECU wide unique, symbolic handle for receive CAN L-PDU. The CanIfRxPduId is configurable at
      pre-compile and post-built time. It shall fulfill ANSI/AUTOSAR definitions for constant
      defines.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: CanIfRxPduReadData
  长名称: ''
  描述: Enables and disables the Rx buffering for reading of received L-PDU data.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CanIfRxPduReadNotifyStatus
  长名称: ''
  描述: Enables and disables receive indication for each receive CAN L-PDU for reading its
      notification status.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CanIfRxPduUserRxIndicationName
  长名称: ''
  描述: This parameter defines the name of the <User_RxIndication>.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CanIfRxPduUserRxIndicationUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the indication
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. CanIfRxPduCanIdRange

**描述**: Optional container that allows to map a range of CAN Ids to one PduId.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfRxPduCanIdRangeLowerCanId
  长名称: ''
  描述: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN
      Ids are mapped to one PduId.
  默认值: ''
  最小值: 0
  最大值: 536870911
- 
  序号: 2
  名称: CanIfRxPduCanIdRangeUpperCanId
  长名称: ''
  描述: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN
      Ids are mapped to one PduId.
  默认值: ''
  最小值: 0
  最大值: 536870911
```

### 12. CanIfTTRxFrameTriggering

**描述**: This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTTRxJoblistTimeMark
  长名称: ''
  描述: Defines the point in time, when the joblist execution funciton (JLEF) shall be called for the
      referenced rx trigger. Value is given in cycle time. This parameter is only configurable
      if a joblist is enabled by parameter CanIfTTJobList.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 13. CanIfTxPduCfg

**描述**: This container contains the configuration (parameters) of a transmit CAN L-PDU. It has to be
configured as often as a transmit CAN L-PDU is needed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfTxPduCanId
  长名称: ''
  描述: CAN Identifier of transmit CAN L-PDUs used by the CAN Driver for CAN L-PDU transmission.
  默认值: ''
  最小值: 0
  最大值: 536870911
- 
  序号: 2
  名称: CanIfTxPduCanIdType
  长名称: ''
  描述: Type of CAN Identifier of the transmit CAN L-PDU used by the CAN Driver module for CAN L-PDU
      transmission.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanIfTxPduDlc
  长名称: ''
  描述: Data length code (in bytes) of transmit CAN L-PDUs used by the CAN Driver for CAN L-PDU
      transmission.
  默认值: ''
  最小值: 0
  最大值: 8
- 
  序号: 4
  名称: CanIfTxPduId
  长名称: ''
  描述: ECU wide unique, symbolic handle for transmit CAN L-PDU. The CanIfTxPduId is configurable at
      pre-compile and post-built time.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: CanIfTxPduPnFilterPdu
  长名称: ''
  描述: If CanIfPublicPnFilterSupport is enabled, by this parameter PDUs could be configured which
      will pass the CanIfPnFilter.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CanIfTxPduReadNotifyStatus
  长名称: ''
  描述: Enables and disables transmit confirmation for each transmit CAN L-PDU for reading its
      notification status.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CanIfTxPduType
  长名称: ''
  描述: Defines the type of each transmit CAN L-PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CanIfTxPduUserTxConfirmationName
  长名称: ''
  描述: This parameter defines the name of the <User_TxConfirmation>. This
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CanIfTxPduUserTxConfirmationUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the confirmation of the
      successfully transmitted CANTXPDUID has to be routed via the <User_TxConfirmation>.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 14. CanIfTTTxFrameTriggering

**描述**: This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfTTTxJoblistTimeMark
  长名称: ''
  描述: Defines the point in time, when the joblist execution funciton (JLEF) shall be called for the
      referenced tx frame trigger.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 15. CanIfPrivateCfg

**描述**: This container contains the private configuration (parameters) of the CAN Interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfPrivateDlcCheck
  长名称: ''
  描述: Selects whether the DLC check is supported.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanIfPrivateSoftwareFilterType
  长名称: ''
  描述: Selects the desired software filter mechanism for reception only.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanIfSupportTTCAN
  长名称: ''
  描述: Defines whether TTCAN is supported.
  默认值: false
  最小值: ''
  最大值: ''
```

### 16. CanIfTTGeneral

**描述**: This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfTTJoblist
  长名称: ''
  描述: Defines whether TTCAN is processed via a joblist.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanIfTTMaxIsrDelay
  长名称: ''
  描述: Defines the maximum delay for the execution of the joblist execution function JLEF. This
      parameter is only configurable if a joblist is enabled by parameter CanIfTTJobList.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 17. CanIfPublicCfg

**描述**: This container contains the public configuration (parameters) of the CAN Interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfPublicCancelTransmitSupport
  长名称: ''
  描述: Configuration parameter to enable/disable dummy API for upper layer modules which allows to
      request the cancellation of an I-PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanIfPublicCddHeaderFile
  长名称: ''
  描述: Defines header files for callback functions which shall be included in case of CDDs. Range of
      characters is 1.. 32.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanIfPublicChangeBaudrateSupport
  长名称: ''
  描述: Configuration parameter to enable/disable the API to change the baudrate of a CAN controller.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CanIfPublicDevErrorDetect
  长名称: ''
  描述: Enables and disables the development error detection and notification mechanism.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CanIfPublicHandleTypeEnum
  长名称: ''
  描述: This parameter is used to configure the Can_HwHandleType. The Can_HwHandleType represents the
      hardware object handles of a CAN hardware unit. For CAN hardware units with more than
      255 HW objects the extended range shall be used (UINT16).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CanIfPublicMultipleDrvSupport
  长名称: ''
  描述: Selects support for multiple CAN Drivers.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CanIfPublicNumberOfCanHwUnits
  长名称: ''
  描述: Number of served CAN hardware units.
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 8
  名称: CanIfPublicPnSupport
  长名称: ''
  描述: Selects support of Partial Network features in CanIf.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CanIfPublicReadRxPduDataApi
  长名称: ''
  描述: Enables / Disables the API CanIf_ReadRxPduData() for reading received L-PDU data.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CanIfPublicReadRxPduNotifyStatusApi
  长名称: ''
  描述: Enables and disables the API for reading the received L-PDU data.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CanIfPublicReadTxPduNotifyStatusApi
  长名称: ''
  描述: Enables and disables the API for reading the notification status of transmit and receive
      L-PDUs.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: CanIfPublicSetDynamicTxIdApi
  长名称: ''
  描述: Enables and disables the API for reconfiguration of the CAN Identifier for each Transmit
      L-PDU.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: CanIfPublicTxBuffering
  长名称: ''
  描述: Enables and disables the buffering of transmit L-PDUs (rejected by the CanDrv) within the CAN
      Interface module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: CanIfPublicTxConfirmPollingSupport
  长名称: ''
  描述: Configuration parameter to enable/disable the API to poll for Tx Confirmation state.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: CanIfPublicVersionInfoApi
  长名称: ''
  描述: Enables and disables the API  for reading the version information about the CAN Interface.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: CanIfPublicWakeupCheckValidByNM
  长名称: ''
  描述: If enabled, only NM messages shall validate a detected wake-up event
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: CanIfPublicWakeupCheckValidSupport
  长名称: ''
  描述: Selects support for wake up validation
  默认值: false
  最小值: ''
  最大值: ''
```

### 18. CanIfTrcvDrvCfg

**描述**: This container contains the configuration (parameters) of all addressed CAN transceivers by each
underlying CAN Transceiver Driver module. For each CAN transceiver Driver a seperate instance of
this container shall be provided.

该容器没有参数。

### 19. CanIfTrcvCfg

**描述**: This container contains the configuration (parameters) of one addressed CAN transceiver by the
underlying CAN Transceiver Driver module. For each CAN transceiver a seperate instance of this
container has to be provided.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanIfTrcvId
  长名称: ''
  描述: This parameter abstracts from the CAN Transceiver Driver specific parameter Transceiver. Each
      transceiver of all connected CAN Transceiver Driver modules shall be assigned to one
      specific TransceiverId of the CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: CanIfTrcvWakeupSupport
  长名称: ''
  描述: This parameter defines if a respective transceiver of the referenced CAN Transceiver Driver
      modules is queriable for wake up events.
  默认值: false
  最小值: ''
  最大值: ''
```

