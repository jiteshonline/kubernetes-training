Create HPA opject for autocalling myapp-deployment deployment
kubectl autoscale deploy myapp-deployment --min 1 --max 5 --cpu-percent 10

Generating loads to myapp-deployment
kubectl run -i --tty load-generator --rm --image=busybox --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://10.7.149.116:31000; done"
