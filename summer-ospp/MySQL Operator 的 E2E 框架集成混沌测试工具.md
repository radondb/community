# 项目
MySQL Operator 的 E2E 框架集成混沌测试工具

# 项目描述
## 项目目标
为 RadonDB MySQL Kubernetes E2E 测试框架贡献至少一种混沌测试故障类型相关 API 及测试用例。

## 项目介绍

- ## 什么是 RadonDB MySQL？
  
  - K8s
  
  - 高可用
  
  - MySQL
  
  [k8s环境下的高可用MySQL集群](https://github.com/radondb/radondb-mysql-kubernetes/blob/main/README_zh.md)

- ## 什么是E2E(End-to-End)测试？
  
  端到端测试，推荐阅读：[What is End-to-End (E2E) Testing? | All You Need to Know (katalon.com)](https://katalon.com/resources-center/blog/end-to-end-e2e-testing)
  
  - 自动测试
  - 模拟真实用户场景

- ## 什么是混沌测试？
  
  - 模拟多种多样的故障注入（网络异常，io异常等）
  
  > Chaos mesh 官方文档：https://chaos-mesh.org/website-zh/docs/

## 示例

使用 yaml 创建 pod-kill 故障

```yaml
apiVersion: chaos-mesh.org/v1alpha1 
kind: PodChaos   
metadata:        
  name: pod-kill-example  
  namespace: chaos-testing
spec:
  action: pod-kill
  mode: one
  selector:
    namespaces:
      - default
    labelSelectors:
      'role': 'leader'
```

伪代码

```go
func killPod(action, mode string, selector Selector) *podChaos {
    //...
}
```

## 测试用例流程

1. 创建集群

2. 等待集群就绪

3. 注入故障

4. 观察集群状态

5. 打印报告


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