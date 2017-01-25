# Jenkins stacks

## prometheus-grafana-df-proxy.yml

This stack sets up the node-exporter, cAdvisor, Prometheus, and Grafana

### Requirements

* logging-df-proxy.yml stack

```bash
docker stack deploy -c ../logging/logging-df-proxy.yml logging
```

### Deployment

```bash
docker stack deploy -c prometheus-grafana-df-proxy.yml metrics
```

Use `http://metrics_prometheus:9090` as Prometheus data source and `http://logging_elasticsearch:9200` for ElasticSearch.