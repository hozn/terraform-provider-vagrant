---
page_title: "Provider: Vagrant"
description: |-
  Integrate vagrant into terraform.
---

# Vagrant Provider
A Vagrant provider for terraform.

A note about lippertmarkus/vagrant in the registry: when I originally wrote
this provider, the terraform registry didn't exist. My terraform needs waned
and I didn't hear about the registry until some time later. lippertmarkus
forked my provider and published to the registry as a convenience. Thanks! But,
it's just an older version of this exact same codebase. So, I recommend you use
bmatcuk/vagrant to get the latest updates instead.

## Installation
Add bmatcuk/vagrant to [required_providers](https://www.terraform.io/docs/language/providers/requirements.html#requiring-providers):

```terraform
terraform {
  required_providers {
    vagrant = {
      source  = "bmatcuk/vagrant"
      version = "~> 3.0.0"
    }
  }
}
```

## Example Usage

```terraform
provider "vagrant" {
  # no config
}
```

<!-- schema generated by tfplugindocs -->
## Schema

## Debugging
If terrafrom is failing on the vagrant step, you can get additional output by
running terraform with logging output enabled. Try something like:

```bash
env TF_LOG=TRACE terraform apply ...
```

And, of course, you can always run vagrant on your Vagrantfile directly.