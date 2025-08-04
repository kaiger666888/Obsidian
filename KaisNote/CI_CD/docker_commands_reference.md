# Docker常用命令参考手册

## 容器管理命令

### 查看容器
```bash
# 查看正在运行的容器
docker ps

# 查看所有容器（包括停止的）
docker ps -a

# 查看最近创建的容器
docker ps -l

# 只显示容器ID
docker ps -q

# 自定义显示格式
docker ps --format "table {{.ID}}\t{{.Image}}\t{{.Status}}\t{{.Names}}"

# 显示容器大小
docker ps -s

# 按条件过滤
docker ps --filter "status=running"
docker ps --filter "name=webapp"
docker ps --filter "ancestor=nginx"
```

### 运行容器
```bash
# 基本运行
docker run nginx

# 后台运行
docker run -d nginx

# 指定容器名称
docker run --name my-nginx nginx

# 端口映射
docker run -p 8080:80 nginx

# 挂载数据卷
docker run -v /host/path:/container/path nginx

# 环境变量
docker run -e ENV_VAR=value nginx

# 交互式运行
docker run -it ubuntu bash

# 一次性运行（运行后自动删除）
docker run --rm nginx

# 资源限制
docker run --memory=512m --cpus=1.5 nginx

# 网络配置
docker run --network=host nginx
docker run --network=bridge nginx
```

### 容器操作
```bash
# 启动容器
docker start container_name_or_id

# 停止容器
docker stop container_name_or_id

# 强制停止容器
docker kill container_name_or_id

# 重启容器
docker restart container_name_or_id

# 暂停容器
docker pause container_name_or_id

# 恢复暂停的容器
docker unpause container_name_or_id

# 删除容器
docker rm container_name_or_id

# 强制删除运行中的容器
docker rm -f container_name_or_id

# 删除所有停止的容器
docker container prune

# 批量删除容器
docker rm $(docker ps -aq)
```

### 容器执行命令
```bash
# 在运行的容器中执行命令
docker exec container_name command

# 交互式执行
docker exec -it container_name bash

# 以特定用户执行
docker exec -u root container_name command

# 设置工作目录
docker exec -w /app container_name command

# 设置环境变量
docker exec -e VAR=value container_name command
```

## 镜像管理命令

### 查看镜像
```bash
# 列出本地镜像
docker images

# 显示镜像详细信息
docker images -a

# 只显示镜像ID
docker images -q

# 显示镜像大小
docker images --format "{{.Repository}}:{{.Tag}} {{.Size}}"

# 过滤镜像
docker images --filter "dangling=true"
docker images --filter "reference=nginx*"
```

### 镜像操作
```bash
# 拉取镜像
docker pull nginx
docker pull nginx:1.20

# 推送镜像
docker push username/image:tag

# 构建镜像
docker build -t image_name .
docker build -t image_name -f Dockerfile.prod .

# 删除镜像
docker rmi image_name_or_id

# 强制删除镜像
docker rmi -f image_name_or_id

# 删除未使用的镜像
docker image prune

# 删除所有镜像
docker rmi $(docker images -q)

# 标记镜像
docker tag source_image:tag target_image:tag

# 保存镜像到文件
docker save -o image.tar image_name

# 从文件加载镜像
docker load -i image.tar

# 导出容器为镜像
docker export container_name > container.tar

# 导入容器镜像
docker import container.tar new_image_name
```

## 数据卷管理

### 数据卷命令
```bash
# 创建数据卷
docker volume create volume_name

# 列出数据卷
docker volume ls

# 查看数据卷详细信息
docker volume inspect volume_name

# 删除数据卷
docker volume rm volume_name

# 删除未使用的数据卷
docker volume prune

# 使用数据卷运行容器
docker run -v volume_name:/path/in/container nginx

# 绑定挂载
docker run -v /host/path:/container/path nginx

# 只读挂载
docker run -v /host/path:/container/path:ro nginx
```

## 网络管理

### 网络命令
```bash
# 列出网络
docker network ls

# 创建网络
docker network create network_name
docker network create --driver bridge my_network

# 查看网络详细信息
docker network inspect network_name

# 连接容器到网络
docker network connect network_name container_name

# 断开容器网络连接
docker network disconnect network_name container_name

# 删除网络
docker network rm network_name

# 删除未使用的网络
docker network prune

# 在指定网络中运行容器
docker run --network=network_name nginx
```

## 系统管理命令

### 系统信息
```bash
# 显示Docker系统信息
docker info

# 显示Docker版本
docker version

# 显示磁盘使用情况
docker system df

# 显示实时事件
docker events

# 显示容器进程
docker top container_name

# 显示容器资源使用统计
docker stats

# 显示特定容器统计
docker stats container_name

# 显示容器日志
docker logs container_name
docker logs -f container_name  # 跟踪日志
docker logs --tail 100 container_name  # 显示最后100行
```

### 系统清理
```bash
# 清理未使用的资源
docker system prune

# 清理所有未使用的资源（包括镜像）
docker system prune -a

# 清理未使用的容器
docker container prune

# 清理未使用的镜像
docker image prune

# 清理未使用的数据卷
docker volume prune

# 清理未使用的网络
docker network prune
```

## Docker Compose命令

### 基本操作
```bash
# 启动服务
docker-compose up

# 后台启动服务
docker-compose up -d

# 停止服务
docker-compose down

# 重启服务
docker-compose restart

# 查看服务状态
docker-compose ps

# 查看服务日志
docker-compose logs
docker-compose logs service_name

# 进入服务容器
docker-compose exec service_name bash

# 运行一次性命令
docker-compose run service_name command

# 拉取镜像
docker-compose pull

# 构建镜像
docker-compose build

# 停止并删除容器、网络、数据卷
docker-compose down -v
```

## 镜像仓库命令

### Docker Hub操作
```bash
# 登录Docker Hub
docker login

# 登录到私有仓库
docker login registry.example.com

# 登出
docker logout

# 搜索镜像
docker search nginx

# 查看镜像标签（需要第三方工具或API）
curl -s https://registry.hub.docker.com/v2/repositories/nginx/tags/
```

## 高级命令

### 容器检查和调试
```bash
# 查看容器详细信息
docker inspect container_name

# 查看容器文件系统变化
docker diff container_name

# 复制文件到容器
docker cp file.txt container_name:/path/

# 从容器复制文件
docker cp container_name:/path/file.txt ./

# 提交容器为镜像
docker commit container_name new_image_name

# 查看镜像历史
docker history image_name

# 等待容器退出
docker wait container_name
```

### 资源管理
```bash
# 更新容器资源限制
docker update --memory=1g container_name
docker update --cpus=2 container_name

# 查看容器端口映射
docker port container_name

# 重命名容器
docker rename old_name new_name

# 查看容器中运行的进程
docker top container_name
```

## 常用命令组合

### 批量操作
```bash
# 停止所有运行的容器
docker stop $(docker ps -q)

# 删除所有容器
docker rm $(docker ps -aq)

# 删除所有镜像
docker rmi $(docker images -q)

# 删除悬空镜像
docker rmi $(docker images -f "dangling=true" -q)

# 删除退出状态的容器
docker rm $(docker ps --filter "status=exited" -q)

# 按名称模式删除容器
docker rm $(docker ps -a --filter "name=test*" -q)
```

### 监控和调试
```bash
# 实时查看容器日志
docker logs -f --tail 100 container_name

# 查看容器详细配置
docker inspect container_name | jq '.[0].Config'

# 查看容器网络配置
docker inspect container_name | jq '.[0].NetworkSettings'

# 查看容器挂载点
docker inspect container_name | jq '.[0].Mounts'

# 进入容器调试
docker exec -it container_name /bin/bash
# 或
docker exec -it container_name /bin/sh
```

## 实用技巧

### 命令别名设置
```bash
# 在 ~/.bashrc 或 ~/.zshrc 中添加
alias dps='docker ps'
alias dpsa='docker ps -a'
alias di='docker images'
alias drm='docker rm'
alias drmi='docker rmi'
alias dex='docker exec -it'
alias dlogs='docker logs -f'
```

### 常用过滤器
```bash
# 按状态过滤
docker ps --filter "status=running"
docker ps --filter "status=exited"
docker ps --filter "status=paused"

# 按镜像过滤
docker ps --filter "ancestor=nginx"

# 按名称过滤
docker ps --filter "name=web"

# 按标签过滤
docker ps --filter "label=environment=production"

# 按网络过滤
docker ps --filter "network=bridge"

# 按端口过滤
docker ps --filter "expose=80"
```

### 格式化输出
```bash
# 自定义表格格式
docker ps --format "table {{.ID}}\t{{.Image}}\t{{.Command}}\t{{.Status}}\t{{.Names}}"

# JSON格式输出
docker ps --format "{{json .}}"

# 只显示特定字段
docker ps --format "{{.Names}}: {{.Status}}"

# 显示创建时间
docker ps --format "table {{.Names}}\t{{.Image}}\t{{.CreatedAt}}\t{{.Status}}"
```

---

> **提示**: 大多数Docker命令都支持 `--help` 参数来查看详细的使用说明，例如：`docker run --help`
