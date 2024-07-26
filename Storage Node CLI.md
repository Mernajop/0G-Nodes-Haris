#Storage Node CLI

## Install the Storage Node CLI

First, download and install the CLI tool:

```
wget https://github.com/0gnetwork/storage-node-cli/releases/download/v1.0.0/storage-node-cli-linux-amd64 -O storage-node-cli
chmod +x storage-node-cli
sudo mv storage-node-cli /usr/local/bin/
```
## Initialize the CLI with Validator Data

Initialize the CLI using the provided validator data:

```
storage-node-cli init \
    --account "0g18dw5z7sfa5rqg64dm34dqn5jzjx22ky7qnvapu" \
    --operator "0gvaloper18dw5z7sfa5rqg64dm34dqn5jzjx22ky7reap5p" \
    --consensus "0gvalcons19audas9pys9x9t73puxncmp2z45a3rr8m54lqg" \
    --hex "2F78DEC0A1240A62AFD10F0D3C6C2A1569D88C67"
```
## Check Node Status

To check the status of your storage node:

```
storage-node-cli status
```
## Interact with the Storage Node

You can perform various operations using the CLI. Here are some examples:

Store Data

```
storage-node-cli store --key "example-key" --value "example-value"
```
Retrieve Data

```
storage-node-cli retrieve --key "example-key"
```
Delete Data

```
storage-node-cli delete --key "example-key"
```
