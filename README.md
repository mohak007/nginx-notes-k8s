# Notes App + Nginx on Kubernetes

This repo contains Kubernetes manifests to run:
- A notes app on `localhost/app`
- Nginx welcome page on `localhost/nginx`
- Root `/` shows the notes app (or nginx, depending on ingress config).

## How to deploy

```bash
kubectl apply -f nginx/deployment.yml
kubectl apply -f nginx/service.yml
kubectl apply -f nginx/ingress.yml
kubectl apply -f notes-app/deployment.yml
kubectl apply -f notes-app/service.yml
