# 项目
一键备份 MySQL on Kubernetes 集群数据到 NFS 存储

# 项目描述
## 项目目标
将 RadonDB MySQL Kubernetes 的 NFS 备份步骤集成为一个命令。

## 项目技术要求
- MySQL
- NFS
- Kubernetes Operator
- Golang

## 背景
RadonDB MySQL Kubernetes 是基于 MySQL 的开源、高可用、云原生集群解决方案。支持一主多从高可用架构，并具备安全、自动备份、监控告警、自动扩容等全套管理功能。

RadonDB MySQL Kubernetes 支持在 Kubernetes 和 KubeSphere 上安装部署和管理，自动执行与运行 RadonDB MySQL 集群有关的任务。
 
RadonDB MySQL Kubernetes 除了可以将数据库备份到 S3 存储外，也可以将数据库备份到 NFS 存储。

## 详情
NFS 备份方式是用户在没有 S3 存储到情况下的备份方案。通过 NFS，用户挂载本地存储，自定义存储实现数据库灵活备份恢复。
 
NFS 备份，需要有三个步骤：
- 创建 StorageClass 与 Persistent Volumn
- 创建 NFS Resource 与 Service
- 绑定 NFS 的 IP 到 Backup Resource ，应用 Backup Resource，执行备份 Job

项目要求能自动进行上面三个步骤。

# 项目产出要求
实现一个命令行工具，能一条命令执行数据库的 NFS 备份。

# 参考文档

- https://github.com/radondb/radondb-mysql-kubernetes/
- https://kubernetes.io/zh/docs/home/
- https://radondb.com
- https://github.com/radondb/radondb-mysql-kubernetes/blob/main/docs/zh-cn/deploy_radondb-mysql_operator_on_k8s.md
- https://github.com/radondb/radondb-mysql-kubernetes/pull/232

# 导师
- [柯煜昌](https://github.com/acekingke)