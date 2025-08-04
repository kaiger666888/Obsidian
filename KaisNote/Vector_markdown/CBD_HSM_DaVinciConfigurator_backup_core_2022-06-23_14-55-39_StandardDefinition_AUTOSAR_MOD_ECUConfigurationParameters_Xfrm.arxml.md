# Xfrm

## 容器列表

### 1. XfrmGeneral

**描述**: Contains the general configuration parameters of the module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: XfrmDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. XfrmImplementationMapping

**描述**: For each transformer (TransformationTechnology) in a transformer chain (DataTransformation) which is
applied to an ISignal it is necessary to specify the BswModuleEntry which implements it. This is the
container to hold these mappings.

该容器没有参数。

### 3. XfrmDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 4. XfrmSignal

**描述**: Reference to the signal in the system description that transports the transformed data.

该容器没有参数。

### 5. XfrmISignalGroupRefChoice

**描述**: Reference to the ISignalGroup in the system description that transports the transformed data.

该容器没有参数。

### 6. XfrmISignalRefChoice

**描述**: Reference to the ISignal in the system description that transports the transformed data.

该容器没有参数。

