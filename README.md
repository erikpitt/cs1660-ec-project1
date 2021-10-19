# cs1660-ec-project1

## DockerHub URLs

* https://hub.docker.com/repository/docker/erikjoy/sa-frontend
* https://hub.docker.com/repository/docker/erikjoy/sa-webapp
* https://hub.docker.com/repository/docker/erikjoy/sa-logic

## Container Orchestration Instructions
_Note: Couldn't get it to deploy on GKE_
1. minkube start
2. kubectl create -f resource-manifests/sa-frontend-pod.yaml
3. kubectl apply -f resource-manifests/sa-frontend-pod.yaml
4. kubectl create -f resource-manifests/service-sa-frontend-lb.yaml
5. kubectl apply -f resource-manifests/sa-frontend-deployment.yaml
6. kubectl apply -f resource-manifests/sa-logic-deployment.yaml
7. kubectl apply -f resource-manifests/service-sa-logic.yaml
8. kubectl apply -f resource-manifests/sa-web-app-deployment.yaml
9. kubectl apply -f resource-manifests/service-sa-web-app-lb.yaml

## Container Registry Instructions
### sa-logic
1. docker pull erikjoy/sa-logic
2. docker tag erikjoy/sa-logic gcr.io/pristine-sum-326223/sa-logic
3. docker push gcr.io/pristine-sum-326223/sa-logic

### sa-webapp
1. docker pull erikjoy/sa-webapp
2. docker tag erikjoy/sa-webapp gcr.io/pristine-sum-326223/sa-webapp
3. docker push gcr.io/pristine-sum-326223/sa-webapp

### sa-frontend
1. docker pull erikjoy/sa-frontend
2. docker tag erikjoy/sa-frontend gcr.io/pristine-sum-326223/sa-frontend
3. docker push gcr.io/pristine-sum-326223/sa-frontend
