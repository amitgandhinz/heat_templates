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
    "stack_name": "drawbuildplay.com",
    "timeout_mins": 15,
    "template_url": "https://raw.githubusercontent.com/amitgandhinz/heat_templates/master/drawbuildplay.com/DNS.yaml",
    "parameters" : {
      "hostname" : "drawbuildplay.com",
      "email" : "amit@gandhi.co.nz"
    }
}
```
