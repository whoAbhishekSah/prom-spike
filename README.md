# prom-spike
Analysing the Prometheus and Alert manager stack with CPU Load Alert test

Prometheus server scapes data from node_exporters running in background.

Example run on 8081 port: 
- `./node_exporter --web.listen-address 127.0.0.1:8081`

<hr>

Run Promteheus with config file:

Example run on given configuration file: `./prometheus --config.file=prometheus.yml`

Promtehus scrapes metrics from the `node_exporter` and you can view it in the built in expression browser or set up grafana on top this. 
Obviously, Grafana is the popluar choice here.

Alert rules can be defined with prometheus and put in yml files. (see prometheus config file) and viewed on alerts tab.

Prometheus UI Alert Tab : Default - http://localhost:9090/alerts

<hr>

The alerts are sent to Alertmanager. The receivers are controllerd via `alertmanager.yml` configuration file. 

Example run : `/alertmanager --config.file=alertmanager.yml`
