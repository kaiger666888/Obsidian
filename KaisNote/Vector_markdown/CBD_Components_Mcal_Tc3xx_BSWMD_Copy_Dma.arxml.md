# Dma

## 模块描述

Configuration of the Dma (Direct Memory Access) module.

## 容器列表

### 1. DmaGeneral

**描述**: General configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: DmaDevErrorDetect
  长名称: ''
  描述: Enables/Disables the Development Error Detection in the DMA Driver
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DmaMultiCoreErrorDetect
  长名称: ''
  描述: If enabled, the multicore error detection will be enabled
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DmaSafetyEnable
  长名称: ''
  描述: Enables/Disables the Safety checks in the DMA Driver
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DmaInitCheckApi
  长名称: ''
  描述: This parameter decides the availability of the API Dma_InitCheck in the code
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DmaDeInitApi
  长名称: ''
  描述: This parameter decides the availability of the API Dma_DeInit in the code
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DmaChDeInitApi
  长名称: ''
  描述: This parameter decides the availability of the API Dma_ChDeinit in the code
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DmaSuspendApi
  长名称: ''
  描述: This parameter decides the availability of the API Dma_TransferFreeze and Dma_TransferResume
      in the code
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DmaTriggerApi
  长名称: ''
  描述: This parameter decides the availability of the API Dma_EnableHardwareTrigger and
      Dma_DisableHardwareTrigger in the code
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DmaDataPendingApi
  长名称: ''
  描述: This parameter decides the availability of the API API Dma_ChGetRemainingData in the code
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DmaBufferSwitchApi
  长名称: ''
  描述: This parameter decides the availability of the API Dma_ChSwitchBuffer in the code
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DmaGetVersionInfoApi
  长名称: ''
  描述: This parameter decides the availability of the API Dma_GetVersionInfo in the code
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: DmaMaxTransactionSetPerChannel
  长名称: ''
  描述: Specifies how many transaction sets are allowed to be defined per channel
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 13
  名称: DmaInitDeInitApiMode
  长名称: ''
  描述: This option specifies the mode in which the DMA init and deinit function operates
  默认值: DMA_MCAL_SUPERVISORMODE
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: DmaRuntimeApiMode
  长名称: ''
  描述: This option specifies the mode in which the DMA runtime functions operate
  默认值: DMA_MCAL_SUPERVISORMODE
  最小值: ''
  最大值: ''
```

### 2. DmaChannelConfig

**描述**: DMA channel configuration for this channel

#### 参数列表

```yaml
- 
  序号: 1
  名称: DmaChannelId
  长名称: ''
  描述: DMA channel number
  默认值: 0
  最小值: 0
  最大值: 127
- 
  序号: 2
  名称: DmaChannelAssignedPartition
  长名称: ''
  描述: Hardware partition to which this channel is allocated to
  默认值: 0
  最小值: 0
  最大值: 3
- 
  序号: 3
  名称: DmaChannelNumTransactionSet
  长名称: ''
  描述: No of transaction set for this channel.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: DmaTcsInterruptTransactionLoss
  长名称: ''
  描述: Enables/Disables the transaction request lost interrupt
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DmaChannelNotification
  长名称: ''
  描述: User defined Notification Function Pointer of type void NotificationRoutine(uint32_t Channel,
      Dma_ChEventType_t Event)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DmaErrorNotification
  长名称: ''
  描述: User defined Notification Function Pointer of type void NotificationRoutine(uint32_t Channel,
      Dma_MoveEngineEventType_t Event)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DmaChannelUser
  长名称: ''
  描述: |
    This parameter defines the user of this DMA channel.
                                                    CRC: Channel used by CRC library
                                                    HSSL: Channel used by HSSL driver
                                                    SPI: Channel used by SPI driver
                                                    Other: Channel used by any other module
  默认值: Other
  最小值: ''
  最大值: ''
```

### 3. DmaChannelTransactionSet

**描述**: Transaction set setting for this DMA channel

#### 参数列表

```yaml
- 
  序号: 1
  名称: DmaTcsIndex
  长名称: ''
  描述: DMA Transaction set Index
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DmaTcsSourceAddress
  长名称: ''
  描述: start address of the source memory
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DmaTcsDestinationAddress
  长名称: ''
  描述: Destination address of the source memory
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DmaTcsDoubleBuffer
  长名称: ''
  描述: start address of the second buffer
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DmaUserHeaderFileWithExternDeclarations
  长名称: ''
  描述: The header file containing the declaration of the variables used for specifying the addresses
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DmaTcsMoveLength
  长名称: ''
  描述: |
    DMA move consisting of one read and one write each) moves data of given number of bits from
    source to destination. This parameter defines number of bits for the DMA move
                                                            DMA_WIDTH_8BITS : 8-bits per move.
                                                            DMA_WIDTH_16BITS : 16-bits per move.
                                                            DMA_WIDTH_32BITS : 32-bits per move.
                                                            DMA_WIDTH_64BITS : 64-bits per move.
                                                            DMA_WIDTH_128BITS: 128-bits per move.
                                                            DMA_WIDTH_256BITS: 256-bits per move.
  默认值: DMA_WIDTH_8BITS
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DmaPatternMode
  长名称: ''
  描述: |
    This parameter defines the mode used during a pattern match. The user should choose the mode as
    needed for the 8bit, 16bit or 32bit pattern match.
                                                            Pattern_Detection_Disabled : Pattern
    match disabled.
                                                            Pattern_Mode_1: Pattern match mode 1
                                                            Pattern_Mode_2: Pattern match mode 2
                                                            Pattern_Mode_3: Pattern match mode 3
                                                            Pattern_Mode_5: Pattern match mode 5
                                                            Pattern_Mode_6: Pattern match mode 6
                                                            Pattern_Mode_7: Pattern match mode 7
  默认值: Pattern_Detection_Disabled
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DmaTcsTransferLength
  长名称: ''
  描述: |
    This parameter defines the number of moves composed for a DMA transfer.
                                                            DMA_MOVES_1: 1 DMA move per transfer.
                                                            DMA_MOVES_2: 2 DMA move per transfer.
                                                            DMA_MOVES_3: 3 DMA move per transfer.
                                                            DMA_MOVES_4: 4 DMA move per transfer.
                                                            DMA_MOVES_5: 5 DMA move per transfer.
                                                            DMA_MOVES_8: 8 DMA move per transfer.
                                                            DMA_MOVES_9: 9 DMA move per transfer.
                                                            DMA_MOVES_16:16 DMA move per transfer.
  默认值: DMA_MOVES_1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DmaTcsTransactionLength
  长名称: ''
  描述: This parameter defines how many transfers are performed per DMA transaction
  默认值: 0
  最小值: 0
  最大值: 16383
- 
  序号: 10
  名称: DmaTcsCircularBufferSourceEnable
  长名称: ''
  描述: This parameter used to enable/disable the source circular buffer
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DmaTcsCircularBufferDestinationEnable
  长名称: ''
  描述: This parameter used to enable/disable the destination circular buffer
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: DmaTcsCircularBufferSourceLength
  长名称: ''
  描述: |
    This parameter determines how many bits of the source address of a circular buffer.
                                                            DMA_CIRCULAR_BUFFER_LENGTH_1BYTE: Source
    address SADR[31:0] is not updated.
                                                            DMA_CIRCULAR_BUFFER_LENGTH_2BYTE: Source
    address SADR[31:1] is not updated.
                                                            DMA_CIRCULAR_BUFFER_LENGTH_4BYTE: Source
    address SADR[31:2] is not updated
                                                            .....
                                                            DMA_CIRCULAR_BUFFER_LENGTH_16384BYTE:
    Source address SADR[31:14] is not updated
                                                            DMA_CIRCULAR_BUFFER_LENGTH_32768BYTE:
    Source address SADR[31:15] is not updated
  默认值: DMA_CIRCULAR_BUFFER_LENGTH_1BYTE
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: DmaTcsCircularBufferDestinationLength
  长名称: ''
  描述: |
    This parameter determines how many bits of the source address of a circular buffer.
                                                            DMA_CIRCULAR_BUFFER_LENGTH_1BYTE: Source
    address SADR[31:0] is not updated.
                                                            DMA_CIRCULAR_BUFFER_LENGTH_2BYTE: Source
    address SADR[31:1] is not updated.
                                                            DMA_CIRCULAR_BUFFER_LENGTH_4BYTE: Source
    address SADR[31:2] is not updated
                                                            .....
                                                            DMA_CIRCULAR_BUFFER_LENGTH_16384BYTE:
    Source address SADR[31:14] is not updated
                                                            DMA_CIRCULAR_BUFFER_LENGTH_32768BYTE:
    Source address SADR[31:15] is not updated
  默认值: DMA_CIRCULAR_BUFFER_LENGTH_1BYTE
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: DmaTcsSourceAddressModificationFactor
  长名称: ''
  描述: |
    This parameter defines how the source address changes after every move operation.
                                                            DMA_FACTOR_1 : Address offset is 1 x
    DmaMoveLength.
                                                            DMA_FACTOR_2 : Address offset is 2 x
    DmaMoveLength.
                                                            DMA_FACTOR_4 : Address offset is 4 x
    DmaMoveLength.
                                                            DMA_FACTOR_8 : Address offset is 8 x
    DmaMoveLength.
                                                            DMA_FACTOR_16 : Address offset is 16 x
    DmaMoveLength.
                                                            DMA_FACTOR_32 : Address offset is 32 x
    DmaMoveLength.
                                                            DMA_FACTOR_64 : Address offset is 64 x
    DmaMoveLength.
                                                            DMA_FACTOR_128 : Address offset is 128 x
    DmaMoveLength.
  默认值: DMA_FACTOR_1
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: DmaTcsDestinationAddressModificationFactor
  长名称: ''
  描述: |
    This parameter defines how the source address changes after every move operation.
                                                            DMA_FACTOR_1 : Address offset is 1 x
    DmaMoveLength.
                                                            DMA_FACTOR_2 : Address offset is 2 x
    DmaMoveLength.
                                                            DMA_FACTOR_4 : Address offset is 4 x
    DmaMoveLength.
                                                            DMA_FACTOR_8 : Address offset is 8 x
    DmaMoveLength.
                                                            DMA_FACTOR_16 : Address offset is 16 x
    DmaMoveLength.
                                                            DMA_FACTOR_32 : Address offset is 32 x
    DmaMoveLength.
                                                            DMA_FACTOR_64 : Address offset is 64 x
    DmaMoveLength.
                                                            DMA_FACTOR_128 : Address offset is 128 x
    DmaMoveLength.
  默认值: DMA_FACTOR_1
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: DmaTcsAppendTimeStamp
  长名称: ''
  描述: This parameter determines if time stamp is to be appended after the last DMA move of a
      transaction
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: DmaTcsSourceAddressMovement
  长名称: ''
  描述: This parameter determines if the source address after every move operation is to be increased
      or decreased
  默认值: DMA_INCREASING
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: DmaTcsDestinationAddressMovement
  长名称: ''
  描述: This parameter determines if the Destinaion address after every move operation is to be
      increased or decreased
  默认值: DMA_INCREASING
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: DmaTcsShadowRegisterConfiguration
  长名称: ''
  描述: This parameter determines how the shadow register is to be used
  默认值: DMA_SHADOWING_DISABLED
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: DmaCLLNextIndex
  长名称: ''
  描述: This parameter defines the next TCS node in case of conditional linked list match feature
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 21
  名称: DmaNextTcsIndex
  长名称: ''
  描述: This parameter determines the next node of the TCS linked list
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 22
  名称: DmaTcsTriggerFrequency
  长名称: ''
  描述: This parameter determines how much of data will the move engine move upon a trigger request
      [Either hardware or software].
  默认值: DMA_TRANSFER_PER_TRIGGER
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: DmaTcsHardwareTrigger
  长名称: ''
  描述: This parameter defines the triggering mode for the hardware trigger.
  默认值: DMA_NO_HARDWARE_TRIGGER
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: DmaTcsDaisyChaining
  长名称: ''
  描述: This parameter determines whether the adjacent lower channel is daisy chained with this
      channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: DmaTcsInterruptSourceAddressWrap
  长名称: ''
  描述: Enables/Disables the wrap source interrupt
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: DmaTcsInterruptDestinationAddressWrap
  长名称: ''
  描述: Enables/Disables the wrap destination interrupt
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: DmaTcsDataTransferInterrupt
  长名称: ''
  描述: Enables/Disables the data transfer or transaction interrupt
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: DmaTcsInterruptDataTransfer
  长名称: ''
  描述: Interrupts can be generated either for every transfer or even transaction.
  默认值: DMA_INTERRUPT_PER_TRANSACTION
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: DmaTcsInterruptDataTransferThreshold
  长名称: ''
  描述: An interrupt can be generated after a certain number of transfers equaling a threshold have
      been completed.
  默认值: 0
  最小值: 0
  最大值: 15
- 
  序号: 30
  名称: DmaTcsSwapDataCRCByteOrder
  长名称: ''
  描述: Swaps the Data CRC byte order
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: DmaTcsAutoStartEnable
  长名称: ''
  描述: Enables the autostart feature for linked lists
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 32
  名称: DmaTcsReferenceAddressCrc
  长名称: ''
  描述: Reference CRC value for address CRC
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 33
  名称: DmaTcsReferenceDataCrc
  长名称: ''
  描述: Reference CRC value for data CRC
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 4. DmaMoveEngineConfig

**描述**: DMA move engine configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: DmaMESourceErrorInterrupt
  长名称: ''
  描述: Enables/Disables the Source error interrupt of a move engine
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DmaMEDestinationErrorInterrupt
  长名称: ''
  描述: Enables/Disables the Destination error interrupt of a move engine
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DmaMELinkedListErrorInterrupt
  长名称: ''
  描述: Enables/Disables the Linked List error interrupt of a move engine
  默认值: false
  最小值: ''
  最大值: ''
```

### 5. CommonPublishedInformation

**描述**: Common container, aggregated by all modules. It contains published information about vendor and
versions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: VendorId
  长名称: ''
  描述: DMA Vendor ID
  默认值: 17
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: ModuleId
  长名称: ''
  描述: DMA Module ID
  默认值: 255
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: ArMajorVersion
  长名称: ''
  描述: DMA Autosar major version
  默认值: 4
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: ArMinorVersion
  长名称: ''
  描述: DMA Autosar mivor version
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: ArPatchVersion
  长名称: ''
  描述: DMA Autosar major version
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: SwMajorVersion
  长名称: ''
  描述: Major version number of the vendor specific implementation of the module. The numbering is
      vendor specific
  默认值: 20
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: SwMinorVersion
  长名称: ''
  描述: Minor version number of the vendor specific implementation of the module. The numbering is
      vendor specific
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: SwPatchVersion
  长名称: ''
  描述: Patch level version number of the vendor specific implementation of the module. The numbering
      is vendor specific
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: Release
  长名称: ''
  描述: AURIX2G derivative used for the implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. DmaPatternConfig

**描述**: DMA pattern matching configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: DmaPattern0
  长名称: ''
  描述: This parameter is to set the pattern in the PRR0 register.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: DmaPattern1
  长名称: ''
  描述: This parameter is to set the pattern in the PRR1 register.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 7. DmaResourcePartition

**描述**: Dma hardware access protection configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DmaResourcePartitionBusMode
  长名称: ''
  描述: This parameter controls whether hardware resources access the on chip buses in supervisor mode
      or user mode.
  默认值: DMA_RP_SUPERVISOR_MODE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DmaPermittedBusMaster
  长名称: ''
  描述: permitted bus masters to access this hardware resource. each 32 bit belongs to one master
  默认值: 4294967295
  最小值: 0
  最大值: 4294967295
```

