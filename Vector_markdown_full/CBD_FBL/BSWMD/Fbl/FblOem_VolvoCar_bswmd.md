# Fbl - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:06

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Fbl](#fbl)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Fbl

#### 基本信息

- **UUID**: `c71b8bd5-f404-43d8-9c60-b9daeb75da24`
- **模块名称**: `Fbl`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME

#### 模块描述

Configuration of the Fbl (Flash Bootloader) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 3.00.00

- **发布日期**: 2020-11-24T22:45:56+01:00
- **发布者**: visrcn

**变更内容**:

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. FblGeneral

**容器属性**:

- **UUID**: `517f190f-dd2f-4f8c-81ff-d44c534eb739`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **49** 个参数：

####### INTEGER 类型参数

######## 1. FblMaximumNumberOfSegments

- **UUID**: `3ad90a4d-198a-4b75-8c7f-5ec54278fd08`
- **参数名**: `FblMaximumNumberOfSegments`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The download of an application can be separated in several segments depending on the linker settings. To store the addresses and lengths of these segments, the FBL uses an array. Enter the maximum number of address segments here.

######## 2. FblSleepTime

- **UUID**: `83786666-f8b6-49b5-bee9-c667ab601482`
- **参数名**: `FblSleepTime`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `60000`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If the sleep mode is enabled and the diagnostic layer does not receive a diagnostic request for the period of time specified with this attribute then the function fbl_ap.c::ApplFblBusSleep() is called.

######## 3. FblHeaderAddress

- **UUID**: `15f171e4-8fc0-436f-8f6d-00652d0a0b40`
- **参数名**: `FblHeaderAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This is the start address of the bootloader's FblHeader structure (defined in module fbl_main.c). The bootloader header can be located at an arbitrary address using the provided section #pragma instructions.

CAUTION:
If the application software uses the FblStart mechanism to enter the bootloader, you have to update fbl_cfg.h on change of the FBL header address!

######## 4. FblDiagnosticBufferSize

- **UUID**: `83532550-9884-4cff-b067-53efc97061a4`
- **参数名**: `FblDiagnosticBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This is the size of the RAM buffer which is used to store diagnostic request/response messages. Usually, the download performance will benefit from choosing bigger buffer sizes. The maximum usable buffer size depends on the underlying transport protocol.

######## 5. FblP2Server

- **UUID**: `97bb64c7-1ab3-4944-8880-fd10d2f7ab3a`
- **参数名**: `FblP2Server`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `50`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the P2 diagnostic timeout here. The FBL will always send a response, before P2 expires.

######## 6. FblP2StarServer

- **UUID**: `ecaa58c2-2061-4703-aac6-84b2922478a1`
- **参数名**: `FblP2StarServer`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: P2* diagnostic response pending time. The FBL will send response pending messages while processing long-lasting service requests. Use this option to configure the response pending timing.

######## 7. FblS3ServerExtendedSession

- **UUID**: `be21218d-a925-4c8a-b94f-fe298a32e39f`
- **参数名**: `FblS3ServerExtendedSession`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specifiy the S3 diagnostic timeout for the extended session here. Time for the FBL to keep the extended diagnostic session active while not receiving any diagnostic request message.

######## 8. FblS3ServerProgrammingSession

- **UUID**: `236b6f0b-44cf-4c36-a69c-fa6ee2d18f58`
- **参数名**: `FblS3ServerProgrammingSession`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify the S3 diagnostic timeout for the programming session here. Time for the FBL to keep the programming diagnostic session active while not receiving any diagnostic request message.

######## 9. FblFillCode

- **UUID**: `398e83d2-931b-4014-a038-79dea72e44a1`
- **参数名**: `FblFillCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The gaps between two download segments will be filled with the specified byte code. It's recommended to use an illegal opcode according to the used hardware platform.

######## 10. FblWatchdogTriggerCycle

- **UUID**: `e8eac1ee-163c-4abb-9e98-7d1c0a18c438`
- **参数名**: `FblWatchdogTriggerCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If the watchdog service is enabled, the bootloader will call user function fbl_apwd.c::ApplFblWDTrigger() with the specified cycle time.

######## 11. FblDataProcessingBufferSize

- **UUID**: `0dbd548a-6d07-40fd-a37c-8d9b311e125b`
- **参数名**: `FblDataProcessingBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the maximum output buffer size available for handling of preprocessed data, e.g. decryption or decompression.

######## 12. FblVerificationSegmentation

- **UUID**: `e6de1d3f-0ec8-4c45-b4bb-78f79bf107c6`
- **参数名**: `FblVerificationSegmentation`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the maximum data length passed to the on-the-fly verification in a single processing cycle.

######## 13. FblWriteSegmentation

- **UUID**: `fa91b732-3fe3-4db7-b9dd-94ab088b49a0`
- **参数名**: `FblWriteSegmentation`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Defines the maximum data length passed to the programming routine in a single processing cycle.
Used for options "Adaptive RCR-RP for TransferData service" and "Pipelined programming".

######## 14. FblMaximumAmountOfLogicalBlocks

- **UUID**: `10aaa9f4-aebd-4a35-a7b6-82bf7fcfe984`
- **参数名**: `FblMaximumAmountOfLogicalBlocks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This is the maximum number of logical blocks which can be handled by the bootloader. For the configuration of this value, please consider potential growth of the LBT in the future. After the bootloader has been programmed into the ECU, it’s not possible to download an LBT where the number of blocks exceeds the configured value.

Note: The parameter is only considered if FblReprogrammableLbt is enabled.

######## 15. FblBlockStartAddress

- **UUID**: `260c0cc3-7edc-482a-847c-09511df1fbc5`
- **参数名**: `FblBlockStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Start address of the FBL block.

######## 16. FblBlockLength

- **UUID**: `91c7b8c5-ee04-4b64-bbb6-9208813aca88`
- **参数名**: `FblBlockLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Length of the FBL block in bytes.

####### BOOLEAN 类型参数

######## 1. FblStayInBoot

- **UUID**: `36f62416-fb05-4df4-aec8-0f9e9ba2ecda`
- **参数名**: `FblStayInBoot`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If activated the FBL waits a specified time before jumping to a valid application. If a special message is received within this time the FBL stays active. This feature is designed for development phase to avoid reflashing the FBL if the application doesn't work properly.

######## 2. FblSleepMode

- **UUID**: `dafd960e-d37d-43ef-8095-3c32c0354c28`
- **参数名**: `FblSleepMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enable sleep mode/power down support for FBL.

######## 3. FblApplicationTimerTask

- **UUID**: `a70f0ec8-09e5-4897-b26a-aa8e0d597b70`
- **参数名**: `FblApplicationTimerTask`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If this option is enabled, the bootloader provides function fbl_ap.c::ApplFblTask(). You can add user specific code to this function which will be called cyclically by the bootloader. The actual call cycle is derived from GENy attribute FblTp_Iso/TP call cycle.

Note: The task function won't be called during diagnostic service processing.

######## 4. FblGapFilling

- **UUID**: `9bc58874-2772-41cf-b4fd-57239e9a5750`
- **参数名**: `FblGapFilling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If this option is enabled, the bootloader will fill any gaps in the download file (Flashware) with the value of the Fill code attribute.

######## 5. FblInternalMemoryCopy

- **UUID**: `f5842baa-4400-4e95-999f-d2fa90fd0640`
- **参数名**: `FblInternalMemoryCopy`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled, the bootloader will use an internal memory copy function instead of the library memcpy() function of the compiler vendor.

######## 6. FblGatewaySupport

- **UUID**: `06e43226-d6fa-4b03-b44a-fdef1816e8ff`
- **参数名**: `FblGatewaySupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This option is used for bootloaders that are connected to multiple CAN networks and contains a gateway support feature. 
It controls if the bootloader shall support or not the gateway feature. The gateway feature routes messages from a main network to one or more sub networks, depending on the feature of the gateway support in the bootloader.

######## 7. FblPresencePattern

- **UUID**: `c4ac63d9-c612-44f3-adcc-de009adfbb52`
- **参数名**: `FblPresencePattern`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Logical blocks and/or application validation is checked using presence patterns at the end of each logical block. If this option is used, the decision if an application is available can be made without loading a memory driver (e.g. Eeprom Emulation or external Eeprom).

######## 8. FblStartFunction

- **UUID**: `3fc18ed9-7af8-4537-a6c7-0884d1bcf899`
- **参数名**: `FblStartFunction`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This option provides a user-friendly way to start the bootloader from within the application by using the macro CallFblStart().

PRECONDITIONS:
- The FblHeader address is configured correctly (see GENy component FblDrvCan_*).
- The application module which uses CallFblStart() includes fbl_def.h (fbl_cfg.h has to be provided, too). Remember to update fbl_cfg.h if the address of FblHeader changes!

By disabling this option, the user can gain more influence on how the transition from application to bootloader is done.
This is the procedure which has to be followed:
- Set a flag in the application software
- Issue a reset
- Check flag in user adaptable function fbl_apnv.c::ApplFblExtProgRequest() and provide the appropriate return value.

######## 9. FblCommonData

- **UUID**: `c3b9e800-f98f-4639-a949-9734e3ff0eb7`
- **参数名**: `FblCommonData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: By enabling this option, the bootloader provides an interface to access (constant) data which is linked with the bootloader. This enables the application software to read e.g. DID values from the same memory location as the bootloader. In particular, this is useful for DIDs that report hardware specific information which doesn't change if the application software is updated.
The structure of the common data is completely user specific and can be declared in file comdat.h. The actual structure definition is usually located in file fbl_ap.c. The bootloader stores the address of this structure in the FblHeader. The respective value can be retrieved by using macro GetFblCommonDataPtr().
To access the common data via GetFblCommonDataPtr(), the application software has to include the files fbl_def.h (which itself needs fbl_cfg.h) and comdat.h.
For more detailed usage information, please refer to the respective technical reference.

######## 10. FblResponseAfterReset

- **UUID**: `deb0914d-8d1b-4a4f-b0bc-5ee3452e779b`
- **参数名**: `FblResponseAfterReset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Send the response to a default session request or a reset request after the ECU has been reset.

Before the reset, a response pending message is sent by the Bootloader. The actual response has to be sent by the application software or the Bootloader depending on a flag set in non-initialized memory.

######## 11. FblUserSubfunction

- **UUID**: `9e3d28c1-3e1d-4ad0-a1eb-15136d15da74`
- **参数名**: `FblUserSubfunction`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This option can be activated if user specific subfunction parameters have to be supported which are not defined within the OEM specification.
If the bootloader receives a request with a supported service identifier and an unknown subfunction parameter, the user adaptable function fbl_apdi.c::ApplDiagUserSubFunction() will be called.

######## 12. FblUserService

- **UUID**: `e8187137-1546-480c-b1c4-0c176e203829`
- **参数名**: `FblUserService`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This option can be activated if user specific diagnostic services have to be supported which are not defined within the OEM specification.
If the bootloader receives a request with an unsupported service identifier, the user adaptable function fbl_apdi.c::ApplDiagUserService() will be called.

######## 13. FblUserRoutine

- **UUID**: `c69326ee-0e31-4635-95a6-14512ebc2c9e`
- **参数名**: `FblUserRoutine`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This option can be activated if user specific diagnostic routines have to be supported which are not defined within the OEM specification.
If the bootloader receives a request with an unsupported routine ID, the user adaptable function fbl_apdi.c::ApplDiagRoutineControl() will be called.

######## 14. FblWatchdogService

- **UUID**: `7b36976d-d786-4cee-a309-f16b8192c2a1`
- **参数名**: `FblWatchdogService`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If this option is enabled, the bootloader provides an API for watchdog service handling. User specific watchdog service code can be added to function fbl_apwd.c::ApplFblWDTrigger().

######## 15. FblEncryptionMode

- **UUID**: `3dd77f8c-daf6-47b7-96dc-7d5d518fe434`
- **参数名**: `FblEncryptionMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enabling this option allows for transmission of encrypted data. The data which is received by the bootloader will be decrypted by means of a dedicated decryption module.

######## 16. FblCompressionMode

- **UUID**: `64863c20-da9e-4a65-aa3d-d0341d805d5f`
- **参数名**: `FblCompressionMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enabling this option allows for transmission of compressed data. The data which is received by the bootloader will be decompressed by means of a dedicated compression module.

######## 17. FblInputVerification

- **UUID**: `003c4cac-0136-44af-b0f5-e317d5762669`
- **参数名**: `FblInputVerification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the signature verification will take the downloaded data instead of the data written to non-volatile memory (e.g. flash) as input.
The transferred data is passed to the hash/checksum calculation before any data processing takes place. E.g. if compressed data is downloaded the signature is calculated over the compressed data and not the uncompressed contents actually written to flash.

######## 18. FblProcessedVerification

- **UUID**: `bacb8ed7-0645-4409-80fe-039f4500f3d0`
- **参数名**: `FblProcessedVerification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

######## 19. FblPipelinedVerification

- **UUID**: `8230d69d-160b-41b3-81c9-5e2fbfd61b38`
- **参数名**: `FblPipelinedVerification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

######## 20. FblOutputVerification

- **UUID**: `ae3aeeb4-9550-4370-a85f-c172e727fc91`
- **参数名**: `FblOutputVerification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

######## 21. FblAdaptiveDataTransferRcrrp

- **UUID**: `29bb75de-2b21-4c14-982e-9597e294707e`
- **参数名**: `FblAdaptiveDataTransferRcrrp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Disable to force the transmission of the first RCR-RP (Response Pending) message before starting processing of the download data.
If enabled the first RCR-RP will be conditionally send based on the P2 timeout. Requires that a single program operation takes less than P2!
Programming time depends on "Write segmentation" and/or "Data processing buffer size"
Also applies to times required by on-the-fly signature verification and data processing.

######## 22. FblPipelinedProgramming

- **UUID**: `91189456-351a-4aab-aaef-caf752cff154`
- **参数名**: `FblPipelinedProgramming`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: With this feature enabled, the FBL immediately sends a positive response after the reception of a TransferData request, so that the next data transfer can be performed while the previous data block is programmed. The same parallelization applies to the signature calculation over the transfer data in RAM and the decompression/decryption of the received data. In best case only the pure transmission time is required.

######## 23. FblSuspendDriverOperation

- **UUID**: `59b47d69-aeab-4523-b856-c32fa41942d8`
- **参数名**: `FblSuspendDriverOperation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Memory driver can be suspended in mid-operation by external event.

######## 24. FblUnalignedDataTransfer

- **UUID**: `844a35e1-a16e-4b3f-ad15-7acb3677e04f`
- **参数名**: `FblUnalignedDataTransfer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If enabled the data transferred during download using the TransferData service can be of arbitrary length.
Otherwise all data transfers have to be aligned to a multiple of the largest memory write segment size.

######## 25. FblVerificationFunction

- **UUID**: `dee5700a-4fb1-4b50-816d-e90d940e5970`
- **参数名**: `FblVerificationFunction`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Add support for Driver_VerifySync

######## 26. FblApplicationStateTask

- **UUID**: `212d0309-22c8-4a03-bf5a-a0316284150d`
- **参数名**: `FblApplicationStateTask`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If this option is enabled, the bootloader provides function fbl_ap.c::ApplFblStateTask(). You can add user specific code to this function which will be called as a background task by the bootloader.

Note: The task function won't be called during diagnostic service processing.

######## 27. FblReprogrammableLbt

- **UUID**: `2e96a021-d776-42ff-a066-ab8c653b98f1`
- **参数名**: `FblReprogrammableLbt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enable support for post-build update of the Logical Block Table. If this option is enabled, the generated Fbl_Lbt.c/Fbl_Lbt.h files will only contain the SBL and LBT blocks. The full version of the LBT will be generated into the files Fbl_Lbt_PBcfg.c/Fbl_Lbt_PBcfg.h.

######## 28. FblOta

- **UUID**: `cef6ffbc-e482-4e42-9646-48bd5dc274fd`
- **参数名**: `FblOta`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables support for Over The Air update functionality in the Bootloader. To be used with an application stack that supports OTA.

######## 29. FblOneStepUpdater

- **UUID**: `a1c872d1-e6a4-4e23-bf8d-b3f03f5b626a`
- **参数名**: `FblOneStepUpdater`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables/disables the one step updater. In case it is enabled, the Updater as well as the Application/Data is downloaded in one flashing process. This means that the Updater is started after it was downloaded.

######## 30. FblHardwareSwap

- **UUID**: `1d88a3d8-9abf-4720-9a79-714db1c9085d`
- **参数名**: `FblHardwareSwap`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Specify if the hardware swap should be used.

####### STRING 类型参数

######## 1. FblUserConfigFile

- **UUID**: `7e06f6b3-0f50-4298-b38a-1e8caf5c98cc`
- **参数名**: `FblUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: FBL: If a file path is specified, the file is read and its contents are put at the end of the FBL config file.

DEM: Path to an external user configuration file used by the "Configurator 5" generation tool.

If you want to overwrite some of the settings in the generated configuration file (Dem_Cfg.h), you can specify a path to a user defined configuration file. The user defined configuration file will be included at the end of the generated preprocessor switches. Definitions in the user defined configuration file can overwrite definitions in the generated configuration file. 

To specify the file name, you can use "$(var)" sequence(s) in the specified path. Each such sequence is replaced by the content of the related environment variable "var".
Additionally you can use following predefined sequences:
$(DpaProjectFolder) Absolute directory of the loaded *.dpa file.
$(EcuProjectName) Name of the project defined in the loaded *.dpa file.
$(EcucFile) Absolute directory "ECUC", defined by the loaded *.dpa file, containing files $(EcuProjectName).ecuc.arxml and $(EcuProjectName).ecuc.Initial.arxml .
$(EcucFolder) Parent directory of $(EcucFile).
$(SipRootPath) Absolute directory "SIP", defined by the loaded *.dpa file.
$(OutputFolder) (Relative) directory "GenData", defined by the loaded *.dpa file. See setting "Root Target Folder" of Configurator 5.
$(ServiceSwcFolder) Absolute directory "ServiceComponents", defined by the loaded *.dpa file.
$(cwd) Current working directory when starting Configurator 5.

RESTRICTIONS: Not all of the settings can be overwritten simply by triggering the preprocessor switch. Some of the options are complex and the code generator generates less or more code depending on the setting.

USE SUCH A FILE ONLY AFTER DISCUSSION WITH VECTOR.

####### ENUMERATION 类型参数

######## 1. FblProjectState

- **UUID**: `d1f6672e-65d8-4934-83f2-d1438b1e5b10`
- **参数名**: `FblProjectState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `INTEGRATION`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `PRODUCTION_REDUCED_CHECKS` (来源: Vector Informatik)
  - `PRODUCTION_DEFAULT` (来源: Vector Informatik)
  - `INTEGRATION` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Code that is required for integration/development is automatically removed once the production state is configured. Test FBL_PROJECT_STATE for FBL_INTEGRATION / FBL_PRODUCTION to use this for your own code. Bootloader internal checks are configured according to the current project state:

~~~ Integration ~~~
Choose this state during development/integration of your integration project.
This configuration adds internal configuration and user code checks and hence helps you to find configuration errors easily. Errors found will trigger the callback ApplFblFatalError(). A user specific error handling can be added, e.g. flashing Led if no debugger is available (default: while(1){;});

~~~ Production (default) ~~~
Choose this state when ready for production.
Configuration checks are turned off.

~~~ Production (reduced checks) ~~~
Choose this state when ready for production and if you need to minimize code size.
Some additional checks will also be disabled in order to reduce code size. The resulting configuration reports NRCs on runtime errors late. This will make it more difficult to analyze errors that occur on production ECUs. It is therefore recommended to configure "Production (default)" if possible.

######## 2. FblFlashDriverUsage

- **UUID**: `a20663a9-8f24-4e4b-9ac4-811ee081dd4d`
- **参数名**: `FblFlashDriverUsage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DOWNLOAD_DRIVER`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DOWNLOAD_DRIVER` (来源: Vector Informatik)
  - `USE_FLASH_DRIVER_FROM_ROM` (来源: Vector Informatik)
  - `OPTIONAL_FLASH_DRIVER_DOWNLOAD` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Configures the source of the flash driver RAM image.

Download Driver: Flash Driver is downloaded to the ECU.
Use Flash Driver from ROM: Flash Driver is stored in an encrypted ROM image in the bootloader’s flash memory and copied to RAM before initialization.
Optional Flash Driver Download: Flash Driver can be downloaded to the ECU. If it isn’t downloaded, the flash driver from an internal image will be used.

Please note: Depending on your OEM’s requirements, not all of these options may be available in the embedded bootloader implementation.

##### 2. FblFlashBlockTable

**容器属性**:

- **UUID**: `98205f70-2c53-49bc-bf4d-b4c86f4821bf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblFlashBlockTable`
- **多重性**: [1..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FblFlashBlock

**容器属性**:

- **UUID**: `253bd6e4-512d-40f6-b18c-7b3d95dc8043`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblFlashBlock`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FblFbStartAddress

- **UUID**: `64ff10f4-7dd4-4c66-8a15-cbc404f79c50`
- **参数名**: `FblFbStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Start address of the flash block.

########## 2. FblFbEndAddress

- **UUID**: `7ae48668-44b4-404b-a9fa-e436b0944c43`
- **参数名**: `FblFbEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: End address of the flash block.

######### STRING 类型参数

########## 1. FblFbDescription

- **UUID**: `5eee1dd8-0e48-4a51-9b68-529a7fddef2e`
- **参数名**: `FblFbDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: A short description of the flash block.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. FblFbMemoryDeviceRef

- **UUID**: `6952bbd6-a1cf-401e-bd42-76ea5bd0bb56`
- **引用名**: `FblFbMemoryDeviceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `FblMemoryDevice`
- **完整路径**: `/MICROSAR/Fbl/FblMemoryDeviceTable/FblMemoryDevice`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

########## 2. FblFbLogicalBlockRef

- **UUID**: `18748905-78ff-4ee7-874f-39cd7bd19d27`
- **引用名**: `FblFbLogicalBlockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `FblLogicalBlock`
- **完整路径**: `/MICROSAR/Fbl/FblLogicalBlockTable/FblLogicalBlock`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

##### 3. FblFlashBlock

**容器属性**:

- **UUID**: `253bd6e4-512d-40f6-b18c-7b3d95dc8043`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblFlashBlock`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. FblFbStartAddress

- **UUID**: `64ff10f4-7dd4-4c66-8a15-cbc404f79c50`
- **参数名**: `FblFbStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Start address of the flash block.

######## 2. FblFbEndAddress

- **UUID**: `7ae48668-44b4-404b-a9fa-e436b0944c43`
- **参数名**: `FblFbEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: End address of the flash block.

####### STRING 类型参数

######## 1. FblFbDescription

- **UUID**: `5eee1dd8-0e48-4a51-9b68-529a7fddef2e`
- **参数名**: `FblFbDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: A short description of the flash block.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. FblFbMemoryDeviceRef

- **UUID**: `6952bbd6-a1cf-401e-bd42-76ea5bd0bb56`
- **引用名**: `FblFbMemoryDeviceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `FblMemoryDevice`
- **完整路径**: `/MICROSAR/Fbl/FblMemoryDeviceTable/FblMemoryDevice`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

######## 2. FblFbLogicalBlockRef

- **UUID**: `18748905-78ff-4ee7-874f-39cd7bd19d27`
- **引用名**: `FblFbLogicalBlockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `FblLogicalBlock`
- **完整路径**: `/MICROSAR/Fbl/FblLogicalBlockTable/FblLogicalBlock`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

##### 4. FblLogicalBlockTable

**容器属性**:

- **UUID**: `f498f78c-8d20-487e-906c-6c516289215c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblLogicalBlockTable`
- **多重性**: [1..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FblLogicalBlock

**容器属性**:

- **UUID**: `c8b4852b-c996-4920-a237-afe8fd927360`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblLogicalBlock`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. FblLbBlockIndex

- **UUID**: `9c123740-70b1-4abc-b7ff-e12a15ad8b04`
- **参数名**: `FblLbBlockIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

########## 2. FblLbStartAddress

- **UUID**: `04068ab3-7fa1-4422-820a-ab9fe62edd9a`
- **参数名**: `FblLbStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Start address of the logical block. This value is computed automatically.

########## 3. FblLbEndAddress

- **UUID**: `22253013-06fb-4879-bfbe-324f7f078690`
- **参数名**: `FblLbEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: End address of the logical block. This value is computed automatically.

########## 4. FblLbHeaderAddress

- **UUID**: `ab7f0f15-7ac6-495f-9dfd-b59a02216fcc`
- **参数名**: `FblLbHeaderAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

########## 5. FblLbBmHeaderAddress

- **UUID**: `e1fa2949-3655-429a-9025-8677be99067b`
- **参数名**: `FblLbBmHeaderAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Header address of the BootManager. The value has to be within the start and end address of the logical block.

######### STRING 类型参数

########## 1. FblLbOutputVerification

- **UUID**: `002f4839-d11e-4d9c-b894-393d895b8ca8`
- **参数名**: `FblLbOutputVerification`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `SecM_Verification`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Verification function used for output verification. The interface of the provided function has to be compatible with the prototype of SecM_Verification.

When "Output Verification" is enabled, this function verification will take the data written to non-volatile memory (e.g. flash) as input.
The processing will be performed on the written contents, after the complete data was transferred and programmed.

In some use cases it might be useful to call an alternative user-specific function for a logical block. E.g. if you like to avoid read back of the written data from a slave processor in a multi-processor configuration. This function could pass the request including the necessary information to the slave controller. Calculation is then carried out on the slave controller and the result is passed back to the master controller.

Set to "0" to disable output verification for this particular block. Caution: In this case the Bootloader will accept any signature/checksum, regardless of the previously downloaded data!

########## 2. FblLbDescription

- **UUID**: `37df208c-1d63-43a5-82a0-e8fad462021e`
- **参数名**: `FblLbDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Short description of this Logical Block

######### ENUMERATION 类型参数

########## 1. FblLbBlockType

- **UUID**: `ee1ed2ee-73e6-42c6-b974-a3cbb339298b`
- **参数名**: `FblLbBlockType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CODE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SOFTWARE` (来源: Vector Informatik)
  - `SBL` (来源: Vector Informatik)
  - `ESS` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

########## 2. FblLbDisposability

- **UUID**: `a38e128c-f7be-42ef-b7fb-daf563a991ca`
- **参数名**: `FblLbDisposability`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `MANDATORY`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MANDATORY` (来源: Vector Informatik)
  - `OPTIONAL` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

##### 5. FblLogicalBlock

**容器属性**:

- **UUID**: `c8b4852b-c996-4920-a237-afe8fd927360`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblLogicalBlock`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. FblLbBlockIndex

- **UUID**: `9c123740-70b1-4abc-b7ff-e12a15ad8b04`
- **参数名**: `FblLbBlockIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

######## 2. FblLbStartAddress

- **UUID**: `04068ab3-7fa1-4422-820a-ab9fe62edd9a`
- **参数名**: `FblLbStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Start address of the logical block. This value is computed automatically.

######## 3. FblLbEndAddress

- **UUID**: `22253013-06fb-4879-bfbe-324f7f078690`
- **参数名**: `FblLbEndAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: End address of the logical block. This value is computed automatically.

######## 4. FblLbHeaderAddress

- **UUID**: `ab7f0f15-7ac6-495f-9dfd-b59a02216fcc`
- **参数名**: `FblLbHeaderAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

######## 5. FblLbBmHeaderAddress

- **UUID**: `e1fa2949-3655-429a-9025-8677be99067b`
- **参数名**: `FblLbBmHeaderAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Header address of the BootManager. The value has to be within the start and end address of the logical block.

####### STRING 类型参数

######## 1. FblLbOutputVerification

- **UUID**: `002f4839-d11e-4d9c-b894-393d895b8ca8`
- **参数名**: `FblLbOutputVerification`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `SecM_Verification`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Verification function used for output verification. The interface of the provided function has to be compatible with the prototype of SecM_Verification.

When "Output Verification" is enabled, this function verification will take the data written to non-volatile memory (e.g. flash) as input.
The processing will be performed on the written contents, after the complete data was transferred and programmed.

In some use cases it might be useful to call an alternative user-specific function for a logical block. E.g. if you like to avoid read back of the written data from a slave processor in a multi-processor configuration. This function could pass the request including the necessary information to the slave controller. Calculation is then carried out on the slave controller and the result is passed back to the master controller.

Set to "0" to disable output verification for this particular block. Caution: In this case the Bootloader will accept any signature/checksum, regardless of the previously downloaded data!

######## 2. FblLbDescription

- **UUID**: `37df208c-1d63-43a5-82a0-e8fad462021e`
- **参数名**: `FblLbDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Short description of this Logical Block

####### ENUMERATION 类型参数

######## 1. FblLbBlockType

- **UUID**: `ee1ed2ee-73e6-42c6-b974-a3cbb339298b`
- **参数名**: `FblLbBlockType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CODE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SOFTWARE` (来源: Vector Informatik)
  - `SBL` (来源: Vector Informatik)
  - `ESS` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

######## 2. FblLbDisposability

- **UUID**: `a38e128c-f7be-42ef-b7fb-daf563a991ca`
- **参数名**: `FblLbDisposability`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `MANDATORY`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MANDATORY` (来源: Vector Informatik)
  - `OPTIONAL` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME

##### 6. FblMemoryDeviceTable

**容器属性**:

- **UUID**: `14c049a3-fcdf-4a87-8464-ec24bbdbb4a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblMemoryDeviceTable`
- **多重性**: [1..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FblMemoryDevice

**容器属性**:

- **UUID**: `1fd8d636-da1d-42f0-bef1-2b75324aad81`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblMemoryDevice`
- **多重性**: [0..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. FblMdIndex

- **UUID**: `9393bcd4-8255-45ba-a078-f3fba2b45b2c`
- **参数名**: `FblMdIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This value specifies the unique index of the memory device.

########## 2. FblMdSegmentSize

- **UUID**: `e6988fdd-9d54-4bb5-ac29-7fbc87b7126d`
- **参数名**: `FblMdSegmentSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Write segment size of memory device. The write segment size is the smallest entity that can be programmed in one write access. Refer to the memory device specification for this value.

########## 3. FblMdErasedValue

- **UUID**: `3f7cfb70-5be1-44c9-b6be-3ab2e9598779`
- **参数名**: `FblMdErasedValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Erased value of the memory device. The erased value is the memory content after the memory was erased. Refer to the memory device specification for this value.

######### BOOLEAN 类型参数

########## 1. FblMdInitHook

- **UUID**: `5825010b-7c84-4e9c-a879-b30aa21d83df`
- **参数名**: `FblMdInitHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the init function is called.

########## 2. FblMdDeinitHook

- **UUID**: `cd70c4fe-8935-402b-9c7d-677c46219ec3`
- **参数名**: `FblMdDeinitHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the deinit function is called.

########## 3. FblMdReadHook

- **UUID**: `8244b40b-d334-4ada-a43c-91072c59a34a`
- **参数名**: `FblMdReadHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the read function is called.

########## 4. FblMdEraseHook

- **UUID**: `97bfb86f-ea28-4b8e-830e-105ef1c4249a`
- **参数名**: `FblMdEraseHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the erase function is called.

########## 5. FblMdWriteHook

- **UUID**: `8c3b9e2b-0478-41d2-9f86-377f0c1b9f88`
- **参数名**: `FblMdWriteHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the write function is called.

########## 6. FblMdVerifyHook

- **UUID**: `021429e9-b472-4619-bd9a-920fa679f49e`
- **参数名**: `FblMdVerifyHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the verify function is called.

Note: Only applicable for certain platforms, e.g. RL78

##### 7. FblMemoryDevice

**容器属性**:

- **UUID**: `1fd8d636-da1d-42f0-bef1-2b75324aad81`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblMemoryDevice`
- **多重性**: [0..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. FblMdIndex

- **UUID**: `9393bcd4-8255-45ba-a078-f3fba2b45b2c`
- **参数名**: `FblMdIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This value specifies the unique index of the memory device.

######## 2. FblMdSegmentSize

- **UUID**: `e6988fdd-9d54-4bb5-ac29-7fbc87b7126d`
- **参数名**: `FblMdSegmentSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Write segment size of memory device. The write segment size is the smallest entity that can be programmed in one write access. Refer to the memory device specification for this value.

######## 3. FblMdErasedValue

- **UUID**: `3f7cfb70-5be1-44c9-b6be-3ab2e9598779`
- **参数名**: `FblMdErasedValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Erased value of the memory device. The erased value is the memory content after the memory was erased. Refer to the memory device specification for this value.

####### BOOLEAN 类型参数

######## 1. FblMdInitHook

- **UUID**: `5825010b-7c84-4e9c-a879-b30aa21d83df`
- **参数名**: `FblMdInitHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the init function is called.

######## 2. FblMdDeinitHook

- **UUID**: `cd70c4fe-8935-402b-9c7d-677c46219ec3`
- **参数名**: `FblMdDeinitHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the deinit function is called.

######## 3. FblMdReadHook

- **UUID**: `8244b40b-d334-4ada-a43c-91072c59a34a`
- **参数名**: `FblMdReadHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the read function is called.

######## 4. FblMdEraseHook

- **UUID**: `97bfb86f-ea28-4b8e-830e-105ef1c4249a`
- **参数名**: `FblMdEraseHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the erase function is called.

######## 5. FblMdWriteHook

- **UUID**: `8c3b9e2b-0478-41d2-9f86-377f0c1b9f88`
- **参数名**: `FblMdWriteHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the write function is called.

######## 6. FblMdVerifyHook

- **UUID**: `021429e9-b472-4619-bd9a-920fa679f49e`
- **参数名**: `FblMdVerifyHook`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the verify function is called.

Note: Only applicable for certain platforms, e.g. RL78

##### 8. FblVolvoCar

**容器属性**:

- **UUID**: `eca455df-0f6b-4635-b2c0-6787a4d823e9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FblVolvoCar`
- **多重性**: [1..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. FblMaximumReadableDIDs

- **UUID**: `ece3d4b6-4cd9-4314-9ec8-74459b402356`
- **参数名**: `FblMaximumReadableDIDs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [5..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This attribute defines the maximum number of data identifiers which can be handled by the bootloader in a single ReadDataByIdentifier request. The specified value is used to allocate a RAM buffer which will keep the DIDs which have been extracted from the diag buffer.
If the specified maximum number is exceeded, the bootloader will respond with NRC 0x13 (IncorrectMessageLengthOrInvalidFormat).

######## 2. FblCompleteAndCompatibleBlockAddress

- **UUID**: `efb8a1d7-8b4e-4d3a-9d10-cc38937d6e82`
- **参数名**: `FblCompleteAndCompatibleBlockAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: This value defines the memory address where the complete & compatible block will be stored.

####### BOOLEAN 类型参数

######## 1. FblWriteDataByIdentifierService

- **UUID**: `6e254577-6f21-477b-8cdc-8d97f954cd52`
- **参数名**: `FblWriteDataByIdentifierService`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If activated, the optional diagnostic service WriteDataByIdentifier (0x2E) will be provided. Turn the option off to reduce the bootloader code size or if the service shall not be supported.

Note: Customer specific data identifiers can be added to user adaptable function fbl_apdi.c::ApplFblWriteDataByIdentifier().

######## 2. FblRequestUploadService

- **UUID**: `deb14b30-cc06-4b8d-94d5-eb1afa3860f1`
- **参数名**: `FblRequestUploadService`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: If activated, the optional diagnostic service RequestUpload (0x35) will be provided. Turn the option off to reduce the bootloader code size or if the service shall not be supported.

######## 3. FblFlashErasedDetection

- **UUID**: `1968c317-b207-49ab-b2dc-61e842831e25`
- **参数名**: `FblFlashErasedDetection`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: The flash erased detection feature provides the possibility to check whether the flash memory is already erased or not. The intention is to reduce the overall download time of the initial ECU programming process at end-of-line.

CAUTION: This feature is subject to certain restrictions which have to be considered before activation. Please consult the technical reference for further information!

######## 4. FblSeedKeyModule

- **UUID**: `2c44ed3f-fa98-42cd-bb0b-fbd7c2f64a27`
- **参数名**: `FblSeedKeyModule`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: With enabling this option, each access to the bootloader's core functionality will require that the ECU is unlocked before. For this purpose, a seed/key mechanism is used which is implemented according to the Ford EESE Diagnostic Programming Security Algorithm (document no. 00.06.15.151).

####### STRING 类型参数

######## 1. FblSecretKey

- **UUID**: `2da31e01-3205-4647-9cb4-8a9217206da2`
- **参数名**: `FblSecretKey`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `0102030405`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
- **描述**: Secret key for the seed/key functionality. This key is ECU specific and must be adapted.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Fbl_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **Fbl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Fbl_Pre**
2. **Fbl_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Fbl_Impl

- **UUID**: `3c5681ce-4d2b-48ec-bd7b-f7e615e37e61`
- **实现名称**: `Fbl_Impl`
- **编程语言**: C
- **软件版本**: 4.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Fbl_Pre

- **UUID**: `07b2f757-d092-4f82-bd2a-05988d681bb0`
- **配置名称**: `Fbl_Pre`
- **定义引用**: `/MICROSAR/Fbl`

### 2. Fbl_Rec

- **UUID**: `19856788-e7d5-4ec1-b7e8-ce87bf4d01ec`
- **配置名称**: `Fbl_Rec`
- **定义引用**: `/MICROSAR/Fbl`
