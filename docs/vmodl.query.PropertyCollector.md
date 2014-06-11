vmodl.query.PropertyCollector
=============================


The <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> managed object retrieves and detects changes   to the properties of other managed objects. The <a href="vmodl.query.PropertyCollector.md#retrievePropertiesEx">RetrievePropertiesEx</a> method provides one-time property retrieval. The   <a href="vmodl.query.PropertyCollector.md#waitForUpdatesEx">WaitForUpdatesEx</a> method provides incremental change detection and   supports both polling and notification.    <p> For change detection a client creates one or more filters to specify the   subset of managed objects in which the client is interested. Filters keep   per-session state to track incremental changes. Because this state is   per-session: <ul>    <li> A session cannot share its <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> filters with other        sessions    <li> two different clients can share the same session, and so can        share the same filters, but this is not recommended    <li> When a session terminates, the associated <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> filters        are automatically destroyed.    </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='filter'>filter</a> | [vmodl.query.PropertyCollector.Filter](vmodl.query.PropertyCollector.Filter.md "vmodl.query.PropertyCollector.Filter") | true | System.View | The filters that this <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> uses to determine the list of   properties for which it detects incremental changes. |


CreateFilter([spec](vmodl.query.PropertyCollector.FilterSpec.md "vmodl.query.PropertyCollector.FilterSpec"))
------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidType](vmodl.fault.InvalidType.md "vmodl.fault.InvalidType"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound"), [vmodl.query.InvalidProperty](vmodl.query.InvalidProperty.md "vmodl.query.InvalidProperty")

---
| service name | CreateFilter |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.query.InvalidProperty](vmodl.query.InvalidProperty.md "vmodl.query.InvalidProperty") | if "spec" has a property that is not defined on one of the objects. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if any of the following is true:      <ul>      <li>"spec" is empty.      <li>"spec" contains a selection with properties not defined on its          type.      </ul> |
| [vmodl.fault.InvalidType](vmodl.fault.InvalidType.md "vmodl.fault.InvalidType") | if "spec" contains, directly or indirectly, a type name that      does not refer to a known type. |
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | See <a href="vmodl.query.PropertyCollector.FilterSpec.md#reportMissingObjectsInResults">reportMissingObjectsInResults</a>. |




RetrieveProperties([specSet](vmodl.query.PropertyCollector.FilterSpec.md "vmodl.query.PropertyCollector.FilterSpec"))
---------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidType](vmodl.fault.InvalidType.md "vmodl.fault.InvalidType"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound"), [vmodl.query.InvalidProperty](vmodl.query.InvalidProperty.md "vmodl.query.InvalidProperty")

---
### Deprecated
As of vSphere API 4.1, use <a href="vmodl.query.PropertyCollector.md#retrievePropertiesEx">RetrievePropertiesEx</a>.

| service name | RetrieveProperties |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.query.InvalidProperty](vmodl.query.InvalidProperty.md "vmodl.query.InvalidProperty") | See <a href="vmodl.query.PropertyCollector.md#createFilter">CreateFilter</a> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | See <a href="vmodl.query.PropertyCollector.md#createFilter">CreateFilter</a> |
| [vmodl.fault.InvalidType](vmodl.fault.InvalidType.md "vmodl.fault.InvalidType") | See <a href="vmodl.query.PropertyCollector.md#createFilter">CreateFilter</a> |
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | See <a href="vmodl.query.PropertyCollector.md#createFilter">CreateFilter</a> |




CheckForUpdates([version](#string "string"))
--------------------------------------------
 raises [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled"), [vmodl.query.InvalidCollectorVersion](vmodl.query.InvalidCollectorVersion.md "vmodl.query.InvalidCollectorVersion")

---
### Deprecated
As of vSphere API 4.1, use   <a href="vmodl.query.PropertyCollector.md#waitForUpdatesEx">WaitForUpdatesEx</a> with a   <a href="vmodl.query.PropertyCollector.WaitOptions.md#maxWaitSeconds">maxWaitSeconds</a> of 0.

| service name | CheckForUpdates |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.query.InvalidCollectorVersion](vmodl.query.InvalidCollectorVersion.md "vmodl.query.InvalidCollectorVersion") | if the data version does not meet the      requirements above. |
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | if <a href="vmodl.query.PropertyCollector.md#cancelWaitForUpdates">CancelWaitForUpdates</a> has been called or the session was closed      or the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> was destroyed at some point after the call was      received but before the update calculation was actually started |




WaitForUpdates([version](#string "string"))
-------------------------------------------
 raises [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled"), [vmodl.query.InvalidCollectorVersion](vmodl.query.InvalidCollectorVersion.md "vmodl.query.InvalidCollectorVersion")

---
### Deprecated
As of vSphere API 4.1, use <a href="vmodl.query.PropertyCollector.md#waitForUpdatesEx">WaitForUpdatesEx</a>.

| service name | WaitForUpdates |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.query.InvalidCollectorVersion](vmodl.query.InvalidCollectorVersion.md "vmodl.query.InvalidCollectorVersion") | if the data version does not meet the      requirements above. |
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | if <a href="vmodl.query.PropertyCollector.md#cancelWaitForUpdates">CancelWaitForUpdates</a> has been called or the session was closed      or the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> was destroyed at some point after the call was      received |




CancelWaitForUpdates()
----------------------

| service name | CancelWaitForUpdates |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




WaitForUpdatesEx([version](#string "string"), [options](vmodl.query.PropertyCollector.WaitOptions.md "vmodl.query.PropertyCollector.WaitOptions"))
--------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled"), [vmodl.query.InvalidCollectorVersion](vmodl.query.InvalidCollectorVersion.md "vmodl.query.InvalidCollectorVersion")

---
| service name | WaitForUpdatesEx |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.query.InvalidCollectorVersion](vmodl.query.InvalidCollectorVersion.md "vmodl.query.InvalidCollectorVersion") | if the data version does not meet the      requirements above. |
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | if <a href="vmodl.query.PropertyCollector.md#cancelWaitForUpdates">CancelWaitForUpdates</a> has been called or the session was closed      or the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> was destroyed at some point after the call was      received |




RetrievePropertiesEx([specSet](vmodl.query.PropertyCollector.FilterSpec.md "vmodl.query.PropertyCollector.FilterSpec"), [options](vmodl.query.PropertyCollector.RetrieveOptions.md "vmodl.query.PropertyCollector.RetrieveOptions"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidType](vmodl.fault.InvalidType.md "vmodl.fault.InvalidType"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound"), [vmodl.query.InvalidProperty](vmodl.query.InvalidProperty.md "vmodl.query.InvalidProperty")

---
| service name | RetrievePropertiesEx |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.query.InvalidProperty](vmodl.query.InvalidProperty.md "vmodl.query.InvalidProperty") | See <a href="vmodl.query.PropertyCollector.md#createFilter">CreateFilter</a> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if any of the following is true:      See <a href="vmodl.query.PropertyCollector.md#createFilter">CreateFilter</a> |
| [vmodl.fault.InvalidType](vmodl.fault.InvalidType.md "vmodl.fault.InvalidType") | See <a href="vmodl.query.PropertyCollector.md#createFilter">CreateFilter</a> |
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | See <a href="vmodl.query.PropertyCollector.md#createFilter">CreateFilter</a> |




ContinueRetrievePropertiesEx([token](#string "string"))
-------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.query.InvalidProperty](vmodl.query.InvalidProperty.md "vmodl.query.InvalidProperty")

---
| service name | ContinueRetrievePropertiesEx |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.query.InvalidProperty](vmodl.query.InvalidProperty.md "vmodl.query.InvalidProperty") | vmodl.query.InvalidProperty |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the token does not match the token from the      previous <a href="vmodl.query.PropertyCollector.RetrieveResult.md">RetrieveResult</a> returned on the same      session by the same <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>. |




CancelRetrievePropertiesEx([token](#string "string"))
-----------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.query.InvalidProperty](vmodl.query.InvalidProperty.md "vmodl.query.InvalidProperty")

---
| service name | CancelRetrievePropertiesEx |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.query.InvalidProperty](vmodl.query.InvalidProperty.md "vmodl.query.InvalidProperty") | vmodl.query.InvalidProperty |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the token does not match the token from the      previous <a href="vmodl.query.PropertyCollector.RetrieveResult.md">RetrieveResult</a> returned on the same      session by the same <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>. |




CreatePropertyCollector()
-------------------------

| service name | CreatePropertyCollector |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




DestroyPropertyCollector()
--------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | DestroyPropertyCollector |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if this <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> is not allowed to be          destroyed. |




