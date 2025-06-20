# How to Install Docker and Configure Docker on Ubuntu EC2
If you found this repo useful, give it a star 

1. You need to create Ubuntu ec2.
   
2. Connect ec2 instant using ssh command
   
   ssh -i <path of .pem file> ubuntu@ipaddress
   
3. In ubuntu run command
   
   sudo apt update -y

4. Now this command to install docker.
   
   sudo apt install docker.io -y

5. Check if docker is ruuning or not.

   sudo systemctl status docker

6. Now check if docker is ready to use or not by running simple command.

   docker run hello-world

   It will give error of permission denied. This is because you have installed docker using sudo and by default docker has to be installed using root user only. Docker deamon also execute using root user.

7. To remove this error, we need to add ubuntu user to docker group by using command.

   Sudo usermod -aG docker ubuntu

   Usermod command modifying the behaviour of ubuntu user and its making it the part of user group. even after running this command again it will show the same error. Because after thsi you need to restart or you need to logout or again login.

8. So logout and again login

9. Now run command

   docker run hello-world

   Now docker is up and runing and ready to use.

   Congratulations! Now you can write your first docker file.
   
    
      
   
   
