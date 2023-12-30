## EKS-jenkins-CI-CD-AWS-docker
This is an overview of how to deploy into a kubernetes cluster from a Jenkins CI/CD through a private DockerHub, and a sequel to the repository # EKS-cluster-deployment-using-Jenkins 

The prerequisites of the project include the installation of Jenkins (from a docker image) on a container, setup of the jenkins server, docker, AWS cli, kubectl, AWS Iam authenticator and AWS credentials using jenkins.

Demo executed - Complete CI/CD Pipeline with DockerHub:
Created Deployment and Service for App deployment

![1  deployment yaml](https://github.com/opeyemiagbadero/EKS-jenkins-CI-CD-AWS-docker/assets/79456052/6405ab30-1317-4658-9a15-d886c03db832)


![2  service yaml](https://github.com/opeyemiagbadero/EKS-jenkins-CI-CD-AWS-docker/assets/79456052/b1907773-ada4-435f-9198-9b51a512ab5d)

Adjusted Jenkinsﬁle as used in the EKS-cluster-deployment-using-Jenkins repo to set environment variables with envsubst

![editted the Jenkinsfile to reflect the envsubst and the new environmental variables](https://github.com/opeyemiagbadero/EKS-jenkins-CI-CD-AWS-docker/assets/79456052/ca59e632-87a8-4902-9afc-15bf2d79d597)


Installed “gettext-base” tool inside Jenkins Container on the AWS Server to have envsubst available. 

![3  create a envsbust command for the place holders in the deployment and service files](https://github.com/opeyemiagbadero/EKS-jenkins-CI-CD-AWS-docker/assets/79456052/fd3398f2-5e86-42ad-a128-10910a7f2304)

Created Secret for DockerHub Registry in EKS cluster and added reference to Deployment ﬁle

![4  Create Secret for Dockerhub Credentials](https://github.com/opeyemiagbadero/EKS-jenkins-CI-CD-AWS-docker/assets/79456052/8b602d08-26a8-42ad-8373-ab2917293cac)


![5  Update Kubernetes Deployment in Kubernetes Deployment yaml file, reference the created secret in the imagePullSecrets section](https://github.com/opeyemiagbadero/EKS-jenkins-CI-CD-AWS-docker/assets/79456052/ce8d1745-609e-4ed3-aef8-4fab1db7c996)

Executed Jenkins Pipeline
![7  pipeline screenshot](https://github.com/opeyemiagbadero/EKS-jenkins-CI-CD-AWS-docker/assets/79456052/8a2d10c1-586a-4121-b990-3c0120a60d6f)
