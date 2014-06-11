vim.host.TpmEventLogEntry
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


This data object represents a single entry of an event log created by   Trusted Platform Module (TPM).   <p />   An TPM event log entry represents a single change to the value of   a Platform Configuration Register (PCR). It contains detailed information   about the reason of PCR value change, and the specifics of the event.   <p />   Multiple objects of this type form an TPM event log. This log allows for   verification of the both the software stack running on a host and the attestation   process itself.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| pcrIndex | int | None | None | Index of the PCR that was affected by the event. |
| eventDetails | [vim.host.TpmEventDetails](vim.host.TpmEventDetails.md "vim.host.TpmEventDetails") | None | None | The details of the event. |


