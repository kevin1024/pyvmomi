vim.host.ConnectSpec
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Specifies the parameters needed to add a single host. This includes   a small set of optional information about the host configuration.    This allows the network and datastore configuration of the host to    be synchronized with the naming conventions of the datacenter, as well    as the configuration of a vim account (the username/password for the   virtual machine files that is created on disk).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostName | string | true | None | The DNS name or IP address of the host. (Required for adding    a host.) |
| port | int | true | None | The port number for the connection. If this is not specified,    the default port number is used. For ESX 2.x hosts this is the authd   port (902 by default). For ESX 3.x and above and VMware Server hosts   this is the https port (443 by default).   If this is a reconnect, the port number is unchanged. |
| sslThumbprint | string | true | None | The thumbprint of the SSL certificate, which the host is   expected to have.  If this value is set and matches the   certificate thumbprint presented by the host, then the host is   authenticated. If this value is not set or does not match the   certificate thumbprint presented by the host, then the host's   certificate is verified by checking whether it was signed by a   recognized CA.   <p>   The thumbprint is always computed using the SHA1 hash and is   the string representation of that hash in the format:   xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx   where, 'x' represents a hexadecimal digit |
| userName | string | true | None | The administration account on the host. (Required for adding    a host.) |
| password | string | true | None | The password for the administration account. (Required for adding    a host.) |
| vmFolder | [vim.Folder](vim.Folder.md "vim.Folder") | true | None | The folder in which to store the existing virtual machines on the host.   If this folder is not specified, a default folder is chosen    (and possibly created) by the VirtualCenter.  This folder exists (or   is possibly created) on the   VirtualCenter server and is called "Discovered VM". |
| force | bool | None | None | If this flag is set to "true", then the connection succeeds even    if the host is already being managed by another VirtualCenter server.    The original VirtualCenter server loses connection to the host. |
| vimAccountName | string | true | None | The username to be used for accessing the virtual   machine files on the disk. |
| vimAccountPassword | string | true | None | The password to be used  with the    <a href="vim.host.ConnectSpec.md#vimAccountName">vimAccountName</a>    property for accessing the virtual   machine files on the disk. |
| managementIp | string | true | None | The IP address of the VirtualCenter server that will manage this host.   This field can be used to control which IP address the VirtualCenter agent   will send heartbeats to. If it is not set, VirtualCenter will use the local IP   address used when communicating with the host. Setting this field is useful   when the VirtualCenter server is behind a NAT in which case the external NAT    address must be used. |


