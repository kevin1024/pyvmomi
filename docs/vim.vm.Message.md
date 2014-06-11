vim.vm.Message
==============
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Message data which is intended to be displayed according  to the locale of a client.   <p>A <a href="vim.vm.Message.md">VirtualMachineMessage</a> contains both a formatted, localized version of the  text and the data needed to perform localization in conjunction  with localization catalogs.</p>   <p>Clients of the VIM API may use  <a href="vim.SessionManager.md">SessionManager</a>.<a href="vim.SessionManager.md#setLocale">SetLocale</a>  to cause the server to emit localized <a href="vim.vm.Message.md#text">text</a>, or may perform  client-side localization based on message catalogs provided by the  <a href="vim.LocalizationManager.md">LocalizationManager</a>.</p>   <p>Message variables are always integers, e.g. {1} and {2}, which are  1-based indexes into <a href="vim.vm.Message.md#argument">argument</a>.</p>   <ul>  <li>The corresponding argument may be a recursive lookup:    <ul>      <li><a href="vim.vm.Message.md#argument">argument</a> = ["button.cancel", "msg.revert"]</li>      <li>CATALOG(locmsg, <a href="vim.vm.Message.md#id">id</a>) = "Select '{1}' to {2}"</li>      <li>CATALOG(locmsg, button.cancel) = "Cancel"</li>      <li>CATALOG(locmsg, msg.revert) = "revert"</li>      <li>==&gt; <a href="vim.vm.Message.md#text">text</a> = "Select 'Cancel' to revert"</li>    </ul>  </li>  <li>If the recursive lookup fails, the argument is a plain string.    <ul>      <li><a href="vim.vm.Message.md#argument">argument</a> = ["127.0.0.1"]</li>      <li>CATALOG(locmsg, <a href="vim.vm.Message.md#id">id</a>) = "IP address is {1}"</li>      <li>==&gt; <a href="vim.vm.Message.md#text">text</a> "IP address is 127.0.0.1"</li>    </ul>  </li>  </ul><br>See <a href="vim.LocalizationManager.md">LocalizationManager</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | A unique identifier for this particular message.   This field is a key for looking up format strings in the locmsg  catalog. |
| argument | object | true | None | Substitution arguments for variables in the localized message.   Substitution variables in the format string identified by <a href="vim.vm.Message.md#id">id</a>  are 1-based indexes into this array. Substitution variable {1}  corresponds to argument[0], etc. |
| text | string | true | None | Text in session locale.  Use <a href="vim.SessionManager.md">SessionManager</a>.<a href="vim.SessionManager.md#setLocale">SetLocale</a> to  change the session locale. |


