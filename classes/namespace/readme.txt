Command to Create namespace
kubectl create namespace <nameOfNamespace>

Command to create pod in a namespace
kubectl deploy -f abcd.yaml --namespace=<nameOfNamespace>

Command to get pods in a namespace
kubectl get pods --namespace=<nameOfNamespace>
kubectl get pod -n mynamespace

Command to get pods from all namespaces
kubectl get pods --all-namespaces

Command to find objects run in namespace
kubectl api-resources --namespaced=true

Command to find objects do not run in namespace
kubectl api-resources --namespaced=false

Command to context of namespace for all subsequent kubectl commands
kubectl config set-context $(kubectl config current-context) --namespace=mynamespace
