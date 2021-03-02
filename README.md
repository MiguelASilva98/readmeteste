# Agents
### Agents Description
-

* **Machine requirements**: 
  * Ubuntu 18.04.1 LTS
  * Git 
  * Docker
  * Docker-compose
  * Mongo
  * Python

## Pre-Requesites 
### Install Git
```python
sudo apt-get update
```
```python
sudo apt-get install git
```
```python
git --version
```

### Install and config Docker
Reference: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04
```python
sudo apt update
```
```python
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
```python
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
```python
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
```
```python
sudo apt update
```
```python
sudo apt install docker-ce
```
```python
sudo systemctl status docker
```

### Install Docker-compose
```python
sudo curl -L “https://github.com/docker/compose/releases/download/1.28.5/docker-compose-$(uname -s)-$(uname -m)” -o /usr/local/bin/docker-compose
```
```python
sudo chmod +x /usr/local/bin/docker-compose
```
```python
docker-compose --version
```
Docker compose’s version should be shown.

## Build VON-Network
If all of the previous steps have been completed, it is now possible to initialize a Von-Network.

Git Repository: https://github.com/bcgov/von-network

Use below command to download code to your local:
```python
git clone https://github.com/bcgov/von-network.git
```
Go to the directory below
```python
cd von-network/
```
Use below command to build nodes of the network:
```python
sudo ./manage build
```
Use below command to start nodes of the network:
```python
sudo ./manage start
```
All VON-Network nodes should now be active.

## Run Agents 

* **Agents requirements**: 
  * Von-network running
  
### Install Agents
Reference: https://github.com/hyperledger/aries-cloudagent-python/blob/main/demo/README.md#running-in-docker

Git Repository: https://github.com/hyperledger/aries-cloudagent-python

Use below command to download code to your local machine:
```python
git clone https://github.com/hyperledger/aries-cloudagent-python
```
Go to the directory
```python
cd aries-cloudagent-python/demo
```
Now it is possible to initialize the agent
```python
./run_demo faber
```
In a new terminal, change directory into aries-cloudagent-python directory of your clone of this repository. Start the alice agent by issuing the following command:
```python
./run_demo alice
```
