## EKS-jenkins-CI-CD-AWS-docker
This is an overview of how to deploy into a kubernetes cluster from a Jenkins CI/CD through a private DockerHub, and a sequel to the repository # EKS-cluster-deployment-using-Jenkins 

The prerequisites of the project include the installation of Jenkins (from a docker image) on a container, setup of the jenkins server, docker, AWS cli, kubectl, AWS Iam authenticator and AWS credentials using jenkins.

Demo executed - Complete CI/CD Pipeline with DockerHub:
Created Deployment and Service for App deployment
Adjust Jenkinsﬁle to set environment variables with envsubst
Installed “gettext-base” tool inside Jenkins Container on DigitalOcean Server
to have envsubst available
Created Secret for DockerHub Registry in EKS cluster (connect to EKS
cluster if not already) and added reference to Deployment ﬁle
Executed Jenkins Pipeline
