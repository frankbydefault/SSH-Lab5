# SSH-Lab5
Building the images
```
$ sudo docker build -t <img_name> <Dockerfile_path>
```

Runing the containers
```
$ sudo docker run -it <img_name>
```
Getting the Ip of the server container (C4)
```
$ sudo docker inspect \ -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container_name_or_id>
```
Connecting to ssh inside container
```
# ssh -p 22 test@<ip_container>
```
