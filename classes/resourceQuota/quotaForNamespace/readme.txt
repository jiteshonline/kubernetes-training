kubectl create namespace testing


1. kubectl apply -f  cpulimit.yaml --namespace=testing
   kubectl get resourcequota --namespace=testing


2. kubectl apply -f  deploy.yaml --namespace=testing
   Continers won't be created as limites on memory and cpu not defined.


3. kubectl apply -f  deploy1.yaml --namespace=testing
   Replica of 3 containers will be created.

4. kubectl apply -f  deploy2.yaml --namespace=testing
   Although 3 containers requested still will created only 1 as limit going higher than allowed in namespace

5. kubectl apply -f podlimit.yaml --namespace=testing
   Setting pod limit to 4 in a namespace

6. kubectl scale --replicas=5 deployment.apps/deployments --namespace=testing
   Although need 5 replicas of deployment still will create only 4 as pod limit set to 4

7. kubectl apply -f defaultMemCPU.yaml --namespace=testing
   Setting default memory value for containers

8. kubectl apply -f  deploy.yaml --namespace=testing
   Default values will be used for deployment


9. kubectl run -i --tty load-generator --rm --image=busybox --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://10.7.149.116:31000; done"
