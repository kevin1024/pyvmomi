vim.host.VmfsDatastoreOption.Info
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Base class that describes a VMFS datastore provisioning option.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| layout | [vim.host.DiskPartitionInfo.Layout](vim.host.DiskPartitionInfo.Layout.md "vim.host.DiskPartitionInfo.Layout") | None | None | The partition table layout that the disk will have if this   provisioning option is selected.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter.    Since this property is on a DataObject, an update returned by WaitForUpdatesEx may   contain values for this property when some other property on the DataObject changes.   If this update is a result of a call to WaitForUpdatesEx with a non-empty   version parameter, the value for this property may not be current. |
| partitionFormatChange | bool | true | None | Indicates whether selecting this option will change the partition  format type on the disk.<br>See <a href="vim.host.DiskPartitionInfo.PartitionFormat.md">HostDiskPartitionInfoPartitionFormat</a><br> |


