vim.profile.host.ProfileManager.ConfigTaskList
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.ProfileManager.ConfigTaskList.md">HostProfileManagerConfigTaskList</a> data object  represents a set of tasks to be performed on a host during host profile application.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| configSpec | [vim.host.ConfigSpec](vim.host.ConfigSpec.md "vim.host.ConfigSpec") | true | None | Set of configuration changes to be applied to the host. |
| taskDescription | [vmodl.LocalizableMessage](vmodl.LocalizableMessage.md "vmodl.LocalizableMessage") | true | None | Description of tasks that will be performed on the host  to carry out HostProfile application. |


