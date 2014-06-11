vim.Extension.OvfConsumerInfo
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This data object contains configuration for extensions that also extend the OVF  functionality of vCenter server.  <p>  <b>Note:</b> This feature is for internal use only.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| callbackUrl | string | None | None | Callback url for the OVF consumer. This URL must point to a SOAP API  implementing the OVF consumer interface.  <p>  Example: https://extension-host:8081/  </p>  <p>  This callback is for internal use only. |
| sectionType | string | None | None | A list of fully qualified OVF section types that this consumer handles.   <p>  Fully qualified means that each section type must be prefixed with its namespace  enclosed in curly braces. See the examples below.   <p>  An InvalidArgument error is thrown if there is overlap between OVF consumers,  meaning that the same section type appears in the sectionType list of more than  one OVF consumer.  <p>  Example: [ "{http://www.vmware.com/schema/vServiceManager}vServiceDependency",             "{http://www.vmware.com/schema/vServiceManager}vServiceBinding" ] |


