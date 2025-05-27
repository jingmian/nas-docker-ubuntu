# KasmWeb Ubuntu Noble Desktop 群晖NAS安装指南

## 项目简介

本项目提供了在群晖NAS上部署 kasmweb/ubuntu-noble-desktop 的完整解决方案，支持 ARM 和 x86_64 双架构。

## 系统要求

- 群晖 NAS（支持 ARM 或 x86_64 架构）
- Docker 已安装
- 可用存储空间

## 快速开始

### 1. 克隆项目

```bash
cd /volume1/docker
git clone https://github.com/your-repository/kasm-ubuntu.git
cd kasm-ubuntu
```

### 2. 设置权限

为确保正常运行，需要设置正确的权限：

```bash
chmod 777 data
```

### 3. 启动服务

您可以选择以下两种方式之一启动服务：

#### 方式一：使用群晖 Container Manager（推荐）

1. 打开群晖 DSM，进入 "Container Manager"
2. 点击左侧 "容器" -> 点击右上角 "添加" -> 选择 "从文件夹导入"
3. 选择路径：`/volume1/docker/kasm-ubuntu`
4. 系统会自动识别 docker-compose.yml 文件
5. 点击 "下一步"，确认配置信息
6. 点击 "应用" 开始构建和启动容器

#### 方式二：使用终端命令行

如果您更习惯使用命令行，可以通过 SSH 连接到群晖后执行以下命令：

```bash
cd /volume1/docker/kasm-ubuntu
docker-compose up -d
```

### 4. 访问服务

服务启动后，您可以通过浏览器访问：

```
https://您的群晖IP:12902
```

## 安全说明

- 服务使用 HTTPS 协议，确保数据传输安全
- 请确保使用强密码保护您的服务
- 建议在内网环境使用，如需外网访问请做好安全防护

## 注意事项

- 首次启动可能需要几分钟时间
- 请确保您的群晖NAS有足够的系统资源
- 建议定期备份数据目录

## 支持

如有问题，请通过以下方式获取支持：
- 提交 Issue
- 查看官方文档 