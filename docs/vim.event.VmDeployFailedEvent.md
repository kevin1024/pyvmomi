vim.event.VmDeployFailedEvent
=============================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)


This event records a failure to deploy from a template.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| destDatastore | [vim.event.EntityEventArgument](vim.event.EntityEventArgument.md "vim.event.EntityEventArgument") | None | None | The destination datastore the template is being deployed to. |
| reason | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | The reason for the failure. |


