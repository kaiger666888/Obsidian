# ResourceM

## 模块描述

Configuration of RM (Resource Manager) module.

## 容器列表

### 1. ResourceMMcalConfig

**描述**: General container to select Master Core and allocate resources

#### 参数列表

```yaml
- 
  序号: 1
  名称: ResourceMMasterCore
  长名称: ''
  描述: Select Master core.
  默认值: CORE0
  最小值: ''
  最大值: ''
```

### 2. ResourceMMcalCore

**描述**: General container to allocate Mcal resources to cores

#### 参数列表

```yaml
- 
  序号: 1
  名称: ResourceMCoreID
  长名称: ''
  描述: Select Master core.
  默认值: CORE0
  最小值: ''
  最大值: ''
```

### 3. ResourceMAllocation

**描述**: Container to allocate module resources.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ResourceMModuleName
  长名称: ''
  描述: Module name.
  默认值: ADC
  最小值: ''
  最大值: ''
```

