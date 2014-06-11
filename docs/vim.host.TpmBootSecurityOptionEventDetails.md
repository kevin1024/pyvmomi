vim.host.TpmBootSecurityOptionEventDetails
==========================================
inherits from [vim.host.TpmEventDetails](docs/vim.host.TpmEventDetails.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Details of a Trusted Platform Module (TPM) event recording kernel security   option passed at boot time and currently in effect.   <p />   This event type exists to simplify parsing of the security-related information   by internal and third-party solutions. Each boot option may be passed to kernel   multiple times and/or in different forms. Replicating the parsing logic of the   kernel would be neither convinient, nor secure for the client applications.   <p />   Each instance of this event reports details of a single security-related   boot option, as set in the kernel.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| bootSecurityOption | string | None | None | Security-related options string, reflecting the state of an option set   in the kernel.   <p />   This string is in the form of a KEY=VALUE pair. |


