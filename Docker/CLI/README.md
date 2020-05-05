## Docker commands cheatsheet

### Setup
Install docker in the docker home page (Install the dmg file)
https://docs.docker.com/v17.12/docker-for-mac/install/#download-docker-for-mac

## Get started commands
```
docker version
docker run -it hello-world

```


### Basic commands
``` shell script
docker images   // Listing all images
docker ps       // View the current process
```

### Pull images
docker 

### Build
``` shell script
docker build -t deiveehan/ctrl-space-io-home .
```

### Push
``` shell script
docker push deiveehan/ctrl-space-io-home
```

### Run image
``` shell script
docker run -t -d deiveehan/ctrl-space-io-home // Custom image
```

### Connect to the container using ssh
``` shell script
docker connect
```

### Delete images
``` shell script
docker rmi -f deiveehan/ctrl-space-io-home
docker rmi $(docker images -q)                // Deletes all images in local
```

### Kill container
```shell script
docker ps
docker kill <container-id>
```


### Monitor
``` shell script
docker ps
docker ps -a                      // lists all containers
docker ps --filter status=running // selects containers that are running.
```
