<h1 align="center">Hi 👋, I'm SYED ASAD RAZA</h1>
<h3 align="center">A passionate DevOps Instructor | Microsoft Certified Trainer | Cloud & DevOps Engineer at Ascend healthcare | 云工程师 | Microsoft Azure Cloud Engineer | ExAzure Administrator at Sysytems Limited </h3>

## Devops_Docker_lab_Scratch for Beginner
To setup the lab, as participants, we would install Docker Toolbox and create Containers for each application being used to setup learning environment.

### Uninstall Old Versions
```
sudo apt-get remove docker docker-engine docker.io containerd runc
```
### Install Docker On Ubuntu
#### _digital ocean totorail to install docker_
```
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - 
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" 
apt-cache policy docker-ce
sudo apt install docker-ce -y
```
### _Docker Offical-doc To Install_
```
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null 

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
sudo systemctl status docker
```

### POST INSTALLATION ACTIVITIES
```
docker --version
docker info
docker version
```
## DOCKER ENGINE

![Docker Engine](https://user-images.githubusercontent.com/71556060/196001769-03af9e4c-0afe-4711-a2e3-5db1c129227d.png)

## IMAGES

A Container Image is a lightweight, standalone, executable package of software that includes everything needed to run an application: 
  - Code
  - Runtime
  - System tools
  - System libraries 
  - Settings
### PULLING IMAGES
```
docker image pull alpine:latest
docker pull asadzoot/helloworld
```
```
docker ls
```
```
docker image rm alpine:latest
```
## DOCKER CONTAINERS
````
docker run -it asadzoot/helloworld sh
````
````
# exit
````
````
docker container ls
docker ps
docker container ls -a
````
````
docker exec -it asadzoot/helloworld
````
````
docker container start asadzoot/helloworld
docker container stop asadzoot/helloworld 
docker container rm asadzoot/helloworld
````
````
docker run -d --name mycontainer asadzoot/helloworld
````
````
docker run -d --name mycontainer -p 8000:80 asadzoot/helloworld
````

https://hub.docker.com/r/asadzoot/helloworld

https://hub.docker.com/u/asadzoot

