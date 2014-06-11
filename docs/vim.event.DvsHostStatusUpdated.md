vim.event.DvsHostStatusUpdated
==============================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


A host has it's status or statusDetail updated.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostMember | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The host. |
| oldStatus | string | true | None | Host's old status. |
| newStatus | string | true | None | Host's new status. |
| oldStatusDetail | string | true | None | Comments regarding host's old status. |
| newStatusDetail | string | true | None | Comments regarding host's new status. |


