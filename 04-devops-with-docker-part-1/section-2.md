# Running and stopping containers

1. docker run ubuntu, docker ls, docker run -it ubuntu, docker run -d -it --name looper ubuntu sh -c "while true; do date; sleep 1; done"

![image](https://github.com/user-attachments/assets/39a7d778-0cea-4fb5-a5c7-86f270d616de)

2. docker logs -f looper

![image](https://github.com/user-attachments/assets/f99da2db-1ba0-490e-9883-191c359db63b)

3. docker attach looper, docker logs -f looper, 

![image](https://github.com/user-attachments/assets/546c2cf6-8e6e-464f-a7f3-54e9d4d5b19d)

## Running processes inside a container with docker exec

1. 
![image](https://github.com/user-attachments/assets/3249aa94-b558-472a-aaad-859cccb9e71b)

2. 
![image](https://github.com/user-attachments/assets/17683d71-df99-43bf-8b80-70c4ad846694)

## Exercise 1.3 
```
1. docker run -d --name secret_container devopsdockeruh/simple-web-service:ubuntu
2. docker exec -it secret_container bash
3. tail -f ./text.log
```
 https://github.com/docker-hy
 
![image](https://github.com/user-attachments/assets/c48aa0f8-fc17-4e75-a80b-4c62c711de07)

## Exercise 1.4

```
Command to start the container:
docker run -it ubuntu sh -c "while true; do echo 'Input website:'; read website; echo 'Searching..'; sleep 1; curl http://\$website; done"

Commands to fix missing dependencies:
docker exec -it <CONTAINER_ID> bash
apt-get update
apt-get install -y curl
```

![image](https://github.com/user-attachments/assets/3eff8ccb-03c0-4efd-ac69-f3698bdebece)

![image](https://github.com/user-attachments/assets/8f815e89-7a3d-41ea-9d52-7fe8975e734c)
