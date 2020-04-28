# IIEC_Docker_Project_Ghost 

On March 01, 2020 Indian Innovation and Entrepreneurship Community (IIEC) under the mentorship Mr.Vimal Daga started a great initiative of training Docker container technology to the persuing students from basic to advance . I am the part of the initiative and I learned a lot of things bout Docker and Containerization. Now, I am in a stage to do a project on Docker Compose.


### Ghost : 
Ghost is a powerful platform for creating an online blog or publication. 
Ghost is a free and open source blogging platform written in JavaScript and distributed under the MIT License, designed to simplify the process of online publishing for individual bloggers as well as online publications.

The concept of the Ghost platform was first floated publicly in November 2012 in a blog post by project founder John O'Nolan, which generated enough response to justify coding a prototype version with collaborator Hannah Wolfe.

## 1. Pre-Configuration :
REDHAT ENTERPRISES LINUX 8 and installed with Docker and Docker Compose .
* we need to download mysql to check database
```
dnf install mysql
```

## 2. Install Docker 
* Install docker 
``` 
dnf install docker-ce
```
* start docker 
```
systemctl start docker 
```
* To check the status of docker 
```
systemctl status docker 
```
**Disable firewall if Docker is dead**

## 3.Required Images 
I am using the MySQL as database to the ghost. mysql:5.7 and ghost:1-alphine images from docker hub

* To pull mysql
```
docker pull mysql:5.7
```
* To pull ghost
```
docker pull ghost:1-alpine
```

## 4. Install Docker Compose 
* We need to download docker compose software . Follow the instructions in the link to install docker compose
https://docs.docker.com/compose/install/
* The docker compose file must be **docker-compose.yml** . we have to check every time we create the docker compose file.

## 5. Docker-Compose
* Write in **docker-compose.yml** file

![docker-compose.yml](/ghost_vim.png?raw=true)

from above screen shot :

**version**  is the version of the docker compose we are using.

**services** specify about the running services in docker 

**volume** are the storage units for services

**image** specifies about the image we are using 

**evironments** are the variables to specify before starting of the container

**restart** is to restart the service if it any containers start

**port** is to specify particular service 

**depends_on** is to specify it depends on database to store data



## 6.Docker-Compose Up

* To start docker compose
```
docker-compose up -d 
```

* To stop the docker compose
```
docker-compose stop
```

* To start the docker compose
```
docker-compose start
```
![docker-compose.yml](/ghost_upd.png?raw=true)

## 7.Launch the Web App 
Open the browser and search with IP Address and Port mentioned .
![docker-compose.yml](/ghost_launch.png?raw=true)

### we can also launch the webapp manually without using the docker compose 

#### This is my first project.
### All credits goes to Vimal Daga sir. Thank you Vimal Daga sir for training the Docker in such a level that I can do projects.
