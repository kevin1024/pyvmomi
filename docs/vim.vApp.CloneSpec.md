vim.vApp.CloneSpec
==================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Specification for a vApp cloning operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| location | [vim.Datastore](vim.Datastore.md "vim.Datastore") | None | Datastore.AllocateSpace | Location where the destination vApp must be stored |
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | VApp.Create | The target host for the virtual machines. This is often not a required   parameter. If not specified, the behavior is as follows:   <ul>      <li> If the target pool represents a stand-alone host, that host is used.      <li> If the target pool represents a DRS-enabled cluster, a host selected           by DRS is used.      <li> If the target pool represents a cluster without DRS enabled or a           DRS-enabled cluster in manual mode, an InvalidArgument exception is           thrown.   </ul> |
| resourceSpec | [vim.ResourceConfigSpec](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec") | true | None | The resource configuration for the vApp. |
| vmFolder | [vim.Folder](vim.Folder.md "vim.Folder") | true | VApp.Create | The VM Folder to associate the vApp with |
| networkMapping | [vim.vApp.CloneSpec.NetworkMappingPair](vim.vApp.CloneSpec.NetworkMappingPair.md "vim.vApp.CloneSpec.NetworkMappingPair") | true | None | Network mappings. See NetworkMappingPair. |
| property | [vim.KeyValue](vim.KeyValue.md "vim.KeyValue") | true | None | A set of property values to override. |
| resourceMapping | [vim.vApp.CloneSpec.ResourceMap](vim.vApp.CloneSpec.ResourceMap.md "vim.vApp.CloneSpec.ResourceMap") | true | None | The resource configuration for the cloned vApp. |
| provisioning | string | true | None | Specify how the VMs in the vApp should be provisioned. |


