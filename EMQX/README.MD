# Summer Song 开源集市项目 —— EMQX

[![GitHub Release](https://img.shields.io/github/release/emqx/emqx?color=brightgreen&label=Release)](https://github.com/emqx/emqx/releases)
[![Docker Pulls](https://img.shields.io/docker/pulls/emqx/emqx?label=Docker%20Pulls)](https://hub.docker.com/r/emqx/emqx)
[![Slack](https://img.shields.io/badge/Slack-EMQ-39AE85?logo=slack)](https://slack-invite.emqx.io/)
[![Discord](https://img.shields.io/discord/931086341838622751?label=Discord&logo=discord)](https://discord.gg/xYGf3fQnES)
[![Twitter](https://img.shields.io/badge/Twitter-EMQ-1DA1F2?logo=twitter)](https://twitter.com/EMQTech)
[![Community](https://img.shields.io/badge/Community-EMQX-yellow)](https://askemq.com)
[![YouTube](https://img.shields.io/badge/Subscribe-EMQ%20中文-FF0000?logo=youtube)](https://www.youtube.com/channel/UCir_r04HIsLjf2qqyZ4A8Cg)

[EMQX 官网 https://emqx.io/zh ](https://emqx.io/zh)

EMQX 是一款全球下载量超千万的大规模分布式物联网 MQTT 服务器，单集群支持 1 亿物联网设备连接，消息分发时延低于 1 毫秒。为高可靠、高性能的物联网实时数据移动、处理和集成提供动力，助力企业构建关键业务的 IoT 平台与应用。

EMQX 自 2013 年在 GitHub 发布开源版本以来，获得了来自 50 多个国家和地区的 20000 余家企业用户的广泛认可，累计连接物联网关键设备超过 1 亿台。

## 项目地址

代码库：https://github.com/emqx/emqx

文档地址：https://www.emqx.io/docs/zh/v5.0/

## 任务发布

### 任务 1： 使用EMQX发布订阅消息

    1. 下载二进制包安装或使用docker部署EMQX
    2. 准备合适的MQTT 客户端，可使用EMQX 管理控制台内置的 Websocket MQTT 客户端、[ MQTTX ](https://github.com/emqx/MQTTX/releases)之类MQTT桌面客户端、使用SDK(https://www.emqx.com/zh/mqtt-client-sdk)自行编写客户端等
    3. 向EMQX发布消息，并能够订阅成功

### 任务 2： 使用EMQX规则只订阅预期消息

    1. 使用EMQX 管理控制台创建规则，编写SQL将指定topic1消息转发到另外topic2
    2. 使用MQTT 客户端发布消息到topic1,topic2只订阅到经过处理的消息
   
