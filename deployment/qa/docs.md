## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.1.0 |
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | =2.71.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | =2.71.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_acr"></a> [acr](#module\_acr) | ../../modules/acr | n/a |
| <a name="module_acr_private_dns_zone"></a> [acr\_private\_dns\_zone](#module\_acr\_private\_dns\_zone) | ../../modules/privatednszone | n/a |
| <a name="module_acr_private_endpoint"></a> [acr\_private\_endpoint](#module\_acr\_private\_endpoint) | ../../modules/privateendpoint | n/a |
| <a name="module_aks-cluster"></a> [aks-cluster](#module\_aks-cluster) | ../../modules/aks-cluster | n/a |
| <a name="module_aks-network"></a> [aks-network](#module\_aks-network) | ../../modules/aks-network | n/a |
| <a name="module_argo"></a> [argo](#module\_argo) | ../../modules/argocd | n/a |

## Resources

| Name | Type |
|------|------|
| [azurerm_resource_group.aks](https://registry.terraform.io/providers/hashicorp/azurerm/2.71.0/docs/resources/resource_group) | resource |
| [azurerm_role_assignment.acrpull](https://registry.terraform.io/providers/hashicorp/azurerm/2.71.0/docs/resources/role_assignment) | resource |
| [azurerm_role_assignment.resourcegroup_vnet](https://registry.terraform.io/providers/hashicorp/azurerm/2.71.0/docs/resources/role_assignment) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_acr_name"></a> [acr\_name](#input\_acr\_name) | ACR name | `string` | `"acrstandardqa"` | no |
| <a name="input_address_space"></a> [address\_space](#input\_address\_space) | The address space that is used the virtual network | `string` | `"10.1.0.0/16"` | no |
| <a name="input_appgw_cidr"></a> [appgw\_cidr](#input\_appgw\_cidr) | appgw subnet cidr | `string` | `"10.1.6.0/24"` | no |
| <a name="input_appgw_subnetname"></a> [appgw\_subnetname](#input\_appgw\_subnetname) | appgw subnet name | `string` | `"appgw-aks-wesco-standard-qa"` | no |
| <a name="input_cluster_name"></a> [cluster\_name](#input\_cluster\_name) | This variable defines the AKS Cluster Name | `string` | `"aks-wesco-standard-qa"` | no |
| <a name="input_dns_prefix"></a> [dns\_prefix](#input\_dns\_prefix) | DNS Prefix | `string` | `"aks-wesco-standard-qa"` | no |
| <a name="input_kubernetes_version"></a> [kubernetes\_version](#input\_kubernetes\_version) | n/a | `string` | `"1.21.9"` | no |
| <a name="input_location"></a> [location](#input\_location) | Location | `string` | `"eastus"` | no |
| <a name="input_max_pods"></a> [max\_pods](#input\_max\_pods) | maximum number of pods that can run on a single node | `string` | `"110"` | no |
| <a name="input_network_security_group_name"></a> [network\_security\_group\_name](#input\_network\_security\_group\_name) | network security group name | `string` | `"nsg-aks-wesco-standard-qa"` | no |
| <a name="input_node_count"></a> [node\_count](#input\_node\_count) | number of nodes to deploy | `string` | `"2"` | no |
| <a name="input_os_disk_size_gb"></a> [os\_disk\_size\_gb](#input\_os\_disk\_size\_gb) | size of the OS disk to attach to the nodes | `string` | `"100"` | no |
| <a name="input_os_type"></a> [os\_type](#input\_os\_type) | type of OS to run on nodes | `string` | `"Linux"` | no |
| <a name="input_pendpoint_cidr"></a> [pendpoint\_cidr](#input\_pendpoint\_cidr) | private endpoint subnet cidr | `string` | `"10.1.5.0/24"` | no |
| <a name="input_pendpoint_subnetname"></a> [pendpoint\_subnetname](#input\_pendpoint\_subnetname) | n/a | `string` | `"pe-aks-wesco-standard-qa"` | no |
| <a name="input_resource_group"></a> [resource\_group](#input\_resource\_group) | Resoruce Group Name | `string` | `"rg-wesco-standard-qa"` | no |
| <a name="input_subnet_cidr"></a> [subnet\_cidr](#input\_subnet\_cidr) | the subnet Address range | `string` | `"10.1.0.0/22"` | no |
| <a name="input_subnet_name"></a> [subnet\_name](#input\_subnet\_name) | name to give the subnet | `string` | `"snet-aks-wesco-standard-qa"` | no |
| <a name="input_vm_size"></a> [vm\_size](#input\_vm\_size) | size/type of VM to use for nodes | `string` | `"Standard_DS2_v2"` | no |
| <a name="input_vnet_name"></a> [vnet\_name](#input\_vnet\_name) | name of the vnet that this subnet will belong to | `string` | `"vnet-aks-wesco-standard-qa"` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_k8shostname"></a> [k8shostname](#output\_k8shostname) | n/a |
