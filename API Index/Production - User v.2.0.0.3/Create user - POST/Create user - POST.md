# Create user - POST

POST /v2/user

## Description

&#xA;&#xA;Create user in the system&#xA;

* [Request Payloads](#request-payloads)
* [Response Payloads](#response-payloads)

|                                       |                                                 |
| ------------------------------------- | ----------------------------------------------- |
| HTTP Method                           | Post                                         |
| API                                   | User                                           |
| Api Version                           | 2.0.0.3                                         |
| Resource Version                      | 1                                               |
| Summary                               | to create user                                      |
| Base Path                             | /v2/user                                     |
| Resource                              | Create user                                      |
| Endpoint URL                          | https://api.test.com/v2/user              |
| Service Status                        | Unknown                                         |
| Legislative / Regulatory / Compliance |                                             |
| Firewalls Details                     |                                              |
| Security Certificate Details          |                                              |
| Vendor or Partner Considerations      |                                             |

## Request Payloads

### Request Header


N/A
---

### Query Params


N/A
---

### Request Body

#### Payload 



| Parameter | Description | Sample | PII | Sensitive | Unique Identifier | Mandatory | Default | Details |
| :----- | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :----- |
| User | &#xA;&#xA;User is app&#xA; |  -  | No | No | No | No |  -  | Data Type : object<br>  |
| >User Name | &#xA;&#xA;User name, unique as per user&#xA;&#xA;&#xA;Cannot be changed once created&#xA;&#xA;&#xA;Minimum 6 characters&#xA;&#xA;&#xA;Only accept alphanumeric characters&#xA; | tubxxxxx33 | **Yes** | **Yes** | Yes | No |  -  | Data Type : string<br> Min. length : 6<br> Max. length : No<br> Regex : \w<br>  |
| >Password | &#xA;&#xA;Hard password &#xA; | sdvz@$RCvcv | No | No | No | No |  -  | Data Type : string<br> Min. length : 8<br> Max. length : No<br> Regex :  - <br>  |
| >Name |  | Tu | No | No | No | No |  -  | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |



#### Json sample
```
{
  "userName": "tubxxxxx33",
  "password": "sdvz@$RCvcv",
  "name": "Tu"
}
```


#### Json Schema
```
{
  "title": "User",
  "description": "<p>User is app</p>",
  "type": "object",
  "properties": {
    "userName": {
      "title": "User Name",
      "description": "<p>User name, unique as per user</p><p>Cannot be changed once created</p><p>Minimum 6 characters</p><p>Only accept alphanumeric characters</p>",
      "type": "string",
      "items": [],
      "minLength": 6,
      "maxLength": 30,
      "pattern": "\\w"
    },
    "password": {
      "title": "Password",
      "description": "<p>Hard password </p>",
      "type": "string",
      "items": [],
      "minLength": 8,
      "maxLength": 100
    },
    "name": {
      "title": "Name",
      "type": "string",
      "items": []
    }
  },
  "required": [
    "userName",
    "password"
  ],
  "items": []
}
```

---