vim.dvs.VmwareDistributedVirtualSwitch.PvlanConfigSpec
======================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This class defines the configuration of a PVLAN map entry

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| pvlanEntry | [vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry](vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry.md "vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry") | None | None | The PVLAN entry to be added or removed. |
| operation | string | None | None | Operation type.  See   <a href="vim.ConfigSpecOperation.md">ConfigSpecOperation</a> for valid values,   except for the "edit" value, which is not supported. |


