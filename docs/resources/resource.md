---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "twingate_resource Resource - terraform-provider-twingate"
subcategory: ""
description: |-
  
---

# twingate_resource (Resource)





<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **address** (String) The resource's IP/FQDN
- **name** (String) name of the resource

### Optional

- **group_ids** (List of String) List of group IDs added to the resource
- **protocols** (Block List, Max: 1) Restrict access to certain protocols and ports. By default or when this argument is not defined, there is no restriction i.e. all protocols and ports are allowed. (see [below for nested schema](#nestedblock--protocols))
- **remote_network_id** (String) Remote Network ID to assign to the resource

### Read-Only

- **id** (String) Autogenerated ID of the resource in encoded in base64

<a id="nestedblock--protocols"></a>
### Nested Schema for `protocols`

Required:

- **tcp** (Block List, Min: 1, Max: 1) (see [below for nested schema](#nestedblock--protocols--tcp))
- **udp** (Block List, Min: 1, Max: 1) (see [below for nested schema](#nestedblock--protocols--udp))

Optional:

- **allow_icmp** (Boolean) Whether to allow ICMP throughput

<a id="nestedblock--protocols--tcp"></a>
### Nested Schema for `protocols.tcp`

Required:

- **policy** (String) Whether to allow all ports or restrict protocol access within certain port ranges.

Optional:

- **ports** (List of String)


<a id="nestedblock--protocols--udp"></a>
### Nested Schema for `protocols.udp`

Required:

- **policy** (String) Whether to allow all ports or restrict protocol access within certain port ranges.

Optional:

- **ports** (List of String)

