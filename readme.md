# GoSecure helm exercise

This helm chart will deploy two services, one will be a simple hello world web server and the other will be a nginx service that will act as a proxy to hello world.

## Dependencies
- Helm Version: v3.3.0
- Kubernetes: v1.16.5


### dry-run
helm install test .\ --dry-run

### install
helm install test .\

### test
kubectl get --namespace default -o jsonpath="{.spec.ports[0].nodePort}" services nginx-service
http://127.0.0.1:(port)

### uninstall
helm uninstall test


