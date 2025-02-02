# Automatic creation of the ESXi-based VMs and Network to support OKD4 installation


Guide to install OKD4 on a VMware ESXi machine:

[https://medium.com/@craig_robinson/guide-installing-an-okd-4-5-cluster-508a2631cbee]

These terraform files will create the basic infrastructure (virtual machines and network) in the ESXi host described in his document.

## Requirements
- Free version of VMware ESXi 6.5 (might work with other versions)
- Terraform 0.12+
- terraform-provider-esxi [https://github.com/josenk/terraform-provider-esxi]

## Usage
- Install the requirements and make sure they are functional
- Clone this repo:
`git clone https://github.com/DxDrill/OKD-Installation`
- Adjust variable values to your environment
 - Everything in vars.tf
 - MAC addresses in main.tf
- Execute:

`cd okd4-esxi-infra/terraform`

`terraform init`

`terraform plan`

`terraform apply`