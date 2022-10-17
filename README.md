# DockerSwarm Monitoring

Monitoring service for Docker Swarm using: Prometheus / Grafana / cAdvisor / Node Exporter / Alert Manager.

## Features

- `Swarm cluster` monitoring;
- `Traefik` reverse proxy monitoring;
- Remote `docker hub` monitoring;

## Before install

- You need the Traefik to access services. First install the Traefik.

## Install

Set your options :

1. change `volumes`, `hosts`, `networks` info in `docker-stack.yml` file;
2. change source info in `prometheus/prometheus.yml` file;
3. change grafana `admin password` in `grafana/config.monitoring` file;
4. add `alert type` in `alertmanager/config.yml` file;


```shell
docker stack deploy -c docker-stack.yml monitoring
```

- Access Grafana: http(s)://grafana.*.*
- Access Prometheus: http(s)://prometheus.*.*
