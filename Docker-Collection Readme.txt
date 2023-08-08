- docker commit 212116aef4e1 grafana-test:1.0
- docker commit e97ad639b545 prometheus-test:1.0
- docker commit abe17df1c220 jenkins-test:1.0
- docker commit 58f18a87cc22 swagger-test:1.0

1. Save to the disk your docker image:
docker save --output="image_name.tar" id_image

docker save --output="grafana-test.tar" d1a1ebbaaef7b7f73d23313ce028e892dfb6b884afb34b235865e4e832087101
docker save --output="prometheus-test.tar" 1e192cac5f6092af54d94e136c88d217a9d6eab3d39980c61b7e5528f62571c0
docker save --output="jenkins-test.tar" 0ce14a199ce2b1d5c3d8183c68d8a9e0bbb49a29c06c6fe6794a8714391c3bb2
docker save --output="swagger-test.tar" d6a74662bff72e470bf8207fab1a01a7f93311360f364600131febce0e6955b1

2. Load your docker image from the disc:
docker load --input grafana-test.tar --name grafana-test
docker load --input prometheus-test.tar --name prometheus-test
docker load --input jenkins-test.tar --name jenkins-test
docker load --input swagger-test.tar --name swagger-test

3. if after list images the repository and tag are < none >, you can rename your image setting new repository:tag
Docker tag new_repository:new_tag

----------------------------------
docker import - grafana-test:1.0