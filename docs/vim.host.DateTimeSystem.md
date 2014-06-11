vim.host.DateTimeSystem
=======================
as of [VI API 2.5](vim.version.md#vim.version.version2)


This managed object provides for NTP and date/time related    configuration on a host.    Information regarding the running status of the NTP daemon and    functionality to start and stop the daemon is provided by the    <a href="vim.host.ServiceSystem.md">HostServiceSystem</a> object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='dateTimeInfo'>dateTimeInfo</a> | [vim.host.DateTimeInfo](vim.host.DateTimeInfo.md "vim.host.DateTimeInfo") | None | System.Read | The DateTime configuration of the host. |


UpdateDateTimeConfig([config](vim.host.DateTimeConfig.md "vim.host.DateTimeConfig"))
------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | UpdateDateTimeConfig |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Host.Config.DateTime |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if an error occurs. |




QueryAvailableTimeZones()
-------------------------

| service name | QueryAvailableTimeZones |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryDateTime()
---------------

| service name | QueryDateTime |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.Read |
| return type | [datetime](datetime.md "datetime") |
### Faults
| fault | description |
|:------|:------------|




UpdateDateTime([dateTime](#datetime "datetime"))
------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | UpdateDateTime |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Host.Config.DateTime |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if an error occurs. |




RefreshDateTimeSystem()
-----------------------

| service name | RefreshDateTimeSystem |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | Host.Config.DateTime |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




