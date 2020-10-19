# Kubernetes Ingress Using Minikube

In this project, we have considered a use case where we are implementing Kubernetes Ingress.

## Use Case
In this exercise, we are creating a simple Flask app, dockerizing it and deploying it on GKE. Also, deploying a NGINX pod and using that to route the traffic to the python application pod.


## Prerequisites

**1.** Install *kubectl*.
```
$ sudo apt-get update && sudo apt-get install -y apt-transport-https gnupg2 curl

$ curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -

$ echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list

$ sudo apt-get update

$ sudo apt-get install -y kubectl

```

**2.** Install Minikube.
- Commands to install Minikube in Linux. For more, click [here](https://minikube.sigs.k8s.io/docs/start/#binary-download).
```
$ curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

$ sudo install minikube-linux-amd64 /usr/local/bin/minikube

```

- To run Minikube, run the command `minikube start`. If minikube fails to start, see the [drivers](https://minikube.sigs.k8s.io/docs/drivers/) page for help setting up a compatible container or virtual-machine manager.
To check the status of Minikube, execute `minikube status`.


**3.** Enable the *ingress* addon in Minikube.
```
$ minkube addons list               // List all the addons available on Minikube

$ minikube addons enable ingress    // Enable the ingress addon on Minikube

```

## Steps
|Steps  |Task                                                              |Status            |
|-------|------------------------------------------------------------------|------------------|
|1.     |Created the k8s deployment with nginx pod for serving traffic.    |:heavy_check_mark:|
|2.     |Configure the *default.conf* inside the nginx pod.                |:heavy_check_mark:|       
|3.     |Create a k8s configmap using the *default.conf* file.             |:heavy_check_mark:|
|4.     |Created the k8s deployment for the simple Flask app.              |:heavy_check_mark:|
|5.     |Created a k8s Ingress (nginx) and set up the hostname.            |:heavy_check_mark:|

kubectl port-forward service/python-service 5000:5000

kubectl create configmap nginx-config --from-file=default.conf

Enable ingress in minikube