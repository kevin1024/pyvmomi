vim.ExtensionManager
====================
as of [VI API 2.5](vim.version.md#vim.version.version2)


This managed object type provides directory and basic management   services for all registered extensions.   <p>   Clients use the ExtensionManager, available in   <a href="vim.ServiceInstance.md">ServiceInstance</a>,   to access extension objects.   <p>   While several authentication methods are available for extension   servers to use (see <a href="vim.SessionManager.md">SessionManager</a>), only one   authentication method is valid for an extension at any given   time.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='extensionList'>extensionList</a> | [vim.Extension](vim.Extension.md "vim.Extension") | true | System.View | The list of currently registered extensions. |


UnregisterExtension([extensionKey](#string "string"))
-----------------------------------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UnregisterExtension |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Extension.Unregister |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the specified extension      is not registered. |




FindExtension([extensionKey](#string "string"))
-----------------------------------------------

| service name | FindExtension |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




RegisterExtension([extension](vim.Extension.md "vim.Extension"))
----------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | RegisterExtension |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Extension.Register |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the Extension description is incomplete or an extension      is already registered with the given unique key, or if the extension is an OVF      extension and its section types overlap with other registered OVF extensions. |




UpdateExtension([extension](vim.Extension.md "vim.Extension"))
--------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateExtension |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Extension.Update |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the specified extension key is not registered. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the Extension description is incomplete or invalid, or      if the extension is an OVF extension and its section types overlap with other      registered OVF extensions. |




GetPublicKey()
--------------

### Deprecated
As of VI 4.0, use trusted certificates and      <a href="vim.SessionManager.md#loginExtensionBySubjectName">LoginExtensionBySubjectName</a> or      <a href="vim.ExtensionManager.md#setCertificate">SetExtensionCertificate</a> and      <a href="vim.SessionManager.md#loginExtensionByCertificate">LoginExtensionByCertificate</a>.

| service name | GetPublicKey |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




SetPublicKey([extensionKey](#string "string"), [publicKey](#string "string"))
-----------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
### Deprecated
As of VI 4.0, use trusted certificates and      <a href="vim.SessionManager.md#loginExtensionBySubjectName">LoginExtensionBySubjectName</a> or      <a href="vim.ExtensionManager.md#setCertificate">SetExtensionCertificate</a> and      <a href="vim.SessionManager.md#loginExtensionByCertificate">LoginExtensionByCertificate</a>.

| service name | SetPublicKey |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Extension.Update |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the public key is invalid. |




SetExtensionCertificate([extensionKey](#string "string"), [certificatePem](#string "string"))
---------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NoClientCertificate](vim.fault.NoClientCertificate.md "vim.fault.NoClientCertificate"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | SetExtensionCertificate |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#vim.version.version2) |
| privilege    | Extension.Update |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if an extension specified by &quot;extensionKey&quot;                    is not registered. |
| [vim.fault.NoClientCertificate](vim.fault.NoClientCertificate.md "vim.fault.NoClientCertificate") | if certificatePem is not specified, and                               no certificate was passed over SSL handshake. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the certificate described by                           &quot;certificatePem&quot; is not in PEM                           format, or could not be decoded to an X.509 certificate. |




QueryManagedBy([extensionKey](#string "string"))
------------------------------------------------

| service name | QueryManagedBy |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryExtensionIpAllocationUsage([extensionKeys](#string "string"))
------------------------------------------------------------------

| service name | QueryExtensionIpAllocationUsage |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




