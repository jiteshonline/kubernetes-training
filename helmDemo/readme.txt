Installing helm chart 
--------------------------
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
chmod 700 get_helm.sh
./get_helm.sh


----------------------------------------------------
1. Creting helm chart directtory setup
helm create mychart

2. installing chart
helm install myhelm-deploy mychart --set service.type=NodePort
helm list

3. Adding dependecy to Chart.yaml & dependency udpate
helm dependency update mychart

4. helm install myhelm-deploy2 mychart --set service.type=NodePort

5. helm delete myhelm-deploy2

6. helm uninstall myhelm-deploy

7. Packing chart for release
helm package mychart


-------------------------------------------
helm install nginx -n mynginx helm-example --dry-run
	nginx - name of the application/ deployment
	mynginx - namespace
	helm-example - location where chart present


helm list -n mynginx
helm list --all-namespaces


helm delete -n mynginx nginx

helm install nginx -n mynginx helm-example --set nginx-deployment.nginx-image=1.21.1 --dry-run
helm template helm-example helm-example
helm install nginx -n mynginx helm-example -f customvalues.yaml
helm upgrade nginx -n mynginx helm-example --values customvalues.yaml

Bitname NGINX chart
1. Got to helm artifacts
2. search for nginx
3. helm repo add bitnami https://charts.bitnami.com/bitnami
4. helm search repo nginx
5. helm pull bitnami/nginx
   helm pull bitnami/nginx --untar=true
6. helm install mynginx nginx
   helm install mynginx bitnami/nginx
