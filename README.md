
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

You can access the website1 at http://localhost/website1 and website2 at http://localhost/website2. The default http://localhost or any other directory will result a 404 error page.

# Running the Task A

1. Clone this repository by using `git clone https://github.com/WillySeahh/otot-task-a`.
2. Navigate to the project root directory by using `cd otot-task-a`.
3. Navigate to the website1 by using `cd webpage1` and run `docker-compose up --build -d` to build the image for website1 and run the docker container.
4. Navigate to the website2 by using `cd ../webpage2` and run `docker-compose up --build -d` to build the image for website2 and run the docker container.
5. Navigate to the reverse proxy server by using `cd ../reverseProxy` and run `docker-compose up --build -d` to build the image for reverse proxy server and run the docker container.
6. Go to browser and enter http://localhost/webpage1 to access webpage1 and http://localhost/wepage2 to access webpage2. If you enter the directory other than these 2 (e.g. http://localhost/webpage3), it will show a 404 error page.
7. Stop all running docker container by using `docker stop $(docker ps -q)` on Linux or Git Bash **OR** `docker ps -q | % { docker stop $_ }` on Windows PowerShell.
