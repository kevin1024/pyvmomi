vim.Extension.EventTypeInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type describes event types defined by the extension.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| eventID | string | None | None | The ID of the event type. Should follow java package   naming conventions for uniqueness. |
| eventTypeSchema | string | true | None | Optional XML descriptor for the EventType.    The structure of this descriptor is:  <code><pre>  &lt;EventType&gt;    &lt;eventTypeID&gt;<i>eventID</i>&lt;/eventTypeID&gt;    &lt;description&gt;Optional description for event eventID&lt;/description&gt;    <i>&lt!-- Optional arguments: --&gt;</i>    &lt;arguments&gt;       <i>&lt!-- Zero or more of: --&gt;</i>       &lt;argument&gt;         &lt;name&gt;<i>argName</i>&lt;/name&gt;         &lt;type&gt;<i>argtype</i>&lt;/name&gt;       &lt;/argument&gt;    &lt;/arguments&gt;  &lt;/EventType&gt;  </pre></code>    where <i>argtype</i> can be one of the following:  <ul>  <li><i>string</i>  <li><i>moid</i>  <li><i>long</i>  <li><i>int</i>  <li><i>bool</i>  </ul>    Note: <i>moid</i> is really just a string, with some additional  semantic meaning attached - that it is the identifier of some  object in the inventory, and can be looked up by a client that  is so inclined. |


