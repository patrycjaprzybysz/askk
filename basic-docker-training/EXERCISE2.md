# EXERCISE 2 - Changing images

### Getting setup

1. ```docker pull ubuntu 16.04``` and docker images

![image](https://github.com/user-attachments/assets/e220f29f-c9fb-4aa2-a73f-dc4efbeee41b)

![image](https://github.com/user-attachments/assets/211f4d29-de79-4894-9e2e-b41d8cb40bef)

### Modifying an image

1. ping - not succesed

![image](https://github.com/user-attachments/assets/76076162-593a-453a-a3ba-5fc5aa9edfc1)

2. update the list of available software: ```apt-get update```

![image](https://github.com/user-attachments/assets/fe669274-b22b-4457-9bd4-1bd7c9eb72ea)

3. Call ```apt-get install iputils-ping``` to install the package containing ping:

![image](https://github.com/user-attachments/assets/c8893853-af12-4fb6-bb49-7b0e9aaf29be)

4. ```ping google.pl```

![image](https://github.com/user-attachments/assets/59777006-bde4-4464-9279-edff1fb1b6a9)

### Committing changes

1. ```docker ps -a```

![image](https://github.com/user-attachments/assets/a3e0c16b-25a5-499b-b0e0-b4e384c4d0d2)

2. ```docker commit -a "Patrycja" -m "Added ping utility" 350 delner/ping```

![image](https://github.com/user-attachments/assets/4bd2022d-5c7c-4d7a-8613-d320186b08c5)

3. ```docker images```

![image](https://github.com/user-attachments/assets/2e612a2e-dae5-4a37-a4dc-3ddae4349082)

4. ```docker run -it --rm delner/ping /bin/bash```

![image](https://github.com/user-attachments/assets/881999bf-bb00-480f-990d-5d4ae41b32f2)




