# Eth

## 模块描述

Configuration of the Eth (Ethernet driver) module.

## 容器列表

### 1. EthGeneral

**描述**: General configuration of Ethernet Driver module

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthDevErrorDetect
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
  名称: EthVersionInfoApi
  长名称: ''
  描述: |
    This parameter enables/disables the function Eth_GetVersionInfo() to get major, minor and patch
    version information.
    
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthVersionInfoApiMacro
  长名称: ''
  描述: |
    Parameter not used.
    This parameter defines if Eth_GetVersionInfo() is implemented as a macro.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthUserConfigFile
  长名称: User Config File
  描述: |
    Reference to an external text file that will be included during generation to Eth_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
    
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthIndex
  长名称: ''
  描述: |
    Specifies the InstanceId of this module instance. If only one instance is present it shall have
    the Id 0.
    
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: EthMaxCtrlsSupported
  长名称: ''
  描述: |
    This value specifies the maximum number of controller configurations per driver.
    
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 7
  名称: EthUpdatePhysAddrFilter
  长名称: ''
  描述: |
    Enables/Disables optional API Eth_UpdatePhysAddrFilter.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EthEnableRxInterrupt
  长名称: Enable Rx Interrupt
  描述: |
    This parameter defines if the receive interrupt is used.
    
    Restrictions: 'EthEnableRxInterrupt' and 'EthIfEnableRxInterrupt' must be set to the same value.
    
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EthEnableTxInterrupt
  长名称: Enable Tx Interrupt
  描述: |
    This parameter defines if the transmit interrupt is used.
    
    Restrictions: 'EthEnableTxInterrupt' and 'EthIfEnableTxInterrupt' must be set to the same value.
    
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthOsIsrCategory
  长名称: ''
  描述: |
    This parameter specifies how the interrupt routines will be handled.
    
    If CATEGORY_1 or CATEGORY_2 is selected the Os will handle the interrupts according to the
    seleted category.
    For interrupt handling without support from Os the value NO_OS_SUPPORT must be selected.
  默认值: CATEGORY_2
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EthRuntimeMeasurementSupport
  长名称: ''
  描述: |
    If enabled runtime measurement points are added to the BSW module code and are added to the
    module configuration of MICROSAR RTM. The available measurement points can be seen and
    configured in the RTM module configuration. Availability of the MICROSAR RTM module is a
    prerequisite to make use of the runtime measurement functionality.
    Runtime measurement should be disabled in production code as measurement points may inflict
    additional runtime.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: EthEnableZeroCopyExtensions
  长名称: Enable Zero-Copy Extensions
  描述: |
    This parameter defines if the Zero-Copy Extensions for reception buffers and transmission
    buffers are enabled.
    
    Impact on handling of:
    
    Reception Buffers:
    The Rx Buffers aren't implicitly released after the RxIndication() to the upper layer by the
    driver itself anymore but must be explicitly released by the Upper Layer. This mechanism allows
    to keep buffers for explicit usage until the EthIf_ReleaseRxBuffer() API is called.
    
    Transmission Buffers:
    In addition to using internal Tx Buffers provided by the driver during ProvideTxBuffer() a User
    is able to inject external buffers used for transmission with the call to ProvideExtTxBuffer().
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: EthEnableHeaderAccessApi
  长名称: Enable Header Access API
  描述: |
    This parameter defines if APIs are provided to allow access to the Ethernet frame header.
    
    Usually the Ethernet frame header is cut off during reception or is assembled during
    transmission by the Ethernet driver. To read the header information during reception or to
    overwrite the header that is assembled by the driver druing transmission these APIs can be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: EthZeroCopyBufferStartOffset
  长名称: Zero Copy Buffer Start Offset
  描述: |
    Configure the buffer start offset for zero copy extension.
    
    This offset will be added to each buffer start. The additional space can be used for
    transmission on other bus systems. It will not be used for external provided buffers.
    
    Note: The size of the offset must be a multiple of the expected controller alignment size. Value
    0 is allowed to disable the offset.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 15
  名称: EthUsePeripheralAccessApi
  长名称: Use Peripheral Access API
  描述: |
    This parameter defines if the Peripheral Access APIs are used for accessing protected registers
    related to the Ethernet driver.
    
    Depending on the derivative some Ethernet driver related register may be only accessibly in a
    Privileged Mode. If the Ethernet driver is not running in a necessary Privileged Mode then the
    OS has to support the register access by Peripheral Access APIs.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: EthRuntimeEnvironment
  长名称: Runtime Environment
  描述: |
    This parameter defines the runtime environment the Ethernet driver is executed on.
    
    ETH_AUTOSAR_OS:
    The driver is executed in a common AUTOSAR OS environment.
    
    ETH_GREENHILLS_INTEGRITY:
    The driver is executed in a Greenhills INTEGRITY OS environment.
  默认值: ETH_AUTOSAR_OS
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: EthAdditionalIncludes
  长名称: Additional Includes
  描述: This parameter defines an additional file to be included in the Eth_Lcfg.h.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: EthSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: EthMainFunctionPeriod
  长名称: Main Function Period
  描述: This parameter defines the period the main function of the driver is called with.
  默认值: 0.02
  最小值: 0.001
  最大值: 1
- 
  序号: 20
  名称: EthGetEtherStatsApi
  长名称: ''
  描述: This paramter enables or disables the optional GetRxStats / GetTxStats APIs.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: EthPreCtrlInitUserCallout
  长名称: Pre-Controller-Initialization User Callout
  描述: |
    This parameter defines the function to be called before the driver initializes a Ethernet
    controller.
    
    The function that is provided here has to have following signature:
    void <User_PreCtrlInitCallout>(uint8 EthCtrlIdx);
    
    
    NULL_PTR as value disables the functionality.
    
    With the passed EthCtrlIdx, representing the Symbolic Name Value of the respective Ethernet
    Controller, one can distinguish between the initialization context that is currently executed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: EthPostCtrlInitUserCallout
  长名称: Post-Controller-Initialization User Callout
  描述: |
    This parameter defines the function to be called after the driver has initialized a Ethernet
    controller.
    
    The function that is provided here has to have following signature:
    void <User_PostCtrlInitCallout>(uint8 EthCtrlIdx);
    
    
    NULL_PTR as value disables the functionality.
    
    With the passed EthCtrlIdx, representing the Symbolic Name Value of the respective Ethernet
    Controller, one can distinguish between the initialization context that is currently executed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: EthEnableExplicitBufferMapping
  长名称: ''
  描述: |
    This parameter is deprecated: This feature is now always on. The configured value has no effect.
    There are five memory sections that can be used to define the memory locations of the driver's
    buffers and descriptors:
    - RX_BUFFER for the reception buffers
    - TX_BUFFER for the transmission buffers
    - RX_DESCRIPTOR for the reception descriptors
    - TX_DESCRIPTOR for the transmission descriptors
    - DESCRIPTOR_BASE_ADDRESS_TABLE for the descriptor base address table.
    These memory sections are used for the buffers and descriptors of all EthCtrlConfigs (Ethernet
    channels) of this driver.
    
    The final mapping is done via AUTOSAR Memory Map, whereas the user must implement the buffer
    specific memory sections within the memory map by himself according to the hardware
    requirements.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: EthGetAndResetMeasurementDataApi
  长名称: Get and Reset Measurement Data
  描述: |
    This parameter enables/disables the function Eth_GetAndResetMeasurementData() which is used to
    get or reset the vendor specific frame drop statistics due to insufficient buffers.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: EthRxBufWarnLvlCallout
  长名称: Rx Buffer Warning Level Callout
  描述: |
    This parameter defines the function to be called when the driver detects that all the configured
    reception buffers within a EthRxBufConfig are in use by the software. This condition occurs, if
    the DMAC does not have a free buffer to copy additional incoming frame data to, which means that
    frame loss can occur if the situation persists.
    
    The function that is provided here has to have following signature:
    void User_RxBufWarnLvlCallout(uint8 CtrlIdx, uint8 BufRingIdx);
    Where CtrlIdx is the unique identifier for the affected Ethernet controller and BufRingIdx the
    controller local reception buffer ring (BufRingIdx equal to 0 to amount of buffer rings
    configured minus one).
    
    NULL_PTR as value disables the functionality.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. EthConfigSet

**描述**: All included containers and parameters that may be part of a multiple configuration set.

该容器没有参数。

### 3. EthCtrlConfig

**描述**: Configuration of the individual controller

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthCtrlEnableMii
  长名称: ''
  描述: |
    This parameter defines if the Media Independent Interface (MII) for transceiver access is
    enabled.
    
    Restrictions: Must be enabled for transceiver usage.
    
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthCtrlEnableRxInterrupt
  长名称: ''
  描述: |
    This parameter defines if the receive interrupt for the controller is enabled.
    
    Restrictions: 'EthCtrlEnableRxInterrupt' must be equal for all controllers and equal to
    'EthEnableRxInterrupt'
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthCtrlEnableTxInterrupt
  长名称: ''
  描述: |
    This parameter defines if the transmit interrupt for the controller is enabled.
    
    Restrictions: 'EthCtrlEnableTxInterrupt' must be equal for all controllers and equal to
    'EthEnableTxInterrupt'
    
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthCtrlIdx
  长名称: ''
  描述: |
    This value specifies the instance ID of the configured controller.
    
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: EthCtrlRxBufLenByte
  长名称: Max receive buffer length
  描述: |
    This value specifies the maximum receive buffer length (frame length).
    
    Restrictions: Value has to be the maximum value of all 'EthCtrlRxBufLenByte' in 'EthRxBufConfig'
    containers.
    
    
  默认值: 1522
  最小值: 0
  最大值: 1522
- 
  序号: 6
  名称: EthCtrlTxBufLenByte
  长名称: Max transmit buffer length
  描述: |
    This value specifies the maximum transmit buffer length (frame length).
    
    Resctrictions: Value has to be the maximum value of all 'EthCtrlTxBufLenByte' in
    'EthTxBufConfig' containers.
    
    
  默认值: 1522
  最小值: 0
  最大值: 1522
- 
  序号: 7
  名称: EthRxBufTotal
  长名称: ''
  描述: |
    This value specifies the number of receive buffers.
    Resctrictions: Value has to be the sum of all values of 'EthRxBufTotal' in container
    'EthRxBufConfig'.
    
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: EthTxBufTotal
  长名称: ''
  描述: |
    This value specifies the number of transmit buffers.
    Restrictions: Value has to be the sum of all values of 'EthTxBufTotal' in container
    'EthTxBufConfig'.
    
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: EthCtrlEnableMacWriteAccess
  长名称: ''
  描述: |
    This parameter defines if access to an NvM block containing the MAC address and the
    corresponding API is enabled.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthCtrlPhysAddr
  长名称: Physical Address (MAC-Address)
  描述: |
    This parameter defines the Controller Physical Hardware Address (MAC-Address). The input format
    has to match xx:xx:xx:xx:xx:xx, where x stands for a hex value between 0 and F.
    
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EthCtrlEnableQoS
  长名称: Enable QoS
  描述: |
    This parameter defines if QoS (Quality of Service) is enabled.
    
    VLAN tagged frames are prioritized according to their VLAN priority. The priority handling is
    taken into account during reception and transmission of frames.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: EthCtrlEnablePtp
  长名称: ''
  描述: This parameter defines if Precision-Time-Protocol support is enabled or not. PTP is mostly
      used in combination with Audio Video Bridging (AVB)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: EthCtrlEnableTrafficShaping
  长名称: ''
  描述: This parameter defines whether Traffic Shaping is used. Therefore the ethernet controller uses
      an algorithm like CBS (Credit Based Shaping) for limiting the maximum bandwidth per
      queue.
  默认值: NO_TRAFFIC_SHAPING
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: EthEnableAVBConformance
  长名称: ''
  描述: |
    This parameter defines if the QoS/FQTSS features a used for a AVB or generalized usecase.
    In the AVB usecase a maximum  of 75% of the Port Transmit Rate can be used for traffic class A
    and B. Only frames with a frametype related to AVB are passed to the queues for traffic class A
    and B.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: EthCtrlMiiInterface
  长名称: PHY Managment Interface
  描述: |
    This parameter defines the interface type used to connect PHY and MAC.
    
    Please refere to the derivative's reference manual and the board schematic to retrieve the
    correct interface type.
  默认值: ETH_MII_MODE
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: EthCtrlPeripheralRegionOsIdentifier
  长名称: Peripheral Region Os Identifier
  描述: Unique C Identifier which is used by the Ethernet Controller driver for accessing the OS
      configured peripheral region.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: EthCtrlResetLoopMaxCycles
  长名称: Controller Reset Loop Cycles
  描述: |
    This value specifies the number of loop cycles after the controller reset timeout occurs.
    
  默认值: 1000
  最小值: 1
  最大值: 1000000
- 
  序号: 18
  名称: EthCtrlMiiLoopMaxCycles
  长名称: Controller MII Loop Cycles
  描述: This value specifies the number of loop cycles after the timeout for MII accesses occurs.
  默认值: 1000
  最小值: 1
  最大值: 1000000
- 
  序号: 19
  名称: EthCtrlLoopMaxCycles
  长名称: Controller Loop Cycles
  描述: |
    This value specifies the number of loop cycles after hardware dependent loop timeouts occur.
    
  默认值: 1000
  最小值: 1
  最大值: 1000000
- 
  序号: 20
  名称: EthEthSwtMgmtHdrLen
  长名称: EthSwt Management Header Length
  描述: This parameter defines the additional management header length inserted by an Ethernet switch
      doing frame management for special frames.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 21
  名称: EthCtrlEnableOsfMode
  长名称: ''
  描述: This parameter defines whether OSF mode is used for frame transmission. When OSF mode is
      enabled, the processing of a second Tx-descriptor is started before the first one is
      transmitted completely. This results in increased throughput in transmission.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: EthCtrlCsrClkRange
  长名称: CSR Clock Range
  描述: |
    The CSR clock range determines the frequency of the MDC clock according to CSR clock frequnecy.
    
    The MDC clock should be approximately between 1.0 MHz to 2.5 MHz.
    
    
    
  默认值: CLK_20_35_MHZ
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: EthCtrlPrtSpdSel
  长名称: Port Speed Selection
  描述: |
    This parameter selects the ethernet port speed (10Mbit/s, 100Mbit/s and 1000Mbit/s) .
    
  默认值: PS_1000_MBITS
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: EthCtrlSkewTx
  长名称: Skew Tx value
  描述: |
    This value specifies for a  transceiver speed of 1000Mbit/s the TX clock delay for RGMII mode.
    (value * 222,22 ps)
    It is not applicable for transceiver speeds lower than 1000Mbit/s.
  默认值: 2
  最小值: 0
  最大值: 15
- 
  序号: 25
  名称: EthCtrlSkewRx
  长名称: Skew Rx value
  描述: |
    This value specifies  for a  transceiver speed of 1000Mbit/s the RX clock delay for RGMII mode.
    (value * 222,22 ps)
    It is not applicable for transceiver speeds lower than 1000Mbit/s.
  默认值: 0
  最小值: 0
  最大值: 15
- 
  序号: 26
  名称: EthTxConfirmationCallout
  长名称: ''
  描述: |
    This parameter defines the alternative function to be called upon the confirmation of an
    Ethernet frame instead of the EthIf_TxConfirmation.
    
    NULL_PTR as value disables the functionality and the EthIf_TxConfirmation is called again.
    
    The signature of the function specified in this parameter has to match the signature of the
    EthIf_TxConfirmation used in the delivery.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: EthRxIndicationCallout
  长名称: ''
  描述: |
    This parameter defines the alternative function to be called upon the reception of an Ethernet
    frame instead of the EthIf_RxIndication.
    
    NULL_PTR as value disables the functionality and the EthIf_RxIndication is called again.
    
    The signature of the function specified in this parameter has to match the signature of the
    EthIf_RxIndication used in the delivery.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: EthCtrlEnablePpsEventOnTimeApi
  长名称: Enable Pps Event on Time Api
  描述: This parameter enables the ArmPpsEventOnTime Api. The Api is used for PPS sub-module of the
      Ethernet MAC to trigger an event on the PPS line at the given globalTime.
  默认值: false
  最小值: ''
  最大值: ''
```

### 4. EthRxBufConfig

**描述**: This container includes the configuration of an Rx buffer.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthRxSegmentNumber
  长名称: Number of Rx Segments
  描述: This value defines the number of Rx segments the receiver buffer is assembled of.
  默认值: 2
  最小值: 2
  最大值: 65535
- 
  序号: 2
  名称: EthRxExtSegmentNumber
  长名称: Number of Extended Rx Segments
  描述: |
    This value specifies the maximum expected number of extended buffers that can be used for frame
    reception.
    The number of normal buffers (Parameter 'Number of Rx Buffers') is used to generate the amount
    of RX descriptors and normal RX buffers. Due to the delayed RX buffer release for the zero copy
    feature RX descriptors could be blocked and the packet reception would be stopped. During a
    delayed buffer release the extended buffers are used to assign them to the RX descriptor, while
    a buffer release is still pending.
    The packet number that can be received during a burst may be limited to 'Number of Rx Buffers',
    but with the extended buffer it is still possible receive this burst while buffer releases are
    still pending.
    
    Restrictions: The amount of normal and extended buffers must not exceed a total of 255.
  默认值: 2
  最小值: 1
  最大值: 255
- 
  序号: 3
  名称: EthRxSegmentSize
  长名称: Rx Buffer Segment Size
  描述: |
    This parameter defines the size of a segment the receive buffer is built of.
    
    Multiple of these segments are used to hold a complete Ethernet frame.
  默认值: 1522
  最小值: 60
  最大值: 1600
- 
  序号: 4
  名称: EthRxMaxFrameSize
  长名称: Maximum Rx Frame Size
  描述: This parameter defines the maximum length of an Ethernet frame, which is allowed to be
      received.
  默认值: 1522
  最小值: 60
  最大值: 1600
```

### 5. EthTxBufConfig

**描述**: This container includes the configuration of a Tx buffer.


#### 参数列表

```yaml
- 
  序号: 1
  名称: EthCtrlTxBufLenByte
  长名称: Maximum Buffer Size
  描述: |
    This value limits the maximum length (including Ethernet header + payload + CRC) of the Ethernet
    frame in bytes.
    In case VLAN is enabled the Ethernet header length is 18, otherwise 14. The maximum payload
    length is 1500 bytes and the minimum length is 46 bytes. The CRC consists of 4 bytes.
    
    Example:
    - Configuring a buffer that shall hold a VLAN tagged Ethernet frame with a maximum payload of
    1500 bytes, the overall frame length is 1500 bytes payload + 18 bytes header + 4 bytes CRC =
    1522 bytes.
    - Configuring a buffer that shall hold an Ethernet frame without VLAN tag and a minimum payload
    of 46 bytes, the overall frame length is 46 bytes payload + 14 bytes header + 4 bytes CRC = 64
    bytes.
  默认值: 1522
  最小值: 64
  最大值: 1522
- 
  序号: 2
  名称: EthTxBufTotal
  长名称: Number of Tx Buffers
  描述: This value specifies the number of transmit buffers.
  默认值: 2
  最小值: 2
  最大值: 255
```

### 6. EthDemEventParameterRefs

**描述**: This container includes the references to DemEventParameter elements which shall be invoked using
the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from
the referenced DemEventParameter's DemEventId value.


该容器没有参数。

### 7. EthQosConfig

**描述**: This container includes the configuration which is necessary for QoS (QualityOfService).

该容器没有参数。

### 8. EthQosRxQueue

**描述**: This container includes the configuration for the receive queues.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthMappedVlanPriority
  长名称: ''
  描述: This parameter defines which VLAN priorities are mapped to this receive queue.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: EthPriority
  长名称: ''
  描述: This parameter defines the priority of the queue. The priority is hardware dependent and set
      by DaVinci Configurator automatically.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 9. EthQosTxQueue

**描述**: This container includes the configuration for the transmit queues.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthMappedVlanPriority
  长名称: ''
  描述: This parameter defines which VLAN priorities are mapped to this transmit queue.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: EthPriority
  长名称: ''
  描述: This parameter defines the priority of the queue. The priority is hardware dependent and set
      by DaVinci Configurator automatically.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: EthQueueBandwidthLimit
  长名称: ''
  描述: This parameter defines maximum bandwidth which can be used by this queue in Bits/s
  默认值: 10000000
  最小值: 0
  最大值: 1000000000
- 
  序号: 4
  名称: EthTransmissionQueueType
  长名称: ''
  描述: This parameter defines the type of the configured queue. This type is hardware dependent and
      set by a validator. Upper layers need this parameters for a mapping betwenn vlan
      priority and the type of a queue.
  默认值: ETH_NON_AVB_QUEUE
  最小值: ''
  最大值: ''
```

### 10. EthCtrlOffloading

**描述**: This container includes the configuration for checksum offloading.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthCtrlEnableOffloadChecksumIPv4
  长名称: Enable IPv4 Checksum Offloading
  描述: This parameter defines that the IPv4 checksum calculation is offloaded to the ethernet
      controller and calculated by hardware.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthCtrlEnableOffloadChecksumICMP
  长名称: Enable ICMPv4 Checksum Offloading
  描述: This parameter defines that the ICMP checksum calculation is offloaded to the ethernet
      controller and calculated by hardware.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthCtrlEnableOffloadChecksumTCP
  长名称: Enable IPv4 encapsulated TCP Checksum Offloading
  描述: This parameter defines that the checksum calculation for IPv4 encapsulated TCP segments is
      offloaded to the ethernet controller and calculated by hardware.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthCtrlEnableOffloadChecksumUDP
  长名称: Enable IPv4 encapsulated UDP Checksum Offloading
  描述: This parameter defines that the checksum calculation for IPv4 encapsulated UDP is offloaded to
      the ethernet controller and calculated by hardware.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthCtrlEnableOffloadChecksumTCPv6
  长名称: Enable IPv6 encapsulated TCP Checksum Offloading
  描述: This parameter defines that the checksum calculation for IPv6 encapsulated TCPis offloaded to
      the ethernet controller and calculated by hardware.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthCtrlEnableOffloadChecksumICMPv6
  长名称: Enable ICMPv6 Checksum Offloading
  描述: This parameter defines that the ICMPv6 checksum calculation is offloaded to the ethernet
      controller and calculated by hardware.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EthCtrlEnableOffloadChecksumIPv6HeaderRouting
  长名称: Enable IPv6 Header Routing Checksum Offloading
  描述: This parameter defines that the checksum offloading  for protocols encapsulated in IPv6 with
      Routing extension header is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EthCtrlEnableOffloadChecksumIPv6HeaderDestinationOptions
  长名称: Enable IPv6 Header Destination Option Checksum Offloading
  描述: This parameter defines that the checksum offloading for protocols encapsulated in IPv6 with
      Destination Options extension header is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EthCtrlEnableOffloadChecksumIPv6HeaderHopByHopOptions
  长名称: Enable IPv6 Header Hop By Hop Checksum Offloading
  描述: This parameter defines that the checksum offloading for protocols encapsulated in IPv6 with
      Hop by Hop Options extension header is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthCtrlEnableOffloadChecksumUDPv6
  长名称: Enable IPv6 encapsulated UDP Checksum Offloading
  描述: This parameter defines that the checksum calculation for IPv6 encapsulated UDP is offloaded to
      the ethernet controller and calculated by hardware.
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. EthExtTxBufConfig

**描述**: This container contains the configuration for external transmission buffers.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthCtrlMaxExtBufNum
  长名称: Maximum Amount of External Tx Buffers
  描述: This value specifies the maximum number of external transmission buffers that shall shall be
      injected simultaniously.
  默认值: 2
  最小值: 1
  最大值: 255
```

### 12. EthAutosarOs

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthRegBaseAddress
  长名称: Register Base Address
  描述: This parameter defines the register base address for the Ethernet controller used.
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
```

### 13. EthGreenhillsIntegrityOs

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthRegMemRegionIdentifier
  长名称: Register Memory Region Identifier
  描述: This parameter defines the identifier used to identify the phyiscal Memory Region representing
      the Ethernet controllers register space.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthDeviceIdentifier
  长名称: Device Identifier
  描述: This parameter defines the identifier used to identify the IO Device object representing the
      Ethernet controller within INTEGRITY.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthResManagerPassword
  长名称: Resource Manager Password
  描述: |
    This paramter defines the password used to grant access to the Resource Manager of INTEGRITY.
    
    This password is used within calls to the INTEGRITY Resource Manager (e.g. RequestResource()) to
    retrieve the needed OS objects for IO Device, register memory region and so on.
    
    If no password is used by the Resource Manager NULL must be provided as value to signal the omit
    of the password check.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthRegMemRegionPool
  长名称: Register Memory Region Pool
  描述: |
    This parameter defines the Memory Region Pool where the virtual Memory Region to map the
    registers into the virtual address space is drawn from.
    
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthEventPriority
  长名称: Event Priority
  描述: This parameter defines the prioirty of the event issued to user space to handle interrupt
      events issued by the Ethernet controller.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: EthAsrOsWrapperIsrNo
  长名称: AUTOSAR OS Wrapper ISR Number
  描述: This parameter defines the define generated by the INTEGRITY AUTOSAR OS wrapper for the ISR
      number related to the Ethernet controller.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 14. EthInterruptMapping

**描述**: This container holds the configuration elements necessary to configure the interrupt mapping for the
different supported derivatives.

该容器没有参数。

### 15. EthInterruptServiceRoutine

**描述**: This container defines an ISR which aggregates the possible events that result in issuing an
interrupt.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthPreIsrUserFunction
  长名称: Pre ISR User Function
  描述: |
    This parameter defines a user function that shall be called at the start of the ISR.
    
    The function declaration must be provided by a header file added to EthAdditionalIncludes in the
    EthGeneral configuration container.
    
    Function signature shall be as followed:
    void <UserFunction>(uint8 CtrlIdx);
    
    NULL_PTR: No user function shall be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthPostIsrUserFunction
  长名称: Post ISR User Function
  描述: |
    This parameter defines a user function that shall be called at the end of the ISR.
    
    The function declaration must be provided by a header file added to EthAdditionalIncludes in the
    EthGeneral configuration container.
    
    Function signature shall be as followed:
    void <UserFunction>(uint8 CtrlIdx);
    
    NULL_PTR: No user function shall be called.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 16. EthIrqEventList

**描述**: IRQ event processing list of the ISR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIrqHandlerPos
  长名称: IRQ Handler Processing Position
  描述: This parameter defines the position within the IRQ processing list of the ISR.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 17. EthIrqEvent

**描述**: Container represents the processing function of a specific interrupt event.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthIrqEventDescription
  长名称: IRQ Event Description
  描述: This parameter describes which interrupt event is handled by the IRQ event processing
      function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 18. EthCtrlPinRouting

**描述**: This container contains parameter for pin routing, which is done by ETH_GPCTL register.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Eth_GPCTL_ALT0
  长名称: ''
  描述: This parameter defines the value of ALT0 of the ETH_GPCTL register.
  默认值: ETH_ALT_1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Eth_GPCTL_ALT1
  长名称: ''
  描述: This parameter defines the value of ALT1 of the ETH_GPCTL register.
  默认值: ETH_ALT_0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Eth_GPCTL_ALT2
  长名称: ''
  描述: This parameter defines the value of ALT2 of the ETH_GPCTL register.
  默认值: ETH_ALT_0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Eth_GPCTL_ALT3
  长名称: ''
  描述: This parameter defines the value of ALT3 of the ETH_GPCTL register.
  默认值: ETH_ALT_0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Eth_GPCTL_ALT4
  长名称: ''
  描述: This parameter defines the value of ALT4 of the ETH_GPCTL register.
  默认值: ETH_ALT_0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Eth_GPCTL_ALT5
  长名称: ''
  描述: This parameter defines the value of ALT5 of the ETH_GPCTL register.
  默认值: ETH_ALT_0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Eth_GPCTL_ALT6
  长名称: ''
  描述: This parameter defines the value of ALT6 of the ETH_GPCTL register.
  默认值: ETH_ALT_0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Eth_GPCTL_ALT7
  长名称: ''
  描述: This parameter defines the value of ALT7 of the ETH_GPCTL register.
  默认值: ETH_ALT_0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: Eth_GPCTL_ALT8
  长名称: ''
  描述: This parameter defines the value of ALT8 of the ETH_GPCTL register.
  默认值: ETH_ALT_0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: Eth_GPCTL_ALT9
  长名称: ''
  描述: This parameter defines the value of ALT9 of the ETH_GPCTL register.
  默认值: ETH_ALT_0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: Eth_GPCTL_ALT10
  长名称: ''
  描述: This parameter defines the value of ALT10 of the ETH_GPCTL register.
  默认值: ETH_ALT_0
  最小值: ''
  最大值: ''
```

