Install k8s
1. Install hyperkit in system
2. Install minikube (Minikube has kubectl dependency)

Commands
1. minikube start —vm-driver=hyperkit
2. kubectl get nodes (get the status of nodes)
3. minikube status (same as above) 

Note: minikube is generally used to create or delete the cluster, kubectl is used to manage, configure the minikube cluster.


Commmands for kubectl
1. Kubectl get nodes
2. kubectl get pods
3. kubectl get service

Lets create an nigix image
1. kubectl create deployment nginx-depl —image=nginx (basic command for creating pods)
2. kubectl get deployment
3. kubectl get replicates (no need to create/update/delete any replicates directly, only be working with deployments directly)

Layer of abstraction
1. Deployment manages a…
2. Replicaset manages a…
3. Pod manages a…
4. Container
5. Everything below deployment is handled by Kubernetes

To edit deployment
1. kubectl edit deployment <name>

Debugging pods
1. kubectl logs <pod name>
2. kubectl exec -it <pod name> — bin/bash
3. kubectl describe pod <pod name>

Deleting deployment
1. kubectl delete deployment <deployment name>

Using YAML file:
1. kubectl apply -f <filename>

BASE64 encode for secrets
1. echo -n '<secret>' | base64
2. echo QWxhZGRpbjpvcGVuIHNlc2FtZQ== | base64 --decode
