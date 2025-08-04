# EcuC

## 模块描述

Virtual module to collect ECU Configuration specific / global configuration information.

## 容器列表

### 1. EcucPartitionCollection

**描述**: Collection of Partitions defined for this ECU.

该容器没有参数。

### 2. EcucPartition

**描述**: Definition of one Partition on this ECU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcucPartitionBswModuleExecution
  长名称: ''
  描述: Denotes the main BSW partition. Satellite-BSW modules may also be executed in other
      Partitions.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PartitionCanBeRestarted
  长名称: ''
  描述: Specifies the requirement whether the Partition can be restarted. If set to true all software
      executing in this partition shall be capable of handling a restart.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ASIL
  长名称: ''
  描述: ASIL level of this Partition.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. EcucPduCollection

**描述**: Collection of all Pdu objects flowing through the Com-Stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduIdTypeEnum
  长名称: ''
  描述: The PduIdType is used within the entire AUTOSAR Com Stack except for bus drivers. The size of
      this global type depends on the maximum number of PDUs used within one software module.
      If no software module deals with more PDUs that 256, this type can be set to uint8. If
      at least one software module handles more than 256 PDUs, this type must be set to
      uint16. See AUTOSAR_SWS_CommunicationStackTypes for more details.
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PduLengthTypeEnum
  长名称: ''
  描述: The PduLengthType is used within the entire AUTOSAR Com Stack except for bus drivers. The size
      of this global type depends on the maximum length of PDUs to be sent by an ECU. If no
      segmentation is used the length depends on the maximum payload size of a frame of the
      underlying communication system (for FlexRay maximum size is 255 bytes, therefore
      uint8). If segementation is used it depends on the maximum length of a  segmeneted N-PDU
      (in general uint16 is used). See AUTOSAR_SWS_CommunicationStackTypes for more details.
  默认值: UINT8
  最小值: ''
  最大值: ''
```

### 4. Pdu

**描述**: One Pdu flowing through the COM-Stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DynamicLength
  长名称: ''
  描述: This parameter defines whether the Pdu has dynamic length (true) or not (false). Please note
      that this parameter is only relevant for UserDefinedPdus, UserDefinedIPdus and
      J1939DcmIPdus.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MetaDataLength
  长名称: ''
  描述: Number of additional bytes in PDU data that contain auxiliary information (MetaData) for the
      PDU, e.g. the CAN ID. These bytes are handled as part of the PDU data and increase the
      PDU data length accordingly.
  默认值: ''
  最小值: 1
  最大值: 4
- 
  序号: 3
  名称: PduLength
  长名称: ''
  描述: The maximum used length of the Pdu in bytes.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: J1939Requestable
  长名称: ''
  描述: |
    Specifies whether this PDU can be requested on a J1939 bus using the J1939Rm.
    
    The PDU can be transmitted by COM, the RTE, a CDD, J1939Nm, or J1939Dcm. The configuration of
    J1939Rm for PDUs with J1939Requestable set to TRUE depends strongly on the transmitting module.
    
    RTE: The application receives a callback via service port interface, and triggers one of the
    signals of the requestable PDU according to the requested PGN.
    
    COM: J1939Rm calls Com_TriggerIPduSendWithMetaData for the requestable PDU.
    
    CDD: J1939Rm calls <Cdd>_RequestIndication, the CDD sends the PDU corresponding to the requested
    PGN.
    
    J1939Dcm, J1939Nm: J1939Rm calls <Msn>_RequestIndication to trigger transmission of diagnostic
    messages and the AddressClaimed message.
  默认值: false
  最小值: ''
  最大值: ''
```

### 5. EcucPostBuildVariants

**描述**: Collection of toplevel PostBuildSelectable variants. The PredefinedVariants linked inside this
container will determine how many PostBuildSelectableVariants exist. If this container exist the
name pattern for initialization of BSW modules will be <Mip>_Config_<PredefinedVariant.shortName>.
If this container does not exist the name pattern for initialization of BSW modlues will be
<Mip>_Config.

该容器没有参数。

### 6. EcucVariationResolver

**描述**: Collection of PredefinedVariant elements containing definition of values for SwSystemconst which
shall be applied when resolving the variability during ECU Configuration.

该容器没有参数。

### 7. EcucGeneral

**描述**: Global configuration parameters of the EcuC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CPUType
  长名称: ''
  描述: Register width of the CPU in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ByteOrder
  长名称: ''
  描述: Byte order on memory level.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: BitOrder
  长名称: ''
  描述: Bit order on register level.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: AtomicBitAccessInBitfield
  长名称: ''
  描述: |
    Enables optimization for single bit read and write accesses in bit-fields if the compiler
    creates an atomic access in all cases.
    This is compiler and platform dependent and has to be checked and configured very carefully!
    
    Caution
    Enabling this configuration option requires atomic bit access in bit-fields. This option must
    only be enabled if the before mentioned access type is supported by the hardware, the compiler
    and the used compiler options. Enabling this option without verifying those conditions may lead
    to data consistency issues.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: AtomicVariableAccess
  长名称: ''
  描述: |
    Selection of Bit size for atomic read and write accesses of global variables.
    This configuration switch is compiler and platform dependent and has to be checked and
    configured very carefully!
    
    Caution
    Setting this configuration option to "Atomic16BitAccess" requires atomic access all global 8 Bit
    and 16 Bit variables.
    Setting this configuration option to "Atomic32BitAccess" requires atomic access all global 8
    Bit, 16 Bit and 32 Bit variables.
    Setting this configuration option to "Atomic64BitAccess" requires atomic access all global 8
    Bit, 16 Bit, 32 Bit and 64 Bit variables.
    The optimization must only be enabled if the before mentioned access types are supported by the
    hardware, the compiler and the used compiler options. Enabling the optimization without
    verifying those conditions may lead to data consistency issues.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SizeOfEnum
  长名称: ''
  描述: Size of type enum in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SizeOfInt
  长名称: ''
  描述: Size of type int in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SizeOfROMPointer
  长名称: ''
  描述: Size of ROM pointer in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SizeOfRAMPointer
  长名称: ''
  描述: Size of RAM pointer in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: BitFieldDataType
  长名称: ''
  描述: |
    Defines the data type of a C bit-field.
    The default value is int as defined by MISRA.
    Other values can be used, but the compiler may add padding bits into the bit-field structures.
  默认值: INT
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: StructAlignment
  长名称: ''
  描述: |
    Alignment of struct elements.
    
    Alignment is given in bit:
    N bit means, that the address of each struct element in bit must be a multiple of N.
    
    Auto Alignment:
    In this case, the alignment of each struct element is determined by its natural alignment
    requirements.
    
    Remark:
    The alignment of the overall struct is done automatically and cannot be configured except for
    structs in arrays (see StructInArrayAlignment).
  默认值: Auto
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: ArrayAlignment
  长名称: ''
  描述: |
    Alignment of arrays.
    
    Alignment is given in bit:
    N bit means, that the size and the address of an array in bit must be a multiple of N.
    
    Auto Alignment:
    In this case, the alignment of an array is the same as the alignment of one array element. The
    address and the size of the array must be a multiple of this alignment requirement.
  默认值: Auto
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: StructInArrayAlignment
  长名称: ''
  描述: |
    Alignment of structs in an array.
    
    Alignment is given in bit:
    N bit means, that the size and the address of the struct in bit must be a multiple of N.
    
    Auto Alignment:
    In this case, the alignment of the overall struct is determined by the struct element with the
    most restrictive alignment requirements.
  默认值: Auto
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: DummyFunction
  长名称: ''
  描述: Dummy functions used to avoid NULL pointer entrance in call tables
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: EcuCSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: DummyStatement
  长名称: ''
  描述: Dummy statements used to avoid compiler warnings about e.g. unused parameters
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: DummyStatementKind
  长名称: ''
  描述: Dummy statements used to avoid compiler warnings about e.g. unused parameters.
  默认值: None
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: ConditionalGenerating
  长名称: ''
  描述: If enabled, only the files are written to the output directory which are changed in their
      content. As a result the time stamps will only be updated if changes have been made.
      Enabling this feature will result in a reduced compile time. Disable the feature if all
      files shall be updated with the generation step.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: EcucBswImplementationCodeType
  长名称: ''
  描述: |
    Defines the realization type of MICROSAR BSW modules with Service-SWC APIs at the point in time
    when the RTE is build:
    - Source Code: All BSW modules with Service SWC interfaces are available as Source Code. This
    option shall be used by default as it allows the RTE to generate optimized code.
    - Library: Some or all BSW modules with Service SWC interface are available as library only.
    This option requires the RTE to disable some optimization strategies.
  默认值: EcuCSourceCode
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: EcuCUseStdReturnTypeForRte
  长名称: ''
  描述: Defines whether the Std_ReturnType is used for RTE.
  默认值: false
  最小值: ''
  最大值: ''
```

### 8. PostbuildLoadable

**描述**: Post-Build Loadable specific settings.

#### 参数列表

```yaml
- 
  序号: 1
  名称: AlignmentFillPattern
  长名称: ''
  描述: Alignment Fill Pattern. Byte pattern which is used for the inserted padding bytes.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: PBROMStartAddress
  长名称: Post-Build ROM Start Address
  描述: Start address of post-build ROM data. The defined memory are is used globally for all modules
      excluding these defined as IndividualPostBuildLoadableModule.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: PBRAMStartAddress
  长名称: Post-Build RAM Start Address
  描述: Start address of post-build RAM data (flexible RAM management). The defined memory are is used
      globally for all modules excluding these defined as IndividualPostBuildLoadableModule.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: PBROMEndAddress
  长名称: Post-Build ROM End Address
  描述: End address of available ROM for post-build. The defined memory are is used globally for all
      modules excluding these defined as IndividualPostBuildLoadableModule.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: PBRAMEndAddress
  长名称: Post-Build RAM End Address
  描述: End address of available RAM for post-build. The defined memory are is used globally for all
      modules excluding these defined as IndividualPostBuildLoadableModule.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 9. IndividualPostBuildLoadableModule

**描述**: Modules that shall be updated individually need to be configured here. For each module a dedicated
Post-Build ROM and RAM memory are need to be defined. Modules that are updated individually must not
be part of the global root structure. For each module defined here an individual Hex file will be
created.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ModulePBROMStartAddress
  长名称: Module Specific Post-Build ROM Start Address
  描述: Start address of post-build ROM data.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: ModulePBRAMStartAddress
  长名称: Module Specific Post-Build RAM Start Address
  描述: Start address of post-build RAM data (flexible RAM management).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: ModulePBROMEndAddress
  长名称: Module Specific Post-Build ROM End Address
  描述: End address of available ROM for post-build.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: ModulePBRAMEndAddress
  长名称: Module Specific Post-Build RAM End Address
  描述: End address of available RAM for post-build.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 10. ModuleInitializationStructure

**描述**: Defines the name of the module initialzation structure(s) used for BSW initialization. Projects not
using post-build selectable have one initialization structure. For these projects the parameter
ModuleInitStructureStartAddress need not to be configured as the address is equal to the configured
ModulePBROMStartAddress.
Projects using selectable post-build have for each module multiple module intialization structures
(one for each identity). For each identity one ModuleInitializationStructure container shall be
defined. For each container the ModuleInitStructureStartAddress must be configured according to the
location of that structure in ROM. All module initialization structures shall be located sequently
directly after ModulePBROMStartAddress.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ModuleInitStructureStartAddress
  长名称: ''
  描述: |
    Relevant for post-build selectable projects with multiple module initialization structures.
    The indicated addresses must follow directly after the PBROMStartAddress. There may be gaps
    
     If there is only a single initialization structure this container is not relevant as the start
    address must be equal to PBROMStartAddress.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 11. GlobalInitializationStructure

**描述**: Defines the name of the global root structure(s) used for BSW initialization. Projects not using
post-build selectable have one initialization structure. For these projects the parameter
GlobalRootStructureStartAddress need not to be configured as the address is equal to the configured
PBROMStartAddress.
Projects using selectable post-build have multiple global root structures (one for each identity).
For each identity one GlobalInitializationStructure container shall be defined. For each container
the GlobalRootStructureStartAddress must be configured according to the location of that structure
in ROM. All global root structures shall be located sequently directly after PBROMStartAddress.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GlobalRootStructureStartAddress
  长名称: ''
  描述: Start address of post-build ROM data.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 12. BswInitialization

**描述**: Contains all functions

该容器没有参数。

### 13. InitFunction

**描述**: Name of the init function.

E.g. ComM_Init

#### 参数列表

```yaml
- 
  序号: 1
  名称: Header
  长名称: ''
  描述: Header which declares function and types.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ConfigType
  长名称: ''
  描述: Name of ConfigType
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ConfigPtrName
  长名称: ''
  描述: Name of Config Pointer which shall be passed to function. If Empty no parameter is passed. If
      Init Function has a pointer, at least a NULL_PTR should be inserted here.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ConfigPtrClass
  长名称: ''
  描述: Memory class of Config Pointer.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: InitPhase
  长名称: ''
  描述: Phase in which this init function shall be called.
  默认值: INIT_TWO_POST_NVMREADALL
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: AdditionalInitCode
  长名称: ''
  描述: |
    Specify additional code which can be referenced from the initialization callouts of EcuM and
    BswM.
    
    E.g.: Mcu_InitClock()
    
    If it is necessary to call a function with a module pointer from the global postbuild-loadable
    configuration, the placeholder %CONFIGPTR% can be used:
    
    E.g.: Mcu_Init(%CONFIGPTR%)
  默认值: ''
  最小值: ''
  最大值: ''
```

### 14. InterruptFunctionality

**描述**: Global interrupt configuration for Mcs12 .

#### 参数列表

```yaml
- 
  序号: 1
  名称: GlobalReEnableCat1
  长名称: ''
  描述: |
    Mcs12 specific parameter. It shall contain a c-Code instruction that re-enables Irqs in
    interrupt context, to allow nested interrupts of different sources with higher priority. This
    code is mostly an inline assembler instruction and therefore Compiler specific. It is
    used in case that a driver interrupt is configured as category 1.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GlobalReEnableCat2
  长名称: ''
  描述: |
    Mcs12 specific parameter. It shall contain a c-Code instruction that re-enables Irqs in
    interrupt context, to allow nested interrupts of different sources with higher priority. This
    code is mostly an inline assembler instruction and therefore Compiler specific. It is
    used in case that a driver interrupt is configured as category 2.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 15. EcucHardware

**描述**: Hardware definition of this Ecu.

该容器没有参数。

### 16. EcucCoreDefinition

**描述**: Definition of one Core on this Ecu.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EcucCoreId
  长名称: ''
  描述: ID of the core.
  默认值: 0
  最小值: 0
  最大值: 65535
```

