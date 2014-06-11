vim.host.DiagnosticPartition.CreateDescription
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The diagnostic partition create description details what will be done   to create a new diagnostic partition on a disk.  It contains a CreateSpec   that can be submitted to create the partition and information that can   be shown to the user.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| layout | [vim.host.DiskPartitionInfo.Layout](vim.host.DiskPartitionInfo.Layout.md "vim.host.DiskPartitionInfo.Layout") | None | None | Layout describing the format of the disk    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter.    Since this property is on a DataObject, an update returned by WaitForUpdatesEx may   contain values for this property when some other property on the DataObject changes.   If this update is a result of a call to WaitForUpdatesEx with a non-empty   version parameter, the value for this property may not be current. |
| diskUuid | string | None | None | The UUID of the SCSI disk on which to create the diagnostic partition.   This disk UUID will match that found in the identification field of the   creation spec.<br>See <a href="vim.host.ScsiDisk.md">HostScsiDisk</a><br>See <a href="vim.host.ScsiLun.md#uuid">uuid</a><br> |
| spec | [vim.host.DiagnosticPartition.CreateSpec](vim.host.DiagnosticPartition.CreateSpec.md "vim.host.DiagnosticPartition.CreateSpec") | None | None | Creation specification for diagnostic partition |


