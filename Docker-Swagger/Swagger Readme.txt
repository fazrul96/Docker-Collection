net stop winnat
net start winnat

https://swagger.io/docs/open-source-tools/swagger-ui/usage/installation/
docker pull swaggerapi/swagger-ui
docker run -p 8081:8080 --name swagger swaggerapi/swagger-ui

https://swagger.io/docs/open-source-tools/swagger-editor/
docker pull swaggerapi/swagger-editor
docker run -p 8082:8080 swaggerapi/swagger-editor