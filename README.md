# Projet CI/CD

Un CI/CD, c'est une chaîne automatisée qui aide les programmeurs à intégrer leur code, le tester et le déployer de manière automatisée. Vous n'êtes pas développeur, mais c'est souvent au spécialiste système de mettre en œuvre et supporter le mécanisme CI/CD.

Vous devez mettre en place un CI/CD simple sur un environnement Kubernetes.

Vous disposez déjà d'un cluster Kubernetes et d'une machine virtuelle qui vous facilitera la mise en œuvre de votre projet.

Vous réaliserez ce projet à l'aide d'outils gratuits.

Vous devez vous créer (avec votre courriel du cégep) un compte sur :
-  GitHub
-  Docker-hub
-  CircleCI


# 
# 1. Configuration du Git


GitHub est une plateforme de gestion de versions basée sur Git, largement utilisée pour le développement collaboratif de logiciels. Elle permet aux informaticiens de sauvegarder leur code source, leurs scripts, leurs manifestes et tous autres types de documentations. 

Permets de suivre les modifications effectuées et de travailler simultanément sur différents aspects d’un projet via des branches. 

Dans un pipeline CI/CD, GitHub agit comme le point central où le code est hébergé. Les modifications du code, via des commits ou des pull requests, peuvent déclencher des workflows automatisés, comme les tests ou les déploiements, grâce à l’intégration avec d’autres outils.

Cette étape met en place le dépôt de donnée qui servira de stockage du code.


[Consultez le guide sur git](1.git.md)



# 2. Configuration du Docker Hub


Docker Hub est un registre cloud public qui permet de stocker, gérer et distribuer des images Docker. Une image Docker est un package contenant tout ce dont une application a besoin pour fonctionner, comme les bibliothèques, les dépendances et le code. 

Dans un processus CI/CD, Docker Hub est utilisé pour héberger les images créées à partir du code source. Ces images peuvent ensuite être récupérées et utilisées par des outils comme Kubernetes pour déployer l’application dans des environnements spécifiques, garantissant ainsi une compatibilité et une portabilité optimales.

Cette étape met en place votre registraire d'image docker.


[Consultez le guide sur docker hub](2.docker.md)



# 3. Configuration du CircleCI


CircleCI est une plateforme d’intégration et de déploiement continu (CI/CD) qui permet d’automatiser les étapes du pipeline de développement logiciel. Elle effectue des tests automatiques à chaque modification de code pour s’assurer de son bon fonctionnement, ce qui aide à identifier rapidement les erreurs ou les régressions. 

Dans notre projet, CircleCI automatisera le processus de construction d’images Docker, de leur envoi vers votre espace Docker Hub, puis de leur déploiement dans votre cluster Kubernetes. 

Sa flexibilité et sa capacité à s’intégrer facilement avec d’autres outils en font un choix populaire pour l’automatisation des workflows CI/CD.

Cette étape met en place le workflow CI/CD.


[Consultez le guide sur docker hub](3.circleCi.md)




