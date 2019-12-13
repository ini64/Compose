https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/

```console
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0-beta6/aio/deploy/recommended.yaml
kubectl proxy
```


http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/.

```console
kubectl apply -f admin-rolebinding.yaml
kubectl apply -f admin-user.yaml
```

kubectl -n kube-system describe secret > secret.txt find 

```consoel
Name:         admin-user-token-mwmkz
Namespace:    kube-system
Labels:       <none>
Annotations:  kubernetes.io/service-account.name: admin-user
              kubernetes.io/service-account.uid: c9bb3cb7-1d41-11ea-88e6-00155d669538

Type:  kubernetes.io/service-account-token

Data
====
ca.crt:     1025 bytes
namespace:  11 bytes
token:      eyJhbGciOiJSUzI1NiIsImtpZCI6IiJ9.eyJpc3MiOiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJrdWJlLXN5c3RlbSIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VjcmV0Lm5hbWUiOiJhZG1pbi11c2VyLXRva2VuLW13bWt6Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9zZXJ2aWNlLWFjY291bnQubmFtZSI6ImFkbWluLXVzZXIiLCJrdWJlcm5ldGVzLmlvL3NlcnZpY2VhY2NvdW50L3NlcnZpY2UtYWNjb3VudC51aWQiOiJjOWJiM2NiNy0xZDQxLTExZWEtODhlNi0wMDE1NWQ2Njk1MzgiLCJzdWIiOiJzeXN0ZW06c2VydmljZWFjY291bnQ6a3ViZS1zeXN0ZW06YWRtaW4tdXNlciJ9.iZxRHZsewlQfwsmkRhJZ7_k1vaWQ_PCCnfyck6Dj-0gd8INTCB-a-Sv1ZXvCeE3Y_EyMV5JwObEqkRTS6Lz7dK_9b1dskJ97-ILc5jK1d5xCz42JnN3zAjoWyBnQ1ncOE4fNA2L1ShrvX8OMymJGF2geCFmC38Qkq2iHL7y8IY-Gsman7vfCWUTiQesU40FFRWHyNuyq5AA8KI37pite5sFGiH_hhjKc2xLRuPAAW6JR2jSCfLmIzKM1xMRNXhWcuiYcwhpShrJBXV7Epw9-zcFHOBBr-Z0jaqMNizLh4U-QJLbIJay86UZF7tBQMuyeFewYSozKZRvw05RKKsYnPA
```
