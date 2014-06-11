vim.vApp.VmConfigSpec
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


vApp related configuration of a VM.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| product | [vim.vApp.ProductSpec](vim.vApp.ProductSpec.md "vim.vApp.ProductSpec") | true | None | Information about the product.  <p>  Reconfigure privilege: VApp.ApplicationConfig |
| property | [vim.vApp.PropertySpec](vim.vApp.PropertySpec.md "vim.vApp.PropertySpec") | true | None | List of properties.  <p>  Adding and editing properties requires various privileges depending on which fields  are affected. See <a href="vim.vApp.PropertyInfo.md">VAppPropertyInfo</a> for details.  <p>  Deleting properties requires the privilege VApp.ApplicationConfig. |
| ipAssignment | [vim.vApp.IPAssignmentInfo](vim.vApp.IPAssignmentInfo.md "vim.vApp.IPAssignmentInfo") | true | None | IP assignment policy and DHCP support configuration.  <p>  Reconfigure privilege: See <a href="vim.vApp.IPAssignmentInfo.md">VAppIPAssignmentInfo</a> |
| eula | string | true | None | End User Liceses Agreements.   <p>  If this list is set, it replaces all exiting  licenses. An empty list will not   make any changes to installed licenses. A list with a single element {""} will   remove all licenses and leave an empty list.  <p>  Reconfigure privilege: VApp.ApplicationConfig |
| ovfSection | [vim.vApp.OvfSectionSpec](vim.vApp.OvfSectionSpec.md "vim.vApp.OvfSectionSpec") | true | None | List of uninterpreted OVF meta-data sections.  <p>  Reconfigure privilege: VApp.ApplicationConfig |
| ovfEnvironmentTransport | string | true | None | List the transports to use for properties. Supported values are: iso and  com.vmware.guestInfo.  <p>  If this list is set, it replaces all exiting entries. An empty list will not make  any changes. A list with a single element {""} will clear the list of transports.  <p>  Reconfigure privilege: VApp.ApplicationConfig |
| installBootRequired | bool | true | None | If this is on a VirtualMachine object, it specifies whether the VM needs an   initial boot before the deployment is complete. If this is on a vApp object,   it indicates than one or more VMs needs an initial reboot. This flag is   automatically reset once the reboot has happened.  <p>  Reconfigure privilege: VApp.ApplicationConfig |
| installBootStopDelay | int | true | None | Specifies the delay in seconds to wait for the VM to power off after the initial  boot (used only if installBootRequired is true). A value of 0 means wait forever.   <p>  Reconfigure privilege: VApp.ApplicationConfig |


