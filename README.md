# k8s spec files

<br>

Kubernetes spec files for [karthikasasanka/fastapi-celery-redis-rabbitmq](https://github.com/karthikasasanka/fastapi-celery-redis-rabbitmq)

<br>

### How to start sevices 

```bash
git clone https://github.com/karthikasasanka/fastapi-celery-redis-rabbitmq-k8s-specs
cd fastapi-celery-redis-rabbitmq-k8s-specs
kubectl create -f .
```

Kubernetes will be assign random node ports for the services.


Get list of the services and corresponding nodeports,

``` 
kubectl get svc
```
output will be something similar to 
```
.
.
shopping-api             NodePort       10.109.89.230   <none>        5000:32021/TCP   18m
shopping-celery-flower   NodePort       10.101.72.146   <none>        5555:31744/TCP   18m
.
.
```
shopping api is accessable at 32021 and celery flower at 31744(nodeports may change)



## Kubernetes with minikube

services can be launched as below

```
minikube service shopping-api
minikube service shopping-celery-flower
 ```


## kubernetes with docker-desktop

services can be accessed with 

```
 http://localhost:<nodeport>
 ```


### Cleanup

```bash
kubectl delete services,deployments -l app=shopping
```

~~ [Kubernetes](https://kubernetes.io/)