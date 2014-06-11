vim.vApp.EntityConfigInfo
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This object type describes the  behavior of an entity (virtual machine or   sub-vApp container) in a vApp container.    <p>  The auto-start/auto-stop configurations control the behavior of the   start/stop vApp operations.   <p>   An virtual machine entity can be configured to wait for a period of time before   starting or to wait to receive a successful heartbeat from a virtual machine   before starting the next virtual machine in the sequence.    <ul>      <li>For a power-on operation, if waitForHeartbeat is true, then the power-on          sequence continues after the the first heartbeat has been received. If          waitingForGuest is false, the system waits for the specified delay and          then continues the power-on sequence.      <li>For a power-off operation, if delay is non-zero, the requested power-off          action is invoked (powerOff, suspend, guestShutdown) on the virtual          machine and the system waits until the number of seconds specified in the          delay have passed.    </ul>   If startAction and stopAction for an entity are both set to none, that   entity does not participate in the sequence.    <p>   The start/stop delay and waitingForGuest is not used if the entity is a   vApp container. For a vApp the only value values for startAction is none   or powerOn, and the valid values for stopAction is none or powerOff.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | Entity to power on or power off. This can be a virtual machine or a vApp. |
| tag | string | true | None | Tag for entity.  <p>  Reconfigure privilege: VApp.ApplicationConfig |
| startOrder | int | true | None | Specifies the start order for this entity. Entities are started from lower    numbers to higher-numbers and reverse on shutdown. Multiple entities with the    same start-order can be started in parallel and the order is unspecified. This   value must be 0 or higher.   <p>  Reconfigure privilege: VApp.ApplicationConfig |
| startDelay | int | true | None | Delay in seconds before continuing with the next entity in the order of entities   to be started.  <p>  Reconfigure privilege: VApp.ApplicationConfig |
| waitingForGuest | bool | true | None | Determines if the virtual machine should start after receiving a heartbeat,   from the guest. When a virtual machine is next in the start   order, the system either waits a specified period of time for a virtual   machine to power on or it waits until it receives a successful heartbeat from a   powered on virtual machine. By default, this is set to false.   <p>   This property has no effect for vApps.   <p>  Reconfigure privilege: VApp.ApplicationConfig |
| startAction | string | true | None | How to start the entity. Valid settings are none or powerOn.  If set to none, then   the entity does not participate in auto-start.  <p>  Reconfigure privilege: VApp.ApplicationConfig |
| stopDelay | int | true | None | Delay in seconds before continuing with the next entity in the order   sequence. This is only used if the stopAction is guestShutdown.  <p>  Reconfigure privilege: VApp.ApplicationConfig |
| stopAction | string | true | None | Defines the stop action for the entity. Can be set to none, powerOff,  guestShutdown, or suspend. If set to none, then the entity does not participate in  auto-stop.  <p>  Reconfigure privilege: VApp.ApplicationConfig |
| destroyWithParent | bool | true | None | Whether the entity should be removed, when this vApp is removed.  This is only set for linked children.  <p>  Reconfigure privilege: VApp.ApplicationConfig |


