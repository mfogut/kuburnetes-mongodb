#Kuburnetes MongoDB Deployment and Service
- 1 - Create deployment configuration file. See 'mongodb-deployment.yaml'
- 2 - Create secret configuration file in order to put MongoDB env variable. (root username and password.)
- 3 - In order to deploy mongodb-deployment.yaml file first you have to deploy mongodb-secret file because deployment file variable depends to secret file.
    - kubectl apply -f mongodb-secret.yaml
- 4 -  Deploy mongodb-deployment file.
    - kubectl apply -f mongodb-deployment.yaml
- 5 - Deploy mongodb-servive file.
    - kubectl apply -f mongodb-service.yaml

#Kubernetes MongoExpress Deployment and Service
- 1 - Create deployment configuration file. See 'mongodb-express-deployment.yaml'
- 2 - Create configmap file in order to put MongoExpress env variable.
- 3 - In order to deploy mongo-express-deployment file first you have to deploy mongo-configmap file because deployment file variable store in mongo-configmap file.
    - kubectl apply -f mongodb-configmap.yaml
- 4 - Deploy mongo-express-deployment file.
    - kubectl apply -f mongo-express-deployment.yaml
- 5 - Deploy mongo-express-service file.
- 6 - Test if Mongo Express reachable externally
    - minikube service <service-name>