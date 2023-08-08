docker run --privileged -d --restart=unless-stopped -p 8083:8080 -p 4443:443 --name rancher rancher/rancher

docker run --privileged -d --restart=unless-stopped -p 8083:8080 -p 4443:443 -e CATTLE_AGENT_VALIDATE_CERTS=false --name rancher rancher/rancher
