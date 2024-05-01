## Create

kubectl apply -f nginx-deployment.yaml
kubectl rollout status deployment/nginx-deployment

kubectl get pods -o wide

kubectl apply -f busybox.yaml
kubectl exec -ti busybox -- nslookup kubernetes.default

kubectl apply -f nginx-service.yaml
kubectl get svc nginx-service

curl http://<EXTERNAL-IP>

kubectl logs <pod-name>


## Destroy

kubectl delete deployment nginx-deployment
kubectl delete pod busybox
kubectl delete service nginx-service