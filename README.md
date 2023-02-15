# Using redis-server and redis-sentinel

- redis-0
- redis-1
- redis-2
- sentinel-0
- sentinel-1
- sentinel-2

## For example to connect to redis-0

```
cd redis-0
redis-server redis.conf
```

## And for sentinel-0

```
cd sentinel-0
redis-sentinel sentinel.conf
```

# Using Docker

## Inside "copy paste" folder you can find the same configuration but for docker

###### for connection commands see the 'docker-container-command-creation.txt' file

# Using Clustering

## Inside cluster you have to repeat the following steps for each subfolder

## For example for 7000 folder

```
cd 7000
redis-server redis.conf
```

## Then with all six instances running, you can create the cluster

```
redis-cli --cluster create 127.0.0.1:7000 127.0.0.1:7001 127.0.0.1:7002 127.0.0.1:7003 127.0.0.1:7004 127.0.0.1:7005 --cluster-replicas 1 -a redispw
```
