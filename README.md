# Traefik notes

Some examples to deploy traefik as local reverse proxy or loadbalancer.

## Docker

```bash
├── docker
│   ├── conf
│   │   └── dynamic_conf.yml
│   └── docker-compose.yml
```

Add in `docker-compose.yml` the value of `HOST` env var, move into the docker folder and run:

```
docker-compose up -d
```

> NOTE: an example of tcp loadbalancer is available

## Kubernetes

```bash
├── kubernetes
│   ├── 01-configmap.yaml
│   ├── 02-deployment.yaml
│   └── 03-svc.yaml
```

Modify the dynamic config in `kubernetes/01-configmap.yaml`, and change the service url for your app, then run:

```
kubectl apply -f ./kubernetes/
```


