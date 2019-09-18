# Update user password - PUT ONE

PUT /v2/user

## Description



* [Request Payloads](#request-payloads)
* [Response Payloads](#response-payloads)

|                                       |                                                 |
| ------------------------------------- | ----------------------------------------------- |
| HTTP Method                           | Put                                         |
| API                                   | User                                           |
| Api Version                           | 2.0.0.3                                         |
| Resource Version                      | 1                                               |
| Summary                               | To update user password                                      |
| Base Path                             | /v2/user                                     |
| Resource                              | Update user password                                      |
| Endpoint URL                          | https://api-dev.test.com/v2/user              |
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
| Password | &#xA;&#xA;Hard password &#xA; | sdvz@$RCvcv | No | No | No | No |  -  | Data Type : string<br> Min. length : 8<br> Max. length : No<br> Regex :  - <br>  |



#### Json sample
```
{
  "pass": "sdvz@$RCvcv"
}
```


#### Json Schema
```
{
  "title": "",
  "type": "object",
  "properties": {
    "pass": {
      "title": "Password",
      "description": "<p>Hard password </p>",
      "type": "string",
      "items": [],
      "minLength": 8,
      "maxLength": 100
    }
  },
  "required": [
    "pass"
  ],
  "items": []
}
```

---