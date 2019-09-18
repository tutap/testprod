# Create task - POST

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
| Summary                               | To create task                                      |
| Base Path                             | /v2/tasks                                     |
| Resource                              | Create task                                      |
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
| Task |  |  -  | No | No | No | No |  -  | Data Type : object<br>  |
| >Id | &#xA;&#xA;Entity ID, using uuid&#xA; | b1f139fc-4b05-4a1e-bbd3-427ebc3c02dc | No | No | Yes | No |  -  | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |
| >Task Name | &#xA;&#xA;Name of the task&#xA; | do homework | No | No | No | No |  -  | Data Type : string<br> Min. length : 1<br> Max. length : No<br> Regex :  - <br>  |
| >Description | &#xA;&#xA;**Optional. **Description of the task&#xA; | lorem lipsum | No | No | No | No |  -  | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |
| >Priority | &#xA;&#xA;Priority of the task:&#xA;&#xA;&#xA;*   Urgent&#xA;*   High&#xA;*   Normal&#xA;*   Low | Normal | No | No | No | No | Normal | Data Type : string<br> Min. length :  - <br> Max. length : No<br> Regex :  - <br>  |



#### Json sample
```
{
  "id": "b1f139fc-4b05-4a1e-bbd3-427ebc3c02dc",
  "taskName": "do homework",
  "description": "lorem lipsum",
  "priority": "Normal"
}
```


#### Json Schema
```
{
  "title": "Task",
  "type": "object",
  "properties": {
    "id": {
      "title": "Id",
      "description": "<p>Entity ID, using uuid</p>",
      "type": "string",
      "items": []
    },
    "taskName": {
      "title": "Task Name",
      "description": "<p>Name of the task</p>",
      "type": "string",
      "items": [],
      "minLength": 1
    },
    "description": {
      "title": "Description",
      "description": "<p><strong>Optional. </strong>Description of the task</p>",
      "type": "string",
      "items": []
    },
    "priority": {
      "title": "Priority",
      "description": "<p>Priority of the task:</p><ul><li>Urgent</li><li>High</li><li>Normal</li><li>Low</li></ul>",
      "type": "string",
      "default": "Normal",
      "items": [],
      "enum": [
        "Urgent",
        "High",
        "Normal",
        "Low"
      ]
    }
  },
  "required": [
    "id",
    "taskName",
    "priority"
  ],
  "items": []
}
```

---