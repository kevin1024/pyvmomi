vmodl.LocalizableMessage
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vmodl.version.version1)


Message data which is intended to be displayed according  to the locale of a client.   <p>A <a href="vmodl.LocalizableMessage.md">LocalizableMessage</a> contains both a formatted, localized  version of the text and the data needed to perform localization in  conjunction with localization catalogs.</p>   <p>Clients of the VIM API may use vim.SessionManager.setLocale()  to cause the server to emit a localized <a href="vmodl.LocalizableMessage.md#message">message</a>, or may perform  client-side localization based on message catalogs provided by the  server.</p>   <ul>  <li>If the substition variable is a string, no further lookup is required.    <ul>      <li><a href="vmodl.LocalizableMessage.md#arg">arg</a> = [("address" = "127.0.0.1")]</li>      <li>CATALOG(locmsg, <a href="vmodl.LocalizableMessage.md#key">key</a>) = "IP address is {address}"</li>      <li>==&gt; <a href="vmodl.LocalizableMessage.md#message">message</a> = "IP address is 127.0.0.1"</li>    </ul>  </li>  <li>If the substitution variable is an integer, value is a lookup key.    <ul>      <li><a href="vmodl.LocalizableMessage.md#arg">arg</a> = [("1" = "button.cancel"), ("2" = "msg.revert")]</li>      <li>CATALOG(locmsg, <a href="vmodl.LocalizableMessage.md#key">key</a>) = "Select '{1}' to {2}"</li>      <li>CATALOG(locmsg, button.cancel) = "Cancel"</li>      <li>CATALOG(locmsg, msg.revert) = "revert"</li>      <li>==&gt; <a href="vmodl.LocalizableMessage.md#message">message</a> = "Select 'Cancel' to revert"</li>    </ul>  </li>  <li>If the variable contains '@', value is a label lookup in another  catalog, where {name.@CATALOG.prefix} looks up prefix.<a href="vmodl.LocalizableMessage.md#arg">arg</a>[name].label  in CATALOG.    <ul>      <li><a href="vmodl.LocalizableMessage.md#arg">arg</a> = [("field" = "queued")]</li>      <li>CATALOG(locmsg, <a href="vmodl.LocalizableMessage.md#key">key</a>) = "State is {field.@enum.TaskInfo.State}"</li>      <li>CATALOG(enum, TaskInfo.State.queued.label) is "Queued"</li>      <li>==&gt; <a href="vmodl.LocalizableMessage.md#message">message</a> = "State is Queued"</li>    </ul>  </li>  </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Unique key identifying the message in the localized message catalog. |
| arg | [vmodl.KeyAnyValue](vmodl.KeyAnyValue.md "vmodl.KeyAnyValue") | true | None | Substitution arguments for variables in the localized message. |
| message | string | true | None | Message in session locale.  Use vim.SessionManager.setLocale() to change the session locale. |


