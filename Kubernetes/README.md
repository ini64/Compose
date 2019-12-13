
install windows docker 

turn on kubernets.

clone https://github.com/kubernetes-sigs/metrics-server

copy deploy folder

edit deploy/1.8+/metrics-server-deployment.yaml
add

```yaml
  imagePullPolicy: Always
  command:
  - /metrics-server
  - --kubelet-insecure-tls
  volumeMounts:
```

```cosole
kubectl delete -f deploy/1.8+/
kubectl apply -f deploy/1.8+
```
