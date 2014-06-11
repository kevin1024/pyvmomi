vim.CustomizationSpecInfo
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about a specification.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | Unique name of the specification. |
| description | string | None | None | Description of the specification. |
| type | string | None | None | Guest operating system for this specification (Linux or Windows). |
| changeVersion | string | true | None | The changeVersion is a unique identifier for a given version    of the configuration. Each change to the configuration will    update this value. This is typically implemented as an ever    increasing count or a time-stamp. However, a client should    always treat this as an opaque string.    <p>    If specified when updating a specification, the changes will only be    applied if the current changeVersion matches the specified changeVersion. This    field can be used to guard against updates that has happened    between the configInfo was read and until it is applied. |
| lastUpdateTime | datetime | true | None | Time when the specification was last modified. This time is ignored when  the CustomizationSpecItem containing this is used as an input to  CustomizationSpecManager.create. |


