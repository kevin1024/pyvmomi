vim.cluster.FixedSizeSlotPolicy
===============================
inherits from [vim.cluster.SlotPolicy](docs/vim.cluster.SlotPolicy.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


This policy allows setting a fixed slot size

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| cpu | int | None | None | The cpu component of the slot size (in MHz) |
| memory | int | None | None | The memory component of the slot size (in megabytes) |


