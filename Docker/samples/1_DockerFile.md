```shell script
docker build -t nginx-custom .

### Sample 1
```
#### Run again to check if it is downloading again
```
docker build -t nginx-custom .
```

Run the customized image

### Sample 2

Edit the file sample-2/Dockerfile

```shell script
docker build -t nginx-custom .
doicker run -d -p 8080:80 custom-nginx
http localhost:8080
docker container rm -f c84f519acf97
```

### Handling images

```shell script
docker image pull nginx:1.14.0        // Pulls image from the repository
docker images                         // List all images
docker image ls -a                    // List all the images with layers
docker image inspect nginx:1.14.0     //Inspect an image
docker image inspect nginx:1.14.0 --format "{{.Architecture}}"    // Get a specific attribute while inspecting..
docker image rm nginx:1.14.0          // Remove an image
docker rmi nginx:1.14.0               // Same as above

docker run -d --name nginx nginx:1.14.0
docker image rm -f nginx:1.14.0
docker image prune

```
### Docker Registries:
- storing and distributing images

Creating a registry server
```shell script
docker run -d -p 5000:5000 --restart=always --name registry registry:2
docker logs registry
docker stop registry && docker container rm -v registry

docker run -d -p 5000:5000 --restart=always --name registry -e REGISTRY_LOG_LEVEL=debug registry:2
docker logs registry
docker stop registry && docker container rm -v registry

```

Using Registries
```shell script
docker login
docker search ubuntu          // Searches image in the registry
docker pull ubuntu
docker push <registryhost>/ubuntu

```
###Note:
- Keep things that does not change in the beginning layers
- Avoid creating mulitiple layers
- Avoid packaging unnecessary files / packages (keep it simple..)

