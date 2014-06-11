vim.host.TpmOptionEventDetails
==============================
inherits from [vim.host.TpmEventDetails](docs/vim.host.TpmEventDetails.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Details of a Trusted Platform Module (TPM) event recording boot-time options.   <p />   The boot-time options set on the system are packaged into a file that is supplied   to the kernel at boot time. The boot options may be a string of key=value pairs   (possibly separated by a new line) or a blob of arbitrary data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| optionsFileName | string | None | None | Name of the file containing the boot options. |
| bootOptions | int | true | None | Options set by the boot option package.   <p />   This array exposes the raw contents of the settings file (or files) that were   passed to kernel during the boot up process, and, therefore, should be treated   accordingly. |


