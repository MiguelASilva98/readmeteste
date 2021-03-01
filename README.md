# Agents
## Agents Description
-
## VON Network Setup Requirements 

- Machine requirements
--Ubuntu 18.04.1 LTS
--Git 
--Docker
-Docker-compose

## Install Git
```python
sudo apt-get update
sudo apt-get install git
git — version
```
## Install and config Docker
```python
sudo apt-get update

sudo apt-get install \
apt-transport-https \
ca-certificates \
curl \
gnupg-agent \
software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository \
“deb [arch=amd64] https://download.docker.com/linux/ubuntu \
$(lsb_release -cs) \
stable”
#update repository
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io
#check version
docker — version
```
## Install Docker-compose
```python
sudo curl -L “https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)” -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

docker-compose — version
```
Docker compose’s version should be shown.

## Build VON-Network
If all of the previous steps have been completed, it is now possible to initialize a Von-Network.

Git Repository: https://github.com/bcgov/von-network

Use below command to download code to your local:
```python
git clone https://github.com/bcgov/von-network.git
```
Use below command to build nodes of the network:
```python
./manage build
```
Use below command to start nodes of the network:
```python
./manage start
```

All VON-Network nodes should now be active.