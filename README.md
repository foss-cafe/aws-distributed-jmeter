# Terraform module for Jmeter Load testing
<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| terraform | ~> 0.12.24 |
| aws | ~> 2.60 |

## Providers

| Name | Version |
|------|---------|
| aws | ~> 2.60 |
| http | n/a |
| local | n/a |
| tls | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| ami | AMI image for Jmeter | `string` | n/a | yes |
| cidr\_blocks | VPC CIDR | `list` | n/a | yes |
| instance\_type | description | `string` | `"m5.large"` | no |
| name | description | `string` | `"default"` | no |
| slaves\_instance\_count | Slave count | `number` | `1` | no |
| source\_jmx | description | `list` | `[]` | no |
| subnet\_id | Subnet IDs | `string` | n/a | yes |
| subnet\_ids | A list of VPC Subnet IDs to launch in | `list(string)` | `[]` | no |
| vpc\_id | VPC ID | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| master\_ip | Jmeter Master IP addr |
| private\_key | SSH private key data |
| public\_key | SSH public Key data |
| slave\_ips | Jmeter Slave IP addrs |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
