# Mend Graph Service

## 1. Build
Build the project using Maven. Run the following command from the project root directory: 
````
mvn clean install
````

To crete docker container with the service, run
````
mvn clean install -Pdocker
````

## 2. Deploy
The docker container exposes port 80 for HTTP interface.
Run the docker image mapping the container port 80 to the host port according your needs.
````
docker run -p <host-port>:80 leonidsh/mend-graph-service-server
````

For example, if you like to map the service API in the container to host port 80, run as following:
````
docker run -p 80:80 leonidsh/mend-graph-service-server
````

## 3. Test
The service provides API visibility and documentation via Swagger UI:
http://localhost/graph/swagger-ui/index.html