[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)[![semantic-release: conventional](https://img.shields.io/badge/semantic--release-conventional-e10079?logo=semantic-release)](https://github.com/semantic-release/semantic-release)

# Information Security Management Process Support Module

This repository contains a terraform module for provisioning the resources needed for the services supporting the [Information Security Management (ISM)]()
<!-- Why the heck is FitSM not callable!? -->

It provides resources at edge (Cloudflare) and data center (Nomad) locations.
See below for specific resources, data sources and provisioners.

## SMS Support Services

The services provisioned by this module are:

1. Dependency Track

## Jira integration

This module is designed to be integrated with Jira in order to track specific ticket types in the service management system.
Features include:

1. Automated ticket creation in Jira when vulnerabilities are discovered in components
1. Bidirectional synchronisation between Dependency Track and Jira for tickets managing vulnerabilities

## Edge resources

This module makes explicit use of Cloudflare features in order to implement the functionality.
Events are delivered to workers which use KV stores to looking cached configuration and state data.
API Keys are stored as Secrets and available only to the workers bound to them via their environment.

## Pre-commit hooks


The [pre-commit](https://pre-commit.com) framework is used to manage pre-commit hooks for this repository.
A few well-known hooks are provided to cover correctness, security and safety in terraform.
See [`.pre-commit-config.yaml`](.pre-commit-config.yaml)


<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >1.2.0 |

## Providers

No providers.

## Modules

No modules.

## Resources

No resources.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_dummy"></a> [dummy](#input\_dummy) | dummy variable | `string` | n/a | yes |

## Outputs

No outputs.
<!-- END_TF_DOCS -->
