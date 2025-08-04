# vItaHlp

## 模块描述

Configuration of the vItaHlp (Vector Integration Test Application for Hardware License Package)
module.

## 容器列表

### 1. vItaHlpTestModules

**描述**: Test Module definitions of vItaHlp.

该容器没有参数。

### 2. vItaHlpCanTestModule

**描述**: Definitions of CAN test modules for vItaHlp.
Add a container for each CAN Driver under test.
A CAN test module may comprise several CanTestConfig containers.

该容器没有参数。

### 3. vItaHlpCanTestConfig

**描述**: Definition of parameters used for the vItaHlp CAN module tests.
Add a container for each CAN Controller under test.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vItaHlpCanCanoeChannelName
  长名称: Canoe Channel Name
  描述: |
    Set the name as configured in the CANoe network.
    Do not use CANoe keywords (CAN1...CAN32) as channel name. Generally avoid using similar
    constructs like CAN0, CAN00, etc. for channel names.
    
    Note: Please take care that the Canoe Channel names are consistent (e.g. use the same Canoe
    Channel name if TestCom and CAN Test Module references the same CAN Controller).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vItaHlpCanStandardTestCommunicationRx
  长名称: Standard Test - Communication Rx
  描述: |
    Enables CAN reception tests for the Unit Under Test (CAN Controller).
    The CAN reception test is instantiated for all referenced Standard Test Elements which represent
    CAN Hardware Rx objects.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vItaHlpCanStandardTestCommunicationTx
  长名称: Standard Test - Communication Tx
  描述: |
    Enables CAN transmission tests for the Unit Under Test (CAN Controller).
    The CAN transmission test is instantiated for all referenced Standard Test Elements which
    represent CAN Hardware Tx objects.
  默认值: true
  最小值: ''
  最大值: ''
```

### 4. vItaHlpOsTestModule

**描述**: Definitions of the OS test module for vItaHlp.
An OS test module may comprise several OsTestConfig containers.

该容器没有参数。

### 5. vItaHlpOsTestConfig

**描述**: Definition of parameters used for the vItaHlp OS module tests.
Add a container for each OS Core under test.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vItaHlpOsStandardTestStartup
  长名称: Standard Test - Startup
  描述: |
    Enables OS Startup test for the Unit Under Test (OS Core).
    The OS Startup test is instantiated for the referenced OS Test Communication Task Ref.
    For detailed information regarding the demands on the referenced OsTask refer to the description
    of the vItaHlpOsTestCommunicationTaskRef parameter.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vItaHlpOsStandardTestCounter
  长名称: Standard Test - Counter
  描述: |
    Enables OS Counter test for the Unit Under Test (OS Core).
    The OS Counter test is instantiated for the referenced OS Counter. It checks that the configured
    alarm action is performed, when the corresponding counter event occurs and the alarm expires.
    The OS Counter must be referenced by an OS Alarm with a configured OsAlarmAction
    OsAlarmActivateTask. The task which is referenced by the alarm action must not be used/activated
    by the RTE/BRE during execution of vItaHlp. The task implementation is provided by vItaHlp.
  默认值: false
  最小值: ''
  最大值: ''
```

### 6. vItaHlpOsStandardTestCounterTestElement

**描述**: Definition of test element parameters used for the OS Counter test.
Add a container for each test element.

该容器没有参数。

### 7. vItaHlpEthTestModule

**描述**: Definitions of Eth test modules for vItaHlp.
Add a container for each Ethernet driver under test.
An Eth test module may comprise several EthTestConfig containers.

该容器没有参数。

### 8. vItaHlpEthTestConfig

**描述**: Definition of parameters used for the vItaHlp Eth module tests.
Add a container for each Ethernet controller under test.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vItaHlpEthCanoeChannelName
  长名称: Canoe Channel Name
  描述: |
    Set the name as configured in the CANoe network.
    Do not use CANoe keywords (Eth1...Eth32) as channel name. Generally avoid using similar
    constructs like Eth0, Eth00, etc. for channel names.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vItaHlpEthStandardTestCommunicationTx
  长名称: Standard Test - Communication Tx
  描述: Enables the Eth transmission test for the Unit Under Test (Ethernet controller).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vItaHlpEthStandardTestCommunicationRx
  长名称: Standard Test - Communication Rx
  描述: Enables the Eth reception test for the Unit Under Test (Ethernet controller).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vItaHlpEthStandardTestEgressTimestampIncreasingPlausible
  长名称: Standard Test - Egress Timestamp Increasing/Plausible
  描述: Enables the Eth Egress Timestamp Increasing and Plausible Test for the Unit Under Test
      (Ethernet controller).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vItaHlpEthStandardTestIngressTimestampIncreasingPlausible
  长名称: Standard Test - Ingress Timestamp Increasing/Plausible
  描述: Enables the Eth Ingress Timestamp Increasing and Plausible Test for the Unit Under Test
      (Ethernet controller).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vItaHlpEthStandardTestGlobalTimestampIncreasingPlausible
  长名称: Standard Test - Global Timestamp Increasing/Plausible
  描述: Enables the Eth Global Timestamp Increasing and Plausible Test for the Unit Under Test
      (Ethernet controller).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vItaHlpEthStandardTestCrossTimestampIncreasing
  长名称: Standard Test - Cross Timestamp Increasing
  描述: Enables the Eth Cross Timestamp Increasing Test for the Unit Under Test (Ethernet controller).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vItaHlpEthStandardTestEgressTimestampEnablingDisabling
  长名称: Standard Test - Egress Timestamp Enabling/Disabling
  描述: |
    Enables the Eth Egress Timestamp Enabling/DisablingTest for the Unit Under Test (Ethernet
    controller).
    
    This test is limited to Ethernet ASR Versions 4.4.0 and higher. If the controller under test has
    ASR version 4.3.1 or lower, this test must not be activated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vItaHlpEthNumberOfCyclesForTimestampTests
  长名称: Number of cycles for Timestamp tests
  描述: Sets the cycle count for Egress Timestamp Increasing/Plausible Test, Ingress TImestamp
      Increasing/Plausible Test and Global Timestamp Increasing/Plausible Test.
  默认值: 5
  最小值: 2
  最大值: 100
- 
  序号: 10
  名称: vItaHlpEthToleranceForTimeDifferencePlausibilityCheck
  长名称: Tolerance for time difference plausibility check
  描述: |
    Sets the tolerance of time difference in milliseconds for the plausibility part of Egress
    Timestamp Increasing/Plausible Test, Ingress Timestamp Increasing/Plausible Test and Global
    Timestamp Increasing/Plausible Test.
    
    Contains information about how much time difference deviation in timestamps of two consecutive
    frames is accepted. Tolerance is set as +/- value, so accepted tolerance time span is twice as
    big as set value.
    
    If value is set to 0, plausibility part of tests will not be executed.
  默认值: 5
  最小值: 0
  最大值: 40
```

### 9. vItaHlpFlsTestModule

**描述**: Definitions of Fls test module for vItaHlp.
A Fls test module may comprise several FlsTestConfig containers.

该容器没有参数。

### 10. vItaHlpFlsTestConfig

**描述**: Definition of parameters used for the vItaHlp Fls module tests.
Add a container for each flashable sector under test.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vItaHlpFlsStandardTestFlsWrite
  长名称: Standard Test - Flash Write
  描述: |
    Enables the Flash Write test for the Unit Under Test (FlsSector).
    Requires the following APIs from the Fls module to be enabled:
       - /Fls/FlsGeneral/FlsCompareApi
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vItaHlpFlsStandardTestFlsRead
  长名称: Standard Test - Flash Read
  描述: Enables the Flash Read test for the Unit Under Test (FlsSector).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vItaHlpFlsStandardTestFlsCompare
  长名称: Standard Test - Flash Compare
  描述: |
    Enables the Flash Compare test for the Unit Under Test (FlsSector).
    Requires the following APIs from the Fls module to be enabled:
       - /Fls/FlsGeneral/FlsCompareApi
       - /Fls/FlsGeneral/FlsGetJobResultApi
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vItaHlpFlsStandardTestFlsEraseAndBlankCheck
  长名称: Standard Test - Flash Erase and BlankCheck
  描述: |
    Enables the Flash Erase and BlankCheck test for the Unit Under Test (FlsSector).
    Disable this test, in case the Fls_BlankCheck API is not supported at all by the DUT, or in case
    the Fls_BlankCheck API is disabled for the given Fls driver module.
    Requires the following APIs from the Fls module to be enabled:
       - /Fls/FlsGeneral/FlsGetJobResultApi
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. vItaHlpFlsStandardTestTestElement

**描述**: Definition of test element parameters used for the Fls test.
Add a container for each test element.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vItaHlpFlsStandardTestTestElementStartPage
  长名称: Start Page
  描述: The index of the page of a flash memory area, which is used for the test. The index 0 denotes
      the first page of the first sector. The index is unique over all flash pages of the Unit
      Under Test (FlsSector).
  默认值: 0
  最小值: 0
  最大值: ''
- 
  序号: 2
  名称: vItaHlpFlsStandardTestTestElementNumberOfPages
  长名称: Number of Pages
  描述: |
    The number of consecutive flash pages, used for the test.
    The maximum number of flash pages is given by the number of configured flash sectors
    (FlsNumberOfSectors), the size of a flash sector (FlsSectorSize) and the size of a flash page
    (FlsPageSize) as:
    max number of pages = FlsNumberOfSectors * FlsSectorSize / FlsPageSize
  默认值: 1
  最小值: 1
  最大值: ''
```

### 12. vItaHlpMcuTestModule

**描述**: Definitions of MCU test module for vItaHlp.
The MCU test module contains a single MCUTestConfig container.

该容器没有参数。

### 13. vItaHlpMcuTestConfig

**描述**: Definition of parameters used for the vItaHlp MCU module tests.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vItaHlpMcuStandardTestPerformReset
  长名称: Standard Test - Perform Reset
  描述: Enables the MCU Perform Reset test.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vItaHlpMcuStandardTestClockTiming
  长名称: Standard Test - Clock Timing
  描述: |
    Enables the MCU Clock Timing test.
    The MCU Clock Timing test requires an OS alarm with a configured OsAlarmAction
    OsAlarmActivateTask. The referenced task must not be used/activated by the RTE/BRE during
    execution of vItaHlp.
    Moreover, the referenced task must not be used by another vItaHlp test module.
    The task implementation is provided by vItaHlp.
  默认值: true
  最小值: ''
  最大值: ''
```

### 14. vItaHlpLinTestModule

**描述**: Definitions of LIN test modules for vItaHlp.
Add a container for each LIN Driver under test.
A LIN test module may comprise several LinTestConfig containers.

该容器没有参数。

### 15. vItaHlpLinTestConfig

**描述**: Definition of parameters used for the vItaHlp LIN module tests.
Add a container for each LIN channel under test.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vItaHlpLinCanoeChannelName
  长名称: Canoe Channel Name
  描述: |
    Set the name as configured in the CANoe network.
    Do not use CANoe keywords (LIN1...LIN32) as channel name. Generally avoid using similar
    constructs like LIN0, LIN00, etc. for channel names.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vItaHlpLinStandardTestCommunicationMasterResponse
  长名称: Standard Test - Communication Master Response
  描述: Enables the LIN transmission test with response from LIN Master for the Unit Under Test (LIN
      channel).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vItaHlpLinStandardTestCommunicationSlaveResponse
  长名称: Standard Test - Communication Slave Response
  描述: Enables the LIN transmission test with response from LIN Slave for the Unit Under Test (LIN
      channel).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vItaHlpLinStandardTestSleepWakeupFromMaster
  长名称: Standard Test - Sleep/Wakeup from Master
  描述: Enables the LIN Sleep/Wakeup test for the Unit Under Test (LIN channel). The wakeup is
      initiated from LIN Master.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vItaHlpLinStandardTestSleepWakeupFromSlave
  长名称: Standard Test - Sleep/Wakeup from Slave
  描述: Enables the LIN Sleep/Wakeup test for the Unit Under Test (LIN channel). The wakeup is
      requested from LIN Slave.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vItaHlpLinStandardTestCommunicationIgnoreResponse
  长名称: Standard Test - Communication Ignore Response
  描述: |
    Enables the LIN transmission test for no response on LIN channel under test.
    The test can be enabled only for LIN Slave nodes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vItaHlpLinModuleUnitUnderTestNodeType
  长名称: Node Type
  描述: The node type of the LIN channel, for which the tests shall be executed.
  默认值: MASTER
  最小值: ''
  最大值: ''
```

### 16. vItaHlpWdgTestModule

**描述**: Definitions of WDG test modules for vItaHlp.
Add a container for each Watchdog driver under test.
The WDG test module contains a single WDG TestConfig container.

该容器没有参数。

### 17. vItaHlpWdgTestConfig

**描述**: Definition of parameters used for the vItaHlp WDG module tests.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vItaHlpWdgStandardTestImmediateReset
  长名称: Standard Test - Immediate Reset
  描述: Enables the WDG Immediate Reset test.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vItaHlpWdgStandardTestTimingResetSlow
  长名称: Standard Test - Timing Reset Slow
  描述: |
    Enables the WDG test to verify the timing conditions of the watchdog driver.
    For this test, the watchdog hardware is configured with a long timeout period (Slow-Mode).
    The test can be enabled, if the HW derivative
       - Supports Slow-Mode AND
       - Slow-Mode is configured as default mode OR switching to Slow-Mode is supported during
    runtime.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vItaHlpWdgStandardTestTimingResetFast
  长名称: Standard Test - Timing Reset Fast
  描述: |
    Enables the WDG test to verify the timing conditions of the watchdog driver.
    For this test, the watchdog hardware is configured with a short timeout period (Fast-Mode).
    The test can be enabled, if the HW derivative
       - Supports Fast-Mode AND
       - Fast-Mode is configured as default mode OR switching to Fast-Mode is supported during
    runtime.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vItaHlpWdgStandardTestDisableAllowed
  长名称: Standard Test - Disable Allowed
  描述: |
    Enables the WDG test to verify, if disabling of the watchdog driver is allowed.
    Enable this test, if switching from Fast-Mode or Slow-Mode to Off-Mode is supported during
    runtime.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vItaHlpTimeoutPeriodSlow
  长名称: ''
  描述: The timeout period used for triggering the watchdog hardware, if configured for long timeout
      period (Slow-Mode).
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: vItaHlpTimeoutPeriodFast
  长名称: ''
  描述: The timeout period used for triggering the watchdog hardware, if configured for short timeout
      period (Fast-Mode).
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 18. vItaHlpTestCom

**描述**: Test Communication for vItaHlp.

该容器没有参数。

### 19. vItaHlpTestComCan

#### 参数列表

```yaml
- 
  序号: 1
  名称: vItaHlpCanCanoeChannelName
  长名称: Canoe Channel Name
  描述: |
    Set the name as configured in the CANoe network.
    Do not use CANoe keywords (CAN1...CAN32) as channel name. Generally avoid using similar
    constructs like CAN0, CAN00, etc. for channel names.
    
    Note: Please take care that the Canoe Channel names are consistent (e.g. use the same Canoe
    Channel name if TestCom and CAN Test Module references the same CAN Controller).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 20. vItaHlpTestComEth

#### 参数列表

```yaml
- 
  序号: 1
  名称: vItaHlpEthCanoeChannelName
  长名称: Canoe Channel Name
  描述: |
    Set the name as configured in the CANoe network.
    Do not use CANoe keywords (Eth1...Eth32) as channel name. Generally avoid using similar
    constructs like Eth0, Eth00, etc. for channel names.
    
    Note: Please take care that the Canoe Channel names are consistent (e.g. use the same Canoe
    Channel name if TestCom and Eth Test Module references the same Eth Controller).
  默认值: ''
  最小值: ''
  最大值: ''
```

