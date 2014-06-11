vim.host.TpmSoftwareComponentEventDetails
=========================================
inherits from [vim.host.TpmEventDetails](docs/vim.host.TpmEventDetails.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Details of a Trusted Platform Module (TPM) event recording a software component   related event.   <p />   This event is created when measuring a software component installed on the system.   A software component may be a tardisk, a kernel module or any other type supported   by the package system.   <p />   Some software components are not packaged as VIBs (currently the package database   and persistent state information of ESXi). For these components the VIB fields   will contain empty strings.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| componentName | string | None | None | Name of the software component that caused this TPM event. |
| vibName | string | None | None | Name of the VIB containing the software component. |
| vibVersion | string | None | None | Version of the VIB containing the software component. |
| vibVendor | string | None | None | Vendor of the VIB containing the software component. |


