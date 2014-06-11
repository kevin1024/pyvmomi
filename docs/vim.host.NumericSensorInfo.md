vim.host.NumericSensorInfo
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Base class for numeric sensor information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The name of the physical element associated with the sensor |
| healthState | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | true | None | The health state of the of the element indicated by the sensor.    This property is populated only for sensors that support threshold    settings.<br>See <a href="vim.host.NumericSensorInfo.HealthState.md">HostNumericSensorHealthState</a><br> |
| currentReading | long | None | None | The current reading of the element indicated by the sensor. The actual   sensor reading is obtained by multiplying the current reading by the   scale factor. |
| unitModifier | int | None | None | The unit multiplier for the values returned by the sensor. All values   returned by the sensor are current reading * 10 raised to the power of    the UnitModifier. |
| baseUnits | string | None | None | The base units in which the sensor reading is specified. If rateUnits                 is set the units of the current reading is further qualified by the                   rateUnits.<br>See <a href="vim.host.NumericSensorInfo.md#rateUnits">rateUnits</a><br> |
| rateUnits | string | true | None | The rate units in which the sensor reading is specified. For example if               the baseUnits is Volts and the rateUnits is per second the value                      returned by the sensor are in Volts/second. |
| sensorType | string | None | None | The type of the sensor. If the sensor type is set to Other the sensor    name can be used to further identify the type of sensor. The sensor   units can also be used to further implicitly determine the type of the    sensor.<br>See <a href="vim.host.NumericSensorInfo.SensorType.md">HostNumericSensorType</a><br> |


