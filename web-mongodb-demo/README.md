# Web App with MongoDB
In this example we have used: Deplyment, Service, ConfigMap, and Secret.

### Commands:
Run:
```shell
kubectl apply -f mongo-config.yaml
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo.yaml
kubectl apply -f webapp.yaml
```
Get all created components in the cluster:
```shell
 kubectl get all
 # Or:
 kubectl get pod
 kubectl get service
 kubectl get secret
 kubectl get configmap
 ```
 Details about something:
 ```shell
 kubectl describe service mongo-service
 kubectl logs service mongo-service
 ```
Pod logs:
```shell
kubectl logs <pod_id>
# keep listening and don't exit (stream the logs):
kubectl logs -f <pod_id>
```
Access the deployed app:
```shell
# Get minikube IP
minikube ip
# Or
kubectl get node -o wide
```