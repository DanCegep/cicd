# Projet CI/CD

Projet pour réaliser un CI/CD simple à l'aide d'outils gratuit.

Vous devez vous créez un compte sur :
-  Github
-  Docker-hub
-  CircleCI


# 
# 1. Basez-vous sur le lien ci dessous.
https://k21academy.com/devops-job-bootcamp/end-to-end-ci-cd-pipeline-setup-for-kubernetes-with-circleci-a-beginners-guide/#4

Commencer au  Step 2: Create a Simple Application. Créer le répertoire dans /home/etudiant/Documents/project.
Faire Step 3 
Faire step 4, mais prendre le fichier config.yaml qui se trouve dans ce projet dans le répertoire CircleCI
Faire step 5
Ne pas faire step 6, mais copier le répertoire k8 et modifier le fichier pour mettre votre dockerhub-username "image: your-dockerhub-username/my-k8s-app:latest"

Faire les commande suivant dans ton visualstudio code

git add .
git commit -m "Add CircleCI configuration and Kubernetes deployment"
git push -u origin master

# 2. Configurer CircleCI

Aller sur https://app.circleci.com/home

Créer une organisation  (Start a new organization - Organizations are shared contexts for people and projects on CircleC)

Faire les étapes dans https://circleci.com/docs/deploy/set-up-circleci-deploys/#set-up-circleci-deploys

Attention : mettre les bons namespace
![image](https://github.com/user-attachments/assets/0e105b8a-da01-471d-9ede-a0aac95c37cd)

Une fois que vous avez fait la commande helm upgrade --install circleci-release-agent-system
Demandez à l'enseignant de venir vérifier votre installation.


Pour valider

helm list --namespace circleci-release-agent-system

kubectl get all --namespace circleci-release-agent-system

Et voir que l'agent est Online sur le site.

# 3. Ajouter le manifeste du projet.

Ajouter le réperoire k9 de ce projet. Ce répertoire contient les manifestes.

Modifier les manifestes avec les info de votre projet CircleCI.

Aller sur Organization settings et prenez le "Organization ID" de votre projet.

![image](https://github.com/user-attachments/assets/7b9cc8c9-4f72-4b85-8dac-911c55ffa0a6)


# 3. Déploiyez l'agent avec helm

Faire les étapes 1 à 7

https://devtron.ai/blog/the-complete-guide-to-circleci-pipelines-for-kubernetes-2/#connect-circleci-dashboard-to-github

Pour le fichier config.yml, utilisez celui qui se trouve dans ce projet.


