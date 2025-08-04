# 标准HTTP方法详解

## 概述

HTTP方法定义了客户端想要对服务器资源执行的操作类型。每个方法都有特定的语义和用途。

## 主要HTTP方法详解

### 1. GET - 获取资源

**用途**: 从服务器获取数据，不应该有副作用（幂等）

**特点**:
- 安全的（Safe）：不会修改服务器状态
- 幂等的（Idempotent）：多次调用结果相同
- 可缓存的（Cacheable）
- 参数通过URL查询字符串传递

**示例**:
```http
GET /api/users/123 HTTP/1.1
Host: example.com

# 响应
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": 123,
  "name": "张三",
  "email": "zhangsan@example.com"
}
```

**使用场景**:
- 获取用户信息
- 列出商品清单
- 搜索结果
- 下载文件

### 2. POST - 创建资源

**用途**: 向服务器提交数据，通常用于创建新资源

**特点**:
- 不安全的：会修改服务器状态
- 非幂等的：多次调用可能产生不同结果
- 不可缓存的
- 数据在请求体中传输

**示例**:
```http
POST /api/users HTTP/1.1
Host: example.com
Content-Type: application/json

{
  "name": "李四",
  "email": "lisi@example.com"
}

# 响应
HTTP/1.1 201 Created
Location: /api/users/124
Content-Type: application/json

{
  "id": 124,
  "name": "李四",
  "email": "lisi@example.com",
  "created_at": "2025-01-31T10:30:00Z"
}
```

**使用场景**:
- 创建新用户
- 提交表单
- 上传文件
- 发送邮件

### 3. PUT - 更新/替换资源

**用途**: 完全替换目标资源，如果资源不存在则创建

**特点**:
- 不安全的：会修改服务器状态
- 幂等的：多次调用结果相同
- 不可缓存的
- 完全替换语义

**示例**:
```http
PUT /api/users/123 HTTP/1.1
Host: example.com
Content-Type: application/json

{
  "name": "张三（已更新）",
  "email": "zhangsan_new@example.com",
  "phone": "13800138000"
}

# 响应
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": 123,
  "name": "张三（已更新）",
  "email": "zhangsan_new@example.com",
  "phone": "13800138000",
  "updated_at": "2025-01-31T10:35:00Z"
}
```

**使用场景**:
- 更新用户完整信息
- 替换配置文件
- 上传新版本文件

### 4. PATCH - 部分更新资源

**用途**: 对资源进行部分修改，只更新指定字段

**特点**:
- 不安全的：会修改服务器状态
- 非幂等的（通常）：取决于具体实现
- 不可缓存的
- 部分更新语义

**示例**:
```http
PATCH /api/users/123 HTTP/1.1
Host: example.com
Content-Type: application/json

{
  "email": "zhangsan_updated@example.com"
}

# 响应
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": 123,
  "name": "张三",
  "email": "zhangsan_updated@example.com",
  "phone": "13800138000",
  "updated_at": "2025-01-31T10:40:00Z"
}
```

**使用场景**:
- 更新用户邮箱
- 修改商品价格
- 更改文章状态

### 5. DELETE - 删除资源

**用途**: 删除指定的资源

**特点**:
- 不安全的：会修改服务器状态
- 幂等的：删除已删除的资源通常返回相同结果
- 不可缓存的

**示例**:
```http
DELETE /api/users/123 HTTP/1.1
Host: example.com

# 响应
HTTP/1.1 204 No Content

# 或者返回删除的资源信息
HTTP/1.1 200 OK
Content-Type: application/json

{
  "message": "用户 123 已删除",
  "deleted_at": "2025-01-31T10:45:00Z"
}
```

**使用场景**:
- 删除用户账户
- 移除商品
- 清空购物车

### 6. HEAD - 获取资源元信息

**用途**: 获取资源的响应头信息，不返回响应体

**特点**:
- 安全的：不会修改服务器状态
- 幂等的：多次调用结果相同
- 可缓存的

**示例**:
```http
HEAD /api/users/123 HTTP/1.1
Host: example.com

# 响应（只有头部，无响应体）
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 156
Last-Modified: Wed, 31 Jan 2025 10:30:00 GMT
ETag: "abc123"
```

**使用场景**:
- 检查资源是否存在
- 获取文件大小
- 检查缓存是否有效

### 7. OPTIONS - 获取支持的方法

**用途**: 查询服务器对特定资源支持的HTTP方法和其他选项

**特点**:
- 安全的：不会修改服务器状态
- 幂等的：多次调用结果相同
- 主要用于CORS预检请求

**示例**:
```http
OPTIONS /api/users/123 HTTP/1.1
Host: example.com

# 响应
HTTP/1.1 200 OK
Allow: GET, PUT, PATCH, DELETE, HEAD, OPTIONS
Access-Control-Allow-Methods: GET, PUT, PATCH, DELETE
Access-Control-Allow-Headers: Content-Type, Authorization
```

**使用场景**:
- CORS预检请求
- API文档生成
- 客户端功能检测

## HTTP方法对比表

| 方法 | 安全性 | 幂等性 | 可缓存 | 请求体 | 响应体 | 主要用途 |
|------|--------|--------|--------|--------|--------|----------|
| GET | ✅ | ✅ | ✅ | ❌ | ✅ | 获取资源 |
| POST | ❌ | ❌ | ❌ | ✅ | ✅ | 创建资源 |
| PUT | ❌ | ✅ | ❌ | ✅ | ✅ | 替换资源 |
| PATCH | ❌ | ❌* | ❌ | ✅ | ✅ | 部分更新 |
| DELETE | ❌ | ✅ | ❌ | ❌* | ✅* | 删除资源 |
| HEAD | ✅ | ✅ | ✅ | ❌ | ❌ | 获取元信息 |
| OPTIONS | ✅ | ✅ | ❌ | ❌ | ✅ | 获取选项 |

*注：PATCH的幂等性取决于具体实现；DELETE可以有请求体和响应体，但通常不使用

## 实际应用示例

### RESTful API 设计

```http
# 用户管理API
GET    /api/users          # 获取用户列表
POST   /api/users          # 创建新用户
GET    /api/users/123      # 获取特定用户
PUT    /api/users/123      # 完全更新用户
PATCH  /api/users/123      # 部分更新用户
DELETE /api/users/123      # 删除用户
HEAD   /api/users/123      # 检查用户是否存在
OPTIONS /api/users         # 获取支持的操作
```

### 文件操作API

```http
# 文件管理API
GET    /api/files/doc.pdf     # 下载文件
PUT    /api/files/doc.pdf     # 上传/替换文件
DELETE /api/files/doc.pdf     # 删除文件
HEAD   /api/files/doc.pdf     # 获取文件信息（大小、修改时间等）
```

### 状态码配合

```http
# GET 请求
GET /api/users/123
→ 200 OK (找到)
→ 404 Not Found (未找到)

# POST 请求
POST /api/users
→ 201 Created (创建成功)
→ 400 Bad Request (数据无效)
→ 409 Conflict (资源已存在)

# PUT 请求
PUT /api/users/123
→ 200 OK (更新成功)
→ 201 Created (创建成功)
→ 400 Bad Request (数据无效)

# DELETE 请求
DELETE /api/users/123
→ 204 No Content (删除成功，无内容)
→ 200 OK (删除成功，返回信息)
→ 404 Not Found (资源不存在)
```

## 最佳实践

### 1. 语义化使用
- 严格按照HTTP方法的语义使用
- 不要用GET执行有副作用的操作
- 不要用POST做所有操作

### 2. 幂等性考虑
- 确保PUT和DELETE操作的幂等性
- 对于非幂等操作，提供适当的错误处理

### 3. 缓存策略
- 合理利用GET和HEAD的可缓存特性
- 设置适当的缓存头信息

### 4. 错误处理
- 为不同的HTTP方法返回合适的状态码
- 提供清晰的错误消息

### 5. 安全考虑
- 对修改操作进行适当的认证和授权
- 使用HTTPS保护敏感数据
- 实施CORS策略

## 常见误用和避免方法

### ❌ 错误用法
```http
# 用GET执行删除操作
GET /api/users/123/delete

# 用POST做所有操作
POST /api/getUser
POST /api/updateUser
POST /api/deleteUser
```

### ✅ 正确用法
```http
# 使用合适的HTTP方法
DELETE /api/users/123

# RESTful设计
GET    /api/users/123
PUT    /api/users/123
DELETE /api/users/123
```

通过正确理解和使用HTTP方法，可以构建更加标准、易于理解和维护的Web API。
