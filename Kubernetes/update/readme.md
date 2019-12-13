 kubectl set image deployment/app-deployment app=172.20.102.146:5000/internal:latest
 
 kubectl rollout status deployment app-deployment