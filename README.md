# Spring Security 模块化示例

这个 Java 示例展示如何把 Spring Security 的基础配置、浏览器认证和演示应用分成多个 Maven 模块。可以从演示应用追到浏览器认证模块，再看核心模块如何被共享。

| 模块 | 阅读入口 |
| --- | --- |
| 聚合构建 | [父 POM](cancer-security/pom.xml) |
| 核心配置 | [core](cancer-security-core/) |
| 浏览器认证 | [browser](cancer-security-browser/) |
| API 模块 | [api](cancer-security-api/) |
| 演示应用 | [DemoApplication](cancer-security-demo/src/main/java/com/cancer/security/demo/CancerSecurityDemoApplication.java) |

## 本地验证

在仓库根目录运行 `mvn -f cancer-security/pom.xml clean verify` 验证聚合构建。运行演示应用前，按本机环境检查演示模块的配置。

## 示例应用的本地配置

启动示例前配置测试数据库和测试登录应用。示例从环境变量读取凭据。

| 入口 | 环境变量 |
| --- | --- |
| 数据库 | `DEMO_DATASOURCE_PASSWORD` |
| OAuth2 | `DEMO_OAUTH2_CLIENT_SECRET` |
| QQ 登录 | `DEMO_QQ_APP_ID`、`DEMO_QQ_APP_SECRET` |
| 微信登录 | `DEMO_WECHAT_APP_ID`、`DEMO_WECHAT_APP_SECRET` |

使用测试租户的凭据和回调地址验证登录流程。凭据由本机进程或部署环境提供。
