vim.LicenseManager.DiagnosticInfo
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type provides summary status and diagnostic information for   <a href="vim.LicenseManager.md">LicenseManager</a>. Counters in this property can be reset to zero. The   property specified as a discontinuity is used to determine when this last   occurred.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sourceLastChanged | datetime | None | None | A timestamp of when sourceAvailable last changed state, expressed in UTC. |
| sourceLost | string | None | None | Counter to track number of times connection to source was lost.   This value starts at zero and wraps at 2^32-1 to zero.   Discontinuity: sourceLastChanged. |
| sourceLatency | float | None | None | Exponentially decaying average of the transaction time for license   acquisition and routine communications with LicenseSource.   Units: milliseconds. |
| licenseRequests | string | None | None | Counter to track total number of licenses requested.   This value starts at zero and wraps at 2^32-1 to zero.   Discontinuity: sourceLastChanged. |
| licenseRequestFailures | string | None | None | Counter to track Total number of licenses requests that were   not fulfilled (denied, timeout, or other).   This value starts at zero and wraps at 2^32-1 to zero.   Discontinuity: sourceLastChanged. |
| licenseFeatureUnknowns | string | None | None | Counter to track Total number of license features parsed from   License source that are not recognized.   This value starts at zero and wraps at 2^32-1 to zero.   Discontinuity: sourceLastChanged. |
| opState | [vim.LicenseManager.LicenseState](vim.LicenseManager.LicenseState.md "vim.LicenseManager.LicenseState") | None | None | The general state of the license subsystem. |
| lastStatusUpdate | datetime | None | None | A timestamp of when opState was last updated. |
| opFailureMessage | string | None | None | A human readable reason when optState reports Fault condition. |


