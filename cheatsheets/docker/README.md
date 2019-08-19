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


### Delete images
docker rmi -f deiveehan/ctrl-space-io-home
