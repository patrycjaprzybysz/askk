# EXERCISE 1: running containers

### Pulling an image

1. Docker images

![image](https://github.com/user-attachments/assets/1ee2c80d-5c6d-42f3-a90d-0125eecd56e5)

2. Docker search ubuntu

![image](https://github.com/user-attachments/assets/0c30a839-00f2-475c-9fec-a5d46eaec82d)

3. Docker pull ubuntu:22.04

![image](https://github.com/user-attachments/assets/de25e090-3154-42ac-9e6c-8edf7e1b543f)

4. docker pull ubuntu:22.10

![image](https://github.com/user-attachments/assets/897cfc57-cc23-473f-8aa8-50a4367eb13b)

5. docker images

![image](https://github.com/user-attachments/assets/feedeb7a-03ac-4185-963b-ba9ccc80a21b)

6. docker rmi

![image](https://github.com/user-attachments/assets/bf3fa052-b981-4d30-a0f7-69414c9d4633)

7. docker images

![image](https://github.com/user-attachments/assets/d0d3dc1f-995b-400a-9bf0-3934ee766f00)

8. docker delete all images (cmd)

![image](https://github.com/user-attachments/assets/c48d206b-7502-42a2-b487-143a3383229f)

### Running our container

1. Docker run

![image](https://github.com/user-attachments/assets/d28d4322-ce27-4870-86eb-69d53523e9e3)

2. docker ps

![image](https://github.com/user-attachments/assets/69437a41-9d4c-4514-8af2-0c84a37cce54)

3. docker ps -a

![image](https://github.com/user-attachments/assets/d6fd1bb9-514b-4f8b-b4e5-b053516dac50)

4. docker run ubuntu:22.04 /bin/bash and docker ps -a

![image](https://github.com/user-attachments/assets/34e2d793-bd0c-4a67-a513-053e10f4f930)

5. docker run -it ubuntu:22.04 /bin/bash

![image](https://github.com/user-attachments/assets/d025b7eb-05ba-4b40-a05e-45dde9db4739)

6. pwd ls command inside container

![image](https://github.com/user-attachments/assets/9d3631b3-f48e-4e54-95ce-8ab5ae8079b0)

7. docker run -d ubuntu:22.04 /bin/sleep 3600 (run the container idly for 1 hour:)

![image](https://github.com/user-attachments/assets/9a7e32d7-758c-485f-812a-5dc627a9cf80)

8. docker ps

![image](https://github.com/user-attachments/assets/ce95caef-e728-4090-81bc-58d3dbc23ec3)

9. docker exec -it 45c /bin/bash

![image](https://github.com/user-attachments/assets/1e90ae55-03fa-4df7-85e5-0c5f25cb07af)

10. ps aux inside container

![image](https://github.com/user-attachments/assets/eb15b027-c299-4c19-8c5b-ed5d55edad82)

11. exit and  docker ps 

![image](https://github.com/user-attachments/assets/77c29112-b1e8-451f-aebc-e2004f0f911b)

12. docker stop 45c

![image](https://github.com/user-attachments/assets/0121e1f8-48ee-46ce-8a1c-cca41aa5c7aa)

13. docker ps -a

![image](https://github.com/user-attachments/assets/62b1fd36-20ef-4385-9add-c49b52ad4159)

### Removing containers

1. docker ps -a

![image](https://github.com/user-attachments/assets/cc8bac0f-f3e0-4929-9acd-e0c65b1a5ae8)

2. docker rm 45c

![image](https://github.com/user-attachments/assets/807bf153-57da-4d87-b1dd-fde5a66e8291)

3. docker delete all containers (cmd) FOR /F "tokens=*" %i IN ('docker ps -a -q') DO docker rm %i

![image](https://github.com/user-attachments/assets/c19282ad-3bcf-41f3-8b7c-afb689d35593)

4. docker ps -a

![image](https://github.com/user-attachments/assets/6ab776bf-a9b6-48dd-bb38-f0d0064a170c)

5. docker run --rm ubuntu:22.04 /bin/echo 'Hello and goodbye!'

![image](https://github.com/user-attachments/assets/c8e44b27-3b1b-4110-a6e2-b322f123db4b)
