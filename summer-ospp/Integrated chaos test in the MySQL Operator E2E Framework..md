# Integrated chaos test in the MySQL Operator E2E Framework

## Target
Contributes at least one chaos object API and test cases to the Radondb MySQL Kuberneve E2E test framework.

[Project Details](https://summer-ospp.ac.cn/#/org/prodetail/22a600078)

## Technical Requirements
- MySQL
- Kubernetes
- Golang

## Background
RadonDB MySQL is an open-source, cloud-native, highly availability cluster solutions based on MySQL. The Radondb MySQL Kubernetes E2E Test Framework is developed based on Ginkgo V2 for automation testing of RadondB MySQL Kubernetes.
 
## Description
The chaos test platform used in this project is Chaos Mesh. Chaos Mesh uses CRD to define chaos objects for fault injection. We can write apis to create a CR that is used to inject faults, and call them in the test case. At present, our e2e framework has supported the injection of some fault types, it can provide reference.

## Output Requirements
Complete at least one API related to chaotic test fault type
- Write relevant test cases

## Project Repository
https://github.com/radondb/radondb-mysql-kubernetes
