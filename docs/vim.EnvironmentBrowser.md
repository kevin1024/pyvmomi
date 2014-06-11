vim.EnvironmentBrowser
======================


This managed object type provides access to the environment that a   ComputeResource presents for creating and configuring a virtual machine.   <p>   The environment consists of three main components:   <ul>   <li>The virtual machine configuration options. Each vim.vm.ConfigOption       describes the execution environment for a virtual machine, the particular        set of virtual hardware that is supported. A       ComputeResource might support multiple sets. Access is provided        through the configOptionDescriptor property and the        <a href="vim.EnvironmentBrowser.md#queryConfigOption">QueryConfigOption</a> operation.   <li>The supported device targets. Each virtual device specified in the virtual       machine needs to be hooked up to a "physical" counterpart. For networks,        this means choosing a network name; for a virtual CD-rom this might be        an ISO image, etc.  The environment browser provides access to the device        targets through the        <a href="vim.EnvironmentBrowser.md#queryConfigTarget">QueryConfigTarget</a> operation.   <li>Storage locations and files. A selection of locations where the virtual machine       files can be stored, and the possibility to browse for existing virtual disks       and ISO images. The datastore browser, provided by the datastoreBrowser        property, provides access to the contents of one or more datastores. The        items in a datastore are files that contain configuration, virtual disk, and        the other data associated with a virtual machine.   <li>The capabilities supported by the ComputeResource to which the virtual       machine belongs.    </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='datastoreBrowser'>datastoreBrowser</a> | [vim.host.DatastoreBrowser](vim.host.DatastoreBrowser.md "vim.host.DatastoreBrowser") | true | System.View | DatastoreBrowser to browse datastores that are available on this entity. |


QueryConfigOptionDescriptor()
-----------------------------

| service name | QueryConfigOptionDescriptor |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryConfigOption([key](#string "string"), [host](vim.HostSystem.md "vim.HostSystem"))
--------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryConfigOption |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if any of the following is true:   <ul>   <li>An invalid key is passed.   <li>An invalid host is passed.   <li>A key or host is specified, when the command is invoked from the environment        browser of a virtual machine.   </ul> |




QueryConfigTarget([host](vim.HostSystem.md "vim.HostSystem"))
-------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryConfigTarget |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if an invalid host is specified , or a host is given when           the EnvironmentBrowser is from a virtual machine. |




QueryTargetCapabilities([host](vim.HostSystem.md "vim.HostSystem"))
-------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryTargetCapabilities |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if an invalid host is specified , or a host is given when           the EnvironmentBrowser is from a virtual machine. |




