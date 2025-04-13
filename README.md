# Projet CI/CD

Projet pour réaliser un CI/CD simple à l'aide d'outils gratuit.

Vous devez vous créez un compte sur :
-  Github
-  Docker-hub
-  CircleCI

# 1. Basez-vous sur le lien ci dessous.
https://k21academy.com/devops-job-bootcamp/end-to-end-ci-cd-pipeline-setup-for-kubernetes-with-circleci-a-beginners-guide/#4

Commencer au  Step 2: Create a Simple Application. Créer le répertoire dans /home/etudiant/Documents/project.
Faire Step 3 et 4, mais prendre le fichier config.yaml qui se trouve dans ce projet dans le répertoire CircleCI

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

# 3. Ajouter le manifeste de ce projet dans votre projet.

Apporté les modifications au manifeste avec les info à l'étape où vous êtes rendu.

![image](https://github.com/user-attachments/assets/a359da7d-f9f6-47ff-850e-6c988c16e601)



# 3. Déploiyez l'agent avec helm
https://circleci.com/docs/deploy/set-up-the-release-agent/

Faire les étapes 1 à 7

https://devtron.ai/blog/the-complete-guide-to-circleci-pipelines-for-kubernetes-2/#connect-circleci-dashboard-to-github

Pour le fichier config.yml, utilisez celui qui se trouve dans ce projet.


