## Docker commands cheatsheet

### Basic commands
docker images   // Listing all images
docker ps       // View the current process


### Build
docker build -t deiveehan/ctrl-space-io-home .

### Push
docker push deiveehan/ctrl-space-io-home


### Run image
docker run -t -d deiveehan/ctrl-space-io-home // Custom image

### Connect to the container using ssh
docker connect

### Delete images
docker rmi -f deiveehan/ctrl-space-io-home
docker rmi $(docker images -q)                // Deletes all images in local


### Monitor
docker ps
docker ps -a                      // lists all containers
docker ps --filter status=running // selects containers that are running.
