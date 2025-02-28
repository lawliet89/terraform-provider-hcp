---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "hcp_hvn Data Source - terraform-provider-hcp"
subcategory: ""
description: |-
  The HVN data source provides information about an existing HashiCorp Virtual Network.
---

# hcp_hvn (Data Source)

The HVN data source provides information about an existing HashiCorp Virtual Network.

## Example Usage

```terraform
data "hcp_hvn" "example" {
  hvn_id = var.hvn_id
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `hvn_id` (String) The ID of the HashiCorp Virtual Network (HVN).

### Optional

- `project_id` (String) The ID of the HCP project where the HVN is located.
If not specified, the project specified in the HCP Provider config block will be used, if configured.
If a project is not configured in the HCP Provider config block, the oldest project in the organization will be used.
- `timeouts` (Block, Optional) (see [below for nested schema](#nestedblock--timeouts))

### Read-Only

- `cidr_block` (String) The CIDR range of the HVN.
- `cloud_provider` (String) The provider where the HVN is located.
- `created_at` (String) The time that the HVN was created.
- `id` (String) The ID of this resource.
- `organization_id` (String) The ID of the HCP organization where the HVN is located.
- `provider_account_id` (String) The provider account ID where the HVN is located.
- `region` (String) The region where the HVN is located.
- `self_link` (String) A unique URL identifying the HVN.
- `state` (String) The state of the HVN route.

<a id="nestedblock--timeouts"></a>
### Nested Schema for `timeouts`

Optional:

- `default` (String)
