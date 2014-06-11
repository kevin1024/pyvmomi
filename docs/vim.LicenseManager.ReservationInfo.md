vim.LicenseManager.ReservationInfo
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A reservation describes how many licenses of a particular feature are being used   by a particular feature.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Key of the License Feature.   <p><br>See <a href="vim.LicenseManager.FeatureInfo.md#key">key</a><br> |
| state | [vim.LicenseManager.ReservationInfo.State](vim.LicenseManager.ReservationInfo.State.md "vim.LicenseManager.ReservationInfo.State") | None | None | Describes the reservation state of a license. |
| required | int | None | None | Contains the required number of licenses of the particular type that the   product needs in its current configuration.   <p>   Licenses are normally allocated at the same time as they are needed, so the   value of required is set at the time the license is needed. For example,   in the case of the number of licenses based on virtual machines, the required   count is set at the time a virtual machine is powered on, just before the   license is checked out. |


