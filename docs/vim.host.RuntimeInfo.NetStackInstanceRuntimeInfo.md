vim.host.RuntimeInfo.NetStackInstanceRuntimeInfo
================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This data type describes network stack instance runtime info

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| netStackInstanceKey | string | None | None | Key of the instance |
| state | string | true | None | State of the instance   See State for valid values. |
| vmknicKeys | string | true | None | The keys of vmknics that are using this stack |
| maxNumberOfConnections | int | true | None | The maximum number of socket connections can be worked on this   instance currently after booting up. |
| currentIpV6Enabled | bool | true | None | If true then dual IPv4/IPv6 stack enabled else IPv4 only. |


