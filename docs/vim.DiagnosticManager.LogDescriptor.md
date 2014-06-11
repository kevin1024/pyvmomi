vim.DiagnosticManager.LogDescriptor
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Describes a log file that is available on a server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | A key to identify the log file for browsing and download operations. |
| fileName | string | None | None | The filename of the log. |
| creator | string | None | None | The application that generated the log file. For more information on currently   supported creators, see <a href="vim.DiagnosticManager.LogDescriptor.Creator.md">DiagnosticManagerLogCreator</a>. |
| format | string | None | None | Describes the format of the log file. For more information on currently    supported formats, see <a href="vim.DiagnosticManager.LogDescriptor.Format.md">DiagnosticManagerLogFormat</a>. |
| mimeType | string | None | None | Describes the mime-type of the returned file. Typical   mime-types include:   <ul>   <li>text/plain - for a plain log file</li>   </ul> |
| info | [vim.Description](vim.Description.md "vim.Description") | None | None | Localized description of log file. |


