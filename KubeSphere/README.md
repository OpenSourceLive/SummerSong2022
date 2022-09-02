# KubeSphere

![https://raw.githubusercontent.com/kubesphere/kubesphere/master/docs/images/kubesphere-icon.gif]

## KubeSphere 项目地址

官网：https://kubesphere.com.cn/

文档：https://kubesphere.com.cn/docs/v3.3/

GitHub: https://github.com/kubesphere

## 任务


### 任务 1：在 KubeSphere 中部署 Redis

1. 使用帐户 project-regular （密码 P@88w0rd）登录控制台（http://139.198.27.132:30880）。

1. 依次点击**平台管理** --> **访问控制**，进入企业空间 `demo-workspace`。

2. 在**项目**中，进入 `demo-project` 项目的概览页面，点击左上角的应用商店。

4. 找到 Redis，点击**应用信息**页面上的**安装**。

5. 设置名称并选择应用版本。请确保将 Redis 部署在 `demo-project` 中，点击**下一步**。

6. 在**应用设置**页面，为应用指定持久化存储卷和密码。操作完成后，点击**安装**。

7. 稍等片刻待 Redis 启动并运行。

8. 转到**服务**页面，点击 Redis 的服务名称。

9. 在**容器组**中展开菜单查看容器详情，随后点击**终端**图标。

10. 在弹出窗口的终端中运行 `redis-cli` 命令来测试使用该应用：

```bash
$ redis-cli -a <your_password>
127.0.0.1:6379> PING
PONG
```


### 任务 2：使用 Argo CD 持续部署应用

1. 使用帐户 project-regular （密码 P@88w0rd）登录控制台（http://139.198.27.132:30880）。

2. 依次点击**平台管理** --> **访问控制**，进入企业空间 `demo-workspace`。

3. 在**DevOps 项目**中，进入 `demo-devops`。

4. 在**持续部署**中，点击**创建**，填写名称，选择代码仓库，然后点击**下一步**。

5. 将**部署位置**中的项目改为 `demo-project`，清单文件路径改为 `./dev`，并勾选**清理资源**和**自恢复**，然后点击创建。

6. 点击刷新按钮，确定健康状态是**健康**，同步状态是**已同步**，点击左上角的 `demo-devops`，然后选择**项目**，进入 `demo-project` 项目，依次选择**应用负载** --> **工作负载**，可以看到应用已经成功运行。