# jenkins application

## Usage

### Deploy Application

Create namespace, deployment, and service:

```sh
kubectl apply -f namespace.yml
kubectl apply -f deployment.yaml -n jenkins
```

### Exposing Service

a. Using load balancer (requires [metallb](https://metallb.universe.tf/) for bare metal):

```sh
apply -f service.yml -n jenkins
```

b. Using simple ingress:

```sh
apply -f ingress.yml -n jenkins
```
