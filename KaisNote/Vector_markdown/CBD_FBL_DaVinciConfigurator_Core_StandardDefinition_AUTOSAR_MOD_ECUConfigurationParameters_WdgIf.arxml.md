# WdgIf

## 模块描述

Configuration of the WdgIf (Watchdog Interface) module.

## 容器列表

### 1. WdgIfDevice

**描述**: It contains the information for the selection of a particular Watchdog device in case multiple
Watchdog drivers are connected.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgIfDeviceIndex
  长名称: ''
  描述: Represents the watchdog interface ID so that it can be referenced by the watchdog manager.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 2. WdgIfGeneral

**描述**: This container collects all generic watchdog interface parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgIfDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling the development error detection and reporting.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: WdgIfVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the service returning the version information.
  默认值: ''
  最小值: ''
  最大值: ''
```

