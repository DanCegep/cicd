changer ces ligne pour vos lignes

            docker login -u $DOCKERHUB_USERNAME -p $DOCKERHUB_PASSWORD
            docker push dancegep/my-k8s-app:latest

ET

          name: Deploy to Kubernetes
          command: |
            kubectl set image deployment/my-k8s-deployment my-container=dancegep/my-k8s-app:latest
