# How to Install Docker on Ubuntu EC2
If you found this repo useful, give it a star

1. you need to create Ubuntu ec2.
   
   Connect ec2 instant using ssh command
   
   ssh -i <path of .pem file> ubuntu@ <ip address> 
3. In ubuntu run command
   
   sudo apt update -y

5. Now this command to install docker
   
   sudo apt install docker.io -y

6. Check if docker is ruuning or not.

   sudo systemctl status docker

7. Now check if docker is ready to use or not by running simple command.

   docker run hello-world

   It will give error of permission denied. This is because you have installed docker using sudo and by default docker has to be installed using root user only. Docker deamon also execute using root user.

8. To remove this error, we need to add ubuntu user to docker group by using command

   Sudo usermod -aG docker ubuntu

   usermod command modifying the behaviour of ubuntu user and its making it the part of user group. even after running this command again it will show the same error. Because after thsi you need to restart or you need to logout or again login.

9. so logout and again login
      
   
   
