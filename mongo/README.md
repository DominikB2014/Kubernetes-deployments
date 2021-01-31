All config files to create a basic k8s cluster with:
- Mongodb deployment
- Mongodb internal service
- Mongo-express deployment
- Mongo-express external service (for public access in a browser)
- K8s secret to store root user and password for mongo shared between the mongodb deployment and mongo-express deployment.
- K8s config to store a mapping between the mongodb service and its internal ip in order for mongo-express to connect to mongodb

### Request Path
Browser -> External mongo-express service -> mongo-express pod -> mongodb internal service -> mongodb pod

localhost:<port> -> <serviceExternalIp>:3000 -> mongo-express container -> <serviceInternalIp>:27017 -> mongodb container
