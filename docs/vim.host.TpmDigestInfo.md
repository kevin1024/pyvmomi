vim.host.TpmDigestInfo
======================
inherits from [vim.host.DigestInfo](docs/vim.host.DigestInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type describes the digest values in the Platform   Configuration Register (PCR) of a Trusted Platform Module (TPM) device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| pcrNumber | int | None | None | Index of the PCR that stores the TPM digest value. |


