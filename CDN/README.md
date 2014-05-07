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
    "stack_name": "cdn",
    "timeout_mins": 15,
    "template_url": "https://raw.githubusercontent.com/amitgandhinz/heat_templates/master/CDN/cdn.yaml",
    "parameters" : {
      "image": "Ubuntu 14.04 LTS (Trusty Tahr)",
      "flavor": "1 GB Performance",
      "web_nodes_count": 1,
      "fastly_api_key": "deadbeef",
      "git_repo" : "https://amitgandhinz:password@github.com:amitgandhinz/cdn.git"
    }
}
```
