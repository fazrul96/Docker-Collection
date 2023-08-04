https://grafana.com/docs/grafana/latest/setup-grafana/installation/docker/

https://grafana.com/docs/grafana/latest/getting-started/build-first-dashboard/


docker run -d -p 3000:3000 --name=grafana grafana/grafana-oss

docker run -d -p 9090:9090 --name=prometheus prom/prometheus:latest

- Test Connection from Grafana Container: Access the Grafana container's shell and try to ping the Prometheus container:

docker exec -it grafana /bin/sh
ping prometheus

- Test Connection to Prometheus API: Inside the Grafana container, try to use curl to fetch data from the Prometheus API:

docker exec -it grafana /bin/sh
curl http://prometheus:9090/api/v1/query?query=up