# Det

## 模块描述

Default Error Tracer. DET is the central error handler in the AUTOSAR architecture. All other basic
software modules can report development errors, runtime errors and transient faults to the DET.
#AUTOSAR #ServiceComponent

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
  默认值: 4096
  最小值: 4096
  最大值: 65535
```

### 3. DetModuleInstance

**描述**: Describes the Instance used for the according Service Port. It shall be used to differentiate
software component instances when multiple instantiation is used.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DetInstanceId
  长名称: ''
  描述: This parameter describes the InstanceId used for the according Service Port. It shall be used
      to differentiate software component instances when multiple instantiation is used. Else
      it shall be set to 0.
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
  描述: This parameter controls the fowarding of DET errors to the DLT module. If the parameter is
      present and set to true, the DET forwards all errors to the function
      Dlt_DetForwardErrorTrace before other DET functionality is performed.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DetVersionInfoApi
  长名称: ''
  描述: |
    This parameter if set to true enables the function Det_GetVersionInfo() to get major, minor and
    patch version information.
    true: Version info API enabled.
    false: Version info API disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DetEnableDet
  长名称: ''
  描述: This parameter if set to true enables reporting of development error. It can be used to
      disable the DET completely.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DetExtDebugSupport
  长名称: ''
  描述: This parameter if set the true enables the extended debug support feature which provides
      additional functionality to the DET such as filtering, logging and flexible break
      handling. Please refer to the technical reference for details.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DetGlobalFilterSize
  长名称: ''
  描述: |
    This parameter configures the number of global filters which can be used to discard irrelevant
    errors. The filters are typically configured at runtime using a debugger. Please refer to the
    technical reference about details.
    This setting is only relevant if extended debug support (DetExtDebugSupport) is enabled.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: DetBreakFilterSize
  长名称: ''
  描述: |
    This parameter configures the number of break handler filters which can be used to exit the DET
    without entering the endless loop. The filters are typically configured at runtime using a
    debugger. Please refer to the technical reference about details.
    This setting is only relevant if extended debug support (DetExtDebugSupport) is enabled.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: DetLogBufferSize
  长名称: ''
  描述: |
    This parameter configures the size of the log buffer which can be used to log errors reported to
    the DET. The log buffer is typically accessed at runtime using a debugger. Please refer to the
    technical reference about details.
    This setting is only relevant if extended debug support (DetExtDebugSupport) is enabled.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: DetReportErrorRecursionLimit
  长名称: ''
  描述: This parameter configures the number of allowed recursions for calling Det_ReportError. Refer
      to the technical reference for details. To disable recursion detection set this value to
      0.
  默认值: 0
  最小值: 0
  最大值: 254
- 
  序号: 9
  名称: DetReportRuntimeErrorRecursionLimit
  长名称: ''
  描述: This parameter configures the number of allowed recursions for calling Det_ReportRuntimeError.
      Refer to the technical reference for details. To disable recursion detection set this
      value to 0.
  默认值: 0
  最小值: 0
  最大值: 254
- 
  序号: 10
  名称: DetReportTransientFaultRecursionLimit
  长名称: ''
  描述: This parameter configures the number of allowed recursions for calling
      Det_ReportTransientFault. Refer to the technical reference for details. To disable
      recursion detection set this value to 0.
  默认值: 0
  最小值: 0
  最大值: 254
- 
  序号: 11
  名称: DetDltFilterSize
  长名称: ''
  描述: |
    This parameter configures the number of Dlt filters which can be used to suppress reporting of
    irrelevant errors to the Dlt module. The filters are typically configured at runtime using a
    debugger. Please refer to the technical reference about details.
    This setting is only relevant if extended debug support (DetExtDebugSupport) is enabled and if
    Dlt forwarding (DetForwardToDlt) is enabled.
    
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: DetUserConfigFile
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
```

### 5. DetNotification

**描述**: Configuration of the notification functions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DetErrorHook
  长名称: ''
  描述: |
    Optional list of functions to be called by the Default Error Tracer in context of each call of
    Det_ReportError.
    The type of these functions shall be identical the type of Det_ReportError itself:
    Std_ReturnType (*f)(uint16, uint8, uint8, uint8).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DetReportRuntimeErrorCallout
  长名称: ''
  描述: |
    This parameter defines the existence and the names of callout functions for the corresponding
    runtime error handler.
    The type of these functions shall be identical the type of Det_ReportRuntimeError itself:
    Std_ReturnType (*f)(uint16, uint8, uint8, uint8)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DetReportTransientFaultCallout
  长名称: ''
  描述: |
    This parameter defines the existence and the names of callout functions for the corresponding
    transient fault handler.
    The type of these functions shall be identical the type of Det_ReportTransientFault itself:
    Std_ReturnType (*f)(uint16, uint8, uint8, uint8)
  默认值: ''
  最小值: ''
  最大值: ''
```

