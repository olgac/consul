# consul
H/A Consul Cluster on Docker Swarm

Commands
-------------

```bash

wget https://raw.githubusercontent.com/olgac/consul/master/docker-compose.yml
docker network create --driver=overlay --attachable prod

docker node update --label-add consul=true node-1
docker stack deploy -c docker-compose.yml consul
sleep 30
docker node update --label-add consul=true node-2
docker node update --label-add consul=true node-3

#docker run -d -p 9000:9000 --name portainer -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer
```
