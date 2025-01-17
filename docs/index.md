---
layout: ""
page_title: "Provider: Netbox"
description: |-
  The netbox provider provides resources and data sources to interact with Netbox.
---

# Netbox Provider

The Terraform Netbox provider is a plugin for Terraform that allows for the full lifecycle management of [Netbox](https://docs.netbox.dev/en/stable/) resources.

You must configure the provider with proper credentials before you can use it.

Use the navigation to the left to read about the available resources.

Each resource's `id` (unless otherwise specified) is computed by the resource and should not be specified for resource creation. These IDs are critical for relating different resource objects to each other - a common pattern is creating a resource / retrieving a datasource for a type of Netbox object, then using that object's id for creation in a subsequent resource (see example below)

## Example Usage

```terraform
terraform {
  required_providers {
    netbox = {
      source  = "e-breuninger/netbox"
      version = "~> 1.6"
    }
  }
}

# example provider configuration for https://demo.netbox.dev
provider "netbox" {
  server_url = "https://demo.netbox.dev/"
  api_token  = "<your api key>"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `api_token` (String) Netbox API authentication token
- `server_url` (String) Location of Netbox server including scheme and optional port

### Optional

- `allow_insecure_https` (Boolean) Flag to set whether to allow https with invalid certificates
- `headers` (Map of String) Set these header on all requests to Netbox
- `skip_version_check` (Boolean) If true, do not try to determine the running Netbox version at provider startup. Disables warnings about possibly unsupported Netbox version. Also useful for local testing on terraform plans.
