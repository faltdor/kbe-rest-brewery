# KUBERNETES COMMANDS

### GENERAL 

* kubectl get nodes
* kubectl config get-context
* kubectl get all
* kubectl logs <--tail=20 / -f > <POD NAME>
    
### CREATE DEPLOYMENT 
* kubectl create deployment kbe-rest --image springframeworkguru/kbe-rest-brewery --dry-run=client  -o=yaml > deployment.yml
* kubectl apply -f deployment.yml 

### CREATE SERVICE
* kubectl create service clusterip kbe-rest --tcp=8080:8080 --dry-run=client -o=yaml >> service.yml
* kubectl apply -f service.yml

### PORT FORWARDING
* kubectl port-forward service/kbe-rest 8080:8080