Creating config from file
kubectl create configmap myconfigmap --from-file=env.conf

Creating config map
kubectl create configmap myconfigmap --from-literal=MYENV=Dev --from-literal=TIER=Dev
