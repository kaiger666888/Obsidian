# J1939Nm

## 模块描述

The SAE J1939 Nm module

## 容器列表

### 1. J1939NmConfigSet

**描述**: This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist
once per configuration set.

该容器没有参数。

### 2. J1939NmChannel

**描述**: Physical CAN channel handled by J1939Nm.

该容器没有参数。

### 3. J1939NmRxPdu

**描述**: Contains the configuration of the I-PDU used to receive the AddressClaimed PG.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939NmRxPduId
  长名称: ''
  描述: The I-PDU identifier used for RxIndication from CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 4. J1939NmTxPdu

**描述**: Contains the configuration of the I-PDU used to transmit the AddressClaimed PG.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939NmTxPduId
  长名称: ''
  描述: The I-PDU identifier used for TxConfirmation from CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 5. J1939NmNode

**描述**: Logical node representing one function handled by J1939Nm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939NmNodeId
  长名称: ''
  描述: Unique identifier of this node. May be chosen to be identical with
      J1939NmNodePreferredAddress, if the same address shall not be used by different nodes on
      different channels.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: J1939NmNodeNameArbitraryAddressCapable
  长名称: ''
  描述: Arbitrary Address Capable field of the NAME of this node.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: J1939NmNodeNameECUInstance
  长名称: ''
  描述: ECU Instance field of the NAME of this node.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 4
  名称: J1939NmNodeNameFunction
  长名称: ''
  描述: Function field of the NAME of this node.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: J1939NmNodeNameFunctionInstance
  长名称: ''
  描述: Function Instance field of the NAME of this node.
  默认值: ''
  最小值: 0
  最大值: 31
- 
  序号: 6
  名称: J1939NmNodeNameIdentityNumber
  长名称: ''
  描述: Identity Number field of the NAME of this node.
  默认值: ''
  最小值: 0
  最大值: 2097151
- 
  序号: 7
  名称: J1939NmNodeNameIndustryGroup
  长名称: ''
  描述: Industry Group field of the NAME of this node.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 8
  名称: J1939NmNodeNameManufacturerCode
  长名称: ''
  描述: Manufacturer Code field of the NAME of this node.
  默认值: ''
  最小值: 0
  最大值: 2047
- 
  序号: 9
  名称: J1939NmNodeNameVehicleSystem
  长名称: ''
  描述: Vehicle System field of the NAME of this node.
  默认值: ''
  最小值: 0
  最大值: 127
- 
  序号: 10
  名称: J1939NmNodeNameVehicleSystemInstance
  长名称: ''
  描述: Vehicle System Instance field of the NAME of this node.
  默认值: ''
  最小值: 0
  最大值: 15
- 
  序号: 11
  名称: J1939NmNodePreferredAddress
  长名称: ''
  描述: Source address of this node used for address claiming.
  默认值: ''
  最小值: 0
  最大值: 253
- 
  序号: 12
  名称: J1939NmNodeStartUpDelay
  长名称: ''
  描述: If enabled, the communication will start after a delay of 250ms after transmission of the
      initial AddressClaimed. If disabled, communication will start immediately at start-up.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. J1939NmDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 7. J1939NmGeneral

**描述**: Contains the general configuration parameters of the module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939NmDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling development error detection support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: J1939NmMainFunctionPeriod
  长名称: ''
  描述: Call cycle in seconds of J1939Nm_MainFunction.
  默认值: ''
  最小值: 0.001
  最大值: 0.255
- 
  序号: 3
  名称: J1939NmTxConfirmationTimeout
  长名称: ''
  描述: Time in seconds to wait for a confirmation after transmission of a message. The behaviour when
      the time elapses depends on the transmitted message.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 4
  名称: J1939NmUserCallout
  长名称: ''
  描述: Pre-processor switch for enabling the <User_AddressClaimedIndication> and defining the name of
      the callout function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: J1939NmUserCalloutHeaderFile
  长名称: ''
  描述: Header file which is included by J1939Nm when J1939NmUserCallout is enabled. This header file
      must provide the prototype of the <User_AddressClaimedIndication> defined in
      J1939NmUserCallout.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: J1939NmVersionInfoApi
  长名称: ''
  描述: Pre-processor switch for enabling version info API support.
  默认值: ''
  最小值: ''
  最大值: ''
```

