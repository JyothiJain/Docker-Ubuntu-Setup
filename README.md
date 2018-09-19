# Docker-Ubuntu-Setup

 Docker can help a user to develop, deploy and run an application on a container, a container will run by running an image which is  an exceutable package that includes everything needed to run an application --the code, a runtime, libraries, environment variables, and configuration files. This document will help in basic setup of a docker.

## Prerequisites:

OS: Ubuntu 16.04 LTS  


## Installation Steps

#### Uninstall the older versions(If any exists, if not its good to have a check)

sudo apt-get remove docker docker-engine docker.io



## Set up the repository


#### Update the apt package index:

sudo apt-get update




#### Install packages to allow apt to use a repository over HTTPS:
 
sudo apt-get install apt-transport-https ca-certificates curl software- properties-common




#### Add Docker’s official GPG key
 
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -




#### Verify that you now have the key with the fingerprint 
 sudo apt-key fingerprint 0EBFCD88



#### set up the stable repository

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
xenial \
stable"



## Install Docker CE

#### Update the apt package index:
 
sudo apt-get update




#### Install the latest version of Docker CE, or go to the next step to install a specific version:

sudo apt-get install docker-ce



#### Verify that Docker CE is installed correctly by running the hello-world image
 
sudo docker run hello-world




## Optional steps to create the docker group and add your user(this will let a user use docker commands without using sudo)

#### Create the docker group
sudo groupadd docker



#### Add your user to the docker group
sudo usermod -aG docker $USER



#### Log out and log back in to ubuntu so that your group membership is re-evaluated
docker run hello-world



