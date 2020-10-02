# Kubernetes Ingress Using Minikube

In this project, we have considered a use case where we are implementing Kubernetes Ingress.

## Use Case
```
Use Case
```

## Prerequisites
```
Prerequisites
```

## Steps
|Steps  |Task                                                              |Status            |
|-------|------------------------------------------------------------------|------------------|
|1.     |Created the k8s deployment with nginx pod for serving traffic.    |:heavy_check_mark:|
|2.     |Configure the *default.conf* inside the nginx pod.                |:heavy_check_mark:|       
|3.     |Create a k8s configmap using the *default.conf* file.             |:heavy_check_mark:|
|4.     |Created the k8s deployment for the simple Flask app.                     |:heavy_check_mark:|
|5.     |Created a k8s Ingress (nginx) and set up the hostname.            |:heavy_check_mark:|

kubectl port-forward service/python-service 5000:5000

kubectl create configmap nginx-config --from-file=default.conf

Enable ingress in minikube