# LinSM

## 模块描述

Configuration of the Lin State Manager module.

## 容器列表

### 1. LinSMConfigSet

**描述**: This container describes one of multiple configuration sets of LinSm.

该容器没有参数。

### 2. LinSMChannel

**描述**: Describes each LIN channel the LinSM is connected to.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinSMConfirmationTimeout
  长名称: ''
  描述: Timeout in seconds for the goto sleep and wakeup calls to LinIf. The timeout must be longer
      than a goto-sleep command on the bus (i.e. it is bit rate dependent).
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: LinSMSleepSupport
  长名称: ''
  描述: Some LIN clusters does not need sleep, they will just shut off. This parameter will affect the
      behavior to achieve the no communication state.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: LinSMTransceiverPassiveMode
  长名称: ''
  描述: Selects STANDBY (true) or SLEEP (false) transceiver mode when entering LINSM_NO_COM.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. LinSMSchedule

**描述**: The schedule references to a schedule that is located in the LinIf configuration. Moreover, the PDU
groups are located in the COM configuration. Note that there are two references to PDU groups. The
simple reason is that a PDU group is only allowed to contain one direction (TX or RX).

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinSMScheduleIndex
  长名称: ''
  描述: This index parameter can be used by the BswM as a  SymbolicNameReference target. The LinSM
      just forwards the request from the BswM to LinIf. Note that the value of the
      LinSMScheduleIndex shall be the same as the value from the LinIf.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 4. LinSMGeneral

**描述**: This container contains general parameters of LIN State Manager module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinSMDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: LinSMMainProcessingPeriod
  长名称: ''
  描述: Fixed period that the MainFunction shall be called.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: LinSMVersionInfoApi
  长名称: ''
  描述: Switches the LinSM_GetVersionInfo function ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
```

