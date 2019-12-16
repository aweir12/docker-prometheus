# docker-prometheus
Prometheus docker stack

## What is included in this stack?
* Prometheus
* Prometheus Pushgateway
* Grafana

## Configuration

### Prometheus
Currently, there are only two configuration changes made from the default Prometheus images.
1. Set the scrape interval to every 15 seconds.
2. Provision the Pushgateway job so that it's automatically scraped.

Further configuration changes are possible by modifying the file 
````console
./conf/prometheus/prometheus.yml
````