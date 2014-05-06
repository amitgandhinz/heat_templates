Example Usage
=============


```
POST /v1/{{project_id}}/stacks HTTP/1.1
Host: ord.orchestration.api.rackspacecloud.com
Content-Type: application/json; charset=utf-8
X-Auth-Token: {{token}}
X-Auth-Key: {{apikey}}
X-Auth-User: {{username}}


{
    "stack_name": "gandhi.co.nz",
    "timeout_mins": 15,
    "template_url": "https://raw.githubusercontent.com/amitgandhinz/heat_templates/master/gandhi.co.nz/DNS.yaml",
    "parameters" : {
      "hostname" : "gandhi.co.nz",
      "email" : "amit@gandhi.co.nz"
    }
}
```
