vim.host.FileAccess.Modes
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The FileAccess.Modes data object type defines the known access modes   for a datastore. The property values specify how to interpret   the "what" property for a FileAccess object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| browse | string | true | None | Can see the existence of a file. |
| read | string | None | None | Can read a file. |
| modify | string | None | None | Can read and write a file. |
| use | string | None | None | Can execute or operate a file or look inside a directory. |
| admin | string | true | None | Can change permissions for a file. |
| full | string | None | None | Can do anything to a file, including change permissions. |


