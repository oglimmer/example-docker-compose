# All purpose docker compose

# Domains (fake domains)

You have to add these domains to your /etc/hosts

```
127.0.0.1 prometheus.example.com blog.example.com web.example.com traefik.example.com portainer.example.com grafana.example.com loki.example.com
```

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
