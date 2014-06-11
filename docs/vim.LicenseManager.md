vim.LicenseManager
==================


This managed object type controls entitlements for a given VMware   platform. VMware platforms include VirtualCenter, ESX Server, VMware Server,   Workstation and Player. Entitlements define what software capabilities   this host may use.   <p>   Entitlements are identified by a short string 'key'. Keys can represent either   a particular edition (Full, Starter) or a particular feature/function (featureKey)   (backup, nas). An edition implies zero one or more functions which are express,   denied or optional. For example a 'Full' edition includes 'iscsi' function but a   Starter edition might disallow it.   <p>   Which edition a given VMware platform uses can be defined at any time. Generally this   is done right after first install and boot as installation software may not set it.   For editions that are similar in nature, any future changes to edition   type will only impact future requests for functionality.   Current functionality is left unaffected. The same is true for optional   functions enabled/disabled after some period of time. For dissimilar editions,   such transitions may require entering maintenance mode first else an exception of   InvalidState will be thrown.   <p>   To specify the edition type and any optional functions, use updateLicense for   ESX Server and addLicense follow by LicenseAssingmentManager.updateAssignedLicense   for VirtualCenter.    <p>                  When an edition is specified for a given host, the cost of that edition   (how many licenses are needed) is determined. The cost is computed   using the license's CostUnit value multiplied by the number of units activated.   For example, when a VMware platform is set to an edition which uses a 'cpuPackage'   on a two socket server, two licenses would be needed to successfully   install that edition.   <p>                  Here is a diagram of the unit costs supported by this API and their relationships.   <pre>                 +------------------------------+   +--------+      +-------+    | +-----------+ +-----------+  |   | Server |      |  Host |    | |           | |           |  |   +--------+      +-------+    | |  cpuCore  | |   cpuCore |  |                   +-------+    | +-----------+ +-----------+  |   +--------+      |  Host |    |                  cpuPackage  |   |  VM    |      +-------+    +------------------------------+   +--------+   </pre>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='source'>source</a> | [vim.LicenseManager.LicenseSource](vim.LicenseManager.LicenseSource.md "vim.LicenseManager.LicenseSource") | None | None | Set or return a data object type of LocalLicense or LicenseServer. |
| <a href='sourceAvailable'>sourceAvailable</a> | bool | None | None | Current state of the license source. License sources that are LocalSource   are always available. |
| <a href='diagnostics'>diagnostics</a> | [vim.LicenseManager.DiagnosticInfo](vim.LicenseManager.DiagnosticInfo.md "vim.LicenseManager.DiagnosticInfo") | true | None | Return current diagnostic information. |
| <a href='featureInfo'>featureInfo</a> | [vim.LicenseManager.FeatureInfo](vim.LicenseManager.FeatureInfo.md "vim.LicenseManager.FeatureInfo") | true | None | The list of features that can be licensed. |
| <a href='licensedEdition'>licensedEdition</a> | string | None | None | The product's license edition. The edition defines which product license   the server requires. This, in turn, determines the core set of functionalities   provided by the product and the additional features that can be licensed. If    no edition is set the property is set to the empty string ("").    To set the edition use <a href="vim.LicenseManager.md#setEdition">SetLicenseEdition</a>. |
| <a href='licenses'>licenses</a> | [vim.LicenseManager.LicenseInfo](vim.LicenseManager.LicenseInfo.md "vim.LicenseManager.LicenseInfo") | None | dynamic | Get information about all the licenses avaiable. |
| <a href='licenseAssignmentManager'>licenseAssignmentManager</a> | [vim.LicenseAssignmentManager](vim.LicenseAssignmentManager.md "vim.LicenseAssignmentManager") | true | System.View | License Assignment Manager |
| <a href='evaluation'>evaluation</a> | [vim.LicenseManager.EvaluationInfo](vim.LicenseManager.EvaluationInfo.md "vim.LicenseManager.EvaluationInfo") | None | System.Read |  |


QuerySupportedFeatures([host](vim.HostSystem.md "vim.HostSystem"))
------------------------------------------------------------------

### Deprecated
As of vSphere API 4.0, use    <a href="vim.LicenseAssignmentManager.md#queryAssignedLicenses">QueryAssignedLicenses</a> instead.

| service name | QuerySupportedFeatures |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryLicenseSourceAvailability([host](vim.HostSystem.md "vim.HostSystem"))
--------------------------------------------------------------------------

### Deprecated
As of vSphere API 4.0, use    <a href="vim.LicenseAssignmentManager.md#queryAssignedLicenses">QueryAssignedLicenses</a> instead.

| service name | QueryLicenseSourceAvailability |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryLicenseUsage([host](vim.HostSystem.md "vim.HostSystem"))
-------------------------------------------------------------

### Deprecated
As of vSphere API 4.0, use    <a href="vim.LicenseAssignmentManager.md#queryAssignedLicenses">QueryAssignedLicenses</a> instead.

| service name | QueryLicenseUsage |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




SetLicenseEdition([host](vim.HostSystem.md "vim.HostSystem"), [featureKey](#string "string"))
---------------------------------------------------------------------------------------------
 raises [vim.fault.LicenseServerUnavailable](vim.fault.LicenseServerUnavailable.md "vim.fault.LicenseServerUnavailable"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
### Deprecated
As of vSphere API 4.0, use    <a href="vim.LicenseAssignmentManager.md#queryAssignedLicenses">QueryAssignedLicenses</a> instead.

| service name | SetLicenseEdition |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If the feature cannot be supported on the platform,           potentially because the hardware configuration does not support it. |
| [vim.fault.LicenseServerUnavailable](vim.fault.LicenseServerUnavailable.md "vim.fault.LicenseServerUnavailable") | If the license server is unavailable. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If a feature key is not an edition feature key. |




CheckLicenseFeature([host](vim.HostSystem.md "vim.HostSystem"), [featureKey](#string "string"))
-----------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
### Deprecated
As of vSphere API 4.0, use    <a href="vim.LicenseAssignmentManager.md#queryAssignedLicenses">QueryAssignedLicenses</a> instead.

| service name | CheckLicenseFeature |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type | [bool](bool.md "bool") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If the feature cannot be supported on the platform,           potentially because the hardware configuration does not support it. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If a feature name is not found. |




EnableFeature([host](vim.HostSystem.md "vim.HostSystem"), [featureKey](#string "string"))
-----------------------------------------------------------------------------------------
 raises [vim.fault.LicenseServerUnavailable](vim.fault.LicenseServerUnavailable.md "vim.fault.LicenseServerUnavailable"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
### Deprecated
As of vSphere API 4.0, use    <a href="vim.LicenseAssignmentManager.md#updateAssignedLicense">UpdateAssignedLicense</a> instead.

| service name | EnableFeature |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type | [bool](bool.md "bool") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If the feature cannot be supported on the platform,           potentially because the hardware configuration does not support it. |
| [vim.fault.LicenseServerUnavailable](vim.fault.LicenseServerUnavailable.md "vim.fault.LicenseServerUnavailable") | If the license server is unavailable. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If a feature name is not found or it is not optional. |




DisableFeature([host](vim.HostSystem.md "vim.HostSystem"), [featureKey](#string "string"))
------------------------------------------------------------------------------------------
 raises [vim.fault.LicenseServerUnavailable](vim.fault.LicenseServerUnavailable.md "vim.fault.LicenseServerUnavailable"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
### Deprecated
As of vSphere API 4.0, use   <a href="vim.LicenseAssignmentManager.md#removeAssignedLicense">RemoveAssignedLicense</a> instead.

| service name | DisableFeature |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type | [bool](bool.md "bool") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If the feature is in use. |
| [vim.fault.LicenseServerUnavailable](vim.fault.LicenseServerUnavailable.md "vim.fault.LicenseServerUnavailable") | If the license server is unavailable. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If a feature name is not found or it is not optional. |




ConfigureLicenseSource([host](vim.HostSystem.md "vim.HostSystem"), [licenseSource](vim.LicenseManager.LicenseSource.md "vim.LicenseManager.LicenseSource"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.LicenseServerUnavailable](vim.fault.LicenseServerUnavailable.md "vim.fault.LicenseServerUnavailable"), [vim.fault.CannotAccessLocalSource](vim.fault.CannotAccessLocalSource.md "vim.fault.CannotAccessLocalSource"), [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses"), [vim.fault.InvalidLicense](vim.fault.InvalidLicense.md "vim.fault.InvalidLicense")

---
### Deprecated
As of vSphere API 4.0, use <a href="vim.LicenseManager.md#updateLicense">UpdateLicense</a>   instead.

| service name | ConfigureLicenseSource |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CannotAccessLocalSource](vim.fault.CannotAccessLocalSource.md "vim.fault.CannotAccessLocalSource") | if the local source cannot be accessed. |
| [vim.fault.InvalidLicense](vim.fault.InvalidLicense.md "vim.fault.InvalidLicense") | if the new license source is LocalLicenseSource and the   license file is not valid. |
| [vim.fault.LicenseServerUnavailable](vim.fault.LicenseServerUnavailable.md "vim.fault.LicenseServerUnavailable") | if the license server is unreachable. |
| [vmodl.fault.NotEnoughLicenses](vmodl.fault.NotEnoughLicenses.md "vmodl.fault.NotEnoughLicenses") | if the new license source does not have enough licenses. |




UpdateLicense([licenseKey](#string "string"), [labels](vim.KeyValue.md "vim.KeyValue"))
---------------------------------------------------------------------------------------

| service name | UpdateLicense |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




AddLicense([licenseKey](#string "string"), [labels](vim.KeyValue.md "vim.KeyValue"))
------------------------------------------------------------------------------------

| service name | AddLicense |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




RemoveLicense([licenseKey](#string "string"))
---------------------------------------------

| service name | RemoveLicense |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




DecodeLicense([licenseKey](#string "string"))
---------------------------------------------

| service name | DecodeLicense |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




UpdateLicenseLabel([licenseKey](#string "string"), [labelKey](#string "string"), [labelValue](#string "string"))
----------------------------------------------------------------------------------------------------------------

| service name | UpdateLicenseLabel |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




RemoveLicenseLabel([licenseKey](#string "string"), [labelKey](#string "string"))
--------------------------------------------------------------------------------

| service name | RemoveLicenseLabel |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




