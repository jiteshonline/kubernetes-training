Creating config from file
kubectl create configmap myconfigmap --from-file=env.conf

Creating config map
kubectl create configmap evnconfigmap --from-literal=MYENV-Dev --from-literal=MYTIER=Frontend
