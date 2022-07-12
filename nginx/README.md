# nginx application

## Usage

### Deploy Application

Create namespace, deployment, and service:

```sh
kubectl create ns nginx
kubectl apply -f nginx.yaml -n nginx
```

### Exposing Service

a. Using load balancer (requires [metallb](https://metallb.universe.tf/) for bare metal):

```sh
apply -f nginx-service.yml -n nginx
```

b. Using simple ingress:

```sh
apply -f ingress.yml -n nginx
```
