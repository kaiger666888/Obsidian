# Ubuntu Linux常用命令参考手册

## 文件和目录操作

### 基本文件操作
```bash
# 查看当前目录
pwd

# 列出文件和目录
ls                    # 基本列表
ls -l                 # 详细列表
ls -la                # 包含隐藏文件的详细列表
ls -lh                # 人类可读的文件大小
ls -lt                # 按修改时间排序
ls -lS                # 按文件大小排序
ls -lR                # 递归显示子目录

# 切换目录
cd /path/to/directory # 切换到指定目录
cd                    # 切换到家目录
cd ~                  # 切换到家目录
cd ..                 # 返回上级目录
cd -                  # 返回之前的目录

# 创建目录
mkdir directory_name
mkdir -p path/to/directory  # 递归创建目录
mkdir -m 755 directory      # 创建时指定权限

# 删除目录
rmdir directory_name        # 删除空目录
rm -r directory_name        # 递归删除目录及内容
rm -rf directory_name       # 强制递归删除

# 复制文件和目录
cp file1 file2              # 复制文件
cp -r dir1 dir2             # 递归复制目录
cp -p file1 file2           # 保持原文件属性
cp -u file1 file2           # 只在源文件较新时复制
cp -i file1 file2           # 交互式复制（覆盖前询问）

# 移动/重命名文件
mv file1 file2              # 重命名文件
mv file1 /path/to/dir/      # 移动文件到目录
mv dir1 dir2                # 重命名目录

# 删除文件
rm file_name                # 删除文件
rm -i file_name             # 交互式删除
rm -f file_name             # 强制删除
rm *.txt                    # 删除所有txt文件
```

### 文件查看和编辑
```bash
# 查看文件内容
cat file_name               # 显示整个文件
less file_name              # 分页查看文件
more file_name              # 分页查看文件
head file_name              # 显示文件前10行
head -n 20 file_name        # 显示前20行
tail file_name              # 显示文件后10行
tail -n 20 file_name        # 显示后20行
tail -f file_name           # 实时跟踪文件变化

# 编辑文件
nano file_name              # 使用nano编辑器
vim file_name               # 使用vim编辑器
gedit file_name             # 使用图形界面编辑器

# 创建空文件或更新时间戳
touch file_name
touch file1 file2 file3

# 查找文件中的文本
grep "pattern" file_name
grep -i "pattern" file_name     # 忽略大小写
grep -r "pattern" directory     # 递归搜索目录
grep -n "pattern" file_name     # 显示行号
grep -v "pattern" file_name     # 显示不匹配的行
```

## 文件搜索和查找

### find命令
```bash
# 按名称查找文件
find /path -name "filename"
find /path -name "*.txt"        # 查找所有txt文件
find /path -iname "*.TXT"       # 忽略大小写查找

# 按类型查找
find /path -type f              # 查找文件
find /path -type d              # 查找目录
find /path -type l              # 查找符号链接

# 按大小查找
find /path -size +10M           # 查找大于10MB的文件
find /path -size -1k            # 查找小于1KB的文件
find /path -empty               # 查找空文件

# 按时间查找
find /path -mtime -7            # 查找7天内修改的文件
find /path -atime +30           # 查找30天前访问的文件
find /path -ctime -1            # 查找1天内状态改变的文件

# 按权限查找
find /path -perm 755            # 查找权限为755的文件
find /path -perm -644           # 查找至少有644权限的文件

# 执行操作
find /path -name "*.tmp" -delete    # 查找并删除tmp文件
find /path -name "*.log" -exec rm {} \;  # 查找并删除log文件
```

### locate命令
```bash
# 快速查找文件（需要先更新数据库）
sudo updatedb              # 更新locate数据库
locate filename            # 快速查找文件
locate -i filename         # 忽略大小写查找
```

### which和whereis命令
```bash
# 查找命令的位置
which command_name          # 查找命令的路径
whereis command_name        # 查找命令、源代码和手册页的位置
type command_name           # 显示命令的类型和位置
```

## 系统信息和进程管理

### 系统信息
```bash
# 系统信息
uname -a                    # 显示所有系统信息
uname -r                    # 显示内核版本
hostname                    # 显示主机名
uptime                      # 显示系统运行时间和负载
whoami                      # 显示当前用户名
id                          # 显示用户和组ID
date                        # 显示当前日期时间
cal                         # 显示日历

# 硬件信息
lscpu                       # 显示CPU信息
lsmem                       # 显示内存信息
lsblk                       # 显示块设备信息
lsusb                       # 显示USB设备
lspci                       # 显示PCI设备
dmidecode                   # 显示硬件详细信息（需要sudo）

# 系统资源
free -h                     # 显示内存使用情况
df -h                       # 显示磁盘使用情况
du -h directory             # 显示目录大小
du -sh *                    # 显示当前目录下各项大小
lsof                        # 显示打开的文件
```

### 进程管理
```bash
# 查看进程
ps aux                      # 显示所有进程
ps -ef                      # 显示所有进程（不同格式）
ps -u username              # 显示特定用户的进程
pgrep process_name          # 查找进程ID
pidof process_name          # 查找进程ID

# 实时监控
top                         # 实时显示进程状态
htop                        # 更友好的进程监控（需要安装）
iotop                       # 显示IO使用情况（需要sudo）
iftop                       # 显示网络使用情况（需要sudo）

# 进程控制
kill PID                    # 终止进程
kill -9 PID                 # 强制终止进程
killall process_name        # 终止所有同名进程
pkill process_name          # 按名称终止进程

# 后台作业管理
command &                   # 在后台运行命令
jobs                        # 显示后台作业
fg %1                       # 将作业1调到前台
bg %1                       # 将作业1放到后台
nohup command &             # 运行命令并忽略挂起信号
```

## 网络命令

### 网络配置和状态
```bash
# 网络接口配置
ip addr show                # 显示网络接口信息
ip link show                # 显示网络接口状态
ifconfig                    # 显示网络接口配置（传统命令）
iwconfig                    # 显示无线网络配置

# 路由信息
ip route show               # 显示路由表
route -n                    # 显示路由表（传统命令）
netstat -rn                 # 显示路由表

# 网络连接
netstat -tuln               # 显示监听端口
netstat -tupln              # 显示所有网络连接
ss -tuln                    # 现代版netstat
ss -tupln                   # 显示所有网络连接和进程

# 网络工具
ping hostname               # 测试网络连接
ping -c 4 hostname          # ping 4次
traceroute hostname         # 跟踪网络路径
nslookup hostname           # DNS查询
dig hostname                # DNS查询（更详细）
wget URL                    # 下载文件
curl URL                    # 获取网页内容
```

### 防火墙管理
```bash
# UFW (Ubuntu防火墙)
sudo ufw status             # 查看防火墙状态
sudo ufw enable             # 启用防火墙
sudo ufw disable            # 禁用防火墙
sudo ufw allow 22           # 允许SSH端口
sudo ufw allow ssh          # 允许SSH服务
sudo ufw deny 80            # 拒绝HTTP端口
sudo ufw delete allow 80    # 删除规则
sudo ufw reset              # 重置所有规则
```

## 包管理

### APT包管理器
```bash
# 更新包列表
sudo apt update

# 升级已安装的包
sudo apt upgrade
sudo apt full-upgrade       # 完整升级

# 安装包
sudo apt install package_name
sudo apt install package1 package2  # 安装多个包
sudo apt install -y package_name    # 自动确认安装

# 删除包
sudo apt remove package_name        # 删除包但保留配置
sudo apt purge package_name         # 完全删除包和配置
sudo apt autoremove                 # 删除不需要的依赖包

# 搜索包
apt search keyword
apt list --installed         # 列出已安装的包
apt list --upgradable        # 列出可升级的包
apt show package_name        # 显示包信息

# 修复安装
sudo apt --fix-broken install
sudo dpkg --configure -a    # 配置未完成的包
```

### Snap包管理器
```bash
# 查看snap包
snap list                   # 列出已安装的snap包
snap find keyword           # 搜索snap包

# 安装snap包
sudo snap install package_name
sudo snap install --classic package_name  # 经典模式安装

# 更新snap包
sudo snap refresh           # 更新所有snap包
sudo snap refresh package_name  # 更新特定包

# 删除snap包
sudo snap remove package_name

# 查看snap信息
snap info package_name
```

## 用户和权限管理

### 用户管理
```bash
# 用户信息
whoami                      # 当前用户名
id                          # 当前用户和组ID
groups                      # 当前用户所属组
who                         # 显示登录用户
w                           # 显示登录用户详细信息
last                        # 显示登录历史

# 切换用户
sudo command                # 以管理员权限执行命令
sudo -u username command    # 以指定用户执行命令
su - username               # 切换到其他用户
su -                        # 切换到root用户

# 用户管理（需要sudo权限）
sudo adduser username       # 添加用户
sudo deluser username       # 删除用户
sudo usermod -aG group username  # 将用户添加到组
sudo passwd username        # 修改用户密码
```

### 文件权限
```bash
# 查看权限
ls -l file_name             # 查看文件权限

# 修改权限
chmod 755 file_name         # 设置权限为755
chmod +x file_name          # 添加执行权限
chmod -w file_name          # 移除写权限
chmod u+r,g+w file_name     # 用户添加读权限，组添加写权限

# 修改所有者
sudo chown username file_name         # 修改文件所有者
sudo chown username:group file_name   # 修改所有者和组
sudo chown -R username directory      # 递归修改目录所有者

# 修改组
sudo chgrp group file_name            # 修改文件所属组
```

## 文本处理

### 文本操作命令
```bash
# 文本处理
sort file_name              # 排序文件内容
sort -r file_name           # 反向排序
sort -n file_name           # 数值排序
uniq file_name              # 去重（需要先排序）
cut -d':' -f1 /etc/passwd   # 按分隔符切割文本
awk '{print $1}' file_name  # 打印第一列
sed 's/old/new/g' file_name # 替换文本

# 字符统计
wc file_name                # 统计行数、词数、字符数
wc -l file_name             # 只统计行数
wc -w file_name             # 只统计词数
wc -c file_name             # 只统计字符数

# 文本比较
diff file1 file2            # 比较两个文件
cmp file1 file2             # 比较文件内容
```

### 重定向和管道
```bash
# 输出重定向
command > file              # 重定向输出到文件（覆盖）
command >> file             # 重定向输出到文件（追加）
command 2> file             # 重定向错误输出
command &> file             # 重定向所有输出

# 管道
command1 | command2         # 将command1的输出作为command2的输入
ls -l | grep ".txt"         # 列出txt文件
ps aux | grep nginx         # 查找nginx进程
cat file | sort | uniq      # 排序并去重

# 输入重定向
command < file              # 从文件读取输入
command << EOF              # Here文档输入
```

## 压缩和解压

### tar命令
```bash
# 创建压缩包
tar -czf archive.tar.gz directory/     # 创建gzip压缩包
tar -cjf archive.tar.bz2 directory/    # 创建bzip2压缩包
tar -cf archive.tar directory/         # 创建未压缩的tar包

# 解压缩包
tar -xzf archive.tar.gz                # 解压gzip压缩包
tar -xjf archive.tar.bz2               # 解压bzip2压缩包
tar -xf archive.tar                    # 解压tar包
tar -xzf archive.tar.gz -C /path/      # 解压到指定目录

# 查看压缩包内容
tar -tzf archive.tar.gz                # 查看gzip压缩包内容
tar -tf archive.tar                    # 查看tar包内容

# 追加文件到压缩包
tar -rzf archive.tar.gz newfile        # 追加文件到压缩包
```

### 其他压缩工具
```bash
# zip/unzip
zip -r archive.zip directory/          # 创建zip压缩包
unzip archive.zip                       # 解压zip文件
unzip -l archive.zip                    # 查看zip内容

# gzip/gunzip
gzip file_name                          # 压缩文件
gunzip file_name.gz                     # 解压文件
zcat file_name.gz                       # 查看压缩文件内容
```

## 系统服务管理

### systemctl命令（SystemD）
```bash
# 服务状态
sudo systemctl status service_name     # 查看服务状态
sudo systemctl is-active service_name  # 检查服务是否运行
sudo systemctl is-enabled service_name # 检查服务是否开机启动

# 服务控制
sudo systemctl start service_name      # 启动服务
sudo systemctl stop service_name       # 停止服务
sudo systemctl restart service_name    # 重启服务
sudo systemctl reload service_name     # 重新加载服务配置

# 开机启动
sudo systemctl enable service_name     # 设置开机启动
sudo systemctl disable service_name    # 禁用开机启动

# 查看服务
systemctl list-units --type=service    # 列出所有服务
systemctl list-unit-files --type=service  # 列出服务单元文件

# 查看日志
journalctl -u service_name              # 查看服务日志
journalctl -u service_name -f           # 实时跟踪服务日志
journalctl --since "2023-01-01"         # 查看指定时间后的日志
```

## 定时任务

### cron任务
```bash
# 编辑cron任务
crontab -e                  # 编辑当前用户的cron任务
sudo crontab -e             # 编辑root用户的cron任务
crontab -l                  # 列出当前用户的cron任务
crontab -r                  # 删除所有cron任务

# cron时间格式: 分 时 日 月 周 命令
# 示例：
# 0 2 * * *     /path/to/script.sh    # 每天凌晨2点执行
# */5 * * * *   /path/to/script.sh    # 每5分钟执行
# 0 0 1 * *     /path/to/script.sh    # 每月1号执行

# 查看cron日志
grep CRON /var/log/syslog   # 查看cron执行日志
```

## 环境变量和别名

### 环境变量
```bash
# 查看环境变量
env                         # 显示所有环境变量
echo $PATH                  # 显示PATH变量
echo $HOME                  # 显示家目录
printenv                    # 显示环境变量

# 设置环境变量
export VAR_NAME=value       # 临时设置环境变量
export PATH=$PATH:/new/path # 添加路径到PATH

# 永久设置环境变量（添加到以下文件之一）
# ~/.bashrc                 # 用户级bash配置
# ~/.profile                # 用户级配置
# /etc/environment          # 系统级环境变量
```

### 别名设置
```bash
# 查看别名
alias                       # 显示所有别名

# 设置临时别名
alias ll='ls -la'
alias la='ls -la'
alias l='ls -CF'
alias ..='cd ..'
alias ...='cd ../..'
alias grep='grep --color=auto'

# 永久别名（添加到~/.bashrc）
echo "alias ll='ls -la'" >> ~/.bashrc
source ~/.bashrc            # 重新加载配置

# 删除别名
unalias alias_name
```

## 实用技巧

### 历史命令
```bash
# 命令历史
history                     # 显示命令历史
history | grep keyword      # 搜索历史命令
!n                          # 执行历史中第n条命令
!!                          # 执行上一条命令
!string                     # 执行最近以string开头的命令
Ctrl+r                      # 反向搜索历史命令
```

### 快捷键
```bash
# 常用快捷键
Ctrl+c                      # 取消当前命令
Ctrl+z                      # 暂停当前命令
Ctrl+d                      # 退出终端或结束输入
Ctrl+l                      # 清屏
Ctrl+a                      # 光标移到行首
Ctrl+e                      # 光标移到行尾
Ctrl+u                      # 删除光标前的内容
Ctrl+k                      # 删除光标后的内容
Ctrl+w                      # 删除光标前的单词
Tab                         # 自动补全
```

### 通配符
```bash
# 通配符使用
*                           # 匹配任意字符
?                           # 匹配单个字符
[abc]                       # 匹配a、b或c
[a-z]                       # 匹配a到z的任意字符
[!abc]                      # 匹配除a、b、c外的字符
{file1,file2}               # 匹配file1或file2

# 示例
ls *.txt                    # 列出所有txt文件
rm file?.log                # 删除file1.log, file2.log等
cp file[1-3].txt backup/    # 复制file1.txt到file3.txt
```

## 故障排除

### 常用故障排除命令
```bash
# 磁盘问题
df -h                       # 检查磁盘空间
du -sh /*                   # 检查根目录各目录大小
lsof +D /path               # 查看目录下打开的文件
fuser -v /path              # 查看使用文件/目录的进程

# 内存问题
free -h                     # 查看内存使用
ps aux --sort=-%mem         # 按内存使用排序进程
top -o %MEM                 # 按内存使用排序显示进程

# 网络问题
ping -c 4 8.8.8.8          # 测试网络连通性
netstat -tuln | grep :80   # 检查80端口是否监听
ss -tuln | grep :80        # 现代版netstat
sudo netstat -tulpn        # 显示进程和端口

# 日志查看
tail -f /var/log/syslog     # 实时查看系统日志
journalctl -xe              # 查看详细系统日志
dmesg                       # 查看内核消息
```

### 系统维护
```bash
# 清理系统
sudo apt autoremove         # 删除不需要的包
sudo apt autoclean          # 清理包缓存
sudo journalctl --vacuum-time=3d  # 清理3天前的日志
sudo find /tmp -type f -atime +7 -delete  # 删除7天前的临时文件

# 检查系统
sudo fsck /dev/sdaX         # 检查文件系统
sudo badblocks -v /dev/sdaX # 检查坏块
memtest86+                  # 内存测试（重启后选择）
```

---

> **提示**: 
> - 使用 `man command_name` 查看命令的详细手册
> - 使用 `command_name --help` 查看命令的简要帮助
> - 使用 `which command_name` 确认命令是否存在
> - 在不确定的情况下，先在测试环境中尝试命令，特别是涉及删除和修改的操作
