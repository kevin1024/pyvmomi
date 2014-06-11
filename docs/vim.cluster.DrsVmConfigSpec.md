vim.cluster.DrsVmConfigSpec
===========================
inherits from [vim.option.ArrayUpdateSpec](docs/vim.option.ArrayUpdateSpec.md)


Updates the per-virtual-machine DRS configuration.   <p>   To update the DRS configuration of a virtual machine, a copy of this object   is included in the <a href="vim.cluster.ConfigSpecEx.md">ClusterConfigSpecEx</a> object passed to the method   <a href="vim.ComputeResource.md#reconfigureEx">ReconfigureComputeResource_Task</a>.    <p>   If <i>reconfigureEx</i> is used to   incrementally update the cluster configuration (i.e., the parameter <b>modify</b> is true),    then three operations are provided for updating the DRS configuration for a virtual machine.    These operations are listed below (see <a href="vim.option.ArrayUpdateSpec.md">ArrayUpdateSpec</a> for more    information on these operations).    <ul>    <li> add: add a configuration for the virtual machine, overwritting the existing          configuration if one exists    <li> edit: incrmentally update the existing configuration; an existing configuration          must exist    <li> remove: remove the existing configuration; an existing configuration must exist   </ul>    If, instead, this method is used to overwrite the cluster configuration (i.e., the parameter    <b>modify</b> is false) thereby creating a new configuration, only the add operation is allowed.    In this case, <i>add</i> creates a DRS configuration for a virtual machine in the new cluster   configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| info | [vim.cluster.DrsVmConfigInfo](vim.cluster.DrsVmConfigInfo.md "vim.cluster.DrsVmConfigInfo") | true | None |  |


