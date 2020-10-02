# CS3219 OTOT Task A
Name: Willy Seah Wee Hung  
Matric Number: A0183766N  
Email: E0310561@u.nus.edu  

OTOT Assignment A

TASK: Deploy a simple web server using Nginx running in a Docker container.

LEARNING OBJECTIVE: To understand how containerization works and what its advantages are.

MARKING SCHEME:  
● Demonstrate ability to write simple Dockerfile (1 mark)  
● Setup Nginx and run a reverse proxy (1 mark)  
● Demonstrate ability to use Docker Hub registry to keep track of images (1 mark)  

There are total 3 containers running `Nginx`. The 2 websites run in `webpage1` and `webpage2` container. The reverse proxy server run in `reverseproxy` container.

You can access the website1 at http://localhost/webpage1 and website2 at http://localhost/webpage2. The default http://localhost or any other directory will result a 404 error page.

# Guide to running task-a

1. Clone this repository by using `git clone https://github.com/WillySeahh/otot-task-a`.
2. Ensure you have Docker running on your computer. Else kindly downlaod it from here. https://hub.docker.com  
3. Using cmd/Terminal navigate to the project `otot-task-a-main`. 
4. Type in`cd webpage1` and run `docker-compose up --build -d` to build the image for webpage1 and run the docker container. You should see something like this:
![Image 1](https://github.com/WillySeahh/otot-task-a/blob/main/images/imagesInDockerDashboard.png) 
5. Type in `cd ../webpage2` and run `docker-compose up --build -d` to build the image for webpage2 and run the docker container.
![Image 1](https://github.com/WillySeahh/otot-task-a/blob/main/images/imagesInDockerDashboard.png) 
6. Type in `cd ../reverseProxy` and run `docker-compose up --build -d` to build the image for reverse proxy server and run the docker container.
![Image 1](https://github.com/WillySeahh/otot-task-a/blob/main/images/imagesInDockerDashboard.png) 
7. Start Chrome browser or Firefox and type in http://localhost/webpage1 to access webpage1 and http://localhost/wepage2 to access webpage2. 
![Image 1](https://github.com/WillySeahh/otot-task-a/blob/main/images/webpage1.png) 
![Image 1](https://github.com/WillySeahh/otot-task-a/blob/main/images/webpage2.png) 
Visiting other webpages will return a Error 404 result. 
8. Stop all running docker container by using `docker stop $(docker ps -q)` on Linux or Git Bash **OR** `docker ps -q | % { docker stop $_ }` on Windows PowerShell.
