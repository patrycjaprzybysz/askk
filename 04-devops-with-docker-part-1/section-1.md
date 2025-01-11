# Running containers

1. ``` docker container run hello-world ```, ``` docker run hello-world ```

![image](https://github.com/user-attachments/assets/7612a053-cea2-4d37-a508-fd2e377954b0)

# Image and containers

1. List all your images with ```docker image ls```

![image](https://github.com/user-attachments/assets/3dc22e32-d38a-4b49-80e5-0e0612be77d4)

2. List all your containers with ``` docker container ls ```

![image](https://github.com/user-attachments/assets/3edebb9e-4f86-42e5-a7b2-65ad978d5bad)

3. ``` docker container ls -a ```, Without -a flag it will only print running containers. 
docker container ls = docker ps

![image](https://github.com/user-attachments/assets/b22c8773-4f05-4024-9418-8bca25a5c943)

# Docker CLI basics

1. ```docker container rm ...```  ``` docker image rm hello-world ```

![image](https://github.com/user-attachments/assets/27c623b1-c459-4051-aae0-af87658703a1)

2. starting a new container ``` docker run nginx```

![image](https://github.com/user-attachments/assets/270cfb50-d243-49c9-921c-2f2812ae81bf)

![image](https://github.com/user-attachments/assets/088398b0-5234-47d6-a5aa-e4f6f8860bfd)

# Exercises 1.1-1.2

## 1.1 task 

1. Start 3 containers in detached mode from an image that doesn't automatically exit (for example, nginx).

```
docker run -d --name container1 nginx
docker run -d --name container2 nginx
docker run -d --name container3 nginx
```

2. Stop two of the containers and leave one container running.

```
docker stop container2
docker stop container3
```

3. Run docker ps -a to display the status of all containers:

```
docker ps -a
```

![image](https://github.com/user-attachments/assets/bc56c5d8-1aa5-4fcd-8ba8-9fdab5ca8403)

## 1.2 task 

1.  Check the current containers and images

![image](https://github.com/user-attachments/assets/309e8290-55bc-4b4b-89f7-db82a3464f5d)

2. Remove all containers ``` for /F "tokens=*" %i in ('docker ps -aq') do docker rm %i ```

3. Remove all images ``` for /F "tokens=*" %i in ('docker images -q') do docker rmi %i ```

4. Verify cleanup

![image](https://github.com/user-attachments/assets/6bfdf86c-2e1b-426b-a9e3-0e43143a9553)



