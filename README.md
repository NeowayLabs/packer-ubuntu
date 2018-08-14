# Packer images

Default image builder for Neoway environment.

## Prerequisites

* [Docker](https://docs.docker.com/engine/installation/)

## Getting started

### Export your credentials as environment variables

[Create Azure Service Principal](https://www.terraform.io/docs/providers/azurerm/authenticating_via_service_principal.html) then export the credentials.

```bash
$ export AZURE_CLIENT_ID=YOUR_AZURE_CLIENT_ID
$ export AZURE_CLIENT_SECRET=YOUR_AZURE_CLIENT_SECRET
$ export AZURE_SERVICE_PRINCIPAL=YOUR_AZURE_SERVICE_PRINCIPAL
$ export AZURE_SUBSCRIPTION_ID=YOUR_AZURE_SUBSCRIPTION_ID
$ export AZURE_TENANT_ID=YOUR_AZURE_TENANT_ID
```

### Setup

Setup the docker image with [Terraform](https://www.terraform.io/) and [Packer](https://packer.io) to get things done.

```bash
$ make setup
```

### Initialize the packer environment

```bash
$ make terraform-init
```

### Create the packer environment

```bash
$ make terraform-apply
```

### Initialize packer

```bash
$ make packer-build
```

### Destroy the packer environment

TIP: Just use this if you want destroy everything what you build (include the packer image).

```bash
$ make terraform-destroy
```