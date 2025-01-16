<h2 align=center>Run Gaianet Node by Docker</h2>

## Info
- You need to have min 16 GB RAM in your system (VPS), btw it also works on 8 GB RAM as well (I tested).
- Recommended : 32 GB RAM
- You can buy VPS from [PQ Hosting](https://pq.hosting/?from=622403&lang=en) using cryptocurrency
- Make sure to use : Ubuntu-22.04 or Ubuntu-24.04

## Installation
- First install `Docker` in your system if it is not already there by using below command
```
source <(wget -O - https://raw.githubusercontent.com/zunxbt/installation/main/docker.sh)
```
```
sudo groupadd docker && sudo usermod -aG docker $(whoami) && newgrp docker
```
- Install `gaianet docker image` and run it via this command
```
sudo docker run --name gaianet -p 6969:6969 -v $(pwd)/qdrant_storage:/root/gaianet/qdrant/storage:z gaianet/phi-3-mini-instruct-4k_paris:latest
```
- Now use these below command to get node-info
```
docker exec -it gaianet /bin/bash
```
```
/root/gaianet/bin/gaianet info
```
- Copy `Node ID` and `Device ID` and then write `exit` to detach from this container
- Visit [Gaianode Site](https://www.gaianet.ai/setting/nodes) and then connect your wallet
- Now click on `connect new node`, here enter your `Node ID` and `Device ID` and then click on `Join` button
