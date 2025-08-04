# vHsmUpd

## 模块描述

Configuration of the vHsmUpd (Hsm Updater) module.

## 容器列表

### 1. vHsmUpdGeneral

**描述**: General configuration parameters of the vHsmUpd.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmUpdRetryCounter
  长名称: ''
  描述: This value defines the maximal number of retries the vHsmUpd does, before an error callout
      gets called.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: vHsmUpdEnableUserCompareMechanism
  长名称: ''
  描述: |
    This parameter defines whether a user defined compare mechanism of the vHsm firmware is
    implemented.
    
    The vHsmUpd normally decides whether an update of the vHsm firmware is necessary by comparing
    the given values by size.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vHsmUpdDecryptionRamBufferSize
  长名称: ''
  描述: |
    This value defines the size for the decryption buffer which is used for decrypting the update
    image. A greater value could speed up the update process but leads to more memory consumption in
    RAM.
    
    There are three restrictions regarding this value:
        1) The size must be a multiple of 16Bytes.
        2) The size must be a multiple of the code flash page size.
        3) The update image size shall be at least equal to the configured value.
    
  默认值: 256
  最小值: 16
  最大值: 65535
```

### 2. vHsmUpdUpdateHeaderFixAddress

**描述**: Exactly two header locations must be specified when using this choice. Location_A will be parsed and
only if no valid header is found here, the second Location_B will be processed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmUpdHeaderLocation_A
  长名称: ''
  描述: This value specifies the physical flash address where an update header is located. The address
      to configure here is the address of the presence pattern and not the first content of
      the update header.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vHsmUpdHeaderLocation_B
  长名称: ''
  描述: This value specifies the physical flash address where an update header is located. The address
      to configure here is the address of the presence pattern and not the first content of
      the update header.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 3. vHsmUpdUpdateHeaderVariableAddress

**描述**: Define a start address and the number of locations to search for an update header when using this
choice. vHsmUpd searches these locations until the first valid update header is found.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmUpdFirstHeaderAddress
  长名称: ''
  描述: This value specifies the physical flash address where an update header is located. The address
      to configure here is the address of the presence pattern and not the first content of
      the update header.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vHsmUpdNumberOfPossibleHeaders
  长名称: ''
  描述: |
    This value specifies the number of locations to search for the update header. vHsmUpd expects
    all header locations to be aligned to page size of the hardware. The next address to search for
    the update header will be calculated as the size of the update header is known.
    
    Therefore, the update header area shall not contain any gaps, but lie sequentially in flash
    memory.
  默认值: 1
  最小值: 1
  最大值: 4294967295
```

### 4. vHsmUpdIpc

**描述**: Configuration parameters for the Ipc-Communication, i.e. the communcation with the host core.

The communication takes place in both directions, i.e. both the Host and the HSM write information
for the other. Therefore, two required areas have to be configured --- vHsmUpdIpcHsmToHost and
vHsmUpdIpcHostToHsm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmUpdIpcBaseAddress
  长名称: ''
  描述: |
    This value specifies the address, which is used by the vHsmUpd to communicate with the Host
    application. The address must be writeable by the vHsmUpd (shall be located within RAM) and
    should be readable by the Host. Just one byte is used.
    
    Hardware restrictions regarding the address must be respected by the user.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vHsmUpdIpcHsmToHost
  长名称: ''
  描述: |
    This value specifies the address, which is used by the HSM to communicate with the Host
    application. The address must be writable by the HSM and readable by the Host application. The
    vHsmUpd has to be able to evaluate this address and clear it.
    
    vHsmUpdIpcHsmToHost specifies a 4 byte writable address.
    
    Hardware restrictions regarding the address must be respected by the user.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vHsmUpdIpcHostToHsm
  长名称: ''
  描述: |
    This value specifies the address, which is used by the Host application to communicate with the
    HSM. The address must be writable by the Host application and readable by the HSM. The vHsmUpd
    has to be able to evaluate this address.
    
    vHsmUpdIpcHostToHsm specifies a 4 byte writable address.
    
    Hardware restrictions regarding the address must be respected by the user.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vHsmUpdIpcWaitMask
  长名称: ''
  描述: |
    This mask value shall be written to the area specified by vHsmUpdIpcHostToHsm.
    
    The vHsmUpd polls this value to get the current state of the Host. If the value is written, the
    vHsmUpd assumes the Host to be ready for an update.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

