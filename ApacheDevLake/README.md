# Summer Song开源集市项目 —— Apache DevLake

![Apache DevLake](https://github.com/apache/incubator-devlake/raw/main/img/logo.svg)

## 项目地址

官网：https://devlake.apache.org/

文档：https://devlake.apache.org/docs/Overview/Introduction

代码: https://github.com/apache/incubator-devlake


## 任务发布

### 任务1：运行DevLake并完成对 Apache DevLake 的 Github issues 收集

#### 任务内容

1. 根据 [Install via Docker Compose](https://devlake.apache.org/docs/GettingStarted/DockerComposeSetup) 文档所示，成功启动 Apache DevLake
2. 根据 [Configuring Github](https://devlake.apache.org/docs/UserManuals/ConfigUI/GitHub)，建立 Github connection, 并完成 Issue Tracking 的收集(注意 Step 2 的 Data Entities 仅保留 Issue Tracking 即可，其它的移除)
3. **可选** 用数据库管理工具，连接到 docker-compose 启动的 mysql 数据库，确认 issues 表有数据

#### 任务奖励

礼品- T恤


### 任务2：成功搭建DevLake开发环境

#### 任务内容

1. 安装 golang 语言环境
2. 克隆 Apache DevLake 代码仓库 https://github.com/apache/incubator-devlake
3. 以独立模式运行 github 插件并收集 issues 数据
   ```sh
   go run plugins/github/github.go -c 1 -o apache -r incubator-devlake -t collectApiIssues,extractApiIssues,convertIssues
   ```
   其中, `-c` 指定 github connection id ，可从 config-ui 中查看或连接到数据库查看 `_tool_github_connections` 表取得。`-o` 和 `-r` 分别指定仓库的所有者的具体的仓库。`-t` 指定要跑的子任务
4. **可选** 用数据库管理工具，连接到 docker-compose 启动的 mysql 数据库，确认 issues 表有数据

#### 任务奖励

礼品-笔记本礼盒 


### 任务3：完成以上两项或现场提PR并合入

#### 任务内容

- 完成任务1和任务2
- 或解决现场提供的任意 issue，现场完成PR并合入


#### 任务奖励

手机支架

