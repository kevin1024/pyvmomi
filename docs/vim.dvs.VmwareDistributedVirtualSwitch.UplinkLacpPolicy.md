vim.dvs.VmwareDistributedVirtualSwitch.UplinkLacpPolicy
=======================================================
inherits from [vim.InheritablePolicy](docs/vim.InheritablePolicy.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)
### DEPRECATED



This class defines VMware specific Link Aggregation Control Protocol   policy.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enable | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | The flag to indicate whether or not   Link Aggregation Control Protocol is enabled.   It can be set to true if the value of   <a href="vim.dvs.VmwareDistributedVirtualSwitch.ConfigInfo.md#lacpApiVersion">lacpApiVersion</a>   is LacpApiVersion#singleLag,   else an exception ConflictingConfiguration will be thrown. |
| mode | [vim.StringPolicy](vim.StringPolicy.md "vim.StringPolicy") | true | None | The mode of Link Aggregation Control Protocol.   See UplinkLacpMode for valid values. |


