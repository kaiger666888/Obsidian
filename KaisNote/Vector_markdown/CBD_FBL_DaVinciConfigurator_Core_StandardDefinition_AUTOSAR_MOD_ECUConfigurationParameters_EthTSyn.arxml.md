# EthTSyn

## 模块描述

Configuration of the Synchronized Time-base Manager (StbM) module with respect to global time
handling on Ethernet.

## 容器列表

### 1. EthTSynGeneral

**描述**: This container holds the general parameters of the Ethernet-specific Synchronized Time-base Manager

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynDevErrorDetect
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
  名称: EthTSynHardwareTimestampSupport
  长名称: ''
  描述: |
    Activate/Deactivate the hardware time stamping functionality of the Ethernet hardware.
    True: Clock is administrated by EthIf-Lower layer (e.g. Eth). Timestamps are requested from
    EthIf (e.g. EthIf_GetIngressTimestamp())
    False: Clock is administrated by StbM, therefore timestamps are provided by the StbM.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthTSynMainFunctionPeriod
  长名称: ''
  描述: Schedule period of the main function EthTSyn_MainFunction. Unit: [s].
  默认值: 0.005
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 4
  名称: EthTSynVersionInfo
  长名称: ''
  描述: |
    Activate/Deactivate the version information API (EthTSyn_GetVersionInfo) to get major, minor and
    patch version information.
    True: version information API activated
    False: version information API deactivated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthTSynDestPhyAddr
  长名称: Destination Physical Address (MAC-Address)
  描述: Destination Physical Hardware Address (MAC-Address) of EthTSyn-gPTP Frames. Input format has
      to match xx::xx::xx::xx::xx::xx, where x stands for a hex value between 0 and F.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
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
  序号: 7
  名称: EthTSynPublicCddHeaderFile
  长名称: ''
  描述: Defines header files for call-back functions (e.g. Sync / FollowUp sent) which shall be
      included in case of CDDs. Range of characters is 1.. 32.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EthTSynGmCapable
  长名称: Grand Master Capable
  描述: Select whether the EthTSyn can act as Grand Master. In a bridge configuration, the ECU will
      take over the role of the GM in case a Sync-Timeout is detected on the Slave-Por
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
  描述: The global time domain ID.
  默认值: 0
  最小值: 0
  最大值: 31
- 
  序号: 2
  名称: EthTSynGlobalTimeFollowUpTimeout
  长名称: ''
  描述: Specifies the time waited for the reception of a FollowUp message after receiving a Sync
      message. After the Timeout the Sync message will be discarded. Unit: seconds
  默认值: 0.125
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 3
  名称: EthTSynGlobalTimeSyncTimeout
  长名称: ''
  描述: This parameter is only used in a Bridge configuration. It specifies the time, the bridge is
      waiting for the reception of a new Sync message on its slave port before a Grand Master
      timeout is assumed and the Bridge begins to generate its own Sync and FollowUp messages.
  默认值: 0.25
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: EthTSynBridgeKeepSourcePortIdentity
  长名称: ''
  描述: |
    This parameter is only used in a bridge configuration.
    
    When this parameter is enabled, the source port identity of forwarded Sync/FollowUp messages is
    not modified.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. EthTSynGlobalTimeMaster

**描述**: Configuration of the global time master. Each global time domain is required to have exactly one
global time master. This master may or may not exist on the configured ECU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynGlobalTimeTxFollowUpOffset
  长名称: ''
  描述: This represents configuration of the TX offset for Follow_Up / Pdelay_Resp_Follow_Up messages.
      Unit: seconds
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: EthTSynGlobalTimeTxPdelayReqPeriod
  长名称: ''
  描述: This represents configuration of the TX period for Pdelay_Req messages. Unit: seconds
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: EthTSynGlobalTimeTxPeriod
  长名称: ''
  描述: This represents configuration of the TX period. Unit: seconds
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 4. EthTSynGlobalTimeSlave

**描述**: Configuration of a time slave. Each global time domain is required to have at least one time slave.
The configured ECU may or may not represent a time slave.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynGlobalTimeTxFollowUpOffset
  长名称: ''
  描述: This represents configuration of the TX offset for Follow_Up / Pdelay_Resp_Follow_Up messages.
      Unit: seconds
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: EthTSynGlobalTimeTxPdelayReqPeriod
  长名称: ''
  描述: This represents configuration of the TX period for Pdelay_Req messages. Unit: seconds
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: EthTSynTimeHardwareCorrectionThreshold
  长名称: ''
  描述: This parameter can be taken to define the maximum deviation between the local time and the
      time obtained from SYNC message that triggers a correction of the time drift caused by
      the hardware on the local node.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. EthTSynTimeSourceConfig

**描述**: Configuration of the Time Sources used by the EthTSyn module

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynTimestampMethod
  长名称: ''
  描述: |
    Select which timestamping method is used.
    HW_TIMESTAMPING:
    - Clock is managed in HW
    
    STBM_TIMESTAMPING:
    - Clock is managed in StbM
    
    OS/GPT/CALLOUT_TIMESTAMPING:
    - Clock is managed in EthTSyn
    - Local Time is derived from Os/Gpt Counter or from UserCallout
  默认值: HW_TIMESTAMPING
  最小值: ''
  最大值: ''
```

### 6. EthTSynTimestampCalloutConfig

**描述**: Configuration of Timestamp Usercallout.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthTSynTimestampUserCallout
  长名称: ''
  描述: |
    Name of the User-Callout function when Timestamp Method is set to "CALLOUT-TIMESTAMPING".
    This Function is called when EthTSyn_GetCurrentTimeRaw is invoked.
    The Callout-function has the following signature:
    
    Std_ReturnType TimestampUserCallout(EthTSyn_TimestampTickType *CurrentTickTime)
    
    The function shall return "E_OK" when the retrieval of the Time was successful and "E_NOT_OK"
    otherwise.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthTSynUserCalloutMaxValue
  长名称: ''
  描述: Max Tick Value returned by the Usercallout.
  默认值: 1000000000
  最小值: 1
  最大值: 4294967296
- 
  序号: 3
  名称: EthTSynUserIncludeFile
  长名称: ''
  描述: This parameter defines a header file name which shall be included by EthTSyn for the Timestamp
      UserCallout.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthTSynUserCalloutNsPerTick
  长名称: ''
  描述: Time of one "Tick" (returned by the Usercallout) in Nanoseconds.
  默认值: 1
  最小值: 1
  最大值: 1000000000
```

