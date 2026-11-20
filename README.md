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
