vim.host.MultipathInfo.LogicalUnitPolicy
========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.host.MultipathInfo.LogicalUnitPolicy.md">HostMultipathInfoLogicalUnitPolicy</a> data object   describes a path selection policy for a device. This policy determines   how paths should be utilized when accessing a device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| policy | string | None | None | String representing the path selection policy for a device. Use one of the following   strings:   <p>   <ul>   <li><code>VMW_PSP_FIXED</code> - Use a preferred path whenever possible.   <li><code>VMW_PSP_RR</code> -  Load balance.   <li><code>VMW_PSP_MRU</code> -  Use the most recently used path.   </ul>    You can also use the   <a href="vim.host.StorageSystem.md#queryPathSelectionPolicyOptions">QueryPathSelectionPolicyOptions</a> method   to retrieve the set of valid strings.   Use the key from the resulting structure   <a href="vim.host.PathSelectionPolicyOption.md">HostPathSelectionPolicyOption</a>. |


