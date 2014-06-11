vim.host.VMotionConfig
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object configuring VMotion on the host.   The runtime information is available from the    <a href="vim.host.VMotionInfo.md">VMotionInfo</a> data object type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vmotionNicKey | string | true | None | Key of the VirtualNic used for VMotion. |
| enabled | bool | None | None | Flag to indicate whether or not VMotion is enabled. |


