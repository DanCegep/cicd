# Projet CI/CD

Un CI/CD, c'est une chaîne automatisée qui aide les programmeurs à intégrer leur code, le tester et le déployer de manière automatisée. Vous n'êtes pas développeur, mais c'est souvent au spécialiste système de mettre en œuvre et supporter le mécanisme CI/CD.

Vous devez mettre en place un CI/CD simple sur un environnement Kubernetes.

Vous disposez déjà d'un cluster Kubernetes et d'une machine virtuelle qui vous facilitera la mise en œuvre de votre projet.

Vous réaliserez ce projet à l'aide d'outils gratuits.

Vous devez vous créer (avec votre courriel du cégep) un compte sur :
-  GitHub
-  Docker-hub
-  CircleCI


# Architecture

Vous avez un cluster Kubernetes avec 4 Namespace Dev, QA, Prépod et Prod. Vous devez créer un CICD en utilisant trois produits cloud gratuits.


GitHub : Plateforme de gestion de code collaboratif où le code est versionné et stocké. Il déclenche les pipelines CI/CD via des commits ou des pull requests. Il assure une collaboration fluide et une gestion centralisée du code.


Docker Hub: Registre pour héberger, partager et déployer des images Docker. Il garantit des déploiements standardisés et rapides dans divers environnements. Les équipes peuvent stocker et accéder facilement à leurs conteneurs.


CircleCI : Outil CI/CD qui automatise les tests, intégrations et déploiements de code. Il surveille les changements dans GitHub et garantit un déploiement fiable. Il minimise les erreurs humaines grâce à ses processus automatisés.


![image](https://github.com/user-attachments/assets/a4aacdee-01a8-421b-bbd8-a5c63835d7f5)



# 1. Configuration du Git


GitHub est une plateforme de gestion de versions basée sur Git, largement utilisée pour le développement collaboratif de logiciels. Elle permet aux informaticiens de sauvegarder leur code source, leurs scripts, leurs manifestes et tous les autres types de documentations. 

Permets de suivre les modifications effectuées et de travailler simultanément sur différents aspects d’un projet via des branches. 

Dans un pipeline CI/CD, GitHub agit comme le point central où le code est hébergé. Les modifications du code, via des commits ou des pull requests, peuvent déclencher des workflows automatisés, comme les tests ou les déploiements, grâce à l’intégration avec d’autres outils.

Cette étape met en place le dépôt de donnée qui servira de stockage du code.


[Consultez le guide sur GitHub](1.git.md)



# 2. Configuration du Docker Hub


Docker Hub est un registre cloud public qui permet de stocker, gérer et distribuer des images Docker. Une image Docker est un package contenant tout ce dont une application a besoin pour fonctionner, comme les bibliothèques, les dépendances et le code. 

Dans un processus CI/CD, Docker Hub est utilisé pour héberger les images créées à partir du code source. Ces images peuvent ensuite être récupérées et utilisées par des outils comme Kubernetes pour déployer l’application dans des environnements spécifiques, garantissant ainsi une compatibilité et une portabilité optimales.

Cette étape met en place votre registraire d'image docker.


[Consultez le guide sur Docker Hub](2.docker.md)



# 3. Configuration du CircleCI


CircleCI est une plateforme d’intégration et de déploiement continu (CI/CD) qui permet d’automatiser les étapes du pipeline de développement logiciel. Elle effectue des tests automatiques à chaque modification de code pour s’assurer de son bon fonctionnement, ce qui aide à identifier rapidement les erreurs ou les régressions. 

Dans notre projet, CircleCI automatisera le processus de construction d’images Docker, de leur envoi vers votre espace Docker Hub, puis de leur déploiement dans votre cluster Kubernetes. 

Sa flexibilité et sa capacité à s’intégrer facilement avec d’autres outils en font un choix populaire pour l’automatisation des workflows CI/CD.

Cette étape met en place le workflow CI/CD.


[Consultez le guide sur CircleCi](3.CircleCI.md)


# 4. Déployez et testez le pipeline

Maintenant que tout est en place et que tous nos environnements sont créés, déployons notre projets node.js et testons notre pipeline.

[Consultez le guide sur le déploiement et pipeline](4.deployer.md)




