# Traefik notes

Some examples to deploy traefik as local reverse proxy or loadbalancer.

## Docker

├── docker
│   ├── conf
│   │   └── dynamic_conf.yml
│   └── docker-compose.yml

Add in docker-compose the value of `HOST` env var, and run `docker-compose up -d`

> NOTE: an example of tcp loadbalancer is available

## Kubernetes

├── kubernetes
│   ├── 01-configmap.yaml
│   ├── 02-deployment.yaml
│   └── 03-svc.yaml

Modify the dynamic config in `kubernetes/01-configmap.yaml`, and change the service url for your apps, then run:

``kubectl apply -f ./kubernetes/`

