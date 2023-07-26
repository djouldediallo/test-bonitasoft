########################### Lien d'installation du minikube #####################################################

https://kubernetes.io/fr/docs/tasks/tools/install-minikube/



########################### 1) Deployement de l'application Bonita avec la base de de donnée h2 #############################

Pour deployer l'application bonita avec la base de donnée h2:
Placez vous dans le repertoire deploy-using-h2 avec la commande suivante:

cd deploy-using-h2/

Executer la commande ci dessous pour deployer l'application:

kubectl apply -k ./

Ensuite pour y acceder sur l'application executer la commande suivante et vous verrez l'URL :

minikube service bonita-service --url -n bonita

Pour y acceder voici les informations ci dessous:
LOGIN = bonita
Passworld = bonitalogin

### Pour supprimer le deployement ##

kubectl delete -k ./



######################### 2) Deployement de l'application Bonita avec la base de donnée PostgreSql #############################

Pour deployer l'application bonita avec la base de donnée PostgreSql 
Placez vous dans le repertoire deploy-using-h2 avec la commande suivante:

cd deploy-using-postgres/

Executer la commande ci dessous pour deployer l'immage:

kubectl apply -k ./

Ensuite pour y acceder sur l'application executer la commande suivante et vous verrez l'URL :

minikube service bonita-service-using-postgresql --url -n bonita

Pour y acceder voici les informations ci dessous:
LOGIN = tech_user
Passworld = secret

### Pour supprimer le deployement ##

kubectl delete -k ./



