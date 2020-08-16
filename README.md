# k8s spec files

<br>

Kubernetes spec files for [karthikasasanka/fastapi-celery-redis-rabbitmq](https://github.com/karthikasasanka/fastapi-celery-redis-rabbitmq)

<br>

### How to start sevices 

```bash
git clone https://github.com/karthikasasanka/fastapi-celery-redis-rabbitmq-k8s-specs
cd shopping-api-k8s-specs
kubectl create -f .
```

This will expose fastapi application on 5000 and celery flower on 5555

swagger docs - `http://localhost:5000/`

redoc - `http://localhost:5000/redoc`

celery flower - `http://localhost:5555`

### Prerequisite

  * working setup of kubernetes and kubectl(refer: [Kubernetes](https://kubernetes.io/docs/tasks/tools/))


### Cleanup

```bash
kubectl delete services,deployments -l app=shopping
```
