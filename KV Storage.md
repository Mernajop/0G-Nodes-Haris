# KV Storage

## Access the Key-Value Storage API

To interact with the key-value storage API, you can use curl or any HTTP client.

## Store Data

Use the following command to store data in the key-value storage:

```
curl -X POST https://harris-kv.trekorenthusiast.pics/store \
    -H "Content-Type: application/json" \
    -d '{
        "key": "example-key",
        "value": "example-value",
        "validator": {
            "account": "0g18dw5z7sfa5rqg64dm34dqn5jzjx22ky7qnvapu",
            "operator": "0gvaloper18dw5z7sfa5rqg64dm34dqn5jzjx22ky7reap5p",
            "consensus": "0gvalcons19audas9pys9x9t73puxncmp2z45a3rr8m54lqg",
            "hex": "2F78DEC0A1240A62AFD10F0D3C6C2A1569D88C67"
        }
    }'
```
## Retrieve Data

Use the following command to retrieve data from the key-value storage:

```
curl -X GET https://harris-kv.trekorenthusiast.pics/retrieve \
    -H "Content-Type: application/json" \
    -d '{
        "key": "example-key"
    }'
```
## Delete Data

Use the following command to delete data from the key-value storage:

```
curl -X DELETE https://harris-kv.trekorenthusiast.pics/delete \
    -H "Content-Type: application/json" \
    -d '{
        "key": "example-key"
    }'
```
## Check Storage Status

Use the following command to check the storage status:

```
curl -X GET https://harris-storage.trekorenthusiast.pics/status
```
