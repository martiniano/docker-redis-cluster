# docker-redis-cluster


> Based on repository <https://github.com/itsmetommy/docker-redis-cluster> with some customizations.

## Build and start all containers

```bash
cd docker-redis-cluster
```
```bash
docker-compose up --build -d
```

## View containers
```bash
docker ps
```

## Connect to one of the masters
```bash
docker exec -it docker-redis-cluster_redis-1_1 redis-cli -c
127.0.0.1:6379>
```

## Create keys
```bash
127.0.0.1:6379> set mykey1 1
127.0.0.1:6379> set mykey2 2
127.0.0.1:6379> set mykey3 3
127.0.0.1:6379> get mykey1
127.0.0.1:6379> get mykey2
127.0.0.1:6379> get mykey3
```

## View nodes
```bash
127.0.0.1:6379> cluster nodes
```

## View slots
```bash
127.0.0.1:6379> cluster slots
``` 

## Clean up
```bash
docker-compose down
```