---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "netbox_cluster_group Data Source - terraform-provider-netbox"
subcategory: ""
description: |-
  
---

# netbox_cluster_group (Data Source)



## Example Usage

```terraform
data "netbox_cluster_group" "dc_west" {
  name = "dc-west"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String)

### Read-Only

- `cluster_group_id` (Number)
- `id` (String) The ID of this resource.


