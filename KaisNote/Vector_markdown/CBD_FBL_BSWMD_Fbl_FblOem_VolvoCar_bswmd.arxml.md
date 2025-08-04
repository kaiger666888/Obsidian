# Fbl

## 模块描述

Configuration of the Fbl (Flash Bootloader) module.

## 容器列表

### 1. FblGeneral

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblUserConfigFile
  长名称: ''
  描述: |
    FBL: If a file path is specified, the file is read and its contents are put at the end of the
    FBL config file.
    
    DEM: Path to an external user configuration file used by the "Configurator 5" generation tool.
    
    If you want to overwrite some of the settings in the generated configuration file (Dem_Cfg.h),
    you can specify a path to a user defined configuration file. The user defined configuration file
    will be included at the end of the generated preprocessor switches. Definitions in the user
    defined configuration file can overwrite definitions in the generated configuration file.
    
    To specify the file name, you can use "$(var)" sequence(s) in the specified path. Each such
    sequence is replaced by the content of the related environment variable "var".
    Additionally you can use following predefined sequences:
    $(DpaProjectFolder) Absolute directory of the loaded *.dpa file.
    $(EcuProjectName) Name of the project defined in the loaded *.dpa file.
    $(EcucFile) Absolute directory "ECUC", defined by the loaded *.dpa file, containing files
    $(EcuProjectName).ecuc.arxml and $(EcuProjectName).ecuc.Initial.arxml .
    $(EcucFolder) Parent directory of $(EcucFile).
    $(SipRootPath) Absolute directory "SIP", defined by the loaded *.dpa file.
    $(OutputFolder) (Relative) directory "GenData", defined by the loaded *.dpa file. See setting
    "Root Target Folder" of Configurator 5.
    $(ServiceSwcFolder) Absolute directory "ServiceComponents", defined by the loaded *.dpa file.
    $(cwd) Current working directory when starting Configurator 5.
    
    RESTRICTIONS: Not all of the settings can be overwritten simply by triggering the preprocessor
    switch. Some of the options are complex and the code generator generates less or more code
    depending on the setting.
    
    USE SUCH A FILE ONLY AFTER DISCUSSION WITH VECTOR.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FblProjectState
  长名称: ''
  描述: |
    Code that is required for integration/development is automatically removed once the production
    state is configured. Test FBL_PROJECT_STATE for FBL_INTEGRATION / FBL_PRODUCTION to use this for
    your own code. Bootloader internal checks are configured according to the current project state:
    
    ~~~ Integration ~~~
    Choose this state during development/integration of your integration project.
    This configuration adds internal configuration and user code checks and hence helps you to find
    configuration errors easily. Errors found will trigger the callback ApplFblFatalError(). A user
    specific error handling can be added, e.g. flashing Led if no debugger is available (default:
    while(1){;});
    
    ~~~ Production (default) ~~~
    Choose this state when ready for production.
    Configuration checks are turned off.
    
    ~~~ Production (reduced checks) ~~~
    Choose this state when ready for production and if you need to minimize code size.
    Some additional checks will also be disabled in order to reduce code size. The resulting
    configuration reports NRCs on runtime errors late. This will make it more difficult to analyze
    errors that occur on production ECUs. It is therefore recommended to configure "Production
    (default)" if possible.
  默认值: INTEGRATION
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FblStayInBoot
  长名称: ''
  描述: If activated the FBL waits a specified time before jumping to a valid application. If a
      special message is received within this time the FBL stays active. This feature is
      designed for development phase to avoid reflashing the FBL if the application doesn't
      work properly.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FblMaximumNumberOfSegments
  长名称: ''
  描述: The download of an application can be separated in several segments depending on the linker
      settings. To store the addresses and lengths of these segments, the FBL uses an array.
      Enter the maximum number of address segments here.
  默认值: 1
  最小值: 1
  最大值: ''
- 
  序号: 5
  名称: FblSleepMode
  长名称: ''
  描述: Enable sleep mode/power down support for FBL.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FblSleepTime
  长名称: ''
  描述: If the sleep mode is enabled and the diagnostic layer does not receive a diagnostic request
      for the period of time specified with this attribute then the function
      fbl_ap.c::ApplFblBusSleep() is called.
  默认值: 60000
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: FblApplicationTimerTask
  长名称: ''
  描述: |
    If this option is enabled, the bootloader provides function fbl_ap.c::ApplFblTask(). You can add
    user specific code to this function which will be called cyclically by the bootloader. The
    actual call cycle is derived from GENy attribute FblTp_Iso/TP call cycle.
    
    Note: The task function won't be called during diagnostic service processing.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FblHeaderAddress
  长名称: ''
  描述: |
    This is the start address of the bootloader's FblHeader structure (defined in module
    fbl_main.c). The bootloader header can be located at an arbitrary address using the provided
    section #pragma instructions.
    
    CAUTION:
    If the application software uses the FblStart mechanism to enter the bootloader, you have to
    update fbl_cfg.h on change of the FBL header address!
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 9
  名称: FblDiagnosticBufferSize
  长名称: ''
  描述: This is the size of the RAM buffer which is used to store diagnostic request/response
      messages. Usually, the download performance will benefit from choosing bigger buffer
      sizes. The maximum usable buffer size depends on the underlying transport protocol.
  默认值: 255
  最小值: 0
  最大值: ''
- 
  序号: 10
  名称: FblP2Server
  长名称: ''
  描述: Specify the P2 diagnostic timeout here. The FBL will always send a response, before P2
      expires.
  默认值: 50
  最小值: 0
  最大值: ''
- 
  序号: 11
  名称: FblP2StarServer
  长名称: P2* Server
  描述: P2* diagnostic response pending time. The FBL will send response pending messages while
      processing long-lasting service requests. Use this option to configure the response
      pending timing.
  默认值: 5000
  最小值: 0
  最大值: ''
- 
  序号: 12
  名称: FblS3ServerExtendedSession
  长名称: ''
  描述: Specifiy the S3 diagnostic timeout for the extended session here. Time for the FBL to keep the
      extended diagnostic session active while not receiving any diagnostic request message.
  默认值: 5000
  最小值: 0
  最大值: ''
- 
  序号: 13
  名称: FblS3ServerProgrammingSession
  长名称: ''
  描述: Specify the S3 diagnostic timeout for the programming session here. Time for the FBL to keep
      the programming diagnostic session active while not receiving any diagnostic request
      message.
  默认值: 5000
  最小值: 0
  最大值: ''
- 
  序号: 14
  名称: FblGapFilling
  长名称: ''
  描述: If this option is enabled, the bootloader will fill any gaps in the download file (Flashware)
      with the value of the Fill code attribute.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: FblFillCode
  长名称: ''
  描述: The gaps between two download segments will be filled with the specified byte code. It's
      recommended to use an illegal opcode according to the used hardware platform.
  默认值: 255
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: FblInternalMemoryCopy
  长名称: ''
  描述: If enabled, the bootloader will use an internal memory copy function instead of the library
      memcpy() function of the compiler vendor.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: FblGatewaySupport
  长名称: ''
  描述: |
    This option is used for bootloaders that are connected to multiple CAN networks and contains a
    gateway support feature.
    It controls if the bootloader shall support or not the gateway feature. The gateway feature
    routes messages from a main network to one or more sub networks, depending on the feature of the
    gateway support in the bootloader.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: FblPresencePattern
  长名称: ''
  描述: Logical blocks and/or application validation is checked using presence patterns at the end of
      each logical block. If this option is used, the decision if an application is available
      can be made without loading a memory driver (e.g. Eeprom Emulation or external Eeprom).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: FblStartFunction
  长名称: ''
  描述: |
    This option provides a user-friendly way to start the bootloader from within the application by
    using the macro CallFblStart().
    
    PRECONDITIONS:
    - The FblHeader address is configured correctly (see GENy component FblDrvCan_*).
    - The application module which uses CallFblStart() includes fbl_def.h (fbl_cfg.h has to be
    provided, too). Remember to update fbl_cfg.h if the address of FblHeader changes!
    
    By disabling this option, the user can gain more influence on how the transition from
    application to bootloader is done.
    This is the procedure which has to be followed:
    - Set a flag in the application software
    - Issue a reset
    - Check flag in user adaptable function fbl_apnv.c::ApplFblExtProgRequest() and provide the
    appropriate return value.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: FblCommonData
  长名称: ''
  描述: |
    By enabling this option, the bootloader provides an interface to access (constant) data which is
    linked with the bootloader. This enables the application software to read e.g. DID values from
    the same memory location as the bootloader. In particular, this is useful for DIDs that report
    hardware specific information which doesn't change if the application software is updated.
    The structure of the common data is completely user specific and can be declared in file
    comdat.h. The actual structure definition is usually located in file fbl_ap.c. The bootloader
    stores the address of this structure in the FblHeader. The respective value can be retrieved by
    using macro GetFblCommonDataPtr().
    To access the common data via GetFblCommonDataPtr(), the application software has to include the
    files fbl_def.h (which itself needs fbl_cfg.h) and comdat.h.
    For more detailed usage information, please refer to the respective technical reference.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: FblResponseAfterReset
  长名称: ''
  描述: |
    Send the response to a default session request or a reset request after the ECU has been reset.
    
    Before the reset, a response pending message is sent by the Bootloader. The actual response has
    to be sent by the application software or the Bootloader depending on a flag set in
    non-initialized memory.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: FblUserSubfunction
  长名称: ''
  描述: |
    This option can be activated if user specific subfunction parameters have to be supported which
    are not defined within the OEM specification.
    If the bootloader receives a request with a supported service identifier and an unknown
    subfunction parameter, the user adaptable function fbl_apdi.c::ApplDiagUserSubFunction() will be
    called.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: FblUserService
  长名称: ''
  描述: |
    This option can be activated if user specific diagnostic services have to be supported which are
    not defined within the OEM specification.
    If the bootloader receives a request with an unsupported service identifier, the user adaptable
    function fbl_apdi.c::ApplDiagUserService() will be called.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: FblUserRoutine
  长名称: ''
  描述: |
    This option can be activated if user specific diagnostic routines have to be supported which are
    not defined within the OEM specification.
    If the bootloader receives a request with an unsupported routine ID, the user adaptable function
    fbl_apdi.c::ApplDiagRoutineControl() will be called.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: FblWatchdogService
  长名称: ''
  描述: If this option is enabled, the bootloader provides an API for watchdog service handling. User
      specific watchdog service code can be added to function fbl_apwd.c::ApplFblWDTrigger().
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: FblWatchdogTriggerCycle
  长名称: ''
  描述: If the watchdog service is enabled, the bootloader will call user function
      fbl_apwd.c::ApplFblWDTrigger() with the specified cycle time.
  默认值: 1
  最小值: 1
  最大值: ''
- 
  序号: 27
  名称: FblEncryptionMode
  长名称: ''
  描述: Enabling this option allows for transmission of encrypted data. The data which is received by
      the bootloader will be decrypted by means of a dedicated decryption module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: FblCompressionMode
  长名称: ''
  描述: Enabling this option allows for transmission of compressed data. The data which is received by
      the bootloader will be decompressed by means of a dedicated compression module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: FblDataProcessingBufferSize
  长名称: ''
  描述: Defines the maximum output buffer size available for handling of preprocessed data, e.g.
      decryption or decompression.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 30
  名称: FblInputVerification
  长名称: ''
  描述: |
    If enabled the signature verification will take the downloaded data instead of the data written
    to non-volatile memory (e.g. flash) as input.
    The transferred data is passed to the hash/checksum calculation before any data processing takes
    place. E.g. if compressed data is downloaded the signature is calculated over the compressed
    data and not the uncompressed contents actually written to flash.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: FblProcessedVerification
  长名称: ''
  描述: ''
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 32
  名称: FblPipelinedVerification
  长名称: ''
  描述: ''
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 33
  名称: FblOutputVerification
  长名称: ''
  描述: ''
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 34
  名称: FblVerificationSegmentation
  长名称: ''
  描述: Defines the maximum data length passed to the on-the-fly verification in a single processing
      cycle.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 35
  名称: FblAdaptiveDataTransferRcrrp
  长名称: ''
  描述: |
    Disable to force the transmission of the first RCR-RP (Response Pending) message before starting
    processing of the download data.
    If enabled the first RCR-RP will be conditionally send based on the P2 timeout. Requires that a
    single program operation takes less than P2!
    Programming time depends on "Write segmentation" and/or "Data processing buffer size"
    Also applies to times required by on-the-fly signature verification and data processing.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 36
  名称: FblPipelinedProgramming
  长名称: ''
  描述: With this feature enabled, the FBL immediately sends a positive response after the reception
      of a TransferData request, so that the next data transfer can be performed while the
      previous data block is programmed. The same parallelization applies to the signature
      calculation over the transfer data in RAM and the decompression/decryption of the
      received data. In best case only the pure transmission time is required.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 37
  名称: FblSuspendDriverOperation
  长名称: ''
  描述: Memory driver can be suspended in mid-operation by external event.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 38
  名称: FblWriteSegmentation
  长名称: ''
  描述: |
    Defines the maximum data length passed to the programming routine in a single processing cycle.
    Used for options "Adaptive RCR-RP for TransferData service" and "Pipelined programming".
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 39
  名称: FblUnalignedDataTransfer
  长名称: ''
  描述: |
    If enabled the data transferred during download using the TransferData service can be of
    arbitrary length.
    Otherwise all data transfers have to be aligned to a multiple of the largest memory write
    segment size.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 40
  名称: FblVerificationFunction
  长名称: ''
  描述: Add support for Driver_VerifySync
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 41
  名称: FblFlashDriverUsage
  长名称: ''
  描述: |
    Configures the source of the flash driver RAM image.
    
    Download Driver: Flash Driver is downloaded to the ECU.
    Use Flash Driver from ROM: Flash Driver is stored in an encrypted ROM image in the bootloader’s
    flash memory and copied to RAM before initialization.
    Optional Flash Driver Download: Flash Driver can be downloaded to the ECU. If it isn’t
    downloaded, the flash driver from an internal image will be used.
    
    Please note: Depending on your OEM’s requirements, not all of these options may be available in
    the embedded bootloader implementation.
    
  默认值: DOWNLOAD_DRIVER
  最小值: ''
  最大值: ''
- 
  序号: 42
  名称: FblApplicationStateTask
  长名称: ''
  描述: |
    If this option is enabled, the bootloader provides function fbl_ap.c::ApplFblStateTask(). You
    can add user specific code to this function which will be called as a background task by the
    bootloader.
    
    Note: The task function won't be called during diagnostic service processing.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 43
  名称: FblReprogrammableLbt
  长名称: Reprogrammable LBT
  描述: Enable support for post-build update of the Logical Block Table. If this option is enabled,
      the generated Fbl_Lbt.c/Fbl_Lbt.h files will only contain the SBL and LBT blocks. The
      full version of the LBT will be generated into the files
      Fbl_Lbt_PBcfg.c/Fbl_Lbt_PBcfg.h.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 44
  名称: FblMaximumAmountOfLogicalBlocks
  长名称: ''
  描述: |
    This is the maximum number of logical blocks which can be handled by the bootloader. For the
    configuration of this value, please consider potential growth of the LBT in the future. After
    the bootloader has been programmed into the ECU, it’s not possible to download an LBT where the
    number of blocks exceeds the configured value.
    
    Note: The parameter is only considered if FblReprogrammableLbt is enabled.
  默认值: 8
  最小值: 0
  最大值: 254
- 
  序号: 45
  名称: FblBlockStartAddress
  长名称: FBL Block Start Address
  描述: Start address of the FBL block.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 46
  名称: FblBlockLength
  长名称: FBL Block Length
  描述: Length of the FBL block in bytes.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 47
  名称: FblOta
  长名称: OTA functionality
  描述: Enables support for Over The Air update functionality in the Bootloader. To be used with an
      application stack that supports OTA.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 48
  名称: FblOneStepUpdater
  长名称: One Step Updater
  描述: Enables/disables the one step updater. In case it is enabled, the Updater as well as the
      Application/Data is downloaded in one flashing process. This means that the Updater is
      started after it was downloaded.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 49
  名称: FblHardwareSwap
  长名称: ''
  描述: Specify if the hardware swap should be used.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. FblFlashBlockTable

该容器没有参数。

### 3. FblFlashBlock

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblFbStartAddress
  长名称: 01 Start Address
  描述: Start address of the flash block.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: FblFbEndAddress
  长名称: 02 End Address
  描述: End address of the flash block.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FblFbDescription
  长名称: 05 Description
  描述: A short description of the flash block.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. FblLogicalBlockTable

该容器没有参数。

### 5. FblLogicalBlock

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblLbBlockIndex
  长名称: 01 Block Index
  描述: ''
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: FblLbBlockType
  长名称: 02 BlockType
  描述: ''
  默认值: CODE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FblLbDisposability
  长名称: 03 Disposability
  描述: ''
  默认值: MANDATORY
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FblLbStartAddress
  长名称: 04 Start Address
  描述: Start address of the logical block. This value is computed automatically.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: FblLbEndAddress
  长名称: 05 End Address
  描述: End address of the logical block. This value is computed automatically.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: FblLbHeaderAddress
  长名称: 06 Header Address
  描述: ''
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: FblLbOutputVerification
  长名称: 13 Output Verification
  描述: |
    Verification function used for output verification. The interface of the provided function has
    to be compatible with the prototype of SecM_Verification.
    
    When "Output Verification" is enabled, this function verification will take the data written to
    non-volatile memory (e.g. flash) as input.
    The processing will be performed on the written contents, after the complete data was
    transferred and programmed.
    
    In some use cases it might be useful to call an alternative user-specific function for a logical
    block. E.g. if you like to avoid read back of the written data from a slave processor in a
    multi-processor configuration. This function could pass the request including the necessary
    information to the slave controller. Calculation is then carried out on the slave controller and
    the result is passed back to the master controller.
    
    Set to "0" to disable output verification for this particular block. Caution: In this case the
    Bootloader will accept any signature/checksum, regardless of the previously downloaded data!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FblLbDescription
  长名称: 14 Description
  描述: Short description of this Logical Block
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FblLbBmHeaderAddress
  长名称: 07 BM Header Address
  描述: Header address of the BootManager. The value has to be within the start and end address of the
      logical block.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 6. FblMemoryDeviceTable

该容器没有参数。

### 7. FblMemoryDevice

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblMdIndex
  长名称: 01 Device Index
  描述: This value specifies the unique index of the memory device.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: FblMdSegmentSize
  长名称: 02 Segment Size
  描述: Write segment size of memory device. The write segment size is the smallest entity that can be
      programmed in one write access. Refer to the memory device specification for this value.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: FblMdErasedValue
  长名称: 03 Erased Value
  描述: Erased value of the memory device. The erased value is the memory content after the memory was
      erased. Refer to the memory device specification for this value.
  默认值: 255
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: FblMdInitHook
  长名称: 04 Init Hook
  描述: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the init
      function is called.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FblMdDeinitHook
  长名称: 05 Deinit Hook
  描述: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the
      deinit function is called.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FblMdReadHook
  长名称: 06 Read Hook
  描述: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the read
      function is called.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FblMdEraseHook
  长名称: 07 Erase Hook
  描述: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the erase
      function is called.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FblMdWriteHook
  长名称: 08 Write Hook
  描述: Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the write
      function is called.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FblMdVerifyHook
  长名称: 09 Verify Hook
  描述: |
    Enables a callout hook before (ApplFblPreMemDriver) and after (ApplFblPostMemDriver) the verify
    function is called.
    
    Note: Only applicable for certain platforms, e.g. RL78
  默认值: false
  最小值: ''
  最大值: ''
```

### 8. FblVolvoCar

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblWriteDataByIdentifierService
  长名称: ''
  描述: |
    If activated, the optional diagnostic service WriteDataByIdentifier (0x2E) will be provided.
    Turn the option off to reduce the bootloader code size or if the service shall not be supported.
    
    Note: Customer specific data identifiers can be added to user adaptable function
    fbl_apdi.c::ApplFblWriteDataByIdentifier().
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FblRequestUploadService
  长名称: ''
  描述: If activated, the optional diagnostic service RequestUpload (0x35) will be provided. Turn the
      option off to reduce the bootloader code size or if the service shall not be supported.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FblMaximumReadableDIDs
  长名称: ''
  描述: |
    This attribute defines the maximum number of data identifiers which can be handled by the
    bootloader in a single ReadDataByIdentifier request. The specified value is used to allocate a
    RAM buffer which will keep the DIDs which have been extracted from the diag buffer.
    If the specified maximum number is exceeded, the bootloader will respond with NRC 0x13
    (IncorrectMessageLengthOrInvalidFormat).
  默认值: 5
  最小值: 5
  最大值: 255
- 
  序号: 4
  名称: FblFlashErasedDetection
  长名称: ''
  描述: |
    The flash erased detection feature provides the possibility to check whether the flash memory is
    already erased or not. The intention is to reduce the overall download time of the initial ECU
    programming process at end-of-line.
    
    CAUTION: This feature is subject to certain restrictions which have to be considered before
    activation. Please consult the technical reference for further information!
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FblSeedKeyModule
  长名称: ''
  描述: With enabling this option, each access to the bootloader's core functionality will require
      that the ECU is unlocked before. For this purpose, a seed/key mechanism is used which is
      implemented according to the Ford EESE Diagnostic Programming Security Algorithm
      (document no. 00.06.15.151).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FblSecretKey
  长名称: ''
  描述: Secret key for the seed/key functionality. This key is ECU specific and must be adapted.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FblCompleteAndCompatibleBlockAddress
  长名称: Complete & Compatible Block Address
  描述: This value defines the memory address where the complete & compatible block will be stored.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

