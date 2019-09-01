## Docker commands cheatsheet

### Basic commands
``` shell script
docker images   // Listing all images
docker ps       // View the current process
```

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


### Monitor
``` shell script
docker ps
docker ps -a                      // lists all containers
docker ps --filter status=running // selects containers that are running.
```
