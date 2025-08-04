# Gerrit Plugin Checks API 总结

## API概述

Gerrit Plugin Checks API是由`plugin.checks()`提供的JavaScript API，允许插件为Gerrit的"Checks"标签页和摘要视图做出贡献。每个插件可以注册一个checks provider，当变更页面加载时会被调用，返回包含Runs列表的响应，每个run可以包含多个Results。

## 核心功能

### 1. Checks Provider注册
- Provider必须实现一个fetch()接口，返回Promise<FetchResponse>，包含runs和results数据
- 当变更页面加载时，注册的provider会被自动调用

### 2. UI集成
- 如果没有插件注册到ChecksApi，Checks标签页将被隐藏
- 为外部CI/分析系统的结果提供统一的UI展示界面

## 相关链接分析

### 核心文档链接
- `https://gerrit-review.googlesource.com/Documentation/pg-plugin-checks-api.html` - 官方API文档
- 源代码中有详细的ChecksApi文档，但链接指向master分支，可能反映比您安装版本更新的API

### 设计背景
- 可以在设计文档中了解该API的动机、用例和原始计划

### 实际应用示例
- 有一些开源插件使用了Checks API的例子可供参考
- Jenkins插件实现了Gerrit Checks API，添加REST API端点查询在给定Patchset上工作的Runs，返回CheckRun对象列表用于填充Gerrit UI中的checks相关信息

## 与Checks Plugin的关系

### 重要说明
- Google的Gerrit团队已决定停止开发checks plugin，推荐的解决方案是Checks UI（即Plugin Checks API），它能展示来自外部CI/分析系统的结果
- Checks API得到完全支持，将是集成机器人、分析器、检查器结果到Gerrit的最佳（唯一）方式，允许任意自定义JS插件动态提供检查结果

## 技术实现

### 数据结构
- FetchResponse包含runs和results
- 每个run可以包含多个result
- REST API返回CheckInfo实体列表

### 集成方式
- 为检查器（CI系统、静态分析器等）与Gerrit Code Review集成提供统一体验
- 支持外部CI系统通过API将检查结果展示在Gerrit界面中

## 总结

这个API主要解决了外部检查系统（如CI、静态分析工具等）与Gerrit界面集成的问题，提供了标准化的方式来展示检查结果。