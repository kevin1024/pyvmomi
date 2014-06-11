vim.OvfConsumer.OvfSection
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


A self-contained OVF section

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| lineNumber | int | None | None | The line number in the OVF descriptor on which this section starts.  <p>  The line number is only present on sections that were imported as part of an OVF  descriptor (as opposed to sections that are about to be exported to OVF).  <p>  The value is zero if the section did not originate from an OVF descriptor. |
| xml | string | None | None | The XML fragment for the section.  <p>  The XML fragment must explicitly define all namespaces and namespace prefixes  that are used in the fragment, including the default namespace. |


