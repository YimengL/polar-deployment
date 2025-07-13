#### READ ME
Deployment repo for Polar Bookshop System

#### How to run

prerequisites:
```shell
# Create a new Kubernetes cluster named polar on top of Docker
$ minikube start --cpus 2 --memory 4g --driver docker --profile polar

# Stop the cluster when done
$ minikube stop --profile polar
```