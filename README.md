# CICD Pipeline for Java Application to deploy on Kubernetes Cluster using Jenkins
This project is a CICD pipeline for deploying a Java application on a Kubernetes cluster using Jenkins. It uses Docker as the container runtime and Docker Hub as the container registry. The project also includes Sonarqube for code analysis and Helm for packaging and deploying on Kubernetes.

![Screenshot (309)](https://user-images.githubusercontent.com/70194383/230273138-02cd6fec-874d-46ea-90f2-c6a143ea145e.png)


## Technologies and Tools Used
* Kubernetes: Orchestration tool
* Docker: Container runtime
* Jenkins: CI/CD server
* Docker Hub: Container registry
* Helm: Package and deploy on Kubernetes
* Git: Version control system
* Maven: Build tool
* Sonarqube: Code analysis server

## Prerequisites
To use this project, you will need the following:

* A Kubernetes cluster
* Docker installed on your local machine
* Jenkins installed on your local machine or on a remote server
* A Docker Hub account
* Git installed on your local machine
* Maven installed on your local machine
* Sonarqube installed on your local machine or on a remote server


## Getting Started
To get started, follow these steps:

1. Clone this repository to your local machine:

~~~sh
git clone https://github.com/DIK-SHITA08/CICD_Kubernetes_Cluster_using_Jenkins.git
~~~

2. Build the Java application using Maven:
~~~sh
mvn clean install
~~~

3. Build the Docker image:
~~~sh
docker build -t <your-docker-hub-username>/<your-image-name>:<tag> .
~~~

4. Push the Docker image to Docker Hub:
~~~sh
docker push <your-docker-hub-username>/<your-image-name>:<tag>
~~~

5. Create a Kubernetes deployment using Helm:
~~~sh
helm install <your-release-name> ./helm-chart
~~~

6. Verify that the Java application is running on the Kubernetes cluster:
~~~sh
kubectl get pods
~~~

7. Set up a Jenkins job to automate the CICD pipeline. Use the ***Jenkinsfile*** included in this repository as a template.


## Contributing

If you would like to contribute to this project, please follow these steps:

1. Fork this repository to your own account.
2. Create a branch from the ***main*** branch with a descriptive name.
3. Make your changes and commit them with descriptive commit messages.
4. Push your changes to your forked repository.
5. Create a pull request to merge your changes into the ***main*** branch of this repository.


