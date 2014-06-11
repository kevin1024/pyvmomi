vim.event.EventDescription.EventDetail
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Each Event object provides an automatic event message string through   its <a href="vim.event.Event.md#fullFormattedMessage">fullFormattedMessage</a>    property. However, you can use the EventDetail object's properties to    format an event message string that is appropriate when viewed from    a specific context. The variable information (vm.name, and so on) is    derived from the Event object's event arguments    (<a href="vim.event.Event.md#vm">VmEventArgument</a>, and so on).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Type of event being described. |
| description | string | true | None | A string that is a short human-parseable description of the event.   <p>   This is not the full message string (which may contain details   of the arguments, etc.), but merely a more understandable, and   localized, description of what the event stands for. It is meant   for contexts where the <i>name</i> of the event has to be displayed   to end-users, e.g. when creating Event-based Alarms.  `     *  <p>   E.g., for <a href="vim.event.VmPoweredOnEvent.md">VmPoweredOnEvent</a>, the eventDescription   in English might say "VM Powered On". |
| category | string | None | None | A category of events. |
| formatOnDatacenter | string | None | None | A string that is appropriate in the context of a specific    Datacenter. For example, a renaming event in this context produces    the following string:   <p>      "Renamed {vm.name} from {oldName} to {newName}"   <p>   where <a href="vim.event.VmRenamedEvent.md#oldName">oldName</a> and    <a href="vim.event.VmRenamedEvent.md#newName">newName</a> are properties of the    VmRenamedEvent object. |
| formatOnComputeResource | string | None | None | A string that is appropriate in the context of a specific cluster.    For example, a powering on event in this context produces the    following string:   <p>      "{vm.name} on {host.name} is powered on". |
| formatOnHost | string | None | None | A string that is appropriate in the context    of a specific Host. For example, a powering on event in this    context produces the following string:   <p>      "{vm.name} is powered on" |
| formatOnVm | string | None | None | A string that is appropriate for the context of a specific    virtual machine. For example, a powering on event in this context    produces the following string:   <p>      "Virtual machine on {host.name} is powered on" |
| fullFormat | string | None | None | A string whose context is not entity-specific.  For example, a    powering on event produces the following string:   <p>      "{vm.name} on  {host.name} in {datacenter.name} is powered on" |
| longDescription | string | true | None | A detailed description of the event.  It includes common causes   and actions to remediate them.  It may also include links to kb   articles and other diagnostic information.   For example, the BadUserNameSessionEvent may produce the   following string:   <p>      <EventLongDescription id="vim.event.BadUserNameSessionEvent">         <description>            The user could not be logged in because of an unknown or invalid            user name.         </description>         <cause>            <description>The user name was unknown to the system</description>            <action>Use a user name known to the system user directory</action>            <action>(On Linux) Check if the user directory is correctly                    configured.</action>            <action>Check the health of the domain controller (if you are using                    Active Directory)</action>         </cause>         <cause>            <description>The user provided an invalid password</description>            <action>Supply the correct password</action>         </cause>      </EventLongDescription> |


