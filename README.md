
# Terraform Azure VM Deployment

This repository contains Terraform code to deploy a virtual machine (VM) in Azure along with other necessary resources such as network security groups, public IP addresses, virtual networks, etc.

## Prerequisites

Before getting started, make sure you have the following installed on your local machine:

- [Terraform](https://www.terraform.io/downloads.html)
- [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)

## **_Build With_** 

<div style="text-align: left">
    <p>
        <a href="https://code.visualstudio.com" target="_blank"> <img alt="V" src="https://raw.githubusercontent.com/devicons/devicon/55609aa5bd817ff167afce0d965585c92040787a/icons/vscode/vscode-original.svg" height="60" width = "60"></a>
        <a href="https://www.terraform.io/" target="blank"><img src="https://static-00.iconduck.com/assets.00/terraform-icon-1803x2048-hodrzd3t.png" width="60" alt="Terraform Logo" /></a>
        <a href="https://https://portal.azure.com/#home/" target="blank"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fa/Microsoft_Azure.svg/1200px-Microsoft_Azure.svg.png" width="60" alt="Azure Logo" /></a>
   
    </p>
</div>

## Configuration

1. Clone this repository to your local machine:

    ```bash
    git clone <repository_url>
    ```

2. Change to the cloned directory:

    ```bash
    cd terraform-azure-vm
    ```

3. Create a `terraform.tfvars` file and provide values for the `name_vm` (VM name) and `location` (location) variables:

    ```hcl
    name_vm = "vm_name"
    location = "location"
    ```

## Deployment

The Terraform code in this repository deploys the following resources in Azure:

- A virtual machine with Ubuntu Server image.
- A public IP address for the virtual machine.
- A network security group to control network traffic.
- A virtual network with an internal subnet.
- A security rule to allow incoming SSH traffic.

To deploy the infrastructure in Azure, follow these steps:

1. Initialize the Terraform directory:

    ```bash
    terraform init
    ```

2. Review the resources that will be created:

    ```bash
    terraform plan
    ```

3. Apply the changes to create the resources:

    ```bash
    terraform apply
    ```

    You will be prompted to confirm before applying the changes. Respond with `yes`.

## Cleanup

To delete the resources created in Azure, run:

```bash
terraform destroy
