# docker-prometheus
Prometheus docker stack

## What is included in this stack?
* Prometheus
* Prometheus Pushgateway
* Grafana

## Configuration

### Prometheus
There are only two configuration changes made from the default Prometheus images:
1. Set the scrape interval to every 15 seconds.
2. Provision the Pushgateway job so that it's automatically scraped.

* Further configuration changes are possible by modifying the file `./conf/prometheus/prometheus.yml`.

### Pushgateway
There are no configuration changes made from the default Pushgateway image.

### Grafana
The following configuration changes have been made to the default Grafana image:
1. Configure administrator username and password.
2. Provision the Prometheus datasource in Grafana.

#### Setting Grafana Admin Username and Password
By default the stack sets the admin user to "admin" and the password to "password123". It is strongly encouraged that you change these values by setting your host environment variables `GR_ADMIN_USER` and `GR_ADMIN_PW` prior to deployment.

#### Further Grafana Configuration Options
* You can made additional changes to the Grafana instance congifuration by modifying the file `./conf/grafana/grafana.ini`
* You can configure additional datasource to be provisioned on startup by modifying the file `./conf/grafana/provisioning/datasources` directory contents.
