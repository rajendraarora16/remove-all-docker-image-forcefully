# Remove all docker image forcefully

**Stop all containers**
```
docker stop `docker ps -qa`
```

**Remove all containers**
```
docker rm `docker ps -qa`
```

**Remove all images**
```
docker rmi -f `docker images -qa `
```

**Remove all volumes**
```
docker volume rm $(docker volume ls -qf)
```

**Remove all networks**
```
docker network rm `docker network ls -q`
```

**Your installation should now be all fresh and clean**

**The following commands should not output any items:**
```
docker ps -a
docker images -a 
docker volume ls
```

**The following command show only show the default networks:**
```
docker network ls
```


**To remove forcefully in just a two commands**

```
docker rmi $(docker images -q)
docker rm $(docker ps -a -q)
```

**Killing docker container and forcefully remove it**

```
docker container kill <container-id e.g: 93cb5edd356c>
docker image rm csd_monitor_server
```

**Removing docker repo forcefully**

```
docker rmi -f <REPO-NAME-via-docker-images-command>
```
