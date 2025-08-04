# Xcp

## 模块描述

Configuration of the XCP module

## 容器列表

### 1. XcpConfig

该容器没有参数。

### 2. XcpDaqList

**描述**: This container contains the configuration of the DAQs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: XcpDaqListNumber
  长名称: ''
  描述: Index number of the DAQ list
  默认值: ''
  最小值: 0
  最大值: 65534
- 
  序号: 2
  名称: XcpDaqListType
  长名称: ''
  描述: This indicates whether this DAQ list represents a DAQ or a STIM.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: XcpMaxOdt
  长名称: ''
  描述: MAX_ODT indicates the maximum amount of ODTs in this DAQ list
  默认值: ''
  最小值: 0
  最大值: 252
- 
  序号: 4
  名称: XcpMaxOdtEntries
  长名称: ''
  描述: This parameter indicates the maximum amount of entries in an ODT of this DAQ list (STATIC
      configuration).
  默认值: ''
  最小值: 0
  最大值: 255
```

### 3. XcpDto

**描述**: This container collects data transfer object specific parameters for the DAQ list.

#### 参数列表

```yaml
- 
  序号: 1
  名称: XcpDtoPid
  长名称: ''
  描述: Packet identifier (PID) of the DTO that identifies the ODT the content of the DTO.
  默认值: ''
  最小值: 0
  最大值: 251
```

### 4. XcpOdt

**描述**: This container contains ODT-specific parameter for the DAQ list.

#### 参数列表

```yaml
- 
  序号: 1
  名称: XcpOdtEntryMaxSize
  长名称: ''
  描述: This parameter indicates the upper limit for the size of the element described by an ODT
      entry. Depending on the DaqListType this ODT belongs to it describes the limit for a DAQ
      (MAX_ODT_ENTRY_SIZE_DAQ) or a STIM (MAX_ODT_ENTRY_SIZE_STIM).
  默认值: ''
  最小值: 0
  最大值: 254
- 
  序号: 2
  名称: XcpOdtNumber
  长名称: ''
  描述: Index number of this ODT within the DAQ list.
  默认值: ''
  最小值: 0
  最大值: 251
```

### 5. XcpOdtEntry

**描述**: This container collects all configuration parameters that comprise an ODT entry.

#### 参数列表

```yaml
- 
  序号: 1
  名称: XcpOdtEntryAddress
  长名称: ''
  描述: Memory address that the ODT entry is referencing to.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: XcpOdtEntryLength
  长名称: ''
  描述: Length of the referenced memory area that is referenced by the ODT entry.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: XcpOdtEntryNumber
  长名称: ''
  描述: Index number of the ODT entry
  默认值: ''
  最小值: 0
  最大值: 254
```

### 6. XcpDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 7. XcpEventChannel

**描述**: This container contains the configuration of event channels on the XCP slave.

#### 参数列表

```yaml
- 
  序号: 1
  名称: XcpEventChannelConsistency
  长名称: ''
  描述: Type of consistency used by event channel
  默认值: ODT
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: XcpEventChannelMaxDaqList
  长名称: ''
  描述: Maximum amount of DAQ lists that are handled by this event channel.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: XcpEventChannelNumber
  长名称: ''
  描述: Index number of the event channel.
  默认值: ''
  最小值: 0
  最大值: 65534
- 
  序号: 4
  名称: XcpEventChannelPriority
  长名称: ''
  描述: Priority of the event channel
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: XcpEventChannelTimeCycle
  长名称: ''
  描述: The event channel time cycle indicates which sampling period is used to process this event
      channel. A value of 0 means 'Not cyclic'.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: XcpEventChannelTimeUnit
  长名称: ''
  描述: This configuration parameter indicates the unit of the event channel time cycle.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: XcpEventChannelType
  长名称: ''
  描述: This configuration parameter indicates what kind of DAQ list can be allocated to this event
      channel.
  默认值: DAQ
  最小值: ''
  最大值: ''
```

### 8. XcpRxPdu

**描述**: This container specifies received PDUs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: XcpRxPduId
  长名称: ''
  描述: ID of the PDU that will be received via a Xcp_<module>RxIndication.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 9. XcpTxPdu

**描述**: This container specifies transmission PDUs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: XcpTxPduId
  长名称: ''
  描述: The PDU identifier, which has to be used by the lower layer BSW module for TxConfirmations or
      TriggerTransmits.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 10. XcpGeneral

**描述**: This container contains the general configuration parameters of the XCP.

#### 参数列表

```yaml
- 
  序号: 1
  名称: XcpDaqConfigType
  长名称: ''
  描述: Sets the DAQ_CONFIG_TYPE bit within the DAQ_PROPERTIES parameter to "static" or to "dynamic".
      If DAQ_STATIC is selected, the DAQ_CONFIG_TYPE bit is set to "0". If DAQ_DYNAMIC is
      selected, the DAQ_CONFIG_TYPE bit is set to "1".
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: XcpDaqCount
  长名称: ''
  描述: Indicates the number of DAQ lists for dynamic configuration.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: XcpDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification on or off.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: XcpIdentificationFieldType
  长名称: ''
  描述: Type of Identification Field the slave will use when transferring DAQ Packets to the master.
      The master has to use the same Type of Identification Field when transferring STIM
      Packets to the slave.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: XcpMainFunctionPeriod
  长名称: ''
  描述: The XCP does not require this information but the BSW scheduler, which invokes the main
      function, needs it in order to plan its tasks.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 6
  名称: XcpMaxCto
  长名称: ''
  描述: MAX_CTO shows the maximum length of a CTO packet in bytes.
  默认值: ''
  最小值: 8
  最大值: 255
- 
  序号: 7
  名称: XcpMaxDto
  长名称: ''
  描述: MAX_DTO shows the maximum length of a DTO packet in bytes.
  默认值: ''
  最小值: 8
  最大值: 65535
- 
  序号: 8
  名称: XcpMaxEventChannel
  长名称: ''
  描述: ''
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 9
  名称: XcpMinDaq
  长名称: ''
  描述: Indicates the number of predefined, read only DAQ lists on the XCP slave.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: XcpOdtCount
  长名称: ''
  描述: This parameter indicates the amount of ODTs of a DAQ list using dynamic DAQ list
      configuration.
  默认值: ''
  最小值: 0
  最大值: 252
- 
  序号: 11
  名称: XcpOdtEntriesCount
  长名称: ''
  描述: Indicates the amount of entries into an ODT using dynamic DAQ list configuration.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: XcpOdtEntrySizeDaq
  长名称: ''
  描述: Indicates the size of an element described by an ODT entry to the DaqListType for a DAQ.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: XcpOdtEntrySizeStim
  长名称: ''
  描述: Indicates the size of an element described by an ODT entry to the DaqListType for a stim.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: XcpOnCanEnabled
  长名称: ''
  描述: Enabling of XCPonCAN functionality
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: XcpOnCddEnabled
  长名称: ''
  描述: Enabling of XCPonCdd functionality
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: XcpOnEthernetEnabled
  长名称: ''
  描述: Enabling of XCPonEthernet functionality
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: XcpOnFlexRayEnabled
  长名称: ''
  描述: Enabling of XCPonFlexRay functionality
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: XcpPrescalerSupported
  长名称: ''
  描述: This parameter enables and disables the support for Prescaler support. True is Enabled, False
      is disabled
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: XcpSuppressTxSupport
  长名称: ''
  描述: Switches the support of suppressing transmission of PDUs per communication channel on or off.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: XcpTimestampTicks
  长名称: ''
  描述: This parameter defines the timestamp that will increment based TIMESTAMP_TICKS per unit and
      wrap around if an overflow occurs.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 21
  名称: XcpTimestampType
  长名称: ''
  描述: This parameter indicates the number of bytes used for the timestamp field. In case
      No_TIME_STAMP is selected the timestamp field is not available.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: XcpTimestampUnit
  长名称: ''
  描述: This parameter indicates the resolution of the data acquisition clock of the slave when
      transferring data to master.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: XcpVersionInfoApi
  长名称: ''
  描述: Enables/disables the existence of the XCP_GetVersionInfo() API service.
  默认值: ''
  最小值: ''
  最大值: ''
```

