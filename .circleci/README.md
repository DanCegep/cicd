changer ces lignes pour vos info de votre compte docker hub

ligne 17 et 21

     - run:
          name: Build Docker Image
          command: |
            docker build -t dancegep/my-k8s-app:latest .
      - run:
          name: Push Docker Image
          command: |
            docker login -u $DOCKERHUB_USERNAME -p $DOCKERHUB_PASSWORD
            docker push dancegep/my-k8s-app:latest
ET

ligne 37

          name: Deploy to Kubernetes
          command: |
            kubectl set image deployment/my-k8s-deployment my-container=dancegep/my-k8s-app:latest
