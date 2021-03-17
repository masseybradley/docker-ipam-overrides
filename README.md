# ipam overrides

```
COMPOSE_PROJECT_NAME=net1 docker-compose -f docker-compose.yml -f docker-compose.net1.yml up -d
COMPOSE_PROJECT_NAME=net2 docker-compose -f docker-compose.yml -f docker-compose.net2.yml up -d
```

```
docker inspect net1_nginx_1 --format {{.NetworkSettings.Networks.net1_default.IPAddress}}
172.28.0.2
docker inspect net2_nginx_1 --format {{.NetworkSettings.Networks.net2_default.IPAddress}}
172.29.0.2
```
