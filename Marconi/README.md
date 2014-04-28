Example Usage
=============

Note - *this* Marconi Heat template is not deployment ready yet.
 - Done -> Servers spin up
 - Done -> MongoDB, Memcache, and Marconi Software is installed on to the servers
 - TODO -> Servers are currently misconfigured
 - TODO -> ReplicaSets are not yet configured
 - TODO -> Marconi WSGI app is not configured to point to Mongo
 - TODO -> There are likely security holes in the configuration currently, leaving your servers potentially vulnerable to hackers.

Template generated using Marconi Installation Guide found here (as of Apr 28, 2014)
 - https://github.com/openstack/marconi/blob/master/doc/source/installing.rst

```
POST /v1/{{project_id}}/stacks HTTP/1.1
Host: ord.orchestration.api.rackspacecloud.com
Content-Type: application/json; charset=utf-8
X-Auth-Token: {{token}}
X-Auth-Key: {{apikey}}
X-Auth-User: {{username}}


{
    "stack_name": "marconi",
    "timeout_mins": 15,
    "template_url": "https://raw.githubusercontent.com/amitgandhinz/heat_templates/master/Marconi/marconi.yaml",
    "parameters" : {
      "image": "Ubuntu 14.04 LTS (Trusty Tahr)",
      "flavor": "1 GB Performance",
      "web_nodes_count": 2,
      "mongo_nodes_count" 3,
      "admin_password": "test",
      "admin_tenant_name": "admin name",
      "admin_user": "admin user",
      "admin_keystone_uri": "https://admin.keystone.com",
      "keystone_uri": "https://keystone.com",
      "keystone_version": "v2.0",
      "token_cache_time": 3600
    }
}
```
