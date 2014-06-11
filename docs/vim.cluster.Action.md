vim.cluster.Action
==================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Base class for all action recommendations in VirtualCenter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| type | string | None | None | Type of the action. This is encoded to differentiate between  different types of actions aimed at achieving different goals. |
| target | vim.ExtensibleManagedObject | true | None | The target object on which this action will be applied. For  instance, a migration action will have a virtual machine as its  target object, while a host power action will have a host as its  target action. |


