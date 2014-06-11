vim.vm.customization.CustomNameGenerator
========================================
inherits from [vim.vm.customization.NameGenerator](docs/vim.vm.customization.NameGenerator.md)


Specifies that the VirtualCenter server will launch an external application to   generate the (hostname/IP). The command line for this application must be specified   in the server configuration file (vpxd.cfg) in the vpxd/name-ip-generator key.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| argument | string | true | None | An optional argument that is passed to the utility for this IP address. The   meaning of this field is user-defined in the script. |


