# Dma - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:11

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Dma](#dma)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Dma

#### 基本信息

- **UUID**: `ECUC:c03229fe-3dca-435e-a47c-1ae11e6c1832`
- **模块名称**: `Dma`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the Dma (Direct Memory Access) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2017-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. DmaGeneral

**容器属性**:

- **UUID**: `ECUC:c03229fe-4dca-416e-a47c-1ae11e6c1842`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DmaGeneral`
- **多重性**: [0..1]

**容器描述**:

General configuration

###### 参数配置

此容器包含 **13** 个参数：

####### INTEGER 类型参数

######## 1. DmaMaxTransactionSetPerChannel

- **UUID**: `ECUC:c03229fe-1dca-417e-a47c-1aa11e6c2212`
- **参数名**: `DmaMaxTransactionSetPerChannel`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: INFINEON_AURIX2G
- **描述**: Specifies how many transaction sets are allowed to be defined per channel

####### BOOLEAN 类型参数

######## 1. DmaDevErrorDetect

- **UUID**: `DCE:a4e850e4-be6b-4d72-b360-c13bb0bff7f6`
- **参数名**: `DmaDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the Development Error Detection in the DMA Driver

######## 2. DmaMultiCoreErrorDetect

- **UUID**: `ECUC:348d2d10-2ba2-4a1e-aaa8-002da540f627`
- **参数名**: `DmaMultiCoreErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: INFINEON_AURIX2G
- **描述**: If enabled, the multicore error detection will be enabled

######## 3. DmaSafetyEnable

- **UUID**: `DCE:a4e850e4-be6b-4d72-b360-c23bb0bff7f6`
- **参数名**: `DmaSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the Safety checks in the DMA Driver

######## 4. DmaInitCheckApi

- **UUID**: `DCE:a4e850e4-be6b-4d72-b360-c24bb0bff7f6`
- **参数名**: `DmaInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter decides the availability of the API Dma_InitCheck in the code

######## 5. DmaDeinitApiConfiguration

- **UUID**: `ECUC:c03229fe-5dca-416e-a47c-1ae11e6c1852`
- **参数名**: `DmaDeinitApiConfiguration`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter decides the availability of the API Dma_ChDeinit in the code

######## 6. DmaSuspendApiConfiguration

- **UUID**: `ECUC:c03229fe-6dca-416e-a47c-1aa11e6c1862`
- **参数名**: `DmaSuspendApiConfiguration`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter decides the availability of the API Dma_TransferFreeze and Dma_TransferResume in the code

######## 7. DmaTriggerApiConfiguration

- **UUID**: `ECUC:c03229fe-7dca-416e-a47c-1aa11e6c1972`
- **参数名**: `DmaTriggerApiConfiguration`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter decides the availability of the API Dma_EnableHardwareTrigger and Dma_DisableHardwareTrigger in the code

######## 8. DmaDataPendingApiConfiguration

- **UUID**: `ECUC:c03229fe-8dca-416e-a47c-1aa11e6c2082`
- **参数名**: `DmaDataPendingApiConfiguration`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter decides the availability of the API API Dma_ChGetRemainingData in the code

######## 9. DmaBufferSwitchApiConfiguration

- **UUID**: `ECUC:c03229fe-9dca-416e-a47c-1aa11e6c2192`
- **参数名**: `DmaBufferSwitchApiConfiguration`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter decides the availability of the API Dma_ChSwitchBuffer in the code

######## 10. DmaVersionInfoApi

- **UUID**: `ECUC:c03229fe-9dca-416e-a48c-1aa11e6c2192`
- **参数名**: `DmaVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter decides the availability of the API Dma_GetVersionInfo in the code

####### ENUMERATION 类型参数

######## 1. DmaInitApiMode

- **UUID**: `ECUC:c03229fe-6dca-425e-a47c-1ae21a6c2362`
- **参数名**: `DmaInitApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_MCAL_SUPERVISORMODE`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_MCAL_USER1MODE` (来源: INFINEON_AURIX2G)
  - `DMA_MCAL_SUPERVISORMODE` (来源: INFINEON_AURIX2G)
- **描述**: This option specifies the mode in which the DMA init function operates

######## 2. DmaRuntimeApiMode

- **UUID**: `ECUC:c03229fe-6dca-425e-a47c-1ae31a6c2362`
- **参数名**: `DmaRuntimeApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_MCAL_SUPERVISORMODE`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_MCAL_USER1MODE` (来源: INFINEON_AURIX2G)
  - `DMA_MCAL_SUPERVISORMODE` (来源: INFINEON_AURIX2G)
- **描述**: This option specifies the mode in which the DMA runtime functions operate

##### 2. DmaChannelConfig

**容器属性**:

- **UUID**: `ECUC:c03229fe-2dca-418e-a47c-1ab11e6c1922`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DmaChannelConfig`
- **多重性**: [1..128]

**容器描述**:

DMA channel configuration for this channel

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. DmaChannelId

- **UUID**: `ECUC:c03229fe-3aca-418e-a47c-1ab11e6c2032`
- **参数名**: `DmaChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..127]
- **来源**: INFINEON_AURIX2G
- **描述**: DMA channel number

######## 2. DmaChannelAssignedPartition

- **UUID**: `ECUC:c03229fe-3dca-418e-a47c-1ab11e6c2032`
- **参数名**: `DmaChannelAssignedPartition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **描述**: Hardware partition to which this channel is allocated to

######## 3. DmaChannelNumTransactionSet

- **UUID**: `ECUC:c03229fe-4dca-418e-a47c-1ab11e6c2142`
- **参数名**: `DmaChannelNumTransactionSet`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: INFINEON_AURIX2G
- **描述**: No of transaction set for this channel.

####### BOOLEAN 类型参数

######## 1. DmaTcsInterruptTransactionLoss

- **UUID**: `ECUC:c03229fe-5dca-426e-a47c-1ae11a6c3152`
- **参数名**: `DmaTcsInterruptTransactionLoss`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the transaction request lost interrupt

####### FUNCTION-NAME 类型参数

######## 1. DmaChannelNotification

- **UUID**: `ECUC:c03229fe-5dca-418e-a47c-1ab11e6c2252`
- **参数名**: `DmaChannelNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: User defined Notification Function Pointer of type void NotificationRoutine(uint32_t Channel, Dma_ChEventType_t Event)

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DmaChannelTransactionSet

**容器属性**:

- **UUID**: `ECUC:c03229fe-8dca-418e-a47c-1ab11e6c2582`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DmaChannelTransactionSet`
- **多重性**: [1..65535]

**容器描述**:

Transaction set setting for this DMA channel

######## 参数配置

此容器包含 **31** 个参数：

######### INTEGER 类型参数

########## 1. DmaTcsIndex

- **UUID**: `ECUC:c03229fe-9d4a-418e-a57c-1ab11e6c2692`
- **参数名**: `DmaTcsIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **描述**: DMA Transaction set Index

########## 2. DmaTcsTransactionLength

- **UUID**: `ECUC:c03229fe-5dca-419e-a47c-1ab11e6c3152`
- **参数名**: `DmaTcsTransactionLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16383]
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter defines how many transfers are performed per DMA transaction

########## 3. DmaNextTcsIndex

- **UUID**: `ECUC:c03229fe-6dca-425e-a47c-16e11a6c2362`
- **参数名**: `DmaNextTcsIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter determines the next node of the TCS linked list

########## 4. DmaTcsInterruptDataTransferThreshold

- **UUID**: `ECUC:c03229fe-2dca-426e-a47c-1ae11a6c2822`
- **参数名**: `DmaTcsInterruptDataTransferThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **来源**: INFINEON_AURIX2G
- **描述**: An interrupt can be generated after a certain number of transfers equaling a threshold have been completed.

########## 5. DmaTcsReferenceAddressCrc

- **UUID**: `ECUC:c03929fe-9dca-418e-a47c-1ab11e6c2692`
- **参数名**: `DmaTcsReferenceAddressCrc`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **描述**: Reference CRC value for address CRC

########## 6. DmaTcsReferenceDataCrc

- **UUID**: `ECUC:c03279fe-9dca-418e-a47c-1ab11e6c2692`
- **参数名**: `DmaTcsReferenceDataCrc`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **描述**: Reference CRC value for data CRC

######### BOOLEAN 类型参数

########## 1. DmaTcsCircularBufferSourceEnable

- **UUID**: `ECUC:c03229fe-6dca-419e-a47c-1ab11e6c3262`
- **参数名**: `DmaTcsCircularBufferSourceEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter used to enable/disable the source circular buffer

########## 2. DmaTcsCircularBufferDestinationEnable

- **UUID**: `ECUC:c03229fe-7dca-419e-a47c-1ab11e6c3372`
- **参数名**: `DmaTcsCircularBufferDestinationEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter used to enable/disable the destination circular buffer

########## 3. DmaTcsAppendTimeStamp

- **UUID**: `ECUC:c03229fe-3dca-425e-a47c-1ae11a6c2032`
- **参数名**: `DmaTcsAppendTimeStamp`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter determines if time stamp is to be appended after the last DMA move of a transaction

########## 4. DmaTcsDaisyChaining

- **UUID**: `ECUC:c03229fe-9dca-425e-a47c-1ae11a6c2692`
- **参数名**: `DmaTcsDaisyChaining`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter determines whether the adjacent lower channel is daisy chained with this channel.

########## 5. DmaTcsInterruptSourceAddressWrap

- **UUID**: `ECUC:c03229fe-3dca-426e-a47c-1ae11a6c2932`
- **参数名**: `DmaTcsInterruptSourceAddressWrap`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the wrap source interrupt

########## 6. DmaTcsInterruptDestinationAddressWrap

- **UUID**: `ECUC:c03229fe-4dca-426e-a47c-1ae11a6c3042`
- **参数名**: `DmaTcsInterruptDestinationAddressWrap`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the wrap destination interrupt

########## 7. DmaTcsDataTransferInterrupt

- **UUID**: `ECUC:c03229fe-4dca-416e-a47c-1ae11a6c3042`
- **参数名**: `DmaTcsDataTransferInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the data transfer or transaction interrupt

########## 8. DmaTcsSwapDataCRCByteOrder

- **UUID**: `ECUC:c03229fe-5dca-426e-a47c-1ae12a6c3152`
- **参数名**: `DmaTcsSwapDataCRCByteOrder`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Swaps the Data CRC byte order

########## 9. DmaTcsAutoStartEnable

- **UUID**: `ECUC:c03259fe-5dca-426e-a47c-1ae12a6c3152`
- **参数名**: `DmaTcsAutoStartEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables the autostart feature for linked lists

######### STRING 类型参数

########## 1. DmaTcsSourceAddress

- **UUID**: `ECUC:c03229fe-9dca-418e-a47c-1ab11e6c2692`
- **参数名**: `DmaTcsSourceAddress`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **字符串变体**:
  - 默认值: `NULL_PTR`
- **描述**: start address of the source memory

########## 2. DmaTcsDestinationAddress

- **UUID**: `ECUC:c03229fe-1dca-419e-a47c-1ab11e6c2712`
- **参数名**: `DmaTcsDestinationAddress`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **字符串变体**:
  - 默认值: `NULL_PTR`
- **描述**: Destination address of the source memory

########## 3. DmaTcsDoubleBuffer

- **UUID**: `ECUC:c03229fe-2dca-419e-a47c-1ab11e6c2822`
- **参数名**: `DmaTcsDoubleBuffer`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **字符串变体**:
  - 默认值: `NULL_PTR`
- **描述**: start address of the second buffer

########## 4. DmaUserHeaderFileWithExternDeclarations

- **UUID**: `ECUC:c03229fe-9dca-418e-a47c-1ab11e682592`
- **参数名**: `DmaUserHeaderFileWithExternDeclarations`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **字符串变体**:
  - 默认值: `NULL`
- **描述**: The header file containing the declaration of the variables used for specifying the addresses

######### ENUMERATION 类型参数

########## 1. DmaTcsMoveLength

- **UUID**: `ECUC:c03229fe-3dca-419e-a47c-1ab11e6c2932`
- **参数名**: `DmaTcsMoveLength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_WIDTH_8BITS`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_WIDTH_8BITS` (来源: INFINEON_AURIX2G)
  - `DMA_WIDTH_16BITS` (来源: INFINEON_AURIX2G)
  - `DMA_WIDTH_32BITS` (来源: INFINEON_AURIX2G)
  - `DMA_WIDTH_64BITS` (来源: INFINEON_AURIX2G)
  - `DMA_WIDTH_128BITS` (来源: INFINEON_AURIX2G)
  - `DMA_WIDTH_256BITS` (来源: INFINEON_AURIX2G)
- **描述**: DMA move consisting of one read and one write each) moves data of given number of bits from source to destination. This parameter defines number of bits for the DMA move
                                                        DMA_WIDTH_8BITS : 8-bits per move.
                                                        DMA_WIDTH_16BITS : 16-bits per move.
                                                        DMA_WIDTH_32BITS : 32-bits per move.
                                                        DMA_WIDTH_64BITS : 64-bits per move.
                                                        DMA_WIDTH_128BITS: 128-bits per move.
                                                        DMA_WIDTH_256BITS: 256-bits per move.

########## 2. DmaTcsTransferLength

- **UUID**: `ECUC:c03229fe-4dca-419e-a47c-1ab11e6c3042`
- **参数名**: `DmaTcsTransferLength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_MOVES_1`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_MOVES_1` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_2` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_3` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_4` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_5` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_8` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_9` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of moves composed for a DMA transfer.
                                                        DMA_MOVES_1: 1 DMA move per transfer.
                                                        DMA_MOVES_2: 2 DMA move per transfer.
                                                        DMA_MOVES_3: 3 DMA move per transfer.
                                                        DMA_MOVES_4: 4 DMA move per transfer.
                                                        DMA_MOVES_5: 5 DMA move per transfer.
                                                        DMA_MOVES_8: 8 DMA move per transfer.
                                                        DMA_MOVES_9: 9 DMA move per transfer.
                                                        DMA_MOVES_16: 16 DMA move per transfer.

########## 3. DmaTcsCircularBufferSourceLength

- **UUID**: `ECUC:c03229fe-8dca-419e-a47c-1ab11e6c3482`
- **参数名**: `DmaTcsCircularBufferSourceLength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_CIRCULAR_BUFFER_LENGTH_1BYTE`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_CIRCULAR_BUFFER_LENGTH_1BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_2BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_4BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_8BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_16BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_32BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_64BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_128BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_256BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_512BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_1024BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_2048BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_4096BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_8192BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_16384BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_32768BYTE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines how many bits of the source address of a circular buffer.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_1BYTE: Source address SADR[31:0] is not updated.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_2BYTE: Source address SADR[31:1] is not updated.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_4BYTE: Source address SADR[31:2] is not updated
                                                        .....
                                                        DMA_CIRCULAR_BUFFER_LENGTH_16384BYTE: Source address SADR[31:14] is not updated
                                                        DMA_CIRCULAR_BUFFER_LENGTH_32768BYTE: Source address SADR[31:15] is not updated

########## 4. DmaTcsCircularBufferDestinationLength

- **UUID**: `ECUC:c03229fe-9dca-419e-a47c-1ab11e6c3592`
- **参数名**: `DmaTcsCircularBufferDestinationLength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_CIRCULAR_BUFFER_LENGTH_1BYTE`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_CIRCULAR_BUFFER_LENGTH_1BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_2BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_4BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_8BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_16BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_32BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_64BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_128BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_256BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_512BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_1024BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_2048BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_4096BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_8192BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_16384BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_32768BYTE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines how many bits of the source address of a circular buffer.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_1BYTE: Source address SADR[31:0] is not updated.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_2BYTE: Source address SADR[31:1] is not updated.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_4BYTE: Source address SADR[31:2] is not updated
                                                        .....
                                                        DMA_CIRCULAR_BUFFER_LENGTH_16384BYTE: Source address SADR[31:14] is not updated
                                                        DMA_CIRCULAR_BUFFER_LENGTH_32768BYTE: Source address SADR[31:15] is not updated

########## 5. DmaTcsSourceAddressModificationFactor

- **UUID**: `ECUC:c03229fe-1dca-425e-a47c-1ae11a6c1812`
- **参数名**: `DmaTcsSourceAddressModificationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_FACTOR_1`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_FACTOR_1` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_2` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_4` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_8` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_16` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_32` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_64` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_128` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines how the source address changes after every move operation.
                                                        DMA_FACTOR_1 : Address offset is 1 x DmaMoveLength.
                                                        DMA_FACTOR_2 : Address offset is 2 x DmaMoveLength.
                                                        DMA_FACTOR_4 : Address offset is 4 x DmaMoveLength.
                                                        DMA_FACTOR_8 : Address offset is 8 x DmaMoveLength.
                                                        DMA_FACTOR_16 : Address offset is 16 x DmaMoveLength.
                                                        DMA_FACTOR_32 : Address offset is 32 x DmaMoveLength.
                                                        DMA_FACTOR_64 : Address offset is 64 x DmaMoveLength.                                                        
                                                        DMA_FACTOR_128 : Address offset is 128 x DmaMoveLength.

########## 6. DmaTcsDestinationAddressModificationFactor

- **UUID**: `ECUC:c03229fe-2dca-425e-a47c-1ae11a6c1922`
- **参数名**: `DmaTcsDestinationAddressModificationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_FACTOR_1`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_FACTOR_1` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_2` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_4` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_8` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_16` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_32` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_64` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_128` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines how the source address changes after every move operation.
                                                        DMA_FACTOR_1 : Address offset is 1 x DmaMoveLength.
                                                        DMA_FACTOR_2 : Address offset is 2 x DmaMoveLength.
                                                        DMA_FACTOR_4 : Address offset is 4 x DmaMoveLength.
                                                        DMA_FACTOR_8 : Address offset is 8 x DmaMoveLength.
                                                        DMA_FACTOR_16 : Address offset is 16 x DmaMoveLength.
                                                        DMA_FACTOR_32 : Address offset is 32 x DmaMoveLength.
                                                        DMA_FACTOR_64 : Address offset is 64 x DmaMoveLength.                                                        
                                                        DMA_FACTOR_128 : Address offset is 128 x DmaMoveLength.

########## 7. DmaTcsSourceAddressMovement

- **UUID**: `ECUC:c03229fe-4dca-425e-a47c-1ae11a6c2142`
- **参数名**: `DmaTcsSourceAddressMovement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_INCREASING`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_INCREASING` (来源: INFINEON_AURIX2G)
  - `DMA_DECREASING` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines if the source address after every move operation is to be increased or decreased

########## 8. DmaTcsDestinationAddressMovement

- **UUID**: `ECUC:c03229fe-5dca-425e-a47c-1ae11a6c2252`
- **参数名**: `DmaTcsDestinationAddressMovement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_INCREASING`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_INCREASING` (来源: INFINEON_AURIX2G)
  - `DMA_DECREASING` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines if the Destinaion address after every move operation is to be increased or decreased

########## 9. DmaTcsShadowRegisterConfiguration

- **UUID**: `ECUC:c03229fe-6dca-425e-a47c-1ae11a6c2362`
- **参数名**: `DmaTcsShadowRegisterConfiguration`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_SHADOWING_DISABLED`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_SHADOWING_DISABLED` (来源: INFINEON_AURIX2G)
  - `DMA_SOURCE_ADDRESS_BUFFERING_RO` (来源: INFINEON_AURIX2G)
  - `DMA_DEST_ADDRESS_BUFFERING_RO` (来源: INFINEON_AURIX2G)
  - `DMA_SOURCE_ADDRESS_BUFFERING_RW` (来源: INFINEON_AURIX2G)
  - `DMA_DEST_ADDRESS_BUFFERING_RW` (来源: INFINEON_AURIX2G)
  - `DMA_SOURCE_DOUBLE_BUFFERING_SW_SWITCH` (来源: INFINEON_AURIX2G)
  - `DMA_SOURCE_DOUBLE_BUFFERING_HW_SW_SWITCH` (来源: INFINEON_AURIX2G)
  - `DMA_DEST_DOUBLE_BUFFERING_SW_SWITCH` (来源: INFINEON_AURIX2G)
  - `DMA_DEST_DOUBLE_BUFFERING_HW_SW_SWITCH` (来源: INFINEON_AURIX2G)
  - `DMA_LINKED_LIST` (来源: INFINEON_AURIX2G)
  - `DMA_ACCUMULATED_LINKED_LIST` (来源: INFINEON_AURIX2G)
  - `DMA_SAFE_LINKED_LIST` (来源: INFINEON_AURIX2G)
  - `DMA_CONDITIONAL_LINKED_LIST` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines how the shadow register is to be used

########## 10. DmaTcsTriggerFrequency

- **UUID**: `ECUC:c03229fe-7dca-425e-a47c-1ae11a6c2472`
- **参数名**: `DmaTcsTriggerFrequency`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_TRANSFER_PER_TRIGGER`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_TRANSFER_PER_TRIGGER` (来源: INFINEON_AURIX2G)
  - `DMA_TRANSACTION_PER_TRIGGER` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines how much of data will the move engine move upon a trigger request [Either hardware or software].

########## 11. DmaTcsHardwareTrigger

- **UUID**: `ECUC:c03229fe-8dca-425e-a47c-1ae11a6c2582`
- **参数名**: `DmaTcsHardwareTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_NO_HARDWARE_TRIGGER`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_NO_HARDWARE_TRIGGER` (来源: INFINEON_AURIX2G)
  - `DMA_HARDWARE_TRIGGER_SINGLE_MODE` (来源: INFINEON_AURIX2G)
  - `DMA_HARDWARE_TRIGGER_CONTINUOUS_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the triggering mode for the hardware trigger.

########## 12. DmaTcsInterruptDataTransfer

- **UUID**: `ECUC:c03229fe-1dca-426e-a47c-1ae11a6c2712`
- **参数名**: `DmaTcsInterruptDataTransfer`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_INTERRUPT_PER_TRANSACTION`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_INTERRUPT_PER_TRANSFER` (来源: INFINEON_AURIX2G)
  - `DMA_INTERRUPT_PER_TRANSACTION` (来源: INFINEON_AURIX2G)
  - `DMA_INTERRUPT_AFTER_THRESHOLD` (来源: INFINEON_AURIX2G)
- **描述**: Interrupts can be generated either for every transfer or even transaction.

##### 3. DmaChannelTransactionSet

**容器属性**:

- **UUID**: `ECUC:c03229fe-8dca-418e-a47c-1ab11e6c2582`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DmaChannelTransactionSet`
- **多重性**: [1..65535]

**容器描述**:

Transaction set setting for this DMA channel

###### 参数配置

此容器包含 **31** 个参数：

####### INTEGER 类型参数

######## 1. DmaTcsIndex

- **UUID**: `ECUC:c03229fe-9d4a-418e-a57c-1ab11e6c2692`
- **参数名**: `DmaTcsIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **描述**: DMA Transaction set Index

######## 2. DmaTcsTransactionLength

- **UUID**: `ECUC:c03229fe-5dca-419e-a47c-1ab11e6c3152`
- **参数名**: `DmaTcsTransactionLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16383]
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter defines how many transfers are performed per DMA transaction

######## 3. DmaNextTcsIndex

- **UUID**: `ECUC:c03229fe-6dca-425e-a47c-16e11a6c2362`
- **参数名**: `DmaNextTcsIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter determines the next node of the TCS linked list

######## 4. DmaTcsInterruptDataTransferThreshold

- **UUID**: `ECUC:c03229fe-2dca-426e-a47c-1ae11a6c2822`
- **参数名**: `DmaTcsInterruptDataTransferThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **来源**: INFINEON_AURIX2G
- **描述**: An interrupt can be generated after a certain number of transfers equaling a threshold have been completed.

######## 5. DmaTcsReferenceAddressCrc

- **UUID**: `ECUC:c03929fe-9dca-418e-a47c-1ab11e6c2692`
- **参数名**: `DmaTcsReferenceAddressCrc`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **描述**: Reference CRC value for address CRC

######## 6. DmaTcsReferenceDataCrc

- **UUID**: `ECUC:c03279fe-9dca-418e-a47c-1ab11e6c2692`
- **参数名**: `DmaTcsReferenceDataCrc`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **描述**: Reference CRC value for data CRC

####### BOOLEAN 类型参数

######## 1. DmaTcsCircularBufferSourceEnable

- **UUID**: `ECUC:c03229fe-6dca-419e-a47c-1ab11e6c3262`
- **参数名**: `DmaTcsCircularBufferSourceEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter used to enable/disable the source circular buffer

######## 2. DmaTcsCircularBufferDestinationEnable

- **UUID**: `ECUC:c03229fe-7dca-419e-a47c-1ab11e6c3372`
- **参数名**: `DmaTcsCircularBufferDestinationEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter used to enable/disable the destination circular buffer

######## 3. DmaTcsAppendTimeStamp

- **UUID**: `ECUC:c03229fe-3dca-425e-a47c-1ae11a6c2032`
- **参数名**: `DmaTcsAppendTimeStamp`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter determines if time stamp is to be appended after the last DMA move of a transaction

######## 4. DmaTcsDaisyChaining

- **UUID**: `ECUC:c03229fe-9dca-425e-a47c-1ae11a6c2692`
- **参数名**: `DmaTcsDaisyChaining`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter determines whether the adjacent lower channel is daisy chained with this channel.

######## 5. DmaTcsInterruptSourceAddressWrap

- **UUID**: `ECUC:c03229fe-3dca-426e-a47c-1ae11a6c2932`
- **参数名**: `DmaTcsInterruptSourceAddressWrap`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the wrap source interrupt

######## 6. DmaTcsInterruptDestinationAddressWrap

- **UUID**: `ECUC:c03229fe-4dca-426e-a47c-1ae11a6c3042`
- **参数名**: `DmaTcsInterruptDestinationAddressWrap`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the wrap destination interrupt

######## 7. DmaTcsDataTransferInterrupt

- **UUID**: `ECUC:c03229fe-4dca-416e-a47c-1ae11a6c3042`
- **参数名**: `DmaTcsDataTransferInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the data transfer or transaction interrupt

######## 8. DmaTcsSwapDataCRCByteOrder

- **UUID**: `ECUC:c03229fe-5dca-426e-a47c-1ae12a6c3152`
- **参数名**: `DmaTcsSwapDataCRCByteOrder`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Swaps the Data CRC byte order

######## 9. DmaTcsAutoStartEnable

- **UUID**: `ECUC:c03259fe-5dca-426e-a47c-1ae12a6c3152`
- **参数名**: `DmaTcsAutoStartEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables the autostart feature for linked lists

####### STRING 类型参数

######## 1. DmaTcsSourceAddress

- **UUID**: `ECUC:c03229fe-9dca-418e-a47c-1ab11e6c2692`
- **参数名**: `DmaTcsSourceAddress`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **字符串变体**:
  - 默认值: `NULL_PTR`
- **描述**: start address of the source memory

######## 2. DmaTcsDestinationAddress

- **UUID**: `ECUC:c03229fe-1dca-419e-a47c-1ab11e6c2712`
- **参数名**: `DmaTcsDestinationAddress`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **字符串变体**:
  - 默认值: `NULL_PTR`
- **描述**: Destination address of the source memory

######## 3. DmaTcsDoubleBuffer

- **UUID**: `ECUC:c03229fe-2dca-419e-a47c-1ab11e6c2822`
- **参数名**: `DmaTcsDoubleBuffer`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **字符串变体**:
  - 默认值: `NULL_PTR`
- **描述**: start address of the second buffer

######## 4. DmaUserHeaderFileWithExternDeclarations

- **UUID**: `ECUC:c03229fe-9dca-418e-a47c-1ab11e682592`
- **参数名**: `DmaUserHeaderFileWithExternDeclarations`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **字符串变体**:
  - 默认值: `NULL`
- **描述**: The header file containing the declaration of the variables used for specifying the addresses

####### ENUMERATION 类型参数

######## 1. DmaTcsMoveLength

- **UUID**: `ECUC:c03229fe-3dca-419e-a47c-1ab11e6c2932`
- **参数名**: `DmaTcsMoveLength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_WIDTH_8BITS`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_WIDTH_8BITS` (来源: INFINEON_AURIX2G)
  - `DMA_WIDTH_16BITS` (来源: INFINEON_AURIX2G)
  - `DMA_WIDTH_32BITS` (来源: INFINEON_AURIX2G)
  - `DMA_WIDTH_64BITS` (来源: INFINEON_AURIX2G)
  - `DMA_WIDTH_128BITS` (来源: INFINEON_AURIX2G)
  - `DMA_WIDTH_256BITS` (来源: INFINEON_AURIX2G)
- **描述**: DMA move consisting of one read and one write each) moves data of given number of bits from source to destination. This parameter defines number of bits for the DMA move
                                                        DMA_WIDTH_8BITS : 8-bits per move.
                                                        DMA_WIDTH_16BITS : 16-bits per move.
                                                        DMA_WIDTH_32BITS : 32-bits per move.
                                                        DMA_WIDTH_64BITS : 64-bits per move.
                                                        DMA_WIDTH_128BITS: 128-bits per move.
                                                        DMA_WIDTH_256BITS: 256-bits per move.

######## 2. DmaTcsTransferLength

- **UUID**: `ECUC:c03229fe-4dca-419e-a47c-1ab11e6c3042`
- **参数名**: `DmaTcsTransferLength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_MOVES_1`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_MOVES_1` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_2` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_3` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_4` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_5` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_8` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_9` (来源: INFINEON_AURIX2G)
  - `DMA_MOVES_16` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the number of moves composed for a DMA transfer.
                                                        DMA_MOVES_1: 1 DMA move per transfer.
                                                        DMA_MOVES_2: 2 DMA move per transfer.
                                                        DMA_MOVES_3: 3 DMA move per transfer.
                                                        DMA_MOVES_4: 4 DMA move per transfer.
                                                        DMA_MOVES_5: 5 DMA move per transfer.
                                                        DMA_MOVES_8: 8 DMA move per transfer.
                                                        DMA_MOVES_9: 9 DMA move per transfer.
                                                        DMA_MOVES_16: 16 DMA move per transfer.

######## 3. DmaTcsCircularBufferSourceLength

- **UUID**: `ECUC:c03229fe-8dca-419e-a47c-1ab11e6c3482`
- **参数名**: `DmaTcsCircularBufferSourceLength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_CIRCULAR_BUFFER_LENGTH_1BYTE`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_CIRCULAR_BUFFER_LENGTH_1BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_2BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_4BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_8BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_16BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_32BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_64BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_128BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_256BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_512BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_1024BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_2048BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_4096BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_8192BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_16384BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_32768BYTE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines how many bits of the source address of a circular buffer.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_1BYTE: Source address SADR[31:0] is not updated.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_2BYTE: Source address SADR[31:1] is not updated.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_4BYTE: Source address SADR[31:2] is not updated
                                                        .....
                                                        DMA_CIRCULAR_BUFFER_LENGTH_16384BYTE: Source address SADR[31:14] is not updated
                                                        DMA_CIRCULAR_BUFFER_LENGTH_32768BYTE: Source address SADR[31:15] is not updated

######## 4. DmaTcsCircularBufferDestinationLength

- **UUID**: `ECUC:c03229fe-9dca-419e-a47c-1ab11e6c3592`
- **参数名**: `DmaTcsCircularBufferDestinationLength`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_CIRCULAR_BUFFER_LENGTH_1BYTE`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_CIRCULAR_BUFFER_LENGTH_1BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_2BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_4BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_8BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_16BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_32BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_64BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_128BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_256BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_512BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_1024BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_2048BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_4096BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_8192BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_16384BYTE` (来源: INFINEON_AURIX2G)
  - `DMA_CIRCULAR_BUFFER_LENGTH_32768BYTE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines how many bits of the source address of a circular buffer.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_1BYTE: Source address SADR[31:0] is not updated.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_2BYTE: Source address SADR[31:1] is not updated.
                                                        DMA_CIRCULAR_BUFFER_LENGTH_4BYTE: Source address SADR[31:2] is not updated
                                                        .....
                                                        DMA_CIRCULAR_BUFFER_LENGTH_16384BYTE: Source address SADR[31:14] is not updated
                                                        DMA_CIRCULAR_BUFFER_LENGTH_32768BYTE: Source address SADR[31:15] is not updated

######## 5. DmaTcsSourceAddressModificationFactor

- **UUID**: `ECUC:c03229fe-1dca-425e-a47c-1ae11a6c1812`
- **参数名**: `DmaTcsSourceAddressModificationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_FACTOR_1`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_FACTOR_1` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_2` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_4` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_8` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_16` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_32` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_64` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_128` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines how the source address changes after every move operation.
                                                        DMA_FACTOR_1 : Address offset is 1 x DmaMoveLength.
                                                        DMA_FACTOR_2 : Address offset is 2 x DmaMoveLength.
                                                        DMA_FACTOR_4 : Address offset is 4 x DmaMoveLength.
                                                        DMA_FACTOR_8 : Address offset is 8 x DmaMoveLength.
                                                        DMA_FACTOR_16 : Address offset is 16 x DmaMoveLength.
                                                        DMA_FACTOR_32 : Address offset is 32 x DmaMoveLength.
                                                        DMA_FACTOR_64 : Address offset is 64 x DmaMoveLength.                                                        
                                                        DMA_FACTOR_128 : Address offset is 128 x DmaMoveLength.

######## 6. DmaTcsDestinationAddressModificationFactor

- **UUID**: `ECUC:c03229fe-2dca-425e-a47c-1ae11a6c1922`
- **参数名**: `DmaTcsDestinationAddressModificationFactor`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_FACTOR_1`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_FACTOR_1` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_2` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_4` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_8` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_16` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_32` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_64` (来源: INFINEON_AURIX2G)
  - `DMA_FACTOR_128` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines how the source address changes after every move operation.
                                                        DMA_FACTOR_1 : Address offset is 1 x DmaMoveLength.
                                                        DMA_FACTOR_2 : Address offset is 2 x DmaMoveLength.
                                                        DMA_FACTOR_4 : Address offset is 4 x DmaMoveLength.
                                                        DMA_FACTOR_8 : Address offset is 8 x DmaMoveLength.
                                                        DMA_FACTOR_16 : Address offset is 16 x DmaMoveLength.
                                                        DMA_FACTOR_32 : Address offset is 32 x DmaMoveLength.
                                                        DMA_FACTOR_64 : Address offset is 64 x DmaMoveLength.                                                        
                                                        DMA_FACTOR_128 : Address offset is 128 x DmaMoveLength.

######## 7. DmaTcsSourceAddressMovement

- **UUID**: `ECUC:c03229fe-4dca-425e-a47c-1ae11a6c2142`
- **参数名**: `DmaTcsSourceAddressMovement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_INCREASING`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_INCREASING` (来源: INFINEON_AURIX2G)
  - `DMA_DECREASING` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines if the source address after every move operation is to be increased or decreased

######## 8. DmaTcsDestinationAddressMovement

- **UUID**: `ECUC:c03229fe-5dca-425e-a47c-1ae11a6c2252`
- **参数名**: `DmaTcsDestinationAddressMovement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_INCREASING`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_INCREASING` (来源: INFINEON_AURIX2G)
  - `DMA_DECREASING` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines if the Destinaion address after every move operation is to be increased or decreased

######## 9. DmaTcsShadowRegisterConfiguration

- **UUID**: `ECUC:c03229fe-6dca-425e-a47c-1ae11a6c2362`
- **参数名**: `DmaTcsShadowRegisterConfiguration`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_SHADOWING_DISABLED`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_SHADOWING_DISABLED` (来源: INFINEON_AURIX2G)
  - `DMA_SOURCE_ADDRESS_BUFFERING_RO` (来源: INFINEON_AURIX2G)
  - `DMA_DEST_ADDRESS_BUFFERING_RO` (来源: INFINEON_AURIX2G)
  - `DMA_SOURCE_ADDRESS_BUFFERING_RW` (来源: INFINEON_AURIX2G)
  - `DMA_DEST_ADDRESS_BUFFERING_RW` (来源: INFINEON_AURIX2G)
  - `DMA_SOURCE_DOUBLE_BUFFERING_SW_SWITCH` (来源: INFINEON_AURIX2G)
  - `DMA_SOURCE_DOUBLE_BUFFERING_HW_SW_SWITCH` (来源: INFINEON_AURIX2G)
  - `DMA_DEST_DOUBLE_BUFFERING_SW_SWITCH` (来源: INFINEON_AURIX2G)
  - `DMA_DEST_DOUBLE_BUFFERING_HW_SW_SWITCH` (来源: INFINEON_AURIX2G)
  - `DMA_LINKED_LIST` (来源: INFINEON_AURIX2G)
  - `DMA_ACCUMULATED_LINKED_LIST` (来源: INFINEON_AURIX2G)
  - `DMA_SAFE_LINKED_LIST` (来源: INFINEON_AURIX2G)
  - `DMA_CONDITIONAL_LINKED_LIST` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines how the shadow register is to be used

######## 10. DmaTcsTriggerFrequency

- **UUID**: `ECUC:c03229fe-7dca-425e-a47c-1ae11a6c2472`
- **参数名**: `DmaTcsTriggerFrequency`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_TRANSFER_PER_TRIGGER`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_TRANSFER_PER_TRIGGER` (来源: INFINEON_AURIX2G)
  - `DMA_TRANSACTION_PER_TRIGGER` (来源: INFINEON_AURIX2G)
- **描述**: This parameter determines how much of data will the move engine move upon a trigger request [Either hardware or software].

######## 11. DmaTcsHardwareTrigger

- **UUID**: `ECUC:c03229fe-8dca-425e-a47c-1ae11a6c2582`
- **参数名**: `DmaTcsHardwareTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_NO_HARDWARE_TRIGGER`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_NO_HARDWARE_TRIGGER` (来源: INFINEON_AURIX2G)
  - `DMA_HARDWARE_TRIGGER_SINGLE_MODE` (来源: INFINEON_AURIX2G)
  - `DMA_HARDWARE_TRIGGER_CONTINUOUS_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter defines the triggering mode for the hardware trigger.

######## 12. DmaTcsInterruptDataTransfer

- **UUID**: `ECUC:c03229fe-1dca-426e-a47c-1ae11a6c2712`
- **参数名**: `DmaTcsInterruptDataTransfer`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_INTERRUPT_PER_TRANSACTION`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_INTERRUPT_PER_TRANSFER` (来源: INFINEON_AURIX2G)
  - `DMA_INTERRUPT_PER_TRANSACTION` (来源: INFINEON_AURIX2G)
  - `DMA_INTERRUPT_AFTER_THRESHOLD` (来源: INFINEON_AURIX2G)
- **描述**: Interrupts can be generated either for every transfer or even transaction.

##### 4. DmaMoveEngineConfig

**容器属性**:

- **UUID**: `ECUC:c03229fe-2dca-417e-a47c-1aa11e6c2322`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DmaMoveEngineConfig`
- **多重性**: [0..1]

**容器描述**:

DMA move engine configuration

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. DmaMESourceErrorInterrupt

- **UUID**: `ECUC:c03229fe-3dca-417e-a47c-1aa11e6c2432`
- **参数名**: `DmaMESourceErrorInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the Source error interrupt of a move engine

######## 2. DmaMEDestinationErrorInterrupt

- **UUID**: `ECUC:c03229fe-4dca-417e-a47c-1aa11e6c2542`
- **参数名**: `DmaMEDestinationErrorInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the Destination error interrupt of a move engine

######## 3. DmaMELinkedListErrorInterrupt

- **UUID**: `ECUC:c03229fe-6dca-417e-a47c-1aa11e6c2762`
- **参数名**: `DmaMELinkedListErrorInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: Enables/Disables the Linked List error interrupt of a move engine

##### 5. CommonPublishedInformation

**容器属性**:

- **UUID**: `ECUC:c03229fe-3dca-416e-a47c-1ae11e6c1832`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CommonPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Common container, aggregated by all modules. It contains published information about vendor and versions.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. VendorId

- **UUID**: `ECUC:c03229fe-4dca-445e-a47c-1ae11e6c1842`
- **参数名**: `VendorId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `17`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **描述**: DMA Vendor ID

######## 2. ModuleId

- **UUID**: `ECUC:c03229fe-5dca-455e-a47c-1ae11e6c1852`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **描述**: DMA Module ID

######## 3. ArMajorVersion

- **UUID**: `ECUC:c03229fe-6dca-465e-a47c-1ae11e6c1862`
- **参数名**: `ArMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **描述**: DMA Autosar major version

######## 4. ArMinorVersion

- **UUID**: `ECUC:c03229fe-7dca-475e-a47c-1ae11e6c1872`
- **参数名**: `ArMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **描述**: DMA Autosar mivor version

######## 5. ArPatchVersion

- **UUID**: `ECUC:c03229fe-8dca-485e-a47c-1ae11e6c1882`
- **参数名**: `ArPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **描述**: DMA Autosar major version

######## 6. SwMajorVersion

- **UUID**: `ECUC:c03229fe-9dca-495e-a47c-1ae11e6c1892`
- **参数名**: `SwMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **描述**: Major version number of the vendor specific implementation of the module. The numbering is vendor specific

######## 7. SwMinorVersion

- **UUID**: `ECUC:c03229fe-1dca-415e-a47c-1ae11e6c1812`
- **参数名**: `SwMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `40`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **描述**: Minor version number of the vendor specific implementation of the module. The numbering is vendor specific

######## 8. SwPatchVersion

- **UUID**: `ECUC:c03229fe-2dca-425e-a47c-1ae11e6c1822`
- **参数名**: `SwPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific

####### STRING 类型参数

######## 1. Release

- **UUID**: `3b407478-6777-4f40-b7cf-f33b0854e638`
- **参数名**: `Release`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `_TRICORE_TC397`
- **描述**: AURIX2G derivative used for the implementation

##### 6. DmaResourcePartition

**容器属性**:

- **UUID**: `ECUC:c03229fe-8dca-417e-a47c-1aa11e6c2982`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DmaResourcePartition`
- **多重性**: [4..4]

**容器描述**:

Dma hardware access protection configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DmaPermittedBusMaster

- **UUID**: `ECUC:c03229fe-1dca-418e-a47c-1ab11e6c1812`
- **参数名**: `DmaPermittedBusMaster`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4294967295`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **描述**: permitted bus masters to access this hardware resource. each 32 bit belongs to one master

####### ENUMERATION 类型参数

######## 1. DmaResourcePartitionBusMode

- **UUID**: `ECUC:c03229fe-9dca-417e-a47c-1aa11e6c3092`
- **参数名**: `DmaResourcePartitionBusMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `DMA_RP_SUPERVISOR_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `DMA_RP_USER_MODE` (来源: INFINEON_AURIX2G)
  - `DMA_RP_SUPERVISOR_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This parameter controls whether hardware resources access the on chip buses in supervisor mode or user mode.

####### FUNCTION-NAME 类型参数

######## 1. DmaMoveEngineErrorNotifRoutine

- **UUID**: `ECUC:c03229fe-7dca-417e-a47c-1aa11e6c2872`
- **参数名**: `DmaMoveEngineErrorNotifRoutine`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: User defined Notification Function Pointer of type void NotificationRoutine(uint32_t Channel, Dma_MoveEngineEventType_t Event)

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AURIX2G

- **UUID**: `ECUC:AUTOSAR`
- **包名称**: `AURIX2G`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Dma**
