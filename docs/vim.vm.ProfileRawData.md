vim.vm.ProfileRawData
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The extensible data object type encapsulates additional data specific   to Virtual Machine and its devices.   <p>   This data is provided by vSphere Extensions which are integral part   of vSphere.   <p>   The data is not persisted in Virtual Machine configuration file but is   stored and managed by extensions.   <p>   Storage Profile Based Management (SPBM) will be one of the consumers of   this data structure. SPBM will provide detailed information about   Virtual Machine storage requirements.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| extensionKey | string | None | None | vSphere Extension Identifier |
| objectData | string | true | None | Extension-specific additional data to be associated  with Virtual machine and its devices.  <p> |


