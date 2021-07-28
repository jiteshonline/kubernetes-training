1. Create headless service
2. Deploye stateful object
3. Deploy ubuntu pods for running nslookup command
	a. Install nslookup utility
		i. apt-get update
		ii. apt-get install dnsutils
4. get into the test pod
	kubectl exec -it testpod1 -- /bin/bash
5. Lookup on headless service nginx, it will list all the containers for this service
	nslookup nginx
6. Lookup for pod creted with stateful
	nslookup web-0.nginx
7. Create regular service, it will display IP address of service running on
	nslookup nginx-regular
