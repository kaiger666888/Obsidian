# EthTSyn

## 模块描述

The Ethernet Time Synchronization module implements a protocol for time synchronization over
Ethernet. It is developed according to AUTOSAR specification which is based on IEEE802.1As ((g)PTP)
with some modifications.
#Ethernet #TimeSync #AVB
#AUTOSAR

## 容器列表

### 1. EthTSynGeneral

**描述**: This container holds the general parameters of the Ethernet-specific Synchronized Time-base Manager

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynDestPhyAddr
  长名称: ''
  描述: |
    Destination Physical Address (MAC-Address).
    Destination Physical Hardware Address (MAC-Address) of EthTSyn-gPTP Frmaes. Input format has to
    match xx:xx:xx:xx:xx:xx, where x stands for a hex value between 0 and F.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthTSynDevErrorDetect
  长名称: ''
  描述: Switches the development error detection and notification on or off.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTSynGlobalTimeRxToUplinkSwitchResidenceTime
  长名称: ''
  描述: |
    This parameter is specifying the default value used for the residence time of the Ethernet
    Switch [Ingress to Uplink].
    This value is used by the EthTSyn if the calculation of the residence time failed.
  默认值: 0
  最小值: 0
  最大值: 4
- 
  序号: 4
  名称: EthTSynGlobalTimeUplinkToTxSwitchResidenceTime
  长名称: ''
  描述: |
    This parameter is specifying the default value used for the residence time of the Ethernet
    Switch [Uplink to Egress].
    This value is used by the EthTSyn if the calculation of the residence time failed.
  默认值: 0
  最小值: 0
  最大值: 4
- 
  序号: 5
  名称: EthTSynHardwareTimestampSupport
  长名称: ''
  描述: Activate/Deactivate the hardware time stamping functionality of the Ethernet hardware.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthTSynMainFunctionPeriod
  长名称: ''
  描述: |
    Schedule period of the main function EthTSyn_MainFunction.
    
    Note: Only integral milliseconds are supported
  默认值: 0.005
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: EthTSynMasterSlaveConflictDetection
  长名称: ''
  描述: Enables master / slave conflict detection and notification.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EthTSynMessageCompliance
  长名称: ''
  描述: |
    * true: IEEE 802.1AS compliant message format will be used.
    * false: IEEE 802.1AS message format with AUTOSAR extension will be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EthTSynSwitchMgmtRxMessageBufferCount
  长名称: ''
  描述: This parameter is used to determine the amount of Rx message buffers available in the EthTSyn
      when EthTSyn is used in a Bridge configuration.
  默认值: 10
  最小值: 1
  最大值: 255
- 
  序号: 10
  名称: EthTSynVersionInfoApi
  长名称: ''
  描述: Activate/Deactivate the version information API (EthTSyn_GetVersionInfo). True: version
      information API activated False: version information API deactivated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EthTSynUserConfigFile
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
  名称: EthTSynPublicCddHeaderFile
  长名称: ''
  描述: Defines header files for call-back functions (e.g. Sync / FollowUp sent) which shall be
      included in case of CDDs. Range of characters is 1.. 32.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: EthTSynSwitchMgmtRxMessageBufferPayloadSize
  长名称: ''
  描述: |
    This parameter is specifying the size of the payload portion for each Bridge message buffer in
    Bytes.
    This size has to be configured such that every expected EthTSyn-Frame can be stored here. Please
    note that the Common Ptp Header (34 Byte) is excluded from this size here.
  默认值: 42
  最小值: 42
  最大值: 1500
- 
  序号: 14
  名称: EthTSynEnableSwitchMgmt
  长名称: ''
  描述: This parameter is used to determine if the Switch management functionality of the EthTSyn is
      enabled or disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: EthTSynSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: EthTSynSwitchMgmtMainFunctionPeriod
  长名称: ''
  描述: |
    Schedule period of the main function EthTSyn_SwtMgmt_MainFunction.
    
    Note: Only integral milliseconds are supported
  默认值: 0.001
  最小值: 0
  最大值: 65535
- 
  序号: 17
  名称: EthTSynSwitchMgmtTxMgmtObjQueueSize
  长名称: ''
  描述: This parameter is used to determine the size of the Tx mamagement object queue in the EthTSyn
      when EthTSyn is used in a Bridge configuration.
  默认值: 10
  最小值: 1
  最大值: 255
- 
  序号: 18
  名称: EthTSynSwitchMgmtBridgeMode
  长名称: ''
  描述: Selection of the bridge operation mode
  默认值: TRANSPARENT_CLOCK
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: EthTSynSwitchMgmtSwitchAndHostAsOneTimeAwareSystem
  长名称: ''
  描述: |
    Selection whether the Ethernet Switch and the host controller are considered as one time-aware
    system.
    
    When switch and host are considered as one time-aware system, it is expected that both the
    switch and the Ethernet controller of the host use the same clock source (are both clocks are
    synchronized, which is out of scope for the EthTSyn).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: EthTSynAsymTransparentClockEgrTsBufSize
  长名称: ''
  描述: Amount of egress timestamps which can be per received frame.
  默认值: 10
  最小值: 1
  最大值: 255
- 
  序号: 21
  名称: EthTSynEnablePortParameterStatistics
  长名称: ''
  描述: This parameter is used to determine if the port parameter statistics functionality of the
      EthTSyn is enabled or disabled.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. EthTSynGlobalTimeDomain

**描述**: This represents the existence of a global time domain on Ethernet. The EthTSyn module can
administrate several global time domains at the same time that in itself form a hierarchy of domains
and sub-domains.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynGlobalTimeDomainId
  长名称: ''
  描述: |
    The global time domain ID.
    
    Note: This value is automatically derived from the StbMSynchronizedTimeBase referenced by
    EthTSynSynchronizedTimeBaseRef.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: EthTSynSwitchMgmtKeepSourcePortIdentity
  长名称: ''
  描述: |
    This parameter is only used in a bridge configuration.
    
    When this parameter is enabled, the source port identity of forwarded Sync/FollowUp messages is
    not modified.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTSynSwitchMgmtGlobalTimeSyncTimeout
  长名称: ''
  描述: |
    This parameter is only used in a Bridge configuration. It specifies the time, the bridge is
    waiting for the reception of a new Sync message on its slave port before a Grand Master timeout
    is assumed and the Bridge begins to generate its own Sync and FollowUp messages.
    
    Note: A value of 0 disable this timeout observation. In case this timeout observation is
    disabled, the grandmaster capable bridge will not start generating its own Sync and FollowUp
    messages in case no more Sync/FollowUp messages are received on the bridges slave port.
  默认值: 0
  最小值: 0
  最大值: 4
- 
  序号: 4
  名称: EthTSynIsOffsetTimeDomain
  长名称: ''
  描述: |
    Information only (computed automatically).
    
    This parameter is set to 'TRUE' if the EthTSynSynchronizedTimeBaseRef of this time domain point
    to an offset time base.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthTSynEnableTimeValidation
  长名称: ''
  描述: |
    Enables/disables time recording for time validation for a specific Time Domain.
    
    Note: Value is set according to parameter StbMEnableTimeValidation of the referenced Time Base
    in the StbM
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthTSynSwitchMgmtNumMsgForwardRetries
  长名称: ''
  描述: |
    This parameter is only used in a bridge configuration. It defines the amount of retries done for
    forwarded Sync and FollowUp messages.
    
    Note: Some hints regarding the value and meaning of the retry counter are described in the
    Technical Reference of the EthTSyn module.
  默认值: 3
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: EthTSynGlobalTimeDomainDestPhyAddr
  长名称: ''
  描述: |
    This parameter can be used to override the Destination Physical Hardware Address (MAC-Address)
    of EthTSyn-gPTP Frames (configured via EthTSynGeneral/EthTSynDestPhyAddr) for the
    EthTSynGlobalTimeDomain. Input format has to match xx:xx:xx:xx:xx:xx, where x stands for a hex
    value between 0 and F.
    
    When this parameter exists, this value will be used as destination MAC for frames transmitted in
    this time domain. In case of a multicast MAC-Address, the physical address filter of the HW will
    be updated to be able to receive frames with this destination address as well.
    
    Note: In case of a Unicast address, no update of the physical address filter will be done. If
    frames need to be received directed to this unicast address, the user has to ensure that
    reception is possible (e.g. by enabling the promiscuous mode of the HW).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. EthTSynGlobalTimeFollowUpDataIDList

**描述**: The DataIDList for Follow_Up message ensures the identification of data elements due to CRC
calculation process.

该容器没有参数。

### 4. EthTSynGlobalTimeFollowUpDataIDListElement

**描述**: Element of the DataIDList for Follow_Up message ensures the identification of data elements due to
CRC calculation process.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynGlobalTimeFollowUpDataIDListIndex
  长名称: ''
  描述: Index of the DataIDList for Follow_Up message ensures the identification of data elements due
      to CRC calculation process.
  默认值: 0
  最小值: 0
  最大值: 15
- 
  序号: 2
  名称: EthTSynGlobalTimeFollowUpDataIDListValue
  长名称: ''
  描述: Value of the DataIDList for Follow_Up message ensures the identification of data elements due
      to CRC calculation process.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 5. EthTSynPortConfig

**描述**: Configuration of the EthTSyn-Ports within the TimeDomain.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynFramePrio
  长名称: ''
  描述: This optional parameter, if present, indicates the priority of outgoing EthTSyn messages, if
      sent via VLAN (used for the 3-bit PCP field of the VLAN tag). If this optional parameter
      is not present, frames are sent without a priority and VLAN field.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: EthTSynGlobalTimeDebounceTime
  长名称: ''
  描述: This represents the configuration of a TX debounce time for messages transmitted by the
      EthTSyn on the same physical/HW port.
  默认值: 0
  最小值: 0
  最大值: 4
- 
  序号: 3
  名称: EthTSynPortNumber
  长名称: ''
  描述: Determines the Port Number
  默认值: 0
  最小值: 0
  最大值: 65534
- 
  序号: 4
  名称: EthTSynPortIndex
  长名称: ''
  描述: |
    Index of the PortConfig within the context of the EthTSyn. This index is only used if
    EthTSynEnablePortParameterStatistics is enabled and only for PortConfigs which collect port
    paramter statistices. See TechRef for more details about which PortConfigs are relevant for this
    feature.
    
    This Index is calculated automatically and provided as symbolic name value.
  默认值: 0
  最小值: 0
  最大值: 254
```

### 6. EthTSynPdelayConfig

**描述**: Configuration of cyclic propagation delay measurement.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynGlobalTimePdelayRespEnable
  长名称: ''
  描述: This parameter allows disabling Pdelay_Resp / Pdelay_Resp_Follow_Up transmission, if no
      Pdelay_Req messages are expected.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthTSynGlobalTimePropagationDelay
  长名称: ''
  描述: |
    If cyclic propagation delay measurement is enabled, this parameter represents the default value
    of the propagation delay until the first actually measured propagation delay is available.
    If cyclic propagation delay measurement is disabled, this parameter represents the static value
    of the propagation delay.
  默认值: 0
  最小值: 0
  最大值: 4
- 
  序号: 3
  名称: EthTSynGlobalTimeTxPdelayReqPeriod
  长名称: ''
  描述: |
    This represents configuration of the TX period for Pdelay_Req messages.
    A value of 0 disables the cyclic Pdelay measurement.
  默认值: 1
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: EthTSynPdelayRespAndRespFollowUpTimeout
  长名称: ''
  描述: |
    Timeout value for Pdelay_Resp and Pdelay_Resp_Follow_Up after a Pdelay_Req has been transmitted
    resp. a Pdelay_Resp has been received.
    A value of 0 deactivates this timeout ovservation.
  默认值: 0
  最小值: 0
  最大值: 4
- 
  序号: 5
  名称: EthTSynPdelayAverageWeight
  长名称: ''
  描述: |
    To determine the Pdelay, a weighted average calculation can be used instead of always take the
    last measured value.
    
    This parameter represents the weight factor (w) for PathDelay calculation:
    NewPathDelay = ( ( (w - 1) * OldPathDelay) + CurrentPathDelay) / w
  默认值: 30
  最小值: 1
  最大值: 255
- 
  序号: 6
  名称: EthTSynPdelayReqAllowedLostResponses
  长名称: ''
  描述: Determines the number of allowed lost responses of a PDelay_Request. If this count is
      exceeded, the AsCapable Flag of the Port is set to false.
  默认值: 3
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: EthTSynPdelayLatencyThreshold
  长名称: ''
  描述: |
    Threshold for calculated Pdelay. If a measured Pdelay exceeds
    EthTSynPdelayLatencyThreshold, this value is discarded.
    
    Unit: seconds
    
    Note: Lost response counter is incremented in case of discarded Pdelay.
  默认值: 1E-05
  最小值: 0
  最大值: 4
- 
  序号: 8
  名称: EthTSynUseStaticPdelay
  长名称: ''
  描述: When this parameter is set to TRUE, the configured Pdelay value
      (EthTSynGlobalTimePropagationDelay) is always used as Pdelay. The optional Pdelay
      measurement does not affect this value.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EthTSynAlwaysAsCapable
  长名称: Always AsCapable
  描述: |
    This parameter sets AsCapable to true without checking for a gPTP-capable counterpart via
    Pdelay-Mechanism. The AsCapable flag will not be influenced by the Pdelay-Mechanism at all.
    According to IEEE 802.1AS this parameter must be false at start-up and is set automatically to
    true if a gPTP-capable device at the other end of the link is detected.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthTSynPdelayRespUseGlobalTime
  长名称: ''
  描述: |
    This parameter is used to determine if a Pdelay Responder shall use the global or the virtual
    local time within Pdelay_Resp and Pdelay_Resp_Fup messages.
    
    Note:
    Can only be enabled when:
    - EthTSynGeneral/EthTSynMessageCompliance is enabled
    - EthTSynGeneral/EthTSynEnableSwitchMgmt is disabled
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. EthTSynGlobalTimeMaster

**描述**: Configuration of the global time master. Each global time domain is required to have exactly one
global time master. This master may or may not exist on the configured ECU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynCyclicMsgResumeTime
  长名称: ''
  描述: Defines the time where the 1st regular cycle time based message transmission takes place,
      after an immediate transmission before.
  默认值: 0
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 2
  名称: EthTSynGlobalTimeTxCrcSecured
  长名称: ''
  描述: This represents the configuration of whether or not CRC is supported.
  默认值: CRC_NOT_SUPPORTED
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTSynGlobalTimeTxPeriod
  长名称: ''
  描述: |
    This represents configuration of the TX period for Sync/FollowUp messages.
    
    Notes:
    - A value of '0' disables the cyclic Sync message transmission (requires
    EthTSynImmediateTimeSync == TRUE).
    This parameter does not have any effect (hence, the above mentioned restriction does not apply
    as well) when all of the following conditions are true:
    - /MICROSAR/EthTSyn/EthTSynGeneral/EthTSynSwitchMgmtBridgeMode is set to
    ASYMMETRIC_TRANSPARENT_CLOCK or TRANSPARENT_CLOCK
    - /MICROSAR/EthTSyn/EthTSynGlobalTimeDomain also contains a slave port
    (/MICROSAR/EthTSyn/EthTSynGlobalTimeDomain/EthTSynPortConfig/EthTSynPortRole/EthTSynGlobalTimeSlave)
  默认值: 0.125
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 4
  名称: EthTSynImmediateTimeSync
  长名称: ''
  描述: |
    Enables/Disables the cyclic polling of StbM_GetTimeBaseUpdateCounter() within
    EthTSyn_MainFunction() and therefore the optional transmission of immediate time sync messages.
    
    Note:
    This parameter does not have any effect when all of the following conditions are true:
    - /MICROSAR/EthTSyn/EthTSynGeneral/EthTSynSwitchMgmtBridgeMode is set to
    ASYMMETRIC_TRANSPARENT_CLOCK or TRANSPARENT_CLOCK
    - /MICROSAR/EthTSyn/EthTSynGlobalTimeDomain also contains a slave port
    (/MICROSAR/EthTSyn/EthTSynGlobalTimeDomain/EthTSynPortConfig/EthTSynPortRole/EthTSynGlobalTimeSlave)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthTSynSyncSentCallBackFunction
  长名称: ''
  描述: |
    This function is called after a SYNC message has successfully been transmitted.
    Call-back function has following signature:
    
    
    void EthTSyn_SyncSentCallback(EthTSyn_IntPortIdxType PortIdx, const uint8* TxBufPtr );
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthTSynFollowUpSentCallBackFunction
  长名称: ''
  描述: |
    This function is called after a FOLLOW_UP message has successfully been transmitted.
    Call-back function has following signature:
    
    void EthTSyn_FollowUpSentCallback(EthTSyn_IntPortIdxType PortIdx, const uint8* TxBufPtr);
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EthTSynTxAnnouncePeriod
  长名称: ''
  描述: |
    This represents configuration of the TX period for optional Announce messages.
    
    Note: A value of '0' disables the cyclic Announce message transmission.
  默认值: 0.125
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 8
  名称: EthTSynTxSubTLVOFS
  长名称: Tx Sub TLV OFS
  描述: |
    Definition of whether (true) or not (false) a Sub-TLV:OFS Secured or Sub-TLV:OFS Not Secured
    shall be sent in the AUTOSAR TLV of a Follow_Up message.
    
    Note: Parameter as defined in AUTOSAR 22-11
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EthTSynTxSubTLVStatus
  长名称: ''
  描述: |
    Definition of whether (true) or not (false) a Sub-TLV:Status Secured or Sub-TLV:Status Not
    Secured shall be sent in the AUTOSAR TLV of a Follow_Up message.
    
    Note: Parameter as defined in AUTOSAR 22-11
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthTSynTxSubTLVTime
  长名称: ''
  描述: |
    Definition of whether (true) or not (false) a Sub-TLV:Time Secured shall be sent in the AUTOSAR
    TLV of a Follow_Up message.
    
    Note: Parameter as defined in AUTOSAR 22-11
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EthTSynTxSubTLVUserData
  长名称: ''
  描述: |
    Definition of whether (true) or not (false) a Sub-TLV:UserData Secured or Sub-TLV:User Data Not
    Secured shall be sent in the AUTOSAR TLV of a Follow_Up message.
    
    Note: Parameter as defined in AUTOSAR 22-11
  默认值: false
  最小值: ''
  最大值: ''
```

### 8. EthTSynCrcTimeFlagsTxSecured

**描述**: This container collects definitions which parts of the Follow_Up message elements shall be used for
CRC calculation.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynCrcCorrectionField
  长名称: ''
  描述: correctionField from the Follow_Up Message Header shall be included in CRC calculation.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthTSynCrcDomainNumber
  长名称: ''
  描述: domainNumber from the Follow_Up Message Header shall be included in CRC calculation.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTSynCrcMessageLength
  长名称: ''
  描述: messageLength from the Follow_Up Message Header shall be included in CRC calculation.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthTSynCrcPreciseOriginTimestamp
  长名称: ''
  描述: preciseOriginTimestamp from the Follow_Up Message Field shall be included in CRC calculation.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthTSynCrcSequenceId
  长名称: ''
  描述: sequenceId from the Follow_Up Message Header shall be included in CRC calculation.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthTSynCrcSourcePortIdentity
  长名称: ''
  描述: sourcePortIdentity from the Follow_Up Message Header shall be included in CRC calculation.
  默认值: false
  最小值: ''
  最大值: ''
```

### 9. EthTSynGlobalTimeSlave

**描述**: Configuration of a time slave. Each global time domain is required to have at least one time slave.
The configured ECU may or may not represent a time slave.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynGlobalTimeFollowUpTimeout
  长名称: ''
  描述: |
    Timeout value of the Follow_Up message (of the subsequent Sync message).
    
    A value of 0 deactivates this timeout observation.
  默认值: 0.125
  最小值: 0
  最大值: 4
- 
  序号: 2
  名称: EthTSynRxCrcValidated
  长名称: ''
  描述: |
    Definition of whether or not validation of the CRC is supported.
    
    CRC_IGNORED - EthTSyn accepts all FollowUp messages. Possibly included CRCs in any ArSubTlv will
    be ignored.
    CRC_NOT_VALIDATED - EthTSyn only accepts FollowUp messages where no CRC is included in optional
    ArSubTlvs (i.e. SubTlv Types: 0x51, 0x61 and 0x34).
    CRC_OPTIONAL - EthTSyn accepts all FollowUp messages. If an ArSubTlv inlcudes a CRC, the CRC is
    validated.
    CRC_VALIDATED - EthTSyn only accepts FollowUp messages where CRC is included in optional
    ArSubTlvs (i.e. SubTlv Types: 0x28, 0x50, 0x60 and 0x44). The Crc is validated.
  默认值: CRC_IGNORED
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTSynAnnounceMaxStepRemoved
  长名称: ''
  描述: |
    This represents the maximum number of network hops between the Grandmaster and this slave.
    
    Note: Only used when EthTSynEnableAnnounce==true
  默认值: 7
  最小值: 1
  最大值: 254
- 
  序号: 4
  名称: EthTSynAnnounceTimeout
  长名称: ''
  描述: |
    Determines the maximum delay time in ms between incoming Announce messages sent by the master.
    
    Note: Only used when EthTSynEnableAnnounce==true
  默认值: 0.1
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: EthTSynEnableAnnounce
  长名称: ''
  描述: When this option is enabled, the slave has to receive an valid annouce message before
      synchronization is possible. The slave stores the ClockIdentity of the GrandMaster
      (received via announce message) and validates Sync/FollowUp messages using this clock
      identity.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthTSynEnableSourcePortIdentityCheck
  长名称: ''
  描述: |
    This parameter speciefies whether the SourcePortIdentity of received Sync/FollowUp messages
    should be verified or not.
    
    Note: When enabled, the valid source port identity for Sync/FollowUp messages has to be
    configured using the container EthTSynSourcePortIdentityCheckConfig.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EthTSynFollowUpCorrectionFieldThreshold
  长名称: ''
  描述: |
    This represents a threshold in nanoseconds for the correction field of a FollowUp message
    received by the slave.
    The FollowUp message is discarded if this threshold is exceeded.
  默认值: 281474976710655
  最小值: 0
  最大值: 281474976710655
- 
  序号: 8
  名称: EthTSynRxSubTLVOFS
  长名称: Rx Sub TLV OFS
  描述: |
    Definition of whether or not a Sub-TLV:OFS Secured or Sub-TLV:OFS Not Secured shall be present
    and shall be evaluated when processing a received Follow_Up message.
    
    Note: Parameter as defined in AUTOSAR 22-11
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EthTSynRxSubTLVStatus
  长名称: ''
  描述: |
    Definition of whether or not a Sub-TLV:Status Secured or Sub-TLV:Status Not Secured shall be
    present and shall be evaluated when processing a received Follow_Up message.
    
    Note: Parameter as defined in AUTOSAR 22-11
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthTSynRxSubTLVTime
  长名称: ''
  描述: |
    Definition of whether or not a Sub-TLV:Time Secured shall be present and shall be evaluated when
    processing a received Follow_Up message.
    
    Note: Parameter as defined in AUTOSAR 22-11
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EthTSynRxSubTLVUserData
  长名称: ''
  描述: |
    Definition of whether or not a Sub-TLV:UserData Secured or Sub-TLV:UserData Not Secured shall be
    present and shall be evaluated when processing a received Follow_Up message.
    
    Note: Parameter as defined in AUTOSAR 22-11
  默认值: false
  最小值: ''
  最大值: ''
```

### 10. EthTSynCrcFlagsRxValidated

**描述**: This container collects definitions which parts of the Follow_Up message elements shall be included
in CRC validation.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynCrcCorrectionField
  长名称: ''
  描述: correctionField from the Follow_Up Message Header shall be included in CRC calculation.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthTSynCrcDomainNumber
  长名称: ''
  描述: domainNumber from the Follow_Up Message Header shall be included in CRC calculation.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTSynCrcMessageLength
  长名称: ''
  描述: messageLength from the Follow_Up Message Header shall be included in CRC calculation.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthTSynCrcPreciseOriginTimestamp
  长名称: ''
  描述: preciseOriginTimestamp from the Follow_Up Message Field shall be included in CRC calculation.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthTSynCrcSequenceId
  长名称: ''
  描述: sequenceId from the Follow_Up Message Header shall be included in CRC calculation.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthTSynCrcSourcePortIdentity
  长名称: ''
  描述: sourcePortIdentity from the Follow_Up Message Header shall be included in CRC calculation.
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. EthTSynSourcePortIdentityCheckConfig

**描述**: Configuration of the Master Source Port Identity used to verifiy the Source Port Identity of
Sync/FollowUp received by the slave if Source Port Identity Check is enabled.

Note: Only used when EthTSynEnableSourcePortIdentityCheck==true

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynMasterPhysicalAddress
  长名称: ''
  描述: The Physical Hardware Address (MAC-Address) of Time Master. Input format has to match
      xx::xx::xx::xx::xx::xx, where x stands for a hex value between 0 and F.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 12. EthTSynSwitchTimeSyncConfig

**描述**: Configuration of all parameters required for the time synchronization of the Ethernet Switch.

Note: Only Ethernet switches configured here will be synchronized.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynSwitchTimeSyncSyncPrecisionLimit
  长名称: ''
  描述: |
    This parameter is used to determine the max allowed offset of the Switch time to the global
    time.
    If this limit is exceeded, the SyncState changes to UNSYNC.
    
    Note: The Offset is measured with each synchronization event.
  默认值: 1E-05
  最小值: 0
  最大值: 4
- 
  序号: 2
  名称: EthTSynSwitchTimeSyncMaxOutOfSyncCount
  长名称: ''
  描述: This parameter inidcates how often in a row the measured Switch offset can exceed the
      configured SwitchSyncPrecisionLimit befor the Sync state is changed to UNSYNC.
  默认值: 3
  最小值: 1
  最大值: 255
- 
  序号: 3
  名称: EthTSynSwitchTimeSyncSyncStateChangeCallback
  长名称: ''
  描述: |
    Callout to inform about a change of the sync state of the Switch.
    Call-back function has following signature:
    
    void SyncStateChgCbk(uint8 EthTSynSwitchIdx, EthTSyn_SyncStateType SyncState)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthTSynSwitchTimeSyncIndex
  长名称: ''
  描述: |
    Index of the Switch (cascade)/SwitchTimeSyncConfig within the context of the EthTSyn.
    
    This Index is calculated automatically and provided as symbolic name value.
  默认值: 0
  最小值: 0
  最大值: 254
- 
  序号: 5
  名称: EthTSynSwitchTimeSyncApplyRateRatioToSlaveSwitches
  长名称: ''
  描述: |
    With this parameter it can be decided if a correction of the RateRatio has to be applied to the
    slave switches seperatly or not:
    
    TRUE:  RateRatio is applied to all slave switches seperatly
    FALSE: RateRatio is only applied to the master switch
    
    Notes:
    - This parameter is only relevant when at least one slave switch is configured
    - When
    ./EthTSynSwitchTimeSyncMechanism/EthTSynRateRegulator/EthTSynUseOffsetCorrectionForInitialCorrection
    is enabled, the initial offset correction is always applied to all slave switches
    - Setting of this parameter depends on the Hardware setup (e.g. it might be set to FALSE when
    the master switch is providing the clock for the slave switches)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthTSynSwitchTimeSyncSyncEventTimeout
  长名称: ''
  描述: |
    Timeout for sync event. When no sync event occurres (or required timestamps of the sync event
    are not available) within this timeout, the sync state will be changed to ETHTSYN_UNCERTAIN.
    
    Note: A value of 0 disables the timeout observation.
  默认值: 1
  最小值: 0
  最大值: 4
```

### 13. EthTSynRateRegulator

**描述**: Configuration of the RateRegulator time synchronization method:

- Offset correction (time leap) is only performed when the Sync-State was never reached yet
(optional)
- Adoption of the RateRatio (frequency) is done in such way, that absolute time offsets are
corrected without time leaps

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynUseOffsetCorrectionForInitialCorrection
  长名称: ''
  描述: Decide if offset correction should be used before reaching the Sync-State for the first time.
      This might be useful to compensate big time offset at startup.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthTSynRateRatioMax
  长名称: ''
  描述: |
    Defining the max allowed value of the RateRatio.
    If the RateRatio calculated by the regulator exceeds this threshold, it is set to this value.
    
    Note: This value onyl defines the boundary for the relative RateRatio (i.e. the RateRatio
    computed with one synchronitation event)
  默认值: 1.1
  最小值: 1
  最大值: 2
- 
  序号: 3
  名称: EthTSynRateRatioMin
  长名称: ''
  描述: |
    Defining the max allowed value of the RateRatio.
    If the RateRatio calculated by the regulator falls below this threshold, it is set to this
    value.
    
    Note: This value onyl defines the boundary for the relative RateRatio (i.e. the RateRatio
    computed with one synchronitation event)
  默认值: 0.9
  最小值: 0.5
  最大值: 1
- 
  序号: 4
  名称: EthTSynNumberOfParallelRateMeasurements
  长名称: ''
  描述: Decide how many rate measurements are running parallel. A higher value increases the duration
      of each rate measurement. This decreases the effect of errors due to fluctuations of the
      sync cycle duration. A lower value on the other hand, increases performance.
  默认值: 3
  最小值: 1
  最大值: 255
- 
  序号: 5
  名称: EthTSynNumberOfSyncCyclesForOffsetCorrection
  长名称: ''
  描述: Decide how many sync cycles it should take for the rate regulator to correct an offset. High
      values might increase the duration until the system is synchronized but stabilize the
      regulating mechanism.
  默认值: 3
  最小值: 1
  最大值: 255
- 
  序号: 6
  名称: EthTSynOffsetJumpCorrectionThreshold
  长名称: ''
  描述: If the offset exceeds this value, offset jump correction is used instead of rate regulator.
      This can be useful for large offsets because the rate regulator might need too long to
      synchronize in this case.
  默认值: 0.001
  最小值: 1E-09
  最大值: 4
```

