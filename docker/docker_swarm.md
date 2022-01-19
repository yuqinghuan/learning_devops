![docker_swarm_1.jpg](../img/docker_swarm_1.jpg)
![docker_swarm_2.jpg](../img/docker_swarm_2.jpg)
![docker_swarm_3.jpg](../img/docker_swarm_3.jpg)

```
docker service create --name database --env-file .env --mount type=bind,src=/Users/venkateshachintalwar/Documents/Online_Projects/Docker/db/init.sql,dst=/docker-entrypoint-initdb.d/init.sql mysql/mysql-server:5.7
```

```
git clone https://github.com/venky8283/Docker.git
```