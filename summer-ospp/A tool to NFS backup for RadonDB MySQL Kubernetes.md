# A tool to NFS backup for RadonDB MySQL Kubernetes


## Target
Intergrate all steps of RadonDB MySQL Kubernetes's NFS backup to a comand tool.

[Project Details](https://summer-ospp.ac.cn/#/org/prodetail/22a600067)

## Technical Requirements
- MySQL
- NFS
- Kubernetes Operator
- Golang

## Background
RadonDB MySQL Kubernetes supports deployment and management of RaodnDB MySQL clusters on Kubernetes or KubeShpere and automates tasks related to operating a RadonDB MySQL cluster.

## Description
Info: RadonDB MySQL Kubernetes not only support to backup database to S3 storage, but also support to backup database to NFS strorage. T NFS, and mount the local storage, or custome storage to achieve the flexiable backup and recovery.

Backup to NFS storage, need 3 steps as follow:

- create storageClass and  Persistent Volumn
- create NFS resource and Service
- bind NFS IP to Backup Resource, then apply the Backup Resource, do the Backup job

The project should make it automatically .

## Output Requirements
A tool to NFS backup for RadonDB MySQL Kubernetes.

## Project Repository
https://github.com/radondb/radondb-mysql-kubernetes
