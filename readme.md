# Horizon Chatbot Service

Starts a web application (index.html) to connect to IBM Watson Assistant chatbot. 

Open your browser and navigate to:

http://localhost:88

## Input Values

The following input values can be given to this service in the input file given to `hzn register`:


| Name | Required? | Type | Description |
| ---- | --------- | ---- | ---------------- |

| MOCK | no | boolean | default is false. If true, send fake data instead of querying the cpu and gps services |
| PUBLISH | no | boolean | default is true. If false, do not send data to message hub, only print it to the log |



#### Example:
A sample `services` section of the input file given to `hzn register`:
```
    "services": [
        {
            "org": "$HZN_ORG_ID",
            "url": "https://$MYDOMAIN/service-$CHATBOT_NAME",
            "versionRange": "[0.0.0,INFINITY)",
            "variables": {
                "MOCK": false,
                "PUBLISH": true,
            }
        }
    ]
```

