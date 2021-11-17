QueueIt Docker-compose-Nginx-Reverse-Proxy
===================================

Tutorial
---------
Followed
[Docker compose : Nginx reverse proxy with multiple containers](http://www.bogotobogo.com/DevOps/Docker/Docker-Compose-Nginx-Reverse-Proxy-Multiple-Containers.php) 

Modified using steps descibed in https://github.com/queueit/KnownUser.V3.Lua/tree/master/Examples/Nginx


Step 1 
Configure CUSTOMER_ID and SECRET_KEY in tpl/default.conf file.

```
code tpl/default.conf 
```

Step 2
Build the reverseproxy docker image.
```sh
docker build --label reverseproxy  -t reverseproxy --file QueueItDockerfile .
```

Step 3

Start the microservices using docker-compose:
```sh
docker compose up -d
```
