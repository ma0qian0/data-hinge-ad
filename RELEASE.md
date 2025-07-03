# 星枢数据中台版本发布记录

## 1.0.2

**发布日期**：2025-07-03

**发布日志**：

【基础版】

1. 增加airflow调度引擎，支持openmetadata元数据采集
2. 增加telegraf+influxdb+grafana(TIG)监控体系
3. 优化部署文档

【增强版】

1. 增加dolphinscheduler元数据血缘增量解析写入openmetadata



## 1.0.1

**发布日期**：2025-06-30

**发布日志**：

【基础版】

1. 修复数据中台门户切换用户登录不成功的问题
2. 修改postgresql镜像为bitnami/postgresql:15.10.0，涉及的子应用使用独立的账号和权限
3. 增加容器日志清理策略
4. 增加数据库备份策略
5. 优化部署文档



## 1.0.0

**发布日期**：2025-06-18

**发布日志**【基础版】

基础版产品功能及核心组件：
1. 数据门户：jeecgboot/ruoyi+keycloak
2. 数据调度：dolphinscheduler
3. 离线数据开发：clickhouse/doris
4. 实时数据开发：dinky+flink
5. 全链路数据血缘：openmetadata
6. 数据质量：dolphinscheduler/openmetadata
7. 数据服务：magicapi

| 服务类型         | 服务名称                | 版本            | 备注                                                   |
| ---------------- | ----------------------- | --------------- | ------------------------------------------------------ |
| database         | mysql                   | 8.0.39          | portal后端数据库                                       |
|                  | postgresql              | 15.10.0         | keycloak/dolphinscheduler/openmatadata/dinky后端数据库 |
|                  | redis                   | bullseye        | 缓存服务                                               |
|                  | clickhouse              | 25.4.3          | OLAP                                                   |
| portal           | keycloak                | 18.0.2          | 统一单点登录服务                                       |
|                  | nginxWebUi              | 4.2.0           | nginx可视化配置                                        |
|                  | portal-server           | 3.8.0-20250623  | jeecgboot框架后端                                      |
| 中间件           | zookeeper               | 3.7.1           | dolphinScheduler服务依赖                               |
|                  | kafka                   | 4.0             | 实时开发可能需要的依赖                                 |
|                  | flink                   | 1.20.0          | 实时开发需要的依赖                                     |
| dolphinscheduler | dolphinScheduler-api    | v3.2.2-20250618 | 离线开发平台                                           |
|                  | dolphinScheduler-master | 3.2.2           |                                                        |
|                  | dolphinScheduler-worker | v3.2.2-20250527 |                                                        |
|                  | dolphinScheduler-alert  | 3.2.2           |                                                        |
| openmatadata     | openmatadata-server     | 1.7.1           | 数据治理平台                                           |
| magicapi         | magicapi                | v2.1.1-20250530 | 数据服务                                               |
| dinky            | dinky                   | 1.2.3           | 实时开发平台                                           |
| kafka-ui         | kafka-ui                | 7073c72         | kafka可视化管理前端                                    |

