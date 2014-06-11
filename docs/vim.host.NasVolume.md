vim.host.NasVolume
==================
inherits from [vim.host.FileSystemVolume](docs/vim.host.FileSystemVolume.md)


This data object type describes the NAS volume.  Applies to both   NFS and CIFS.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| remoteHost | string | None | None | The host that runs the NFS/CIFS server.   Clients must plan to use remoteHostNames for both NFS v3   as well as NFS v4.1 because this field remoteHost may be   deprecated in future. |
| remotePath | string | None | None | The remote path of NFS/CIFS mount point. |
| userName | string | true | None | In case of CIFS, the user name used while connecting to the server. |


