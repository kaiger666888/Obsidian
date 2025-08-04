# Gerrit Checks插件开发完整指南

## 概述

Gerrit Checks API是Gerrit Code Review系统提供的一个扩展接口，允许开发者创建自定义插件来集成CI系统、静态分析工具和其他检查工具。本指南将详细介绍如何从零开始开发一个Gerrit Checks插件。

## 技术架构概览

### 核心组件
- **Checks API**: Gerrit提供的JavaScript插件接口
- **Checks Provider**: 插件中负责提供检查结果的组件
- **Runs**: 代表一次检查执行
- **Results**: 每个Run的具体结果

### 工作流程
```
外部CI/分析系统 → Gerrit Checks插件 → Checks API → Gerrit UI显示
```

## 开发环境搭建

### 环境要求

#### 系统要求
- **操作系统**: Linux/macOS/Windows
- **Java版本**: JDK 11或更高版本
- **构建工具**: Bazel 4.0+
- **Git版本**: 2.20+

#### 必需软件安装

**1. 安装Java开发环境**
```bash
# Ubuntu/Debian
sudo apt update
sudo apt install openjdk-11-jdk

# CentOS/RHEL
sudo yum install java-11-openjdk-devel

# macOS
brew install openjdk@11
```

**2. 安装Bazel构建工具**
```bash
# Ubuntu/Debian
sudo apt install apt-transport-https curl gnupg
curl -fsSL https://bazel.build/bazel-release.pub.gpg | gpg --dearmor > bazel.gpg
sudo mv bazel.gpg /etc/apt/trusted.gpg.d/
echo "deb [arch=amd64] https://storage.googleapis.com/bazel-apt stable jdk1.8" | sudo tee /etc/apt/sources.list.d/bazel.list
sudo apt update && sudo apt install bazel

# macOS
brew install bazel

# 或者直接下载二进制文件
wget https://github.com/bazelbuild/bazel/releases/download/4.2.1/bazel-4.2.1-linux-x86_64
chmod +x bazel-4.2.1-linux-x86_64
sudo mv bazel-4.2.1-linux-x86_64 /usr/local/bin/bazel
```

**3. 获取Gerrit源码**
```bash
git clone https://gerrit.googlesource.com/gerrit
cd gerrit
git checkout stable-3.4  # 选择合适的版本
```

### 开发工具配置

#### IDE推荐配置
- **IntelliJ IDEA**: 推荐使用，支持Bazel插件
- **Eclipse**: 需要安装Bazel插件
- **VS Code**: 需要安装Java和Bazel扩展

#### IntelliJ IDEA配置步骤
```bash
# 1. 安装Bazel插件
# File → Settings → Plugins → 搜索"Bazel"安装

# 2. 导入项目
# File → Import Bazel Project
# 选择gerrit目录下的.bazelproject文件
```

## 插件项目结构

### 标准项目结构
```
my-checks-plugin/
├── BUILD                      # Bazel构建文件
├── plugin.properties         # 插件元信息
├── src/main/java/            # Java源码
│   └── com/example/plugin/
│       ├── Module.java       # Guice模块
│       ├── ChecksProvider.java # Checks提供者
│       └── RestApiModule.java  # REST API模块
├── src/main/resources/       # 资源文件
│   └── static/
│       └── checks.js         # 前端JavaScript
└── src/test/java/           # 测试代码
```

### 创建插件骨架

**1. 创建基础目录结构**
```bash
mkdir my-checks-plugin
cd my-checks-plugin
mkdir -p src/main/java/com/example/plugin
mkdir -p src/main/resources/static
mkdir -p src/test/java/com/example/plugin
```

**2. 创建BUILD文件**
```python
load("//tools/bzl:plugin.bzl", "gerrit_plugin")

gerrit_plugin(
    name = "my-checks-plugin",
    srcs = glob(["src/main/java/**/*.java"]),
    resources = glob(["src/main/resources/**/*"]),
    manifest_entries = [
        "Gerrit-PluginName: my-checks-plugin",
        "Gerrit-Module: com.example.plugin.Module",
        "Implementation-Title: My Checks Plugin",
        "Implementation-URL: https://example.com/my-checks-plugin",
    ],
)
```

**3. 创建plugin.properties**
```properties
# Plugin metadata
Gerrit-PluginName=my-checks-plugin
Gerrit-Module=com.example.plugin.Module
Gerrit-HttpModule=com.example.plugin.RestApiModule

Implementation-Title=My Checks Plugin
Implementation-Version=1.0.0
Implementation-Vendor=Example Corp
Implementation-URL=https://example.com/my-checks-plugin
```

## 核心代码实现

### 1. Guice模块配置 (Module.java)

```java
package com.example.plugin;

import com.google.gerrit.extensions.registration.DynamicSet;
import com.google.gerrit.extensions.webui.JavaScriptPlugin;
import com.google.gerrit.extensions.webui.WebUiPlugin;
import com.google.inject.AbstractModule;

public class Module extends AbstractModule {
    @Override
    protected void configure() {
        // 注册JavaScript插件
        DynamicSet.bind(binder(), WebUiPlugin.class)
            .toInstance(new JavaScriptPlugin("checks.js"));
    }
}
```

### 2. REST API模块 (RestApiModule.java)

```java
package com.example.plugin;

import com.google.gerrit.extensions.registration.DynamicMap;
import com.google.gerrit.extensions.restapi.RestApiModule;
import com.google.gerrit.server.change.ChangeResource;

public class RestApiModule extends RestApiModule {
    @Override
    protected void configure() {
        // 注册REST API端点
        DynamicMap.mapOf(binder(), ChangeResource.class);
        child(CHANGE_KIND, "checks").to(ChecksCollection.class);
        get(CHANGE_KIND, "checks").to(ListChecks.class);
        post(CHANGE_KIND, "checks").to(PostChecks.class);
    }
}
```

### 3. Checks数据模型

```java
package com.example.plugin;

import com.google.gson.annotations.SerializedName;
import java.time.Instant;
import java.util.List;

public class CheckRun {
    @SerializedName("checkName")
    public String checkName;
    
    @SerializedName("patchset")
    public PatchSet patchset;
    
    @SerializedName("status")
    public CheckState status;
    
    @SerializedName("started")
    public Instant started;
    
    @SerializedName("finished")
    public Instant finished;
    
    @SerializedName("results")
    public List<CheckResult> results;
    
    public static class CheckResult {
        @SerializedName("category")
        public Category category;
        
        @SerializedName("summary")
        public String summary;
        
        @SerializedName("message")
        public String message;
        
        @SerializedName("links")
        public List<Link> links;
    }
    
    public enum CheckState {
        NOT_STARTED,
        SCHEDULED,
        RUNNING,
        SUCCESSFUL,
        FAILED,
        NOT_RELEVANT
    }
    
    public enum Category {
        ERROR,
        WARNING, 
        INFO,
        SUCCESS
    }
}
```

### 4. 前端JavaScript实现 (checks.js)

```javascript
// src/main/resources/static/checks.js
Gerrit.install(function(self) {
    'use strict';

    // 定义Checks Provider
    const checksProvider = {
        // 获取指定change的checks
        fetch: function(changeInfo) {
            return new Promise((resolve, reject) => {
                // 调用后端API获取checks数据
                self.get(`/changes/${changeInfo._number}/checks`)
                    .then(response => response.json())
                    .then(checks => {
                        // 转换数据格式以符合Checks API要求
                        const runs = checks.map(check => ({
                            checkName: check.checkName,
                            patchset: check.patchset,
                            status: check.status,
                            started: check.started,
                            finished: check.finished,
                            results: check.results || []
                        }));
                        resolve(runs);
                    })
                    .catch(error => {
                        console.error('Failed to fetch checks:', error);
                        reject(error);
                    });
            });
        },

        // 可选：支持重新运行checks
        rerun: function(changeInfo, runInfo) {
            return self.post(`/changes/${changeInfo._number}/checks`, {
                action: 'rerun',
                checkName: runInfo.checkName
            });
        }
    };

    // 注册Checks Provider
    self.checksApi().register(checksProvider, 'my-checks-plugin');
});
```

### 5. REST API端点实现

```java
package com.example.plugin;

import com.google.gerrit.extensions.restapi.RestReadView;
import com.google.gerrit.server.change.ChangeResource;
import com.google.gson.reflect.TypeToken;
import com.google.inject.Inject;
import com.google.inject.Singleton;
import java.util.List;

@Singleton
public class ListChecks implements RestReadView<ChangeResource> {
    
    private final ChecksDataService checksDataService;
    
    @Inject
    ListChecks(ChecksDataService checksDataService) {
        this.checksDataService = checksDataService;
    }
    
    @Override
    public List<CheckRun> apply(ChangeResource resource) {
        // 从外部系统或数据库获取checks数据
        return checksDataService.getChecksForChange(
            resource.getChange().getId(),
            resource.getPatchSet().id()
        );
    }
}
```

## 构建和部署

### 构建插件

```bash
# 在Gerrit源码根目录执行
bazel build plugins/my-checks-plugin

# 或者构建所有插件
bazel build plugins:all
```

### 部署到Gerrit服务器

**方法1: 热部署（推荐用于开发）**
```bash
# 复制插件到Gerrit plugins目录
cp bazel-bin/plugins/my-checks-plugin/my-checks-plugin.jar \
   /path/to/gerrit/plugins/

# 重启Gerrit或启用插件
ssh -p 29418 admin@gerrit-server gerrit plugin reload my-checks-plugin
```

**方法2: 通过管理界面部署**
1. 登录Gerrit管理界面
2. 进入 `Browse` → `Repositories` → `All-Projects`
3. 选择 `General` → `Plugin Manager`
4. 上传插件JAR文件并启用

### 验证部署

```bash
# 检查插件状态
ssh -p 29418 admin@gerrit-server gerrit plugin ls

# 查看插件日志
tail -f /path/to/gerrit/logs/error_log
```

## 测试和调试

### 单元测试

```java
package com.example.plugin;

import static com.google.common.truth.Truth.assertThat;
import static org.mockito.Mockito.*;

import com.google.gerrit.testing.GerritJUnit;
import org.junit.Test;
import org.junit.runner.RunWith;

@RunWith(GerritJUnit.class)
public class ChecksProviderTest {
    
    @Test
    public void testGetChecksForChange() {
        // 模拟测试数据
        ChangeResource mockResource = mock(ChangeResource.class);
        ChecksDataService mockService = mock(ChecksDataService.class);
        
        // 设置期望
        when(mockService.getChecksForChange(any(), any()))
            .thenReturn(createTestCheckRuns());
        
        // 执行测试
        ListChecks listChecks = new ListChecks(mockService);
        List<CheckRun> result = listChecks.apply(mockResource);
        
        // 验证结果
        assertThat(result).hasSize(2);
        assertThat(result.get(0).checkName).isEqualTo("build-test");
    }
    
    private List<CheckRun> createTestCheckRuns() {
        // 创建测试数据
        CheckRun run1 = new CheckRun();
        run1.checkName = "build-test";
        run1.status = CheckRun.CheckState.SUCCESSFUL;
        
        CheckRun run2 = new CheckRun();
        run2.checkName = "lint-check";
        run2.status = CheckRun.CheckState.FAILED;
        
        return Arrays.asList(run1, run2);
    }
}
```

### 运行测试

```bash
# 运行特定插件的测试
bazel test plugins/my-checks-plugin:all

# 运行所有测试
bazel test plugins:all_tests
```

### 调试技巧

**1. 日志调试**
```java
import com.google.gerrit.server.logging.Metadata;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;

public class ChecksProvider {
    private static final Logger log = LoggerFactory.getLogger(ChecksProvider.class);
    
    public void someMethod() {
        log.info("Processing checks for change: {}", changeId);
        log.debug("Debug info: {}", debugData);
    }
}
```

**2. 前端调试**
```javascript
// 在浏览器开发者工具中调试
console.log('Checks data:', checksData);
console.group('Gerrit Checks Plugin');
console.log('Change info:', changeInfo);
console.groupEnd();
```

## 高级功能实现

### 与外部CI系统集成

```java
@Singleton
public class JenkinsChecksService implements ChecksDataService {
    
    private final HttpClient httpClient;
    private final String jenkinsUrl;
    
    @Inject
    JenkinsChecksService(@GerritServerConfig Config config, HttpClient httpClient) {
        this.jenkinsUrl = config.getString("jenkins", null, "url");
        this.httpClient = httpClient;
    }
    
    @Override
    public List<CheckRun> getChecksForChange(Change.Id changeId, PatchSet.Id patchSetId) {
        try {
            // 调用Jenkins API获取构建状态
            String apiUrl = String.format("%s/job/gerrit-verification/api/json", jenkinsUrl);
            HttpGet request = new HttpGet(apiUrl);
            
            HttpResponse response = httpClient.execute(request);
            String json = EntityUtils.toString(response.getEntity());
            
            // 解析Jenkins响应并转换为CheckRun格式
            return parseJenkinsResponse(json, changeId, patchSetId);
            
        } catch (Exception e) {
            log.error("Failed to fetch Jenkins build status", e);
            return Collections.emptyList();
        }
    }
}
```

### 实时状态更新

```javascript
// 支持实时更新的Checks Provider
const checksProvider = {
    fetch: function(changeInfo) {
        return new Promise((resolve, reject) => {
            // 获取初始状态
            self.get(`/changes/${changeInfo._number}/checks`)
                .then(response => response.json())
                .then(checks => {
                    resolve(checks);
                    
                    // 为正在运行的checks设置轮询更新
                    const runningChecks = checks.filter(c => c.status === 'RUNNING');
                    if (runningChecks.length > 0) {
                        startPolling(changeInfo._number, runningChecks);
                    }
                })
                .catch(reject);
        });
    }
};

function startPolling(changeNumber, runningChecks) {
    const pollInterval = setInterval(() => {
        self.get(`/changes/${changeNumber}/checks`)
            .then(response => response.json())
            .then(updatedChecks => {
                // 检查是否有状态变化
                const stillRunning = updatedChecks.filter(c => c.status === 'RUNNING');
                if (stillRunning.length === 0) {
                    clearInterval(pollInterval);
                }
                
                // 通知UI更新
                self.checksApi().announceUpdate();
            });
    }, 10000); // 每10秒轮询一次
}
```

## 性能优化

### 缓存策略

```java
@Singleton
public class CachedChecksService implements ChecksDataService {
    
    private final LoadingCache<String, List<CheckRun>> cache;
    private final ChecksDataService delegate;
    
    @Inject
    CachedChecksService(ChecksDataService delegate) {
        this.delegate = delegate;
        this.cache = CacheBuilder.newBuilder()
            .maximumSize(1000)
            .expireAfterWrite(5, TimeUnit.MINUTES)
            .build(new CacheLoader<String, List<CheckRun>>() {
                @Override
                public List<CheckRun> load(String key) {
                    String[] parts = key.split(":");
                    Change.Id changeId = Change.id(Integer.parseInt(parts[0]));
                    PatchSet.Id patchSetId = PatchSet.id(changeId, Integer.parseInt(parts[1]));
                    return delegate.getChecksForChange(changeId, patchSetId);
                }
            });
    }
    
    @Override
    public List<CheckRun> getChecksForChange(Change.Id changeId, PatchSet.Id patchSetId) {
        String cacheKey = changeId.get() + ":" + patchSetId.get();
        try {
            return cache.get(cacheKey);
        } catch (ExecutionException e) {
            log.warn("Cache miss for checks", e);
            return delegate.getChecksForChange(changeId, patchSetId);
        }
    }
}
```

### 异步处理

```java
@Singleton
public class AsyncChecksService {
    
    private final ExecutorService executor;
    private final ChecksDataService checksService;
    
    @Inject
    AsyncChecksService(ChecksDataService checksService) {
        this.checksService = checksService;
        this.executor = Executors.newFixedThreadPool(10);
    }
    
    public CompletableFuture<List<CheckRun>> getChecksAsync(Change.Id changeId, PatchSet.Id patchSetId) {
        return CompletableFuture.supplyAsync(() -> 
            checksService.getChecksForChange(changeId, patchSetId), executor);
    }
}
```

## 安全考虑

### 权限控制

```java
@Singleton 
public class SecureChecksProvider {
    
    private final Provider<CurrentUser> userProvider;
    private final PermissionBackend permissionBackend;
    
    @Inject
    SecureChecksProvider(Provider<CurrentUser> userProvider, 
                        PermissionBackend permissionBackend) {
        this.userProvider = userProvider;
        this.permissionBackend = permissionBackend;
    }
    
    public List<CheckRun> getChecksForChange(ChangeResource resource) {
        CurrentUser user = userProvider.get();
        
        try {
            // 验证用户是否有权限查看checks
            permissionBackend.currentUser().change(resource).check(ChangePermission.READ);
            
            // 进一步检查特定的checks权限
            if (!hasChecksPermission(user, resource)) {
                return Collections.emptyList();
            }
            
            return checksService.getChecksForChange(
                resource.getChange().getId(),
                resource.getPatchSet().id()
            );
            
        } catch (AuthException | PermissionBackendException e) {
            log.warn("Permission denied for checks access", e);
            return Collections.emptyList();
        }
    }
}
```

### 输入验证

```java
public class ChecksInputValidator {
    
    public void validateCheckRun(CheckRun checkRun) throws BadRequestException {
        if (Strings.isNullOrEmpty(checkRun.checkName)) {
            throw new BadRequestException("Check name is required");
        }
        
        if (checkRun.checkName.length() > 100) {
            throw new BadRequestException("Check name too long");
        }
        
        if (!isValidCheckName(checkRun.checkName)) {
            throw new BadRequestException("Invalid check name format");
        }
    }
    
    private boolean isValidCheckName(String name) {
        return name.matches("^[a-zA-Z0-9_-]+$");
    }
}
```

## 发布和维护

### 版本管理

```properties
# plugin.properties
Implementation-Version=1.2.0
Gerrit-ApiVersion=3.4.0
Min-Gerrit-Version=3.4.0
Max-Gerrit-Version=3.5.99
```

### 持续集成配置

```yaml
# .github/workflows/ci.yml
name: CI
on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Set up JDK 11
        uses: actions/setup-java@v2
        with:
          java-version: '11'
          distribution: 'adopt'
      
      - name: Cache Bazel
        uses: actions/cache@v2
        with:
          path: ~/.cache/bazel
          key: bazel-${{ runner.os }}-${{ hashFiles('WORKSPACE', 'BUILD') }}
      
      - name: Build plugin
        run: bazel build plugins/my-checks-plugin
      
      - name: Run tests
        run: bazel test plugins/my-checks-plugin:all
```

### 文档和示例

创建完整的文档结构：

```
docs/
├── README.md                 # 插件概述和快速开始
├── installation.md          # 安装部署指南  
├── configuration.md         # 配置说明
├── api-reference.md         # API参考文档
├── examples/                # 示例代码
│   ├── basic-integration.md
│   └── advanced-features.md
└── troubleshooting.md       # 问题排查指南
```

## 总结

开发Gerrit Checks插件需要掌握以下关键技术：

### 技术栈总览
- **后端**: Java + Guice依赖注入 + Gerrit API
- **前端**: JavaScript + Gerrit Web UI API  
- **构建**: Bazel构建系统
- **测试**: JUnit + Mockito + Truth断言库

### 开发流程总结
1. **环境搭建**: 安装Java、Bazel，获取Gerrit源码
2. **项目创建**: 建立标准目录结构，配置构建文件
3. **核心实现**: 开发Checks Provider、REST API、前端界面
4. **测试调试**: 编写单元测试，进行集成测试
5. **部署发布**: 构建插件，部署到Gerrit服务器

### 最佳实践
- 遵循Gerrit插件开发规范
- 实现适当的缓存和异步处理
- 注重安全性和权限控制
- 提供完整的文档和示例
- 建立持续集成流程

通过本指南，您应该能够成功开发出功能完整、性能良好的Gerrit Checks插件，有效集成外部CI/CD系统和代码分析工具。