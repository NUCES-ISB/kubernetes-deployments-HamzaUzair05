# Flask App with PostgreSQL on Kubernetes

## Deployment Steps:
1. Apply ConfigMap & Secret:
   ```sh
   kubectl apply -f manifests/configmap/postgres-configmap.yaml
   kubectl apply -f manifests/secret/postgres-secret.yaml

kubectl apply -f manifests/deployment/postgres-deployment.yaml
kubectl apply -f manifests/service/postgres-service.yaml

kubectl apply -f manifests/deployment/flask-deployment.yaml
kubectl apply -f manifests/service/flask-service.yaml

kubectl get service flask-service

