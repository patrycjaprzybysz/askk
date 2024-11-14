# Exercise 3: Building images

### Getting setup

1. delete existing image

![image](https://github.com/user-attachments/assets/0c9e68e5-a016-4787-beef-c38f3db2b850)

### Creating a Dockerfile

1. ```echo. > Dockerfile``` (cmd)

![image](https://github.com/user-attachments/assets/e1c28957-aa22-41da-96a4-53c30b31eec5)


2. dockerfile in notebook

![image](https://github.com/user-attachments/assets/e9490e13-a7ad-45ae-bc1e-9113d52bd9d5)

3. dockerfile with ping

![image](https://github.com/user-attachments/assets/cfc43faa-ff36-4a18-9a7b-eb5f70b902dd)

### Building the Dockerfile

1. ```docker build -t delner/ping .```

![image](https://github.com/user-attachments/assets/52d8a575-5eb0-422a-9996-aba3e915658d)

2. docker images

![image](https://github.com/user-attachments/assets/0a35bab3-5c4f-40cf-beff-ba387a722351)

### Optimizing the Dockerfile

1. removing old logs

![image](https://github.com/user-attachments/assets/68fe7064-f0ec-4a89-9935-3d63643754db)

2. build again (nothing changed)

![image](https://github.com/user-attachments/assets/4c67e9bf-e1c7-40a1-9d79-842884950eda)

3. new dockerfile

![image](https://github.com/user-attachments/assets/b04c9963-4e60-4744-95ab-f85d913ee906)

4. build again (smaller size)

![image](https://github.com/user-attachments/assets/7d480f05-2e3f-4c63-af59-d4b785a5b36d)

### Other Dockerfile directives

Some important ones:

* COPY: Copy files from your host into the Docker image.
* WORKDIR: Specify a default directory to execute commands from.
* CMD: Specify a default command to run.
* ENV: Specify a default environment variable.
* EXPOSE: Expose a port by default.
* ARG: Specify a build-time argument (for more configurable, advanced builds.)

1. add the ENV and CMD directives.

![image](https://github.com/user-attachments/assets/00eaa2c8-b4f9-48d8-bc3f-b8b8abbdaec3)

2. ping google.pl run automatically 

![image](https://github.com/user-attachments/assets/e2308ac5-8747-4b9f-97ca-4218078273d2)
