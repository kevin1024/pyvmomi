vmodl.LocalizedMethodFault
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A wrapper class used to pass MethodFault data objects over the wire   along with a localized display message for the fault.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| fault | [vmodl.MethodFault](vmodl.MethodFault.md "vmodl.MethodFault") | None | None |  |
| localizedMessage | string | true | None | The localized message that would be sent in the faultstring element  of the SOAP Fault.  It is optional so that clients are not required  to send a localized message to the server, but servers are required  to send the localized message to clients. |


