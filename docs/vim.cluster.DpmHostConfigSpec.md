vim.cluster.DpmHostConfigSpec
=============================
inherits from [vim.option.ArrayUpdateSpec](docs/vim.option.ArrayUpdateSpec.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


The <a href="vim.cluster.DpmHostConfigSpec.md">ClusterDpmHostConfigSpec</a> data object provides information   that the Server uses to update the DPM configuration for a   single host (identified by the   <a href="vim.cluster.DpmHostConfigInfo.md#key">key</a> property).   The host DPM configuration overrides the cluster   default DPM setting   (<a href="vim.cluster.ConfigSpecEx.md">ClusterConfigSpecEx</a>.<a href="vim.cluster.ConfigSpecEx.md#dpmConfig">dpmConfig</a>).   <p>   The vSphere API defines three update operations (<a href="vim.option.ArrayUpdateSpec.md">ArrayUpdateSpec</a>.<a href="vim.option.ArrayUpdateSpec.md#operation">operation</a>).   <ul>    <li> add: Define DPM behavior for a host. If the cluster        configuration already includes a DPM behavior override        for the specified host, this operation        removes the existing override and adds the new one.        The new DPM override will use the cluster default value        if you do not specify the behavior property        (<a href="vim.cluster.DpmConfigInfo.md#defaultDpmBehavior">defaultDpmBehavior</a>).    </li>    <li> edit: Perform an incremental update to an existing        DPM configuration entry for a host.        The reconfigure method changes only the properties        that you set in the data object. The entry must exist        in the        <a href="vim.cluster.ConfigSpecEx.md">ClusterConfigSpecEx</a>.<a href="vim.cluster.ConfigSpecEx.md#dpmHostConfigSpec">dpmHostConfigSpec</a> array.    </li>    <li> remove: Remove the DPM override for the specified        host. To identify the host to delete, use the        <a href="vim.option.ArrayUpdateSpec.md#removeKey">removeKey</a> property        to specify the <a href="vim.cluster.DpmHostConfigInfo.md#key">key</a>        in the host override.    </li>   </ul>   <p>   Use the <a href="vim.ComputeResource.md#reconfigureEx">ReconfigureComputeResource_Task</a> method   to update the DPM configuration. If you set the modify parameter   to true, you can use any of the three operations (add, edit, or remove).   If you set the modify parameter to false, you can use only the   add operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| info | [vim.cluster.DpmHostConfigInfo](vim.cluster.DpmHostConfigInfo.md "vim.cluster.DpmHostConfigInfo") | true | None |  |


