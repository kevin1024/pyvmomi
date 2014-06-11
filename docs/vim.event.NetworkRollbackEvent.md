vim.event.NetworkRollbackEvent
==============================
inherits from [vim.event.Event](docs/vim.event.Event.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


This event records when networking configuration on the host   is rolled back as it disconnects the host from vCenter server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| methodName | string | None | None | Method name which caused the disconnect |
| transactionId | string | None | None | Transaction ID for the method call that caused the disconnect |


