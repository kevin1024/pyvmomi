vim.host.IscsiManager.IscsiDependencyEntity
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Defines a dependency entity.   Contains the affected Virtual NIC device name and iSCSI HBA name  (if Virtual NIC is associated with the HBA).   See IscsiMigrationDependency

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| pnicDevice | string | None | None | The affected Physical NIC device |
| vnicDevice | string | None | None | The affected Virtual NIC device |
| vmhbaName | string | None | None | The iSCSI HBA that the Virtual NIC is associated with, if any. |


