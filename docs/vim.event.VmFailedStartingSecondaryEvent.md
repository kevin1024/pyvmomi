vim.event.VmFailedStartingSecondaryEvent
========================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records vmotion failure when starting a secondary VM.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | string | true | None | The reason for the failure.   See <a href="vim.event.VmFailedStartingSecondaryEvent.FailureReason.md">VmFailedStartingSecondaryEventFailureReason</a> |


