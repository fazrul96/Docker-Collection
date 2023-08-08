1docker pull minio/minio

docker run -p 9000:9000 -p 9001:9001 --name s3 quay.io/minio/minio server /data --console-address ":9001"

RootUser: minioadmin
RootPass: minioadmin