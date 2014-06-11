vim.host.MultipathInfo.Path
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.host.MultipathInfo.Path.md">HostMultipathInfoPath</a> data object   is a storage entity that represents a topological path from a   host bus adapter to a SCSI logical unit.  Each path is unique although each   host bus adapter/SCSI logical unit pair can have multiple paths.   <p>   Path objects are identified by a key.  The specifics of how   the key is formatted are dependent on the implementation.  Example   implementations include using strings like "vmhba1:0:0:0".

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Identifier of the path. |
| name | string | None | None | Name of path.   <p>   Use this name to configure LogicalUnit multipathing policy using <a href="vim.host.StorageSystem.md#enableMultipathPath">EnableMultipathPath</a> and <a href="vim.host.StorageSystem.md#disableMultipathPath">DisableMultipathPath</a>. |
| pathState | string | None | None | State of the path.  Must be one of the values of   <a href="vim.host.MultipathInfo.PathState.md">MultipathState</a>   <dl>     <dt>active</dt>     <dd>Path can be used for I/O and is currently a working path.</dd>     <dt>standby</dt>     <dd>Path can be used for I/O but is not a working path or can be     used if active paths fail.</dd>     <dt>disabled</dt>     <dd>Path has been administratively disabled.</dd>     <dt>dead</dt>     <dd>Path cannot be used for I/O.</dd>     <dt>unknown</dt>     <dd>Path is in unknown error state.</dd>   </dl> |
| state | string | true | None | System-reported state of the path. Must be one of the values of   <a href="vim.host.MultipathInfo.PathState.md">MultipathState</a>  <dl>     <dt>active</dt>     <dd>Path can be used for I/O.</dd>     <dt>standby</dt>     <dd>Path can be used for I/O if active paths fail.</dd>     <dt>disabled</dt>     <dd>Path has been administratively disabled.</dd>     <dt>dead</dt>     <dd>Path cannot be used for I/O.</dd>     <dt>unknown</dt>     <dd>Path is in unknown error state.</dd>  </dl> |
| isWorkingPath | bool | true | None | A path, managed by a given path selection policy(psp) plugin, is  denoted to be a Working Path if the psp plugin is likely to select the  path for performing I/O in the near future. |
| adapter | [vim.host.HostBusAdapter](vim.host.HostBusAdapter.md "vim.host.HostBusAdapter") | None | None | The host bus adapter at one endpoint of this path. |
| lun | [vim.host.MultipathInfo.LogicalUnit](vim.host.MultipathInfo.LogicalUnit.md "vim.host.MultipathInfo.LogicalUnit") | None | None | The logical unit at one endpoint of this path. |
| transport | [vim.host.TargetTransport](vim.host.TargetTransport.md "vim.host.TargetTransport") | true | None | Transport information for the target end of the path. |


