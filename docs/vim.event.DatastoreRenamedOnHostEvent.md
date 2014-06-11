vim.event.DatastoreRenamedOnHostEvent
=====================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)


This event records when a datastore is added to VirtualCenter   and is renamed by VirtualCenter because this datastore already   exists in VirtualCenter with a different name, or because the   name conflicts with another datastore in VirtualCenter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldName | string | None | None | The old datastore name. |
| newName | string | None | None | The new datastore name. |


