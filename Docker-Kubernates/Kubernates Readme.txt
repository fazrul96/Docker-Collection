#Generate Token
kubectl apply -f create-service-cccount.yml
kubectl apply -f create-cluster-role-binding.yml
kubectl -n kubernetes-dashboard create token admin-user

#Kubernates Serve
kubectl proxy

#Get Service
kubectl get service

#Get Pod
kubectl get pods
kubectl describe pods
kubectl logs

#Get Deployment
kubectl get deployment

#Create Pod
kubectl create -f create-swagger-pod.yml
kubectl create -f create-swagger-editor-pod.yml

#Create Deployment
kubectl apply -f create-swagger-deployment.yml
kubectl apply -f create-swagger-editor-deployment.yml

#Create Ingress
kubectl apply -f create-swagger-ingress.yml

#Create Service
kubectl apply -f create-swagger-ingress.yml

#Expose Deployment
kubectl expose deployment swagger-deployment --type LoadBalancer --port 8081 --target-port 80

------------------------------------------ 1 line Command --------------------------
#Generate Token
kubectl apply -f create-service-account.yml ; 
kubectl apply -f create-cluster-role-binding.yml ; 
kubectl -n kubernetes-dashboard create token admin-user ; 
kubectl proxy --port=8080;

#Create Replica && View Replica
kubectl create -f create-swagger-pod.yml ;
kubectl apply -f create-swagger-deployment.yml ; 
kubectl apply -f create-swagger-service.yml ;
kubectl get pods ;
kubectl get deployment ;
kubectl get service ;
kubectl get ingress ;

#Delete Replica
kubectl delete pod swagger-pod ;
kubectl delete deployment swagger-deployment ;
kubectl delete service swagger-deployment ;

#Cleaning Up
kubectl delete services example-service
kubectl delete deployment hello-world

#Access Application
http://<node-ip>:<node-port>

------------------------------------------ Example --------------------------

1. Run a Hello World application in your cluster: Create the application Deployment using the file above:
kubectl apply -f hello-application.yml

kubectl get deployments hello-world
kubectl describe deployments hello-world

kubectl get replicasets
kubectl describe replicasets

kubectl expose deployment hello-world --type=NodePort --name=example-service

kubectl describe services example-service

kubectl get pods --selector="run=load-balancer-example" --output=wide

<public-node-ip>: localhost
<node-port>: kubectl describe services <serviceName>

curl http://localhost:32407

Ingress 
kubectl apply -f hello-ingress.yml

C:\Windows\System32\drivers\etc

<cluster-ip>-kubernetes IP
10.96.0.1       kubernates-hello-world-test.mfzrl.cyou
10.96.0.1 		kubernates-swagger-test.mfzrl.cyou
10.96.0.1		kubernates-grafana-test.mfzrl.cyou
10.96.0.1       jenkins-test.mfzrl.cyou
10.96.0.1       grafana-test.mfzrl.cyou
10.96.0.1       prometheus-test.mfzrl.cyou
10.96.0.1       swagger-test.mfzrl.cyou
10.96.0.1       swagger-editor-test.mfzrl.cyou
10.96.0.1       cypress-test.mfzrl.cyou
10.96.0.1       s3-test.mfzrl.cyou
