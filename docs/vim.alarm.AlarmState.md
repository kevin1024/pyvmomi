vim.alarm.AlarmState
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about the alarm's state.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Unique key that identifies the alarm. |
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | None | Entity on which the alarm is instantiated. |
| alarm | [vim.alarm.Alarm](vim.alarm.Alarm.md "vim.alarm.Alarm") | None | None | Alarm object from which the AlarmState object is instantiated. |
| overallStatus | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | None | None | Overall status of the alarm object.   This is the value of the alarm's top-level expression.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter.    Since this property is on a DataObject, an update returned by WaitForUpdatesEx may   contain values for this property when some other property on the DataObject changes.   If this update is a result of a call to WaitForUpdatesEx with a non-empty   version parameter, the value for this property may not be current. |
| time | datetime | None | None | Time the alarm triggered. |
| acknowledged | bool | true | None | Flag to indicate if the alarm's actions have been acknowledged for the   associated ManagedEntity. |
| acknowledgedByUser | string | true | None | The user who acknowledged this triggering.  If the triggering has not   been acknowledged, then the value is not valid. |
| acknowledgedTime | datetime | true | None | The time this triggering was acknowledged.  If the triggering has not   been acknowledged, then the value is not valid. |


