# [Spring MVC] Web 框架分步入门

**课程：https://stahe.github.io/zh-springmvc-sept-2026/**

所有代码和课程的作者：**Claude**（Anthropic 的 AI），应 **Serge Tahé** 的请求编写——2026 年 9 月。

## 概述

本课程循序渐进地指导你使用 **Spring MVC**（Spring Boot 4）构建 Web 应用，由服务器生成 HTML 页面（**Thymeleaf** 视图）。它只假定你对 HTTP、HTML 和 Java 编程语言有基本了解。

课程由两部分组成：

- **28 个简短示例**，每个示例只聚焦一个概念，按章节组织：

| 章节 | 内容 | 示例 |
|---|---|---|
| 控制器、动作、路由 | 从浏览器到动作：路由、响应、重定向、服务和依赖注入 | 01–06 |
| 动作模型 | 请求参数：绑定、转换、验证、POST 请求、自定义绑定 | 07–12 |
| 视图及其模型 | Thymeleaf、模板和片段、辅助工具、表单、验证、Post/Redirect/Get | 13–21 |
| 国际化 | 双语应用（MessageSource、LocaleResolver） | 22 |
| 数据作用域 | 单例、请求和原型 Bean；Cookie | 23 |
| 请求生命周期 | Servlet 过滤器、拦截器、`@ControllerAdvice`、错误页面 | 24 |
| 身份验证与授权 | Spring Security、存放在 Cookie 中的 JWT 令牌、角色、验证码、速率限制 | 25–27 |
| 分层架构与数据访问 | Web / 业务 / DAO 层、Spring Data JPA、Hibernate、MySQL、事务 | 28 |

- **一个完整的案例研究**：用于安排诊所预约的 **RdvMedecins** 应用。它有三种角色（管理员、医生、患者）、日历、预约和取消功能、医生和客户管理、患者账户创建、防机器人保护，以及法语和英语界面。课程对它的每个文件都做了注释。

## 源代码

源代码可从课程中下载。它包括：

- `exemples/`：28 个示例，每个文件夹一个 Maven 模块；
- `rdvmedecins2-spring-mvc/`：案例研究。

## 技术

Java 21 · Spring Boot 4.1（Spring MVC、Spring Security、Spring Data JPA）· Thymeleaf · Hibernate · MySQL 8（或 MariaDB）· Maven（Maven Wrapper）· Bootstrap 5。

## 先决条件

- JDK 21（例如 Eclipse Temurin）；
- Visual Studio Code，以及“Extension Pack for Java”和“Spring Boot Extension Pack”扩展；
- MySQL 8（Windows 上的 Laragon）或 MariaDB，用于示例 28 和案例研究；
- curl。

这些工具的安装说明见课程附录。

## 运行示例或案例研究

```bash
# 运行一个示例（端口 5000），在其目录中执行
cd examples/01-structure
../mvnw spring-boot:run          # Windows：..\mvnw spring-boot:run

# 案例研究（端口 8081），先用 database/dbrdvmedecins2.sql 创建数据库
cd rdvmedecins2-spring-mvc
./mvnw spring-boot:run           # Windows：mvnw spring-boot:run
```

首次运行时，Maven Wrapper 会下载 Maven，然后下载各个库：你必须连接到互联网。
