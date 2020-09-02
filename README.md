# Apigee-Compute-Proxy-v1

## Features included in this API Proxy

* SOAP and JSON payload transformation
* Load balancing and health checking to backend service
* Security
  * Access Control (IP whitelist) **(Need to change IP range in the policy)**
  * API Key Verify
  * Basic Authentication decode
* Rate limit
  * Spike Arrest (Config in API Product)
  * Quota (Config in API Product)
* Cache
  * ResponseCache (Cache by request URL and request payload)
* Logging
  * MessageLogging (Write Log file at **/opt/apigee/var/log/edge-message-processor/messagelogging/demoorg/test/Compute-Proxy-v1/{Reversion}/Message-Logging/api-proxy.log** in the **Message Processor Node**)

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
