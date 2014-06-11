vim.vApp.ProductInfo
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Information that describes what product a vApp contains, for example,   the software that is installed in the contained virtual machines.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | int | None | None | A unique key for the product section |
| classId | string | true | None | Class name for this attribute.  <p>  Valid values for classId:  Any string except any white-space characters. |
| instanceId | string | true | None | Class name for this attribute.  <p>  Valid values for instanceId:  Any string except any white-space characters. |
| name | string | true | None | Name of the product. |
| vendor | string | true | None | Vendor of the product. |
| version | string | true | None | Short version of the product, for example, 1.0. |
| fullVersion | string | true | None | Full-version of the product, for example, 1.0-build 12323. |
| vendorUrl | string | true | None | URL to vendor homepage. |
| productUrl | string | true | None | URL to product homepage. |
| appUrl | string | true | None | URL to entry-point for application. This is often specified using   a macro, for example, http://${app.ip}/, where app.ip is a defined property   on the virtual machine or vApp container. |


