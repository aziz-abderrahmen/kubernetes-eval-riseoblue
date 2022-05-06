 # kubernetes-eval-riseoblue 
 
 ## Connecter deux serveurs sur un cluster avec kubernetes
 

 ### Premier deploiment Redis : 
 
#### Pour deployer l'application, lancer la commande : 

kubectl apply -t redis-deployment-riseoblue.yaml


### Pour deployer le service, lancer la commande : 

kubectl apply -t redis-service-riseoblue.yaml



### Deuxieme deploiment Node-Redis : 

#### Lancer la commande : 

kubectl apply -t node-redis-deployment-riseoblue.yaml

### Pour le service Lancer la commande : 

kubectl apply -t node-redis-service-riseoblue.yaml


### Pour augmenter le nombre de pods tapez cette commande :

kubectl scale deployment node-redis-deployment --replicas=4




## Contexte 

### Tapez : 
kubectl get pods pour afficher les pods sur le cluster 
kubectl logs node-redis-riseoblue-{HASH} pour verifier que le serveur node-redis a bien etabli la connexion avec redis 

### Vous devez avoir ce msg dans le terminal : 
redis connected to redis://10.3.169.69 <br/>
listening at http://localhost:6379
