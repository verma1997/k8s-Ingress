# Kubernetes Ingress Using Minikube

In this project, we have considered a use case where we are implementing Kubernetes Ingress.

|S.No.|Task                                                              |Status            |
|-----|------------------------------------------------------------------|------------------|
|1.   |Created the k8s deployment with nginx pod for serving traffic.    |:heavy_check_mark:|
|2.   |Dockerize a simple Flask app.                                     |:heavy_check_mark:|
|3.   |Created the k8s deployment for the Flask app.                     |:heavy_check_mark:|       
|4.   |Created a k8s Ingress (nginx) and set up the hostname.            |:heavy_check_mark:|
|5.   |Configure the *default.conf* inside the nginx pod.                |:heavy_check_mark:|

kubectl port-forward service/python-service 5000:5000