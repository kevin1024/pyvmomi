vim.HbrManager.ReplicationVmInfo.ProgressInfo
=============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


A set of statistics related to the progress of the current  operation (full sync or lwd).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| progress | int | None | None | An estimation of the operation progress as a percentage completed,  from 0 to 100. |
| bytesTransferred | long | None | None | Number of bytes transferred so far.  <p>  For sync operations, this value includes (i.e. counts multiple  times) areas that were transferred multiple times (due to stopping  and continuing the operation, or for some errors). |
| bytesToTransfer | long | None | None | The total number of bytes to be transferred.  <p>  For lwd operations, this is the total size of the disk images that  are transferring. This is known from the start and will not change  during a lwd operation.  <p>  For sync operations, this is the total size of the blocks that have  been found not to match between the primary and secondary (by  comparing checksums). It starts from 0 and grows as the checksum  operations advance. The value includes (i.e. counts multiple times)  areas that will end up being transferred more than once (due to  stopping and continuing the operation, or for some errors). |
| checksumTotalBytes | long | true | None | The total number of bytes to be checksummed, only present for sync  tasks. This is the total size of all disks. |
| checksumComparedBytes | long | true | None | The total number of bytes that were checksummed, only present for  sync tasks. |


