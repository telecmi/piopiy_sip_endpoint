## Create SIP Endpoint

Creating SIP Endpoint allows you to make and receive video calls, where making video calls can be made to APP to APP,APP to Browser and browser to browser calling.

## Prerequisites

1. Sign up for a free <a href="https://doc.telecmi.com/piopiy/docs/get-started" target="_blank">PIOPIY demo account</a>.

2. Create your <a href="https://doc.telecmi.com/piopiy/docs/create-endpoint" target="_blank">endpoint</a> and <a href="https://doc.telecmi.com/piopiy/docs/add-capacity" target="_blank">add capacity</a>.

3. Buy <a href="https://doc.telecmi.com/piopiy/docs/choose-number" target="_blank">PIOPIY phone number</a>.

4. Setup your webserver and map your POST method URL in <a href="https://doc.telecmi.com/piopiy/docs/build-app/#app-id-and-secret" target="_blank">answer URL</a>.


## Create SIP Usermurugan1

To create a SIP user, send your __POST__ method request with valid parameters to the following base URL.

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

Below is the following sample JSON __POST__ method request to create user

```javascript
{
"appid": 2222223,
"secret": "635a5e93-3e5f-4aa5-b7ab-2a04cd5es039",
"username": "Alexa",
"password": "Alexa@123"
}
```
### Sample JSON Response

If the provided information is valid, your web server will get a sample response from PIOPIY Platform as given below

```javascript
{
    "code": "cmi-200",
    "username": "Alexa",
    "password": "Alexa@123",
    "connect_URL": "piopiysbc.telecmi.com",
    "audio": true,
    "video": true,
    "type": "SIP"
}
```

## Update SIP User

To update a SIP user password, send your __POST__ method request with valid parameters to the following base URL.

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

Below is the following sample JSON __POST__ method request to update user

```javascript
{
"appid": 2222223,
"secret": "635a5e93-3e5f-4aa5-b7ab-2a04cd5es039",
"username": "Alexa",
"password": "Alexa@1234"
}
```
### Sample JSON Response

If the provided information is valid, your web server will get a sample response from PIOPIY Platform as given below

```javascript
{
    "code": "cmi-200",
    "username": "Alexa",
    "password": "Alexa@1234",
    "msg": "Updated successfully"
}
```

## Get SIP User Details

To get a SIP user details, send your __POST__ method request with valid parameters to the following base URL.

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

Below is the following sample JSON __POST__ method request to get SIP user details.

```javascript
{
"appid": 2222223,
"secret": "635a5e93-3e5f-4aa5-b7ab-2a04cd5es039",
"username": "Alexa"
}
```
### Sample JSON Response

If the provided information is valid, your web server will get a sample response from PIOPIY Platform as given below

```javascript
{
    "code": "cmi-200",
    "username": "Alexa",
    "password": "Alexa@1234",
    "connect_URL": "piopiysbc.telecmi.com",
    "audio": true,
    "video": true,
    "type": "SIP"
}
```

## TO list all SIP user

To list all the SIP user, send your __POST__ method request with valid parameters to the following base URL.

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

Below is the following sample JSON __POST__ method request to list all the SIP user.

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
                "username": "Sam",
                "password": "Sam@123"
            },
            {
                "username": "John",
                "password": "John@123"
            },
            {
                "username": "Victor",
                "password": "Victor@123"
            },
            {
                "username": "Alexa",
                "password": "Alexa@1234"
            }
        ]
    }
}
```

## Remove SIP User 

To remove SIP user, send your __POST__ method request with valid parameters to the following base URL.

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

Below is the following sample JSON __POST__ method request to remove SIP user.

```javascript
{
"appid": 2222223,
"secret": "635a5e93-3e5f-4aa5-b7ab-2a04cd5es039",
"username": "Alexa"
}
```
### Sample JSON Response

If the provided information is valid, your web server will get a sample response from PIOPIY Platform as given below

```javascript
{
    "code": "cmi-200",
    "username": "Alexa",
    "msg": "Removed successfully"
}
```

## Forward Call to SIP user

The bridge action will connect the call to other SIP users. For example, when the caller dials the SIP user, the incoming call can be routed to SIP user APP or Browser at a time.

### Bridge action JSON

#### Group

Connects video or audio call to multiple SIP user

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
                    "user": "Sam"
                },
                {
                    "type": "sip",
                    "user": "Victor"
                }
            ]
        }
    ]
```

#### Single

Connects video or audio call to single SIP user

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
                    "user": "Sam"
                }
            ]
        }
    ]
```