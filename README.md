# king-ghidorah

An experimental combination of the python hydra configuration library and opentofu.

[Python Hydra](https://hydra.cc/docs/intro/) is a configuration tool written in python that allows for complex management and merging of yamnl configuration files.

[OpenTofu](https://opentofu.org/) is an open source drop-in replacement for terraform.

By combining the two, we get a tool that can better handle B2B on-premise, mixed-cloud, fully cloud environments, with
customizations possible for development and production, as well as client-specific customizations.

## Why?

King Ghidorah was created to address a B2B infrastructure management at ReelData.

We support on-premise installations, mixed cloud installations, and cloud installations of our products.

Additionally, we have development and production environments where simulators are deployed to emulate the hardware our products rely upon.

Furthermore, we offer systems integrations with different third-party companies our clients use to manage their own operations.

This led to a complicated matrix of configuration options that ranged from client specific, to third party vendor specific, to location specific.

King Ghidorah addresses this by offering a straight-forward way to define common blocks of templatable configuration using hydra, and then use that configuration
to enrich an otherwise vanilla terraform plan.

### Problems we're attempting to solve

- To allow for writing simple CI scripts to update configuration, use hydra YAML config instead of `HCL` or `.tfvars`
- To allow client site specific configuration, enable defining configuration overriding per client-site
- To allow third party vendor specific configuration, enable defining configuration groups which are then applied across multiple clients
- To allow for shared configuration, enable defining default configuration
- To keep documentation for terraform helpful and relevant, keep terraform modules as simple HCL

### Alternatives

[OpenTofu](https://opentofu.org/) or [Terraform](https://www.terraform.io/)

[Terragrunt](https://terragrunt.gruntwork.io/) is the most standard recommendation for managing more complicated arrangements of deployment targets.
Terragrunt is a good tool but I wanted to get away from HCL as HCL is difficult to programmatically update from a CI file. I also wanted something that was
seperated from the terraform modules I was writing.

[Terraform CDK](https://developer.hashicorp.com/terraform/cdktf) is a great option for managing the provisioning of infrastructure to a variety of environments.
The largest downside to this tool is that it is

## Usage

It doesn't exist yet.
