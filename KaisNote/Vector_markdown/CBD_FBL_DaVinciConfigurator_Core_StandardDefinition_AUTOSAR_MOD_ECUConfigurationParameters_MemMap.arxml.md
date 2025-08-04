# MemMap

## 模块描述

Configuration of the MemMap module.

## 容器列表

### 1. MemMapAddressingModeSet

**描述**: Defines a set of addressing modes which might apply to a SwAddrMethod.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemMapSupportedAddressingMethodOption
  长名称: ''
  描述: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MemMapSupportedMemoryAllocationKeywordPolicy
  长名称: ''
  描述: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: MemMapSupportedSectionInitializationPolicy
  长名称: ''
  描述: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: MemMapSupportedSectionType
  长名称: ''
  描述: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. MemMapAddressingMode

**描述**: Defines a addressing mode with a set of #pragma statements implementing the start and the stop of a
section.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemMapAddressingModeStart
  长名称: ''
  描述: Defines a set of #pragma statements implementing the start of a section.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MemMapAddressingModeStop
  长名称: ''
  描述: Defines a set of #pragma statements implementing the start of a section.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: MemMapAlignmentSelector
  长名称: ''
  描述: Defines a the alignments for which the MemMapAddressingMode applies.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. MemMapAllocation

**描述**: Defines a set of addressing modes which might apply to a SwAddrMethod.

该容器没有参数。

### 4. MemMapGenericMapping

**描述**: Defines which SwAddrMethod is implemented with which MemMapAddressingModeSet.

该容器没有参数。

### 5. MemMapSectionSpecificMapping

**描述**: Defines which MemorySection of a BSW Module or a Software Component is implemented with which
MemMapAddressingModeSet.

该容器没有参数。

