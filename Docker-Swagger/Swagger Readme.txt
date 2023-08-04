https://swagger.io/docs/open-source-tools/swagger-ui/usage/installation/

docker pull swaggerapi/swagger-ui

net stop winnat
net start winnat

docker run -p 80:8080 --name swagger swaggerapi/swagger-ui