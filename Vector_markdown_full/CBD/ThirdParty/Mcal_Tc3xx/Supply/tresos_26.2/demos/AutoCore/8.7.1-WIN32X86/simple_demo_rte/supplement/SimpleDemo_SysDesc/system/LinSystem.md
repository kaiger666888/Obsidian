# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:46

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3_STRICT_COMPACT.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **7** 个包：

### 1. LinSystem

- **包名称**: `LinSystem`
- **包含元素数量**: 1

#### 包含的元素

##### SYSTEM 类型元素

1. **LinSystem**

### 2. CLUSTERS

- **包名称**: `CLUSTERS`
- **包含元素数量**: 1

#### 包含的元素

##### LIN-CLUSTER 类型元素

1. **LinNetwork**

### 3. ECUINSTANCES

- **包名称**: `ECUINSTANCES`
- **包含元素数量**: 2

#### 包含的元素

##### ECU-INSTANCE 类型元素

1. **DebugNode**
2. **EcuTestNode**

### 4. SYSSIGNALS

- **包名称**: `SYSSIGNALS`
- **包含元素数量**: 2

#### 包含的元素

##### SYSTEM-SIGNAL 类型元素

1. **CounterIn**
2. **CounterOut**

### 5. FRAMES

- **包名称**: `FRAMES`
- **包含元素数量**: 2

#### 包含的元素

##### LIN-UNCONDITIONAL-FRAME 类型元素

1. **Pdu_CounterIn**
2. **Pdu_CounterOut**

### 6. PDUS

- **包名称**: `PDUS`
- **包含元素数量**: 2

#### 包含的元素

##### I-SIGNAL-I-PDU 类型元素

1. **Pdu_CounterIn**
2. **Pdu_CounterOut**

### 7. ISIGNALS

- **包名称**: `ISIGNALS`
- **包含元素数量**: 2

#### 包含的元素

##### I-SIGNAL 类型元素

1. **CounterIn**
2. **CounterOut**
