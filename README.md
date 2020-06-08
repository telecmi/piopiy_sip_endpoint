## Create SIP Endpoint

Creating SIP Endpoint allows you to make and receive video calls, where making video calls can be made to APP to APP,APP to Browser and browser to browser calling.

## Prerequisites

1. Sign up for a free <a href="https://doc.telecmi.com/piopiy/docs/get-started" target="_blank">PIOPIY demo account</a>.

2. Create your <a href="https://doc.telecmi.com/piopiy/docs/create-endpoint" target="_blank">endpoint</a> and <a href="https://doc.telecmi.com/piopiy/docs/add-capacity" target="_blank">add capacity</a>.

3. Buy <a href="https://doc.telecmi.com/piopiy/docs/choose-number" target="_blank">PIOPIY phone number</a>.

4. Setup your webserver and map your POST method URL in <a href="https://doc.telecmi.com/piopiy/docs/build-app/#app-id-and-secret" target="_blank">answer URL</a>.


## Create SIP Endpoint

To create a SIP Endpoint, send your __POST__ method request with valid parameters to the following base URL.

### Base URL

```
https://piopiy.telecmi.com/v1/endpoint/add_sip

```
### Required Parameters

These are the required __POST__ method parameters with description

| Parameter Name| Type   |      Description                                                      |  
|  ---          |    --- | ---                                                                   | 
| *appid         | number | Your app id                                                           | 
| *secret        | string | Your app secret                                                       | 
| *username      | string | The name of the user                                          | 
| *password      | string | Password for the user                            | 


### Sample JSON Request

Below is the following sample JSON __POST__ method request to create SIP endpoint

```javascript
{
"appid": 2222223,
"secret": "635a5e93-3e5f-4aa5-b7ab-2a04cd5es039",
"username": "YOUR_USERNAME",
"password": "YOUR_PASSWORD"
}
```
### Sample JSON Response

If the provided information is valid, your web server will get a sample response from PIOPIY Platform as given below

```javascript
{
    "code": "cmi-200",
    "username": "YOUR_USERNAME",
    "password": "YOUR_PASSWORD",
    "connect_URL": "PIOPIY_SBC_URL",
    "audio": true,
    "video": true,
    "type": "SIP"
}
```

## Update SIP Endpoint

To update a SIP Endpoint password, send your __POST__ method request with valid parameters to the following base URL.

### Base URL

```
https://piopiy.telecmi.com/v1/endpoint/update_sip

```
### Required Parameters

These are the required __POST__ method parameters with description

| Parameter Name| Type   |      Description                                                      |  
|  ---          |    --- | ---                                                                   | 
| *appid         | number | Your app id                                                           | 
| *secret        | string | Your app secret                                                       | 
| *username      | string | The name of the existing user                                          | 
| *password      | string | New Password for the user                            | 


### Sample JSON Request

Below is the following sample JSON __POST__ method request to update SIP Endpoint

```javascript
{
"appid": 2222223,
"secret": "635a5e93-3e5f-4aa5-b7ab-2a04cd5es039",
"username": "YOUR_USERNAME",
"password": "YOUR_UPDATED_PASSWORD"
}
```
### Sample JSON Response

If the provided information is valid, your web server will get a sample response from PIOPIY Platform as given below

```javascript
{
    "code": "cmi-200",
    "username": "YOUR_USERNAME",
    "password": "YOUR_UPDATED_PASSWORD",
    "msg": "Updated successfully"
}
```

## Get SIP Endpoint Details

To get a SIP endpoint details, send your __POST__ method request with valid parameters to the following base URL.

### Base URL

```
https://piopiy.telecmi.com/v1/endpoint/get_sip

```
### Required Parameters

These are the required __POST__ method parameters with description

| Parameter Name| Type   |      Description                                                      |  
|  ---          |    --- | ---                                                                   | 
| *appid         | number | Your app id                                                           | 
| *secret        | string | Your app secret                                                       | 
| *username      | string | The name of the existing user                                          | 


### Sample JSON Request

Below is the following sample JSON __POST__ method request to get SIP endpoint details.

```javascript
{
"appid": 2222223,
"secret": "635a5e93-3e5f-4aa5-b7ab-2a04cd5es039",
"username": "YOUR_USERNAME"
}
```
### Sample JSON Response

If the provided information is valid, your web server will get a sample response from PIOPIY Platform as given below

```javascript
{
    "code": "cmi-200",
    "username": "YOUR_USERNAME",
    "password": "YOUR_PASSWORD",
    "connect_URL": "PIOPIY_SBC_URL",
    "audio": true,
    "video": true,
    "type": "SIP"
}
```

## To list all SIP Endpoint

To list all the SIP endpoint, send your __POST__ method request with valid parameters to the following base URL.

### Base URL

```
https://piopiy.telecmi.com/v1/endpoint/list_sip

```
### Required Parameters

These are the required __POST__ method parameters with description

| Parameter Name| Type   |      Description                                                      |  
|  ---          |    --- | ---                                                                   | 
| *appid         | number | Your app id                                                           | 
| *secret        | string | Your app secret                                                       | 
| *page      | number | The Number of page per 10 record                                          | 


### Sample JSON Request

Below is the following sample JSON __POST__ method request to list all the SIP endpoint.

```javascript
{
"appid": 2222223,
"secret": "635a5e93-3e5f-4aa5-b7ab-2a04cd5es039",
"page": 1
}
```
### Sample JSON Response

If the provided information is valid, your web server will get a sample response from PIOPIY Platform as given below

```javascript
{
    "code": "cmi-200",
    "list": {
        "count": 4,
        "rows": [
            {
                "username": "YOUR_USERNAME",
                "password": "YOUR_PASSWORD"
            },
            {
                "username": "YOUR_USERNAME_1",
                "password": "YOUR_PASSWORD"
            },
            {
                "username": "YOUR_USERNAME_2",
                "password": "YOUR_PASSWORD"
            },
            {
                "username": "YOUR_USERNAME_3",
                "password": "YOUR_PASSWORD"
            }
        ]
    }
}
```

## Remove SIP Endpoint 

To remove SIP endpoint, send your __POST__ method request with valid parameters to the following base URL.

### Base URL

```
https://piopiy.telecmi.com/v1/endpoint/remove_sip

```
### Required Parameters

These are the required __POST__ method parameters with description

| Parameter Name| Type   |      Description                                                      |  
|  ---          |    --- | ---                                                                   | 
| *appid         | number | Your app id                                                           | 
| *secret        | string | Your app secret                                                       | 
| *username      | string | The name of the existing user                                          | 


### Sample JSON Request

Below is the following sample JSON __POST__ method request to remove SIP endpoint.

```javascript
{
"appid": 2222223,
"secret": "635a5e93-3e5f-4aa5-b7ab-2a04cd5es039",
"username": "YOUR_USERNAME"
}
```
### Sample JSON Response

If the provided information is valid, your web server will get a sample response from PIOPIY Platform as given below

```javascript
{
    "code": "cmi-200",
    "username": "YOUR_USERNAME",
    "msg": "Removed successfully"
}
```

## Connect Call to SIP Endpoint

The Connect call to SIP Endpoint will be PIOPIY call management object. PIOPIY call management object is a JSON, that is used to control all the voice calls and video calls made through the PIOPIY API platform. If your PIOPIY phone number gets the incoming call, our PIOPIY platform will check for the answer URL associated with the phone number. Then the answer URL will make a request to the POST method URL and execute your PCMO actions.

The connect action will connect the call to other SIP endpoint. For example, when the caller dials the SIP endpoint, the incoming call can be routed to SIP endpoint APP or Browser at a time.

### Connect action JSON

#### Group

Connects video or audio call to multiple SIP endpoint

```javascript
[
        {
            "action": "connect",
            "duration": 600,
            "timeout": 20,
            "from": 914471000000,
            "loop": 1,
            "call_type": 'audio',
            "ring_type": "group",
            "call": [
                {
                    "type": "sip",
                    "user": "YOUR_USERNAME"
                },
                {
                    "type": "sip",
                    "user": "YOUR_USERNAME_1"
                }
            ]
        }
    ]
```

#### Single

Connects video or audio call to single SIP endpoint

```javascript
[
        {
            "action": "connect",
            "duration": 600,
            "timeout": 20,
            "from": 914471000000,
            "loop": 1,
            "call_type": 'audio',
            "call": [
                {
                    "type": "sip",
                    "user": "YOUR_USERNAME"
                }
            ]
        }
    ]
```