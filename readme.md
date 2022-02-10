postgresql git:(master) ✗ echo example123 | base64


kubectl apply -f postgresql-persistent.yaml

kubectl apply -f postgresql-persistentclaim.yaml

kubectl apply -f postgresql-configMap.yaml

kubectl apply -f postgresql-secrets.yaml

kubectl apply -f postgresql-deployment.yaml

kubectl apply -f postgresql-service.yaml

kubectl get pv
kubectl get pvc 
minikube tunnel 

postgresql git:(master) ✗ kubectl get pod postgresql-dep-7fcb5784cc-n4xfp  --template='{{(index (index .spec.containers 0).ports 0).containerPort}}{{"\n"}}'
5432

postgresql git:(master) ✗ kubectl port-forward postgresql-dep-7fcb5784cc-n4xfp 6000:5432 
Forwarding from 127.0.0.1:6000 -> 5432
Forwarding from [::1]:6000 -> 5432