heat_templates
==============

A collection of Openstack Heat Templates

Example Usage
=============

POST /v1/{{project_id}}/stacks HTTP/1.1
Host: ord.orchestration.api.rackspacecloud.com
Content-Type: application/json; charset=utf-8
X-Auth-Token: {{token}}
X-Auth-Key: {{apikey}}
X-Auth-User: {{username}}


{
    "stack_name": "marconi",
    "timeout_mins": 15,
    "template_url": "https://gist.githubusercontent.com/amitgandhinz/11265123/raw",
    "parameters" : {
      "image": "Ubuntu 14.04 LTS (Trusty Tahr)",
      "flavor": "1 GB Performance",
      "web_nodes_count": 2,
      "mongo_nodes_count" 3
      
    }
}