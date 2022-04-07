# NodePort-K8S-Minikube
## This repo is to 
1- Create a deployment of 2 replicas using image of  linuxacademycontent/store-products:1.0.0.
2- Create a service of NodePort to expose this deployment outside the host.

## Setup environmet
I worked on Minikube hosted on virtualbox on vm (ubuntu) vmware workstation

## Commands to run
kubectl apply -f deployment.yml

### To make the deployment being exposed from outside
kubectl expose deployment myapp-deployment --type=NodePort --port=80

### To get the url of the app
minikube service myapp-deployment --url

### To acess the application 
curl <url>

