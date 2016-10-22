# Docker-compose-jenkins
This repo is intended to guide the creation of the docker-compose environment for jenkins


# Prerequisites

* docker-machine
* docker 
* docker-compose

# Create a virtual machine 

docker-machine create -d virtualbox --virtualbox-memory "5048" example-jenkins

* eval $(docker-machine env example-jenkins)

To view docker machine below command could be used 

* docker-machine active

* docker-machine ip example-jenkins


# Executing docker-compose.yml file 

Use ' docker-compose up -d ' in dir containing docker-compose.yml file

check if the container is up and running using 'docker ps '

# How to bash into jenkins installation file 

## For windows 
* winpty docker  exec -ti  jenkins bash   

## For linux 

* docker  exec -ti  jenkins bash   


# How to access jenkins in web browser

http://<ip>:8080/

username : admin
password : <Password in /var/jenkins_home/secrets/initialAdminPassword can be obtain once you bash in the machine >


Login and enjoy , further reference for jenkins can be found at https://jenkins.io/doc/
