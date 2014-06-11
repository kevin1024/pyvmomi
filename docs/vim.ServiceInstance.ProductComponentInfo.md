vim.ServiceInstance.ProductComponentInfo
========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


ProductComponentInfo data object type describes installed components.  Product component is defined as a software module that is released  and versioned independently but has dependency relationship with other products.  If one product, for usability or any other reason, bundles other products,  ProductComponentInfo type may be used to describe installed components.  For example, ESX product may bundle VI Client in its releases.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | Opaque identifier that is unique for this product component |
| name | string | None | None | Canonical name of product component |
| version | string | None | None | Version of product component |
| release | int | None | None | Release property is a number which increments with each  new release of product. Product release may not rev version  but release number is always incremented. |


