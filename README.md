#### READ ME
Deployment repo for Polar Bookshop System

#### How to run docker-compose locally

```shell
cd docker
$ docker compose up -d

# Stop the containers when done
$ docker compose down
```

#### How to run K8s with Tilt

prerequisites:
```shell
# Create a new Kubernetes cluster named polar on top of Docker
$ minikube start --cpus 2 --memory 4g --driver docker --profile polar

# Up and run postgres
$ cd kubernetes/platform/development
$ kubectl apply -f services


$ kubectl delete -f services

# Up and run services
$ cd kubernetes/applications/development
$ tilt up



# Stop the cluster when done
$ tilt down

$ minikube stop --profile polar


```

#### Test

```shell
$ http POST :9002/orders isbn=1234567891 quantity=3
$ http GET :9002/orders
```