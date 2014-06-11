vim.LatencySensitivity
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Specification of the latency-sensitivity information.   <p />   The latency-sensitivity is used to request from the kernel a constraint   on the scheduling delay of the virtual CPUs or other resources. This allows   latency-sensitive applications(e.g. VOIP, audio/video streaming, etc.) to run   in a virtual machine which is configured to use specific scheduling   latencies and to be scheduled with low latency.   <p />   The kernel does not provide any guarantee that it will meet the   latency-sensitivity requirement of a virtual machine CPU or other resources   but it will always accept the latency-sensitivity value provided.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| level | [vim.LatencySensitivity.SensitivityLevel](vim.LatencySensitivity.SensitivityLevel.md "vim.LatencySensitivity.SensitivityLevel") | None | None | The nominal latency-sensitive level of the application. |
| sensitivity | int | true | None | The custom absolute latency-sensitivity value of the application.   This value will be used only when the latency-sensitivity   <a href="vim.LatencySensitivity.md#level">level</a> property is is set to   <code>custom</code>. It is ignored in all other cases.   <p />   The unit of this value is micro-seconds and the application is more   latency sensitive when this value is smaller. For example, if the   absolute latency-sensitivity is 2000us, the kernel will   try to schedule the virtual machine in a way so that its scheduling   latency is not more than 2ms. |


