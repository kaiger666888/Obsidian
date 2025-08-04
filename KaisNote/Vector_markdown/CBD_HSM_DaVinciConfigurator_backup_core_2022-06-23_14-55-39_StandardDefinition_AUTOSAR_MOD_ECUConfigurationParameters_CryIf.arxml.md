# CryIf

## 模块描述

Configuration of the Crypto Interface.

## 容器列表

### 1. CryIfChannel

**描述**: Container for incorporation of CryIfChannel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryIfChannelId
  长名称: ''
  描述: Identifier of the crypto channel 
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 2. CryIfGeneral

**描述**: Container for common configuration options.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryIfDevErrorDetect
  长名称: ''
  描述: |
    Switches the development error detection and notification on or off.
      true: detection and notification is enabled.
      false: detection and notification is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CryIfVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable and disable availability of the API CryIf_GetVersionInfo().
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. CryIfKey

**描述**: Container for Channel configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: CryIfKeyId
  长名称: ''
  描述: Identifier of the key. 
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

