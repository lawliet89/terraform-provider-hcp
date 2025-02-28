---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "hcp_hvn_route Data Source - terraform-provider-hcp"
subcategory: ""
description: |-
  The HVN route data source provides information about an existing HVN route.
---

# hcp_hvn_route (Data Source)

The HVN route data source provides information about an existing HVN route.

## Example Usage

```terraform
data "hcp_hvn_route" "example" {
  hvn_link         = var.hvn_link
  destination_cidr = var.hvn_route_id
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `hvn_link` (String) The `self_link` of the HashiCorp Virtual Network (HVN).
- `hvn_route_id` (String) The ID of the HVN route.

### Optional

- `project_id` (String, Deprecated) The ID of the HCP project where the HVN route is located. Always matches the project ID in `hvn_link`. Setting this attribute is deprecated, but it will remain usable in read-only form.
- `timeouts` (Block, Optional) (see [below for nested schema](#nestedblock--timeouts))

### Read-Only

- `created_at` (String) The time that the HVN route was created.
- `destination_cidr` (String) The destination CIDR of the HVN route.
- `id` (String) The ID of this resource.
- `self_link` (String) A unique URL identifying the HVN route.
- `state` (String) The state of the HVN route.
- `target_link` (String) A unique URL identifying the target of the HVN route.

<a id="nestedblock--timeouts"></a>
### Nested Schema for `timeouts`

Optional:

- `default` (String)
