# All purpose docker compose

# Domains (fake domains)

You have to add these domains to your /etc/hosts

```
127.0.0.1 prometheus.example.com blog.example.com web.example.com traefik.example.com portainer.example.com grafana.example.com loki.example.com
```

# Content

## Traefik

We have traefik to handle
* TLS and the certificate renewals
* central http/https entrypoint and routing to the different containers

## Portainer

Can deploy additional containers, outside of docker-compose.yml

## Grafana

Displays data from Prometheus and Loki

## Loki

Event level database

## Prometheus

Time series database for metrics

## Promtail

Moves the access logs from Traefik into Loki / Grafana

## Logrotate

Rotates the access log file in Traefik once a day.

## Blog

Example blog.

## Web

Example web project.

# user/pass

All users password combinations are admin/admin

# run

```
docker compose up --build -d
```

# Access

This sample application uses the following domains:

```
https://traefik.example.com # secured by admin/admin
https://portainer.example.com # secured by admin/admin
https://grafana.example.com # secured by admin/admin
https://loki.example.com # secured by admin/admin
https://prometheus.example.com # secured by admin/admin
https://blog.example.com
https://web.example.com
```
