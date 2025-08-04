# IoHwAb

## 模块描述

Configuration of the I/O Hardware Abstraction module

## 容器列表

### 1. IoHwAbGeneral

**描述**: This container contains common configuration options for the I/O Hardware Abstraction module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbDevErrorDetect
  长名称: Development Mode
  描述: This parameter enables/disables development error detection and reporting.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IoHwAbVersionInfoApi
  长名称: Enable IoHwAb_GetVersionInfo
  描述: |
    Pre-processor switch to enable/disable the API to read out the modules version information.
    
    Note: The function will be removed from the code completely.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IoHwAbUseInitFunction
  长名称: Enable IoHwAb_Init
  描述: |
    Pre-processor switch to enable/disable the Initialization-API.
    
    Note: The function will be removed from the code completely.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IoHwAbCfgIncludeList
  长名称: ''
  描述: Include List for used basic software component headers.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. IoHwAbDatatypes

**描述**: Container for the data types configuration. There is a set of base types that cannot be changed, but
can be used to create implementation specific types (Type references, Arrays or Structs/Records).

该容器没有参数。

### 3. IoHwAbImplementationTypes

**描述**: Container for the implementation specific datatypes. Implementation specific datatypes can be
configured/assembled by using base datatypes.

该容器没有参数。

### 4. IoHwAbTypeReference

**描述**: Container for configuring a type reference. A type reference is a deviation from a base type, i.e.
the generated files (e.g. Rte_Type.h) will contain a typedef like the following example:

typedef sint8 BatteryVoltageValue;

该容器没有参数。

### 5. IoHwAbInvalidValue

**描述**: Optional container for configuring an invalid value for a IoHwAb type reference.

该容器没有参数。

### 6. IoHwAbInvalidValueBoolean

**描述**: Container for configuring an invalid value of a type "boolean".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInvalidValue
  长名称: ''
  描述: This field contains the initial value of a type "boolean".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. IoHwAbInvalidValueFloat32

**描述**: Container for configuring an invalid value of a type "float32".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInvalidValue
  长名称: ''
  描述: This field contains the initial value of a type "float32".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. IoHwAbInvalidValueFloat64

**描述**: Container for configuring an invalid value of a type "float64".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInvalidValue
  长名称: ''
  描述: This field contains the initial value of a type "float64".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. IoHwAbInvalidValueUint8

**描述**: Container for configuring an invalid value of a type "uint8".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInvalidValue
  长名称: ''
  描述: This field contains the initial value of a type "uint8".
  默认值: ''
  最小值: 0
  最大值: 255
```

### 10. IoHwAbInvalidValueUint16

**描述**: Container for configuring an invalid value of a type "uint16".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInvalidValue
  长名称: ''
  描述: This field contains the initial value of a type "uint16".
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 11. IoHwAbInvalidValueUint32

**描述**: Container for configuring an invalid value of a type "uint32".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInvalidValue
  长名称: ''
  描述: This field contains the initial value of a type "uint32".
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 12. IoHwAbInvalidValueSint8

**描述**: Container for configuring an invalid value of a type "sint8".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInvalidValue
  长名称: ''
  描述: This field contains the initial value of a type "sint8".
  默认值: ''
  最小值: -128
  最大值: 127
```

### 13. IoHwAbInvalidValueSint16

**描述**: Container for configuring an invalid value of a type "sint16".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInvalidValue
  长名称: ''
  描述: This field contains the initial value of a type "sint16".
  默认值: ''
  最小值: -32768
  最大值: 32767
```

### 14. IoHwAbInvalidValueSint32

**描述**: Container for configuring an invalid value of a type "sint32".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInvalidValue
  长名称: ''
  描述: This field contains the initial value of a type "sint32".
  默认值: ''
  最小值: -2147483648
  最大值: 2147483647
```

### 15. IoHwAbArray

**描述**: Container for configuring an array type. An array type is the typedef of an array containing n data
elements of a base type or a type reference, i.e. the generated files (e.g. Rte_Type.h) will contain
a typedef like the following example:

typedef uint8 AlternatorPower_au8[13];

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbArraySize
  长名称: Number of Array elements
  描述: Parameter for the configuration of the array size, i.e. the number of elements of the selected
      datatype.
  默认值: 5
  最小值: 0
  最大值: 18446744073709551615
```

### 16. IoHwAbRecord

**描述**: Container for configuring a record/struct type. An record type is the typedef of a struct containing
data elements of a base type or a type reference, i.e. the generated files (e.g. Rte_Type.h) will
contain a typedef like the following example:

typedef struct
{
    uint16 Period;
    uint16 ActiveTime;
}DutyCycle;

该容器没有参数。

### 17. IoHwAbRecordElement

**描述**: Container for configuring a record/struct element.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbRecordElementPosition
  长名称: Position
  描述: This parameter contains the position of the of the record element inside the record.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 18. IoHwAbBaseType

**描述**: Container for the base data types. These types are a representation of the standard types and cannot
be changed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbBaseDataType
  长名称: Base Type
  描述: Label for the referenced base type. This type should be used within the user blocks instead of
      the base type itself.
  默认值: IOHWAB_UINT8
  最小值: ''
  最大值: ''
```

### 19. IoHwAbRunnable

**描述**: Container for configuring a Runnable Entity that will be generated as
- Runnable into the SWC Description File of the I/O Hardware Abstraction
- Function-body in the C-Source that can be filled with user code
A Runnable Entity is called cyclically by the RTE.

Note: More information on Runnables can be found in the 'Virtual Functional Bus' document.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbTriggerPeriod
  长名称: Trigger Period
  描述: This field contains the trigger time of the Runnable Entity.
  默认值: 10
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: IoHwAbTimebase
  长名称: Timebase
  描述: This field contains the timebase of the trigger's time.
  默认值: IoHwAbMSec
  最小值: ''
  最大值: ''
```

### 20. IoHwAbSRPortPrototype

**描述**: Container for configuring a Sender/Receiver Port Prototype. This container is the instantiation of a
Sender/Receiver Port Interface.

Note: More information on Sender/Receiver Port Interfaces can be found in the 'Virtual Functional
Bus' document.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbSRDirection
  长名称: Direction
  描述: This parameter configures whether the BSW is the sender (PPort -  provides values of
      data-elements) or the receiver (RPort - reads/consumes values of data-elements ) of the
      configured signal.
  默认值: IOHWAB_RECEIVER
  最小值: ''
  最大值: ''
```

### 21. IoHwAbInitValue

**描述**: Container for configuring initial values of the data elements of the corresponding SR PortInterface.

Note: Only the initial values of BaseTypes and TypeReferences can be configured.

该容器没有参数。

### 22. IoHwAbInitValueFloat32

**描述**: Container for configuring an initial value of a type "float32".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInitValue
  长名称: ''
  描述: This field contains the initial value of a type "float32".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 23. IoHwAbInitValueBoolean

**描述**: Container for configuring an initial value of a type "boolean".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInitValue
  长名称: ''
  描述: This field contains the initial value of a type "boolean".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 24. IoHwAbInitValueUint16

**描述**: Container for configuring an initial value of a type "uint16".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInitValue
  长名称: ''
  描述: This field contains the initial value of a type "uint16".
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 25. IoHwAbInitValueFloat64

**描述**: Container for configuring an initial value of a type "float64".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInitValue
  长名称: ''
  描述: This field contains the initial value of a type "float64".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 26. IoHwAbInitValueUint8

**描述**: Container for configuring an initial value of a type "uint8".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInitValue
  长名称: ''
  描述: This field contains the initial value of a type "uint8".
  默认值: ''
  最小值: 0
  最大值: 255
```

### 27. IoHwAbInitValueUint32

**描述**: Container for configuring an initial value of a type "uint32".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInitValue
  长名称: ''
  描述: This field contains the initial value of a type "uint32".
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 28. IoHwAbInitValueSint8

**描述**: Container for configuring an initial value of a type "sint8".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInitValue
  长名称: ''
  描述: This field contains the initial value of a type "sint8".
  默认值: ''
  最小值: -128
  最大值: 127
```

### 29. IoHwAbInitValueSint16

**描述**: Container for configuring an initial value of a type "sint16".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInitValue
  长名称: ''
  描述: This field contains the initial value of a type "sint16".
  默认值: ''
  最小值: -32768
  最大值: 32767
```

### 30. IoHwAbInitValueSint32

**描述**: Container for configuring an initial value of a type "sint32".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInitValue
  长名称: ''
  描述: This field contains the initial value of a type "sint32".
  默认值: ''
  最小值: -2147483648
  最大值: 2147483647
```

### 31. IoHwAbInitValueArrayOrRecord

**描述**: Container for configuring an initial value of an array or a record.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInitValue
  长名称: ''
  描述: |
    This field contains the initial value of an array or a record.
    
    All values ​​should, as usual with the array / struct notation, stand one after the other,
    separated by a comma within a curly bracket,
    
    Example - array with size 3 and init values 0, 1 and 2: {0,1,2}
  默认值: ''
  最小值: ''
  最大值: ''
```

### 32. IoHwAbCSPortPrototype

**描述**: Container for configuring a Client/Server Port Prototype. This container is the instantiation of a
Client/Server Port Interface.

Note: More information on Client/Server Port Interfaces can be found in the 'Virtual Functional Bus'
document.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbCSDirection
  长名称: Direction
  描述: |
    This parameter configures whether the BSW is the Client (RPort -  requires (=uses or invokes)
    the operations defined in the interface from an AUTOSAR service) or the Server (PPort -
    provides (=implements) the operations defined in the interface to an AUTOSAR service) of the
    configured signal.
    
    Note: Currently, the I/O Hardware Abstraction only supports Server Ports.
  默认值: IOHWAB_CLIENT
  最小值: ''
  最大值: ''
```

### 33. IoHwAbSRPortInterface

**描述**: Container for configuring a Sender/Receiver Port Interface. This container holds the configuration
elements for configuring a Sender/Receiver 'template'-interface. This interface is being
instantiated by a Sender/Receiver Port Prototype.

Note: More information on Sender/Receiver Port Interfaces can be found in the 'Virtual Functional
Bus' document.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbTemplate
  长名称: Used Template
  描述: This parameter documents which 'template' has been used for creating this port interface.
  默认值: IoHwAb_Template_None
  最小值: ''
  最大值: ''
```

### 34. IoHwAbDataElement

**描述**: This container configures a data element of the Sender/Receiver Interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbInvalidationPolicy
  长名称: ''
  描述: This parameter configures whether the sending component can actively invalidate a particular
      data element or which strategy of handling invalid values is applied on the receiver
      side.
  默认值: DontInvalidate
  最小值: ''
  最大值: ''
```

### 35. IoHwAbCSPortInterface

**描述**: Container for configuring a Client/Server Port Interface. This container holds the configuration
elements for configuring a Client/Server 'template'-interface. This interface is being instantiated
by a Client/Server Port Prototype.

Note: More information on Client/Server Port Interfaces can be found in the 'Virtual Functional Bus'
document.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbTemplate
  长名称: ''
  描述: |
    Parameter not used.
    
    This parameter documents which 'template' has been used for creating this port interface.
  默认值: IoHwAb_Template_None
  最小值: ''
  最大值: ''
```

### 36. IoHwAbOperation

**描述**: Container for configuring a Client/Server Port Operation.

该容器没有参数。

### 37. IoHwAbOperationArgument

**描述**: This container contains the configuration of am Operation Element of a Client/Server Operation. This
Operation Element will be generated as function parameter in the I/O Hardware Abstraction
implementation.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbArgDirection
  长名称: Parameter Direction
  描述: |
    Direction of the function parameter:
    - In: parameter is given by value
    - Out/InOut: parameter given 'by reference' (actually, it is given as a pointer to a variable)
  默认值: IOHWAB_IN
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IoHwAbOperationArgumentPosition
  长名称: Position
  描述: This parameter contains the position of the of the operation argument.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 38. IoHwAbApplicationError

**描述**: This container configures the name an application error, which may be result of a server call via
the port interface. The configured application errors are available to all operations declared in
this interface.


#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbErrorCode
  长名称: Error Code
  描述: This parameter configures the numeric value of an application error.
  默认值: 1
  最小值: 1
  最大值: 63
```

### 39. IoHwAbSchedulable

**描述**: Container for configuring a BSW Schedulable Entity that will be generated as
- Schedulable Entity into the Internal Behavior File of the I/O Hardware Abstraction
- Function-body in the C-Source that can be filled with user code
A Runnable Entity is called cyclically by the SchM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IoHwAbBswTriggerPeriod
  长名称: Trigger Period
  描述: This contains the trigger time of the Schedulable Entity.
  默认值: 10
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: IoHwAbBswTimebase
  长名称: Timebase
  描述: This field contains the timebase of the trigger's time.
  默认值: IoHwAbMSec
  最小值: ''
  最大值: ''
```

