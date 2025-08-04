# 🧩 一、推荐 AUTOSAR 文档结构 & 学习顺序

AUTOSAR 的官方 Adaptive Platform 文档由多个 Feature Document、SWS（Software Specification）、EXP（Explanation）组成：

| 类别   | 文档代码         | 内容简介                                    |
| ---- | ------------ | --------------------------------------- |
| 架构概览 | **APSYS**    | Adaptive Platform System Overview（系统总览） |
| 方法论  | **APMETH**   | Adaptive Platform Methodology（配置与开发流程）  |
| 执行管理 | **APEM**     | Execution Management（服务生命周期调度）          |
| 通信机制 | **APCOM**    | ara::com & SOME/IP（服务发现与通信）             |
| 永久化  | **APPER**    | Persistency（持久化服务）                      |
| 文件系统 | **APFS**     | File System Access（应用访问文件）              |
| 安全加密 | **APCRYP**   | Crypto Service（加密库接口）                   |
| 诊断服务 | **APDIAG**   | Diagnostics & DLT Logging               |
| 服务发现 | **APSOMEIP** | 基于 SOME/IP 的服务发现协议规范                    |
| 服务部署 | **APMAN**    | Manifest 文件结构（应用部署配置）                   |

---

# 🧭 二、详细阶段学习路线

## 🚩 第一阶段：构建宏观认知

目标：了解 Adaptive Platform 的整体设计理念、架构层次、与 Classic Platform 区别

### 📘 推荐文档与顺序：

1. **APSYS – Adaptive Platform System Overview**
    
    - 学习重点：
        
        - Execution Management & Service-Oriented Architecture (SOA)
            
        - Applications vs Services 的角色划分
            
        - Platform Host OS 要求（Linux/QNX/POSIX）
            
2. **APMETH – Adaptive Methodology**
    
    - 学习重点：
        
        - Manifest 概念（Application Manifest、Machine Manifest）
            
        - 如何生成代码（Model-based / Service Contracts / VFB-mapping）
            

> 建议配合官方 AUTOSAR 系统架构图理解层次关系（Application ↔ Middleware ↔ Platform）

---

## 🚩 第二阶段：核心机制理解

目标：深入理解 AP 核心运行机制，如服务通信、调度执行、安全接口等

### 📘 推荐模块与顺序：

1. **APCOM – ara::com**
    
    - 学习重点：
        
        - 服务定义、实例注册、客户端代理机制
            
        - SOME/IP 绑定过程
            
        - 与 Classic 的 RTE 对比
            
2. **APEM – Execution Management**
    
    - 生命周期状态图（AppState，MachineState）
        
    - Health Management（HM）
        
    - 与 Service Instantiation 的关系
        
3. **APMAN – Manifest**
    
    - 学习重点：
        
        - Manifest 文件结构、字段（例如 ExecDependency, ServiceDependencies）
            
        - 如何配置 Execution Slots
            
4. **APPER – Persistency**
    
    - 数据存储机制、映射文件系统、KV 存储接口
        
5. **APDIAG – Diagnostics**
    
    - ara::diag 服务接口
        
    - DLT 日志机制及其配置
        

---

## 🚩 第三阶段：配置集成与工程实现

目标：掌握如何配置 Adaptive 应用，理解部署方式与中间件接口生成方式

### 📘 推荐路径：

1. **APSOMEIP – Service Discovery 与通信协议**
    
    - 与 ara::com 紧密结合，用于服务发现注册、启停控制
        
2. **APCRYP – Crypto & Security**
    
    - 如何调用 PKCS11 接口做 HSM 集成
        
3. **APFS – FileSystem**
    
    - 如何进行路径映射、容器内数据访问权限设置
        
4. **APRPC – RPC 绑定配置（如 Capic）**
    
    - 与代码生成工具链（如 EB tresos Studio、Vector DaVinci Adaptive）配合使用
        
5. 配合实际工具使用：
    
    - Vector DaVinci Adaptive/Configurator
        
    - Adaptive Platform Foundation（基于 Linux 的运行环境）
        

---

## 🚩 第四阶段：实践与验证

目标：使用真实工具平台搭建 Adaptive 应用，验证服务通信与调度执行

### 推荐实践：

- 创建一个简单的 Service + Client（带 `ServiceManifest` 和 `ClientManifest`）
    
- 使用 ara::com 实现发布订阅
    
- 配置 Execution Management 中的 State 依赖
    
- 使用 ara::log 和 DLT 输出调试日志
    
- 使用 Adaptive Platform Runtime（如 Vector AEP）运行调试