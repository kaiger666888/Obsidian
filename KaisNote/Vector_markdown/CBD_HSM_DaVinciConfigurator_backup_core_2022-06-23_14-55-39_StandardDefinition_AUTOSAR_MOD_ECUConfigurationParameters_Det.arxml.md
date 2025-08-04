# Det

## 模块描述

Det configuration includes the functions to be called at notification. On one

## 容器列表

### 1. DetConfigSet

**描述**: Configuration set container for Det.

该容器没有参数。

### 2. DetModule

**描述**: This container describes a non BSW module that is using the Det via Service Interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DetModuleId
  长名称: ''
  描述: Unique identifier of the error reporting component. When reporting errors to the DET, a
      symbolic name derived from the moduleID has to be used to identify the reporter.
  默认值: ''
  最小值: 4096
  最大值: 65535
```

### 3. DetModuleInstance

**描述**: Describes the Instance used for the according Service Port.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DetInstanceId
  长名称: ''
  描述: Describes the InstanceId used for the according Service Port.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 4. DetGeneral

**描述**: Generic configuration parameters of the Det module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DetForwardToDlt
  长名称: ''
  描述: Only if the parameter is present and set to true, the Det requires the Dlt interface and
      forwards it's call to the function Dlt_DetForwardErrorTrace. In this case the optional
      interface to Dlt_Det is required.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DetReportRuntimeErrorCallout
  长名称: ''
  描述: This parameter defines the existence and the names of callout functions for the corresponding
      runtime error handler.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DetReportTransientFaultCallout
  长名称: ''
  描述: This parameter defines the existence and the names of callout functions for the corresponding
      transient fault handler.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DetVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information.
  默认值: false
  最小值: ''
  最大值: ''
```

### 5. DetNotification

**描述**: Configuration of the notification functions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DetErrorHook
  长名称: ''
  描述: Optional list of functions to be called by the Default Error Tracer in context of each call of
      Det_ReportError.
  默认值: ''
  最小值: ''
  最大值: ''
```

