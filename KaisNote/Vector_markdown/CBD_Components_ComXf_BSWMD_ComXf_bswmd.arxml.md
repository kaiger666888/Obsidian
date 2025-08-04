# ComXf

## 模块描述

COM Based Transformer (COMXF) is used by the Runtime Environment (RTE) to serialize and deserialize
structured application data to/from a bytestream that can be handled by the COM module.
#Transformer #RuntimeEnvironment #Communication
#AUTOSAR

## 容器列表

### 1. XfrmGeneral

**描述**: Contains the general configuration parameters of the module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: XfrmDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: XfrmVersionInfoApi
  长名称: ''
  描述: Activate/Deactivate the version information API.
  默认值: false
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

