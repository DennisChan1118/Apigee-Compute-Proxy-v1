# Apigee-Compute-Proxy-v1

## Use the following 'curl' command to invoke 'AddInteger' service:
```
curl -X POST 'http://{your host}:{your port}/v1/compute/add?apikey={your API Key}' \
-H 'Content-Type: application/json' \
-H 'Authorization: Basic {your base64 encoded username and password for basic authentication}' \
-d '{
    "arg1": "2",
    "arg2": "3"
}'
```

The expected result is
```
{
    "answer": 5
}
```
