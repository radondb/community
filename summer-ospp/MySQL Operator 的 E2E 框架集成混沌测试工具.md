# 项目
MySQL Operator 的 E2E 框架集成混沌测试工具

# 项目描述
## 项目目标
为 RadonDB MySQL Kubernetes E2E 测试框架贡献至少一种混沌测试故障类型相关 API 及测试用例。

## 项目技术要求
- MySQL
- Kubernetes
- Go

## 背景
RadonDB MySQL Kubernetes 是基于 MySQL 的开源、高可用、云原生集群解决方案。RadonDB MySQL Kubernetes E2E 测试框架基于 Ginkgo v2 开发，用于对 RadonDB MySQL Kubernetes 进行自动化测试。

## 详情
本项目中使用的混沌测试平台为 Chaos Mesh，Chaos Mesh 使用CRD来定义故障类型。我们只需要编写 API 来创建用于注入故障的 CR，并在测试用例中调用。目前我们的测试框架已经支持了部分故障类型的注入，可以提供参考。

# 项目产出要求
至少完成一种混沌测试故障类型相关 API
- 编写相关测试用例

# 导师
-  [程润科](https://github.com/runkecheng)