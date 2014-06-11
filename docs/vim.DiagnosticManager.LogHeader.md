vim.DiagnosticManager.LogHeader
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A header that is returned with a set of log entries. This header   describes where entries are located in the log file. Log files typically   grow dynamically, so indexes based on line numbers may become inaccurate.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| lineStart | int | None | None | The first line of this log segment. |
| lineEnd | int | None | None | The last line of this log segment. |
| lineText | string | true | None | Log entries, listed by line, for this log segment. |


