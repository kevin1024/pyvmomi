vim.OvfManager.CreateImportSpecParams
=====================================
inherits from [vim.OvfManager.CommonParams](docs/vim.OvfManager.CommonParams.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Parameters for deploying an OVF.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entityName | string | None | None | The name to set on the entity (more precisely, on the top-level vApp or  VM of the entity) as it appears in VI. If empty, the product name is obtained  from the ProductSection of the descriptor. If that name is not specified, the  ovf:id of the top-level entity is used. |
| hostSystem | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | The host to validate the OVF descriptor against, if it cannot be deduced from  the resource pool.  <p>  The privilege System.Read is required on the host. |
| networkMapping | [vim.OvfManager.NetworkMapping](vim.OvfManager.NetworkMapping.md "vim.OvfManager.NetworkMapping") | true | None | The mapping of network identifiers from the descriptor to networks in the VI  infrastructure.  <p>  The privilege Network.Assign is required on all networks in the list. |
| ipAllocationPolicy | string | true | None | The IP allocation policy chosen by the caller.          <p>  See <a href="vim.vApp.IPAssignmentInfo.md">VAppIPAssignmentInfo</a>. |
| ipProtocol | string | true | None | The IP protocol chosen by the caller.          <p>  See <a href="vim.vApp.IPAssignmentInfo.md">VAppIPAssignmentInfo</a>. |
| propertyMapping | [vim.KeyValue](vim.KeyValue.md "vim.KeyValue") | true | None | The assignment of values to the properties found in the descriptor. If no value  is specified for an option, the default value from the descriptor is used. |
| resourceMapping | [vim.OvfManager.ResourceMap](vim.OvfManager.ResourceMap.md "vim.OvfManager.ResourceMap") | true | None | The resource configuration for the created vApp. This can be used to distribute   a vApp across  multiple resource pools (and create linked children). |
| diskProvisioning | string | true | None | An optional disk provisioning. If set, all the disks in the deployed OVF will  have get the same specified disk type (e.g., thin provisioned).    The valide values for disk provisioning are:   <ul>   <li><a href="vim.OvfManager.CreateImportSpecParams.DiskProvisioningType.md#monolithicSparse">monolithicSparse</a>   <li><a href="vim.OvfManager.CreateImportSpecParams.DiskProvisioningType.md#monolithicFlat">monolithicFlat</a>   <li><a href="vim.OvfManager.CreateImportSpecParams.DiskProvisioningType.md#twoGbMaxExtentSparse">twoGbMaxExtentSparse</a>   <li><a href="vim.OvfManager.CreateImportSpecParams.DiskProvisioningType.md#twoGbMaxExtentFlat">twoGbMaxExtentFlat</a>   <li><a href="vim.OvfManager.CreateImportSpecParams.DiskProvisioningType.md#thin">thin</a>   <li><a href="vim.OvfManager.CreateImportSpecParams.DiskProvisioningType.md#thick">thick</a>   <li><a href="vim.OvfManager.CreateImportSpecParams.DiskProvisioningType.md#sparse">sparse</a>   <li><a href="vim.OvfManager.CreateImportSpecParams.DiskProvisioningType.md#flat">flat</a>    <li><a href="vim.OvfManager.CreateImportSpecParams.DiskProvisioningType.md#seSparse">seSparse</a>   </ul><br>See <a href="vim.vm.device.VirtualDiskOption.DiskMode.md">VirtualDiskMode</a><br> |
| instantiationOst | [vim.OvfConsumer.OstNode](vim.OvfConsumer.OstNode.md "vim.OvfConsumer.OstNode") | true | None | The instantiation OST to configure OVF consumers. This is created by the client  from the annotated OST. See <a href="vim.OvfConsumer.md">OvfConsumer</a> for details. |


