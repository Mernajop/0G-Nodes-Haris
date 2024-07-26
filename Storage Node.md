## Install Docker
First, install Docker by running the following commands:

```
sudo apt-get update
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

## Pull the 0G Storage Node Docker Image
```
docker pull 0gnetwork/storage-node:latest
```
## Run the Storage Node

Use the following command to run the storage node container:

```
docker run -d \
    --name storage-node \
    -e VALIDATOR_ACCOUNT="0g18dw5z7sfa5rqg64dm34dqn5jzjx22ky7qnvapu" \
    -e VALIDATOR_OPERATOR="0gvaloper18dw5z7sfa5rqg64dm34dqn5jzjx22ky7reap5p" \
    -e VALIDATOR_CONSENSUS="0gvalcons19audas9pys9x9t73puxncmp2z45a3rr8m54lqg" \
    -e VALIDATOR_HEX="2F78DEC0A1240A62AFD10F0D3C6C2A1569D88C67" \
    -p 5678:5678 \
    0gnetwork/storage-node:latest
```
## Verify the Node is Running

You can check the logs to ensure the node is running correctly:

```
docker logs storage-node
```
