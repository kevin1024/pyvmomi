vim.vApp.OvfSectionInfo
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The OvfSection encapsulates uninterpreted meta-data sections in   an OVF descriptor. When an OVF package is imported, non-required /    non-interpreted sections will be stored as OvfSection object. During    the creation of an OVF package, these sections will be placed in the    OVF descriptor.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | int | true | None | A unique key to identify a section. |
| namespace | string | true | None | The namespace for the value in xsi:type attribute. |
| type | string | true | None | The value of the xsi:type attribute not including the namespace prefix. |
| atEnvelopeLevel | bool | true | None | Whether this is a global envelope section |
| contents | string | true | None | The XML fragment including the top-level &lt;Section...&gt; element. The   fragment is self-contained will all required namespace definitions. |


