# Commands
### docker-demo

#docker-compose demo mix of containers

#how to run:

#in root directory project: 
```shell
docker-compose up --build
```

#one_shot_killer: 
```shell
docker stop $(docker ps -aq); docker rm -f $(docker ps -a -q); docker rmi -f $(docker images -q)
```

#docker stop if runned, skip if not
```
docker stop nodejs-api-wrapper || true && docker rm nodejs-api-wrapper || true
```
#inspect network
```
docker network ls
docker network inspect bridge
```
The docker-compose stop command will stop your containers, but it won’t remove them.

The docker-compose down command will stop your containers, but it also removes the stopped containers as well as any networks that were created.

You can take down 1 step further and add the -v flag to remove all volumes too. This is great for doing a full blown reset on your environment by running docker-compose down -v
Show info about stack_name and version:
```
curl -X GET localhost:9200
```
Show indices:
```
curl -X GET localhost:9200/_cat/indices?v
```
Delete one-selected index:
```
curl -XDELETE 'http://localhost:9200/filebeat-7.4.2-2019/'
```
Delete all indices, use carefully!:
```
curl -X DELETE 'http://localhost:9200/_all'
```
