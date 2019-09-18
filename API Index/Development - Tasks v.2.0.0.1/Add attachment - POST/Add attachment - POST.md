# Add attachment - POST

POST /v2/tasks

## Description



* [Request Payloads](#request-payloads)
* [Response Payloads](#response-payloads)

|                                       |                                                 |
| ------------------------------------- | ----------------------------------------------- |
| HTTP Method                           | Post                                         |
| API                                   | Tasks                                           |
| Api Version                           | 2.0.0.1                                         |
| Resource Version                      | 1                                               |
| Summary                               | Add an attachment                                      |
| Base Path                             | /v2/tasks                                     |
| Resource                              | Add attachment                                      |
| Endpoint URL                          | https://api-dev.test.com/v2/tasks              |
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
| File | &#xA;&#xA;Represent upload file&#xA; |  -  | No | No | No | No |  -  | Data Type : object<br>  |
| >File Name |  | hello.jpg | No | No | No | No |  -  | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |
| >Original File Name |  | Untitled.txt | No | No | No | No |  -  | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |
| >File Size |  | 200000 | No | No | No | No |  -  | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |



#### Json sample
```
{
  "name": "hello.jpg",
  "originalFileName": "Untitled.txt",
  "size": "200000"
}
```


#### Json Schema
```
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "title": "File",
  "description": "<p>Represent upload file</p>",
  "type": "object",
  "properties": {
    "name": {
      "title": "File Name",
      "type": "string",
      "items": []
    },
    "originalFileName": {
      "title": "Original File Name",
      "type": "string",
      "items": []
    },
    "size": {
      "title": "File Size",
      "type": "string",
      "items": []
    }
  },
  "required": [
    "name"
  ],
  "items": []
}
```

---