# EXERCISE 5: Volumes

### Setting up the server

1. run our Apache HTTPD server

This command will start a new container from HTTP 2.4, name it apache, bind port 80 to the host machine 
(more on this later), and set a flag to delete the container when it stops.

![image](https://github.com/user-attachments/assets/7e97ddd8-58f9-4af0-9661-0c344a51f16a)

2. run curl localhost to query the web server for the default page:

![image](https://github.com/user-attachments/assets/0a2f85ac-7970-4a30-aedc-f6ebbe6ada04)

3. replace HTML file with new content

![image](https://github.com/user-attachments/assets/334db52c-227a-4254-89f0-66afa833d3f3)

4. Running curl again now looks a little different:

![image](https://github.com/user-attachments/assets/2d3032da-c269-4d42-9f65-bd188ea349c3)

5. possible problems

This container, for its lifetime, will continue to serve our new HTML file.
However, containers in Docker are, in practice, considered ephemeral. They can die unexpectedly, and in certain deployments,
be removed without warning. If you're depending upon the container state for your application, you might lose important data 
when such containers die. This is especially a concern for applications like databases, which are supposed to be considered 
permanent datastores.

In the case of our HTTPD server, simply stopping the container will cause it to be autoremoved. 
We can bring another container back up in it's place, but it won't have our changes any more.

![image](https://github.com/user-attachments/assets/464bbe05-078b-4cc7-9302-43c8d70f6c8f)

### Managing volumes

1. To list your volumes, run docker volume ls:

![image](https://github.com/user-attachments/assets/39e2c82b-1b69-4b76-bf41-70aa3eb1d840)

2. To create a new volume, run docker volume create and give it a volume name.

![image](https://github.com/user-attachments/assets/f1864810-cf48-4e1b-8870-620d83660bcb)

3. To remove a volume, run docker volume rm and give it the volume name.

![image](https://github.com/user-attachments/assets/c57af4a5-ba2f-4afa-8e0b-e7aaa5a7d81b)

### Mounting volumes on containers

1. create a new volume named httpd_htdocs:

![image](https://github.com/user-attachments/assets/0f0d130b-cfd6-484b-9476-99c8bf703edd)

2. re-run our docker run command, providing the -v mount flag.

![image](https://github.com/user-attachments/assets/a2c04f25-d164-4071-9e85-e5f6876114dd)

3. re-copy in our modified HTML file.

![image](https://github.com/user-attachments/assets/a93502a9-b8e4-4993-9966-84e2917d11f9)

4. run curl to verify it worked.

![image](https://github.com/user-attachments/assets/0166e837-b374-403e-a383-1c190a6d7888)

5. let's stop the container

![image](https://github.com/user-attachments/assets/7b193ef3-c7f4-46b5-98d6-b374c946709f)

6. Then once again start httpd with the same run command as last time. 

This time, however, we can curl and see our file changes are still there from before.

![image](https://github.com/user-attachments/assets/994937fe-6c3e-4bef-b13d-3e73a885c2f0)

### Mounting host directories on containers

1. 
![image](https://github.com/user-attachments/assets/cd6b4731-68fb-4c02-9ad6-489169b87299)

2. curl localhost

![image](https://github.com/user-attachments/assets/f20822b0-2ce5-4c56-bf02-8a827b814a12)
